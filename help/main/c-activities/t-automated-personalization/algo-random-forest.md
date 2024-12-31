---
keywords: Zufällige Gesamtstruktur;Entscheidungsbaum;AP;Automated Personalization
description: Erfahren Sie [!DNL Adobe Target]  wie der Algorithmus „Random Forest“ sowohl in [!UICONTROL Automated Personalization] (AP)- als auch in [!UICONTROL Auto-Target]-Aktivitäten verwendet.
title: Wie verwendet  [!DNL Target]  den Algorithmus der zufälligen Gesamtstruktur?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 41%

---

# Random-Forest-Algorithmus

Der wichtigste Personalisierungsalgorithmus, der sowohl in (AP)- als auch in [!DNL Auto-Target] -Aktivitäten verwendet wird, ist „Random Forest“. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere prädiktive Leistung zu erzielen, als sie mit einem der einzelnen Lernalgorithmen erzielt werden könnte. Der Random Forest-Algorithmus in [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] ist eine Klassifizierungs- oder Regressionsmethode, die durch das Erstellen einer Vielzahl von Entscheidungsbäumen während des Trainings funktioniert.

Wenn man an Statistiken denkt, kommt einem ein einzelnes Regressionsmodell in den Sinn, mit dem man ein Ergebnis vorhersagen kann. Neueste datenwissenschaftliche Forschungen legen nahe, dass „Ensemble-Methoden“, bei denen mehrere Modelle aus demselben Datensatz erstellt und dann intelligent kombiniert werden, bessere Ergebnisse liefern als die Vorhersage auf der Grundlage eines einzelnen Modells.

Der Algorithmus der zufälligen Gesamtstruktur ist der wichtigste zugrunde liegende Personalisierungsalgorithmus, der in [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target] verwendet wird. Random Forest kombiniert hunderte von Entscheidungen mit Bäumen, um eine bessere Vorhersage zu treffen, als ein einzelner Baum allein treffen könnte.

## Was ist ein Entscheidungsbaum? {#section_7F5865D8064447F4856FED426243FDAC}

Ziel eines Entscheidungsbaums ist es, alle verfügbaren Besuchsdaten, aus denen ein System lernen kann, aufzuschlüsseln und diese Daten dann zu gruppieren, bei denen die Besuche innerhalb jeder Gruppe in Bezug auf die Zielmetrik einander so ähnlich wie möglich sind. In den verschiedenen Gruppen sind die Besuche jedoch in Bezug auf die Zielmetrik (z. B. Konversionsrate) so unterschiedlich wie möglich. Der Entscheidungsbaum untersucht die verschiedenen Variablen, die er im Trainingssatz hat, um zu bestimmen, wie die Daten in einer gegenseitig ausschließenden, kollektiv erschöpfenden Weise (MECE) in diese Gruppen (oder „Blätter„) aufgeteilt werden, um dieses Ziel zu maximieren.

Nehmen wir in einem einfachen Beispiel zwei Eingabevariablen an:

* Geschlecht (mit zwei möglichen Werten, männlich oder weiblich)
* Postleitzahl (mit fünf potenziellen Werten in dem kleinen Datensatz: 11111, 22222, 33333, 44444 oder 55555)

Wenn die Zielmetrik Konversion ist, würde die Baumstruktur zunächst bestimmen, welche der beiden Variablen die größte Varianz in der Konversionsrate der Besuchsdaten erklärt.

Nehmen wir einmal an, die Postleitzahl sei sehr prädiktiv. Diese Variable würde dann den ersten „Zweig“ des Baumes bilden. Der Entscheidungsbaum würde dann festlegen, wie die Besuchsdaten aufgeteilt werden sollen, z. B. die Konversionsrate der Datensätze innerhalb der einzelnen Splits wäre so ähnlich wie möglich und die Konversionsrate zwischen den Splits so unterschiedlich wie möglich. Angenommen, in diesem Beispiel sind 11111, 22222, 33333 eine Aufspaltung und 44444 und 55555 eine zweite Aufspaltung.

Diese Aktion führt zur ersten Ebene des Entscheidungsbaums:

![decision_tree_1 Bild](assets/decsion_tree_1.png)

Der Entscheidungsbaum stellt die Frage: „Was ist die prognostizierbarste Variable?“ In diesem Beispiel gibt es nur zwei Variablen, daher ist die Antwort hier eindeutig Geschlecht. Die Baumstruktur versucht nun, eine ähnliche Übung zur Aufspaltung der Daten (*jede Verzweigung)*. Betrachten wir zunächst Zweig 11111, 22222 und 33333. Wenn es in diesen Postleitzahlbereichen zwischen Männern und Frauen einen Unterschied bei der Konversion gäbe, dann gäbe es zwei Blätter (Männer und Frauen) und dieser Zweig wäre komplett. Nehmen wir an, dass es in den anderen Bereichen, 44444 und 55555, keinen statistischen Unterschied gibt zwischen der Konversion von Frauen und Männern. In diesem Fall wird der erste Zweig zum endgültigen Split.

Das Beispiel würde zur folgenden Baumstruktur führen:

![decision_tree_2 Bild](assets/decsion_tree_2.png)

## Wie werden Entscheidungsbäume von Random Forest verwendet? {#section_536C105EF9F540C096D60450CAC6F627}

Entscheidungsbäume können ein effektives statistisches Werkzeug sein. Sie haben jedoch einige Nachteile. Am kritischsten ist, dass sie die Daten „überanpassen“ können, sodass ein einzelner Baum zukünftige Daten schlecht vorhersagt, die nicht für den Aufbau des ursprünglichen Baums verwendet wurden. Dieses Problem ist in der Statistik als [Verzerrung-Varianz-Dilemma](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) bekannt. Zufällige Wälder helfen, diese übermäßig große Herausforderung zu bewältigen. Auf der obersten Ebene ist Random Forest eine Sammlung von Entscheidungsbäumen, die leicht unterschiedlich auf dem gleichen Datensatz aufgebaut sind und gemeinsam „abstimmen“, um ein besseres Modell zu erhalten, als ein einzelner Baum dies kann. Die Bäume werden erstellt, indem eine Untergruppe von Besuchsdatensätzen mit Ersetzung (auch als Einsacken bezeichnet) nach dem Zufallsprinzip ausgewählt und eine Untergruppe der Attribute zufällig ausgewählt wird, sodass die Gesamtstruktur aus etwas anderen Entscheidungsbäumen besteht. Diese Methode ermöglicht kleine Variationen der Bäume, die im Random Forest entstehen. Das Hinzufügen dieser kontrollierten Varianz hilft, die Vorhersagegenauigkeit des Algorithmus zu verbessern.

## Wie verwenden die [!DNL Target] Personalisierungsalgorithmen die Zufallsstruktur? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### So werden Modelle erstellt

Das folgende Diagramm fasst zusammen, wie Modelle für [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten erstellt werden:

![random_forest_flow Bild](assets/random_forest_flow.png){width="650" zoomable="yes"}

1. Target erfasst Daten zu Besuchern bei der zufälligen Bereitstellung von Erlebnissen oder Angeboten
1. Nachdem [!DNL Target] eine kritische Masse an Daten erreicht hat, führt [!DNL Target] Feature Engineering durch
1. [!DNL Target] erstellt für jedes Erlebnis oder Angebot Modelle für zufällige Gesamtstrukturen
1. [!DNL Target] prüft, ob das Modell einen Schwellenwert für die Qualität erreicht
1. [!DNL Target] verschiebt das Modell in die Produktion, um zukünftigen Traffic zu personalisieren

[!DNL Target] verwendet automatisch erfasste Daten und von Ihnen bereitgestellte benutzerdefinierte Daten, um seine Personalisierungsalgorithmen zu erstellen. Diese Modelle prognostizieren das beste Erlebnis oder das beste Angebot für den Besucher. Im Allgemeinen wird ein Modell pro Erlebnis (bei einer [!UICONTROL Auto-Target]) oder pro Angebot (bei einer [!UICONTROL Automated Personalization]) erstellt. [!DNL Target] zeigt dann das Erlebnis oder Angebot an, das die höchste prognostizierte Erfolgsmetrik liefert (z. B. Konversionsrate). Diese Modelle müssen mit zufällig ausgewählten Besuchen trainiert werden, bevor sie für eine Vorhersage verwendet werden können. Daher werden auch den Besuchern, die sich in der personalisierten Gruppe befinden, bei Beginn einer Aktivität nach dem Zufallsprinzip verschiedene Erlebnisse oder Angebote angezeigt, bis die Personalisierungsalgorithmen betriebsbereit sind.

Jedes Modell muss validiert werden, um sicherzustellen, dass es das Verhalten von Besuchern vorhersagen kann, bevor es in Ihrer Aktivität verwendet wird. Die Modelle werden anhand ihrer Fläche unter der Kurve (AUC) validiert. Da eine Validierung erforderlich ist, hängt der genaue Zeitpunkt, zu dem ein Modell mit der Bereitstellung personalisierter Erlebnisse beginnt, von den Details der Daten ab. Für die praktische Traffic-Planung dauert es in der Regel mehr als die Mindestzahl an Konversionen, bis ein Modell funktionsfähig ist.

Wenn ein Modell für ein Erlebnis oder ein Angebot in Funktion geht, wird das Uhrensymbol links neben dem Erlebnis-/Angebotsnamen zu einem grünen Kontrollkästchen. Wenn gültige Modelle für mindestens zwei Erlebnisse oder Angebote vorhanden sind, werden einige Besuche personalisiert.

### Funktionstransformation

Bevor die Daten in den Personalisierungsalgorithmus aufgenommen werden, durchlaufen sie eine Merkmalumwandlung, die man sich als Vorbereitung der mit den Trainingsdatensätzen gesammelten Daten für die Verwendung durch die Personalisierungsmodelle vorstellen kann.

Die Merkmalumwandlungen hängen vom Attributtyp ab. Es gibt vor allem zwei Arten von Attributen (oder „Features“, wie sie manchmal von Datenwissenschaftlern genannt werden):

* **Kategorische Merkmale:** Kategorische Merkmale lassen sich nicht zählen, können jedoch in verschiedene Gruppen unterteilt werden. Dabei kann es sich um Merkmale wie Land, Geschlecht oder Postleitzahl handeln.
* **Numerische Merkmale:** Diese Merkmale lassen sich messen oder zählen – beispielsweise Alter, Einkommen usw.

Für kategorische Merkmale wird ein Satz mit allen möglichen Merkmalsausprägungen gepflegt und die Umwandlungswahrscheinlichkeit wird verwendet, um die Datengröße zu reduzieren. Bei numerischen Funktionen wird durch eine Neuskalierung sichergestellt, dass die Funktionen allgemein vergleichbar sind.

### Ausgleich zwischen Lernen und Personalisierung mit dem mehrarmigen Banditen

Nachdem [!DNL Target] Personalisierungsmodelle erstellt hat, um Ihren Traffic zu personalisieren, gibt es einen klaren Zielkonflikt für zukünftige Besucher Ihrer Aktivität. Sollen Sie den gesamten Traffic basierend auf dem aktuellen Modell personalisieren oder sollten Sie weiterhin von neuen Besuchern lernen, indem Sie ihnen nach dem Zufallsprinzip zufällige Angebote unterbreiten? Sie möchten sicherstellen, dass der Personalisierungsalgorithmus immer über neue Trends bei Ihren Besuchern informiert ist, während Sie gleichzeitig den größten Teil des Traffics personalisieren.

Der mehrarmige Bandit hilft [!DNL Target] dabei, dieses Ziel zu erreichen. Der mehrarmige Bandit stellt sicher, dass das Modell immer einen kleinen Bruchteil des Traffics „ausgibt“, um während des gesamten Lebens der Lernaktivität weiter zu lernen und eine Übernutzung der zuvor gelernten Trends zu verhindern.

In der Welt der Datenwissenschaft ist das Multi-Armed-Bandit-Problem ein klassisches Beispiel für das Dilemma zwischen Exploration und Exploitation, bei dem eine Sammlung einarmiger Banditen mit jeweils unbekannter Belohnungswahrscheinlichkeit vergeben wird. Die Grundidee besteht in der Entwicklung einer Strategie, die dazu führt, dass der Automat mit der höchsten Erfolgswahrscheinlichkeit bedient wird, sodass der Gesamtgewinn maximiert wird. Multi-Armed Bandit wird im System für die Online-Bewertung verwendet, nachdem die Online-Modelle erstellt wurden. Dieser Prozess hilft beim Online-Lernen während der Exploration. Der aktuelle mehrarmige Algorithmus ist ein epsilon () gieriger Algorithmus. Bei diesem Algorithmus wird mit einer Wahrscheinlichkeit von 1-ε der beste Arm gewählt. Die Wahrscheinlichkeit für die zufällige Auswahl eines beliebigen anderen Arms ist ε.
