---
keywords: faq;frequently asked questions;analytics for target;a4T;metric;metric definitions
description: Dieses Thema enthält Antworten auf häufig zu Metrikdefinitionen und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Metrikdefinitionen – Häufig gestellte Fragen zu A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 100%

---


# Metrikdefinitionen – Häufig gestellte Fragen zu A4T{#metric-definitions-a-t-faq}

Dieses Thema enthält Antworten auf häufig zu Metrikdefinitionen und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Wie ist die Gültigkeit für eine Aktivitätsmitgliedschaft? Wie lange werden die Aktionen von Besuchern nach deren Teilnahme an der Aktivität in der Aktivität gezählt, wenn sie sie nicht erneut anzeigen?  {#section_41B4958F33534E4B96DEE0C981227A79}

Die Standardgültigkeit für die Aktivität beträgt 90 Tage nach der letzten Interaktion des Besuchers mit der Aktivität. Dies kann von der Kundenbetreuung bei Bedarf angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

## Funktionieren die erweiterten Optionen für Erfolgsmetriken in Target mit A4T?  {#section_F060E3438F4144258BB95813EDEABDAA}

Diese Optionen funktionieren zurzeit nicht mit A4T.

## Was sind errechnete Metriken und wie ersetzen sie die SiteCatalyst:Event-Mbox, die ich vorher verwendet habe?  {#section_D59F4719E6B94758A2187427C17F8EF3}

Mit errechneten Metriken können Sie benutzerdefinierte Metriken erstellen, die aus Segmenten oder mathematischen Berechnungen abgeleitet wurden. In der Vergangenheit hätten Sie vielleicht die `SiteCatlayst:Event` Mbox verwendet, in der `evar27=shoes` und das Ereignis `purchase` lauteten. Jetzt erstellen Sie ein Segment mit `evar27=shoes` und anschließend eine errechnete Metrik, in der das Ereignis mit dem übernommenen Segment `purchase` lautet. Der Vorteil daran ist, dass diese Metriken zu jeder Zeit erstellt werden können, selbst wenn die Aktivität bereits begonnen hat. Anschließend können sie für jeden Bericht in Analytics verwendet werden.

## Ordnet A4T mehreren Kampagnen die Konversionen zu?  {#section_7F15C727206440CD86B3A8CE77087DF9}

Ja. Dies wird mithilfe der Einstellung „Vollständige Zuordnung“ durchgeführt.
