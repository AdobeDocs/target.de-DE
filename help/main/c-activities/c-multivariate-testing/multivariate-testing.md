---
keywords: Multivarianz-Test;MVT;Vollfaktoriell;MVT oder A/B;Multivarianz A/B;Traffic-Schätzung;wann MVT verwendet werden sollte;MVT-Überlegungen;Multivarianz;Teilfaktoriell;Teil-Faktorium;Vollfaktoriell
description: Erfahren Sie, wie Sie eine [!UICONTROL Multivarianz-Test] (MVT) in [!DNL Adobe Target] um Angebotskombinationen in Elementen auf einer Seite zu vergleichen, um zu bestimmen, welche Kombination die beste Leistung erzielt.
title: Was ist ein [!UICONTROL Multivarianz-Test]?
feature: Multivariate Tests
exl-id: c8b60011-cb3a-4e28-b84f-06910687b14b
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '1452'
ht-degree: 49%

---

# [!UICONTROL Multivarianz-Tests – Überblick]

A [!UICONTROL Multivarianz-Test] (MVT)-Aktivität in [!DNL Adobe Target] Vergleicht Kombinationen von Angeboten in Elementen auf einer Seite, um zu bestimmen, welche Kombination für eine bestimmte Zielgruppe die beste Leistung erzielt. A [!UICONTROL Multivarianz-Test] -Aktivität hilft auch dabei herauszufinden, welches Element den größten Einfluss auf den Erfolg der Aktivität hat.

Multivarianz-Tests helfen Ihnen dabei, den relativen Einfluss bestimmter Elemente auf die Konversion im Vergleich zu anderen Elementen auf der Seite zu ermitteln. Multivarianz-Tests können Ihnen auch dabei helfen, eine Kombination von Elementen zu verfeinern, die sich als effektiv erwiesen haben.

Ein Vorteil: [!UICONTROL Multivarianz-Test] bietet im Vergleich zu einem A/B-Test die Möglichkeit, anzuzeigen, welche Elemente auf Ihrer Seite den größten Einfluss auf die Konversion haben. Dieser Vorteil wird auch als &quot;Haupteffekt&quot;bezeichnet. Diese Informationen sind beispielsweise hilfreich, um zu bestimmen, wo Inhalte platziert werden sollen, die die meiste Aufmerksamkeit erhalten sollen.

[!UICONTROL Multivarianz-Test] -Aktivitäten helfen Ihnen auch dabei, zusammengesetzte Effekte zwischen zwei oder mehr Elementen auf einer Seite zu finden. Zum Beispiel kann eine bestimmte Anzeige zu mehr Konversionen führen, wenn sie mit einem bestimmten Banner oder Heldenbild kombiniert wird. Dies wird auch als „Interaktionseffekt“ bezeichnet.

[!DNL Target] verwendet vollständige Multivariater Tests, um Sie bei der Optimierung Ihres Inhalts zu unterstützen. Ein vollständiger Multivariater Test untersucht alle möglichen Inhaltskombinationen mit gleicher Wahrscheinlichkeit. Wenn Sie zum Beispiel über zwei Seitenelemente mit je drei Angeboten verfügen, entspricht dies neun möglichen Kombinationen (3 x 3). Drei Elemente, von denen zwei jeweils drei mögliche Angebote und eines zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2).

In [!DNL Target], ist jede Kombination ein Erlebnis. Die [!UICONTROL Multivarianz-Test] vergleicht die einzelnen Erlebnisse, sodass Sie erfahren, welche Kombinationen am erfolgreichsten sind. Daten werden gleichzeitig erfasst und analysiert, um zu verstehen, wie die Erfolgsmetrik durch die einzelnen Orte und Angebote beeinflusst wird.

![Multivarianz-Bild](assets/multivariate.png)

Aufgrund der Anzahl der Kombinationen, die generiert werden können, wird ein [!UICONTROL Multivarianz-Test] erfordert mehr Zeit und mehr Traffic als ein A/B-Test. Der auf der Seite eingehende Traffic muss ausreichend sein, um statistisch signifikante Ergebnisse für jedes Erlebnis zu erzielen. Um nützliche Ergebnisse zu erhalten, müssen Sie wissen, wie viel Traffic auf Ihrer Seite anfällt, und die optimale Anzahl von Kombinationen für die richtige Zeitdauer testen, um die erforderlichen Ergebnisse zu erhalten.

Die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) kann Ihnen dabei helfen, einen Test zu entwerfen, der mit Ihrem Traffic funktioniert. Bevor Sie die Traffic-Schätzung verwenden, müssen Sie über gute Statistiken verfügen, aus denen die Anzahl der Impressionen und Konversionen hervorgeht, die Ihre Seite normalerweise erhält. Berücksichtigen Sie Ihr tägliches Traffic-Niveau. Je mehr Erlebnisse in einer Aktivität enthalten, desto mehr Traffic muss die Aktivität enthalten oder desto länger muss Ihre Aktivität ausgeführt werden. Wenn Ihr Traffic-Aufkommen nicht hoch ist, sollten Sie einige Kombinationen testen. Andernfalls kann es zu lange dauern, bis Sie aussagekräftige Testergebnisse erzielen.

## MVT-Terminologie {#section_DF475CA7F34B4CFDB7BE7363761D64AE}

Das Verständnis grundlegender Begriffe kann für die Einrichtung eines Multivariater Tests hilfreich sein.

Es gibt verschiedene Begriffe, die branchenweit unterschiedlich verwendet werden. In diesem Abschnitt werden die von [!DNL Target] verwendeten Begriffe definiert.

**Kombination:** Die Inhaltsvarianten, die erstellt werden, wenn Sie verschiedene Inhaltsoptionen an verschiedenen Orten testen. Wenn Sie zum Beispiel drei Orte mit jeweils drei Inhaltsoptionen testen, ergeben sich 27 mögliche Kombinationen (3 x 3 x 3). Ein Besucher Ihrer Site sieht eine Kombination, die auch als Erlebnis bezeichnet wird.

**Inhalt:** Text oder Bild, der/das eine Testvariation an einem Ort darstellt. In einem Multivarianz-Test werden mehrere Inhaltsoptionen an verschiedenen Orten verglichen. Bei der MVT-Methode wird der Inhalt zuweilen als *Stufe* bezeichnet.

**Element:** Ein DOM-Element, das Inhaltsvarianten enthält, die im Rahmen eines Multivarianz-Tests getestet werden sollen. Siehe auch *Ort*.

**Ort:** Ein spezifischer Inhaltsbereich auf einer Seite, der oftmals in einem einzelnen DOM-Element enthalten ist. Bei der MVT-Methode wird der Ort zuweilen als *Faktor* bezeichnet. Ein vollständiger Multivarianz-Test vergleicht alle möglichen Angebotskombinationen in Ihren Orten.

## Verwendungsbereiche [!UICONTROL Multivarianz-Test] vs. A/B {#section_3D2B966B6671406C861A1843EA41D28C}

Multivarianz-Tests können gemeinsam mit A/B-Tests zur Optimierung Ihrer Seite verwendet werden. Die gemeinsame Verwendung dieser Tests wird zum Beispiel in folgenden Fällen empfohlen:

* Verwenden Sie einen A/B-Test, um Ihr Seitenlayout zu optimieren, und anschließend einen Multivarianz-Test, um die jeweils besten Inhalte für die einzelnen Elemente auf der Seite festzulegen..

  Ein A/B-Test ermöglicht wichtige Aussagen zum Layout und Multivarianz-Tests eignen sich hervorragend, um Inhalte in den Elementen Ihres Seitenentwurfs zu testen. Die Durchführung eines A/B-Tests am Layout vor dem Testen mehrerer Inhaltsoptionen kann Ihnen dabei helfen, das beste Layout und den wirkungsvollsten Inhalt zu bestimmen.

* Verwenden Sie einen Multivarianz-Test um zu ermitteln, welches Element am wichtigsten ist, und anschließend einen stärker fokussierten A/B-Test für dieses Element.

  Bei mehr als fünf verschiedenen Erlebnissen mit zwei oder mehr Elementen ist ein Multivarianz-Test empfehlenswert, bevor Sie Ihre A/B-Tests durchführen. Der Multivarianz Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Elemente, auf die sich ein Marketingexperte konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf das wichtigste Element zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Elemente und Inhalte am nützlichsten sind, um Sie bei der Erreichung Ihrer Ziele zu unterstützen, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. Sie können beispielsweise zwei spezifische Bilder gegeneinander testen oder den Wortlaut oder die Farben eines Aktionsaufrufs vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Zu beachten   {#section_979FE3F398654C1EA1C86E7DBC9A8DAD}

* Verwenden Sie einen Multivarianz-Test, wenn Sie mindestens drei Elemente testen müssen. Wenn Sie weniger haben, starten Sie eine Reihe von  A/B-Tests.
* Wählen Sie die Seitenelemente aus, die Ihrer Meinung nach den größten Einfluss auf die Ergebnisse haben.
* Vermeiden Sie die Einbeziehung zu vieler Elemente oder Orte in einen Test. Je größer die Zahl, desto länger die Testdauer.
* Planen Sie den Testentwurf im Voraus. Bearbeiten Sie einen Test nicht, nachdem er live geschaltet wurde und Daten erfasst und analysiert werden.
* Elemente sollten unabhängig voneinander sein.

  Testen Sie z. B. Ihr Layout und Ihren Inhalt nicht im selben Test.

* Planen Sie in Anbetracht der gestiegenen Anzahl der Erlebnisse zusätzliche Zeit für die Qualitätssicherung ein. Sie können auch teilfaktorielle Tests verwenden, um den für einen Multivarianz-Test benötigten Traffic zu reduzieren. Weitere Informationen finden Sie unten unter Teilfaktorielle Tests:

## Teilfaktorielle Tests

[!DNL Target] bietet vollfaktorielle Multivariater Tests als integrierte Aktivitätsoption. In Statistiken bietet &quot;Design of Experiments&quot;viele Ansätze oder Entwürfe, um zu bestimmen, welche Faktoren die Ergebnisse beeinflussen. Ein solcher Ansatz ist die [Taguchi-Methode](https://en.wikipedia.org/wiki/Taguchi_methods) für Tests mit Teilfaktoren. Mit Taguchi können Marketingexperten eine Reihe von Annahmen treffen, die die Anzahl der Permutationen von Erlebnissen reduzieren, die getestet werden müssen, und wiederum die Traffic-Anforderungen für einen Multivarianz-Test reduzieren. Diese Funktionalität und dieser Testansatz können in [!DNL Target] mithilfe dieses [Offline-Tabelle](/help/main/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx).

Wenn Ihr Team andere Design of Experiments-Ansätze verwendet, können Sie diese Berechnungstabelle als Referenz-Implementierung für benutzerdefinierte Experiment-Designs verwenden.

Bedenken Sie die folgenden Tipps bei der Verwendung der Offline-Berechnungstabelle:

* Wählen Sie die Elemente aus, die Sie ändern möchten, sowie die Anzahl der Versionen der einzelnen Elemente (3 x 2, 4 x 3 usw.).
* Seien Sie bei der Nummerierung konsequent. Wenn die Schaltfläche beispielsweise Element 1 ist und die Optionen blau, grün und gelb sind, ist die blaue Schaltfläche 1-1, die grüne Schaltfläche ist 1-2 und die gelbe Schaltfläche ist 1-3.
* Die Offline-Tabelle bietet die angemessene Anzahl benötigter Erfahrungen (vier für 3x2, neun für 4x3 usw.).
* Erstellen Sie die Erlebnisse im A/B-Workflow mit [Visual Experience Composer (VEC)](/help/main/c-experiences/experiences.md). Sie können benutzerdefinierten Code verwenden, HTML, WYSIWYG oder eine beliebige Kombination davon bearbeiten.
* Nachdem die Aktivität beendet ist (basierend auf dem Stichprobengrößenrechner), führen Sie die Ergebnisse über die Tabelle aus, um die anderen Details zu erhalten.

Weitere Informationen und Best Practices finden Sie unter [Best Practices für Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/best-practices.md#reference_53635817FFB741EF8C4E56CC70688EDD).

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Übersichtsvideo werden die in verfügbaren Aktivitätstypen erläutert. [!DNL Target]. Multivariate Tests werden ab 4:20 erklärt.

* Beschreiben Sie die Arten von Aktivitäten, die Teil von [!DNL Adobe Target] sind
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird erläutert, wie Sie einen Multivarianz-Test mithilfe der [!DNL]Geführter dreistufiger Arbeitsablauf für Target.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395)
