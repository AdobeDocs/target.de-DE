---
keywords: Recommendations; Angebot
description: Erfahren Sie, wie Sie Adobe Recommendations als Angebot in A/B-Test-Aktivitäten (einschließlich automatischer Zuordnung und automatischen Targetings) und Erlebnis-Targeting(XT)-Aktivitäten nutzen.
title: Wie verwende ich Recommendations als Angebot in anderen Aktivitätstypen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 99%

---

# Recommendations als Angebot

Sie können jetzt Empfehlungen in [!UICONTROL A/B-Tests] (einschließlich [!UICONTROL Automatisierter Zuordnung] und [!UICONTROL Automatischen Targetings]) und [!UICONTROL Erlebnis-Targeting] (XT) einbeziehen.

Diese Funktion eröffnet völlig neue Funktionen wie z. B.:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie einfach mit Empfehlungen auf der Seite, einschließlich der Reihenfolge mehrerer Empfehlungen.
* Traffic automatisch an die leistungsfähigsten Empfehlungserlebnisse mit [!UICONTROL Automatisierte Zuordnung] leiten.
* Dynamische Zuweisung von Besuchern zu angepassten Empfehlungserlebnissen basierend auf ihrem Profil mithilfe von [!UICONTROL automatischem Targeting].

Als erstes erstellen Sie eine [!UICONTROL A/B-Test]- oder [!UICONTROL Erlebnis-Targeting]-Aktivität mit dem [!UICONTROL Visual Experience Composer] und verwenden die Aktion [!UICONTROL Einfügen vor], [!UICONTROL Einfügen nach] oder [!UICONTROL Ersetzen mit], um einem Erlebnis Empfehlungen hinzuzufügen.

## Empfehlung als Angebot in einem A/B-Test oder XT-Vorgang hinzufügen

1. Starten Sie den geleiteten Arbeitsablauf mit drei Schritten mit dem Visual Experience Composer (VEC), um eine [A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)- oder [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)-Aktivität (XT) zu erstellen.

   >[!NOTE]
   >
   >Denken Sie bei A/B-Tests daran, dass Sie die Option [Automatisierte Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) wählen können, um Traffic automatisch an die leistungsschwächsten Empfehlungen oder die Option [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) zu leiten, um Besuchern benutzerspezifische Empfehlungserlebnisse basierend auf ihrem Profil zuzuweisen.

1. Klicken Sie beim Erstellen eines [Erlebnisses](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) auf das Element, dem Sie eine Empfehlung hinzufügen möchten, und wählen Sie die Aktion **[!UICONTROL Einfügen vor]**, **[!UICONTROL Einfügen nach]** oder **[!UICONTROL Ersetzen mit]** und wählen Sie dann [!UICONTROL Empfehlung] aus.

   Die folgende Abbildung zeigt die Option [!UICONTROL Einfügen nach > Empfehlung].

   ![Empfehlung als Angebot einfügen](/help/main/c-recommendations/assets/replace-after-recommendations.png)

1. Wählen Sie aus den folgenden Optionen aus, um beliebte Empfehlungskriterien nach Seitentyp anzuzeigen:

   * Einkaufswagenseite
   * Kategorieseite
   * „Homepage“
   * Landingpage
   * Produktseite
   * Suchergebnisseite
   * Danksagungsseite
   * Sonstige

1. Wählen Sie die gewünschten [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md) aus und klicken Sie dann auf [!UICONTROL Weiter].
1. Wählen Sie den gewünschten [Entwurf](/help/main/c-recommendations/c-design-overview/design-overview.md) aus und klicken Sie dann auf [!UICONTROL Weiter].
1. Geben Sie im Dialogfeld [!UICONTROL Optionen] Folgendes an:

   * Wählen Sie eine [Sammlung](/help/main/c-recommendations/c-products/collections.md) aus.
   * Konfigurieren Sie nach Bedarf die Optionen [„Vorwärts-Promotion“ und „Zurück-Promotion“](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md).

1. Klicken Sie auf [!UICONTROL Speichern].
1. Beenden Sie die Konfiguration der A/B-Test- oder XT-Aktivität mit dem dreiteiligen geleiteten Arbeitsablauf.

## Konfiguration eines Empfehlungsangebots bearbeiten

Sie haben zwei Möglichkeiten, um die Konfiguration eines Angebots zu bearbeiten:

* Verwenden des Menüs [!UICONTROL Bearbeiten]
* Verwenden des Bedienfelds [!UICONTROL Änderungen]

### Bearbeiten eines Empfehlungsangebots über das Menü „Bearbeiten“

1. Klicken Sie auf das Angebot, das Sie bearbeiten möchten, und dann auf **[!UICONTROL Bearbeiten]**.

   ![Bearbeiten eines Recommendations-Angebots](/help/main/c-recommendations/assets/recs-offer-edit.png)

1. Wählen Sie aus den folgenden Optionen:

   * [Kriterien ändern](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Entwurf ändern](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Sammlung ändern](/help/main/c-recommendations/c-products/collections.md)
   * [Promotion ändern](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Nehmen Sie die gewünschten Änderungen vor.

### Bearbeiten eines Empfehlungsangebots über das Bedienfeld „Änderungen“

1. Klicken Sie auf das Symbol [!UICONTROL Änderungen] **(`</>`)**, um den Bereich [Änderungen](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) anzuzeigen.
1. Bewegen Sie den Mauszeiger über die gewünschte Aktion und klicken Sie auf das Symbol für das **[!UICONTROL Bearbeiten]**.

   ![Bedienfeld für Änderungen](/help/main/c-recommendations/assets/recs-offer-modifications.png)

1. Nehmen Sie die gewünschten Änderungen vor.

## Empfehlungsangebot löschen

Es gibt zwei Möglichkeiten, ein Empfehlungsangebot zu löschen:

* Verwenden des Menüs [!UICONTROL Bearbeiten]
* Verwenden des Bedienfelds [!UICONTROL Änderungen]

### Löschen eines Empfehlungsangebots über das Menü „Bearbeiten“

1. Klicken Sie auf das Angebot, das Sie entfernen möchten, und dann auf **[!UICONTROL Layout > Entfernen]**.

   ![Entfernen](/help/main/c-recommendations/assets/recs-offer-remove.png)

### Löschen eines Empfehlungsangebots über das Bedienfeld für Änderungen

1. Klicken Sie auf das Symbol [!UICONTROL Änderungen] **(&lt;/>)**, um den Bereich [Änderungen](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) anzuzeigen.
1. Bewegen Sie den Mauszeiger über die gewünschte Aktion und klicken Sie dann auf das [!UICONTROL Löschen]-Symbol.

   ![Symbol „Löschen“](/help/main/c-recommendations/assets/recs-offer-delete.png)

### Status des Recommendations-Angebots anzeigen {#status}

Der Status der Recommendations-Angebote (Algorithmus) wird unten auf der [!UICONTROL Übersichtsseite] für A/B-Test- und XT-Aktivitäten angezeigt, die Recommendations-Angebote enthalten.

* Ergebnisse bereit
* Ergebnisse nicht bereit
* Feed-Fehler

![Status des Recommendations-Angebots](/help/main/c-recommendations/assets/recs-offer-status.png)

## Schulungsvideo: Recommendations als Angebot ![Übersichts-Badge](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
