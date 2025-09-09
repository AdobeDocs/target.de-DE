---
keywords: Berichte; Herunterladen von Berichten; csv; Erfolgsmetriken; Bestelldetails
description: Erfahren Sie, wie Sie Daten aus Adobe [!DNL Target] Aktivitäten im CSV-Format herunterladen können, um sie schnell in Excel, Access oder andere Datenanalyseprogramme zu importieren.
title: Wie lade ich Berichtsdaten in einer CSV-Datei herunter?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: e42398b8774fff57c00658636a52bd0038ad94b4
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 30%

---

# Herunterladen von Daten in Form einer CSV-Datei

Laden Sie Daten im CSV-Format herunter, um sie schnell in [!DNL Excel], [!DNL Access] oder andere Datenanalyseprogramme zu importieren.

So laden Sie Daten als CSV-Datei herunter:

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität.

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol Filtern ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um die Liste zu filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf das **[!UICONTROL Download]**-Symbol ![Download-Symbol](/help/main/assets/icons/Download.svg) und wählen Sie dann einen Berichtstyp aus, der für die Analyse in Excel und anderen Tools heruntergeladen werden soll.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

## CSV-Download-Format für Beliebtheit und schlüsselbasierte Algorithmen {#format}

Die CSV-Download-Datei enthält konsistent die Ergebnisse, die nach der Ausführung der Backend-Kriterien generiert wurden.

**Bei Popularitätsalgorithmen (nicht schlüsselbasiert) umfasst die Datei Folgendes:**

* Eine Reihe von Backup-Recommendations mit dem Präfix *
* Eine separate Zeile mit Empfehlungen, die auf Algorithmuseinstellungen basieren

**Bei schlüsselbasierten Algorithmen umfasst die Datei Folgendes:**

* Eine Sicherungszeile, die den Popularitätsalgorithmen ähnelt
* Mehrere Zeilen im Schlüsselwertformat, wobei der erste Eintrag die Produkt-ID des Schlüssels ist, gefolgt von kommagetrennten Produkt-IDs, die Empfehlungskandidaten darstellen

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Der [!UICONTROL Success Metrics] zeigt Informationen zu Ihren Erfolgsmetriken sowie zu den folgenden Metriken an, die nicht in der [!DNL Target]-Benutzeroberfläche verfügbar sind:

* Durchschnittszeit bis zur Konversion in Stunden, sodass Sie sehen können, wie lange ein Besucher im Schnitt braucht, um den Konversionspunkt zu erreichen
* Summe der Erträge im Quadrat zur Offline-Berechnung vor statistischer Genauigkeit

Die Daten werden bis zum Ende der Aktivität gespeichert.

>[!NOTE]
>
>Der CSV-Bericht enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden. Um diese berechneten Metriken zu berechnen, laden Sie die [!DNL Target] [Konfidenzrechner abschließen](/help/main/assets/complete_confidence_calculator.xlsx) Excel-Datei herunter, um den Wert der Aktivität einzugeben, oder überprüfen Sie [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Der [!UICONTROL Order Details] zeigt Informationen zu Ihren Bestellungen an, darunter:

* Datum und Uhrzeit der Bestellung
* Bestellmenge (wenn Sie eine Bestellaufgabe-Mbox eingefügt haben)

  Der [!UICONTROL Order Details]-Bericht funktioniert nur, wenn Sie Bestellungen haben.

* Bestellmarkierung (doppelte oder extreme Bestellungen)

  Eine Bestellung wird als extrem gekennzeichnet, wenn sie mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert aufweist. Bei dieser Berechnung wird der letzte Monat der Daten verwendet (bis zu dem Zeitpunkt, an dem die Berechnung vorgenommen wurde). Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Bestellungen automatisch ausgeschlossen. Weitere Informationen finden Sie unter [Ausschließen extremer Bestellungen](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Produkt-ID

  Die Gesamtlänge der Produkt-IDs, verkettet mit Kommas, sollte 255 Zeichen nicht überschreiten, da sonst die IDs im Bericht nicht ordnungsgemäß angezeigt werden. Wenn Ihr Auftrag Produkte mit den IDs „aa, bb“ enthält, ist die Gesamtlänge „aa,bb“, also 5 Zeichen.

* Erlebnis

  Im [!UICONTROL Order Details] Bericht für [!UICONTROL A/B Test]-, [!UICONTROL Experience Targeting] (XT)- und [!UICONTROL Multivariate Test] (MVT)-Aktivitäten enthält die [!UICONTROL Experience] die `localId`. Dies ist die Wert-Ausgabe aus der `$campaign.recipe.id` in Angebots-Token.

  Es gibt keine [!UICONTROL Experience] Spalte für [!UICONTROL Automated Personalization] (AP)-Aktivitäten. Die aktuelle Spalte [!UICONTROL Algorithm Name] wurde durch die Terminologie „Kontrolle“ im Vergleich zu „Zielgruppe“ ersetzt, wie an anderer Stelle in [!DNL Target] dargestellt.

  Es gab keine Auswirkungen auf [!UICONTROL Recommendations] Aktivitäten.

>[!NOTE]
>
>* Zu den Daten des Bestellberichts gehören Daten aus vier Wochen für die Standardumgebung (Hostgruppe) und Daten aus zwei Wochen für alle nicht standardmäßigen Umgebungen.
>* Umsatzmetriken, die auf &quot;[!UICONTROL Increment count and keep the user in the activity]&quot; eingestellt sind, protokollieren Auftragsdetails nur für die erste Bestellung, die von demselben Besucher getätigt wurde. Alle nachfolgenden Bestellungen erhöhen die Konversionsanzahl, erhöhen jedoch nicht den Umsatz in RPV/AOV/Sales und sind nicht im [!UICONTROL Order Details] enthalten.

## Best Practices  

* Um einen Auftragseintrag aufzuzeichnen, muss der `orderTotal` übergeben werden.
* Über den `ProductPurchasedId` mbox-Parameter übergebene Werte werden im [!UICONTROL Order Details]-Bericht aufgeführt.
* Best Practice ist es, eine `orderID` und eine `orderTotal` einzuschließen. Dadurch können doppelte Bestellungen automatisch ignoriert werden.

## Einschränkungen  {#section_49B9590904A645B18E694B4EFFFC1DEF}

Die folgenden Informationen gelten für die Option [!UICONTROL Download] :

* Sie können beide Berichte für [!UICONTROL A/B Test]-, [!UICONTROL Automated Personalization]-, [!UICONTROL Experience Targeting]- und [!UICONTROL Multivariate]-Aktivitäten herunterladen. Sie können den [!UICONTROL Success Metrics] für [!UICONTROL Recommendations] Aktivitäten nicht herunterladen.
* Die Option [!UICONTROL Download] ist nicht für [!UICONTROL A/B Test]- und [!UICONTROL Experience Targeting] verfügbar, die vor [!DNL Target] Version 15.7.1 (Juli 2015) erstellt wurden.
* Erlebnisse ohne verknüpfte Daten werden im heruntergeladenen Bericht nicht erfasst.
* Zielgruppen, die in der [!DNL Target] Reporting-Benutzeroberfläche angewendet wurden, werden nicht in den Download-Bericht übernommen.
* Berichte, die als CSV-Dateien zum Herunterladen generiert wurden, sind nicht konsistent, wenn die Aktivität mehr als eine Metrik verwendet. Der herunterladbare Bericht wird nur auf der Grundlage der Berichtseinstellungen generiert und berücksichtigt denselben Wert für alle anderen verwendeten Metriken. Der korrekte Bericht ist immer der in der Benutzeroberfläche von [!DNL Target] angezeigte Bericht.
