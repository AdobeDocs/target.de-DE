---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Metrik; Metrikdefinitionen
description: Hier finden Sie Antworten auf Fragen zu Metrikdefinitionen und zur Verwendung von Analytics for [!DNL Target] (A4T). Mit A4T können Sie Analytics-Berichte mit Adobe [!DNL Target] Aktivitäten verwenden.
title: Wo finde ich Informationen zu Metrikdefinitionen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
TQID: https://experienceleague.adobe.com/CLUm25T-5PCOzdXVL94kCgvqM-OL3dZzWXkG1qmN8IE
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 36%

---

# Metrikdefinitionen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zu Metrikdefinitionen und zur Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) gestellt werden.

## Wie ist die Gültigkeit für eine Aktivitätszugehörigkeit? Wie lange nach Eintritt der Aktivität werden die Aktionen der Besucher in der Aktivität gezählt, wenn sie sie nicht erneut sehen? {#section_41B4958F33534E4B96DEE0C981227A79}

+++Antwort
Die Standardgültigkeit für die Aktivität beträgt 90 Tage nach der letzten Interaktion des Besuchers mit der Aktivität. Diese Einstellung kann bei Bedarf von ClientCare angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

+++

## Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen? {#adv-settings}

+++Antwort
Die [!UICONTROL Advanced Settings] sind nicht für Aktivitäten verfügbar, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden.

Bei Aktivitäten, die A4T verwenden, verwendet die Zielmetrik immer die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; und &quot;[!UICONTROL On Every Impression]&quot;. Diese Einstellungen *nicht*.

Für Nicht-A4T-Aktivitäten können Sie die [erweiterten Einstellungsoptionen](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) verwenden, um zu verwalten, wie Sie den Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder entfernt werden soll, und die Auswahl, ob die Metrik einmal pro Eintritt oder bei jeder Impression gezählt werden soll. Sie können auf die [!UICONTROL Advanced Settings] in einer Nicht-A4T-Aktivität zugreifen, indem Sie auf die vertikalen Auslassungszeichen > [!UICONTROL Advanced Settings] klicken, wie unten dargestellt:

![Erweiterte Einstellungen](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## Was sind berechnete Metriken und wie ersetzen sie die SiteCatalyst:Event-Mbox, die ich verwendet habe? {#section_D59F4719E6B94758A2187427C17F8EF3}

+++Antwort
Mit errechneten Metriken können Sie benutzerdefinierte Metriken erstellen, die aus Segmenten oder mathematischen Berechnungen abgeleitet wurden. In der Vergangenheit hätten Sie vielleicht die `SiteCatlayst:Event` Mbox verwendet, in der `evar27=shoes` und das Ereignis `purchase` lauteten. Jetzt erstellen Sie ein Segment mit `evar27=shoes` und anschließend eine errechnete Metrik, in der das Ereignis mit dem übernommenen Segment `purchase` lautet. Diese Metriken können jederzeit erstellt werden, auch nachdem die Aktivität gestartet wurde. Anschließend können sie für jeden Bericht in Analytics verwendet werden.

+++

## Ordnet A4T mehreren Kampagnen die Konversionen zu? {#section_7F15C727206440CD86B3A8CE77087DF9}

+++Antwort
Ja, mithilfe der Einstellung „Vollständige Zuordnung“.

+++
