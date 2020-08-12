---
keywords: reports;auto-target;auto target;AT
description: Informationen zur Interpretation des AT-Zusammenfassungsberichts.
title: AT (Automatisches Targeting)-Zusammenfassungsbericht
feature: null
subtopic: Multivariate Test
topic: Standard
uuid: a30fa886-e8df-408f-bbc9-11a917a592d8
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 65%

---


# AT (Automatisches Targeting)-Zusammenfassungsbericht{#auto-target-summary-report}

Informationen zur Interpretation der Zusammenfassungsberichte für die automatische Zielgruppe.

To display the Auto-Target Summary reports:

1. From the [!UICONTROL Activities] page, click the desired Auto-Target activity.

   If you have many activities, you can filter the list by selecting options from the Type, Status, Property, Reporting Source, Experience Composer, Metrics Type, and Activity Source drop-down lists.

1. Klicken Sie auf die Registerkarte [!UICONTROL Berichte].

## Tabellenansicht 

The following illustration shows what a typical summary report looks like in &quot;table view&#39; when using Auto-Target:

![Bericht zur automatischen Zielgruppe der Ansicht von Tabellen](/help/c-reports/assets/at-table-view.png)

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
* The various columns in the table show the number of visits, conversion rate, average lift and confidence level, and confidence. Weitere Informationen finden Sie unter [Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md).

## Grafikansicht

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in der &quot;Ansicht von Diagrammen&quot;bei Verwendung der automatischen Zielgruppe aussieht:

![Bericht zur Ansicht von Diagrammen mit automatischer Zielgruppe](/help/c-reports/assets/at-graph-view.png)

As shown below, you can use the two drop-down lists to choose the desired metrics, counting methodology, and more. Weitere Informationen finden Sie unter Übersicht über die [Berichtseinstellungen](/help/c-reports/c-report-settings/report-settings.md) :

![Bericht zur Ansicht von Diagrammen mit automatischer Zielgruppe](/help/c-reports/assets/at-graph-view-2.png)

## Automatisierte Segmente

Klicken Sie auf das Symbol Automatisierte Segmente. Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebot/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Automated segments icon](/help/c-reports/assets/icon-automated-sements.png)

Weitere Informationen finden Sie unter Bericht [&quot;Automatisierte Segmente&quot;](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf das Symbol Wichtige Attribute. This report shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol &quot;Wichtige Attribute&quot;](/help/c-reports/assets/icon-important-attributes.png)

Weitere Informationen finden Sie unter Bericht &quot; [Wichtige Attribute&quot;](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).
