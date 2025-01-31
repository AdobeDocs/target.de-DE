---
keywords: Recommendations; Angebot
description: Erfahren Sie, wie Sie Adobe Recommendations als Angebot in A/B-Test-Aktivitäten (einschließlich automatischer Zuordnung und automatischen Targetings) und Erlebnis-Targeting(XT)-Aktivitäten nutzen.
title: Wie verwende ich Recommendations als Angebot in anderen Aktivitätstypen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 84cea4555448caecc079112c1a13bb63472adfbd
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 47%

---

# Recommendations als Angebot

Sie können jetzt Empfehlungen in [!UICONTROL A/B Test] (einschließlich [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]) und [!UICONTROL Experience Targeting] (XT) einbeziehen.

Diese Funktion eröffnet völlig neue Funktionen wie z. B.:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie einfach mit der Platzierung von Recommendations auf der Seite, einschließlich der Reihenfolge mehrerer Recommendations.
* Übertragen Sie Traffic mithilfe von [!UICONTROL Auto-Allocate] automatisch an das Erlebnis mit den besten Recommendations.
* Dynamische Zuweisung von Besuchern zu benutzerspezifischen Recommendations-Erlebnissen basierend auf ihrem Profil mithilfe von [!UICONTROL Auto-Target].

Erstellen Sie zunächst eine [!UICONTROL A/B Test]- oder [!UICONTROL Experience Targeting]-Aktivität mit dem [!UICONTROL Visual Experience Composer] und fügen Sie mithilfe der [!UICONTROL Recommend]-Aktion Empfehlungen zu einem Erlebnis hinzu.

## Empfehlung als Angebot in einem A/B-Test oder XT-Vorgang hinzufügen

1. Starten Sie den geleiteten Arbeitsablauf mit drei Schritten mit dem Visual Experience Composer (VEC), um eine [A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)- oder [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)-Aktivität (XT) zu erstellen.

   >[!NOTE]
   >
   >Denken Sie bei A/B-Tests daran, dass Sie die Option [Automatisierte Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) wählen können, um Traffic automatisch an die leistungsschwächsten Empfehlungen oder die Option [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) zu leiten, um Besuchern benutzerspezifische Empfehlungserlebnisse basierend auf ihrem Profil zuzuweisen.

1. Klicken Sie beim Erstellen [Erlebnisses](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) auf das Element, dem Sie eine Empfehlung als Angebot hinzufügen möchten, klicken Sie auf **[!UICONTROL Replace Content]** ( ![Symbol „Inhalt ersetzen](/help/main/assets/icons/Switch.svg) ) und wählen Sie dann **[!UICONTROL Recommendation]** aus.

   ![Empfehlung als Angebot einfügen](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Klicken Sie in der [!UICONTROL Recommendation] Leiste auf der rechten Seite auf **[!UICONTROL Select a Recommendation]** , um das Dialogfeld [!UICONTROL Select Criteria] anzuzeigen.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** oder wählen Sie ein vorhandenes Kriterium aus.

1. (Optional) Klicken Sie auf das **[!UICONTROL Filter]** ( ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um eine der folgenden Optionen auszuwählen und beliebte Recommendations-Kriterien nach Seitentyp anzuzeigen:

   * Einkaufswagenseite
   * Kategorieseite
   * „Homepage“
   * Landingpage
   * Produktseite
   * Suchergebnisseite
   * Danksagungsseite
   * Sonstige

1. Klicken Sie auf **[!UICONTROL Create Criteria]** oder wählen Sie ein vorhandenes [Kriterium](/help/main/c-recommendations/c-algorithms/algorithms.md) aus und klicken Sie dann auf **[!UICONTROL Next]** , um das Dialogfeld [!UICONTROL Select Design] anzuzeigen.

1. Klicken Sie auf **[!UICONTROL Create Design]** oder wählen Sie ein vorhandenes [Design](/help/main/c-recommendations/c-design-overview/design-overview.md) aus und klicken Sie dann auf **[!UICONTROL  Next]**.

1. Geben Sie im Dialogfeld [!UICONTROL Options] Folgendes an:

   * Wählen Sie eine [Sammlung](/help/main/c-recommendations/c-products/collections.md) aus.
   * Konfigurieren Sie nach Bedarf die Optionen [„Vorwärts-Promotion“ und „Zurück-Promotion“](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md).

1. Klicken Sie auf **[!UICONTROL Save]**.
1. Beenden Sie die Konfiguration der A/B-Test- oder XT-Aktivität mit dem dreiteiligen geleiteten Arbeitsablauf.

## Konfiguration eines Empfehlungsangebots bearbeiten

1. Klicken Sie in der [!UICONTROL Recommendation] Leiste auf das Symbol **[!UICONTROL Edit]** ( ![Bearbeiten](/help/main/assets/icons/Edit.svg) ) neben [!UICONTROL Criteria Name], [!UICONTROL Design Name] oder [!UICONTROL Collection Name], um das Element zu ändern.

## Empfehlungsangebot löschen

1. Klicken Sie auf das **[!UICONTROL Delete]**-Symbol ![Löschsymbol](/help/main/assets/icons/Delete.svg) ) oben im [!UICONTROL Recommendation].

### Anzeigen des Status des Recommendations-Angebots {#status}

Der Status Recommendations-Angebote (Algorithmus) wird für A/B-Test - und XT -Aktivitäten, die Recommendations-Angebote enthalten, unten auf der [!UICONTROL Overview] der Aktivität angezeigt:

* Ergebnisse bereit
* Ergebnisse nicht bereit
* Feed-Fehler
