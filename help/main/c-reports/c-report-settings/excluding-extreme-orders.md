---
keywords: Target; Berichte; Berichtseinstellungen; extreme Bestellungen; Extremwerte
description: Erfahren Sie, wie Sie Extremwerte von Berichten in Adobe ausschließen, sodass einige ungewöhnliche Bestellungen Ihre Aktivitätsergebnisse nicht beeinflussen. [!DNL Target]
title: Wie schließe ich extreme Werte in Berichten aus?
feature: Reports
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 65%

---

# Ausschließen von Extremwerten

Sie können Extremwerte davon ausschließen, dass sie sich auf Berichte in [!DNL Adobe Target] auswirken, sodass einige ungewöhnliche Bestellungen Ihre Aktivitätsergebnisse nicht beeinflussen. Ein Beispiel für eine ungewöhnliche Bestellung ist, wenn ein Trainer Ausrüstungen für eine ganze Mannschaft kauft, anstatt dass einzelne Sportler individuell bestellen.

>[!NOTE]
>
>Die Markierung [!UICONTROL Exclude Extreme Values] gilt nur für Aktivitäten mit den Metriktypen [!UICONTROL Revenue] und [!UICONTROL Engagement].

Extremwerte werden automatisch entsprechend den unten beschriebenen Regeln markiert. Sie können einstellen, ob extreme Werte in Ihren Bericht aufgenommen werden sollen oder nicht. Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Werte automatisch ausgeschlossen.

Ein Wert wird als extrem betrachtet, wenn in den Daten des letzten Monats mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert vorliegen (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde).

Bei der Verwendung von RPV ist der Filter für extreme Werte häufig nützlich. RPV kombiniert Konversionsraten und den durchschnittlichen Bestellwert und zeigt häufig die Unbeständigkeit dieser Metriken auf. Wenn Sie RPV verwenden und bestimmen, dass Aufträge nicht als normal verteilt angezeigt werden, sehen Sie normalere Ergebnisse, wenn Sie den Filter für extreme Bestellungen anwenden.

Wenn ein Wert als extrem markiert wurde, wird der Bestellwert durch den durchschnittlichen Bestellwert des Erlebnisses des letzten Monats ersetzt, wobei die Extreme ausgespart werden. Die Bestellung wird auch im [!UICONTROL Order Details] -Bericht und im CSV-Download für tägliche Ergebnisse als extrem markiert.

**So schließen Sie extreme Werte aus Ihren Berichten aus:**

1. Öffnen Sie eine Aktivität mit den Metriktypen Umsatz oder Interaktion und klicken Sie auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf das Zahnradsymbol, um das Dialogfeld **[!UICONTROL Settings]** anzuzeigen.

   ![Schrittergebnis](assets/exclude_extreme_values.png)

1. Schieben Sie den Umschalter **[!UICONTROL Exclude Extreme Values]** nach Wunsch in die Position &quot;Ein&quot;oder &quot;Aus&quot;.
1. Klicken Sie auf **[!UICONTROL Save]**.
