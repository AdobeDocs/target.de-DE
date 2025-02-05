---
keywords: Target;Berichte;Berichteinstellungen;mehrere Metriken;Metriken;angezeigte Metriken;ausgeblendete Metriken
description: Erfahren Sie, wie Sie mit Adobe Target mehrere Metriken auswählen, die in einem Bericht angezeigt werden sollen.
title: Wie kann ich mehrere Metriken in einem Bericht anzeigen?
feature: Reports
exl-id: 8d8aedd8-4583-4131-8ae0-df14e071940a
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 12%

---

# Anzeigen mehrerer Metriken in einem Bericht

Sie können mehrere Metriken auswählen, die in einem [!DNL Adobe Target] angezeigt werden sollen.

Beachten Sie beim Arbeiten mit mehreren Metriken in Berichten die folgenden Informationen:

* Die Möglichkeit, mehrere Metriken anzuzeigen, ist nur für [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md), [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) und [Experience Targeting](/help/main/c-activities/t-experience-target/experience-target.md) (XT) verfügbar.
* Einem Bericht können nicht mehr als 20 Metriken für eine Aktivität hinzugefügt werden, die [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwendet. Sie können so viele Metriken wie in Ihrer Aktivität zu Berichten für Aktivitäten hinzufügen, die *nicht)* verwenden.
* Sie können die Option [Herunterladen](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) nicht verwenden, um Berichte in CSV herunterzuladen, wenn Sie mehrere Metriken ausgewählt haben. Sie müssen nur eine einzelne Metrik auswählen, um die Option [!UICONTROL Download] zu aktivieren.
* Es können nicht mehrere Metriken für Aktivitäten angezeigt werden, die vor der [!DNL Target] vom Juli 2015 (30. Juli 2015) erstellt wurden.

**So wählen Sie mehrere Metriken für die Anzeige im Bericht aus:**

1. Um einen Bericht anzuzeigen, klicken Sie auf **[!UICONTROL Activities]**, dann auf die gewünschte Aktivität in der Liste und anschließend auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf die Dropdown-Liste **[!UICONTROL Report Metric]** , um die [!UICONTROL Shown Metrics]- und [!UICONTROL Hidden Metrics] anzuzeigen.

   Sie können das [!UICONTROL Search] verwenden, um schnell verfügbare Metriken zu finden, die der [!UICONTROL Shown Metrics] hinzugefügt werden können.

   Beachten Sie, dass Sie mehrere Metriken aus dem [!UICONTROL Table View]- und dem [!UICONTROL Graph View] des Berichts auswählen können.

1. Bewegen Sie den Mauszeiger über die gewünschten Metriken in der [!UICONTROL Hidden Metrics] Liste und klicken Sie dann auf **[!UICONTROL Select]** , um sie in die [!UICONTROL Shown Metrics] Liste zu verschieben.

   Oder

   Ziehen Sie die gewünschten Metriken per Drag-and-Drop aus der [!UICONTROL Hidden Metrics] in die [!UICONTROL Shown Metrics].

   Es muss mindestens eine Metrik in der [!UICONTROL Shown Metrics] vorhanden sein.

   Sie können die Metriken neu anordnen, indem Sie sie per Drag-and-Drop in die gewünschte Reihenfolge in der [!UICONTROL Shown Metrics] ziehen. Die ausgewählte Reihenfolge wird in der [!UICONTROL Table View] und [!UICONTROL Graph View] angezeigt. Um eine Metrik aus der [!UICONTROL Shown Metrics] zu entfernen, bewegen Sie den Mauszeiger über die Metrik und klicken Sie dann auf das Symbol **X** .

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** .
1. (Bedingt) Wenn Sie den Bericht im [!UICONTROL Table View] anzeigen, bewegen Sie den Mauszeiger über die Spaltenüberschrift einer Metrik, um einen blauen Pfeil anzuzeigen. Klicken Sie auf den Pfeil, um die Tabelle zu erweitern und die [!UICONTROL Lift] und [!UICONTROL Confidence] für diese Metrik anzuzeigen.

   Sie können nur jeweils eine Metrik/Spalte erweitern. Klicken Sie erneut auf den Pfeil, um die Spalten zu reduzieren.

1. (Bedingt) Wenn Sie den Bericht im [!UICONTROL Graph View] anzeigen, können Sie einzelne Metriken aus der Dropdown-Liste auswählen, die angezeigt werden sollen.
