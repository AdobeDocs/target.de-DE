---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; auto-target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen
description: Erfahren Sie, wie verschiedene von Adobe definierte Segmente funktionieren. [!DNL Target] Personalisierungsmodelle reagieren auf Angebote/Erlebnisse in der Aktivität, indem sie den Bericht "Automatisierte Segmente"anzeigen.
title: Was ist der Bericht "Automatisierte Segmente"?
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: 79d51e39b733ee13270f924912251e45c8597917
workflow-type: tm+mt
source-wordcount: '2143'
ht-degree: 74%

---

# ![PREMIUM](/help/main/assets/premium.png) Bericht für automatisierte Segmente

Informationen über [!UICONTROL Automatisierte Segmente] einen der beiden für Benutzer von [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] (AT) Tätigkeiten.

>[!NOTE]
>
>Beachten Sie bei Verwendung von Personalization Insights-Berichten Folgendes:
>
>* AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
>
>* [!UICONTROL Personalization Insights-Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. ] Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
>
>* [!UICONTROL Personalization Insights] Berichte sind nur verfügbar, wenn die Variable [!UICONTROL Primäres Ziel] wird aus dem [!UICONTROL Berichtsmetrik] Dropdown-Liste.
>
>* Personalization Insights-Berichte werden nur in der [Standardumgebung](/help/main/administrating-target/hosts.md) unterstützt.
>
>* [!UICONTROL Personalization Insights] -Berichte werden nur für Aktivitäten generiert, die sich im [!UICONTROL Live] und wurden mindestens 15 Tage lang aktiviert und erhalten Traffic.


Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

## Zugriff auf den Bericht für automatisierte Segmente {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klicken **[!UICONTROL Tätigkeiten]** und klicken Sie dann auf die gewünschte [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) -Aktivität aus der Liste aus.

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie Optionen aus dem [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Eigenschaft], [!UICONTROL Berichtsquelle], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp]und [!UICONTROL Aktivitätsquelle] Dropdown-Listen.

1. Klicken Sie auf **[!UICONTROL Berichte]**.

   Die [Automated Personalization-Zusammenfassung](/help/main/c-reports/personalization-reports/reports-ap.md) oder [Zusammenfassung für automatisches Targeting](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) angezeigt, der Informationen über die Leistung Ihrer Aktivitäten bereitstellt und durch das Symbol des ersten Bildschirms dargestellt wird. Die beiden zusätzlichen Symbole stehen für die beiden Personalization Insights-Berichte: „Automatisierte Segmente“ und „Wichtige Attribute“. Das automatische Targeting verfügt über ein zusätzliches Diagrammsymbol für die grafische Ansicht des [!UICONTROL Zusammenfassung] Bericht.

   ![Personalization Insights-Bericht in Adobe Target](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Der Bericht für [!UICONTROL Automatisierte Segmente] steht erst nach mindestens 15 Tagen nach der Aktivierung Ihrer Aktivität zur Verfügung. Bis dahin können Sie nicht auf diesen Bericht zugreifen und das Symbol für [!UICONTROL „Automatisierte Segmente“] ist ausgegraut. Nach 15 Tagen und sofern ausreichend Personalisierungstraffic in Ihrer Aktivität verfügbar ist, ist der Bericht [!UICONTROL „Automatisierte Segmente“] verfügbar.

1. 15 Tage nach der Aktivierung der Aktivität können Sie auf das Symbol **[!UICONTROL Automatisierte Segmente]** klicken.

   ![Symbol &quot;Automatisierte Segmente&quot;](/help/main/c-reports/assets/icon-automated-sements.png)

1. Wählen Sie den gewünschten Datumsbereich aus.

   Im Gegensatz zu [!UICONTROL Zusammenfassung] Bericht (Leistungsberichte), [!UICONTROL Personalization Insights], einschließlich [!UICONTROL Automatisierte Segmente], ist nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], ausreichend Daten anzusammeln, um zu verhindern, dass Insights aus kurzfristigen Mustern in Ihrer Aktivität abgeleitet werden. Die beiden Entscheidungen, die Sie beim Datumsbereich treffen können, sind „Enddatum“ und „Dauer“. Sie werden feststellen, dass der &quot;Start&quot; ausgegraut ist. Das Startdatum ändert sich automatisch basierend auf Ihrer Auswahl für Enddatum und Dauer.

   ![Kalender in Adobe Target-Bericht](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   Sie können über die Dropdownliste [!UICONTROL „Dauer auswählen“] auf die verfügbaren festen Datumsbereiche zugreifen.

   ![Dropdownliste &quot;Dauer&quot;in Adobe Target](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Überprüfen Sie die Daten des Berichts [!UICONTROL „Automatisierte Segmente“].

   ![Bericht „Automatisierte Segmente“](/help/main/c-reports/assets/automated_segments_report.png)

1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF), um ihn in Excel und anderen Tools zu analysieren.

   >[!NOTE]
   >
   >Der Bericht „Personalization Insights UI“ enthält Informationen zur Auswahl. Der CSV-Download für den Bericht „Automatisierte Segmente“ enthält zusätzliche Details. Der Download des Berichts „Automatisierte Segmente“ enthält im Vergleich zu den Segmenten in der Benutzeroberfläche zusätzliche automatisierte Segmente sowie Informationen zu ihrer Performance in Ihren Angeboten oder Erlebnissen.

## Bericht für automatisierte Segmente interpretieren

Folgende Tabelle enthält Informationen dazu, wie der Bericht zu interpretieren ist, und beschreibt seine Bestandteile:

| Element | Details |
|--- |--- |
| Linker Bereich | Im linken Bereich werden die 20 größten „automatisierten Segmente“ aufgeführt, bestimmt durch die Target-Personalisierungsmodelle für diese Aktivität. Ein „automatisiertes Segment“ ist wie eine Zielgruppe, jedoch wird es statt vom Marketing-Experten durch die Target-Personalisierungsmodelle bestimmt. Jedes automatisierte Segment besteht aus bestimmten Werten (oder Wertbereichen) für spezifische Attribute.<br>Automatisierte Segmente können sich überschneiden. Automatisierte Segmente können über ein, zwei, drei oder vier Attribute definiert werden. Weitere Informationen finden Sie in den Beispielen unten.<br>Weitere Informationen zu den Personalisierungsmodellen von Target finden Sie unter [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). Weitere Informationen zu den Attributmodellen von Target, die für die Erstellung automatisierter Segmente verwendet werden, finden Sie unter [Datenerfassung für die Personalisierungs-Algorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md). |
| Mittiges Diagramm | Die mittleren Diagramme zeigen die Leistung des Aktivitätsinhalts für das hervorgehobene automatisierte Segment an. Wenn Sie im linken Bereich auf ein anderes Segment klicken, wird das mittige Diagramm angepasst. |
| Tortendiagramme | Die Tortendiagramme oben im mittleren Bereich zeigen die Größe des automatisierten Segments sowie die Gesamtzahl personalisierter Besuche in der Aktivität, wie z. B. den Traffic zu dieser Aktivität, der von dem Personalisierungsmodell bereitgestellt wurde. Sie enthalten weder Kontroll-Traffic noch Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird. Die Größe des Segments basiert nur auf personalisierten Besuchen.<br>![Kreisdiagramm](/help/main/c-reports/assets/pie.png) |
| Zweiachsiges Balkendiagramm | Das zweiachsige Balkendiagramm enthält Besuchs- und Konversionsinformationen nach Angebot oder Erlebnis für das spezifische automatisierte Segment. |
| Pinkfarbener Balken | Der pinkfarbene Balken zeigt die Konversionsrate und verwendet die untere Achse des Diagramms. Fahren Sie mit dem Mauszeiger über den Balken, um weitere Informationen anzuzeigen. |
| Blauer Balken | Der blaue Balken zeigt die Anzahl der Besuche und verwendet die obere Achse des Diagramms. Fahren Sie mit dem Mauszeiger über den Balken, um weitere Informationen anzuzeigen. |
| Graue gestrichelte Linie | Die graue gestrichelte Linie zeigt die Konversionsrate für alle personalisierten Besuche in der Aktivität über alle Angebote/Erlebnisse und automatisierten Segmente hinweg. |

**Automatisierte Segmente – Beispiel 1**

Dieses automatisierte Segment wird basierend auf einem Attribut definiert. Bei Besuchern in diesem automatisierten Segment trat die AP-Aktivität an einem Werktag außerhalb der Geschäftszeiten oder am Wochenende auf.

![Beispiel 1 des Berichts &quot;Automatisierte Segmente&quot;](/help/main/c-reports/assets/automated_segment_example_1.png)

**Automatisierte Segmente – Beispiel 2**

Dieses automatisierte Segment wird basierend auf zwei Attributen definiert. Besucher in diesem automatisierten Segment, bei denen diese AP-Aktivität auftrat, wiesen bei ihrem aktuellen Besuch weniger als drei Seitenaufrufe auf und befanden sich zwischen Breitengrad 42,57 und 47,29 (also ungefähr zwischen New Hampshire/Oregon und Washington/Maine für ein US-ansässiges Unternehmen).

![Beispiel 2 des Berichts &quot;Automatisierte Segmente&quot;](/help/main/c-reports/assets/automated_segment_example_2.png)

## Häufig gestellte Fragen zu automatisierten Segmenten {#section_740910A52FA646B4AC9452F98C2F5719}

**Es sind noch keine Personalization Insights-Berichte für meine Aktivität verfügbar. Woran liegt das?**

Es kann verschiedene Gründe dafür geben, dass die [!UICONTROL Personalization Insights]-Berichte noch nicht für Ihre Aktivität verfügbar sind:

* 15 Tage sind seit der Aktivierung der Aktivität noch nicht vergangen. Die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ sind erst 15 Tage nach der Aktivierung der Aktivität verfügbar. Bis dahin können Sie nicht auf diese Berichte zugreifen und die Symbole für „Automatisierte Segmente“ und „Wichtige Attribute“ sind ausgegraut.
* Ihre Aktivität bietet nicht ausreichend Traffic im angegebenen Zeitraum. Nach 15 Tagen und sofern ausreichend Personalisierungstraffic in Ihrer Aktivität verfügbar ist, um die Personalisierungsmodelle zu erstellen, sind die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ verfügbar.
* Ihre Aktivität verfügt über ein Ziel zur Umsatzoptimierung. Zurzeit [!UICONTROL Personalization Insights] ist nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Adobe wird in einer zukünftigen Version Unterstützung für Zielaktivitäten zur Umsatzoptimierung hinzufügen.

**Was ist ein Attribut?**

Ein Attribut ist eine Information zu einem Besucher oder seinem spezifischen Besuch, die von den Personalisierungsalgorithmen verwendet wird, um die Traffic-Personalisierung anzupassen. Bei einem Attribut kann es sich beispielsweise um den Browsertyp, den Standort, die Uhrzeit des Besuchs usw. handeln.

Weitere Informationen zu den Attributen, die [!DNL Target] in seinen Personalisierungsmodellen nutzt, finden Sie unter [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Weitere Informationen zum Hochladen neuer Attribute in Target zur Verwendung in den Target-Personalisierungsmodellen finden Sie unter [Verfahren für die Datenübernahme in Target](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/){target=_blank}.

**Was ist ein automatisiertes Segment?**

Ein „automatisiertes Segment“ ist wie eine Zielgruppe, jedoch wird es statt vom Marketing-Experten durch die Target-Personalisierungsmodelle bestimmt.

Ein automatisiertes Segment besteht aus bestimmten Werten (oder Wertbereichen) für spezifische Attribute. Ein Beispiel für automatisierte Segmente finden Sie oben in Schritt 5. Segmente können sich überschneiden.

Weitere Informationen zum Random-Forest-Personalisierungsalgorithmus, der die Grundlage für die Target-Personalisierungsmodelle bildet, finden Sie unter  [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Wodurch wird die Reihenfolge der automatisierten Segmente festgelegt?**

Über eine Bewertung für jedes Segment, die auf seiner Größe und seiner Performance bezüglich des Inhalts in Ihrer Aktivität basiert. Die Kombination dieser Eingaben bestimmt die Reihenfolge der automatisierten Segmente. So werden beispielsweise größere Segmente, die bei der Interaktion mit den verschiedenen Inhalten größere Unterschiede aufweisen, weiter oben in der Segmentliste angezeigt.

**Warum werden nur manche meiner Angebote/Erlebnisse im Bericht „Automatisierte Segmente“ angezeigt?**

AP- und AT-Aktivitäten erstellen ein Modell pro Angebot (bei AP) bzw. pro Erlebnis (bei AT). Mit diesen beiden Modellen stellen die Aktivitäten personalisierten Traffic bereit und schaffen Ihre [!UICONTROL Personalization Insights]. Wenn nicht alle Angebote/Erlebnisse in [!UICONTROL Personalization Insights]ist es wahrscheinlich, dass Sie keine Modelle für diese spezifischen Angebote/Erlebnisse erstellt haben. Sie können die [!UICONTROL Zusammenfassung] und überprüfen Sie, ob neben diesem Angebot/Erlebnis ein Uhrensymbol vorhanden ist. Dieses Symbol zeigt an, dass noch keine Modelle für dieses Angebot/Erlebnis erstellt wurden.

**Warum erhalten in einem bestimmten automatisierten Segment manche Angebote/Erlebnisse mit einer geringeren Konversionsrate mehr Traffic als andere Angebote/Erlebnisse?**

Es kann verschiedene Gründe dafür geben, dass Ihnen in einem automatisierten Segment mehr Besuche für Angebote oder Erlebnisse mit einer geringeren Konversionsrate angezeigt werden:

* Geringe Anzahl von Aufrufen für manche oder alle Angebote/Erlebnisse eines bestimmten automatisierten Segments.
* Aktivitäten mit geringerem Volumen, in denen für Angebote/Erlebnisse noch keine Modelle erstellt wurden oder in denen Modelle für manche Angebote/Erlebnisse schneller erstellt werden als für andere
* Targeting-Regeln in einem bestimmten Angebot, die einschränken, welchen Besuchern welche Angebote/Erlebnisse angezeigt werden

**Entsprechen die Informationen in den Berichten [!UICONTROL „Automatisierte Segmente“] und [!UICONTROL „Wichtige Attribute“] den Informationen im CSV-Download?**

Nein. Der UI-Bericht enthält ausgewählte Informationen. Der CSV-Download enthält zusätzliche Details. Der Download des Insights-Berichts „Automatisierte Segmente“ enthält im Vergleich zu den Segmenten in der Benutzeroberfläche zusätzliche automatisierte Segmente sowie Informationen zu ihrer Performance in Ihren Angeboten oder Erlebnissen. Der Bericht „Wichtige Attribute“ enthält die 100 wichtigsten Besucherattribute und ihre relative Wichtigkeit, während in der UI nur die 10 wichtigsten Besucherattribute angezeigt werden.

**Kann ich [!UICONTROL Personalization Insights] für einen benutzerspezifischen Datumsbereich anzeigen?**

Berichte zu Personalization Insights (beides [!UICONTROL Automatisierte Segmente] und [!UICONTROL Wichtige Attribute]) ist nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], ausreichend Daten anzusammeln, um zu verhindern, dass Insights aus kurzfristigen Mustern in Ihrer Aktivität abgeleitet werden. Sie können diese Zeiträume mit einem beliebigen Enddatum festlegen (sofern hierfür ausreichend Daten in der Aktivität vorhanden sind).

**Wie wird [!UICONTROL Personalization Insights] erstellt?**

[!UICONTROL Personalization Insights] wird mithilfe der patentierten Adobe-Technik namens MAGIX (Model Agnostic Globally Interpretable Explanations) erstellt. Weitere Informationen zu MAGIX finden Sie im veröffentlichten Beitrag des Adobe-Forschungsteams auf der [Website &quot;arXiv.org&quot;](https://arxiv.org/abs/1706.07160).

**Warum stimmt der Gesamtwert der Besuchertraffic-Daten im Bericht [!UICONTROL „Automatisierte Segmente“] nicht mit dem AP- oder AT-Zusammenfassungs- bzw. -Performancebericht überein?**

Die [!UICONTROL Personalization Insights] Berichte umfassen nur Besucher, die einen von den Target-Personalisierungsmodellen ausgewählten Inhalt gesehen haben (d. h. keinen Kontroll-Traffic oder Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird). Dieser Traffic-Typ wird als &quot;personalisierter&quot; Traffic bezeichnet. Der zusammenfassende Leistungsbericht in AP/AT umfasst Kontroll- und &quot;zielgerichtete&quot;Traffic. Gezielter Traffic beinhaltet Personalisierungs-Traffic, Traffic, der mithilfe des Gesamt-Gewinnermodells bereitgestellt wird, sowie zufällig ausgewählten Traffic, der zum Lernen eingesetzt wird.

**Schließen sich automatisierte Segmente gegenseitig aus?**

Nein, automatisierte Segmente können sich überschneiden.

**Ist [!UICONTROL Personalization Insights] für umsatzbasierte Modellierungsziele/Primärziele verfügbar?**

Zum jetzigen Zeitpunkt ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Adobe wird in einer zukünftigen Version Unterstützung für Zielaktivitäten zur Umsatzoptimierung hinzufügen.

**Wozu kann ich die Informationen in Personalization Insights nutzen?**

* Entdecken Sie neue Zielgruppen für das Targeting: Wenn Ihnen ein bestimmtes automatisiertes Segment angezeigt wird, das sich gut bewährt hat, sollten Sie erwägen, eine Zielgruppe zu erstellen, damit Sie dieses Segment in anderen Berichten wiederverwenden können.
* Testen Sie Ihre Hypothesen dahingehend, welcher Besuchertyp auf welche Ihrer Erlebnisse reagiert.
* Ermitteln Sie, welche Inhalte für welche Besuchertypen funktionieren: Welche Angebote waren bei welchen Besuchern erfolgreich?
* Ermitteln Sie Gründe für Inhalte mit schlechter Performance.
* Finden Sie heraus, welche Attribute am wichtigsten für das Lernen des Modells waren.
* Ermitteln Sie, welche Attribute in den Personalisierungsmodellen eingesetzt werden und wie wichtig sie sind.
* Finden Sie Möglichkeiten für zusätzliche Datenpunkte, die Sie an Target übergeben können, um die Personalisierung weiter zu optimieren.

**Gibt es eine Logik bei der Reihenfolge, in der Attribute in einer Segmentkarte angezeigt werden?**

Nein, die Reihenfolge der Karten basiert nur auf einer Rangfolge, die oben beschrieben wurde. Die Reihenfolge der Attribute innerhalb einer Karte basiert auf keiner Logik.
