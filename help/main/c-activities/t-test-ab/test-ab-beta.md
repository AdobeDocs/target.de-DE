---
keywords: AB;A/B;AB...n;Erlebnisse vergleichen;Targeting;Inhalt vergleichen;automatisches Targeting;automatische Zuordnung
description: Erkunden Sie die A/B-Test-Aktivitäten in  [!DNL Target]  - [!UICONTROL Manual], [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].
title: Entdecken Sie die in [!DNL Target] verfügbaren A/B-Test-Aktivitäten.
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: 36cc6486a95b977589aced55168a93ffd300d78f
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 21%

---

# A/B-Test - Überblick

Eine manuelle [!UICONTROL A/B Test] -Aktivität (manchmal auch als A/B...N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am meisten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

>[!TIP]
>
>Zusätzlich zur Aktivität [!UICONTROL Manual] (Standard) [!UICONTROL A/B Test] (wird in diesem Artikel erläutert) stellt [!DNL Target] zwei weitere Typen von [!UICONTROL A/B Test] Aktivitäten bereit: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]. Weitere Informationen finden Sie unten unter [Typen von A/B-Testaktivitäten](#types) .

Manuelle A/B-Tests sind nützlich, wenn Sie eine klare Vorstellung davon haben, wie Sie die Seitenleistung basierend auf Erfolgsmetriken oder der Bereitstellung alternativer Inhalte verbessern können.

Manuelle A/B-Tests eignen sich gut für umfangreiche Änderungen, die neue Layouts oder eine deutlich unterschiedliche Behandlung der Elemente erfordern können. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente unterteilt werden kann, sollten Sie vor dem Ausführen eines [Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) einen A/B-Test durchführen.

Bei der Einrichtung Ihres A/B-Tests können Sie den Prozentsatz der Besucher bestimmen, die die einzelnen Erlebnisse sehen. Sie können beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen oder ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wenn die Anzahl unterschiedlicher Erlebnisse fünf überschreitet und sich über zwei oder mehr Orte erstreckt, sollten Sie einen [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) in Erwägung ziehen, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Auf diese Bereiche sollte sich ein Marketing-Experte konzentrieren. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Orte und Inhalte am nützlichsten sind, um Sie bei der Erreichung Ihrer Ziele zu unterstützen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. So können Sie z. B. zwei spezifische Bilder gegeneinander testen oder den Wortlaut oder die Farben eines Aktionsaufrufs vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Test-Aktivitäten {#types}

Zusätzlich zur manuellen [!UICONTROL A/B Test] -Aktivität bietet [!DNL Target] zwei weitere Arten von [!UICONTROL A/B Testing] Aktivitäten: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergleicht zwei oder mehr Erlebnisse, um zu prüfen, welches Erlebnis über einen zuvor definierten Testzeitraum Konversionen am meisten verbessert.<P>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle [!UICONTROL A/B Test] -Aktivität einrichten, aber die Schritte für die anderen Typen von [!UICONTROL A/B Test] -Aktivitäten sind ähnlich. |
| [!UICONTROL Auto-Allocate] | Identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und leitet dann den Traffic an den Gewinner weiter, wodurch die Konversion im Zuge der Testausführung und des Lernens erhöht wird.<P>Informationen zu den Vorteilen der Verwendung einer [!UICONTROL Auto-Allocate] -Aktivität finden Sie unter [Automatische Zuordnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Wie lange sollten A/B-Tests laufen* und [Übersicht über die automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) . |
| ![Premium Badge](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Verwendet das erweiterte maschinelle Lernen zum Personalisieren von Inhalten und Fördern von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Das am besten angepasste Erlebnis wird dann Besuchern basierend auf ihren individuellen Kundenprofilen und früheren Verhaltensweisen ähnlicher Besucher bereitgestellt.<P>Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen dazu, welche dieser [!UICONTROL A/B Test] -Aktivitäten für Sie geeignet ist, finden Sie im interaktiven [Adobe Target Activities Guide PDF](/help/main/c-activities/target-activities-guide.md).

Die Schritte zum Erstellen der drei Typen von [!UICONTROL A/B Test] -Aktivitäten sind ähnlich. So erstellen Sie eine [!UICONTROL Auto-Allocate] - oder [!UICONTROL Auto-Target] -Aktivität:

1. Beginnen Sie mit dem [ Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).
1. Wenn Sie zur Seite [!UICONTROL Targeting] gelangen, klicken Sie auf das Steuerelement [!UICONTROL Traffic Allocation] und wählen Sie dann die gewünschte Traffic-Zuordnungsmethode im rechten Bereich aus, wie unten dargestellt:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experience]

   ![Einstellungen für die Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

## Empfehlungen in A/B-Aktivitäten einschließen

Sie können Empfehlungen in [!UICONTROL A/B Test]-, [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target] -Aktivitäten (und [!UICONTROL Experience Targeting]-Aktivitäten (XT) einbeziehen. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen.