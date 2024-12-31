---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Aktivitätseinrichtung
description: Hier finden Sie Antworten auf Fragen zum Einrichten von Aktivitäten bei der Verwendung von Analytics für  [!DNL Target] A4T). Mit A4T können Sie Analytics-Berichte für - [!DNL Target]  verwenden.
title: Wo finde ich häufig gestellte Fragen zu Aktivitätseinstellungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 6%

---

# Aktivitätseinstellungen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Einrichtung von Aktivitäten und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T).

## Welche Aktivitätstypen werden [!DNL Analytics] als Berichtsquelle (A4T) unterstützt? {#section_5E4F58CD25A5424E869E6FE0803968EF}

+++Antwort
Eine vollständige Liste finden Sie unter „Unterstützte Aktivitätstypen“ in [Adobe Analytics as the Reporting Source for Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

+++

## Kann ich denselben Aktivitätsnamen für zwei Aktivitäten aus separaten Arbeitsbereichen verwenden, wenn ich A4T-Berichte verwende?

+++Antwort

Verwenden Sie nicht denselben Aktivitätsnamen für zwei Aktivitäten aus separaten [Arbeitsbereichen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) die A4T-Berichte verwenden.

Auch wenn dies bei Verwendung von [!DNL Target] als Berichtsquelle unterstützt wird, wird bei Verwendung von [!UICONTROL Analytics for Target] als Berichtsquelle die Verwendung desselben Aktivitätsnamens für zwei Aktivitäten nicht unterstützt.

+++

## Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen?

+++Antwort
Bei Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; und &quot;[!UICONTROL On Every Impression]&quot;. Diese Einstellungen *nicht*.

Weitere Informationen finden Sie unter „Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen?“. in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Ich habe soeben eine Aktivität erstellt. Warum werden keine Daten angezeigt? {#section_9F8092BE4225442896F926540292F221}


+++Antwort
Wenn eine Aktivität erstellt wird, sendet [!DNL Target] eine Classification-Datei an [!DNL Analytics]. Obwohl [!DNL Analytics] die Daten erfasst und verarbeitet, wird dies in den Berichten erst dann angezeigt, wenn die Klassifizierungsdatei aktualisiert wurde. Dieser Vorgang kann 24 bis 72 Stunden dauern. Wenn Sie nach 72 Stunden Ihre Daten nicht sehen, wenden Sie [an die Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Wenn Sie wissen, dass Sie eine Aktivität starten, können Sie die Aktivität auch einige Tage zuvor erstellen. Die Klassifizierungen werden beim Speichern der Aktivität gesendet. Dadurch werden Ihre Daten gleich beim Start in den Berichten angezeigt. Beachten Sie, dass die Verarbeitung von Daten in [!DNL Analytics] 45-90 Minuten dauert.

+++

## Warum kann ich beim Erstellen einer Aktivität nicht Analytics als Berichtsquelle auswählen? {#section_9F4F69C3085F4C2480AF439127EB27CD}

+++Antwort
Sie können Ihre [!UICONTROL Reporting Settings] in [!UICONTROL Administration] ändern.

1. Klicken Sie [!DNL Target] auf **[!UICONTROL Administration]**.
1. Klicken Sie in der Dropdown-Liste **[!UICONTROL Experience Cloud solution used for reporting]** auf **[!UICONTROL Select per Activity]**.

![Bild für jede Aktivität auswählen](assets/select-per-activity.png)

Die Dropdown-Liste &quot;**[!UICONTROL Reporting Source]**&quot; im Bildschirm &quot;**[!UICONTROL Goal & Settings]**&quot; ist zum Erstellen und Bearbeiten von Aktivitäten aktiviert.

Um [!DNL Analytics] immer als Berichtsquelle zu verwenden, wählen Sie **[!UICONTROL Adobe Analytics]** aus der Dropdown-Liste in [!UICONTROL Administration] aus.

+++

## Kann ein Besucher bei verschiedenen Besuchen in einer automatischen Targeting-Aktivität, die A4T verwendet, zwischen zielgerichteten und gesteuerten Erlebnissen wechseln?

+++Antwort
Im Folgenden wird davon ausgegangen, dass sich die visitorId für einen Besucher zwischen den Besuchen nicht ändert.

Wenn der Prozentsatz der Traffic-Zuordnung während der Aktivität angepasst wird, ist es möglich, dass ein Besucher zwischen Targeting- und Kontrollerlebnissen wechseln kann.

Wenn die Prozentsätze nicht während der Aktivität angepasst werden, wird ein Besucher, der das Steuerelement anfänglich sieht, immer an das Steuerelement gesendet. Ein Besucher, der an zielgerichtete Erlebnisse gesendet wird, wird immer an zielgerichtete Erlebnisse gesendet.

* Nachdem der Besucher in den anvisierten „Bucket“ des Traffics aufgenommen wurde, kann er von Besuch zu Besuch zu einem anderen Erlebnis weitergeleitet werden, wenn die Modelle für maschinelles Lernen bestimmen, dass ein anderes Erlebnis für den neuen Besuch relevant ist.
* Nachdem ein Besucher dem Kontroll-„Bucket“ des Traffics zugewiesen wurde, sieht er immer dasselbe Erlebnis, da die Erlebniszuweisung auf einem deterministischen pseudo-zufälligen Hash der visitorId des Besuchers basiert.

+++

## Kann ich eine binomische [!DNL Analytics] mit einem Segment als Optimierungsziel in einer [!UICONTROL Auto-Allocate] verwenden? {#binomial}

+++Antwort
Sie können keine [!DNL Analytics] Metrik mit einem Segment als Optimierungsziel in einer [!UICONTROL Auto-Allocate] Aktivität verwenden. Als Problemumgehung können Sie ein benutzerspezifisches Ereignis definieren, mit dem dasselbe Ziel erreicht wird, und dieses als Optimierungszielmetrik verwenden.

+++