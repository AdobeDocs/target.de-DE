---
keywords: Randwald; Entscheidungsbaum; App; Automated Personalization
description: Erfahren Sie, wie [!DNL Adobe Target] den Random Forest-Algorithmus sowohl in den Aktivitäten [!UICONTROL Automated Personalization] (AP) als auch in den Aktivitäten [!UICONTROL Auto-Target] verwendet.
title: Wie verwendet [!DNL Target] den Random Forest-Algorithmus?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 41%

---

# Random-Forest-Algorithmus

Der wichtigste Personalisierungsalgorithmus, der sowohl für die AP- als auch für die [!DNL Auto-Target]-Aktivitäten verwendet wird, ist Random Forest. Ensemble-Methoden, wie Random Forest, verwenden mehrere Lernalgorithmen, um eine bessere Vorhersageleistung zu erzielen, als sie sich aus den einzelnen Lernalgorithmen ergeben könnte. Der Random Forest-Algorithmus in [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] ist eine Classification- oder Regressionsmethode, die beim Trainieren eine Vielzahl von Entscheidungsbäumen erstellt.

Wenn man an Statistiken denkt, kommt einem ein einzelnes Regressionsmodell in den Sinn, mit dem man ein Ergebnis vorhersagen kann. Neueste datenwissenschaftliche Forschungen legen nahe, dass „Ensemble-Methoden“, bei denen mehrere Modelle aus demselben Datensatz erstellt und dann intelligent kombiniert werden, bessere Ergebnisse liefern als die Vorhersage auf der Grundlage eines einzelnen Modells.

Der Random Forest-Algorithmus ist der wichtigste zugrunde liegende Personalisierungsalgorithmus, der in den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] verwendet wird. Random Forest kombiniert Hunderte von Entscheidungsbäumen, um zu einer besseren Vorhersage zu gelangen, als es ein einzelner Baum allein tun könnte.

## Was ist ein Entscheidungsbaum? {#section_7F5865D8064447F4856FED426243FDAC}

Ziel einer Entscheidungsstruktur ist es, alle verfügbaren Besuchsdaten, aus denen ein System lernen kann, aufzuschlüsseln und diese Daten dann zu gruppieren, wobei Besuche innerhalb jeder Gruppe im Hinblick auf die Zielmetrik so ähnlich wie möglich sind. Gruppenübergreifend sind die Besuche jedoch hinsichtlich der Zielmetrik (z. B. Konversionsrate) so unterschiedlich wie möglich. Der Entscheidungsbaum untersucht die verschiedenen Variablen, die er im Trainings-Satz hat, um zu bestimmen, wie die Daten in einer MECE-Methode (Mutally Exclusive Collective Exhaustive) in diese Gruppen (oder &quot;Blätter&quot;) aufgeteilt werden, um dieses Ziel zu maximieren.

In einem einfachen Beispiel nehmen wir zwei Eingabevariablen an:

* Geschlecht (mit zwei möglichen Werten, männlich oder weiblich)
* Postleitzahl (mit fünf potenziellen Werten im kleinen Datensatz: 11111, 2222, 33333, 44444 oder 5555)

Wenn die Zielmetrik Konversion ist, bestimmt der Baum zunächst, welche der beiden Variablen die größte Variation der Konversionsrate der Besuchsdaten erklärt.

Nehmen wir einmal an, die Postleitzahl sei sehr prädiktiv. Diese Variable würde dann den ersten „Zweig“ des Baumes bilden. Der Entscheidungsbaum würde dann festlegen, wie die Besuchsdaten aufgeteilt werden sollen, z. B. die Konversionsrate der Datensätze innerhalb der einzelnen Splits wäre so ähnlich wie möglich und die Konversionsrate zwischen den Splits so unterschiedlich wie möglich. In diesem Beispiel wird angenommen, dass 11111, 2222, 3333 eine Aufspaltung und 44444 und 55555 eine zweite Aufspaltung sind.

Diese Aktion führt zur ersten Ebene des Entscheidungsbaums:

![decsion_tree_1 image](assets/decsion_tree_1.png)

Der Entscheidungsbaum stellt die Frage: &quot;Was ist die prädiktivste Variable?&quot; In diesem Beispiel gibt es nur zwei Variablen, daher lautet die Antwort hier eindeutig Geschlecht. Der Baum sucht nun nach einer ähnlichen Übung, um die Daten *in jedem Zweig* aufzuteilen. Betrachten wir zunächst Zweig 11111, 22222 und 33333. Wenn es in diesen Postleitzahlbereichen zwischen Männern und Frauen einen Unterschied bei der Konversion gäbe, dann gäbe es zwei Blätter (Männer und Frauen) und dieser Zweig wäre komplett. In den anderen Zweigen, 44444 und 5555, nehmen wir an, es gibt keinen statistischen Unterschied zwischen der Konvertierung von Frauen und Männern. In diesem Fall wird der erste Zweig zum endgültigen Split.

Das Beispiel würde zu der folgenden Baumstruktur führen:

![decsion_tree_2 image](assets/decsion_tree_2.png)

## Wie werden Entscheidungsbäume von Random Forest verwendet? {#section_536C105EF9F540C096D60450CAC6F627}

Entscheidungsbäume können ein effektives statistisches Werkzeug sein. Sie haben jedoch einige Nachteile. Am kritischsten ist, dass sie die Daten „überanpassen“ können, sodass ein einzelner Baum zukünftige Daten schlecht vorhersagt, die nicht für den Aufbau des ursprünglichen Baums verwendet wurden. Dieses Problem ist in der Statistik als [Verzerrung-Varianz-Dilemma](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) bekannt. Random-Wälder helfen bei der Überanpassung. Auf der obersten Ebene ist Random Forest eine Sammlung von Entscheidungsbäumen, die leicht unterschiedlich auf dem gleichen Datensatz aufgebaut sind und gemeinsam „abstimmen“, um ein besseres Modell zu erhalten, als ein einzelner Baum dies kann. Die Bäume werden durch die zufällige Auswahl einer Teilmenge von Besuchsprotokollen mit Ersetzung (auch als Ausbaggern bezeichnet) und die zufällige Auswahl einer Teilmenge der Attribute erstellt, sodass der Wald aus leicht unterschiedlichen Entscheidungsbäumen besteht. Diese Methode ermöglicht kleine Variationen der Bäume, die im Random Forest entstehen. Das Hinzufügen dieser kontrollierten Varianz hilft, die Vorhersagegenauigkeit des Algorithmus zu verbessern.

## Wie verwenden die [!DNL Target]-Personalisierungsalgorithmen Random Forest? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### Wie Modelle erstellt werden

Das folgende Diagramm fasst zusammen, wie Modelle für [!UICONTROL Auto-Target] - und [!UICONTROL Automated Personalization] -Aktivitäten erstellt werden:

![random_forest_flow image](assets/random_forest_flow.png){width="650" zoomable="yes"}

1. Target erfasst Daten zu Besuchern, während Erlebnisse oder Angebote zufällig bereitgestellt werden
1. Nachdem [!DNL Target] eine kritische Datenmenge erreicht hat, führt [!DNL Target] die Funktionsentwicklung durch
1. [!DNL Target] erstellt Random Forest-Modelle für jedes Erlebnis oder Angebot
1. [!DNL Target] überprüft, ob das Modell einen Schwellenwert für die Qualitätsbewertung erreicht
1. [!DNL Target] überträgt das Modell zur Produktion, um zukünftigen Traffic zu personalisieren

[!DNL Target] verwendet automatisch erfasste Daten und von Ihnen bereitgestellte benutzerdefinierte Daten, um seine Personalisierungsalgorithmen zu erstellen. Diese Modelle prognostizieren das beste Erlebnis oder das beste Angebot für den Besucher. Im Allgemeinen wird ein Modell pro Erlebnis (bei einer [!UICONTROL Auto-Target] -Aktivität) oder pro Angebot (bei einer [!UICONTROL Automated Personalization] -Aktivität erstellt. [!DNL Target] angezeigt, zeigt dann das Erlebnis oder Angebot an, das die höchste prognostizierte Erfolgsmetrik liefert (z. B. Konversionsrate). Diese Modelle müssen mit zufällig ausgewählten Besuchen trainiert werden, bevor sie für eine Vorhersage verwendet werden können. Daher werden auch den Besuchern, die sich in der personalisierten Gruppe befinden, bei Beginn einer Aktivität nach dem Zufallsprinzip verschiedene Erlebnisse oder Angebote angezeigt, bis die Personalisierungsalgorithmen betriebsbereit sind.

Jedes Modell muss validiert werden, um sicherzustellen, dass es gut darin ist, das Verhalten der Besucher vorherzusagen, bevor es in Ihrer Aktivität verwendet wird. Modelle werden anhand ihres Bereichs unter der Kurve (AUC) validiert. Aufgrund der Notwendigkeit einer Validierung hängt der genaue Zeitpunkt, zu dem ein Modell mit der Bereitstellung personalisierter Erlebnisse beginnt, von den Details der Daten ab. Für die praktische Traffic-Planung dauert es in der Regel mehr als die Mindestzahl an Konversionen, bis ein Modell funktionsfähig ist.

Wenn ein Modell für ein Erlebnis oder ein Angebot in Funktion geht, wird das Uhrensymbol links neben dem Erlebnis-/Angebotsnamen zu einem grünen Kontrollkästchen. Wenn es gültige Modelle für mindestens zwei Erlebnisse oder Angebote gibt, beginnen einige Besuche zu personalisieren.

### Merkmalumwandlung

Bevor die Daten in den Personalisierungsalgorithmus aufgenommen werden, durchlaufen sie eine Merkmalumwandlung, die man sich als Vorbereitung der mit den Trainingsdatensätzen gesammelten Daten für die Verwendung durch die Personalisierungsmodelle vorstellen kann.

Die Merkmalumwandlungen hängen vom Attributtyp ab. Es gibt vor allem zwei Arten von Attributen (oder „Features“, wie sie manchmal von Datenwissenschaftlern genannt werden):

* **Kategorische Merkmale:** Kategorische Merkmale lassen sich nicht zählen, können jedoch in verschiedene Gruppen unterteilt werden. Dabei kann es sich um Merkmale wie Land, Geschlecht oder Postleitzahl handeln.
* **Numerische Merkmale:** Diese Merkmale lassen sich messen oder zählen – beispielsweise Alter, Einkommen usw.

Für kategorische Merkmale wird ein Satz mit allen möglichen Merkmalsausprägungen gepflegt und die Umwandlungswahrscheinlichkeit wird verwendet, um die Datengröße zu reduzieren. Bei numerischen Funktionen stellt die Neuskalierung sicher, dass die Funktionen auf allen Ebenen vergleichbar sind.

### Ausbalancieren von Lernen und Personalisierung mit dem Multi-Armed Bandit

Nachdem für [!DNL Target] Personalisierungsmodelle zur Personalisierung Ihres Traffics erstellt wurden, gibt es einen klaren Kompromiss für zukünftige Besucher Ihrer Aktivität. Sollten Sie den gesamten Traffic basierend auf dem aktuellen Modell personalisieren oder sollten Sie weiterhin von neuen Besuchern lernen, indem Sie ihnen zufällige Angebote bereitstellen? Sie möchten sicherstellen, dass der Personalisierungsalgorithmus immer über neue Trends bei Ihren Besuchern informiert ist, während Sie gleichzeitig den größten Teil des Traffics personalisieren.

Der mehrarmige Bandit zeigt, wie [!DNL Target] Ihnen dabei hilft, dieses Ziel zu erreichen. Der &quot;mehrarmige Bandit&quot;stellt sicher, dass das Modell immer einen kleinen Bruchteil des Traffics &quot;ausgibt&quot;, um während des gesamten Lebenszyklus des Aktivitätslernens weiter zu lernen und eine Übernutzung zuvor erlernter Trends zu verhindern.

In der datenwissenschaftlichen Welt ist das Multi-Armed Bandit-Problem ein klassisches Beispiel für das Exploration versus Explosion-Dilemma, in dem eine Sammlung einarmiger Banditen mit unbekannter Belohnungswahrscheinlichkeit gegeben wird. Die Grundidee besteht in der Entwicklung einer Strategie, die dazu führt, dass der Automat mit der höchsten Erfolgswahrscheinlichkeit bedient wird, sodass der Gesamtgewinn maximiert wird. Multi-Armed Bandit wird im System für die Online-Bewertung verwendet, nachdem die Online-Modelle erstellt wurden. Dieser Prozess hilft beim Online-Lernen während der Erkundung. Der aktuelle Multi-Armed-Algorithmus ist ein Greedy-Algorithmus für Epsilon (ε). Bei diesem Algorithmus wird mit einer Wahrscheinlichkeit von 1-ε der beste Arm gewählt. Die Wahrscheinlichkeit für die zufällige Auswahl eines beliebigen anderen Arms ist ε.
