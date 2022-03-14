---
keywords: Targeting; Zielgruppe; Berichterstellung; Erfolgsmetrik
description: Erfahren Sie, wie Sie eine Erfolgsmetrik auswählen in [!DNL Adobe Target] , der den Benutzer für die Reporting-Zielgruppe qualifiziert.
title: Kann ich eine Berichterstellungszielgruppe auf eine Erfolgsmetrik anwenden?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 54%

---

# Anwenden einer Reporting-Zielgruppe auf eine Erfolgsmetrik

Wählen Sie eine Erfolgsmetrik aus, die den Benutzer für die Reporting-Zielgruppe in [!DNL Adobe Target].

Mit der Dropdownliste [!UICONTROL Angewendet am] können Sie Zielgruppen bei allen Aktivitäten Erfolgsmetriken zuordnen. Somit können Sie die Berichtszahlen anzeigen, nachdem die Metrik erreicht wurde. Dasselbe gilt auch für nachfolgende Aktionen.

![](assets/success_metric.png)

Ein Beispiel: Angenommen, Sie haben eine Aktivität für alle Besucher erstellt, die über Ihre Homepage die Konversionsseite erreichen, aber Sie möchten sich auch stärker auf Besucher konzentrieren, die im Vorfeld ihrer Konversion einen Wert von mehr als 50 $ zum Warenkorb hinzugefügt haben.

Die [!UICONTROL Angewandt bei] Dropdownliste bietet potenziell drei Kategorien: Besucher der Aktivität, nur Besucher, die einen bestimmten Schritt in der Aktivität erreichen, oder nur Besucher, die eine Konversion erreichen. Oder, anders gesagt, Sie können festlegen, dass ein Besucher eine Mbox auf der Entrypage der Aktivität, eine mbox, die einen bestimmten Punkt in der Mitte der Aktivität definiert, oder die Konversions-Mbox am Ende der Aktivität erreichen muss.

[Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) sind nur verfügbar, wenn Sie sie für Ihre Aktivität konfiguriert haben. Wenn Sie keine Erfolgsmetriken definiert haben, sehen Sie nur zwei Optionen aus der Dropdownliste: [!UICONTROL Kampagneneinstieg] und [!UICONTROL Konversion].

Bedenken Sie folgende Informationen, wenn Sie einer Erfolgsmetrik eine Berichterstellungszielgruppe zuweisen:

* Für Aktionen vor der Aktion mit der angewendeten Erfolgsmetrik [!DNL Target] wendet keine segmentierte Zielgruppe an.
* Für Aktionen nach der angewendeten Erfolgsmetrik, [!DNL Target] wendet eine segmentierte Zielgruppe an.

Um die Segmentierung in Berichten anzuzeigen, wählen Sie die gewünschte Zielgruppe aus dem [!UICONTROL Zielgruppe] Dropdown-Liste im Aktivitätsbericht.

![](assets/reporting_audience_dropdown.png)
