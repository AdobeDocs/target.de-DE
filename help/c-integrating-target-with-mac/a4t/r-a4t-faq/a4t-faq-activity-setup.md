---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: Dieses Thema enthält Antworten auf häufig zum Aktivitäts-Setup und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: a12eea60aa3e66cdb54ab284fa3f942be4d56178
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 36%

---


# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T

This topic contains answers to questions that are frequently asked about activity setup and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Welche Aktivitätstypen unterstützen Analytics als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Warum kann ich bei der Konfiguration meiner Zielmetrik nicht auf Erweiterte Einstellungen zugreifen?

Bei Aktivitäten, die [!DNL Analytics] als Berichte-Quelle (A4T) verwendet werden, verwendet die Zielmetrik immer die Einstellungen &quot;Anzahl[!UICONTROL erhöhen und Benutzer in Aktivität]halten&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Dies ist *nicht* konfigurierbar.

Weitere Informationen finden Sie unter &quot;Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die Optionen für erweiterte Einstellungen zugreifen?&quot; in [Metric definitions - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}

When an activity is created, [!DNL Target] sends a classification file to [!DNL Analytics]. Although [!DNL Analytics] is capturing the and processing the data, it does not show in the reports until the classification file has been updated. Dies kann bis zu 24 Stunden dauern. Wenn Ihre Daten auch nach 48 Stunden noch nicht angezeigt werden, [wenden Sie sich an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten möchten, können Sie die Aktivität auch schon einige Tage im Voraus erstellen. Die Classifications werden dann gesendet, wenn die Aktivität gespeichert wird. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Please note that it takes 45-90 minutes for data to be processed in [!DNL Analytics].

## Warum kann ich Analytics nicht als meine Berichterstellungsquelle auswählen, wenn ich eine neue Aktivität erstelle?  {#section_9F4F69C3085F4C2480AF439127EB27CD}

You can change your [!UICONTROL Reporting Settings] options in [!UICONTROL Administration].

1. Klicken Sie [!DNL Target]in &quot; **[!UICONTROL Administration]**&quot;.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Für die Berichterstellung verwendete Experience Cloud-Lösung]** auf **[!UICONTROL Pro Aktivität auswählen]**.

![](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Berichterstellungsquelle]** wird auf dem Bildschirm **[!UICONTROL Ziele und Einstellungen]** für Erstellungs- und Bearbeitungsaktivitäten aktiviert.

To always use [!DNL Analytics] as the reporting source, select **[!UICONTROL Adobe Analytics]** from the drop-down list in [!UICONTROL Administration].

## Kann ein Besucher in einer Aktivität mit automatisierter Zielgruppe, die A4T verwendet, zwischen zielgerichteten und kontrollierten Erlebnissen bei verschiedenen Besuchen wechseln?

Folgendes gilt, wenn die visitorId für einen Besucher zwischen Besuchen nicht geändert wird.

Wenn der Prozentsatz für die Traffic-Zuordnung in der Mitte der Aktivität angepasst wird, kann es sein, dass ein Besucher zwischen zielgerichteten Erlebnissen und Kontrollerlebnissen wechseln kann.

Wenn die Prozentsätze nicht in der Mitte der Aktivität angepasst werden, wird ein Besucher, der die Kontrolle anfänglich sieht, immer zur Kontrolle gesendet. Ein Besucher, der an zielgerichtete Erlebnisse gesendet wird, wird immer an zielgerichtete Erlebnisse gesendet.

* Nachdem der Besucher sich im zielgerichteten Traffic-Behälter befindet, kann er von Besuch zu Besuch an ein anderes Erlebnis gesendet werden, wenn die Modelle für maschinelles Lernen feststellen, dass ein anderes Erlebnis für den neuen Besuch relevant ist.
* Nachdem einem Besucher das Kontrollelement &quot;Bucket&quot;für Traffic zugewiesen wurde, wird immer dasselbe Erlebnis angezeigt, da die Erlebniszuweisung auf einem deterministischen Pseudo-Zufall-Hash der visitorId des Besuchers basiert.
