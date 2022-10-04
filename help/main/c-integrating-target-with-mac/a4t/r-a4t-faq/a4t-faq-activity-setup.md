---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Aktivitätseinrichtung
description: Antworten auf Fragen zur Aktivitätseinrichtung bei der Verwendung von Analytics für [!DNL Target] (A4T). Mit A4T können Sie Analytics-Reporting für [!DNL Target] Aktivitäten.
title: Wo finde ich häufig gestellte Fragen zu Aktivitätseinstellungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 20%

---

# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Aktivitätseinrichtung und Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T).

## Welche Aktivitätstypen unterstützen Analytics als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf Erweiterte Einstellungen zugreifen?

Für Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik den[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]&quot; und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen sind *not* konfigurierbar.

Weitere Informationen finden Sie unter &quot;Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die erweiterten Einstellungsoptionen zugreifen?&quot; in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}

Wenn eine Aktivität erstellt wird, [!DNL Target] sendet eine Classification-Datei an [!DNL Analytics]. Obwohl [!DNL Analytics] erfasst und verarbeitet die Daten, wird dies erst nach Aktualisierung der Classification-Datei in den Berichten angezeigt. Dieser Vorgang kann bis zu 24 Stunden dauern. Wenn Ihre Daten auch nach 48 Stunden noch nicht angezeigt werden, [wenden Sie sich an den Kundendienst](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten, können Sie die Aktivität auch ein paar Tage zuvor erstellen und die Classifications werden bei der Speicherung der Aktivität gesendet. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Bitte beachten Sie, dass es 45-90 Minuten dauert, bis Daten in [!DNL Analytics].

## Warum kann ich Analytics nicht als meine Berichterstellungsquelle auswählen, wenn ich eine Aktivität erstelle? {#section_9F4F69C3085F4C2480AF439127EB27CD}

Sie können Ihre [!UICONTROL Berichtseinstellungen] Optionen in [!UICONTROL Administration].

1. In [!DNL Target]klicken **[!UICONTROL Administration]**.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Für die Berichterstellung verwendete Experience Cloud-Lösung]** auf **[!UICONTROL Pro Aktivität auswählen]**.

![Abbild &quot;select-per-activity&quot;](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Berichterstellungsquelle]** wird auf dem Bildschirm **[!UICONTROL Ziele und Einstellungen]** für Erstellungs- und Bearbeitungsaktivitäten aktiviert.

Verwendung von [!DNL Analytics] als Berichtsquelle auswählen **[!UICONTROL Adobe Analytics]** aus der Dropdownliste in [!UICONTROL Administration].

## Kann ein Besucher in einer Aktivität vom Typ Automatisches Targeting, die A4T verwendet, in verschiedenen Besuchen zwischen zielgerichteten und kontrollierten Erlebnissen wechseln?

Folgendes gilt, vorausgesetzt, die visitorId ändert sich für einen Besucher zwischen Besuchen nicht.

Wenn der Prozentsatz der Traffic-Zuordnung mitten in der Aktivität angepasst wird, kann ein Besucher zwischen zielgerichteten Erlebnissen und Kontrollerlebnissen wechseln.

Wenn die Prozentsätze nicht während der Aktivität angepasst werden, wird ein Besucher, der das Steuerelement anfänglich sieht, immer zur Kontrolle gesendet. Ein Besucher, der an zielgerichtete Erlebnisse gesendet wird, wird immer an zielgerichtete Erlebnisse gesendet.

* Nachdem der Besucher in der zielgerichteten Traffic-Gruppe enthalten war, kann er von Besuch zu Besuch an ein anderes Erlebnis gesendet werden, wenn die Modelle für maschinelles Lernen feststellen, dass ein anderes Erlebnis für den neuen Besuch relevant ist.
* Nachdem einem Besucher das Kontrollelement &quot;Bucket&quot;des Traffics zugewiesen wurde, wird ihm immer dasselbe Erlebnis angezeigt, da die Erlebniszuweisung auf einem deterministischen Pseudo-zufälligen Hash der visitorId des Besuchers basiert.


## Kann ich ein Binomialsystem verwenden? [!DNL Analytics] Metrik mit einem Segment, das als Optimierungsziel in einer [!UICONTROL Automatische Zuordnung] Aktivität? {#binomial}

Sie können keine [!DNL Analytics] Metrik mit einem Segment, das als Optimierungsziel in einer [!UICONTROL Automatische Zuordnung] Aktivität. Als Problemumgehung können Sie ein benutzerspezifisches Ereignis definieren, das dasselbe Ziel erreicht und als Optimierungszielmetrik verwendet.