---
keywords: automatisierte Personalisierung; Angebote; Target; Zielgruppe; Targeting-Regeln; Targeting
description: Erfahren Sie, wie Sie mithilfe von AP-Aktivitäten (0) einzelne Angebote auf bestimmte Zielgruppen ausrichten.[!UICONTROL Automated Personalization]
title: Wie kann ich [!UICONTROL Automated Personalization] Angebote als Ziel auswählen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
solution: Target,Analytics
hide: true
hidefromtoc: true
source-git-commit: 2eb99fb0c108b600d098fc14036b678c50e689b3
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 19%

---

# Target [!UICONTROL Automated Personalization]-Angebote

In einer AP-Aktivität (0} [!DNL Automated Personalization]) können Sie Angebote auf bestimmte Zielgruppen ausrichten.[!DNL Adobe Target]

Mit dieser Funktion reduzieren Sie die Anzahl der Angebote, die ein bestimmter Besucher zu sehen bekommt. Betrachten Sie beispielsweise eine [!UICONTROL Automated Personalization] -Aktivität mit drei Angeboten. Angebot 1 verfügt über eine Targeting-Regel, die seine Exposition gegenüber Audience A begrenzt. Diese Aktivität wurde zwei Besuchern angezeigt.

| | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppenqualifikation | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario sieht Besucher 1 Angebot 1 (da dieser Besucher Teil von Zielgruppe A ist), was dem höchsten Ergebnis des Besuchers entspricht. Besucher 2 sieht jedoch Angebot 2, obwohl das höchste Ergebnis für Angebot 1 vorliegt, da Besucher 2 nicht Teil von Zielgruppe A ist. Dieses Beispiel zeigt, warum Targeting-Regeln sparsam eingesetzt werden sollten, um geschäftlichen Anforderungen gerecht zu werden. Durch Hinzufügen dieser Regeln kann die Effektivität von [!DNL Target] Personalisierungsmodellen reduziert werden.

## Einrichten von Targeting-Regeln

1. Erstellen Sie eine [Automated Personalization-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) mit den Angeboten, die Sie als Ziel auswählen möchten.
1. Nachdem Sie die Angebote für die Aktivität im Tab [!UICONTROL Visual Experience Composer] eingerichtet haben, klicken Sie auf das Symbol **[!UICONTROL Manage Content]** ( ![Symbol Inhalt verwalten](/help/main/assets/icons/Experience.svg) ).

   Das Dialogfeld [!UICONTROL Manage Content] wird angezeigt.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Offers]** .

1. Wählen Sie die gewünschten Angebote aus und wählen Sie dann die Zielgruppen aus, die Sie für das Angebot qualifizieren möchten.

   Um das Targeting für ein einzelnes Angebot einzurichten, klicken Sie neben dem gewünschten Angebot auf das Symbol &quot;Weitere Informationen&quot;( ![Mehr Infosymbol](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Target Audience]** , um das Dialogfeld [!UICONTROL Add Audiences] anzuzeigen.

   Um das Targeting für mehrere Angebote einzurichten, aktivieren Sie die Kontrollkästchen der gewünschten Angebote und klicken Sie dann auf den Link **[!UICONTROL Target Audience]** , der unten in der Liste angezeigt wird.

1. Wählen Sie im Dialogfeld [!UICONTROL Add Audiences] die gewünschten Zielgruppen für die Angebote aus und klicken Sie dann auf **[!UICONTROL Assign Audience]** , um zum Dialogfeld [!UICONTROL Manage Content] zurückzukehren.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer vorhandenen Zielgruppe können Sie mehrere Zielgruppen kombinieren, um kombinierte On-Demand-Zielgruppen zu erstellen, anstatt eine neue Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Done]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.