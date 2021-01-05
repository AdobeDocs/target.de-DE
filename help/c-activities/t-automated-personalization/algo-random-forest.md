---
keywords: random forest;decision tree;ap;Automated Personalization
description: Der wichtigste Personalisierungsalgorithmus von Target, der sowohl in der automatisierten Personalisierung als auch im automatischen Targeting verwendet wird, ist Random Forest. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere Prognoseleistung zu erzielen, als dies bei der isolierten Verwendung dieser Lernalgorithmen möglich wäre. Der Random Forest-Algorithmus der automatisierten Personalisierung ist eine Classification- oder Regressionsmethode, deren Funktionsweise die Konstruktion einer Vielzahl von Entscheidungsbäumen während der Anlernzeit zugrunde liegt.
title: Random-Forest-Algorithmus
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 97%

---


# ![PREMIUM](/help/assets/premium.png) Random-Forest-Algorithmus

Der wichtigste Personalisierungsalgorithmus von Target, der sowohl in der automatisierten Personalisierung als auch im automatischen Targeting verwendet wird, ist Random Forest. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere Prognoseleistung zu erzielen, als dies bei der isolierten Verwendung dieser Lernalgorithmen möglich wäre. Der Random Forest-Algorithmus der automatisierten Personalisierung ist eine Classification- oder Regressionsmethode, deren Funktionsweise die Konstruktion einer Vielzahl von Entscheidungsbäumen während der Anlernzeit zugrunde liegt.

Wenn man an Statistiken denkt, kommt einem ein einzelnes Regressionsmodell in den Sinn, mit dem man ein Ergebnis vorhersagen kann. Neueste datenwissenschaftliche Forschungen legen nahe, dass „Ensemble-Methoden“, bei denen mehrere Modelle aus demselben Datensatz erstellt und dann intelligent kombiniert werden, bessere Ergebnisse liefern als die Vorhersage auf der Grundlage eines einzelnen Modells.

Der Random Forest-Algorithmus ist der Schlüssel des Personalisierungsalgorithmus, der bei automatisierten Personalisierungs- und Targeting-Aktivitäten verwendet wird. Random Forest fasst Hunderte von Entscheidungsbäumen zusammen, um eine bessere Vorhersage zu erhalten, als es ein einzelner Baum allein könnte.

## Was ist ein Entscheidungsbaum? {#section_7F5865D8064447F4856FED426243FDAC}

Das Ziel eines Entscheidungsbaums ist es, alle verfügbaren Besuchsdaten, aus denen ein System lernen kann, aufzuschlüsseln und diese Daten zu gruppieren, wobei die Besuche innerhalb jeder Gruppe in Bezug auf die Zielmetrik so ähnlich wie möglich sind. Gruppenübergreifend sind die Besuche jedoch, bezogen auf die Zielkennzahl (z. B. Konversionsrate), so unterschiedlich wie möglich. Der Entscheidungsbaum betrachtet die verschiedenen Variablen, die er im Trainingssatz hat, um zu bestimmen, wie die Daten in einem MECE(Mutually-Exclusive-Collectively-Exhaustive)-Weg in diese Gruppen (oder „Blätter“) aufgeteilt werden können, um dieses Ziel auszubauen.

Als einfaches Beispiel nehmen wir an, dass wir nur zwei Eingangsvariablen haben:

* Geschlecht (mit zwei möglichen Werten, männlich oder weiblich)
* Postleitzahl (mit fünf möglichen Werten in unserem kleinen Datensatz: 11111, 22222, 33333, 44444 oder 55555)

Wenn unsere Zielmetrik die Konversion ist, dann würde der Baum zuerst bestimmen, welche unserer beiden Variablen die größte Variation der Konversionsrate der Besuchsdaten erklärt.

Nehmen wir einmal an, die Postleitzahl sei sehr prädiktiv. Diese Variable würde dann den ersten „Zweig“ des Baumes bilden. Der Entscheidungsbaum würde dann festlegen, wie die Besuchsdaten aufgeteilt werden sollen, z. B. die Konversionsrate der Datensätze innerhalb der einzelnen Splits wäre so ähnlich wie möglich und die Konversionsrate zwischen den Splits so unterschiedlich wie möglich. In unserem Beispiel gehen wir davon aus, dass 11111, 22222, 33333 ein Split und 44444 und 55555 ein zweiter Split sind.

Diese Aktion würde die erste Schicht unseres Entscheidungsbaums ergeben:

![](assets/decsion_tree_1.png)

Der Entscheidungsbaum würde die Frage stellen: „Was ist die prädiktivste Variable?“ In unserem Beispiel haben wir nur zwei Variablen, daher lautet die Antwort hier eindeutig Geschlecht. Der Baum versucht nun, ein ähnliches Verfahren auszuführen, um die Daten *in jedem Zweig* aufzuteilen. Betrachten wir zunächst Zweig 11111, 22222 und 33333. Wenn es in diesen Postleitzahlbereichen zwischen Männern und Frauen einen Unterschied bei der Konversion gäbe, dann gäbe es zwei Blätter (Männer und Frauen) und dieser Zweig wäre komplett. In dem anderen Zweig, 44444 und 55555, gehen wir einmal davon aus, dass es keinen statistischen Unterschied gibt, wie Frauen und Männer konvertieren. In diesem Fall wird der erste Zweig zum endgültigen Split.

Unser Beispiel würde zu dem unten stehenden Baum führen:

![](assets/decsion_tree_2.png)

## Wie werden Entscheidungsbäume von Random Forest genutzt? {#section_536C105EF9F540C096D60450CAC6F627}

Entscheidungsbäume können ein effektives statistisches Werkzeug sein. Sie haben jedoch einige Nachteile. Am kritischsten ist, dass sie die Daten „überanpassen“ können, sodass ein einzelner Baum zukünftige Daten schlecht vorhersagt, die nicht für den Aufbau des ursprünglichen Baums verwendet wurden. Dieses Problem ist in der Statistik als [Verzerrung-Varianz-Dilemma](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) bekannt. Random Forest kann bei der Überwindung dieses „Überanpassungsproblems“ helfen. Auf der obersten Ebene ist Random Forest eine Sammlung von Entscheidungsbäumen, die leicht unterschiedlich auf dem gleichen Datensatz aufgebaut sind und gemeinsam „abstimmen“, um ein besseres Modell zu erhalten, als ein einzelner Baum dies kann. Die Bäume werden durch die zufällige Auswahl einer Teilmenge von Besuchsdatensätzen mit Ersetzungen (bekannt als „Bagging“) sowie durch die zufällige Auswahl einer Teilmenge der Attribute aufgebaut, sodass der Wald aus leicht unterschiedlichen Entscheidungsbäumen besteht. Diese Methode ermöglicht kleine Variationen der Bäume, die im Random Forest entstehen. Das Hinzufügen dieser kontrollierten Varianz hilft, die Vorhersagegenauigkeit des Algorithmus zu verbessern.

## Wie verwenden die Personalisierungsalgorithmen der Zielgruppe Random Forest? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

**Der Aufbau von Modellen**

Das folgende Diagramm fasst zusammen, wie Modelle für automatisches Targeting oder automatisierte Personalisierungsaktivitäten aufgebaut werden:

![](assets/random_forest_flow.png)

1. Target sammelt Daten über Besucher, indem es zufällige Erlebnisse/Angebote vorschlägt.
1. Wenn Target eine bestimmte Menge an Daten gesammelt hat, führt es eine Merkmalbearbeitung durch.
1. Target erstellt Random Forest-Modelle für jedes Erlebnis und jedes Angebot.
1. Target prüft, ob das Modell einen Schwellenwert für die Qualitätsbewertung erreicht.
1. Target schiebt das Modell in die Produktion, um den zukünftigen Traffic zu personalisieren.

Target verwendet zur Erstellung seiner Personalisierungsalgorithmen Daten, die es automatisch sammelt, sowie benutzerdefinierte Daten, die von Ihnen zur Verfügung gestellt werden. Diese Modelle prognostizieren das beste Erlebnis oder das beste Angebot für den Besucher. In der Regel wird ein Modell pro Erlebnis (bei einer automatischen Targeting-Aktivität) oder pro Angebot (bei einer automatisierten Personalisierungsaktivität) erstellt. Target wählt für die Anzeige dann das Erlebnis oder das Angebot, das die höchste vorhergesagte Erfolgsmetriken (z. B. Konversionsrate) liefert. Diese Modelle müssen mit zufällig ausgewählten Besuchen trainiert werden, bevor sie für eine Vorhersage verwendet werden können. Daher werden auch den Besuchern, die sich in der personalisierten Gruppe befinden, bei Beginn einer Aktivität nach dem Zufallsprinzip verschiedene Erlebnisse oder Angebote angezeigt, bis die Personalisierungsalgorithmen betriebsbereit sind.

Jedes Modell muss validiert werden, um sicherzustellen, dass es das Besucherverhalten in ausreichendem Maße vorhersagen kann, bevor es in Ihrer Aktivität verwendet wird. Die Modelle werden anhand ihrer AUC (Fläche unter der Kurve) validiert. Aufgrund der Notwendigkeit dieser Validierung hängt der genaue Zeitpunkt, an dem ein Modell mit der Bereitstellung personalisierter Erlebnisse beginnt, von der Datengenauigkeit ab. Für die praktische Traffic-Planung dauert es in der Regel mehr als die Mindestzahl an Konversionen, bis ein Modell funktionsfähig ist.

Wenn ein Modell für ein Erlebnis oder ein Angebot in Funktion geht, wird das Uhrensymbol links neben dem Erlebnis-/Angebotsnamen zu einem grünen Kontrollkästchen. Wenn es funktionierende Modelle für mindestens zwei Erlebnisse/Angebote gibt, können die ersten Besuche personalisiert werden.

**Merkmalumwandlung **

Bevor die Daten in den Personalisierungsalgorithmus aufgenommen werden, durchlaufen sie eine Merkmalumwandlung, die man sich als Vorbereitung der mit den Trainingsdatensätzen gesammelten Daten für die Verwendung durch die Personalisierungsmodelle vorstellen kann.

Die Merkmalumwandlungen hängen vom Attributtyp ab. Es gibt vor allem zwei Arten von Attributen (oder „Features“, wie sie manchmal von Datenwissenschaftlern genannt werden):

* **Kategorische Merkmale:** Kategorische Merkmale lassen sich nicht zählen, können jedoch in verschiedene Gruppen unterteilt werden. Dabei kann es sich um Merkmale wie Land, Geschlecht oder Postleitzahl handeln.
* **Numerische Merkmale:** Diese Merkmale lassen sich messen oder zählen – beispielsweise Alter, Einkommen usw.

Für kategorische Merkmale wird ein Satz mit allen möglichen Merkmalsausprägungen gepflegt und die Umwandlungswahrscheinlichkeit wird verwendet, um die Datengröße zu reduzieren. Für numerische Merkmale wird durch Umskalierung gewährleistet, dass die Merkmale flächendeckend vergleichbar sind.

**Ausgewogenheit zwischen Lernen und Personalisierung mit dem Multi-Armed Bandit**

Nachdem Target Personalisierungsmodelle entwickelt hat, um Ihren Traffic zu personalisieren, stecken Sie in einem gewissen Konflikt, was die zukünftigen Besucher Ihrer Aktivität angeht: Sollten Sie nun den gesamten Traffic auf Basis des aktuellen Modells personalisieren oder sollten Sie weiterhin von neuen Besuchern lernen, indem Sie ihnen zufällige Angebote vorlegen? Sie möchten sicherstellen, dass der Personalisierungsalgorithmus immer über neue Trends bei Ihren Besuchern informiert ist, während Sie gleichzeitig den größten Teil des Traffics personalisieren.

Mit Multi-Armed Bandit von Target können Sie dieses Ziel erreichen. Multi-Armed Bandit gewährleistet, dass das Modell immer einen kleinen Anteil des Traffics darauf verwendet, während des gesamten Lebenszyklus der Aktivität weiter zu lernen, um so eine Übernutzung der zuvor erlernten Trends zu verhindern.

In der Welt der Datenwissenschaftler ist das Problem mit Multi-Armed Bandit (MAB) ein klassisches Beispiel für den Zwiespalt zwischen Exploration und Exploitation, bei dem eine Ansammlung „einarmiger Banditen“ mit unbekannter Belohnungswahrscheinlichkeit vorgegeben wird. Die Grundidee besteht in der Entwicklung einer Strategie, die dazu führt, dass der Automat mit der höchsten Erfolgswahrscheinlichkeit bedient wird, sodass der Gesamtgewinn maximiert wird. MAB wird im System beim Online-Scoring nach Erstellung der Online-Modelle verwendet. Dadurch wird das Online-Lernen während der Exploration unterstützt. Der aktuelle Multi-Armed-Algorithmus ist der Greedy-Algorithmus epsilon (ε). Bei diesem Algorithmus wird mit einer Wahrscheinlichkeit von 1-ε der beste Arm gewählt. Die Wahrscheinlichkeit für die zufällige Auswahl eines beliebigen anderen Arms ist ε.
