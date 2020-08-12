---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: Dieses Thema enthält Antworten auf häufig zum Aktivitäts-Setup und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T
feature: null
topic: Standard
uuid: 3472ab3c-908b-40f8-81a6-512dccde64a6
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 89%

---


# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T{#activity-settings-a-t-faq}

Dieses Thema enthält Antworten auf häufig zum Aktivitäts-Setup und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Welche Aktivitätstypen unterstützen Analytics als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](../../../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}

Beim Erstellen einer Aktivität sendet Target eine Classifications-Datei an Analytics. Obwohl Analytics die Daten erfasst und verarbeitet, werden sie erst nach der Aktualisierung der Classifications-Datei in den Berichten angezeigt. Dies kann bis zu 24 Stunden dauern. Wenn Ihre Daten auch nach 48 Stunden noch nicht angezeigt werden, [wenden Sie sich an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten möchten, können Sie die Aktivität auch schon einige Tage im Voraus erstellen. Die Classifications werden dann gesendet, wenn die Aktivität gespeichert wird. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Bitte beachten Sie, dass es zwischen 45 und 90 Minuten dauern kann, bis die Daten in Analytics verarbeitet werden.

## Warum kann ich Analytics nicht als meine Berichterstellungsquelle auswählen, wenn ich eine neue Aktivität erstelle?  {#section_9F4F69C3085F4C2480AF439127EB27CD}

Sie können die Optionen für die Berichte-Einstellungen in Administration ändern.

1. In Adobe Target, click **[!UICONTROL Administration]**.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Für die Berichterstellung verwendete Experience Cloud-Lösung]** auf **[!UICONTROL Pro Aktivität auswählen]**.

![](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Berichterstellungsquelle]** wird auf dem Bildschirm **[!UICONTROL Ziele und Einstellungen]** für Erstellungs- und Bearbeitungsaktivitäten aktiviert.

To always use Analytics as the reporting source, select **[!UICONTROL Adobe Analytics]** from the drop-down list in Administration.
