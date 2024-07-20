---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; Auto-Target; Auto Target; Auto-Target-Bericht; Auto Target-Bericht; Personalisierung; Insights; FAQ; häufig gestellte Fragen; wichtige Attribute
description: Erfahren Sie, wie Sie den Bericht [!UICONTROL Important Attributes] verwenden, der die wichtigsten Attribute anzeigt, die das Personalisierungsmodell beeinflusst haben, und deren relative Bedeutung.
title: Was ist der Bericht "Wichtige Attribute"?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Reports
exl-id: c1069ca7-e221-4865-a82e-6cff5b4c0055
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1790'
ht-degree: 56%

---

# Bericht „Wichtige Attribute“

Informationen zum Bericht [!UICONTROL Important Attributes], einem der beiden für Benutzer der Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] (AT) verfügbaren speziellen Berichte.

>[!NOTE]
>
>Beachten Sie bei Verwendung von [!UICONTROL Personalization Insights] -Berichten Folgendes:
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

In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

## Zugriff auf den Bericht [!UICONTROL Important Attributes] {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität vom Typ [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) .

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf **[!UICONTROL Reports]**.

   Der Bericht [Automated Personalization-Zusammenfassung](/help/main/c-reports/personalization-reports/reports-ap.md) oder [Zusammenfassung des automatischen Targetings](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) wird angezeigt. Er enthält Informationen zur Performance Ihrer Aktivitäten, dargestellt durch das erste Bildschirmsymbol. Die beiden zusätzlichen Symbole stellen die beiden [!UICONTROL Personalization Insights] Berichte dar: [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes].

   ![Zusammenfassungsbericht für Automated Personalization-Aktivität](/help/main/c-reports/assets/summary-report-ap.png)

   Beachten Sie, dass [!UICONTROL Auto-Target] über ein zusätzliches Diagrammsymbol für die grafische Ansicht des Berichts [!UICONTROL Summary] verfügt.

   ![Zusammenfassungsbericht für Aktivität vom Typ &quot;Automatisches Targeting&quot;](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Der Bericht [!UICONTROL Important Attributes] steht erst nach mindestens 15 Tagen nach der Aktivierung Ihrer Aktivität zur Verfügung. In diesem Anfangszeitraum können Sie nicht auf diesen Bericht zugreifen oder auf das Symbol [!UICONTROL Important Attributes] klicken. Nach 15 Tagen und sofern ausreichend personalisierter Traffic in Ihrer Aktivität verfügbar ist, ist der Bericht [!UICONTROL Important Attributes] verfügbar.

1. 15 Tage nach der Aktivierung der Aktivität klicken Sie auf das Symbol **[!UICONTROL Important Attributes]** .

   ![Symbol &quot;Wichtige Attribute&quot;in einem Adobe Target-Bericht](/help/main/c-reports/assets/model_attribute_ranking.png)

1. Wählen Sie den gewünschten Datumsbereich aus.

   Im Gegensatz zum [!UICONTROL Summary] -Bericht (Leistungsberichte) ist [!UICONTROL Personalization Insights], einschließlich [!UICONTROL Important Attributes], nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage und 60 Tage.

   Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], einen ausreichend großen Datenbereich zu verwenden, um die Wahrscheinlichkeit zu verringern, dass Sie Einblicke aus einem kurzlebigen Muster in Ihrer Aktivität gewinnen. Die beiden Entscheidungen, die Sie beim Datumsbereich treffen können, sind „Enddatum“ und „Dauer“. „Start“ ist ausgegraut. Das Startdatum ändert sich automatisch basierend auf Ihrer Auswahl für Enddatum und Dauer.

   ![Kalender in einem Adobe Target-Bericht](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   Sie können über die Dropdownliste [!UICONTROL Choose Duration] auf die verfügbaren festen Datumsbereiche zugreifen.

   ![Wählen Sie die Dropdownliste Dauer in einem Bericht aus](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Überprüfen Sie die [!UICONTROL Important Attributes] -Berichtsdaten.

   ![Bericht &quot;Wichtige Attribute&quot;in Adobe Target](/help/main/c-reports/assets/model_attribute_ranking_report.png)

1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF), um ihn in Excel und anderen Tools zu analysieren.

   >[!NOTE]
   >
   >Der Bericht „Personalization Insights UI“ enthält Informationen zur Auswahl. Der CSV-Download für den Bericht „Wichtige Attribute“ enthält zusätzliche Details. Der Download des Berichts „Wichtige Attribute“ enthält die vollständige Liste der 100 wichtigsten Attribute, während der UI-Bericht nur die wichtigsten 10 enthält. Wenn Sie im Bericht nach einem bestimmten Attribut suchen, es aber nicht enthalten ist, heißt das nicht, dass das entsprechende Attribut die Aktivität nicht beeinflusst hat. Es heißt nur, dass es nicht unter den 100 wichtigsten Attributen ist.

## Bericht für wichtige Attribute interpretieren

Folgende Tabelle enthält Informationen dazu, wie der Bericht zu interpretieren ist, und beschreibt seine Bestandteile:

| Element | Details |
|--- |--- |
| Balkendiagramm | Das mehrfarbige Balkendiagramm oben auf dem Bildschirm zeigt die relative Wichtigkeit und ordnet sie der Punktfarbe neben den Attributen in der Tabelle zu. Sie können auch mit dem Mauszeiger über eine Farbe im Balkendiagramm fahren, um das Attribut anzuzeigen, für das sie steht.  Die Bewertungen der wichtigsten Attribute ergeben zusammen 100 %. Weitere Informationen zum Hinzufügen weiterer Attribute, die die Target-Personalisierungsmodelle verwenden können, finden Sie unter [Hochladen von Daten für die Personalization-Algorithmen von Target](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md). |
| Diagramm „Modell-Attribut-Ranking“ | Das Diagramm „Modell-Attribut-Ranking“ enthält die 10 Attribute, die für die Entscheidung des Target-Personalisierungsmodells, welche Inhalte welchem Besucher angezeigt werden sollen, am wichtigsten waren. Die Bewertung zeigt, wie wichtig ein bestimmter Wert (im Verhältnis zu den 100 wichtigsten Attributen) für die Target-Personalisierungsmodelle in dieser Aktivität waren. |

## Häufig gestellte Fragen zu wichtigen Attributen {#section_740910A52FA646B4AC9452F98C2F5719}

Antworten auf häufig gestellte Fragen zur Verwendung des Berichts [!UICONTROL Important Attributes] finden Sie in den folgenden häufig gestellten Fragen.

### Personalization Insights-Berichte sind noch nicht für meine Aktivität verfügbar. Warum ist das?

Es gibt verschiedene Gründe, warum die [!UICONTROL Personalization Insights] -Berichte noch nicht für Ihre Aktivität verfügbar sind:

* Es sind noch keine 15 Tage seit Aktivierung der Aktivität vergangen. Die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ sind erst 15 Tage nach der Aktivierung der Aktivität verfügbar. Bis dahin können Sie nicht auf diese Berichte zugreifen und die Symbole für „Automatisierte Segmente“ und „Wichtige Attribute“ sind ausgegraut.
* Ihre Aktivität bietet nicht ausreichend Traffic im angegebenen Zeitraum. Nach 15 Tagen und sofern [ausreichend Personalisierungstraffic](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB) in Ihrer Aktivität verfügbar ist, um die Personalisierungsmodelle zu erstellen, sind die Berichte „Automatisierte Segmente“ und „Wichtige Attribute“ verfügbar.
* Ihre Aktivität verfügt über ein Ziel zur Umsatzoptimierung. Derzeit ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Wir werden die Unterstützung von Umsatzoptimierungszielen in einer künftigen Version ergänzen.

### Was ist ein Attribut?

Ein Attribut ist eine Information zu einem Besucher oder seinem spezifischen Besuch, die von den Personalisierungsalgorithmen verwendet wird, um die Traffic-Personalisierung anzupassen. Bei einem Attribut kann es sich beispielsweise um den Browsertyp, den Standort, die Uhrzeit des Besuchs usw. handeln.

Weitere Informationen zu den Attributen, die [!DNL Target] in seinen Personalisierungsmodellen nutzt, finden Sie unter [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Weitere Informationen zum Hochladen neuer Attribute in Target zur Verwendung in den Target-Personalisierungsmodellen finden Sie unter [Verfahren für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}.

### Ich sehe ein oder mehrere Attribute, die das Modell nicht für das Training verwenden soll. Kann ich diese Attribute aus dem Trainings-Modell entfernen? {#models-api}

Mit der [!UICONTROL Models API] -API, die auch als Blockierungsliste-API bezeichnet wird, können Benutzer die Liste der Attribute (auch als Funktionen bezeichnet) anzeigen und verwalten, die in Modellen für maschinelles Lernen für [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Auto-Target] (AT)-Aktivitäten verwendet werden. Wenn Sie ein oder mehrere Attribute von der Verwendung durch die Modelle für AP- oder AT-Aktivitäten ausschließen möchten, können Sie die Modelle-API verwenden, um diese Attribute zur &quot;Blockierungsliste&quot;hinzuzufügen.

Detaillierte Informationen finden Sie unter [Übersicht der Modelle-API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} im *Adobe Target-Entwicklerhandbuch*. Informationen zur Verwendung der API zum Blockieren von Attributen finden Sie unter [Modelle-API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api-overview.html){target=_blank}.

### Entsprechen die Informationen in den Berichten [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] den Informationen im CSV-Download?

Nein. Der UI-Bericht enthält ausgewählte Informationen. Der CSV-Download enthält zusätzliche Details. Der Download des Insights-Berichts „Automatisierte Segmente“ enthält im Vergleich zu den Segmenten in der Benutzeroberfläche zusätzliche automatisierte Segmente sowie Informationen zu ihrer Performance in Ihren Angeboten oder Erlebnissen. Der Bericht „Wichtige Attribute“ enthält die 100 wichtigsten Besucherattribute und ihre relative Wichtigkeit, während in der UI nur die 10 wichtigsten Besucherattribute angezeigt werden.

### Kann ich Personalization Insights für einen benutzerdefinierten Datumsbereich anzeigen?

Die Personalization Insights-Berichterstellung (sowohl [!UICONTROL Automated Segments] als auch [!UICONTROL Important Attributes]) ist nur für feste Datumsbereiche verfügbar: 15 Tage, 30 Tage, 45 Tage, 60 Tage und 90 Tage. Diese festen Datumsbereiche ermöglichen es [!UICONTROL Personalization Insights], einen ausreichend großen Datenbereich zu verwenden, um die Wahrscheinlichkeit zu verringern, dass Sie Einblicke aus einem kurzlebigen Muster in Ihrer Aktivität gewinnen. Sie können diese Zeiträume mit einem beliebigen Enddatum festlegen (sofern hierfür ausreichend Daten in der Aktivität vorhanden sind).

### Wie wird [!UICONTROL Personalization Insights] erstellt?

[!UICONTROL Personalization Insights] wird mit einer patentierten Adobe-Technik namens MAGIX (Model Agnostic Globally Interpretable Explanations) erstellt. Weitere Informationen zu MAGIX finden Sie in der veröffentlichten Publikation des Adobe-Forschungsteams auf der [arXiv.org Website](https://arxiv.org/abs/1706.07160).

### Ist [!UICONTROL Personalization Insights] für umsatzbasierte Modellierungsziele/Primärziele verfügbar?

Derzeit ist [!UICONTROL Personalization Insights] nur für Aktivitäten mit Zielen zur Konversionsoptimierung verfügbar. Wir werden die Unterstützung von Umsatzoptimierungszielen in einer künftigen Version ergänzen.

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

### Welche verschiedenen Möglichkeiten gibt es, um die Informationen in Personalization Insights zu nutzen?

* Entdecken Sie neue Zielgruppen für Ihr Targeting: Wenn Sie ein bestimmtes automatisiertes Segment finden, das besonders gut abschneidet, können Sie hieraus eine Zielgruppe erstellen, die Sie als Segment in anderen Berichten verwenden können.
* Testen Sie Thesen dazu, welche Besuchertypen auf welche Erlebnisse reagieren.
* Ermitteln Sie, welche Inhalte für welche Besuchertypen funktionieren: Welche Angebote waren bei welchen Besuchern erfolgreich?
* Ermitteln Sie Gründe für Inhalte mit schlechter Performance.
* Finden Sie heraus, welche Attribute am wichtigsten für das Lernen des Modells waren.
* Ermitteln Sie, welche Attribute in den Personalisierungsmodellen eingesetzt werden und wie wichtig sie sind.
* Finden Sie Möglichkeiten für zusätzliche Datenpunkte, die Sie an Target übergeben können, um die Personalisierung weiter zu optimieren.

## Bekannte Probleme

Das folgende Problem wird derzeit vom [!DNL Target] -Technikerteam untersucht.

* [!DNL Adobe Experience Platform] Segmentnamen werden nicht im [!UICONTROL Important Attributes] -Bericht für die Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] (AT) angezeigt. (Die 3813 populärsten)
