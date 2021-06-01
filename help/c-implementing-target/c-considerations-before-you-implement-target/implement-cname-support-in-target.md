---
keywords: Client Care;CNAME;Zertifikatsprogramm;kanonischer Name;Cookies;Zertifikat;AMC;Adobe-verwaltetes Zertifikat;Digest;Domain-Steuerelement-Validierung;DCV
description: Wenden Sie sich an den Kundendienst von Adobe, um die CNAME-Unterstützung (Canonical Name) in Adobe [!DNL Target] zu implementieren, um Probleme mit der Anzeigenblockierung oder ITP-bezogene Cookie-Richtlinien zu handhaben.
title: Wie verwende ich CNAME in Target?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
source-git-commit: 1f27ebfb7fb4203558f4d10e5e98cced04a82f2b
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 1%

---

# CNAME und Target

Anleitung zum Arbeiten mit [!DNL Adobe] Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in [!DNL Adobe Target]. Verwenden Sie CNAME, um Probleme mit der Anzeigenblockierung oder ITP-bezogene Cookie-Richtlinien (Intelligent Tracking Prevention) zu verarbeiten. Mit CNAME werden Aufrufe an eine Domäne gesendet, die dem Kunden gehört, und nicht an eine Domäne, die [!DNL Adobe] gehört.

## Unterstützung von CNAME anfordern in Target

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ unten).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Eintrag in Ihrem DNS, der auf Ihren regulären [!DNL Target] Hostnamen `clientcode.tt.omtrdc.net` verweist.

   Wenn Ihr Clientcode beispielsweise &quot;cnameccustomer&quot;lautet und Ihr Hostname `target.example.com` lautet, sieht Ihr DNS-CNAME-Eintrag ähnlich aus wie:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >Die Zertifizierungsstelle der Adobe, DigiCert, kann erst nach Abschluss dieses Schritts ein Zertifikat ausstellen. Daher kann [!DNL Adobe] Ihre Anfrage nach einer CNAME-Implementierung erst erfüllen, wenn dieser Schritt abgeschlossen ist.

1. [Füllen Sie dieses ](/help/assets/FPC_Request_Form.xlsx) Formular aus und fügen Sie es ein, wenn Sie ein Adobe Client Care-Ticket  [öffnen, in dem CNAME-Unterstützung angefordert wird](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * Adobe [!DNL Target] Clientcode:
   * SSL-Zertifikat-Hostnamen (Beispiel: `target.example.com target.example.org`):
   * SSL-Zertifikatkäufer (Adobe wird dringend empfohlen, siehe FAQ): Adobe/Kunde
   * Wenn der Kunde das Zertifikat kauft, auch bekannt als &quot;Bring Your Own Certificate&quot;(BYOC), füllen Sie diese zusätzlichen Details aus:
      * Zertifikatorganisation (Beispiel: Beispiel: Firma Inc):
      * Organisationseinheit Zertifikat (optional, Beispiel: Marketing):
      * Zertifikatstaat (Beispiel: US):
      * Zertifikatstatus/-region (Beispiel: Kalifornien):
      * Zertifikatstadt (Beispiel: San Jose):

1. Wenn [!DNL Adobe] das Zertifikat kauft, kauft [!DNL Adobe] Ihr Zertifikat bei DigiCert und stellt es auf den Produktionsservern der Adobe bereit.

   Wenn der Kunde das Zertifikat (BYOC) kauft, sendet Ihnen [!DNL Adobe] Client Care die Certificate Signing Request (CSR). Verwenden Sie die CSR, wenn Sie das Zertifikat über Ihre Zertifizierungsstelle Ihrer Wahl erwerben. Nachdem das Zertifikat ausgestellt wurde, senden Sie eine Kopie des Zertifikats und etwaiger Zwischenzertifikate zur Bereitstellung an [!DNL Adobe] Client Care.

   [!DNL Adobe] Der Kundendienst benachrichtigt Sie, wenn Ihre Implementierung bereit ist.

1. Aktualisieren Sie `serverDomain` auf den neuen CNAME in at.js.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat bereitstellen (Eigenes Zertifikat mitbringen oder BYOC)?

Sie können Ihr eigenes Zertifikat bereitstellen. [!DNL Adobe] empfiehlt diese Vorgehensweise jedoch nicht. Die Verwaltung des SSL-Zertifikatlebenszyklus ist sowohl für [!DNL Adobe] als auch für Sie einfacher, wenn [!DNL Adobe] das Zertifikat kauft und steuert. SSL-Zertifikate müssen jedes Jahr erneuert werden. Daher muss sich [!DNL Adobe] Client Care jedes Jahr an Sie wenden, um ein neues Zertifikat rechtzeitig zu erhalten. Einige Kunden können Schwierigkeiten haben, ein neues Zertifikat zeitnah zu erstellen. Ihre [!DNL Target]-Implementierung ist gefährdet, wenn das Zertifikat abläuft, da Browser Verbindungen ablehnen.

>[!IMPORTANT]
>
>Wenn Sie eine [!DNL Target] CNAME-Implementierung für Ihr eigenes Zertifikat anfordern, sind Sie dafür verantwortlich, [!DNL Adobe] Kundenunterstützung jedes Jahr erneuerte Zertifikate bereitzustellen. Wenn Sie zulassen, dass Ihr CNAME-Zertifikat abläuft, bevor [!DNL Adobe] ein neues Zertifikat bereitstellen kann, tritt ein Ausfall für Ihre spezifische [!DNL Target]-Implementierung auf.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Vor dem 1. September 2020 ausgestellte Bescheinigungen sind zweijährige Bescheinigungen. Zertifikate, die am oder nach dem 1. September 2020 ausgestellt wurden, sind einjährige Zertifikate. Weitere Informationen zum Umstieg auf einjährige Zertifikate [finden Sie hier](https://www.digicert.com/position-on-1-year-certificates).

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] CNAME-Implementierungen erfordern nur einen Hostnamen pro Domäne auf dem SSL-Zertifikat und im DNS des Kunden. Adobe empfiehlt einen Hostnamen. Einige Kunden benötigen für ihre eigenen Zwecke (z. B. Tests im Staging) mehr Hostnamen pro Domäne, was unterstützt wird.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`. Adobe empfiehlt, dieser Praxis zu folgen, aber die Wahl liegt letztendlich bei Ihnen. Fordern Sie keinen Hostnamen eines vorhandenen DNS-Eintrags an. Dies führt zu einem Konflikt und verzögert die Zeit für die Lösung Ihrer [!DNL Target] CNAME-Anfrage.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics]. Können wir dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, [!DNL Target] erfordert einen separaten Hostnamen und ein separates Zertifikat.

### Ist meine aktuelle Implementierung von [!DNL Target] von ITP 2.x betroffen?

Navigieren Sie in einem Safari-Browser zu der Website, auf der Sie eine JavaScript -Bibliothek für [!DNL Target] haben. Wenn ein [!DNL Target]-Cookie im Kontext eines CNAME gesetzt wird, z. B. `analytics.company.com`, sind Sie von ITP 2.x nicht betroffen.

ITP-Probleme können für [!DNL Target] mit nur einem [!DNL Analytics] CNAME behoben werden. Sie benötigen einen separaten [!DNL Target] CNAME nur in Ad-Blocking-Szenarien, in denen [!DNL Target] blockiert ist.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welche Arten von Dienstunterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats gibt es keine Dienstunterbrechung (einschließlich Zertifikatsverlängerungen).

Nachdem Sie jedoch den Hostnamen im [!DNL Target]-Implementierungscode (`serverDomain` in at.js) in den neuen CNAME-Hostnamen (`target.example.com`) geändert haben, behandeln Webbrowser wiederkehrende Besucher als neue Besucher. Die Rückgabe der Profildaten der Besucher geht verloren, da der Zugriff auf das vorherige Cookie unter dem alten Hostnamen (`clientcode.tt.omtrdc.net`) nicht möglich ist. Der Zugriff auf das vorherige Cookie ist aufgrund von Browser-Sicherheitsmodellen nicht möglich. Diese Störung tritt nur beim ersten Cut-over auf den neuen CNAME auf. Zertifikatverlängerungen haben nicht die gleiche Wirkung, da sich der Hostname nicht ändert.

### Welcher Schlüsseltyp und welcher Zertifikatsignaturalgorithmus wird für meine CNAME-Implementierung verwendet?

Alle Zertifikate sind RSA SHA-256 und Schlüssel sind standardmäßig RSA 2048-Bit. Größen, die größer als 2048 Bit sind, werden derzeit nicht unterstützt.

### Wie kann ich überprüfen, ob meine CNAME-Implementierung für Traffic bereit ist?

Verwenden Sie den folgenden Satz von Befehlen (im Befehlszeilen-Terminal macOS oder Linux mit bash und curl 7.49+):

1. Fügen Sie diese Bash-Funktion in Ihr Terminal ein:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Fügen Sie diesen Befehl ein (ersetzen Sie `target.example.com` durch Ihren Hostnamen):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Wenn die Implementierung bereit ist, sehen Sie die Ausgabe wie unten dargestellt. Wichtig ist, dass alle Zeilen `CN=target.example.com` enthalten, was dem gewünschten Hostnamen entspricht. Wenn Zeilen `CN=*.tt.omtrdc.net` enthalten, ist die Implementierung **nicht** bereit.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge36.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Validieren Sie Ihren neuen DNS-CNAME mit einer anderen curl-Anfrage, die auch `CN=target.example.com` anzeigen sollte:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Wenn dieser Befehl fehlschlägt, der obige `validateEdgeFpsslSni`-Befehl jedoch erfolgreich ist, warten Sie, bis Ihre DNS-Updates vollständig propagiert werden. DNS-Einträge haben eine zugewiesene [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records)-Kennung, die die Cache-Ablaufzeit für DNS-Antworten dieser Datensätze vorschreibt. Daher müssen Sie möglicherweise mindestens so lange warten wie Ihre TTLs. Sie können den Befehl `dig target.example.com` oder [die G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) verwenden, um Ihre spezifischen TTLs nachzuschlagen.

### Wie verwende ich einen Ausschluss-Link mit CNAME?

Wenn Sie CNAME verwenden, sollte der Ausschluss-Link den Parameter &quot;client=`clientcode`&quot;enthalten, z. B.:
`https://my.cname.domain/optout?client=clientcode`.

Ersetzen Sie `clientcode` durch Ihren Clientcode und fügen Sie dann den Text oder das Bild hinzu, das mit der [Ausschluss-URL](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#reference_E7A62B7B99C94B3A806CB262D16E27FC) verknüpft werden soll.

## Bekannte Einschränkungen

* Der QA-Modus ist nicht fixierbar, wenn Sie CNAME und at.js 1.x verwenden, da er auf einem Drittanbieter-Cookie basiert. Um dieses Problem zu umgehen, fügen Sie jeder URL, zu der Sie navigieren, die Vorschauparameter hinzu. Der QS-Modus hängt bei CNAME und at.js 2.x an.
* Derzeit funktioniert die Einstellung `overrideMboxEdgeServer` nicht ordnungsgemäß mit CNAME, wenn Sie at.js-Versionen vor at.js 1.8.2 und at.js 2.3.1 verwenden. Wenn Sie eine ältere Version von at.js verwenden, sollte diese Einstellung auf `false` gesetzt werden, um fehlerhafte Anforderungen zu vermeiden. Alternativ sollten Sie [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) auf eine neuere, unterstützte Version aktualisieren.
* Bei Verwendung von CNAME erhöht sich wahrscheinlich die Größe des Cookie-Headers für [!DNL Target] -Aufrufe. [!DNL Adobe] empfiehlt, die Cookie-Größe unter 8 KB zu halten.
