---
keywords: A/B;Aktivitätsmetriken;Metriken;Metriken festlegen;Zielmetrik;Aktivitätseinstellungen;Erfolgsmetrik;Konversion;Umsatz;Interaktion
description: Erfahren Sie, wie Sie in einer [!DNL Adobe Target] A/B-Aktivität Metriken angeben, um festzustellen, wann ein Besuch erfolgreich war, z. B. [!UICONTROL Conversion], [!UICONTROL Revenue] und [!UICONTROL Engagement].
title: Wie setze ich Zielmetriken in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 9e9e8787-c0cd-4aab-bd2d-0e9591e0a07d
source-git-commit: 2d5272a852dc879e7307695744b70afe7fee9a38
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 59%

---

# Festlegen von Metriken

Verwenden Sie Metriken in einer [!DNL Adobe Target] A/B-Aktivität, um zu ermitteln, wann ein Besuch erfolgreich war.

Detaillierte Informationen zu Erfolgsmetriken finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Wählen Sie im Abschnitt **[!UICONTROL Reporting Settings]** der Seite **[!UICONTROL Goals & Settings]** eine [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) aus.

   ![Erfolgsmetrik auswählen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_metrics-new.png)

   Die Option [!UICONTROL Select Metrics] listet die Erfolgsmetriken auf, die Sie für Ihre Aktivität auswählen können. Die Erfolgsmetriken sind in folgende Kategorien unterteilt:

   * [!UICONTROL Conversion]
   * [!UICONTROL Revenue]
   * [!UICONTROL Engagement]

   Sie können die vorgefertigten Erfolgsmetriken verwenden oder eine benutzerdefinierte Erfolgsmetrik erstellen. Sie können auch eine Erfolgsmetrik als primäre Metrik kennzeichnen. Berichte und Experience Cloud-Karten zeigen standardmäßig die primäre Metrik, falls eine festgelegt ist.

1. Geben Sie die Einstellungen für Ihre Metriken an.

   Die verfügbaren Einstellungen hängen von der von Ihnen verwendeten Erfolgsmetrik ab.

   Wenn diese Option aktiviert ist, stellt das Feld [!UICONTROL Estimated Value of the Conversion] (nicht verfügbar für die Metriken [!UICONTROL Page Score] ) einen Wert für Ihr Ziel bereit. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

   Die richtige Konfiguration der Erfolgsmetriken ist wichtig, um sicherzustellen, dass Sie die erwarteten Daten erhalten.

   Weitere Informationen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Optional) Fügen Sie zusätzliche Metriken hinzu.

Wenn Sie eine Metrik benennen oder umbenennen, sind folgende Zeichen nicht zulässig:

| Zeichen | Beschreibung |
|--- |--- |
| / | Vorwärtsschrägstrich |
| ? | Fragezeichen |
| # | Raute |
| : | Doppelpunkt |
| = | Gleich |
| + | Plus |
| - | Minus |
| @ | At-Zeichen |

## Schulungsvideo: Aktivitätsmetriken (7:43) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Arbeit mit Erfolgsmetriken.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
