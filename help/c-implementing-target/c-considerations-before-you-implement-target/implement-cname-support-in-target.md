---
keywords: Client-Pflege;cname;Zertifikat-Programm;Kanonischer Name;Cookies;Zertifikat;amc;adobe-verwaltetes Zertifikat;Digicert;Domänenkontrollvalidierung;dcv
description: Arbeiten Sie mit Adobe Client Care zusammen, um CNAME (Canonical Name)-Unterstützung in Adobe Target zu implementieren, um Probleme mit der Anzeigensperre oder ITP-bezogene Cookie-Richtlinien zu behandeln.
title: Wie verwende ich CNAME in der Zielgruppe?
feature: Datenschutz und Sicherheit
role: Entwickler
translation-type: tm+mt
source-git-commit: 69677b9d384d9817a39386fc1388a4aa42121713
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 2%

---


# CNAME und Adobe Target

Anweisungen zum Arbeiten mit [!DNL Adobe] Client Care zur Implementierung der CNAME-Unterstützung (kanonischer Name) in [!DNL Adobe Target]. Verwenden Sie CNAME, um Probleme mit der Anzeigenblockierung oder ITP-bezogene Cookie-Richtlinien (Intelligent Tracking Prevention) zu behandeln. Mit CNAME werden Aufrufe an eine Domäne des Kunden statt an eine Domäne gesendet, die [!DNL Adobe] gehört.

## CNAME-Unterstützung bei der Zielgruppe anfordern

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ unten).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Eintrag in Ihrem DNS, der auf Ihren regulären [!DNL Target] Hostnamen `clientcode.tt.omtrdc.net` verweist.

   Wenn Ihr Client-Code z. B. &quot;cnamecustomer&quot;lautet und Ihr Hostname `target.example.com` lautet, sieht Ihr DNS-CNAME-Datensatz wie folgt aus:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >Die Zertifizierungsstelle der Adobe, DigiCert, kann erst nach Abschluss dieses Schritts ein Zertifikat ausstellen. [!DNL Adobe] kann Ihre Anforderung einer CNAME-Implementierung daher erst nach Abschluss dieses Schritts erfüllen.

1. [Füllen Sie dieses ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) Formular aus und fügen Sie es ein, wenn Sie ein Adobe Client Care Ticket  [öffnen, das CNAME-Support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) anfordert:

   * Adobe [!DNL Target] Client-Code:
   * SSL-Zertifikat-Hostnamen (Beispiel: `target.example.com target.example.org`):
   * SSL-Zertifikatkäufer (Adobe wird dringend empfohlen, siehe FAQ): Adobe/Kunde
   * Wenn der Kunde das Zertifikat kauft, das auch als &quot;Eigenes Zertifikat&quot;(BYOC) bezeichnet wird, füllen Sie die folgenden zusätzlichen Angaben aus:
      * Zertifikatorganisation (Beispiel: Beispiel Firma Inc):
      * Organisatorische Einheit des Zertifikats (optional, Beispiel: Marketing):
      * Zertifikatland (Beispiel: US):
      * Zertifikatstaat/-region (Beispiel: Kalifornien):
      * Zertifikatort (Beispiel: San Jose):

1. Wenn [!DNL Adobe] das Zertifikat kauft, funktioniert [!DNL Adobe] mit DigiCert, um das Zertifikat auf Produktionsservern der Adobe zu erwerben und bereitzustellen.

   Wenn der Kunde das Zertifikat (BYOC) kauft, sendet Ihnen [!DNL Adobe] Client Care die Zertifikatssignaturanforderung (CSR). Verwenden Sie den CSR, wenn Sie das Zertifikat über Ihre Zertifizierungsstelle Ihrer Wahl erwerben. Nachdem das Zertifikat ausgestellt wurde, senden Sie eine Kopie des Zertifikats und aller Zwischenzertifikate zur Bereitstellung an den [!DNL Adobe] Client Care.

   [!DNL Adobe] Der Kundendienst benachrichtigt Sie, wenn Ihre Implementierung fertig ist.

1. Aktualisieren Sie `serverDomain` auf den neuen CNAME in at.js.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat bereitstellen (Eigenes Zertifikat mitbringen oder BYOC)?

Sie können Ihr eigenes Zertifikat bereitstellen. [!DNL Adobe] empfiehlt diese Vorgehensweise jedoch nicht. Die Verwaltung des SSL-Zertifikatlebenszyklus ist sowohl für [!DNL Adobe] als auch für Sie einfacher, wenn [!DNL Adobe] das Zertifikat kauft und steuert. SSL-Zertifikate müssen jedes Jahr erneuert werden. Deshalb muss sich [!DNL Adobe] Client Care jedes Jahr an Sie wenden, um ein neues Zertifikat rechtzeitig zu erhalten. Manche Kunden können Schwierigkeiten haben, rechtzeitig ein neues Zertifikat zu erhalten. Ihre [!DNL Target]-Implementierung wird gefährdet, wenn das Zertifikat abläuft, da Browser Verbindungen ablehnen.

>[!IMPORTANT]
>
>Wenn Sie eine [!DNL Target] CNAME-Implementierung mit Ihrem eigenen Zertifikat anfordern, sind Sie dafür verantwortlich, dass dem [!DNL Adobe]-Kundendienst jedes Jahr erneuerte Zertifikate bereitgestellt werden. Wenn Sie zulassen, dass Ihr CNAME-Zertifikat abläuft, bevor [!DNL Adobe] ein neues Zertifikat bereitstellen kann, führt dies zu einem Ausfall für Ihre spezifische [!DNL Target]-Implementierung.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Vor dem 1. September 2020 ausgestellte Bescheinigungen sind zweijährige Bescheinigungen. Zertifikate, die am oder nach dem 1. September 2020 ausgestellt werden, sind einjährige Zertifikate. Weitere Informationen zum Umstieg auf einjährige Zertifikate [hier](https://www.digicert.com/position-on-1-year-certificates).

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] CNAME-Implementierungen erfordern nur einen Hostnamen pro Domäne auf dem SSL-Zertifikat und im DNS des Kunden. Adobe empfiehlt einen Hostnamen. Einige Kunden benötigen für ihre eigenen Zwecke mehr Hostnamen pro Domäne (z. B. Tests im Staging), was unterstützt wird.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`. Adobe empfiehlt, diesem Verfahren zu folgen, aber die Wahl liegt letztendlich bei Ihnen. Fordern Sie keinen Hostnamen eines vorhandenen DNS-Datensatzes an. Dies führt zu einem Konflikt und verzögert die Zeit bis zur Lösung Ihrer [!DNL Target] CNAME-Anforderung.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics], können wir dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, [!DNL Target] erfordert einen separaten Hostnamen und ein separates Zertifikat.

### Hat meine aktuelle Implementierung von Zielgruppe Auswirkungen auf ITP 2.x?

Navigieren Sie in einem Safari-Browser zu der Website, auf der Sie eine JavaScript -Bibliothek für [!DNL Target] haben. Wenn ein [!DNL Target]-Cookie im Kontext eines CNAME gesetzt wird, z. B. `analytics.company.com`, werden Sie nicht von ITP 2.x beeinflusst.

ITP-Probleme können für [!DNL Target] mit nur einem [!DNL Analytics] CNAME gelöst werden. Sie benötigen einen separaten CNAME [!DNL Target] nur in Anzeigenblockierungsszenarien, in denen [!DNL Target] blockiert ist.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welche Art von Serviceunterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats gibt es keine Serviceunterbrechung (einschließlich Zertifikatsverlängerungen).

Nachdem Sie jedoch den Hostnamen im [!DNL Target]-Implementierungscode (`serverDomain` in at.js) in den neuen CNAME-Hostnamen (`target.example.com`) geändert haben, behandeln Webbrowser rückkehrende Besucher als neue Besucher. Die Daten zum Profil der zurückgegebenen Besucher gehen verloren, da auf das vorherige Cookie unter dem alten Hostnamen (`clientcode.tt.omtrdc.net`) nicht zugegriffen werden kann. Der Zugriff auf das vorherige Cookie ist aufgrund von Sicherheitsmodellen im Browser nicht möglich. Diese Störung tritt nur beim ersten CNAME-Cut-Over auf. Zertifikatverlängerungen haben nicht dieselbe Wirkung, da sich der Hostname nicht ändert.

### Welcher Schlüsseltyp und welcher Zertifikatssignaturalgorithmus wird für meine CNAME-Implementierung verwendet?

Alle Zertifikate sind RSA SHA-256 und Schlüssel sind standardmäßig RSA 2048-Bit. Schlüsselgrößen, die größer als 2048 Bit sind, werden derzeit nicht unterstützt.

### Wie kann ich überprüfen, ob meine CNAME-Implementierung für Traffic bereit ist?

Verwenden Sie die folgenden Befehle (im Kommandozeilenterminal macOS oder Linux, mit bash und curl 7.49+):

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

   Wenn die Implementierung fertig ist, sehen Sie die Ausgabe wie unten. Wichtig ist, dass alle Zeilen `CN=target.example.com` enthalten, was dem gewünschten Hostnamen entspricht. Wenn Zeilen `CN=*.tt.omtrdc.net` enthalten, ist die Implementierung **nicht** fertig.

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

1. Validieren Sie Ihren neuen DNS-CNAME mit einer anderen Curl-Anforderung, die auch `CN=target.example.com` anzeigen sollte:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Wenn dieser Befehl fehlschlägt, aber der Befehl `validateEdgeFpsslSni` oben erfolgreich ausgeführt wird, warten Sie, bis Ihre DNS-Updates vollständig übertragen werden. DNS-Datensätze haben eine verknüpfte [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records), die die Cache-Ablaufzeit für DNS-Antworten dieser Datensätze vorgibt. Daher müssen Sie möglicherweise mindestens so lange warten, wie Ihre TTLs funktionieren. Sie können den Befehl `dig target.example.com` oder [die G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) verwenden, um Ihre spezifischen TTLs nachzuschlagen.

## Bekannte Einschränkungen

* Der QS-Modus ist nicht fixierbar, wenn Sie CNAME und at.js 1.x verwenden, da er auf einem Drittanbieter-Cookie basiert. Die Lösung besteht darin, jeder URL, zu der Sie navigieren, die Parameter für die Vorschau hinzuzufügen. Der QS-Modus ist fixierbar, wenn Sie CNAME und at.js 2.x haben.
* Derzeit funktioniert die Einstellung `overrideMboxEdgeServer` nicht ordnungsgemäß mit CNAME, wenn at.js-Versionen vor &quot;at.js&quot;1.8.2 und &quot;at.js 2.3.1&quot;verwendet werden. Wenn Sie eine ältere Version von at.js verwenden, sollte diese Einstellung auf `false` eingestellt werden, um fehlerhafte Anforderungen zu vermeiden. Alternativ sollten Sie auch erwägen, at.js auf eine neuere, unterstützte Version zu aktualisieren.[](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)
* Bei Verwendung von CNAME erhöht sich die Wahrscheinlichkeit, dass die Größe des Cookie-Headers für [!DNL Target]-Aufrufe zunimmt. [!DNL Adobe] empfiehlt, die Cookie-Größe unter 8 KB zu halten.
