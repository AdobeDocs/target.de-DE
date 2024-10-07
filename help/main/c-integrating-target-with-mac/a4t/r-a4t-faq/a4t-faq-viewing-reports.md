---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Bericht; Berichte; Berichte anzeigen; Berichterstellung; Zählmethodik; Impressionen; Besucher; Besuche; Standardmetrik; Aktivitätskonversionen; unspezifisch
description: Hier finden Sie Antworten auf häufig zur Anzeige von Berichten bei der Verwendung von Analytics für [!DNL Target]  (A4T) gestellte Fragen. Mit A4T können Sie Analytics-Berichte für [!DNL Target] Aktivitäten verwenden.
title: Suchen Sie Antworten auf Fragen zur Anzeige von Berichten mit A4T?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: c747a8a0ed480130f254818e21b98addca16ca41
workflow-type: tm+mt
source-wordcount: '2539'
ht-degree: 24%

---

# Anzeigen von Berichten – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Anzeige von Berichten bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) gestellte Fragen.

## Kann ich meine [!DNL Target]-Aktivitätsdaten in [!DNL Analysis Workspace] anzeigen? {#workspace}

+++Antwort
Sie können [!DNL Analysis Workspace] verwenden, um Ihre [!DNL Target] -Aktivitäten und -Erlebnisse zu analysieren. Im Bereich [Analytics für Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de) können Sie Steigerung und Konfidenz für bis zu drei Erfolgsmetriken anzeigen. Sie können auch mithilfe von Tabellen und Visualisierungen tiefer einsteigen.

Ausführliche Informationen und Beispiele finden Sie im Tutorial [Analytics &amp; Target: Best Practices for Analysis ](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), bereitgestellt von [!UICONTROL Adobe Experience League].

+++

## Wo können Segmente in [!DNL Analysis Workspace] angewendet werden? {#segmentation}

+++Antwort
Segmente werden am häufigsten oben in einem Bedienfeld in der Segment-Dropzone verwendet. Das Segment wird auf alle Tabellen und Visualisierungen im Bereich angewendet. Diese Technik ist am nützlichsten, um zu sehen, wie sich der Test auf eine Untergruppe von Personen auswirkt (z. B. wie hat dieser Test für Personen in Großbritannien funktioniert).

Ein Segment kann auch direkt in der Freiformtabelle angeordnet werden. Beachten Sie jedoch, dass Sie es über die gesamte Tabelle hinweg überlagern müssen, um die Steigerungs- und Konfidenzberechnungen im A4T-Bedienfeld beizubehalten. Segmente auf Spaltenebene werden derzeit im Bereich nicht unterstützt.

+++

## Welches Attribution IQ-Modell wird in [!DNL Analysis Workspace] verwendet?

+++Antwort
Bei der Verwendung von [!DNL Target] Aktivitätsimpressionen und -konversionen in [!DNL Analysis Workspace] ist das &quot;Selber-Kontakt&quot;-Attribution IQ-Modell das Standardmodell, das auf die Metriken angewendet wird, um eine genaue Zählung sicherzustellen. Dieses Modell funktioniert in 99 % der Fälle gut. Sie können diese Standardzuordnung jedoch in Attribution IQ überschreiben.

+++

## Warum werden nicht verwandte Erlebnisse zurückgegeben, wenn ich ein Treffersegment für eine bestimmte [!DNL Target] -Aktivität verwende? {#activity-segmentation}

+++Antwort
Die [!DNL Target] -Variable, die an [!DNL Analytics] gesendet wird, hat einen standardmäßigen 90-Tage-Ablaufzeitraum. (Hinweis: Dieser Ablaufzeitraum kann bei Bedarf von der Kundenunterstützung angepasst werden.) Wenn Besucher während dieses Ablauffensters durch die Site navigieren, sind sie Teil vieler [!DNL Target] -Aktivitäten, die alle in der Dimension erfasst werden.

Wenn Sie Segmentierung für eine Aktivität erstellen, die in einem Treffer vorhanden sein soll, erhalten Sie alle Erlebnisse, die Teil dieser Aktivität sind, *plus* alle anderen Erlebnisse, die bei diesem Treffer bestehen bleiben.

+++

## Warum kann ich beim Konfigurieren von [!UICONTROL Goal Metrics] nicht auf [!UICONTROL Advanced Settings] zugreifen?

+++Antwort
Bei Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;und &quot;[!UICONTROL On Every Impression]&quot;. Diese Einstellungen sind *nicht* konfigurierbar.

Weitere Informationen finden Sie unter &quot;Warum kann ich beim Konfigurieren meiner Zielmetriken nicht auf die erweiterten Einstellungsoptionen zugreifen?&quot; in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Sollte ich Besucher, Besuche oder Aktivitätsimpressionen als Normalisierungsmetrik (d. h. Zählmethodologie) verwenden? {#metrics}

+++Antwort
Es gibt mehrere Optionen zur Normalisierung von Metriken in A4T-Berichten. Diese Metrik, auch als Zählmethodik bezeichnet, wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.

* ***Unique Visitors*** werden nur einmal erhöht, wenn sich ein Benutzer zum ersten Mal für eine Aktivität qualifiziert.
* ***Besuche*** erhöhen sich für jede Sitzung, sobald ein Benutzer (Unique Visitor) eine Aktivität aufruft, selbst wenn die Aktivität bei nachfolgenden Besuchen nicht angezeigt wird.
* ***Aktivitätsimpressionen*** erhöhen sich bei jeder Bereitstellung des Aktivitätsinhalts. (gemessen durch [!DNL Target]).

Wenn ein Besucher eine Seite anzeigt, die eine Aktivität enthält, wird eine Variable für diesen Besucher festgelegt, die den Namen der Aktivität enthält. Informationen zu den verschiedenen Zählmethoden finden Sie in den unten aufgeführten ausführlichen Szenarien.

Beachten Sie Folgendes:

* Der obige Metriken-Trigger, wenn ein Benutzer sich für eine Aktivität qualifiziert und Inhalt von [!DNL Target] zurückgegeben wird. Das bedeutet nicht zwingend, dass der Benutzer das Angebot gesehen hat. Wenn ein Aktivitätserlebnis sich unterhalb des angezeigten Bildschirmbereichs befindet und der Benutzer nicht nach unten scrollt, wurde das Angebot zwar von [!DNL Target] bereitgestellt, aber nicht vom Benutzer gesehen.
* [!UICONTROL Activity Impressions] (gemessen durch [!DNL Target]) und [!UICONTROL Instances] (gemessen durch [!DNL Analytics]) sind gleich, es sei denn, es gibt mehrere Mbox-Aufrufe auf derselben Seite in derselben Aktivität. Dadurch werden mehrere [!UICONTROL Activity Impressions] gezählt, aber nur ein einzelner [!UICONTROL Instance].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für Aktivitäten mit automatischem Targeting](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de) in *Adobe Target-Tutorials*.

+++

## Warum sind &quot;Aktivitätsimpressionen&quot;und &quot;Aktivitätskonversionen&quot;höher in [!DNL Analysis Workspace] als [!UICONTROL Reports & Analytics]? {#sametouch}

+++Antwort
[!DNL Reports & Analytics] wendet ein Gleichkontakt-Attributionsmodell auf &quot;Aktivitätsimpressionen&quot;und &quot;Aktivitätskonversionen&quot;an, während [!DNL Analysis Workspace] die Rohmetriken anzeigt, die aufgrund der Persistenz der Dimension [!DNL Target] überhöht erscheinen können.

Um genaue [!UICONTROL Activity Impressions] - und [!UICONTROL Activity Conversions] -Metriken in [!DNL Analysis Workspace] auszuwerten, stellen Sie sicher, dass auf beide Metriken [!UICONTROL Same Touch] -Attributionsmodelle angewendet werden. Modelle können angewendet werden, indem Sie auf das Zahnrad für die Spalteneinstellungen klicken, [!UICONTROL Non-default attribution models] aktivieren und dann [!UICONTROL Same Touch] auswählen. Weitere Informationen zur Attribution finden Sie in der Übersicht über die Attribute IQ ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) im *Leitfaden für Analytics-Tools*.[

+++

## Was bedeutet &quot;Aktivitätskonversionen&quot;, wenn der Marketingexperte während der Aktivitätseinrichtung eine [!DNL Analytics] -Metrik auswählt? {#section_F3EBACF85AF846E9B366A549AAB64356}

+++Antwort
&quot;Aktivitätskonversionen&quot;sind leer, wenn eine [!DNL Analytics] -Metrik als Konversionsmetrik für die Aktivität ausgewählt wurde.

+++

## Warum wird in den [!DNL Analytics] -Berichten &quot;nicht angegeben&quot;angezeigt? Was bedeutet das? {#unspecified}

+++Antwort
In anderen Berichten bedeutet &quot;Nicht angegeben&quot;, dass Daten einer Classification-Regel nicht entsprachen. In A4T sollte dies jedoch nie passieren. Wenn Sie „Nicht angegeben“ angezeigt bekommen, wurde der Classifications-Service noch nicht ausgeführt. Es dauert normalerweise zwischen 24 und 72 Stunden, bis Aktivitätsdaten in den Berichten angezeigt werden. Auch wenn die Aktivitäten erst zu diesem Zeitpunkt in diesem Bericht angezeigt werden, werden alle mit diesen Aktivitäten verbundenen Besucherdaten erfasst und nach Abschluss der Classification angezeigt.

Nach dem Classification-Zeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn die Classification für diese Aktivität durchgeführt wurde und im Bericht weiterhin die Zeile &quot;Nicht angegeben&quot;angezeigt wird, stellen Sie sicher, dass der Bericht keine Nicht-[!DNL Target]-Metrik verwendet, um die Daten anzuzeigen. Sofern der Bericht keine [!DNL Target]-spezifische Metrik verwendet, enthält diese Zeile &quot;Nicht angegeben&quot;Ereignisse für Aufrufe, die nicht mit [!DNL Target] verknüpft sind. Diese Zeile enthält keine mit [!DNL Target] verknüpften Informationen (z. B. Besucher/Besuche/Impressionen).

+++

## Warum werden [!DNL Target] -Metriken auch dann an [!DNL Analytics] gesendet, wenn die Aktivität deaktiviert wurde? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

+++Antwort
Die [!DNL Target] -Variable, die an [!DNL Analytics] gesendet wird, hat einen standardmäßigen 90-Tage-Ablaufzeitraum. Dieser Ablaufzeitraum kann bei Bedarf von der Kundenunterstützung angepasst werden. Diese Einstellung ist für alle Aktivitäten global, daher sollte sie nicht für einen Fall angepasst werden.

Möglicherweise werden nach dem Ablaufzeitraum [!DNL Analytics] [!DNL Target] -Variablen an  gesendet, da der Ablauf 90 Tage beträgt. Dies ist jedoch nur dann der Fall, wenn dieser Benutzer nie eine weitere A4T-aktivierte [!DNL Target] -Aktivität sieht. Wenn ein Benutzer am 45. Tag zur Site zurückkehrt und eine andere Aktivität ansieht, wird der gesamte Zähler für den A4T-eVar-Wert wieder auf 90 Tage zurückgesetzt. Das heißt, dass die erste Kampagne jetzt ab dem 1. Tag für 45 + 90 = 135 Tage fortbesteht. Wenn der Benutzer weiterhin zurückkehrt, können Sie an den Punkt gelangen, an dem Metriken in Ihren Berichten von viel älteren Aktivitäten an [!DNL Analytics] gesendet werden. Wenn Benutzer Cookies löschen und nicht zur Site zurückkehren, werden die Zahlen in dieser Aktivität zwar abgenommen, Sie können sie aber trotzdem sehen.

Das bedeutet, dass Aktivitäten bis zu 90 Tage nach dem Ende der Aktivität weiterhin Seitenansichten, Besuche usw. für Besucher erhalten, die während der Aktivität Teil der Aktivität wurden. Wenn Sie sich jedoch die Metrik [!UICONTROL Activity Impressions] ansehen, sollten nach dem Ende der Aktivität keine Impressionen mehr angezeigt werden.

Dies ist ein normales und erwartetes Verhalten. Die A4T-Variable funktioniert wie alle anderen eVars. Der Wert wird so lange dem Benutzer zugeordnet bis die Ablaufzeit erreicht ist (90 Tage). Wenn eine Aktivität also nur zwei Wochen lang aktiv ist, wird der Wert mindestens 90 Tage lang dem Benutzer zugeordnet.

Die Best Practice ist, Berichte für eine solche Aktivität nur für den Zeitraum anzuzeigen, in dem die Aktivität aktiv war. Die Daten sollten standardmäßig korrekt eingestellt werden, wenn Sie die Aktivität in [!DNL Analytics] anzeigen. Wenn Sie das Datum also nicht manuell verlängert haben, sollte dies aus Sicht der Berichterstellung kein Problem sein.

Nehmen wir beispielsweise an, die A4T-Variable läuft nach 90 Tagen ab und der Test ist vom 1. Januar bis 15. Januar aktiv.

Am 1. Januar besucht der Benutzer die Seite, sieht einmal die Aktivität XYZ und hat danach fünf weitere Seitenansichten. In den nächsten zwei Wochen kehrt der Benutzer nicht zur Seite zurück. Die Daten für diesen Benutzer sehen dann wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

Der Benutzer kehrt am 1. Februar zurück, zeigt fünf weitere Seiten an, findet keine Target-Aktivitäten mehr und die ursprüngliche Aktivität ist nicht mehr aktiv. Auch wenn die Aktivität nicht mehr aktiv ist, wird der Benutzer wegen der eVar-Persistenz jedoch weiterhin verfolgt. Die Daten sehen anschließend wie folgt aus:

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
| Gesamt | 2 | 20 | 3 | 1 | 1 |

Da beide Erlebnisse vor der Konversion gesehen wurden, erhalten beide Erlebnisse eine &quot;Gutschrift&quot;für die Bestellung. Im System gab es jedoch nur eine Bestellung, was die Summe zeigt. Für die Berichterstellung mit dem Wert [!DNL Target] ist es unwichtig, dass alle Aktivitäten, die der Benutzer gesehen hat, gutgeschrieben wurden, da Sie keine [!DNL Target] -Aktivität mit einer anderen Aktivität vergleichen, um festzustellen, welche erfolgreicher ist. Sie vergleichen die Ergebnisse zweier Elemente innerhalb der einzelnen Aktivität. Es ist für einen Benutzer nicht möglich, in derselben Aktivität unterschiedliche Erlebnisse zu sehen, sodass Sie sich keine Gedanken über eine Kreuzkontamination der Auftragskredite machen müssen.

Weitere Informationen finden Sie unter [Konversionsvariablen (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) im *Analytics-Administratorhandbuch*.

+++

## Warum sehe ich nach der Deaktivierung meiner Aktivität weiterhin zusätzliche Impressionen? {#deactivated}

+++Antwort
Eine Quelle von Impressionen auf den Bericht einer A4T-Aktivität nach der Deaktivierung kann QA-Modus-Traffic sein. Target protokolliert normalerweise keine Ereignisse für eine deaktivierte Aktivität, Analytics kann jedoch nicht erkennen, dass Impressionen aus dem QA-Modus kommen. Wenn der Target-Aktivitätsbericht aus Analytics abgerufen wird, werden diese Impressionen angezeigt. Dies funktioniert ordnungsgemäß, da Kunden eine Möglichkeit benötigen, A4T-Berichte zu überprüfen, selbst wenn die Aktivität nicht im QA-Modus aktiv ist.

+++

## Warum berechnen [!DNL Analytics] und [!UICONTROL Analytics for Adobe Target] (A4T) die Zahlen für die [!UICONTROL Unique Visitors] Metrik unterschiedlich? {#section_0C3B648AB54041F9A2AA839D51791883}

+++Antwort
Wenn Sie einen A/B-Test ausführen, bei dem der T-Test ](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} (die Konfidenzmetrik) von [Welch verwendet wird, um einen Gewinner eines Tests zu wählen, besteht eine der Annahmen darin, dass es einen festen Zeithorizont gibt. Der Test ist nur dann statistisch gültig, wenn Sie sich diese feste Stichprobengröße ansehen.

Die Metrik [!UICONTROL Unique Visitors] unterscheidet sich nur dann in [!DNL Analytics] und [!DNL Target], wenn Sie einen Zeitraum betrachten, der kürzer als der eigentliche Test ist. Wenn Sie Ihre Stichprobengröße nicht erreicht haben, ist der Test nicht so zuverlässig. Weitere Informationen finden Sie unter [How Not to Run an A/B-Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) auf der [Website von Evan Miller](https://www.evanmiller.org/index.html).

Die Metrik &quot;[!UICONTROL Unique Visitors]&quot;zeigt die Anzahl der Personen an, die dem Test ausgesetzt waren, die die Site während des angegebenen Zeitraums besucht haben. Diese Personen sind Teil des Tests und sollten gezählt werden. Wenn Sie nur die Anzahl der Personen sehen wollen, die innerhalb einer einzigen Woche betroffen waren, können Sie ein Segment der Besucher erstellen, die eine Aktivitätsimpression hatten, und dieses auf den Bericht anwenden.

Sie können die Dauer der Beibehaltung der [!DNL Target] -Variable auf eine Sitzung verkürzen. Dies ist jedoch problematisch für Tests, bei denen das Konversionsereignis nicht so wahrscheinlich innerhalb derselben Sitzung eintritt.

+++

## Warum wird derselbe Besucher in [!DNL Analytics] manchmal bei mehreren Erlebnissen gezählt? {#section_1397E972D31C4207A142E4D2D6D794A2}

+++Antwort
In der folgenden Liste werden die Gründe erläutert, aus denen derselbe Besucher in [!DNL Analytics] bei mehreren Erlebnissen gezählt werden kann:

* Das Profil [!DNL Target] ist abgelaufen, aber das Cookie [!DNL Analytics] ist noch vorhanden. In diesem Fall wertet [!DNL Target] den Benutzer erneut aus, [!DNL Analytics] betrachtet den Besucher jedoch als dieselbe Person.
* Wenn der Besucher den `mbox3rdPartyId` verwendet und der anonyme Besucher mit dem Drittanbieter-ID-Profil zusammengeführt wird, könnte [!DNL Target] den Besucher in ein anderes Erlebnis versetzen, das mit der Drittanbieter-ID übereinstimmt. Weitere Informationen finden Sie unter [Echtzeit-Profilsynchronisierung für mbox3rdPartyID](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] verfolgt möglicherweise verschiedene Geräte als denselben Besucher auf andere Weise, als [!DNL Target] diese Geräte verfolgt: Die in [!DNL Target] eingerichtete Drittanbieter-ID unterscheidet sich von der in Analytics.

+++

## Unterstützt A4T Virtual Report Suites? {#virtual}

+++Antwort
Virtual Report Suites sind zwar nicht in der Liste [!UICONTROL Report Suite] enthalten, jedoch haben alle A4T-Daten, die mit einer Report Suite geteilt werden, die mit einer Virtual Report Suite in [!DNL Analytics] verknüpft ist, Zugriff auf diese Daten. Beachten Sie, dass eine von Virtual Report Suites erstellte Zielgruppe nicht für [!DNL Target] freigegeben werden kann.

+++

## Kann ich den Prozentsatz der Traffic-Zuordnung in einer Aktivität ändern, die nach der Aktivierung der Aktivität A4T verwendet?

+++Antwort
Eine Änderung des Prozentsatzes der Traffic-Zuordnung in einer Aktivität nach der Aktivierung kann zu inkonsistenten Berichten in [!DNL Analytics] führen, da sich die Änderung nur auf neue Besucher auswirkt. Wiederkehrende Besucher sind nicht betroffen.

Am besten sollten Sie die vorhandene Aktivität stoppen und dann eine neue Aktivität erstellen, anstatt den Prozentsatz nach der Aktivierung zu ändern. Die Berichterstellung für die neue Aktivität beginnt mit neuen Besuchern und Daten von zurückkehrenden Besuchern führen nicht zu inkonsistenten Berichten.

+++

## Wie werden Besuche in [!DNL Analytics] gezählt und Konversionsgutschriften in einer [!UICONTROL Auto-Target] -Aktivität zugewiesen, die A4T verwendet?

+++Antwort
Wenn sich ein Besucher für eine A4T-Aktivität qualifiziert, Inhalte anzeigt oder konvertiert, sendet [!DNL Target] Ereignisdaten an [!DNL Analytics]. Mit diesen Ereignisdaten kann [!DNL Analytics] Konversionsereignisse und andere Clickstream-Ereignisse, die auf der Seite stattfinden, den relevanten [!DNL Target] Aktivitäten und Erlebnissen zuordnen.

Beachten Sie Folgendes bei der Anzeige von [!DNL Analytics] -Berichten:

* Als Best Practice empfiehlt sich im Allgemeinen, Ihr Berichtsfenster mit dem Anfangsdatum der Aktivität zu beginnen.
* Wenn eine Konversion außerhalb des Berichtsfensters erfolgt, ist die Konversion nicht in [!DNL Analytics] sichtbar.
* Im &quot;gezielten&quot;Teil des Traffics für [!UICONTROL Auto-Target] -Aktivitäten können Besuchern von einer Sitzung zur nächsten unterschiedliche Erlebnisse angezeigt werden. Wenn sich beispielsweise das Profil oder der Kontext geändert hat und die Algorithmen für maschinelles Lernen von [!DNL Target] entscheiden, dass sie mit höherer Wahrscheinlichkeit in ein neues Erlebnis konvertieren. Wenn Besucher von Erlebnis zu Erlebnis wechseln, wird die Besuchsanzahl für jedes angezeigte Erlebnis erhöht. Dies ist im Gegensatz zu normalen A/B-Test-Aktivitäten, bei denen Erlebnisse besuchsübergreifend für einen Besucher gebunden sind.
* Wenn einem Besucher über mehrere Besuche hinweg mehrere Erlebnisse angezeigt werden, wird jede Konversion immer dem letzten Erlebnis zugeordnet, das der Besucher gesehen hat. Wie bereits erwähnt, wird die Besuchsanzahl für jedes Erlebnis erhöht, das der Besucher gesehen hat. Dadurch können die Konversionsraten pro Erlebnis künstlich gedrückt werden, wenn Erlebnisse unter der Dimension &quot;[!UICONTROL Targeted]&quot;in [!DNL Adobe Analytics] -Berichten angezeigt werden.

+++

## Wie kann ich Aktivitätsimpressionen in [!DNL Analysis Workspace] bei Verwendung von [!UICONTROL Analytics for Target] (A4T) verfolgen? {#activity-impressions}

+++Antwort

Anzeigen von Aktivitätsimpressionen in [!DNL Analysis Workspace]:

1. Klicken Sie in der Benutzeroberfläche von [!DNL Target] auf **[!UICONTROL View in Analytics]**.
1. Fügen Sie die Spalte **[!UICONTROL Activity Impressions]** zum Bericht [[!DNL Analytics Workspace]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html){target=_blank} hinzu.
1. Klicken Sie in der Spalte **[!UICONTROL Activity Impressions]** auf das Symbol [!UICONTROL Gear] .
1. Klicken Sie auf **[!UICONTROL Use non-default attribution model]**.
1. Wählen Sie **[!UICONTROL Same Touch Model]** > **[!UICONTROL Apply]** aus.

+++
