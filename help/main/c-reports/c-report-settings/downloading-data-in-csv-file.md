---
keywords: Berichte; Herunterladen von Berichten; csv; Erfolgsmetriken; Bestelldetails
description: Erfahren Sie, wie Sie Daten von Adobe [!DNL Target] Aktivitäten im CVS-Format herunterladen können, um sie schnell in Excel, Access oder andere Datenanalyseprogramme zu importieren.
title: Wie lade ich Berichtsdaten in eine CSV-Datei herunter?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: fc1dcc2b6de1248c35191c1ecd7b36aeb891fd3f
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 37%

---

# Herunterladen von Daten in Form einer CSV-Datei

Sie können Daten im .csv-Format herunterladen, um sie schnell in Excel, Access oder andere Datenanalyseprogramme zu importieren.

So laden Sie Daten als CSV-Datei herunter:

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität.

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie Optionen aus den Dropdownlisten [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf das Symbol **[!UICONTROL Download]** und wählen Sie dann einen Berichtstyp aus, den Sie zur Analyse in Excel oder anderen Tools herunterladen möchten.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

   ![Download-Optionen](/help/main/c-reports/assets/download-options.png)

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Der Bericht [!UICONTROL Success Metrics] zeigt Informationen über Ihre Erfolgsmetriken und die folgenden Metriken an, die nicht in der Benutzeroberfläche von [!DNL Target] verfügbar sind:

* Durchschnittszeit bis zur Konversion in Stunden, sodass Sie sehen können, wie lange ein Besucher im Schnitt braucht, um den Konversionspunkt zu erreichen
* Summe der Erträge im Quadrat zur Offline-Berechnung vor statistischer Genauigkeit

Die Daten werden bis zum Ende der Aktivität gespeichert.

>[!NOTE]
>
>Der CSV-Bericht enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden. Laden Sie zur Berechnung dieser berechneten Metriken die Excel-Datei [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) herunter, um den Aktivitätswert einzugeben, oder überprüfen Sie die [Statistischen Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Der Bericht [!UICONTROL Order Details] zeigt Informationen zu Ihren Bestellungen an, darunter:

* Datum und Uhrzeit der Bestellung
* Bestellmenge (wenn Sie eine Bestellaufgabe-Mbox eingefügt haben)

  Der Bericht [!UICONTROL Order Details] funktioniert nur, wenn Sie Bestellungen haben.

* Bestellmarkierung (doppelte oder extreme Bestellungen)

  Eine Bestellung wird als extrem markiert, wenn sie mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert aufweist. Bei dieser Berechnung wird der letzte Monat der Daten verwendet (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde). Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Bestellungen automatisch ausgeschlossen. Weitere Informationen finden Sie unter [Ausschließen extremer Bestellungen](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Produkt-ID

  Die Gesamtlänge von Produkt-IDs, die mit Kommas verknüpft sind, sollte 255 Zeichen nicht überschreiten, da die IDs im Bericht nicht richtig angezeigt werden. Wenn Ihr Auftrag Produkte mit den IDs „aa, bb“ enthält, ist die Gesamtlänge „aa,bb“, also 5 Zeichen.

* Erlebnis

  Im Bericht [!UICONTROL Order Details] für die Aktivitäten [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT) und [!UICONTROL Multivariate Test] (MVT) enthält die Spalte [!UICONTROL Experience] das Erlebnis `localId`. Dies ist die Wert-Ausgabe aus der `$campaign.recipe.id` in Angebots-Token.

  Es gibt keine [!UICONTROL Experience] -Spalte für [!UICONTROL Automated Personalization] -Aktivitäten (AP). Die aktuelle Spalte [!UICONTROL Algorithm Name] wurde durch die Terminologie &quot;Kontrolle&quot;versus &quot;Zielgruppe&quot;ersetzt, wie an anderer Stelle in [!DNL Target] gezeigt.

  Auf [!UICONTROL Recommendations] -Aktivitäten hat dies keinen Einfluss.

>[!NOTE]
>
>* Zu den Daten des Bestellberichts gehören Daten aus vier Wochen für die Standardumgebung (Hostgruppe) und Daten aus zwei Wochen für alle nicht standardmäßigen Umgebungen.
>* Umsatzmetriken, die auf &quot;[!UICONTROL Increment count and keep the user in the activity]&quot; eingestellt sind, protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher getätigt wurde. Alle nachfolgenden Bestellungen erhöhen die Konversionsanzahl, fügen jedoch keine Umsätze zu RPV/AOV/Sales hinzu und sind nicht im [!UICONTROL Order Details] -Bericht enthalten.

## Best Practices  

* Um einen Bestelldatensatz aufzuzeichnen, muss der Parameter `orderTotal` übergeben werden.
* Werte, die über den Mbox-Parameter `ProductPurchasedId` weitergegeben werden, werden im Bericht [!UICONTROL Order Details] aufgeführt.
* Best Practice ist, einen `orderID` und einen `orderTotal` einzuschließen. Dadurch können doppelte Bestellungen automatisch ignoriert werden.

## Einschränkungen  {#section_49B9590904A645B18E694B4EFFFC1DEF}

Die folgenden Informationen gelten für die Option [!UICONTROL Download] :

* Sie können beide Berichte für die Aktivitäten [!UICONTROL A/B Test], [!UICONTROL Automated Personalization], [!UICONTROL Experience Targeting] und [!UICONTROL Multivariate] herunterladen. Der [!UICONTROL Success Metrics] -Bericht kann nicht für [!UICONTROL Recommendations] -Aktivitäten heruntergeladen werden.
* Die Option [!UICONTROL Download] steht nicht für [!UICONTROL A/B Test] - und [!UICONTROL Experience Targeting] -Aktivitäten zur Verfügung, die vor der [!DNL Target] -Version 15.7.1 (Juli 2015) erstellt wurden.
* Erlebnisse ohne verknüpfte Daten werden im heruntergeladenen Bericht nicht erfasst.
* Zielgruppen, die auf die Berichterstellungs-Benutzeroberfläche von [!DNL Target] angewendet werden, werden nicht in den Download-Bericht übernommen.
* Berichte, die als CSV-Dateien zum Herunterladen generiert wurden, sind nicht konsistent, wenn die Aktivität mehr als eine Metrik verwendet. Der herunterladbare Bericht wird nur auf der Grundlage der Berichtseinstellungen generiert und berücksichtigt denselben Wert für alle anderen verwendeten Metriken. Der korrekte Bericht ist immer der in der Benutzeroberfläche von [!DNL Target] angezeigte Bericht.
