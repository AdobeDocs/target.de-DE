---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 45bd128a01dcb8d4d8d330d8ed4a4df04b98a612
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 2%

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, damit Aufrufe an eine Domäne des Kunden statt an eine Domäne, die sich im Besitz der Adobe befindet, gesendet werden.

## CNAME-Unterstützung anfordern

Perform the following steps to request CNAME support in [!DNL Target]:

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ).

1. For each hostname, create a CNAME record in your DNS pointing to your regular [!DNL Target] hostname `clientcode.tt.omtrdc.net`.

   For example, if your client code is &quot;cnamecustomer&quot; and your proposed hostname is `target.example.com`, your DNS CNAME record should look something like this:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >* Adobe&#39;s certificate authority, DigiCert, cannot issue a certificate until this step is complete. Therefore, Adobe cannot fulfill your request for a CNAME implementation until this step is complete.


1. [Fill out this form](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/assets/FPC_Request_Form.xlsx) and include it when you [open an Adobe Client Care ticket requesting CNAME support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * Adobe- [!DNL Target] Client-Code:
   * SSL-Zertifikat-Hostnamen (Beispiel: `target.example.com target.example.org`):
   * SSL-Zertifikatkäufer (Adobe wird dringend empfohlen, siehe FAQ): Adobe/Kunde
   * Wenn der Kunde das Zertifikat kauft (auch BYOC genannt), füllen Sie bitte die folgenden zusätzlichen Angaben aus:
      * Zertifikatorganisation (Beispiel: Beispiel Firma Inc):
      * Organisatorische Einheit des Zertifikats (optional, Beispiel: Marketing):
      * Zertifikatland (Beispiel: US):
      * Zertifikatstaat/-region (Beispiel: Kalifornien):
      * Zertifikatort (Beispiel: San Jose):

1. Wenn die Adobe das Zertifikat kauft, arbeitet die Adobe mit DigiCert zusammen, um das Zertifikat auf den Produktionsservern der Adobe zu erwerben und bereitzustellen.

   Wenn der Kunde das Zertifikat (BYOC) kauft, sendet Ihnen der Adobe Client Care die Zertifikatssignaturanforderung (CSR), die Sie beim Erwerb des Zertifikats über Ihre Zertifizierungsstelle verwenden müssen. Nachdem das Zertifikat ausgestellt wurde, müssen Sie eine Kopie des Zertifikats und aller Zwischenzertifikate zur Bereitstellung an Adobe Client Care zurücksenden.

   Adobe Client Care benachrichtigt Sie, wenn Ihre Implementierung fertig ist.

1. Nachdem Sie die vorherigen Aufgaben abgeschlossen und die Adobe Client Care Sie darauf hingewiesen haben, dass die Implementierung fertig ist, müssen Sie den CNAME in at.js aktualisieren, `serverDomain` um den neuen CNAME zu erhalten.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat (auch BYOC) angeben?

Ja, Sie können Ihr eigenes Zertifikat bereitstellen. wird jedoch nicht empfohlen. Die Verwaltung des SSL-Zertifikatlebenszyklus ist sowohl für die Adobe als auch für Sie erheblich einfacher, wenn die Adobe das Zertifikat kauft und steuert. SSL-Zertifikate müssen jedes Jahr erneuert werden, d. h. Adobe Client Care muss sich jedes Jahr mit Ihnen in Verbindung setzen, um der Adobe rechtzeitig ein neues Zertifikat zu senden. Manche Kunden haben möglicherweise Schwierigkeiten, jedes Jahr ein neues Zertifikat zeitnah zu erstellen, was ihre [!DNL Target] Implementierung gefährdet, da Browser die Verbindung nach Ablauf des Zertifikats verweigern.

>[!IMPORTANT]
>
>Beachten Sie, dass Sie, wenn Sie eine CNAME-Implementierung mit [!DNL Target] Ihrem eigenen Zertifikat anfordern, dafür verantwortlich sind, der Adobe Client Care jährlich erneuerte Zertifikate bereitzustellen. Wenn Ihr CNAME-Zertifikat abläuft, bevor die Adobe ein neues Zertifikat bereitstellen kann, führt dies zu einem Ausfall für Ihre spezifische [!DNL Target] Implementierung.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Certificates issued before September 1, 2020 will be two-year certificates. Certificates issued on or after September 1, 2020 will be one-year certificates. You can read more about the move to one-year certificates [here](https://www.digicert.com/position-on-1-year-certificates).

### What hostnames should I choose? How many hostnames per domain should I choose?

[!DNL Target] CNAME implementations require only one hostname per domain on the SSL certificate and in the customer&#39;s DNS, so that&#39;s what we recommend. Some customers might require additional hostnames per domain for their own purposes (testing in staging, for example), which is supported.

Most customers choose a hostname like `target.example.com`, so that&#39;s what we recommend, but the choice is ultimately yours. Be sure not to request a hostname of an existing DNS record as that would cause a conflict and delay time to resolution of your [!DNL Target] CNAME request.

### I already have a CNAME implementation for [!DNL Adobe Analytics], can we use the same certificate or hostname?

Nein, es [!DNL Target] ist ein separater Hostname und Zertifikat erforderlich.

### Hat meine aktuelle Implementierung von Zielgruppe Auswirkungen auf ITP 2.x?

In a Safari browser, navigate to your website on which you have a Target JavaScript library. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

ITP-Probleme können für die Zielgruppe mit einem Analytics-CNAME gelöst werden. Sie benötigen einen separaten CNAME für Zielgruppen nur bei Werbeblockierungsszenarien, in denen die Zielgruppe blockiert ist.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welche Art von Serviceunterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats gibt es keine Serviceunterbrechung (einschließlich Zertifikatsverlängerungen). Wenn Sie jedoch den Hostnamen im [!DNL Target] Implementierungscode (`serverDomain` in at.js) in den neuen CNAME-Hostnamen (`target.example.com`) ändern, behandeln Webbrowser rückkehrende Besucher als neue Besucher und ihre Profil-Daten gehen verloren, da der vorherige Cookie aufgrund von Browsersicherheitsmodellen nicht mehr unter dem alten Hostnamen (`clientcode.tt.omtrdc.net`) verfügbar ist. Dies ist eine einmalige Unterbrechung nur beim ersten CNAME-Cut-Over. Zertifikatverlängerungen haben nicht dieselbe Wirkung, da sich der Hostname nicht ändert.

### Welcher Schlüsseltyp und welcher Zertifikatssignaturalgorithmus werden für meine CNAME-Implementierung verwendet?

Alle Zertifikate sind RSA SHA-256 und Schlüssel sind standardmäßig RSA 2048-Bit. Schlüsselgrößen, die größer als 2048 Bit sind, werden derzeit nicht unterstützt.

### Wie kann ich überprüfen, ob meine CNAME-Implementierung für Traffic bereit ist?

Verwenden Sie die folgenden Befehle (im MacOs- oder Linux-Befehlszeilenterminal mit bash und curl 7.49+):

1. Fügen Sie zuerst diese Bash-Funktion in Ihr Terminal ein:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Fügen Sie diesen Befehl als Nächstes ein (ersetzen Sie ihn `target.example.com` durch Ihren Hostnamen):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Wenn die Implementierung fertig ist, sollten Sie die Ausgabe wie unten sehen. Wichtig ist, dass alle Zeilen angezeigt `CN=target.example.com`werden, was unserem gewünschten Hostnamen entspricht. Wenn eine davon angezeigt wird `CN=*.tt.omtrdc.net`, ist die Implementierung **nicht** bereit.

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

1. Validieren Sie Ihren neuen DNS-CNAME mit einer anderen Curl-Anforderung, die auch Folgendes anzeigen sollte `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Wenn dieser Befehl fehlschlägt, aber der obige `validateEdgeFpsslSni` Befehl erfolgreich ausgeführt wird, müssen Sie möglicherweise warten, bis Ihre DNS-Updates vollständig übertragen werden. DNS records have an associated [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) that dictates cache expiration time for DNS replies of those records, so you may need to wait at least as long as your TTLs. You can use the `dig target.example.com` command or [the G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) to look up your specific TTLs.

## Bekannte Einschränkungen

* QA mode will not be sticky when you have CNAME and at.js 1.x because it is based on a third-party cookie. The workaround is to add the preview parameters to each URL you navigate to. Der QS-Modus ist fixierbar, wenn Sie CNAME und at.js 2.x haben.
* Currently the `overrideMboxEdgeServer` setting doesn&#39;t work properly with CNAME. Dies sollte so festgelegt werden, `false` dass keine fehlerhaften Anfragen gestellt werden.
* Bei der Verwendung von CNAME erhöht sich die Wahrscheinlichkeit, dass die Größe des Cookie-Headers für Zielgruppen-Aufrufe zunimmt. Es wird empfohlen, die Cookie-Größe unter 8 KB zu halten.
