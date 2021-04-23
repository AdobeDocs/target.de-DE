---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Bericht; Berichte; Berichte anzeigen; Berichterstellung; Zählmethodik; Impressionen; Besucher; Besuche; Standardmetrik; Aktivitätskonversionen; unspezifisch
description: Ermitteln Sie Antworten auf Fragen, die bei der Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten häufig nach der Anzeige von Berichten gefragt werden.
title: Antworten auf Fragen zur Ansicht von Berichten mit A4T?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
translation-type: tm+mt
source-git-commit: 0136e1a17181ed6bc39b112ee464eff5af7785b0
workflow-type: tm+mt
source-wordcount: '2512'
ht-degree: 37%

---

# Anzeigen von Berichten – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig nach der Anzeige von Berichten bei Verwendung von [!DNL Adobe Analytics] als Berichte für [!DNL Adobe Target] (A4T) gefragt werden.

## Kann ich meine [!DNL Target]-Aktivität-Daten in Analysis Workspace Ansicht haben? {#workspace}

Sie können [!DNL Analysis Workspace] verwenden, um Ihre [!DNL Target]-Aktivitäten und -Erlebnisse zu analysieren. Im Bedienfeld [Analytics für Zielgruppen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) können Sie Steigerung und Konfidenz für bis zu drei Erfolgsmetriken sehen. Mithilfe von Tabellen und Visualisierungen können Sie auch tiefer graben.

Ausführliche Informationen und Beispiele finden Sie unter [Analytics &amp; Zielgruppe: Best Practices für das Tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) zur Analyse, bereitgestellt von Adobe Experience League.

## Wo können Segmente in Analysis Workspace angewendet werden? {#segmentation}

Segmente werden am häufigsten am oberen Rand eines Bedienfelds in der Segment-Dropzone verwendet. Das Segment wird auf alle Tabellen und Visualisierungen im Bedienfeld angewendet. Diese Technik ist am nützlichsten, um zu sehen, wie der Test eine Untergruppe von Personen betrifft (wie hat dieser Test zum Beispiel für Menschen in Großbritannien funktioniert)?

Ein Segment kann auch direkt in der Freiformtabelle überlagert werden. Beachten Sie jedoch, dass Sie es über die gesamte Tabelle hinweg überlagern müssen, um die Steigerungs- und Konfidenzberechnungen im A4T-Bedienfeld beizubehalten. Segmente auf Spaltenebene werden derzeit im Bedienfeld nicht unterstützt.

## Warum werden nicht verwandte Erlebnisse zurückgegeben, wenn ich ein Treffersegment für eine bestimmte [!DNL Target]-Aktivität anwende? {#activity-segmentation}

Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. (Hinweis: Diese Ablaufzeit kann bei Bedarf vom Kundendienst angepasst werden. Während Besucher durch die Site in diesem Ablauffenster navigieren, gehören sie zu vielen [!DNL Target]-Aktivitäten, die alle in der Dimension erfasst werden.

Wenn Sie segmentieren, dass eine Aktivität in einem Treffer vorhanden sein soll, erhalten Sie alle Erlebnisse, die Teil dieser Aktivität sind *plus* alle anderen Erlebnisse, die bei diesem Treffer bestehen bleiben.

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf Erweiterte Einstellungen zugreifen?

Bei Aktivitäten, die [!DNL Analytics] als Berichte-Quelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität halten]&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen können nicht konfiguriert werden.**

Weitere Informationen finden Sie unter &quot;Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen?&quot; in [Metrikdefinitionen - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Sollte ich Besucher, Besuche oder Aktivitäten-Impressionen als Normalisierungsmetrik verwenden (d. h. als Zählmethodik)? {#metrics}

Es gibt mehrere Optionen zum Normalisieren von Metriken im A4T-Berichte. Diese Metrik, auch als Zählmethodik bezeichnet, wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.

* ***Unique Visitors*** wird um eins erhöht, wenn ein Benutzer sich zum ersten Mal für eine Aktivität qualifiziert.
* ***Besuche*** wird mit jeder Sitzung erhöht, sobald ein Benutzer (Unique Visitor) eine Aktivität beginnt, selbst wenn diese Aktivität nicht in nachfolgenden Besuchen angezeigt wird.
* ***Aktivitätsimpressionen*** wird jedes Mal erhöht, wenn Aktivitätsinhalt bereitgestellt wird. (Gemessen von [!DNL Target]).

Wenn ein Besucher eine Seite anzeigt, die eine Aktivität enthält, wird eine Variable für diesen Besucher festgelegt, die den Namen der Aktivität enthält. Informationen zu den verschiedenen Zählmethoden finden Sie in den unten aufgeführten ausführlichen Szenarien.

Beachten Sie Folgendes:

* Der obige Metriken-Trigger, wenn sich ein Benutzer für eine Aktivität qualifiziert und der Inhalt von [!DNL Target] zurückgegeben wird. Das bedeutet nicht zwingend, dass der Benutzer das Angebot gesehen hat. Wenn ein Aktivitätserlebnis sich unterhalb des angezeigten Bildschirmbereichs befindet und der Benutzer nicht nach unten scrollt, wurde das Angebot zwar von [!DNL Target] bereitgestellt, aber nicht vom Benutzer gesehen.
* [!UICONTROL Aktivitätsimpressionen] (gemessen durch [!DNL Target]) und [!UICONTROL Instanzen] (gemessen durch [!DNL Analytics]) sind gleich, sofern nicht mehrere Mbox-Aufrufe auf derselben Seite in derselben Aktivität vorhanden sind. Hierdurch werden mehrere [!UICONTROL Aktivitätsimpressionen] gezählt, aber nur eine [!UICONTROL Instanz].

Weitere Informationen finden Sie unter [Wie Sie A4T-Berichte in Analysis Workspace für Aktivitäten mit automatischer Zielgruppe](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target-Tutorials einrichten*.

## Warum sind &quot;Aktivitäten-Impressionen&quot;und &quot;Aktivitäten-Konversionen&quot;in Analysis Workspace höher als in Reports &amp; Analysen? {#sametouch}

[!DNL Reports & Analytics] wendet ein Gleichheitszuordnungsmodell auf &quot;Aktivität Impressionen&quot;und &quot;Aktivität-Konversionen&quot;an, während die Rohmetriken  [!DNL Analysis Workspace] angezeigt werden, die aufgrund der Persistenz der  [!DNL Target] Dimension überhöht erscheinen können.

Um genaue Metriken für [!UICONTROL Aktivität-Impressionen] und [!UICONTROL Aktivitäten-Konversionen] in [!DNL Analysis Workspace] auszuwerten, stellen Sie sicher, dass für beide Metriken [!UICONTROL Gleicher Touch] Zuordnungsmodelle angewendet wurden. Modelle können angewendet werden, indem Sie auf das Zahnradsymbol der Spalte klicken, [!UICONTROL Nicht standardmäßige Attributionsmodelle] aktivieren und [!UICONTROL Same Touch] auswählen. Weitere Informationen zur Zuordnung finden Sie unter [Übersicht über Attribute IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) im *Analytics Tools Guide*.

## Was bedeutet „Aktivitätskonversionen“, wenn der Marketingexperte beim Setup einer Aktivität eine Analytics-Metrik auswählt? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Aktivität-Konversionen&quot;sind leer, wenn eine [!DNL Analytics]-Metrik als Konversionsmetrik für die Aktivität ausgewählt wurde.

## Warum steht in den Analytics-Berichten „Nicht angegeben“? Was bedeutet das? {#unspecified}

In anderen Berichten bedeutet „Nicht angegeben“, dass Daten eine bestimmte Classification nicht erfüllt haben. Dies sollte jedoch in A4T nie passieren. Wenn Sie „Nicht angegeben“ angezeigt bekommen, wurde der Classifications-Service noch nicht ausgeführt. Es dauert normalerweise zwischen 24 und 72 Stunden, bis Aktivitätsdaten in den Berichten angezeigt werden. Obwohl die Aktivitäten erst zu diesem Zeitpunkt in diesem Bericht angezeigt werden, werden alle mit diesen Aktivitäten verknüpften Besucher-Daten erfasst und nach Abschluss der Klassifizierung angezeigt.

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn die Klassifizierung für diese Aktivität durchgeführt wurde und Sie trotzdem eine Zeile &quot;Nicht angegeben&quot;im Bericht sehen, stellen Sie sicher, dass der Bericht keine Nicht-[!DNL Target]-Metrik verwendet, um die Daten anzuzeigen. Sofern der Bericht keine [!DNL Target]-spezifische Metrik verwendet, enthält diese Zeile &quot;Nicht angegeben&quot;Ereignis für Aufrufe, die nicht mit [!DNL Target] verknüpft sind. Diese Zeile enthält keine [!DNL Target]-verknüpften Informationen (z. B. Besucher/Besuche/Impressionen).

## Warum werden [!DNL Target]-Metriken nach der Deaktivierung der Aktivität an Analytics gesendet? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. Dieser Ablaufzeitraum kann bei Bedarf vom Kundendienst angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

Möglicherweise sehen Sie nach Ablauf [!DNL Target]-Variablen, die an [!DNL Analytics] gesendet werden, da der Ablauf 90 Tage beträgt, jedoch nur, wenn der Benutzer nie eine weitere A4T-fähige [!DNL Target]-Aktivität sieht. Wenn ein Benutzer am 45. Tag zur Site zurückkehrt und eine andere Aktivität ansieht, wird der gesamte Zähler für den A4T-eVar-Wert wieder auf 90 Tage zurückgesetzt. Das heißt, dass die erste Kampagne jetzt ab dem 1. Tag für 45 + 90 = 135 Tage fortbesteht. Wenn der Benutzer immer wieder zurückkehrt, können Sie an den Punkt gelangen, an dem Metriken von viel älteren Aktivitäten an [!DNL Analytics] in Ihrem Berichte gesendet werden. Wenn Benutzer Cookies löschen und nicht zur Site zurückkehren, werden die Nummern in dieser Aktivität abgelegt, sie können aber trotzdem angezeigt werden.

Das bedeutet, dass Aktivitäten bis zu 90 Tage nach Ende der Aktivität weiterhin Ansichten, Besuche usw. für Besucher erhalten, die während der Aktivität Teil der Aktivität wurden. Sollten Sie jedoch einen Blick auf die Metrik [!UICONTROL Aktivitätsimpressionen] werfen, sollten nach Ablauf der Aktivität keine weiteren Impressionen erfasst werden.

Dies ist ein normales und erwartetes Verhalten. Die A4T-Variable funktioniert wie alle anderen eVars. Der Wert wird so lange dem Benutzer zugeordnet bis die Ablaufzeit erreicht ist (90 Tage). Wenn also eine Aktivität nur zwei Wochen lang aktiv ist, wird der Wert mindestens für die nächsten 90 Tage mit dem Benutzer verknüpft.

Die Best Practice ist, Berichte für eine solche Aktivität nur für den Zeitraum anzuzeigen, in dem die Aktivität aktiv war. Die Daten sollten bei der Ansicht der Aktivität in [!DNL Analytics] standardmäßig korrekt eingestellt werden. Sofern Sie das Datum nicht manuell verlängert haben, sollte dies kein Problem vom Standpunkt des Berichte sein.

Nehmen wir beispielsweise an, dass die Variable A4T nach 90 Tagen abläuft und der Test vom 1. Januar bis 15. Januar aktiv ist.

Am 1. Januar besucht der Benutzer die Seite, sieht einmal die Aktivität XYZ und hat danach fünf weitere Seitenansichten. In den nächsten zwei Wochen kehrt der Benutzer nicht zur Seite zurück. Die Daten für diesen Benutzer sehen dann wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

Der Benutzer kehrt dann am 1. Februar zurück, sieht fünf weitere Seiten, findet keine weiteren Target-Aktivitäten vor und die ursprüngliche Aktivität ist nicht mehr aktiv. Auch wenn die Aktivität nicht mehr aktiv ist, wird der Benutzer wegen der eVar-Persistenz jedoch weiterhin verfolgt. Die Daten sehen anschließend wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Individuelle Besucher |
|--- |--- |--- |--- |--- |
| XYZ | 3 | 10 | 2 | 1 |

Der Benutzer kehrt am 1. März zurück und sieht die neue Aktivität ABC. Er sieht außerdem fünf Seiten. Da Aktivität XYZ dem Benutzer weiterhin durch Persistenz folgt und dieser Benutzer dann ABC eingestellt hat, werden in Berichte zwei Zeilenelemente angezeigt:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Individuelle Besucher |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

Der Benutzer kehrt am 1. April zurück, betrachtet fünf weitere Seiten und tätigt einen Kauf. Die 90-Tage-Ablaufzeit dieses ersten eVar wird am 1. April zurückgesetzt, sodass Sie dies in Berichte sehen können. Und allen Target-Aktivitäten, die der Benutzer sieht, wird die Konversion gutgeschrieben, die Gesamtzahl der Konversionen wird jedoch dedupliziert:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Individuelle Besucher | Bestellungen |
|--- |--- |--- |--- |--- |--- |
| XYZ | 3 | 20 | 4 | 1 | 3 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Gesamt | 2 | 20 | 3 | 3 | 1 |

Da beide Erlebnisse vor der Konvertierung gesehen wurden, erhalten beide Erlebnisse eine &quot;Gutschrift&quot;für die Bestellung. Im System gab es jedoch nur eine Bestellung, was die Summe zeigt. Für [!DNL Target]-Berichte, da Sie keine [!DNL Target]-Aktivität gegen eine andere Aktivität stellen, um zu sehen, welche erfolgreicher ist, ist es egal, dass alle Aktivitäten, die der Benutzer gesehen hat, gutgeschrieben wurden. Sie vergleichen die Ergebnisse zweier Elemente innerhalb einer Aktivität. Es ist für einen Benutzer nicht möglich, verschiedene Erlebnisse auf die gleiche Aktivität zu sehen, sodass Sie sich keine Sorgen über eine Kreuzkontamination der Bestellungskredite machen müssen.

Weitere Informationen finden Sie unter [Umrechnungsvariablen (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) im *Analytics Admin Guide*.

## Warum sehe ich nach der Deaktivierung meiner Aktivität weiterhin mehr Impressionen? {#deactivated}

Eine Quelle von Impressionen für einen Bericht einer A4T-Aktivität nach der Deaktivierung kann QS-Modus-Traffic sein. Zielgruppe protokolliert normalerweise keine Ereignis für eine deaktivierte Aktivität, Analytics kann jedoch nicht erkennen, dass Impressionen aus dem QS-Modus stammen. Wenn der Bericht zur Zielgruppe-Aktivität aus Analytics abgerufen wird, werden diese Impressionen angezeigt. Dies funktioniert wie vorgesehen, da Kunden eine Möglichkeit benötigen, A4T-Berichte zu prüfen, auch wenn die Aktivität nicht im QS-Modus aktiv ist.

## Warum werden Zahlen für die Metrik &quot;Individuelle Besucher&quot;in Analytics und Analytics for Adobe Target (A4T) unterschiedlich berechnet? {#section_0C3B648AB54041F9A2AA839D51791883}

Wenn Sie einen A/B-Test ausführen, der den Student-t-Test (die Konfidenzmetrik) verwendet, um einen Gewinner auszuwählen, gilt unter anderem die Annahme, dass es einen festen Zeithorizont gibt. Der Test ist nur dann statistisch gültig, wenn Sie diese feste Stichprobengröße untersuchen.

Die Metrik [!UICONTROL Individuelle Besucher] unterscheidet sich nur dann in [!DNL Analytics] und [!DNL Target], wenn Sie einen kürzeren Zeitraum als den eigentlichen Test betrachten. Wenn die Stichprobengröße nicht erreicht wird, ist der Test nicht sehr zuverlässig. Weitere Informationen finden Sie unter [How Not to Run an A/B-Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) auf der [Website von Evan Miller](https://www.evanmiller.org/index.html).

Die Metrik [!UICONTROL Individuelle Besucher] zeigt die Anzahl der Personen an, die dem Test ausgesetzt wurden, die die Site während des angegebenen Zeitraums besucht haben. Diese Leute sind Teil des Tests und sollten gezählt werden. Wenn Sie nur die Anzahl der Personen sehen wollen, die innerhalb einer einzigen Woche betroffen waren, können Sie ein Segment der Besucher erstellen, die eine Aktivitätsimpression hatten, und dieses auf den Bericht anwenden.

Sie können den Zeitraum verkürzen, in dem die Variable [!DNL Target] auf eine Sitzung beibehalten wird; Dies ist jedoch problematisch bei Tests, bei denen das Konversions-Ereignis nicht mit der gleichen Wahrscheinlichkeit innerhalb derselben Sitzung erfolgt.

## Warum wird in Analytics derselbe Besucher manchmal bei mehreren Besuchen gezählt?   {#section_1397E972D31C4207A142E4D2D6D794A2}

In der folgenden Liste werden die Gründe erläutert, warum derselbe Besucher in mehreren Erlebnissen in [!DNL Analytics] gezählt werden könnte:

* Das [!DNL Target]-Profil ist abgelaufen, aber das [!DNL Analytics]-Cookie ist noch vorhanden. In diesem Fall bewertet [!DNL Target] den Benutzer neu, [!DNL Analytics] betrachtet den Besucher jedoch als dieselbe Person.
* Wenn der Besucher das `mbox3rdPartyId` verwendet und der anonyme Besucher mit dem Drittanbieter-ID-Profil zusammengeführt wird, könnte [!DNL Target] den Besucher in ein anderes Erlebnis setzen, das mit der Drittanbieter-ID übereinstimmt. Weitere Informationen finden Sie unter [Echtzeit-Profilsynchronisierung für mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] kann verschiedene Geräte auf andere Weise als denselben Besucher verfolgen, als  [!DNL Target] Geräte: die Einrichtung der Drittanbieter-ID in  [!DNL Target] unterscheidet sich von der in Analytics.

## Unterstützt A4T Virtual Report Suites?

Virtual Report Suites sind *nicht* in der Report Suite-Liste enthalten und Zielgruppen aus Virtual Report Suites werden in A4T-Berichten nicht unterstützt.

## Kann ich den Prozentsatz der Traffic-Zuordnung in einer Aktivität ändern, die nach der Aktivierung der Aktivität A4T verwendet?

Das Ändern des Prozentsatzes der Traffic-Zuordnung in einer Aktivität nach der Aktivierung kann zu inkonsistenten Berichten in [!DNL Analytics] führen, da sich die Änderung nur auf neue Besucher auswirkt. Wiederkehrende Besucher sind nicht betroffen.

Am besten sollten Sie die vorhandene Aktivität stoppen und dann eine neue Aktivität erstellen, anstatt den Prozentsatz nach der Aktivierung zu ändern. Berichte für die Beginn der neuen Aktivität mit neuen Besuchern und Daten von zurückkehrenden Besuchern führen nicht zu inkonsistenten Berichten.

## Wie werden Besuche in Analytics gezählt und Umrechnungsgutschriften in einer Aktivität mit automatischer Zielgruppe zugeordnet, die A4T verwendet?

Wenn sich ein Besucher für eine A4T-Aktivität qualifiziert, Ansichten enthält oder konvertiert, sendet [!DNL Target] die Daten des Ereignisses an [!DNL Analytics]. Mit diesen Ereignis-Daten kann [!DNL Analytics] Konversions-Ereignis und andere Clickstream-Ereignis, die auf der Seite stattfinden, den entsprechenden [!DNL Target]-Aktivitäten und -Erlebnissen zuordnen.

Beachten Sie hier einige Punkte, die bei der Anzeige von [!DNL Analytics]-Berichten zu beachten sind:

* Als Best Practice sollten Sie mit dem Beginn der Aktivität beginnen.
* Wenn eine Konversion außerhalb des Berichtsfensters erfolgt, ist die Konversion in [!DNL Analytics] nicht sichtbar.
* Wenn der Traffic für die Aktivitäten [!UICONTROL Auto-Zielgruppe] im &quot;Targeting&quot;-Bereich liegt, sehen Besucher möglicherweise unterschiedliche Erlebnisse von einer Sitzung zur nächsten. Wenn sich beispielsweise das Profil oder der Kontext geändert haben und [!DNL Target]-Algorithmen für maschinelles Lernen entscheiden, ist die Wahrscheinlichkeit einer Konvertierung in ein neues Erlebnis höher. Wenn Besucher von Erlebnis zu Erlebnis wechseln, wird die Anzahl der Besuche für jedes Erlebnis erhöht. Dies ist im Gegensatz zu normalen A/B-Testing-Aktivitäten, bei denen Erlebnisse über mehrere Besuche hinweg für einen Besucher Stickiness aufweisen.
* Wenn ein Besucher mehrere Erlebnisse besuchsübergreifend sieht, wird jede Konversion immer dem letzten Erlebnis zugeordnet, das der Besucher gesehen hat. Wie bereits erwähnt, erhöht sich die Anzahl der Besuche für jedes Erlebnis, das der Besucher sah. Dadurch können die Konvertierungsraten pro Erlebnis künstlich verringert werden, wenn Erlebnisse unter der Dimension &quot;[!UICONTROL Targeting]&quot;in [!DNL Adobe Analytics]-Berichten angezeigt werden.
