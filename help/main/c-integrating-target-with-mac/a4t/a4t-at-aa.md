---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten in [!DNL Target] , die [!DNL Analytics] als Berichtsquelle (A4T).
title: Unterstützt A4T [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: e458793e4d0110d97f3f5124cbe6e54520d3f0e9
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 3%

---

# A4T-Unterstützung für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] activities

Die [!DNL Adobe Target]-to-[!DNL Adobe Analytics] Integration, auch bekannt als [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) unterstützt [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.

Die A4T-Integration ermöglicht Ihnen Folgendes:

* Verwendung [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)Multi-Armed Bandit-Funktion von , um Traffic zu erfolgreichsten Erlebnissen zu führen.
* Verwendung [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)den maschinellen Lernalgorithmus von , um ein bestes Erlebnis für jeden Besucher auszuwählen. [!UICONTROL Automatisches Targeting] wählt bei Verwendung eines [!DNL Adobe Analytics] Zielmetrik und [!DNL Adobe Analytics]&quot; umfassende Berichterstellungs- und Analysefunktionen.

Stellen Sie sicher, dass [A4T zur Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten implementiert](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Wenn Sie `analyticsLogging = client_side`, müssen Sie auch die `sessionId` Wert zu [!DNL Analytics]. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T)](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/){target=_blank} im *Adobe Target SDKs* Handbuch.

Erster Schritt:

1. Beim Erstellen einer [!UICONTROL A/B-Test] -Aktivität auf der **[!UICONTROL Targeting]** eine der folgenden Optionen als **[!UICONTROL Traffic-Zuordnungsmethode]**:

   * [!UICONTROL Automatisch dem besten Erlebnis zuweisen]
   * [!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]

   ![Optionen für die Traffic-Zuordnungsmethoden: Manuelles, automatisches Zuweisen und automatisches Targeting](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Weitere Informationen und schrittweise Anweisungen finden Sie unter [Erstellen einer Aktivität vom Typ &quot;Automatische Zuordnung&quot;](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Erstellen einer Aktivität vom Typ Automatisches Targeting](/help/main/c-activities/auto-target/create-auto-target.md).

1. Auswählen **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichtsquelle]** auf **[!UICONTROL Ziele und Einstellungen]** und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

   ![Berichtsquelle auf der Seite &quot;Ziele und Einstellungen&quot;](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Wählen Sie eine [!UICONTROL Primäres Ziel] Metrik.

   * Verwendung [!DNL Adobe Target] Um das Optimierungsziel festzulegen, wählen Sie **[!UICONTROL Konversion]** .
   * Auswählen **[!UICONTROL Analytics-Metrik verwenden]** und wählen Sie dann eine Metrik aus [!DNL Analytics] zur Verwendung als Optimierungsziel. Sie können einen vordefinierten [!DNL Analytics] Konversionsmetrik oder [!DNL Analytics] benutzerspezifisches Ereignis.

   Siehe [Unterstützte Zielmetriken](#supported) unten finden Sie weitere Informationen.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Automatische Zuordnung] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zum Erlebnis gebracht werden, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Automatisches Targeting] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zu einem personalisierten besten Erlebnis gelangen.

1. Verwenden Sie die **[!UICONTROL Berichte]** , um die Berichterstellung Ihrer Aktivität nach Wahl anzuzeigen. [!DNL Adobe Analytics] Metriken. Klicken **[!UICONTROL In Analytics anzeigen]** , um Ihre Berichtsdaten tief einzutauchen und weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

[!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

[!DNL Target] ermöglicht die Auswahl von Metriken basierend auf binomialen Ereignissen oder Metriken basierend auf kontinuierlichen Ereignissen bei Verwendung von [!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.

* **Metriken basierend auf binomialen Ereignissen**: Ein binomiales Ereignis geschieht entweder oder nicht. Binomielle Ereignisse umfassen einen Klick, eine Konversion, eine Bestellung usw. Diese Ereignistypen werden manchmal auch als Bernoulli-, binäre oder diskrete Ereignisse bezeichnet.

* **Auf kontinuierlichen Ereignissen basierende Metriken**. Kontinuierliche Metriken umfassen Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Seitenansichten in der Sitzung usw. Diese Ereignistypen werden manchmal auch als nicht-binomielle oder nicht-Bernoulli-Metriken bezeichnet.

>[!IMPORTANT]
>
>Als [!DNL Adobe Target Standard/Premium] Version 2.15.1 (8. und 9. März 2023), [!DNL Target] unterstützt weiterhin bestehende Aktivitäten mit Metriken, die jetzt nicht mehr unterstützt werden (aufgeführt in den folgenden Tabellen). Nach dem 9. September 2023 werden diese Metriken jedoch nicht mehr in bestehenden Aktivitäten unterstützt und alle Aktivitäten, die nicht unterstützte Metriken verwenden, werden eingestellt, um die vorhandene Aktivitätsmigration zum neuen Verhalten zu erzwingen.

### Auswirkungen auf [!UICONTROL Automatische Zuordnung] activities

| Name der Metrik | Wird nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Konversionsrate, RPV |
| [!UICONTROL averagetimespentonsite] | Konversionsrate, RPV |
| [!UICONTROL bouncerate] | Konversionsrate, RPV |
| [!UICONTROL Absprünge] | Konversionsrate, RPV |
| [!UICONTROL Einträge] | Konversionsrate, RPV |
| [!UICONTROL Ausstiege] | Konversionsrate, RPV |
| [!UICONTROL pageviews] | RPV |
| [!UICONTROL Neuladungen] | RPV |
| [!UICONTROL Besucher] | Konversionsrate, RPV |
| [!UICONTROL Besuche] | RPV |

### Auswirkungen auf [!UICONTROL Automatisches Targeting] activities

| Name der Metrik | Wird nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL Cartremovals] | RPV |
| [!UICONTROL pageviews] | RPV |
| [!UICONTROL Besucher] | Konversionsrate, RPV |
| [!UICONTROL Besuche] | RPV |

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für beide [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten. Andere Einschränkungen und Hinweise gelten für den einen oder den anderen Aktivitätstyp.

### Automatische Zuordnung und automatisches Targeting {#both}

* Bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting]sollten Sie immer Berichte anzeigen in [!DNL Analytics].
* Die Berichtsquelle kann nicht geändert werden über [!DNL Analytics] nach [!DNL Target] oder umgekehrt, nachdem eine Aktivität aktiviert wurde.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das beabsichtigte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerspezifisches Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise eine Metrik optimieren möchten, z. B. &quot;Formularabschlüsse pro Besucher&quot;, wählen Sie als primäre Zielmetrik ein benutzerspezifisches Ereignis aus, das &quot;Formularabschlüsse&quot;entspricht. [!DNL Target] Normalisiert die Konversionsmetriken automatisch auf Besuchsbasis, um eine ungleichmäßige Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik zu verwenden, um eine Normalisierung durchzuführen.
* Bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting] -Aktivitäten, sollten Sie immer Berichte anzeigen in [!DNL Analytics].
* Die Berichtsquelle kann nicht geändert werden über [!DNL Analytics] nach [!DNL Target] oder umgekehrt, nachdem eine Aktivität aktiviert wurde.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das beabsichtigte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerspezifisches Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise eine Metrik optimieren möchten, z. B. &quot;Formularabschlüsse pro Besucher&quot;, wählen Sie als primäre Zielmetrik ein benutzerspezifisches Ereignis aus, das &quot;Formularabschlüsse&quot;entspricht. [!DNL Target] Normalisiert Konversionsmetriken automatisch auf Besucherbasis für [!UICONTROL Automatische Zuordnung] Aktivitäten verwenden, sodass es nicht erforderlich ist, eine berechnete Metrik zu verwenden, um eine Normalisierung durchzuführen.

### Automatische Zuordnung {#aa}

* **Häufigkeit der Schulungen**: [!UICONTROL Automatische Zuordnung] Modelle werden wie gewohnt jede Stunde trainiert.
* **Attributionsmodelle**: [!DNL Target] verwendet die [!DNL Adobe Analytics] Standardattributionsmodell für[!UICONTROL  Automatische Zuordnung] Aktivitäten, die A4T verwenden.
* **Konfidenz**: Die von [!UICONTROL Automatische Zuordnung] Aktivitäten unterscheidet sich von der Formel, die standardmäßig in [!DNL Adobe Analytics] [!UICONTROL A4T] Bereich. [Wie hier beschrieben](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Automatische Zuordnung] verwendet konservativere Konfidenzintervalle als normale [!UICONTROL A/B-Test] Aktivitäten. Diese konservativen Konfidenzniveaus kompensieren wiederholte Auswertungen (Peeks) bei Daten. Daher wird der Standardbericht in [!DNL Adobe Analytics] zeigt im Vergleich zu den von der [!UICONTROL Automatische Zuordnung] -Algorithmus. Sie können jedoch bestimmen, welches Erlebnis von den Algorithmen bevorzugt wird, basierend darauf, welches Erlebnis mehr Unique Visitors an das Erlebnis sendet.
* **Gewinnerstatus**: Derzeit wird die [Abzeichen &quot;Noch kein Gewinner&quot;und &quot;Gewinner&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) sind nicht verfügbar in der [!UICONTROL A4T] Bedienfeld in [!DNL Analysis Workspace]. Diese Abzeichen sind auch dann nicht verfügbar, wenn derselbe Bericht in [!DNL Target]. Das Zeichen &quot;Stern&quot;des Gewinners wird in einer [!DNL Target] für einen [!UICONTROL Automatische Zuordnung] -Aktivität, die A4T verwendet, sollte ignoriert werden. Dieses Zeichen spiegelt reguläre Konfidenzberechnungen wider und nicht die von [!UICONTROL Automatische Zuordnung].

### Automatisches Targeting {#at}

* [!UICONTROL Automatisches Targeting] -Modelle werden wie gewohnt alle 24 Stunden trainiert. Konversionsereignisdaten stammen jedoch von [!DNL Analytics] wird um zusätzliche sechs bis 24 Stunden verzögert. Diese Verzögerung bedeutet die Verteilung des Traffics nach [!DNL Target] verfolgt die neuesten Ereignisse, die in [!DNL Analytics]. Diese Verzögerung hat die größte Auswirkung in den ersten 48 Stunden nach der ersten Aktivierung einer Aktivität. Die Leistung der Aktivität wird stärker widergespiegelt [!DNL Analytics] Konversionsverhalten nach fünf Tagen vergangen ist.

   Erwägen Sie die Verwendung von [!UICONTROL Automatische Zuordnung] anstelle von [!UICONTROL Automatisches Targeting] für Aktivitäten mit kurzer Dauer, bei denen der größte Traffic innerhalb der ersten fünf Tage des Aktivitätslebens auftritt.

* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!UICONTROL Automatisches Targeting] -Aktivität, enden Sitzungen nach Ablauf von sechs Stunden. Konversionen, die nach sechs Stunden stattfinden, werden nicht gezählt.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Leitfaden für Analytics-Tools*.

## Tutorials

Obwohl Rich-Analytics-Funktionen in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], einige Änderungen an der Standardeinstellung [!UICONTROL Analytics for Target] -Bedienfeld zur korrekten Interpretation erforderlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten. Diese Änderungen sind aufgrund von Unterschieden zwischen den Experimentaktivitäten erforderlich (manuelles A/B und [!UICONTROL Automatische Zuordnung]) und Personalisierungsaktivitäten ([!UICONTROL Automatisches Targeting]).

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Automatische Zuordnung] activities

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse [!UICONTROL Automatische Zuordnung] Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatisierter Zuordnung](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank} in *Adobe Target Tutorials*.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Automatisches Targeting] activities

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse [!UICONTROL Automatisches Targeting] Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank} in *Adobe Target Tutorials*.


