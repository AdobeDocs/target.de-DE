---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie Aktivitäten für die automatische Zuordnung und automatische Zielgruppe in Adobe Target erstellen, die Analytics als Berichte-Quelle (A4T) verwenden.
title: Unterstützt A4T Aktivitäten mit automatisierter Zuordnung und automatischer Zielgruppe?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# A4T-Unterstützung für Aktivitäten zur automatischen Zuordnung und automatischen Zielgruppe

Die [!DNL Adobe Target]-to-[!DNL Adobe Analytics]-Integration, auch als [Analytics for Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) bezeichnet, unterstützt [!UICONTROL Aktivitäten mit automatischer Zuordnung] und [!UICONTROL Auto-Zielgruppe].

Die A4T-Integration ermöglicht Ihnen Folgendes:

* Verwenden Sie die Multi-Armed Bandit-Funktion von [Automatisierte Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), um Traffic zu erfolgreichsten Erlebnissen zu verhelfen.
* Verwenden Sie den Algorithmus zum Lernen von Ensemble-Maschinen von [Auto-Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md), um ein optimales Erlebnis für jeden Besucher basierend auf Profil, Verhalten und Kontext auszuwählen, während Sie eine [!DNL Adobe Analytics]-Zielmetrik und die [!DNL Adobe Analytics]’ Rich-Berichte- und Analyse-Funktionen verwenden.

Vergewissern Sie sich, dass Sie [A4T für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben. Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den Wert `sessionId` an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T) Berichte](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) im Handbuch *Adobe Target SDKs*.

Erster Schritt:

1. Wählen Sie beim Erstellen einer A/B-Test-Aktivität auf der Seite **[!UICONTROL Targeting]** eine der folgenden Optionen als **[!UICONTROL Traffic-Zuordnungsmethode]**:

   * [!UICONTROL Automatische Zuordnung zu bestem Erlebnis]
   * [!UICONTROL Automatische Zielgruppe für personalisierte Erlebnisse]

   ![Optionen für Traffic-Zuordnungsmethoden: Manuelle, automatische Zuordnung und automatische Zielgruppe](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Weitere Informationen und schrittweise Anleitungen finden Sie unter [Eine Aktivität für die automatische Zuordnung erstellen](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Eine Aktivität für die automatische Zielgruppe erstellen](/help/c-activities/auto-target/create-auto-target.md).

1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichte-Quelle]** auf der Seite **[!UICONTROL Ziele und Einstellungen]** und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

   ![Berichte-Quelle auf der Seite &quot;Ziele und Einstellungen&quot;](/help/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Wählen Sie eine Metrik für das Primär-Ziel.

   * Wählen Sie **[!UICONTROL Konversion]**, um [!DNL Adobe Target] zum Festlegen des Optimierungsziels zu verwenden.
   * Wählen Sie **[!UICONTROL Verwenden Sie eine Analytics-Metrik]** und wählen Sie dann eine Metrik aus [!DNL Analytics] zur Verwendung als Optimierungsziel. Sie können eine vordefinierte [!DNL Analytics]-Konversionsmetrik oder ein benutzerdefiniertes [!DNL Analytics]-Ereignis verwenden.

   Weitere Informationen finden Sie unter [Unterstützte Zielmetriken](#supported) weiter unten.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Die automatische ] Zuordnung verwendet Ihre ausgewählte Metrik, um die Aktivität zu optimieren, wodurch Besucher zu dem Erlebnis geleitet werden, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Auto-] Targeting verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zu einem personalisierten besten Erlebnis werden.

1. Verwenden Sie die Registerkarte **[!UICONTROL Berichte]**, um den Berichte Ihrer Aktivität nach Ihrer Auswahl von [!DNL Adobe Analytics]-Metriken Ansicht. Klicken Sie auf **[!UICONTROL Ansicht in Analytics]**, um tief zu tauchen und Ihre Berichte-Daten weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targetlet Sie wählen einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targeting erfordert die Auswahl einer Metrik, die auf einem binomialen Ereignis basiert, d. h. einem Ereignis, das entweder passiert oder nicht, z. B. ein Klick, eine Konversion, eine Bestellung usw. Diese Ereignisse werden manchmal auch als Bernoulli-, Binär- oder diskrete Ereignis bezeichnet.

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targeting unterstützen keine Optimierung für kontinuierliche Metriken wie Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Ansichten während der Sitzung usw. Diese nicht unterstützten Metriktypen werden manchmal auch als nicht-binomielle oder nicht-Bernoulli-Metriken bezeichnet.

Die folgenden Metriktypen werden nicht als primäre Zielmetriken unterstützt:

* [!DNL Adobe Target] Interaktions- und Umsatzmetriken
* [!DNL Adobe Analytics] Interaktions- und Umsatzmetriken

   Es ist möglicherweise möglich, eine [!DNL Analytics]-Interaktions- oder Umsatzmetrik als primäre Zielmetrik auszuwählen, da [!DNL Target] nicht alle Interaktions- und Umsatzmetriken von [!DNL Analytics] identifizieren und ausschließen kann. Gehen Sie vorsichtig vor, um nur binomielle Konversionsmetriken oder benutzerdefinierte Ereignis von [!DNL Analytics] auszuwählen.

* [!DNL Adobe Analytics] berechnete Metriken

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe]. Andere Einschränkungen und Hinweise gelten für die eine oder andere Aktivität.

### Automatische Zuordnung und Zielgruppe

* Die Quelltexte des Berichte können nicht von [!DNL Analytics] in [!DNL Target] oder umgekehrt geändert werden, nachdem eine Aktivität aktiviert wurde.
* Obwohl errechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das angestrebte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerdefiniertes Ereignis als primäre Zielmetrik auswählen. Wenn Sie z. B. eine Metrik wie &quot;Formularabschlüsse pro Besucher&quot;optimieren möchten, wählen Sie ein benutzerdefiniertes Ereignis, das &quot;Formularabschlüsse&quot;als primäre Zielmetrik entspricht. [!DNL Target] normalisiert Konversionsmetriken automatisch pro Besuch, um eine ungleiche Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik für die Normalisierung zu verwenden.
* [!DNL Target] verwendet das Zuordnungsmodell &quot;Gleich Touch&quot;in der Funktion  [!UICONTROL Automatische ] Zuordnung: Analytics for Zielgruppe (A4T).

### Automatische Zuordnung

* [!UICONTROL Auto-] Allocatemodels trainieren wie gewohnt alle zwei Stunden.

### Automatisches Targeting

* [!UICONTROL Auto-] Targeting-Modelle werden weiterhin alle 24 Stunden trainiert, wie üblich. Konversionsdaten von [!DNL Analytics] werden jedoch um weitere sechs bis 24 Ereignis verzögert. Diese Verzögerung bedeutet, dass die Verteilung des Traffics durch [!DNL Target] die neuesten Ereignis verfolgt, die in [!DNL Analytics] aufgezeichnet wurden. Dies hat die größte Wirkung in den ersten 48 Stunden nach der ersten Aktivierung einer Aktivität. Die Performance der Aktivität spiegelt das Umrechnungsverhalten nach Ablauf von fünf Tagen stärker wider. [!DNL Analytics] Sie sollten in Erwägung ziehen, [!UICONTROL Automatisierte Zuordnung] anstelle von [!UICONTROL Autom. Zielgruppe] für Aktivitäten mit kurzer Dauer zu verwenden, in denen der meisten Traffic innerhalb der ersten fünf Lebensjahre der Aktivität auftritt.
* Wenn [!DNL Analytics] als Datenquelle für eine [!UICONTROL Auto-Zielgruppe]-Aktivität verwendet wird, gelten Sitzungen als beendet, nachdem sechs Stunden abgelaufen sind. Konversionen, die nach sechs Stunden auftreten, werden nicht gezählt.

Weitere Informationen finden Sie unter [Zuordnungsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Analytics-Tools-Handbuch*.
