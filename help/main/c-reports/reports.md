---
keywords: Berichte; IP-Adresse blockieren; Besucher von IP-Adresse blockieren; Berichte herunterladen; csv; Reporting
description: Erfahren Sie, wie Sie die Berichterstellungsfunktionen in Adobe verwenden. [!DNL Target] , um die Leistung Ihrer Aktivitäten zu untersuchen. Treffen Sie bessere Entscheidungen basierend auf Ihren Daten, um den ROI zu steigern.
title: Wie kann ich Berichte anzeigen?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: a7a03cba466fbe7abfc8eb1f80292e1a2de7fe2d
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 41%

---

# Berichte

Berichte enthalten Informationen über den Fortschritt und die Ergebnisse Ihrer [!DNL Adobe Target] Aktivitäten, die Ihnen dabei helfen, anhand Ihrer Daten Entscheidungen zu treffen. Berichtsdaten können Ihnen bei der Entscheidung helfen, wann eine Aktivität beendet werden soll, zeigen Ihnen, welches Erlebnis des Angebots der Gewinner ist, und liefern Einblicke oder Erkenntnisse, die Sie benötigen, um die nächsten Aktionen zu bestimmen.

## Bericht anzeigen {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität.

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie Optionen aus dem [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], und [!UICONTROL Activity Source] Dropdown-Listen.

   Sie können beispielsweise [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting] aus dem [!UICONTROL Type] Dropdownliste und [!UICONTROL Live] aus dem [!UICONTROL Status] Dropdownliste, um nur aktive A/B-Tests und Erlebnis-Targeting-Aktivitäten anzuzeigen.

   Die folgende Abbildung zeigt die [!UICONTROL Type] Dropdown-Liste mit zwei ausgewählten Typen: [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting]. Beachten Sie, dass die drei Typen von A/B-Tests (manuell, [automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) und [automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) standardmäßig ausgewählt sind. Sie können einen oder mehrere Typen nach Bedarf aufheben.

   ![Berichte nach Typ filtern](/help/main/c-reports/assets/report_filters-new.png)

1. Klicken Sie auf **[!UICONTROL Reports]** Registerkarte.

   Jeder Bericht enthält eine Legende zum besseren Verständnis des Berichts.

   ![Berichtslegende](/help/main/c-reports/assets/report_menu_bar-new.png)

   Die Legende enthält folgende Informationen:

   * den Aktivitätsstatus, einschließlich des Datumsbereichs, in dem die Aktivität ausgeführt wurde
   * Die [prognostiziertes erfolgreiches Erlebnis](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (sofern verfügbar).

   >[!NOTE]
   >
   >Erlebnisergebnisse werden angezeigt, nachdem mindestens ein Teilnehmer das Erlebnis gesehen hat.

1. (Optional) [Konfigurieren Sie den Bericht](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) nach Bedarf.
1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md), um ihn in Excel und anderen Tools zu analysieren.

   Die folgenden Optionen sind verfügbar:

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (Optional) Klicken Sie auf die **[!UICONTROL Table View]** und **[!UICONTROL Graph View]** Symbole zum Wechseln zwischen Berichtsformaten.

   ![Symbole für Tabellen- und Diagrammansicht](/help/main/c-reports/assets/table-and-graph-icons.png)

   Je nach ausgewähltem Berichtstyp stehen möglicherweise weitere Ansichten und Berichte zur Verfügung:

   | Berichtstyp | Ansicht |
   | --- | --- |
   | [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Klicken Sie auf **[!UICONTROL Automated Segments]** oder **[!UICONTROL Important Attributes]** Symbole.<ul><li>Die [Bericht &quot;Automatisierte Segmente&quot;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) zeigt an, wie verschiedene Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.</li><li>Die [Bericht &quot;Wichtige Attribute&quot;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) zeigt, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Personalisierungsentscheidung des Modells sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.</li></ul> |
   | [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Zusätzlich zu den [Automated Personalization-Zusammenfassungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md)können Sie auf die **[!UICONTROL Automated Segments]** oder **[!UICONTROL Important Attributes]** Symbole.<ul><li>Die [Bericht &quot;Automatisierte Segmente&quot;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) zeigt an, wie verschiedene Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.</li><li>Die [Bericht &quot;Wichtige Attribute&quot;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) zeigt, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Personalisierungsentscheidung des Modells sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.</li></ul> |
   | [Multivariate Tests](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Zusätzlich zu den [Experience Performance-Bericht](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md)können Sie auf die [Location Contribution](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) -Symbol, um den Bericht zu wechseln und den Beitrag nach Ort anzuzeigen. |

## Zusätzliche Berichtsinformationen für bestimmte Aktivitätstypen {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Neben den allgemeinen Reporting-Informationen in diesem Thema und seinen Unterthemen sind folgende zusätzliche Informationen zu den einzelnen Aktivitätstypen in dieser Anleitung verfügbar:

| Aktivitätstyp | Details |
|--- |--- |
| [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) | Informationen zur Steigerung und Konfidenz sowie zu den in [!DNL Target] verwendeten statistischen Konzepten finden Sie unter [Planen eines A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md). |
| [Interpretieren der automatischen Zuordnungsberichte](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretieren der Ergebnisse eines [!UICONTROL Auto-Allocate] A/B-Aktivität durch Untersuchung wichtiger Indikatoren, einschließlich Steigerung und Vertrauen in der [!DNL Target] Benutzeroberfläche. |
| [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informationen über [!UICONTROL Summary] Bericht für AT-Aktivitäten. Weitere Informationen finden Sie unter [Zusammenfassungsbericht für Automatisches Targeting](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br>Informationen über die beiden [!UICONTROL Personalization Insights] Berichte für AT- und AP-Aktivitäten: [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] Bericht. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informationen über die beiden [!UICONTROL Automated Personalization Summary] Berichte für AP-Aktivitäten: [!UICONTROL Activity Level] und [!UICONTROL Offer Level] Bericht. Weitere Informationen finden Sie unter [Automatisierte Personalisierung - Zusammenfassungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).<br>Informationen über die beiden [!UICONTROL Personalization Insights] Berichte für AT- und AP-Aktivitäten: [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] Bericht. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informationen zu den beiden Berichten für MVT-Aktivitäten: [!UICONTROL Experience Performance] und [!UICONTROL Location Contribution] Bericht. Weitere Informationen finden Sie unter [Experience Performance-Bericht (](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) MVT) und [Location Contribution-Bericht](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics als Berichtsquelle für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informationen zur Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target]. Mit A4T erhalten Sie Zugriff auf [!DNL Analytics]-Berichte für Ihre [!DNL Target]-Aktivitäten. Weitere Informationen finden Sie unter [Analytics für Target-Berichterstellung (A4T)](/help/main/c-reports/analytics-for-target-a4t-reporting.md). |
| [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | Informationen zur Integration zwischen [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} und [!DNL Target] bietet leistungsstarke Analyse- und Zeitsparen-Tools für Ihr Optimierungsprogramm. |

## Berichtsdaten von bestimmten IP-Adressen blockieren

Sie können Besucher von bestimmten IP-Adressen für die Aufnahme in Berichten blockieren. Dies ist beispielsweise hilfreich, um Berichtsdaten von Ihren internen Besuchern zu blockieren.

[Kundenunterstützung kontaktieren](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) , um IP-Filter einzurichten. Diese Filterung wird bei Verwendung von [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als Berichtsquelle verwenden.
