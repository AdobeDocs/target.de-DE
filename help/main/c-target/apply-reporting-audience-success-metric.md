---
keywords: Targeting; Zielgruppe; Berichterstellung; Erfolgsmetrik
description: Erfahren Sie, wie Sie eine Erfolgsmetrik in auswählen [!DNL Adobe Target]  die den Benutzer für die Reporting-Zielgruppe qualifiziert.
title: Kann ich eine Reporting-Zielgruppe auf eine Erfolgsmetrik anwenden?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
TQID: https://experienceleague.adobe.com/n3iyCzlY5oDOrCEqvo6nO51PvknlySPCMasQZ0JfIEM
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 36%

---

# Anwenden einer Reporting-Zielgruppe auf eine Erfolgsmetrik

Wählen Sie eine Erfolgsmetrik , die den Benutzer für die Reporting-Zielgruppe in [!DNL Adobe Target] qualifiziert.

Über die Dropdown-Liste [!UICONTROL Applied At] können Sie für alle Aktivitäten eine Zielgruppe auf eine Erfolgsmetrik anwenden. So können Sie die Berichtszahlen nach Erreichen der Metrik sowie für nachfolgende Aktionen anzeigen.

![success_metric-Bild](assets/success_metric.png)

Ein Beispiel: Angenommen, Sie haben eine Aktivität für alle Besucher erstellt, die über Ihre Homepage die Konversionsseite erreichen, aber Sie möchten sich auch stärker auf Besucher konzentrieren, die im Vorfeld ihrer Konversion einen Wert von mehr als 50 $ zum Warenkorb hinzugefügt haben.

Die Dropdown-Liste [!UICONTROL Applied At] bietet möglicherweise drei Kategorien:

* Alle Besucher der Aktivität
* Nur Besucher, die einen bestimmten Schritt in der Aktivität erreichen
* Nur Besucher, die eine Konversion erreichen

Oder, anders gesagt, Sie können festlegen, dass ein Besucher eine Mbox auf der Entrypage der Aktivität, eine mbox, die einen bestimmten Punkt in der Mitte der Aktivität definiert, oder die Konversions-Mbox am Ende der Aktivität erreichen muss.

>[!NOTE]
>
>[Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) sind nur verfügbar, wenn Sie sie für Ihre Aktivität konfiguriert haben. Wenn Sie keine Erfolgsmetriken definiert haben, sehen Sie in der Dropdown-Liste nur zwei Optionen: [!UICONTROL Campaign Entry] und [!UICONTROL Conversion].


## Zu beachten

Bedenken Sie folgende Informationen, wenn Sie einer Erfolgsmetrik eine Berichterstellungszielgruppe zuweisen:

* Nur Erfolgsmetriken, die mit der Metrik beginnen, auf die die Zielgruppe angewendet wird, zeigen Berichtsdaten an, die nach Zielgruppe segmentiert sind
* Erfolgsmetriken, die denjenigen vorausgehen, auf die die Zielgruppe angewendet wird, werden nicht nach Zielgruppe segmentiert und zeigen alle Besucherdaten an
* Die Metriken werden anhand ihrer Reihenfolge in der Aktivitätsdefinition betrachtet, wobei die [!UICONTROL Primary Goal] die letzte ist.

## Anzeigen der Segmentierung in Berichten

Um die Segmentierung im Reporting anzuzeigen, wählen Sie die gewünschte Zielgruppe aus der Dropdown-Liste [!UICONTROL Audience] im Bericht der Aktivität aus.

![reporting_audience_dropdown image](assets/reporting_audience_dropdown.png)

## Beispiel

Stellen Sie sich eine Aktivität vor, die über Erfolgsmetriken1, Erfolgsmetriken2, Erfolgsmetriken3 und das Primäre Ziel verfügt.

Angenommen, für Audience1 ist die Berichterstellung „Einstieg“ festgelegt und für Audience2 die Berichterstellung „Erfolgsmetrik2“. Die Zielgruppen filtern die Berichtsdaten wie folgt:

|  | Besuchern | Erfolgsmetrik1 | Erfolgsmetrik2 | Erfolgsmetrik3 | Primäres Ziel |
| --- | --- | --- | --- | --- | --- |
| Audience1 | Angewendet | Angewendet | Angewendet | Angewendet | Angewendet |
| Audience2 | Nicht angewendet | Nicht angewendet | Angewendet | Angewendet | Angewendet |
