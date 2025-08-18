---
keywords: a4t;A4T;Analytics als Berichtsquelle für Target;Analytics for Target
description: Erfahren Sie, wie Sie [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten  [!DNL Target]  erstellen,  [!DNL Analytics]  als Berichtsquelle (A4T) verwenden.
title: Unterstützt A4T [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: ddced04c730519dae74e70a60bed26462825ad23
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 4%

---

# A4T-Unterstützung für [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]

Die [!DNL Adobe Target]-zu-[!DNL Adobe Analytics]-Integration mit der Bezeichnung [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) unterstützt [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target].

Die A4T-Integration bietet folgende Möglichkeiten:

* Verwenden Sie die Multi-Armed[Bandit-Funktion „Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), um Traffic zu den erfolgreichsten Erlebnissen zu leiten.
* Verwenden Sie den Machine[Learning-Algorithmus der ](/help/main/c-activities/auto-target/auto-target-to-optimize.md)Automatisches Targeting“, um das beste Erlebnis für jeden Besucher auszuwählen. [!UICONTROL Auto-Target] wählt das beste Erlebnis basierend auf dem Profil, dem Verhalten und dem Kontext jedes Benutzers aus und verwendet dabei eine [!DNL Adobe Analytics] Zielmetrik und die umfangreichen Reporting- und Analysefunktionen von [!DNL Adobe Analytics].

Stellen Sie sicher, dass Sie [A4T zur Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten implementiert haben](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den `sessionId` Wert an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} im *Adobe Target-Entwicklerhandbuch*.

Erster Schritt:

1. Klicken [ beim Erstellen einer [!UICONTROL A/B Test] Aktivität ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) der Seite **[!UICONTROL Targeting]** auf das **[!UICONTROL Traffic Allocation]** und wählen Sie dann im rechten Bereich die gewünschte Traffic-Zuordnungsmethode aus.

   ![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/assets/auto-target.png)

   Die folgenden Traffic-Zuordnungsmethoden sind verfügbar:

   * **[!UICONTROL Manual (Default)]**: Geben Sie den Prozentsatz der Eintritte an, die für jedes Erlebnis angezeigt werden sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Auto-Allocate to best experience]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Auto-Allocate] - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] nutzt fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Anschließend wird Besuchern auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher das jeweils passendste Erlebnis bereitgestellt. Weitere Informationen finden Sie unter [Automatisches Targeting - Übersicht](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Weitere Informationen und schrittweise Anweisungen finden Sie unter [Erstellen einer automatischen Zuordnungsaktivität](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Erstellen einer automatischen Targeting-Aktivität](/help/main/c-activities/auto-target/create-auto-target.md).

1. Wählen Sie auf der Seite **[!UICONTROL Adobe Analytics]** die Option **[!UICONTROL Reporting Source]** für Ihre **[!UICONTROL Goals & Settings]** und danach das Unternehmen und die Report Suite aus, die Ihrem gewünschten Optimierungsziel entsprechen.

   ![Reporting-Source-Abschnitt auf der Seite Ziele und Einstellungen](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Geben Sie den Tracking-Server und die Sandbox an.

1. Wählen Sie eine [!UICONTROL Primary Goal].

   * Um [!DNL Adobe Target] zur Angabe des Optimierungsziels zu verwenden, wählen Sie **[!UICONTROL Conversion]** aus.
   * Wählen Sie **[!UICONTROL Use an Analytics metric]** und dann eine Metrik aus [!DNL Analytics] als Optimierungsziel aus. Sie können eine vorkonfigurierte [!DNL Analytics]-Konversionsmetrik oder ein [!DNL Analytics] benutzerspezifisches Ereignis verwenden.

   Weitere Informationen finden [ unter ](#supported)Unterstützte Zielmetriken“.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Auto-Allocate] verwendet die ausgewählte Metrik, um die Aktivität zu optimieren, wodurch Besucher zu dem Erlebnis gelangen, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Auto-Target] verwendet die von Ihnen ausgewählte Metrik, um die Aktivität zu optimieren und Besucher zu einem personalisierten Best Experience zu führen.

1. Auf der Registerkarte **[!UICONTROL Reports]** können Sie die Berichte Ihrer Aktivität nach Auswahl der [!DNL Adobe Analytics] Metriken anzeigen. Klicken Sie auf **[!UICONTROL View in Analytics]** , um tief in Ihre Berichtsdaten einzutauchen und sie weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

[!UICONTROL A4T] für [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken
* [!DNL Adobe Analytics] Konversionsmetriken
* Benutzerdefinierte Ereignisse [!DNL Adobe Analytics]

>[!NOTE]
>
>Nach dem Auswählen von [!UICONTROL Use an Analytics Metric] wählen Sie [!UICONTROL Maximize Unique Visitor Conversion Rate] aus, um verfügbare [!DNL Adobe Analytics] Konversionsmetriken anzuzeigen, und [!UICONTROL Maximize Metric Value per Visitor], um [!DNL Adobe Analytics] benutzerspezifischen Ereignisse zu untersuchen.

[!DNL Target] können Sie Metriken auswählen, die auf binomialen Ereignissen basieren, oder Metriken, die auf kontinuierlichen Ereignissen basieren, wenn Sie [!UICONTROL A4T] für [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten verwenden.

* **Metriken basierend auf binomialen Ereignissen**: Ein binomiales Ereignis tritt entweder nicht auf oder nicht. Binomiale Ereignisse umfassen einen Klick, eine Konversion, eine Reihenfolge usw. Diese Arten von Ereignissen werden manchmal auch als Bernoulli-, binäre oder diskrete Ereignisse bezeichnet.

* **Metriken basierend auf kontinuierlichen Ereignissen**. Zu den kontinuierlichen Metriken gehören Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Seitenansichten in einer Sitzung usw. Diese Arten von Ereignissen werden manchmal auch als nicht-binomische oder nicht-Bernoulli-Metriken bezeichnet.

>[!IMPORTANT]
>
>Ab [!DNL Adobe Target Standard/Premium] Version 22.15.1 (8. und 9. März 2023) unterstützt [!DNL Target] weiterhin vorhandene Aktivitäten mit den Metriken, die jetzt nicht mehr unterstützt werden (aufgeführt in den folgenden Tabellen). Nach dem 9. September 2023 werden diese Metriken jedoch nicht mehr in vorhandenen Aktivitäten unterstützt und alle Aktivitäten, die nicht unterstützte Metriken verwenden, werden eingestellt, um die Migration vorhandener Aktivitäten auf das neue Verhalten zu erzwingen.

### Auswirkungen auf [!UICONTROL Auto-Allocate] Aktivitäten

| Name der Metrik | Nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL averagetimespentonsite] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL bouncerate] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL bounces] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL entries] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL exits] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL pageviews] | Kennzahlwert maximieren |
| [!UICONTROL reloads] | Kennzahlwert maximieren |
| [!UICONTROL visitors] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL visits] | Kennzahlwert maximieren |

### Auswirkungen auf [!UICONTROL Auto-Target] Aktivitäten

| Name der Metrik | Nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL cartremovals] | Kennzahlwert maximieren |
| [!UICONTROL pageviews] | Kennzahlwert maximieren |
| [!UICONTROL visitors] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL visits] | Kennzahlwert maximieren |

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten sowohl für [!UICONTROL Auto-Allocate]- als auch für [!UICONTROL Auto-Target]. Weitere Einschränkungen und Hinweise gelten für den einen oder den anderen Aktivitätstyp.

### Automatische Zuordnung und automatisches Targeting {#both}

* Bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Auto-Allocate] oder [!UICONTROL Auto-Target] sollten Berichte immer in [!DNL Analytics] angezeigt werden.
* Die Berichtsquelle kann nach der Aktivierung einer Aktivität nicht von [!DNL Analytics] in [!DNL Target] oder umgekehrt geändert werden.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das gewünschte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerdefiniertes Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise für eine Metrik wie „Formularabschlüsse pro Besucher“ optimieren möchten, wählen Sie ein benutzerspezifisches Ereignis aus, das „Formularabschlüsse“ als primäre Zielmetrik entspricht. [!DNL Target] normalisiert Konversionsmetriken automatisch pro Besuch, um eine ungleichmäßige Traffic-Verteilung zu berücksichtigen, sodass es nicht erforderlich ist, eine berechnete Metrik zu verwenden, um eine Normalisierung durchzuführen.

### Automatische Zuordnung {#aa}

* **Trainingshäufigkeit**: [!UICONTROL Auto-Allocate] Modelle werden wie gewohnt stündlich trainiert.
* **Attributionsmodelle**: [!DNL Target] verwendet das [!DNL Adobe Analytics] standardmäßige Attributionsmodell für [!UICONTROL  Auto-Allocate] Aktivitäten, die A4T verwenden.
* **Konfidenz**: Die von [!UICONTROL Auto-Allocate] Aktivitäten verwendete Konfidenzformel unterscheidet sich von der Formel, die standardmäßig im Bedienfeld [!DNL Adobe Analytics] [!UICONTROL A4T] angezeigt wird. [Wie hier beschrieben](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) verwendet [!UICONTROL Auto-Allocate] konservativere Konfidenzintervalle als reguläre [!UICONTROL A/B Test]. Diese konservativen Konfidenzniveaus kompensieren wiederholte Auswertungen (Peeks) an den Daten. Daher zeigt der Standardbericht in [!DNL Adobe Analytics] engere Konfidenzintervalle im Vergleich zu den Intervalle an, die vom [!UICONTROL Auto-Allocate]-Algorithmus verwendet werden. Sie können jedoch anhand der Algorithmen bestimmen, welches Erlebnis durch welche Erlebnisse begünstigt wird, an die mehr Unique Visitors gesendet werden.
* **Status des Gewinners**: Derzeit sind die Abzeichen [Noch kein Gewinner“ und ](/help/main/c-activities/automated-traffic-allocation/determine-winner.md)Gewinner“ im [!UICONTROL A4T] in [!DNL Analysis Workspace] nicht verfügbar. Diese Abzeichen sind auch dann nicht verfügbar, wenn derselbe Bericht in [!DNL Target] angezeigt wird. Ein Gewinner-Abzeichen „Stern“, das in einem [!DNL Target] für eine [!UICONTROL Auto-Allocate]-Aktivität mit A4T angezeigt wird, sollte ignoriert werden. Dieses Badge spiegelt reguläre Konfidenzberechnungen wider und nicht die von [!UICONTROL Auto-Allocate] verwendeten Berechnungen.

### Automatisches Targeting {#at}

* [!UICONTROL Auto-Target] Modelle trainieren wie gewohnt alle 24 Stunden weiter. Konversionsereignisdaten aus [!DNL Analytics] werden jedoch um weitere sechs bis 24 Stunden verzögert. Diese Verzögerung bedeutet die Verteilung des Traffics, indem die Trails die neuesten in [!DNL Target] aufgezeichneten Ereignisse [!DNL Analytics]. Diese Verzögerung hat den größten Effekt in den ersten 48 Stunden nach der Aktivierung einer Aktivität. Die Leistung der Aktivität entspricht genauer [!DNL Analytics] Konversionsverhalten nach fünf Tagen.

  Erwägen Sie die Verwendung von [!UICONTROL Auto-Allocate] anstelle von [!UICONTROL Auto-Target] für kurzzeitige Aktivitäten, bei denen der meiste Traffic innerhalb der ersten fünf Tage nach dem Leben der Aktivität auftritt.

* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!UICONTROL Auto-Target]-Aktivität enden Sitzungen nach Ablauf von sechs Stunden. Konversionen, die nach sechs Stunden auftreten, werden nicht gezählt.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Handbuch zu Analytics-Tools*.

## Tutorials

Obwohl in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace] umfangreiche Analysefunktionen verfügbar sind, sind einige Änderungen am [!UICONTROL Analytics for Target] erforderlich, um [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target] korrekt zu interpretieren. Diese Änderungen sind aufgrund von Unterschieden zwischen Experimentieraktivitäten (manuelle A/B- und [!UICONTROL Auto-Allocate]) und Personalisierungsaktivitäten ([!UICONTROL Auto-Target]) erforderlich.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Auto-Allocate] Aktivitäten

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse [!UICONTROL Auto-Allocate] -Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten des Typs Automatische Zuordnung](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=de){target=_blank} in *Adobe Target-Tutorials*.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Auto-Target] Aktivitäten

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse [!UICONTROL Auto-Target] -Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für automatische Targeting-Aktivitäten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de){target=_blank} in *Adobe Target-Tutorials*.


