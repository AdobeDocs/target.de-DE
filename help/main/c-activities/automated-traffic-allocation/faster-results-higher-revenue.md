---
keywords: automatisierte Traffic-Zuordnung; Targeting; automatische Zuordnung; automatische Zuordnung
description: Erfahren Sie, wie Sie [!UICONTROL Automatische Zuordnung] Aktivität in [!DNL Adobe Target] identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu.
title: can [!UICONTROL Automatische Zuordnung] Aktivitäten erzielen schnellere Ergebnisse und höhere Umsätze?
feature: Auto-Allocate
exl-id: 104ad88f-044b-4c2f-bdaf-f023fd1787a5
source-git-commit: e9976135c46f6658030b07fce384364f0c9ff0ed
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# [!UICONTROL Automatische Zuordnung] bietet schnellere Testergebnisse und einen höheren Umsatz als ein manueller Test

Bei einer manuellen A/B-Aktivität gehen möglicherweise Konversionen verloren, da Sie das erfolgreichste Erlebnis erst dann für Ihre gesamte Zielgruppe bereitstellen können, wenn die Aktivität abgeschlossen ist. Ihre Traffic-Verteilung bleibt fest, auch wenn Sie erkennen, dass einige Erlebnisse eine bessere Leistung erzielen als andere. Die Aktivität muss den gesamten Kurs durchlaufen, bevor Sie einen Gewinner erzielen können.

## Automatische Zuordnung von Traffic

Wenn Sie möchten, dass eine Option das erfolgreichste Erlebnis öfter und früher in der Aktivität bereitstellt und gleichzeitig die Einrichtungs- und Berechnungskosten für die Auswahl von Stichprobengrößen, Konfidenzstufen und anderen statistischen Konzepten entfernt oder reduziert, [!UICONTROL Automatische Zuordnung] ist Ihre beste Option.

## Wie funktioniert [!UICONTROL Automatische Zuordnung] arbeiten?

[!UICONTROL Automatische Zuordnung] verwendet den Grundsatz des Multi-Armed Bandit. Wenn der Begriff nicht bekannt ist, ist ein einarmiger Bandit ein umgangssprachlicher Begriff für einen Spielautomaten (wie: Las Vegas). Visualisieren Sie die automatische Zuordnung des Traffics als mit mehreren Steckplatinen, in diesem Fall mit Testvarianten, und ziehen Sie zunächst alle Griffe gleich. Im Laufe der Zeit können eine oder mehrere Maschinen oder Testvarianten mehr ausgeben als andere. Wenn diese Situation eintritt, würde ein Spieler natürlich anfangen, die Griffe der Spieler zu ziehen, die öfter gewinnen. Hinsichtlich der Traffic-Zuordnung [!DNL Target] gibt mehr Besuchern das Erlebnis oder die Erlebnisse, die mehr gewinnen.

Beachten Sie die folgende Abbildung einer zweiwöchigen A/B-Aktivität. Mit [!UICONTROL Automatische Zuordnung], sobald ein erfolgreiches Erlebnis entsteht, [!UICONTROL Target] leitet im Test frühzeitig einen größeren Teil des Traffics an diesen Gewinner weiter.

![Abbildung der automatischen Zuordnung](/help/main/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## Wie funktioniert [!UICONTROL Automatische Zuordnung] schnellere Ergebnisse liefern?

Der Vorteil ist klar: Mehr Besucher sehen die Varianten, die am besten funktionieren. Und wenn eine einzelne Variante vorankommt, werden noch mehr Besucher in dieses erfolgreichste Erlebnis umgeleitet, während der Test noch läuft. Diese Methode ist besonders hilfreich, wenn die laufende A/B-Aktivität während eines Kerngeschäftsereignisses wie Feiertag, Produktstart oder Weltnachrichten stattfindet.

## Wie lässt sich [!UICONTROL Automatische Zuordnung] höhere Umsätze erzielen?

[!UICONTROL Automatische Zuordnung] ermittelt den Gewinner schneller als eine manuelle A/B-Aufspaltung und ermöglicht es Ihnen außerdem, diesen Gewinner sofort zu nutzen, um Umsätze aufzufangen, die bei einem herkömmlichen oder manuellen Ansatz verloren gegangen wären. weil [!UICONTROL Automatische Zuordnung] leitet mehr Traffic zum Erlebnis mit der höchsten Konversionsrate weiter. Dies kann Ihren Umsatz steigern, während die Aktivität ausgeführt und gelernt wird.

Im folgenden Beispiel: [!UICONTROL Automatische Zuordnung] während des Tests mehr Umsatz erwirtschaftete, indem mehr Traffic (40 %) in Erlebnis D geleitet wurde, das die höchste Konversionsrate aufwies.

![Die automatische Zuordnung bietet eine höhere Darstellung des Umsatzes](/help/main/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## In welchen Fällen sollte ich bei der manuellen Traffic-Zuordnung bleiben?

Wenn Sie die Leistung jedes Erlebnisses in einer Rangfolge im Vergleich zu den anderen anzeigen müssen, ist ein manueller A/B-Test am besten geeignet. [!UICONTROL Automatische Zuordnung] findet und nutzt die besten Erlebnisse, garantiert jedoch keine Differenzierung zwischen den leistungsschwächeren Erlebnissen. Verwenden Sie die manuelle Traffic-Zuordnung, um vollständig zu kontrollieren, wie viel Besucher-Traffic von den einzelnen Testvarianten angezeigt wird, und um die für Ihr Unternehmen relevanten statistischen Schwellenwerte anzupassen.

## Erste Schritte

Bereit zum Starten Ihrer ersten [!UICONTROL Automatische Zuordnung] Aktivität? [Hier erfahren Sie mehr darüber](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).
