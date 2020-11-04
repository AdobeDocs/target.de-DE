---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content;auto-target;auto-allocate
description: Eine manuelle A/B-Test-Aktivität vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.
title: Überblick über A/B-Tests
feature: ab
uuid: 154559cf-58bb-425d-bb2e-4eaf34c89451
translation-type: tm+mt
source-git-commit: 6e0605304d99c0a070ad22a232e2ba2246611f94
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 38%

---


# Überblick über A/B-Tests

A manual [!UICONTROL A/B Test] activity compares two or more versions of your website content to see which version best improves your conversions during a pre-specified test period.

>[!NOTE]
>
>Zusätzlich zur manuellen (Standardeinstellung) [!UICONTROL A/B-Test] -Aktivität (in diesem Abschnitt erläutert) [!DNL Target] stehen zwei weitere Typen von [!UICONTROL A/B-Test] -Aktivitäten zur Verfügung: [!UICONTROL Automatische Zuordnung] und [!UICONTROL automatische Zielgruppe].
>
>Weitere Informationen finden Sie unter [Typen von A/B-Testing-Aktivitäten](#types) .

A manual [!UICONTROL A/B Test] activity (sometimes referred to as an A/B...N test) compares two or more versions of your Web site content to see which best lifts your conversions, sales, or other metrics you identify. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

Manuelle A/B-Tests sind besonders hilfreich, wenn Sie eine klare Hypothese haben, wie Sie die Seitenleistung anhand von Erfolgsmetriken oder Versänden alternativer Inhalte verbessern können.

Manuelle A/B-Tests eignen sich gut für umfangreiche Änderungen, bei denen neue Layouts oder eine ganz andere Behandlung der Elemente erforderlich sein können. If your test design does not easily break down into individual page elements, you should run an A/B test before a [multivariate test](/help/c-activities/c-multivariate-testing/multivariate-testing.md).

Beim Einrichten des A/B-Tests können Sie den Prozentsatz der Besucher ermitteln, die die einzelnen Erlebnisse sehen. Sie könnten beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen, oder Sie könnten ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](../../c-activities/t-test-ab/sample-size-determination.md).

Bei mehr als fünf verschiedenen Erlebnissen mit zwei oder mehr Orten ist möglicherweise ein [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) empfehlenswert, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Orte, auf die sich ein Marketingexperte konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Sobald Sie festgelegt haben, welche Orte und Inhalte am nützlichsten sind, um Ihnen bei der Erreichung Ihrer Ziele zu helfen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern, z. B. um zwei spezifische Bilder untereinander zu testen oder die Formulierungen oder Farben eines Aktionsaufrufs zu vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Aktivitäten für A/B-Tests {#types}

Zusätzlich zur manuellen [!UICONTROL A/B-Test] -Aktivität (in diesem Abschnitt erläutert) [!DNL Target] stehen zwei weitere Typen von A/B-Test-Aktivitäten zur Verfügung: [!UICONTROL Automatische Zuordnung] und [!UICONTROL automatische Zielgruppe].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manueller A/B-Test] | Vergleicht zwei oder mehr Erlebnisse, um zu prüfen, durch welche Erlebnisse Konversionen über einen zuvor definierten Testzeitraum am besten optimiert werden.<br>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle [!UICONTROL A/B-Test] -Aktivität einrichten. Die Schritte für die anderen Typen von [!UICONTROL A/B-Test] -Aktivitäten sind jedoch ähnlich. |
| [!UICONTROL Automatische Zuordnung] | Identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und leitet den Traffic dann an den Gewinner weiter, wobei die Konversionen durch die Testausführung und das Lernen erhöht werden.<br>Informationen zu den Vorteilen der Verwendung einer Aktivität mit automatisierter Zuordnung finden Sie unter [Automatisierte Zuordnung](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Wie lange sollten Sie einen A/B-Test* und eine Übersicht über die [automatische Zuordnung durchführen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium-Zeichen](/help/assets/premium.png) [!UICONTROL Auto-Zielgruppe] | Verwendet das erweiterte maschinelle Lernen zum Personalisieren von Inhalt und Fördern von Konversionen, indem mehrere vom Vermarkter definierte Erlebnisse mit hoher Leistung identifiziert werden und das passendste Erlebnis für Benutzer bereitgestellt wird. Dies basiert auf den individuellen Kundenprofilen und dem Verhalten ähnlicher vorheriger Besucher.<br>Weitere Informationen finden Sie unter [Automatische Zielgruppe](/help/c-activities/auto-target-to-optimize.md). |

Weitere Informationen darüber, welche dieser [!UICONTROL A/B-Test] -Aktivitäten für Sie am besten geeignet sind, finden Sie im PDF-Dokument &quot;PDF [zu interaktiven](/help/c-activities/target-activities-guide.md)Adobe Target-Aktivitäten&quot;.

Die Schritte zum Erstellen der drei Typen von [!UICONTROL A/B-Test] -Aktivitäten sind ähnlich. Um eine Aktivität für die [!UICONTROL automatische Zuordnung] oder [!UICONTROL automatische Zielgruppe] zu erstellen, wählen Sie Beginn durch [Erstellung einer A/B-Test-Aktivität](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md). Wenn Sie jedoch zur [!UICONTROL Targeting] -Seite gelangen, wählen Sie die gewünschte Traffic-Zuordnungsmethode wie unten dargestellt:

* [!UICONTROL Automatische Zuordnung zu bestem Erlebnis]
* [!UICONTROL Automatische Zielgruppe für personalisiertes Erlebnis]

![Einstellungen der Traffic-Zuordnungsmethode](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Schulungsvideo: Aktivität Types (9:03) - ![Überblick](/help/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
