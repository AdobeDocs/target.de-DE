---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content
description: Beim A/B-Test werden zwei oder mehr Versionen Ihrer Website-Inhalte verglichen, um festzustellen, mit welcher Version Ihre Konversionen in einem vorab festgelegten Zeitraum verbessert werden.
title: A/B-Test
feature: ab
uuid: 154559cf-58bb-425d-bb2e-4eaf34c89451
translation-type: tm+mt
source-git-commit: 130edc89b2c324a0d892a4221f644248e23357a4
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 58%

---


# A/B-Test

Ein manueller A/B-Test vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.

>[!NOTE]
>
>Zusätzlich zur manuellen (Standardeinstellung) A/B-Test-Aktivität (in diesem Abschnitt erläutert) [!DNL Target] stehen zwei weitere Typen von A/B-Test-Aktivitäten zur Verfügung: [!UICONTROL Automatische Zuordnung] und [!UICONTROL automatische Zielgruppe].
>
>Weitere Informationen finden Sie unter [Typen von A/B-Testing-Aktivitäten](#types) .

Ein manueller A/B-Test (manchmal auch als A/B...N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am meisten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

Manuelle A/B-Tests sind besonders hilfreich, wenn Sie eine klare Hypothese haben, wie Sie die Seitenleistung anhand von Erfolgsmetriken oder Versänden alternativer Inhalte verbessern können.

Manuelle A/B-Tests eignen sich gut für umfangreiche Änderungen, bei denen neue Layouts oder eine ganz andere Behandlung der Elemente erforderlich sein können. Wenn Ihr Testdesign nicht ohne Weiteres in einzelne Seitenelemente unterteilt werden kann, sollten Sie vor einem Multivariater Test zunächst einen A/B-Test durchführen.

Sie können beim Einrichten Ihres Tests festlegen, welcher Prozentsatz an Besuchern das jeweilige Erlebnis anzeigen kann. Sie könnten beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen, oder Sie könnten ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](../../c-activities/t-test-ab/sample-size-determination.md#concept_2801F552DB874C20B8A17C1B774C0383).

Bei mehr als fünf verschiedenen Erlebnissen mit zwei oder mehr Orten ist möglicherweise ein [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) empfehlenswert, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Orte, auf die sich ein Marketingexperte konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Sobald Sie festgelegt haben, welche Orte und Inhalte am nützlichsten sind, um Sie bei der Erreichung Ihrer Ziele zu unterstützen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern, wie zum Beispiel den vergleichenden Test zweier spezifischer Bilder oder den Vergleich von Formulierungen oder Farben eines Aktionsaufrufs. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Aktivitäten für A/B-Tests {#types}

Zusätzlich zur manuellen (Standardeinstellung) A/B-Test-Aktivität (in diesem Abschnitt erläutert) [!DNL Target] stehen zwei weitere Typen von A/B-Test-Aktivitäten zur Verfügung: [!UICONTROL Automatische Zuordnung] und [!UICONTROL automatische Zielgruppe].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| Manueller A/B-Test | Vergleicht zwei oder mehr Erlebnisse, um zu prüfen, durch welche Erlebnisse Konversionen über einen zuvor definierten Testzeitraum am besten optimiert werden.<br>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle A/B-Testing-Aktivität einrichten. Die Schritte für die anderen A/B-Testing-Aktivitäten sind jedoch ähnlich. |
| [!UICONTROL Automatische Zuordnung] | Identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und leitet den Traffic dann an den Gewinner weiter, wobei die Konversionen durch die Testausführung und das Lernen erhöht werden.<br>Weitere Informationen finden Sie unter [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium-Zeichen](/help/assets/premium.png) [!UICONTROL Auto-Zielgruppe] | Verwendet das erweiterte maschinelle Lernen zum Personalisieren von Inhalt und Fördern von Konversionen, indem mehrere vom Vermarkter definierte Erlebnisse mit hoher Leistung identifiziert werden und das passendste Erlebnis für Benutzer bereitgestellt wird. Dies basiert auf den individuellen Kundenprofilen und dem Verhalten ähnlicher vorheriger Besucher.<br>Weitere Informationen finden Sie unter [Automatische Zielgruppe](/help/c-activities/auto-target-to-optimize.md). |

Weitere Informationen darüber, welche dieser A/B-Testing-Aktivitäten für Sie am besten geeignet ist, finden Sie im PDF-Dokument &quot;Leitfaden zu interaktiven [Adobe Target-Aktivitäten&quot;](/help/c-activities/target-activities-guide.md).

Die Schritte zum Erstellen der drei Typen von A/B-Testing-Aktivitäten sind ähnlich. Um eine Aktivität für die [!UICONTROL automatische Zuordnung] oder [!UICONTROL automatische Zielgruppe] zu erstellen, wählen Sie Beginn durch [Erstellung einer A/B-Testing-Aktivität](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md). Wenn Sie jedoch zur [!UICONTROL Targeting] -Seite gelangen, wählen Sie die gewünschte Traffic-Zuordnungsmethode:

* [!UICONTROL Automatische Zuordnung zu bestem Erlebnis]
* [!UICONTROL Automatische Zielgruppe für personalisiertes Erlebnis]

![Einstellungen der Traffic-Zuordnungsmethode](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Schulungsvideo: Aktivität Types (9:03) - ![Überblick](/help/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
