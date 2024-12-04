---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung
description: Erfahren Sie, wie eine [!UICONTROL Auto-Target] -Aktivität jedem Besucher basierend auf Kundenprofilen und dem Verhalten ähnlicher Besucher das optimal auf ihn zugeschnittene Erlebnis bereitstellt.
title: Was ist eine [!UICONTROL Auto-Target] -Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Auto-Target
hide: true
hidefromtoc: true
exl-id: 3e55e032-3a70-4023-b705-2e489aa60277
source-git-commit: 5846e567cffda70ecd75f2975b0891f9a3f423a5
workflow-type: tm+mt
source-wordcount: '1828'
ht-degree: 18%

---

# [!UICONTROL Auto-Target] Übersicht

[!UICONTROL Auto-Target] -Aktivitäten in [!DNL Adobe Target] verwenden das erweiterte maschinelle Lernen, um aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen auszuwählen, um Inhalte zu personalisieren und Konversionen zu fördern. [!UICONTROL Auto-Target] stellt jedem Besucher basierend auf dem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen das am besten angepasste Erlebnis bereit.

>[!NOTE]
>
>* [!UICONTROL Auto-Target] ist als Teil der [!DNL Target Premium] -Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) unterstützt [!UICONTROL Auto-Target] -Aktivitäten. Weitere Informationen finden Sie unter [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Echtzeit-Erfolgsgeschichte mit Automatisches Targeting {#success}

Ein großer Bekleidungshändler verwendete kürzlich eine [!UICONTROL Auto-Target] -Aktivität mit zehn auf Produktkategorien basierenden Erlebnissen (plus zufallsbasierter Kontrolle), um jedem Besucher den richtigen Inhalt bereitzustellen. &quot;[!UICONTROL Add to Cart]&quot; wurde als primäre Optimierungsmetrik ausgewählt. Die zielgerichteten Erlebnisse stiegen im Durchschnitt um 29,09 %. Nach dem Erstellen der [!UICONTROL Auto-Target] -Modelle wurde die Aktivität auf 90 % personalisierte Erlebnisse festgelegt.

In nur zehn Tagen wurde eine Steigerung von über 1.700.000 Dollar erreicht.

Lesen Sie weiter, um zu erfahren, wie Sie mit [!UICONTROL Auto-Target] die Steigerung und den Umsatz Ihrer Organisation steigern können.

## Überblick {#section_972257739A2648AFA7E7556B693079C9}

Wählen Sie beim [ Erstellen einer A/B-Aktivität ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) mit dem geleiteten Arbeitsablauf mit drei Schritten die Option **[!UICONTROL Auto-Target for personalized experiences]** auf der Seite **[!UICONTROL Targeting]** (Schritt 2).

![Einstellungen für die Traffic-Zuordnungsmethode](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

Mit der Option [!UICONTROL Auto-Target] im A/B-Aktivitätsfluss können Sie maschinelles Lernen nutzen, um basierend auf einer Reihe von Erlebnissen, die von Marketingexperten definiert wurden, zu personalisieren. [!UICONTROL Auto-Target] soll im Vergleich zu herkömmlichen A/B-Tests oder [!UICONTROL Auto Allocate] eine maximale Optimierung liefern, indem bestimmt wird, welches Erlebnis für jeden Besucher angezeigt werden soll. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden, bestimmt [!UICONTROL Auto-Target] automatisch das beste Erlebnis für einen bestimmten Besucher. Das beste Erlebnis basiert auf dem Besucherprofil und anderen kontextbezogenen Informationen, um ein stark personalisiertes Erlebnis zu bieten.

Ähnlich wie bei [!UICONTROL Automated Personalization] verwendet [!UICONTROL Auto-Target] einen [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Methode in der Datenwissenschaft, um das beste Erlebnis zu ermitteln, das einem Besucher angezeigt werden soll. Da sich [!UICONTROL Auto-Target] an Änderungen im Besucherverhalten anpassen kann, kann es dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Diese Methode wird manchmal auch als &quot;Always-on&quot;-Modus bezeichnet.

Im Gegensatz zu einer A/B-Aktivität, bei der die Erlebniszuordnung an einen bestimmten Besucher gebunden ist, optimiert [!UICONTROL Auto-Target] das angegebene Geschäftsziel im Laufe jedes Besuchs. Wie in [!UICONTROL Auto Personalization] reserviert [!UICONTROL Auto-Target] standardmäßig einen Teil des Traffics der Aktivität als Kontrollgruppe, um die Steigerung zu messen. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

## Zu beachten

Beachten Sie bei Verwendung von [!UICONTROL Auto-Target] einige wichtige Aspekte:

* Sie können eine bestimmte Aktivität nicht von [!UICONTROL Auto-Target] auf [!UICONTROL Automated Personalization] umstellen, und umgekehrt.
* Sie können nicht von der Traffic-Zuordnung [!UICONTROL Manual] (traditionell [!UICONTROL A/B Test]) zu [!UICONTROL Auto-Target] und umgekehrt wechseln, nachdem eine Aktivität als Entwurf gespeichert wurde.
* Ein Modell wird erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic im Vergleich zum Senden des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

  Der Traffic aus einem zweiten Satz von Modellen wird für jede Modellgruppe (AP) oder jedes Erlebnis (AT) erstellt. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

  Anforderungen werden unabhängig von der Umgebung mit demselben Modell bereitgestellt. Die Vielzahl von Traffic sollte jedoch aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte Gesamterlebnis mit dem realen Verhalten übereinstimmt.

* Verwenden Sie mindestens zwei Erlebnisse.

## Terminologie   {#section_A309B7E0B258467789A5CACDC1D923F3}

Die folgenden Begriffe sind bei der Erörterung von [!UICONTROL Auto-Target] nützlich:

| Begriff | Definition |
|---|---|
| [Multi-Armed Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist ein führender Ansatz beim maschinellen Lernen. In der Datenwissenschaft ist es eine Ensemble-Classification oder Regressionsmethode, die funktioniert, indem sie viele Entscheidungsbäume basierend auf Besuchsattributen und Besuchsattributen erstellt. Innerhalb von [!DNL Target] wird Random Forest verwendet, um zu bestimmen, welches Erlebnis die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) für jeden bestimmten Besucher aufweist. |
| [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Ziel des Thompson-Samplings ist es, zu ermitteln, welches Erlebnis insgesamt das beste (nicht personalisierte) Erlebnis ist, und gleichzeitig die &quot;Kosten&quot;für die Suche nach diesem Erlebnis zu minimieren. Beim Thompson-Sampling wird immer ein Gewinner ausgewählt, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. |

## Funktionsweise von [!UICONTROL Auto-Target] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Weitere Informationen zu den den [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] zugrunde liegenden Daten und Algorithmen finden Sie unter den folgenden Links:

| Begriff | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Der wichtigste Personalisierungsalgorithmus von [!DNL Target], der sowohl in [!UICONTROL Auto-Target] als auch in [!UICONTROL Automated Personalization] verwendet wird, ist Random Forest. Ensemble-Methoden, wie Random Forest, verwenden mehrere Lernalgorithmen, um eine bessere Vorhersageleistung zu erzielen, als sie sich aus den einzelnen Lernalgorithmen ergeben könnte. Der Random Forest-Algorithmus in den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] ist eine Classification- oder Regressionsmethode, die durch die Erstellung einer Vielzahl von Entscheidungsbäumen während der Schulung arbeitet. |
| [Hochladen von Daten für die Personalization-Algorithmen von  [!DNL Target]](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Es gibt mehrere Möglichkeiten, Daten für die Modelle [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] einzugeben. |
| [Datenerfassung für die Personalization-Algorithmen von  [!DNL Target]](/help/main/c-activities/t-automated-personalization/ap-data.md) | Die Personalisierungsalgorithmen von [!DNL Target] erfassen automatisch verschiedene Daten. |

## Bestimmen der Traffic-Zuordnung  {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach dem Ziel Ihrer Aktivität können Sie eine unterschiedliche Traffic-Zuordnung zwischen den Kontroll- und personalisierten Erlebnissen auswählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdownliste [!UICONTROL Custom Allocation] können Sie aus den folgenden Optionen auswählen:

* [!UICONTROL Evaluate Personalization Algorithm (50/50)]
* [!UICONTROL Maximize Personalization Traffic (90/10)]
* [!UICONTROL Custom Allocation]

![Dropdown-Liste für das Zuordnungsziel](/help/main/c-activities/assets/split-new-ui.png)

In der folgenden Tabelle werden die drei Optionen erläutert:

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **[!UICONTROL Evaluate Personalization Algorithm (50/50)]**: Wenn Sie den Algorithmus testen möchten, verwenden Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit &quot;zufälligen Erlebnissen&quot;als Kontrolle empfohlen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ weniger Besucher verfügen über ein personalisiertes Erlebnis</li></ul> |
| **[!UICONTROL Maximize Personalization Traffic (90/10)]**: Wenn Sie eine &quot;Always on&quot;-Aktivität erstellen möchten, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen, um sicherzustellen, dass genügend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiter lernen können. Der Nachteil besteht darin, dass Sie im Austausch für die Personalisierung eines größeren Teils Ihres Traffics weniger präzise wissen, was genau die Steigerung ist. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher mit einem personalisierten Erlebnis</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **Zuordnung anpassen** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

Um den Prozentsatz von [!UICONTROL Control] anzupassen, klicken Sie im Bereich [!UICONTROL Traffic Allocation] auf [!UICONTROL Experiences] und passen Sie dann die Prozentsätze nach Bedarf an. Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

Sie können [ein bestimmtes Erlebnis auswählen, das als Kontrolle verwendet werden soll](/help/main/c-activities/t-automated-personalization/experience-as-control.md), oder die Option „Zufälliges Erlebnis“ verwenden.

## Wann sollten Sie [!UICONTROL Auto-Target] anstelle von [!UICONTROL Automated Personalization] wählen? {#section_BBC4871C87944DD7A8B925811A30C633}

Es gibt verschiedene Szenarien, in denen Sie möglicherweise [!UICONTROL Auto-Target] anstelle von [!UICONTROL Automated Personalization] verwenden möchten:

* Wenn Sie das gesamte Erlebnis und nicht einzelne Angebote definieren möchten, die automatisch zu einem Erlebnis kombiniert werden.
* Wenn Sie den vollständigen Satz von [!UICONTROL Visual Experience Composer] (VEC) Funktionen verwenden möchten, die nicht von [!UICONTROL Auto Personalization] unterstützt werden: den Editor für benutzerdefinierten Code, mehrere Erlebniszielgruppen und mehr.
* Wenn Sie strukturelle Änderungen an Ihrer Seite in unterschiedlichen Erlebnissen vornehmen möchten. Wenn Sie beispielsweise Elemente auf Ihrer Startseite neu anordnen möchten, ist [!UICONTROL Auto-Target] für die Verwendung besser geeignet als [!UICONTROL Automated Personalization].

## Was hat [!UICONTROL Auto-Target] mit [!UICONTROL Automated Personalization] gemein? {#section_2A601F482F9A44E38D4B694668711319}

### Der Algorithmus optimiert für ein positives Ergebnis bei jedem Besuch.

* Der Algorithmus prognostiziert die Neigung eines Besuchers zur Konversion (oder den geschätzten Umsatz aus Konversion), um das beste Erlebnis bereitzustellen.
* Ein Besucher kann nach Ende einer bestehenden Sitzung für ein neues Erlebnis infrage kommen (es sei denn, der Besucher ist Mitglied der Kontrollgruppe. In diesem Fall bleibt das Erlebnis, das dem Besucher beim ersten Besuch zugewiesen wird, bei nachfolgenden Besuchen gleich).
* Innerhalb einer Sitzung ändert sich die Prognose nicht, um die visuelle Konsistenz zu gewährleisten.

### Der Algorithmus passt sich an Änderungen im Besucherverhalten an.

* Der &quot;mehrarmige Bandit&quot;stellt sicher, dass das Modell immer einen kleinen Bruchteil des Traffics &quot;ausgibt&quot;, um während des gesamten Lebenszyklus des Aktivitätslernens weiter zu lernen und eine Übernutzung zuvor erlernter Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden anhand der neuesten Daten zum Besucherverhalten neu erstellt, um sicherzustellen, dass [!DNL Target] immer wechselnde Besucherpräferenzen nutzt.
* Wenn der Algorithmus keine Gewinnererlebnisse für Einzelpersonen bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) gefunden.

### Der Algorithmus optimiert kontinuierlich für eine einzige Zielmetrik.

* Diese Metrik kann auf Konversionen oder Umsätzen (genauer: [!UICONTROL Revenue per Visit]) basieren.

### [!DNL Target] erfasst automatisch Informationen über Besucher, um die Personalisierungsmodelle zu erstellen.

* Weitere Informationen zu den in [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] verwendeten Parametern finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] verwendet automatisch alle [!DNL Adobe Experience Cloud] freigegebenen Zielgruppen, um die Personalisierungsmodelle zu erstellen.

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

### Marketer können Offline-Daten, Tendenzwerte oder andere benutzerdefinierte Daten hochladen, um Personalisierungsmodelle zu erstellen.

* Erfahren Sie mehr über das Hochladen von Daten für [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).[

## Wie unterscheidet sich [!UICONTROL Auto-Target] von [!UICONTROL Automated Personalization]? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Auto-Target] benötigt häufig weniger Traffic als [!UICONTROL Automated Personalization], damit ein personalisiertes Modell erstellt werden kann.

Auch wenn die für die Erstellung der Modelle [!UICONTROL Auto-Target] oder [!UICONTROL Auto Personalization] erforderliche Traffic-Menge *pro Erlebnis* identisch ist, gibt es in der Regel mehr Erlebnisse in einer [!UICONTROL Automated Personalization] -Aktivität als in einer [!UICONTROL Auto-Target] -Aktivität.

Wenn Sie beispielsweise über eine [!UICONTROL Auto Personalization] -Aktivität verfügen, in der Sie zwei Angebote pro Position mit zwei Positionen erstellt haben, wären insgesamt vier (2 = 4) Erlebnisse in der Aktivität enthalten (ohne Ausschlüsse). Mit [!UICONTROL Auto-Target] können Sie festlegen, dass Erlebnis 1 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht und Erlebnis 2 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht. Da Sie mit [!UICONTROL Auto-Target] mehrere Änderungen innerhalb eines Erlebnisses vornehmen können, können Sie die Anzahl der Gesamterlebnisse in Ihrer Aktivität reduzieren.

Für [!UICONTROL Auto-Target] können einfache Faustregeln verwendet werden, um die Traffic-Anforderungen zu verstehen:

* **Wenn [!UICONTROL Conversion] Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag und Erlebnis, und die Aktivität muss außerdem mindestens 7.000 Besuche und 350 Konversionen aufweisen.
* **Wenn [!UICONTROL Revenue per Visit] Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag und Erlebnis, und zusätzlich muss die Aktivität mindestens 1.000 Konversionen pro Erlebnis aufweisen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

### [!UICONTROL Auto-Target] verfügt über eine vollständige Setup-Funktion.

* Da [!UICONTROL Auto-Target] in den Arbeitsablauf einer A/B-Aktivität eingebettet ist, profitiert [!UICONTROL Auto-Target] von dem ausgereifteren und bewährten [!UICONTROL Visual Experience Composer] (VEC). Sie können auch [QA-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) mit [!UICONTROL Auto-Target] verwenden.

### [!UICONTROL Auto-Target] bietet ein umfangreiches Framework für Online-Tests.

* Der &quot;mehrarmige Bandit&quot;ist Teil eines größeren Online-Test-Frameworks, das es [!DNL Adobe] Datenwissenschaftlern und Forschern ermöglicht, die Vorteile ihrer kontinuierlichen Verbesserungen unter realen Bedingungen zu verstehen.
* In Zukunft werden wir mit diesem Testbett die Plattform für maschinelles Lernen mit dem Namen [!DNL Adobe] für datenbewusste Kunden öffnen können, damit diese ihre eigenen Modelle einbringen können, um die Modelle mit dem Wert [!DNL Target] zu ergänzen.

## Berichterstellung und [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Weitere Informationen finden Sie unter [Berichterstellung und Automatisches Targeting](/help/main/c-activities/auto-target/reporting-and-auto-target.md).
