---
keywords: Automated Personalization;Angebote;Zielgruppe;Zielgruppe;Zielgruppenbestimmungsregeln;Zielgruppenbestimmung
description: Erfahren Sie, wie Sie mithilfe von [!UICONTROL Automated Personalization] (AP)-Aktivitäten einzelne Angebote für bestimmte Zielgruppen erstellen können.
title: Wie kann ich [!UICONTROL Automated Personalization]-Angebote auswählen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
TQID: https://experienceleague.adobe.com/AVqyD-Von-gzuVXC09N9qHY5hEe1QLQwSavCE0mp7Ok
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 18%

---

# Target-[!UICONTROL Automated Personalization]Angebote

In einer [!DNL Adobe Target] [!DNL Automated Personalization] (AP) -Aktivität können Sie Angebote für bestimmte Zielgruppen auswählen.

Mit dieser Funktion reduzieren Sie die Anzahl der Angebote, die ein bestimmter Besucher zu sehen bekommt. Nehmen wir als Beispiel eine [!UICONTROL Automated Personalization]-Aktivität mit drei Angeboten. Angebot 1 verfügt über eine Zielgruppenbestimmungsregel, die die Exposition gegenüber Audience A begrenzt. Zwei Besucher haben diese Aktivität gesehen.

| | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppen-Qualifizierung | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario sieht Besucher 1 Angebot 1 (da dieser Besucher als Teil von Zielgruppe A qualifiziert ist), was der höchste Wert für diesen Besucher ist. Besucher 2 sieht jedoch Angebot 2, obwohl der höchste Wert für Angebot 1 gilt, da Besucher 2 nicht zu Zielgruppe A gehört. Dieses Beispiel zeigt, warum Targeting-Regeln nur sparsam eingesetzt werden sollten, um geschäftlichen Anforderungen gerecht zu werden. Das Hinzufügen dieser Regeln kann die Effektivität [!DNL Target] Personalisierungsmodelle verringern.

## Einrichten von Targeting-Regeln

1. Erstellen oder bearbeiten Sie eine [Automated Personalization](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)Aktivität mit den Angeboten, die Sie ansprechen möchten.
1. Nachdem Sie die Angebote für die Aktivität im [!UICONTROL Visual Experience Composer] eingerichtet haben, klicken Sie auf das Symbol **[!UICONTROL Inhalt verwalten]** ( ![Symbol Inhalt verwalten](/help/main/assets/icons/Experience.svg) ).

   Das [!UICONTROL Inhalt verwalten] wird angezeigt.

1. Klicken Sie auf die **[!UICONTROL Angebote]**.

1. Wählen Sie die gewünschten Angebote und dann die Zielgruppen aus, die Sie für das Anzeigen dieses Angebots qualifizieren möchten.

   Um die Zielgruppenbestimmung für ein einzelnes Angebot einzurichten, klicken Sie auf das Symbol Mehr Informationen ( ![Mehr Info-Symbol](/help/main/assets/icons/MoreSmallList.svg) ) neben dem gewünschten Angebot und dann auf **[!UICONTROL Zielgruppe]**, um das Dialogfeld [!UICONTROL Audiences hinzufügen] anzuzeigen.

   Um das Targeting für mehrere Angebote einzurichten, aktivieren Sie die Kontrollkästchen der gewünschten Angebote und klicken Sie dann auf den Link **[!UICONTROL Zielgruppe]**, der unten in der Liste angezeigt wird.

1. Wählen [!UICONTROL &#x200B; Dialogfeld „Zielgruppen hinzufügen] die gewünschten Zielgruppen für die Angebote aus und klicken Sie dann auf **[!UICONTROL Zielgruppe zuweisen]**, um zum Dialogfeld [!UICONTROL Inhalt verwalten] zurückzukehren.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie auch mehrere Zielgruppen kombinieren, um nach Bedarf kombinierte Zielgruppen zu erstellen, anstatt eine neue Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.
