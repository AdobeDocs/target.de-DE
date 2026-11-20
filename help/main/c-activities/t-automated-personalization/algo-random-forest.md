---
keywords: Zufällige Gesamtstruktur;Entscheidungsbaum;AP;Automated Personalization
description: Erfahren Sie, wie [!DNL Adobe Target] den Algorithmus der zufälligen Gesamtstruktur sowohl in [!UICONTROL Automated Personalization] (AP)- als [!UICONTROL Automatisches Targeting]-Aktivitäten verwendet.
title: Wie verwendet [!DNL Target] den Algorithmus der zufälligen Gesamtstruktur?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
TQID: 'https://experienceleague.adobe.com/Ui8E8CkiiJSdqim9fzIgPDdsKG1MMtuu3EUuAqgmm0M'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 7eede3484d524e87127de9147aa786484fc87c7d
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 6%
---
# Random-Forest-Algorithmus {#random-forest-algorithm}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie [!DNL Target] den Algorithmus „Zufällige Gesamtstruktur“ verwendet, um die Personalisierungsmodelle von **[!UICONTROL Automated Personalization]**- und **[!UICONTROL Automatisches Targeting]**-Aktivitäten zu erstellen.

>[!ENDSHADEBOX]

Der wichtigste Personalisierungsalgorithmus, der sowohl in **[!UICONTROL Automated Personalization]** (AP)- als auch in **[!UICONTROL Automatisches Targeting]**-Aktivitäten verwendet wird, ist „Gesamtstruktur“. Es handelt sich dabei um eine Klassifizierungs- oder Regressionsmethode, bei der während des Trainings eine Vielzahl von Entscheidungsbäumen erstellt wird.

Random Forest ist eine Ensemble-Methode. Wenn man an Statistiken denkt, kommt einem ein einzelnes Regressionsmodell in den Sinn, mit dem man ein Ergebnis vorhersagen kann. Jüngste datenwissenschaftliche Forschungsergebnisse deuten darauf hin, dass „Ensemble-Methoden“, bei denen mehrere Modelle aus demselben Datensatz erstellt und dann intelligent kombiniert werden, bessere Ergebnisse liefern, als Vorhersagen, die allein auf einem einzigen Modell beruhen oder die aus einem der einzelnen Lernalgorithmen gewonnen werden könnten.

## Was ist ein Entscheidungsbaum? {#section_7F5865D8064447F4856FED426243FDAC}

In einem Entscheidungsbaum werden alle Besuchsdaten, aus denen ein System lernen kann, in Gruppen unterteilt. Besuche innerhalb jeder Gruppe sind in Bezug auf die Zielmetrik (z. B. Konversionsrate) einander so ähnlich wie möglich, und die Besuche zwischen Gruppen sind so unterschiedlich wie möglich. Dazu untersucht der Baum die Variablen im Trainingssatz und teilt die Daten auf eine gegenseitig ausschließende, kollektiv erschöpfende Weise (MECE) in Gruppen (oder „Blätter„) auf, die dieses Ziel maximieren.

Im folgenden einfachen Beispiel ist die Zielmetrik Konversion und es gibt zwei Eingabevariablen:

* Geschlecht (mit zwei möglichen Werten, männlich oder weiblich)
* Postleitzahl (mit fünf potenziellen Werten in dem kleinen Datensatz: 11111, 22222, 33333, 44444 oder 55555)

### Erste Teilung {#first-split}

Die Baumstruktur bestimmt zunächst, welche der beiden Variablen die größte Variation in der Konversionsrate der Besuchsdaten erklärt. Nehmen wir an, die Postleitzahl ist am prädiktivsten. Diese Variable bildet den ersten „Zweig“ des Baums. Die Baumstruktur teilt dann die Besuchsdaten wie oben beschrieben in Gruppen auf. Angenommen, 11111, 22222 und 33333 sind eine Aufspaltung und 44444 und 55555 eine zweite Aufspaltung.

![Erste Ebene des Entscheidungsbaums](assets/decsion_tree_1.png){width="440" align="center"}

### Innerhalb jedes Zweiges aufteilen {#second-split}

Der Baum stellt die Frage: „Was ist die vorhersagendste Variable?“ führt erneut eine ähnliche Übung zur Aufspaltung der Daten (*jede Verzweigung)*. Es bleibt nur noch das Geschlecht, also ist es hier die Antwort. Gehen Sie in der 11111, 22222 und 33333 Filiale davon aus, dass es einen Unterschied in der Konversion zwischen Männern und Frauen gibt. Es gibt dann zwei Blätter (Männer und Frauen), und dieser Zweig ist vollständig. Gehen wir in der 44444 und 55555 Branche davon aus, dass es keinen statistischen Unterschied zwischen der Konversion von Frauen und Männern gibt. In diesem Fall ist die erste Teilung die endgültige Teilung.

![Vollständiger Entscheidungsbaum](assets/decsion_tree_2.png){width="480" align="center"}

## Wie werden Entscheidungsbäume von Random Forest verwendet? {#section_536C105EF9F540C096D60450CAC6F627}

Entscheidungsbäume sind ein nützliches statistisches Tool. Sie haben jedoch einige Nachteile. Am wichtigsten ist, dass sie die Daten „übermäßig anpassen“ können, sodass ein einzelner Baum zukünftige Daten, die nicht zum Aufbau des ursprünglichen Baums verwendet wurden, nur schlecht vorhersagt. Dieses Problem ist in der Statistik als [Verzerrung-Varianz-Dilemma](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) bekannt.

Zufällige Wälder helfen, diese Herausforderung zu überwinden. Ein zufälliger Wald ist eine Sammlung von Hunderten von Entscheidungsbäumen, die auf demselben Datensatz etwas anders aufgebaut sind und die zusammen „abstimmen“, um ein besseres Modell als ein einzelner Baum zu erhalten. Die Bäume werden erstellt, indem eine Untergruppe von Besuchsdatensätzen per Zufallsauswahl mit Ersetzung (auch als Absacken bezeichnet) ausgewählt und eine Untergruppe der Attribute zufällig ausgewählt wird, sodass die Gesamtstruktur aus etwas anderen Entscheidungsbäumen besteht. Diese Methode führt kleine Variationen in die Bäume ein. Durch Hinzufügen dieser kontrollierten Varianz kann die prädiktive Genauigkeit des Algorithmus verbessert werden.

## Wie verwenden die [!DNL Target] Personalisierungsalgorithmen die Zufallsstruktur? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### So werden Modelle erstellt

[!DNL Target] verwendet automatisch erfasste Daten und von Ihnen bereitgestellte benutzerdefinierte Daten, um seine Personalisierungsalgorithmen zu erstellen. Das folgende Diagramm fasst zusammen, wie Modelle für **[!UICONTROL Automatisches Targeting]** und **[!UICONTROL Automated Personalization]**-Aktivitäten erstellt werden:

![Fluss, der zusammenfasst, wie Modelle für zufällige Gesamtstrukturen erstellt werden](assets/random_forest_flow.png){width="850" zoomable="yes"}

1. [!DNL Target] erfasst Daten zu Besuchern und stellt dabei nach dem Zufallsprinzip Erlebnisse oder Angebote bereit.
1. Nachdem [!DNL Target] eine kritische Masse an Daten erreicht hat, führt [!DNL Target] Feature Engineering durch.
1. [!DNL Target] erstellt Modelle des Typs „Zufällige Gesamtstruktur“ für jedes Erlebnis oder Angebot.
1. [!DNL Target] validiert das Modell, indem es prüft, ob es einen Schwellenwert für die Qualität erreicht.
1. [!DNL Target] verschiebt das Modell in die Produktion, um zukünftigen Traffic zu personalisieren.

Diese Modelle prognostizieren das beste Erlebnis oder das beste Angebot für den Besucher. Im Allgemeinen wird ein Modell pro Erlebnis (in einer **[!UICONTROL automatischen Targeting]**-Aktivität) oder pro Angebot (in einer **[!UICONTROL Automated Personalization]**-Aktivität) erstellt. [!DNL Target] zeigt dann das Erlebnis oder Angebot an, das die höchste prognostizierte Erfolgsmetrik liefert (z. B. Konversionsrate). Die Modelle müssen auf zufällig bereitgestellten Besuchen trainiert werden, bevor sie für die Prognose verwendet werden können. Daher werden auch den Besuchern, die der personalisierten Gruppe angehören, beim ersten Start einer Aktivität nach dem Zufallsprinzip verschiedene Erlebnisse oder Angebote angezeigt, bis die Personalisierungsalgorithmen bereit sind.

Die Modelle werden auf Grundlage ihrer Area Under the Curve (AUC) validiert, um sicherzustellen, dass jedes Modell das Verhalten der Besucher vorhersagen kann, bevor es in Ihrer Aktivität verwendet wird. Der genaue Zeitpunkt, zu dem ein Modell mit der Bereitstellung personalisierter Erlebnisse beginnt, hängt von den Details der Daten ab, da das Modell zuerst validiert werden muss. Für die praktische Traffic-Planung dauert es in der Regel mehr als die Mindestzahl an Konversionen, bis ein Modell funktionsfähig ist.

Wenn ein Modell für ein Erlebnis oder Angebot gültig wird, ändert sich das Uhrensymbol links neben dem Erlebnis- oder Angebotsnamen in ein grünes Kontrollkästchen. Wenn gültige Modelle für mindestens zwei Erlebnisse oder Angebote vorhanden sind, werden einige Besuche personalisiert.

### Funktionstransformation

Bevor die Daten durch den Personalisierungsalgorithmus geleitet werden, durchlaufen sie eine Funktionstransformation, bei der es sich um die Vorbereitung der in den Trainingsdatensätzen erfassten Daten handelt, damit diese von den Personalisierungsmodellen verwendet werden können. Die Transformation hängt vom Typ des Attributs ab (oder „Funktion“, wie Datenwissenschaftler es manchmal beschreiben):

| Merkmalstyp | Beschreibung | Schreibweise |
|---|---|---|
| **Kategorisch** | Kann nicht gezählt werden, kann aber in verschiedene Gruppen wie Land, Geschlecht oder Postleitzahl sortiert werden. | Ein Satz aller möglichen Funktionen wird beibehalten und die Wahrscheinlichkeitstransformation wird verwendet, um die Datengröße zu reduzieren. |
| **Nummerisch** | Kann gemessen oder gezählt werden, z. B. Alter oder Einkommen. | Durch die Neuskalierung wird sichergestellt, dass die Funktionen überall vergleichbar sind. |

### Ausgleich zwischen Lernen und Personalisierung mit dem mehrarmigen Banditen

Nachdem [!DNL Target] die Personalisierungsmodelle erstellt hat, sind Sie mit einem Nachteil für zukünftige Besucher Ihrer Aktivität konfrontiert. Sie können den gesamten Traffic basierend auf dem aktuellen Modell personalisieren oder Sie können weiterhin von neuen Besuchern lernen, indem Sie ihnen nach dem Zufallsprinzip zufällige Angebote unterbreiten. Der Personalisierungsalgorithmus sollte immer neue Trends bei Ihren Besuchern erkennen, während er den Großteil des Traffics personalisiert. Der mehrarmige Bandit ist, wie [!DNL Target] dieses Ziel erreicht: Er stellt sicher, dass das Modell immer einen kleinen Teil des Traffics „ausgibt“, um während des gesamten Lebens der Aktivität weiter zu lernen und eine Übernutzung der zuvor erlernten Trends zu verhindern.

In der Welt der Datenwissenschaft ist das Multi-Armed-Bandit-Problem ein klassisches Beispiel für das Dilemma zwischen Exploration und Exploitation, bei dem eine Sammlung einarmiger Banditen mit jeweils unbekannter Belohnungswahrscheinlichkeit vergeben wird. Der Grundgedanke ist, eine Strategie zu entwickeln, die dazu führt, dass der Arm mit der höchsten Erfolgswahrscheinlichkeit gespielt wird, damit die gesamte Belohnung maximiert wird. Der mehrarmige Bandit wird im System für die Online-Bewertung verwendet, nachdem die Online-Modelle erstellt wurden. Dieser Prozess hilft beim Online-Lernen während der Exploration. Der aktuelle mehrarmige Algorithmus ist ein epsilon () gieriger Algorithmus. In diesem Algorithmus wird mit Wahrscheinlichkeit 1 - der beste Arm gewählt. Mit der Wahrscheinlichkeit wird jeder andere Arm zufällig ausgewählt.
