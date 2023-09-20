---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung
description: Erfahren Sie, wie Sie [!UICONTROL Automatisches Targeting] Aktivität in [!DNL Target] stellt jedem Besucher basierend auf Kundenprofilen und dem Verhalten ähnlicher Besucher das am besten angepasste Erlebnis bereit.
title: Was ist eine [!UICONTROL Automatisches Targeting] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 1b1b2271738d12f8da4e695900b70e280f50d8cf
workflow-type: tm+mt
source-wordcount: '1984'
ht-degree: 43%

---

# [!UICONTROL Automatisches Targeting – Überblick]

[!UICONTROL Automatisches Targeting] Aktivitäten in [!DNL Adobe Target] Verwenden Sie das erweiterte maschinelle Lernen, um aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen auszuwählen, um Inhalte zu personalisieren und Konversionen zu fördern. [!UICONTROL Automatisches Targeting] stellt jedem Besucher basierend auf dem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen das am besten angepasste Erlebnis bereit.

>[!NOTE]
>
>* [!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) unterstützt [!UICONTROL Automatisches Targeting] Aktivitäten. Weitere Informationen finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Echtzeit-Erfolgsgeschichte mit Automatisches Targeting {#success}

Ein großer Bekleidungshändler verwendete kürzlich eine [!UICONTROL Automatisches Targeting] Aktivität mit zehn kategoriebasierten Erlebnissen (plus zufallsbasierter Kontrolle), um jedem Besucher den richtigen Inhalt bereitzustellen. &quot;[!UICONTROL Zum Warenkorb hinzufügen]wurde als primäre Optimierungsmetrik ausgewählt. Die zielgerichteten Erlebnisse stiegen im Durchschnitt um 29,09 %. Nach dem Erstellen der [!UICONTROL Automatisches Targeting] -Modellen wurde die Aktivität auf 90 % personalisierte Erlebnisse festgelegt.

In nur zehn Tagen wurde eine Steigerung von über 1.700.000 Dollar erreicht.

Lesen, um zu erfahren, wie Sie [!UICONTROL Automatisches Targeting] , um die Steigerung und den Umsatz Ihrer Organisation zu steigern.

## Überblick {#section_972257739A2648AFA7E7556B693079C9}

while [Erstellen einer A/B-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) Wählen Sie mithilfe des geleiteten Arbeitsablaufs mit drei Schritten die **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]** -Option auf **[!UICONTROL Targeting]** Seite (Schritt 2).

![Automatisches Targeting für personalisierte Erlebnisse](/help/main/c-activities/assets/auto-target-ui-new.png)

Mit der Option [!UICONTROL Automatisches Targeting] im A/B-Aktivitätsfluss können Sie maschinelles Lernen nutzen, damit basierend auf einer Reihe von Erlebnissen, die von Marketingexperten definiert wurden, personalisiert wird. [!UICONTROL Automatisches Targeting] ist so konzipiert, dass im Vergleich zu herkömmlichen A/B-Tests eine maximale Optimierung erzielt wird oder [!UICONTROL Automatische Zuordnung], indem festgelegt wird, welches Erlebnis für jeden Besucher angezeigt werden soll. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden, [!UICONTROL Automatisches Targeting] bestimmt automatisch das beste Erlebnis für einen bestimmten Besucher. Das beste Erlebnis basiert auf dem Besucherprofil und anderen kontextbezogenen Informationen, um ein stark personalisiertes Erlebnis zu bieten.

Ähnlich wie [!UICONTROL Automated Personalization], [!UICONTROL Automatisches Targeting] verwendet eine [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Methode in der Datenwissenschaft, um das beste Erlebnis zu ermitteln, das einem Besucher angezeigt werden soll. weil [!UICONTROL Automatisches Targeting] kann sich an Änderungen des Besucherverhaltens anpassen und dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Diese Methode wird manchmal auch als &quot;Always-on&quot;-Modus bezeichnet.

Im Gegensatz zu einer A/B-Aktivität, bei der die Erlebniszuordnung an einen bestimmten Besucher gebunden ist, optimiert [!UICONTROL Automatisches Targeting] das angegebene Geschäftsziel im Verlauf der einzelnen Besuche. Wie in [!UICONTROL Automatisierte Personalisierung] reserviert[!UICONTROL  Automatisches Targeting] standardmäßig einen Teil des Traffics der Aktivität als Kontrollgruppe zum Messen der Steigerung. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

## Zu beachten

Bei der Verwendung von [!UICONTROL Automatisches Targeting]:

* Es ist nicht möglich, eine bestimmte Aktivität von [!UICONTROL Automatisches Targeting] nach [!UICONTROL Automated Personalization]und umgekehrt.
* Sie können nicht zwischen [!UICONTROL Manuell] Traffic-Zuordnung (traditionell) [!UICONTROL A/B-Test]) zu [!UICONTROL Automatisches Targeting]und umgekehrt, nachdem eine Aktivität als Entwurf gespeichert wurde.
* Ein Modell wird erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic im Vergleich zum Senden des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

  Der Traffic aus einem zweiten Satz von Modellen wird für jede Modellgruppe (AP) oder jedes Erlebnis (AT) erstellt. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

  Anforderungen werden unabhängig von der Umgebung mit demselben Modell bedient, aber die Mehrzahl des Traffics sollte aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte insgesamt erfolgreichste Erlebnis mit dem realen Verhalten übereinstimmt.

* Verwenden Sie mindestens zwei Erlebnisse.

## Terminologie   {#section_A309B7E0B258467789A5CACDC1D923F3}

Bei Erörterungen zu [!UICONTROL Automatisches Targeting] sind die folgenden Begriffe hilfreich:

| Begriff | Definition |
|---|---|
| [Multi-Armed Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist ein führender Ansatz beim maschinellen Lernen. In der Datenwissenschaft ist es eine Ensemble-Classification oder Regressionsmethode, die funktioniert, indem sie viele Entscheidungsbäume basierend auf Besuchsattributen und Besuchsattributen erstellt. Within [!DNL Target]wird Random Forest verwendet, um zu bestimmen, welches Erlebnis für jeden einzelnen Besucher die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) aufweisen soll. |
| [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Ziel des Thompson-Samplings ist es, zu ermitteln, welches Erlebnis insgesamt das beste (nicht personalisierte) Erlebnis ist, und gleichzeitig die &quot;Kosten&quot;für die Suche nach diesem Erlebnis zu minimieren. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. |

## Funktionsweise von [!UICONTROL Automatisches Targeting] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Unter den folgenden Links erhalten Sie weitere Informationen über Daten und Algorithmen, die den Funktionen [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ zugrunde liegen:

| Begriff | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | [!DNL Target]des wichtigsten Personalisierungsalgorithmus, der in beiden [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization] ist Random Forest. Ensemble-Methoden, wie Random Forest, verwenden mehrere Lernalgorithmen, um eine bessere Vorhersageleistung zu erzielen, als sie sich aus den einzelnen Lernalgorithmen ergeben könnte. Der Random Forest-Algorithmus im [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] -Aktivitäten sind eine Classification- oder Regressionsmethode, die zum Zeitpunkt der Schulung durch die Erstellung einer Vielzahl von Entscheidungsbäumen arbeitet. |
| [Hochladen von Daten für [!DNL Target]Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Es gibt mehrere Möglichkeiten, um Daten für die Modelle [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ einzugeben. |
| [Datenerfassung für [!DNL Target]Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/ap-data.md) | [!DNL Target]Die Personalisierungsalgorithmen von erfassen automatisch verschiedene Daten. |

## Bestimmen der Traffic-Zuordnung  {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach dem Ziel Ihrer Aktivität können Sie eine unterschiedliche Traffic-Zuordnung zwischen den Kontroll- und personalisierten Erlebnissen auswählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdownliste [!UICONTROL Zuordnung anpassen] können Sie aus den folgenden Optionen auswählen:

* [!UICONTROL Personalisierungsalgorithmus auswerten]
* [!UICONTROL Personalisierungs-Datenverkehr maximieren]
* [!UICONTROL Zuordnung anpassen]

![Dropdown-Liste für das Zuordnungsziel](/help/main/c-activities/assets/split-new.png)

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **Personalisierungsalgorithmus auswerten (50/50)**: Wenn Sie den Algorithmus testen möchten, sollten Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus verwenden. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit &quot;zufälligen Erlebnissen&quot;als Kontrolle empfohlen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ weniger Besucher verfügen über ein personalisiertes Erlebnis</li></ul> |
| **Personalisierungs-Traffic maximieren (90/10)**: Wenn Sie eine &quot;Always on&quot;-Aktivität erstellen möchten, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen, um sicherzustellen, dass ausreichend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiter lernen können. Der Nachteil besteht darin, dass Sie im Austausch für die Personalisierung eines größeren Teils Ihres Traffics weniger präzise wissen, was genau die Steigerung ist. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher mit einem personalisierten Erlebnis</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **Zuordnung anpassen** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

So passen Sie die [!UICONTROL Kontrolle] prozentualen Anteil, klicken Sie auf die Symbole im [!UICONTROL Zuordnung] Spalte. Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

![Traffic-Zuordnung für automatisches Targeting ändern](/help/main/c-activities/assets/auto-target-control.png)

Sie können [ein bestimmtes Erlebnis auswählen, das als Kontrolle verwendet werden soll](/help/main/c-activities/t-automated-personalization/experience-as-control.md), oder die Option „Zufälliges Erlebnis“ verwenden.

## Wann sollte [!UICONTROL Automatisches Targeting][!UICONTROL  anstelle von „Automatisierte Personalisierung“ gewählt werden]? {#section_BBC4871C87944DD7A8B925811A30C633}

Es gibt verschiedene Szenarien, in denen Sie [!UICONTROL Automatisches Targeting] over [!UICONTROL Automated Personalization]:

* Wenn Sie das gesamte Erlebnis und nicht einzelne Angebote definieren möchten, die automatisch zu einem Erlebnis kombiniert werden.
* Wenn Sie den vollständigen Satz von [!UICONTROL Visual Experience Composer] (VEC) Funktionen, die von nicht unterstützt werden [!UICONTROL Automatisierte Personalisierung]: der Editor für benutzerdefinierten Code, mehrere Erlebniszielgruppen und mehr.
* Wenn Sie strukturelle Änderungen an Ihrer Seite in unterschiedlichen Erlebnissen vornehmen möchten. Wenn Sie beispielsweise Elemente auf Ihrer Startseite neu anordnen möchten, [!UICONTROL Automatisches Targeting] ist besser geeignet als [!UICONTROL Automated Personalization].

## Funktion [!UICONTROL Automatisches Targeting] haben [!UICONTROL Automated Personalization]? {#section_2A601F482F9A44E38D4B694668711319}

### Der Algorithmus optimiert für ein erfolgreiches Resultat jedes Besuchs.

* Der Algorithmus prognostiziert die Neigung eines Besuchers zur Konversion (oder den geschätzten Umsatz aus Konversion), um das beste Erlebnis bereitzustellen.
* Ein Besucher kann nach Ende einer bestehenden Sitzung für ein neues Erlebnis infrage kommen (es sei denn, der Besucher ist Mitglied der Kontrollgruppe. In diesem Fall bleibt das Erlebnis, das diesem Besucher beim ersten Besuch zugewiesen wird, bei nachfolgenden Besuchen gleich).
* Innerhalb einer Sitzung ändert sich die Prognose nicht, um die visuelle Konsistenz zu gewährleisten.

### Der Algorithmus passt sich an Änderungen im Besucherverhalten an.

* Der &quot;mehrarmige Bandit&quot;stellt sicher, dass das Modell immer einen kleinen Bruchteil des Traffics &quot;ausgibt&quot;, um während des gesamten Lebenszyklus des Aktivitätslernens weiter zu lernen und eine Übernutzung zuvor erlernter Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden anhand der neuesten Daten zum Besucherverhalten neu erstellt, um sicherzustellen, dass [!DNL Target] nutzt immer wechselnde Besucherpräferenzen aus.
* Wenn der Algorithmus keine Gewinnererlebnisse für Einzelpersonen bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) gefunden.

### Der Algorithmus optimiert kontinuierlich für eine einzige Zielmetrik.

* Diese Metrik kann auf Konversionen oder Umsätzen (genauer gesagt: [!UICONTROL Umsatz pro Besuch]).

### [!DNL Target] sammelt automatisch Informationen über Besucher, um Personalisierungsmodelle zu erstellen.

* Weitere Informationen zu den bei [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendeten Parametern finden Sie unter [Datenerfassung bei „Automatisierte Personalisierung“](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] verwendet automatisch alle[!DNL Adobe Experience Cloud] von gemeinsam genutzten Zielgruppen, um diese Personalisierungsmodelle zu erstellen.

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

### Marketer können für die Erstellung von Personalisierungsmodellen Offline-Daten, Propensity Scores oder andere benutzerdefinierte Daten hochladen.

* Weitere Informationen zum [Hochladen von Daten für „Automatisches Targeting“ und „Automatisierte Personalisierung“[!UICONTROL .]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md)

## Funktionsweise [!UICONTROL Automatisches Targeting] unterscheidet sich von [!UICONTROL Automated Personalization]? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Für die Erstellung eines personalisierten Modells ist beim automatischen Targeting] häufig weniger Traffic erforderlich als bei der automatisierten Personalisierung.

Auch wenn die zum Erstellen der Modelle *Automatisches Targeting* und [!UICONTROL Automatisierte Personalisierung] erforderliche Traffic-Menge [!UICONTROL pro Erlebnis] identisch ist, liegen in der Regel in einer Aktivität vom Typ „Automatisierte Personalisierung“ mehr Aktivitäten vor als in einer Aktivität vom Typ [!UICONTROL Automatisches Targeting.]

Wenn Sie beispielsweise eine [!UICONTROL Automatisierte Personalisierung] Aktivität, in der Sie zwei Angebote pro Position mit zwei Positionen erstellt haben, wären insgesamt vier Erlebnisse (2 = 4) in der Aktivität enthalten (ohne Ausschlüsse). Mit [!UICONTROL Automatisches Targeting] können Sie festlegen, dass Erlebnis 1 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht und dass Erlebnis 2 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht. Da Ihnen [!UICONTROL Automatisches Targeting] ermöglicht auszuwählen, dass Sie über mehrere Änderungen in einem Erlebnis verfügen möchten, können Sie die Anzahl der Gesamterlebnisse in Ihrer Aktivität reduzieren.

Für [!UICONTROL Automatisches Targeting] können einfache Faustregeln zum Nachvollziehen der Traffic-Anforderungen verwendet werden:

* **Wenn „Konversion“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 7.000 Besuche und 350 Konversionen verfügen.
* **Wenn „Umsatz pro Besuch“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 1.000 Konversionen pro Erlebnis verfügen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

### [!UICONTROL Für das automatische Targeting] ist ein kompletter Satz von Setup-Funktionen vorhanden.

* weil [!UICONTROL Automatisches Targeting] in den Arbeitsablauf der A/B-Aktivität eingebettet ist, [!UICONTROL Automatisches Targeting] Vorteile der ausgereifteren und vollwertigen [!UICONTROL Visual Experience Composer] (VEC). Sie können auch [QA-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) mit [!UICONTROL Automatisches Targeting].

### [!UICONTROL Für automatisches Targeting] gibt es ein umfangreiches Framework für Online-Tests.

* Der &quot;mehrarmige Bandit&quot;ist Teil eines größeren Online-Test-Frameworks, das [!DNL Adobe] Datenwissenschaftler und Forscher, um die Vorteile ihrer kontinuierlichen Verbesserungen unter realen Bedingungen zu verstehen.
* In der Zukunft werden wir dieses Testbett öffnen können [!DNL Adobe] Plattform für maschinelles Lernen für datenbewusste Kunden, damit sie eigene Modelle einbringen können, um die [!DNL Target] Modelle.

## Berichterstellung und [!UICONTROL Automatisches Targeting] {#section_42EE7F5E65E84F89A872FE9921917F76}

Weitere Informationen finden Sie unter [Berichterstellung und automatisches Targeting](/help/main/c-activities/auto-target/reporting-and-auto-target.md).

## Schulungsvideo: Erklärungen zu Aktivitäten vom Typ „Automatisches Targeting“

In diesem Video wird die Einrichtung einer A/B-Aktivität für [!UICONTROL Automatisches Targeting] beschrieben.

Nach Abschluss dieser Schulung sollten Sie zu Folgendem in der Lage sein:

* Definieren von Tests zu [!UICONTROL Automatisches Targeting]
* Vergleichen und Kontrahieren von [!UICONTROL Automatisches Targeting][!UICONTROL  mit „Automatisierte Personalisierung“]
* Erstellen von Aktivitäten für [!UICONTROL Automatisches Targeting]

>[!VIDEO](https://video.tv.adobe.com/v/18558)
