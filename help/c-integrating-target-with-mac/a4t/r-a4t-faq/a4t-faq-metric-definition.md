---
keywords: faq;frequently asked questions;analytics for target;a4T;metric;metric definitions
description: Dieses Thema enthält Antworten auf häufig zu Metrikdefinitionen und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Metrikdefinitionen – Häufig gestellte Fragen zu A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: a12eea60aa3e66cdb54ab284fa3f942be4d56178
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 65%

---


# Metrikdefinitionen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu Metrikdefinitionen und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Wie ist die Gültigkeit für eine Aktivitätsmitgliedschaft? Wie lange werden die Aktionen von Besuchern nach deren Teilnahme an der Aktivität in der Aktivität gezählt, wenn sie sie nicht erneut anzeigen?   {#section_41B4958F33534E4B96DEE0C981227A79}

Die Standardgültigkeit für die Aktivität beträgt 90 Tage nach der letzten Interaktion des Besuchers mit der Aktivität. Dies kann von der Kundenbetreuung bei Bedarf angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

## Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die Optionen für erweiterte Einstellungen zugreifen? {#adv-settings}

Die Optionen [!UICONTROL Erweiterte Einstellungen] stehen nicht für Aktivitäten zur Verfügung, die [!DNL Analytics] als Berichte-Quelle (A4T) verwenden.

Bei Aktivitäten, die A4T verwenden, verwendet die Zielmetrik immer die Einstellungen &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität halten]&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Dies ist *nicht* konfigurierbar.

Bei Nicht-A4T-Aktivitäten können Sie mit den Optionen [Erweiterte Einstellungen](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) verwalten, wie Sie den Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder entfernt werden soll und ob die Metrik einmal pro Teilnehmer oder bei jeder Impression gezählt werden soll. Sie können auf die Optionen [!UICONTROL Erweiterte Einstellungen] in einer Nicht-A4T-Aktivität zugreifen, indem Sie auf die senkrechten Auslassungspunkte > [!UICONTROL Erweiterte Einstellungen] klicken, wie unten dargestellt:

![Erweiterte Einstellungen](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

## Was sind errechnete Metriken und wie ersetzen sie die SiteCatalyst:Event-Mbox, die ich vorher verwendet habe?   {#section_D59F4719E6B94758A2187427C17F8EF3}

Mit errechneten Metriken können Sie benutzerdefinierte Metriken erstellen, die aus Segmenten oder mathematischen Berechnungen abgeleitet wurden. In der Vergangenheit hätten Sie vielleicht die `SiteCatlayst:Event` Mbox verwendet, in der `evar27=shoes` und das Ereignis `purchase` lauteten. Jetzt erstellen Sie ein Segment mit `evar27=shoes` und anschließend eine errechnete Metrik, in der das Ereignis mit dem übernommenen Segment `purchase` lautet. Der Vorteil daran ist, dass diese Metriken zu jeder Zeit erstellt werden können, selbst wenn die Aktivität bereits begonnen hat. Anschließend können sie für jeden Bericht in Analytics verwendet werden.

## Ordnet A4T mehreren Kampagnen die Konversionen zu?   {#section_7F15C727206440CD86B3A8CE77087DF9}

Ja. Dies wird mithilfe der Einstellung „Vollständige Zuordnung“ durchgeführt.
