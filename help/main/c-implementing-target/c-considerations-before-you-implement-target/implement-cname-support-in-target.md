---
keywords: Client Care;CNAME;Zertifikatsprogramm;kanonischer Name;Cookies;Zertifikat;AMC;Adobe-verwaltetes Zertifikat;Digest;Domain-Steuerelement-Validierung;DCV
description: Arbeiten mit [!DNL Adobe] Kundenunterstützung zur Implementierung der CNAME-Unterstützung (Canonical Name) in [!DNL Adobe Target] um Probleme mit der Anzeigenblockierung zu beheben.
title: Wie verwende ich CNAME in Target?
feature: Privacy & Security
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 1%

---

# CNAME und [!DNL Target]

Anweisungen für die Arbeit mit [!DNL Adobe] Kundenunterstützung zur Implementierung der CNAME-Unterstützung (Canonical Name) in [!DNL Adobe Target]. Verwenden Sie CNAME, um Probleme mit der Anzeigenblockierung oder ITP-bezogene Cookie-Richtlinien (Intelligent Tracking Prevention) zu verarbeiten. Mit CNAME werden Aufrufe an eine Domäne gesendet, die dem Kunden gehört, und nicht an eine Domäne im Besitz von [!DNL Adobe].

## CNAME-Unterstützung anfordern in [!DNL Target]

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ unten).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Eintrag in Ihrem DNS, der auf Ihren regulären Namen verweist. [!DNL Target] hostname `clientcode.tt.omtrdc.net`.

   Wenn Ihr Clientcode beispielsweise &quot;cnameccustomer&quot;lautet und Ihr Hostname vorgeschlagen wird, lautet `target.example.com`, sieht Ihr DNS-CNAME-Eintrag ähnlich aus:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >[!DNL Adobe]Die Zertifizierungsstelle von DigiCert kann erst nach Abschluss dieses Schritts ein Zertifikat ausstellen. Daher [!DNL Adobe] kann Ihre Anfrage nach einer CNAME-Implementierung erst erfüllen, wenn dieser Schritt abgeschlossen ist.

1. [Füllen Sie dieses Formular aus](/help/main/assets/FPC_Request_Form.xlsx) und schließen Sie sie ein, wenn Sie [Öffnen Sie eine [!DNL Adobe] Kundenunterstützungs-Ticket, in dem CNAME-Unterstützung angefordert wird](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * [!DNL Adobe Target] client code:
   * SSL-Zertifikat-Hostnamen (Beispiel: `target.example.com target.example.org`):
   * SSL-Zertifikatkäufer ([!DNL Adobe] wird dringend empfohlen, siehe FAQ): Adobe/Kunde
   * Wenn der Kunde das Zertifikat kauft, auch bekannt als &quot;Bring Your Own Certificate&quot;(BYOC), füllen Sie diese zusätzlichen Details aus:
      * Zertifikatorganisation (Beispiel: Beispiel: Firma Inc):
      * Organisationseinheit Zertifikat (optional, Beispiel: Marketing):
      * Zertifikatstaat (Beispiel: US):
      * Zertifikatstatus/-region (Beispiel: Kalifornien):
      * Zertifikatstadt (Beispiel: San Jose):

1. Wenn [!DNL Adobe] die Bescheinigung erworben hat, [!DNL Adobe] verwendet DigiCert, um Ihr Zertifikat zu erwerben und bereitzustellen in [!DNL Adobe]Produktionsserver.

   Wenn der Kunde das Zertifikat (BYOC) kauft, [!DNL Adobe] ClientCare sendet Ihnen die Anforderung zur Zertifikatsignierung (CSR). Verwenden Sie die CSR, wenn Sie das Zertifikat über Ihre Zertifizierungsstelle Ihrer Wahl erwerben. Nach Erteilung des Zertifikats senden Sie eine Kopie des Zertifikats und etwaiger Zwischenzertifikate an [!DNL Adobe] Kundenunterstützung für die Bereitstellung.

   [!DNL Adobe] Der Kundendienst benachrichtigt Sie, wenn Ihre Implementierung bereit ist.

1. Aktualisieren Sie die `serverDomain` ([Dokumentation](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)) auf den neuen CNAME-Hostnamen und legen Sie `overrideMboxEdgeServer` nach `false` ([Dokumentation](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)) in Ihrer at.js-Konfiguration.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat bereitstellen (Eigenes Zertifikat mitbringen oder BYOC)?

Sie können Ihr eigenes Zertifikat bereitstellen. Allerdings [!DNL Adobe] empfiehlt diese Vorgehensweise nicht. Die Verwaltung des SSL-Zertifikatlebenszyklus ist für beide leichter [!DNL Adobe] und wenn [!DNL Adobe] bestellt und kontrolliert das Zertifikat. SSL-Zertifikate müssen jedes Jahr erneuert werden. Daher [!DNL Adobe] Der Kundendienst muss sich jedes Jahr mit Ihnen in Verbindung setzen, um rechtzeitig ein neues Zertifikat zu erhalten. Einige Kunden können Schwierigkeiten haben, ein neues Zertifikat zeitnah zu erstellen. Ihre [!DNL Target] -Implementierung wird gefährdet, wenn das Zertifikat abläuft, da Browser Verbindungen ablehnen.

>[!IMPORTANT]
>
>Wenn Sie eine [!DNL Target] CNAME-Implementierung für das eigene Zertifikat mitbringen, sind Sie dafür verantwortlich, erneuerte Zertifikate für [!DNL Adobe] Kundenunterstützung jedes Jahr. Gültigkeit Ihres CNAME-Zertifikats vor [!DNL Adobe] kann ein neues Zertifikat bereitstellen, was zu einem Ausfall für Ihre spezifischen [!DNL Target] Implementierung.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Alle [!DNL Adobe]-erworbene Zertifikate sind ein Jahr lang gültig. Siehe [Artikel von DigiCert zu 1-Jahres-Zertifikaten](https://www.digicert.com/blog/position-on-1-year-certificates) für weitere Informationen.

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] CNAME-Implementierungen erfordern nur einen Hostnamen pro Domäne auf dem SSL-Zertifikat und im DNS des Kunden. [!DNL Adobe] empfiehlt einen Hostnamen pro Domäne. Einige Kunden benötigen für ihre eigenen Zwecke (z. B. Tests im Staging) mehr Hostnamen pro Domäne, was unterstützt wird.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`. [!DNL Adobe] empfiehlt, dieser Praxis zu folgen, aber die Wahl liegt letztendlich bei Ihnen. Fordern Sie keinen Hostnamen eines vorhandenen DNS-Eintrags an. Dies führt zu einem Konflikt und verzögert die Behebung Ihrer [!DNL Target] CNAME-Anfrage.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics]Kann ich dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, [!DNL Target] erfordert einen separaten Hostnamen und ein separates Zertifikat.

### Ist meine aktuelle Implementierung von [!DNL Target] von ITP 2.x beeinflusst?

Apple Intelligent Tracking Prevention (ITP) Version 2.3 führte die CNAME Cloaking Mitigation-Funktion ein, die in der Lage ist, [!DNL Adobe Target] CNAME-Implementierungen und reduzieren die Gültigkeit des Cookies auf sieben Tage. Aktuell [!DNL Target] gibt keine Problemumgehung für die CNAME-Cloaking-Abmilderung von ITP. Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](https://developer.adobe.com/target/before-implement/privacy/apple-itp-2x/).

### Welche Arten von Dienstunterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats gibt es keine Dienstunterbrechung (einschließlich Zertifikatsverlängerungen).

Nachdem Sie jedoch den Hostnamen in Ihrem [!DNL Target] Implementierungscode (`serverDomain` in at.js) auf den neuen CNAME-Hostnamen (`target.example.com`), behandeln Webbrowser wiederkehrende Besucher als neue Besucher. Die Profildaten der zurückgegebenen Besucher gehen verloren, da der Zugriff auf das vorherige Cookie unter dem alten Hostnamen (`clientcode.tt.omtrdc.net`). Der Zugriff auf das vorherige Cookie ist aufgrund von Browser-Sicherheitsmodellen nicht möglich. Diese Störung tritt nur beim ersten Cut-over auf den neuen CNAME auf. Zertifikatverlängerungen haben nicht die gleiche Wirkung, da sich der Hostname nicht ändert.

### Welcher Schlüsseltyp und welcher Zertifikatsignaturalgorithmus wird für meine CNAME-Implementierung verwendet?

Alle Zertifikate sind RSA SHA-256 und Schlüssel sind standardmäßig RSA 2048-Bit. Größen, die größer als 2048 Bit sind, werden derzeit nicht unterstützt.

### Wie kann ich überprüfen, ob meine CNAME-Implementierung für Traffic bereit ist?

Verwenden Sie den folgenden Befehlssatz (im Befehlszeilen-Terminal von macOS oder Linux mit bash und curl >=7.49):

1. Kopieren Sie diese Bash-Funktion und fügen Sie sie in Ihr Terminal ein oder fügen Sie die Funktion in Ihre Bash-Startskriptdatei ein (normalerweise `~/.bash_profile` oder `~/.bashrc`), damit die Funktion über alle Terminalsitzungen hinweg verfügbar ist:

   ```
   function adobeTargetCnameValidation {
     local hostname="$1"
     if [ -z "$hostname" ]; then
       echo "ERROR: no hostname specified"
       return 1
     fi
   
     local service="Adobe Target CNAME implementation"
     local edges="31 32 34 35 36 37 38"
     local edgeDomain="tt.omtrdc.net"
     local edgeFormat="mboxedge%d%s.$edgeDomain"
     local shardFormat="-alb%02d"
     local shards=5
     local shardsFoundCount=0
     local shardsFound
     local shardsFoundOutput
     local curlRegex="subject:.*CN=|expire date:|issuer:"
     local curlValidation="SSL certificate verify ok"
     local curlResponseValidation='"OK"'
     local curlEndpoint="/uptime?mboxClient=uptime3"
     local url="https://$hostname$curlEndpoint"
     local sslLabsUrl="https://ssllabs.com/ssltest/analyze.html?hideResults=on&latest&d=$hostname"
     local success="✅"
     local failure="🚫"
     local info="🔎"
     local rule="="
     local horizontalRule="$(seq ${COLUMNS:-30} | xargs printf "$rule%.0s")"
     local miniRule="$(seq 5 | xargs printf "$rule%.0s")"
     local curlVersion="$(curl --version | head -1 | cut -d' ' -f2 )"
     local curlVersionRequired=">=7.49"
     local edgeCount="$(wc -w <<< "$edges" | tr -d ' ')"
     local edge
     local shard
     local currEdgeShard
     local dnsOutput
     local cnameExists
     local endToEndTestSucceeded
     local curlResult
   
     for shard in $(seq $shards); do
       if [ "$shardsFoundCount" -eq 0 ]; then
         for edge in $edges; do
           if [ "$shard" -eq 1 ]; then
             currEdgeShard="$(printf "$edgeFormat" "$edge" "")"
           else
             currEdgeShard="$(
               printf "$edgeFormat" "$edge" "$(
                 printf -- "$shardFormat" "$shard"
               )"
             )"
           fi
           curlResult="$(curl -vsm20 --connect-to "$hostname:443:$currEdgeShard:443" "$url" 2>&1)"
           if grep -q "$curlValidation" <<< "$curlResult"; then
             shardsFound+=" $currEdgeShard"
             if grep -q "$curlResponseValidation" <<< "$curlResult"; then
               shardsFoundCount=$((shardsFoundCount+1))
               shardsFoundOutput+="\n\n$miniRule $success $hostname [edge shard: $currEdgeShard] $miniRule\n"
             else
               shardsFoundOutput+="\n\n$miniRule $failure $hostname [edge shard: $currEdgeShard] $miniRule\n"
             fi
             shardsFoundOutput+="$(grep -E "$curlRegex" <<< "$curlResult" | sort)"
             if ! grep -q "$curlResponseValidation" <<< "$curlResult"; then
               shardsFoundOutput+="\nERROR: unexpected HTTP response from this shard using $url"
             fi
           fi
         done
       fi
     done
   
     echo
     echo "$horizontalRule"
     echo
     echo "$service validation for hostname $hostname:"
     dnsOutput="$(dig -t CNAME +short "$hostname" 2>&1)"
     if grep -qFi ".$edgeDomain" <<< "$dnsOutput"; then
       echo "$success $hostname passes DNS CNAME validation"
       cnameExists=true
     else
       echo -n "$failure $hostname FAILED DNS CNAME validation -- "
       if [ -n "$dnsOutput" ]; then
         echo -e "$dnsOutput is not in the subdomain $edgeDomain"
       else
         echo "required DNS CNAME record pointing to <target-client-code>.$edgeDomain not found"
       fi
     fi
   
     curlResult="$(curl -vsm20 "$url" 2>&1)"
     if grep -q "$curlValidation" <<< "$curlResult"; then
       if grep -q "$curlResponseValidation" <<< "$curlResult"; then
         echo -en "$success $hostname passes TLS and HTTP response validation"
         if [ -n "$cnameExists" ]; then
           echo
         else
           echo " -- the DNS CNAME is not pointing to the correct subdomain for ${service}s with Adobe-managed certificates" \
             "(bring-your-own-certificate implementations don't have this requirement), but this test passes as configured"
         fi
         endToEndTestSucceeded=true
       else
         echo -n "$failure $hostname FAILED HTTP response validation --" \
           "unexpected response from $url -- "
         if [ -n "$cnameExists" ]; then
           echo "DNS is NOT pointing to the correct shard, notify Adobe Client Care"
         else
           echo "the required DNS CNAME record is missing, see above"
         fi
       fi
     else
   
       echo -n "$failure $hostname FAILED TLS validation -- "
       if [ -n "$cnameExists" ]; then
         echo "DNS is likely NOT pointing to the correct shard or there's a validation issue with the certificate or" \
           "protocols, see curl output below and optionally SSL Labs ($sslLabsUrl):"
         echo ""
         echo "$horizontalRule"
         echo "$curlResult" | sed 's/^/    /g'
         echo "$horizontalRule"
         echo ""
       else
         echo "the required DNS CNAME record is missing, see above"
       fi
     fi
   
     if [ "$shardsFoundCount" -ge "$edgeCount" ]; then
       echo -n "$success $hostname passes shard validation for the following $shardsFoundCount edge shards:"
       echo -e "$shardsFoundOutput"
       echo
   
       if [ -n "$cnameExists" ] && [ -n "$endToEndTestSucceeded" ]; then
         echo "$horizontalRule"
         echo ""
         echo "  For additional TLS/SSL validation, including detailed browser/client support,"
         echo "  see SSL Labs (click the first IP address if prompted):"
         echo ""
         echo "    $info  $sslLabsUrl"
         echo ""
         echo "  To check DNS propagation around the world, see whatsmydns.net:"
         echo ""
         echo "    $info  DNS A records:     https://whatsmydns.net/#A/$hostname"
         echo "    $info  DNS CNAME record:  https://whatsmydns.net/#CNAME/$hostname"
       fi
     else
       echo -n "$failure $hostname FAILED shard validation -- shards found: $shardsFoundCount," \
         "expected: $edgeCount"
       if bc -l <<< "$(cut -d. -f1,2 <<< "$curlVersion") $curlVersionRequired" 2>/dev/null | grep -q 0; then
         echo -n " -- insufficient curl version installed: $curlVersion, but this script requires curl version" \
           "$curlVersionRequired because it uses the curl --connect-to flag to bypass DNS and directly test" \
           "each Adobe Target edge shards' SNI confirguation for $hostname"
       fi
       if [ -n "$shardsFoundOutput" ]; then
         echo -e ":\n$shardsFoundOutput"
       fi
       echo
     fi
     echo
     echo "$horizontalRule"
     echo
   }
   ```

1. Fügen Sie diesen Befehl ein (ersetzen `target.example.com` mit Ihrem Hostnamen):

   ```
   adobeTargetCnameValidation target.example.com
   ```

   Wenn die Implementierung bereit ist, sehen Sie die Ausgabe wie unten dargestellt. Wichtig ist, dass alle Validierungsstatuszeilen `✅` anstelle von `🚫`. Jeder [!DNL Target] Edge-CNAME-Shard sollte zeigen `CN=target.example.com`, der mit dem primären Hostnamen im angeforderten Zertifikat übereinstimmt (zusätzliche SAN-Hostnamen auf dem Zertifikat werden in dieser Ausgabe nicht gedruckt).

   ```
   $ adobeTargetCnameValidation target.example.com
   
   ==========================================================
   
   Adobe Target CNAME implementation validation for hostname target.example.com:
   ✅ target.example.com passes DNS CNAME validation
   ✅ target.example.com passes TLS and HTTP response validation
   ✅ target.example.com passes shard validation for the following 7 edge shards:
   
   ===== ✅ target.example.com [edge shard: mboxedge31-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge32-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge34-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge35-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge36-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge37-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge38-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ==========================================================
   
     For additional TLS/SSL validation, including detailed browser/client support,
     see SSL Labs (click the first IP address if prompted):
   
       🔎  https://ssllabs.com/ssltest/analyze.html?hideResults=on&latest&d=target.example.com
   
     To check DNS propagation around the world, see whatsmydns.net:
   
       🔎  DNS A records:     https://whatsmydns.net/#A/target.example.com
       🔎  DNS CNAME record:  https://whatsmydns.net/#CNAME/target.example.com
   
   ==========================================================
   ```

   >[!NOTE]
   >
   >Wenn dieser Überprüfungsbefehl bei der DNS-Validierung fehlschlägt, Sie jedoch bereits die erforderlichen DNS-Änderungen vorgenommen haben, müssen Sie möglicherweise warten, bis Ihre DNS-Updates vollständig propagiert werden. DNS-Einträge sind mit [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) die die Cache-Ablaufzeit für DNS-Antworten dieser Datensätze vorgibt. Daher müssen Sie möglicherweise mindestens so lange warten wie Ihre TTLs. Sie können die `dig target.example.com` Befehl oder [G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) , um Ihre spezifischen TTLs nachzuschlagen. Informationen zur Überprüfung der DNS-Verbreitung auf der ganzen Welt finden Sie unter [whatsmydns.net](https://whatsmydns.net/#CNAME).

### Wie verwende ich einen Ausschluss-Link mit CNAME?

Wenn Sie CNAME verwenden, sollte der Ausschluss-Link den Wert &quot;client=&quot;enthalten.`clientcode` -Parameter, z. B.:
`https://my.cname.domain/optout?client=clientcode`.

Ersetzen `clientcode` mit Ihrem Clientcode verwenden, fügen Sie dann den Text oder das Bild hinzu, das mit der [Ausschluss-URL](https://developer.adobe.com/target/before-implement/privacy/privacy/).

## Bekannte Einschränkungen

* Der QA-Modus ist nicht fixierbar, wenn Sie CNAME und at.js 1.x verwenden, da er auf einem Drittanbieter-Cookie basiert. Um dieses Problem zu umgehen, fügen Sie jeder URL, zu der Sie navigieren, die Vorschauparameter hinzu. Der QS-Modus hängt bei CNAME und at.js 2.x an.
* Bei Verwendung von CNAME wird es wahrscheinlicher, dass die Größe des Cookie-Headers für [!DNL Target] -Aufrufe zunehmen. [!DNL Adobe] empfiehlt, die Cookie-Größe unter 8 KB zu halten.
