---
keywords: Berichte; Herunterladen von Berichten; csv; Erfolgsmetriken; Bestelldetails
description: Erfahren Sie, wie Sie Daten von Adobe herunterladen können. [!DNL Target] Aktivitäten im CVS-Format zum schnellen Import in Excel, Access oder andere Datenanalyseprogramme.
title: Wie lade ich Berichtsdaten in eine CSV-Datei herunter?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: fc1dcc2b6de1248c35191c1ecd7b36aeb891fd3f
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 54%

---

# Herunterladen von Daten in Form einer CSV-Datei

Sie können Daten im .csv-Format herunterladen, um sie schnell in Excel, Access oder andere Datenanalyseprogramme zu importieren.

So laden Sie Daten als CSV-Datei herunter:

1. Klicken Sie auf **[!UICONTROL Aktivitäten]** und dann in der Liste auf die gewünschte Aktivität.

   Sollten Ihnen viele Aktivitäten zur Auswahl stehen, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Berichtsquelle], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Aktivitätsquelle] auswählen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Berichte]**.
1. Klicken Sie auf das Symbol **[!UICONTROL „Herunterladen“]** und wählen Sie einen Berichtstyp aus, den Sie für die Analyse in Excel oder anderen Tools herunterladen möchten.

   * [!UICONTROL Berichte in CSV exportieren]
   * [!UICONTROL Bestelldetails als CSV exportieren]

   ![Download-Optionen](/help/main/c-reports/assets/download-options.png)

## [!UICONTROL Exportieren von Berichten in das CSV-Format] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Die [!UICONTROL Erfolgsmetriken] zeigt Ihnen Informationen über Ihre Erfolgsmetriken und die folgenden Metriken an, die in der Variablen [!DNL Target] Benutzeroberfläche:

* Durchschnittszeit bis zur Konversion in Stunden, sodass Sie sehen können, wie lange ein Besucher im Schnitt braucht, um den Konversionspunkt zu erreichen
* Summe der Erträge im Quadrat zur Offline-Berechnung vor statistischer Genauigkeit

Die Daten werden bis zum Ende der Aktivität gespeichert.

>[!NOTE]
>
>Der CSV-Bericht enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden. Um diese berechneten Metriken zu berechnen, laden Sie die [!DNL Target] [Vollständige Vertrauensberechnung](/help/main/assets/complete_confidence_calculator.xlsx) Excel-Datei zur Eingabe des Aktivitätswerts oder zur Überprüfung [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Bestelldetails als CSV exportieren] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Die [!UICONTROL Bestelldetails] zeigt Ihnen Informationen zu Ihren Bestellungen an, darunter:

* Datum und Uhrzeit der Bestellung
* Bestellmenge (wenn Sie eine Bestellaufgabe-Mbox eingefügt haben)

   Die [!UICONTROL Bestelldetails] funktioniert nur, wenn Sie Bestellungen haben.

* Bestellmarkierung (doppelte oder extreme Bestellungen)

   Eine Bestellung wird als extrem markiert, wenn sie mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert aufweist. Bei dieser Berechnung wird der letzte Monat der Daten verwendet (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde). Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Bestellungen automatisch ausgeschlossen. Weitere Informationen finden Sie unter [Ausschließen extremer Bestellungen](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Produkt-ID

   Die Gesamtlänge von Produkt-IDs, die mit Kommas verknüpft sind, sollte 255 Zeichen nicht überschreiten, da die IDs im Bericht nicht richtig angezeigt werden. Wenn Ihr Auftrag Produkte mit den IDs „aa, bb“ enthält, ist die Gesamtlänge „aa,bb“, also 5 Zeichen.

* Erlebnis

   Im Bericht [!UICONTROL Auftragsdetails] für [!UICONTROL A/B-Test], [!UICONTROL Erlebnis-Targeting] (XT) und [!UICONTROL Multivariate Test]-Aktivitäten (MVT) enthält die Spalte [!UICONTROL Erlebnis] das Erlebnis `localId`. Dies ist die Wert-Ausgabe aus der `$campaign.recipe.id` in Angebots-Token.

   Es gibt keine Spalte [!UICONTROL Erlebnis] für Aktivitäten für [!UICONTROL Automatisierte Personalisierung] (AP). Die bisherige Spalte [!UICONTROL Algorithmusname] wurde durch die Terminologie „Steuerung“ vs. „Angestrebt“ ersetzt, wie in anderen Teilen von [!DNL Target] dargestellt.

   Auf [!UICONTROL Recommendations]-Aktivitäten hat dies keinen Einfluss.

>[!NOTE]
>
>* Zu den Daten des Bestellberichts gehören Daten aus vier Wochen für die Standardumgebung (Hostgruppe) und Daten aus zwei Wochen für alle nicht standardmäßigen Umgebungen.
>* Umsatzmetriken, die auf &quot;[!UICONTROL Anzahl erhöhen und Benutzer in der Aktivität belassen]&quot; protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher getätigt wurde. Alle nachfolgenden Bestellungen erhöhen die Konversionsanzahl, führen jedoch nicht zu RPV/AOV/Sales und sind nicht in der Variablen [!UICONTROL Bestelldetails] Bericht.


## Best Practices  

* Um einen Bestelldatensatz aufzuzeichnen, muss die `orderTotal` -Parameter übergeben werden.
* Werte, die über den `ProductPurchasedId`-Mbox-Parameter weitergegeben wurden, werden im Bestelldetailbericht aufgelistet.
* Best Practice ist, eine `orderID` und `orderTotal`. Dadurch können doppelte Bestellungen automatisch ignoriert werden.

## Einschränkungen  {#section_49B9590904A645B18E694B4EFFFC1DEF}

Die folgenden Informationen gelten für die [!UICONTROL Download] Option:

* Sie können beide Berichte herunterladen für [!UICONTROL A/B-Test], [!UICONTROL Automated Personalization], [!UICONTROL Erlebnis-Targeting]und [!UICONTROL Multivarianz] Aktivitäten. Sie können die [!UICONTROL Erfolgsmetriken] Bericht für [!UICONTROL Recommendations] Aktivitäten.
* Die [!UICONTROL Download] ist nicht verfügbar für [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] Aktivitäten, die vor [!DNL Target] Version 15.7.1 (Juli 2015).
* Erlebnisse ohne verknüpfte Daten werden im heruntergeladenen Bericht nicht erfasst.
* In der [!DNL Target] Die Reporting-Benutzeroberfläche wird nicht in den Download-Bericht übertragen.
* Berichte, die als CSV-Dateien zum Herunterladen generiert wurden, sind nicht konsistent, wenn die Aktivität mehr als eine Metrik verwendet. Der herunterladbare Bericht wird nur auf der Grundlage der Berichtseinstellungen generiert und geht bei allen anderen verwendeten Metriken von demselben Wert aus. Der korrekte Bericht ist immer der in der Benutzeroberfläche von [!DNL Target] angezeigte Bericht.
