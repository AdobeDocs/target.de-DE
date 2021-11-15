---
keywords: a/b;a/a;aa;
description: Erfahren Sie, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen sollten und wie die Ergebnisse interpretiert werden.
title: Was ist A/A-Tests?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
source-git-commit: 4e3a94554dd9c1e8cc6e98eda10d454536bc9b1f
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 1%

---

# A/A-Tests

Vor dem Durchführen eines A/A-Tests auf Ihrer Site mit [!DNL Adobe Target]ist es wichtig zu verstehen, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen sollten und wie die Ergebnisse interpretiert werden.

## Was sind A/A-Tests?

Bevor Sie A/A-Tests erläutern, sollten Sie A/B-Tests überprüfen, damit wir dann die Unterschiede besprechen können.

In einem standardmäßigen A/B-Test wird Traffic zwei oder mehr verschiedenen Erlebnissen zugeordnet. Ein Erlebnis ist in der Regel die &quot;Kontrolle&quot;und Varianten des Erlebnisses werden mit dem Kontrollelement getestet, um zu sehen, welches Erlebnis die höchste Steigerung in einer bestimmten Metrik erzielt.

A/A-Tests beinhalten jedoch die Zuordnung von Traffic zu zwei identischen Erlebnissen, normalerweise mit einer Traffic-Zuordnung von 50/50. Mit einem standardmäßigen A/B-Test möchten Sie in der Regel eine Steigerung der Konversion ermitteln. Dies unterscheidet sich von einem A/A-Test, bei dem Ihr Ziel normalerweise darin besteht, festzustellen, ob *no* Unterschiede bei der Steigerung zwischen den identischen Erlebnissen.

## Warum sollten Sie zwei identische Erlebnisse testen und was bewirkt dies?

Einige Unternehmen führen A/A-Tests durch, wenn sie ein neues Testwerkzeug implementieren, z. B. [!DNL Target], um festzustellen, ob:

* Die Aktivität wurde korrekt eingerichtet
* Der Code wurde korrekt implementiert
* Die Berichterstellung ist korrekt

Obwohl nur wenige Unternehmen A/A-Tests durchführen, empfiehlt es sich, diese als &quot;vernünftige&quot;Experimente durchzuführen, um nach der Implementierung des Tools oder vor der Durchführung von A/B-Tests Vertrauen zu schaffen, was sich auf die Konversion und den Umsatz auswirken könnte.

## Warum können Sie die Steigerung für ein Erlebnis sehen, wenn die Erlebnisse identisch sind?

Es gibt zahlreiche Gründe, warum Sie möglicherweise eine Steigerung in einem Erlebnis gegenüber einem anderen (identischen) Erlebnis sehen:

### Der A/A-Test wurde kontinuierlich überwacht

Ein häufig auftretendes Problem bei der Durchführung jeglicher Art von Tests, einschließlich A/A-Tests, besteht darin, die Ergebnisse kontinuierlich zu betrachten und einen Test frühzeitig anzuhalten, sobald Sie die statistische Bedeutung erkennen, und ein erfolgreiches Erlebnis zu deklarieren. Analysten machen oft das so genannte &quot;Data Peeking&quot;. Beim Datenabruf werden die Testdaten frühzeitig und häufig geprüft und gleichzeitig versucht, zu ermitteln, welches Erlebnis die bessere Leistung erzielt. Das Risiko besteht darin, den Test vorzeitig zu beenden, wodurch die Ergebnisse ungültig werden könnten.

Bei einem A/A-Test kann das Pinkeln von Daten oft dazu führen, dass Analysten die Steigerung in einem Erlebnis sehen, obwohl eigentlich kein Unterschied bestehen sollte, da die beiden Erlebnisse identisch sind. Tatsächlich sind A/A-Tests bei kontinuierlicher Peking tatsächlich _garantiert_ die &quot;statistische Bedeutung&quot;(d. h. eine Konfidenz über einem bestimmten Schwellenwert, z. B. 95 %) zu einem bestimmten Zeitpunkt während des Tests anzuzeigen.

Um dies zu vermeiden, sollten Sie wie bei einem regulären A/B-Test vorab entscheiden, welche Stichprobengröße zu verwenden ist, basierend auf der minimalen Wirkungsgröße (der minimalen Steigerung, unter der ein Effekt für Ihr Unternehmen nicht wichtig ist), der Leistung und dem Signifikanzniveau, die Sie für akzeptabel halten.

Bei einem A/A-Test würde das Ziel dann sein, *not* ein statistisch signifikantes Ergebnis anzeigen, nachdem Ihr Test die gewünschte Stichprobengröße erreicht hat.

Die [!UICONTROL Adobe Target-Stichprobengrößenrechner] ist ein wichtiges Tool, mit dem Sie feststellen können, welche Stichprobengröße Sie anstreben und wie lange Sie den Test ausführen sollten.

* [Adobe Target Size Calculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Darüber hinaus finden Sie in den folgenden Artikeln Informationen darüber, wie lange Sie eine Aktivität ausführen sollten, sowie weitere hilfreiche Tipps und Tricks:

* [Wie lange sollten A/B-Tests laufen?](/help/c-activities/t-test-ab/sample-size-determination.md)
* [Zehn häufige Fehler bei A/B und wie diese vermieden werden](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### Statistische Bedeutung wirkt sich auf Ihre Testergebnisse aus

Das Signifikanzniveau eines Tests bestimmt, wie wahrscheinlich es ist, dass der Test einen signifikanten Unterschied der Konversionsraten zwischen zwei verschiedenen Angeboten meldet, obwohl es tatsächlich keinen echten Unterschied gibt. Dies wird als falsch positiv oder als Fehler vom Typ I bezeichnet. Das Signifikanzniveau ist ein vom Benutzer angegebener Schwellenwert und es gibt einen Kompromiss zwischen der Toleranz für falsch-positive Ergebnisse und der Anzahl der Besucher, die bei der Auswahl des richtigen Signifikanzniveaus in den Test einbezogen werden müssen.

Ein häufig verwendetes Signifikanzniveau in A/A- und A/B-Tests beträgt 5 %, was einem Konfidenzniveau von 95 % entspricht (Konfidenzniveau = 100 % - Signifikanzniveau). Ein Konfidenzniveau von 95 % bedeutet, dass jedes Mal, wenn Sie einen Test durchführen, eine 5-%-Chance besteht, eine statistisch signifikante Steigerung zu erkennen, selbst wenn kein Unterschied zwischen den Erlebnissen besteht.

Angenommen, Sie möchten mit Ihrem A/A-Test ein Konfidenzniveau von 95 % erreichen. Bei einem Konfidenzniveau von 95 % konnten 1 von 20 A/A-Tests eine statistisch signifikante Steigerung der Konversionen zeigen. Bei einem Konfidenzniveau von 90 % konnte bei 1 von 10 Tests eine Steigerung der Konversionen beim Testen identischer Erlebnisse angezeigt werden.

## Best Practice

Wenn Sie in Ihrer Organisation einen A/A-Test für erforderlich halten, beachten Sie, dass die identischen Erlebnisse vorübergehend einen Unterschied zum Kontrollelement aufweisen können. Dies kann normal sein, je nachdem, wann der Test ausgeführt werden darf. Der Unterschied sollte mit mehr Zeit und Besuchern verringert werden.

Es empfiehlt sich, die reguläre A/B-Testmethode zu verwenden: die Stichprobengröße vorzeitig anhand einer minimalen relevanten Effektgröße, der gewünschten Leistung und der Signifikanz zu bestimmen, indem die [Adobe Target Size Calculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

Anschließend geben Sie ausreichend Zeit und Besucher ein, bevor Sie zu Schlussfolgerungen gelangen. Denken Sie daran, dass je nach Signifikanzniveau Ihres Tests die Wahrscheinlichkeit besteht, dass ein Erlebnis einen Unterschied in der Steigerung zeigt und sogar zum Gewinner erklärt wird.
