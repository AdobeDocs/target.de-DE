---
keywords: a/b;a/a;aa;
description: Erfahren Sie, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen sollten und wie die Ergebnisse interpretiert werden.
title: Was sind A/A-Tests?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
source-git-commit: 4f0ebdd06287a438e519d9bccb677ab1a9093396
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 1%

---

# A/A-Tests

Bevor Sie mit [!DNL Adobe Target] einen A/A-Test auf Ihrer Site durchführen, müssen Sie wissen, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen sollten und wie die Ergebnisse interpretiert werden.

## Was sind A/A-Tests?

Bevor wir A/A-Tests erläutern, sollten wir die A/B-Tests noch einmal durchgehen, damit wir die Unterschiede besprechen können.

Bei einem standardmäßigen A/B-Test wird der Traffic zwei oder mehr unterschiedlichen Erlebnissen zugeordnet. Ein Erlebnis ist in der Regel das „Kontrollerlebnis“, und Varianten des Erlebnisses werden im Vergleich zum Kontrollerlebnis getestet, um zu sehen, welches Erlebnis in einer bestimmten Metrik den meisten Anstieg erzeugt.

A/A-Tests beinhalten jedoch die Zuordnung von Traffic zu zwei identischen Erlebnissen, normalerweise mit einer Aufteilung der Traffic-Zuordnung von 50/50. Mit einem standardmäßigen A/B-Test möchten Sie in der Regel eine Steigerung der Konversionsrate feststellen. Dies unterscheidet sich von einem A/A-Test, bei dem Ihr Ziel normalerweise darin besteht, festzustellen, *es* Unterschied in der Steigerung zwischen den identischen Erlebnissen gibt.

## Warum sollten Sie zwei identische Erlebnisse testen wollen und was bewirkt dies?

Einige Unternehmen führen A/A-Tests durch, wenn sie ein neues Test-Tool wie [!DNL Target] implementieren, um festzustellen, ob:

* Die Aktivität wurde korrekt eingerichtet
* Der Code wurde korrekt implementiert
* Das Reporting ist korrekt

Obwohl nur wenige Unternehmen A/A-Tests durchführen, empfiehlt es sich, diese als „Vernunftexperimente“ durchzuführen, um Vertrauen zu schaffen, nachdem das Tool implementiert wurde oder bevor A/B-Tests durchgeführt wurden, die sich auf Konversionen und Umsätze auswirken könnten.

## Warum wird für ein Erlebnis möglicherweise ein Lift angezeigt, wenn die Erlebnisse identisch sind?

Es gibt zahlreiche Gründe, warum Sie möglicherweise eine Steigerung in einem Erlebnis gegenüber einem anderen (identischen) Erlebnis sehen:

### Der A/A-Test wurde kontinuierlich überwacht

Ein häufiges Problem bei der Durchführung von Tests jeglicher Art, einschließlich A/A-Tests, besteht darin, die Ergebnisse kontinuierlich zu betrachten und einen Test vorzeitig zu stoppen, wenn Sie statistische Signifikanz sehen, und ein erfolgreichstes Erlebnis zu erklären. Analysten machen oft das, was als „Data Peeking“ bezeichnet wird. Beim Data Peeking werden die Testdaten früh und häufig betrachtet, während versucht wird festzustellen, welches Erlebnis eine bessere Leistung erzielt. Das Risiko besteht darin, den Test vorzeitig abzubrechen, wodurch die Ergebnisse ungültig werden könnten.

Bei einem A/A-Test kann Data Peeking dazu führen, dass Analysten eine Steigerung in einem Erlebnis sehen, obwohl es eigentlich keinen Unterschied geben sollte, da die beiden Erlebnisse identisch sind. Tatsächlich zeigen A/A-Tests mit kontinuierlichem Peeking *garantiert* irgendwann während des Tests „statistische Signifikanz“ (d. h. eine Konfidenz oberhalb eines bestimmten Schwellenwerts, z. B. 95 %).

Um dies zu vermeiden, sollten Sie daher wie bei einem regulären A/B-Test vorab entscheiden, welche Stichprobengröße verwendet werden soll, basierend auf der minimalen Effektgröße (der minimalen Steigerung, unterhalb derer ein Effekt für Ihr Unternehmen nicht wichtig ist), der Leistung und dem Signifikanzniveau, das Sie akzeptabel finden.

Bei einem A/A-Test wäre das Ziel dann, *nicht* ein statistisch signifikantes Ergebnis zu sehen, nachdem Ihr Test die gewünschte Stichprobengröße erreicht hat.

Die [!UICONTROL Adobe Target Sample Size Calculator] ist ein wichtiges Tool, mit dem Sie bestimmen können, auf welche Stichprobengröße Sie abzielen sollten und wie lange Sie den Test ausführen sollten.

* [Adobe Target-Größenberechnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Darüber hinaus finden Sie in den folgenden Artikeln Informationen darüber, wie lange Sie eine Aktivität ausführen sollten, sowie weitere hilfreiche Tipps und Tricks:

* [Wie lange sollten A/B-Tests laufen?](/help/main/c-activities/t-test-ab/sample-size-determination.md)
* [Zehn häufige A/B-Fehler und wie diese vermieden werden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### Statistische Signifikanz wirkt sich auf Testergebnisse aus

Das Signifikanzniveau eines Tests bestimmt, wie wahrscheinlich es ist, dass der Test einen signifikanten Unterschied bei den Konversionsraten zwischen zwei verschiedenen Angeboten meldet, obwohl es tatsächlich keinen echten Unterschied gibt. Dies wird als falsch positiv oder als Fehler vom Typ I bezeichnet. Das Signifikanzniveau ist ein vom Benutzer festgelegter Schwellenwert, und es besteht ein Kompromiss zwischen der Toleranz für falsch positive Ergebnisse und der Anzahl der Besucher, die in den Test einbezogen werden müssen, um das richtige Signifikanzniveau auszuwählen.

Ein häufig verwendetes Signifikanzniveau in A/A- und A/B-Tests beträgt 5 %, was einem Konfidenzniveau von 95 % entspricht (Konfidenzniveau = 100 % - Signifikanzniveau). Ein Konfidenzniveau von 95 % bedeutet, dass bei jeder Durchführung eines Tests eine Wahrscheinlichkeit von 5 % besteht, eine statistisch signifikante Steigerung zu erkennen, auch wenn es keinen Unterschied zwischen den Erlebnissen gibt.

Angenommen, Sie möchten mit Ihrem A/A-Test ein Konfidenzniveau von 95 % erreichen. Mit einem Konfidenzniveau von 95 % konnte 1 von 20 A/A-Tests eine statistisch signifikante Steigerung der Konversionen zeigen. Bei einem Konfidenzniveau von 90 % kann jeder 10. Test beim Testen identischer Erlebnisse eine Steigerung der Konversionen zeigen.

## Best Practice

Wenn Sie sich entscheiden, dass in Ihrer Organisation ein A/A-Test erforderlich ist, beachten Sie, dass die identischen Erlebnisse möglicherweise vorübergehend einen Unterschied zur Kontrolle aufweisen. Dies kann normal sein, je nachdem, wie lange der Test ausgeführt werden darf. Der Unterschied sollte sich verringern, wenn mehr Zeit und Besucher zur Verfügung stehen.

Best Practice ist die Verwendung der regulären A/B-Testmethode: Bestimmen Sie die Stichprobengröße im Voraus auf der Grundlage einer minimalen relevanten Effektgröße, der gewünschten Leistung und der Signifikanz mithilfe des [Adobe Target-Größenrechners](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

Warten Sie dann ausreichend Zeit und Besuchende, bevor Sie zu einem Ergebnis kommen, und denken Sie daran, dass je nach Signifikanzniveau Ihres Tests die Möglichkeit besteht, dass ein Erlebnis einen Unterschied in der Steigerung zeigt und sogar zum Gewinner erklärt wird.
