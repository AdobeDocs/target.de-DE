---
keywords: reports;auto-target;auto target;AT
description: Informationen zur Interpretation des AT-Zusammenfassungsberichts.
title: AT (Automatisches Targeting)-Zusammenfassungsbericht
subtopic: Multivariate Test
topic: Standard
uuid: a30fa886-e8df-408f-bbc9-11a917a592d8
translation-type: tm+mt
source-git-commit: 3faba3d3158bed69ae5d756fb70c97d17110c1d8

---


# AT (Automatisches Targeting)-Zusammenfassungsbericht{#auto-target-summary-report}

Informationen zur Interpretation der Berichte zur Auto-Target-Zusammenfassung.

So zeigen Sie die Berichte zur AutoTarget-Zusammenfassung an:

1. Klicken Sie auf der Seite &quot; [!UICONTROL Aktivitäten] &quot;auf die gewünschte Auto-Target-Aktivität.

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten Typ, Status, Eigenschaft, Berichtsquelle, Experience Composer, Metriktyp und Aktivitätsquelle auswählen.

1. Klicken Sie auf die Registerkarte [!UICONTROL Berichte].

## Tabellenansicht 

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in der &quot;Tabellenansicht&quot;bei Verwendung des automatischen Targeting aussieht:

![Bericht zur automatischen Zielgruppenansicht](/help/c-reports/assets/at-table-view.png)

Im Folgenden finden Sie einige Tipps und Hinweise für das Interpretieren Ihrer Berichte vom Typ „Automatisches Targeting“:

* Die einzelnen Zeilen der Tabelle zeigen die Leistung der Aktivität.

   * In den obersten zwei Zeilen in der Tabelle auf der Berichtsseite werden die Ergebnisse eines A/B-Tests zwischen den der Kontrolle (d. h. einem zufällig bereitgestellten Erlebnis) zugewiesenen Besuchern und den dem Personalisierungsalgorithmus zugewiesenen Besuchern angezeigt. Anhand dieser Informationen kann die Leistung des Personalisierungsalgorithmus im Vergleich zur zufallsgestützten Kontrolle gemessen werden.
   * In den restlichen Zeilen werden Ergebnisse auf Erlebnisebene angezeigt. Für jedes Erlebnis gibt es einen Vergleich zwischen der durchschnittlichen Antwort der Besucher, denen dieses Erlebnis als eine zufallsgestützte Kontrolle angezeigt wird, und der durchschnittlichen Antwort der Besucher, denen das Erlebnis mit dem Personalisierungsalgorithmus angezeigt wird.

* Das grüne Häkchensymbol neben den einzelnen Erlebnissen im Bericht gibt an, dass für dieses Erlebnis ein Modell für das personalisierte maschinelle Lernen generiert wurde. Das Uhrensymbol gibt an, dass nicht genügend Traffic verarbeitet wurde, um das Modell zu erstellen.

   * Da das Modell pro Erlebnis erstellt wird, ist es möglich, dass ein Modell für einige Erlebnisse mit einem grünen Häkchen und andere mit einem Uhrensymbol angezeigt werden.
   * In diesem Fall wird den Erlebnissen mit nicht erstellten Modellen zusätzlicher Traffic gesendet, um die Geschwindigkeit der Aktivität zu erhöhen, für die für alle Erlebnisse Modelle erstellt sind.
   * Es müssen mindestens zwei Erlebnisse mit erstellten Modellen (grünes Häkchen) vorhanden sein, damit die Personalisierung beginnt.

* Ein Vergleich der Konversionsrate von Erlebnis A mit der von Erlebnis B ist beim automatischen Targeting kein passender Vergleich. Es stellt sich die Frage, ob Erlebnis A eine bessere Leistung erzielt, wenn es intelligent bereitgestellt wird, als wenn es auf zufällige Weise bereitgestellt wird (d. h. im Vergleich zur Kontrolle). Marketer sollten die Steigerungen einzelner Erlebnisse vorsichtig interpretieren, da der Personalisierungsalgorithmus versucht, die Optimierung für die Erfolgsmetrik über die gesamte Aktivität und nicht für jedes einzelne Erlebnis vorzunehmen.
* Für Erlebnisse mit der höchsten Steigerung kann davon ausgegangen werden, dass dort die höchste Differenzierung der Population vorliegt. Das heißt, dass der Algorithmus ein Segment gefunden hat, dem dieses Erlebnis am besten gefällt.
* Die verschiedenen Spalten in der Tabelle zeigen die Anzahl der Besuche, die Konversionsrate, die durchschnittliche Steigerung und das Konfidenzniveau sowie die Konfidenz an. Weitere Informationen finden Sie unter [Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md).

## Grafikansicht

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in der &quot;Diagrammansicht&quot;bei Verwendung des automatischen Targeting aussieht:

![Bericht zur automatischen Targeting-Diagrammansicht](/help/c-reports/assets/at-graph-view.png)

Wie unten gezeigt, können Sie die beiden Dropdown-Listen verwenden, um die gewünschten Metriken, Zählmethodiken und mehr auszuwählen. Weitere Informationen finden Sie unter Übersicht über die [Berichtseinstellungen](/help/c-reports/c-report-settings/report-settings.md) :

![Bericht zur automatischen Targeting-Diagrammansicht](/help/c-reports/assets/at-graph-view-2.png)

## Automatisierte Segmente

Klicken Sie auf das Symbol Automatisierte Segmente. Dieser Bericht zeigt, wie unterschiedliche Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Symbol für automatisierte Segmente](/help/c-reports/assets/icon-automated-sements.png)

Weitere Informationen finden Sie unter Bericht [&quot;Automatisierte Segmente&quot;](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf das Symbol Wichtige Attribute. Dieser Bericht zeigt, wie verschiedene Attribute bei verschiedenen Aktivitäten wichtiger (oder weniger) für die Art und Weise sind, wie das Modell sich für die Personalisierung entscheidet. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol &quot;Wichtige Attribute&quot;](/help/c-reports/assets/icon-important-attributes.png)

Weitere Informationen finden Sie unter Bericht &quot; [Wichtige Attribute&quot;](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).
