---
keywords: Erlebnis-Targeting;XT;Metriken;Metriken festlegen;Zielmetrik;Aktivitätseinstellungen;Erfolgsmetrik;Konversion;Umsatz;Interaktion
description: Erfahren Sie, wie Sie Metriken in einer  [!DNL Adobe Target] [!UICONTROL Erlebnis-Targeting]-Aktivität angeben, um zu bestimmen, wann ein Besuch erfolgreich ist, [!UICONTROL Konversion], [!UICONTROL Umsatz] oder [!UICONTROL Interaktion].
title: Wie lege ich Zielmetriken in einer [!UICONTROL Erlebnis-Targeting]-Aktivität fest?
feature: Experience Targeting
exl-id: 16249930-8b9c-441c-bd14-5f32332556d2
TQID: https://experienceleague.adobe.com/DRFhQ7plSdYqXdzodxFe8h22fSz9xZs9ATt5Ri2s6AA
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 52%

---

# Festlegen von Metriken in [!UICONTROL Erlebnis-Targeting]-Aktivitäten (XT)

Verwenden Sie Metriken in einer [!DNL Adobe Target] [!UICONTROL Experience Targeting]&#x200B;(XT)-Aktivität, um den Erfolg eines Besuchs festzustellen.

Ausführliche Informationen zu Erfolgsmetriken finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Geben Sie das Ziel der Aktivität an.
1. Wählen Sie eine [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) aus.

   ![Erfolgsmetrik auswählen](/help/main/c-activities/t-experience-target/t-xt-create/assets/ab_metrics-new.png)

   Auf [!UICONTROL &#x200B; Seite „Metriken &#x200B;]&quot; werden die Erfolgsmetriken aufgelistet, die Sie für Ihre Aktivität auswählen können. Die Erfolgsmetriken sind in folgende Kategorien unterteilt:

   * [!UICONTROL Konversion]
   * [!UICONTROL Umsatz]
   * [!UICONTROL Interaktion]

   Sie können eine der vordefinierten Erfolgsmetriken verwenden oder eine benutzerdefinierte Erfolgsmetrik erstellen. Sie können auch eine Erfolgsmetrik als primäre Metrik kennzeichnen. Berichte und Experience Cloud-Karten zeigen standardmäßig die primäre Metrik, falls eine festgelegt ist.
1. Geben Sie die Einstellungen für Ihre Metriken an.

   Die verfügbaren Einstellungen hängen von der verwendeten Erfolgsmetrik ab.

   Wenn diese Option aktiviert ist[!UICONTROL &#x200B; liefert der Feld „Geschätzter Wert der Konversion] (für Metriken [!UICONTROL Seitenbewertung] nicht verfügbar) einen Wert für Ihr Ziel. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

   Es ist sehr wichtig, die Erfolgsmetriken korrekt zu konfigurieren, um die erwarteten Daten zu erhalten.

   Weitere Informationen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Optional) Fügen Sie zusätzliche Metriken hinzu.
1. Klicken Sie **[!UICONTROL Weiter]** wenn Sie mit dem Festlegen Ihrer Metriken fertig sind.

Wenn Sie eine Metrik benennen oder umbenennen, sind die folgenden Zeichen nicht zulässig:

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

## Schulungsvideo: Aktivitätsmetriken (7:43) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Arbeit mit Erfolgsmetriken.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen [!UICONTROL &#x200B; Metriken &#x200B;]Konversion[!UICONTROL &#x200B; Umsatz] und [!UICONTROL Interaktion]
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
