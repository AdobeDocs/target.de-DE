---
keywords: automatisierte Personalisierung; Angebote; Target; Zielgruppe; Targeting-Regeln; Targeting
description: Erfahren Sie, wie Sie mithilfe eines [!UICONTROL Automated Personalization] Aktivität (AP) in [!DNL Adobe Target].
title: Wie kann ich Target verwenden? [!UICONTROL Automated Personalization] Angebote?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: eacee6f353aa685d17b781ac82d3f79574384dfe
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 29%

---

# Target [!UICONTROL Automated Personalization] Angebote

In einer [!DNL Adobe Target] [!DNL Automated Personalization] Aktivität (AP) können Sie Angebote auf bestimmte Zielgruppen ausrichten.

Mit dieser Funktion reduzieren Sie die Anzahl der Angebote, die ein bestimmter Besucher zu sehen bekommt. Betrachten Sie beispielsweise eine [!UICONTROL Automated Personalization] -Aktivität, die drei Angebote enthält. Angebot 1 verfügt über eine Targeting-Regel, die seine Exposition gegenüber Audience A begrenzt. Diese Aktivität wurde zwei Besuchern angezeigt.

| | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppenqualifikation | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario sieht Besucher 1 Angebot 1 (da dieser Besucher Teil von Zielgruppe A ist), was dem höchsten Ergebnis des Besuchers entspricht. Besucher 2 sieht jedoch Angebot 2, obwohl das höchste Ergebnis für Angebot 1 vorliegt, da Besucher 2 nicht Teil von Zielgruppe A ist. Dieses Beispiel zeigt, warum Targeting-Regeln sparsam eingesetzt werden sollten, um geschäftlichen Anforderungen gerecht zu werden. Das Hinzufügen dieser Regeln kann die Effektivität von [!DNL Target] Personalisierungsmodelle.

## Einrichten von Targeting-Regeln

1. Erstellen Sie eine [Automated Personalization-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) enthält die Angebote, die Sie ansprechen möchten.
1. Nach der Einrichtung der Angebote für die Aktivität im [!UICONTROL Visual Experience Composer]klicken **[!UICONTROL Inhalt verwalten]**.

   ![Verwalten von Inhalt](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Die [!UICONTROL Inhalt verwalten] angezeigt.

1. Klicken Sie auf **[!UICONTROL Angebote]** Registerkarte.

   ![Angebotsseite](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Wählen Sie die gewünschten Angebote aus und wählen Sie dann die Zielgruppen aus, die Sie für das Angebot qualifizieren möchten.

   Um die Zielgruppenauswahl für ein einzelnes Angebot einzurichten, bewegen Sie den Mauszeiger über das gewünschte Angebot und klicken Sie dann auf das **[!UICONTROL Targeting]**-Symbol.

   Um das Targeting für mehrere Angebote einzurichten, aktivieren Sie die Kontrollkästchen der gewünschten Angebote und klicken Sie auf die Schaltfläche **[!UICONTROL Targeting]** -Symbol, das oben rechts in der Liste angezeigt wird.

1. Im [!UICONTROL Zielgruppe auswählen] wählen Sie die gewünschten Zielgruppen für die Angebote aus und klicken Sie auf **[!UICONTROL Fertig]** , um zu [!UICONTROL Inhalt verwalten] Dialogfeld.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.
