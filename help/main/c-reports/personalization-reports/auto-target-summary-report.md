---
keywords: Berichte;automatisches Targeting;automatisches Targeting;AT;Bericht
description: Erfahren Sie, wie der Zusammenfassungsbericht für automatisches Targeting in Adobe Target interpretiert wird. Von diesem Bericht aus können Sie zu den Berichten Automatisierte Segmente und Wichtige Attribute wechseln.
title: Wie verwende ich den automatischen Targeting- Zusammenfassungsbericht?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 37%

---

# [!UICONTROL Auto-Target Summary report]

Informationen zur Interpretation der [!UICONTROL Auto-Target Summary] in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Es ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/main/c-intro/intro.md#premium).

So zeigen Sie die [!UICONTROL Auto-Target Summary] Berichte an:

1. Klicken Sie auf der Seite [!UICONTROL Activities] auf die gewünschte [!UICONTROL Auto-Target].

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol Filtern ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um die Liste zu filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Reports]** und dann auf das gewünschte Symbol:

   * **[!UICONTROL Table View]** ( ![Tabellenansichtssymbol](/help/main/assets/icons/Table.svg) )
   * **[!UICONTROL Graph View]** ( ![Diagrammansichtssymbol](/help/main/assets/icons/GraphTrend.svg) )
   * **[!UICONTROL Automated Segments]** ( ![Bericht zu automatischen Segmenten](/help/main/assets/icons/AutomatedSegment.svg) )
   * [!UICONTROL Important Attributes]** ( ![Symbol „Wichtige Attribute“](/help/main/assets/icons/ViewList.svg) )

## Tabellenansicht 

Einige Tipps und Überlegungen zur Interpretation Ihrer [!UICONTROL Auto-Target]:

* Die verschiedenen Zeilen in der Tabelle helfen Ihnen, die Performance der Aktivität zu verstehen.

   * Die beiden obersten Zeilen der Tabelle auf der Berichtseite zeigen die Ergebnisse eines A/B-Tests zwischen den Besuchern, die dem Steuerelement zugewiesen wurden (d. h. zufällig bereitgestellte Erlebnisse), und den Besuchern, die dem Personalisierungsalgorithmus zugewiesen wurden. Diese Informationen können verwendet werden, um zu messen, wie der Personalisierungsalgorithmus im Vergleich zur zufällig bereitgestellten Kontrolle ausgeführt wurde.
   * In den restlichen Zeilen werden Ergebnisse auf Erlebnisebene angezeigt. Für jedes Erlebnis gibt es einen Vergleich zwischen der durchschnittlichen Antwort der Besucher, denen dieses Erlebnis als eine zufallsgestützte Kontrolle angezeigt wird, und der durchschnittlichen Antwort der Besucher, denen das Erlebnis mit dem Personalisierungsalgorithmus angezeigt wird.

* Das grüne Häkchensymbol neben den einzelnen Erlebnissen im Bericht gibt an, dass für dieses Erlebnis ein Modell für das personalisierte maschinelle Lernen generiert wurde. Das Uhrensymbol gibt an, dass nicht genügend Traffic verarbeitet wurde, um das Modell zu erstellen.

   * Da das Modell pro Erlebnis erstellt wird, ist es möglich, dass ein Modell für einige Erlebnisse mit einem grünen Häkchen und andere mit einem Uhrensymbol angezeigt werden.
   * In diesem Fall wird den Erlebnissen mit nicht erstellten Modellen zusätzlicher Traffic gesendet, um die Geschwindigkeit der Aktivität zu erhöhen, für die für alle Erlebnisse Modelle erstellt sind.
   * Es müssen mindestens zwei Erlebnisse mit erstellten Modellen (grünes Häkchen) vorhanden sein, damit die Personalisierung gestartet wird.

* Der Vergleich der Konversionsrate von Erlebnis A mit der von Erlebnis B ist in [!UICONTROL Auto-Target] nicht der richtige Vergleich. Es stellt sich die Frage, ob Erlebnis A eine bessere Leistung erzielt, wenn es intelligent bereitgestellt wird, als wenn es auf zufällige Weise bereitgestellt wird (d. h. im Vergleich zur Kontrolle). Marketer sollten die Steigerungen einzelner Erlebnisse vorsichtig interpretieren, da der Personalisierungsalgorithmus versucht, die Optimierung für die Erfolgsmetrik über die gesamte Aktivität und nicht für jedes einzelne Erlebnis vorzunehmen.
* Für Erlebnisse mit der höchsten Steigerung kann davon ausgegangen werden, dass dort die höchste Differenzierung der Population vorliegt. Das heißt, der Algorithmus hat ein Segment gefunden, das dieses bestimmte Erlebnis am meisten mag.
* Die verschiedenen Spalten in der Tabelle zeigen die Anzahl der Besuche, die Konversionsrate, den durchschnittlichen Anstieg und das Konfidenzniveau sowie die Konfidenz. Weitere Informationen finden Sie unter [Statistische Berechnungen in A/B-](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Grafikansicht

Verwenden Sie die beiden Dropdown-Listen, um die gewünschten Metriken, die Zählmethodik und mehr auszuwählen. Weitere Informationen finden [&#x200B; unter &#x200B;](/help/main/c-reports/c-report-settings/report-settings.md) der Berichtseinstellungen:

## Automatisierte Segmente

Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie verschiedene durch die [!DNL Target] Personalisierungsmodelle definierte automatisierte Segmente auf die Angebote/Erlebnisse in der Aktivität reagierten.

Weitere Informationen finden Sie unter [Automated Segments-Bericht](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Dieser Bericht zeigt, wie in verschiedenen Aktivitäten verschiedene Attribute für die Personalisierungsentscheidung des Modells mehr (oder weniger) wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

Weitere Informationen finden Sie unter [Bericht „Wichtige Attribute](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).
