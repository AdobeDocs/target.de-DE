---
keywords: automated traffic allocation;targeting;auto-allocate
description: Die Funktion „Automatisch zuweisen“ identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.
title: Auto-Allocate can give you faster test results and higher revenue than a manual test
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 5%

---


# Auto-Allocate can give you faster test results and higher revenue than a manual test

With a manual A/B activity, you might be losing conversions because you can’t deliver the winning experience to your entire audience until the activity completes. Your traffic distribution remains fixed even after you recognize that some experiences are outperforming others, and the activity must run its entire course before you can act on a winner.

## Automatische Zuordnung von Traffic

If you want an option to serve the winning experience more often and earlier in the activity while simultaneously removing or reducing the set-up and calculation cost of picking sample sizes, confidence levels, and other statistical concepts, [!UICONTROL Auto-Allocate] is your best option.

## Wie funktioniert die automatische Zuordnung?

[!UICONTROL Die automatische Zuordnung] verwendet das Prinzip des Multi-Armed Bandit. If the term is unfamiliar, a one-armed bandit is a colloquial term for a slot machine (think: Las Vegas). Visualisieren Sie die automatische Zuordnung von Traffic als mit mehreren Stecknadelautomaten, in diesem Fall mit Testvarianten, und ziehen Sie zunächst alle Griffe gleich. Im Laufe der Zeit könnten eine oder mehrere Maschinen oder Testvarianten mehr auszahlen als andere. Wenn das passiert, würde ein Spieler natürlich Beginn die Griffe der Griffe ziehen, die öfter gewinnen. In traffic allocation terms, [!DNL Adobe Target] will serve more visitors the experience or experiences that are winning more.

Betrachten Sie die folgende Abbildung einer zweiwöchigen A/B-Aktivität. Bei [!UICONTROL automatisierter Zuordnung]wird, sobald ein erfolgreiches Erlebnis entsteht, der Traffic zu diesem Gewinner frühzeitig im Test durch die [!UICONTROL Zielgruppe] umgeleitet.

![Abbildung zur automatischen Zuordnung](/help/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## Wie kann ich mit der automatischen Zuordnung schneller Ergebnisse erzielen?

Die Vorteile sind ziemlich klar: mehr Besucher sehen die Varianten, die am besten funktionieren. Und während eine einzige Variante vorankommt, werden noch mehr Besucher zu diesem Gewinn-Erlebnis umgeleitet, während der Test noch läuft. Dies ist besonders hilfreich, wenn die ausgeführte A/B-Aktivität während eines Kerngeschäftes wie Feiertag, Produkteinführung oder World News Ereignis stattfindet.

## Wie könnte die automatisierte Zuordnung zu einem höheren Umsatz führen?

[!UICONTROL Die automatisierte Zuordnung] findet den Gewinner schneller als eine manuelle A/B-Aufteilung und ermöglicht es Ihnen außerdem, diesen Gewinner sofort zu nutzen, um den Mehrwert zu erfassen, der bei einem herkömmlichen oder manuellen Ansatz verloren gegangen wäre. Da die [!UICONTROL automatisierte Zuordnung] mehr Traffic zum Erlebnis mit dem höchsten Konversionsrate leitet, kann sie Ihren Umsatz erhöhen, während die Aktivität ausgeführt wird und lernt.

Im folgenden Beispiel erzielte die [!UICONTROL automatisierte Zuordnung] während des Tests mehr Umsatz, indem mehr Traffic (40 %) zu Erlebnis D gedrängt wurde, das den höchsten Konversionsrat aufwies.

![Die automatische Zuordnung bietet eine bessere Darstellung des Umsatzes.](/help/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## In welchen Fällen sollte ich bei der manuellen Traffic-Zuordnung bleiben?

Wenn Sie die Rangfolge der einzelnen Erlebnisse im Vergleich zu den anderen festlegen müssen, ist ein manueller A/B-Test am besten geeignet. [!UICONTROL Die automatisierte Zuordnung] findet und nutzt die leistungsstärksten Erlebnisse, garantiert jedoch keine Differenzierung zwischen den leistungsschwächeren Erlebnissen. Sie sollten die manuelle Traffic-Zuordnung verwenden, um vollständig zu kontrollieren, wie viel Traffic in Ihrem Besucher die einzelnen Testvarianten sieht, und um die statistischen Schwellenwerte anzupassen, die für Ihr Unternehmen relevant sind.

## Erste Schritte

Sind Sie bereit, Ihre erste [!UICONTROL Aktivität für die automatische Zuordnung] zu starten? [Erfahren Sie hier](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

