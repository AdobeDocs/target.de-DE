---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; Auto-Target; Auto Target; Auto-Target-Bericht; Auto Target-Bericht; Personalisierung; Insights; FAQ; häufig gestellte Fragen; wichtige Attribute
description: Erfahren Sie, wie Sie die [!UICONTROL Wichtige Attribute] -Bericht, der die wichtigsten Attribute anzeigt, die das Personalisierungsmodell beeinflusst haben, und deren relative Bedeutung.
title: Was ist der Bericht "Wichtige Attribute"?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Reports
exl-id: c1069ca7-e221-4865-a82e-6cff5b4c0055
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1871'
ht-degree: 67%

---

# Bericht „Wichtige Attribute“

Informationen über [!UICONTROL Wichtige Attribute] einen der beiden für Benutzer von [!UICONTROL Automated Personalization] AP und [!UICONTROL Automatisches Targeting] (AT) Tätigkeiten.

>[!NOTE]
>
>Beachten Sie Folgendes bei der Verwendung von [!UICONTROL Personalization Insights] Berichte:
>
>* AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
>
>* [!UICONTROL Personalization Insights] -Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
>
>* [!UICONTROL Personalization Insights] Berichte sind nur verfügbar, wenn die Variable [!UICONTROL Primäres Ziel] wird aus dem [!UICONTROL Berichtsmetrik] Dropdown-Liste.
>
>* [!UICONTROL Personalization Insights] Berichte werden in der [Standardumgebung](/help/main/administrating-target/hosts.md) nur.
>
>* [!UICONTROL Personalization Insights] -Berichte werden nur für Aktivitäten generiert, die sich im [!UICONTROL Live] und wurden mindestens 15 Tage lang aktiviert und erhalten Traffic.

In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

## Zugriff auf [!UICONTROL Wichtige Attribute] Bericht {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klicks **[!UICONTROL Tätigkeiten]** und klicken Sie dann auf die gewünschte [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) -Aktivität aus der Liste aus.

   Sollten Ihnen viele Aktivitäten zur Auswahl stehen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Berichtsquelle], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Aktivitätsquelle] auswählen.

1. Klicken Sie auf **[!UICONTROL Berichte]**.

   Die [Automated Personalization-Zusammenfassung](/help/main/c-reports/personalization-reports/reports-ap.md) oder [Zusammenfassung für automatisches Targeting](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) angezeigt, der Informationen über die Leistung Ihrer Aktivitäten bereitstellt, die durch das Symbol des ersten Bildschirms dargestellt werden. Die beiden zusätzlichen Symbole stellen die beiden [!UICONTROL Personalization Insights] Berichte: [!UICONTROL Automatisierte Segmente] und [!UICONTROL Wichtige Attribute].

   ![Zusammenfassungsbericht für Automated Personalization-Aktivität](/help/main/c-reports/assets/summary-report-ap.png)

   Beachten Sie Folgendes: [!UICONTROL Automatisches Targeting] verfügt über ein zusätzliches Diagrammsymbol für die grafische Ansicht des [!UICONTROL Zusammenfassung] Bericht.

   ![Zusammenfassungsbericht für die Aktivität &quot;Automatisches Targeting&quot;](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Der Bericht [!UICONTROL Wichtige Attribute] steht erst nach mindestens 15 Tagen nach der Aktivierung Ihrer Aktivität zur Verfügung. Bis dahin können Sie nicht auf diesen Bericht zugreifen und das Symbol für [!UICONTROL „Wichtige Attribute“] ist ausgegraut. Nach 15 Tagen und sofern ausreichend personalisierter Traffic in Ihrer Aktivität verfügbar ist, wird die [!UICONTROL Wichtige Attribute] -Bericht verfügbar.

1. 15 Tage nach der Aktivierung der Aktivität klicken Sie auf das **[!UICONTROL Wichtige Attribute]** Symbol.

   ![Symbol &quot;Wichtige Attribute&quot;in einem Adobe Target-Bericht](/help/main/c-reports/assets/model_attribute_ranking.png)

1. Wählen Sie den gewünschten Datumsbereich aus.

   Im Gegensatz zu [!UICONTROL Zusammenfassung] Bericht (Leistungsberichte), [!UICONTROL Personalization Insights], einschließlich [!UICONTROL Wichtige Attribute], ist nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage.

   Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], ausreichend Daten anzusammeln, um zu verhindern, dass Insights aus kurzfristigen Mustern in Ihrer Aktivität abgeleitet werden. Die beiden Entscheidungen, die Sie beim Datumsbereich treffen können, sind „Enddatum“ und „Dauer“. „Start“ ist ausgegraut. Das Startdatum ändert sich automatisch basierend auf Ihrer Auswahl für Enddatum und Dauer.

   ![Kalender in einem Adobe Target-Bericht](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   Sie können über die Dropdownliste [!UICONTROL „Dauer auswählen“] auf die verfügbaren festen Datumsbereiche zugreifen.

   ![Dropdownliste &quot;Dauer&quot;in einem Bericht auswählen](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Überprüfen Sie die Daten des Berichts [!UICONTROL „Wichtige Attribute“].

   ![Bericht &quot;Wichtige Attribute&quot;in Adobe Target](/help/main/c-reports/assets/model_attribute_ranking_report.png)

1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF), um ihn in Excel und anderen Tools zu analysieren.

   >[!NOTE]
   >
   >Der Bericht „Personalization Insights UI“ enthält Informationen zur Auswahl. Der CSV-Download für den Bericht „Wichtige Attribute“ enthält zusätzliche Details. Der Download des Berichts „Wichtige Attribute“ enthält die vollständige Liste der 100 wichtigsten Attribute, während der UI-Bericht nur die wichtigsten 10 enthält. Wenn Sie im Bericht nach einem bestimmten Attribut suchen, es aber nicht enthalten ist, heißt das nicht, dass das entsprechende Attribut die Aktivität nicht beeinflusst hat. Es heißt nur, dass es nicht unter den 100 wichtigsten Attributen ist.

## Bericht für wichtige Attribute interpretieren

Folgende Tabelle enthält Informationen dazu, wie der Bericht zu interpretieren ist, und beschreibt seine Bestandteile:

| Element | Details |
|--- |--- |
| Balkendiagramm | Das mehrfarbige Balkendiagramm oben auf dem Bildschirm zeigt die relative Wichtigkeit und ordnet sie der Punktfarbe neben den Attributen in der Tabelle zu. Sie können auch mit dem Mauszeiger über eine Farbe im Balkendiagramm fahren, um das Attribut anzuzeigen, für das sie steht.  Die Bewertungen der wichtigsten Attribute ergeben zusammen 100 %. Weitere Informationen zum Hinzufügen weiterer Attribute, die von den Target-Personalisierungsmodellen verwendet werden können, finden Sie unter [Hochladen von Daten für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md). |
| Diagramm „Modell-Attribut-Ranking“ | Das Diagramm „Modell-Attribut-Ranking“ enthält die 10 Attribute, die für die Entscheidung des Target-Personalisierungsmodells, welche Inhalte welchem Besucher angezeigt werden sollen, am wichtigsten waren. Die Bewertung zeigt, wie wichtig ein bestimmter Wert (im Verhältnis zu den 100 wichtigsten Attributen) für die Target-Personalisierungsmodelle in dieser Aktivität waren. |

## Häufig gestellte Fragen zu wichtigen Attributen {#section_740910A52FA646B4AC9452F98C2F5719}

Antworten auf häufig gestellte Fragen zur Verwendung der [!UICONTROL Wichtige Attribute] Bericht.

### Personalization Insights-Berichte sind noch nicht für meine Aktivität verfügbar. Warum ist das?

Es kann verschiedene Gründe dafür geben, dass die [!UICONTROL Personalization Insights]-Berichte noch nicht für Ihre Aktivität verfügbar sind:

* Es sind noch keine 15 Tage seit Aktivierung der Aktivität vergangen. Die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ sind erst 15 Tage nach der Aktivierung der Aktivität verfügbar. Bis dahin können Sie nicht auf diese Berichte zugreifen und die Symbole für „Automatisierte Segmente“ und „Wichtige Attribute“ sind ausgegraut.
* Ihre Aktivität bietet nicht ausreichend Traffic im angegebenen Zeitraum. Nach 15 Tagen und sofern [ausreichend Personalisierungstraffic](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB) in Ihrer Aktivität verfügbar ist, um die Personalisierungsmodelle zu erstellen, sind die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ verfügbar.
* Ihre Aktivität verfügt über ein Ziel zur Umsatzoptimierung. Zum jetzigen Zeitpunkt ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Wir werden die Unterstützung von Umsatzoptimierungszielen in einer künftigen Version ergänzen.

### Was ist ein Attribut?

Ein Attribut ist eine Information zu einem Besucher oder seinem spezifischen Besuch, die von den Personalisierungsalgorithmen verwendet wird, um die Traffic-Personalisierung anzupassen. Bei einem Attribut kann es sich beispielsweise um den Browsertyp, den Standort, die Uhrzeit des Besuchs usw. handeln.

Weitere Informationen zu den Attributen, die [!DNL Target] in seinen Personalisierungsmodellen nutzt, finden Sie unter [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Weitere Informationen zum Hochladen neuer Attribute in Target zur Verwendung in den Target-Personalisierungsmodellen finden Sie unter [Verfahren für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}.

### Ich sehe ein oder mehrere Attribute, die das Modell nicht für das Training verwenden soll. Kann ich diese Attribute aus dem Trainings-Modell entfernen? {#models-api}

Die [!UICONTROL Modelle-API], die auch als Blockierungsliste-API bezeichnet wird, ermöglicht Benutzern, die Liste der Attribute (auch als Funktionen bezeichnet) anzuzeigen und zu verwalten, die in Modellen für maschinelles Lernen für [!UICONTROL Automated Personalization] AP und [!UICONTROL Automatisches Targeting] (AT) Tätigkeiten. Wenn Sie ein oder mehrere Attribute von der Verwendung durch die Modelle für AP- oder AT-Aktivitäten ausschließen möchten, können Sie die Modelle-API verwenden, um diese Attribute zur &quot;Blockierungsliste&quot;hinzuzufügen.

Detaillierte Informationen finden Sie unter [Übersicht über die Modelle-API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} in the *Adobe Target Developer Guide*. To use the API to block attributes, see [Models API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api-overview.html){target=_blank}.

### Ist die Information in der [!UICONTROL Automatisierte Segmente] und [!UICONTROL Wichtige Attribute] die gleichen Berichte wie im CSV-Download?

Nein. Der UI-Bericht enthält ausgewählte Informationen. Der CSV-Download enthält zusätzliche Details. Der Download des Insights-Berichts „Automatisierte Segmente“ enthält im Vergleich zu den Segmenten in der Benutzeroberfläche zusätzliche automatisierte Segmente sowie Informationen zu ihrer Performance in Ihren Angeboten oder Erlebnissen. Der Bericht „Wichtige Attribute“ enthält die 100 wichtigsten Besucherattribute und ihre relative Wichtigkeit, während in der UI nur die 10 wichtigsten Besucherattribute angezeigt werden.

### Kann ich Personalization Insights für einen benutzerdefinierten Datumsbereich anzeigen?

Personalization Insights (sowohl [!UICONTROL „Automatisierte Segmente“] als auch [!UICONTROL „Wichtige Attribute“]) ist nur für feste Zeiträume verfügbar: 15, 30, 45, 60 oder 90 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], ausreichend Daten anzusammeln, um zu verhindern, dass Insights aus kurzfristigen Mustern in Ihrer Aktivität abgeleitet werden. Sie können diese Zeiträume mit einem beliebigen Enddatum festlegen (sofern hierfür ausreichend Daten in der Aktivität vorhanden sind).

### Wie ist [!UICONTROL Personalization Insights] erstellt?

[!UICONTROL Personalization Insights] wird mithilfe der patentierten Adobe-Technik namens MAGIX (Model Agnostic Globally Interpretable Explanations) erstellt. Weitere Informationen zu MAGIX finden Sie im veröffentlichten Beitrag des Adobe-Forschungsteams auf der [arXiv.org website](https://arxiv.org/abs/1706.07160).

### sind [!UICONTROL Personalization Insights] verfügbar für umsatzbasierte Modellierungsziele/Primärziele?

Zum jetzigen Zeitpunkt ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Wir werden die Unterstützung von Umsatzoptimierungszielen in einer künftigen Version ergänzen.

### Wie hoch ist die Wichtigkeitsbewertung des Attributs im Bericht &quot;Wichtige Attribute&quot;?

Die Wichtigkeitsbewertung im Abschnitt „Attribut-Wichtigkeitsbewertung“ des Berichts zeigt, welche Variablen, die der Algorithmus zum Lernen verwendet hat, bei der Aufteilung aller Besucher auf die vom Algorithmus ermittelten Segmente am wichtigsten waren. Den 100 wichtigsten vom Modell verwendeten Attributen wird eine prozentuale Bewertung zugewiesen.

### Warum erhalten in einem bestimmten automatisierten Segment manche Angebote/Erlebnisse mit einer geringeren Konversionsrate mehr Traffic als andere Angebote/Erlebnisse?

Es kann verschiedene Gründe dafür geben, dass Ihnen in einem automatisierten Segment mehr Besuche für Angebote oder Erlebnisse mit einer geringeren Konversionsrate angezeigt werden:

* Geringe Anzahl von Aufrufen für manche oder alle Angebote/Erlebnisse eines bestimmten automatisierten Segments.
* Aktivitäten mit geringerem Volumen, in denen für bestimmte Angebote oder Erlebnisse keine Modelle erstellt wurden.
* Aktivitäten mit geringerem Volumen, in denen Modelle für einige Angebote/Erlebnisse früher erstellt wurden als andere. Beispiel: Ein zusätzliches Modell wurde am Tag 22 erstellt und Sie sehen sich Daten von den Tagen 10 bis 24 an.
* Targeting-Regeln in einem bestimmten Angebot, die einschränken, welchen Besuchern welche Angebote/Erlebnisse angezeigt werden.
* In den Insight-Berichten gibt es keine Konfidenzintervalle. Wenn die Konversionsraten jedoch nahe genug sind, kann das Modell Traffic bereitstellen, sodass es im Punktwert höher ist, aber keine &quot;statistisch unterschiedlichen&quot;Zahlen vorliegen.

Es kann hilfreich sein zu wissen, wie das Modell funktioniert, das Traffic bereitstellt. Jede einzelne Person wird auf der Grundlage ihres Gesamtprofils angesprochen. Die Insight-Berichte verallgemeinern dieses Verhalten jedoch, damit es von Menschen besser interpretiert werden kann. Daher schließen sich Segmente nicht gegenseitig aus. Dies kann zu einzelnen Segmenten führen, die dieses Verhalten aufweisen, da eine Person in mehreren Segmenten vorkommen kann.

### Auf welche unterschiedliche Weise kann ich die Informationen in Personalization Insights nutzen?

* Entdecken Sie neue Zielgruppen für Ihr Targeting: Wenn Sie ein bestimmtes automatisiertes Segment finden, das besonders gut abschneidet, können Sie hieraus eine Zielgruppe erstellen, die Sie als Segment in anderen Berichten verwenden können.
* Testen Sie Thesen dazu, welche Besuchertypen auf welche Erlebnisse reagieren.
* Ermitteln Sie, welche Inhalte für welche Besuchertypen funktionieren: Welche Angebote waren bei welchen Besuchern erfolgreich?
* Ermitteln Sie Gründe für Inhalte mit schlechter Performance.
* Finden Sie heraus, welche Attribute am wichtigsten für das Lernen des Modells waren.
* Ermitteln Sie, welche Attribute in den Personalisierungsmodellen eingesetzt werden und wie wichtig sie sind.
* Finden Sie Möglichkeiten für zusätzliche Datenpunkte, die Sie an Target übergeben können, um die Personalisierung weiter zu optimieren.

## Bekannte Probleme

Das folgende Problem wird derzeit vom [!DNL Target] Technikerteam.

* [!DNL Adobe Experience Platform] Segmentnamen werden für die Aktivitäten [!UICONTROL Automatisierte Personalisierung] (AP) und [!UICONTROL Automatisches Targeting] (AT) nicht im Bericht [!UICONTROL Wichtige Attribute] angezeigt. (Die 3813 populärsten)
