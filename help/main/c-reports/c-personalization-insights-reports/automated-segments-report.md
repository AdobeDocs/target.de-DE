---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; auto-target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen
description: Erfahren Sie, wie verschiedene Segmente, die von Adobe [!DNL Target] Personalisierungsmodellen definiert werden, auf Angebote/Erlebnisse in der Aktivität reagieren, indem Sie den Bericht „Automatisierte Segmente“ anzeigen.
title: Was ist der Bericht „Automatisierte Segmente“?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 60%

---

# [!UICONTROL Automated Segments]

Informationen zum [!UICONTROL Automated Segments] Bericht, einem der beiden Sonderberichte, die Benutzern von [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] (AT) zur Verfügung stehen.

>[!NOTE]
>
>Beachten Sie bei der Verwendung von Personalization Insights-Berichten Folgendes:
>
>* AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
>
>* [!UICONTROL Personalization Insights] Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
>
>* [!UICONTROL Personalization Insights] Berichte sind nur verfügbar, wenn der [!UICONTROL Primary Goal] aus der Dropdown-Liste [!UICONTROL Report Metric] ausgewählt wurde.
>
>* [!UICONTROL Personalization Insights] Berichte werden nur in der [Standardumgebung](/help/main/administrating-target/hosts.md) unterstützt.
>
>* [!UICONTROL Personalization Insights] Berichte werden nur für Aktivitäten generiert, die sich im Status [!UICONTROL Live] befinden und für mindestens 15 Tage aktiviert wurden und Traffic empfangen.

Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

## Zugreifen auf den Bericht „Automatisierte Segmente“ {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klicken Sie auf **[!UICONTROL Activities]** und dann auf die gewünschte [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)- oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)-Aktivität in der Liste.

   Wenn Sie über viele Aktivitäten verfügen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf **[!UICONTROL Reports]**.

   Der Bericht [Automated Personalization-](/help/main/c-reports/personalization-reports/reports-ap.md) oder [Automatische Targeting-Zusammenfassung](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) wird angezeigt, der Informationen zur Leistung Ihrer Aktivitäten enthält, dargestellt durch das erste Bildschirmsymbol. Die beiden zusätzlichen Symbole stehen für die beiden Personalization Insights-Berichte: „Automatisierte Segmente“ und „Wichtige Attribute“. Automatisches Targeting verfügt über ein zusätzliches Diagrammsymbol für die grafische Ansicht des [!UICONTROL Summary].

   ![Personalization Insights-Bericht in Adobe Target](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Der [!UICONTROL Automated Segments] Bericht ist frühestens 15 Tage nach Aktivierung der Aktivität verfügbar. In diesem Zeitraum können Sie weder auf diesen Bericht zugreifen noch auf das [!UICONTROL Automated Segments] klicken. Wenn Sie nach 15 Tagen ausreichend personalisierten Traffic in Ihrer Aktivität haben, ist der [!UICONTROL Automated Segments] Bericht verfügbar.

1. Nach 15 Tagen nach Aktivierung der Aktivität können Sie auf das **[!UICONTROL Automated Segments]** klicken.

   ![Symbol für automatisierte Segmente](/help/main/c-reports/assets/icon-automated-sements.png)

1. Wählen Sie den gewünschten Datumsbereich aus.

   Im Gegensatz zum [!UICONTROL Summary]-Bericht (Leistungsberichte) ist [!UICONTROL Personalization Insights], einschließlich [!UICONTROL Automated Segments], nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], einen ausreichend großen Datenbereich zu verwenden, um die Wahrscheinlichkeit zu verringern, dass Sie Einblicke aus einem kurzlebigen Muster in Ihrer Aktivität ableiten. Die beiden Entscheidungen, die Sie beim Datumsbereich treffen können, sind „Enddatum“ und „Dauer“. Sie werden feststellen, dass „Start“ ausgegraut ist. Das Startdatum ändert sich automatisch basierend auf Ihrer Auswahl für Enddatum und Dauer.

   ![Kalender im Adobe Target-Bericht](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   Sie können über die Dropdown-Liste [!UICONTROL Choose Duration] auf die verfügbaren festen Datumsbereiche zugreifen.

   ![Dropdownliste „Dauer“ in Adobe Target](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Überprüfen Sie die [!UICONTROL Automated Segments] Berichtsdaten.

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
| Mittiges Diagramm | Die mittleren Diagramme zeigen an, wie der Inhalt Ihrer Aktivität für das hervorgehobene automatisierte Segment ausgeführt wurde. Wenn Sie im linken Bereich auf ein anderes Segment klicken, wird das mittige Diagramm angepasst. |
| Tortendiagramme | Die Tortendiagramme oben im mittleren Bereich zeigen die Größe des automatisierten Segments sowie die Gesamtzahl personalisierter Besuche in der Aktivität, wie z. B. den Traffic zu dieser Aktivität, der von dem Personalisierungsmodell bereitgestellt wurde. Sie enthalten weder Kontroll-Traffic noch Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird. Die Größe des Segments basiert nur auf personalisierten Besuchen.<br>![Tortendiagramm](/help/main/c-reports/assets/pie.png) |
| Zweiachsiges Balkendiagramm | Das zweiachsige Balkendiagramm enthält Besuchs- und Konversionsinformationen nach Angebot oder Erlebnis für das spezifische automatisierte Segment. |
| Pinkfarbener Balken | Der pinkfarbene Balken zeigt die Konversionsrate und verwendet die untere Achse des Diagramms. Fahren Sie mit dem Mauszeiger über den Balken, um weitere Informationen anzuzeigen. |
| Blauer Balken | Der blaue Balken zeigt die Anzahl der Besuche und verwendet die obere Achse des Diagramms. Fahren Sie mit dem Mauszeiger über den Balken, um weitere Informationen anzuzeigen. |
| Graue gestrichelte Linie | Die graue gestrichelte Linie zeigt die Konversionsrate für alle personalisierten Besuche in der Aktivität über alle Angebote/Erlebnisse und automatisierten Segmente hinweg. |

**Automatisierte Segmente – Beispiel 1**

Dieses automatisierte Segment wird basierend auf einem Attribut definiert. Bei Besuchern in diesem automatisierten Segment trat die AP-Aktivität an einem Werktag außerhalb der Geschäftszeiten oder am Wochenende auf.

![Beispiel 1 für den Bericht zu automatisierten Segmenten](/help/main/c-reports/assets/automated_segment_example_1.png)

**Automatisierte Segmente – Beispiel 2**

Dieses automatisierte Segment wird basierend auf zwei Attributen definiert. Besucher in diesem automatisierten Segment, bei denen diese AP-Aktivität auftrat, wiesen bei ihrem aktuellen Besuch weniger als drei Seitenaufrufe auf und befanden sich zwischen Breitengrad 42,57 und 47,29 (also ungefähr zwischen New Hampshire/Oregon und Washington/Maine für ein US-ansässiges Unternehmen).

![Beispiel 2 im Bericht zu automatisierten Segmenten](/help/main/c-reports/assets/automated_segment_example_2.png)

## Häufig gestellte Fragen zu automatisierten Segmenten {#section_740910A52FA646B4AC9452F98C2F5719}

**Es sind noch keine Personalization Insights-Berichte für meine Aktivität verfügbar. Woran liegt das?**

Es gibt mehrere Gründe, warum die [!UICONTROL Personalization Insights] noch nicht für Ihre Aktivität verfügbar sind:

* Seit der Aktivierung der Aktivität sind noch keine 15 Tage vergangen. Die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ sind erst 15 Tage nach der Aktivierung der Aktivität verfügbar. Bis dahin können Sie nicht auf diese Berichte zugreifen und die Symbole für „Automatisierte Segmente“ und „Wichtige Attribute“ sind ausgegraut.
* Ihre Aktivität bietet nicht ausreichend Traffic im angegebenen Zeitraum. Nach 15 Tagen und sofern ausreichend Personalisierungstraffic in Ihrer Aktivität verfügbar ist, um die Personalisierungsmodelle zu erstellen, sind die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ verfügbar.
* Ihre Aktivität verfügt über ein Ziel zur Umsatzoptimierung. Derzeit ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Konversionsoptimierungszielen verfügbar. Adobe wird in einer zukünftigen Version Unterstützung für Aktivitäten zum Ziel der Umsatzoptimierung hinzufügen.

**Was ist ein Attribut?**

Ein Attribut ist eine Information zu einem Besucher oder seinem spezifischen Besuch, die von den Personalisierungsalgorithmen verwendet wird, um die Traffic-Personalisierung anzupassen. Bei einem Attribut kann es sich beispielsweise um den Browsertyp, den Standort, die Uhrzeit des Besuchs usw. handeln.

Weitere Informationen zu den Attributen, die [!DNL Target] in seinen Personalisierungsmodellen nutzt, finden Sie unter [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Weitere Informationen zum Hochladen neuer Attribute in Target zur Verwendung in den Personalisierungsmodellen von Target finden Sie unter [Verfahren für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}.

**Was ist ein automatisiertes Segment?**

Ein „automatisiertes Segment“ ist wie eine Zielgruppe, jedoch wird es statt vom Marketing-Experten durch die Target-Personalisierungsmodelle bestimmt.

Ein automatisiertes Segment besteht aus bestimmten Werten (oder Wertbereichen) für spezifische Attribute. Ein Beispiel für automatisierte Segmente finden Sie oben in Schritt 5. Segmente können sich überschneiden.

Weitere Informationen zum Personalisierungsalgorithmus für zufällige Gesamtstrukturen, der die Grundlage für die Personalisierungsmodelle von Target ist, finden Sie unter [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Was bestimmt die Reihenfolge der automatisierten Segmente?**

Über eine Bewertung für jedes Segment, die auf seiner Größe und seiner Performance bezüglich des Inhalts in Ihrer Aktivität basiert. Die Kombination dieser Eingaben bestimmt die Reihenfolge der automatisierten Segmente. So werden beispielsweise größere Segmente, die bei der Interaktion mit den verschiedenen Inhalten größere Unterschiede aufweisen, weiter oben in der Segmentliste angezeigt.

**Warum werden nur manche meiner Angebote/Erlebnisse im Bericht „Automatisierte Segmente“ angezeigt?**

AP- und AT-Aktivitäten erstellen ein Modell pro Angebot (bei AP) bzw. pro Erlebnis (bei AT). Diese Aktivitäten beginnen mit der Bereitstellung von personalisiertem Traffic und erstellen Ihre [!UICONTROL Personalization Insights] mit nur zwei erstellten Modellen. Wenn Sie nicht alle Ihre Angebote/Erlebnisse in [!UICONTROL Personalization Insights] sehen, haben Sie wahrscheinlich keine Modelle für diese spezifischen Angebote/Erlebnisse erstellt. Sie können den [!UICONTROL Summary] Ihrer Aktivität überprüfen und feststellen, ob neben diesem Angebot/Erlebnis ein Uhrensymbol vorhanden ist. Dieses Symbol zeigt an, dass für dieses Angebot/Erlebnis noch keine Modelle erstellt wurden.

**Warum erhalten in einem bestimmten automatisierten Segment manche Angebote/Erlebnisse mit einer geringeren Konversionsrate mehr Traffic als andere Angebote/Erlebnisse?**

Es kann verschiedene Gründe dafür geben, dass Ihnen in einem automatisierten Segment mehr Besuche für Angebote oder Erlebnisse mit einer geringeren Konversionsrate angezeigt werden:

* Geringe Anzahl von Aufrufen für manche oder alle Angebote/Erlebnisse eines bestimmten automatisierten Segments.
* Aktivitäten mit geringerem Volumen, in denen für Angebote/Erlebnisse noch keine Modelle erstellt wurden oder in denen Modelle für manche Angebote/Erlebnisse schneller erstellt werden als für andere
* Targeting-Regeln in einem bestimmten Angebot, die einschränken, welchen Besuchern welche Angebote/Erlebnisse angezeigt werden

**Sind die Informationen in den [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] Berichten mit denen im CSV-Download identisch?**

Nein. Der UI-Bericht enthält ausgewählte Informationen. Der CSV-Download enthält zusätzliche Details. Der Download des Insights-Berichts „Automatisierte Segmente“ enthält im Vergleich zu den Segmenten in der Benutzeroberfläche zusätzliche automatisierte Segmente sowie Informationen zu ihrer Performance in Ihren Angeboten oder Erlebnissen. Der Bericht „Wichtige Attribute“ enthält die 100 wichtigsten Besucherattribute und ihre relative Wichtigkeit, während in der UI nur die 10 wichtigsten Besucherattribute angezeigt werden.

**Kann ich [!UICONTROL Personalization Insights] für einen benutzerdefinierten Datumsbereich sehen?**

Personalization Insights-Berichte (sowohl [!UICONTROL Automated Segments] als auch [!UICONTROL Important Attributes]) sind nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], einen ausreichend großen Datenbereich zu verwenden, um die Wahrscheinlichkeit zu verringern, dass Sie Einblicke aus einem kurzlebigen Muster in Ihrer Aktivität ableiten. Sie können diese Zeiträume mit einem beliebigen Enddatum festlegen (sofern hierfür ausreichend Daten in der Aktivität vorhanden sind).

**Wie wird [!UICONTROL Personalization Insights] erstellt?**

[!UICONTROL Personalization Insights] wird mithilfe einer zum Adobe-Patent angemeldeten Technik namens MAGIX (Model Agnostic Globally Interpretable Explanations) erstellt. Weitere Informationen zu MAGIX finden Sie in der Publikation des Adobe-Forschungsteams auf der [arXiv.org](https://arxiv.org/abs/1706.07160).

**Warum stimmen die Traffic-Daten der Besucher im [!UICONTROL Automated Segments] nicht mit meinem AP- oder AT-Zusammenfassungs-/Leistungsbericht überein?**

Die [!UICONTROL Personalization Insights] Berichte umfassen nur Besucherinnen und Besucher, die einen von den Personalisierungsmodellen von Target ausgewählten Inhalt gesehen haben (d. h. sie berücksichtigen nicht den Kontroll-Traffic oder den Traffic, der vom allgemeinen Gewinnermodell bereitgestellt wird). Dieser Traffic wird als „personalisierter“ Traffic bezeichnet. Der zusammenfassende Leistungsbericht in AP/AT enthält Kontroll- versus „Targeting“-Traffic. Gezielter Traffic beinhaltet Personalisierungs-Traffic, Traffic, der mithilfe des Gesamt-Gewinnermodells bereitgestellt wird, sowie zufällig ausgewählten Traffic, der zum Lernen eingesetzt wird.

**Schließen sich automatisierte Segmente gegenseitig aus?**

Nein, automatisierte Segmente können sich überschneiden.

**Ist [!UICONTROL Personalization Insights] für umsatzbasierte Modellierungsziele/primäre Ziele verfügbar?**

Derzeit ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Konversionsoptimierungszielen verfügbar. Adobe wird in einer zukünftigen Version Unterstützung für Aktivitäten zum Ziel der Umsatzoptimierung hinzufügen.

**Wozu kann ich die Informationen in Personalization Insights nutzen?**

* Erkunden neuer Zielgruppen: Wenn Sie ein bestimmtes automatisiertes Segment sehen, das eine gute Leistung erbringt, sollten Sie eine Zielgruppe erstellen, damit Sie dieses Segment in anderen Berichten wiederverwenden können.
* Testen Sie Ihre Hypothesen darüber, welche Art von Besuchern auf welche Ihrer Erlebnisse reagieren.
* Ermitteln Sie, welche Inhalte für welche Besuchertypen funktionieren: Welche Angebote waren bei welchen Besuchern erfolgreich?
* Ermitteln Sie Gründe für Inhalte mit schlechter Performance.
* Finden Sie heraus, welche Attribute am wichtigsten für das Lernen des Modells waren.
* Ermitteln Sie, welche Attribute in den Personalisierungsmodellen eingesetzt werden und wie wichtig sie sind.
* Finden Sie Möglichkeiten für zusätzliche Datenpunkte, die Sie an Target übergeben können, um die Personalisierung weiter zu optimieren.

**Gibt es eine Logik bei der Reihenfolge, in der Attribute in einer Segmentkarte angezeigt werden?**

Nein, die Reihenfolge der Karten basiert nur auf einer Rangfolge, die oben beschrieben wurde. Die Reihenfolge der Attribute innerhalb einer Karte basiert auf keiner Logik.
