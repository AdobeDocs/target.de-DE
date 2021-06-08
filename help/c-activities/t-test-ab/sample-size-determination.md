---
keywords: AB;A/B;AB...n;Stichprobengröße;Stichprobengrößenrechner;automatische Zuordnung;automatische Zuordnung;Rechner
description: Erfahren Sie, wie lange ein A/B-Test ausgeführt werden soll. Ein erfolgreicher A/B-Test in Adobe [!DNL Target] erfordert genügend Besucher (Stichprobengröße), um Ihre Konversionsrate zu verbessern.
title: Wie lange sollte ich einen A/B-Test durchführen?
feature: A/B-Tests
exl-id: 4f4ce387-bbbe-44af-965b-affc3ee09d74
source-git-commit: 4c696f55f56a116cff61c2c307f750e72cc0107c
workflow-type: tm+mt
source-wordcount: '3063'
ht-degree: 63%

---

# Wie lange sollten A/B-Tests laufen?

Eine erfolgreiche [!UICONTROL A/B-Test] -Aktivität in [!DNL Adobe Target] erfordert genügend Besucher (Stichprobengröße), um Ihre Konversionsrate zu verbessern. Woher wissen Sie, wie lange ein A/B-Test dauert? Dieser Artikel enthält Informationen zu [!UICONTROL Aktivitäten mit automatischer Zuordnung] und zum [!UICONTROL Adobe Target] Stichprobengrößenrechner, mit dem Sie sicherstellen können, dass Ihre Aktivität über ausreichend Besucher verfügt, um Ihre Ziele zu erreichen.

Es ist verlockend, einen Test zu stoppen, wenn eines der Angebote in den ersten Tagen der Aktivität deutlich besser oder schlechter abschneidet als die anderen. Wenn jedoch die Anzahl der Beobachtungen gering ist, ist die Wahrscheinlichkeit hoch, dass eine positive oder negative Steigerung nur zufällig beobachtet wurde, da die Konversionsrate als Durchschnitt einer geringen Besucherzahl ermittelt wurde. Wenn die Aktivität mehr Datenpunkte erfasst, nähern sich die Konversionsraten ihren eigentlichen, langfristigen Werten an.

>[!IMPORTANT]
>
>Das vorzeitige Beenden einer Aktivität ist einer der zehn signifikanten Fallstricke, auf die Sie beim Durchführen von A/B-Tests möglicherweise stoßen. Weitere Informationen finden Sie unter [Zehn häufige Fehler bei A/B-Tests und wie diese vermieden werden](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md#concept_578A7947C9554868B30F12DFF9E3F8E3).

[!DNL Adobe Target] stellt Tools bereit, mit denen Sie sicherstellen können, dass Ihre Aktivität über eine ausreichend große Stichprobengröße verfügt, um Ihre Konversionsziele zu erreichen: Automatische Zuordnung.

## Automatisch zuweisen {#auto-allocate}

Eine Aktivität vom Typ [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) ist ein A/B-Test, der einen Gewinner unter zwei oder mehr Erlebnissen identifiziert. Ein automatisierter Zuordnungstest ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.

Mit A/B-Standardtests sind Kosten verbunden. Sie müssen Traffic generieren, um die Leistung jedes einzelnen Erlebnisses zu messen und durch Analysen die erfolgreichsten Erlebnisse zu ermitteln. Die Verteilung von Traffic bleibt auch dann festgelegt, wenn Sie erkennen, dass einige Erlebnisse andere übertreffen. Außerdem ist es schwierig, die Stichprobengröße korrekt zu bestimmen, und die Aktivität muss komplett durchlaufen, bevor Sie einen Sieger finden. Und es besteht immer noch die Chance, dass der ermittelte Gewinner kein wahrer Gewinner ist.

Die Lösung ist [!UICONTROL Automatische Zuordnung]. [!UICONTROL Die Funktion „Automatisierte Zuordnung“ senkt diese Kosten sowie die Kosten für die Bestimmung eines erfolgreichsten Erlebnisses. ] [!UICONTROL Die Funktion „Automatisierte Zuordnung“ überwacht die Zielmetrikleistung aller Erlebnisse und sendet proportional mehr neue Teilnehmer an Erlebnisse mit einer hohen Leistung. ] Es wird ausreichend Traffic für die Erkundung der anderen Erlebnisse reserviert. Sie können die Vorteile der Aktivität auf Ihren Ergebnissen sehen, selbst wenn die Aktivität noch ausgeführt wird: Optimierung erfolgt parallel zum Lernen.

[!UICONTROL Die Funktion „Automatisierte Zuordnung“ überführt Besucher nach und nach zu den erfolgreichsten Erlebnissen, anstatt dass Sie mit dem Bestimmen eines Siegers warten müssen, bis die Aktivität abgeschlossen ist. ] Sie profitieren schneller von Steigerungen, da den Aktivitätsteilnehmern, die zu weniger erfolgreichen Erlebnissen geleitet worden wären, nun potenziell erfolgreiche Erlebnisse angezeigt werden.

Bei der Verwendung der Funktion [!UICONTROL „Automatisierte Zuordnung“] zeigt [!DNL Adobe Target] oben auf der Seite der Aktivität ein Abzeichen mit „Noch kein Gewinner“ an, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Konfidenz erreicht hat. [!DNL Target] bestimmt dann das erfolgreichste Erlebnis, indem oben auf der Aktivitätsseite ein entsprechendes Symbol angezeigt wird.

Weitere Informationen finden Sie unter [Übersicht über die automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

## Adobe [!DNL Target] Stichprobengrößenrechner {#section_6B8725BD704C4AFE939EF2A6B6E834E6}

Wenn Sie sich dafür entscheiden, eine manuelle [!UICONTROL A/B-Test] -Aktivität anstelle von [!UICONTROL Automatische Zuordnung] zu verwenden, hilft Ihnen der [!DNL Target] Stichprobengrößenrechner dabei, die für einen erfolgreichen Test erforderliche Stichprobengröße zu bestimmen. Ein manueller A/B-Test ist ein fester Horizonttest, daher ist der Rechner hilfreich. Die Verwendung des Taschenrechners für eine Aktivität vom Typ [!UICONTROL Automatische Zuordnung] ist optional, da [!UICONTROL Automatische Zuordnung] einen Gewinner erklärt. Der Rechner gibt Ihnen eine grobe Schätzung der benötigten Stichprobengröße. Im Folgenden finden Sie weiter Informationen zur Verwendung des Rechners.

Bevor Sie Ihren A/B-Test einrichten, greifen Sie auf den Adobe Target [Stichprobengrößenrechner](https://experienceleague.adobe.com/tools/calculator/testcalculator.html) zu.

![Adobe Target-Stichprobengrößenrechner](/help/c-activities/t-test-ab/assets/sample_size_calculator-new.png)

Es ist wichtig, vor einem A/B-Test eine angemessene Stichprobengröße (Anzahl der Besucher) zu bestimmen, um die Zeit zu bestimmen, die die Aktivität vor der Auswertung der Ergebnisse ausführen soll. Eine einfache Überwachung der Aktivität bis zur Erreichung der statistischen Bedeutung führt dazu, dass das Konfidenzintervall stark unterschätzt wird, was den Test unzuverlässig macht. Mit diesem Ergebnis wird beabsichtigt, dass - für den Fall, dass ein statistisch signifikantes Ergebnis entdeckt wird - der Test gestoppt und ein Gewinner ernannt wird. Sollte das Ergebnis jedoch nicht statistisch signifikant sein, wird der Test weiter ausgeführt. Diese Vorgehensweise begünstigt das positive Ergebnis erheblich, wodurch die Falsch-Positiv-Rate zunimmt und das effektive Signifikanzniveau des Tests verzerrt wird.

Dies kann zu vielen falsch-positiven Ergebnissen führen, was zur Implementierung von Angeboten führt, die nicht die prognostizierte Steigerung am Ende liefern. Eine schlechte Steigerung selbst ist ein unbefriedigendes Ergebnis, aber eine noch schwerwiegendere Folge ist, dass die Unfähigkeit, eine genaue Steigerung vorherzusagen, im Laufe der Zeit das Vertrauen der Organisation in Tests als Praxis untergräbt.

Dieser Artikel erörtert die Faktoren, die bei der Ermittlung der Stichprobengröße abzuwägen sind, und stellt einen Tabellenrechner vor, mit dem sich eine angemessene Stichprobengröße schätzen lässt. Durch Berechnung der Stichprobengröße mithilfe des Stichprobengrößenrechners (Link siehe oben) vor Beginn eines A/B-Tests stellen Sie sicher, dass Sie jederzeit hochwertige A/B-Tests durchführen, die statistischen Standards entsprechen.

Es gibt fünf benutzerdefinierte Parameter zur Definition eines A/B-Tests. Diese Parameter sind miteinander verknüpft, sodass sich der fünfte berechnen lässt, wenn vier der Parameter festgelegt wurden:

* Statistische Bedeutung
* Teststärke
* Zuverlässig bestimmbare Mindeststeigerung
* Baseline-Konversionsrate
* Anzahl der Besucher

Bei einem A/B-Test werden die statistische Bedeutung, Teststärke, zuverlässig bestimmbare Mindeststeigerung und Baseline-Konversionsrate durch einen Analysten festgelegt. Anschließend wird die erforderliche Anzahl der Besucher aus diesen Zahlen berechnet. In diesem Artikel werden diese Elemente erläutert und Richtlinien zur Ermittlung dieser Metriken für einen bestimmten Test festgelegt.

![](assets/samplesize.png)

Die unten stehende Abbildung veranschaulicht die vier möglichen Ergebnisse eines A/B-Tests.

![](assets/outcomes.png)

Es ist wünschenswert, keine Falsch-Positiv-Werte bzw. Falsch-Negativ-Werte zu erhalten. Die Erzielung von Null-Falsch-Positiv-Werten kann jedoch niemals durch einen statistischen Test garantiert werden. Es ist immer möglich, dass beobachtete Trends nicht repräsentativ für die zugrundeliegenden Konversionsraten sind. Beispielsweise könnte man in einem Test, um zu sehen, ob Kopf oder Zahl auf einem Münzwurf wahrscheinlicher war, selbst mit einer fairen Münze, zehn Köpfe auf zehn Würfe nur zufällig bekommen. Die statistische Bedeutung und die Teststärke tragen zur Quantifizierung der Falsch-Positiv- und Falsch-Negativ-Raten bei und ermöglichen es, diese für einen gegebenen Test auf einem vertretbaren Niveau zu halten.

### Statistische Bedeutung {#section_8230FB9C6D1241D8B1786B72B379C3CD}

Das Signifikanzniveau eines Tests bestimmt, wie wahrscheinlich es ist, dass der Test einen signifikanten Unterschied der Konversionsraten zwischen zwei verschiedenen Angeboten meldet, obwohl es tatsächlich keinen echten Unterschied gibt. Diese Situation wird als falsch positiv oder als Fehler vom Typ I bezeichnet. Das Signifikanzniveau ist ein vom Benutzer angegebener Schwellenwert und stellt einen Kompromiss zwischen der Toleranz für falsch-positive Ergebnisse und der Anzahl der Besucher dar, die in den Test einbezogen werden müssen.

Bei einem A/B-Test wird zunächst angenommen, dass beide Angebote dieselbe Konversionsrate aufweisen. Anschließend wird die Wahrscheinlichkeit des beobachteten Ergebnisses auf Basis dieser Annahme berechnet. Wenn diese Wahrscheinlichkeit (der p-Wert) kleiner als ein vordefinierter Schwellenwert (das Signifikanzniveau) ist, kommt [!DNL Target] zu dem Schluss, dass die ursprüngliche Annahme - dass beide Angebote dieselbe Konversionsrate aufweisen - falsch ist. Daher unterscheiden sich die Konversionsraten von A und B statistisch auf dem gegebenen Signifikanzniveau.

Ein allgemein übliches Signifikanzniveau bei A/B-Tests beträgt 5 %, was einem Konfidenzniveau von 95 % entspricht (Konfidenzniveau = 100 % - Signifikanzniveau). Ein Konfidenzniveau von 95 % bedeutet, dass Sie jedes Mal, wenn Sie einen Test durchführen, mit einer Wahrscheinlichkeit von 5 % eine statistisch signifikante Steigerung beobachten werden, auch wenn kein Unterschied zwischen den Angeboten besteht.

Typische Interpretationen des Konfidenzniveaus werden in der unten stehenden Tabelle zusammengefasst:

| Konfidenzniveau | Interpretation |
|--- |--- |
| &lt; 90% | Kein Beweis, dass es einen Unterschied zwischen den Konversionsraten gibt |
| 90-95 % | Schwacher Beweis, dass es einen Unterschied zwischen den Konversionsraten gibt |
| 95-99 % | Moderater Beweis, dass es einen Unterschied zwischen den Konversionsraten gibt |
| 99-99,9 % | Starker Beweis, dass es einen Unterschied zwischen den Konversionsraten gibt |
| +99,9 % | Sehr starker Beweis, dass es einen Unterschied zwischen den Konversionsraten gibt |

Es wird empfohlen, immer ein Konfidenzniveau von 95 % oder neuer zu verwenden.

Es ist wünschenswert, das höchstmögliche Konfidenzniveau zu verwenden, damit der Test nur wenige Falsch-Positiv-Werte liefert. Ein höheres Konfidenzniveau erfordert jedoch eine höhere Besucheranzahl, wodurch sich der Zeitbedarf für den Test erhöht. Darüber hinaus bewirkt eine Steigerung des Konfidenzniveaus eine Senkung der Teststärke.

### Teststärke {#section_1169C27F8E4643719D38FB9D6EBEB535}

Die Teststärke eines A/B-Tests ist die Wahrscheinlichkeit der Aufdeckung eines echten Unterschieds der Konversionsrate in einer bestimmten Größenordnung. Aufgrund der zufälligen (stochastischen) Natur der Konversionsereignisse ist es möglich, dass ein statistisch signifikanter Unterschied - zufällig - nicht beobachtet wird, obwohl es einen echten Unterschied bei der Konversionsrate zwischen den beiden Angeboten gibt. Dieses Szenario wird als falsch negativ oder als Fehler Typ II bezeichnet.

Die Teststärke wird oft ignoriert, weil ihre Ermittlung im Gegensatz zur statistischen Bedeutung für die Durchführung eines A/B-Tests nicht erforderlich ist. Das Ignorieren der Teststärke geht jedoch mit einer erheblichen Wahrscheinlichkeit einher, dass echte Unterschiede zwischen den Konversionsraten verschiedener Angebote durch den Test nicht erkannt werden, weil die Stichprobe zu klein ist. Das führt dazu, dass der Test von Falsch-Positiv-Werten dominiert wird.

Eine hohe Teststärke ist wünschenswert, damit der Test mit großer Wahrscheinlichkeit einen echten Unterschied der Konversionsraten erkennt und weniger Falsch-Negativ-Werte ergibt. Eine größere Anzahl von Besuchern ist jedoch erforderlich, um die Teststärke zur Erkennung einer bestimmten Steigerung zu erhöhen, was die für den Test erforderliche Zeit verlängert.

Ein üblicher Wert für die Teststärke ist 80 %, was bedeutet, dass der Test mit achtzigprozentiger Wahrscheinlichkeit einen Unterschied ermittelt, der der zuverlässig bestimmbaren Mindeststeigerung entspricht. Die Ermittlung kleinerer Steigerungen durch den Test ist weniger wahrscheinlich, die Ermittlung größerer Steigerungen wiederum wahrscheinlicher.

### Zuverlässig bestimmbare Mindeststeigerung {#section_6101367EE9634C298410BBC2148E33A9}

Die meisten Organisationen möchten den kleinstmöglichen Unterschied der Konversionsrate ermitteln, da sich eine Implementierung selbst bei einer geringen Steigerung lohnt. Wenn Sie jedoch möchten, dass der A/B-Test mit hoher Wahrscheinlichkeit eine geringe Steigerung erkennt, wäre die Anzahl der Besucher, die in den Test einbezogen werden müssen, überaus groß. Der Grund dafür ist, dass bei einem geringen Unterschied der Konversionsrate beide Konversionsraten mit hoher Genauigkeit geschätzt werden müssen, um den Unterschied zu ermitteln, für den viele Besucher erforderlich sind. Deswegen sollte die zuverlässig bestimmbare Mindeststeigerung durch geschäftliche Anforderungen festgelegt werden, die den Trade-off zwischen der Entdeckung geringer Steigerungen und der Durchführung des Tests über längere Zeiträume berücksichtigen.

Zum Beispiel wird angenommen, dass zwei Angebote (A und B) echte Konversionsraten von 10 % und 15 % aufweisen. Wenn diese Angebote für 100 Besucher eingeblendet werden, besteht aufgrund der stochastischen Natur der Konversionen eine 95-prozentige Wahrscheinlichkeit, dass für Angebot A Konversionsraten zwischen 4 % und 16 % und für Angebot B Konversionsraten zwischen 8 % und 22 % beobachtet werden. Diese Bandbreiten werden in der Statistik als Konfidenzintervalle bezeichnet. Sie repräsentieren die Konfidenz bezüglich der Genauigkeit der geschätzten Konversionsraten. Je größer die Stichprobe (mehr Besucher), desto mehr können Sie darauf vertrauen, dass die Schätzwerte für die Konversionsrate genau sind.

Die unten stehende Abbildung veranschaulicht diese Wahrscheinlichkeitsverteilungen.

![](assets/probability_distributions.png)

Aufgrund der großen Überlappung dieser beiden Bandbreiten kann der Test nicht ermitteln, ob die Konversionsraten voneinander abweichen. Aus diesem Grund ermöglicht ein Test mit 100 Besuchern keine Unterscheidung zwischen den beiden Angeboten. Wenn Target die Angebote jedoch jeweils 5.000 Besuchern präsentiert, besteht eine 95%ige Wahrscheinlichkeit, dass die beobachteten Konversionsraten im Bereich von 9 % bis 11 % bzw. 14 % bis 16 % fallen.

![](assets/probability_distributions2.png)

In diesem Fall ist es unwahrscheinlich, dass der Test zu einem falschen Ergebnis führt, sodass der Test mit 5.000 Besuchern zwischen den beiden Angeboten unterscheiden kann. Der Test mit 5.000 Besuchern weist ein Konfidenzintervall von ca. +/-1 % auf. Das bedeutet, dass der Test Unterschiede von etwa 1 % erkennen kann. Aus diesem Grund wären noch mehr Besucher erforderlich, wenn die echten Konversionsraten der Angebote bzw. bei 10 % und 10,5 % und nicht bei 10 % und 15 % liegen würden.

### Baseline-Konversionsrate {#section_39380C9CA3C649B6BE6E1F8A06178B05}

Die Baseline-Konversionsrate ist die Konversionsrate des Kontrollangebotes (Angebot A). Oftmals können Sie sich auf Basis früherer Erfahrungen eine gute Vorstellung von der Konversionsstufe für das Angebot machen. Wenn dies nicht der Fall ist (zum Beispiel, weil es sich um einen neuen Angebotstyp oder ein neues kreatives Element handelt), kann der Test einen ganzen Tag oder länger ausgeführt werden, um eine ungefähre Schätzung der Baseline-Konversionsrate zu erhalten, die bei der Berechnung der Stichprobengröße verwendet werden kann.

### Anzahl der Besucher {#section_19009F165505429E95291E6976E498DD}

Es kann schwierig sein, die Opportunitätskosten für die Ausführung eines Tests über einen langen Zeitraum mit dem Risiko falscher Positivwerte und falscher Negativwerte abzuwägen. Es liegt auf der Hand, dass Sie keine falschen Entscheidungen treffen möchten, jedoch sollte auch eine Lähmung durch zu strikte bzw. rigide Teststandards vermieden werden.

Als allgemeine Richtlinie werden ein Konfidenzniveau von 95 % und eine Teststärke von 80 % empfohlen.

Der Stichprobenkalkulator (Link siehe oben) fragt Sie nach der statistischen Bedeutung (Empfehlung: 95 %) und der statistischen Aussagekraft (Empfehlung: 80 %). Nach Eingabe der Baseline-Konversionsrate und des täglichen Traffics für alle Angebote gibt die Tabelle die erforderliche Anzahl der Besucher zur Erkennung einer Steigerung von 1 %, 2 %, 5 %, 10 %, 15 % und 20 % mit einer Wahrscheinlichkeit an, die der angegebenen Teststärke entspricht. Die Tabelle ermöglicht dem Benutzer auch die Eingabe einer benutzerdefinierten zuverlässig erkennbaren Mindeststeigerung. Darüber hinaus gibt die Tabelle die Anzahl der Wochen an, die erforderlich sind, um den Test auf dem vom Benutzer angegebenen Traffic-Niveau zu basieren. Die erforderliche Wochenanzahl wird auf die nächste volle Woche aufgerundet, um zu vermeiden, dass die Ergebnisse durch Wochentagseffekte beeinflusst werden.

Es gibt einen Trade-off zwischen der durch den Test zuverlässig ermittelbaren Mindeststeigerung und der erforderlichen Anzahl der Besucher. Die unten stehende Abbildung, die für eine Baseline-Konversionsrate (Kontrolle) von 5 % gilt, zeigt stark abnehmende Erträge bei einer zunehmenden Anzahl von Besuchern. Die Mindeststeigerung, die zuverlässig ermittelt werden kann, verbessert sich deutlich mit den ersten hinzugefügten Benutzern, es ist jedoch eine zunehmend größere Anzahl von Besuchern erforderlich, um den Test weiter zu verbessern. Die Abbildung trägt dazu bei, einen angemessenen Trade-off zwischen der für die Ausführung des Tests erforderlich Zeit (die durch die Anzahl der erforderlichen Besucher und den Site-Traffic bestimmt wird) und der Mindeststeigerung, die sich durch den Test zuverlässig erkennen lässt, zu ermitteln.

![](assets/samplesizecontrol.png)

In diesem Beispiel könnten Sie entscheiden, dass die Möglichkeit, eine Steigerung von 5 % (die einer Konversionsrate des alternativen Angebots von (100 % + 5 %) x 5 % = 5,25 % entspricht) bei 80 von 100 Tests zu ermitteln, angemessen ist. Sie benötigen daher eine Stichprobengröße von 100.000 Besuchern für jedes Angebot. Wenn die Site pro Tag 20.000 Besucher aufweist und Sie zwei Angebote testen, muss der Test über 2 x 100.000/20.000 = 10 Tage ausgeführt werden, bevor sich ermitteln lässt, ob das Alternativangebot dem Kontrollangebot statistisch signifikant überlegen ist.

Auch hier wird in jedem Fall empfohlen, die erforderliche Zeit auf eine ganze Woche aufzurunden, um Wochentagseffekte zu vermeiden. In diesem Beispiel würde der Test vor der Auswertung der Ergebnisse über zwei Wochen ausgeführt werden.

### Umsatz-pro-Besuch-Metrik  {#section_C704C0861C9B4641AB02E911648D2DC2}

Bei Nutzung des Umsatzes pro Besuch (Revenue per Visit - RPV) als Metrik wird eine weitere Streuungsquelle hinzugefügt, da RPV das Produkt aus Umsatz pro Bestellung und Konversionsrate ist (RPV = Umsatz / Anzahl der Besucher = (Umsatz pro Bestellung x Anzahl der Bestellungen) / Anzahl der Besucher = Umsatz pro Bestellung x (Anzahl der Besucher x CTR) / Anzahl der Besucher = Umsatz pro Bestellung x CTR), mit der jeweils eigenen Varianz. Die Varianz der Konversionsrate kann mithilfe eines mathematischen Modells direkt geschätzt werden, die Varianz des Umsatzes pro Bestellung ist jedoch spezifisch für die Aktivität. Verwenden Sie daher Kenntnisse über diese Abweichung von früheren Aktivitäten oder führen Sie den A/B-Test für einige Tage durch, um die Varianz des Umsatzes zu schätzen. Die Varianz wird aus den Werten für Summe der Verkäufe, Summe der Verkäufe im Quadrat und Anzahl der Besucher berechnet, die in der CSV-Download-Datei enthalten sind. Nachdem dies festgestellt wurde, verwenden Sie das Arbeitsblatt, um die erforderliche Zeit zum Abschließen des Tests zu berechnen.

Der Stichprobengrößenrechner (Link siehe oben) kann Ihnen dabei helfen, die RPV-Metrik zu konfigurieren. Wenn Sie den Rechner öffnen, sehen Sie eine Registerkarte mit der Bezeichnung [!UICONTROL RPV-Metrik]. Sie benötigen die folgenden Informationen, wenn Sie die RPV-Version des Rechners verwenden:

* Anzahl der Besucher des Kontrollangebots
* Gesamtumsatz des Kontrollangebots

   Stellen Sie sicher, dass der Filter für extreme Bestellungen ausgewählt ist.

* Die Quadratsumme des Umsatzes für das Kontrollangebot

   Vergewissern Sie sich, dass der extreme Auftragsfilter aktiviert ist.

Im Allgemeinen erfordert die Verwendung von RPV als Metrik 20-30 % mehr Zeit, um dasselbe Niveau der statistischen Konfidenz für dasselbe Niveau der gemessenen Steigerung zu erreichen. Dies liegt daran, dass RPV die zusätzliche Varianz unterschiedlicher Bestellgrößen pro Konversion aufweist. Dies sollte bei der Wahl zwischen einer direkten Konversionsrate und RPV als Metrik, auf der Ihre endgültige Geschäftsentscheidung basiert, berücksichtigt werden.

## Korrektur für den Vergleich mehrerer Angebote {#section_1474113764224D0B85472D8B023CCA15}

Jedes Mal, wenn Sie zwei Angebote vergleichen, entspricht die Wahrscheinlichkeit eines Falsch-Positiv-Werts (Beobachtung eines statistisch signifikanten Unterschieds, auch wenn es keinen Unterschied bei der Konversionsrate gibt) dem Signifikanzniveau. Wenn zum Beispiel fünf Angebote A/B/C/D/E vorliegen und es sich bei A um das Kontrollangebot handelt, werden vier Vergleiche vorgenommen (Kontrolle zu B, Kontrolle zu C, Kontrolle zu D und Kontrolle zu E) und die Wahrscheinlichkeit eines Falsch-Positiv-Werts beträgt 18,5 %, selbst wenn das Konfidenzniveau 95 % beträgt, da Pr (mindestens ein Falsch-Positiv-Wert) = 1 - Pr (keine Falsch-Positiv-Werte) = 1 - 0,95 = 18,5 %. Als Falsch-Positiv-Wert gilt in diesem Zusammenhang, wenn der Kontrollwert besser als die Alternative bzw. wenn die Alternative besser als der Kontrollwert ausfällt, auch wenn es tatsächlich keinen Unterschied zwischen diesen Werten gibt.

## Schlussfolgerung  {#section_AEA2427B90AE4E9395C7FF4F9C5CA066}

Durch die Verwendung der Aktivität [!UICONTROL Automatische Zuordnung] identifiziert [!DNL Target] einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird. [!UICONTROL Mit der automatischen Zuordnung erreichen Sie Ihre Konversionsziele ohne Aufwand und Ungewissheit.]

Wenn Sie den in diesem Artikel vorgestellten Stichprobengrößenrechner (Link siehe oben) verwenden und den Test für die von ihm empfohlene Dauer ausführen lassen, können Sie sicherstellen, dass Sie immer hochwertige A/B-Tests durchführen, die die Falsch-Positiv- und Falsch-Negativ-Raten einhalten, die Sie für den spezifischen Test als angemessen festgelegt haben. Dadurch wird gewährleistet, dass Ihre Tests konsistent und in der Lage sind, die von Ihnen gewünschte Steigerung zuverlässig zu ermitteln.
