---
keywords: Visual Experience Composer-Optionen; Experience Composer-Optionen; Erlebnisoptionen; Angebotsentscheidung; Offer Decisioning; AJO; Journey Optimizer
description: Erfahren Sie, wie Sie einer Aktivität eine  [!DNL Adobe Journey Optimizer]  erstellte Angebotsentscheidung hinzufügen.
title: Wie verwende ich Angebotsentscheidungen?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
TQID: https://experienceleague.adobe.com/xEae4As4rNbPv-an3Iu8PCMzxftSAmN4iu0PEq6VDFQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1017
ht-degree: 2%

---

# Verwenden von Angebotsentscheidungen

Verwenden Sie [!DNL Adobe Target] mit [!DNL Adobe Journey Optimizer] Angebotsentscheidungen, um das nächstbeste Angebot für Ihre Besucher im Web und auf Mobilgeräten zu ermitteln und bereitzustellen.

Fügen Sie in [!DNL Adobe Journey Optimizer] erstellte Angebotsentscheidungen [!DNL Target] -Aktivitäten (manueller [!UICONTROL A/B-Test] oder [!UICONTROL Experience Targeting]) hinzu, indem Sie entweder den [!UICONTROL Visual Experience Composer] (VEC) oder den [!UICONTROL formularbasierten Composer] verwenden, um Ihren Besuchern auf Ihren eingehenden Kanälen auf Basis von [!DNL Target] personalisierte Angebote zu testen und bereitzustellen.

Weitere Informationen zu [!DNL Adobe Journey Optimizer] und Angebotsentscheidungen finden Sie in den folgenden Themen in der *[!DNL Journey Optimizer]*:

* [Erste Schritte mit Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)

* [Über das Entscheidungs-Management](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html)

## Voraussetzungen

Um Angebotsentscheidungen in [!DNL Target] zu verwenden, benötigen Sie Folgendes:

* [!DNL Adobe Target Standard] oder [!DNL Adobe Target Premium] mit der [Adobe Experience Platform Web SDK implementiert](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

  Die Funktion ist nicht verfügbar, wenn [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs implementiert wird.

* [!DNL Adobe Journey Optimizer Ultimate] (AJO + Offer Decisioning) oder [!DNL Adobe Experience Platform] und das Add-on {2Offer Decisioning} Application Service .

## Beispiele für Anwendungsfälle

Im Folgenden finden Sie Beispiele für Anwendungsfälle, in denen Sie mithilfe der [!DNL Target]/[!DNL Adobe Journey Optimizer]-Integration Angebotsentscheidungen in [!DNL Target] Aktivitäten verwenden können:

### Sportartikelwerbung

Als Marketing-Experte für eine Sportliga möchten Sie Inhalte auf Ihrer Homepage (sowohl auf Desktop- als auch auf mobilen Websites) personalisieren. Sie möchten Inhalte basierend auf mehreren Dimensionen personalisieren und ein Angebot für Shop-bezogene Franchise-Waren unterbreiten. Sie interessieren sich für:

* Das Lieblingsteam des Besuchers
* Kürzliche Aktivitäten von Athleten/Spielern (z. B. Teambewegung, Vertragsaktualisierungen oder Verletzungen)

Sie möchten zum Beispiel ein personalisiertes Erlebnis für jede der folgenden Regionen bieten: Dortmund, Frankfurt und Bochum sowie für Benutzer, die implizite und explizite Fans dieser Teams sind. Als Metriken möchten Sie Besuche und Klicks auf die Merchandise-Site betrachten.

Sie möchten eine [!UICONTROL A/B-Test]-Aktivität (50/50-Aufteilung) zwischen dem Standarderlebnis und dem personalisierten Erlebnis entwerfen (die eine Angebotsentscheidung mit Angeboten für jede Region und jedes Team umfasst). Sie möchten mit dieser Aktivität die Konversion und die Steigerung für das personalisierte Erlebnis im Vergleich zur Kontrolle bestimmen.

### Spiel-Streaming-Plattformen

Als Marketing-Experte für eine Gaming-Organisation möchten Sie ein personalisiertes Angebot für eine Game-Streaming-Plattform für Desktop- und Mobile-Benutzer aus verschiedenen Regionen bereitstellen: Deutschland, Frankreich, Mexiko und Brasilien. Wenn ein Besucher von einem dieser Länder aus auf den Desktop oder die mobile Website zugreift, möchten Sie ein Angebot für Spiel-Streaming in der Landessprache und mit einem entsprechenden Preis für die Landeswährung bereitstellen.

In [!DNL Adobe Journey Optimizer] können Sie ein personalisiertes Homepage-Hero-Angebot für jede der Zielregionen sowie ein Fallback-Angebot mit einem standardmäßigen Homepage-Hero erstellen. Anschließend können Sie eine Angebotsentscheidung erstellen, die diese Angebote und ihre Eignungsregeln enthält. Anschließend können Sie [!DNL Target] eine [!DNL Experience Targeting] (XT)-Aktivität erstellen und diese Angebotsentscheidung in Ihren Desktop oder Ihre mobile Website einfügen, um Besuchern ein personalisiertes Erlebnis zu bieten.

## Erstellen Sie ein Erlebnis, das eine Angebotsentscheidung verwendet:

1. Klicken Sie beim Bearbeiten oder Erstellen einer manuellen [!UICONTROL A/B]Test- oder [!UICONTROL Experience Targeting]&#x200B;(XT)-Aktivität in [!UICONTROL Visual Experience Composer] (VEC) auf ein Seitenelement, um das Menü [Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) anzuzeigen.

   ![Optionsmenü im Visual Experience Composer](assets/options-menu1.png)

   >[!NOTE]
   >
   >Sie können auch ein Erlebnis erstellen, das [!UICONTROL Angebotsentscheidungen] im [[!UICONTROL formularbasierten Experience Composer) &#x200B;]](/help/main/c-experiences/form-experience-composer.md).

1. Klicken Sie **[!UICONTROL Inhalt ersetzen]** und anschließend auf **[!UICONTROL Angebotsentscheidung]**.

   Die Option [!UICONTROL Angebotsentscheidung] ist nur beim Bearbeiten oder Erstellen [[!UICONTROL &#x200B; manuellen A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types)Tests oder [[!UICONTROL Erlebnis-Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) verfügbar. Diese Option steht für andere Aktivitätstypen nicht zur Verfügung. Die verfügbaren Optionen im Menü variieren je nach ausgewähltem Element.

   ![Optionsmenü im Visual Experience Composer](assets/options-menu.png)

1. Wählen **[!UICONTROL in der Leiste]** Angebotsentscheidung hinzufügen“ auf der rechten Seite des VEC die gewünschte Sandbox aus und klicken Sie dann auf Angebotsentscheidung auswählen.placement.

   Mit einer [Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} im [!DNL Adobe Experience Platform] können Sie Ihre Instanz in virtuelle Umgebungen unterteilen. Sie könnten beispielsweise über eine Produktionsumgebung und eine Staging-Umgebung verfügen. Eine [Platzierung](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] hilft sicherzustellen, dass der richtige Angebotsinhalt an der richtigen Stelle angezeigt wird.

   ![Sandbox- und Platzierungen -Dropdown-Listen im Dialogfeld Angebotsentscheidung hinzufügen](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Wählen Sie die gewünschte Platzierung und Angebotsentscheidung aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   ![Dialogfeld Angebotsentscheidung auswählen](/help/main/c-integrating-target-with-mac/ajo/assets/select-offer-decision.png)

   Ihre Website wird in VEC angezeigt, wo Sie die neu erstellte Angebotsentscheidung in der Leiste [!UICONTROL Änderungen] sehen können. Sie können unten in der Leiste „Angebotsentscheidung[!UICONTROL &#x200B; auf ein Angebot &#x200B;]&#x200B;[!UICONTROL &#x200B; Angebotsvorschau] klicken, um die Angebotsentscheidung zu untersuchen.

   <!--You can examine the various offers contained in the offer by clicking the appropriate icon at the bottom of the [!UICONTROL Offer Preview] dialog box, including the fallback offer. A fallback offer is the default offer displayed when a visitor is not eligible for any of the personalized offers in the collection.-->

   ![Angebotsvorschau](assets/offer-preview2.png)

1. Schließen Sie die Erstellung der Aktivität ab[!UICONTROL &#x200B; indem Sie die Schritte &#x200B;]Zielgruppenbestimmung[!UICONTROL &#x200B; und Ziele und Einstellungen] des dreiteiligen geleiteten Workflows abschließen.

   >[!IMPORTANT]
   >
   >Um sicherzustellen, dass die [!DNL Target] personalisiert ist, stellen Sie sicher, dass das aktuelle Start-/Enddatum der Aktivität mit dem Start-/Enddatum der Angebotsentscheidung in [!DNL Adobe Journey Optimizer] übereinstimmt. Wenn die [!DNL Target] Start-/Enddaten außerhalb des Start-/Enddatumsbereichs der Angebotsentscheidung liegen, wird den Besuchern der [!DNL Target] Standardinhalt angezeigt.

## Hinweise und Einschränkungen

Beachten Sie bei der Arbeit mit Angebotsentscheidungen die folgenden Informationen:

* Die Offer Decisioning-Integration funktioniert für [!DNL Target]-Implementierungen, die auf der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} basieren. Diese Funktion ist nicht verfügbar, wenn [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs implementiert wird.

* Die [!DNL Target]/[!DNL Adobe Journey Optimizer]-Integration unterstützt nur [manuelle [!UICONTROL A/B-]](/help/main/c-activities/t-test-ab/test-ab.md#types)- und [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md)-Aktivitäten (XT). Diese Funktion ist für andere Aktivitätstypen nicht verfügbar.

* Sie können [[!UICONTROL Analytics) nicht als Berichtsquelle &#x200B;]](/help/main/c-integrating-target-with-mac/a4t/a4t.md)A4T) verwenden, wenn Sie Angebotsentscheidungen in einer Aktivität verwenden. Wählen Sie [!DNL Target] als Berichtsquelle auf der Seite [!UICONTROL Ziele und Einstellungen] während der Aktivitätseinrichtung, wenn Sie Angebotsentscheidungen in der Aktivität verwenden.

* Angebote mit dem Inhaltstyp text/html unterstützen nicht die Bereitstellung von deliveryURL-Inhalten. Die deliveryURL wird vom [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) nur dann unterstützt, wenn der Client für das explizite Abrufen und Erstellen des Inhalts verantwortlich ist.

* [!DNL Target] Reporting bietet keine Berichte auf Angebotsentscheidungs-Ebene.

* Die Visualisierung [QA-](/help/main/c-activities/c-activity-qa/activity-qa.md)) für [!DNL Target] Erlebnisse, die Angebotsentscheidungen enthalten, wirkt sich auf die Frequenzlimitierung aus, die in [!DNL Adobe Journey Optimizer] für diese Angebotsentscheidungen festgelegt wird.
