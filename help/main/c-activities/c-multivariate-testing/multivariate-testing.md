---
keywords: Multivarianz-Test;MVT;Full Factorial;MVT oder A/B;Multivarianz-A/B;Traffic-Schätzung;Wann MVT zu verwenden ist;MVT-Überlegungen;Multivarianz;partiell-faktoriell;partiell-faktoriell;voll-faktoriell
description: Erfahren Sie, wie Sie einen [!UICONTROL Multivarianz-Test] (MVT) verwenden, [!DNL Adobe Target] Kombinationen von Angeboten in Elementen auf einer Seite zu vergleichen, um zu bestimmen, welche Kombination die besten Ergebnisse erzielt.
title: Was ist ein [!UICONTROL Multivarianz-]?
feature: Multivariate Tests
exl-id: c8b60011-cb3a-4e28-b84f-06910687b14b
TQID: 'https://experienceleague.adobe.com/JKmjIHJuRxAXlhvUOrrmLMVLnJFhA3T4xkahgH-ozHE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 25%
---
# Erste Schritte mit [!UICONTROL Multivarianz-Test] {#get-started-mvt}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie ein **[!UICONTROL Multivarianz-Test]** funktioniert, welche Begriffe [!DNL Target] verwendet, wann er anstelle von A/B-Tests verwendet wird und wie durch partiell-faktorielles Testen die Traffic-Anforderungen reduziert werden.

>[!ENDSHADEBOX]

Eine **[!UICONTROL Multivarianz-Test]**-Aktivität (MVT) in [!DNL Adobe Target] vergleicht Kombinationen von Angeboten in Elementen auf einer Seite, um festzustellen, welche Kombination für eine bestimmte Zielgruppe am besten funktioniert. Außerdem lässt sich so erkennen, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. Multivariate Tests helfen Ihnen dabei, den relativen Einfluss zu erkennen, den bestimmte Elemente im Vergleich zu anderen Elementen auf der Seite auf die Konversion haben, und können Ihnen dabei helfen, eine Kombination von Elementen zu verfeinern, die sich als effektiv erwiesen haben.

Ein **[!UICONTROL Multivarianz-Test]** bietet im Vergleich zu einem A/B-Test zwei Vorteile:

* Es zeigt an, welche Elemente auf Ihrer Seite den größten Einfluss auf die Konversion haben, was auch als „Haupteffekt“ bezeichnet wird. Diese Informationen sind beispielsweise nützlich, um zu bestimmen, wo die Inhalte platziert werden sollen, denen Sie die meiste Aufmerksamkeit schenken möchten.
* Auf diese Weise lassen sich zusammengesetzte Effekte zwischen zwei oder mehr Elementen auf einer Seite finden, was auch als „Interaktionseffekt“ bezeichnet wird. Zum Beispiel kann eine bestimmte Anzeige zu mehr Konversionen führen, wenn sie mit einem bestimmten Banner oder Heldenbild kombiniert wird.

[!DNL Target] verwendet vollständige Multivariater Tests, um Sie bei der Optimierung Ihres Inhalts zu unterstützen. Ein vollständiger Multivarianz-Test untersucht alle möglichen Inhaltskombinationen mit gleicher Wahrscheinlichkeit. Wenn Sie zum Beispiel über zwei Seitenelemente mit je drei Angeboten verfügen, entspricht dies neun möglichen Kombinationen (3 x 3). Drei Elemente, von denen zwei jeweils drei mögliche Angebote und eines zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2).

In [!DNL Target] ist jede Kombination ein Erlebnis. Der **[!UICONTROL Multivarianz-Test]** vergleicht jedes Erlebnis, damit Sie lernen können, welche Kombinationen am erfolgreichsten sind. Gleichzeitig erfasst und analysiert [!DNL Target] Daten, um zu verstehen, wie sich die einzelnen Standorte und Angebote auf die Erfolgsmetrik auswirken.

![Multivarianz-Testkombinationen](assets/multivariate.png)

Aufgrund der Anzahl der Kombinationen, die generiert werden können, benötigt ein **[!UICONTROL Multivarianz-Test]** mehr Zeit und Traffic als ein A/B-Test. Der auf der Seite eingehende Traffic muss ausreichend sein, um statistisch signifikante Ergebnisse für jedes Erlebnis zu erzielen. Um nützliche Ergebnisse zu erhalten, verstehen Sie den Traffic, den Ihre Seite erhält, und testen Sie die optimale Anzahl von Kombinationen für den richtigen Zeitraum.

Die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#traffic-estimator) kann Ihnen beim Entwerfen eines Tests helfen, der mit Ihrem Traffic funktioniert. Bevor Sie sie verwenden, sollten Sie über gute Statistiken verfügen, die die Anzahl der Impressionen und Konversionen zeigen, die Ihre Site normalerweise erhält, und Ihr Traffic-Niveau pro Tag berücksichtigen. Je mehr Erlebnisse eine Aktivität hat, desto mehr Traffic muss die Aktivität enthalten oder desto länger muss sie ausgeführt werden. Wenn Ihr Traffic nicht hoch ist, testen Sie einige Kombinationen. Andernfalls kann es sein, dass die Zeit, die zum Erzeugen aussagekräftiger Testergebnisse benötigt wird, zu lang ist, um nützlich zu sein.

## MVT-Terminologie {#mvt-terminology}

Mehrere Begriffe werden in der Branche auf unterschiedliche Weise verwendet. In der folgenden Tabelle werden die Begriffe definiert, die [!DNL Target] beim Einrichten eines Multivarianz-Tests verwenden.

| Begriff | Definition |
|--- |--- |
| Kombination | Die Inhaltsvarianten, die erstellt werden, wenn Sie verschiedene Inhaltsoptionen an verschiedenen Orten testen. Wenn Sie beispielsweise drei Standorte mit jeweils drei Inhaltsoptionen testen, gibt es 27 mögliche Kombinationen (3 x 3 x 3). Ein Besucher Ihrer Site sieht eine Kombination, die auch als Erlebnis bezeichnet wird. |
| Inhalt | Der Text oder das Bild, aus dem eine Testvarianz an einem Ort besteht. In einem Multivarianz-Test werden mehrere Inhaltsoptionen an mehreren Orten verglichen. Bei der MVT-Methode wird der Inhalt zuweilen als *Stufe* bezeichnet. |
| Element | Ein DOM-Element, das Inhaltsvarianten enthält, die im MVT-Test getestet werden sollen. Siehe auch *Ort*. |
| Standort | Ein spezifischer Inhaltsbereich auf einer Seite, der oftmals in einem einzelnen DOM-Element enthalten ist. Bei der MVT-Methode wird der Ort zuweilen als *Faktor* bezeichnet. Ein vollständiger Multivarianz-Test vergleicht alle möglichen Angebotskombinationen in Ihren Orten. |

## Verwendung von [!UICONTROL Multivarianz-Test] im Vergleich zu A/B {#when-to-use-mvt}

Die folgende Tabelle zeigt, wann ein **[!UICONTROL Multivarianz-Test]** ein A/B-Test oder beides zusammen zur Seitenoptimierung verwendet werden sollte.

| Situation | Vorgehensweise | Details |
|--- |--- |--- |
| Es stehen weniger als drei Elemente zum Testen zur Verfügung. | Führen Sie eine Reihe von A/B-Tests aus. | Verwenden Sie einen Multivarianz-Test, wenn Sie mindestens drei Elemente testen müssen. |
| Sie möchten sowohl das Layout als auch den Inhalt Ihrer Seite optimieren. | Verwenden Sie zur Optimierung Ihres Seiten-Layouts einen A/B-Test und anschließend einen MVT-Test, um den besten Inhalt für jedes Seitenelement zu ermitteln. | Ein A/B-Test kann wichtige Rückmeldungen zum Layout geben, und MVT-Tests eignen sich hervorragend zum Testen des Inhalts in den Elementen in Ihrem Seitendesign. Wenn Sie vor dem Testen mehrerer Inhaltsoptionen einen A/B-Test für das Layout durchführen, können Sie das beste Layout und den wirkungsvollsten Inhalt ermitteln. |
| Die Anzahl der verschiedenen Erlebnisse übersteigt fünf und umfasst zwei oder mehr Elemente. | Verwenden Sie einen Multivarianz-Test um zu ermitteln, welches Element am wichtigsten ist, und anschließend einen stärker fokussierten A/B-Test für dieses Element. | Der Multivarianz Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Elemente, auf die sich ein Marketingexperte konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf das wichtigste Element zur Erreichung Ihrer Ziele ist. Anschließend können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern, indem Sie beispielsweise zwei bestimmte Bilder gegeneinander testen oder den Wortlaut oder die Farben einer call to action vergleichen. Wenn Sie einem MVT-Test mit einem oder mehreren A/B-Tests folgen, können Sie den bestmöglichen Inhalt für die gewünschten Ergebnisse ermitteln. |

Weitere Überlegungen, z. B. wie viele Elemente einbezogen werden sollten und wie der Test geplant wird, finden Sie unter [Best Practices für Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/best-practices.md).

## Partiell-faktorielle Testung {#partial-factorial}

[!DNL Target] bietet vollfaktorielle Multivariater Tests als integrierte Aktivitätsoption. In der Statistik bietet „Design of Experiments“ viele Ansätze oder Designs, um zu bestimmen, welche Faktoren die Ergebnisse beeinflussen. Ein solcher Ansatz ist die [Taguchi-Methode](https://en.wikipedia.org/wiki/Taguchi_methods) für partiell-faktorielle Tests. Die Taguchi-Methode ermöglicht es Marketing-Experten, eine Reihe von Annahmen zu treffen, die die Anzahl der Permutationen von Erlebnissen reduzieren, die getestet werden müssen, was wiederum die Traffic-Anforderungen für einen Multivarianz-Test verringert. Sie können diesen Ansatz in [!DNL Target] anwenden, indem Sie diese [Offline-Tabelle](/help/main/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx) verwenden.

Wenn Ihr Team andere Ansätze für das Design von Experimenten verwendet, können Sie die Tabelle als Referenzimplementierung für benutzerdefinierte Experimentdesigns verwenden.

Bedenken Sie die folgenden Tipps bei der Verwendung der Offline-Berechnungstabelle:

* Wählen Sie die zu ändernden Elemente und die Anzahl der Versionen jedes Elements aus (3x2, 4x3 usw.).
* Seien Sie bei der Nummerierung konsequent. Wenn die Schaltfläche beispielsweise Element 1 ist und die Optionen blau, grün und gelb sind, ist die blaue Schaltfläche 1-1, die grüne Schaltfläche ist 1-2 und die gelbe Schaltfläche ist 1-3.
* Die Offline-Tabelle bietet die angemessene Anzahl benötigter Erfahrungen (vier für 3x2, neun für 4x3 usw.).
* Erstellen Sie die Erlebnisse im A/B-Workflow mit [Visual Experience Composer (VEC)](/help/main/c-experiences/experiences.md). Sie können benutzerdefinierten Code verwenden, HTML, WYSIWYG oder eine beliebige Kombination davon bearbeiten.
* Führen Sie nach Abschluss der Aktivität (basierend auf dem Stichprobengrößenrechner) die Ergebnisse durch die Tabelle aus, um die anderen Details zu erhalten.

## Schulungsvideos {#training-videos}

Die folgenden Videos enthalten weitere Informationen zu den auf dieser Seite besprochenen Konzepten.

### Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Übersichtsvideo werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. Multivarianz-Tests werden ab 4:20 erklärt. In diesem Video erfahren Sie, wie Sie:

* Beschreiben Sie die in [!DNL Adobe Target] enthaltenen Aktivitätstypen.
* Wählen Sie den entsprechenden Aktivitätstyp aus, um Ihre Ziele zu erreichen.
* Beschreiben Sie den angeleiteten dreistufigen Workflow, der für alle Aktivitätstypen gilt.

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird erläutert, wie Sie einen Multivarianz-Test mithilfe des [!DNL Target] dreistufigen Workflows verstehen, planen und erstellen. In diesem Video erfahren Sie, wie Sie:

* Definieren und Entwerfen eines Multivarianz-Tests
* Erstellen Sie einen Multivarianz-Test.

>[!VIDEO](https://video.tv.adobe.com/v/17395)
