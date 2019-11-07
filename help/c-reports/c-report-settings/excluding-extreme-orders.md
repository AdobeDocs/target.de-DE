---
keywords: Target; Berichte; Berichtseinstellungen; extreme Bestellungen; Extremwerte
description: Extreme Werte können in Adobe Target ausgeschlossen werden, sodass einige ungewöhnliche Bestellungen Ihre Aktivitätsergebnisse nicht beeinflussen. Ein Beispiel für eine ungewöhnliche Bestellung ist, wenn ein Trainer Ausrüstungen für eine ganze Mannschaft kauft, anstatt dass einzelne Sportler individuell bestellen.
title: Extreme Werte in Adobe Target-Berichten ausschließen
uuid: bb151b54-09ef-40b5-bc04-95c61b761f5a
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Ausschließen von Extremwerten{#exclude-extreme-values}

Sie können Extremwerte aus Berichten ausschließen, sodass einige ungewöhnliche Bestellungen die Aktivitätsergebnisse nicht beeinflussen. Ein Beispiel für eine ungewöhnliche Bestellung ist, wenn ein Trainer Ausrüstungen für eine ganze Mannschaft kauft, anstatt dass einzelne Sportler individuell bestellen.

>[!NOTE]
>
>Die Flagge [!UICONTROL Extreme Werte ausschließen] gilt nur für Aktivitäten mit den Metriktypen Umsatz und Interaktion.

Extremwerte werden automatisch entsprechend den unten beschriebenen Regeln markiert. Sie können einstellen, ob extreme Werte in Ihren Bericht aufgenommen werden sollen oder nicht. Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Werte automatisch ausgeschlossen.

Ein Wert wird als extrem betrachtet, wenn in den Daten des letzten Monats mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert vorliegen (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde).

Bei der Verwendung von RPV ist der Filter für extreme Werte häufig nützlich. RPV kombiniert Konversionsraten und den durchschnittlichen Bestellwert und zeigt häufig die Unbeständigkeit dieser Metriken auf. Wenn Sie RPV verwenden und bestimmen, dass Aufträge nicht als normal verteilt angezeigt werden, sehen Sie normalere Ergebnisse, wenn Sie den Filter für extreme Bestellungen anwenden.

Wenn ein Wert als extrem markiert wurde, wird der Bestellwert durch den durchschnittlichen Bestellwert des Erlebnisses des letzten Monats ersetzt, wobei die Extreme ausgespart werden. Die Bestellung wird auch im Bestelldetailbericht und im CSV-Download der täglichen Ergebnisse als extrem gekennzeichnet.

**So schließen Sie extreme Werte aus Ihren Berichten aus:**

1. Öffnen Sie eine Aktivität, die die Metriktypen Umsatz oder Interaktion enthält, und klicken Sie dann auf die Registerkarte **[!UICONTROL Berichte]**.
1. Klicken Sie auf das Zahnradsymbol.

   ![Berichtseinstellungen](/help/c-reports/c-report-settings/assets/report-settings-gear-icon.png)

   Das Dialogfeld [!UICONTROL Berichtseinstellungen] wird angezeigt.

   ![Schrittergebnis](assets/exclude_extreme_values.png)

1. Schalten Sie die Option **[!UICONTROL Extreme Werte ausschließen]** ein bzw. aus.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
