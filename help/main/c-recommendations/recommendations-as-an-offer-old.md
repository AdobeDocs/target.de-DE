---
keywords: Recommendations; Angebot
description: Erfahren Sie, wie Sie Adobe Empfehlungen als Angebot in A/B-Test-Aktivitäten (einschließlich automatischer Zuordnung und automatischen Targetings) und Erlebnis-Targeting(XT)-Aktivitäten nutzen.
title: Wie verwende ich Empfehlungen als Angebot in anderen Aktivitätstypen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: f6034e83564a9a386e21e4e57279c66cc3c94537
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 42%

---

# Empfehlungen als Angebot

Sie können jetzt Empfehlungen in [!UICONTROL A/B-Test]-Aktivitäten (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) und [!UICONTROL Experience Targeting] (XT) einbeziehen.

Diese Funktion eröffnet völlig neue Funktionen wie z. B.:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie einfach mit der Platzierung von Recommendations auf der Seite, einschließlich der Reihenfolge mehrerer Recommendations.
* Übertragen Sie Traffic mithilfe der automatischen Zuordnung automatisch an das [!UICONTROL  Recommendations-Erlebnis mit ] besten Leistung.
* Dynamische Zuweisung von Besuchern zu benutzerspezifischen Recommendations-Erlebnissen basierend auf ihrem Profil mithilfe [!UICONTROL automatischen Targetings].

Erstellen Sie zunächst eine Aktivität des Typs [!UICONTROL A/B]-Test oder [!UICONTROL Erlebnis] mit dem [!UICONTROL Visual Experience Composer] und fügen Sie mithilfe der Aktion [!UICONTROL Recommend] einem Erlebnis Empfehlungen hinzu.

## Empfehlung als Angebot in einem A/B-Test oder XT-Vorgang hinzufügen

1. Starten Sie den geleiteten Workflow mit drei Schritten mit dem Visual Experience Composer (VEC), um eine [A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)- oder [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)-Aktivität (XT) zu erstellen.

   >[!NOTE]
   >
   >Denken Sie bei A/B-Tests daran, dass Sie die Option [Automatisierte Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) wählen können, um Traffic automatisch an die leistungsschwächsten Empfehlungen oder die Option [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) zu leiten, um Besuchern benutzerspezifische Empfehlungserlebnisse basierend auf ihrem Profil zuzuweisen.

1. Klicken Sie beim Erstellen [Erlebnisses](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) auf das Element, dem Sie eine Empfehlung als Angebot hinzufügen möchten, klicken Sie auf **[!UICONTROL Inhalt ersetzen]** (![Symbol „Inhalt ersetzen](/help/main/assets/icons/Switch.svg) ) und wählen Sie dann **[!UICONTROL Empfehlung]**.

   ![Empfehlung als Angebot einfügen](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Klicken Sie in [!UICONTROL  Leiste ]Empfehlung“ auf der rechten Seite auf **[!UICONTROL Empfehlung auswählen]** um das Dialogfeld [!UICONTROL Kriterien auswählen] anzuzeigen.

1. Klicken Sie **[!UICONTROL Kriterien erstellen]** oder wählen Sie ein vorhandenes Kriterium aus.

1. (Optional) Klicken Sie auf **[!UICONTROL Filter]**-Symbol ( ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um eine der folgenden Optionen zum Anzeigen beliebter Recommendations-Kriterien nach Seitentyp auszuwählen:

   * Einkaufswagenseite
   * Kategorieseite
   * „Homepage“
   * Landingpage
   * Produktseite
   * Suchergebnisseite
   * Danksagungsseite
   * Sonstige

1. Klicken Sie **[!UICONTROL Kriterium erstellen]** oder wählen Sie ein vorhandenes [Kriterium](/help/main/c-recommendations/c-algorithms/algorithms.md) aus und klicken Sie dann auf **[!UICONTROL Weiter]**, um das Dialogfeld [!UICONTROL Design auswählen] anzuzeigen.

1. Klicken Sie **[!UICONTROL Design erstellen]** oder wählen Sie ein vorhandenes [Design](/help/main/c-recommendations/c-design-overview/design-overview.md) aus und klicken Sie dann auf **[!UICONTROL Weiter]**.

1. Geben [!UICONTROL  im Dialogfeld ]Optionen“ Folgendes an:

   * Wählen Sie eine [Sammlung](/help/main/c-recommendations/c-products/collections.md) aus.
   * Konfigurieren Sie nach Bedarf die Optionen [„Vorwärts-Promotion“ und „Zurück-Promotion“](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md).

1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Beenden Sie die Konfiguration der A/B-Test- oder XT-Aktivität mit dem dreiteiligen geleiteten Workflow.

## Konfiguration eines Empfehlungsangebots bearbeiten

1. Klicken Sie in der [!UICONTROL Empfehlung]-Leiste auf das Symbol **[!UICONTROL Bearbeiten]** ( ![Bearbeiten-](/help/main/assets/icons/Edit.svg) ) neben [!UICONTROL Kriterienname], [!UICONTROL Designname] oder [!UICONTROL Sammlungsname], um das Element zu ändern.

## Empfehlungsangebot löschen

1. Klicken Sie auf **[!UICONTROL Löschen]**-Symbol ( ![Löschsymbol](/help/main/assets/icons/Delete.svg) ) oben im Bedienfeld [!UICONTROL Empfehlung].

### Anzeigen des Status des Recommendations-Angebots {#status}

Der Status Recommendations-Angebote (Algorithmus) wird für A/B-Test- und XT-Aktivitäten, die Recommendations-Angebote enthalten[!UICONTROL  unten auf der ] „Übersicht“ der Aktivität angezeigt:

* Ergebnisse bereit
* Ergebnisse nicht bereit
* Feed-Fehler
