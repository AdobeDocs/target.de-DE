---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe „Analytics for Target“ (A4T) ist eine lösungsübergreifende Integration, die Ihnen das Erstellen von Aktivitäten ermöglicht, die auf Konversionsmetriken und Zielgruppensegmenten aus Analytics basieren. Dank dieser Integration können Sie Ihre Ergebnisse anhand von Analytics-Berichten überprüfen. Wenn Sie Analytics als Berichterstellungsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf der Analytics-Datenerfassung.
title: Adobe Analytics als Berichtsquelle für Adobe Target (A4T)
feature: null
subtopic: Integrating
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1257'
ht-degree: 46%

---


# Adobe Analytics als Berichtsquelle für Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

[!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Sie Aktivitäten auf der Grundlage von [!DNL Analytics] Konversionsmetriken und Audiencen erstellen können. The A4T integration lets you use [!DNL Analytics] reports to examine your results. If you use [!DNL Analytics] as the reporting source for an activity, all reporting and segmentation for that activity is based on [!DNL Analytics] data collection.

## A4T – Überblick {#section_92B66069210C40DBA937790E8CC596CF}

The [!DNL Analytics for Target] integration between [!DNL Analytics] and [!DNL Target] provides powerful analysis and timesaving tools for your optimization program.

The three primary benefits of using [!DNL Analytics] data in [!DNL Target] are:

* Marketers can dynamically apply [!DNL Analytics] success metrics or reporting segments to [!DNL Target] activity reports at any time. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Da alle Daten aus einer einzigen Quelle stammen, sind keine Schwankungen zu erwarten, die bei der Erfassung von Daten in zwei separaten Systemen auftreten würden.
* Your existing [!DNL Analytics] implementation collects all required data. Es ist nicht notwendig, Mboxes ausschließlich für das Erfassen von Daten für Berichte auf Seiten zu implementieren. Although, it is still recommended that you implement an order confirmation mbox for [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activities.

>[!IMPORTANT]
>
>Bevor Sie A4T verwenden können, müssen Sie eine Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie [dieses Formular](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.
>
>The integration that enables [!DNL Analytics] as the data source for [!DNL Target] (A4T) represents the next generation of the Test&amp;Target to SiteCatalyst plug-in. Dieses Plugin ist veraltet, es wird aber nach wie vor für Kunden unterstützt, die es bereits verwenden.

If you use [!DNL Analytics] as the reporting source for an activity, all reporting and segmentation for that activity is based on [!DNL Analytics].

All [!DNL Analytics] metrics, including calculated metrics, are available in [!DNL Target] and the [!UICONTROL Target Activities] report in [!DNL Analytics]. Likewise, any segment available in [!DNL Analytics] can be applied to both solutions. You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the activity has completed.

Every metric is included, including any customer or calculated metrics that are built-in in [!DNL Analytics].

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn Sie über einen Einsatz von A4T nachdenken, sollten Sie die folgenden Punkte beachten:

* To use [!DNL Analytics] as the reporting source for [!DNL Target], both you and your company must have access to [!DNL Analytics] and to [!DNL Target]. [Wenden Sie sich an Ihren Kundenvertreter,](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) wenn Sie eine der beiden Lösungen benötigen.
* Die Berichtsquelle wird für jede Aktivität festgelegt. [!DNL Target] erfasst weiterhin Daten, die in Berichte verwendet werden sollen, und [!DNL Target] Daten sind weiterhin verfügbar, wenn Sie eine Aktivität lieber auf Daten stützen möchten, die von [!DNL Target].
* Sie können nur eine der beiden Berichtsquellen verwenden. Sie können für eine einzelne Aktivität nicht Daten aus beiden Quellen erfassen.
* When using A4T, all success metrics available to your activities are [!DNL Analytics] metrics. Ihre Zielmetrik kann jedoch auf einem Mbox-Abruf basieren. For example, you can use Target&#39;s out-of-the-box click-tracking capabilities with A4T instead of having to implement [!DNL Analytics] click-tracking code.
* When viewing reporting of an A4T activity in the [!DNL Target] UI, you are viewing [!DNL Analytics] data. For example, if you use the [!UICONTROL Visitor] metric in [!DNL Target], you are using the [!DNL Analytics] [!UICONTROL Visitor] metric, not the [!DNL Target] [!UICONTROL Visitors] metric, which is now called [!UICONTROL Entrants]. This difference is especially important for basic traffic metrics ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) and conversion metrics.
* Any existing [!DNL Target] activities continue to use [!DNL Target] data collection and are not affected by enabling A4T.
* Only one mbox-based metric is allowed when using [!DNL Analytics] as the reporting source.
* A server-to-server call from [!DNL Target] to [!DNL Analytics] sends activity and experience information to [!DNL Analytics]. This integration does not result in additional server calls for either [!DNL Target] or [!DNL Analytics].

   In some situations, the classification call from [!DNL Target] to [!DNL Analytics] might fail and activities do not show data in [!DNL Analytics]. If this happens, see [Troubleshoot the Analytics and Target integration (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). You can also [contact Client Care](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) for further assistance.

## Supported activity types {#section_F487896214BF4803AF78C552EF1669AA}

The following table shows you which activity types support [!DNL Analytics] as the reporting source in [!DNL Target] (A4T):

| Aktivitätstypen | Kompatibel mit A4T? | Anmerkungen (falls zutreffend) |
|--- |--- |--- |
| A/B-Aktivität mit manueller Traffic-Aufteilung | Ja |  |
| A/B-Aktivität mit automatisierter Zuordnung | Ja | See [Analytics for Target (A4T) support for Auto-Allocate activities](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| A/B-Aktivität mit automatischem Targeting | Nein |  |
| Erlebnis-Targeting (XT) | Ja |  |
| Multivarianz-Tests (MVT) | Ja | Requires mbox-based goal metric goal to get the [!UICONTROL Element Contribution] report.  The [!UICONTROL Element Contribution] report does not currently support [!DNL Analytics] metrics. |
| AP-Aktivität (Automatisierte Personalisierung) | Nein |  |
| Recommendations-Aktivität | Ja |  |
| Mobile App | Ja | Wird unterstützt mit dem Mobile Services SDK, Version 4.13.1 (oder neuer).  Weitere Informationen finden Sie in der [Dokumentation zu Mobile Services](https://docs.adobe.com/content/help/en/mobile-services/using/home.html). |
| E-Mail | Nein |  |
| API für serverseitige Bereitstellung | Ja | Weitere Informationen finden Sie unter [Serverseitig: Target implementieren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| NodeJS-SDK | Ja | Weitere Informationen finden Sie unter [Serverseitig: Target implementieren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| AEM 6.1 (oder früher) Cloud Service Integration | Nein |  |
| AEM 6.2 (oder neuer) Cloud Service Integration | Ja | For more information, see [Integrating with Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in the [!DNL Adobe Experience Manager] 6.2 documentation. |
| Jede Aktivität mit einem Umleitungs-Angebot | Ja | Die Mindestanforderungen für die Verwendung von Weiterleitungsangeboten mit A4T sind strenger. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Ja |  |

Because all activity types do not yet support A4T, it is recommended that you keep or implement important conversion mboxes, such as the `orderConfirmPage` mbox.

## Examples of A4T reports {#section_F0A43A1CB2F04E8282B909E4D7034361}

To view A4T reports in [!DNL Target], click **[!UICONTROL Activities]**, click the desired activity from the list that uses [!DNL Analytics] as its reporting source, then click the **[!UICONTROL Reports]** tab.

>[!NOTE]
>
>Sie können oben auf der Seite [!UICONTROL Aktivitäten] die Dropdown-Liste [!UICONTROL Berichtsquelle] nutzen, um nur Aktivitäten anzuzeigen, die [!DNL Analytics] als Berichtsquelle verwenden.

You can toggle between the [!UICONTROL Table View] and [!UICONTROL Graph View] of the report by clicking the appropriate icon at the top right side of the report.

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Berichtsmetrik], in der die verfügbaren [!DNL Analytics]-Zielmetriken aufgeführt sind:

![](assets/a4t_report_graph1.png)

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Zielgruppe], in der die verfügbaren [!DNL Analytics]-Zielgruppen aufgeführt sind:

![](assets/a4t_report_graph2.png)

Die folgende Abbildung zeigt die [!UICONTROL Tabellenansicht] eines A4T-Berichts:

![](assets/a4t_report_table.png)

Um den Bericht in [!DNL Analytics] statt in [!DNL Target] anzuzeigen, klicken Sie oben im Bericht auf **[!UICONTROL In Analytics anzeigen]**.

## Analytics und Target: Tutorial „Best Practices für Analysen“{#section_3438E6E77A464424B717A4FD333B84B2}

Open the [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, provided by [!DNL Adobe Experience League].

## Schulungsvideos:

Die folgenden Videos enthalten weitere Informationen zu den in diesem Thema behandelten Konzepten.

### Analytics for Target (A4T) (4:32) ![Overview badge](/help/assets/overview.png)

This video explains how to use [!DNL Analytics] as a reporting source in [!DNL Target] to drive the analysis of your optimization program.

* Erläuterung: Was ist A4T und wozu dient es?
* Erläuterung der Funktionsweise von A4T
* Verstehen der Voraussetzungen für die Verwendung von A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics / Target Integration (A4T) (40:33) ![Tutorial badge](/help/assets/tutorial.png)

Dieses Video ist eine Aufzeichnung von [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), eine Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* So richten Sie die Integration ein und überprüfen, ob sie funktioniert
* So funktioniert die Integration
* Erfahren Sie, welche Berichte Sie in Analytics am besten verwenden
* Antworten auf häufige Fragen zu A4T

[Ambulanzzeiten für Analytics/Zielgruppe-Integration (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)