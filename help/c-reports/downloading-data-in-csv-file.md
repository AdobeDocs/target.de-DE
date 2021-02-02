---
keywords: Berichte; Herunterladen von Berichten; csv; Erfolgsmetriken; Bestelldetails
description: Laden Sie Daten im .csv-Format herunter, um sie schnell in Excel, Access oder andere Programm zur Analyse von Daten mit Adobe Target zu importieren.
title: Herunterladen von Daten in einer CSV-Datei
feature: Reports
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 83%

---


# Herunterladen von Daten in Form einer CSV-Datei{#downloading-data-in-a-csv-file}

Sie können Daten im .csv-Format herunterladen, um sie schnell in Excel, Access oder andere Datenanalyseprogramme zu importieren.

So laden Sie Daten als CSV-Datei herunter:

1. Klicken Sie auf **[!UICONTROL Aktivitäten]** und dann in der Liste auf die gewünschte Aktivität.

   Sollten Ihnen viele Aktivitäten zur Auswahl stehen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Berichtsquelle], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Aktivitätsquelle] auswählen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Berichte]**.
1. Klicken Sie auf das Symbol **[!UICONTROL „Herunterladen“]** und wählen Sie einen Berichtstyp aus, den Sie für die Analyse in Excel oder anderen Tools herunterladen möchten.

   * [!UICONTROL Berichte in CSV exportieren]
   * [!UICONTROL Bestelldetails als CSV exportieren]

   ![Download-Optionen](/help/c-reports/assets/download-options.png)

## Exportieren von Berichten in das CSV-Format {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Im Erfolgsmetrikbericht finden Sie Informationen zu Ihren Erfolgsmetriken sowie zu folgenden Metriken, die nicht in der Benutzeroberfläche von Target zur Verfügung stehen:

* Durchschnittszeit bis zur Konversion in Stunden, sodass Sie sehen können, wie lange ein Besucher im Schnitt braucht, um den Konversionspunkt zu erreichen
* Summe der Erträge im Quadrat zur Offline-Berechnung vor statistischer Genauigkeit

Die Daten werden bis zum Ende der Aktivität gespeichert.

>[!NOTE]
>
>Der CSV-Bericht enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden. Um diese berechneten Metriken zu berechnen, laden Sie die Excel-Zielgruppe [Complete Confidence Calculator](/help/assets/complete_confidence_calculator.xlsx) herunter, um den Wert der Aktivität einzugeben, oder überprüfen Sie die [statistischen Berechnungen, die von Zielgruppe](/help/assets/statistical-calculations.pdf) verwendet werden.

## Bestelldetails als CSV exportieren {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Der Bericht &quot;Bestelldetails&quot;enthält Informationen zu Ihren Bestellungen, darunter:

* Datum und Uhrzeit der Bestellung
* Bestellmenge (wenn Sie eine Bestellaufgabe-Mbox eingefügt haben)

   Der Bestellbericht funktioniert nur, wenn Sie über Bestellungen verfügen.

* Bestellmarkierung (doppelte oder extreme Bestellungen)

   Eine Bestellung wird als extrem gekennzeichnet, wenn in den Daten des letzten Monats mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert vorliegen (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde). Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Bestellungen automatisch ausgeschlossen. Weitere Informationen finden Sie unter [Ausschließen extremer Bestellungen](/help/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Produkt-ID

   Die Gesamtlänge von Produkt-IDs (mit Kommas verknüpft) sollte 255 Zeichen nicht überschreiten, damit die IDs korrekt im Bericht angezeigt werden. Wenn Ihr Auftrag Produkte mit den IDs „aa, bb“ enthält, ist die Gesamtlänge „aa,bb“, also 5 Zeichen.

* Erlebnis

   Im Bericht [!UICONTROL Auftragsdetails] für [!UICONTROL A/B-Test], [!UICONTROL Erlebnis-Targeting] (XT) und [!UICONTROL Multivariate Test]-Aktivitäten (MVT) enthält die Spalte [!UICONTROL Erlebnis] das Erlebnis `localId`. Dies ist die Wert-Ausgabe aus der `$campaign.recipe.id` in Angebots-Token.

   Es gibt keine Spalte [!UICONTROL Erlebnis] für Aktivitäten für [!UICONTROL Automatisierte Personalisierung] (AP). Die bisherige Spalte [!UICONTROL Algorithmusname] wurde durch die Terminologie „Steuerung“ vs. „Angestrebt“ ersetzt, wie in anderen Teilen von [!DNL Target] dargestellt.

   Auf [!UICONTROL Recommendations]-Aktivitäten hat dies keinen Einfluss.

>[!NOTE]
>
>* Zu den Daten des Bestellberichts gehören Daten aus vier Wochen für die Standardumgebung (Hostgruppe) und Daten aus zwei Wochen für alle nicht standardmäßigen Umgebungen.
>* Umsatzmetriken, die auf „Anzahl inkrementieren und Benutzer in der Aktivität beibehalten“ festgelegt sind, protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher aufgegeben wurde. Alle nachfolgenden Bestellungen erhöhen die Anzahl Konversionen, steigern den Umsatz von RPV/AOV/Vertrieb jedoch nicht und werden nicht in den Bestelldetailbericht aufgenommen.


## Best Practices

* Zur Aufzeichnung eines Bestelldatensatzes muss der `orderTotal`-Parameter weitergegeben werden.
* Werte, die über den `ProductPurchasedId`-Mbox-Parameter weitergegeben wurden, werden im Bestelldetailbericht aufgelistet.
* Best Practice ist, eine `orderID` sowie eine `orderTotal` aufzunehmen. Dadurch können doppelte Bestellungen automatisch ignoriert werden.

## Einschränkungen   {#section_49B9590904A645B18E694B4EFFFC1DEF}

Die folgenden Informationen gelten für den Download:

* Sie können Berichte für A/B-Tests, Automated Personalization-, Erlebnis-Targeting- und Multivarianz-Aktivitäten herunterladen. Sie können jedoch keinen Erfolgsmetrikenbericht für Recommendations-Aktivitäten herunterladen.
* Die Option zum Herunterladen steht nicht für A/B- und Erlebniszielaktivitäten zur Verfügung, die vor der Target-Version 15.7.1 (Juli 2015) erstellt wurden.
* Erlebnisse ohne verknüpfte Daten werden im heruntergeladenen Bericht nicht erfasst.
* In der Reporting-Benutzeroberfläche von Target angewendete Zielgruppen werden nicht in den Download-Bericht übertragen.
