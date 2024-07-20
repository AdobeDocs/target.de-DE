---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; auto-target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen
description: Erfahren Sie, wie verschiedene durch Adobe [!DNL Target] Personalisierungsmodelle definierte Segmente auf Angebote/Erlebnisse in der Aktivität reagieren, indem Sie den Bericht "Automatisierte Segmente"anzeigen.
title: Was ist der Bericht "Automatisierte Segmente"?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 60%

---

# Bericht [!UICONTROL Automated Segments]

Informationen zum Bericht [!UICONTROL Automated Segments], einem der beiden für Benutzer der Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] (AT) verfügbaren speziellen Berichte.

>[!NOTE]
>
>Beachten Sie bei der Verwendung von Personalization Insights-Berichten Folgendes:
>
>* AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
>
>* [!UICONTROL Personalization Insights] -Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
>
>* [!UICONTROL Personalization Insights] -Berichte sind nur verfügbar, wenn die [!UICONTROL Primary Goal] aus der Dropdownliste [!UICONTROL Report Metric] ausgewählt ist.
>
>* [!UICONTROL Personalization Insights] -Berichte werden nur in der [Standardumgebung](/help/main/administrating-target/hosts.md) unterstützt.
>
>* [!UICONTROL Personalization Insights] -Berichte werden nur für Aktivitäten generiert, die sich im Status [!UICONTROL Live] befinden und die mindestens 15 Tage lang aktiviert wurden und Traffic erhalten.

Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

## Zugriff auf den Bericht &quot;Automatisierte Segmente&quot; {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität vom Typ [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) .

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf **[!UICONTROL Reports]**.

   Der Bericht [Automated Personalization-Zusammenfassung](/help/main/c-reports/personalization-reports/reports-ap.md) oder [Zusammenfassung des automatischen Targetings](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) wird angezeigt. Er enthält Informationen zur Performance Ihrer Aktivitäten, dargestellt durch das erste Bildschirmsymbol. Die beiden zusätzlichen Symbole stehen für die beiden Personalization Insights-Berichte: „Automatisierte Segmente“ und „Wichtige Attribute“. Das automatische Targeting verfügt über ein zusätzliches Diagrammsymbol für die grafische Ansicht des Berichts [!UICONTROL Summary] .

   ![Personalization Insights-Bericht in Adobe Target](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Der Bericht [!UICONTROL Automated Segments] steht erst nach mindestens 15 Tagen nach der Aktivierung Ihrer Aktivität zur Verfügung. In diesem Anfangszeitraum können Sie nicht auf diesen Bericht zugreifen oder auf das Symbol [!UICONTROL Automated Segments] klicken. Nach 15 Tagen und sofern ausreichend personalisierter Traffic in Ihrer Aktivität verfügbar ist, ist der Bericht [!UICONTROL Automated Segments] verfügbar.

1. 15 Tage nach der Aktivierung der Aktivität können Sie auf das Symbol **[!UICONTROL Automated Segments]** klicken.

   ![Symbol &quot;Automatisierte Segmente&quot;](/help/main/c-reports/assets/icon-automated-sements.png)

1. Wählen Sie den gewünschten Datumsbereich aus.

   Im Gegensatz zum [!UICONTROL Summary] -Bericht (Leistungsberichte) ist [!UICONTROL Personalization Insights], einschließlich [!UICONTROL Automated Segments], nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], einen ausreichend großen Datenbereich zu verwenden, um die Wahrscheinlichkeit zu verringern, dass Sie Einblicke aus einem kurzlebigen Muster in Ihrer Aktivität gewinnen. Die beiden Entscheidungen, die Sie beim Datumsbereich treffen können, sind „Enddatum“ und „Dauer“. Sie werden feststellen, dass der &quot;Start&quot; ausgegraut ist. Das Startdatum ändert sich automatisch basierend auf Ihrer Auswahl für Enddatum und Dauer.

   ![Kalender im Adobe Target-Bericht](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   Sie können über die Dropdownliste [!UICONTROL Choose Duration] auf die verfügbaren festen Datumsbereiche zugreifen.

   ![Dropdown-Liste &quot;Dauer&quot;in Adobe Target](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Überprüfen Sie die [!UICONTROL Automated Segments] -Berichtsdaten.

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
| Tortendiagramme | Die Tortendiagramme oben im mittleren Bereich zeigen die Größe des automatisierten Segments sowie die Gesamtzahl personalisierter Besuche in der Aktivität, wie z. B. den Traffic zu dieser Aktivität, der von dem Personalisierungsmodell bereitgestellt wurde. Sie enthalten weder Kontroll-Traffic noch Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird. Die Größe des Segments basiert nur auf personalisierten Besuchen.<br>![Tortendiagramm](/help/main/c-reports/assets/pie.png) |
| Zweiachsiges Balkendiagramm | Das zweiachsige Balkendiagramm enthält Besuchs- und Konversionsinformationen nach Angebot oder Erlebnis für das spezifische automatisierte Segment. |
| Pinkfarbener Balken | Der pinkfarbene Balken zeigt die Konversionsrate und verwendet die untere Achse des Diagramms. Fahren Sie mit dem Mauszeiger über den Balken, um weitere Informationen anzuzeigen. |
| Blauer Balken | Der blaue Balken zeigt die Anzahl der Besuche und verwendet die obere Achse des Diagramms. Fahren Sie mit dem Mauszeiger über den Balken, um weitere Informationen anzuzeigen. |
| Graue gestrichelte Linie | Die graue gestrichelte Linie zeigt die Konversionsrate für alle personalisierten Besuche in der Aktivität über alle Angebote/Erlebnisse und automatisierten Segmente hinweg. |

**Automatisierte Segmente – Beispiel 1**

Dieses automatisierte Segment wird basierend auf einem Attribut definiert. Bei Besuchern in diesem automatisierten Segment trat die AP-Aktivität an einem Werktag außerhalb der Geschäftszeiten oder am Wochenende auf.

![Beispiel des Berichts &quot;Automatisierte Segmente&quot; 1](/help/main/c-reports/assets/automated_segment_example_1.png)

**Automatisierte Segmente – Beispiel 2**

Dieses automatisierte Segment wird basierend auf zwei Attributen definiert. Besucher in diesem automatisierten Segment, bei denen diese AP-Aktivität auftrat, wiesen bei ihrem aktuellen Besuch weniger als drei Seitenaufrufe auf und befanden sich zwischen Breitengrad 42,57 und 47,29 (also ungefähr zwischen New Hampshire/Oregon und Washington/Maine für ein US-ansässiges Unternehmen).

![Beispiel des Berichts &quot;Automatisierte Segmente&quot;2](/help/main/c-reports/assets/automated_segment_example_2.png)

## Häufig gestellte Fragen zu automatisierten Segmenten {#section_740910A52FA646B4AC9452F98C2F5719}

**Es sind noch keine Personalization Insights-Berichte für meine Aktivität verfügbar. Woran liegt das?**

Es gibt verschiedene Gründe, warum die [!UICONTROL Personalization Insights] -Berichte noch nicht für Ihre Aktivität verfügbar sind:

* 15 Tage sind seit der Aktivierung der Aktivität noch nicht vergangen. Die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ sind erst 15 Tage nach der Aktivierung der Aktivität verfügbar. Bis dahin können Sie nicht auf diese Berichte zugreifen und die Symbole für „Automatisierte Segmente“ und „Wichtige Attribute“ sind ausgegraut.
* Ihre Aktivität bietet nicht ausreichend Traffic im angegebenen Zeitraum. Nach 15 Tagen und sofern ausreichend Personalisierungstraffic in Ihrer Aktivität verfügbar ist, um die Personalisierungsmodelle zu erstellen, sind die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ verfügbar.
* Ihre Aktivität verfügt über ein Ziel zur Umsatzoptimierung. Derzeit ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Adobe wird in einer zukünftigen Version Unterstützung für Zielaktivitäten zur Umsatzoptimierung hinzufügen.

**Was ist ein Attribut?**

Ein Attribut ist eine Information zu einem Besucher oder seinem spezifischen Besuch, die von den Personalisierungsalgorithmen verwendet wird, um die Traffic-Personalisierung anzupassen. Bei einem Attribut kann es sich beispielsweise um den Browsertyp, den Standort, die Uhrzeit des Besuchs usw. handeln.

Weitere Informationen zu den Attributen, die [!DNL Target] in seinen Personalisierungsmodellen nutzt, finden Sie unter [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Weitere Informationen zum Hochladen neuer Attribute in Target zur Verwendung in den Target-Personalisierungsmodellen finden Sie unter [Verfahren für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}.

**Was ist ein automatisiertes Segment?**

Ein „automatisiertes Segment“ ist wie eine Zielgruppe, jedoch wird es statt vom Marketing-Experten durch die Target-Personalisierungsmodelle bestimmt.

Ein automatisiertes Segment besteht aus bestimmten Werten (oder Wertbereichen) für spezifische Attribute. Ein Beispiel für automatisierte Segmente finden Sie oben in Schritt 5. Segmente können sich überschneiden.

Weitere Informationen zum Random Forest-Personalisierungsalgorithmus, der die Grundlage für die Target-Personalisierungsmodelle bildet, finden Sie unter [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Was bestimmt die Reihenfolge der automatisierten Segmente?**

Über eine Bewertung für jedes Segment, die auf seiner Größe und seiner Performance bezüglich des Inhalts in Ihrer Aktivität basiert. Die Kombination dieser Eingaben bestimmt die Reihenfolge der automatisierten Segmente. So werden beispielsweise größere Segmente, die bei der Interaktion mit den verschiedenen Inhalten größere Unterschiede aufweisen, weiter oben in der Segmentliste angezeigt.

**Warum werden nur manche meiner Angebote/Erlebnisse im Bericht „Automatisierte Segmente“ angezeigt?**

AP- und AT-Aktivitäten erstellen ein Modell pro Angebot (bei AP) bzw. pro Erlebnis (bei AT). Diese Aktivitäten bieten personalisierten Traffic an und erstellen Ihre [!UICONTROL Personalization Insights] mit nur zwei erstellten Modellen. Wenn nicht alle Angebote/Erlebnisse in [!UICONTROL Personalization Insights] angezeigt werden, sind wahrscheinlich keine Modelle für diese spezifischen Angebote/Erlebnisse erstellt. Sie können den [!UICONTROL Summary] -Bericht Ihrer Aktivität überprüfen und feststellen, ob ein Uhrensymbol neben diesem Angebot/Erlebnis vorhanden ist. Dieses Symbol zeigt an, dass noch keine Modelle für dieses Angebot/Erlebnis erstellt wurden.

**Warum erhalten in einem bestimmten automatisierten Segment manche Angebote/Erlebnisse mit einer geringeren Konversionsrate mehr Traffic als andere Angebote/Erlebnisse?**

Es kann verschiedene Gründe dafür geben, dass Ihnen in einem automatisierten Segment mehr Besuche für Angebote oder Erlebnisse mit einer geringeren Konversionsrate angezeigt werden:

* Geringe Anzahl von Aufrufen für manche oder alle Angebote/Erlebnisse eines bestimmten automatisierten Segments.
* Aktivitäten mit geringerem Volumen, in denen für Angebote/Erlebnisse noch keine Modelle erstellt wurden oder in denen Modelle für manche Angebote/Erlebnisse schneller erstellt werden als für andere
* Targeting-Regeln in einem bestimmten Angebot, die einschränken, welchen Besuchern welche Angebote/Erlebnisse angezeigt werden

**Entsprechen die Informationen in den Berichten [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] den Informationen im CSV-Download?**

Nein. Der UI-Bericht enthält ausgewählte Informationen. Der CSV-Download enthält zusätzliche Details. Der Download des Insights-Berichts „Automatisierte Segmente“ enthält im Vergleich zu den Segmenten in der Benutzeroberfläche zusätzliche automatisierte Segmente sowie Informationen zu ihrer Performance in Ihren Angeboten oder Erlebnissen. Der Bericht „Wichtige Attribute“ enthält die 100 wichtigsten Besucherattribute und ihre relative Wichtigkeit, während in der UI nur die 10 wichtigsten Besucherattribute angezeigt werden.

**Kann ich [!UICONTROL Personalization Insights] für einen benutzerdefinierten Datumsbereich sehen?**

Die Personalization Insights-Berichterstellung (sowohl [!UICONTROL Automated Segments] als auch [!UICONTROL Important Attributes]) ist nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], einen ausreichend großen Datenbereich zu verwenden, um die Wahrscheinlichkeit zu verringern, dass Sie Einblicke aus einem kurzlebigen Muster in Ihrer Aktivität gewinnen. Sie können diese Zeiträume mit einem beliebigen Enddatum festlegen (sofern hierfür ausreichend Daten in der Aktivität vorhanden sind).

**Wie wird [!UICONTROL Personalization Insights] erstellt?**

[!UICONTROL Personalization Insights] wird mit einer patentierten Adobe-Technik namens MAGIX (Model Agnostic Globally Interpretable Explanations) erstellt. Weitere Informationen zu MAGIX finden Sie in der veröffentlichten Publikation des Adobe-Forschungsteams auf der [arXiv.org Website](https://arxiv.org/abs/1706.07160).

**Warum stimmen die gesamten Besuchertraffic-Daten im [!UICONTROL Automated Segments] -Bericht nicht mit meinem AP- oder AT-Zusammenfassungs-/Leistungsbericht überein?**

Die [!UICONTROL Personalization Insights] -Berichte umfassen nur Besucher, die einen von den Target-Personalisierungsmodellen ausgewählten Inhalt gesehen haben (d. h. keinen Kontroll-Traffic oder Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird). Dieser Traffic-Typ wird als &quot;personalisierter&quot; Traffic bezeichnet. Der zusammenfassende Leistungsbericht in AP/AT umfasst Kontroll- und &quot;zielgerichtete&quot;Traffic. Gezielter Traffic beinhaltet Personalisierungs-Traffic, Traffic, der mithilfe des Gesamt-Gewinnermodells bereitgestellt wird, sowie zufällig ausgewählten Traffic, der zum Lernen eingesetzt wird.

**Schließen sich automatisierte Segmente gegenseitig aus?**

Nein, automatisierte Segmente können sich überschneiden.

**Ist [!UICONTROL Personalization Insights] für umsatzbasierte Modellierungsziele/Primärziele verfügbar?**

Derzeit ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Adobe wird in einer zukünftigen Version Unterstützung für Zielaktivitäten zur Umsatzoptimierung hinzufügen.

**Wozu kann ich die Informationen in Personalization Insights nutzen?**

* Entdecken Sie neue Zielgruppen für das Targeting: Wenn Sie ein bestimmtes automatisiertes Segment sehen, das gut funktioniert, sollten Sie erwägen, eine Zielgruppe zu erstellen, damit Sie dieses Segment in anderen Berichten wiederverwenden können.
* Testen Sie Ihre Hypothesen dahingehend, welcher Besuchertyp auf welche Ihrer Erlebnisse reagiert.
* Ermitteln Sie, welche Inhalte für welche Besuchertypen funktionieren: Welche Angebote waren bei welchen Besuchern erfolgreich?
* Ermitteln Sie Gründe für Inhalte mit schlechter Performance.
* Finden Sie heraus, welche Attribute am wichtigsten für das Lernen des Modells waren.
* Ermitteln Sie, welche Attribute in den Personalisierungsmodellen eingesetzt werden und wie wichtig sie sind.
* Finden Sie Möglichkeiten für zusätzliche Datenpunkte, die Sie an Target übergeben können, um die Personalisierung weiter zu optimieren.

**Gibt es eine Logik bei der Reihenfolge, in der Attribute in einer Segmentkarte angezeigt werden?**

Nein, die Reihenfolge der Karten basiert nur auf einer Rangfolge, die oben beschrieben wurde. Die Reihenfolge der Attribute innerhalb einer Karte basiert auf keiner Logik.
