---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target; Analytics für Target
description: Erfahren Sie, wie Sie [!UICONTROL Auto-Allocate] - und [!UICONTROL Auto-Target] -Aktivitäten in [!DNL Target] erstellen, die  [!DNL Analytics]  als Berichtsquelle (A4T) verwenden.
title: Unterstützt A4T [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] Aktivitäten?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 99bd509988a7d1545a6a1fe59aa59f35ef0a7d11
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 1%

---

# A4T-Unterstützung für [!UICONTROL Auto-Allocate] - und [!UICONTROL Auto-Target] -Aktivitäten

Die Integration von [!DNL Adobe Target] bis [!DNL Adobe Analytics], die als [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) bezeichnet wird, unterstützt die Aktivitäten [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].

Die A4T-Integration ermöglicht Ihnen Folgendes:

* Verwenden Sie die Multi-Armed Bandit-Funktion [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) , um Traffic zu erfolgreichsten Erlebnissen zu leiten.
* Verwenden Sie den maschinellen Lernalgorithmus [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) , um das beste Erlebnis für jeden Besucher auszuwählen. [!UICONTROL Auto-Target] wählt das beste Erlebnis auf Grundlage des Profils, Verhaltens und Kontexts jedes Benutzers aus, wobei die Zielmetrik [!DNL Adobe Analytics] und die umfassenden Berichts- und Analysefunktionen von [!DNL Adobe Analytics] verwendet werden.

Stellen Sie sicher, dass Sie [A4T für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten implementiert haben](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den `sessionId` -Wert an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} im *Adobe Target-Entwicklerhandbuch*.

Erster Schritt:

1. Wählen Sie beim Erstellen von [ eine der folgenden Optionen auf der Seite **[!UICONTROL Targeting]** als **[!UICONTROL Traffic Allocation Method]** aus:[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experiences]

   ![Optionen für die Traffic-Zuordnung: Manuell, Automatische Zuordnung und Automatisches Targeting](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Weitere Informationen und schrittweise Anweisungen finden Sie unter [Erstellen einer Aktivität mit automatischer Zuordnung](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Erstellen einer Aktivität mit automatischem Targeting](/help/main/c-activities/auto-target/create-auto-target.md).

1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Reporting Source]** auf der Seite **[!UICONTROL Goals & Settings]** aus und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

   ![Abschnitt &quot;Berichterstellung für Source&quot;auf der Seite &quot;Ziele und Einstellungen&quot;](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Wählen Sie eine Metrik vom Typ [!UICONTROL Primary Goal] aus.

   * Um [!DNL Adobe Target] zum Angeben des Optimierungsziels zu verwenden, wählen Sie **[!UICONTROL Conversion]** aus.
   * Wählen Sie **[!UICONTROL Use an Analytics metric]** und dann eine Metrik aus [!DNL Analytics], die als Optimierungsziel verwendet werden soll. Sie können eine vordefinierte [!DNL Analytics] Konversionsmetrik oder ein benutzerdefiniertes [!DNL Analytics] -Ereignis verwenden.

   Weitere Informationen finden Sie unten unter [Unterstützte Zielmetriken](#supported) .

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Auto-Allocate] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität und bringt Besucher zum Erlebnis, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Auto-Target] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität und bringt Besucher zu einem personalisierten besten Erlebnis.

1. Verwenden Sie die Registerkarte **[!UICONTROL Reports]** , um die Berichterstellung Ihrer Aktivität nach Ihrer Wahl der Metriken [!DNL Adobe Analytics] anzuzeigen. Klicken Sie auf **[!UICONTROL View in Analytics]** , um Ihre Berichtsdaten tief einzutauchen und weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

Mit [!UICONTROL A4T] für [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken
* [!DNL Adobe Analytics] Konversionsmetriken
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

Mit [!DNL Target] können Sie Metriken auf der Grundlage binomialer Ereignisse oder Metriken basierend auf kontinuierlichen Ereignissen auswählen, wenn Sie [!UICONTROL A4T] für [!UICONTROL Auto-Allocate] - und [!UICONTROL Auto-Target] -Aktivitäten verwenden.

* **Metriken basierend auf binomialen Ereignissen**: Ein binomiales Ereignis tritt entweder ein oder nicht auf. Binomielle Ereignisse umfassen einen Klick, eine Konversion, eine Bestellung usw. Diese Ereignistypen werden manchmal auch als Bernoulli-, binäre oder diskrete Ereignisse bezeichnet.

* **Metriken basierend auf kontinuierlichen Ereignissen**. Kontinuierliche Metriken umfassen den Umsatz, die Anzahl der bestellten Produkte, die Sitzungsdauer, die Anzahl der Seitenansichten in der Sitzung usw. Diese Ereignistypen werden manchmal auch als nicht-binomielle oder nicht-Bernoulli-Metriken bezeichnet.

>[!IMPORTANT]
>
>Ab der Version [!DNL Adobe Target Standard/Premium] 22.15.1 (8. und 9. März 2023) unterstützt [!DNL Target] weiterhin bestehende Aktivitäten mit den Metriken, die jetzt nicht mehr unterstützt werden (aufgeführt in den folgenden Tabellen). Nach dem 9. September 2023 werden diese Metriken jedoch nicht mehr in bestehenden Aktivitäten unterstützt und alle Aktivitäten, die nicht unterstützte Metriken verwenden, werden eingestellt, um die vorhandene Aktivitätsmigration zum neuen Verhalten zu erzwingen.

### Auswirkungen auf [!UICONTROL Auto-Allocate] -Aktivitäten

| Name der Metrik | Wird nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL averagetimespentonsite] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL bouncerate] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL bounces] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL entries] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL exits] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL pageviews] | Metrikwert maximieren |
| [!UICONTROL reloads] | Metrikwert maximieren |
| [!UICONTROL visitors] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL visits] | Metrikwert maximieren |

### Auswirkungen auf [!UICONTROL Auto-Target] -Aktivitäten

| Name der Metrik | Wird nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL cartremovals] | Metrikwert maximieren |
| [!UICONTROL pageviews] | Metrikwert maximieren |
| [!UICONTROL visitors] | Konversionsrate, Metrikwert maximieren |
| [!UICONTROL visits] | Metrikwert maximieren |

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für die Aktivitäten [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] . Andere Einschränkungen und Hinweise gelten für den einen oder den anderen Aktivitätstyp.

### Automatische Zuordnung und automatisches Targeting {#both}

* Wenn Sie [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Auto-Allocate] oder [!UICONTROL Auto-Target] verwenden, sollten Sie die Berichte immer in [!DNL Analytics] anzeigen.
* Die Berichtsquelle kann nicht von [!DNL Analytics] auf [!DNL Target] oder umgekehrt geändert werden, nachdem eine Aktivität aktiviert wurde.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das beabsichtigte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerspezifisches Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise eine Metrik optimieren möchten, z. B. &quot;Formularabschlüsse pro Besucher&quot;, wählen Sie als primäre Zielmetrik ein benutzerspezifisches Ereignis aus, das &quot;Formularabschlüsse&quot;entspricht. [!DNL Target] normalisiert automatisch Konversionsmetriken pro Besuch, um eine ungleichmäßige Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik zu verwenden, um eine Normalisierung durchzuführen.

### Automatische Zuordnung {#aa}

* **Trainings-Frequenz**: [!UICONTROL Auto-Allocate] Modelle trainieren weiterhin stündlich, wie gewohnt.
* **Attributionsmodelle**: [!DNL Target] verwendet das standardmäßige Attributionsmodell [!DNL Adobe Analytics] für [!UICONTROL  Auto-Allocate] Aktivitäten, die A4T verwenden.
* **Konfidenz**: Die von [!UICONTROL Auto-Allocate] -Aktivitäten verwendete Konfidenzformel unterscheidet sich von der im Bedienfeld [!DNL Adobe Analytics] [!UICONTROL A4T] standardmäßig angezeigten Formel. [Wie hier ](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) beschrieben, verwendet [!UICONTROL Auto-Allocate] konservativere Konfidenzintervalle als normale [!UICONTROL A/B Test] -Aktivitäten. Diese konservativen Konfidenzniveaus kompensieren wiederholte Auswertungen (Peeks) bei Daten. Daher zeigt der Standardbericht in [!DNL Adobe Analytics] engere Konfidenzintervalle im Vergleich zu den vom [!UICONTROL Auto-Allocate] -Algorithmus verwendeten Intervalle an. Sie können jedoch bestimmen, welches Erlebnis von den Algorithmen bevorzugt wird, basierend darauf, welches Erlebnis mehr Unique Visitors an das Erlebnis sendet.
* **Gewinnerstatus**: Derzeit sind die Zeichen [ &quot;Noch kein Gewinner&quot;und &quot;Gewinner&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) im Bedienfeld [!UICONTROL A4T] in [!DNL Analysis Workspace] nicht verfügbar. Diese Abzeichen sind auch nicht verfügbar, wenn derselbe Bericht in [!DNL Target] angezeigt wird. Ein Zeichen für den Gewinner &quot;star&quot;, das in einem [!DNL Target] -Bericht für eine [!UICONTROL Auto-Allocate] -Aktivität mit A4T angezeigt wird, sollte ignoriert werden. Dieses Zeichen spiegelt reguläre Konfidenzberechnungen wider, nicht aber die von [!UICONTROL Auto-Allocate] verwendeten Berechnungen.

### Automatisches Targeting {#at}

* [!UICONTROL Auto-Target] -Modelle trainieren weiterhin wie gewohnt alle 24 Stunden. Konversionsereignisdaten aus [!DNL Analytics] werden jedoch um zusätzliche sechs bis 24 Stunden verzögert. Diese Verzögerung bedeutet, dass die Verteilung des Traffics nach [!DNL Target] die neuesten Ereignisse verfolgt, die in [!DNL Analytics] aufgezeichnet wurden. Diese Verzögerung hat die größte Auswirkung in den ersten 48 Stunden nach der ersten Aktivierung einer Aktivität. Die Leistung der Aktivität spiegelt das Konversionsverhalten von [!DNL Analytics] nach fünf Tagen genauer wider.

  Erwägen Sie die Verwendung von [!UICONTROL Auto-Allocate] anstelle von [!UICONTROL Auto-Target] für Aktivitäten mit kurzer Dauer, bei denen der größte Traffic innerhalb der ersten fünf Tage des Aktivitätslebens auftritt.

* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!UICONTROL Auto-Target] -Aktivität enden Sitzungen nach sechs Stunden. Konversionen, die nach sechs Stunden stattfinden, werden nicht gezählt.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Leitfaden für Analytics-Tools*.

## Tutorials

Obwohl Rich-Analyse-Funktionen in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace] verfügbar sind, sind einige Änderungen am standardmäßigen Bedienfeld [!UICONTROL Analytics for Target] erforderlich, um die Aktivitäten [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] korrekt zu interpretieren. Diese Änderungen sind aufgrund von Unterschieden zwischen Experimentierungsaktivitäten (manuelles A/B und [!UICONTROL Auto-Allocate]) und Personalisierungsaktivitäten ([!UICONTROL Auto-Target]) erforderlich.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Auto-Allocate] -Aktivitäten

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse von [!UICONTROL Auto-Allocate] -Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatisierter Zuordnung](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=de){target=_blank} in *Adobe Target-Tutorials*.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Auto-Target] -Aktivitäten

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse von [!UICONTROL Auto-Target] -Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de){target=_blank} in *Adobe Target-Tutorials*.


