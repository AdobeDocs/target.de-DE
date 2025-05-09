---
keywords: Visual Experience Composer-Optionen;Experience Composer-Optionen;Erlebnisoptionen;Text bearbeiten;HTML bearbeiten;Text/HTML bearbeiten;Hintergrundfarbe bearbeiten;Hintergrundfarbe;Element einfügen;Link bearbeiten;Visual Experience Composer-Link;CSS-Klasse bearbeiten;CSS-Klasse;CSS-Klasse;Angebot wechseln;Angebot vertauschen;Bild vertauschen;Bild vertauschen;Element entfernen;Element entfernen;Element ausblenden;Element neu anordnen;Element verschieben;Elementgröße ändern;Element vergrößern;Auswahl erweitern;zu diesem Link navigieren;Link navigieren;navigieren;Link navigieren;Link navigieren;Link;Rückgängig;Wiederholen;Wiederholen;benutzerspezifische Ereignisse;Ereignisse;Web-Komponenten;Angebot Entscheidung;Offer Decisioning
description: Erkunden Sie die in der (VEC [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] verfügbaren Optionen.
title: Wie verwende ich die [!UICONTROL Visual Experience Composer] (VEC)-Optionen?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: b1fb49d78b3a159c16e8ebb855ff175c26681da6
workflow-type: tm+mt
source-wordcount: '1861'
ht-degree: 9%

---

# Visual Experience Composer-Optionen

Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die aktualisierte Benutzeroberfläche und ihre Optionen erläutert.

>[!TIP]
>
>Informationen dazu, wie sich der aktualisierte VEC vom alten VEC unterscheidet, finden Sie unter [Änderungen am Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md).

>[!IMPORTANT]
>
>Für die aktualisierte [!UICONTROL Visual Editing Composer] ist die [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper]-Erweiterung erforderlich](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) die auf der [!DNL Chrome Web Store] verfügbar ist.

Der VEC wird angezeigt, wenn Sie eine vorhandene Aktivität erstellen oder bearbeiten.

![Visual Experience Composer (VEC)](/help/main/c-experiences/c-visual-experience-composer/assets/new-vec.png)

## Übersicht über die VEC-Benutzeroberfläche

In den folgenden Abschnitten werden die im aktualisierten VEC verfügbaren Optionen für eine [!UICONTROL A/B Test] Aktivität erläutert. Die Optionen variieren je nach Aktivitätstyp.

### [!UICONTROL Experiences]

Die [!UICONTROL Experiences] wird in der linken Leiste des VEC angezeigt.

![Leiste „Erlebnisse“](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

Sie können Erlebnisse über die [!UICONTROL Experiences] Leiste anzeigen, erstellen, umbenennen oder entfernen.

Die folgenden Optionen sind in der [!UICONTROL Experiences] Leiste verfügbar:

* **Erlebnis anzeigen**: Um ein Erlebnis anzuzeigen, klicken Sie auf das gewünschte Erlebnis, um es auf der [!UICONTROL Design]-Arbeitsfläche anzuzeigen.
* **Erlebnis hinzufügen**: Klicken Sie auf das **[!UICONTROL Add]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ), um ein neues Erlebnis hinzuzufügen. Konfigurieren Sie das neue Erlebnis nach Bedarf.
* **Erlebnis umbenennen**: Klicken Sie auf das Symbol &quot;**[!UICONTROL Rename]**&quot; ( ![Symbol „Umbenennen](/help/main/assets/icons/Rename.svg) ), um das Dialogfeld &quot;[!UICONTROL Rename Experience]&quot; anzuzeigen. Geben Sie den neuen Namen an und klicken Sie dann auf **[!UICONTROL Save]**.
* **Erlebnis duplizieren, löschen oder umleiten**: Klicken Sie auf das **[!UICONTROL More Actions]** ( ![Mehr Aktionen-](/help/main/assets/icons/MoreSmall.svg) ) und wählen Sie dann **[!UICONTROL Duplicate]**, **[!UICONTROL Delete]** oder **[!UICONTROL Redirect to URL]** aus.

### Aktivitätseinstellungen/-konfiguration {#settings}

Klicken Sie auf das [!UICONTROL Configure] ( ![Symbol konfigurieren](/help/main/assets/icons/Setting.svg) ), das über der Arbeitsfläche [!UICONTROL Design] angezeigt wird, um das Menü mit den Eigenschaften der Aktivität anzuzeigen.

![Konfigurationsoptionen für Aktivitäten](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

Die folgenden Optionen sind verfügbar:

* **[!UICONTROL Properties]**: Weisen Sie der Aktivität Eigenschaften zu oder entfernen Sie Eigenschaften aus der Aktivität. [!UICONTROL Properties] ist eine ([[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) Funktion. Weitere Informationen finden Sie unter [Enterprise-Benutzerberechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).
* **[!UICONTROL Page Delivery]**: Gleiches Erlebnis auf ähnlichen Seiten Ihrer Site. Verwenden Sie eine Seitenvorlage, um Ihren Seiten eine Struktur zu verleihen, oder wenn Ihre Seiten ähnliche Elemente enthalten, um Variationen in ähnlich strukturierten Seitenelementen oder in Ihrer gesamten Domain zu testen. Weitere Informationen finden Sie unter [Gleiches Erlebnis auf ähnlichen Seiten](/help/main/c-experiences/c-visual-experience-composer/temtest.md).
* **[!UICONTROL Site Preferences]**: Konfigurieren Sie Ihre Site-Voreinstellungen, um festzulegen, wie [!DNL Target] CSS-Selektoren generiert. Weitere Informationen finden Sie unter _CSS-Selektoren_ in [Konfigurieren der [!UICONTROL Visual Experience Composer]](/help/main/administrating-target/visual-experience-composer-set-up.md).
* **Zusätzliche Seiten hinzufügen**: Fügen Sie der Aktivität zusätzliche Seiten hinzu, um eine mehrseitige Aktivität zu erstellen, mit der Sie eine Story über mehrere Seiten hinweg erstellen können. Das Design ist für jede Seite spezifisch. Weitere Informationen finden Sie unter [Mehrseitige Aktivität](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md).
* **Einzelne Zielgruppe**: Verwenden Sie eine einzelne Zielgruppe für die Aktivität.
* **Mehrere Zielgruppen**: Weisen Sie der Aktivität mehrere Zielgruppen zu. Klicken Sie auf das Symbol Zielgruppen hinzufügen ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) und wählen Sie dann eine oder mehrere Zielgruppen aus der Liste aus. Sie können [ Dialogfeld [!UICONTROL Add Audiences] auch ](/help/main/c-target/combining-multiple-audiences.md)Zielgruppen kombinieren[ oder ](/help/main/c-target/c-audiences/create-audience.md) neue Zielgruppe erstellen.

### [!UICONTROL Design]-/[!UICONTROL Browse]

Verwenden Sie die [!UICONTROL Design]/[!UICONTROL Browse] Umschalter, die oben auf der Design-Arbeitsfläche angezeigt werden, um zwischen Design- und Durchsuchen-Modus zu wechseln.

![Umschalter zum Entwerfen und Durchsuchen](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

Verwenden Sie den [!UICONTROL Browse] , um auf Ihrer Site zu navigieren und die Ansicht oder Seite auszuwählen, die Sie aktualisieren möchten. Wechseln Sie zurück in den [!UICONTROL Design], um Ihre Änderungen hinzuzufügen oder zu bearbeiten.

### [!UICONTROL Undo]/[!UICONTROL Redo]

Sie können die vorgenommenen Änderungen rückgängig machen, indem Sie auf das [!UICONTROL Undo] klicken ( ![Rückgängig-Symbol](/help/main/assets/icons/Undo.svg) ).

![Symbol „Rückgängig“ in VEC](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

Um eine Aktion wiederherzustellen, erweitern Sie die Rückgängig/[!UICONTROL Redo]-Schaltflächengruppe und wählen Sie [!UICONTROL Redo] aus.

### [!UICONTROL Components]

Sie können Ihrer Web-Seite eine Reihe von Komponenten hinzufügen und diese nach Bedarf bearbeiten, indem Sie die neue [!UICONTROL Components] Leiste verwenden.

![Komponentenleiste](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

>[!NOTE]
>
>Wenn in diesem Bereich die [!UICONTROL Modifications] statt der [!UICONTROL Components] Leiste angezeigt wird, klicken Sie auf das **[!UICONTROL Show Components]** ( ![Symbol „Komponenten anzeigen](/help/main/assets/icons/Add.svg) ). Das [!UICONTROL Show Components] ( ![Symbol „Komponenten anzeigen](/help/main/assets/icons/Add.svg) ) und das [!UICONTROL Show Modifications] ( ![Leiste „Änderungen anzeigen](/help/main/assets/icons/History.svg) ) dienen als Umschalter zum Anzeigen der entsprechenden Optionen.

So fügen Sie einem Erlebnis eine neue Komponente hinzu:

1. Klicken Sie auf die gewünschte Komponente, die Sie hinzufügen möchten, um sie zu markieren.

   Die verfügbaren Komponenten werden in logischen Containern gruppiert:

   * [!UICONTROL Basic]
      * [!UICONTROL Divider]
      * [!UICONTROL HTML]
      * [!UICONTROL Image]
   * [!UICONTROL Text]
      * [!UICONTROL Heading]
      * [!UICONTROL Paragraph]
      * [!UICONTROL Link]
   * [!UICONTROL Dynamic]
      * [[!UICONTROL Recommendation]](/help/main/c-recommendations/recommendations-as-an-offer.md)
      * [[!UICONTROL Experience Fragment]](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md)
      * [[!UICONTROL HTML Offer]](/help/main/c-experiences/c-manage-content/manage-content.md)

1. Ziehen Sie die Komponente auf ein vorhandenes Seitenelement auf der [!UICONTROL Design] Arbeitsfläche.
1. Wählen Sie diese Option, um die Komponente vor oder nach dem ausgewählten Element einzufügen.

   Im Vergleich zur vorherigen VEC-Version können Sie ein ausgewähltes Element nicht durch eine Komponente ersetzen.

### [!UICONTROL Modifications]

Um die [!UICONTROL Modifications] Leiste zu öffnen, klicken Sie auf das Symbol [!UICONTROL Show Modifications] ( ![Leiste „Änderungen anzeigen](/help/main/assets/icons/History.svg) ) in der [!UICONTROL Components] Leiste.

![Leiste „Änderungen](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

>[!NOTE]
>
>Das [!UICONTROL Show Components] ( ![Symbol „Komponenten anzeigen](/help/main/assets/icons/Add.svg) ) und das [!UICONTROL Show Modifications] ( ![Leiste „Änderungen anzeigen](/help/main/assets/icons/History.svg) ) dienen als Umschalter zum Anzeigen der entsprechenden Optionen.

In der [!UICONTROL Modifications] Leiste werden alle Änderungen angezeigt, die an Ihrer Seite im [!UICONTROL Visual Experience Composer] (VEC) vorgenommen wurden, und Sie können zusätzliche Änderungen vornehmen (z. B. CSS-Auswahl, Mbox und benutzerdefinierter Code).

Klicken Sie in der Kopfzeile der Leiste auf das **[!UICONTROL More Options]**-Symbol ![Mehr Aktionen](/help/main/assets/icons/MoreSmall.svg) ), um eine Änderung hinzuzufügen, alle Änderungen zu löschen oder alle ungültigen Änderungen zu löschen. Klicken Sie auf [!UICONTROL Select] , um Massenvorgänge durchzuführen: [!UICONTROL Apply to All Pages] oder [!UICONTROL Delete].

Klicken Sie auf das **[!UICONTROL More Options]**-Symbol ( ![Mehr Aktionen-](/help/main/assets/icons/MoreSmall.svg) ) neben jeder Änderung, um die zugehörigen Informationen anzuzeigen, die Änderung zu löschen oder die Änderung auf weitere Ansichten anzuwenden.

### [!UICONTROL Design]

Auf der [!UICONTROL Design] Arbeitsfläche können Sie Viewports auswählen, einschließlich „An Bildschirm anpassen“, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape] und [!UICONTROL Mobile Portrait]. Standardmäßig passt die Arbeitsfläche die Seite zusammen mit den im Abschnitt „Administration“ definierten Darstellungsfeldern [ den Bildschirm ](/help/main/administrating-target/visual-experience-composer-set-up.md).

![Viewport-Optionen](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

Sie können auch ein- oder auszoomen, indem Sie auf das entsprechende Symbol klicken ![Zoom-Symbol](/help/main/assets/icons/ZoomIn.svg) oder ![Zoom-Symbol](/help/main/assets/icons/ZoomOut.svg) ).

Wenn Sie auf ein Seitenelement auf der Arbeitsfläche [!UICONTROL Design] klicken, werden in einem Menü die Optionen angezeigt, die für diesen Elementtyp verfügbar sind. Darüber hinaus wird am unteren Rand der Seite ein DOM-Pfad angezeigt, mit dem Sie einfach durch die Seitenstruktur navigieren können.

Die verschiedenen [!UICONTROL Visual Experience Composer] (VEC)-Aktionen sind in entsprechenden Menüoptionen gruppiert, um Ihren Auftrag schneller und effizienter zu gestalten:

![VEC-Optionen-Menü](/help/main/c-experiences/c-visual-experience-composer/assets/vec-options.png)

>[!NOTE]
>
>Die verfügbaren Optionen hängen vom Aktivitätstyp und vom Element ab, das Sie erstellen oder bearbeiten. Weitere Informationen zum Bearbeiten von Bildern und Angeboten in einer [!UICONTROL A/B Test] Aktivität finden Sie [Elemente über die [!UICONTROL Design] Arbeitsfläche bearbeiten](#design) unten.

### [!UICONTROL Properties]

Mit der [!UICONTROL Properties] Leiste können Sie die Eigenschaften ausgewählter Seitenelemente ändern, unabhängig davon, ob es sich um HTML-Elemente oder [!DNL Target] Objekte wie Empfehlungen oder Angebote handelt.

![Eigenschaftenleiste](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

Klicken Sie auf die Symbole oben in der Leiste, um HTML-Code zu bearbeiten oder Elemente zu löschen, zu duplizieren oder auszublenden. Änderungen werden in der [!UICONTROL Modifications] Leiste angezeigt.

Die [!UICONTROL Properties] ist in der rechten Leiste ausblendbar. Klicken Sie auf das [!UICONTROL Show/Hide Properties]-Symbol ![Eigenschaftensymbol](/help/main/assets/icons/Propertie.svg) ) rechts neben der Leiste, um die [!UICONTROL Properties] Leiste zu reduzieren oder anzuzeigen.

## Bearbeiten von Elementen mithilfe der [!UICONTROL Design] Arbeitsfläche {#design}

Die folgenden Abschnitte zeigen Ihnen, wie Sie Bilder und Text auf der [!UICONTROL Design]-Arbeitsfläche bearbeiten. Die Arbeitsfläche des Designs stellt Ihnen zusammen mit den Leisten Komponenten, Änderungen und Eigenschaften leistungsstarke Tools zur Verfügung, mit denen Sie mühelos Erlebnisse für Ihre Aktivitäten erstellen können.

### Bildoptionen

Wenn Sie in einer [!UICONTROL A/B Test] Aktivität auf ein Bild klicken, sieht der VEC in etwa wie in der folgenden Abbildung aus:

![VEC mit ausgewähltem Bild](/help/main/c-experiences/c-visual-experience-composer/assets/vec-image.png)

Wählen Sie aus dem [!UICONTROL Components] auf der linken Seite Komponenten aus, um die folgenden Elemente einzufügen:

* Einfach (Unterteilung, HTML, Bild).
* Text (Überschrift, Absatz, Link).
* Dynamisch ([Empfehlung](/help/main/c-recommendations/recommendations-as-an-offer.md), [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), HTML-Angebot).

Im Menü oben im Bild können Sie Folgendes tun:

* Fügen Sie einen Link ein ( ![Symbol „Link einfügen](/help/main/assets/icons/Link.svg) ).
* Ändern Sie das Bild ( ![Symbol „Bild auswählen](/help/main/assets/icons/Images.svg) ).
* Personalisierung hinzufügen ( ![Symbol &quot;Personalization hinzufügen](/help/main/assets/icons/PersonalizationField.svg) ).
* Löschen Sie das Bild ( ![Löschsymbol](/help/main/assets/icons/Delete.svg) ).

Im [!UICONTROL Properties] Bereich auf der rechten Seite können Sie die Eigenschaften des Bildes weiter konfigurieren.

Über die Symbole oben im Frame können Sie Folgendes tun:

* Bearbeiten Sie die HTML ( ![Symbol &quot;HTML einfügen](/help/main/assets/icons/Code.svg) ). HTML Weitere Informationen finden [ unter &quot;](#html) bearbeiten“.
* Duplizieren Sie das Bild ( ![Duplikatsymbol](/help/main/assets/icons/Code.svg) ).
* Löschen Sie das Bild ( ![Löschsymbol](/help/main/assets/icons/Delete.svg) ).
* Bild ausblenden ( ![Symbol ausblenden](/help/main/assets/icons/VisibilityOff.svg) ).

Mit den Optionen im rechten Rahmen können Sie Folgendes tun:

* Bearbeiten Sie die CSS-Klasse.
* Konfigurieren Sie die Eigenschaften des Bildes (Quelle, Titel, Alternativtext).
* Link-URL bearbeiten.
* Konfigurieren Sie die Größe des Bildes (Höhe und Breite). Klicken Sie auf [!UICONTROL Show Advanced Options] , um die minimale und maximale Größe, Breite, Höhe, Überlauf und Objektanpassung des Bildes zu konfigurieren.
* Konfigurieren Sie die Position des Bildes auf Ihrer Seite (absolut, fest, relativ, statisch oder fixierbar).
* Konfigurieren Sie den Abstand des Elements, einschließlich Rand und Abstand.
* Konfigurieren Sie die Effekte des Elements (Deckkraft). Klicken Sie auf [!UICONTROL Show Advanced Options], um die Werte für Sepia, Graustufen, Kontrast, Helligkeit und Weichzeichnung des Bildes zu konfigurieren. Sie können das Bild auch invertieren oder drehen.
* Konfigurieren Sie die Inline-Stile des Bildes.

### Textoptionen

Wenn Sie auf Text in einer [!UICONTROL A/B Test] Aktivität klicken, sieht der VEC in etwa wie in der folgenden Abbildung aus:

![VEC mit ausgewähltem Text](/help/main/c-experiences/c-visual-experience-composer/assets/vec-text.png)

Wählen Sie aus dem [!UICONTROL Components] auf der linken Seite Komponenten aus, um die folgenden Elemente einzufügen:

* Einfach (Unterteilung, HTML, Bild).
* Text (Überschrift, Absatz, Link).
* Dynamisch ([Empfehlung](/help/main/c-recommendations/recommendations-as-an-offer.md), [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), HTML-Angebot).

Klicken Sie auf das [!UICONTROL Show Modifications] ( ![Symbol Änderungen anzeigen](/help/main/assets/icons/History.svg) ), um die Änderungen am Erlebnis anzuzeigen.

Das Menü oben im Textelement bietet folgende Möglichkeiten:

* Konfigurieren Sie die Eigenschaften des Textes (Überschriftenebene, Absatz, Blockzitat oder Monospace)
* Wählen Sie die Farbe des Textes aus ( ![Textfarbsymbol](/help/main/assets/icons/TextColor.svg) )
* Konfigurieren Sie die Attribute des Texts (fett, kursiv, unterstrichen oder durchgestrichen) (![Symbol „Textattribute auswählen“](/help/main/assets/icons/Text.svg)).
* Konfigurieren Sie die Ausrichtung des Textes (links, zentriert, rechts, Blocksatz) (![Symbol für Textausrichtung](/help/main/assets/icons/TextAlignCenter.svg) ).
* Fügen Sie einen Link ein ( ![Symbol „Link einfügen](/help/main/assets/icons/Link.svg) ).
* Ersetzen Sie den Inhalt durch ein HTML-Angebot[ „Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) oder [Recommendation](/help/main/c-recommendations/recommendations-as-an-offer.md).
* Bearbeiten Sie die HTML ( ![Symbol &quot;HTML einfügen](/help/main/assets/icons/Code.svg) ).
* Personalisierung hinzufügen ( ![Symbol &quot;Personalization hinzufügen](/help/main/assets/icons/PersonalizationField.svg) ).
* Löschen Sie das Bild ( ![Löschsymbol](/help/main/assets/icons/Delete.svg) ).

In der [!UICONTROL Properties] Leiste auf der rechten Seite können Sie die Eigenschaften des Textes weiter konfigurieren.

Über die Symbole oben im Frame können Sie Folgendes tun:

* Bearbeiten Sie die HTML ( ![Symbol &quot;HTML einfügen](/help/main/assets/icons/Code.svg) ). HTML Weitere Informationen finden [ unter &quot;](#html) bearbeiten“.
* Duplizieren Sie den Text ( ![Duplikatsymbol](/help/main/assets/icons/Code.svg) ).
* Löschen Sie den Text ( ![Löschsymbol](/help/main/assets/icons/Delete.svg) ).
* Blendet den Text aus ( ![Symbol ausblenden](/help/main/assets/icons/VisibilityOff.svg) ).

Mit den Optionen im rechten Rahmen können Sie Folgendes tun:

* Bearbeiten Sie die CSS-Klasse.
* Konfigurieren Sie die Hintergrundfarbe und das Bild des Textes.
* Konfigurieren Sie die Typografie des Textes (Überschriftenstil, Schriftgröße, Schriftstärke, Zeilenhöhe, Ausrichtung, Textfarbe, Textstil (fett, kursiv, unterstrichen oder durchgestrichen)).
* Konfigurieren von Listen, einschließlich Aufzählungszeichen, nummerierten Listen oder A, B, C.
* Wählen Sie die Rahmenfarbe.
* Konfigurieren der Größe des Textfelds (Höhe und Breite). Klicken Sie auf [!UICONTROL Show Advanced Options] , um die minimale und maximale Größe, Breite, Höhe, Überlauf und Objektanpassung des Textfelds zu konfigurieren.
* Konfigurieren Sie die Position des Textfelds auf Ihrer Seite (absolut, fest, relativ, statisch oder fixiert) und legen Sie die Anzahl der Pixel von oben, rechts, unten und links fest.
* Konfigurieren Sie den Abstand des Elements, einschließlich Rand und Abstand.
* Konfigurieren Sie die Effekte des Elements (Deckkraft). Klicken Sie auf [!UICONTROL Show Advanced Options], um die Werte für Sepia, Graustufen, Kontrast, Helligkeit und Weichzeichnung des Bildes zu konfigurieren. Sie können den Text auch invertieren oder drehen.
* Konfigurieren Sie die Inline-Stile.

## HTML bearbeiten

Neben HTML-Code können Sie auch benutzerdefiniertes JavaScript bearbeiten und einfügen.

Beim Bearbeiten von Text und HTML für [!UICONTROL A/B]- und [!UICONTROL Experience Targeting]-Aktivitäten stehen verschiedene Rich-Text-Formatierungsoptionen zur Verfügung. Sie können eine Schriftart und einen Schriftstil auswählen, die Textausrichtung ändern und andere Standardformatierungsoptionen für Texte anwenden. Beim Ändern von HTML können Sie zwischen der Code-Ansicht und der Rich-Editing-Ansicht von HTML wechseln.

Die folgenden HTML 5-Tags können verschachtelt sein:

| Tag | Zulässige verschachtelte Tags |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

## Navigieren in Elementen mithilfe des DOM-Pfads {#dom-path}

Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Zusätzlich wird, wenn Sie auf ein Element klicken, der entsprechende DOM-Pfad unten auf der Seite angezeigt.

![DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path-refresh.png)

Wenn der DOM-Pfad nicht angezeigt wird, klicken Sie auf das [!UICONTROL Show DOM] ( ![DOM-Symbol anzeigen](/help/main/assets/icons/LayersBringToFront.svg) ).

Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten verschieben, um das gewünschte Element auszuwählen.

<!--When you hover over the DOM path, a blue box highlights the corresponding element in the VEC. When you click the element, an orange box highlights the element and the VEC options menu displays, as explained above.-->

Mithilfe des DOM-Pfades können Sie mühelos zu jedem übergeordneten, parallelen oder untergeordneten Element innerhalb des VEC navigieren.

Die DOM-Pfad-Funktion ist auch verfügbar, wenn Sie das [Klick-Tracking](/help/main/c-activities/r-success-metrics/click-tracking.md) einrichten.

<!--## [!UICONTROL Edit]

The following options are available:

### [!UICONTROL Text/HTML] {#edit-text-html}

Change the HTML code for the element, such as the text for a text area, button, or link.

In addition to HTML code, you can edit and inject custom JavaScript.

Several rich text formatting options are available when editing text and HTML for [!UICONTROL A/B] and [!UICONTROL Experience Targeting] activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML.

The following HTML5 tags can be nested:

|Tag|Allowed Nested Tags|
| --- | --- |
|`<a>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>`|
|`<ins>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`|
|`<del>`|`<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>`|
|`<label>`|`<p>`|

### [!UICONTROL Background Color]

Use the color picker to select or configure a background color. You can select a color swatch, and adjust it using RGB values or color hex codes. The red x in the color picker makes the background transparent.

**Note:** This option is not available for an element where a background image is set. 

### [!UICONTROL Styles] {#styles}

Use the [!UICONTROL Styles] panel to view or edit the value of existing styles for the selected element. You can also add additional styling.

To access the [!UICONTROL Styles] panel, click a page element from within the VEC, then click **[!UICONTROL Edit]** > **[!UICONTROL Styles]**.

The [!UICONTROL Styles] panel displays on the right side of the VEC. The panel contains a list of styles that lets you edit or add to the selected element. A real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.

![Styles panel](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

As you apply different styles, you can always revert your changes by clicking the [!UICONTROL Revert] icon that displays at the top-right corner of the [!UICONTROL Styles] panel after you change any section. Clicking the [!UICONTROL Revert] icon reverts all changes on the current section's panel.

Expand each section to edit or add styles, as explained below. To save your changes, click the [!UICONTROL Back] icon at the top of the panel to return to the panel's main display, then click **[!UICONTROL Save]**. 

Blue dots on the main panel and next to each option on the various section panels indicate that you have changed the corresponding styles. This visual indicator makes it easy for you to review your changes before clicking [!UICONTROL Save].

>[!NOTE]
>
>Quick actions for layout changes, background color, resizing, and move are also available as separate actions in the VEC menu. These options can be used as separate actions or you can use the Styles menu, as explained here.

* **[!UICONTROL Background]**

  Change the background color and image.

  * Color (specify the color code or use the color picker)
  * Image (select an image from the image picker)
  * Image source (specify an external URL)
  * Attachment
    * Click the top drop-down list to select scroll, fixed, or local
    * Click the bottom drop-down list to select repeat, repeat-x, repeat-y, no-repeat, space, or round
  * Clip
    * Click the top drop-down list to select border-box, padding-box, content-box, or text
    * Click the bottom drop-down list to select auto audio or audio

* **[!UICONTROL Typography]**

  Change the typography of an element. Typography edits are quick and easy. 

  Although the rich text editor (Edit Text/HTML) is available for fine tuning, quick actions to change the entire element is available via this option. If you want to apply typography changes to only a part of the text (not to the full text), use the [rich text editor](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md). 

  You can edit the following typography styles:

  * [!UICONTROL Font size]
  * [!UICONTROL Font weight]
  * [!UICONTROL Font style]
  * [!UICONTROL Color] (specify the color code or use the color picker)
  * [!UICONTROL Word spacing]
  * [!UICONTROL Line height]
  * [!UICONTROL Text alignment]

* **[!UICONTROL Margin]**

  Change the margin for the selected element. You can change the left, right, bottom, and top margins.

  Click the drop-down icon for each margin to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to set the margin or specify the number of pixels for each margin)

  Margin supports positive and negative values.

  Target also supports other size units, such as rem, pc, em. For more information about these units, see [Web Style Sheets CSS Tips and Tricks](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Padding]**

  Change the padding for the selected element. You can change the left, right, bottom, and top padding.

  Drag the slider to set the padding or specify the number of pixels for padding.

  Padding supports width scales from 0 onwards.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Border]**

  Click the border icons at the top of the panel to change the selected element's border.

  You can edit the following styles for each border (top, right, bottom, and left):

  * [!UICONTROL Border style] (none, hidden, dotted, dashed, solid, or double)
  * [!UICONTROL Border color] (specify the color code or use the color picker)
  * [!UICONTROL Border width] (drag the slider to select a border width or specify the width in pixels)

  Border supports width scales from 0 onwards.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Position]**

  Move the selected element from its current position. You can change the element's top, bottom, left, right, and [Z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) position.

  Click the [!UICONTROL Static] drop-down list to choose from the following position options:

  * [!UICONTROL Static]
  * [!UICONTROL Relative]
  * [!UICONTROL Absolute]
  * [!UICONTROL Sticky]
  * [!UICONTROL Fixed]

  Click the drop-down icon for each position to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to position the element or specify the number of pixels you want to move the element)

  Position supports positive and negative values.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Size]**

  Change the selected element's width and height.

  Click the drop-down icon next to [!UICONTROL Width] and [!UICONTROL Height] to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to size the element or specify the number of pixels for each dimension)

* **[!UICONTROL Filter]**

  Drag the slider for each filter option or specify the desired percentage:

  * [!UICONTROL Sepia]
  * [!UICONTROL Contrast]
  * [!UICONTROL Brightness]
  * [!UICONTROL GrayScale]
  * [!UICONTROL Blur]
  * [!UICONTROL Opacity]
  * [!UICONTROL Invert]
  *[!UICONTROL  Hue-rotate]
  * [!UICONTROL Saturate]

* **[!UICONTROL CSS Editor]**

  The real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.

  The CSS Editor displays any changes that you make in the Styles panel. As shown in the illustration below, the font size, top border, and image size have been changed:

  ![CSS editor with changes](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  Notice the blue dots next to the [!UICONTROL Typography], [!UICONTROL Border], and [!UICONTROL Size] options in the preceding illustration. These dots indicate that you have changed these sections. If you open these section panels, blue dots display next to the specific options that you changed.

  You can type your own code if your desired style is not available by default in the [!UICONTROL Styles].

  The CSS Editor shows details for the current session only. If you save changes and then reopen the editor, details about your previous change do not display in the editor, even if you select the same element again.

  >[!IMPORTANT]
  >
  >You can apply a background image using the CSS Editor, but it might cause flicker. Test your changes before deployment.

### [!UICONTROL CSS Class]

Specify the predefined CSS class used for the element. If more than one element is selected, separate multiple CSS classes with a space.

Available for [!UICONTROL A/B], [!UICONTROL Automated Personalization], and [!UICONTROL Multivariate Test] activities.

### [!UICONTROL Link]

Change the URL in the link.

Use Edit Link to update the selector to point to the same image element. However, linking to a different image element is not supported. To link to a different image element, delete the original action from the code editor and use the [!UICONTROL Visual Experience Composer] to apply the action on the other image element.

## [!UICONTROL Insert Before]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=de){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], and [!UICONTROL Text]

Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.

Select an element on the page, then click [!UICONTROL Insert Before] and choose whether you want to insert an image, HTML, or text. The inserted element appears before the selected element.

The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.

[!UICONTROL Recommendations] supports [!UICONTROL Insert Before] the contents of DIV, SECTION, and ARTICLE tags.

**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Insert After]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=de){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], and [!UICONTROL Text]

Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.

Select an element on the page, then click [!UICONTROL Insert After] and choose whether you want to insert an image, HTML, or text. The inserted element appears after the selected element.

The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.

[!UICONTROL Recommendations] supports [!UICONTROL Insert After] the contents of DIV, SECTION, and ARTICLE tags.

**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Replace Content]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=de){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image]

Select a different image from the Content Library. The images available for swapping include the images uploaded to the Experience Cloud assets folder or uploaded in the Content Library in Target.

During initial activity creation, the URL displayed is not the URL used for delivery. Upon activity synching, that URL is updated to a production Scene7 URL.

For example, the initial URL might look like the following example:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

After activity syncing, the delivery URL might look like the following example:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations supports Replace With in DIV, SECTION, and ARTICLE tags.

**Note:** Swapping images requires an Adobe Scene7 Publishing System Account.

### [!UICONTROL HTML Offer]

Select a different offer from the [!UICONTROL Content Library].

**Note:** HTML Offers are stored on [!DNL Target] servers.

An HTML offer can be up to 256 KB.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Layout]

The following options are available:

### [!UICONTROL Rearrange]

Drag the element to another location inside the same parent element or DIV. Other elements shift location to make space for the rearranged element.

**Note**: Click-tracking does not work on rearranged items.

Currently, certain VEC actions, such as [!UICONTROL Rearrange] and [!UICONTROL Move], assume that the sibling elements of the source and destination parent elements are completely loaded. If lazy loading occurs under the parent DOM elements (source or destination), these VEC actions can cause inconsistent behavior. We are working on a more reliable approach to make VEC actions work in lazy-loaded DOM elements. As a temporary workaround, you can use [!UICONTROL Custom Code] in these scenarios to render your experiences.

### [!UICONTROL Resize]

Resize an element on your page. When you select [!UICONTROL Resize], a handle appears in the bottom-right corner of the element that lets you drag that corner to resize. Hold the Shift key to retain the same aspect ratio.

**Note:** Inline elements cannot be resized.

### [!UICONTROL Move] {#move}

Move elements on your page. Unlike the [!UICONTROL Rearrange] option, [!UICONTROL Move] does not shift other elements to make room for the element being moved. Use the arrow keys to fine tune the move. (Planned enhancement: support to ensure moved elements are not hidden behind other elements.)

In certain situations, such as when a CSS restriction requires an element to remain inside its parent element, you cannot move the element outside its parent. An element cannot be moved outside of a container that has following CSS property: `overflow: hidden`.

See [!UICONTROL Rearrange] above for more information about inconsistent behavior with the [!UICONTROL Move] and [!UICONTROL Rearrange] actions due to lazy loading of DOM elements.

### [!UICONTROL Hide]

Hide the element. The white space remains, but the content is removed.

### [!UICONTROL Remove]

Remove the element. The white space behind the image is removed and the space where the element was is collapsed.

**Note:** Items within a "classic" mbox (an mbox created within a Target Classic campaign) cannot be removed using this option.

## [!UICONTROL Expand Section]

Select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times.

## [!UICONTROL Navigate to Link]

Open the destination of the link.

## [!UICONTROL Undo]/[!UICONTROL Redo]

Undo changes you make to your activities during an editing session. You can also redo changes that have been previously undone.

## Considerations {#considerations}

* If an offer contains HTML content, see "How at.js renders offers with HTML content" in [How at.js works](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=de){target=_blank} for more information.

## Custom element support {#custom}

The VEC supports [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components) to let you create and test personalized experiences and offers on custom elements and on elements inside custom elements. This functionality is available in the VEC for all [!DNL Target] activity types.

>[!NOTE]
>
>VEC support for custom elements is supported in [at.js version](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} 2.7.0 (or later){target=_blank}. Ensure that your website has the required version deployed. If you are using the [Visual Experience Composer helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), it must also have the required version of at.js deployed. The VEC options described above are not visible and available for use with non-supported versions of at.js.
>
>VEC support for custom elements is currently not supported with the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

Most VEC actions are supported on custom events and inside custom events, with the following exceptions: 

The following actions are not available on custom elements:

* [!UICONTROL Edit]
  * [!UICONTROL Text/HTML]
  * [!UICONTROL Link]
  * [!UICONTROL Edit Source]

* [!UICONTROL Replace Content]

The following action is not available inside custom elements:

* [!UICONTROL Layout]
  * [!UICONTROL Rearrange]-->
