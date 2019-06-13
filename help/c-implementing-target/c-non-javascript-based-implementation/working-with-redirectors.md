---
description: Verwenden Sie eine Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden.
keywords: Implementierung; mbox.js nicht-JavaScript; Weiterleitung; Kosten pro Klick; Umsatz pro Klick
seo-description: Verwenden Sie eine Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden.
seo-title: Arbeiten mit Weiterleitungen
solution: Target
subtopic: Erste Schritte
title: Arbeiten mit Weiterleitungen
topic: Standard
uuid: 79d7caf6-5693-4bb3-9131-8d1ae420fa5e
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Arbeiten mit Weiterleitungen{#work-with-redirectors}

Verwenden Sie eine Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden.

Weiterleitungen werden mit einer speziellen Weiterleitungs-URL erstellt, die eine Weiterleitungs-Mbox (Weiterleitung) in Ihr Konto lädt. Verwenden Sie diese Weiterleitung auf ähnliche Weise, wie Sie eine Mbox für Ihre Tests verwenden. Senden Sie die Weiterleitungs-URL als Ziel-Link der Werbung an Ihr Werbenetzwerk.

Verwenden Sie die Weiterleitung, um folgende Aktionen auszuführen:

* Klicks von Ihren Display-Anzeigen auf Ihre Seite zu verfolgen
* Einen einzigen, zentralisierten Bericht zur Verfolgung von Klicks auf Display-Anzeigen in mehreren Werbenetzwerken zu erstellen
* Die Display-Anzeigen und Ziele zu variieren

   Beispielsweise kann dasselbe Banner auf Ihre Startseite, Kategorieseite oder Produktseite verweisen.

* Finden Sie heraus, welche Landingpage die meisten Konversionen bringt.

Hilfe zur Entscheidung über die richtigen Einstellungen finden Sie unter [Nicht-JavaScript-basierte Implementierungen](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

## Erstellen einer Weiterleitung {#task_76608B0F73FC45C4A9F125B894DCF821}

Bevor Sie eine Weiterleitung verwenden können, müssen Sie diese erst erstellen.

1. Legen Sie die Zielort-Variationen für die Werbeanzeige fest, inklusive Standard-Zielposition.
1. Erstellen Sie die Weiterleitungs-URL.

   ```
   https://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox
   /​page?mbox=redirectorlink_456
   &mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
   ```

   * Bei `yourclientcode` handelt es sich um den Clientcode Ihres Unternehmens. Der Clientcode Ihres Unternehmens enthält ausschließlich Kleinbuchstaben und keine Sonderzeichen.

      * **at.js**: Ihren Clientcode finden Sie in der [!UICONTROL -Benutzeroberfläche unter ]„Einrichten“ &gt; „Implementierung“ ganz oben auf der Seite „at.js-Einstellungen bearbeiten“[!DNL Target].

      * **mbox.js**: Ihren Clientcode finden Sie oben auf der Seite [!UICONTROL „Einrichten“ &gt; „Implementierung“ &gt; „mbox.js-Einstellungen bearbeiten“].
   * `redirectorlink_456` ist der Name der Weiterleitungs-mbox, die in Ihrem Konto zur Verwendung für Kampagnen und Tests angezeigt wird.

      Weiterleitungen funktionieren anders als andere Mboxes, erscheinen in Ihrem Konto aber so wie beliebige andere Mboxes. Benennen Sie die Weiterleitung so, dass sie sich einfach von den Standard-Mboxes in Ihrem Konto unterscheiden lässt.  Es hat sich bewährt, den Mbox-Namen mit „redirectorlink“ beginnen zu lassen.

   * `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm` ist das Standardziel.

      Hierbei muss es sich um einen URL-kodierten, absoluten Verweis handeln. Sie können die [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) verwenden, um Ihre URLs schnell zu kodieren.



1. Validieren Sie die Weiterleitung.
   1. Fügen Sie die Weiterleitungs-URL in eine Browserzeile ein, und aktualisieren Sie den Browser.
   1. Melden Sie sich bei Ihrem Konto an, aktualisieren Sie Ihre Mbox-Liste, und überprüfen Sie, ob die neue Weiterleitung als Mbox aufgelistet wird.
1. Um verschiedene Ziele für eine Anzeige zu testen, erstellen Sie [Weiterleitungsangebote](../../c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) für jede Version.
1. Erstellen Sie die Kampagne.

   Unter [Nicht-JavaScript-basierte Implementierungen](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) finden Sie die richtigen Einstellungen, um Ihre Ziele zu erreichen.
1. Führen Sie die Qualitätssicherung für die Kampagne durch.

   Erstellen Sie eine Platzhalterseite mit einem `<a href>`, der die Weiterleitungs-URL enthält. Beispiel:

   ```
   <a href=https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=
   
   redirectorlink_456&mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​usualdestination%2Ehtm>
   ```

1. Überprüfen Sie, ob alle Erlebnisse, Standardinhalte und Berichte wie erwartet in allen Browsern und für alle Ihre Umgebungen funktionieren.

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >* Weiterleitungen werden von der Angebotsvorschau oder Mbox-Suche nicht unterstützt. Zeigen Sie eine Vorschau der Erlebnisse direkt in einem Browser an.
   >* `mboxDebug` funktioniert bei Weiterleitungen nicht.


1. Senden Sie die vollständige Weiterleitungs-URL als Zielort der Display-Anzeige an Ihr Display-Anzeigenetzwerk.

## Verwenden einer Weiterleitung zum Übergeben der Kosten pro Klick und vom Umsatz pro Klick {#concept_3078EF48E9C44B34992D62AAB9628853}

Informationen zum Verwenden einer Weiterleitung zum Übergeben der Kosten pro Klick und vom Umsatz pro Klick.

### Übergeben der Kosten pro Klick {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Verwenden Sie eine Weiterleitung, um die Kosten pro Klick weiterzugeben.

>[!NOTE]
>
>Es wird empfohlen, den Kostenwert mithilfe der Interaktionsmetrik **Ergebnis pro Besuch** zu bestimmen, wie unter [Interaktion](https://marketing.adobe.com/resources/help/de_DE/tnt/help/c_Capturing_Engagement.html) beschrieben.

Fügen Sie `&mboxPageValue=-value` zur URL hinzu. Beachten Sie den Negativwert.

Beispiel: Für Kosten pro Klick in Höhe von 0,10 Cent:

```
https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&mboxPageValue=-0.1&mboxDefault=​https://www.yourcompany.com/usualdestination.htm
```

### Übergeben vom Umsatz pro Klick {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Verwenden Sie eine Weiterleitung, um den Umsatz pro Klick weiterzugeben.

>[!NOTE]
>
>Es wird empfohlen, den Umsatzwert mithilfe der Interaktionsmetrik **Ergebnis pro Besuch** zu bestimmen, wie unter [Interaktion](https://marketing.adobe.com/resources/help/de_DE/tnt/help/c_Capturing_Engagement.html) beschrieben.

Fügen Sie `&mboxPageValue=value` zur URL hinzu.

Beispiel: Für Umsatz pro Klick in Höhe von 0,10 Cent.

```
https://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&mboxPageValue=0.1​&mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```
