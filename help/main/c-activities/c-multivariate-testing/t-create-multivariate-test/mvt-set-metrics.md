---
keywords: Multivarianz;MVT;Metriken;Metriken festlegen;Zielmetrik;Aktivitätseinstellungen;Erfolgsmetrik;Konversion;Umsatz;Interaktion
description: Erfahren Sie, wie Sie Metriken in einer  [!DNL Adobe Target] [!UICONTROL Multivariate Test]-Aktivität angeben, um zu bestimmen, wann ein Besuch erfolgreich war, z. B. [!UICONTROL Conversion], [!UICONTROL Revenue] und [!UICONTROL Engagement].
title: Wie kann ich Zielmetriken in einer [!UICONTROL Multivariate Test] (MVT)-Aktivität festlegen?
feature: Multivariate Tests
exl-id: 8530b3f1-5daa-4a03-a482-93b10eb23208
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 60%

---

# Festlegen von Metriken für eine [!UICONTROL Multivariate Test]

Verwenden Sie Metriken in einem [!DNL Adobe Target]-[!UICONTROL Multivariate Test], um zu bestimmen, wann ein Besuch erfolgreich war.

Ausführliche Informationen zu Erfolgsmetriken finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Geben Sie das Ziel der Aktivität an.
1. Wählen Sie eine [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) aus.

   ![Festlegen der Liste der Metriken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list.png)

   Auf der Seite [!UICONTROL Select Metrics] werden die Erfolgsmetriken aufgelistet, die Sie für Ihre Aktivität auswählen können. Die Erfolgsmetriken sind in folgende Kategorien unterteilt:

   * [!UICONTROL Conversion]
   * [!UICONTROL Revenue]
   * [!UICONTROL Engagement]

   Sie können die vorgefertigten Erfolgsmetriken verwenden oder eine benutzerdefinierte Erfolgsmetrik erstellen. Sie können auch eine Erfolgsmetrik als primäre Metrik kennzeichnen. Berichte und Experience Cloud-Karten zeigen standardmäßig die primäre Metrik, falls eine festgelegt ist.

1. Geben Sie die Einstellungen für Ihre Metriken an.

   Die verfügbaren Einstellungen hängen von der verwendeten Erfolgsmetrik ab.

   Wenn diese Option aktiviert ist, liefert das Feld [!UICONTROL Estimated Value of the Conversion] (für die [!UICONTROL Page Score] Metriken nicht verfügbar) einen Wert für Ihr Ziel. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

   Es ist sehr wichtig, die Erfolgsmetriken korrekt zu konfigurieren, um die erwarteten Daten zu erhalten.

   Weitere Informationen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

1. (Optional) Fügen Sie zusätzliche Metriken hinzu.
1. Klicken Sie auf **[!UICONTROL Continue]** , wenn Sie mit dem Festlegen Ihrer Metriken fertig sind.

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
* Verstehen und Erstellen von [!UICONTROL Conversion], [!UICONTROL Revenue] und [!UICONTROL Engagement] Metriken
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
