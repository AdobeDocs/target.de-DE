---
keywords: Automated Personalization;Angebote;Zielgruppe;Zielgruppe;Zielgruppenbestimmungsregeln;Zielgruppenbestimmung
description: Erfahren Sie, wie Sie mithilfe von [!UICONTROL Automated Personalization] (AP)-Aktivitäten einzelne Angebote für bestimmte Zielgruppen erstellen können.
title: Wie kann ich [!UICONTROL Automated Personalization]-Angebote auswählen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
TQID: 'https://experienceleague.adobe.com/AVqyD-Von-gzuVXC09N9qHY5hEe1QLQwSavCE0mp7Ok'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 8%
---
# Target-[!UICONTROL Automated Personalization]Angebote {#target-ap-offers}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie in einer **[!UICONTROL Automated Personalization]**-Aktivität, wie Sie einzelne Angebote für bestimmte Zielgruppen unterbreiten können.

>[!ENDSHADEBOX]

In einer [!DNL Adobe Target] **[!UICONTROL Automated Personalization]** (AP)-Aktivität können Sie mithilfe von Zielgruppenbestimmungsregeln ein Angebot auf bestimmte Zielgruppen beschränken, sodass nur die Besucher, die zu diesen Zielgruppen gehören, es sehen können. Verwenden Sie Targeting-Regeln sparsam und nur dann, wenn ein Unternehmen sie benötigt, da sie die Anzahl der Angebote reduzieren, die ein Besucher sehen kann, und die Effektivität der [!DNL Target] Personalisierungsmodelle verringern können.

Nehmen wir zum Beispiel eine AP-Aktivität mit drei Angeboten. Angebot 1 verfügt über eine Zielgruppenbestimmungsregel, die die Exposition gegenüber Audience A begrenzt. Zwei Besucher sehen diese Aktivität.

| | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppen-Qualifizierung | Zielgruppe A | Zielgruppe B |
| Bewertung [!DNL Target] Personalisierungsmodells Angebot 1 | 90 | 90 |
| Punktzahl [!DNL Target] Personalisierungsmodells Angebot 2 | 50 | 70 |
| Bewertung [!DNL Target] Personalisierungsmodells Angebot 3 | 80 | 60 |

Besucher 1 qualifiziert sich als Teil von Zielgruppe A, sodass dieser Besucher Angebot 1 sieht, das die höchste Punktzahl hat. Besucher 2 ist nicht Teil von Zielgruppe A, sodass dieser Besucher Angebot 2 sieht, obwohl die höchste Punktzahl für Angebot 1 gilt.

## Einrichten von Targeting-Regeln {#set-up-targeting-rules}

<a id="task_F207ED7A41B84FD39BB6FCBFABF4B23E"></a>

Regeln zur Zielgruppen-Zielgruppenbestimmung steuern, welche Besucher die einzelnen Angebote sehen können, sodass Sie eine bestimmte Geschäftsanforderung erfüllen können, z. B. die Reservierung eines Angebots für ein Kundensegment. Jede Regel beschränkt die Auswahl des Personalisierungsmodells, sodass die Regeln nur auf die Angebote angewendet werden, die sie erfordern.

1. Erstellen oder bearbeiten Sie eine [Automated Personalization-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) die die Angebote enthält, die Sie ansprechen möchten.

   Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.

1. Nachdem Sie die Angebote für die Aktivität im **[!UICONTROL Visual Experience Composer]** eingerichtet haben, klicken Sie auf das Symbol **[!UICONTROL Inhalt verwalten]** ( ![Symbol Inhalt verwalten](/help/main/assets/icons/Experience.svg) ). Das **[!UICONTROL Inhalt verwalten]** wird angezeigt.

   ![Symbol „Inhalt verwalten“](../assets/ap-offers-1.png)

1. Klicken Sie auf die **[!UICONTROL Angebote]**.

1. Wählen Sie die gewünschten Angebote und dann die Zielgruppen aus, die sich für ihre Anzeige qualifizieren.

   * Um die Zielgruppenbestimmung für ein einzelnes Angebot einzurichten, klicken Sie auf das Symbol Mehr Informationen ( ![Mehr Info-Symbol](/help/main/assets/icons/MoreSmallList.svg) ) neben dem Angebot und dann auf **[!UICONTROL Zielgruppe]**, um das Dialogfeld **[!UICONTROL Audiences hinzufügen]** anzuzeigen.
   * Um die Zielgruppenbestimmung für mehrere Angebote einzurichten, aktivieren Sie die Kontrollkästchen der Angebote und klicken Sie dann auf den Link **[!UICONTROL Zielgruppe]**, der unten in der Liste angezeigt wird.

   ![Symbol „Inhalt verwalten“](../assets/ap-offers-2.png)

1. Wählen **[!UICONTROL Dialogfeld „Zielgruppen hinzufügen]** die Zielgruppen für die Angebote aus und klicken Sie dann auf **[!UICONTROL Zielgruppe zuweisen]**, um zum Dialogfeld **[!UICONTROL Inhalt verwalten]** zurückzukehren.

   >[!NOTE]
   >
   >Anstatt eine neue Zielgruppe zu erstellen, können Sie mehrere Zielgruppen mit vorhandenen kombinieren, um kombinierte Zielgruppen auf Anfrage zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

Die Targeting-Regeln gelten jetzt für die ausgewählten Angebote, sodass nur Besucher, die zu den zugewiesenen Audiences gehören, sie sehen können.
