---
keywords: A/B;Aktivitätsmetriken;Metriken;Metriken festlegen;Zielmetrik;Aktivitätseinstellungen;Erfolgsmetrik;Konversion;Umsatz;Interaktion
description: Erfahren Sie, wie Sie Metriken in einer [!DNL Adobe Target] A/B-Aktivität , um zu bestimmen, wann ein Besuch erfolgreich war, z. B. [!UICONTROL Konversion], [!UICONTROL Umsatz], und [!UICONTROL Interaktion].
title: Wie setze ich Zielmetriken in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 9e9e8787-c0cd-4aab-bd2d-0e9591e0a07d
source-git-commit: 2d5272a852dc879e7307695744b70afe7fee9a38
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 68%

---

# Festlegen von Metriken

Metriken in einer [!DNL Adobe Target] A/B-Aktivität , um festzustellen, wann ein Besuch erfolgreich war.

Ausführliche Informationen zu Erfolgsmetriken finden Sie unter  [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Im **[!UICONTROL Berichtseinstellungen]** Abschnitt **[!UICONTROL Ziele und Einstellungen]** Seite, wählen Sie eine [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Erfolgsmetrik auswählen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_metrics-new.png)

   Die [!UICONTROL Metriken auswählen] enthält die Erfolgsmetriken, die Sie für Ihre Aktivität auswählen können. Die Erfolgsmetriken sind in folgende Kategorien unterteilt:

   * [!UICONTROL Konversion]
   * [!UICONTROL Umsatz]
   * [!UICONTROL Interaktion]

   Sie können die vorgefertigten Erfolgsmetriken verwenden oder eine benutzerdefinierte Erfolgsmetrik erstellen. Sie können auch eine Erfolgsmetrik als primäre Metrik kennzeichnen. Berichte und Experience Cloud-Karten zeigen standardmäßig die primäre Metrik, falls eine festgelegt ist.

1. Geben Sie die Einstellungen für Ihre Metriken an.

   Die verfügbaren Einstellungen hängen von der von Ihnen verwendeten Erfolgsmetrik ab.

   Bei Aktivierung bietet das Feld [!UICONTROL Geschätzter Wert der Konversion] (nicht verfügbar für Seitenergebnis-Metriken) einen Wert für Ihr Ziel.  Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

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
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktionen
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
