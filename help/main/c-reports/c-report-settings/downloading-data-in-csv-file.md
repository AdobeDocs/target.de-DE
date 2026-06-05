---
keywords: Berichte; Herunterladen von Berichten; csv; Erfolgsmetriken; Bestelldetails
description: Erfahren Sie, wie Sie Daten aus Adobe [!DNL Target] Aktivitäten im CSV-Format herunterladen können, um sie schnell in Excel, Access oder andere Datenanalyseprogramme zu importieren.
title: Wie lade ich Berichtsdaten in einer CSV-Datei herunter?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
TQID: https://experienceleague.adobe.com/-1FEosKnw-h8hRoK-VTO9VZsi5vIghnMnZp-fUUXo2U
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 737
ht-degree: 35%

---

# Herunterladen von Daten in Form einer CSV-Datei

Laden Sie Daten im CSV-Format herunter, um sie schnell in [!DNL Excel], [!DNL Access] oder andere Datenanalyseprogramme zu importieren.

So laden Sie Daten als CSV-Datei herunter:

1. Klicken Sie auf **[!UICONTROL „Aktivitäten“]** und anschließend in der Liste auf die gewünschte Aktivität.

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol Filtern ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um die Liste zu filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Activity Source] auswählen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Berichte]**.
1. Klicken Sie auf **[!UICONTROL Herunterladen]**-Symbol ![Herunterladen-Symbol](/help/main/assets/icons/Download.svg) und wählen Sie dann einen Berichtstyp aus, der für die Analyse in Excel und anderen Tools heruntergeladen werden soll.

   * [!UICONTROL Exportieren von Berichten in CSV]
   * [!UICONTROL Bestelldetails als CSV exportieren]

## [!UICONTROL Exportieren von Berichten in das CSV-Format] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Der [!UICONTROL Erfolgsmetriken]-Bericht zeigt Informationen zu Ihren Erfolgsmetriken sowie zu den folgenden Metriken an, die in der [!DNL Target]-Benutzeroberfläche nicht verfügbar sind:

* Durchschnittszeit bis zur Konversion in Stunden, sodass Sie sehen können, wie lange ein Besucher im Schnitt braucht, um den Konversionspunkt zu erreichen
* Summe der Erträge im Quadrat zur Offline-Berechnung vor statistischer Genauigkeit

Die Daten werden bis zum Ende der Aktivität gespeichert.

>[!NOTE]
>
>Der CSV-Bericht enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden. Um diese berechneten Metriken zu berechnen, laden Sie die [!DNL Target] [Konfidenzrechner abschließen](/help/main/assets/complete_confidence_calculator.xlsx) Excel-Datei herunter, um den Wert der Aktivität einzugeben, oder überprüfen Sie [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Bestelldetails als CSV exportieren] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Der [!UICONTROL Bestelldetails] zeigt Informationen zu Ihren Bestellungen an, darunter:

* Datum und Uhrzeit der Bestellung
* Bestellmenge (wenn Sie eine Bestellaufgabe-Mbox eingefügt haben)

  Der [!UICONTROL Auftragsdetails] funktioniert nur, wenn Sie Bestellungen haben.

* Bestellmarkierung (doppelte oder extreme Bestellungen)

  Eine Bestellung wird als extrem gekennzeichnet, wenn sie mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert aufweist. Bei dieser Berechnung wird der letzte Monat der Daten verwendet (bis zu dem Zeitpunkt, an dem die Berechnung vorgenommen wurde). Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Bestellungen automatisch ausgeschlossen. Weitere Informationen finden Sie unter [Ausschließen extremer Bestellungen](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* Produkt-ID

  Die Gesamtlänge der Produkt-IDs, verkettet mit Kommas, sollte 255 Zeichen nicht überschreiten, da sonst die IDs im Bericht nicht ordnungsgemäß angezeigt werden. Wenn Ihr Auftrag Produkte mit den IDs „aa, bb“ enthält, ist die Gesamtlänge „aa,bb“, also 5 Zeichen.

* Erlebnis

  Im Bericht [!UICONTROL Bestelldetails] für [!UICONTROL A/B-Test]-, [!UICONTROL Experience Targeting] (XT)- und [!UICONTROL Multivariater Test] (MVT)-Aktivitäten enthält die Spalte [!UICONTROL Erlebnis] die `localId`. Dies ist die Wert-Ausgabe aus der `$campaign.recipe.id` in Angebots-Token.

  Es gibt keine Spalte [!UICONTROL Erlebnis] für Aktivitäten für [!UICONTROL Automatisierte Personalisierung] (AP). Die aktuelle Spalte [!UICONTROL Algorithmusname] wurde durch die Terminologie „Kontrolle“ versus „Zielgruppe“ ersetzt, wie an anderer Stelle in [!DNL Target] gezeigt.

  Auf [!UICONTROL Recommendations]-Aktivitäten hat dies keinen Einfluss.

>[!NOTE]
>
>* Zu den Daten des Bestellberichts gehören Daten aus vier Wochen für die Standardumgebung (Hostgruppe) und Daten aus zwei Wochen für alle nicht standardmäßigen Umgebungen.
>* Umsatzmetriken, die auf „Anzahl [!UICONTROL &#x200B; und Benutzer in der Aktivität belassen“ eingestellt sind] protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher getätigt wurde. Alle nachfolgenden Bestellungen erhöhen die Konversionsanzahl, erhöhen jedoch nicht den Umsatz in RPV/AOV/Sales und sind nicht im Bericht [!UICONTROL Auftragsdetails] enthalten.

## Best Practices

* Um einen Auftragseintrag aufzuzeichnen, muss der `orderTotal` übergeben werden.
* Die über den `ProductPurchasedId` mbox-Parameter übergebenen Werte werden im Bericht [!UICONTROL Bestelldetails] aufgeführt.
* Best Practice ist es, eine `orderID` und eine `orderTotal` einzuschließen. Dadurch können doppelte Bestellungen automatisch ignoriert werden.

## Einschränkungen {#section_49B9590904A645B18E694B4EFFFC1DEF}

Die folgenden Informationen gelten für die Option [!UICONTROL Herunterladen]:

* Sie können beide Berichte für [!UICONTROL A/B-Test]-, [!UICONTROL Automated Personalization]-, [!UICONTROL Erlebnis-Targeting]- und [!UICONTROL Multivarianz]-Aktivitäten herunterladen. Sie können den Bericht [!UICONTROL Erfolgsmetriken“ &#x200B;] Aktivitäten [!UICONTROL Recommendations] nicht herunterladen.
* Die [!UICONTROL Download]-Option ist nicht für [!UICONTROL A/B-Test]- und [!UICONTROL Erlebnis-Targeting]-Aktivitäten verfügbar, die vor [!DNL Target] Version 15.7.1 (Juli 2015) erstellt wurden.
* Erlebnisse ohne verknüpfte Daten werden im heruntergeladenen Bericht nicht erfasst.
* Zielgruppen, die in der [!DNL Target] Reporting-Benutzeroberfläche angewendet wurden, werden nicht in den Download-Bericht übernommen.
* Berichte, die als CSV-Dateien zum Herunterladen generiert wurden, sind nicht konsistent, wenn die Aktivität mehr als eine Metrik verwendet. Der herunterladbare Bericht wird nur auf der Grundlage der Berichtseinstellungen generiert und berücksichtigt denselben Wert für alle anderen verwendeten Metriken. Der korrekte Bericht ist immer der in der Benutzeroberfläche von [!DNL Target] angezeigte Bericht.
