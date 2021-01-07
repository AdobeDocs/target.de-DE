---
keywords: a/b;a/a;aa;
description: Bevor Sie mit Adobe Target einen A/A-Test auf Ihrer Site durchführen, sollten Sie wissen, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test durchführen sollten und wie die Ergebnisse interpretiert werden.
title: A/A-Tests
feature: A/B Tests
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 1%

---


# A/A-Tests

Bevor Sie einen A/A-Test mit [!DNL Adobe Target] auf Ihrer Site durchführen, sollten Sie wissen, was ein A/A-Test ist, warum Sie einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen und wie die Ergebnisse interpretiert werden sollen.

## Was ist A/A-Test?

Bevor Sie A/A-Tests erklären, sollten Sie A/B-Tests überprüfen, damit wir dann die Unterschiede besprechen können.

Bei einem A/B-Standardtest wird Traffic zwei oder mehr verschiedenen Erlebnissen zugeordnet. Ein Erlebnis ist in der Regel das &quot;Steuerelement&quot;und Varianten des Erlebnisses werden mit dem Steuerelement getestet, um zu sehen, welches Erlebnis die größte Steigerung in einer bestimmten Metrik erzielt.

A/A-Tests umfassen jedoch die Zuordnung von Traffic zu zwei identischen Erlebnissen, normalerweise mit einer Aufteilung von 50/50 Traffic. Bei einem Standard-A/B-Test möchten Sie in der Regel eine Steigerung der Umrechnung feststellen. Dies unterscheidet sich von einem A/A-Test, bei dem Ihr Ziel in der Regel darin besteht, festzustellen, dass die Steigerung zwischen den identischen Erlebnissen *no* unterschiedlich ist.

## Warum sollten Sie zwei identische Erlebnisse testen und was bewirkt dies?

Einige Unternehmen führen A/A-Tests durch, wenn sie ein neues Testwerkzeug implementieren, z. B. [!DNL Target], um festzustellen, ob:

* Die Aktivität wurde korrekt eingerichtet
* Der Code wurde korrekt implementiert
* Der Berichte ist korrekt

Obwohl nur wenige Unternehmen A/A-Tests durchführen, ist es in der Tat empfehlenswert, diese als &quot;sanfte&quot;Experimente durchzuführen, um Vertrauen zu schaffen, nachdem das Tool implementiert wurde oder bevor A/B-Tests durchgeführt wurden, die sich auf die Konversion und den Umsatz auswirken könnten.

## Warum sehen Sie möglicherweise eine Steigerung für ein Erlebnis, wenn die Erlebnisse identisch sind?

Es gibt zahlreiche Gründe, warum Sie möglicherweise eine Steigerung in einem Erlebnis gegenüber dem anderen (identischen) Erlebnis sehen:

### Der A/A-Test konnte nicht lange genug ausgeführt werden

Ein häufig auftretendes Problem bei der Durchführung eines Tests, einschließlich eines A/A-Tests, besteht darin, einen Test vorzeitig zu beenden und ein erfolgreiches Erlebnis zu deklarieren. Analysten machen oft das so genannte &quot;Datenpeeking&quot;. Bei der Datenabfrage werden die Testdaten frühzeitig und häufig angezeigt, während gleichzeitig festgestellt wird, welches Erlebnis eine bessere Leistung erzielt. Das Risiko besteht darin, den Test vorzeitig zu beenden, was die Ergebnisse ungültig machen könnte.

Bei einem A/A-Test kann die Datenabfrage dazu führen, dass Analysten eine Steigerung in einem Erlebnis sehen, wenn sie davon ausgehen, dass es keinen Unterschied geben sollte, da die beiden Erlebnisse identisch sind. Bei ausreichender Zeit und ausreichender Besuchszeit sollte die Steigerungsdifferenz verringert werden.

Wie bei einem regelmäßigen A/B-Test sollten Sie daher vorab entscheiden, welche Stichprobengröße Sie verwenden möchten, basierend auf der minimalen Effektgröße, der Leistungsstärke und den Signifikanzstufen, die Sie für akzeptabel halten. Bei einem A/A-Test wäre das Ziel dann *nicht*, ein statistisch signifikantes Ergebnis anzuzeigen, nachdem Ihr Test die gewünschte Stichprobengröße erreicht hat.

Der [!UICONTROL Adobe Target-Stichprobengrößenrechner] ist ein wichtiges Tool, mit dem Sie feststellen können, für welche Stichprobengröße und wie lange Sie den Test durchführen sollten.

* [Adobe Target Size Calculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Darüber hinaus finden Sie in den folgenden Artikeln Informationen darüber, wie lange eine Aktivität ausgeführt werden soll, sowie weitere hilfreiche Tipps und Tricks:

* [Wie lange sollten A/B-Tests laufen?](/help/c-activities/t-test-ab/sample-size-determination.md)
* [Zehn häufige A/B-Fallstricke und wie sie vermieden werden können](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### Statistische Bedeutung beeinflusst Ihre Testergebnisse

Das Signifikanzniveau eines Tests bestimmt, wie wahrscheinlich es ist, dass der Test einen signifikanten Unterschied in den Konversionsraten zwischen zwei verschiedenen Angeboten meldet, wenn es tatsächlich keinen echten Unterschied gibt. Dies wird als falsch-positiv oder als Fehler vom Typ I bezeichnet. Das Signifikanzniveau ist ein vom Anwender angegebener Schwellenwert, und es besteht ein Kompromiss zwischen der Toleranz für Falsch-Positiv-Werte und der Anzahl der Besucher, die bei der Wahl des richtigen Signifikanzniveaus in den Test einbezogen werden müssen.

Ein häufig verwendetes Signifikanzniveau bei A/A- und A/B-Tests beträgt 5 %, was einem Konfidenzniveau von 95 % entspricht (Konfidenzniveau = 100 % - Signifikanzniveau). Ein Konfidenzniveau von 95 % bedeutet, dass bei jedem Test eine Wahrscheinlichkeit von 5 % besteht, eine statistisch signifikante Steigerung zu erkennen, selbst wenn kein Unterschied zwischen den Erlebnissen besteht.

Angenommen, Sie möchten mit Ihrem A/A-Test ein Konfidenzniveau von 95 % erreichen. Bei einem Konfidenzniveau von 95 % könnte jeder 20 A/A-Test eine statistisch signifikante Steigerung der Konversionen aufweisen. Bei einem Konfidenzniveau von 90 % kann bei 1 von 10 Tests eine Steigerung der Konversionen beim Testen identischer Erlebnisse festgestellt werden.

## Best Practice

Wenn Sie entscheiden, dass ein A/A-Test in Ihrem Unternehmen erforderlich ist, beachten Sie, dass die identischen Erlebnisse vorübergehend einen Unterschied zum Kontrollelement aufweisen können. Dies kann normal sein, je nachdem, wann der Test ausgeführt werden darf. Der Unterschied sollte angesichts von mehr Zeit und Besuchern verringert werden.

Best Practice ist die Verwendung einer regelmäßigen A/B-Testmethode: entscheiden Sie mithilfe des [Adobe Target Size Calculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) die Stichprobengröße vorab anhand einer minimalen Effektgröße, der gewünschten Stärke und der Signifikanz.

Anschließend sollten Sie ausreichend Zeit und Besucher einräumen, bevor Sie zu Schlussfolgerungen gelangen. Denken Sie daran, dass je nach der Signifikanz Ihres Tests die Wahrscheinlichkeit besteht, dass ein Erlebnis einen Unterschied in der Steigerung zeigt und sogar als Gewinner ausgewiesen wird.
