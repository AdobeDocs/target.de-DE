---
keywords: automatisierte Personalisierung; Angebote; Target; Zielgruppe; Targeting-Regeln; Targeting
description: Erfahren Sie, wie Sie mithilfe einer Automated Personalization-Aktivität (AP) in Adobe Target einzelne Angebote auf bestimmte Zielgruppen ausrichten können.
title: Wie kann ich [!DNL Target] Automated Personalization-Angebote?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 87%

---

# [!DNL Target] Automated Personalization-Angebote

In einer [!DNL Adobe Target] [!DNL Automated Personalization] Aktivität (AP) können Sie Angebote auf bestimmte Zielgruppen ausrichten.

Mit dieser Funktion reduzieren Sie die Anzahl der Angebote, die ein bestimmter Besucher zu sehen bekommt. Gehen wir hierfür von einer AP-Aktivität aus, die drei Angebote aufweist. Angebot 1 verfügt über eine Targeting-Regel, durch die das Angebot auf Zielgruppe A beschränkt wird. Zwei Besucher haben diese AP-Aktivität gesehen.

|  | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppenqualifikation | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario wird Besucher 1 Angebot 1 angezeigt (da er sich als Teil von Zielgruppe A qualifiziert). Hierbei handelt es sich um die höchste Bewertung des Besuchers. Besucher 2 sieht Angebot 2 jedoch, obwohl er bei Angebot 1 die höchste Bewertung aufweist, da Besucher 2 nicht Teil von Zielgruppe A ist. Dieses Beispiel zeigt, warum Targeting-Regeln sparsam eingesetzt werden sollten, um die Geschäftsanforderungen zu erfüllen. Durch Hinzufügen dieser Regeln kann sich die Effektivität der Target-Personalisierungsmodelle reduzieren.

## Einrichten von Targeting-Regeln

1. Erstellen Sie eine [Aktivität vom Typ „Automatisierte Personalisierung“](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), die die Angebote enthält, die Sie auswählen möchten.
1. Nachdem Sie die Angebote für die Aktivität im Visual Experience Composer eingerichtet haben, klicken Sie auf **[!UICONTROL Inhalt verwalten]**.

   ![Verwalten von Inhalt](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Das Dialogfeld „Inhalt verwalten“ wird geöffnet.

1. Klicken Sie auf die Registerkarte „Angebote“.

   ![Angebotsseite](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Wählen Sie das bzw. die gewünschten Angebote aus und danach die Zielgruppen, die diese sehen sollen.

   Um die Zielgruppenauswahl für ein einzelnes Angebot einzurichten, bewegen Sie den Mauszeiger über das gewünschte Angebot und klicken Sie dann auf das **[!UICONTROL Targeting]**-Symbol.

   Um die Zielgruppenauswahl für mehrere Angebote einzurichten, wählen Sie die Kontrollkästchen für die gewünschten Angebote aus und klicken Sie dann auf das **[!UICONTROL Targeting]-Symbol, das oben rechts in der Liste angezeigt wird.

1. Wählen Sie im Dialogfeld [!UICONTROL Zielgruppe auswählen] die gewünschten Zielgruppen für die Angebote aus und klicken Sie dann auf **[!UICONTROL Fertig]**, um zum Dialogfeld [!UICONTROL Inhalt verwalten] zurückzukehren.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen und bis zu 250 Angebote pro Position einrichten.
