---
keywords: Target;reports;report settings;multiple metrics;metrics;shown metrics;hidden metrics
description: Wählen Sie mehrere Metriken zur Ansicht in einem Bericht mit Adobe Target aus.
title: Ansicht mehrerer Metriken in einem Bericht mit Adobe Target
feature: report settings
uuid: f3ea7313-0f98-4b58-88aa-e2438c06e739
translation-type: tm+mt
source-git-commit: e18f18e6d6e0b8fc6eb5ada845e2fe5377d6c5d0
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 61%

---


# Anzeigen mehrerer Metriken in einem Bericht{#view-multiple-metrics-in-a-report}

Sie können mehrere zu Ansicht Metriken in einem [!DNL Adobe Target] Bericht auswählen.

Beachten Sie beim Arbeiten mit mehreren Metriken in Berichten die folgenden Informationen:

* The ability to view multiple metrics is available for [A/B Test](/help/c-activities/t-test-ab/test-ab.md), [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md), and [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT) activities only.
* You cannot add more than 20 metrics to a report for an activity that uses [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). You can add as many metrics as you have in your activity to reports for activities that do *not* use A4T.
* Wenn Sie mehrere Metriken ausgewählt haben, können Sie die Option [](/help/c-reports/downloading-data-in-csv-file.md)Download nicht zum Herunterladen von Berichten in CSV verwenden. Zum Aktivieren der Option [!UICONTROL Download] dürfen Sie nur eine einzelne Metrik auswählen.
* You cannot view multiple metrics for activities created before the July 2015 [!DNL Target] release (July 30, 2015).

**So wählen Sie mehrere Metriken für die Anzeige im Bericht aus:**

1. Möchten Sie einen Bericht anzeigen, klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte Aktivität aus der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Berichte.]**
1. Klicken Sie auf die Dropdownliste **[!UICONTROL Berichtsmetrik]**, um die Listen [!UICONTROL Angezeigte Metriken] und [!UICONTROL Ausgeblendete Metriken] anzuzeigen.

   ![](assets/multiple_metrics.png)

   Mithilfe des Feldes [!UICONTROL Suche] können Sie schnell verfügbare Metriken finden, die der Liste [!UICONTROL Angezeigte Metriken] hinzugefügt werden sollen.

   Beachten Sie, dass Sie in den beiden Modi [!UICONTROL Tabellenansicht] und [!UICONTROL Diagrammansicht] des Berichts mehrere Metriken auswählen können.

1. Bewegen Sie den Mauszeiger über die gewünschten Metriken in der Liste [!UICONTROL Ausgeblendete Metriken] und klicken Sie dann auf **[!UICONTROL Auswählen]**, um sie in die Liste [!UICONTROL Angezeigte Metriken] zu verschieben.

   Oder

   Verschieben Sie die gewünschten Metriken per Drag-and-drop von der Liste [!UICONTROL Ausgeblendete Metriken] in die Liste [!UICONTROL Angezeigte Metriken].

   Die Liste [!UICONTROL Angezeigte Metriken] muss mindestens eine Metrik enthalten.

   Sie können die Metriken neu anordnen, indem Sie sie per Drag-and-drop in der Liste [!UICONTROL Angezeigte Metriken] in die gewünschte Reihenfolge bringen. The selected order will be reflected in the [!UICONTROL Table View] and [!UICONTROL Graph View]. Wenn Sie eine Metrik aus der Liste [!UICONTROL Angezeigte Metriken] entfernen möchten, bewegen Sie Ihren Mauszeiger über die Metrik und klicken Sie dann auf das **X**-Symbol.

1. Klicken Sie auf **[!UICONTROL Speichern]**, wenn Sie fertig sind.
1. (Conditional) While viewing the report in the [!UICONTROL Table View], hover your mouse pointer on any metric&#39;s column header to display a blue arrow. Klicken Sie auf den Pfeil, um die Tabelle zu erweitern und [!UICONTROL Lift] und [!UICONTROL Vertrauen] für die jeweilige Metrik anzuzeigen.

   ![](assets/multiple_metrics_table.png)

   Sie können nur jeweils eine Metrik/Spalte erweitern. Klicken Sie erneut auf den Pfeil, um die Spalten zu reduzieren.

1. (Bedingt) Beim Anzeigen des Berichts in der Ansicht &quot;Diagramm&quot;können Sie die einzelnen Metriken auswählen, die in der Dropdown-Liste angezeigt werden sollen:

   ![](assets/multiple_metrics_graph.png)

