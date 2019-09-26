---
description: Die Produktteams der modernen Technologie übernehmen kontinuierliche Lieferprinzipien für Produkteinführungen. Target unterstützt Entwickler und Produktteams bei der schnellen und effizienten Einführung neuer Produktfunktionen.
keywords: Rollout;Rollout;kontinuierliche Bereitstellung;Produktstart;schrittweise Einführung
seo-description: Die Produktteams der modernen Technologie übernehmen kontinuierliche Lieferprinzipien für Produkteinführungen. Adobe Target unterstützt Entwickler und Produktteams bei der schnellen und effizienten Einführung neuer Produktfunktionen in einer Phase.
seo-title: Die Produktteams der modernen Technologie übernehmen kontinuierliche Lieferprinzipien für Produkteinführungen. Adobe Target unterstützt Entwickler und Produktteams bei der schnellen und effizienten Einführung neuer Produktfunktionen.
solution: Target
title: Funktionskennzeichnung
topic: Standard
translation-type: tm+mt
source-git-commit: 08debab3ec3d2f6e6bfd3c42476dc1a021185ab7

---


# Funktionskennzeichnung

Die Produktteams der modernen Technologie übernehmen kontinuierliche Lieferprinzipien für Produkteinführungen. Adobe Target unterstützt Entwickler und Produktteams bei der schnellen und effizienten Einführung neuer Produktfunktionen in einer Phase.

Die folgenden Links enthalten Informationen zu wichtigen Konzepten, die Sie verstehen müssen, um eine kontinuierliche Bereitstellung zu ermöglichen:

* [A/B-Testaktivitäten](/help/c-activities/t-test-ab/test-ab.md)
* [JSON-Angebote](/help/c-experiences/c-manage-content/create-json-offer.md)
* [Zielgruppenoptimierung](/help/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md)

## Kontinuierliche Bereitstellung

1. Schalten Sie die Funktion bei der Veröffentlichung standardmäßig aus.

   Verwenden Sie zur Steuerung eine serverseitige oder In-App-Variable.

1. Erstellen Sie ein Target-JSON-Angebot, das diese Variable auf "on"setzt.

1. Erstellen Sie eine A/B-Testaktivität im [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) mit zwei Erlebnissen und verwenden Sie das im vorherigen Schritt erstellte JSON-Angebot in einem Erlebnis.

   Oder

   Create an A/B Test activity in the Form-Based Experience Composer with a single experience and use the JSON offer created in the previous step.[](/help/c-experiences/form-experience-composer.md)

   >[!NOTE]
   >
   >Mit dem formularbasierten Experience Composer können Sie eine A/B-Testaktivität mit einem einzigen Erlebnis erstellen. Sie können die Aktivität nicht mit einem einzigen Erlebnis mit dem VEC erstellen.

1. Specify your desired traffic allocation for the activity.

   If you want to start by rolling this feature out to 5% of your visitors, specify 5 in the Targeting step of the three-part guided workflow and send 100% of the qualifying visitors to the experience with the JSON offer (Experience A).

   The following illustration shows the VEC with two experiences.

   ![Traffic allocation for feature flagging in the VEC](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging.png)

   Die folgende Abbildung zeigt den Form-Based Experience Composer mit einem einzigen Erlebnis.

   ![Traffic allocation for feature flagging in the Form-based Experience Composer](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging-form.png)

1. You can increase the traffic allocation to this activity by gradually increasing the 5% either through the Target UI or using the API until you reach 100% traffic allocation.

   >[!NOTE]
   >
   >An A/B Test activity is sticky for a visitor through the session. If you decrease the traffic allocation, visitors who started seeing this feature continue to view it until their sessions are reset.

## A/B-Testfunktionen

Wenn Sie A/B/...N Testfunktionen verwenden Sie den oben erläuterten Ansatz mit folgenden Verbesserungen:

* Jede Funktionsvariante sollte mit einem geeigneten JSON-Angebot dargestellt werden, das ein Target-Erlebnis bereitstellt.
* Sie können die Traffic-Zuordnung für diesen Test wie oben beschrieben verwalten.

## Parametrisierte Rollouts

Die oben beschriebene Methode hilft Ihnen bei der Verwaltung einer kontrollierten Einführung.

Sie können eine Funktion nur für Ihre Beta-Teilnehmer bereitstellen und diese später für alle anderen Kunden bereitstellen. Dies lässt sich einfach durch die Nutzung von [Target-Positionsparametern](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) oder [Profilparametern](/help/c-target/c-audiences/c-target-rules/visitor-profile.md)erreichen. Diese Parameter können in Verbindung mit einer stufenweisen Traffic-Zuordnung verwendet werden.

## Server- oder clientseitige

Funktionen und Tests können über [Target-APIs](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) (und serverseitige SDKs) sowie clientseitige SDKs (JS, Mobile SDK) bereitgestellt werden. Je nachdem, wie Ihre Website, mobile App oder Ihr Kiosk aufgebaut ist, können Sie die verschiedenen Integrationsoptionen von Target nutzen.
