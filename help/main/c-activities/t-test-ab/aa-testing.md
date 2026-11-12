---
keywords: a/b;a/a;aa;
description: Erfahren Sie, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen sollten und wie die Ergebnisse interpretiert werden.
title: Was sind A/A-Tests?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
TQID: 'https://experienceleague.adobe.com/-kLz0mG8LaFqEbB-9M89vJWTFjfypupbcOQ3MjQz-jQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 322dbbd67ea981ad05ed8a1fdc1137ec50effd12
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%
---
# A/A-Tests {#aa-testing}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, was ein A/A-Test ist, warum Sie einen Test durchführen könnten, warum es zu einer Steigerung zwischen identischen Erlebnissen kommen könnte und welche Best Practice es für die Durchführung von A/A-Tests in [!DNL Target] gibt.

>[!ENDSHADEBOX]

Bevor Sie mit [!DNL Adobe Target] einen A/A-Test auf Ihrer Site durchführen, müssen Sie wissen, was ein A/A-Test ist, warum Sie möglicherweise einen A/A-Test durchführen möchten, wie lange Sie den Test ausführen sollten und wie die Ergebnisse interpretiert werden.

## Was sind A/A-Tests? {#what-is-aa}

Ein A/A-Test unterscheidet sich von einem standardmäßigen A/B-Test in Bezug auf die Zuordnung des Traffics und das, was Sie lernen möchten:

* **A/B-Test** Der Traffic wird zwei oder mehr verschiedenen Erlebnissen zugeordnet. Ein Erlebnis ist in der Regel das „Kontrollerlebnis“, und Varianten des Erlebnisses werden im Vergleich zum Kontrollerlebnis getestet, um zu sehen, welches Erlebnis in einer bestimmten Metrik den meisten Anstieg erzeugt. Normalerweise möchten Sie eine Steigerung der Konversion feststellen.
* **A/A-Test** Der Traffic wird zwei identischen Erlebnissen zugeordnet, normalerweise mit einer Aufteilung der Traffic-Zuordnung von 50/50. Normalerweise besteht Ihr Ziel darin, festzustellen, *es* Unterschied in der Steigerung zwischen den identischen Erlebnissen gibt.

## Warum einen A/A-Test durchführen? {#why-aa}

Einige Unternehmen führen A/A-Tests durch, wenn sie ein neues Test-Tool wie [!DNL Target] implementieren, um festzustellen, ob:

* Die Aktivität wurde korrekt eingerichtet
* Der Code wurde korrekt implementiert
* Das Reporting ist korrekt

Obwohl nur wenige Unternehmen A/A-Tests durchführen, empfiehlt es sich, diese als „Vernunftexperimente“ durchzuführen, um Vertrauen zu schaffen, nachdem das Tool implementiert wurde oder bevor A/B-Tests durchgeführt wurden, die sich auf Konversionen und Umsätze auswirken könnten.

## Warum identische Erlebnisse eine Steigerung zeigen können {#why-lift}

Es gibt zahlreiche Gründe, warum Sie möglicherweise eine Steigerung in einem Erlebnis gegenüber einem anderen (identischen) Erlebnis sehen:

### Der A/A-Test wurde kontinuierlich überwacht

Ein häufiges Problem bei der Durchführung von Tests jeglicher Art, einschließlich A/A-Tests, besteht darin, die Ergebnisse kontinuierlich zu betrachten und einen Test vorzeitig zu stoppen, wenn Sie statistische Signifikanz sehen, und ein erfolgreichstes Erlebnis zu erklären. Analysten machen oft das, was als „Data Peeking“ bezeichnet wird. Beim Data Peeking werden die Testdaten früh und häufig betrachtet, während versucht wird festzustellen, welches Erlebnis eine bessere Leistung erzielt. Das Risiko besteht darin, den Test vorzeitig abzubrechen, wodurch die Ergebnisse ungültig werden könnten.

Bei einem A/A-Test kann Data Peeking dazu führen, dass Analysten eine Steigerung in einem Erlebnis sehen, obwohl es eigentlich keinen Unterschied geben sollte, da die beiden Erlebnisse identisch sind. Tatsächlich zeigen A/A-Tests mit kontinuierlichem Peeking *garantiert* irgendwann während des Tests „statistische Signifikanz“ (d. h. eine Konfidenz oberhalb eines bestimmten Schwellenwerts, z. B. 95 %).

### Statistische Signifikanz wirkt sich auf Testergebnisse aus

Das Signifikanzniveau eines Tests bestimmt, wie wahrscheinlich es ist, dass der Test einen signifikanten Unterschied bei den Konversionsraten zwischen zwei verschiedenen Angeboten meldet, obwohl es tatsächlich keinen echten Unterschied gibt. Dies wird als falsch positiv oder als Fehler vom Typ I bezeichnet. Das Signifikanzniveau ist ein vom Benutzer festgelegter Schwellenwert, und es besteht ein Kompromiss zwischen der Toleranz für falsch positive Ergebnisse und der Anzahl der Besucher, die in den Test einbezogen werden müssen, um das richtige Signifikanzniveau auszuwählen.

Ein häufig verwendetes Signifikanzniveau in A/A- und A/B-Tests beträgt 5 %, was einem Konfidenzniveau von 95 % entspricht (Konfidenzniveau = 100 % - Signifikanzniveau). Ein Konfidenzniveau von 95 % bedeutet, dass bei jeder Durchführung eines Tests eine Wahrscheinlichkeit von 5 % besteht, eine statistisch signifikante Steigerung zu erkennen, auch wenn es keinen Unterschied zwischen den Erlebnissen gibt.

Angenommen, Sie möchten mit Ihrem A/A-Test ein Konfidenzniveau von 95 % erreichen. Mit einem Konfidenzniveau von 95 % konnte 1 von 20 A/A-Tests eine statistisch signifikante Steigerung der Konversionen zeigen. Bei einem Konfidenzniveau von 90 % kann jeder 10. Test beim Testen identischer Erlebnisse eine Steigerung der Konversionen zeigen.

## Best Practice {#best-practice}

Wenn Sie sich entscheiden, dass in Ihrer Organisation ein A/A-Test erforderlich ist, beachten Sie, dass die identischen Erlebnisse möglicherweise vorübergehend einen Unterschied zur Kontrolle aufweisen. Dies kann normal sein, je nachdem, wie lange der Test ausgeführt werden darf. Der Unterschied sollte sich verringern, wenn mehr Zeit und Besucher zur Verfügung stehen.

Verwenden Sie die reguläre A/B-Testmethode:

1. Legen Sie im Voraus fest, welche Stichprobengröße verwendet werden soll, basierend auf der minimalen Effektgröße (der minimalen Steigerung, unterhalb derer ein Effekt für Ihr Unternehmen nicht wichtig ist), der Leistung und dem Signifikanzniveau, das Sie akzeptabel finden. Der **[!UICONTROL Adobe Target-Stichprobengrößenrechner]** ist ein wichtiges Tool, mit dem Sie bestimmen können, auf welche Stichprobengröße Sie abzielen und wie lange Sie den Test ausführen sollten. Siehe den [Adobe Target-Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

1. Lassen Sie sich ausreichend Zeit und Besuchende, bevor Sie irgendwelche Schlussfolgerungen ziehen. Bei einem A/A-Test besteht das Ziel darin *ein statistisch signifikantes Ergebnis* sehen, nachdem Ihr Test die gewünschte Stichprobengröße erreicht hat.

1. Denken Sie daran, dass je nach Signifikanzniveau Ihres Tests die Möglichkeit besteht, dass ein Erlebnis einen Unterschied in der Steigerung zeigt und sogar zum Gewinner erklärt wird.

Informationen zur Dauer einer Aktivität sowie weitere hilfreiche Tipps und Tricks finden Sie in den folgenden Artikeln:

* [Wie lange sollten A/B-Tests laufen?](/help/main/c-activities/t-test-ab/sample-size-determination.md)
* [Zehn häufige A/B-Fehler und wie diese vermieden werden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)
