---
keywords: Target; Berichte; Berichtseinstellungen; extreme Bestellungen; Extremwerte
description: Erfahren Sie, wie Sie in Adobe Extremwerte von den Berichten ausschließen [!DNL Target]  sodass einige ungewöhnliche Bestellungen keine Auswirkungen auf Ihre Aktivitätsergebnisse haben.
title: Wie kann ich extreme Werte in Berichten ausschließen?
feature: Reports
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
TQID: https://experienceleague.adobe.com/yQtG4u-sLVJ66PezWW9ZgmY8ZuK177m-hLdQq-zlmfI
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 62%

---

# Ausschließen von Extremwerten

Sie können Extremwerte von den Berichten in [!DNL Adobe Target] ausschließen, sodass einige ungewöhnliche Bestellungen sich nicht auf Ihre Aktivitätsergebnisse auswirken. Ein Beispiel für eine ungewöhnliche Bestellung ist, wenn ein Trainer Ausrüstungen für eine ganze Mannschaft kauft, anstatt dass einzelne Sportler individuell bestellen.

>[!NOTE]
>
>Das Flag [!UICONTROL Extreme Werte ausschließen] gilt nur für Aktivitäten mit den Metriktypen [!UICONTROL Umsatz] und [!UICONTROL Interaktion].

Extremwerte werden automatisch entsprechend den unten beschriebenen Regeln markiert. Sie können einstellen, ob extreme Werte in Ihren Bericht aufgenommen werden sollen oder nicht. Bei einer Aktivität, die seit einer Stunde läuft oder bei der 15 Bestellungen eingegangen sind (je nachdem, was zuerst eintritt), werden die extremen Werte automatisch ausgeschlossen.

Ein Wert wird als extrem betrachtet, wenn in den Daten des letzten Monats mehr als +/- 3 Standardabweichungen vom durchschnittlichen Bestellwert vorliegen (bis zu dem Zeitpunkt, zu dem die Berechnung vorgenommen wurde).

Bei der Verwendung von RPV ist der Filter für extreme Werte häufig nützlich. RPV kombiniert Konversionsraten und den durchschnittlichen Bestellwert und zeigt häufig die Unbeständigkeit dieser Metriken auf. Wenn Sie RPV verwenden und bestimmen, dass Aufträge nicht als normal verteilt angezeigt werden, sehen Sie normalere Ergebnisse, wenn Sie den Filter für extreme Bestellungen anwenden.

Wenn ein Wert als extrem markiert wurde, wird der Bestellwert durch den durchschnittlichen Bestellwert des Erlebnisses des letzten Monats ersetzt, wobei die Extreme ausgespart werden. Die Bestellung wird auch im Bericht &quot;[!UICONTROL &quot; und ] CSV-Download für tägliche Ergebnisse als extrem gekennzeichnet.

**So schließen Sie extreme Werte aus Ihren Berichten aus:**

1. Öffnen Sie eine Aktivität, die Metriktypen [!UICONTROL Umsatz] oder [!UICONTROL Interaktion] enthält, und klicken Sie dann auf die Registerkarte **[!UICONTROL Berichte]**.
1. Klicken Sie auf das Symbol Berichtseinstellungen ![Berichteinstellungen](/help/main/assets/icons/Setting.svg) ), um das Dialogfeld **[!UICONTROL Einstellungen]** anzuzeigen.

1. Schieben Sie den **[!UICONTROL Extreme Werte ausschließen]**-Umschalter nach Bedarf auf die Position „ein“ oder „aus“.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
