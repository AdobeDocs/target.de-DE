---
keywords: Visual Experience Composer-Optionen;Experience Composer-Optionen;Erlebnisoptionen;Angebotsentscheidung;offer decisioning;Ajo;Journey Optimizer
description: Erfahren Sie, wie Sie einer Aktivität eine in [!DNL Adobe Journey Optimizer] erstellte Angebotsentscheidung hinzufügen.
title: Wie verwende ich Angebotsentscheidungen?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# Verwenden von Angebotsentscheidungen 

Verwenden Sie [!DNL Adobe Target] mit [!DNL Adobe Journey Optimizer] Angebotsentscheidungen, um das nächste beste Angebot für Ihre Besucher im Web und auf Mobilgeräten zu ermitteln und bereitzustellen.

Fügen Sie Angebotsentscheidungen, die in [!DNL Adobe Journey Optimizer] erstellt wurden, zu [!DNL Target] -Aktivitäten hinzu (manuell [!UICONTROL A/B Test] oder [!UICONTROL Experience Targeting]), indem Sie entweder den VEC (4) oder den 5 verwenden, um Ihre Besucher auf Ihren eingehenden Kanälen mit [!DNL Target] zu testen und personalisierte Angebote zu unterbreiten.[!UICONTROL Visual Experience Composer][!UICONTROL Form-Based Composer]

Weitere Informationen zu [!DNL Adobe Journey Optimizer] und Angebotsentscheidungen finden Sie in der Dokumentation zu *[!DNL Journey Optimizer]* in den folgenden Themen:

* [Erste Schritte mit Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)

* [Über die Entscheidungsverwaltung](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html)

## Voraussetzungen 

Um Angebotsentscheidungen in [!DNL Target] zu verwenden, benötigen Sie Folgendes:

* [!DNL Adobe Target Standard] oder [!DNL Adobe Target Premium], die mit dem [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} implementiert wurden.

  Die Funktion ist nicht verfügbar, wenn [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs implementiert wird.

* [!DNL Adobe Journey Optimizer Ultimate] (AJO + Offer decisioning) oder [!DNL Adobe Experience Platform] und das Add-on für den Anwendungsdienst [!UICONTROL Offer Decisioning].

## Anwendungsbeispiele

Die folgenden Beispiele zeigen Anwendungsfälle, wie Sie die Integration [!DNL Target]/[!DNL Adobe Journey Optimizer] verwenden können, um Angebotsentscheidungen in [!DNL Target] -Aktivitäten zu verwenden:

### Sportvermarktung

Als Marketer für eine Sportliga möchten Sie Inhalte auf Ihrer Homepage personalisieren (sowohl auf der Desktop- als auch auf der mobilen Website). Sie möchten Inhalte basierend auf mehreren Dimensionen personalisieren und ein Angebot für Shop-bezogene Franchise-Waren präsentieren. Sie interessieren sich für:

* Das Lieblingsteam des Besuchers
* Jüngste Athlet-/Player-Aktivität (z. B. Teambewegungen, Vertragsaktualisierungen oder Verletzungen)

Sie möchten beispielsweise für jede der folgenden Regionen ein personalisiertes Erlebnis bereitstellen: Dortmund, Frankfurt und Bochum sowie für Benutzer, die implizite und explizite Fans dieser Teams sind. Als Metriken möchten Sie sich Besuche und Klicks zur Merchandising-Site ansehen.

Sie möchten eine [!UICONTROL A/B Test] -Aktivität (50/50-Aufteilung) zwischen dem Standarderlebnis und dem personalisierten Erlebnis (einschließlich einer Angebotsentscheidung mit Angeboten für jede Region und jedes Team) erstellen. Sie möchten diese Aktivität verwenden, um die Konversion und Steigerung für das personalisierte Erlebnis bzw. die Kontrolle zu ermitteln.

### Spiel-Streaming-Plattformen

Als Marketing-Experte für eine Gaming-Organisation möchten Sie ein personalisiertes Angebot für eine Spiel-Streaming-Plattform für Desktop- und Mobilbenutzer aus verschiedenen Ländern bereitstellen: Deutschland, Frankreich, Mexiko und Brasilien. Wenn ein Besucher von einer dieser Regionen aus auf die Desktop- oder mobile Website zugreift, möchten Sie ein Angebot für Spiel-Streaming in der Landessprache und mit einem entsprechenden Preis für die Landeswährung bereitstellen.

In [!DNL Adobe Journey Optimizer] können Sie ein personalisiertes Hero-Angebot für die Startseite für jede Zielregion erstellen sowie ein Fallback-Angebot mit einem standardmäßigen Startheld für die Startseite. Anschließend können Sie eine Angebotsentscheidung erstellen, in der diese Angebote und ihre Eignungsregeln enthalten sind. Anschließend können Sie in [!DNL Target] eine XT-Aktivität (1}) erstellen und diese Angebotsentscheidung in Ihre Desktop- oder mobile Website einfügen, um Besuchern das personalisierte Erlebnis bereitzustellen.[!DNL Experience Targeting]

## Erstellen Sie ein Erlebnis, das eine Angebotsentscheidung verwendet:

1. Klicken Sie beim Bearbeiten oder Erstellen einer manuellen [!UICONTROL A/B Test] - oder [!UICONTROL Experience Targeting] -Aktivität (XT) im [!UICONTROL Visual Experience Composer] (VEC) auf ein Seitenelement, um das [Optionsmenü](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) anzuzeigen.

   ![Menü &quot;Optionen&quot;im Visual Experience Composer](assets/options-menu1.png)

   >[!NOTE]
   >
   >Sie können auch ein Erlebnis erstellen, das [!UICONTROL Offer Decisions] in der [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) verwendet.

1. Klicken Sie auf **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]** oder **[!UICONTROL Replace Content]** und dann auf **[!UICONTROL Offer Decision]**.

   Die Option [!UICONTROL Offer Decision] ist nur beim Bearbeiten oder Erstellen von [manuellen [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) oder [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) Aktivitäten verfügbar. Diese Option ist für andere Aktivitätstypen nicht verfügbar. Die verfügbaren Optionen im Menü variieren je nach ausgewähltem Element.

   ![Menü &quot;Optionen&quot;im Visual Experience Composer](assets/options-menu.png)

1. Wählen Sie im Dialogfeld **[!UICONTROL Add Offer Decision]** die gewünschte Sandbox und Platzierung aus.

   Mit einer [Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} im [!DNL Adobe Experience Platform] können Sie Ihre Instanz in virtuelle Umgebungen aufteilen. Sie können beispielsweise über eine Produktionsumgebung und eine Staging-Umgebung verfügen. Eine [Platzierung](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] hilft sicherzustellen, dass der richtige Angebotsinhalt an der richtigen Stelle angezeigt wird.

   ![Dropdown-Listen Sandbox und Platzierungen im Dialogfeld Angebotsentscheidung hinzufügen](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Wählen Sie die gewünschte Angebotsentscheidung aus und klicken Sie dann auf **[!UICONTROL Create]**.

   ![Ausgewählte Angebotsentscheidung im Dialogfeld Angebotsentscheidung hinzufügen](assets/offer-decision.png)

   Ihre Website wird im VEC angezeigt, wo Sie die neu erstellte Angebotsentscheidung im Bereich [!UICONTROL Modifications] auf der rechten Seite sehen können. Sie können den Mauszeiger über die Änderung bewegen und auf das Symbol [!UICONTROL Preview] klicken, um die Angebotsentscheidung zu untersuchen.

   ![Vorschau-Symbol](assets/preview-icon.png)

   Sie können die verschiedenen im Angebot enthaltenen Angebote untersuchen, indem Sie auf das entsprechende Symbol unten im Dialogfeld [!UICONTROL Offer Preview] klicken, einschließlich des Fallback-Angebots. Ein Fallback-Angebot ist das Standardangebot, das angezeigt wird, wenn ein Besucher für keines der personalisierten Angebote in der Sammlung qualifiziert ist.

   ![Angebotsvorschau](assets/offer-preview.png)

1. Schließen Sie die Erstellung der Aktivität ab, indem Sie die Schritte [!UICONTROL Targeting] und [!UICONTROL Goals & Settings] des dreiteiligen geführten Workflows ausführen.

   >[!IMPORTANT]
   >
   >Um sicherzustellen, dass die [!DNL Target] -Aktivität personalisiert ist, stellen Sie sicher, dass das aktuelle Start-/Enddatum der Aktivität mit dem Start-/Enddatum der Angebotsentscheidung in [!DNL Adobe Journey Optimizer] übereinstimmt. Wenn das Start-/Enddatum [!DNL Target] außerhalb des Datums des Start-/Enddatums der Angebotsentscheidung liegt, wird Besuchern der standardmäßige Inhalt von [!DNL Target] angezeigt.

   ![Warnmeldung bei Angebotsentscheidungen](/help/main/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## Hinweise und Einschränkungen

Beachten Sie bei der Arbeit mit Angebotsentscheidungen die folgenden Informationen:

* Die offer decisioning-Integration funktioniert bei [!DNL Target] -Implementierungen basierend auf dem [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}. Diese Funktion ist nicht verfügbar, wenn [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs implementiert wird.

* Die Integration von [!DNL Target]/[!DNL Adobe Journey Optimizer] unterstützt nur die Aktivitäten [manuell [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) und [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Diese Funktion ist nicht für andere Aktivitätstypen verfügbar.

* Sie können nicht [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, wenn Sie Angebotsentscheidungen in einer Aktivität verwenden. Wählen Sie während der Aktivitätseinrichtung [!DNL Target] als Berichtsquelle auf der Seite [!UICONTROL Goals and Settings] aus, wenn Sie Angebotsentscheidungen in der Aktivität verwenden.

* Angebote mit dem Inhaltstyp text/html unterstützen nicht die Bereitstellung von VersandURL-Inhalten. Die deliveryURL wird durch den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) nur unterstützt, wenn der Client für das explizite Abrufen und Zusammenstellen des Inhalts verantwortlich ist.

* [!DNL Target] -Berichte bieten keine Berichte auf Ebene der Angebotsentscheidungen.

* Die Visualisierung von [QA-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) für [!DNL Target] Erlebnisse, die Angebotsentscheidungen enthalten, wirkt sich auf die in [!DNL Adobe Journey Optimizer] festgelegte Frequenzlimitierung für diese Angebotsentscheidungen aus.
