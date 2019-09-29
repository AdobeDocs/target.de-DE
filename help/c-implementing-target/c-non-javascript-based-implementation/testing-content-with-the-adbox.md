---
description: Stellen Sie mithilfe einer AdBox Bilder in einer externen Implementierung bereit.
keywords: Implementierung; mbox.js nicht-JavaScript; Mbox; AdBox
seo-description: Stellen Sie mithilfe einer AdBox Bilder in einer externen Implementierung bereit.
seo-title: Erstellen einer AdBox für ein Bild
solution: Target
subtopic: Erste Schritte
title: Erstellen einer AdBox für ein Bild
topic: Standard
uuid: 6b1763f7-08de-4bde-9e20-e79b92b02f20
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Erstellen einer AdBox für ein Bild{#create-an-adbox-for-an-image}

Stellen Sie mithilfe einer AdBox Bilder in einer externen Implementierung bereit.

Eine AdBox funktioniert wie eine Mbox, wird aber mithilfe einer URL statt mit JavaScript gesteuert. AdBoxes werden mit einer speziellen AdBox-URL erstellt, die eine „Werbeanzeigen“-Mbox (oder AdBox) in Ihr Adobe-Konto lädt. Verwenden Sie diese AdBox anstelle der Mbox für Ihre Aktivitäten. Verwenden Sie die AdBox-URL anstelle eines direkten Bildverweises in E-Mail- oder anderen Nicht-JavaScript-Implementierungen.

Hilfe zur Auswahl der richtigen Einstellungen finden Sie unter  [Nicht-JavaScript-basierte Implementierungen](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

1. Erstellen der AdBox-URL:

   ```
   https://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/
   image?mbox=emailHeroImage123_320x200
   mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif
   ```

   * Bei `myClientCode` handelt es sich um den Clientcode Ihres Unternehmens. Der Clientcode Ihres Unternehmens enthält ausschließlich Kleinbuchstaben und keine Sonderzeichen.

      * **at.js**: Ihren Clientcode finden Sie in der [!UICONTROL -Benutzeroberfläche unter ]„Einrichten“ &gt; „Implementierung“ ganz oben auf der Seite „at.js-Einstellungen bearbeiten“[!DNL Target].

      * **mbox.js**: Ihren Clientcode finden Sie oben auf der Seite [!UICONTROL „Einrichten“ &gt; „Implementierung“ &gt; „mbox.js-Einstellungen bearbeiten“].
   * Bei `image` handelt es sich um den Aufruftyp. In diesem Fall handelt es sich um ein Bild.

   * Bei `emailHeroImage123_320x200` handelt es sich um den Namen der AdBox.

   * Bei `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif` handelt es sich um den Standardinhalt der Mbox. Dabei muss es sich um ein Bild handeln.

      Hierbei muss es sich um einen URL-kodierten, absoluten Verweis handeln. You can use the [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) to quickly encode your URLs.


1. Erstellen Sie [Weiterleitungsangebote](../../c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) für alle alternativen Bilder.

   >[!NOTE] {class="- topic/note "}
   >
   >In AdBoxes muss ein Weiterleitungsangebot oder das standardmäßige Inhaltsangebot geladen sein. Andere Angebotstypen funktionieren nicht. Da es sich bei der AdBox um eine URL handelt, können nur die URLs angezeigt werden, die sie empfängt, weshalb nur die Weiterleitungsangebote funktionieren.

1. Erstellen Sie die Aktivität.

   Unter [Nicht-JavaScript-basierte Implementierungen](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) finden Sie die richtigen Einstellungen, um Ihre Ziele zu erreichen.
1. Führen Sie die Qualitätssicherung für die Aktivität durch.

   Es hat sich bewährt, eine Platzhalter-Seite zu erstellen und sicherzustellen, dass alle Erlebnisse, Standardinhalte und Berichte wie erwartet in allen Browsern und für alle Ihre Umgebungen funktionieren. 1. Starten Sie die Aktivität.
