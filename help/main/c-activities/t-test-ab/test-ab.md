---
keywords: AB;A/B;AB...n;Erlebnisse vergleichen;Targeting;Inhalt vergleichen;automatisches Targeting;automatische Zuordnung
description: Erfahren Sie mehr über die verschiedenen Arten von A/B-Test-Aktivitäten in Adobe. [!DNL Target] - Manuell, Automatische Zuordnung und Automatisches Targeting. Wählen Sie den, der für Sie geeignet ist.
title: Welche Art von A/B-Aktivitäten sind in Target verfügbar?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: b5da2f5d41739af39d97e0ce9761006794c04d2b
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 25%

---

# A/B-Test - Überblick

Ein Handbuch [!UICONTROL A/B-Test] -Aktivität vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.

>[!NOTE]
>
>Zusätzlich zum Handbuch (Standard) [!UICONTROL A/B-Test] -Aktivität (siehe diesen Abschnitt), [!DNL Target] bietet zwei weitere Typen von [!UICONTROL A/B-Test] Aktivitäten: [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]. Siehe [Typen von A/B-Test-Aktivitäten](#types) unten finden Sie weitere Informationen.

Ein Handbuch [!UICONTROL A/B-Test] -Aktivität (manchmal auch als A/B...N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am meisten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

Manuelle A/B-Tests sind nützlich, wenn Sie eine klare Vorstellung davon haben, wie Sie die Seitenleistung basierend auf Erfolgsmetriken oder der Bereitstellung alternativer Inhalte verbessern können.

Manuelle A/B-Tests eignen sich gut für umfangreiche Änderungen, die neue Layouts oder eine deutlich unterschiedliche Behandlung der Elemente erfordern können. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente unterteilt werden kann, sollten Sie vor einem [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Bei der Einrichtung Ihres A/B-Tests können Sie den Prozentsatz der Besucher bestimmen, die die einzelnen Erlebnisse sehen. Sie könnten beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen, oder Sie könnten ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wenn die Anzahl unterschiedlicher Erlebnisse fünf überschreitet und sich über zwei oder mehr Orte erstreckt, empfiehlt es sich, eine [MVT-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) vor der Durchführung Ihrer A/B-Tests. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Auf diese Bereiche sollte sich ein Marketing-Experte konzentrieren. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Orte und Inhalte am nützlichsten sind, um Sie bei der Erreichung Ihrer Ziele zu unterstützen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. So können Sie z. B. zwei spezifische Bilder gegeneinander testen oder den Wortlaut oder die Farben eines Aktionsaufrufs vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Test-Aktivitäten {#types}

Zusätzlich zum Handbuch [!UICONTROL A/B-Test] -Aktivität (siehe diesen Abschnitt), [!DNL Target] bietet zwei weitere Arten von A/B-Test-Aktivitäten: [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manueller A/B-Test] | Vergleicht zwei oder mehr Erlebnisse, um festzustellen, durch welches Erlebnis Konversionen über einen zuvor festgelegten Testzeitraum am besten verbessert werden.<P>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle [!UICONTROL A/B-Test] -Aktivität, aber die Schritte für die anderen Typen [!UICONTROL A/B-Test] -Aktivitäten sind ähnlich. |
| [!UICONTROL Automatische Zuordnung] | Identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und leitet dann den Traffic an den Gewinner weiter, wodurch die Konversion im Zuge der Testausführung und des Lernens erhöht wird.<P>Informationen zu den Vorteilen der Verwendung eines [!UICONTROL Automatische Zuordnung] -Aktivität, siehe [Automatische Zuordnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Dauer der Durchführung eines A/B-Tests* und [Übersicht über die automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium-Zeichen](/help/main/assets/premium.png) [!UICONTROL Automatisches Targeting] | Verwendet das erweiterte maschinelle Lernen zum Personalisieren von Inhalten und Fördern von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Das am besten angepasste Erlebnis wird dann Besuchern basierend auf ihren individuellen Kundenprofilen und früheren Verhaltensweisen ähnlicher Besucher bereitgestellt.<P>Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen darüber, welche dieser [!UICONTROL A/B-Test] Die Aktivitäten eignen sich für Sie, siehe die interaktiven [Adobe Target Activities Guide PDF](/help/main/c-activities/target-activities-guide.md).

Die Schritte zur Erstellung der drei Typen [!UICONTROL A/B-Test] -Aktivitäten sind ähnlich. So erstellen Sie eine [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting] Aktivität, beginnen mit [Erstellen einer A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), aber wenn Sie zum [!UICONTROL Targeting] die gewünschte Traffic-Zuordnungsmethode aus, wie unten dargestellt:

* [!UICONTROL Automatisch dem besten Erlebnis zuordnen]
* [!UICONTROL Automatisches Targeting für personalisiertes Erlebnis]

![Einstellungen für die Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Empfehlungen in A/B-Aktivitäten einschließen

Sie können Empfehlungen in [!UICONTROL A/B-Test], [!UICONTROL Automatische Zuordnung], und [!UICONTROL Automatisches Targeting] Aktivitäten (und [!UICONTROL Erlebnis-Targeting] (XT). Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen

## Schulungsvideo: Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
