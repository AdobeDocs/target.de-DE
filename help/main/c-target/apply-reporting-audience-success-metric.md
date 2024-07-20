---
keywords: Targeting; Zielgruppe; Berichterstellung; Erfolgsmetrik
description: Erfahren Sie, wie Sie in [!DNL Adobe Target] eine Erfolgsmetrik auswählen, die den Benutzer für die Reporting-Zielgruppe qualifiziert.
title: Kann ich eine Berichterstellungszielgruppe auf eine Erfolgsmetrik anwenden?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: bcbb6dec9d6add07c109b07bf125c1356ad2a8b9
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 36%

---

# Anwenden einer Reporting-Zielgruppe auf eine Erfolgsmetrik

Wählen Sie eine Erfolgsmetrik aus, die den Benutzer für die Berichterstellungszielgruppe in [!DNL Adobe Target] qualifiziert.

In der Dropdownliste [!UICONTROL Applied At] können Sie für alle Aktivitäten eine Zielgruppe auf eine Erfolgsmetrik anwenden, sodass Sie Berichtszahlen anzeigen können, nachdem die Metrik erreicht wurde, und für nachfolgende Aktionen.

![success_metric image](assets/success_metric.png)

Ein Beispiel: Angenommen, Sie haben eine Aktivität für alle Besucher erstellt, die über Ihre Homepage die Konversionsseite erreichen, aber Sie möchten sich auch stärker auf Besucher konzentrieren, die im Vorfeld ihrer Konversion einen Wert von mehr als 50 $ zum Warenkorb hinzugefügt haben.

Die Dropdownliste [!UICONTROL Applied At] bietet potenziell drei Kategorien:

* Alle Besucher der Aktivität
* Nur Besucher, die einen bestimmten Schritt in der Aktivität erreichen
* Nur Besucher, die eine Konversion erreichen

Oder, anders gesagt, Sie können festlegen, dass ein Besucher eine Mbox auf der Entrypage der Aktivität, eine mbox, die einen bestimmten Punkt in der Mitte der Aktivität definiert, oder die Konversions-Mbox am Ende der Aktivität erreichen muss.

>[!NOTE]
>
>[Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) sind nur verfügbar, wenn Sie sie für Ihre Aktivität konfiguriert haben. Wenn Sie keine Erfolgsmetriken definiert haben, sehen Sie nur zwei Optionen aus der Dropdownliste: [!UICONTROL Campaign Entry] und [!UICONTROL Conversion].


## Zu beachten

Bedenken Sie folgende Informationen, wenn Sie einer Erfolgsmetrik eine Berichterstellungszielgruppe zuweisen:

* Nur Erfolgsmetriken, die mit der Metrik beginnen, auf die die Zielgruppe angewendet wird, zeigen nach der Zielgruppe segmentierte Berichtsdaten an
* Erfolgsmetriken, die denen vorangehen, auf die die Zielgruppe angewendet wird, werden nicht von der Zielgruppe segmentiert und zeigen alle Besucherdaten an
* Die Metriken werden basierend auf ihrer Reihenfolge in der Aktivitätsdefinition berücksichtigt, wobei die [!UICONTROL Primary Goal] die letzte ist.

## Segmentierung in Berichten anzeigen

Um die Segmentierung in Berichten anzuzeigen, wählen Sie die gewünschte Zielgruppe aus der Dropdownliste [!UICONTROL Audience] im Aktivitätsbericht aus.

![reporting_audience_dropdown image](assets/reporting_audience_dropdown.png)

## Beispiel

Betrachten Sie eine Aktivität mit Erfolgsmetrik1, Erfolgsmetrik2, Erfolgsmetrik3 und dem Primären Ziel.

Angenommen, Sie haben die Berichterstellung Audience1 auf &quot;Einstieg&quot;und die Berichterstellungszielgruppe Audience2 auf Erfolgsmetrik2 eingestellt. Die Zielgruppen filtern die Berichtsdaten wie folgt:

|  | Besuchern | Erfolgsmetrik1 | Erfolgsmetrik2 | Erfolgsmetrik3 | Primäres Ziel |
| --- | --- | --- | --- | --- | --- |
| Audience1 | Angewendet | Angewendet | Angewendet | Angewendet | Angewendet |
| Audience2 | Nicht angewendet | Nicht angewendet | Angewendet | Angewendet | Angewendet |
