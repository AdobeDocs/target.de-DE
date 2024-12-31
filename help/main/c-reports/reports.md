---
keywords: Berichte;IP-Adresse blockieren;Besucher von IP-Adresse blockieren;Berichte herunterladen;CSV;Berichte
description: Optimieren Sie Ihre Aktivitäten durch  [!DNL Adobe Target] der Reporting-Funktionen von , um die Entscheidungsfindung zu verbessern und den ROI zu steigern.
title: Wie kann ich Berichte anzeigen?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: 5c963e97dae11326396a5c1c5e32d19f4d463c74
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 32%

---

# Berichte

Berichte enthalten Informationen über den Fortschritt und die Ergebnisse Ihrer [!DNL Adobe Target] Aktivitäten, die Ihnen bei datenbasierten Entscheidungen helfen. Berichtsdaten können Ihnen bei der Entscheidung helfen, wann eine Aktivität beendet werden soll, zeigen Ihnen, welches Erlebnis oder Angebot der Gewinner ist, und bieten Einblicke oder Erkenntnisse, die Sie benötigen, um die nächsten Aktionen zu bestimmen.

## Anzeigen eines Berichts {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität.

   Wenn Sie über viele Aktivitäten verfügen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Method] und [!UICONTROL Activity Source] auswählen.

   Sie können beispielsweise [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting] aus der Dropdown-Liste [!UICONTROL Type] und [!UICONTROL Live] aus der Dropdown-Liste [!UICONTROL Status] auswählen, um nur [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting] Aktivitäten anzuzeigen, die sich im aktiven Status befinden.

   Die folgende Abbildung zeigt die Dropdown-Liste [!UICONTROL Type] mit zwei ausgewählten Typen: [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting]. Beachten Sie, dass die drei Typen von A/B-Tests (manuell, [automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) und [automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) standardmäßig ausgewählt sind. Sie können einen oder mehrere Typen nach Bedarf aufheben.

   ![Berichte nach Typ filtern](/help/main/c-reports/assets/report_filters-new.png)

1. Wählen Sie die gewünschte Aktivität aus der Liste aus.

1. Klicken Sie in der linken Leiste auf die Registerkarte **[!UICONTROL Reports]** .

   Jeder Bericht enthält eine Legende zum besseren Verständnis des Berichts.

   Die Legende enthält folgende Informationen:

   * den Aktivitätsstatus, einschließlich des Datumsbereichs, in dem die Aktivität ausgeführt wurde
   * Das [voraussichtliche Gewinnererlebnis](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (falls verfügbar).

   >[!NOTE]
   >
   >Erlebnisergebnisse werden angezeigt, nachdem mindestens ein Teilnehmer das Erlebnis gesehen hat.

1. (Optional) [Konfigurieren Sie den Bericht](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) nach Bedarf.
1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md), um ihn in Excel und anderen Tools zu analysieren.

   Die folgenden Optionen sind verfügbar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Optional) Klicken Sie auf die Symbole **[!UICONTROL Table View]** und **[!UICONTROL Graph View]**, um zwischen Berichtsformaten zu wechseln.

   ![Symbole für Tabellen- und Diagrammansichten](/help/main/c-reports/assets/table-and-graph-icons.png)

   Je nach ausgewähltem Berichtstyp stehen möglicherweise andere Ansichten und Berichte zur Verfügung:

   | Berichtstyp | Ansicht |
   | --- | --- |
   | [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Klicken Sie auf die Symbole **[!UICONTROL Automated Segments]** oder **[!UICONTROL Important Attributes]** .<ul><li>Der [[!UICONTROL Automated Segments] Bericht ](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md), wie verschiedene Besucher unterschiedlich auf die Angebote und Erlebnisse in Ihrer [!UICONTROL Automated Personalization] oder [!UICONTROL Auto-Target] Aktivität reagieren. Dieser Bericht zeigt, wie verschiedene durch die [!DNL Target] Personalisierungsmodelle definierte automatisierte Segmente auf die Angebote und Erlebnisse in der Aktivität reagierten.</li><li>Der [[!UICONTROL Important Attributes] Bericht ](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md), wie verschiedene Attribute in verschiedenen Aktivitäten für die Personalisierungsentscheidung des Modells mehr (oder weniger) wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.</li></ul> |
   | [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Zusätzlich zu den [[!UICONTROL Automated Personalization Summary] können ](/help/main/c-reports/personalization-reports/reports-ap.md) auf die **[!UICONTROL Automated Segments]** oder **[!UICONTROL Important Attributes]** klicken.<ul><li>Der [[!UICONTROL Automated Segments] Bericht ](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md), wie verschiedene Besucher unterschiedlich auf die Angebote und Erlebnisse in Ihrer [!UICONTROL Automated Personalization] oder [!UICONTROL Auto-Target] Aktivität reagieren. Dieser Bericht zeigt, wie verschiedene durch die [!DNL Target] Personalisierungsmodelle definierte automatisierte Segmente auf die Angebote und Erlebnisse in der Aktivität reagierten.</li><li>Der [[!UICONTROL Important Attributes] Bericht ](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md), wie verschiedene Attribute in verschiedenen Aktivitäten für die Personalisierungsentscheidung des Modells mehr (oder weniger) wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.</li></ul> |
   | [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Zusätzlich zum [[!UICONTROL Experience Performance] Bericht können ](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) auf das Symbol [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) klicken, um den Bericht so umzuschalten, dass der Beitrag nach Standort angezeigt wird. |

## Zusätzliche Berichtsdaten zu bestimmten Aktivitätstypen {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Neben den allgemeinen Reporting-Informationen in diesem Thema und seinen Unterthemen sind folgende zusätzliche Informationen zu den einzelnen Aktivitätstypen in dieser Anleitung verfügbar:

| Aktivitätstyp | Details |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | Informationen zur Steigerung und Konfidenz sowie zu den in [!DNL Target] verwendeten statistischen Konzepten finden Sie unter [Planen eines A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpretieren [!UICONTROL Auto-Allocate] Berichte](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretieren Sie die Ergebnisse einer [!UICONTROL Auto-Allocate] A/B-Aktivität, indem Sie wichtige Indikatoren, einschließlich Steigerung und Konfidenz, in der [!DNL Target] Benutzeroberfläche untersuchen. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informationen zum [!UICONTROL Summary] für AT-Aktivitäten. Weitere Informationen finden Sie unter [[!UICONTROL Auto-Target Summary] Bericht](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br>Informationen zu den beiden [!UICONTROL Personalization Insights] für AT- und AP-Aktivitäten: [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes]. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informationen zu den beiden [!UICONTROL Automated Personalization Summary] für AP-Aktivitäten: [!UICONTROL Activity Level] und [!UICONTROL Offer Level]. Weitere Informationen finden Sie unter [Automatisierte Personalisierung - Zusammenfassungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).<br>Informationen zu den beiden [!UICONTROL Personalization Insights] für AT- und AP-Aktivitäten: [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes]. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informationen zu den beiden Berichten über MVT-Aktivitäten: [!UICONTROL Experience Performance] Bericht und [!UICONTROL Location Contribution] Bericht. Weitere Informationen finden Sie unter [Experience Performance-Bericht (](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) MVT) und [Location Contribution-Bericht](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [[!DNL Adobe Analytics] als Reporting-Source für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informationen zur Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target] (A4T). Mit A4T erhalten Sie Zugriff auf [!DNL Analytics]-Berichte für Ihre [!DNL Target]-Aktivitäten. Weitere Informationen finden Sie unter [Analytics für Target-Berichterstellung (A4T)](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informationen zur Integration zwischen [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/customer-journey-analytics){target=_blank} und [!DNL Target], die leistungsstarke Analyse- und Zeitsparungs-Tools für Ihr Optimierungsprogramm bereitstellt. |

## Blockieren von Berichtsdaten aus angegebenen IP-Adressen

Sie können Besucher von bestimmten IP-Adressen für die Aufnahme in Berichten blockieren. Dies ist beispielsweise hilfreich, um Berichtsdaten von internen Besuchern zu blockieren.

[Kundenunterstützung kontaktieren](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) um IP-Filter einzurichten. Diese Filterung gilt nicht, wenn [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als Berichtsquelle verwendet wird.
