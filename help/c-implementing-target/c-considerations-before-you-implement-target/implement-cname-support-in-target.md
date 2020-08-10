---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 8edefa9975cf4f39fb33b0323e5a52893d46ff97
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 2%

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, damit Aufrufe an eine Domäne des Kunden statt an eine Domäne, die sich im Besitz der Adobe befindet, gesendet werden.

## Request CNAME support

Perform the following steps to request CNAME support in [!DNL Target]:

1. Determine the list of hostnames you need for your SSL certificate (see FAQ).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Eintrag in Ihrem DNS, der auf Ihren regulären [!DNL Target] Hostnamen verweist `clientcode.tt.omtrdc.net`.

   For example, if your client code is &quot;cnamecustomer&quot; and your proposed hostname is `target.example.com`, your DNS CNAME record should look something like this:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >* Die Zertifizierungsstelle der Adobe, DigiCert, kann erst nach Abschluss dieses Schritts ein Zertifikat ausstellen. Therefore, Adobe cannot fulfill your request for a CNAME implementation until this step is complete.


1. Füllen Sie das folgende Formular aus und fügen Sie es ein, wenn Sie ein Adobe Client Care Ticket [öffnen, das CNAME-Support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)anfordert:

   * Adobe- [!DNL Target] Client-Code:
   * SSL-Zertifikat-Hostnamen (Beispiel: `target.example.com target.example.org`):
   * SSL certificate purchaser (Adobe is highly recommended, see FAQ): Adobe/customer
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
>Be aware that if you request a [!DNL Target] bring-your-own-certificate CNAME implementation, you are responsible for providing renewed certificates to Adobe Client Care every year. Wenn Ihr CNAME-Zertifikat abläuft, bevor die Adobe ein neues Zertifikat bereitstellen kann, führt dies zu einem Ausfall für Ihre spezifische [!DNL Target] Implementierung.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Certificates issued before September 1, 2020 will be two-year certificates. Zertifikate, die am oder nach dem 1. September 2020 ausgestellt werden, sind einjährige Zertifikate. Weitere Informationen zum Umstieg auf einjährige Zertifikate finden Sie [hier](https://www.digicert.com/position-on-1-year-certificates).

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] Für CNAME-Implementierungen ist nur ein Hostname pro Domäne im SSL-Zertifikat und im DNS des Kunden erforderlich. Daher empfehlen wir Ihnen Folgendes: Einige Kunden benötigen für ihre eigenen Zwecke (z. B. Testen im Staging) zusätzliche Hostnamen pro Domäne.

Most customers choose a hostname like `target.example.com`, so that&#39;s what we recommend, but the choice is ultimately yours. Be sure not to request a hostname of an existing DNS record as that would cause a conflict and delay time to resolution of your [!DNL Target] CNAME request.

### I already have a CNAME implementation for [!DNL Adobe Analytics], can we use the same certificate or hostname?

No, [!DNL Target] requires a separate hostname and certificate.

### Is my current implementation of Target impacted by ITP 2.x?

Navigieren Sie in einem Safari-Browser zu Ihrer Website, auf der Sie über eine JavaScript-Zielgruppe verfügen. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

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

1. Next paste this command (replacing `target.example.com` with your hostname):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Wenn die Implementierung fertig ist, sollten Sie die Ausgabe wie unten sehen. The important part is that all lines show `CN=target.example.com`, which matches our desired hostname. If any of them show `CN=*.tt.omtrdc.net`, the implementation is **not** ready.

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

1. Validate your new DNS CNAME with another curl request, which should also show `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >If this command fails but the `validateEdgeFpsslSni` command above succeeds, you might need to wait for your DNS updates to fully propagate. DNS-Datensätze verfügen über eine zugehörige [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) , die den Cache-Ablauf für DNS-Antworten dieser Datensätze vorschreibt. Daher müssen Sie möglicherweise mindestens so lange warten, wie Ihre TTLs funktionieren. You can use the `dig target.example.com` command or [the G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) to look up your specific TTLs.

## Bekannte Einschränkungen

* QA mode will not be sticky when you have CNAME and at.js 1.x because it is based on a third-party cookie. Die Lösung besteht darin, jeder URL, zu der Sie navigieren, die Parameter für die Vorschau hinzuzufügen. Der QS-Modus ist fixierbar, wenn Sie CNAME und at.js 2.x haben.
* Derzeit funktioniert die `overrideMboxEdgeServer` Einstellung nicht ordnungsgemäß mit CNAME. Dies sollte so festgelegt werden, `false` dass keine fehlerhaften Anfragen gestellt werden.
* When using CNAME it becomes more likely that the size of the cookie header for Target calls will increase. Es wird empfohlen, die Cookie-Größe unter 8 KB zu halten.
