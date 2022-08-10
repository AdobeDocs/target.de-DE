---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie in Adobe Aktivitäten mit automatischer Zuordnung und automatischem Targeting erstellen. [!DNL Target] , die Analytics als Berichtsquelle verwenden (A4T).
title: Unterstützt A4T Aktivitäten mit automatischer Zuordnung und automatischem Targeting?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: e8fc28ef2497c1dfea523a769c9c817cbd74fea2
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 3%

---

# A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten

Die [!DNL Adobe Target]-to-[!DNL Adobe Analytics] Integration, auch bekannt als [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) unterstützt [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.

Die A4T-Integration ermöglicht Ihnen Folgendes:

* Verwendung [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)Multi-Armed Bandit-Funktion, um Traffic zu erfolgreichsten Erlebnissen zu führen.
* Verwendung [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)den maschinellen Lernalgorithmus, um ein bestes Erlebnis für jeden Besucher auszuwählen. Beim automatischen Targeting wird bei Verwendung eines [!DNL Adobe Analytics] Zielmetrik und [!DNL Adobe Analytics]umfassende Berichterstellungs- und Analysefunktionen.

Stellen Sie sicher, dass [A4T zur Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten implementiert](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Wenn Sie `analyticsLogging = client_side`, müssen Sie auch die `sessionId` Wert zu [!DNL Analytics]. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T)](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/){target=_blank} im *Adobe Target SDKs* Handbuch.

Erster Schritt:

1. Beim Erstellen einer A/B-Test-Aktivität wird im **[!UICONTROL Targeting]** eine der folgenden Optionen als **[!UICONTROL Traffic-Zuordnungsmethode]**:

   * [!UICONTROL Automatisch dem besten Erlebnis zuweisen]
   * [!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]

   ![Optionen für die Traffic-Zuordnungsmethoden: Manuelles, automatisches Zuweisen und automatisches Targeting](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Weitere Informationen und schrittweise Anweisungen finden Sie unter [Erstellen einer Aktivität vom Typ &quot;Automatische Zuordnung&quot;](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) und [Erstellen einer Aktivität vom Typ Automatisches Targeting](/help/main/c-activities/auto-target/create-auto-target.md).

1. Auswählen **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichtsquelle]** auf **[!UICONTROL Ziele und Einstellungen]** und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

   ![Berichtsquelle auf der Seite &quot;Ziele und Einstellungen&quot;](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Wählen Sie eine Primäre Zielmetrik aus. Im ersten Dropdown-Menü können Sie entweder ein Ziel angeben in [!DNL Adobe Target] (wird dann von [!DNL Adobe Analytics] als Metrik &quot;Aktivitätskonversionen&quot;) oder zur Verwendung einer [!DNL Analytics] Metrik als Ziel.

   * Verwendung [!DNL Adobe Target] Um das Optimierungsziel festzulegen, wählen Sie **[!UICONTROL Konversion]** und geben Sie dann die Aktion an, die Ihre Zielgruppe ausführen muss, um anzugeben, dass das Konversionsziel erreicht wurde.
   * Wenn Sie stattdessen **[!UICONTROL Analytics-Metrik verwenden]** festgelegt ist, können Sie wählen, welche Art von Optimierungskriterium verwendet werden soll.  Siehe [Unterstützte Zielmetriken und Optimierungskriterien](#supported) unten finden Sie weitere Informationen. Nach Angabe des Optimierungskriteriums können Sie dann eine kompatible Metrik aus [!DNL Analytics] zur Verwendung als Optimierungsziel. Sie können einen vordefinierten [!DNL Analytics] Konversionsmetrik oder [!DNL Analytics] benutzerspezifisches Ereignis.


1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Automatische Zuordnung] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zum Erlebnis gebracht werden, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Automatisches Targeting] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zu einem personalisierten besten Erlebnis gelangen.

1. Verwenden Sie die **[!UICONTROL Berichte]** Registerkarte , um die Berichterstellung Ihrer Aktivität anzuzeigen, und klicken Sie auf **[!UICONTROL In Analytics anzeigen]** , um Ihre Berichtsdaten in Adobe Analytics Workspace tief zu segmentieren und weiter zu segmentieren. In den folgenden Tutorials erfahren Sie, wie Sie Ihre Berichte in Workspace einrichten:
* Automatische Zuordnung: see [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatisierter Zuordnung](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*
* Automatisches Targeting: see [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.

## Unterstützte Zielmetriken und Optimierungskriterien {#supported}

[!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

Allerdings [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] -Modelle werden für **normalisiert** Versionen dieser Metriken, wobei die genaue Normalisierung vom Aktivitätstyp abhängt. Die Optionen für Optimierungskriterien für jeden Aktivitätstyp werden in der folgenden Tabelle erläutert:

| Aktivitätstyp | Metrikquelle | Optimierungskriterium | Beschreibung |
|---------------|---------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatische Zuordnung | Analytics | Maximieren der Unique Visitor-Konversionsrate | Modelle versuchen, das Erlebnis mit der höchsten Unique Visitor-Konversionsrate zu finden. Diese ist definiert als die Anzahl der Besucher, für die die Analytics-Metrik ungleich null ist, dividiert durch die Gesamtanzahl der Besucher (die dieses Erlebnis erhalten haben). Das bedeutet, dass die Metrik als binär behandelt wird - entweder 0 oder 1 für jeden Unique Visitor in der Aktivität.   Verwenden Sie diese Option, wenn Sie sich nur um den Anteil der Benutzer kümmern, die eine bestimmte Aktion ausführen, oder wenn mehrere Konversionsereignisse für einen einzelnen Benutzer nicht sinnvoll sind. |
| Automatische Zuordnung | Analytics | Metrikwert pro Besucher maximieren | Modelle versuchen, das Erlebnis mit dem höchsten Metrikwert pro Besucher zu finden, das als Gesamtwert der Metrik für alle Benutzer definiert ist, die diesem Erlebnis ausgesetzt sind, dividiert durch die Gesamtanzahl der Besucher, die dieses Erlebnis erhalten haben. Das bedeutet, dass die Metrik einen beliebigen Wert für jeden Unique Visitor in der Aktivität annehmen kann. Wenn beispielsweise ein Besucher mehrmals konvertiert, wird jede Konversion gezählt.  Verwenden Sie diese Option, wenn Sie eine kontinuierliche Metrik wie den Gesamtumsatz maximieren möchten oder wenn mehrere Konversionsereignisse für einen einzelnen Benutzer aussagekräftiger als ein Ereignis sind (z. B. wenn mehrere Bestellungen wertvoller als eins sind). |
| Automatische Zuordnung | Target | (nicht konfigurierbar) | Die Metrik wird als binär behandelt und die Unique Visitor-Konversionsrate wird maximiert. |
| Automatisches Targeting | Analytics | Maximieren der Konversionsrate einzelner Besuche | Im Gegensatz zu automatischer Zuordnung oder manuellen A/B-Tests bedeutet die personalisierte Art von automatischem Targeting, dass sich das Erlebnis, das ein Besucher sieht, bei jedem neuen Besuch ändern kann. Die entsprechende Rate ist dann eine besuchsnormalisierte Konversionsrate, die als der Anteil der Besuche definiert ist, in dem eine Metrik ungleich null aufgezeichnet wird. Dies ist die Konversionsrate, die durch automatisches Targeting optimiert wird.   Ähnlich wie bei der automatischen Zuordnung sollte diese Option ausgewählt werden, wenn Sie sich um den Anteil der Besuche kümmern, bei denen eine Konversion stattfindet, d. h. wenn mehrere Konversionsereignisse, die bei einem einzelnen Besuch auftreten, nicht wichtig sind. |
| Automatisches Targeting | Analytics | Metrikwert pro Besuch maximieren | Wenn die Metrik, für die optimiert wird, kontinuierlich ist (z. B. Umsatz) oder wenn das Vorhandensein mehrerer Konversionsereignisse in einem einzelnen Besuch aussagekräftig ist (z. B. mehrere Bestellungen), können Sie den Metrikwert pro Besuch maximieren. Die optimierte &quot;Rate&quot;ist der Gesamtwert der Metrik, dividiert durch die Anzahl der Besuche. |
| Automatisches Targeting | Target | (nicht konfigurierbar) | Die Metrik wird als binär behandelt und die Unique Visits-Konversionsrate wird maximiert. |



Beachten Sie, dass je nach Optimierungskriterium bestimmte [!DNL Adobe Analytics] -Metriken werden nicht unterstützt.

* [!DNL Adobe Analytics] berechnete Metriken werden nicht unterstützt.
* [!DNL Adobe Analytics] Metriken müssen immer segmentierbar sein. Wenn der Wert pro Besucher/Besuch optimiert wird, muss die Metrik eine positive Polarität aufweisen (d. h. positive Werte sind besser als negative).
* [!DNL Adobe Analytics] Metrik verwendet in [!DNL Auto-Target] -Aktivitäten in DataWarehouse-Exporten verfügbar sein.

## Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für beide [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten. Andere Einschränkungen und Hinweise gelten für den einen oder den anderen Aktivitätstyp.

### Automatische Zuordnung und automatisches Targeting {#both}

* Bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting]sollten Sie immer Berichte anzeigen in [!DNL Analytics].
* Die Berichtsquelle kann nicht geändert werden über [!DNL Analytics] nach [!DNL Target] oder umgekehrt, nachdem eine Aktivität aktiviert wurde.
* Obwohl berechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das beabsichtigte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerspezifisches Ereignis als primäre Zielmetrik auswählen. Wenn Sie beispielsweise eine Metrik optimieren möchten, z. B. &quot;Formularabschlüsse pro Besucher&quot;, wählen Sie als primäre Zielmetrik ein benutzerspezifisches Ereignis aus, das &quot;Formularabschlüsse&quot;entspricht. Wie unter [Unterstützte Zielmetriken und Optimierungskriterien](#supported), je nach Aktivitätstyp und Ihrem Optimierungskriterium, [!DNL Target] normalisiert automatisch Konversionsmetriken, sodass eine berechnete Metrik nicht für die Normalisierung verwendet werden muss.


### Automatische Zuordnung {#aa}

* **Häufigkeit der Schulungen**: [!UICONTROL Automatische Zuordnung] Modelle werden wie gewohnt jede Stunde trainiert.
* **Attributionsmodelle**: [!DNL Target] verwendet die [!DNL Adobe Analytics] Standardattributionsmodell für[!UICONTROL  Automatische Zuordnung] Aktivitäten, die A4T verwenden.
* **Konfidenz**: Die von [!UICONTROL Automatische Zuordnung] Aktivitäten unterscheidet sich von der Formel, die standardmäßig in [!DNL Adobe Analytics] [!UICONTROL A4T] Bereich. [Wie hier beschrieben](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Automatische Zuordnung] verwendet konservativere Konfidenzintervalle als normale [!UICONTROL A/B-Test] Aktivitäten. Diese konservativen Konfidenzniveaus kompensieren wiederholte Auswertungen (Peeks) bei Daten. Daher wird der Standardbericht in [!DNL Adobe Analytics] zeigt im Vergleich zu den von der [!UICONTROL Automatische Zuordnung] -Algorithmus. Sie können jedoch bestimmen, welches Erlebnis von den Algorithmen bevorzugt wird, basierend darauf, welches Erlebnis mehr Unique Visitors an das Erlebnis sendet.
* **Gewinnerstatus**: Derzeit wird die [Abzeichen &quot;Noch kein Gewinner&quot;und &quot;Gewinner&quot;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) sind nicht verfügbar in der [!UICONTROL A4T] Bedienfeld in [!DNL Analysis Workspace]. Diese Abzeichen sind auch dann nicht verfügbar, wenn derselbe Bericht in [!DNL Target]. Das Zeichen &quot;Stern&quot;des Gewinners wird in einer [!DNL Target] für einen [!UICONTROL Automatische Zuordnung] -Aktivität, die A4T verwendet, sollte ignoriert werden. Dieses Zeichen spiegelt reguläre Konfidenzberechnungen wider und nicht die von [!UICONTROL Automatische Zuordnung].

### Automatisches Targeting {#at}

* **Häufigkeit der Schulungen**: [!UICONTROL Automatisches Targeting] -Modelle werden wie gewohnt alle 24 Stunden trainiert. Konversionsereignisdaten stammen jedoch von [!DNL Analytics] wird um zusätzliche sechs bis 24 Stunden verzögert. Diese Verzögerung bedeutet die Verteilung des Traffics nach [!DNL Target] verfolgt die neuesten Ereignisse, die in [!DNL Analytics]. Diese Verzögerung hat die größte Auswirkung in den ersten 48 Stunden nach der ersten Aktivierung einer Aktivität. Die Leistung der Aktivität wird stärker reflektiert [!DNL Analytics] Konversionsverhalten nach fünf Tagen vergangen ist. Erwägen Sie die Verwendung von [!UICONTROL Automatische Zuordnung] anstelle von [!UICONTROL Automatisches Targeting] für Aktivitäten mit kurzer Dauer, bei denen der größte Traffic innerhalb der ersten fünf Tage des Aktivitätslebens auftritt.
* Bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!UICONTROL Automatisches Targeting] -Aktivität, enden Sitzungen nach Ablauf von sechs Stunden. Konversionen, die nach sechs Stunden stattfinden, werden nicht gezählt.

Weitere Informationen finden Sie unter [Attributionsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Leitfaden für Analytics-Tools*.

## Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting und automatisierter Zuordnung {#tutorial}

Obwohl Rich-Analytics-Funktionen in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], einige Änderungen an der Standardeinstellung [!UICONTROL Analytics for Target] -Bedienfeld erforderlich sind, um Aktivitäten mit automatischer Zuordnung und automatischem Targeting korrekt zu interpretieren.

Diese Änderungen sind aufgrund der unter [Unterstützte Zielmetriken und Optimierungskriterien](#supported)sowie die Unterschiede zwischen den Experimentaktivitäten (manuelles A/B und [!UICONTROL Automatische Zuordnung]) und Personalisierungsaktivitäten ([!UICONTROL Automatisches Targeting]).

Diese Tutorials führen Sie durch die empfohlenen Änderungen zur Analyse [!UICONTROL A4T] [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten in [!UICONTROL Arbeitsbereich].

Weitere Informationen finden Sie unter  
* [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatisierter Zuordnung](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
* [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
