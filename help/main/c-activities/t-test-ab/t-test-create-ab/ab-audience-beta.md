---
keywords: Zielgruppe;Zielgruppe auswählen;Zielgruppe wählen;Auswahl
description: Definieren Sie anhand von Zielgruppenkriterien, welche Site-Besucher Ihrer Adobe [!DNL Target] Aktivität beitreten.
title: Wie wähle ich eine Zielgruppe in einer [!DNL Target] A/B-Aktivität aus?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: cc823f84fb93cbe2e55d394d0f6f4fe48bbd5293
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 12%

---

# Zielgruppenauswahl

Die Zielgruppe bestimmt, welche qualifizierten Besucher in Ihre [!DNL Adobe Target] -Aktivität eingegeben werden.

Der Schritt [!UICONTROL Targeting] des dreiteiligen geführten Workflows beim Erstellen einer Aktivität ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab-beta.md) zeigt ein Flussdiagramm an, das Sie durch die Schritte zur Zuweisung einer Zielgruppe und ihres Traffic-Prozentsatzes, zur Auswahl der Traffic-Zuordnungsmethode und zur Angabe der Traffic-Zuordnung für jedes Erlebnis in der Aktivität führt.[

![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

Weitere Informationen zu allen Optionen im Flussdiagramm finden Sie unter [Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab-beta.md).

## Auswählen einer Zielgruppe für die Aktivität

1. Klicken Sie auf das Steuerelement **[!UICONTROL All Visitors]** , um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die Audience [!UICONTROL All Visitors] wird als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Wählen Sie für einen A/B-Test ohne spezifisches Zielgruppen-Targeting den Standardwert [!UICONTROL All Visitors].

   Der rechte Rahmen wird angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Besucherprozentsatz für die Aktivität zuweisen können.

1. Um die Zielgruppe zu ändern, klicken Sie im rechten Rahmen auf das Symbol **[!UICONTROL Replace]** ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ).

1. Wählen Sie im Dialogfeld [!UICONTROL Add Audience] die gewünschte Zielgruppe aus [ und klicken Sie dann auf **[!UICONTROL Assign Audience]**.](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)

   Standardeinstellung ist, dass alle Besucher Ihrer Zielgruppe angehören. Sie können die Zielgruppe jedoch anpassen. Zielgruppen werden über &quot;[!UICONTROL Audience Library]&quot;ausgewählt oder Sie können eine Zielgruppe &quot;Nur Aktivität&quot;erstellen. Die [!UICONTROL Audience Library] enthält Zielgruppen, die bereits definiert wurden, einschließlich einiger häufiger Zielgruppen, die als Teil von [!DNL Target] vordefiniert sind.

1. (Bedingt) Klicken Sie auf **Zielgruppen kombinieren** , um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

1. (Bedingt) Um eine neue Zielgruppe zu erstellen, die sich noch nicht im [!UICONTROL Audience Library] befindet, klicken Sie auf **Zielgruppe erstellen** . Im Workflow [create-audience](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

   * Erstellen einer On-Demand-Zielgruppe, die im Ordner &quot;[!UICONTROL Audience Library]&quot;gespeichert ist und in anderen Aktivitäten wiederverwendet werden kann
   * Erstellen Sie eine [aktivitätsspezifische Audience](/help/main/c-target/creating-activity-only-audience.md), die nicht im [!UICONTROL Audience Library] gespeichert ist und nur in der aktuellen Aktivität verwendet werden kann.

1. Klicken Sie im rechten Bereich auf **[!UICONTROL Visitor Percentage]** und geben Sie dann den Prozentsatz qualifizierter Besucher an, die in die Aktivität aufgenommen werden sollen.

1. Wenn Sie mit Ihrer Zielgruppe zufrieden sind, klicken Sie auf **[!UICONTROL Next]** , um zum dritten Schritt des geleiteten Arbeitsablaufs mit drei Schritten zu wechseln.

>[!NOTE]
>
>Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als 10 Minuten sind.

## Anzeigen der Informationen einer Zielgruppe

1. Klicken Sie im Dialogfeld [!UICONTROL Add Audiences] auf das Symbol **[!UICONTROL Information]** ( ![Infosymbol](/help/main/assets/icons/InfoOutline.svg) ) neben einer Zielgruppe, um Details zu dieser Zielgruppe anzuzeigen, einschließlich ihrer Quelle und Attribute.

1. Klicken Sie auf **[!UICONTROL View Full Details]** , um weitere Details zur Zielgruppe anzuzeigen. Zu den Details gehören die Attribute der Zielgruppe, die Beschreibung, der Arbeitsbereich, der Typ und die Quelle der Zielgruppe sowie eine Liste der Aktivitäten, die auf diese Zielgruppe verweisen. Sie können Informationen zu den einzelnen Zielgruppen anzeigen, einschließlich Aktivitätsname, Status, Arbeitsbereich und Zeitpunkt der letzten Änderung der Zielgruppe und durch wen.

## Bearbeiten oder Kopieren einer Zielgruppe

Sie können eine Zielgruppe bearbeiten oder kopieren, indem Sie im Dialogfeld [!UICONTROL Add Audience] auf das Symbol [!UICONTROL More Actions] ( ![Symbol für weitere Aktionen](/help/main/assets/icons/More.svg) ) neben der gewünschten Zielgruppe klicken und dann auf [!UICONTROL Edit] oder [!UICONTROL Copy] klicken.

Das Kopieren einer Zielgruppe ist hilfreich, wenn Sie für eine vorhandene Zielgruppe eine ähnliche Zielgruppe erstellen möchten. Sie können eine Kopie der Audience erstellen, Ihre Änderungen vornehmen und sie dann als neue Audience speichern.

