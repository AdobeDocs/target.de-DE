---
keywords: Visual Experience Composer;VEC;WYSIWYG
description: Machen Sie sich mit den Änderungen vertraut, die in Visual Experience Composer (VEC) in Adobe Target 25.2.1 (17. Februar 2025) eingeführt wurden.
title: Welche Änderungen werden mit dem neuen Visual Experience Composer (VEC) eingeführt?
feature: Visual Experience Composer (VEC)
exl-id: 4c7a5657-93d9-4355-9d2b-c992b36bcb50
source-git-commit: 3dab3c070eecb415136d880ab1a4326dfe8856d8
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# [!UICONTROL Visual Experience Composer] Kalender

Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der vorherigen und der aktualisierten Version des VEC erläutert.

>[!IMPORTANT]
>
>Für die aktualisierte [!UICONTROL Visual Editing Composer] ist die [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper]-Erweiterung erforderlich](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) die im [!DNL Chrome Web Store] verfügbar ist.

Der VEC wird angezeigt, wenn Sie eine vorhandene Aktivität erstellen oder bearbeiten.

![Visual Experience Composer (VEC)](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Wichtige Änderungen am VEC

In den folgenden Abschnitten werden die wichtigsten Änderungen im aktualisierten VEC im Vergleich zur vorherigen Version erläutert.

### [!UICONTROL Experiences]

Wie in der vorherigen Version bleibt die [!UICONTROL Experiences] Leiste auf der linken Seite des VEC. Die [!UICONTROL Experiences] kann nicht reduziert werden.

![Leiste „Erlebnisse“](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

Sie können Erlebnisse mithilfe der [!UICONTROL Experiences] Leiste erstellen, umbenennen oder entfernen. Klicken Sie auf das **[!UICONTROL Add]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ), um ein neues Erlebnis hinzuzufügen. Klicken Sie auf das [!UICONTROL More Actions]-Symbol ![Mehr Aktionen-Symbol](/help/main/assets/icons/MoreSmall.svg) ), um ein Erlebnis zu duplizieren, zu löschen oder umzuleiten.

### [!UICONTROL Components] Leiste (neu)

Sie können Ihrer Web-Seite eine Reihe von Komponenten hinzufügen und diese nach Bedarf bearbeiten, indem Sie die neue [!UICONTROL Components] Leiste verwenden.

![Komponentenleiste](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

Um eine neue Komponente hinzuzufügen, ziehen Sie die Komponente aus der [!UICONTROL Components] Leiste, die Sie über ein vorhandenes Seitenelement in die [!UICONTROL Design] einfügen möchten. Wählen Sie dann aus, dass die Komponente vor oder nach dem ausgewählten Element eingefügt werden soll.

Im Vergleich zur vorherigen VEC-Version können Sie ein ausgewähltes Element nicht durch eine Komponente ersetzen.

### [!UICONTROL Modifications]

Um die [!UICONTROL Modifications] Leiste zu öffnen, klicken Sie auf das Symbol [!UICONTROL Show Modifications] ( ![Leiste „Änderungen anzeigen](/help/main/assets/icons/History.svg) ) in der [!UICONTROL Components] Leiste. Die [!UICONTROL Modifications] Leiste hat die Position von der rechten zur linken Seite der Arbeitsfläche für die Bearbeitung geändert.

![Leiste „Änderungen](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

In der [!UICONTROL Modifications] Leiste werden alle Änderungen angezeigt, die an Ihrer Seite in Visual Experience Composer vorgenommen wurden, und Sie können zusätzliche Änderungen vornehmen (z. B. CSS-Auswahl, Mbox und benutzerdefinierter Code).

Klicken Sie auf das [!UICONTROL More Options] (Symbol ![Mehr Aktionen](/help/main/assets/icons/MoreSmall.svg) ), um eine Änderung hinzuzufügen, alle Änderungen zu löschen oder alle ungültigen Änderungen zu löschen. Klicken Sie auf [!UICONTROL Select] , um Massenvorgänge durchzuführen: [!UICONTROL Apply to All Pages] oder [!UICONTROL Delete].

Um die [!UICONTROL Modifications] Leiste erneut anzuzeigen, klicken Sie auf das Symbol [!UICONTROL Hide Modifications] ( ![Leiste „Änderungen anzeigen](/help/main/assets/icons/History.svg) ) in der [!UICONTROL Modifications] Leiste.

### [!UICONTROL Properties] Leiste (neu)

Mit der [!UICONTROL Properties] Leiste können Sie die Eigenschaften ausgewählter Seitenelemente ändern, unabhängig davon, ob es sich um HTML-Elemente oder [!DNL Target] Objekte wie Empfehlungen oder Angebote handelt.

![Eigenschaftenleiste](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

Klicken Sie auf die Symbole oben in der Leiste, um HTML-Code zu bearbeiten oder Elemente zu löschen, zu duplizieren oder auszublenden. Änderungen werden in der [!UICONTROL Modifications] Leiste angezeigt.

![Eigenschaftensymbole](/help/main/c-experiences/c-visual-experience-composer/assets/options-icons.png)

Die [!UICONTROL Properties] ist in der rechten Leiste ausblendbar. Klicken Sie auf das [!UICONTROL Show/Hide Properties]-Symbol ![Eigenschaftensymbol](/help/main/assets/icons/Propertie.svg) ) rechts neben der Leiste, um die [!UICONTROL Properties] Leiste zu reduzieren oder anzuzeigen.

### Aktivitätseinstellungen/-konfiguration

Klicken Sie auf das [!UICONTROL Configure] ( ![Symbol konfigurieren](/help/main/assets/icons/Setting.svg) ), das über der Arbeitsfläche „Design“ angezeigt wird, um das Menü mit den Eigenschaften der Aktivität anzuzeigen.

![Konfigurationsoptionen für Aktivitäten](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

Über die verschiedenen Optionen können Sie Eigenschaften zuweisen, Seitenbereitstellungsregeln bearbeiten, Website-Voreinstellungen festlegen, zusätzliche Seiten hinzufügen und mehrseitige oder mehrere Zielgruppenaktivitäten aktivieren oder deaktivieren. [!UICONTROL Properties] zuweisen ist eine [[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) Funktion.

Position und Funktionalität sind mit der vorherigen VEC-Benutzeroberfläche vergleichbar.

### [!UICONTROL Design]-/[!UICONTROL Browse]

Verwenden Sie die [!UICONTROL Design]/[!UICONTROL Browse] Umschalter, die oben in der [!UICONTROL Properties] angezeigt werden, um zwischen Design- und Durchsuchen-Modus zu wechseln.

![Umschalter zum Entwerfen und Durchsuchen](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

Verwenden Sie den [!UICONTROL Browse] , um auf Ihrer Site zu navigieren und die Ansicht oder Seite auszuwählen, die Sie aktualisieren möchten. Wechseln Sie zurück in den [!UICONTROL Design], um Ihre Änderungen hinzuzufügen oder zu bearbeiten.

### [!UICONTROL Undo]/[!UICONTROL Redo]

Sie können die vorgenommenen Änderungen rückgängig machen, indem Sie auf das [!UICONTROL Undo] klicken ( ![Rückgängig-Symbol](/help/main/assets/icons/Undo.svg) ).

![Symbol „Rückgängig“ in VEC](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

Um eine Aktion wiederherzustellen, erweitern Sie die Rückgängig/[!UICONTROL Redo]-Schaltflächengruppe und wählen Sie [!UICONTROL Redo] aus.

### [!UICONTROL Design]

Auf der [!UICONTROL Design] Arbeitsfläche können Sie Viewports auswählen, einschließlich „An Bildschirm anpassen“, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape] und [!UICONTROL Mobile Portrait].

![Viewport-Optionen](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

Mit dem aktualisierten VEC können Sie auch ein- oder auszoomen, indem Sie auf das entsprechende Symbol klicken (![Zoom-Symbol](/help/main/assets/icons/ZoomIn.svg) oder ![Zoom-Symbol](/help/main/assets/icons/ZoomOut.svg) ).

## Visuelle Abbildung mit Änderungen der Benutzeroberfläche

Die folgende Abbildung zeigt die Änderungen an der Benutzeroberfläche auf hoher Ebene, die am aktualisierten VEC vorgenommen wurden. Oben in der Abbildung sehen Sie die aktualisierte VEC-Benutzeroberfläche und unten die vorherige Benutzeroberfläche. Die Pfeile zeigen an, wohin sich verschiedene Elemente bewegt haben.

(Klicken Sie auf das Bild, um es auf die gesamte Breite des Browsers zu erweitern.)

![VEC-Vergleich - neu in der vorherigen Benutzeroberfläche](/help/main/c-experiences/c-visual-experience-composer/assets/vec-comparison.png){width="600" zoomable="yes"}

## Weitere Informationen zur aktualisierten Benutzeroberfläche

* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für [!UICONTROL Activities], [!UICONTROL Recommendations] und den [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für die [!UICONTROL Offers Library].

* [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md): Bietet einen kurzen Überblick, der Ihnen hilft, sich mit [!DNL Target] vertraut zu machen, und enthält Links für detailliertere Informationen und schrittweise Anweisungen.

* [[!UICONTROL Visual Experience Composer] Änderungen](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der alten und der aktualisierten Version des VEC erläutert.

* [[!UICONTROL Visual Experience Composer] Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): In diesem Artikel werden die aktualisierte VEC-Benutzeroberfläche und ihre Optionen erläutert.

* [[!DNL Target] Häufig gestellte Fragen zur Aktualisierung der Benutzeroberfläche](/help/main/c-intro/updated-ui-faq.md): In dieser häufig gestellten Frage werden häufige Fragen zur neuen [!DNL Target]-Benutzeroberfläche und -[!UICONTROL Visual Experience Composer] (VEC) behandelt, einschließlich Navigationsänderungen, Funktionsspeicherorte und der Einstellung des Umschalters für die temporäre Benutzeroberfläche. Unabhängig davon, ob Sie Marketing-Experte, Entwickler oder Administrator sind, hilft Ihnen diese häufig gestellte Frage dabei, den Übergang reibungslos zu gestalten und die aktualisierte Benutzeroberfläche optimal zu nutzen.