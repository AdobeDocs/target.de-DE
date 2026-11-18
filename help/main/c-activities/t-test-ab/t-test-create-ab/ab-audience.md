---
keywords: Zielgruppe;Zielgruppe auswählen;Zielgruppe wählen;Auswahl
description: Definieren, welche Site-Besucher basierend auf Zielgruppenkriterien an Ihrer Adobe-[!DNL Target]-Aktivität teilnehmen.
title: Wie wähle ich eine Zielgruppe in einer [!DNL Target] A/B-Aktivität aus?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
TQID: 'https://experienceleague.adobe.com/7W8BrRxk4mKlYlgGb-GSOuc0kRMRWBvSochz9STYrTs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 2%
---
# Zielgruppenauswahl {#select-audience}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie die Zielgruppe einer A/B-Aktivität auswählen, erstellen, kombinieren, anzeigen, bearbeiten und kopieren und wie Sie den Prozentsatz der einzuschließenden Besucher festlegen.

>[!ENDSHADEBOX]

Die Zielgruppe bestimmt, welche qualifizierten Besucher in Ihre [!DNL Adobe Target]-Aktivität eingegeben werden.

Der Schritt **[!UICONTROL Targeting]** des dreiteiligen geleiteten Workflows beim [Erstellen einer Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) zeigt ein Flussdiagramm an, das Sie durch die Schritte zum Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, zum Auswählen der Traffic-Zuordnungsmethode und zum Angeben der Traffic-Zuordnung für jedes Erlebnis in der Aktivität führt.

![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

Weitere Informationen zu allen Optionen im Flussdiagramm finden Sie unter [Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

## Auswählen einer Audience für die Aktivität

Die Zielgruppe steuert, wer Ihre Aktivität sieht. Nur Besucher, die mit der Zielgruppe übereinstimmen, können sie eingeben und Sie entscheiden, welcher Anteil an diesen Besuchern teilnimmt. Standardmäßig ist die Aktivität für alle Besuchenden vorgesehen.

1. Klicken Sie auf das **[!UICONTROL Alle Besucher]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   **[!UICONTROL Alle Besucher]** ist die Standardzielgruppe. Behalten Sie für einen A/B-Test ohne spezielle Zielgruppen-Zielgruppe die Standardeinstellung bei. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

1. Klicken Sie auf **[!UICONTROL Ersetzen]-Symbol** ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ).

   ![](../../assets/audience_activity.png)

1. Navigieren **[!UICONTROL im Dialogfeld]** Zielgruppe hinzufügen“ durch die in der **[!UICONTROL Zielgruppenbibliothek“ ausgewählten Zielgruppen]** oder Sie erstellen eine Zielgruppe, die nur für die Aktivität verwendet wird.

   Die **[!UICONTROL Zielgruppenbibliothek]** enthält Zielgruppen, die zuvor definiert wurden, einschließlich einiger allgemeiner Zielgruppen, die als Teil von [!DNL Target] vorkonfiguriert sind.

   ![](../../assets/audience_activity_2.png)

1. Klicken Sie auf **[!UICONTROL Informations]**-Symbol ( ![Infosymbol](/help/main/assets/icons/InfoOutline.svg) ) neben einer Zielgruppe, um Details zu dieser Zielgruppe anzuzeigen, einschließlich ihrer Quelle und Attribute.

   ![](../../assets/audience_activity_3.png)

   Sie können auch auf **[!UICONTROL Vollständige Details anzeigen]** klicken, um weitere Details zur Zielgruppe anzuzeigen.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Zielgruppen kombinieren]**, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

   +++ Schritte zum Erstellen einer neuen Zielgruppe

   Um eine neue Zielgruppe zu erstellen, die sich noch nicht in der **[!UICONTROL Zielgruppenbibliothek]** befindet, klicken Sie auf **[!UICONTROL Zielgruppe erstellen]** definieren Sie die Zielgruppe und klicken Sie dann auf **[!UICONTROL Fertig]**.

   Während des [Zielgruppen-Workflows](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

   * **[!UICONTROL Zielgruppenbibliothek]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der **[!UICONTROL Zielgruppenbibliothek]** gespeichert und in anderen Aktivitäten wiederverwendet werden kann.
   * **[!UICONTROL Nur diese Aktivität]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht in der **[!UICONTROL Zielgruppenbibliothek]** gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

   +++

1. Sie können eine Zielgruppe bearbeiten oder kopieren, indem Sie auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/More.svg) ) neben der gewünschten Zielgruppe klicken.

1. Klicken Sie nach Auswahl der Zielgruppe auf **[!UICONTROL Zielgruppe zuweisen]**.

1. Klicken Sie **[!UICONTROL rechten Bereich auf]** Besucherprozentsatz) und geben Sie dann den Prozentsatz der qualifizierten Besucher an, die in die Aktivität aufgenommen werden sollen.

1. Wenn Sie mit Ihrer Audience zufrieden sind, klicken Sie auf **[!UICONTROL Weiter]**, um zum dritten Schritt des dreistufigen Workflows zu wechseln.

>[!NOTE]
>
>Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Liste **[!UICONTROL Zielgruppe]** öffnen und die importierten Zielgruppen älter als 10 Minuten sind.
