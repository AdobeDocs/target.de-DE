---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Aktivitätseinrichtung
description: Hier finden Sie Antworten auf Fragen zur Aktivitätseinrichtung bei der Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten.
title: Wo finde ich häufig gestellte Fragen zu Aktivitätseinstellungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 15ca5e92af5ebc66caa52ffc1dc04e1fbcbb2ed3
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 20%

---

# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Aktivitätseinrichtung und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) gestellte Fragen.

## Welche Aktivitätstypen unterstützen Analytics als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf Erweiterte Einstellungen zugreifen?

Bei Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen sind *nicht* konfigurierbar.

Weitere Informationen finden Sie unter &quot;Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die erweiterten Einstellungsoptionen zugreifen?&quot; in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}

Wenn eine Aktivität erstellt wird, sendet [!DNL Target] eine Classification-Datei an [!DNL Analytics]. Obwohl [!DNL Analytics] die Daten erfasst und verarbeitet, zeigt  dies in den Berichten erst nach Aktualisierung der Classification-Datei an. Dieser Vorgang kann bis zu 24 Stunden dauern. Wenn Ihre Daten auch nach 48 Stunden noch nicht angezeigt werden, [wenden Sie sich an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten, können Sie die Aktivität auch ein paar Tage zuvor erstellen und die Classifications werden bei der Speicherung der Aktivität gesendet. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Bitte beachten Sie, dass es 45-90 Minuten dauert, bis Daten in [!DNL Analytics] verarbeitet werden.

## Warum kann ich Analytics nicht als meine Berichterstellungsquelle auswählen, wenn ich eine Aktivität erstelle? {#section_9F4F69C3085F4C2480AF439127EB27CD}

Sie können die [!UICONTROL Berichtseinstellungen] in [!UICONTROL Administration] ändern.

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]**.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Für die Berichterstellung verwendete Experience Cloud-Lösung]** auf **[!UICONTROL Pro Aktivität auswählen]**.

![](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Berichterstellungsquelle]** wird auf dem Bildschirm **[!UICONTROL Ziele und Einstellungen]** für Erstellungs- und Bearbeitungsaktivitäten aktiviert.

Um immer [!DNL Analytics] als Berichtsquelle zu verwenden, wählen Sie **[!UICONTROL Adobe Analytics]** aus der Dropdownliste in [!UICONTROL Administration] aus.

## Kann ein Besucher in einer Aktivität vom Typ Automatisches Targeting, die A4T verwendet, in verschiedenen Besuchen zwischen zielgerichteten und kontrollierten Erlebnissen wechseln?

Folgendes gilt, vorausgesetzt, die visitorId ändert sich für einen Besucher zwischen Besuchen nicht.

Wenn der Prozentsatz der Traffic-Zuordnung mitten in der Aktivität angepasst wird, kann ein Besucher zwischen zielgerichteten Erlebnissen und Kontrollerlebnissen wechseln.

Wenn die Prozentsätze nicht während der Aktivität angepasst werden, wird ein Besucher, der das Steuerelement anfänglich sieht, immer zur Kontrolle gesendet. Ein Besucher, der an zielgerichtete Erlebnisse gesendet wird, wird immer an zielgerichtete Erlebnisse gesendet.

* Nachdem der Besucher in der zielgerichteten Traffic-Gruppe enthalten war, kann er von Besuch zu Besuch an ein anderes Erlebnis gesendet werden, wenn die Modelle für maschinelles Lernen feststellen, dass ein anderes Erlebnis für den neuen Besuch relevant ist.
* Nachdem einem Besucher das Kontrollelement &quot;Bucket&quot;des Traffics zugewiesen wurde, wird ihm immer dasselbe Erlebnis angezeigt, da die Erlebniszuweisung auf einem deterministischen Pseudo-zufälligen Hash der visitorId des Besuchers basiert.


## Kann ich eine binomielle [!DNL Analytics]-Metrik verwenden, bei der ein Segment als Optimierungsziel in einer [!UICONTROL Aktivität mit automatischer Zuordnung] angewendet wird? {#binomial}

Sie können keine [!DNL Analytics]-Metrik verwenden, bei der ein Segment als Optimierungsziel in einer [!UICONTROL Aktivität vom Typ &quot;Automatische Zuordnung]&quot;angewendet wird. Als Problemumgehung können Sie ein benutzerspezifisches Ereignis definieren, das dasselbe Ziel erreicht und als Optimierungszielmetrik verwendet.