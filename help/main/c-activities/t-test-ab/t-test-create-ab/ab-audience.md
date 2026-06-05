---
keywords: Zielgruppe;Zielgruppe auswählen;Zielgruppe wählen;Auswahl
description: Definieren, welche Site-Besucher basierend  [!DNL Target]  Zielgruppenkriterien an Ihrer Adobe-Aktivität teilnehmen.
title: Wie wähle ich eine Zielgruppe in einer A/ [!DNL Target] -Aktivität aus?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
TQID: https://experienceleague.adobe.com/7W8BrRxk4mKlYlgGb-GSOuc0kRMRWBvSochz9STYrTs
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 575
ht-degree: 10%

---

# Zielgruppenauswahl

Die Zielgruppe bestimmt, welche qualifizierten Besucher in Ihre [!DNL Adobe Target]-Aktivität eingegeben werden.

Der Schritt [!UICONTROL Targeting] des dreiteiligen geleiteten Workflows beim [Erstellen einer Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) zeigt ein Flussdiagramm an, das Sie durch die Schritte zum Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, zum Auswählen der Traffic-Zuordnungsmethode und zum Angeben der Traffic-Zuordnung für jedes Erlebnis in der Aktivität führt.

![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

Weitere Informationen zu allen Optionen im Flussdiagramm finden Sie unter [Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

## Auswählen einer Audience für die Aktivität

1. Klicken Sie auf das **[!UICONTROL Alle Besucher]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die [!UICONTROL Alle Besucher]-Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Wählen Sie für einen A/B-Test ohne spezielle Zielgruppen-Zielgruppe als Standard &quot;[!UICONTROL &#x200B; Besucher“].

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

1. Um die Audience zu ändern, klicken Sie auf **[!UICONTROL Ersetzen]-Symbol** ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.

1. Wählen Sie [!UICONTROL &#x200B; Dialogfeld &#x200B;]Zielgruppe hinzufügen[&#x200B; die gewünschte Zielgruppe aus &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Zielgruppe zuweisen]**.

   Standardeinstellung ist, dass alle Besucher Ihrer Zielgruppe angehören. Sie können die Zielgruppe jedoch anpassen. Zielgruppen werden aus der [!UICONTROL Zielgruppenbibliothek“ ausgewählt] oder Sie können eine Zielgruppe erstellen, die nur für Aktivitäten vorgesehen ist. Die [!UICONTROL Zielgruppenbibliothek] enthält Zielgruppen, die zuvor definiert wurden, einschließlich einiger allgemeiner Zielgruppen, die als Teil von [!DNL Target] vorkonfiguriert sind.

1. (Bedingt) Klicken Sie auf **Zielgruppen kombinieren**, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

1. (Bedingt) Um eine neue Zielgruppe zu erstellen, die sich noch nicht in der [!UICONTROL Zielgruppenbibliothek] befindet, klicken Sie auf **Zielgruppe erstellen** definieren Sie die Zielgruppe und klicken Sie dann auf **[!UICONTROL Fertig]**.

   Während des [Zielgruppen-Workflows](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

   * **[!UICONTROL Zielgruppenbibliothek]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der [!UICONTROL Zielgruppenbibliothek] gespeichert wird und in anderen Aktivitäten wiederverwendet werden kann.
   * **[!UICONTROL Nur diese Aktivität]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht in der [!UICONTROL Zielgruppenbibliothek] gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

1. Klicken Sie **[!UICONTROL rechten Bereich auf]** Besucherprozentsatz) und geben Sie dann den Prozentsatz der qualifizierten Besucher an, die in die Aktivität aufgenommen werden sollen.

1. Wenn Sie mit Ihrer Audience zufrieden sind, klicken Sie auf **[!UICONTROL Weiter]**, um zum dritten Schritt des dreistufigen Workflows zu wechseln.

>[!NOTE]
>
>Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Liste [!UICONTROL Zielgruppe] öffnen und die importierten Zielgruppen älter als 10 Minuten sind.

## Anzeigen der Informationen einer Zielgruppe

1. Klicken Sie [!UICONTROL &#x200B; Dialogfeld &#x200B;]Zielgruppen hinzufügen“ auf das Symbol **[!UICONTROL Information]** ( ![Info-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben einer Zielgruppe, um Details zu dieser Zielgruppe anzuzeigen, einschließlich ihrer Quelle und Attribute.

1. Klicken Sie **[!UICONTROL Vollständige Details anzeigen]**, um zusätzliche Details zur Audience anzuzeigen. Zu den Details gehören die Attribute der Zielgruppe, die Beschreibung, der Arbeitsbereich, der Typ und die Quelle der Zielgruppe sowie eine Liste der Aktivitäten, die auf diese Zielgruppe verweisen. Sie können Informationen zu jeder Zielgruppe anzeigen, einschließlich Aktivitätsname, Status, Arbeitsbereich und Zeitpunkt der letzten Änderung der Zielgruppe und von wem.

## Bearbeiten oder Kopieren einer Audience

Sie können eine Zielgruppe bearbeiten oder kopieren, indem Sie auf das Symbol [!UICONTROL Mehr Aktionen] ( ![Symbol Mehr Aktionen](/help/main/assets/icons/More.svg) ) neben der gewünschten Zielgruppe im Dialogfeld [!UICONTROL Zielgruppe hinzufügen] klicken, und dann auf [!UICONTROL Bearbeiten] oder [!UICONTROL Kopieren].

Das Kopieren einer Zielgruppe ist hilfreich, wenn Sie für eine vorhandene Zielgruppe eine ähnliche Zielgruppe erstellen möchten. Sie können eine Kopie der Zielgruppe erstellen, Bearbeitungen vornehmen und sie dann als neue Zielgruppe speichern.
