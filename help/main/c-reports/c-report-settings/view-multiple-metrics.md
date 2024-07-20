---
keywords: Target; Berichte; Berichtseinstellungen; mehrere Metriken; Metriken; angezeigte Metriken; ausgeblendete Metriken
description: Erfahren Sie, wie Sie mehrere Metriken auswählen, die in einem Bericht mit Adobe Target angezeigt werden sollen.
title: Wie kann ich mehrere Metriken in einem Bericht anzeigen?
feature: Reports
exl-id: 8d8aedd8-4583-4131-8ae0-df14e071940a
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 12%

---

# Anzeigen mehrerer Metriken in einem Bericht

Sie können mehrere Metriken auswählen, die in einem [!DNL Adobe Target] -Bericht angezeigt werden sollen.

Beachten Sie beim Arbeiten mit mehreren Metriken in Berichten die folgenden Informationen:

* Die Möglichkeit, mehrere Metriken anzuzeigen, ist nur für die Aktivitäten [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md), [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) und [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) (XT) verfügbar.
* Sie können einem Bericht nicht mehr als 20 Metriken für eine Aktivität hinzufügen, die [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwendet. Sie können so viele Metriken wie in Ihrer Aktivität zu Berichten für Aktivitäten hinzufügen, die A4T nicht verwenden, *nicht* .
* Sie können die [Download-Option](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) nicht verwenden, um Berichte als CSV-Datei herunterzuladen, wenn Sie mehrere Metriken ausgewählt haben. Sie müssen nur eine Metrik auswählen, um die Option [!UICONTROL Download] zu aktivieren.
* Sie können nicht mehrere Metriken für Aktivitäten anzeigen, die vor der Version vom Juli 2015 [!DNL Target] (30. Juli 2015) erstellt wurden.

**So wählen Sie mehrere Metriken für die Anzeige im Bericht aus:**

1. Um einen Bericht anzuzeigen, klicken Sie auf **[!UICONTROL Activities]**, klicken Sie in der Liste auf die gewünschte Aktivität und klicken Sie dann auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf die Dropdownliste **[!UICONTROL Report Metric]** , um die Listen [!UICONTROL Shown Metrics] und [!UICONTROL Hidden Metrics] anzuzeigen.

   ![Bild mit mehreren_Metriken](assets/multiple_metrics.png)

   Sie können das Feld [!UICONTROL Search] verwenden, um schnell verfügbare Metriken zu finden, die zur Liste [!UICONTROL Shown Metrics] hinzugefügt werden können.

   Beachten Sie, dass Sie mehrere Metriken aus den Modi [!UICONTROL Table View] und [!UICONTROL Graph View] des Berichts auswählen können.

1. Bewegen Sie den Mauszeiger über die gewünschten Metriken in der Liste [!UICONTROL Hidden Metrics] und klicken Sie dann auf **[!UICONTROL Select]** , um sie in die Liste [!UICONTROL Shown Metrics] zu verschieben.

   Oder

   Ziehen Sie die gewünschten Metriken aus der Liste [!UICONTROL Hidden Metrics] in die Liste [!UICONTROL Shown Metrics].

   Die Liste [!UICONTROL Shown Metrics] muss mindestens eine Metrik enthalten.

   Sie können die Metriken neu anordnen, indem Sie sie per Drag-and-Drop in die gewünschte Reihenfolge in der Liste [!UICONTROL Shown Metrics] ziehen. Die ausgewählte Reihenfolge wird in den [!UICONTROL Table View] und [!UICONTROL Graph View] angezeigt. Um eine Metrik aus der Liste [!UICONTROL Shown Metrics] zu entfernen, bewegen Sie den Mauszeiger über die Metrik und klicken Sie dann auf das Symbol **X** .

1. Klicken Sie zum Abschluss auf **[!UICONTROL Save]** .
1. (Bedingt) Bewegen Sie beim Anzeigen des Berichts in der [!UICONTROL Table View] den Mauszeiger auf die Spaltenüberschrift einer Metrik, um einen blauen Pfeil anzuzeigen. Klicken Sie auf den Pfeil, um die Tabelle zu erweitern und die [!UICONTROL Lift] und [!UICONTROL Confidence] für diese Metrik anzuzeigen.

   ![Bild &quot;multiple_metrics_table&quot;](assets/multiple_metrics_table.png)

   Sie können nur jeweils eine Metrik/Spalte erweitern. Klicken Sie erneut auf den Pfeil, um die Spalten zu reduzieren.

1. (Bedingt) Beim Anzeigen des Berichts in der Diagrammansicht können Sie einzelne Metriken auswählen, die in der Dropdownliste angezeigt werden sollen:

   ![multiple_metrics_graph image](assets/multiple_metrics_graph.png)
