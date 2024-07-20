---
keywords: AB;A/B;AB...n;Erlebnisse vergleichen;Targeting;Inhalt vergleichen;automatisches Targeting;automatische Zuordnung
description: Erfahren Sie mehr über die verschiedenen Arten von A/B-Test-Aktivitäten in Adobe [!DNL Target]  - Manuelle, automatische Zuordnung und automatisches Targeting. Wählen Sie den, der für Sie geeignet ist.
title: Welche Art von A/B-Aktivitäten sind in Target verfügbar?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: b5da2f5d41739af39d97e0ce9761006794c04d2b
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 25%

---

# A/B-Test - Überblick

Eine manuelle [!UICONTROL A/B Test] -Aktivität vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.

>[!NOTE]
>
>Zusätzlich zur Aktivität Manuell (Standard) [!UICONTROL A/B Test] (siehe diesen Abschnitt) stellt [!DNL Target] zwei weitere Typen von [!UICONTROL A/B Test] Aktivitäten bereit: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]. Weitere Informationen finden Sie unten unter [Typen von A/B-Testaktivitäten](#types) .

Eine manuelle [!UICONTROL A/B Test] -Aktivität (manchmal auch als A/B...N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am meisten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

Manuelle A/B-Tests sind nützlich, wenn Sie eine klare Vorstellung davon haben, wie Sie die Seitenleistung basierend auf Erfolgsmetriken oder der Bereitstellung alternativer Inhalte verbessern können.

Manuelle A/B-Tests eignen sich gut für umfangreiche Änderungen, die neue Layouts oder eine deutlich unterschiedliche Behandlung der Elemente erfordern können. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente unterteilt werden kann, sollten Sie vor einem [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) einen A/B-Test durchführen.

Bei der Einrichtung Ihres A/B-Tests können Sie den Prozentsatz der Besucher bestimmen, die die einzelnen Erlebnisse sehen. Sie könnten beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen, oder Sie könnten ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wenn die Anzahl unterschiedlicher Erlebnisse fünf überschreitet und sich über zwei oder mehr Orte erstreckt, sollten Sie einen [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) in Erwägung ziehen, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Auf diese Bereiche sollte sich ein Marketing-Experte konzentrieren. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Orte und Inhalte am nützlichsten sind, um Sie bei der Erreichung Ihrer Ziele zu unterstützen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. So können Sie z. B. zwei spezifische Bilder gegeneinander testen oder den Wortlaut oder die Farben eines Aktionsaufrufs vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Test-Aktivitäten {#types}

Zusätzlich zur manuellen [!UICONTROL A/B Test] -Aktivität (die in diesem Abschnitt besprochen wird) bietet [!DNL Target] zwei weitere Typen von A/B-Tests: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergleicht zwei oder mehr Erlebnisse, um festzustellen, durch welches Erlebnis Konversionen über einen zuvor festgelegten Testzeitraum am besten verbessert werden.<P>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle [!UICONTROL A/B Test] -Aktivität einrichten, aber die Schritte für die anderen Typen von [!UICONTROL A/B Test] -Aktivitäten sind ähnlich. |
| [!UICONTROL Auto-Allocate] | Identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und leitet dann den Traffic an den Gewinner weiter, wodurch die Konversion im Zuge der Testausführung und des Lernens erhöht wird.<P>Informationen zu den Vorteilen der Verwendung einer [!UICONTROL Auto-Allocate] -Aktivität finden Sie unter [Automatische Zuordnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Wie lange sollten A/B-Tests laufen* und [Übersicht über die automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) . |
| ![Premium Badge](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Verwendet das erweiterte maschinelle Lernen zum Personalisieren von Inhalten und Fördern von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Das am besten angepasste Erlebnis wird dann Besuchern basierend auf ihren individuellen Kundenprofilen und früheren Verhaltensweisen ähnlicher Besucher bereitgestellt.<P>Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen dazu, welche dieser [!UICONTROL A/B Test] -Aktivitäten für Sie geeignet ist, finden Sie im interaktiven [Adobe Target Activities Guide PDF](/help/main/c-activities/target-activities-guide.md).

Die Schritte zum Erstellen der drei Typen von [!UICONTROL A/B Test] -Aktivitäten sind ähnlich. Um eine Aktivität vom Typ [!UICONTROL Auto-Allocate] oder [!UICONTROL Auto-Target] zu erstellen, beginnen Sie mit [ Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md). Wenn Sie jedoch zur Seite [!UICONTROL Targeting] gelangen, wählen Sie die gewünschte Traffic-Zuordnungsmethode wie unten gezeigt:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![Einstellungen für die Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Empfehlungen in A/B-Aktivitäten einschließen

Sie können Empfehlungen in [!UICONTROL A/B Test]-, [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target] -Aktivitäten (und [!UICONTROL Experience Targeting]-Aktivitäten (XT) einbeziehen. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen.

## Schulungsvideo: Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
