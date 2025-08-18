---
keywords: Target; Berichte; Berichtseinstellungen; extreme Bestellungen; Extremwerte
description: Erfahren Sie, wie Sie in Adobe Extremwerte von den Berichten ausschließen [!DNL Target]  sodass einige ungewöhnliche Bestellungen keine Auswirkungen auf Ihre Aktivitätsergebnisse haben.
title: Wie kann ich extreme Werte in Berichten ausschließen?
feature: Reports
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 64%

---

# Ausschließen von Extremwerten

Sie können Extremwerte von den Berichten in [!DNL Adobe Target] ausschließen, sodass einige ungewöhnliche Bestellungen sich nicht auf Ihre Aktivitätsergebnisse auswirken. Ein Beispiel für eine ungewöhnliche Bestellung ist, wenn ein Trainer Ausrüstungen für eine ganze Mannschaft kauft, anstatt dass einzelne Sportler individuell bestellen.

>[!NOTE]
>
>Das [!UICONTROL Exclude Extreme Values]-Flag gilt nur für Aktivitäten mit den Metriktypen [!UICONTROL Revenue] und [!UICONTROL Engagement].

Extremwerte werden automatisch entsprechend den unten beschriebenen Regeln markiert. Sie können einstellen, ob extreme Werte in Ihren Bericht aufgenommen werden sollen oder nicht. Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Werte automatisch ausgeschlossen.

Ein Wert wird als extrem betrachtet, wenn in den Daten des letzten Monats mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert vorliegen (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde).

Bei der Verwendung von RPV ist der Filter für extreme Werte häufig nützlich. RPV kombiniert Konversionsraten und den durchschnittlichen Bestellwert und zeigt häufig die Unbeständigkeit dieser Metriken auf. Wenn Sie RPV verwenden und bestimmen, dass Aufträge nicht als normal verteilt angezeigt werden, sehen Sie normalere Ergebnisse, wenn Sie den Filter für extreme Bestellungen anwenden.

Wenn ein Wert als extrem markiert wurde, wird der Bestellwert durch den durchschnittlichen Bestellwert des Erlebnisses des letzten Monats ersetzt, wobei die Extreme ausgespart werden. Die Reihenfolge wird auch im [!UICONTROL Order Details]-Bericht und im CSV-Download als extrem gekennzeichnet, um tägliche Ergebnisse zu erhalten.

**So schließen Sie extreme Werte aus Ihren Berichten aus:**

1. Öffnen Sie eine Aktivität mit [!UICONTROL Revenue] oder [!UICONTROL Engagement] Metriktypen und klicken Sie auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf das Symbol Berichtseinstellungen ![Berichteinstellungen](/help/main/assets/icons/Setting.svg) , um das Dialogfeld **[!UICONTROL Settings]** anzuzeigen.

1. Schieben Sie den **[!UICONTROL Exclude Extreme Values]** nach Bedarf in die Position „Ein“ oder „Aus“.
1. Klicken Sie auf **[!UICONTROL Save]**.
