---
keywords: Targeting; Zielgruppe; Berichterstellung; Erfolgsmetrik
description: Erfahren Sie, wie Sie eine Erfolgsmetrik in [!DNL Adobe Target] auswählen, die den Benutzer für die Reporting-Zielgruppe qualifiziert.
title: Kann ich eine Berichterstellungszielgruppe auf eine Erfolgsmetrik anwenden?
feature: Erfolgsmetriken
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: 20a5201b5c05b1f083252ac73b3b4bbc91e97aaa
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 54%

---

# Anwenden einer Reporting-Zielgruppe auf eine Erfolgsmetrik

Wählen Sie eine Erfolgsmetrik aus, die den Benutzer für die Reporting-Zielgruppe in [!DNL Adobe Target] qualifiziert.

Mit der Dropdownliste [!UICONTROL Angewendet am] können Sie Zielgruppen bei allen Aktivitäten Erfolgsmetriken zuordnen. Somit können Sie die Berichtszahlen anzeigen, nachdem die Metrik erreicht wurde. Dasselbe gilt auch für nachfolgende Aktionen.

![](assets/success_metric.png)

Ein Beispiel: Angenommen, Sie haben eine Aktivität für alle Besucher erstellt, die über Ihre Homepage die Konversionsseite erreichen, aber Sie möchten sich auch stärker auf Besucher konzentrieren, die im Vorfeld ihrer Konversion einen Wert von mehr als 50 $ zum Warenkorb hinzugefügt haben.

Die Dropdownliste [!UICONTROL Angewandt auf] bietet potenziell drei Kategorien: Besucher der Aktivität, nur Besucher, die einen bestimmten Schritt in der Aktivität erreichen, oder nur Besucher, die eine Konversion erreichen. Oder, anders gesagt, Sie können festlegen, dass ein Besucher eine Mbox auf der Entrypage der Aktivität, eine mbox, die einen bestimmten Punkt in der Mitte der Aktivität definiert, oder die Konversions-Mbox am Ende der Aktivität erreichen muss.

[Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) sind nur verfügbar, wenn Sie sie für Ihre Aktivität konfiguriert haben. Wenn Sie keine Erfolgsmetriken definiert haben, sehen Sie nur zwei Optionen aus der Dropdownliste: [!UICONTROL Campaign Entry] and [!UICONTROL Conversion].

Bedenken Sie folgende Informationen, wenn Sie einer Erfolgsmetrik eine Berichterstellungszielgruppe zuweisen:

* Für Aktionen vor der Aktion mit der angewendeten Erfolgsmetrik wendet [!DNL Target] keine segmentierte Zielgruppe an.
* Für Aktionen nach der angewendeten Erfolgsmetrik wendet [!DNL Target] eine segmentierte Zielgruppe an.

Um die Segmentierung in Berichten anzuzeigen, wählen Sie die gewünschte Zielgruppe aus der Dropdownliste [!UICONTROL Zielgruppe] im Aktivitätsbericht aus.

![](assets/reporting_audience_dropdown.png)
