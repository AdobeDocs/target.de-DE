---
description: Dieses Thema enthält Antworten auf häufig zum Aktivitäts-Setup und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Aktivitätseinrichtung
seo-description: Dieses Thema enthält Antworten auf häufig zum Aktivitäts-Setup und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
seo-title: Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T
solution: Target
title: Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T
topic: Standard
uuid: 3472ab3c-908b-40f8-81a6-512dccde64a6
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T{#activity-settings-a-t-faq}

Dieses Thema enthält Antworten auf häufig zum Aktivitäts-Setup und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Welche Aktivitätstypen unterstützen Analytics als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](../../../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}

Beim Erstellen einer Aktivität sendet Target eine Classifications-Datei an Analytics. Obwohl Analytics die Daten erfasst und verarbeitet, werden sie erst nach der Aktualisierung der Classifications-Datei in den Berichten angezeigt. Dies kann bis zu 24 Stunden dauern. Wenn Ihre Daten nach 48 Stunden nicht angezeigt werden, [wenden Sie sich an den Kundendienst](https://marketing.adobe.com/resources/help/de_DE/target/target/r_problem.html). Wenn Sie wissen, dass Sie eine Aktivität starten möchten, können Sie die Aktivität auch schon einige Tage im Voraus erstellen. Die Classifications werden dann gesendet, wenn die Aktivität gespeichert wird. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Bitte beachten Sie, dass es zwischen 45 und 90 Minuten dauern kann, bis die Daten in Analytics verarbeitet werden.

## Warum kann ich Analytics nicht als meine Berichterstellungsquelle auswählen, wenn ich eine neue Aktivität erstelle? {#section_9F4F69C3085F4C2480AF439127EB27CD}

Sie können Ihre Berichterstellungseinstellungen bei der Einrichtung ändern.

1. Klicken Sie in Adobe Target auf **[!UICONTROL Einrichten]**.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Für die Berichterstellung verwendete Experience Cloud-Lösung]** auf **[!UICONTROL Pro Aktivität auswählen]**.

![](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Berichterstellungsquelle]** wird auf dem Bildschirm **Ziele und Einstellungen]für Erstellungs- und Bearbeitungsaktivitäten aktiviert.[!UICONTROL **

Möchten Sie stets Analytics als Berichtsquelle verwenden, wählen Sie aus der Dropdownliste in der Einrichtung die Option **[!UICONTROL Adobe Analytics]aus.**
