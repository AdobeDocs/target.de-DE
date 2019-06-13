---
description: Adobe Recommendations als Angebot in A/B-Tests und Erlebnis-Targeting-Aktivitäten.
keywords: Empfehlungen; Angebot
seo-description: Adobe Recommendations als Angebot in A/B-Tests (einschließlich Automatisierte Zuordnung und Automatisches Targeting) und Erlebnis-Targeting-Aktivitäten (XT)
seo-title: Adobe Recommendations als Angebot in A/B-Tests (einschließlich Automatisierte Zuordnung und Automatisches Targeting) und Erlebnis-Targeting-Aktivitäten (XT)
solution: Target
title: Empfehlungen als Angebot
title-outputclass: premium
topic: Premium
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Empfehlungen als Angebot

Sie können jetzt Empfehlungen in [!UICONTROL A/B-Tests] (einschließlich [!UICONTROL Automatisierte Zuordnung] und [!UICONTROL Automatisches Targeting]) und [!UICONTROL Erlebnis-Targeting] (XT) einbeziehen.

Diese Funktion eröffnet völlig neue Funktionen wie z. B.:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie einfach mit Empfehlungen auf der Seite, einschließlich der Reihenfolge mehrerer Empfehlungen.
* Traffic automatisch an die leistungsfähigsten Empfehlungserlebnisse mit [!UICONTROL Automatisierte Zuordnung] leiten.
* Dynamische Zuweisung von Besuchern zu angepassten Empfehlungserlebnissen basierend auf ihrem Profil mithilfe von [!UICONTROL automatischem Targeting].

Als erstes erstellen Sie eine [!UICONTROL A/B-Test]- oder [!UICONTROL Erlebnis-Targeting]-Aktivität mit dem [!UICONTROL Visual Experience Composer] und verwenden die Aktion [!UICONTROL Einfügen vor], [!UICONTROL Einfügen nach] oder [!UICONTROL Ersetzen mit], um einem Erlebnis Empfehlungen hinzuzufügen.

## Empfehlung als Angebot in einem A/B-Test oder XT-Vorgang hinzufügen

1. Starten Sie den geleiteten Arbeitsablauf mit drei Schritten mit dem Visual Experience Composer (VEC), um eine [A/B-Test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)- oder [Erlebnis-Targeting](/help/c-activities/t-experience-target/t-xt-create/xt-create.md)-Aktivität (XT) zu erstellen.

   >[!NOTE]
   >
   >Denken Sie bei A/B-Tests daran, dass Sie die Option [Automatisierte Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) wählen können, um Traffic automatisch an die leistungsschwächsten Empfehlungen oder die Option [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md) zu leiten, um Besuchern benutzerspezifische Empfehlungserlebnisse basierend auf ihrem Profil zuzuweisen.

1. Klicken Sie beim Erstellen eines [Erlebnisses](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) auf das Element, dem Sie eine Empfehlung hinzufügen möchten, und wählen Sie die Aktion [!UICONTROL Einfügen vor], [!UICONTROL Einfügen nach] oder [!UICONTROL Ersetzen mit] und wählen Sie dann [!UICONTROL Empfehlung] aus.

   Die folgende Abbildung zeigt die Option [!UICONTROL Einfügen nach &gt; Empfehlung].

   ![Empfehlung als Angebot einfügen](/help/c-recommendations/assets/replace-after-recommendations.png)

1. Wählen Sie aus den folgenden Optionen aus, um beliebte Empfehlungskriterien nach Seitentyp anzuzeigen:

   * Artikelseite
   * Einkaufswagenseite
   * Kategorieseite
   * „Homepage“
   * Landingpage

1. Wählen Sie die gewünschten [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md) aus und klicken Sie dann auf [!UICONTROL Weiter].
1. Wählen Sie den gewünschten [Entwurf](/help/c-recommendations/c-design-overview/design-overview.md) aus und klicken Sie dann auf [!UICONTROL Weiter].
1. Geben Sie im Dialogfeld [!UICONTROL Optionen] Folgendes an:

   * Wählen Sie eine [Sammlung](/help/c-recommendations/c-products/collections.md) aus.
   * Konfigurieren Sie nach Bedarf die Optionen [„Vorwärts-Promotion“ und „Zurück-Promotion“](/help/c-recommendations/t-create-recs-activity/adding-promotions.md).

1. Klicken Sie auf [!UICONTROL Speichern].
1. Beenden Sie die Konfiguration der A/B-Test- oder XT-Aktivität mit dem dreiteiligen geleiteten Arbeitsablauf.

## Konfiguration eines Empfehlungsangebots bearbeiten

Sie haben zwei Möglichkeiten, um die Konfiguration eines Angebots zu bearbeiten:

* Verwenden des Menüs [!UICONTROL Bearbeiten]
* Verwenden des Bedienfelds [!UICONTROL Änderungen]

### Bearbeiten eines Empfehlungsangebots über das Menü „Bearbeiten“

1. Klicken Sie auf das Angebot, das Sie bearbeiten möchten, und klicken Sie dann auf „Bearbeiten“.

   ![Menü „Bearbeiten“](/help/c-recommendations/assets/recs-offer-edit.png)

1. Wählen Sie aus den folgenden Optionen:

   * [Kriterien ändern](/help/c-recommendations/c-algorithms/algorithms.md)
   * [Entwurf ändern](/help/c-recommendations/c-design-overview/design-overview.md)
   * [Sammlung ändern](/help/c-recommendations/c-products/collections.md)
   * [Promotion ändern](/help/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Nehmen Sie die gewünschten Änderungen vor.

### Bearbeiten eines Empfehlungsangebots über das Bedienfeld „Änderungen“

1. Klicken Sie auf das [!UICONTROL Änderungen]-Symbol *&lt;/&gt;*, um den Bereich [Änderungen](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) anzuzeigen.
1. Bewegen Sie den Mauszeiger über die gewünschte Aktion und klicken Sie auf das Symbol für das [!UICONTROL Bearbeiten].

   ![Bedienfeld für Änderungen](/help/c-recommendations/assets/recs-offer-modifications.png)

1. Nehmen Sie die gewünschten Änderungen vor.

## Empfehlungsangebot löschen

Es gibt zwei Möglichkeiten, ein Empfehlungsangebot zu löschen:

* Verwenden des Menüs [!UICONTROL Bearbeiten]
* Verwenden des Bedienfelds [!UICONTROL Änderungen]

### Löschen eines Empfehlungsangebots über das Menü „Bearbeiten“

1. Klicken Sie auf das Angebot, das Sie entfernen möchten, und dann auf [!UICONTROL Layout &gt; Entfernen].

   ![Entfernen](/help/c-recommendations/assets/recs-offer-remove.png)

### Löschen eines Empfehlungsangebots über das Bedienfeld für Änderungen

1. Klicken Sie auf das [!UICONTROL Änderungen]-Symbol *&lt;/&gt;*, um den Bereich [Änderungen](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) anzuzeigen.
1. Bewegen Sie den Mauszeiger über die gewünschte Aktion und klicken Sie dann auf das [!UICONTROL Löschen]-Symbol.

   ![Symbol „Löschen“](/help/c-recommendations/assets/recs-offer-delete.png)