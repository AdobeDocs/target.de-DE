---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Bericht; Berichte; Berichte anzeigen; Berichterstellung; Zählmethodik; Impressionen; Besucher; Besuche; Standardmetrik; Aktivitätskonversionen; unspezifisch
description: Hier finden Sie Antworten auf häufig zur Anzeige von Berichten bei der Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten gestellte Fragen.
title: Antworten auf Fragen zur Anzeige von Berichten mit A4T?
feature: 'Analytics for Target (A4T) '
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: 8b8091557fc1df48830bfa3211aa789b2c987f2d
workflow-type: tm+mt
source-wordcount: '2538'
ht-degree: 36%

---

# Anzeigen von Berichten – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Anzeige von Berichten bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) gestellte Fragen.

## Kann ich meine [!DNL Target]-Aktivitätsdaten in Analysis Workspace anzeigen? {#workspace}

Sie können [!DNL Analysis Workspace] verwenden, um Ihre [!DNL Target] Aktivitäten und Erlebnisse zu analysieren. Im Bedienfeld [Analytics for Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de) können Sie Steigerung und Konfidenz für bis zu drei Erfolgsmetriken anzeigen. Sie können auch mithilfe von Tabellen und Visualisierungen tiefer einsteigen.

Ausführliche Informationen und Beispiele finden Sie unter [Analytics und Target: Best Practices für Analysen-Tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), bereitgestellt von Adobe Experience League.

## Wo können Segmente in Analysis Workspace angewendet werden? {#segmentation}

Segmente werden am häufigsten oben in einem Bedienfeld in der Segment-Dropzone verwendet. Das Segment wird auf alle Tabellen und Visualisierungen im Bereich angewendet. Diese Technik ist am nützlichsten, um zu sehen, wie sich der Test auf eine Untergruppe von Personen auswirkt (z. B. wie hat dieser Test für Personen in Großbritannien funktioniert).

Ein Segment kann auch direkt in der Freiformtabelle angeordnet werden. Beachten Sie jedoch, dass Sie es über die gesamte Tabelle hinweg überlagern müssen, um die Steigerungs- und Konfidenzberechnungen im A4T-Bedienfeld beizubehalten. Segmente auf Spaltenebene werden derzeit im Bereich nicht unterstützt.

## Warum werden nicht verwandte Erlebnisse zurückgegeben, wenn ich ein Treffersegment für eine bestimmte [!DNL Target] -Aktivität verwende? {#activity-segmentation}

Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. (Hinweis: Dieser Ablaufzeitraum kann bei Bedarf von der Kundenunterstützung angepasst werden. Wenn Besucher während dieses Ablauffensters durch die Site navigieren, sind sie Teil vieler [!DNL Target] -Aktivitäten, die alle in der Dimension erfasst werden.

Wenn Sie eine Aktivität segmentieren, die in einem Treffer vorhanden sein soll, erhalten Sie alle Erlebnisse, die Teil dieser Aktivität sind *sowie* alle anderen Erlebnisse, die bei diesem Treffer bestehen bleiben.

## Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf Erweiterte Einstellungen zugreifen?

Bei Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Diese Einstellungen sind *nicht* konfigurierbar.

Weitere Informationen finden Sie unter &quot;Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die erweiterten Einstellungsoptionen zugreifen?&quot; in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Sollte ich Besucher, Besuche oder Aktivitätsimpressionen als Normalisierungsmetrik (d. h. Zählmethodologie) verwenden? {#metrics}

Es gibt mehrere Optionen zur Normalisierung von Metriken in A4T-Berichten. Diese Metrik, auch als Zählmethodik bezeichnet, wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.

* ***Unique Visitors*** wird um eins erhöht, wenn ein Benutzer sich zum ersten Mal für eine Aktivität qualifiziert.
* ***Besuche*** wird mit jeder Sitzung erhöht, sobald ein Benutzer (Unique Visitor) eine Aktivität beginnt, selbst wenn diese Aktivität nicht in nachfolgenden Besuchen angezeigt wird.
* ***Aktivitätsimpressionen*** wird jedes Mal erhöht, wenn Aktivitätsinhalt bereitgestellt wird. (Gemessen durch [!DNL Target]).

Wenn ein Besucher eine Seite anzeigt, die eine Aktivität enthält, wird eine Variable für diesen Besucher festgelegt, die den Namen der Aktivität enthält. Informationen zu den verschiedenen Zählmethoden finden Sie in den unten aufgeführten ausführlichen Szenarien.

Beachten Sie Folgendes:

* Der obige Metriken-Trigger, wenn ein Benutzer sich für eine Aktivität qualifiziert und Inhalt von [!DNL Target] zurückgegeben wird. Das bedeutet nicht zwingend, dass der Benutzer das Angebot gesehen hat. Wenn ein Aktivitätserlebnis sich unterhalb des angezeigten Bildschirmbereichs befindet und der Benutzer nicht nach unten scrollt, wurde das Angebot zwar von [!DNL Target] bereitgestellt, aber nicht vom Benutzer gesehen.
* [!UICONTROL Aktivitätsimpressionen] (gemessen durch [!DNL Target]) und [!UICONTROL Instanzen] (gemessen durch [!DNL Analytics]) sind gleich, sofern nicht mehrere Mbox-Aufrufe auf derselben Seite in derselben Aktivität vorhanden sind. Hierdurch werden mehrere [!UICONTROL Aktivitätsimpressionen] gezählt, aber nur eine [!UICONTROL Instanz].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target-Tutorials*.

## Warum sind &quot;Aktivitätsimpressionen&quot;und &quot;Aktivitätskonversionen&quot;in Analysis Workspace höher als in Reports &amp; Analytics? {#sametouch}

[!DNL Reports & Analytics] wendet ein Gleichkontakt-Attributionsmodell auf &quot;Aktivitätsimpressionen&quot;und &quot;Aktivitätskonversionen&quot;an, während die Rohmetriken  [!DNL Analysis Workspace] angezeigt werden, die aufgrund der Persistenz der  [!DNL Target] Dimension überhöht erscheinen können.

Um genaue [!UICONTROL Aktivitätsimpressionen] und [!UICONTROL Aktivitätskonversionen] -Metriken in [!DNL Analysis Workspace] auszuwerten, stellen Sie sicher, dass auf beide Metriken die Attributionsmodelle [!UICONTROL Selber Kontakt] angewendet werden. Modelle können angewendet werden, indem Sie auf das Zahnradsymbol der Spalte klicken, [!UICONTROL Nicht standardmäßige Attributionsmodelle] aktivieren und [!UICONTROL Same Touch] auswählen. Weitere Informationen zur Attribution finden Sie unter [Übersicht über Attribute IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) im *Leitfaden für Analytics-Tools*.

## Was bedeutet „Aktivitätskonversionen“, wenn der Marketingexperte beim Setup einer Aktivität eine Analytics-Metrik auswählt? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Aktivitätskonversionen&quot;sind leer, wenn eine [!DNL Analytics] -Metrik als Konversionsmetrik für die Aktivität ausgewählt wurde.

## Warum steht in den Analytics-Berichten „Nicht angegeben“? Was bedeutet das? {#unspecified}

In anderen Berichten bedeutet „Nicht angegeben“, dass Daten eine bestimmte Classification nicht erfüllt haben. Dies sollte jedoch in A4T nie passieren. Wenn Sie „Nicht angegeben“ angezeigt bekommen, wurde der Classifications-Service noch nicht ausgeführt. Es dauert normalerweise zwischen 24 und 72 Stunden, bis Aktivitätsdaten in den Berichten angezeigt werden. Auch wenn die Aktivitäten erst zu diesem Zeitpunkt in diesem Bericht angezeigt werden, werden alle mit diesen Aktivitäten verbundenen Besucherdaten erfasst und nach Abschluss der Classification angezeigt.

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn die Classification für diese Aktivität durchgeführt wurde und im Bericht weiterhin die Zeile &quot;Nicht angegeben&quot;angezeigt wird, stellen Sie sicher, dass der Bericht keine Nicht-[!DNL Target]-Metrik zur Anzeige der Daten verwendet. Sofern der Bericht keine [!DNL Target]-spezifische Metrik verwendet, enthält diese Zeile &quot;Nicht angegeben&quot;Ereignisse für Aufrufe, die nicht mit [!DNL Target] verknüpft sind. Diese Zeile enthält keine [!DNL Target]-verknüpften Informationen (z. B. Besucher/Besuche/Impressionen).

## Warum werden [!DNL Target]-Metriken auch nach der Deaktivierung der Aktivität an Analytics gesendet? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. Dieser Ablaufzeitraum kann bei Bedarf von der Kundenunterstützung angepasst werden. Diese Einstellung gilt für alle Aktivitäten, daher sollte sie nicht nur für einen Fall angepasst werden.

Es können [!DNL Target] -Variablen angezeigt werden, die nach dem Ablaufzeitraum an [!DNL Analytics] gesendet werden, da der Ablauf 90 Tage beträgt. Dies ist jedoch nur dann der Fall, wenn der Benutzer keine andere A4T-fähige [!DNL Target] -Aktivität sieht. Wenn ein Benutzer am 45. Tag zur Site zurückkehrt und eine andere Aktivität ansieht, wird der gesamte Zähler für den A4T-eVar-Wert wieder auf 90 Tage zurückgesetzt. Das heißt, dass die erste Kampagne jetzt ab dem 1. Tag für 45 + 90 = 135 Tage fortbesteht. Wenn der Benutzer weiterhin zurückkehrt, können Sie an den Punkt gelangen, an dem Metriken von viel älteren Aktivitäten an [!DNL Analytics] in Ihren Berichten gesendet werden. Wenn Benutzer Cookies löschen und nicht zur Site zurückkehren, werden die Zahlen in dieser Aktivität zurückgesetzt, aber Sie können sie weiterhin sehen.

Das bedeutet, dass Aktivitäten bis zu 90 Tage nach dem Ende der Aktivität weiterhin Seitenansichten, Besuche usw. für Besucher erhalten, die während der Aktivität Teil der Aktivität wurden. Sollten Sie jedoch einen Blick auf die Metrik [!UICONTROL Aktivitätsimpressionen] werfen, sollten nach Ablauf der Aktivität keine weiteren Impressionen erfasst werden.

Dies ist ein normales und erwartetes Verhalten. Die A4T-Variable funktioniert wie alle anderen eVars. Der Wert wird so lange dem Benutzer zugeordnet bis die Ablaufzeit erreicht ist (90 Tage). Wenn eine Aktivität also nur zwei Wochen lang aktiv ist, wird der Wert mindestens 90 Tage lang dem Benutzer zugeordnet.

Die Best Practice ist, Berichte für eine solche Aktivität nur für den Zeitraum anzuzeigen, in dem die Aktivität aktiv war. Die Daten sollten standardmäßig korrekt eingestellt sein, wenn Sie die Aktivität in [!DNL Analytics] anzeigen. Wenn Sie das Datum also nicht manuell verlängert haben, sollte dies aus der Sicht der Berichterstellung kein Problem sein.

Nehmen wir beispielsweise an, die A4T-Variable läuft nach 90 Tagen ab und der Test ist vom 1. Januar bis 15. Januar aktiv.

Am 1. Januar besucht der Benutzer die Seite, sieht einmal die Aktivität XYZ und hat danach fünf weitere Seitenansichten. In den nächsten zwei Wochen kehrt der Benutzer nicht zur Seite zurück. Die Daten für diesen Benutzer sehen dann wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

Der Benutzer kehrt dann am 1. Februar zurück, sieht fünf weitere Seiten, findet keine weiteren Target-Aktivitäten vor und die ursprüngliche Aktivität ist nicht mehr aktiv. Auch wenn die Aktivität nicht mehr aktiv ist, wird der Benutzer wegen der eVar-Persistenz jedoch weiterhin verfolgt. Die Daten sehen anschließend wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

Der Benutzer kehrt am 1. März zurück und sieht die neue Aktivität ABC. Er sieht außerdem fünf Seiten. Da die Aktivität XYZ den Benutzer weiterhin durch Persistenz verfolgt und für diesen Benutzer dann ABC festgelegt ist, werden in der Berichterstellung zwei Zeileneinträge angezeigt:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

Der Benutzer kehrt am 1. April zurück, betrachtet fünf weitere Seiten und tätigt einen Kauf. Die 90-Tage-Gültigkeit dieses ersten eVar wird am 1. April zurückgesetzt, sodass Sie dies in der Berichterstellung sehen. Und allen Target-Aktivitäten, die der Benutzer sieht, wird die Konversion gutgeschrieben, die Gesamtzahl der Konversionen wird jedoch dedupliziert:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors | Bestellungen |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Gesamt | 2 | 20 | 1 | 1 | 1 |

Da beide Erlebnisse vor der Konversion gesehen wurden, erhalten beide Erlebnisse eine &quot;Gutschrift&quot;für die Bestellung. Im System gab es jedoch nur eine Bestellung, was die Summe zeigt. Bei der [!DNL Target]-Berichterstellung ist es unwichtig, dass alle Aktivitäten, die der Benutzer gesehen hat, gutgeschrieben wurden, da Sie eine [!DNL Target] -Aktivität nicht mit einer anderen Aktivität vergleichen, um zu sehen, welche erfolgreicher ist. Sie vergleichen die Ergebnisse zweier Elemente innerhalb der einzelnen Aktivität. Es ist für einen Benutzer nicht möglich, in derselben Aktivität unterschiedliche Erlebnisse zu sehen, sodass Sie sich keine Gedanken über eine Kreuzkontamination der Auftragskredite machen müssen.

Weitere Informationen finden Sie unter [Konversionsvariablen (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) im *Analytics Admin Guide*.

## Warum sehe ich nach der Deaktivierung meiner Aktivität weiterhin zusätzliche Impressionen? {#deactivated}

Eine Quelle von Impressionen auf den Bericht einer A4T-Aktivität nach der Deaktivierung kann QA-Modus-Traffic sein. Target protokolliert normalerweise keine Ereignisse für eine deaktivierte Aktivität, Analytics kann jedoch nicht erkennen, dass Impressionen aus dem QA-Modus kommen. Wenn der Target-Aktivitätsbericht aus Analytics abgerufen wird, werden diese Impressionen angezeigt. Dies funktioniert ordnungsgemäß, da Kunden eine Möglichkeit benötigen, A4T-Berichte zu überprüfen, selbst wenn die Aktivität nicht im QA-Modus aktiv ist.

## Warum berechnen Analytics und Analytics for Adobe Target (A4T) die Zahlen für die Metrik &quot;Unique Visitors&quot;unterschiedlich? {#section_0C3B648AB54041F9A2AA839D51791883}

Wenn Sie einen A/B-Test ausführen, der den Student-t-Test (die Konfidenzmetrik) verwendet, um einen Gewinner auszuwählen, gilt unter anderem die Annahme, dass es einen festen Zeithorizont gibt. Der Test ist nur dann statistisch gültig, wenn Sie diese feste Stichprobengröße untersuchen.

Die Metrik [!UICONTROL Unique Visitors] unterscheidet sich in [!DNL Analytics] und [!DNL Target] nur, wenn Sie einen Zeitraum betrachten, der kürzer als der aktuelle Test ist. Wenn die Stichprobengröße nicht erreicht wird, ist der Test nicht sehr zuverlässig. Weitere Informationen finden Sie unter [How Not to Run an A/B-Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) auf der [Website von Evan Miller](https://www.evanmiller.org/index.html).

Die Metrik [!UICONTROL Unique Visitors] zeigt die Anzahl der Personen an, die dem Test ausgesetzt waren, die die Site während des angegebenen Zeitraums besucht haben. Diese Personen sind Teil des Tests und sollten gezählt werden. Wenn Sie nur die Anzahl der Personen sehen wollen, die innerhalb einer einzigen Woche betroffen waren, können Sie ein Segment der Besucher erstellen, die eine Aktivitätsimpression hatten, und dieses auf den Bericht anwenden.

Sie können die Dauer verkürzen, die die Variable [!DNL Target] auf eine Sitzung beibehalten wird. Dies ist jedoch problematisch für Tests, bei denen das Konversionsereignis nicht so wahrscheinlich innerhalb derselben Sitzung eintritt.

## Warum wird in Analytics derselbe Besucher manchmal bei mehreren Besuchen gezählt?  {#section_1397E972D31C4207A142E4D2D6D794A2}

In der folgenden Liste werden die Gründe erläutert, aus denen derselbe Besucher in [!DNL Analytics] in mehreren Erlebnissen gezählt werden kann:

* Das Profil [!DNL Target] ist abgelaufen, aber das [!DNL Analytics]-Cookie ist noch vorhanden. In diesem Fall bewertet [!DNL Target] den Benutzer erneut, [!DNL Analytics] betrachtet den Besucher jedoch als dieselbe Person.
* Wenn der Besucher das `mbox3rdPartyId` verwendet, könnte [!DNL Target] den Besucher bei der Zusammenführung des anonymen Besuchers mit dem Drittanbieter-ID-Profil in ein anderes Erlebnis versetzen, das mit der Drittanbieter-ID übereinstimmt. Weitere Informationen finden Sie unter [Echtzeit-Profilsynchronisierung für mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] kann verschiedene Geräte als derselbe Besucher auf andere Weise verfolgen, als diese Geräte zu  [!DNL Target] verfolgen: die Einrichtung der Drittanbieter-ID in  [!DNL Target] sich von der in Analytics unterscheidet.

## Unterstützt A4T Virtual Report Suites? {#virtual}

Virtual Report Suites sind zwar nicht in der Liste [!UICONTROL Report Suite] enthalten, jedoch haben alle A4T-Daten, die mit einer Report Suite geteilt werden, die mit einer Virtual Report Suite in [!DNL Analytics] verknüpft ist, Zugriff auf diese Daten. Beachten Sie, dass eine von Virtual Report Suites erstellte Zielgruppe nicht für [!DNL Target] freigegeben werden kann.

## Kann ich den Prozentsatz der Traffic-Zuordnung in einer Aktivität ändern, die nach der Aktivierung der Aktivität A4T verwendet?

Das Ändern des Prozentsatzes der Traffic-Zuordnung in einer Aktivität nach der Aktivierung kann zu inkonsistenten Berichten in [!DNL Analytics] führen, da sich die Änderung nur auf neue Besucher auswirkt. Wiederkehrende Besucher sind nicht betroffen.

Am besten sollten Sie die vorhandene Aktivität stoppen und dann eine neue Aktivität erstellen, anstatt den Prozentsatz nach der Aktivierung zu ändern. Die Berichterstellung für die neue Aktivität beginnt mit neuen Besuchern und Daten von zurückkehrenden Besuchern führen nicht zu inkonsistenten Berichten.

## Wie werden Besuche in Analytics gezählt und Konversionsgutschriften in einer Aktivität vom Typ Automatisches Targeting zugewiesen, die A4T verwendet?

Wenn sich ein Besucher für eine A4T-Aktivität qualifiziert, Inhalte anzeigt oder konvertiert, sendet [!DNL Target] Ereignisdaten an [!DNL Analytics]. Mit diesen Ereignisdaten kann [!DNL Analytics] Konversionsereignisse und andere Clickstream-Ereignisse, die auf der Seite stattfinden, den relevanten [!DNL Target] -Aktivitäten und -Erlebnissen zuordnen.

Beachten Sie Folgendes bei der Anzeige von [!DNL Analytics]-Berichten:

* Als Best Practice empfiehlt sich im Allgemeinen, Ihr Berichtsfenster mit dem Anfangsdatum der Aktivität zu beginnen.
* Wenn eine Konversion außerhalb des Berichtsfensters erfolgt, ist die Konversion nicht in [!DNL Analytics] sichtbar.
* Im &quot;Targeting&quot;-Teil des Traffics für [!UICONTROL Automatisches Targeting]-Aktivitäten können Besucher von einer Sitzung zur nächsten unterschiedliche Erlebnisse sehen. Wenn sich beispielsweise das Profil oder der Kontext geändert hat und die Algorithmen für maschinelles Lernen von [!DNL Target] entscheiden, dass sie mit höherer Wahrscheinlichkeit in ein neues Erlebnis konvertieren. Wenn Besucher von Erlebnis zu Erlebnis wechseln, wird die Besuchsanzahl für jedes angezeigte Erlebnis erhöht. Dies ist im Gegensatz zu normalen A/B-Test-Aktivitäten, bei denen Erlebnisse besuchsübergreifend für einen Besucher gebunden sind.
* Wenn einem Besucher über mehrere Besuche hinweg mehrere Erlebnisse angezeigt werden, wird jede Konversion immer dem letzten Erlebnis zugeordnet, das der Besucher gesehen hat. Wie bereits erwähnt, wird die Besuchsanzahl für jedes Erlebnis erhöht, das der Besucher gesehen hat. Dadurch können die Konversionsraten pro Erlebnis künstlich gedrückt werden, wenn Erlebnisse unter der Dimension &quot;[!UICONTROL Targeted]&quot;in [!DNL Adobe Analytics] -Berichten angezeigt werden.
