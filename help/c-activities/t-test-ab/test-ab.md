---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content;auto-target;auto-allocate
description: Eine manuelle A/B-Test-Aktivität vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.
title: Überblick über A/B-Tests
feature: ab
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 38%

---


# Überblick über A/B-Tests

Eine manuelle [!UICONTROL A/B-Aktivität] vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.

>[!NOTE]
>
>Zusätzlich zur Aktivität Manueller (Standard) [!UICONTROL A/B-Test] (siehe Abschnitt) stellt [!DNL Target] zwei weitere Typen von [!UICONTROL A/B-Test]-Aktivitäten bereit: [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe].
>
>Weitere Informationen finden Sie unter [Typen von A/B-Testing-Aktivitäten](#types) weiter unten.

Eine manuelle [!UICONTROL A/B-Test]-Aktivität (manchmal auch als A/B...N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen Metriken, die Sie identifizieren, am meisten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

Manuelle A/B-Tests sind besonders hilfreich, wenn Sie eine klare Hypothese haben, wie Sie die Seitenleistung anhand von Erfolgsmetriken oder Versänden alternativer Inhalte verbessern können.

Manuelle A/B-Tests eignen sich gut für umfangreiche Änderungen, bei denen neue Layouts oder eine ganz andere Behandlung der Elemente erforderlich sein können. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente unterteilt werden kann, sollten Sie vor einem [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) einen A/B-Test durchführen.

Beim Einrichten des A/B-Tests können Sie den Prozentsatz der Besucher ermitteln, die die einzelnen Erlebnisse sehen. Sie könnten beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen, oder Sie könnten ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/c-activities/t-test-ab/sample-size-determination.md).

Bei mehr als fünf verschiedenen Erlebnissen mit zwei oder mehr Orten ist möglicherweise ein [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) empfehlenswert, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Orte, auf die sich ein Marketingexperte konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Sobald Sie festgelegt haben, welche Orte und Inhalte am nützlichsten sind, um Ihnen bei der Erreichung Ihrer Ziele zu helfen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern, z. B. um zwei spezifische Bilder untereinander zu testen oder die Formulierungen oder Farben eines Aktionsaufrufs zu vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Testing-Aktivitäten {#types}

Zusätzlich zur manuellen Aktivität [!UICONTROL A/B-Test] (in diesem Abschnitt erläutert) stellt [!DNL Target] zwei weitere Typen von A/B-Test-Aktivitäten bereit: [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manueller A/B-Test] | Vergleicht zwei oder mehr Erlebnisse, um zu prüfen, durch welche Erlebnisse Konversionen über einen zuvor definierten Testzeitraum am besten optimiert werden.<br>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle  [!UICONTROL A/B-] Testaktivität einrichten. Die Schritte für die anderen  [!UICONTROL A/B-] Testaktivitäten sind jedoch ähnlich. |
| [!UICONTROL Automatische Zuordnung] | Identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und leitet den Traffic dann an den Gewinner weiter, wobei die Konversionen durch die Testausführung und das Lernen erhöht werden.<br>Informationen zu den Vorteilen der Verwendung einer Aktivität mit automatisierter Zuordnung finden Sie unter  [Automatische ](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) Zuordnung,  *wie lange Sie A/B-* Tests und  [Automatische Zuordnung durchführen sollten](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium ](/help/assets/premium.png) [!UICONTROL badgeAuto-Zielgruppe] | Verwendet das erweiterte maschinelle Lernen zum Personalisieren von Inhalt und Fördern von Konversionen, indem mehrere vom Vermarkter definierte Erlebnisse mit hoher Leistung identifiziert werden und das passendste Erlebnis für Benutzer bereitgestellt wird. Dies basiert auf den individuellen Kundenprofilen und dem Verhalten ähnlicher vorheriger Besucher.<br>Weitere Informationen finden Sie unter  [Automatische Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen darüber, welche dieser [!UICONTROL A/B-Aktivitäten für Sie am besten geeignet sind, finden Sie im PDF [Handbuch zu Adobe Target-Aktivitäten](/help/c-activities/target-activities-guide.md).]

Die Schritte zum Erstellen der drei Typen von [!UICONTROL A/B-Aktivitäten] sind ähnlich. Um eine [!UICONTROL Aktivität für die automatische Zuordnung] oder [!UICONTROL Auto-Zielgruppe] zu erstellen, Beginn durch [Erstellen einer A/B-Test-Aktivität](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) zu erstellen, wählen Sie jedoch beim Aufrufen der Seite [!UICONTROL Targeting] die gewünschte Traffic-Zuordnungsmethode aus, wie nachfolgend gezeigt:

* [!UICONTROL Automatische Zuordnung zu bestem Erlebnis]
* [!UICONTROL Automatische Zielgruppe für personalisiertes Erlebnis]

![Einstellungen der Traffic-Zuordnungsmethode](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Schulungsvideo: Aktivitäten (9:03) ![Übersichtskennzeichen](/help/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
