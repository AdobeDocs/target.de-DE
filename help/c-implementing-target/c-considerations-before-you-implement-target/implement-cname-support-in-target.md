---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 8139b9373dab3b699a93036752d982793fbd1158
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 2%

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, damit Aufrufe an eine Domäne des Kunden statt an eine Domäne im Besitz von Adobe gesendet werden.

## CNAME-Unterstützung anfordern

Perform the following steps to request CNAME support in [!DNL Target]:

1. Die Zertifizierungsstelle von Adobe (DigiCert) muss überprüfen, ob Adobe berechtigt ist, Zertifikate unter Ihrer Domäne zu generieren.

   DigiCert ruft diesen Prozess zur Überprüfung der [Domänenkontrolle (DCV)](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/)auf. Adobe darf erst dann ein Zertifikat unter Ihrer Domäne generieren, wenn dieser Prozess für mindestens eine der folgenden DCV-Methoden abgeschlossen ist:

   * Die schnellste DCV-Methode ist die DNS-CNAME-Methode, bei der Sie Ihrer Domäne einen DNS-CNAME-Eintrag (mit einem Token) hinzufügen, der auf den DCV-Hostnamen (`dcv.digicert.com`) von DigiCert verweist. Dieser CNAME-Datensatz gibt DigiCert an, dass Adobe berechtigt ist, das Zertifikat zu generieren. Adobe Client Care sendet Ihnen die Anweisungen mit den erforderlichen DNS-Aufzeichnungen. Ein Beispiel:

      ```
      3b0332e02daabf31651a5a0d81ba830a.target.example.com.  IN  CNAME  dcv.digicert.com.
      ```

      >[!NOTE]
      >
      >* Diese DCV-Token laufen nach 30 Tagen ab. Adobe Client Care wird Sie dann mit aktualisierten Token in Verbindung setzen. Damit Sie Ihre CNAME-Anforderung so schnell wie möglich lösen können, sollten Sie diese DNS-Änderungen an allen angeforderten Domänen vornehmen, bevor Sie Ihre Anforderung senden.
         >
         >
      * Wenn Ihre Domäne über [DNS-CAA-Einträge](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization)verfügt, müssen Sie `digicert.com` diese hinzufügen, wenn sie noch nicht hinzugefügt wurde. Dieser DNS-Datensatz gibt an, welche Zertifizierungsstellen zur Ausstellung von Zertifikaten für die Domäne berechtigt sind. Der resultierende DNS-Datensatz würde wie folgt aussehen: `example.com. IN CAA 0 issue "digicert.com"`. Mit [der G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CAA) können Sie ermitteln, ob Ihre Stammdomäne einen CAA-Datensatz enthält. Mehr darüber, wie DigiCert mit CAA-Aufzeichnungen umgeht, können Sie [hier](https://docs.digicert.com/manage-certificates/dns-caa-resource-record-check)lesen.


   * DigiCert versucht auch die E-Mail-Methode, bei der E-Mail-Nachrichten an Adressen gesendet werden, die in den WHOIS-Informationen der Domäne gefunden wurden, sowie an vorab festgelegte E-Mail-Adressen (Admin, Administrator, Webmaster, Hostmaster und Postmaster `@[domain_name]`). Weitere Informationen finden Sie in der Dokumentation [zu den](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) DCV-Methoden.

      Um den DCV-E-Mail-Prozess zu beschleunigen, gibt DigiCert die folgende Empfehlung ab:

      &quot;Vergewissern Sie sich, dass Ihre Registrierungsstelle/Ihr WHOIS-Anbieter die entsprechenden E-Mail-Adressen nicht maskiert oder entfernt hat. Falls ja, stellen Sie fest, ob sie eine Möglichkeit bieten (z.B. anonymisierte E-Mail-Adresse, Webformular), Zertifikatbehörden den Zugriff auf die WHOIS-Daten Ihrer Domäne zu ermöglichen.&quot;

1. Erstellen Sie einen CNAME-Eintrag im DNS Ihrer Domäne, der auf Ihren regulären Hostnamen verweist `clientcode.tt.omtrdc.net`. Wenn Ihr Client-Code z. B. &quot;cnamecustomer&quot;ist und Ihr Hostname angegeben ist `target.example.com`, sollte Ihr DNS-CNAME-Eintrag wie folgt aussehen:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Öffnen Sie ein [Adobe Client Care-Ticket, um CNAME-Unterstützung](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) für Ihre [!DNL Target] Anrufe anzufordern.

   Adobe arbeitet mit DigiCert zusammen, um Ihr Zertifikat auf den Produktionsservern von Adobe zu erwerben und bereitzustellen. DigiCert initiiert den DCV-Prozess, und Adobe Client Care benachrichtigt Sie, wenn Ihre Implementierung fertig ist.

1. Nachdem Sie die vorherigen Aufgaben abgeschlossen und Adobe ClientCare Sie darüber informiert haben, dass die Implementierung fertig ist, müssen Sie den neuen CNAME in at.js aktualisieren, `serverDomain` um den neuen CNAME zu erhalten.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAME-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat (auch BYOC) angeben? Wenn ja, wie sieht der Vorgang aus?

Ja, Sie können Ihr eigenes Zertifikat bereitstellen. wird jedoch nicht empfohlen. Die Verwaltung des SSL-Zertifikatlebenszyklus ist sowohl für Adobe als auch für Sie erheblich einfacher, wenn Adobe das Zertifikat kauft und steuert. SSL-Zertifikate müssen jedes Jahr erneuert werden. Das bedeutet, dass Adobe Client Care Sie jedes Jahr kontaktieren muss, um Adobe ein neues Zertifikat rechtzeitig zu senden. Manche Kunden haben möglicherweise Schwierigkeiten, jedes Jahr ein neues Zertifikat zeitnah zu erstellen, was ihre [!DNL Target] Implementierung gefährdet, da Browser die Verbindung nach Ablauf des Zertifikats verweigern.

>[!IMPORTANT]
>
>Wenn Sie eine CNAME-Implementierung mit [!DNL Target] eigenem Zertifikat anfordern, müssen Sie Adobe Client Care jedes Jahr neue Zertifikate zukommen lassen. Wenn Ihr CNAME-Zertifikat abläuft, bevor Adobe ein neues Zertifikat bereitstellen kann, führt dies zu einem Ausfall für Ihre spezifische [!DNL Target] Implementierung.

1. Überspringen Sie Schritt 1 oben, aber führen Sie die Schritte 2 und 3 aus. Wenn Sie ein Adobe Client Care-Ticket öffnen (Schritt 3), teilen Sie ihm mit, dass Sie Ihr eigenes Zertifikat bereitstellen werden.

   Adobe erstellt eine Anforderung zum Signieren von Zertifikaten (CSR) und sendet sie Ihnen zu.

1. Verwenden Sie den CSR, um das Zertifikat über Ihre ausgewählte Zertifizierungsstelle (CA) zu erwerben.

1. Senden Sie das neue öffentliche Zertifikat an Adobe. Adobe-Mitarbeiter stellen das öffentliche Zertifikat auf ihren Produktionsservern bereit.

1. Führen Sie Schritt 4 aus, nachdem Adobe Client Care Sie darüber informiert hat, dass die Implementierung fertig ist.

### Wie lange dauert es, bis mein neues SSL-Zertifikat abläuft?

Zertifikate, die vor dem 1. September 2020 ausgestellt werden, sind zweijährige Zertifikate. Zertifikate, die am oder nach dem 1. September 2020 ausgestellt werden, sind einjährige Zertifikate. Weitere Informationen zum Umstieg auf einjährige Zertifikate finden Sie [hier](https://www.digicert.com/position-on-1-year-certificates).

### Welche Hostnamen sollte ich wählen? Wie viele Hostnamen pro Domäne sollte ich wählen?

[!DNL Target] Für CNAME-Implementierungen ist nur ein Hostname pro Domäne im SSL-Zertifikat und im DNS des Kunden erforderlich. Daher empfehlen wir Ihnen Folgendes: Einige Kunden benötigen für ihre eigenen Zwecke (z. B. Testen im Staging) zusätzliche Hostnamen pro Domäne.

Die meisten Kunden wählen einen Hostnamen wie `target.example.com`, daher empfehlen wir Ihnen, aber die Wahl liegt letztendlich bei Ihnen. Achten Sie darauf, keinen Hostnamen eines vorhandenen DNS-Datensatzes anzufordern, da dies zu Konflikten und Verzögerungen bei der Auflösung Ihrer [!DNL Target] CNAME-Anforderung führen würde.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics], können wir dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, es [!DNL Target] ist ein separater Hostname und Zertifikat erforderlich.

### Hat meine aktuelle Implementierung von Zielgruppe Auswirkungen auf ITP 2.x?

Navigieren Sie in einem Safari-Browser zu Ihrer Website, auf der Sie über eine JavaScript-Zielgruppe verfügen. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

ITP-Probleme können für die Zielgruppe mit einem Analytics-CNAME gelöst werden. Sie benötigen einen separaten CNAME für Zielgruppen nur bei Werbeblockierungsszenarien, in denen die Zielgruppe blockiert ist.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Kann Adobe/DigiCert die DCV-E-Mails an eine andere E-Mail-Adresse senden `<someone>@example.com`?

Nein, DigiCert (oder eine Zertifizierungsstelle) erlaubt es nicht nur jedem, der unter einer Domäne eine E-Mail-Adresse hat, ein SSL-Zertifikat unter derselben Domäne zu autorisieren, es sei denn, diese E-Mail-Adresse ist auch in den WHOIS-Informationen der Domäne oder der vorab festgelegten Liste der Adressen enthalten (siehe oben). Dadurch wird sichergestellt, dass nur autorisierte Personen DCV für eine bestimmte Domäne genehmigen können. Sollte dies für Sie nicht möglich sein, empfehlen wir die Verwendung der DNS CNAME DCV-Methode (siehe oben).

### Wie kann ich überprüfen, ob meine CNAME-Implementierung für Traffic bereit ist?

Verwenden Sie die folgenden Befehle (im MacOs- oder Linux-Befehlszeilenterminal mit bash und curl 7.49+):

1. Fügen Sie zuerst diese Bash-Funktion in Ihr Terminal ein:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..32},34,35,37,38}.tt.omtrdc.net; do
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
   mboxedge17.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge21.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge22.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge26.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge28.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge29.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge30.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
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
