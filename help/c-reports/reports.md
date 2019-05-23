---
description: Berichte enthalten Informationen zur Performance Ihrer Aktivitäten.
keywords: Berichte; IP-Adresse blockieren; Besucher von IP-Adresse blockieren; Herunterladen von Berichten; csv
seo-description: Berichte enthalten Informationen zur Performance Ihrer Aktivitäten
seo-title: Berichte
solution: Target
subtopic: Multivarianz-Test
title: Berichte
topic: Standard
uuid: 8d20f4e7-72fd-4872-a21f-54ce16a2d2ab
translation-type: tm+mt
source-git-commit: 385864d9daae19468c4557e51043d5b788924658

---


# Berichte{#reports} 

Berichte enthalten Informationen über den Fortschritt und die Ergebnisse Ihrer Aktivitäten, die Ihnen bei der Entscheidungsfindung auf Grundlage Ihrer Daten helfen. Mit Berichtsdaten können Sie entscheiden, wann ein Test beendet werden soll, Sie sehen, welches Erlebnis ein Gewinner ist, und Einblicke oder Lernmöglichkeiten bereitstellen, um die nächsten Aktionen zu bestimmen.

>[!NOTE]
>
>Sie können Besucher von bestimmten IP-Adressen für die Aufnahme in Berichten blockieren. Wenden Sie sich an ClientCare, um IP-Filter einzurichten. Diese Filterung wird nicht angewendet, wenn Sie   [Analytics for Target](../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) als Berichtsquelle verwenden.

## Berichtsinformationen für bestimmte Aktivitätstypen {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

Neben den allgemeinen Reporting-Informationen in diesem Thema und seinen Unterthemen sind folgende zusätzliche Informationen zu den einzelnen Aktivitätstypen in dieser Anleitung verfügbar:

| Aktivitätstyp | Details |
|--- |--- |
| [A/B-Test](/help/c-activities/t-test-ab/test-ab.md) | Informationen zur Steigerung und Konfidenz sowie zu den in [!DNL Target] verwendeten statistischen Konzepten finden Sie unter [Planen eines A/B-Tests](/help/c-activities/t-test-ab/sample-size-determination.md). |
| [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md) (AT) | Informationen zum [!UICONTROL Zusammenfassungsbericht] für AT-Aktivitäten. Weitere Informationen finden Sie unter [Zusammenfassungsbericht für Automatisches Targeting](/help/c-reports/auto-target-summary-report.md).<br>Informationen zu den beiden [!UICONTROL Personalization Insights]-Berichten für AT- und AP-Aktivitäten: Bericht für [!UICONTROL Automatisierte Segmente] und Bericht für [!UICONTROL Wichtige Attribute]. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) | Informationen zu den zwei [!UICONTROL Zusammenfassungsberichten zur automatisierten Personalisierung] für AP-Aktivitäten: [!UICONTROL Aktivitätsstufenbericht] und [!UICONTROL Angebotsstufenbericht]. Weitere Informationen finden Sie unter [Automatisierte Personalisierung - Zusammenfassungsberichte](/help/c-reports/reports-ap.md).<br>Informationen zu den beiden [!UICONTROL Personalization Insights]-Berichten für AT- und AP-Aktivitäten: Bericht für [!UICONTROL Automatisierte Segmente] und Bericht für [!UICONTROL Wichtige Attribute]. Weitere Informationen finden Sie unter [Personalization Insights-Berichte](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md). |
| [Multivarianz-Tests](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Informationen zu den beiden Berichten für MVT-Aktivitäten: [!UICONTROL Experience Performance]-Berichte und [!UICONTROL Location Contribution]-Bericht. Weitere Informationen finden Sie unter [Experience Performance-Bericht (](/help/c-reports/experience-performance-report.md) MVT) und [Location Contribution-Bericht](/help/c-reports/location-contribution-report.md) (MVT). |
| [Adobe Analytics als Berichtsquelle für Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Informationen zur Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target]. Mit A4T erhalten Sie Zugriff auf [!DNL Analytics]-Berichte für Ihre [!DNL Target]-Aktivitäten. Weitere Informationen finden Sie unter [Analytics für Target-Berichterstellung (A4T)](/help/c-reports/analytics-for-target-a4t-reporting.md). |

## Anzeigen eines Berichts {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Klicken Sie auf **[!UICONTROL Aktivitäten]** und dann in der Liste auf die gewünschte Aktivität.

   Sollten Ihnen viele Aktivitäten zur Auswahl stehen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Berichtsquelle], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Aktivitätsquelle] auswählen.

   Beispielsweise können Sie die Optionen [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] aus der Dropdownliste [!UICONTROL Typ] auswählen sowie [!UICONTROL Live] aus der Liste [!UICONTROL Status], um ausschließlich aktive Aktivitäten mit A/B-Tests und Erlebnis-Targeting anzuzeigen.

   Die folgende Abbildung zeigt die Dropdownliste [!UICONTROL Typ] mit zwei ausgewählten Typen:

   ![](assets/report_filters.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Berichte].**

   Jeder Bericht enthält eine Legende zum besseren Verständnis des Berichts.

   ![](assets/report_menu_bar.png)

   Die Legende enthält folgende Informationen:

   * den Aktivitätsstatus, einschließlich des Datumsbereichs, in dem die Aktivität ausgeführt wurde
   * das projizierte erfolgreichste Erlebnis
   * Die Quelle der Aktivität, z. B. [!DNL Adobe Target] oder [!DNL Adobe Target Classic].
   >[!NOTE]
   >
   >Erlebnisergebnisse werden angezeigt, nachdem mindestens ein Teilnehmer das Erlebnis gesehen hat.

1. (Optional) [Konfigurieren Sie den Bericht](../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) nach Bedarf.
1. (Optional) [Laden Sie den Bericht im CSV-Format herunter](../c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75), um ihn in Excel und anderen Tools zu analysieren.

   Die folgenden Optionen sind verfügbar:

   * [!UICONTROL Exportieren von Berichten in das CSV-Format]
   * [!UICONTROL Bestelldetails als CSV exportieren]

1. (Optional) Klicken Sie auf das Symbol für die **[!UICONTROL Tabellenansicht]** oder die **Diagrammansicht], um zwischen den Berichtsformaten zu wechseln.[!UICONTROL **

   Klicken Sie nur für Multivarianz-Tests auf den **[!UICONTROL Umgebungseinfluss]** (![Location Contribution-Symbol](assets/icon_location_contribution.png)), um den Bericht zu wechseln und den Einfluss nach Ort anzuzeigen.
