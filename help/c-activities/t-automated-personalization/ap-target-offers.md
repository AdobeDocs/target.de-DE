---
keywords: Automatisierte Personalisierung;Angebot;Zielgruppe;Audience;Targeting-Regeln;Targeting
description: In einer Aktivität „Automatisierte Personalisierung“ können Sie Angebote auf spezielle Zielgruppen ausrichten.
title: 'Automated Personalization-Angebote '
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 93%

---


# ![PREMIUM](/help/assets/premium.png) Targeting von Angeboten mit automatisierter Personalisierung{#target-automated-personalization-offers}

In einer [!DNL Adobe Target] [!DNL Automated Personalization] (AP)-Aktivität können Sie Angebot auf bestimmte Audiencen Zielgruppe haben.

Mit dieser Funktion reduzieren Sie die Anzahl der Angebote, die ein bestimmter Besucher zu sehen bekommt. Gehen wir hierfür von einer AP-Aktivität aus, die drei Angebote aufweist. Angebot 1 verfügt über eine Targeting-Regel, durch die das Angebot auf Zielgruppe A beschränkt wird. Zwei Besucher haben diese AP-Aktivität gesehen.

|  | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppenqualifikation | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario wird Besucher 1 Angebot 1 angezeigt (da er sich als Teil von Zielgruppe A qualifiziert). Hierbei handelt es sich um die höchste Bewertung des Besuchers. Besucher 2 sieht Angebot 2 jedoch, obwohl er bei Angebot 1 die höchste Bewertung aufweist, da Besucher 2 nicht Teil von Zielgruppe A ist. Dieses Beispiel zeigt, warum Targeting-Regeln sparsam eingesetzt werden sollten, um die Geschäftsanforderungen zu erfüllen. Durch Hinzufügen dieser Regeln kann sich die Effektivität der Target-Personalisierungsmodelle reduzieren.

## Einrichten von Targeting-Regeln

1. Erstellen Sie eine [Aktivität vom Typ „Automatisierte Personalisierung“](/help/c-activities/t-automated-personalization/create-ap-activity.md), die die Angebote enthält, die Sie auswählen möchten.
1. Nachdem Sie die Angebote für die Aktivität im Visual Experience Composer eingerichtet haben, klicken Sie auf **[!UICONTROL Inhalt verwalten]**.

   ![Verwalten von Inhalt](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Das Dialogfeld „Inhalt verwalten“ wird geöffnet.

1. Klicken Sie auf die Registerkarte „Angebote“.

   ![Angebotsseite](/help/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Wählen Sie das bzw. die gewünschten Angebote aus und danach die Zielgruppen, die diese sehen sollen.

   Um die Zielgruppenauswahl für ein einzelnes Angebot einzurichten, bewegen Sie den Mauszeiger über das gewünschte Angebot und klicken Sie dann auf das **[!UICONTROL Targeting]**-Symbol.

   Um die Zielgruppenauswahl für mehrere Angebote einzurichten, wählen Sie die Kontrollkästchen für die gewünschten Angebote aus und klicken Sie dann auf das **[!UICONTROL Targeting]-Symbol, das oben rechts in der Liste angezeigt wird.

1. Wählen Sie im Dialogfeld [!UICONTROL Zielgruppe auswählen] die gewünschten Zielgruppen für die Angebote aus und klicken Sie dann auf **[!UICONTROL Fertig]**, um zum Dialogfeld [!UICONTROL Inhalt verwalten] zurückzukehren.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.
