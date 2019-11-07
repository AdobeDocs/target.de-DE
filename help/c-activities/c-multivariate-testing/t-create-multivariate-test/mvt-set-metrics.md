---
keywords: Multivarianz;MVT;Metriken;Metriken festlegen;Zielmetrik;Aktivitätseinstellungen;Erfolgsmetrik;Konversion;Umsatz;Interaktion
description: Verwenden Sie in multivariaten Tests Metriken, um zu erkennen, wann ein Besuch erfolgreich verlief.
title: Festlegen von Metriken
solution: Target,Standard
uuid: 0fb297ba-f1c3-4139-ac37-7fa0bf2ac308
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Festlegen von Metriken{#set-metrics}

Verwenden Sie in multivariaten Tests Metriken, um zu erkennen, wann ein Besuch erfolgreich verlief.

Ausführliche Informationen zu Erfolgsmetriken finden Sie unter  [Erfolgsmetriken](../../../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Geben Sie das Ziel der Aktivität an.
1. Wählen Sie eine [Erfolgsmetrik](../../../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) aus.

   ![Festlegen der Liste der Metriken](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list.png)

   Auf der Seite [!UICONTROL Metriken auswählen] werden die Erfolgsmetriken, die Sie für Ihre Aktivität auswählen können, angezeigt. Die Erfolgsmetriken sind in folgende Kategorien unterteilt:

   * Konversion
   * Umsatz
   * Interaktion
   Sie können die vorgefertigten Erfolgsmetriken verwenden oder eine benutzerdefinierte Erfolgsmetrik erstellen. Sie können auch eine Erfolgsmetrik als primäre Metrik kennzeichnen. Berichte und Experience Cloud-Karten zeigen standardmäßig die primäre Metrik, falls eine festgelegt ist.
1. Geben Sie die Einstellungen für Ihre Metriken an.

   Die verfügbaren Einstellungen hängen von der von Ihnen verwendeten Erfolgsmetrik ab.

   Bei Aktivierung bietet das Feld [!UICONTROL Geschätzter Wert der Konversion] (nicht verfügbar für Seitenergebnis-Metriken) einen Wert für Ihr Ziel. Mit diesem Wert kann Target die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](../../../administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE).

   Es ist sehr wichtig, die Erfolgsmetriken korrekt zu konfigurieren, um die erwarteten Daten zu erhalten.

   Weitere Informationen finden Sie unter [Erfolgsmetriken](../../../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)
1. (Optional) Fügen Sie zusätzliche Metriken hinzu.
1. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie die Einstellung Ihrer Metriken abgeschlossen haben.
Beachten Sie, dass bei der (Um-)Benennung von Metriken folgende Zeichen nicht zulässig sind:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `/` | Vorwärtsschrägstrich |
   | `?` | Fragezeichen |
   | `#` | Raute |
   | `:` | Doppelpunkt |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

## Schulungsvideo: Aktivitätsmetriken (7:43)

Dieses Video enthält Informationen zur Arbeit mit Erfolgsmetriken.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380?captions=ger)
