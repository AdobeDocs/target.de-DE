---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie Aktivitäten für die automatische Zuordnung und automatische Zielgruppe in Adobe [!DNL Target] erstellen, die Analytics als Berichte-Quelle (A4T) verwenden.
title: Unterstützt A4T Aktivitäten mit automatisierter Zuordnung und automatischer Zielgruppe?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 2%

---

# A4T-Unterstützung für Aktivitäten zur automatischen Zuordnung und automatischen Zielgruppe

Die [!DNL Adobe Target]-to-[!DNL Adobe Analytics]-Integration, auch als [Analytics for Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) bezeichnet, unterstützt [!UICONTROL Aktivitäten mit automatischer Zuordnung] und [!UICONTROL Auto-Zielgruppe].

Die A4T-Integration ermöglicht Ihnen Folgendes:

* Verwenden Sie die Multi-Armed Bandit-Funktion von [Automatisierte Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), um Traffic zu erfolgreichsten Erlebnissen zu verhelfen.
* Verwenden Sie den Ensemble-Computer-Lernalgorithmus von [Auto-Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md), um ein optimales Erlebnis für jeden Besucher auszuwählen. Die automatische Zielgruppe wählt das beste Erlebnis basierend auf den Profilen, dem Verhalten und dem Kontext des Benutzers aus, während eine [!DNL Adobe Analytics]-Zielmetrik und [!DNL Adobe Analytics]’ Rich-Berichte- und Analyse-Funktionen verwendet werden.

Vergewissern Sie sich, dass Sie [A4T für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben. Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den Wert `sessionId` an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T) Berichte](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) im Handbuch *Adobe Target SDKs*.

Erster Schritt:

1. Wählen Sie beim Erstellen einer A/B-Test-Aktivität auf der Seite **[!UICONTROL Targeting]** eine der folgenden Optionen als **[!UICONTROL Traffic-Zuordnungsmethode]**:

   * [!UICONTROL Automatische Zuordnung zum besten Erlebnis]
   * [!UICONTROL Automatische Zielgruppe für personalisierte Erlebnisse]

   ![Optionen für Traffic-Zuordnungsmethoden: Manuelle, automatische Zuordnung und automatische Zielgruppe](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Weitere Informationen und schrittweise Anleitungen finden Sie unter [Eine Aktivität für die automatische Zuordnung erstellen](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Eine Aktivität für die automatische Zielgruppe erstellen](/help/c-activities/auto-target/create-auto-target.md).

1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichte-Quelle]** auf der Seite **[!UICONTROL Ziele und Einstellungen]** und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

   ![Berichte-Quelle auf der Seite &quot;Ziele und Einstellungen&quot;](/help/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Wählen Sie eine Metrik für das Primär-Ziel.

   * Um [!DNL Adobe Target] zum Festlegen des Optimierungsziels zu verwenden, wählen Sie **[!UICONTROL Konversion]**.
   * Wählen Sie **[!UICONTROL Verwenden Sie eine Analytics-Metrik]** und wählen Sie dann eine Metrik aus [!DNL Analytics] zur Verwendung als Optimierungsziel. Sie können eine vordefinierte [!DNL Analytics]-Konversionsmetrik oder ein benutzerdefiniertes [!DNL Analytics]-Ereignis verwenden.

   Weitere Informationen finden Sie unter [Unterstützte Zielmetriken](#supported) weiter unten.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Die automatische ] Zuordnung verwendet Ihre ausgewählte Metrik, um die Aktivität zu optimieren, wodurch Besucher zu dem Erlebnis geleitet werden, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Auto-] Targeting nutzt Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zu einem personalisierten besten Erlebnis werden.

1. Verwenden Sie die Registerkarte **[!UICONTROL Berichte]**, um den Berichte Ihrer Aktivität nach Ihrer Auswahl von [!DNL Adobe Analytics]-Metriken Ansicht. Klicken Sie auf **[!UICONTROL Ansicht in Analytics]**, um tief zu tauchen und Ihre Berichte-Daten weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targetlet Sie wählen einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targeting erfordert die Auswahl einer Metrik, die auf einem binomialen Ereignis basiert. Ein binomiales Ereignis passiert entweder oder nicht. Binomiale Ereignis beinhalten einen Klick, eine Konversion, eine Bestellung usw. Diese Ereignisse werden manchmal auch als Bernoulli-, Binär- oder diskrete Ereignis bezeichnet.

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targeting unterstützen keine Optimierung für kontinuierliche Metriken. Kontinuierliche Metriken umfassen Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Ansichten in der Sitzung usw. Diese nicht unterstützten Metriktypen werden manchmal auch als nicht-binomielle oder nicht-Bernoulli-Metriken bezeichnet.

Die folgenden Metriktypen werden nicht als primäre Zielmetriken unterstützt:

* [!DNL Adobe Target] Interaktions- und Umsatzmetriken
* [!DNL Adobe Analytics] Interaktions- und Umsatzmetriken

   Es ist möglich, eine [!DNL Analytics]-Interaktions- oder Umsatzmetrik als primäre Zielmetrik auszuwählen, da [!DNL Target] nicht alle Interaktions- und Umsatzmetriken von [!DNL Analytics] identifizieren und ausschließen kann. Wählen Sie nur binomielle Konversionsmetriken oder benutzerdefinierte Ereignis von [!DNL Analytics] aus.

* [!DNL Adobe Analytics] berechnete Metriken

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe]. Andere Einschränkungen und Hinweise gelten für die eine oder andere Aktivität.

### Automatische Zuordnung und Zielgruppe

* Die Berichte-Quelle kann nicht von [!DNL Analytics] zu [!DNL Target] oder umgekehrt geändert werden, nachdem eine Aktivität aktiviert wurde.
* Obwohl errechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das angestrebte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerdefiniertes Ereignis als primäre Zielmetrik auswählen. Wenn Sie z. B. eine Metrik wie &quot;Formularabschlüsse pro Besucher&quot;optimieren möchten, wählen Sie ein benutzerdefiniertes Ereignis, das &quot;Formularabschlüsse&quot;als primäre Zielmetrik entspricht. [!DNL Target] normalisiert Konversionsmetriken automatisch pro Besuch, um eine ungleiche Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik für die Normalisierung zu verwenden.
* [!DNL Target] verwendet das Zuordnungsmodell &quot;Gleich Touch&quot;in der Funktion  [!UICONTROL Automatische ] Zuordnung: Analytics for Zielgruppe (A4T).

### Automatische Zuordnung

* [!UICONTROL Auto-] Allocatemodels trainieren wie gewohnt alle zwei Stunden.

### Automatisches Targeting

* [!UICONTROL Auto-] Targeting-Modelle werden weiterhin alle 24 Stunden trainiert, wie üblich. Konversionsdaten von [!DNL Analytics] werden jedoch um weitere sechs bis 24 Ereignis verzögert. Diese Verzögerung bedeutet, dass die Verteilung des Traffics durch [!DNL Target] die neuesten Ereignis verfolgt, die in [!DNL Analytics] aufgezeichnet wurden. Diese Verzögerung hat die größte Wirkung in den ersten 48 Stunden nach der ersten Aktivierung einer Aktivität. Die Performance der Aktivität spiegelt das Umrechnungsverhalten nach Ablauf von fünf Tagen stärker wider. [!DNL Analytics] Erwägen Sie die Verwendung von [!UICONTROL Automatisierte Zuordnung] anstelle von [!UICONTROL Automatische Zielgruppe] für Aktivitäten mit kurzer Dauer, in denen der meisten Traffic innerhalb der ersten fünf Lebensjahre der Aktivität auftritt.
* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!UICONTROL Auto-Zielgruppe]-Aktivität enden die Sitzungen nach Ablauf von sechs Stunden. Konversionen, die nach sechs Stunden auftreten, werden nicht gezählt.

Weitere Informationen finden Sie unter [Zuordnungsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Analytics-Tools-Handbuch*.

## Übung: Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischer Zielgruppe {#tutorial}

Obwohl Rich-Analyse-Funktionen in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace] verfügbar sind, sind einige Änderungen am Standardbedienfeld [!UICONTROL Analytics für Zielgruppe] erforderlich, um Aktivitäten der automatischen Zielgruppe korrekt zu interpretieren. Diese Änderungen sind aufgrund von Unterschieden zwischen experimentellen Aktivitäten (manuelle A/B- und [!UICONTROL Automatisierte Zuordnung]) und Personalisierungs-Aktivitäten ([!UICONTROL Automatische Zielgruppe]) erforderlich.

Dieses Lernprogramm führt Sie durch die empfohlenen Änderungen zur Analyse der Aktivitäten [!UICONTROL Auto-Zielgruppe] in [!UICONTROL Workspace].

Weitere Informationen finden Sie unter [Wie Sie A4T-Berichte in Analysis Workspace für Aktivitäten mit automatischer Zielgruppe](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target-Tutorials einrichten*.
