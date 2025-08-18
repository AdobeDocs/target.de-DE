---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Bericht; Berichte; Berichte anzeigen; Berichterstellung; Zählmethodik; Impressionen; Besucher; Besuche; Standardmetrik; Aktivitätskonversionen; unspezifisch
description: Hier finden Sie Antworten auf Fragen, die häufig zum Anzeigen von Berichten bei der Verwendung von Analytics for [!DNL Target] (A4T) gestellt werden. Mit A4T können Sie Analytics-Berichte für - [!DNL Target]  verwenden.
title: Hier finden Sie Antworten auf Fragen zur Anzeige von Berichten mit A4T?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: c747a8a0ed480130f254818e21b98addca16ca41
workflow-type: tm+mt
source-wordcount: '2539'
ht-degree: 26%

---

# Anzeigen von Berichten – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zum Anzeigen von Berichten gestellt werden, wenn [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) verwendet wird.

## Kann ich meine [!DNL Target] Aktivitätsdaten in [!DNL Analysis Workspace] anzeigen? {#workspace}

+++Antwort
Sie können [!DNL Analysis Workspace] verwenden, um Ihre [!DNL Target] Aktivitäten und Erlebnisse zu analysieren. Im [Bedienfeld „Analytics for ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de)&quot; können Sie Steigerung und Konfidenz für bis zu drei Erfolgsmetriken anzeigen. Mithilfe von Tabellen und Visualisierungen können Sie auch tiefer gehen.

Detaillierte Informationen und Beispiele finden Sie im Tutorial [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) von [!UICONTROL Adobe Experience League].

+++

## Wo können Segmente in [!DNL Analysis Workspace] angewendet werden? {#segmentation}

+++Antwort
Segmente werden am häufigsten am oberen Rand eines Bedienfelds in der Segment-Ablagefläche verwendet. Das Segment wird auf alle Tabellen und Visualisierungen im Bedienfeld angewendet. Diese Technik ist am nützlichsten, um festzustellen, wie sich der Test auf eine Untergruppe von Personen auswirkt (wie hat beispielsweise dieser Test bei Personen in Großbritannien funktioniert).

Ein Segment kann auch direkt in der Freiformtabelle überlagert werden. Beachten Sie jedoch, dass Sie es über die gesamte Tabelle hinweg überlagern müssen, um die Berechnungen für Steigerung und Konfidenz im A4T-Bedienfeld beizubehalten. Segmente auf Spaltenebene werden derzeit nicht im Bedienfeld unterstützt.

+++

## Welches Attribution IQ-Modell wird in [!DNL Analysis Workspace] verwendet?

+++Antwort
Bei Verwendung [!DNL Target] Aktivitätsimpressionen und Konversionen in [!DNL Analysis Workspace] ist das Attribution IQ-Modell „Same Touch“ das Standardmodell, das auf die Metriken angewendet wird, um eine genaue Zählung sicherzustellen. Dieses Modell funktioniert in 99 % der Fälle gut. Sie können diese Standardzuordnung jedoch in Attribution IQ überschreiben.

+++

## Warum werden nicht verwandte Erlebnisse zurückgegeben, wenn ich ein Treffersegment für eine bestimmte [!DNL Target]-Aktivität anwende? {#activity-segmentation}

+++Antwort
Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. (Hinweis: Dieser Gültigkeitszeitraum kann bei Bedarf von der Kundenunterstützung angepasst werden.) Wenn Besucher durch dieses Gültigkeitsfenster auf der Website navigieren, sind sie Teil vieler [!DNL Target] Aktivitäten, die alle in der Dimension erfasst werden.

Wenn Sie ein Segment für eine Aktivität erstellen, um in einem Treffer vorhanden zu sein, erhalten Sie alle Erlebnisse, die Teil dieser Aktivität sind *plus* alle anderen Erlebnisse, die in diesem Treffer persistent sind.

+++

## Warum kann ich beim Konfigurieren meiner [!UICONTROL Goal Metrics] nicht auf [!UICONTROL Advanced Settings] zugreifen?

+++Antwort
Bei Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, verwendet die Zielmetrik die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; und &quot;[!UICONTROL On Every Impression]&quot;. Diese Einstellungen *nicht*.

Weitere Informationen finden Sie unter „Warum kann ich bei der Konfiguration meiner Zielmetriken nicht auf die erweiterten Einstellungen zugreifen?“. in [Metrikdefinitionen - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Sollte ich Besucher, Besuche oder Aktivitätsimpressionen als Normalisierungsmetrik verwenden (d. h. Zählmethodik)? {#metrics}

+++Antwort
Es gibt mehrere Optionen zum Normalisieren von Metriken in A4T-Berichten. Diese Metrik, auch als Zählmethodik bezeichnet, wird zum Nenner der Aufstiegsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.

* ***Unique Visitors*** wird einmal inkrementiert, wenn sich ein Benutzer zum ersten Mal für eine Aktivität qualifiziert.
* ***Besuche*** erhöhen sich für jede Sitzung, sobald ein Benutzer (Unique Visitor) in eine Aktivität eintritt, auch wenn die Aktivität bei nachfolgenden Besuchen nicht angezeigt wird.
* ***Aktivitätsimpressionen*** erhöhen sich bei jeder Bereitstellung von Aktivitätsinhalten. (Gemessen nach [!DNL Target]).

Wenn ein Besucher eine Seite anzeigt, die eine Aktivität enthält, wird eine Variable für diesen Besucher festgelegt, die den Namen der Aktivität enthält. Informationen zu den verschiedenen Zählmethoden finden Sie in den unten aufgeführten ausführlichen Szenarien.

Beachten Sie Folgendes:

* Der obige Metrik-Trigger tritt auf, wenn ein Benutzer für eine Aktivität qualifiziert ist und Inhalte von [!DNL Target] zurückgegeben werden. Das bedeutet nicht zwingend, dass der Benutzer das Angebot gesehen hat. Wenn ein Aktivitätserlebnis sich unterhalb des angezeigten Bildschirmbereichs befindet und der Benutzer nicht nach unten scrollt, wurde das Angebot zwar von [!DNL Target] bereitgestellt, aber nicht vom Benutzer gesehen.
* [!UICONTROL Activity Impressions] (gemessen durch [!DNL Target]) und [!UICONTROL Instances] (gemessen durch [!DNL Analytics]) sind gleich, es sei denn, es gibt mehrere Mbox-Aufrufe auf derselben Seite in derselben Aktivität. Dies führt dazu, dass mehrere [!UICONTROL Activity Impressions] gezählt werden, jedoch nur eine einzige [!UICONTROL Instance].

Weitere Informationen finden Sie unter [Einrichten von A4T-Berichten in Analysis Workspace für automatische Targeting-Aktivitäten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de) in *Adobe Target-Tutorials*.

+++

## Warum sind „Aktivitätsimpressionen“ und „Aktivitätskonversionen“ in [!DNL Analysis Workspace] höher als [!UICONTROL Reports & Analytics]? {#sametouch}

+++Antwort
[!DNL Reports & Analytics] wendet ein Attributionsmodell für denselben Kontakt auf „Aktivitätsimpressionen“ und „Aktivitätskonversionen“ an, während [!DNL Analysis Workspace] die Rohmetriken anzeigt, die aufgrund der Persistenz der [!DNL Target] Dimension überhöht erscheinen können.

Um genaue [!UICONTROL Activity Impressions] und [!UICONTROL Activity Conversions] Metriken in [!DNL Analysis Workspace] auszuwerten, stellen Sie sicher, dass auf beide Metriken [!UICONTROL Same Touch] Attributionsmodelle angewendet wurden. Modelle können angewendet werden, indem Sie auf das Zahnrad für die Spalteneinstellungen klicken, [!UICONTROL Non-default attribution models] aktivieren und dann [!UICONTROL Same Touch] auswählen. Weitere Informationen zur Attribution finden Sie unter [Attributes IQ - Übersicht](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) im *Handbuch zu Analytics-Tools*.

+++

## Was bedeutet „Aktivitätskonversionen“, wenn der Marketing-Experte bei der Einrichtung der Aktivität eine [!DNL Analytics] Metrik auswählt? {#section_F3EBACF85AF846E9B366A549AAB64356}

+++Antwort
„Aktivitätskonversionen“ sind leer, wenn eine [!DNL Analytics] als Konversionsmetrik für die Aktivität ausgewählt wurde.

+++

## Warum wird in den [!DNL Analytics] Berichten „nicht spezifiziert“ angezeigt? Was bedeutet das? {#unspecified}

+++Antwort
In anderen Berichten bedeutet „Nicht angegeben“, dass Daten eine bestimmte Classification nicht erfüllt haben. Dies sollte jedoch in A4T nie passieren. Wenn Sie „Nicht angegeben“ angezeigt bekommen, wurde der Classifications-Service noch nicht ausgeführt. Es dauert normalerweise zwischen 24 und 72 Stunden, bis Aktivitätsdaten in den Berichten angezeigt werden. Obwohl die Aktivitäten erst zu diesem Zeitpunkt in diesem Bericht angezeigt werden, werden alle mit diesen Aktivitäten verknüpften Besucherdaten erfasst und nach Abschluss der Klassifizierung angezeigt.

Nach dem Classification-Zeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Falls für diese Aktivität eine Klassifizierung durchgeführt wurde und im Bericht weiterhin eine Zeile „Unspecified“ angezeigt wird, stellen Sie sicher, dass der Bericht keine Metrik vom Typ „Nicht [!DNL Target]&quot; verwendet, um die Daten anzuzeigen. Sofern der Bericht keine [!DNL Target] Metrik verwendet, enthält diese Zeile „Unspecified“ Ereignisse für Aufrufe, die nicht mit [!DNL Target] verbunden sind. Diese Zeile enthält keine [!DNL Target] Informationen (z. B. Besucher/Besuche/Impressionen).

+++

## Warum werden [!DNL Target] Metriken an [!DNL Analytics] gesendet, selbst wenn die Aktivität deaktiviert wurde? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

+++Antwort
Die [!DNL Target]-Variable, die an [!DNL Analytics] gesendet wird, verfällt standardmäßig automatisch nach 90 Tagen. Dieser Gültigkeitszeitraum kann bei Bedarf von der Kundenunterstützung angepasst werden. Diese Einstellung ist für alle Aktivitäten global, sollte jedoch nicht für einen Fall angepasst werden.

Möglicherweise werden [!DNL Target] Variablen angezeigt, die nach dem Gültigkeitszeitraum an [!DNL Analytics] gesendet werden, da der Gültigkeitszeitraum 90 Tage beträgt, jedoch nur, wenn dieser Benutzer nie eine andere A4T-aktivierte [!DNL Target]-Aktivität sieht. Wenn ein Benutzer am 45. Tag zur Site zurückkehrt und eine andere Aktivität ansieht, wird der gesamte Zähler für den A4T-eVar-Wert wieder auf 90 Tage zurückgesetzt. Das heißt, dass die erste Kampagne jetzt ab dem 1. Tag für 45 + 90 = 135 Tage fortbesteht. Wenn der/die Benutzende immer wieder zurückkehrt, gelangt er/sie möglicherweise zu dem Punkt, an dem Metriken aus wesentlich älteren Aktivitäten in Berichten an [!DNL Analytics] gesendet werden. Wenn Benutzer Cookies löschen und nicht zur Website zurückkehren, sinken die Zahlen in dieser Aktivität, aber Sie können sie weiterhin sehen.

Das bedeutet, dass bei -Aktivitäten weiterhin Seitenansichten, Besuche usw. für bis zu 90 Tage nach dem Ende der Aktivität für Besuchende angezeigt werden, die während ihrer Aktivität Teil der Aktivität wurden. Wenn Sie sich jedoch die [!UICONTROL Activity Impressions] Metrik ansehen, sollten Sie nach dem Ende der Aktivität keine Impressions sehen.

Dies ist ein normales und erwartetes Verhalten. Die A4T-Variable funktioniert wie alle anderen eVars. Der Wert wird so lange dem Benutzer zugeordnet bis die Ablaufzeit erreicht ist (90 Tage). Wenn eine Aktivität also nur zwei Wochen lang aktiv ist, wird der Wert mindestens über die nächsten 90 Tage mit dem Benutzer verknüpft.

Die Best Practice ist, Berichte für eine solche Aktivität nur für den Zeitraum anzuzeigen, in dem die Aktivität aktiv war. Die Datumsangaben sollten standardmäßig korrekt festgelegt werden, wenn Sie die Aktivität in [!DNL Analytics] anzeigen. Wenn Sie das Datum also nicht manuell verlängert haben, sollte dies aus Sicht des Reportings kein Problem sein.

Nehmen wir als Beispiel an, dass die A4T-Variable nach 90 Tagen abläuft und der Test vom 1. Januar bis zum 15. Januar aktiv ist.

Am 1. Januar besucht der Benutzer die Seite, sieht einmal die Aktivität XYZ und hat danach fünf weitere Seitenansichten. In den nächsten zwei Wochen kehrt der Benutzer nicht zur Seite zurück. Die Daten für diesen Benutzer sehen dann wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

Der/die Benutzende kehrt am 1. Februar zurück, zeigt fünf weitere Seiten an und erreicht keine Target-Aktivitäten mehr, und die ursprüngliche Aktivität ist nicht mehr aktiv. Auch wenn die Aktivität nicht mehr aktiv ist, wird der Benutzer wegen der eVar-Persistenz jedoch weiterhin verfolgt. Die Daten sehen anschließend wie folgt aus:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

Der Benutzer kehrt am 1. März zurück und sieht die neue Aktivität ABC. Er sieht außerdem fünf Seiten. Da die Aktivität XYZ dem Benutzer noch durch Persistenz folgt und dieser Benutzer dann ABC gesetzt hat, werden im Reporting zwei Zeileneinträge angezeigt:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

Der Benutzer kehrt am 1. April zurück, betrachtet fünf weitere Seiten und tätigt einen Kauf. Der 90-tägige Ablauf dieses ersten eVar-Werts wird am 1. April zurückgesetzt, dies wird also in Berichten angezeigt. Und allen Target-Aktivitäten, die der Benutzer sieht, wird die Konversion gutgeschrieben, die Gesamtzahl der Konversionen wird jedoch dedupliziert:

| Aktivitätsname | Instanzen (Impressionen) | Seitenansichten | Besuche | Unique Visitors | Bestellungen |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Gesamt | 2 | 20 | 3 | 1 | 1 |

Da beide Erlebnisse vor der Konversion gesehen wurden, erhalten beide „Anerkennung“ für die Bestellung. Im System gab es jedoch nur eine Bestellung, was die Summe zeigt. Da Sie für [!DNL Target] Reporting keine [!DNL Target] Aktivität mit einer anderen Aktivität vergleichen, um festzustellen, welche Aktivität erfolgreicher ist, ist es egal, ob alle Aktivitäten, die der/die Benutzende gesehen hat, gutgeschrieben wurden. Sie vergleichen die Ergebnisse von zwei Elementen innerhalb der einzelnen Aktivität. Es ist für einen Benutzer nicht möglich, verschiedene Erlebnisse in derselben Aktivität zu sehen, sodass Sie sich keine Sorgen über eine Kreuzkontamination des Bestellguthabens machen müssen.

Weitere Informationen finden Sie unter [Konversionsvariablen (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) im *Analytics-Administratorhandbuch*.

+++

## Warum sehe ich nach der Deaktivierung meiner Aktivität weiterhin zusätzliche Impressionen? {#deactivated}

+++Antwort
Eine Quelle von Impressionen für den Bericht einer A4T-Aktivität nach der Deaktivierung kann Traffic im QA-Modus sein. Target protokolliert normalerweise keine Ereignisse für eine deaktivierte Aktivität, aber Analytics hat keine Möglichkeit herauszufinden, ob Impressionen aus dem QA-Modus stammen. Wenn der Target-Aktivitätsbericht von Analytics abgerufen wird, werden diese Impressionen angezeigt. Dies funktioniert wie vorgesehen, da Kunden eine Möglichkeit benötigen, A4T-Berichte zu überprüfen, selbst wenn die Aktivität im QA-Modus nicht aktiv ist.

+++

## Warum berechnen [!DNL Analytics] und [!UICONTROL Analytics for Adobe Target] (A4T) die Zahlen für die [!UICONTROL Unique Visitors] Metrik unterschiedlich? {#section_0C3B648AB54041F9A2AA839D51791883}

+++Antwort
Wenn Sie einen A/B-Test durchführen, der den [Welch-t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} (die Konfidenzmetrik) verwendet, um einen Testsieger auszuwählen, besteht eine der Annahmen darin, dass es einen festen Zeitrahmen gibt. Der Test ist statistisch nicht gültig, es sei denn, Sie betrachten diese feste Stichprobengröße.

Die [!UICONTROL Unique Visitors] Metrik unterscheidet sich in [!DNL Analytics] und [!DNL Target] nur, wenn Sie einen Zeitraum betrachten, der kürzer ist als der eigentliche Test. Wenn Sie Ihre Stichprobengröße nicht erreicht haben, ist der Test nicht so zuverlässig. Weitere Informationen finden Sie unter [How Not to Run an A/B-Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) auf der [Website von Evan Miller](https://www.evanmiller.org/index.html).

Die [!UICONTROL Unique Visitors] Metrik zeigt die Anzahl der Personen an, die dem Test ausgesetzt waren und die Site während des angegebenen Zeitraums besucht haben. Diese Personen sind Teil des Tests und sollten gezählt werden. Wenn Sie nur die Anzahl der Personen sehen wollen, die innerhalb einer einzigen Woche betroffen waren, können Sie ein Segment der Besucher erstellen, die eine Aktivitätsimpression hatten, und dieses auf den Bericht anwenden.

Sie können die Zeit verkürzen, während der die [!DNL Target] Variable in einer Sitzung bestehen bleibt. Dies ist jedoch problematisch bei Tests, bei denen das Konversionsereignis nicht mit der gleichen Wahrscheinlichkeit innerhalb derselben Sitzung eintritt.

+++

## Warum wird ein und derselbe Besucher in [!DNL Analytics] manchmal in mehreren Erlebnissen gezählt? {#section_1397E972D31C4207A142E4D2D6D794A2}

+++Antwort
In der folgenden Liste werden Gründe erläutert, warum ein und derselbe Besucher in [!DNL Analytics] in mehreren Erlebnissen gezählt werden kann:

* Das [!DNL Target] ist abgelaufen, aber das [!DNL Analytics]-Cookie ist noch vorhanden. In diesem Fall bewertet [!DNL Target] den Benutzer neu, betrachtet den Besucher jedoch [!DNL Analytics] als dieselbe Person.
* Wenn der Besucher die `mbox3rdPartyId` verwendet, könnte [!DNL Target] bei der Zusammenführung des anonymen Besuchers mit dem ID-Profil des Drittanbieters den Besucher in ein anderes Erlebnis versetzen, das der Drittanbieter-ID entspricht. Weitere Informationen finden Sie unter [Echtzeit-Profilsynchronisierung für mbox3rdPartyID](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] verfolgt möglicherweise andere Geräte als derselbe Besucher auf eine andere Weise als [!DNL Target] verfolgt diese Geräte: Die Einrichtung der Drittanbieter-ID in [!DNL Target] unterscheidet sich von der in Analytics.

+++

## Unterstützt A4T Virtual Report Suites? {#virtual}

+++Antwort
Obwohl Virtual Report Suites nicht in der [!UICONTROL Report Suite] enthalten sind, haben alle A4T-Daten, die für eine Report Suite freigegeben wurden, die mit einer Virtual Report Suite in verknüpft ist, [!DNL Analytics] Zugriff auf diese Daten. Beachten Sie, dass eine aus einer Virtual Report Suite erstellte Zielgruppe nicht für [!DNL Target] freigegeben werden kann.

+++

## Kann ich den Prozentsatz der Traffic-Zuordnung in einer Aktivität ändern, die nach der Aktivierung der Aktivität A4T verwendet?

+++Antwort
Das Ändern des Prozentsatzes der Traffic-Zuordnung in einer Aktivität nach der Aktivierung kann zu inkonsistenten Berichten in [!DNL Analytics] führen, da sich die Änderung nur auf neue Besucher auswirkt. Wiederkehrende Besucher sind nicht betroffen.

Am besten sollten Sie die vorhandene Aktivität stoppen und dann eine neue Aktivität erstellen, anstatt den Prozentsatz nach der Aktivierung zu ändern. Das Reporting für die neue Aktivität beginnt mit neuen Besuchern, und die Daten von wiederkehrenden Besuchern führen nicht zu inkonsistenten Berichten.

+++

## Wie werden Besuche in [!DNL Analytics] gezählt und Konversionsgutschriften in einer [!UICONTROL Auto-Target]-Aktivität zugewiesen, die A4T verwendet?

+++Antwort
Wenn sich ein Besucher für eine A4T-Aktivität qualifiziert, Inhalte anzeigt oder konvertiert, sendet [!DNL Target] Ereignisdaten an [!DNL Analytics]. Mit diesen Ereignisdaten können [!DNL Analytics] Konversionsereignisse und andere Clickstream-Ereignisse auf der Seite den entsprechenden [!DNL Target] Aktivitäten und Erlebnissen zuordnen.

Hier einige Punkte, die Sie beim Anzeigen [!DNL Analytics] Berichte beachten sollten:

* Als Best Practice gilt, dass Ihr Reporting-Fenster ab dem Startdatum der Aktivität beginnen sollte.
* Wenn eine Konversion außerhalb des Berichtsfensters stattfindet, ist die Konversion in [!DNL Analytics] nicht sichtbar.
* Im „Targeting“-Teil des Traffics für [!UICONTROL Auto-Target] Aktivitäten werden Besuchenden möglicherweise von Sitzung zu Sitzung unterschiedliche Erlebnisse angezeigt. Wenn sich beispielsweise ihr Profil oder Kontext geändert hat und die Algorithmen für maschinelles Lernen von [!DNL Target] entscheiden, dass sie mit höherer Wahrscheinlichkeit eine Konversion in ein neues Erlebnis durchführen. Wenn Besucher von Erlebnis zu Erlebnis wechseln, erhöht sich die Besuchsanzahl für jedes angezeigte Erlebnis. Dies unterscheidet sich von regulären A/B-Test-Aktivitäten, bei denen Erlebnisse besuchsübergreifend für einen Besucher haften bleiben.
* Wenn ein Besucher über Besuche hinweg mehrere Erlebnisse sieht, wird jede Konversion immer dem letzten Erlebnis zugeordnet, das der Besucher gesehen hat. Wie bereits erwähnt, erhöht sich die Besuchsanzahl für jedes Erlebnis, das der Besucher gesehen hat. Dadurch können die Konversionsraten pro Erlebnis beim Anzeigen von Erlebnissen unter der Dimension &quot;[!UICONTROL Targeted]&quot; in [!DNL Adobe Analytics]-Berichten künstlich gesenkt werden.

+++

## Wie kann ich Aktivitätsimpressionen bei Verwendung von [!DNL Analysis Workspace] (A4T) in [!UICONTROL Analytics for Target] nachverfolgen? {#activity-impressions}

+++Antwort

So zeigen Sie Aktivitätsimpressionen in [!DNL Analysis Workspace] an:

1. Klicken Sie in der [!DNL Target]-Benutzeroberfläche auf **[!UICONTROL View in Analytics]**.
1. Fügen Sie die Spalte **[!UICONTROL Activity Impressions]** zum [[!DNL Analytics Workspace]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html){target=_blank} hinzu.
1. Klicken Sie in der Spalte **[!UICONTROL Activity Impressions]** auf das Symbol [!UICONTROL Gear] .
1. Klicken Sie auf **[!UICONTROL Use non-default attribution model]**.
1. Wählen Sie **[!UICONTROL Same Touch Model]** > **[!UICONTROL Apply]** aus.

+++
