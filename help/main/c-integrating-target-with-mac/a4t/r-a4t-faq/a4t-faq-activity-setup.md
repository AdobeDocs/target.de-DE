---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Aktivitätseinrichtung
description: Hier finden Sie Antworten auf Fragen zur Aktivitätseinrichtung bei der Verwendung von Analytics für [!DNL Target]  (A4T). Mit A4T können Sie Analytics-Berichte für [!DNL Target] Aktivitäten verwenden.
title: Wo finde ich häufig gestellte Fragen zu Aktivitätseinstellungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 6%

---

# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Aktivitätseinrichtung und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) gestellte Fragen.

## Welche Aktivitätstypen unterstützen [!DNL Analytics] als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

+++Antwort
Eine vollständige Liste finden Sie unter &quot;Unterstützte Aktivitätstypen&quot;in [Adobe Analytics als Reporting-Source für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

+++

## Kann ich bei der Verwendung von A4T-Berichten denselben Aktivitätsnamen für zwei Aktivitäten aus separaten Arbeitsbereichen verwenden?

+++Antwort

Verwenden Sie nicht denselben Aktivitätsnamen für zwei Aktivitäten aus separaten [Arbeitsbereichen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md), die A4T-Berichte verwenden.

Obwohl dies bei Verwendung von [!DNL Target] als Berichtsquelle unterstützt wird, wird die Verwendung desselben Aktivitätsnamens für zwei Aktivitäten nicht unterstützt, wenn [!UICONTROL Analytics for Target] als Berichtsquelle verwendet wird.

+++

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf Erweiterte Einstellungen zugreifen?

+++Antwort
Bei Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;und &quot;[!UICONTROL On Every Impression]&quot;. Diese Einstellungen sind *nicht* konfigurierbar.

Weitere Informationen finden Sie unter &quot;Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die erweiterten Einstellungsoptionen zugreifen?&quot; in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}


+++Antwort
Wenn eine Aktivität erstellt wird, sendet [!DNL Target] eine Classification-Datei an [!DNL Analytics]. Obwohl [!DNL Analytics] die Daten erfasst und verarbeitet, wird dies erst nach Aktualisierung der Classification-Datei in den Berichten angezeigt. Dieser Vorgang kann 24 bis 72 Stunden dauern. Wenn Ihre Daten nach 72 Stunden nicht mehr angezeigt werden, kontaktieren Sie [den Kundendienst](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten, können Sie die Aktivität auch ein paar Tage zuvor erstellen und die Classifications werden bei der Speicherung der Aktivität gesendet. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Bitte beachten Sie, dass es 45-90 Minuten dauert, bis Daten in [!DNL Analytics] verarbeitet werden.

+++

## Warum kann ich Analytics nicht als meine Berichterstellungsquelle auswählen, wenn ich eine Aktivität erstelle? {#section_9F4F69C3085F4C2480AF439127EB27CD}

+++Antwort
Sie können Ihre [!UICONTROL Reporting Settings]-Optionen in [!UICONTROL Administration] ändern.

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]**.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Experience Cloud solution used for reporting]** auf **[!UICONTROL Select per Activity]**.

![Bild pro Aktivität ](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Reporting Source]** ist auf dem Bildschirm **[!UICONTROL Goal & Settings]** für die Erstellung und Bearbeitung von Aktivitäten aktiviert.

Um immer [!DNL Analytics] als Berichtsquelle zu verwenden, wählen Sie **[!UICONTROL Adobe Analytics]** aus der Dropdownliste in [!UICONTROL Administration] aus.

+++

## Kann ein Besucher in einer Aktivität vom Typ Automatisches Targeting, die A4T verwendet, in verschiedenen Besuchen zwischen zielgerichteten und kontrollierten Erlebnissen wechseln?

+++Antwort
Folgendes gilt, vorausgesetzt, die visitorId ändert sich für einen Besucher zwischen Besuchen nicht.

Wenn der Prozentsatz der Traffic-Zuordnung mitten in der Aktivität angepasst wird, kann ein Besucher zwischen zielgerichteten Erlebnissen und Kontrollerlebnissen wechseln.

Wenn die Prozentsätze nicht während der Aktivität angepasst werden, wird ein Besucher, der das Steuerelement anfänglich sieht, immer zur Kontrolle gesendet. Ein Besucher, der an zielgerichtete Erlebnisse gesendet wird, wird immer an zielgerichtete Erlebnisse gesendet.

* Nachdem der Besucher in der zielgerichteten Traffic-Gruppe enthalten war, kann er von Besuch zu Besuch an ein anderes Erlebnis gesendet werden, wenn die Modelle für maschinelles Lernen feststellen, dass ein anderes Erlebnis für den neuen Besuch relevant ist.
* Nachdem einem Besucher das Kontrollelement &quot;Bucket&quot;des Traffics zugewiesen wurde, wird ihm immer dasselbe Erlebnis angezeigt, da die Erlebniszuweisung auf einem deterministischen Pseudo-zufälligen Hash der visitorId des Besuchers basiert.

+++

## Kann ich eine binomielle [!DNL Analytics] -Metrik verwenden, bei der ein Segment als Optimierungsziel in einer [!UICONTROL Auto-Allocate] -Aktivität angewendet wird? {#binomial}

+++Antwort
Sie können keine [!DNL Analytics] -Metrik verwenden, bei der ein Segment als Optimierungsziel in einer [!UICONTROL Auto-Allocate] -Aktivität angewendet wird. Als Problemumgehung können Sie ein benutzerspezifisches Ereignis definieren, das dasselbe Ziel erreicht und als Optimierungszielmetrik verwendet.

+++