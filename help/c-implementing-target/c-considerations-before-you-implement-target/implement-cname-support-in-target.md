---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: e31a4195097d3338e1b07679ab52dfa7f2299017
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 2%

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, damit Aufrufe an eine Domäne des Kunden statt an eine Domäne im Besitz von Adobe gesendet werden.

## CNAME-Unterstützung anfordern

Perform the following steps to request CNAME support in [!DNL Target]:

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Eintrag in Ihrem DNS, der auf Ihren regulären [!DNL Target] Hostnamen verweist `clientcode.tt.omtrdc.net`. Wenn Ihr Client-Code z. B. &quot;cnamecustomer&quot;ist und Ihr Hostname angegeben ist `target.example.com`, sollte Ihr DNS-CNAME-Eintrag wie folgt aussehen:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >* Die Adobe-Zertifikatbehörde DigiCert kann erst nach Abschluss dieses Schritts ein Zertifikat ausstellen. Daher kann Adobe Ihre Anforderung einer CNAME-Implementierung erst dann erfüllen, wenn dieser Schritt abgeschlossen ist.


1. Füllen Sie das folgende Formular aus und fügen Sie es ein, wenn Sie ein Adobe Client Care-Ticket [öffnen, das CNAME-Unterstützung](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C)anfordert:

   * Adobe- [!DNL Target] Clientcode:
   * SSL-Zertifikat-Hostnamen (Beispiel: `target.example.com target.example.org`):
   * SSL-Zertifikatkäufer (Adobe wird dringend empfohlen, siehe FAQ): Adobe/Kunde
   * Wenn der Kunde das Zertifikat kauft (auch BYOC genannt), füllen Sie bitte die folgenden zusätzlichen Angaben aus:
      * Zertifikatorganisation (Beispiel: Beispiel Firma Inc):
      * Organisatorische Einheit des Zertifikats (optional, Beispiel: Marketing):
      * Zertifikatland (Beispiel: US):
      * Zertifikatstaat/-region (Beispiel: Kalifornien):
      * Zertifikatort (Beispiel: San Jose):

1. Wenn Adobe das Zertifikat kauft, arbeitet Adobe mit DigiCert zusammen, um Ihr Zertifikat auf den Produktionsservern von Adobe zu erwerben und bereitzustellen.

   Wenn der Kunde das Zertifikat (BYOC) kauft, sendet Ihnen Adobe Client Care die CSR-Anforderung (Certificate Signing Request) zurück, die Sie beim Erwerb des Zertifikats über Ihre Zertifizierungsstelle verwenden müssen. Nachdem das Zertifikat ausgestellt wurde, müssen Sie eine Kopie des Zertifikats und aller Zwischenzertifikate zur Bereitstellung an Adobe Client Care zurücksenden.

   Adobe Client Care benachrichtigt Sie, wenn Ihre Implementierung fertig ist.

1. Nachdem Sie die vorherigen Aufgaben abgeschlossen und Adobe ClientCare Sie darüber informiert haben, dass die Implementierung fertig ist, müssen Sie den neuen CNAME in at.js aktualisieren, `serverDomain` um den neuen CNAME zu erhalten.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat (auch BYOC) angeben?

Ja, Sie können Ihr eigenes Zertifikat bereitstellen. wird jedoch nicht empfohlen. Die Verwaltung des SSL-Zertifikatlebenszyklus ist sowohl für Adobe als auch für Sie erheblich einfacher, wenn Adobe das Zertifikat kauft und steuert. SSL-Zertifikate müssen jedes Jahr erneuert werden. Das bedeutet, dass Adobe Client Care Sie jedes Jahr kontaktieren muss, um Adobe ein neues Zertifikat rechtzeitig zu senden. Manche Kunden haben möglicherweise Schwierigkeiten, jedes Jahr ein neues Zertifikat zeitnah zu erstellen, was ihre [!DNL Target] Implementierung gefährdet, da Browser die Verbindung nach Ablauf des Zertifikats verweigern.

>[!IMPORTANT]
>
>Wenn Sie eine CNAME-Implementierung mit [!DNL Target] eigenem Zertifikat anfordern, müssen Sie Adobe Client Care jedes Jahr neue Zertifikate zukommen lassen. Wenn Ihr CNAME-Zertifikat abläuft, bevor Adobe ein neues Zertifikat bereitstellen kann, führt dies zu einem Ausfall für Ihre spezifische [!DNL Target] Implementierung.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Zertifikate, die vor dem 1. September 2020 ausgestellt werden, sind zweijährige Zertifikate. Zertifikate, die am oder nach dem 1. September 2020 ausgestellt werden, sind einjährige Zertifikate. Weitere Informationen zum Umstieg auf einjährige Zertifikate finden Sie [hier](https://www.digicert.com/position-on-1-year-certificates).

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] Für CNAME-Implementierungen ist nur ein Hostname pro Domäne im SSL-Zertifikat und im DNS des Kunden erforderlich. Daher empfehlen wir Ihnen Folgendes: Einige Kunden benötigen für ihre eigenen Zwecke (z. B. Testen im Staging) zusätzliche Hostnamen pro Domäne.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`, daher empfehlen wir Ihnen, aber die Wahl liegt letztendlich bei Ihnen. Achten Sie darauf, keinen Hostnamen eines vorhandenen DNS-Datensatzes anzufordern, da dies zu Konflikten und Verzögerungen bei der Auflösung Ihrer [!DNL Target] CNAME-Anforderung führen würde.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics], können wir dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, es [!DNL Target] ist ein separater Hostname und Zertifikat erforderlich.

### Ist meine aktuelle Implementierung von Target von ITP 2.x betroffen?

Navigieren Sie in einem Safari-Browser zu Ihrer Website, auf der Sie über eine Target-JavaScript-Bibliothek verfügen. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

ITP-Probleme können zum Target mit nur einem Analytics CNAME gelöst werden. Sie benötigen einen separaten Target-CNAME nur, wenn das Target blockiert wird.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welche Art von Serviceunterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats gibt es keine Serviceunterbrechung (einschließlich Zertifikatsverlängerungen). Wenn Sie jedoch den Hostnamen im Target-Implementierungscode (`serverDomain` in at.js) in den neuen CNAME-Hostnamen (`target.example.com`) ändern, behandeln Webbrowser rückkehrende Besucher als neue Besucher und ihre Profil-Daten gehen verloren, da der vorherige Cookie aufgrund von Browsersicherheitsmodellen nicht mehr unter dem alten Hostnamen (`clientcode.tt.omtrdc.net`) verfügbar ist. Dies ist eine einmalige Unterbrechung nur beim ersten CNAME-Cut-Over. Zertifikatverlängerungen haben nicht dieselbe Auswirkung, da sich der Hostname nicht ändert.

### Welcher Schlüsseltyp und welcher Zertifikatssignaturalgorithmus werden für meine CNAME-Implementierung verwendet?

Alle Zertifikate sind RSA SHA-256 und Schlüssel sind standardmäßig RSA 2048-Bit. Schlüsselgrößen, die größer als 2048 Bit sind, werden derzeit nicht unterstützt.

### Kann Adobe/DigiCert die DCV-E-Mails an eine andere E-Mail-Adresse senden `<someone>@example.com`?

Nein, DigiCert (oder eine Zertifizierungsstelle) erlaubt es nicht nur jedem, der unter einer Domäne eine E-Mail-Adresse hat, ein SSL-Zertifikat unter derselben Domäne zu autorisieren, es sei denn, diese E-Mail-Adresse ist auch in den WHOIS-Informationen der Domäne oder der vorab festgelegten Liste der Adressen enthalten (siehe oben). Dadurch wird sichergestellt, dass nur autorisierte Personen DCV für eine bestimmte Domäne genehmigen können. Sollte dies für Sie nicht möglich sein, empfehlen wir die Verwendung der DNS CNAME DCV-Methode (siehe oben).

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
   >Wenn dieser Befehl fehlschlägt, aber der obige `validateEdgeFpsslSni` Befehl erfolgreich ausgeführt wird, müssen Sie möglicherweise warten, bis Ihre DNS-Updates vollständig übertragen werden. DNS-Datensätze verfügen über eine zugehörige [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) , die den Cache-Ablauf für DNS-Antworten dieser Datensätze vorschreibt. Daher müssen Sie möglicherweise mindestens so lange warten, wie Ihre TTLs funktionieren. Sie können den `dig target.example.com` Befehl oder [die G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) verwenden, um Ihre spezifischen TTLs nachzuschlagen.

## Bekannte Einschränkungen

* Der QS-Modus ist nicht fixierbar, wenn Sie CNAME und at.js 1.x verwenden, da er auf einem Drittanbieter-Cookie basiert. Die Lösung besteht darin, jeder URL, zu der Sie navigieren, die Parameter für die Vorschau hinzuzufügen. Der QS-Modus ist fixierbar, wenn Sie CNAME und at.js 2.x haben.
* Derzeit funktioniert die `overrideMboxEdgeServer` Einstellung nicht ordnungsgemäß mit CNAME. Dies sollte so festgelegt werden, `false` dass keine fehlerhaften Anfragen gestellt werden.
