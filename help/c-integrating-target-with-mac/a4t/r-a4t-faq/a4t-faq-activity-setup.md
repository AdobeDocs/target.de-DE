---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Aktivitätseinrichtung
description: Antworten auf Fragen zur Einrichtung der Aktivität bei der Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten
title: Wo finde ich FAQs zu den Einstellungen für die Aktivität mit A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 23%

---

# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Einrichtung und Verwendung von [!DNL Analytics] als Berichte für [!DNL Target] (A4T).

## Welche Aktivitätstypen unterstützen Analytics als Berichtsquelle (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf Erweiterte Einstellungen zugreifen?

Bei Aktivitäten, die [!DNL Analytics] als Berichte-Quelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität halten]&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen können nicht konfiguriert werden.**

Weitere Informationen finden Sie unter &quot;Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen?&quot; in [Metrikdefinitionen - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}

Wenn eine Aktivität erstellt wird, sendet [!DNL Target] eine Classification-Datei an [!DNL Analytics]. Obwohl [!DNL Analytics] die Daten erfasst und verarbeitet, wird dies in den Berichten erst angezeigt, wenn die Classification-Datei aktualisiert wurde. Dieser Vorgang kann bis zu 24 Stunden dauern. Wenn Ihre Daten auch nach 48 Stunden noch nicht angezeigt werden, [wenden Sie sich an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten, können Sie die Aktivität auch einige Tage vorher erstellen und die Klassifizierungen werden gesendet, wenn die Aktivität gespeichert wird. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Bitte beachten Sie, dass die Datenverarbeitung in [!DNL Analytics] 45-90 Minuten dauert.

## Warum kann ich Analytics nicht als meine Berichte-Quelle auswählen, wenn ich eine Aktivität erstelle? {#section_9F4F69C3085F4C2480AF439127EB27CD}

Sie können die Optionen [!UICONTROL Berichte-Einstellungen] in [!UICONTROL Administration] ändern.

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]**.
1. Klicken Sie in der Dropdownliste **[!UICONTROL Für die Berichterstellung verwendete Experience Cloud-Lösung]** auf **[!UICONTROL Pro Aktivität auswählen]**.

![](assets/select-per-activity.png)

Die Dropdownliste **[!UICONTROL Berichterstellungsquelle]** wird auf dem Bildschirm **[!UICONTROL Ziele und Einstellungen]** für Erstellungs- und Bearbeitungsaktivitäten aktiviert.

Um immer [!DNL Analytics] als Berichte-Quelle zu verwenden, wählen Sie **[!UICONTROL Adobe Analytics]** aus der Dropdown-Liste in [!UICONTROL Administration].

## Kann ein Besucher in einer Aktivität mit automatisierter Zielgruppe, die A4T verwendet, zwischen zielgerichteten und kontrollierten Erlebnissen bei verschiedenen Besuchen wechseln?

Folgendes gilt, wenn die visitorId für einen Besucher zwischen Besuchen nicht geändert wird.

Wenn der Prozentsatz für die Traffic-Zuordnung in der Mitte der Aktivität angepasst wird, kann es sein, dass ein Besucher zwischen zielgerichteten Erlebnissen und Kontrollerlebnissen wechseln kann.

Wenn die Prozentwerte nicht in der Mitte der Aktivität angepasst werden, wird ein Besucher, der die Steuerung anfänglich sieht, immer zur Kontrolle gesendet. Ein Besucher, der an zielgerichtete Erlebnisse gesendet wird, wird immer an zielgerichtete Erlebnisse gesendet.

* Nachdem der Besucher sich im zielgerichteten Traffic-Behälter befindet, kann er von Besuch zu Besuch an ein anderes Erlebnis gesendet werden, wenn die Modelle für maschinelles Lernen feststellen, dass ein anderes Erlebnis für den neuen Besuch relevant ist.
* Nachdem einem Besucher das Kontrollelement &quot;Bucket&quot;für Traffic zugewiesen wurde, wird immer dasselbe Erlebnis angezeigt, da die Erlebniszuweisung auf einem deterministischen Pseudo-Zufall-Hash der visitorId des Besuchers basiert.
