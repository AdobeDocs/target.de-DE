---
keywords: Automatisches Targeting;Targeting;Traffic-Zuordnung;häufig gestellte Fragen;FAQ;Fehlerbehebung;Fehlerbehebung
description: Erfahren Sie, wie eine [!UICONTROL Auto-Target] jedem Besucher basierend auf Kundenprofilen und dem Verhalten ähnlicher Besucher das passendste Erlebnis bereitstellt.
title: Was ist eine [!UICONTROL Auto-Target] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '1828'
ht-degree: 18%

---

# [!UICONTROL Auto-Target]

[!UICONTROL Auto-Target] Aktivitäten in [!DNL Adobe Target] verwenden fortschrittliche Machine Learning-Algorithmen zur Auswahl eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen, um Inhalte zu personalisieren und Konversionen zu fördern. [!UICONTROL Auto-Target] stellt jedem Besucher das passendste Erlebnis bereit, basierend auf dem individuellen Kundenprofil und dem Verhalten früherer Besucher mit ähnlichen Profilen.

>[!NOTE]
>
>* [!UICONTROL Auto-Target] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) unterstützt [!UICONTROL Auto-Target]. Weitere Informationen finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Erfolgsgeschichte aus der Praxis mit automatischem Targeting {#success}

Ein großer Kleidungseinzelhändler nutzte kürzlich eine [!UICONTROL Auto-Target] -Aktivität mit zehn produktkategoriebasierten Erlebnissen (plus randomisierter Kontrolle), um jedem Besucher die richtigen Inhalte bereitzustellen. Als primäre Optimierungsmetrik wurde &quot;[!UICONTROL Add to Cart]&quot; ausgewählt. Die anvisierten Erlebnisse hatten eine durchschnittliche Steigerung von 29,09 %. Nach dem Erstellen der [!UICONTROL Auto-Target] Modelle wurde die Aktivität auf 90 % personalisierte Erlebnisse festgelegt.

In nur zehn Tagen wurden über 1.700.000 Dollar an Auftrieb erreicht.

Lesen Sie weiter, um zu erfahren, wie Sie [!UICONTROL Auto-Target] verwenden können, um den Anstieg und den Umsatz Ihrer Organisation zu steigern.

## Überblick {#section_972257739A2648AFA7E7556B693079C9}

Wählen [ beim Erstellen einer A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)Aktivität mithilfe des angeleiteten dreistufigen Workflows die Option **[!UICONTROL Auto-Target for personalized experiences]** auf der Seite **[!UICONTROL Targeting]** (Schritt 2).

![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

Mit der Option [!UICONTROL Auto-Target] im A/B-Aktivitätsfluss können Sie maschinelles Lernen nutzen, um mit einem Klick eine Personalisierung auf der Grundlage einer Reihe von vom Marketing-Experten definierten Erlebnissen vorzunehmen. [!UICONTROL Auto-Target] soll im Vergleich zu herkömmlichen A/B-Tests oder [!UICONTROL Auto Allocate] maximale Optimierung bieten, indem bestimmt wird, welches Erlebnis für jeden Besucher angezeigt werden soll. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden, bestimmt [!UICONTROL Auto-Target] automatisch das beste Erlebnis für einen bestimmten Besucher. Das beste Erlebnis basiert auf dem Besucherprofil und anderen kontextuellen Informationen, um ein hochgradig personalisiertes Erlebnis zu bieten.

Ähnlich wie [!UICONTROL Automated Personalization] verwendet [!UICONTROL Auto-Target] einen [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Datenwissenschafts-Ensemble-Methode, um das beste Erlebnis für einen Besucher zu ermitteln. Da [!UICONTROL Auto-Target] sich an Änderungen im Besucherverhalten anpassen können, kann sie dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Diese Methode wird auch als „Always-on“-Modus bezeichnet.

Im Gegensatz zu einer A/B-Aktivität, bei der die Erlebniszuordnung für einen bestimmten Besucher fixiert ist, optimiert [!UICONTROL Auto-Target] das angegebene Geschäftsziel bei jedem Besuch. Wie in [!UICONTROL Auto Personalization] reserviert [!UICONTROL Auto-Target] standardmäßig einen Teil des Traffics der Aktivität als Kontrollgruppe, um die Steigerung zu messen. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

## Zu beachten

Beachten Sie bei der Verwendung von [!UICONTROL Auto-Target] einige wichtige Aspekte:

* Sie können eine bestimmte Aktivität nicht von [!UICONTROL Auto-Target] in [!UICONTROL Automated Personalization] oder umgekehrt wechseln.
* Sie können nicht von [!UICONTROL Manual] Traffic-Zuordnung (traditionelles [!UICONTROL A/B Test]) zu [!UICONTROL Auto-Target] wechseln und umgekehrt, nachdem eine Aktivität als Entwurf gespeichert wurde.
* Es wird ein Modell erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic und dem Versand des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

  Der Traffic eines zweiten Modellsatzes wird für jede Modellierungsgruppe (AP) oder jedes Erlebnis (AT) erstellt. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

  Anfragen werden unabhängig von der Umgebung mit demselben Modell bereitgestellt. Die Pluralität des Traffics sollte jedoch aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte erfolgreichste Erlebnis mit dem Verhalten in der realen Welt übereinstimmt.

* Verwenden Sie mindestens zwei Erlebnisse.

## Terminologie   {#section_A309B7E0B258467789A5CACDC1D923F3}

Die folgenden Begriffe sind bei der Erörterung von [!UICONTROL Auto-Target] hilfreich:

| Begriff | Definition |
|---|---|
| [Mehrarmiger Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist ein führender Ansatz beim maschinellen Lernen. In der Datenwissenschaft ist dies eine Ensemble-Klassifizierung oder Regressionsmethode, die durch die Erstellung vieler Entscheidungsbäume auf der Grundlage von Besucher- und Besuchsattributen funktioniert. In [!DNL Target] wird mithilfe der Zufallsstruktur bestimmt, welches Erlebnis für jeden einzelnen Besucher die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) aufweist. |
| [Thompson-](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Das Ziel des Thompson-Stichprobenverfahrens besteht darin, festzustellen, welches Erlebnis insgesamt am besten ist (nicht personalisiert), und gleichzeitig die „Kosten“ für das Auffinden dieses Erlebnisses zu minimieren. Beim Thompson-Stichprobenverfahren wird immer ein Gewinner ausgewählt, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. |

## Funktionsweise von [!UICONTROL Auto-Target] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Weitere Informationen zu den Daten und Algorithmen, die [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] zugrunde liegen, finden Sie unter den folgenden Links:

| Begriff | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Der wichtigste Personalisierungsalgorithmus von [!DNL Target], der sowohl in [!UICONTROL Auto-Target] als auch in [!UICONTROL Automated Personalization] verwendet wird, ist „Random Forest“. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere prädiktive Leistung zu erzielen, als sie mit einem der einzelnen Lernalgorithmen erzielt werden könnte. Der Random Forest-Algorithmus in den [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target]-Aktivitäten ist eine Klassifizierungs- oder Regressionsmethode, die zum Trainingszeitpunkt eine Vielzahl von Entscheidungsbäumen konstruiert. |
| [Hochladen von Daten für  [!DNL Target] Personalization-Algorithmen von](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Es gibt mehrere Möglichkeiten, Daten für [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Modelle einzugeben. |
| [Datenerfassung für [!DNL Target]s Personalization-Algorithmen](/help/main/c-activities/t-automated-personalization/ap-data.md) | Die Personalisierungsalgorithmen von [!DNL Target] erfassen automatisch verschiedene Daten. |

## Bestimmen der Traffic-Zuordnung  {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach dem Ziel Ihrer Aktivität können Sie eine unterschiedliche Traffic-Zuordnung zwischen den Kontroll- und personalisierten Erlebnissen auswählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdown-Liste [!UICONTROL Custom Allocation] können Sie aus den folgenden Optionen auswählen:

* [!UICONTROL Evaluate Personalization Algorithm (50/50)]
* [!UICONTROL Maximize Personalization Traffic (90/10)]
* [!UICONTROL Custom Allocation]

![Dropdown-Liste für das Zuordnungsziel](/help/main/c-activities/assets/split-new-ui.png)

In der folgenden Tabelle werden die drei Optionen erläutert:

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **[!UICONTROL Evaluate Personalization Algorithm (50/50)]**: Wenn Sie den Algorithmus testen möchten, verwenden Sie eine 50/50-prozentige Aufteilung der Besucher zwischen dem Steuerelement und dem Zielalgorithmus. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Wird zur Verwendung mit „zufälligen Erlebnissen“ als Kontrolle vorgeschlagen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ weniger Besucher haben ein personalisiertes Erlebnis</li></ul> |
| **[!UICONTROL Maximize Personalization Traffic (90/10)]**: Wenn Sie eine „Always on“-Aktivität erstellen möchten, geben Sie 10 % der Besucher die Kontrolle darüber, ob genügend Daten für die Algorithmen vorhanden sind, um im Laufe der Zeit weiterlernen zu können. Der Nachteil hier ist, dass Sie im Gegenzug für die Personalisierung eines größeren Teils Ihres Traffics weniger Präzision in der genauen Steigerung haben. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher, die über ein personalisiertes Erlebnis verfügen</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **Zuordnung anpassen** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

Um den [!UICONTROL Control] anzupassen, klicken Sie im [!UICONTROL Traffic Allocation] auf [!UICONTROL Experiences] und passen Sie die Prozentsätze dann nach Bedarf an. Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

Sie können [ein bestimmtes Erlebnis auswählen, das als Kontrolle verwendet werden soll](/help/main/c-activities/t-automated-personalization/experience-as-control.md), oder die Option „Zufälliges Erlebnis“ verwenden.

## Wann sollte man [!UICONTROL Auto-Target] vor [!UICONTROL Automated Personalization] wählen? {#section_BBC4871C87944DD7A8B925811A30C633}

Es gibt mehrere Szenarien, in denen Sie [!UICONTROL Auto-Target] anstelle von [!UICONTROL Automated Personalization] verwenden können:

* Wenn Sie das gesamte Erlebnis definieren möchten, anstatt einzelne Angebote, die automatisch zu einem Erlebnis kombiniert werden.
* Wenn Sie alle Funktionen von [!UICONTROL Visual Experience Composer] (VEC) verwenden möchten, die von [!UICONTROL Auto Personalization] nicht unterstützt werden: den Editor für benutzerdefinierten Code, mehrere Erlebnis-Zielgruppen und mehr.
* Wenn Sie strukturelle Änderungen an Ihrer Seite in unterschiedlichen Erlebnissen vornehmen möchten. Wenn Sie beispielsweise Elemente auf Ihrer Startseite neu anordnen möchten, ist [!UICONTROL Auto-Target] besser geeignet als [!UICONTROL Automated Personalization].

## Was hat [!UICONTROL Auto-Target] mit [!UICONTROL Automated Personalization] gemeinsam? {#section_2A601F482F9A44E38D4B694668711319}

### Der Algorithmus wird für jeden Besuch für ein günstiges Ergebnis optimiert.

* Der Algorithmus sagt die Neigung eines Besuchers zur Konversion (oder den geschätzten Umsatz aus der Konversion) voraus, um das beste Erlebnis zu erzielen.
* Ein Besucher hat am Ende einer vorhandenen Sitzung Anspruch auf ein neues Erlebnis (es sei denn, der Besucher gehört zur Kontrollgruppe. In diesem Fall bleibt das Erlebnis, das dem Besucher beim ersten Besuch zugewiesen wurde, bei nachfolgenden Besuchen gleich).
* Innerhalb einer Sitzung ändert sich die Prognose nicht, um die visuelle Konsistenz zu wahren.

### Der Algorithmus passt sich Änderungen im Besucherverhalten an.

* Der mehrarmige Bandit stellt sicher, dass das Modell immer einen kleinen Bruchteil des Traffics „ausgibt“, um während des gesamten Lebens der Lernaktivität weiter zu lernen und eine Übernutzung der zuvor gelernten Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden mit den neuesten Daten zum Besucherverhalten neu erstellt, um sicherzustellen, dass [!DNL Target] immer die sich ändernden Besucherpräferenzen nutzen.
* Wenn der Algorithmus keine Gewinnererlebnisse für Einzelpersonen bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) gefunden.

### Der Algorithmus wird kontinuierlich für eine einzelne Zielmetrik optimiert.

* Diese Metrik kann konversionsbasiert oder umsatzbasiert sein (genauer gesagt [!UICONTROL Revenue per Visit]).

### [!DNL Target] erfasst automatisch Informationen über Besucher, um die Personalisierungsmodelle zu erstellen.

* Weitere Informationen zu den in [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] verwendeten Parametern finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] verwendet automatisch alle [!DNL Adobe Experience Cloud] freigegebenen Zielgruppen, um die Personalisierungsmodelle zu erstellen.

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

### Marketing-Experten können Offline-Daten, Tendenzwerte oder andere benutzerdefinierte Daten hochladen, um Personalisierungsmodelle zu erstellen.

* Weitere Informationen zum [ von Daten für [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Wie unterscheidet sich [!UICONTROL Auto-Target] von [!UICONTROL Automated Personalization]? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Auto-Target] benötigt häufig weniger Traffic als [!UICONTROL Automated Personalization], um ein personalisiertes Modell zu erstellen.

Obwohl die Menge des Traffics *pro Erlebnis*, der für die Erstellung von [!UICONTROL Auto-Target]- oder [!UICONTROL Auto Personalization]-Modellen benötigt wird, identisch ist, gibt es in der Regel mehr Erlebnisse in einer [!UICONTROL Automated Personalization] als in einer [!UICONTROL Auto-Target].

Wenn Sie beispielsweise eine [!UICONTROL Auto Personalization]-Aktivität hätten, in der Sie zwei Angebote pro Standort mit zwei Standorten erstellt haben, wären insgesamt vier (2 = 4) Erlebnisse in der Aktivität enthalten (ohne Ausschlüsse). Mit [!UICONTROL Auto-Target] können Sie Erlebnis 1 so einstellen, dass Angebot 1 an Standort 1 und Angebot 2 an Standort 2 einbezogen wird, und Erlebnis 2 so, dass Angebot 1 an Standort 1 und Angebot 2 an Standort 2 einbezogen wird. Da Sie mit [!UICONTROL Auto-Target] mehrere Änderungen in einem Erlebnis vornehmen können, können Sie die Anzahl der gesamten Erlebnisse in Ihrer Aktivität reduzieren.

[!UICONTROL Auto-Target] können einfache Faustregeln verwendet werden, um Traffic-Anforderungen zu verstehen:

* **Wenn [!UICONTROL Conversion] Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag und Erlebnis. Außerdem muss die Aktivität mindestens 7.000 Besuche und 350 Konversionen aufweisen.
* **Wenn [!UICONTROL Revenue per Visit] Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag und Erlebnis. Außerdem muss die Aktivität mindestens 1.000 Konversionen pro Erlebnis aufweisen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

### [!UICONTROL Auto-Target] verfügt über umfassende Einrichtungsfunktionen.

* Da [!UICONTROL Auto-Target] in den Workflow für A/B-Aktivitäten eingebettet ist, profitiert [!UICONTROL Auto-Target] von der ausgereifteren und vollwertigeren [!UICONTROL Visual Experience Composer] (VEC). Sie können auch [QA-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) mit [!UICONTROL Auto-Target] verwenden.

### [!UICONTROL Auto-Target] bietet ein umfassendes Framework für Online-Tests.

* Der Multi-Arm-Bandit ist Teil eines größeren Online-Test-Frameworks, das es [!DNL Adobe] Datenwissenschaftlern und Forschern ermöglicht, die Vorteile ihrer kontinuierlichen Verbesserungen der realen Bedingungen zu verstehen.
* In Zukunft wird es uns diese Testumgebung ermöglichen, die [!DNL Adobe] Plattform für maschinelles Lernen für datenversierte Kunden zu öffnen, sodass sie ihre eigenen Modelle einbringen können, um die [!DNL Target] Modelle zu ergänzen.

## Reporting und [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Weitere Informationen finden Sie unter [Reporting und Automatisches Targeting](/help/main/c-activities/auto-target/reporting-and-auto-target.md).
