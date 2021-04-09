---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung
description: Erfahren Sie, wie eine Aktivität der automatischen Zielgruppe in der Zielgruppe jedem Besucher auf der Grundlage seiner Profil und des Verhaltens ähnlicher Besucher die am besten angepasste Lösung bietet.
title: Was ist eine Aktivität der automatischen Zielgruppe?
feature: Automatisches Targeting
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
translation-type: tm+mt
source-git-commit: a45cfbd52df935fa3138eda6cc7f1028c13ff81d
workflow-type: tm+mt
source-wordcount: '1993'
ht-degree: 70%

---

# ![Überblick über ](/help/assets/premium.png) PREMIUMAuto-Zielgruppe

[!UICONTROL Auto-] Targeting-Aktivitäten  [!DNL Adobe Target] verwenden fortschrittliches maschinelles Lernen, um aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen auszuwählen, um Inhalte zu personalisieren und Konversionen zu fördern. Die automatische Zielgruppe bietet jedem Besucher das maßgeschneiderte Erlebnis, das auf dem individuellen Kundenverhalten und dem Verhalten früherer Besucher mit ähnlichen Profilen basiert.

>[!NOTE]
>
>[!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/c-intro/intro.md).
>
>[!UICONTROL Analytics für Zielgruppe] (A4T) unterstützt  [!UICONTROL Auto-] Targeting-Aktivitäten. Weitere Informationen finden Sie unter [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischer Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Real-world success story using Auto-Zielgruppe {#success}

Ein großer Bekleidungshändler hat kürzlich eine [!UICONTROL Auto-Zielgruppe]-Aktivität mit zehn produktbasierten Erlebnissen (plus zufälliger Kontrolle) verwendet, um den richtigen Inhalt für jeden Besucher bereitzustellen. &quot;[!UICONTROL Hinzufügen zum Warenkorb]&quot;wurde als primäre Optimierungsmetrik ausgewählt. Die angestrebten Erlebnisse stiegen im Durchschnitt um 29,09 %. Nach dem Erstellen des Modells [!UICONTROL Automatische Zielgruppe] wurde die Aktivität auf 90 % personalisierte Erlebnisse eingestellt.

In nur zehn Tagen wurden mehr als 1.700.000 Dollar an Steigerungen erzielt.

Lesen Sie weiter, um zu erfahren, wie Sie mit [!UICONTROL Auto-Zielgruppe] die Steigerung und den Umsatz Ihres Unternehmens steigern können.

## Überblick {#section_972257739A2648AFA7E7556B693079C9}

Beim [Erstellen einer A/B-Aktivität mit einem geleiteten Arbeitsablauf in drei Schritten](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) können Sie Traffic mithilfe der Option [!UICONTROL Automatisches Targeting für personalisierte Erlebnisse] zuordnen:

![Automatisches Targeting für personalisierte Erlebnisse](/help/c-activities/assets/auto-target-ui-new.png)

Mit der Option [!UICONTROL Automatisches Targeting] im A/B-Aktivitätsfluss können Sie maschinelles Lernen nutzen, damit basierend auf einer Reihe von Erlebnissen, die von Marketingexperten definiert wurden, personalisiert wird. [!UICONTROL Automatisches Targeting] soll im Vergleich zum herkömmlichen A/B-Test oder „Automatisch zuweisen“ eine maximale Optimierung bereitstellen, indem bestimmt wird, welches Erlebnis welchem Besucher angezeigt wird. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden, bestimmt [!UICONTROL Automatisches Targeting] automatisch das beste Erlebnis für einen bestimmten Besucher (basierend auf seinem Profil und anderen Kontextinformationen), um ein maximal personalisiertes Erlebnis bereitzustellen.

Ähnlich wie bei der automatisierten Personalisierung verwendet [!UICONTROL Automatisches Targeting] einen Random Forest-Algorithmus, eine führende Methode in der Datenwissenschaft, um das beste Erlebnis für einen Besucher zu ermitteln. Da sich [!UICONTROL Automatisches Targeting] an Änderungen im Besucherverhalten anpassen kann, kann es dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Dies wird manchmal auch als „Always-on“-Modus bezeichnet.

Im Gegensatz zu einer A/B-Aktivität, bei der die Erlebniszuordnung an einen bestimmten Besucher gebunden ist, optimiert [!UICONTROL Automatisches Targeting] das angegebene Geschäftsziel im Verlauf der einzelnen Besuche. Wie in [!UICONTROL Automatisierte Personalisierung] reserviert[!UICONTROL  Automatisches Targeting] standardmäßig einen Teil des Traffics der Aktivität als Kontrollgruppe zum Messen der Steigerung. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

## Zu beachten

Bei der Verwendung von [!UICONTROL Auto-Zielgruppe] sind einige wichtige Aspekte zu beachten:

* Sie können eine bestimmte Aktivität nicht von [!UICONTROL Auto-Zielgruppe] auf Automated Personalization umstellen und umgekehrt.
* Sie können nicht von manueller Traffic-Zuordnung (herkömmlicher A/B-Test) zu [!UICONTROL Auto-Zielgruppe] und umgekehrt wechseln, nachdem eine Aktivität live geschaltet wurde.
* Ein Modell wird erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic im Vergleich zum Senden des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu identifizieren. Bei diesem Modell werden Treffer und Konversionen nur in der Standard-Umgebung berücksichtigt.

   Traffic aus einem zweiten Satz von Modellen wird für jede Modellgruppe (AP) oder Erlebnis (AT) erstellt. Bei jedem dieser Modelle werden Treffer und Konversionen in allen Umgebung berücksichtigt.

   Anforderungen werden unabhängig von der Umgebung mit demselben Modell verarbeitet, aber die Traffic-Pluralität sollte aus der Standardversion stammen, um sicherzustellen, dass das identifizierte, insgesamt erfolgreichste Erlebnis mit dem realen Verhalten übereinstimmt.

* Verwenden Sie mindestens zwei Erlebnisse.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

Bei Erörterungen zu [!UICONTROL Automatisches Targeting] sind die folgenden Begriffe hilfreich:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Random Forest ist ein führender Ansatz beim maschinellen Lernen. In der Datenwissenschaft ist es eine Ensemble-Klassifizierung, oder Regressionsmethode, die funktioniert, indem viele Entscheidungsbäume basierend auf Besucher- und Besuchsattributen erstellt werden. Random Forest wird von Target eingesetzt, um zu bestimmen, welches Erlebnis die höchste Wahrscheinlichkeit einer Konversion (oder den höchsten Umsatz pro Besuch) für jeden einzelnen Besucher hat. Weitere Informationen zu Random Forest in Target finden Sie unter  [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md). |
| Thompson Sampling | Ziel des Thompson Samplings ist es, festzustellen, welches (nicht personalisierte) Erlebnis insgesamt das beste ist, während gleichzeitig die „Kosten“ für die Auffindung dieses Erlebnisses minimiert werden. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Funktionsweise von [!UICONTROL Automatisches Targeting] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Unter den folgenden Links erhalten Sie weitere Informationen über Daten und Algorithmen, die den Funktionen [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ zugrunde liegen:

| Begriff | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist der wichtigste Personalisierungsalgorithmus von Target; er wird in [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendet. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere Prognoseleistung zu erzielen, als dies bei der isolierten Verwendung dieser Lernalgorithmen möglich wäre. Der Random Forest-Algorithmus im Automated Personalization-System ist eine Klassifizierungs- oder Regressionsmethode, die durch den Bau einer Vielzahl von Entscheidungsbäumen zur Schulungszeit funktioniert. |
| [Hochladen von Daten für die Personalisierungsalgorithmen von Target](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Es gibt mehrere Möglichkeiten, um Daten für die Modelle [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ einzugeben. |
| [Datenerfassung für die Target-Personalisierungsalgorithmen](/help/c-activities/t-automated-personalization/ap-data.md) | Die Personalisierungsalgorithmen der Zielgruppe erfassen automatisch verschiedene Daten. |

## Bestimmen der Traffic-Zuordnung   {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach dem Ziel Ihrer Aktivität können Sie eine unterschiedliche Traffic-Zuordnung zwischen den Kontroll- und personalisierten Erlebnissen auswählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdownliste [!UICONTROL Zuordnung anpassen] können Sie aus den folgenden Optionen auswählen:

* Personalisierungsalgorithmus auswerten
* Personalisierungs-Datenverkehr maximieren
* Zuordnung anpassen

![Dropdown-Liste für das Zuordnungsziel](/help/c-activities/assets/split-new.png)

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **Personalisierungsalgorithmus auswerten (50/50)**: Wenn Sie den Algorithmus testen möchten, sollten Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus verwenden. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit „zufällige Erlebnisse“ als Kontrolle empfohlen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ weniger Besucher verfügen über ein personalisiertes Erlebnis</li></ul> |
| **Personalisierungs-Datenverkehr maximieren (90/10)**: Wenn Sie eine „Always on“-Aktivität erstellen möchten, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen, um sicherzustellen, dass ausreichend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiterhin lernen können. Beachten Sie hier, dass Sie im Gegenzug für die Personalisierung eines größeren Teils Ihres Traffics weniger Präzision bei der genauen Steigerung haben. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher mit einem personalisierten Erlebnis</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **Zuordnung anpassen** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

Um den Krontrollprozentsatz anzupassen, klicken Sie auf die Symbole in der Zuordnungsspalte. Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

![Traffic-Zuordnung für automatisches Targeting ändern](/help/c-activities/assets/auto-target-control.png)

Sie können [ein bestimmtes Erlebnis auswählen, das als Kontrolle verwendet werden soll](/help/c-activities/t-automated-personalization/experience-as-control.md), oder die Option „Zufälliges Erlebnis“ verwenden.

## Wann sollte [!UICONTROL Automatisches Targeting] anstelle von „Automatisierte Personalisierung“ gewählt werden? {#section_BBC4871C87944DD7A8B925811A30C633}

Es gibt verschiedene Szenarien, in denen Sie möglicherweise [!UICONTROL Automatisches Targeting][!UICONTROL  anstatt „Automatisierte Personalisierung“ verwenden möchten]:

* Wenn Sie anstelle von individuellen Angeboten, die zum Formen eines Erlebnisses automatisch kombiniert werden, das gesamte Erlebnis definieren.
* Wenn Sie den gesamten Satz von VEC-Funktionen (Visual Experience Composer) verwenden möchten, die nicht von [!UICONTROL Auto-Personalisierung] unterstützt werden: den benutzerdefinierten Code-Editor, mehrere Erlebnis-Audiencen und mehr.
* Wenn Sie strukturelle Änderungen an Ihrer Seite in unterschiedlichen Erlebnissen vornehmen möchten. Wenn Sie beispielsweise Elemente auf Ihrer Startseite neu anordnen möchten, ist [!UICONTROL Die automatische Zielgruppe] besser geeignet als Automated Personalization.

## Was hat [!UICONTROL Automatisches Targeting] mit „Automatisierte Personalisierung“ gemeinsam? {#section_2A601F482F9A44E38D4B694668711319}

**Der Algorithmus optimiert für ein erfolgreiches Resultat jedes Besuchs.**

* Der Algorithmus prognostiziert die Neigung eines Besuchers zur Konversion (oder den voraussichtlichen Erlös aus einer Konversion), um das beste Erlebnis bereitzustellen.
* Ein Besucher kann nach Abschluss einer vorhandenen Sitzung für ein neues Erlebnis genutzt werden (es sei denn, der Besucher befindet sich in der Kontrollgruppe. In diesem Fall bleibt das Erlebnis, das diesem Besucher beim ersten Besuch zugewiesen wird, bei nachfolgenden Besuchen gleich).
* Innerhalb einer Sitzung ändert sich die Prognose nicht, damit die Beständigkeit der angezeigten Darstellung nicht beeinträchtigt wird.

**Der Algorithmus passt sich an Änderungen im Besucherverhalten an.**

* Der mehrarmige Bandit stellt sicher, dass das Modell immer &quot;ausgibt&quot; einen kleinen Bruchteil Traffic, um weiterhin zu lernen während der gesamten Aktivität Lernen und zu verhindern, dass übermäßig erlernte Trends.
* Die zugrunde liegenden Modelle werden alle 24 Stunden mit den neuesten Verhaltensdaten des Besuchers neu erstellt, um sicherzustellen, dass die Zielgruppe immer die sich ändernden Voreinstellungen des Besuchers nutzt.
* Wenn der Algorithmus keine Gewinnererlebnisse für Einzelpersonen bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) gefunden.

**Der Algorithmus optimiert kontinuierlich für eine einzige Zielmetrik.**

* Diese Metrik kann auf Konversionen oder Umsätzen (genauer gesagt: Umsatz pro Besuch) basieren.

**Target sammelt automatisch Informationen über Besucher, um Personalisierungsmodelle zu erstellen.**

* Weitere Informationen zu den bei [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendeten Parametern finden Sie unter [Datenerfassung bei „Automatisierte Personalisierung“](/help/c-activities/t-automated-personalization/ap-data.md).

**Target verwendet automatisch alle von Experience Cloud gemeinsam genutzten Zielgruppen, um diese Personalisierungsmodelle zu erstellen.**

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Informationen zum Verwenden von Experience Cloud-Zielgruppen mit Target finden Sie unter  [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md)

**Marketer können für die Erstellung von Personalisierungsmodellen Offline-Daten, Propensity Scores oder andere benutzerdefinierte Daten hochladen.**

* Weitere Informationen zum [Hochladen von Daten für „Automatisches Targeting“ und „Automatisierte Personalisierung“](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Worin unterscheidet sich [!UICONTROL Automatisches Targeting] von „Automatisierte Personalisierung“? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Für die Erstellung eines personalisierten Modells ist beim automatischen Targeting] häufig weniger Traffic erforderlich als bei der automatisierten Personalisierung.**

Auch wenn die zum Erstellen der Modelle [!UICONTROL Automatisches Targeting] und [!UICONTROL Automatisierte Personalisierung] erforderliche Traffic-Menge *pro Erlebnis* identisch ist, liegen in der Regel in einer Aktivität vom Typ „Automatisierte Personalisierung“ mehr Aktivitäten vor als in einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]. Wenn Sie beispielsweise über eine Aktivität vom Typ [!UICONTROL Automatisierte Personalisierung] verfügen, in der Sie zwei Angebote pro Position mit zwei Positionen erstellen, verfügen Sie insgesamt über vier (2 = 4) in der Aktivität enthaltene Erlebnisse (ohne Ausschlüsse). Mit [!UICONTROL Automatisches Targeting] können Sie festlegen, dass Erlebnis 1 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht und dass Erlebnis 2 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht. Da Ihnen [!UICONTROL Automatisches Targeting] ermöglicht auszuwählen, dass Sie über mehrere Änderungen in einem Erlebnis verfügen möchten, können Sie die Anzahl der Gesamterlebnisse in Ihrer Aktivität reduzieren.

Für [!UICONTROL Automatisches Targeting] können einfache Faustregeln zum Nachvollziehen der Traffic-Anforderungen verwendet werden:

* **Wenn „Konversion“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 7.000 Besuche und 350 Konversionen verfügen.
* **Wenn „Umsatz pro Besuch“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 1.000 Konversionen pro Erlebnis verfügen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

**[!UICONTROL Für das automatische Targeting] ist ein kompletter Satz von Setup-Funktionen vorhanden.**

* Da [!UICONTROL Automatisches Targeting] im Arbeitsablauf einer A/B-Aktivität eingebettet wird, profitiert [!UICONTROL Automatisches Targeting] vom ausgereiften und bewährten Visual Experience Composer (VEC). [QS-Links](/help/c-activities/c-activity-qa/activity-qa.md) können ebenfalls mit [!UICONTROL Automatisches Targeting] genutzt werden.

**[!UICONTROL Für automatisches Targeting] gibt es ein umfangreiches Framework für Online-Tests.**

* Der „mehrarmige Bandit“ ist Bestandteil eines größeren Online-Test-Frameworks, das es unseren Datenwissenschaftlern und Forschern erlaubt, die Resultate ihrer kontinuierlichen Verbesserungen unter Praxisbedingungen zu untersuchen.
* Künftig ermöglicht uns diese Testumgebung, unseren datenaffinen Kunden unsere maschinelle Lernplattform bereitzustellen, damit diese ihre eigenen Modelle einbringen und so die in Target vorhandenen Modelle noch ergänzen können.

## Berichterstellung und [!UICONTROL Automatisches Targeting] {#section_42EE7F5E65E84F89A872FE9921917F76}

Weitere Informationen finden Sie unter [Zusammenfassender Bericht zu „Automatisches Targeting“](/help/c-reports/auto-target-summary-report.md) im Abschnitt [Berichte](/help/c-reports/reports.md).

## Schulungsvideo: Die Aktivitäten für die automatische Zielgruppe ![Kennzeichen ](/help/assets/overview.png)

In diesem Video wird die Einrichtung einer A/B-Aktivität für [!UICONTROL Automatisches Targeting] beschrieben.

Nach Abschluss dieser Schulung sollten Sie zu Folgendem in der Lage sein:

* Definieren von Tests zu [!UICONTROL Automatisches Targeting]
* Vergleichen und Kontrahieren von [!UICONTROL Automatisches Targeting] mit „Automatisierte Personalisierung“
* Erstellen von Aktivitäten für [!UICONTROL Automatisches Targeting]

>[!VIDEO](https://video.tv.adobe.com/v/18558)
