---
keywords: faq;frequently asked questions;analytics for target;a4T;report;reports;view reports;reporting;counting methodology;impressions;visitors;visits;default metric;activity conversions;unspecified
description: Dieses Thema enthält Antworten auf häufig zur Anzeige von Berichten bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Anzeigen von Berichten – Häufig gestellte Fragen zu A4T
feature: a4t troubleshooting
topic: Standard
uuid: d51991f7-cdda-4a59-b64c-7ef1c3f8380d
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 63%

---


# Anzeigen von Berichten – Häufig gestellte Fragen zu A4T{#view-reports-a-t-faq}

This topic contains answers to questions that are frequently asked about viewing reports when using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Kann ich meine Target-Aktivitätsdaten im Analysis Workspace anzeigen? {#workspace}

Sie können Ihre [!DNL Analysis Workspace] Aktivitäten und Erlebnisse [!DNL Target] analysieren. Im Bereich [Analytics für Zielgruppen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) können Sie die Steigerung und das Vertrauen für bis zu drei Erfolgsmetriken anzeigen. Mithilfe von Tabellen und Visualisierungen können Sie auch tiefer graben.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by Adobe Experience League.

## Wo können Segmente in Analysis Workspace angewendet werden? {#segmentation}

Segmente werden meist am oberen Rand eines Bereichs in der Segment-Dropzone angewendet. Das Segment wird auf alle Tabellen und Visualisierungen im Bedienfeld angewendet. Diese Technik ist am nützlichsten, um zu sehen, wie der Test eine Untergruppe von Personen betrifft (wie hat dieser Test zum Beispiel für Menschen in Großbritannien funktioniert)?

## Warum werden nicht verwandte Erlebnisse zurückgegeben, wenn ich ein Treffersegment für eine bestimmte Aktivität der Zielgruppe anwende? {#activity-segmentation}

Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. (Hinweis: Diese Ablaufzeit kann bei Bedarf vom Kundendienst angepasst werden. Während Besucher durch die Site in diesem Ablauffenster navigieren, gehören sie zu vielen [!DNL Target] Aktivitäten, die alle in der Dimension erfasst werden.

Wenn Sie daher segmentieren, dass eine Aktivität in einem Treffer vorhanden sein soll, erhalten Sie alle Erlebnisse, die Teil dieser Aktivität sind, *sowie* alle anderen Erlebnisse, die bei diesem Treffer bestehen bleiben.

## Sollte ich Besucher, Besuche oder Aktivitäten-Impressionen als Normalisierungsmetrik verwenden (d. h. als Zählmethodik)? {#metrics}

Es gibt mehrere Optionen zum Normalisieren von Metriken im A4T-Berichte. Diese Metrik, auch als Zählmethodik bezeichnet, wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.

* ***Unique Visitors*** wird um eins erhöht, wenn ein Benutzer sich zum ersten Mal für eine Aktivität qualifiziert.
* ***Besuche*** wird mit jeder Sitzung erhöht, sobald ein Benutzer (Unique Visitor) eine Aktivität beginnt, selbst wenn diese Aktivität nicht in nachfolgenden Besuchen angezeigt wird.
* ***Aktivitätsimpressionen*** wird jedes Mal erhöht, wenn Aktivitätsinhalt bereitgestellt wird. (gemessen von [!DNL Target]).

Wenn ein Besucher eine Seite anzeigt, die eine Aktivität enthält, wird eine Variable für diesen Besucher festgelegt, die den Namen der Aktivität enthält. Informationen zu den verschiedenen Zählmethoden finden Sie in den unten aufgeführten ausführlichen Szenarien.

Beachten Sie Folgendes:

* All of the above metrics trigger when a user qualifies for an activity and content is returned from [!DNL [!DNL Target]]. Das bedeutet nicht zwingend, dass der Benutzer das Angebot gesehen hat. Wenn ein Aktivitätserlebnis sich unterhalb des angezeigten Bildschirmbereichs befindet und der Benutzer nicht nach unten scrollt, wurde das Angebot zwar von [!DNL Target] bereitgestellt, aber nicht vom Benutzer gesehen.
* [!UICONTROL Aktivitätsimpressionen] (gemessen durch [!DNL Target]) und [!UICONTROL Instanzen] (gemessen durch [!DNL Analytics]) sind gleich, sofern nicht mehrere Mbox-Aufrufe auf derselben Seite in derselben Aktivität vorhanden sind. Hierdurch werden mehrere [!UICONTROL Aktivitätsimpressionen] gezählt, aber nur eine [!UICONTROL Instanz].

## Warum sind &quot;Aktivitäten-Impressionen&quot;und &quot;Aktivitäten-Konversionen&quot;in Analysis Workspace höher als in Reports &amp; Analysen? {#sametouch}

[!DNL Reports & Analytics] wendet ein Gleichheitszuordnungsmodell auf &quot;Aktivität Impressionen&quot;und &quot;Aktivität-Konversionen&quot;an, während die Rohmetriken angezeigt werden, die aufgrund der Persistenz der [!DNL Analysis Workspace] [!DNL Target] Dimension überhöht erscheinen können.

To evaluate accurate [!UICONTROL Activity Impressions] and [!UICONTROL Activity Conversions] metrics in [!DNL Analysis Workspace], ensure that both metrics have [!UICONTROL Same Touch] attribution models applied. Modelle können angewendet werden, indem Sie auf das Zahnradsymbol der Spalte klicken, [!UICONTROL Nicht standardmäßige Attributionsmodelle] aktivieren und [!UICONTROL Same Touch] auswählen. Weitere Informationen zur Zuordnung finden Sie im Überblick [über die](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution.html) Attributes-IQ im *Analytics-Tools-Handbuch*.

## Was bedeutet „Aktivitätskonversionen“, wenn der Marketingexperte beim Setup einer Aktivität eine Analytics-Metrik auswählt? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Activity conversions&quot; will be empty if an [!DNL Analytics] metric was selected as the conversion metric for the activity.

## Warum steht in den Analytics-Berichten „Nicht angegeben“? Was bedeutet das? {#unspecified}

In anderen Berichten bedeutet „Nicht angegeben“, dass Daten eine bestimmte Classification nicht erfüllt haben. Dies sollte jedoch in A4T nie passieren. Wenn Sie „Nicht angegeben“ angezeigt bekommen, wurde der Classifications-Service noch nicht ausgeführt. Es dauert normalerweise zwischen 24 und 72 Stunden, bis Aktivitätsdaten in den Berichten angezeigt werden. Obwohl die Aktivitäten erst zu diesem Zeitpunkt in diesem Bericht angezeigt werden, werden alle an diese Aktivitäten geknüpften Besucherdaten erfasst und nach dem Abschluss der Classification angezeigt.

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

## Warum werden Target-Metriken auch dann noch an Analytics gesendet, wenn die Aktivität deaktiviert wurde? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. Dieser Ablaufzeitraum kann bei Bedarf vom Kundendienst angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

You might see [!DNL Target] variables sent to [!DNL Analytics] after the expiration period because the expiration is 90 days, but only if that user never sees another A4T-enabled [!DNL Target] activity. Wenn ein Benutzer am 45. Tag zur Site zurückkehrt und eine andere Aktivität ansieht, wird der gesamte Zähler für den A4T-eVar-Wert wieder auf 90 Tage zurückgesetzt. Das heißt, dass die erste Kampagne jetzt ab dem 1. Tag für 45 + 90 = 135 Tage fortbesteht. If the user keeps coming back, you might get to the point where you see metrics sent to [!DNL Analytics] in your reporting from much older activities. Wenn Benutzer Cookies löschen und nicht zur Site zurückkehren, gehen die Zahlen für die entsprechende Aktivität zurück, werden aber weiterhin angezeigt.

Das bedeutet, dass Aktivitäten von Besuchern, die während ihrer aktiven Dauer Teil der Aktivität wurden, über einen Zeitraum von bis zu 90 Tagen nach Abschluss der Aktivität weiterhin angesehen, besucht usw. werden können. Sollten Sie jedoch einen Blick auf die Metrik [!UICONTROL Aktivitätsimpressionen] werfen, sollten nach Ablauf der Aktivität keine weiteren Impressionen erfasst werden.

Dies ist ein normales und erwartetes Verhalten. Die A4T-Variable funktioniert wie alle anderen eVars. Der Wert wird so lange dem Benutzer zugeordnet bis die Ablaufzeit erreicht ist (90 Tage). Daher wird der Wert, auch wenn eine Aktivität nur zwei Wochen lang aktiv ist, mindestens 90 Tage lang dem Benutzer zugeordnet.

Die Best Practice ist, Berichte für eine solche Aktivität nur für den Zeitraum anzuzeigen, in dem die Aktivität aktiv war. The dates should be set correctly by default when you view the activity in [!DNL Analytics], so unless you have manually extended the date this shouldn’t be an issue from a reporting standpoint.

Angenommen, die A4T-Variable läuft nach 90 Tagen ab und unser Test ist vom 1. bis 15. Januar aktiv.

Am 1. Januar besucht der Benutzer die Seite, sieht einmal die Aktivität XYZ und hat danach fünf weitere Seitenansichten. In den nächsten zwei Wochen kehrt der Benutzer nicht zur Seite zurück. Die Daten für diesen Benutzer sehen dann wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

Der Benutzer kehrt dann am 1. Februar zurück, sieht fünf weitere Seiten, findet keine weiteren Target-Aktivitäten vor und die ursprüngliche Aktivität ist nicht mehr aktiv. Auch wenn die Aktivität nicht mehr aktiv ist, wird der Benutzer wegen der eVar-Persistenz jedoch weiterhin verfolgt. Die Daten sehen anschließend wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

Der Benutzer kehrt am 1. März zurück und sieht die neue Aktivität ABC. Er sieht außerdem fünf Seiten. Da die Aktivität XYZ aufgrund der Persistenz weiterhin verfolgt und für diesen Benutzer dann auch ABC festgelegt wird, sind im Bericht jetzt zwei Linienelemente vorhanden:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

Der Benutzer kehrt am 1. April zurück, betrachtet fünf weitere Seiten und tätigt einen Kauf. Die Ablauffrist von 90 Tagen für den ersten eVar-Wert wird am 1. April zurückgesetzt, was im Bericht zu sehen ist. Und allen Target-Aktivitäten, die der Benutzer sieht, wird die Konversion gutgeschrieben, die Gesamtzahl der Konversionen wird jedoch dedupliziert:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors | Bestellungen |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Gesamt | 2 | 20 | 3 | 1 | 1 |

Da vor der Konversion beide Erlebnisse gesehen wurden, wird die Bestellung beiden „gutgeschrieben“. Im System gab es jedoch nur eine Bestellung, was die Summe zeigt. For [!DNL Target] reporting, because you aren’t putting a [!DNL Target] activity against another activity to see which is more successful, it doesn’t matter that all activities the user saw got credit. In diesen Berichten werden die Ergebnisse zweier Elemente innerhalb einer einzigen Aktivität verglichen. Ein Benutzer kann innerhalb derselben Aktivität keine unterschiedlichen Erlebnisse sehen, weshalb Sie sich über eine mögliche Kreuzkontamination bei der Zuschreibung der Bestellung keine Gedanken machen müssen.

For more information, see [Conversion Variables (eVar](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) in the *Analytics Admin Guide*.

## Warum berechnen Analytics und Analytics for Target (A4T) die Zahlen für die Metrik „Unique Visitors“ unterschiedlich? {#section_0C3B648AB54041F9A2AA839D51791883}

Wenn Sie einen A/B-Test ausführen, der den Student-t-Test (die Konfidenzmetrik) verwendet, um einen Gewinner auszuwählen, gilt unter anderem die Annahme, dass es einen festen Zeithorizont gibt. Der Test ist nur dann statistisch gültig, wenn Sie diese feste Stichprobengröße untersuchen.

The [!UICONTROL Unique Visitors] metric is different in [!DNL Analytics] and [!DNL Target] only when you are looking at a period of time that is shorter than the actual test. Wenn die Stichprobengröße nicht erreicht wird, ist der Test nicht sehr zuverlässig. Weitere Informationen finden Sie unter [How Not to Run an A/B-Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) auf der [Website von Evan Miller](https://www.evanmiller.org/index.html).

The [!UICONTROL Unique Visitors] metric displays the number of people who have been exposed to the test who have visited the site during the specified time period. Diese Personen sind weiterhin Teil des Tests und müssen berücksichtigt werden. Wenn Sie nur die Anzahl der Personen sehen wollen, die innerhalb einer einzigen Woche betroffen waren, können Sie ein Segment der Besucher erstellen, die eine Aktivitätsimpression hatten, und dieses auf den Bericht anwenden.

You can shorten the amount of time the [!DNL Target] variable persists down to a session; however, that is usually problematic for tests where the conversion event isn’t as likely to happen within the same session.

## Warum wird in Analytics derselbe Besucher manchmal bei mehreren Besuchen gezählt?  {#section_1397E972D31C4207A142E4D2D6D794A2}

The following list explains reasons why the same visitor could be counted in multiple experiences in [!DNL Analytics]:

* The [!DNL Target] profile expired but the [!DNL Analytics] cookie is still there. In this situation, [!DNL Target] re-evaluates the user but [!DNL Analytics] considers the visitor to be the same person.
* Wenn der Besucher die `mbox3rdPartyId` verwendet, sobald der anonyme Besucher mit seinem Drittanbieter-ID-Profil verschmolzen wird, könnte den Besucher in einen anderen Besuch einordnen, der mit der ID eines Drittanbieters übereinstimmt. [!DNL Target] Weitere Informationen finden Sie unter [Echtzeit-Profilsynchronisierung für mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] kann verschiedene Geräte auf andere Weise als denselben Besucher verfolgen, und zwar auf andere Weise als [!DNL Target] die Verfolgung dieser Geräte: Die Einrichtung der Drittanbieter-ID in [!DNL Target] unterscheidet sich von der in Analytics.

## Unterstützt A4T Virtual Report Suites?

Virtual Report Suites sind *nicht* in der Report Suite-Liste enthalten und Zielgruppen aus Virtual Report Suites werden in A4T-Berichten nicht unterstützt.

## Kann ich den Prozentsatz der Traffic-Zuordnung in einer Aktivität ändern, die nach der Aktivierung der Aktivität A4T verwendet?

Changing the traffic allocation percentage in an activity after activation can cause inconsistent reporting in [!DNL Analytics] because the change impacts only new visitors. Wiederkehrende Besucher sind nicht betroffen.

Am besten sollten Sie die vorhandene Aktivität stoppen und dann eine neue Aktivität erstellen, anstatt den Prozentsatz nach der Aktivierung zu ändern. Die Berichterstellung für die neue Aktivität beginnt mit neuen Besuchern und Daten aus zurückkehrenden Besuchern führen nicht zu inkonsistenten Berichten.
