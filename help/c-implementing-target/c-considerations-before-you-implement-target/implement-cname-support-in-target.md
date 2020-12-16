---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
feature: privacy and security
translation-type: tm+mt
source-git-commit: 677d5ed16377fc32b4506ca736084319e5643e67
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 2%

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Anleitungen zum Arbeiten mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Kanonischer Name) in [!DNL Adobe Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, damit Aufrufe an eine Domäne des Kunden statt an eine Domäne, die sich im Besitz der Adobe befindet, gesendet werden.

## CNAME-Unterstützung anfordern

Führen Sie die folgenden Schritte aus, um CNAME-Unterstützung in [!DNL Target] anzufordern:

1. Bestimmen Sie die Liste der Hostnamen, die Sie für Ihr SSL-Zertifikat benötigen (siehe FAQ).

1. Erstellen Sie für jeden Hostnamen einen CNAME-Eintrag in Ihrem DNS, der auf Ihren regulären [!DNL Target] Hostnamen `clientcode.tt.omtrdc.net` verweist.

   Wenn Ihr Client-Code z. B. &quot;cnamecustomer&quot;lautet und Ihr Hostname `target.example.com` lautet, sollte Ihr DNS-CNAME-Eintrag wie folgt aussehen:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >Die Zertifizierungsstelle der Adobe, DigiCert, kann erst nach Abschluss dieses Schritts ein Zertifikat ausstellen. Daher kann die Adobe Ihre Anforderung einer CNAME-Implementierung erst dann erfüllen, wenn dieser Schritt abgeschlossen ist.

1. [Füllen Sie dieses ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) Formular aus und fügen Sie es ein, wenn Sie ein Adobe Client Care Ticket  [öffnen, das CNAME-Support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) anfordert:

   * Adobe [!DNL Target] Client-Code:
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

1. Nachdem Sie die vorherigen Aufgaben abgeschlossen und die Adobe Client Care Sie darauf hingewiesen haben, dass die Implementierung fertig ist, müssen Sie `serverDomain` auf den neuen CNAME in at.js aktualisieren.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat (auch BYOC) angeben?

Ja, Sie können Ihr eigenes Zertifikat bereitstellen. wird jedoch nicht empfohlen. Die Verwaltung des SSL-Zertifikatlebenszyklus ist sowohl für die Adobe als auch für Sie erheblich einfacher, wenn die Adobe das Zertifikat kauft und steuert. SSL-Zertifikate müssen jedes Jahr erneuert werden, d. h. Adobe Client Care muss sich jedes Jahr mit Ihnen in Verbindung setzen, um der Adobe rechtzeitig ein neues Zertifikat zu senden. Manche Kunden haben möglicherweise Schwierigkeiten, jedes Jahr ein neues Zertifikat zeitnah zu erstellen, was ihre [!DNL Target]-Implementierung gefährdet, da Browser Verbindungen nach Ablauf des Zertifikats ablehnen.

>[!IMPORTANT]
>
>Beachten Sie, dass Sie, wenn Sie eine [!DNL Target] CNAME-Implementierung mit Ihrem eigenen Zertifikat anfordern, dafür verantwortlich sind, dass Sie der Adobe Client Care jährlich erneuerte Zertifikate bereitstellen. Wenn Sie zulassen, dass Ihr CNAME-Zertifikat abläuft, bevor die Adobe ein neues Zertifikat bereitstellen kann, führt dies zu einem Ausfall für Ihre spezifische [!DNL Target]-Implementierung.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Zertifikate, die vor dem 1. September 2020 ausgestellt werden, sind zweijährige Zertifikate. Zertifikate, die am oder nach dem 1. September 2020 ausgestellt werden, sind einjährige Zertifikate. Weitere Informationen zum Umstieg auf einjährige Zertifikate [hier](https://www.digicert.com/position-on-1-year-certificates).

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] Für CNAME-Implementierungen ist nur ein Hostname pro Domäne im SSL-Zertifikat und im DNS des Kunden erforderlich. Daher empfehlen wir Ihnen Folgendes: Einige Kunden benötigen für ihre eigenen Zwecke (z. B. Testen im Staging) zusätzliche Hostnamen pro Domäne.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`, daher empfehlen wir Ihnen, aber die Auswahl liegt letztendlich bei Ihnen. Achten Sie darauf, keinen Hostnamen eines vorhandenen DNS-Datensatzes anzufordern, da dies zu Konflikten und Verzögerungen bei der Auflösung Ihrer [!DNL Target] CNAME-Anforderung führen würde.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics], können wir dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, [!DNL Target] erfordert einen separaten Hostnamen und ein separates Zertifikat.

### Hat meine aktuelle Implementierung von Zielgruppe Auswirkungen auf ITP 2.x?

Navigieren Sie in einem Safari-Browser zu Ihrer Website, auf der Sie über eine JavaScript-Zielgruppe verfügen. Wenn Sie ein Zielgruppe-Cookie sehen, das im Kontext eines CNAME gesetzt wurde, z. B. `analytics.company.com`, werden Sie von ITP 2.x nicht beeinflusst.

ITP-Probleme können für die Zielgruppe mit einem Analytics-CNAME gelöst werden. Sie benötigen einen separaten CNAME für Zielgruppen nur bei Werbeblockierungsszenarien, in denen die Zielgruppe blockiert ist.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welche Art von Serviceunterbrechungen kann ich erwarten, wenn meine CNAME-Implementierung bereitgestellt wird?

Bei der Bereitstellung des Zertifikats gibt es keine Serviceunterbrechung (einschließlich Zertifikatsverlängerungen). Wenn Sie jedoch den Hostnamen im [!DNL Target]-Implementierungscode (`serverDomain` in at.js) in den neuen CNAME-Hostnamen (`target.example.com`) ändern, behandeln Webbrowser rückkehrende Besucher als neue Besucher und ihre Profil-Daten gehen verloren, da der vorherige Cookie aufgrund von Browsersicherheitsmodellen unter dem alten Hostnamen (`clientcode.tt.omtrdc.net`) nicht mehr verfügbar ist. Dies ist eine einmalige Unterbrechung nur beim ersten CNAME-Cut-Over. Zertifikatverlängerungen haben nicht dieselbe Wirkung, da sich der Hostname nicht ändert.

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

1. Fügen Sie diesen Befehl dann ein (ersetzen Sie `target.example.com` durch Ihren Hostnamen):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Wenn die Implementierung fertig ist, sollten Sie die Ausgabe wie unten sehen. Wichtig ist, dass alle Zeilen `CN=target.example.com` anzeigen, was unserem gewünschten Hostnamen entspricht. Wenn in einem dieser Elemente `CN=*.tt.omtrdc.net` angezeigt wird, ist die Implementierung **nicht** fertig.

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
   >Wenn dieser Befehl fehlschlägt, aber der Befehl `validateEdgeFpsslSni` oben erfolgreich ausgeführt wird, müssen Sie möglicherweise warten, bis Ihre DNS-Updates vollständig übertragen werden. DNS-Datensätze haben eine verknüpfte [TTL (Time-to-Live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records), die die Cache-Ablaufzeit für DNS-Antworten dieser Datensätze vorgibt, sodass Sie mindestens so lange warten müssen, wie Ihre TTLs. Sie können den Befehl `dig target.example.com` oder [die G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) verwenden, um Ihre spezifischen TTLs nachzuschlagen.

## Bekannte Einschränkungen

* Der QS-Modus ist nicht fixierbar, wenn Sie CNAME und at.js 1.x verwenden, da er auf einem Drittanbieter-Cookie basiert. Die Lösung besteht darin, jeder URL, zu der Sie navigieren, die Parameter für die Vorschau hinzuzufügen. Der QS-Modus ist fixierbar, wenn Sie CNAME und at.js 2.x haben.
* Zurzeit funktioniert die Einstellung `overrideMboxEdgeServer` nicht ordnungsgemäß mit CNAME, wenn at.js-Versionen vor &quot;at.js&quot;1.8.2 und &quot;at.js 2.3.1&quot;verwendet werden. Wenn Sie eine ältere Version von at.js verwenden, sollte diese als `false` eingestellt werden, um fehlerhafte Anforderungen zu vermeiden. Alternativ sollten Sie auch erwägen, at.js auf eine neuere, unterstützte Version zu aktualisieren.[](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)
* Bei der Verwendung von CNAME erhöht sich die Wahrscheinlichkeit, dass die Größe des Cookie-Headers für Zielgruppen-Aufrufe zunimmt. Es wird empfohlen, die Cookie-Größe unter 8 KB zu halten.
