---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: a2e4a4d1036d2c56d752d808054f6f4b4ab1d411

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Instructions about working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, sodass Aufrufe an eine Domäne des Kunden statt an eine Domäne im Besitz von Adobe erfolgen.

## CNAME-Unterstützung anfordern

Perform the following steps to request CNAME support in [!DNL Target]:

1. Die Zertifizierungsstelle von Adobe (DigiCert) muss überprüfen, ob Adobe berechtigt ist, Zertifikate unter Ihrer Domäne zu generieren.

   DigiCert ruft diesen Prozess [zur Überprüfung](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) der Domänenkontrolle (DCV) auf. Adobe darf erst nach Abschluss dieses Vorgangs ein Zertifikat unter Ihrer Domäne generieren.

   DCV verwendet einige Methoden. Vor dem Öffnen eines Adobe Client Care Tickets (Schritt 3) können Sie einige Schritte ausführen, um den DCV-Prozess zu beschleunigen:

   * DigiCert wird zunächst die E-Mail-Methode ausprobieren, bei der E-Mails an Adressen gesendet werden, die in den WHOIS-Informationen der Domäne enthalten sind, sowie an vorab festgelegte E-Mail-Adressen (Admin, Administrator, Webmaster, Hostmaster und Postmaster `@[domain_name]`). Weitere Informationen finden Sie in der Dokumentation[ zu den ](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/)DCV-Methoden.

      Um den DCV-E-Mail-Prozess zu beschleunigen, gibt DigiCert die folgende Empfehlung ab:

      "Vergewissern Sie sich, dass Ihr Registrar/WHOIS-Anbieter keine [relevanten E-Mail-Adressen]maskiert oder entfernt hat. Falls ja, stellen Sie fest, ob sie eine Möglichkeit bieten (z.B. anonymisierte E-Mail-Adresse, Webformular), [Zertifikatbehörden] den Zugriff auf die WHOIS-Daten Ihrer Domäne zu ermöglichen."

   * Wenn die DCV-E-Mail-Methode keine Option für Sie ist, ist die nächste Methode die DNS-TXT-Methode, bei der Sie Ihrer Domäne einen DNS-TXT-Datensatz mit einem Hashwert hinzufügen. Dieser TXT-Datensatz gibt DigiCert an, dass Adobe berechtigt ist, das Zertifikat zu generieren. Wenn Sie diese Methode verwenden müssen, teilen Sie dem Kundendienst von Adobe mit, wenn Sie ein Ticket öffnen (Schritt 3). Dadurch wird der DCV-Prozess beschleunigt.

1. Erstellen Sie einen CNAME-Eintrag im DNS Ihrer Domäne, der auf Ihren regulären Hostnamen verweist `clientcode.tt.omtrdc.net`. Wenn Ihr Client-Code z. B. "cnamecustomer"ist und Ihr Hostname angegeben ist `target.example.com`, sollte Ihr DNS-CNAME-Eintrag wie folgt aussehen:

   ```
   target.example.com  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Öffnen Sie ein [Adobe Client Care-Ticket, um CNAME-Unterstützung](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) für Ihre [!DNL Target] Anrufe anzufordern.

   Adobe arbeitet mit DigiCert zusammen, um Ihr Zertifikat auf den Produktionsservern von Adobe zu erwerben und bereitzustellen. DigiCert initiiert den DCV-Prozess, und Adobe Client Care benachrichtigt Sie, wenn Ihre Implementierung fertig ist.

1. Nachdem Sie die vorhergehenden Aufgaben ausgeführt haben und Adobe Client Care Sie darüber informiert hat, dass die Implementierung fertig ist, müssen Sie den neuen CNAME in at.js `serverDomain` aktualisieren.

## Häufig gestellte Fragen  

Die folgenden Informationen beantworten häufig gestellte Fragen zum Anfordern und Implementieren von CNAM-Unterstützung in [!DNL Target]:

### Kann ich ein eigenes Zertifikat bereitstellen? Wenn ja, wie läuft das?

Ja, dazu können Sie ein eigenes Zertifikat angeben:

1. Überspringen Sie Schritt 1 oben, aber führen Sie die Schritte 2 und 3 aus. Wenn Sie ein Adobe Client Care-Ticket öffnen (Schritt 3), teilen Sie ihm mit, dass Sie Ihr eigenes Zertifikat bereitstellen.

   Adobe erstellt eine Anforderung zum Signieren von Zertifikaten (CSR) und sendet sie Ihnen zu.

1. Verwenden Sie den CSR, um das Zertifikat über Ihre ausgewählte Zertifizierungsstelle (CA) zu erwerben.

1. Senden Sie das neue öffentliche Zertifikat an Adobe. Adobe-Mitarbeiter stellen das öffentliche Zertifikat auf ihren Produktionsservern bereit.

1. Führen Sie Schritt 4 aus, nachdem Adobe Client Care Sie darüber informiert hat, dass die Implementierung fertig ist.

### Ich habe bereits eine CNAME-Implementierung für [!DNL Adobe Analytics], können wir dasselbe Zertifikat oder denselben Hostnamen verwenden?

Nein, es [!DNL Target] ist ein separater Hostname und Zertifikat erforderlich.

### Ist meine aktuelle Implementierung von Target von ITP 2.1 oder 2.2 betroffen?

Navigieren Sie in einem Safari-Browser zu Ihrer Website, auf der Sie über eine Target-JavaScript-Bibliothek verfügen. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

ITP-Probleme können für Target nur mit einem Analytics-CNAME gelöst werden. Sie benötigen einen separaten Target-CNAME nur bei Werbeblockierungsszenarien, in denen Target blockiert ist.

Weitere Informationen zu ITP finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Wie kann ich überprüfen, ob meine CNAME-Implementierung für Traffic bereit ist?

Verwenden Sie die folgenden Befehle (im MacOs- oder Linux-Befehlszeilenterminal mit bash und curl 7.49+):

1. Fügen Sie zuerst diese Bash-Funktion in Ihr Terminal ein:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..33}}.tt.omtrdc.net; do
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
   mboxedge33.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Validieren Sie Ihren neuen DNS-CNAME mit einer anderen Curl-Anforderung, die auch Folgendes anzeigen sollte `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Wenn dieser Befehl fehlschlägt, aber der obige `validateEdgeFpsslSni` Befehl erfolgreich ausgeführt wird, müssen Sie möglicherweise warten, bis Ihre DNS-Updates vollständig übertragen werden.
