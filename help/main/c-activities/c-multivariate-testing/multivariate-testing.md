---
keywords: Multivarianz-Test;MVT;Full Factorial;MVT oder A/B;Multivarianz-A/B;Traffic-Schätzung;Wann MVT zu verwenden ist;MVT-Überlegungen;Multivarianz;partiell-faktoriell;partiell-faktoriell;voll-faktoriell
description: Erfahren Sie, wie Sie mit einem [!UICONTROL Multivariate Test] (MVT) in  [!DNL Adobe Target] , um Kombinationen von Angeboten in Elementen auf einer Seite zu vergleichen und so zu bestimmen, welche Kombination die besten Ergebnisse erzielt.
title: Was ist ein [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: c8b60011-cb3a-4e28-b84f-06910687b14b
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 47%

---

# [!UICONTROL Multivariate Test]

Eine [!UICONTROL Multivariate Test] (MVT) -Aktivität in [!DNL Adobe Target] vergleicht Kombinationen von Angeboten in Elementen auf einer Seite, um festzustellen, welche Kombination für eine bestimmte Zielgruppe am besten funktioniert. Eine [!UICONTROL Multivariate Test] Aktivität hilft auch dabei zu ermitteln, welches Element den größten Einfluss auf den Erfolg der Aktivität hat.

Mithilfe von Multivarianz-Tests können Sie den relativen Einfluss bestimmter Elemente auf die Konversion im Vergleich zu anderen Elementen auf der Seite ermitteln. Multivariate Tests können auch dazu beitragen, eine Kombination von Elementen zu verfeinern, die sich als wirksam erwiesen haben.

Ein Vorteil eines [!UICONTROL Multivariate Test] im Vergleich zu einem A/B-Test besteht darin, dass angezeigt werden kann, welche Elemente auf der Seite den größten Einfluss auf die Konversion haben. Dieser Vorteil wird auch als „Haupteffekt“ bezeichnet. Diese Informationen sind beispielsweise nützlich, um zu bestimmen, wo Inhalte platziert werden sollen, denen Sie die meiste Aufmerksamkeit schenken möchten.

[!UICONTROL Multivariate Test] Aktivitäten helfen Ihnen auch, zusammengesetzte Effekte zwischen zwei oder mehr Elementen auf einer Seite zu finden. Zum Beispiel kann eine bestimmte Anzeige zu mehr Konversionen führen, wenn sie mit einem bestimmten Banner oder Heldenbild kombiniert wird. Dies wird auch als „Interaktionseffekt“ bezeichnet.

[!DNL Target] verwendet vollständige Multivariater Tests, um Sie bei der Optimierung Ihres Inhalts zu unterstützen. Ein vollständiger Multivarianz-Test untersucht alle möglichen Inhaltskombinationen mit gleicher Wahrscheinlichkeit. Wenn Sie zum Beispiel über zwei Seitenelemente mit je drei Angeboten verfügen, entspricht dies neun möglichen Kombinationen (3 x 3). Drei Elemente, von denen zwei jeweils drei mögliche Angebote und eines zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2).

In [!DNL Target] ist jede Kombination ein Erlebnis. Die [!UICONTROL Multivariate Test] vergleicht jedes Erlebnis, damit Sie erfahren können, welche Kombinationen am erfolgreichsten sind. Daten werden gleichzeitig erfasst und analysiert, um zu verstehen, wie die Erfolgsmetrik durch die einzelnen Orte und Angebote beeinflusst wird.

![Multivarianz-Bild](assets/multivariate.png)

Aufgrund der Anzahl der Kombinationen, die generiert werden können, benötigt ein [!UICONTROL Multivariate Test] mehr Zeit und Traffic als ein A/B-Test. Der auf der Seite eingehende Traffic muss ausreichend sein, um statistisch signifikante Ergebnisse für jedes Erlebnis zu erzielen. Um nützliche Ergebnisse zu erhalten, müssen Sie den Traffic verstehen, den Ihre Seite erhält, und die optimale Anzahl von Kombinationen für die richtige Zeitdauer testen, um die erforderlichen Ergebnisse zu erhalten.

Die Traffic[Schätzung des Ziels ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) Ihnen beim Entwurf eines Tests helfen, der mit Ihrem Traffic funktioniert. Bevor Sie die Traffic-Schätzung verwenden, müssen Sie über gute Statistiken verfügen, aus denen die Anzahl der Impressionen und Konversionen hervorgeht, die Ihre Seite normalerweise erhält. Berücksichtigen Sie Ihr tägliches Traffic-Niveau. Je mehr Erlebnisse eine Aktivität enthält, desto mehr Traffic muss die Aktivität enthalten oder desto länger muss Ihre Aktivität ausgeführt werden. Wenn Ihr Traffic nicht hoch ist, sollten Sie einige Kombinationen testen. Andernfalls kann es zu lange dauern, bis aussagekräftige Testergebnisse vorliegen, die nicht nützlich sind.

## MVT-Terminologie {#section_DF475CA7F34B4CFDB7BE7363761D64AE}

Das Verständnis grundlegender Begriffe kann für die Einrichtung eines Multivariater Tests hilfreich sein.

Es gibt verschiedene Begriffe, die branchenweit unterschiedlich verwendet werden. In diesem Abschnitt werden die von [!DNL Target] verwendeten Begriffe definiert.

**Kombination:** Die Inhaltsvarianten, die erstellt werden, wenn Sie verschiedene Inhaltsoptionen an verschiedenen Orten testen. Wenn Sie zum Beispiel drei Orte mit jeweils drei Inhaltsoptionen testen, ergeben sich 27 mögliche Kombinationen (3 x 3 x 3). Ein Besucher Ihrer Site sieht eine Kombination, die auch als Erlebnis bezeichnet wird.

**Inhalt:** Text oder Bild, der/das eine Testvariation an einem Ort darstellt. In einem Multivarianz-Test werden mehrere Inhaltsoptionen an mehreren Orten verglichen. Bei der MVT-Methode wird der Inhalt zuweilen als *Stufe* bezeichnet.

**Element:** Ein DOM-Element, das Inhaltsvarianten enthält, die im Rahmen eines Multivarianz-Tests getestet werden sollen. Siehe auch *Ort*.

**Ort:** Ein spezifischer Inhaltsbereich auf einer Seite, der oftmals in einem einzelnen DOM-Element enthalten ist. Bei der MVT-Methode wird der Ort zuweilen als *Faktor* bezeichnet. Ein vollständiger Multivarianz-Test vergleicht alle möglichen Angebotskombinationen in Ihren Orten.

## Verwendung von [!UICONTROL Multivariate Test] im Vergleich zu A/B {#section_3D2B966B6671406C861A1843EA41D28C}

Multivarianz-Tests können gemeinsam mit A/B-Tests zur Optimierung Ihrer Seite verwendet werden. Die gemeinsame Verwendung dieser Tests wird zum Beispiel in folgenden Fällen empfohlen:

* Verwenden Sie zur Optimierung Ihres Seiten-Layouts einen A/B-Test und anschließend einen MVT-Test, um den besten Inhalt für jedes Seitenelement zu ermitteln.

  Ein A/B-Test ermöglicht wichtige Aussagen zum Layout und Multivarianz-Tests eignen sich hervorragend, um Inhalte in den Elementen Ihres Seitenentwurfs zu testen. Das Ausführen eines A/B-Tests für das Layout vor dem Testen mehrerer Inhaltsoptionen kann Ihnen dabei helfen, das beste Layout und die wirkungsvollsten Inhalte zu ermitteln.

* Verwenden Sie einen Multivarianz-Test um zu ermitteln, welches Element am wichtigsten ist, und anschließend einen stärker fokussierten A/B-Test für dieses Element.

  Wenn mehr als fünf Erlebnisse vorhanden sind und sich über zwei oder mehr Elemente erstrecken, empfiehlt es sich, einen MVT-Test in Betracht zu ziehen, bevor Sie Ihre A/B-Tests durchführen. Der Multivarianz Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Elemente, auf die sich ein Marketingexperte konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf das wichtigste Element zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Elemente und Inhalte für Ihr Erreichen der Ziele am nützlichsten sind, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. Sie können beispielsweise zwei bestimmte Bilder gegeneinander testen oder den Wortlaut oder die Farben eines Aktionsaufrufs vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Zu beachten   {#section_979FE3F398654C1EA1C86E7DBC9A8DAD}

* Verwenden Sie einen Multivarianz-Test, wenn Sie mindestens drei Elemente testen müssen. Wenn die Anzahl der Elemente niedriger ist, führen Sie eine Reihe von A/B-Tests durch.
* Wählen Sie die Seitenelemente aus, von denen Sie glauben, dass sie den größten Einfluss auf die Ergebnisse haben.
* Vermeiden Sie die Einbeziehung zu vieler Elemente oder Orte in einen Test. Je größer die Zahl, desto länger die Testdauer.
* Planen Sie den Testentwurf im Voraus. Bearbeiten Sie keinen Test, nachdem er live geschaltet wurde und Daten erfasst und analysiert werden.
* Elemente sollten voneinander unabhängig sein.

  Testen Sie z. B. Ihr Layout und Ihren Inhalt nicht im selben Test.

* Planen Sie zusätzliche Zeit für die QS ein, da die Anzahl der Erlebnisse steigt. Sie können auch partielle faktorielle Tests verwenden, um den für einen Multivarianz-Test erforderlichen Traffic zu reduzieren. Weitere Informationen finden Sie unten unter Partiell-faktorielle Tests:

## Partiell-faktorielle Testung

[!DNL Target] bietet vollfaktorielle Multivariater Tests als integrierte Aktivitätsoption. In Statistiken:
„Design von Experimenten“ bietet viele Ansätze oder Designs, um zu bestimmen, welche Faktoren die Ergebnisse beeinflussen. Ein solcher Ansatz ist die [Taguchi-Methode](https://en.wikipedia.org/wiki/Taguchi_methods) für partiell-faktorielle Tests. Taguchi ermöglicht es Marketing-Experten, eine Reihe von Annahmen zu treffen, die die Anzahl der Permutationen von Erlebnissen reduzieren, die getestet werden müssen, und reduziert somit die Traffic-Anforderungen für einen Multivarianz-Test. Dieser Funktions- und Testansatz kann in [!DNL Target] mithilfe dieser [Offline-Tabelle“ angewendet ](/help/main/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx).

Wenn Ihr Team andere Design of Experiments-Ansätze verwendet, können Sie diese Berechnungstabelle als Referenz-Implementierung für benutzerdefinierte Experiment-Designs verwenden.

Bedenken Sie die folgenden Tipps bei der Verwendung der Offline-Berechnungstabelle:

* Wählen Sie die zu ändernden Elemente und die Anzahl der Versionen jedes Elements aus (3x2, 4x3 usw.).
* Seien Sie bei der Nummerierung konsequent. Wenn die Schaltfläche beispielsweise Element 1 ist und die Optionen blau, grün und gelb sind, ist die blaue Schaltfläche 1-1, die grüne Schaltfläche ist 1-2 und die gelbe Schaltfläche ist 1-3.
* Die Offline-Tabelle bietet die angemessene Anzahl benötigter Erfahrungen (vier für 3x2, neun für 4x3 usw.).
* Erstellen Sie die Erlebnisse im A/B-Workflow mit [Visual Experience Composer (VEC)](/help/main/c-experiences/experiences.md). Sie können benutzerdefinierten Code verwenden, HTML, WYSIWYG oder eine beliebige Kombination davon bearbeiten.
* Führen Sie nach Abschluss der Aktivität (basierend auf dem Stichprobengrößenrechner) die Ergebnisse durch die Tabelle aus, um die anderen Details zu erhalten.

Weitere Informationen und Best Practices finden Sie unter [Best Practices für Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/best-practices.md#reference_53635817FFB741EF8C4E56CC70688EDD).

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Übersichtsvideo werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. Multivariate Tests werden ab 4:20 erklärt.

* Beschreiben Sie die Arten von Aktivitäten, die Teil von [!DNL Adobe Target] sind
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/29397?captions=ger)

### Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird erläutert, wie Sie einen Multivarianz-Test mithilfe des dreistufigen Workflows Target“ verstehen, planen und erstellen.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/30168?captions=ger)
