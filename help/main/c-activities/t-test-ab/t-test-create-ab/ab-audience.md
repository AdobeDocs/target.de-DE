---
keywords: Zielgruppe;Zielgruppe auswählen;Zielgruppe wählen;Auswahl
description: Definieren, welche Site-Besucher basierend  [!DNL Target]  Zielgruppenkriterien an Ihrer Adobe-Aktivität teilnehmen.
title: Wie wähle ich eine Zielgruppe in einer A/ [!DNL Target] -Aktivität aus?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
source-git-commit: f6845756f9d4220214b0d9131cd5f27db2ae94a9
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 8%

---

# Zielgruppenauswahl

Die Zielgruppe bestimmt, welche qualifizierten Besucher in Ihre [!DNL Adobe Target]-Aktivität eingegeben werden.

Der [!UICONTROL Targeting] Schritt des dreiteiligen geleiteten Workflows beim [Erstellen einer Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) zeigt ein Flussdiagramm an, das Sie durch die Schritte zum Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, zum Auswählen der Traffic-Zuordnungsmethode und zum Angeben der Traffic-Zuordnung für jedes Erlebnis in der Aktivität führt.

![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

Weitere Informationen zu allen Optionen im Flussdiagramm finden Sie unter [Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

## Auswählen einer Audience für die Aktivität

1. Klicken Sie auf das **[!UICONTROL All Visitors]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die [!UICONTROL All Visitors] Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Wählen Sie für einen A/B-Test ohne spezielle Zielgruppen-Zielgruppe den Standardwert [!UICONTROL All Visitors].

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

1. Um die Audience zu ändern, klicken Sie auf das **[!UICONTROL Replace]-** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.

1. Wählen Sie im Dialogfeld [!UICONTROL Add Audience] die [&#x200B; Audience aus &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Assign Audience]**.

   Standardeinstellung ist, dass alle Besucher Ihrer Zielgruppe angehören. Sie können die Zielgruppe jedoch anpassen. Audiences werden aus dem [!UICONTROL Audience Library] ausgewählt oder Sie können eine Zielgruppe nur für Aktivitäten erstellen. Die [!UICONTROL Audience Library] enthält Zielgruppen, die zuvor definiert wurden, einschließlich einiger allgemeiner Zielgruppen, die als Teil der [!DNL Target] vorkonfiguriert sind.

1. (Bedingt) Klicken Sie auf **Zielgruppen kombinieren**, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

1. (Bedingt) Um eine neue Zielgruppe zu erstellen, die sich noch nicht in der [!UICONTROL Audience Library] befindet, klicken Sie auf **Zielgruppe erstellen** definieren Sie die Zielgruppe und klicken Sie dann auf **[!UICONTROL Done]**.

   Während des [Zielgruppen-Workflows](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

   * **[!UICONTROL Audience Library]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der [!UICONTROL Audience Library] gespeichert wird und in anderen Aktivitäten wiederverwendet werden kann.
   * **[!UICONTROL This activity only]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht im [!UICONTROL Audience Library] gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

1. Klicken Sie im rechten Bereich auf **[!UICONTROL Visitor Percentage]** und geben Sie dann den Prozentsatz der qualifizierten Besucher an, die in die Aktivität aufgenommen werden sollen.

1. Wenn Sie mit Ihrer Zielgruppe zufrieden sind, klicken Sie auf **[!UICONTROL Next]** , um zum dritten Schritt des dreistufigen Workflows zu wechseln.

>[!NOTE]
>
>Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die [!UICONTROL Audience] öffnen, und die importierten Zielgruppen sind älter als 10 Minuten.

## Anzeigen der Informationen einer Zielgruppe

1. Klicken Sie im Dialogfeld [!UICONTROL Add Audiences] auf das **[!UICONTROL Information]** ( ![Info-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben einer Zielgruppe, um Details zu dieser Zielgruppe, einschließlich ihrer Quelle und Attribute, anzuzeigen.

1. Klicken Sie auf **[!UICONTROL View Full Details]** , um zusätzliche Details zur Audience anzuzeigen. Zu den Details gehören die Attribute der Zielgruppe, die Beschreibung, der Arbeitsbereich, der Typ und die Quelle der Zielgruppe sowie eine Liste der Aktivitäten, die auf diese Zielgruppe verweisen. Sie können Informationen zu jeder Zielgruppe anzeigen, einschließlich Aktivitätsname, Status, Arbeitsbereich und Zeitpunkt der letzten Änderung der Zielgruppe und von wem.

## Bearbeiten oder Kopieren einer Audience

Um eine Audience zu bearbeiten oder zu kopieren, klicken Sie im [!UICONTROL More Actions]-Dialogfeld neben der gewünschten Audience auf das ![-Symbol &#x200B;](/help/main/assets/icons/More.svg)Mehr Aktionen-[!UICONTROL Add Audience] ) und klicken Sie dann auf [!UICONTROL Edit] oder [!UICONTROL Copy].

Das Kopieren einer Zielgruppe ist hilfreich, wenn Sie für eine vorhandene Zielgruppe eine ähnliche Zielgruppe erstellen möchten. Sie können eine Kopie der Audience erstellen, Ihre Änderungen vornehmen und sie dann als neue Audience speichern.
