---
keywords: Implementation;mbox.js non javascript;redirector;costs per click;revenue per click
description: Verwenden Sie eine Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden.
title: Arbeiten mit Weiterleitungen
feature: email implementation
subtopic: Getting Started
topic: Standard
uuid: 79d7caf6-5693-4bb3-9131-8d1ae420fa5e
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 69%

---


# Arbeiten mit Weiterleitungen{#work-with-redirectors}

Verwenden Sie eine Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden.

Weiterleitungen werden mit einer speziellen Weiterleitungs-URL erstellt, die eine Weiterleitungs-Mbox (Weiterleitung) in Ihr Konto lädt. Verwenden Sie diese Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden. Senden Sie die Weiterleitungs-URL als Ziel-Link der Werbung an Ihr Werbenetzwerk.

Verwenden Sie die Weiterleitung, um  folgende Aktionen auszuführen:

* Klicks von Ihren Display-Anzeigen auf Ihre Seite zu verfolgen
* Einen einzigen, zentralisierten Bericht zur Verfolgung von Klicks auf Display-Anzeigen in mehreren Werbenetzwerken zu erstellen
* Die Display-Anzeigen und Ziele zu variieren

   Beispielsweise kann dasselbe Banner auf Ihre Startseite, Kategorieseite oder Produktseite verweisen.

* Finden Sie heraus, welche Landingpage die meisten Konversionen bringt.

Hilfe zur Entscheidung über die richtigen Einstellungen finden Sie unter  [Nicht-JavaScript-basierte Implementierungen](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

## Create a redirector {#redirector}

Bevor Sie eine Weiterleitung verwenden können, müssen Sie diese erst erstellen.

1. Legen Sie die Zielort-Variationen für die Werbeanzeige fest, inklusive Standard-Zielposition.
1. Erstellen Sie die Weiterleitungs-URL.

   ```
   https://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox
   /​page?mbox=redirectorlink_456
   &mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
   ```

   * Bei `yourclientcode` handelt es sich um den Clientcode Ihres Unternehmens. Der Clientcode Ihres Unternehmens enthält ausschließlich Kleinbuchstaben und keine Sonderzeichen.

      Your client code is available at the top of the [!UICONTROL Administration > Implementation] page of the [!DNL Target] interface.

   * `redirectorlink_456` ist der Name der Weiterleitungs-mbox, die in Ihrem Konto zur Verwendung für Kampagnen und Tests angezeigt wird.

      Weiterleitungen funktionieren anders als andere Mboxes, erscheinen in Ihrem Konto aber so wie beliebige andere Mboxes. Benennen Sie die Weiterleitung so, dass sie sich einfach von den Standard-Mboxes in Ihrem Konto unterscheiden lässt.  Es hat sich bewährt, den Mbox-Namen mit „redirectorlink“ beginnen zu lassen.

   * `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm` ist das Standardziel.

      Hierbei muss es sich um einen URL-kodierten, absoluten Verweis handeln. You can use the [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) to quickly encodes your URLs.

      >[!IMPORTANT]
      >
      >Beachten Sie, dass Sie mit der Weiterleitung dem Risiko einer Open-Redirect-Verwundbarkeit ausgesetzt sein können. Um die unbefugte Verwendung von Weiterleitungs-Links durch Dritte zu vermeiden, empfehlen wir die Verwendung von &quot;autorisierten Hosts&quot;, um die Standard-URL-Domänen für die Weiterleitung zu Zulassungslisten. Zielgruppe verwendet Hosts für Zulassungslisten-Domänen, zu denen Sie Umleitungen zulassen möchten. Weitere Informationen finden Sie unter Zulassungslisten [erstellen, die Hosts angeben, die zum Senden von Mbox-Aufrufen an die Zielgruppe](/help/administrating-target/hosts.md#allowlist) in *Hosts* berechtigt sind.

1. Validieren Sie die Weiterleitung.
   1. *Best Practice* im Bereich Sicherheit: Stellen Sie sicher, dass die in der Weiterleitung verwendete Domäne auf die Zulassungsliste gesetzt ist, wie oben angegeben. Wenn Sie eine Domäne verwenden, die nicht auf die Zulassungsliste gesetzt wird, blockiert Adobe alle Aufrufe dieser Domäne, um zu verhindern, dass böswillige Akteure die Weiterleitung verwenden, um zu potenziell böswilligen Domänen umzuleiten.
   1. Fügen Sie die Weiterleitungs-URL in eine Browserzeile ein, und aktualisieren Sie den Browser.
   1. Melden Sie sich bei Ihrem Konto an, aktualisieren Sie Ihre Mbox-Liste, und überprüfen Sie, ob die neue Weiterleitung als Mbox aufgelistet wird.
1. Um verschiedene Ziele für eine Anzeige zu testen, erstellen Sie [Weiterleitungsangebote](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) für jede Version.
1. Erstellen Sie die Kampagne.

   Unter [Nicht-JavaScript-basierte Implementierungen](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) finden Sie die richtigen Einstellungen, um Ihre Ziele zu erreichen.
1. Führen Sie die Qualitätssicherung für die Kampagne durch.

   Erstellen Sie eine Platzhalterseite mit einem `<a href>`, der die Weiterleitungs-URL enthält. Beispiel:

   ```
   <a href=https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=
   
   redirectorlink_456&mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​usualdestination%2Ehtm>
   ```

1. Überprüfen Sie, ob alle Erlebnisse, Standardinhalte und Berichte wie erwartet in allen Browsern und für alle Ihre Umgebungen funktionieren.

   >[!NOTE]
   >
   >* Weiterleitungen werden von der Angebotsvorschau oder Mbox-Suche nicht unterstützt. Zeigen Sie eine Vorschau der Erlebnisse direkt in einem Browser an.
   >* `mboxDebug` funktioniert bei Weiterleitungen nicht.


1. Senden Sie die vollständige Weiterleitungs-URL als Zielort der Display-Anzeige an Ihr Display-Anzeigenetzwerk.

## Use a redirector to pass Costs per Click and Revenue Per Click {#concept_3078EF48E9C44B34992D62AAB9628853}

Informationen zum Verwenden einer Weiterleitung zum Übergeben der Kosten pro Klick und vom Umsatz pro Klick.

### Übergeben der Kosten pro Klick {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Verwenden Sie eine Weiterleitung, um die Kosten pro Klick weiterzugeben.

>[!NOTE]
>
>Best practice is to determine the cost value using the **Score per visit** engagement metric.

Fügen Sie `&mboxPageValue=-value` zur URL hinzu. Beachten Sie den Negativwert.

Beispiel: Für Kosten pro Klick in Höhe von 0,10 Cent:

```
https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&mboxPageValue=-0.1&mboxDefault=​https://www.yourcompany.com/usualdestination.htm
```

### Übergeben vom Umsatz pro Klick  {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Verwenden Sie eine Weiterleitung, um den Umsatz pro Klick weiterzugeben.

>[!NOTE]
>
>Best practice is to determine the revenue value using the **Score per visit** engagement metric.

Fügen Sie `&mboxPageValue=value` zur URL hinzu.

Beispiel: Für Umsatz pro Klick in Höhe von 0,10 Cent.

```
https://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&mboxPageValue=0.1​&mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```
