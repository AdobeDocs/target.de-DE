---
keywords: Automated Personalization;Angebote;Zielgruppe;Zielgruppe;Zielgruppenbestimmungsregeln;Zielgruppenbestimmung
description: Erfahren Sie, wie Sie mithilfe einer [!UICONTROL Automated Personalization] (AP)-Aktivität in einzelne Angebote für bestimmte Zielgruppen  [!DNL Adobe Target].
title: Wie kann ich [!UICONTROL Automated Personalization] Angebote gezielt ansprechen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 27%

---

# Target [!UICONTROL Automated Personalization] Angebote

In einer [!DNL Adobe Target] [!DNL Automated Personalization] (AP) -Aktivität können Sie Angebote für bestimmte Zielgruppen auswählen.

Mit dieser Funktion reduzieren Sie die Anzahl der Angebote, die ein bestimmter Besucher zu sehen bekommt. Nehmen wir zum Beispiel eine [!UICONTROL Automated Personalization] Aktivität mit drei Angeboten. Angebot 1 verfügt über eine Zielgruppenbestimmungsregel, die die Exposition gegenüber Audience A begrenzt. Zwei Besucher haben diese Aktivität gesehen.

| | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppen-Qualifizierung | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario sieht Besucher 1 Angebot 1 (da dieser Besucher als Teil von Zielgruppe A qualifiziert ist), was der höchste Wert für diesen Besucher ist. Besucher 2 sieht jedoch Angebot 2, obwohl der höchste Wert für Angebot 1 gilt, da Besucher 2 nicht zu Zielgruppe A gehört. Dieses Beispiel zeigt, warum Targeting-Regeln nur sparsam eingesetzt werden sollten, um geschäftlichen Anforderungen gerecht zu werden. Das Hinzufügen dieser Regeln kann die Effektivität [!DNL Target] Personalisierungsmodelle verringern.

## Einrichten von Targeting-Regeln

1. Erstellen Sie eine [Automated Personalization](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)Aktivität mit den Angeboten, die Sie ansprechen möchten.
1. Nachdem Sie die Angebote für die Aktivität im [!UICONTROL Visual Experience Composer] eingerichtet haben, klicken Sie auf **[!UICONTROL Manage Content]**.

   ![Verwalten von Inhalt](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Das Dialogfeld [!UICONTROL Manage Content] wird angezeigt.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Offers]** .

   ![Angebotsseite](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Wählen Sie die gewünschten Angebote und dann die Zielgruppen aus, die Sie für das Anzeigen dieses Angebots qualifizieren möchten.

   Um die Zielgruppenbestimmung für ein einzelnes Angebot einzurichten, bewegen Sie den Mauszeiger über das gewünschte Angebot und klicken Sie dann auf das Symbol **[!UICONTROL Targeting]** .

   Um die Zielgruppenbestimmung auf mehrere Angebote anzuwenden, aktivieren Sie die Kontrollkästchen der gewünschten Angebote und klicken Sie auf das **[!UICONTROL Targeting]** oben rechts in der Liste.

1. Wählen Sie im Dialogfeld [!UICONTROL Choose Audience] die gewünschten Zielgruppen für die Angebote aus und klicken Sie dann auf **[!UICONTROL Done]** , um zum Dialogfeld [!UICONTROL Manage Content] zurückzukehren.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Done]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.
