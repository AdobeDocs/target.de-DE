---
keywords: Berichte;automatisches Targeting;automatisches Targeting;AT;Bericht
description: Erfahren Sie, wie der Zusammenfassungsbericht für automatisches Targeting in Adobe Target interpretiert wird. Von diesem Bericht aus können Sie zu den Berichten Automatisierte Segmente und Wichtige Attribute wechseln.
title: Wie verwende ich den automatischen Targeting- Zusammenfassungsbericht?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 52%

---

# AT (Automatisches Targeting)-Zusammenfassungsbericht

Informationen zur Interpretation der [!UICONTROL Auto-Target Summary] in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Es ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/main/c-intro/intro.md#premium).

So zeigen Sie die [!UICONTROL Auto-Target Summary] Berichte an:

1. Klicken Sie auf der Seite [!UICONTROL Activities] auf die gewünschte [!UICONTROL Auto-Target].

   Wenn Sie über viele Aktivitäten verfügen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf die Registerkarte [!UICONTROL Reports] und dann auf das gewünschte Symbol:

   * Tabellenansicht 
   * Grafikansicht
   * Automatisierte Segmente
   * Wichtige Attribute

## Tabellenansicht 

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in [!UICONTROL Table View] aussieht, wenn der Bericht einer [!UICONTROL Auto-Target] Aktivität angezeigt wird:

![Automatisches Targeting - Tabellenansichtsbericht](/help/main/c-reports/assets/at-table-view.png)

Einige Tipps und Überlegungen zur Interpretation Ihrer [!UICONTROL Auto-Target]:

* Die verschiedenen Zeilen in der Tabelle helfen Ihnen, die Performance der Aktivität zu verstehen.

   * In den obersten zwei Zeilen in der Tabelle auf der Berichtsseite werden die Ergebnisse eines A/B-Tests zwischen den der Kontrolle (d. h. einem zufällig bereitgestellten Erlebnis) zugewiesenen Besuchern und den dem Personalisierungsalgorithmus zugewiesenen Besuchern angezeigt. Anhand dieser Informationen kann die Leistung des Personalisierungsalgorithmus im Vergleich zur zufallsgestützten Kontrolle gemessen werden.
   * In den restlichen Zeilen werden Ergebnisse auf Erlebnisebene angezeigt. Für jedes Erlebnis gibt es einen Vergleich zwischen der durchschnittlichen Antwort der Besucher, denen dieses Erlebnis als eine zufallsgestützte Kontrolle angezeigt wird, und der durchschnittlichen Antwort der Besucher, denen das Erlebnis mit dem Personalisierungsalgorithmus angezeigt wird.

* Das grüne Häkchensymbol neben den einzelnen Erlebnissen im Bericht gibt an, dass für dieses Erlebnis ein Modell für das personalisierte maschinelle Lernen generiert wurde. Das Uhrensymbol gibt an, dass nicht genügend Traffic verarbeitet wurde, um das Modell zu erstellen.

   * Da das Modell pro Erlebnis erstellt wird, ist es möglich, dass ein Modell für einige Erlebnisse mit einem grünen Häkchen und andere mit einem Uhrensymbol angezeigt werden.
   * In diesem Fall wird den Erlebnissen mit nicht erstellten Modellen zusätzlicher Traffic gesendet, um die Geschwindigkeit der Aktivität zu erhöhen, für die für alle Erlebnisse Modelle erstellt sind.
   * Es müssen mindestens zwei Erlebnisse mit erstellten Modellen (grünes Häkchen) vorhanden sein, damit die Personalisierung beginnt.

* Der Vergleich der Konversionsrate von Erlebnis A mit der von Erlebnis B ist in [!UICONTROL Auto-Target] nicht der richtige Vergleich. Es stellt sich die Frage, ob Erlebnis A eine bessere Leistung erzielt, wenn es intelligent bereitgestellt wird, als wenn es auf zufällige Weise bereitgestellt wird (d. h. im Vergleich zur Kontrolle). Marketer sollten die Steigerungen einzelner Erlebnisse vorsichtig interpretieren, da der Personalisierungsalgorithmus versucht, die Optimierung für die Erfolgsmetrik über die gesamte Aktivität und nicht für jedes einzelne Erlebnis vorzunehmen.
* Für Erlebnisse mit der höchsten Steigerung kann davon ausgegangen werden, dass dort die höchste Differenzierung der Population vorliegt. Das heißt, dass der Algorithmus ein Segment gefunden hat, dem dieses Erlebnis am besten gefällt.
* Die verschiedenen Spalten in der Tabelle zeigen die Anzahl der Besuche, die Konversionsrate, den durchschnittlichen Anstieg und das Konfidenzniveau sowie die Konfidenz. Weitere Informationen finden Sie unter [Statistische Berechnungen in A/B-](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Grafikansicht

Die folgende Abbildung zeigt, wie ein typischer Zusammenfassungsbericht in [!UICONTROL Graph View] aussieht, wenn der Bericht einer [!UICONTROL Auto-Target] Aktivität angezeigt wird:

![Automatisches Targeting(AT)-Diagrammansichtsbericht](/help/main/c-reports/assets/at-graph-view.png)

Wie unten gezeigt, können Sie die beiden Dropdown-Listen verwenden, um die gewünschten Metriken, die Zählmethodik und mehr auszuwählen. Weitere Informationen finden [ unter ](/help/main/c-reports/c-report-settings/report-settings.md) der Berichtseinstellungen:

![Automatisches Targeting(AT)-Diagrammansichtsbericht](/help/main/c-reports/assets/at-graph-view-2.png)

## Automatisierte Segmente

Klicken Sie auf das Symbol [!UICONTROL Automated Segments] . Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Symbol für automatisierte Segmente](/help/main/c-reports/assets/icon-automated-sements.png)

Weitere Informationen finden Sie unter [Bericht zu automatisierten Segmenten](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf das Symbol [!UICONTROL Important Attributes] . Dieser Bericht zeigt, wie in verschiedenen Aktivitäten verschiedene Attribute für die Personalisierungsentscheidung des Modells mehr (oder weniger) wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol für wichtige Attribute](/help/main/c-reports/assets/icon-important-attributes.png)

Weitere Informationen finden Sie unter [Bericht zu wichtigen Attributen](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).
