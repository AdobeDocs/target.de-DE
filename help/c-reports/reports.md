---
keywords: reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Berichte enthalten Informationen zur Leistung Ihrer Adobe Target-Aktivitäten
title: Berichte
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 66%

---


# Berichte{#reports}

Berichte enthalten Informationen über den Fortschritt und die Ergebnisse Ihrer [!DNL Adobe Target]-Aktivitäten, die Ihnen helfen, anhand Ihrer Daten Entscheidungen zu treffen. Berichtsdaten können Ihnen dabei helfen, zu entscheiden, wann eine Aktivität beendet werden soll, Ihnen zeigen, welches Erlebnis mit Angebot am erfolgreichsten ist, und Einblicke oder Lernprozesse liefern, die Sie zur Festlegung der nächsten Aktionen benötigen.

## Bericht {#section_C4591A32F6D04C95A1AD5A377C27C28B} anzeigen

1. Klicken Sie auf **[!UICONTROL Aktivitäten]** und dann in der Liste auf die gewünschte Aktivität.

   Sollten Ihnen viele Aktivitäten zur Auswahl stehen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Berichtsquelle], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Aktivitätsquelle] auswählen.

   Beispielsweise können Sie die Optionen [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] aus der Dropdownliste [!UICONTROL Typ] auswählen sowie [!UICONTROL Live] aus der Liste [!UICONTROL Status], um ausschließlich aktive Aktivitäten mit A/B-Tests und Erlebnis-Targeting anzuzeigen.

   Die folgende Abbildung zeigt die Dropdownliste [!UICONTROL Typ] mit zwei ausgewählten Typen:   [!UICONTROL A/B-] Tests und  [!UICONTROL Erlebnis-Targeting]. Beachten Sie, dass die drei Typen von A/B-Tests (manuell, [automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) und [automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md)) standardmäßig ausgewählt sind. Sie können einen oder mehrere Typen nach Bedarf aufheben.

   ![Berichte nach Typ filtern](/help/c-reports/assets/report_filters-new.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Berichte]**.

   Jeder Bericht enthält eine Legende zum besseren Verständnis des Berichts.

   ![Berichtslegende](/help/c-reports/assets/report_menu_bar-new.png)

   Die Legende enthält folgende Informationen:

   * den Aktivitätsstatus, einschließlich des Datumsbereichs, in dem die Aktivität ausgeführt wurde
   * Das [projizierte erfolgreichste Erlebnis](/help/c-activities/automated-traffic-allocation/determine-winner.md) (falls verfügbar).

   >[!NOTE]
   >
   >Erlebnisergebnisse werden angezeigt, nachdem mindestens ein Teilnehmer das Erlebnis gesehen hat.

1. (Optional) [Konfigurieren Sie den Bericht](/help/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) nach Bedarf.
1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](/help/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75), um ihn in Excel und anderen Tools zu analysieren.

   Die folgenden Optionen sind verfügbar:

   * [!UICONTROL Exportieren von Berichten in das CSV-Format]
   * [!UICONTROL Bestelldetails als CSV exportieren]

1. (Optional) Klicken Sie auf das Symbol für die **[!UICONTROL Tabellenansicht]** oder die **[!UICONTROL Diagrammansicht]**, um zwischen den Berichtsformaten zu wechseln.

   ![Symbole für die Ansicht von Tabellen und Diagrammen](/help/c-reports/assets/table-and-graph-icons.png)

   Je nach ausgewähltem Berichtstyp stehen ggf. weitere Ansichten und Berichte zur Verfügung:

   | Berichtstyp | Ansicht |
   | --- | --- |
   | [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md) | Klicken Sie auf die Symbole **[!UICONTROL Automatisierte Segmente]** oder **[!UICONTROL Wichtige Attribute]**.<ul><li>Der Bericht [Automatisierte Segmente](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) zeigt an, wie verschiedene Besucher unterschiedlich auf die Angebot/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.</li><li>Der Bericht [Wichtige Attribute](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) zeigt an, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Art und Weise sind, wie das Modell sich für die Personalisierung entscheidet. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.</li></ul> |
   | [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Zusätzlich zu den [Automated Personalization-Zusammenfassungsberichten](/help/c-reports/reports-ap.md) können Sie auf die Symbole **[!UICONTROL Automatisierte Segmente]** oder **[!UICONTROL Wichtige Attribute]** klicken.<ul><li>Der Bericht [Automatisierte Segmente](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) zeigt an, wie verschiedene Besucher unterschiedlich auf die Angebot/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.</li><li>Der Bericht [Wichtige Attribute](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) zeigt an, wie verschiedene Aktivitäten für die Art und Weise, wie das Modell personalisiert werden soll, mehr oder weniger wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.</li></ul> |
   | [Multivarianz-Tests](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Zusätzlich zum Bericht [Erlebnisleistung](/help/c-reports/experience-performance-report.md) können Sie auf das Symbol [Location Contribution](/help/c-reports/location-contribution-report.md) klicken, um den Bericht zu wechseln und den Beitrag nach Ort anzuzeigen. |

## Zusätzliche Berichte-Informationen für bestimmte Aktivitäten {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Neben den allgemeinen Reporting-Informationen in diesem Thema und seinen Unterthemen sind folgende zusätzliche Informationen zu den einzelnen Aktivitätstypen in dieser Anleitung verfügbar:

| Aktivitätstyp | Details |
|--- |--- |
| [A/B-Test](/help/c-activities/t-test-ab/test-ab.md) | Informationen zur Steigerung und Konfidenz sowie zu den in [!DNL Target] verwendeten statistischen Konzepten finden Sie unter [Planen eines A/B-Tests](/help/c-activities/t-test-ab/sample-size-determination.md). |
| [Berichte zur automatischen Zuordnung interpretieren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Interpretieren Sie die Ergebnisse einer [!UICONTROL Auto-Zuordnung] A/B-Aktivität, indem Sie wichtige Indikatoren, einschließlich Steigerung und Konfidenz, in der [!DNL Target]-Benutzeroberfläche untersuchen. |
| [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) | Informationen zum [!UICONTROL Zusammenfassungsbericht] für AT-Aktivitäten. Weitere Informationen finden Sie unter [Zusammenfassungsbericht für Automatisches Targeting](/help/c-reports/auto-target-summary-report.md).<br>Informationen zu den beiden [!UICONTROL Personalization Insights]-Berichten für AT- und AP-Aktivitäten: Bericht für [!UICONTROL Automatisierte Segmente] und Bericht für [!UICONTROL Wichtige Attribute]. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informationen zu den zwei [!UICONTROL Zusammenfassungsberichten zur automatisierten Personalisierung] für AP-Aktivitäten: [!UICONTROL Aktivitätsstufenbericht] und [!UICONTROL Angebotsstufenbericht]. Weitere Informationen finden Sie unter [Automatisierte Personalisierung - Zusammenfassungsberichte](/help/c-reports/reports-ap.md).<br>Informationen zu den beiden [!UICONTROL Personalization Insights]-Berichten für AT- und AP-Aktivitäten: Bericht für [!UICONTROL Automatisierte Segmente] und Bericht für [!UICONTROL Wichtige Attribute]. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Multivarianz-Tests](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informationen zu den beiden Berichten für MVT-Aktivitäten: [!UICONTROL Experience Performance]-Berichte und [!UICONTROL Location Contribution]-Bericht. Weitere Informationen finden Sie unter [Experience Performance-Bericht (](/help/c-reports/experience-performance-report.md) MVT) und [Location Contribution-Bericht](/help/c-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics als Berichtsquelle für Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informationen zur Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target]. Mit A4T erhalten Sie Zugriff auf [!DNL Analytics]-Berichte für Ihre [!DNL Target]-Aktivitäten. Weitere Informationen finden Sie unter [Analytics für Target-Berichterstellung (A4T)](/help/c-reports/analytics-for-target-a4t-reporting.md). |

## Blockieren von Berichte-Daten aus bestimmten IP-Adressen

Sie können Besucher von bestimmten IP-Adressen für die Aufnahme in Berichten blockieren. Dies ist beispielsweise hilfreich, um Berichte-Daten von Ihren internen Besuchern zu blockieren.

[Wenden Sie sich an ClientCare, um IP-Filter einzurichten. ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Diese Filterung wird nicht angewendet, wenn Sie  [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als Berichtsquelle verwenden.
