---
keywords: A/B;Aktivitätsmetriken;Metriken;Metriken festlegen;Zielmetrik;Aktivitätseinstellungen;Erfolgsmetrik;Konversion;Umsatz;Interaktion
description: Erfahren Sie, wie Sie in einer Adobe Metriken angeben [!DNL Target] A/B-Aktivität , um festzustellen, wann ein Besuch erfolgreich war, z. B. Konversion, Umsatz und Interaktion.
title: Wie setze ich Zielmetriken in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 9e9e8787-c0cd-4aab-bd2d-0e9591e0a07d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 85%

---

# Festlegen von Metriken

Metriken in einer [!DNL Adobe Target] A/B-Aktivität , um festzustellen, wann ein Besuch erfolgreich war.

Ausführliche Informationen zu Erfolgsmetriken finden Sie unter  [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Geben Sie das Ziel der Aktivität an.
1. Wählen Sie eine [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) aus.

   ![Erfolgsmetrik auswählen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_metrics-new.png)

   Auf der Seite [!UICONTROL Metriken auswählen] werden die Erfolgsmetriken, die Sie für Ihre Aktivität auswählen können, angezeigt. Die Erfolgsmetriken sind in folgende Kategorien unterteilt:

   * Konversion
   * Umsatz
   * Interaktion

   Sie können die vorgefertigten Erfolgsmetriken verwenden oder eine benutzerdefinierte Erfolgsmetrik erstellen. Sie können auch eine Erfolgsmetrik als primäre Metrik kennzeichnen. Berichte und Experience Cloud-Karten zeigen standardmäßig die primäre Metrik, falls eine festgelegt ist.
1. Geben Sie die Einstellungen für Ihre Metriken an.

   Die verfügbaren Einstellungen hängen von der von Ihnen verwendeten Erfolgsmetrik ab.

   Bei Aktivierung bietet das Feld [!UICONTROL Geschätzter Wert der Konversion] (nicht verfügbar für Seitenergebnis-Metriken) einen Wert für Ihr Ziel. Mit diesem Wert kann Target die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

   Es ist sehr wichtig, die Erfolgsmetriken korrekt zu konfigurieren, um die erwarteten Daten zu erhalten.

   Weitere Informationen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).
1. (Optional) Fügen Sie zusätzliche Metriken hinzu.
1. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie die Einstellung Ihrer Metriken abgeschlossen haben.

Beachten Sie, dass bei der (Um-)Benennung von Metriken folgende Zeichen nicht zulässig sind:

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
