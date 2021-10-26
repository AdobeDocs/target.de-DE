---
keywords: Kundenbetreuung;cname;Programm des Zertifikats;Kanonischer Name;Cookies;Zertifikat;amc;adobe-verwaltetes Zertifikat;Digicert;Validierung der Domänenkontrolle;dcv
description: Mit Adobe Client Care arbeiten, um CNAME (Canonical Name)-Unterstützung in der Adobe zu implementieren [!DNL Target] um Probleme mit der Anzeigenblockierung zu behandeln.
title: Wie verwende ich CNAME in der Zielgruppe?
feature: Privacy & Security
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
source-git-commit: e51c7805939e8bf32d7f358036c9070931580187
workflow-type: tm+mt
source-wordcount: '1165'
ht-degree: 1%

---

# CNAME und Zielgruppe

Anweisungen für die Arbeit mit [!DNL Adobe] Client Care zur Implementierung der CNAME-Unterstützung (kanonischer Name) in [!DNL Adobe Target]. Verwenden Sie CNAME, um Probleme mit der Anzeigenblockierung oder ITP-bezogene Cookie-Richtlinien (Intelligent Tracking Prevention) zu behandeln. Mit CNAME werden Aufrufe an eine Domäne des Kunden statt an eine Domäne im Besitz von [!DNL Adobe].

## CNAME-Unterstützung für Zielgruppe anfordern

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ unten).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Datensatz in Ihrem DNS, der auf Ihren regulären Namen verweist [!DNL Target] Hostname `clientcode.tt.omtrdc.net`.

   Wenn Ihr Client-Code z. B. &quot;cnamecustomer&quot; lautet und Ihr vorgeschlagener Hostname lautet `target.example.com`, sieht der DNS-CNAME-Datensatz ähnlich aus wie:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >Die Zertifizierungsstelle der Adobe, DigiCert, kann ein Zertifikat erst ausstellen, wenn dieser Schritt abgeschlossen ist. Daher [!DNL Adobe] kann Ihre Anforderung einer CNAME-Implementierung nicht erfüllen, bis dieser Schritt abgeschlossen ist.

1. [Füllen Sie dieses Formular aus](/help/assets/FPC_Request_Form.xlsx) und fügen Sie sie ein, wenn Sie [Adobe Client Care-Ticket öffnen und CNAME-Support anfordern](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * Adobe [!DNL Target] Client-Code:
   * Hostnamen für SSL-Zertifikat (Beispiel: `target.example.com target.example.org`):
   * SSL-Zertifikatkäufer (Adobe wird dringend empfohlen, siehe FAQ): Adobe/Kunde
   * Wenn der Kunde das Zertifikat (BYOC, &quot;Bring Your Own Certificate&quot;) kauft, füllen Sie die folgenden zusätzlichen Angaben aus:
      * Zertifikatorganisation (Beispiel: Beispiel Firma Inc.):
      * Organisationseinheit des Zertifikats (fakultativ, Beispiel: Marketing):
      * Zertifikatsland (Beispiel: USA):
      * Zertifikatsstatus/-region (Beispiel: Kalifornien):
      * Zertifikatstadt (Beispiel: San Jose):

1. Falls [!DNL Adobe] die Bescheinigung kauft, [!DNL Adobe] arbeitet mit DigiCert zusammen, um Ihr Zertifikat auf Produktionsservern der Adobe zu erwerben und bereitzustellen.

   Wenn der Kunde das Zertifikat kauft (BYOC), [!DNL Adobe] Client Care sendet Ihnen die Zertifikatssignaturanfrage (CSR). Verwenden Sie den CSR, wenn Sie das Zertifikat über Ihre Zertifizierungsstelle erwerben. Nachdem die Bescheinigung ausgestellt worden ist, senden Sie eine Kopie der Bescheinigung und der dazwischen liegenden Bescheinigungen an [!DNL Adobe] Client Care für die Bereitstellung.

   [!DNL Adobe] Client Care benachrichtigt Sie, wenn die Implementierung fertig ist.

1. Aktualisieren Sie die `serverDomain` ([Dokumentation](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#serverDomain)) auf den neuen CNAME-Hostnamen und -Satz `overrideMboxEdgeServer` nach `false` ([Dokumentation](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#overridemboxedgeserver)) in Ihrer at.js-Konfiguration.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren der CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat vorlegen (Eigenes Zertifikat mitbringen oder BYOC)?

Sie können Ihr eigenes Zertifikat bereitstellen. Jedoch [!DNL Adobe] empfiehlt diese Praxis nicht. Die Verwaltung des SSL-Zertifikatslebenszyklus ist für beide leichter [!DNL Adobe] und Sie, wenn [!DNL Adobe] das Zertifikat kauft und kontrolliert es. SSL-Zertifikate müssen jedes Jahr erneuert werden. Daher [!DNL Adobe] Die Kundenunterstützung muss sich jedes Jahr mit Ihnen in Verbindung setzen, um ein neues Zertifikat rechtzeitig zu erhalten. Manche Kunden können Schwierigkeiten haben, ein aktualisiertes Zertifikat zeitnah zu produzieren. Ihre [!DNL Target] die Implementierung wird gefährdet, wenn das Zertifikat abläuft, da Browser die Verbindung ablehnen.

>[!IMPORTANT]
>
>Wenn Sie eine [!DNL Target] bring-your-own-Certificate-CNAME-Implementierung, Sie sind dafür verantwortlich, erneuerte Zertifikate zur Verfügung zu stellen für [!DNL Adobe] Kundenbetreuung jedes Jahr. Das CNAME-Zertifikat läuft vor [!DNL Adobe] kann ein aktualisiertes Zertifikat bereitstellen führt zu einem Ausfall für Ihr spezifisches [!DNL Target] Umsetzung.

### Wie lange läuft mein neues SSL-Zertifikat ab?

Alle von der Adobe erworbenen Zertifikate sind ein Jahr lang gültig. Siehe [DigiCert-Artikel über 1-Jahres-Zertifikate](https://www.digicert.com/blog/position-on-1-year-certificates) für weitere Informationen.

### Welche Hostnamen soll ich wählen? Wie viele Hostnamen sollte ich pro Domäne wählen?

[!DNL Target] Für CNAME-Implementierungen ist nur ein Hostname pro Domäne im SSL-Zertifikat und im DNS des Kunden erforderlich. Adobe empfiehlt einen Hostnamen pro Domäne. Einige Kunden benötigen für ihre eigenen Zwecke mehr Hostnamen pro Domäne (z. B. Tests im Staging), was unterstützt wird.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`. Adobe empfiehlt, diesem Verfahren zu folgen, aber die Wahl liegt letztlich bei Ihnen. Anfordern Sie keinen Hostnamen eines vorhandenen DNS-Datensatzes. Dies führt zu einem Konflikt und verzögert die Zeit für die Lösung Ihrer [!DNL Target] CNAME-Anforderung.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics], kann ich das gleiche Zertifikat oder den gleichen Hostnamen verwenden?

Nein, [!DNL Target] erfordert einen separaten Hostnamen und ein separates Zertifikat.

### Ist meine aktuelle Implementierung von [!DNL Target] von ITP 2.x beeinflusst?

Apple Intelligent Tracking Prevention (ITP), Version 2.3, hat die CNAME Cloaking Mitigation-Funktion eingeführt, mit der Adobe Target CNAME-Implementierungen erkannt und der Ablauf des Cookies auf sieben Tage reduziert werden kann. Zurzeit [!DNL Target] hat keine Problemumgehung für die CNAME-Cloaking-Minderung von ITP. Weitere Informationen über ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).


### Welche Art von Service-Unterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats ist keine Dienstunterbrechung aufgetreten (einschließlich Zertifikatsverlängerungen).

Nachdem Sie jedoch den Hostnamen in Ihrem [!DNL Target] Implementierungscode (`serverDomain` in at.js dem neuen CNAME-Hostnamen (`target.example.com`), behandeln Webbrowser rückkehrende Besucher als neue Besucher. Die Daten des Profils des rückkehrenden Besuchers gehen verloren, da der Zugriff auf das vorherige Cookie unter dem alten Hostnamen nicht möglich ist (`clientcode.tt.omtrdc.net`). Der Zugriff auf das vorherige Cookie ist aufgrund von Sicherheitsmodellen im Browser nicht möglich. Diese Störung tritt nur beim ersten Cut-over zum neuen CNAME auf. Zertifikatverlängerungen haben nicht denselben Effekt, da sich der Hostname nicht ändert.

### Welcher Schlüsseltyp und welcher Zertifikatssignaturalgorithmus wird für meine CNAME-Implementierung verwendet?

Alle Zertifikate sind RSA SHA-256 und die Schlüssel sind standardmäßig RSA 2048-bit. Schlüsselgrößen, die größer als 2048 Bit sind, werden derzeit nicht unterstützt.

### Wie kann ich überprüfen, ob meine CNAME-Implementierung Traffic-bereit ist?

Verwenden Sie die folgenden Befehle (im macOS- oder Linux-Befehlszeilenterminal mit bash und curl >=7.49):

1. Kopieren Sie diese Bash-Funktion und fügen Sie sie in Ihr Terminal ein oder fügen Sie sie in Ihre Bash-Startskriptdatei ein (normalerweise `~/.bash_profile` oder `~/.bashrc`), damit die Funktion über Terminalsitzungen hinweg verfügbar ist:

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

1. Diesen Befehl einfügen (ersetzen) `target.example.com` mit Ihrem Hostnamen):

   ```
   adobeTargetCnameValidation target.example.com
   ```

   Wenn die Implementierung bereit ist, wird die Ausgabe wie unten dargestellt. Wichtig ist, dass alle Zeilen des Validierungsstatus angezeigt werden `✅` statt `🚫`. Jeden [!DNL Target] Edge CNAME SHARD muss angezeigt werden `CN=target.example.com`, der dem primären Hostnamen im angeforderten Zertifikat entspricht (zusätzliche SAN-Hostnamen im Zertifikat werden in dieser Ausgabe nicht gedruckt).

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
   >Wenn dieser Überprüfungsbefehl bei der DNS-Validierung fehlschlägt, Sie jedoch bereits die erforderlichen DNS-Änderungen vorgenommen haben, müssen Sie möglicherweise warten, bis Ihre DNS-Aktualisierungen vollständig übertragen werden. DNS-Datensätze sind verknüpft [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) die die Cache-Gültigkeitsdauer für DNS-Antworten dieser Datensätze vorschreibt. Daher müssen Sie möglicherweise mindestens so lange warten, wie Ihre TTLs. Sie können `dig target.example.com` Befehl oder [die G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) um Ihre spezifischen TTLs nachzuschlagen. Informationen zur Überprüfung der DNS-Verbreitung auf der ganzen Welt finden Sie unter [whatsmydns.net](https://whatsmydns.net/#CNAME).

### Wie verwende ich einen Ausschluss-Link mit CNAME?

Wenn Sie CNAME verwenden, sollte der Abmelde-Link den &quot;client=`clientcode` Parameter, z. B.:
`https://my.cname.domain/optout?client=clientcode`.

Ersetzen `clientcode` mit Ihrem Clientcode und fügen Sie dann den Text oder das Bild hinzu, der/das mit dem [Abmelde-URL](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#reference_E7A62B7B99C94B3A806CB262D16E27FC).

## Bekannte Einschränkungen

* Der QA-Modus ist nicht fixierbar, wenn Sie CNAME und at.js 1.x haben, da er auf einem Drittanbieter-Cookie basiert. Die Behelfslösung besteht darin, den einzelnen URL, zu denen Sie navigieren, die Parameter für die Vorschau hinzuzufügen. Der QA-Modus ist fixierbar, wenn Sie CNAME und at.js 2.x haben.
* Bei der Verwendung von CNAME ist es wahrscheinlicher, dass die Größe des Cookie-Headers für [!DNL Target] Anrufe zunehmen. [!DNL Adobe] empfiehlt, die Cookie-Größe unter 8 KB zu halten.
