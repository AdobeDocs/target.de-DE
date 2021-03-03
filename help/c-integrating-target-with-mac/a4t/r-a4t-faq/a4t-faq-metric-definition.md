---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Metrik; Metrikdefinitionen
description: Hier finden Sie Antworten auf Fragen zu Metrikdefinitionen und zur Verwendung von Analytics für die Zielgruppe (A4T). Mit A4T können Sie Analytics-Berichte mit Adobe Target-Aktivitäten verwenden.
title: Wo finde ich Informationen zu Metrikdefinitionen mit A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: e45f0d2d2370f9c7aba2c2bd26afdd4c0e401db8
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 39%

---


# Metrikdefinitionen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig gestellte Fragen zu Metrikdefinitionen und zur Verwendung von [!DNL Adobe Analytics] als Berichte für [!DNL Adobe Target] (A4T).

## Wie ist die Gültigkeit für eine Aktivitätsmitgliedschaft? Wie lange nach Eintritt der Besucher in die Aktivität werden ihre Aktionen in der Aktivität gezählt, wenn sie sie nicht mehr sehen? {#section_41B4958F33534E4B96DEE0C981227A79}

Die Standardgültigkeit für die Aktivität beträgt 90 Tage nach der letzten Interaktion des Besuchers mit der Aktivität. Diese Einstellung kann bei Bedarf von ClientCare angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

## Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen? {#adv-settings}

Die Optionen [!UICONTROL Erweiterte Einstellungen] stehen nicht für Aktivitäten zur Verfügung, die [!DNL Analytics] als Berichte-Quelle (A4T) verwenden.

Bei Aktivitäten, die A4T verwenden, verwendet die Zielmetrik immer die Einstellungen &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität halten]&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen können nicht konfiguriert werden.**

Bei Nicht-A4T-Aktivitäten können Sie mit den Optionen [Erweiterte Einstellungen](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) verwalten, wie Sie den Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder entfernt werden soll und ob die Metrik einmal pro Teilnehmer oder bei jeder Impression gezählt werden soll. Sie können auf die Optionen [!UICONTROL Erweiterte Einstellungen] in einer Nicht-A4T-Aktivität zugreifen, indem Sie auf die senkrechten Auslassungspunkte > [!UICONTROL Erweiterte Einstellungen] klicken, wie unten dargestellt:

![Erweiterte Einstellungen](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

## Was sind errechnete Metriken und wie ersetzen sie die SiteCatalyst:Event-Mbox, die ich vorher verwendet habe?   {#section_D59F4719E6B94758A2187427C17F8EF3}

Mit errechneten Metriken können Sie benutzerdefinierte Metriken erstellen, die aus Segmenten oder mathematischen Berechnungen abgeleitet wurden. In der Vergangenheit hätten Sie vielleicht die `SiteCatlayst:Event` Mbox verwendet, in der `evar27=shoes` und das Ereignis `purchase` lauteten. Jetzt erstellen Sie ein Segment mit `evar27=shoes` und anschließend eine errechnete Metrik, in der das Ereignis mit dem übernommenen Segment `purchase` lautet. Diese Metriken können jederzeit erstellt werden, auch nach der Aktivität. Anschließend können sie für jeden Bericht in Analytics verwendet werden.

## Ordnet A4T mehreren Kampagnen die Konversionen zu?   {#section_7F15C727206440CD86B3A8CE77087DF9}

Ja, mit der Einstellung &quot;Vollständige Zuordnung&quot;.
