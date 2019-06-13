---
description: In einer Aktivität „Automatisierte Personalisierung“ können Sie Angebote auf spezielle Zielgruppen ausrichten.
seo-description: In einer Aktivität „Automatisierte Personalisierung“ können Sie Angebote auf spezielle Zielgruppen ausrichten.
seo-title: Targeting von Automated Personalization-Angeboten
solution: Target,Analytics
title: Targeting von Automated Personalization-Angeboten
title-outputclass: Premium
uuid: 4ee30e1a-bfda-4b20-9313-99e32dcf60ac
badge: Premium
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Targeting von Angeboten mit automatisierter Personalisierung{#target-automated-personalization-offers}

In einer Aktivität „Automatisierte Personalisierung“ können Sie Angebote auf spezielle Zielgruppen ausrichten.

Mit dieser Funktion reduzieren Sie die Anzahl von Angeboten, die ein spezifischer Besucher anzeigen darf. Gehen wir hierfür von einer AP-Automated Personalization-Aktivität aus, die drei Angebote aufweist. Angebot 1 verfügt über eine Targeting-Regel, die es nur Zielgruppe A verfügbar macht. Bei zwei Besuchern ist diese AP-Aktivität aufgetreten.

|  | Besucher 1 | Besucher 2 |
|--- |--- |--- |
| Zielgruppenqualifikation | Zielgruppe A | Zielgruppe B |
| Bewertung des Target-Personalisierungsmodells für Angebot 1 | 90 | 90 |
| Bewertung des Target-Personalisierungsmodells für Angebot 2 | 50 | 70 |
| Bewertung des Target-Personalisierungsmodells für Angebot 3 | 80 | 60 |

In diesem Szenario wird Besucher 1 Angebot 1 angezeigt (da er sich als Teil von Zielgruppe A qualifiziert). Hierbei handelt es sich um die höchste Bewertung des Besuchers. Besucher 2 sieht Angebot 2 jedoch, obwohl er bei Angebot 1 die höchste Bewertung aufweist, da Besucher 2 nicht Teil von Zielgruppe A ist. Dieses Beispiel zeigt, warum Targeting-Regeln sparsam eingesetzt werden sollten, um die Geschäftsanforderungen zu erfüllen. Durch Hinzufügen dieser Regeln kann sich die Effektivität der Target-Personalisierungsmodelle reduzieren.

## Einrichten von Targeting-Regeln

1. Erstellen Sie die Aktivität „Automatisierte Personalisierung“, die die Angebote enthält, die Sie auswählen möchten.
1. Nachdem Sie die Angebote für die Aktivität im Visual Experience Composer eingerichtet haben, klicken Sie auf **[!UICONTROL Inhalt]**.

   Das Dialogfeld „Inhalt verwalten“ wird geöffnet.

   ![](assets/ap_content.png)

   >[!NOTE]
   >
   >Sie können bis zu 50 Positionen einrichten und bis zu 250 Angebote pro Position.

1. Wählen Sie in der Spalte **[!UICONTROL Inhalt]** das Angebot aus, klicken Sie auf **[!UICONTROL Targeting]** und wählen Sie die Zielgruppen aus, die das Angebot sehen sollen.

   Dieses Angebot wird nur den ausgewählten Zielgruppen präsentiert.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie auf **[!UICONTROL Fertig]**.
