---
keywords: a4t;A4T;Analytics als Berichtsquelle für Target;Analytics for Target
description: Erfahren Sie, wie Sie [!UICONTROL automatische Zuordnungs] und [!UICONTROL automatisches Targeting]-Aktivitäten in erstellen [!DNL Target]  die  [!DNL Analytics]  Berichtsquelle (A4T) verwenden.
title: Unterstützt A4T [!UICONTROL automatische Zuordnung] und [!UICONTROL automatisches Targeting]-Aktivitäten?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
TQID: https://experienceleague.adobe.com/VVbjMp7jYDyslZ8ubn8ntPufLK8nKGI9k3ZGh1DLWWs
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
subfeature_v2:
  - id: df62f171-ac37-440f-8f0f-f41a72ebdd34
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1509
ht-degree: 6%

---

# A4T-Unterstützung für [!UICONTROL automatische Zuordnung] und [!UICONTROL automatisches Targeting]-Aktivitäten

Die [!DNL Adobe Target]-zu-[!DNL Adobe Analytics]-Integration, bekannt als [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), unterstützt [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting].

Die A4T-Integration bietet folgende Möglichkeiten:

* Verwenden Sie die Multi-Armed[Bandit-Funktion „Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), um Traffic zu den erfolgreichsten Erlebnissen zu leiten.
* Verwenden Sie den Machine[Learning-Algorithmus der &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md)Automatisches Targeting“, um das beste Erlebnis für jeden Besucher auszuwählen. [!UICONTROL Automatisches Targeting] wählt das beste Erlebnis basierend auf dem Profil, dem Verhalten und dem Kontext jedes Benutzers aus und verwendet dabei eine [!DNL Adobe Analytics] Zielmetrik und die umfassenden Reporting- und Analysefunktionen von [!DNL Adobe Analytics].

Stellen Sie sicher, dass Sie [A4T zur Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten implementiert haben](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den `sessionId` Wert an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} im *Adobe Target-Entwicklerhandbuch*.

Erster Schritt:

1. Klicken [&#x200B; beim Erstellen einer [!UICONTROL A/B]Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)Aktivität auf der Seite **[!UICONTROL Targeting]** auf das Steuerelement **[!UICONTROL Traffic-Zuordnung]** und wählen Sie dann im rechten Bereich die gewünschte Traffic-Zuordnungsmethode aus.

   ![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/assets/auto-target.png)

   Die folgenden Traffic-Zuordnungsmethoden sind verfügbar:

   * **[!UICONTROL Manuell (Standard)]**: Geben Sie den Prozentsatz der Teilnehmer an, die jedes Erlebnis sehen sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Automatische Zuordnung zur besten Erfahrung]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Automatische Zuordnung] - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]**: [!DNL Target] nutzt fortschrittliche Machine-Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden und anschließend Besuchern auf der Grundlage ihrer individuellen Kundenprofile und früherer Verhaltensweisen ähnlicher Besucher ein optimal auf sie zugeschnittenes Erlebnis bereitgestellt wird. Weitere Informationen finden Sie unter [Automatisches Targeting - Übersicht](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Weitere Informationen und schrittweise Anweisungen finden Sie unter [Erstellen einer automatischen Zuordnungsaktivität](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Erstellen einer automatischen Targeting-Aktivität](/help/main/c-activities/auto-target/create-auto-target.md).

1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Reporting-Source]** auf der Seite **[!UICONTROL Ziele und Einstellungen]** das Unternehmen und die Report Suite aus, die Ihrem gewünschten Optimierungsziel entsprechen.

   ![Reporting-Source-Abschnitt auf der Seite Ziele und Einstellungen](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Geben Sie den Tracking-Server und die Sandbox an.

1. Wählen Sie eine [!UICONTROL Primäre Ziel]Metrik.

   * Um [!DNL Adobe Target] zur Angabe des Optimierungsziels zu verwenden, wählen Sie **[!UICONTROL Konversion]** aus.
   * Wählen **[!UICONTROL Analytics-Metrik verwenden]** und wählen Sie dann eine Metrik aus [!DNL Analytics] als Optimierungsziel aus. Sie können eine vorkonfigurierte [!DNL Analytics]-Konversionsmetrik oder ein [!DNL Analytics] benutzerspezifisches Ereignis verwenden.

   Weitere Informationen finden [&#x200B; unter &#x200B;](#supported)Unterstützte Zielmetriken“.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Automatische Zuordnung] nutzt die ausgewählte Metrik, um die Aktivität zu optimieren und Besucher zu dem Erlebnis zu führen, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Automatisches Targeting] nutzt die von Ihnen ausgewählte Metrik, um die Aktivität zu optimieren und Besucher zu einem personalisierten Best Experience zu führen.

1. Auf der Registerkarte **[!UICONTROL Berichte]** können Sie die Berichte Ihrer Aktivität nach [!DNL Adobe Analytics] Metriken anzeigen. Klicken Sie auf **[!UICONTROL In Analytics anzeigen]**, um Ihre Berichtsdaten tiefer zu untersuchen und weiter zu segmentieren.

## Unterstützte Zielmetriken {#supported}

Mit [!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken
* [!DNL Adobe Analytics] Konversionsmetriken
* Benutzerdefinierte Ereignisse [!DNL Adobe Analytics]

>[!NOTE]
>
>Nach der Auswahl [!UICONTROL Analytics-Metrik verwenden] wählen Sie [!UICONTROL Maximieren der Konversionsrate unter Unique Visitor], um verfügbare [!DNL Adobe Analytics] Konversionsmetriken anzuzeigen, und [!UICONTROL Maximieren des Metrikwerts pro Besucher], um [!DNL Adobe Analytics] benutzerspezifische Ereignisse zu untersuchen.

[!DNL Target] können Sie Metriken auswählen, die auf binomialen Ereignissen basieren, oder Metriken, die auf kontinuierlichen Ereignissen basieren, wenn Sie [!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]-Aktivitäten verwenden.

* **Metriken basierend auf binomialen Ereignissen**: Ein binomiales Ereignis tritt entweder nicht auf oder nicht. Binomiale Ereignisse umfassen einen Klick, eine Konversion, eine Reihenfolge usw. Diese Arten von Ereignissen werden manchmal auch als Bernoulli-, binäre oder diskrete Ereignisse bezeichnet.

* **Metriken basierend auf kontinuierlichen Ereignissen**. Zu den kontinuierlichen Metriken gehören Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Seitenansichten in einer Sitzung usw. Diese Arten von Ereignissen werden manchmal auch als nicht-binomische oder nicht-Bernoulli-Metriken bezeichnet.

>[!IMPORTANT]
>
>Ab [!DNL Adobe Target Standard/Premium] Version 22.15.1 (8. und 9. März 2023) unterstützt [!DNL Target] weiterhin vorhandene Aktivitäten mit den Metriken, die jetzt nicht mehr unterstützt werden (aufgeführt in den folgenden Tabellen). Nach dem 9. September 2023 werden diese Metriken jedoch nicht mehr in vorhandenen Aktivitäten unterstützt und alle Aktivitäten, die nicht unterstützte Metriken verwenden, werden eingestellt, um die Migration vorhandener Aktivitäten auf das neue Verhalten zu erzwingen.

### Auswirkungen auf [!UICONTROL automatische Zuordnung] Aktivitäten

| Name der Metrik | Nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL averagePageDepth] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL averageTimePentOnSite] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL bouncerate] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL Bounces] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL Einträge] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL exits] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL Seitenansichten] | Kennzahlwert maximieren |
| [!UICONTROL neu laden] | Kennzahlwert maximieren |
| [!UICONTROL Besucher] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL Besuche] | Kennzahlwert maximieren |

### Auswirkungen auf [!UICONTROL Automatisches Targeting]-Aktivitäten

| Name der Metrik | Nicht mehr unterstützt in: |
| --- | --- |
| [!UICONTROL cartRemovals] | Kennzahlwert maximieren |
| [!UICONTROL Seitenansichten] | Kennzahlwert maximieren |
| [!UICONTROL Besucher] | Konversionsrate, Kennzahlenwert maximieren |
| [!UICONTROL Besuche] | Kennzahlwert maximieren |

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten sowohl für Aktivitäten [!UICONTROL Automatische Zuordnung] als auch [!UICONTROL Automatisches Targeting]. Weitere Einschränkungen und Hinweise gelten für den einen oder den anderen Aktivitätstyp.

### Automatische Zuordnung und automatisches Targeting {#both}

* Bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting] sollten Berichte immer in [!DNL Analytics] angezeigt werden.
* Die Berichtsquelle kann nach der Aktivierung einer Aktivität nicht von [!DNL Analytics] in [!DNL Target] oder umgekehrt geändert werden.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das gewünschte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerdefiniertes Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise für eine Metrik wie „Formularabschlüsse pro Besucher“ optimieren möchten, wählen Sie ein benutzerspezifisches Ereignis aus, das „Formularabschlüsse“ als primäre Zielmetrik entspricht. [!DNL Target] normalisiert Konversionsmetriken automatisch pro Besuch, um eine ungleichmäßige Traffic-Verteilung zu berücksichtigen, sodass es nicht erforderlich ist, eine berechnete Metrik zu verwenden, um eine Normalisierung durchzuführen.

### Automatische Zuordnung {#aa}

* **Trainingshäufigkeit**: [!UICONTROL Automatische Zuordnung] Modelle werden weiterhin wie gewohnt stündlich trainiert.
* **Attributionsmodelle**: [!DNL Target] verwendet das [!DNL Adobe Analytics] standardmäßige Attributionsmodell für [!UICONTROL Automatische Zuordnung]-Aktivitäten, die A4T verwenden.
* **Konfidenz**: Die von Aktivitäten mit [!UICONTROL Automatische Zuordnung] verwendete Konfidenzformel unterscheidet sich von der Formel, die standardmäßig im Bedienfeld [!DNL Adobe Analytics]&#x200B;[!UICONTROL &#x200B; A4T] angezeigt wird. [Wie hier beschrieben](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) verwendet [!UICONTROL Automatische Zuordnung] konservativere Konfidenzintervalle als reguläre [!UICONTROL A/B-Test]-Aktivitäten. Diese konservativen Konfidenzniveaus kompensieren wiederholte Auswertungen (Peeks) an den Daten. Daher zeigt der Standardbericht in [!DNL Adobe Analytics] engere Konfidenzintervalle im Vergleich zu den Intervalle an, die vom Algorithmus [!UICONTROL Automatische Zuordnung] verwendet werden. Sie können jedoch anhand der Algorithmen bestimmen, welches Erlebnis durch welche Erlebnisse begünstigt wird, an die mehr Unique Visitors gesendet werden.
* **Status des Gewinners**: Derzeit sind die Abzeichen [Noch kein Gewinner“ und &#x200B;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md)Gewinner“ im Bedienfeld [!UICONTROL A4T] in [!DNL Analysis Workspace] nicht verfügbar. Diese Abzeichen sind auch dann nicht verfügbar, wenn derselbe Bericht in [!DNL Target] angezeigt wird. Ein Gewinner-Abzeichen „Stern“, das in einem [!DNL Target] Bericht für eine Aktivität [!UICONTROL Automatische Zuordnung] mit A4T angezeigt wird, sollte ignoriert werden. Dieses Badge spiegelt reguläre Konfidenzberechnungen wider und nicht die von der [!UICONTROL automatischen Zuordnung] verwendeten Berechnungen.

### Automatisches Targeting {#at}

* [!UICONTROL Automatisches Targeting] -Modelle werden wie gewohnt alle 24 Stunden trainiert. Konversionsereignisdaten aus [!DNL Analytics] werden jedoch um weitere sechs bis 24 Stunden verzögert. Diese Verzögerung bedeutet die Verteilung des Traffics, indem die Trails die neuesten in [!DNL Analytics] aufgezeichneten Ereignisse [!DNL Target]. Diese Verzögerung hat den größten Effekt in den ersten 48 Stunden nach der Aktivierung einer Aktivität. Die Leistung der Aktivität entspricht genauer [!DNL Analytics] Konversionsverhalten nach fünf Tagen.

  Erwägen Sie die Verwendung [!UICONTROL automatischen Zuordnung] anstelle von [!UICONTROL automatischem Targeting] für kurzzeitige Aktivitäten, bei denen der meiste Traffic innerhalb der ersten fünf Tage des Lebenszyklus der Aktivität auftritt.

* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine Aktivität vom Typ [!UICONTROL Automatisches Targeting] enden Sitzungen nach Ablauf von sechs Stunden. Konversionen, die nach sechs Stunden auftreten, werden nicht gezählt.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Handbuch zu Analytics-Tools*.

## Tutorials

Obwohl in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace] umfangreiche Analysefunktionen verfügbar sind, sind einige Änderungen am Standardbedienfeld [!UICONTROL Analytics for Target] erforderlich, um die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] korrekt zu interpretieren. Diese Änderungen sind aufgrund von Unterschieden zwischen Experimentieraktivitäten (manuelle A/B- und [!UICONTROL automatische Zuordnung]) und Personalisierungsaktivitäten ([!UICONTROL automatisches Targeting]) erforderlich.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für Aktivitäten [!UICONTROL Automatische Zuordnung]

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse [!UICONTROL automatischen Zuordnungs]-Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten des Typs Automatische Zuordnung](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=de){target=_blank} in *Adobe Target-Tutorials*.

### Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für Aktivitäten [!UICONTROL Automatisches Targeting]

Dieses Tutorial führt Sie durch die empfohlenen Änderungen zur Analyse von [!UICONTROL automatischen Targeting]-Aktivitäten in [!DNL Analysis Workspace].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für automatische Targeting-Aktivitäten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de){target=_blank} in *Adobe Target-Tutorials*.


