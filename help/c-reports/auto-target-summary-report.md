---
keywords: reports;auto-target;auto target;AT;report
description: Informationen zur Interpretation des Zusammenfassungsberichts für die automatische Zielgruppe in Adobe Target.
title: AT (Automatisches Targeting)-Zusammenfassungsbericht
feature: reports
subtopic: Multivariate Test
topic: Standard
uuid: a30fa886-e8df-408f-bbc9-11a917a592d8
translation-type: tm+mt
source-git-commit: 56c77e1a7b5dd4e64f59b0416a16c3039a649ba3
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 57%

---


# ![PREMIUM](/help/assets/premium.png) Auto-Zielgruppe - Zusammenfassungsbericht{#auto-target-summary-report}

Information about how to interpret the [!UICONTROL Auto-Target Summary] reports in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Sie ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/c-intro/intro.md#premium).

So zeigen Sie die Berichte zur [!UICONTROL Auto-Zielgruppe-Zusammenfassung] an:

1. Klicken Sie auf der Seite &quot; [!UICONTROL Aktivitäten] &quot;auf die gewünschte Aktivität für die [!UICONTROL automatische Zielgruppe] .

   If you have many activities, you can filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], and [!UICONTROL Activity Source] drop-down lists.

1. Klicken Sie auf die Registerkarte [!UICONTROL Berichte] und dann auf das gewünschte Symbol:

   * Tabellenansicht 
   * Grafikansicht
   * Automatisierte Segmente
   * Wichtige Attribute

## Tabellenansicht 

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in der [!UICONTROL Ansicht] &quot;Tabelle&quot;aussieht, wenn der Bericht einer Aktivität der [!UICONTROL automatischen Zielgruppe] angezeigt wird:

![Bericht zur automatischen Zielgruppe der Ansicht von Tabellen](/help/c-reports/assets/at-table-view.png)

Some tips and considerations as you interpret your [!UICONTROL Auto-Target] reports:

* Die verschiedenen Tabellenzeilen helfen Ihnen, die Performance der Aktivität zu verstehen.

   * In den obersten zwei Zeilen in der Tabelle auf der Berichtsseite werden die Ergebnisse eines A/B-Tests zwischen den der Kontrolle (d. h. einem zufällig bereitgestellten Erlebnis) zugewiesenen Besuchern und den dem Personalisierungsalgorithmus zugewiesenen Besuchern angezeigt. Anhand dieser Informationen kann die Leistung des Personalisierungsalgorithmus im Vergleich zur zufallsgestützten Kontrolle gemessen werden.
   * In den restlichen Zeilen werden Ergebnisse auf Erlebnisebene angezeigt. Für jedes Erlebnis gibt es einen Vergleich zwischen der durchschnittlichen Antwort der Besucher, denen dieses Erlebnis als eine zufallsgestützte Kontrolle angezeigt wird, und der durchschnittlichen Antwort der Besucher, denen das Erlebnis mit dem Personalisierungsalgorithmus angezeigt wird.

* Das grüne Häkchensymbol neben den einzelnen Erlebnissen im Bericht gibt an, dass für dieses Erlebnis ein Modell für das personalisierte maschinelle Lernen generiert wurde. Das Uhrensymbol gibt an, dass nicht genügend Traffic verarbeitet wurde, um das Modell zu erstellen.

   * Da das Modell pro Erlebnis erstellt wird, ist es möglich, dass ein Modell für einige Erlebnisse mit einem grünen Häkchen und andere mit einem Uhrensymbol angezeigt werden.
   * In diesem Fall wird den Erlebnissen mit nicht erstellten Modellen zusätzlicher Traffic gesendet, um die Geschwindigkeit der Aktivität zu erhöhen, für die für alle Erlebnisse Modelle erstellt sind.
   * Es müssen mindestens zwei Erlebnisse mit erstellten Modellen (grünes Häkchen) vorhanden sein, damit die Personalisierung beginnt.

* Comparing the conversion rate of experience A with that of experience B is not the right comparison in [!UICONTROL Auto-Target]. Es stellt sich die Frage, ob Erlebnis A eine bessere Leistung erzielt, wenn es intelligent bereitgestellt wird, als wenn es auf zufällige Weise bereitgestellt wird (d. h. im Vergleich zur Kontrolle). Marketer sollten die Steigerungen einzelner Erlebnisse vorsichtig interpretieren, da der Personalisierungsalgorithmus versucht, die Optimierung für die Erfolgsmetrik über die gesamte Aktivität und nicht für jedes einzelne Erlebnis vorzunehmen.
* Für Erlebnisse mit der höchsten Steigerung kann davon ausgegangen werden, dass dort die höchste Differenzierung der Population vorliegt. Das heißt, dass der Algorithmus ein Segment gefunden hat, dem dieses Erlebnis am besten gefällt.
* Die verschiedenen Tabellenspalten zeigen die Anzahl der Besuche, die Konversionsrat, die durchschnittliche Steigerung und das Konfidenzniveau sowie die Konfidenz an. Weitere Informationen finden Sie unter [Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall](/help/c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md).

## Grafikansicht

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in der [!UICONTROL Graph-Ansicht] aussieht, wenn Sie den Bericht einer Aktivität zur [!UICONTROL automatischen Zielgruppe] anzeigen:

![Bericht zur Ansicht von Diagrammen mit automatischer Zielgruppe](/help/c-reports/assets/at-graph-view.png)

Wie unten gezeigt, können Sie die beiden Dropdown-Listen verwenden, um die gewünschten Metriken, Zählmethodiken und mehr auszuwählen. Weitere Informationen finden Sie unter Übersicht über die [Berichtseinstellungen](/help/c-reports/c-report-settings/report-settings.md) :

![Bericht zur Ansicht von Diagrammen mit automatischer Zielgruppe](/help/c-reports/assets/at-graph-view-2.png)

## Automatisierte Segmente

Klicken Sie auf das Symbol [!UICONTROL Automatisierte Segmente] . Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebot/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Symbol für automatisierte Segmente](/help/c-reports/assets/icon-automated-sements.png)

Weitere Informationen finden Sie unter Bericht [&quot;Automatisierte Segmente&quot;](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf das Symbol [!UICONTROL Wichtige Attribute] . Dieser Bericht zeigt, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Art und Weise sind, wie das Modell sich für die Personalisierung entscheidet. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol &quot;Wichtige Attribute&quot;](/help/c-reports/assets/icon-important-attributes.png)

Weitere Informationen finden Sie unter Bericht &quot; [Wichtige Attribute&quot;](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).
