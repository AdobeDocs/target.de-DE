---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie Aktivitäten mit automatischer Zuordnung und automatischem Targeting in Adobe [!DNL Target] erstellen, die Analytics als Berichtsquelle verwenden (A4T).
title: Unterstützt A4T Aktivitäten mit automatischer Zuordnung und automatischem Targeting?
feature: 'Analytics for Target (A4T) '
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 103ee22a4bf37569f8a02a91af194ebcdc79f3b4
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 3%

---

# A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten

Die Integration von [!DNL Adobe Target]-to-[!DNL Adobe Analytics], auch [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) genannt, unterstützt die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting].

Die A4T-Integration ermöglicht Ihnen Folgendes:

* Verwenden Sie die Multi-Armed Bandit-Funktion von [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), um Traffic zu erfolgreichsten Erlebnissen zu leiten.
* Verwenden Sie den maschinellen Lernalgorithmus von [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md), um ein optimales Erlebnis für jeden Besucher auszuwählen. Beim automatischen Targeting wird das beste Erlebnis basierend auf den Profilen, Verhaltensweisen und Kontexten der Benutzer ausgewählt. Dabei wird eine [!DNL Adobe Analytics]-Zielmetrik und die umfassenden Berichts- und Analysefunktionen von [!DNL Adobe Analytics] verwendet.

Stellen Sie sicher, dass Sie [A4T für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben. Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den Wert `sessionId` an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) im Handbuch *Adobe Target SDKs*.

Erster Schritt:

1. Wählen Sie beim Erstellen einer A/B-Test-Aktivität auf der Seite **[!UICONTROL Targeting]** eine der folgenden Optionen als **[!UICONTROL Traffic-Zuordnungsmethode]** aus:

   * [!UICONTROL Automatisch dem besten Erlebnis zuweisen]
   * [!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]

   ![Optionen für die Traffic-Zuordnungsmethoden: Manuelles, automatisches Zuweisen und automatisches Targeting](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Weitere Informationen und schrittweise Anweisungen finden Sie unter [Erstellen einer Aktivität mit automatischer Zuordnung](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Erstellen einer Aktivität mit automatischem Targeting](/help/c-activities/auto-target/create-auto-target.md).

1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichtsquelle]** auf der Seite **[!UICONTROL Ziele und Einstellungen]** aus und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

   ![Berichtsquelle auf der Seite &quot;Ziele und Einstellungen&quot;](/help/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Wählen Sie eine Primäre Zielmetrik aus.

   * Um [!DNL Adobe Target] zum Angeben des Optimierungsziels zu verwenden, wählen Sie **[!UICONTROL Konversion]** aus.
   * Wählen Sie **[!UICONTROL Analytics-Metrik]** verwenden und dann eine Metrik aus [!DNL Analytics] für die Verwendung als Optimierungsziel auswählen. Sie können eine vordefinierte [!DNL Analytics]-Konversionsmetrik oder ein benutzerdefiniertes [!DNL Analytics]-Ereignis verwenden.

   Weitere Informationen finden Sie unten unter [Unterstützte Zielmetriken](#supported) .

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Die automatische ] Zuordnung verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität und bringt Besucher zum Erlebnis, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Automatisches Targeting ] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität und bringt Besucher zu einem personalisierten besten Erlebnis.

1. Verwenden Sie die Registerkarte **[!UICONTROL Berichte]** , um die Berichterstellung Ihrer Aktivität nach Ihrer Wahl der Metriken [!DNL Adobe Analytics] anzuzeigen. Klicken Sie auf **[!UICONTROL In Analytics anzeigen]** , um Ihre Berichtsdaten tief einzutauchen und weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

[!UICONTROL A4] Für  [!UICONTROL automatische ] Zuordnung und  [!UICONTROL automatisches ] Targeting können Sie einen der folgenden Metriktypen als primäre Zielmetrik zur Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Allokation and  [!UICONTROL Auto-] Targeting erfordert die Auswahl einer Metrik, die auf einem binomialen Ereignis basiert. Ein binomiales Ereignis geschieht entweder oder nicht. Binomielle Ereignisse umfassen einen Klick, eine Konversion, eine Bestellung usw. Diese Ereignistypen werden manchmal auch als Bernoulli-, binäre oder diskrete Ereignisse bezeichnet.

[!UICONTROL A4] Tfür  [!UICONTROL Automatische ] Zuordnung und  [!UICONTROL Automatisches ] Targeting unterstützt keine Optimierung für kontinuierliche Metriken. Kontinuierliche Metriken umfassen Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Seitenansichten in der Sitzung usw. Diese nicht unterstützten Metriktypen werden manchmal auch als nicht binomielle oder nicht-Bernoulli-Metriken bezeichnet.

Die folgenden Metriktypen werden als primäre Zielmetriken nicht unterstützt:

* [!DNL Adobe Target] Interaktion und Umsatzmetriken
* [!DNL Adobe Analytics] Interaktion und Umsatzmetriken

   Es ist möglich, eine [!DNL Analytics] Interaktion- oder Umsatzmetrik als primäre Zielmetrik auszuwählen, da [!DNL Target] nicht alle Interaktion- und Umsatzmetriken von [!DNL Analytics] identifizieren und ausschließen kann. Wählen Sie nur binomielle Konversionsmetriken oder benutzerspezifische Ereignisse aus [!DNL Analytics].

* [!DNL Adobe Analytics] berechnete Metriken

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] . Andere Einschränkungen und Hinweise gelten für den einen oder den anderen Aktivitätstyp.

### Automatische Zuordnung und automatisches Targeting

* Wenn Sie [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting] verwenden, sollten Sie immer Berichte in [!DNL Analytics] anzeigen.
* Die Berichtsquelle kann nach der Aktivierung einer Aktivität nicht von [!DNL Analytics] auf [!DNL Target] oder umgekehrt geändert werden.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das beabsichtigte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerspezifisches Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise eine Metrik optimieren möchten, z. B. &quot;Formularabschlüsse pro Besucher&quot;, wählen Sie als primäre Zielmetrik ein benutzerspezifisches Ereignis aus, das &quot;Formularabschlüsse&quot;entspricht. [!DNL Target] Normalisiert die Konversionsmetriken automatisch auf Besuchsbasis, um eine ungleiche Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik zu verwenden, um eine Normalisierung durchzuführen.
* [!DNL Target] verwendet das Attributionsmodell &quot;Selber Kontakt&quot;in der Funktion  [!UICONTROL Automatische ] Zuordnung: Analytics for Target (A4T).

### Automatische Zuordnung

* [!UICONTROL Auto-] Allocatemodels trainieren wie gewohnt alle zwei Stunden.

### Automatisches Targeting

* [!UICONTROL Auto-] Targeting-Modelle werden wie gewohnt alle 24 Stunden trainiert. Konversionsereignisdaten von [!DNL Analytics] werden jedoch um zusätzliche sechs bis 24 Stunden verzögert. Diese Verzögerung bedeutet, dass der Traffic nach [!DNL Target] verteilt wird, um die neuesten Ereignisse zu verfolgen, die in [!DNL Analytics] aufgezeichnet wurden. Diese Verzögerung hat die größte Auswirkung in den ersten 48 Stunden nach der ersten Aktivierung einer Aktivität. Die Leistung der Aktivität spiegelt das [!DNL Analytics]-Konversionsverhalten nach fünf Tagen genauer wider. Erwägen Sie die Verwendung von [!UICONTROL Automatische Zuordnung] anstelle von [!UICONTROL Automatisches Targeting] für Aktivitäten mit kurzer Dauer, bei denen der größte Traffic innerhalb der ersten fünf Tage des Aktivitätslebens auftritt.
* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!UICONTROL automatische Zielgruppenbestimmung] -Aktivität enden Sitzungen nach sechs Stunden. Konversionen, die nach sechs Stunden stattfinden, werden nicht gezählt.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Leitfaden für Analytics-Tools*.

## Tutorial: Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting {#tutorial}

Obwohl Rich-Analytics-Funktionen in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace] verfügbar sind, sind einige Änderungen am Standardbedienfeld [!UICONTROL Analytics for Target] erforderlich, um Aktivitäten mit automatischem Targeting korrekt zu interpretieren. Diese Änderungen sind aufgrund von Unterschieden zwischen Experimentierungsaktivitäten (manuelles A/B und [!UICONTROL Automatisierte Zuordnung]) und Personalisierungsaktivitäten ([!UICONTROL Automatisches Targeting]) erforderlich.

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse von [!UICONTROL Automatisches Targeting]-Aktivitäten in [!UICONTROL Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target-Tutorials*.
