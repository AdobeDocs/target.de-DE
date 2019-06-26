---
description: In einer Aktivität „Automatisierte Personalisierung“ können Sie Angebote auf spezielle Zielgruppen ausrichten.
seo-description: In einer Aktivität „Automatisierte Personalisierung“ können Sie Angebote auf spezielle Zielgruppen ausrichten.
seo-title: Targeting von Automated Personalization-Angeboten
solution: Target,Analytics
title: Targeting von Automated Personalization-Angeboten
title-outputclass: Premium
uuid: 4ee30e1a-bfda-4b20-9313-99e32dcf60ac
badge: Premium
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![PREMIUM](/help/assets/premium.png) Targeting von Angeboten mit automatisierter Personalisierung{#target-automated-personalization-offers}

In einer automatisierten Personalisierung (AP) können Sie Angebote auf bestimmte Zielgruppen ausrichten.

Mit dieser Funktion reduzieren Sie die Anzahl von Angeboten, die ein spezifischer Besucher anzeigen darf. Betrachten Sie beispielsweise eine AP-Aktivität mit drei Angeboten. Das Angebot 1 verfügt über eine Targeting-Regel, die die Exposition auf Audience A beschränkt. Diese AP-Aktivität wurde von zwei Besuchern gesehen.

|  | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppenqualifikation | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario wird Besucher 1 Angebot 1 angezeigt (da er sich als Teil von Zielgruppe A qualifiziert). Hierbei handelt es sich um die höchste Bewertung des Besuchers. Besucher 2 sieht Angebot 2 jedoch, obwohl er bei Angebot 1 die höchste Bewertung aufweist, da Besucher 2 nicht Teil von Zielgruppe A ist. Dieses Beispiel zeigt, warum Targeting-Regeln sparsam eingesetzt werden sollten, um die Geschäftsanforderungen zu erfüllen. Durch Hinzufügen dieser Regeln kann sich die Effektivität der Target-Personalisierungsmodelle reduzieren.

## Einrichten von Targeting-Regeln

1. Create an [Automated Personalization activity](/help/c-activities/t-automated-personalization/create-ap-activity.md) containing the offers you want to target.
1. After setting up the offers for the activity in the Visual Experience Composer, click **[!UICONTROL Manage Content]**.

   ![Verwalten von Inhalt](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Das Dialogfeld „Inhalt verwalten“ wird geöffnet.

1. Klicken Sie auf die Registerkarte Angebote.

   ![Angebotsseite](/help/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Wählen Sie das gewünschte Angebot aus und wählen Sie die Zielgruppen aus, die Sie für die Anzeige dieses Angebots qualifizieren möchten.

   To set up targeting for a single offer, hover over the desired offer, then click the **[!UICONTORL Targeting]** icon.

   To set up targeting for multiple offers, select the checkboxes for the desired offers, then click the **[!UICONTROL Targeting] icon that displays at the top right of the list.

1. In the [!UICONTROL Choose Audience] dialog box, select the desired audience(s) for the offer(s), then click **[!UICONTROL Done]** to return to the [!UICONTROL Manage Content] dialog box.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

>[!NOTE]
>
>Sie können bis zu 50 Positionen einrichten und bis zu 250 Angebote pro Position.
