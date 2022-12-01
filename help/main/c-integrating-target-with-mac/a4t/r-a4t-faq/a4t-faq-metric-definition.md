---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Metrik; Metrikdefinitionen
description: Antworten auf Fragen zu Metrikdefinitionen und zur Verwendung von Analytics für [!DNL Target] (A4T). Mit A4T können Sie Analytics-Reporting mit Adobe verwenden [!DNL Target] Aktivitäten.
title: Wo finde ich Informationen über Metrikdefinitionen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 29%

---

# Metrikdefinitionen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu Metrikdefinitionen und zur Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T).

## Wie ist die Gültigkeit für eine Aktivitätsmitgliedschaft? Wie lange werden nach Eintritt der Besucher in die Aktivität ihre Aktionen in der Aktivität gezählt, wenn sie sie nicht erneut sehen? {#section_41B4958F33534E4B96DEE0C981227A79}

+++Antwort Die Standardgültigkeit für die Aktivität beträgt 90 Tage nach der letzten Interaktion eines Besuchers mit der Aktivität. Diese Einstellung kann bei Bedarf von ClientCare angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

+++

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen? {#adv-settings}

++ + Antwort auf die [!UICONTROL Erweiterte Einstellungen] -Optionen sind nicht für Aktivitäten verfügbar, die [!DNL Analytics] als Berichtsquelle (A4T).

Bei Aktivitäten, die A4T verwenden, verwendet die Zielmetrik immer die[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]&quot; und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen sind *not* konfigurierbar.

Bei Nicht-A4T-Aktivitäten können Sie die [Optionen für erweiterte Einstellungen](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) um zu verwalten, wie Sie Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder sie entfernen soll und ob die Metrik einmal pro Teilnehmer oder bei jeder Impression gezählt werden soll. Sie können auf die [!UICONTROL Erweiterte Einstellungen] Optionen in einer Nicht-A4T-Aktivität durch Klicken auf die vertikalen Ellipsen > [!UICONTROL Erweiterte Einstellungen], wie unten dargestellt:

![Erweiterte Einstellungen](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## Was sind errechnete Metriken und wie ersetzen sie die SiteCatalyst:Event-Mbox, die ich vorher verwendet habe?  {#section_D59F4719E6B94758A2187427C17F8EF3}

+++ Beantworten Mit berechneten Metriken können Sie benutzerdefinierte Metriken erstellen, die aus Segmenten oder mathematischen Berechnungen abgeleitet wurden. In der Vergangenheit hätten Sie vielleicht die `SiteCatlayst:Event` Mbox verwendet, in der `evar27=shoes` und das Ereignis `purchase` lauteten. Jetzt erstellen Sie ein Segment mit `evar27=shoes` und anschließend eine errechnete Metrik, in der das Ereignis mit dem übernommenen Segment `purchase` lautet. Diese Metriken können jederzeit erstellt werden, selbst wenn die Aktivität bereits begonnen hat. Anschließend können sie für jeden Bericht in Analytics verwendet werden.

+++

## Ordnet A4T mehreren Kampagnen die Konversionen zu?  {#section_7F15C727206440CD86B3A8CE77087DF9}

+++Antwort Ja, mit der Einstellung &quot;Vollständige Zuordnung&quot;.

+++