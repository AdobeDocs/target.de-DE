---
keywords: automatisierte Traffic-Zuordnung; Targeting; Anzahl erhöhen und Benutzer in Aktivität belassen; Traffic-Zuordnung; automatische Zuordnung; automatische Zuordnung
description: Erfahren Sie, wie Sie eine [!UICONTROL Auto-Allocate] -Aktivität in  [!DNL Adobe Target]  verwenden, die einen Gewinner unter zwei oder mehr Erlebnissen identifiziert und dem Gewinner automatisch mehr Traffic zuordnet.
title: Was ist eine [!UICONTROL Auto-Allocate] -Aktivität?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
source-git-commit: 1b1b2271738d12f8da4e695900b70e280f50d8cf
workflow-type: tm+mt
source-wordcount: '3502'
ht-degree: 35%

---

# [!UICONTROL Auto-Allocate] Übersicht

Eine [!UICONTROL Auto-Allocate] -Aktivität in [!DNL Adobe Target] identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.

Wählen Sie beim [ Erstellen einer A/B-Aktivität ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) mit dem geleiteten Arbeitsablauf mit drei Schritten die Option **[!UICONTROL Auto-Allocate to best experience]** auf der Seite **[!UICONTROL Targeting]** (Schritt 2).

## Die Herausforderung {#section_85D5A03637204BACA75E19646162ACFF}

Mit A/B-Standardtests sind Kosten verbunden. Sie müssen Traffic generieren, um die Leistung jedes einzelnen Erlebnisses zu messen und durch Analysen die erfolgreichsten Erlebnisse zu ermitteln. Die Verteilung von Traffic bleibt auch dann festgelegt, wenn Sie erkennen, dass einige Erlebnisse andere übertreffen. Außerdem ist es schwierig, die Stichprobengröße korrekt zu bestimmen, und die Aktivität muss komplett durchlaufen, bevor Sie einen Sieger finden. Und es besteht immer noch die Möglichkeit, dass der identifizierte Gewinner kein wahrer Gewinner ist.

## Die Lösung: [!UICONTROL Auto-Allocate] {#section_98388996F0584E15BF3A99C57EEB7629}

Eine [!UICONTROL Auto-Allocate] -Aktivität reduziert diese Kosten und den Mehraufwand bei der Bestimmung eines Gewinnererlebnisses. [!UICONTROL Auto-Allocate] überwacht die Zielmetrikleistung aller Erlebnisse und sendet proportional mehr neue Teilnehmer an die leistungsstarken Erlebnisse. Es wird ausreichend Traffic für die Erkundung der anderen Erlebnisse reserviert. Sie können die Vorteile des Tests an Ihren Ergebnissen erkennen, selbst wenn die Aktivität gerade ausgeführt wird: Die Optimierung erfolgt parallel zum Lernen.

Mit [!UICONTROL Auto-Allocate] werden Besucher allmählich zu erfolgreichsten Erlebnissen weitergeleitet, anstatt zu verlangen, dass Sie warten, bis eine Aktivität endet, um einen Gewinner zu bestimmen. Sie profitieren schneller von Steigerungen, da den Aktivitätsteilnehmern, die zu weniger erfolgreichen Erlebnissen geleitet worden wären, nun potenziell erfolgreiche Erlebnisse angezeigt werden.

Ein normaler A/B-Test in [!DNL Target] zeigt nur paarweise Vergleiche von Herausforderern mit der Kontrolle an. Wenn beispielsweise eine Aktivität über Erlebnisse verfügt: A, B, C und D, wobei A das Kontrollelement ist, würde ein normaler A/B-Test A mit B, A mit C und A mit D vergleichen.[!DNL Target]

In solchen Tests verwenden die meisten Produkte, einschließlich [!DNL Target], einen p-Wert-basierten Test von [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank}, um eine P-Wert-basierte Konfidenz zu erzielen. Mithilfe dieses Konfidenzwerts wird dann ermittelt, ob sich der Herausforderer ausreichend vom Kontrollelement unterscheidet. [!DNL Target] führt jedoch nicht automatisch die impliziten Vergleiche (B versus C, B versus D und C versus D) durch, die erforderlich sind, um das &quot;beste&quot;Erlebnis zu finden. Aus diesem Grund müssen Marketingexperten die Ergebnisse manuell analysieren, um das Gewinnererlebnis zu ermitteln.

[!UICONTROL Auto-Allocate] führt alle impliziten Vergleiche über Erlebnisse hinweg durch und generiert einen &quot;echten&quot;Gewinner. Es gibt in diesem Test keinen Bedarf für ein „Kontrollerlebnis“.

[!UICONTROL Auto-Allocate] ordnet neuen Besuchern intelligent Erlebnisse zu, bis sich das Konfidenzintervall des besten Erlebnisses nicht mit dem Konfidenzintervall anderer Erlebnisse überschneidet. Normalerweise könnte dieser Prozess zu falsch-positiven Ergebnissen führen, aber [!UICONTROL Auto-Allocate] verwendet Konfidenzintervalle basierend auf der [Bernstein-Ungleichung](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29){target=_blank} , die wiederholte Auswertungen kompensiert. An diesem Punkt gibt es einen echten Gewinner. Wenn [!UICONTROL Auto-Allocate] gestoppt wird und keine wesentliche Zeitabhängigkeit gegenüber den Besuchern besteht, die auf die Seite gelangen, besteht eine Wahrscheinlichkeit von mindestens 95 %, dass [!UICONTROL Auto-Allocate] ein Erlebnis zurückgibt, dessen wahre Antwort nicht schlechter als 1 % (relativ) weniger als die wahre Antwort des erfolgreichsten Erlebnisses ist.

## Verwendung von [!UICONTROL Auto-Allocate] versus [!UICONTROL A/B Test] oder [!UICONTROL Automated Personalization] Aktivitäten {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Verwenden Sie **[!UICONTROL Auto-Allocate]** , wenn Sie Ihre Aktivität von Anfang an optimieren und die erfolgreichsten Erlebnisse so schnell wie möglich identifizieren möchten. Durch die häufigere Bereitstellung leistungsstarker Erlebnisse wird die Gesamtleistung der Aktivität gesteigert.
* Verwenden Sie einen standardmäßigen **[A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)**, wenn Sie die Leistung aller Erlebnisse vor der Optimierung Ihrer Site charakterisieren möchten. Ein A/B-Test hilft Ihnen, alle Ihre Erlebnisse nach Rang zu ordnen, während [!UICONTROL Auto-Allocate] die besten Erlebnisse findet, aber keine Differenzierung unter den weniger leistungsstarken Erlebnissen garantiert.
* Verwenden Sie [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) , wenn Sie Optimierungsalgorithmen mit höchster Komplexität wünschen, z. B. Modelle für maschinelles Lernen, die Prognosen basierend auf individuellen Profilattributen erstellen. [!UICONTROL Auto-Allocate] untersucht das aggregierte Verhalten von Erlebnissen (wie A/B-Standardtests) und unterscheidet nicht zwischen Besuchern.

## Die wichtigsten Vorteile von [!UICONTROL Auto-Allocate] {#section_0913BF06F73C4794862561388BBDDFF0}

* Behält die Genauigkeit eines A/B-Tests bei
* Ermittelt einen statistisch bedeutenden Sieger schneller als mit manuellen A/B-Tests
* Bietet höhere durchschnittliche Kampagnensteigerungen im Vergleich zu manuellen A/B-Tests

## Terminologie   {#section_670F8785BA894745B43B6D4BFF953188}

Die folgenden Begriffe sind bei der Erörterung von [!UICONTROL Auto-Allocate] nützlich:

**Multi-Armed Bandit:** Ein [Multi-Armed Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank}-Ansatz zur Optimierung gleicht forschendes Lernen und die Nutzung dieses Lernens aus.

## Funktionsweise des Algorithmus {#section_ADB69A1C7352462D98849F2918D4FF7B}

Die Gesamtlogik hinter [!UICONTROL Auto-Allocate] umfasst sowohl die gemessene Leistung (z. B. Konversionsrate) als auch die Konfidenzintervalle der kumulativen Daten. Im Gegensatz zu einem standardmäßigen A/B-Test, bei dem der Traffic gleichmäßig zwischen Erlebnissen aufgeteilt wird, ändert [!UICONTROL Auto-Allocate] die Traffic-Zuordnung für alle Erlebnisse.

* 80 % der Besucher werden mithilfe der unten beschriebenen intelligenten Logik zugeordnet.
* 20 % der Besucher werden zufällig über alle Erlebnisse hinweg zugeordnet, um sich an das sich ändernde Besucherverhalten anzupassen.

Die Multi-Armed Bandit-Methode hält einige Erlebnisse für die Erforschung frei, während die leistungsstarken Erlebnisse ausgewertet werden. Es werden mehr neue Besucher in leistungsstärkere Erlebnisse platziert, und gleichzeitig wird die Reaktionsfähigkeit auf sich ändernde Bedingungen beibehalten. Diese Modelle werden mindestens einmal pro Stunde aktualisiert, um sicherzustellen, dass das Modell auf die neuesten Daten reagiert.

Sobald mehr Besucher an der Aktivität teilnehmen, erweisen sich einige Erlebnisse als erfolgreicher und erhalten mehr Traffic. 20 Prozent des Datenverkehrs werden weiterhin per Zufall verteilt, um alle Erlebnisse zu erforschen. Wenn ein Erlebnis mit einer schlechteren Leistung anfängt, sich zu verbessern, erhält es mehr Traffic. Oder: Wenn eine erfolgreiche Aktivität nachlässt, wird diesem Erlebnis weniger Traffic zugeordnet. Zum Beispiel wenn ein Ereignis dazu führt, dass Besucher nach anderen Informationen auf Ihrer Medienwebsite suchen oder wenn Wochenendverkäufe auf Ihrer Retail-Website unterschiedliche Ergebnisse liefern.

Die folgende Abbildung zeigt, wie der Algorithmus während eines Tests mit vier Erlebnissen funktionieren kann (klicken Sie, um die Abbildung zu erweitern):

![Bild automatisch zuordnen](assets/auto-allocate.png){width="600" zoomable="yes"}

Die Abbildung zeigt, wie sich der den einzelnen Erlebnissen zugeordnete Traffic ändert, während die Aktivität mehrere Runden durchläuft, bis ein Gewinner gefunden ist.

| Rund | Beschreibung |
|--- |--- |
| ![Aufwärmrunde](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png){width="200" zoomable="yes"} | **Aufwärmrunde (0)**: Während der Aufwärmrunde wird für jedes Erlebnis gleich viel Traffic zugeteilt, bis jedes Erlebnis in der Aktivität mindestens 1.000 Besucher und 50 Konversionen aufweist.<ul><li>Erlebnis A = 25 %</li><li>Erlebnis B = 25 %</li><li>Erlebnis C = 25 %</li><li>Erlebnis D = 25 %</li></ul>Nachdem jedes Erlebnis 1.000 Besucher und 50 Konversionen erreicht hat, startet [!DNL Target] die automatisierte Traffic-Zuordnung. Sämtliche Zuordnungen werden in Runden vorgenommen, wobei für jede Runde zwei Erlebnisse herausgesucht werden.<br>Nur zwei Erlebnisse gelangen in die nächste Runde: D und C.<br>Künftig bedeutet, dass 80 % des Traffics gleichmäßig auf die beiden Erlebnisse verteilt werden. Die anderen beiden Erlebnisse nehmen weiterhin teil, werden jedoch nur als Teil der zufälligen Traffic-Zuordnung von 20 % bereitgestellt, wenn neue Besucher an der Aktivität teilnehmen.<br>Sämtliche Zuordnungen werden stündlich aktualisiert (erkennbar an der Rundenangabe auf der X-Achse in der Abbildung oben). Nach jeder Runde werden die kumulativen Daten verglichen. |
| ![Runde 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png){width="200" zoomable="yes"} | **Runde 1**: Während dieser Runde werden 80% des Traffics den Erlebnissen C und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis den Erlebnissen A, B, C und D zugeordnet (jeweils 5 %). Während dieser Runde werden beim Erlebnis A gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt das Erlebnis D für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis A für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und A gelangen eine Runde weiter. |
| ![Runde 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png){width="200" zoomable="yes"} | **Runde 2**: Während dieser Runde werden 80% des Traffics den Erlebnissen A und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis B gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt das Erlebnis D für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis B für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und B gelangen eine Runde weiter. |
| ![Runde 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png){width="200" zoomable="yes"} | **Runde 3**: Während dieser Runde werden 80% des Traffics den Erlebnissen B und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis D weiterhin gute Leistungen verzeichnet und auch das Erlebnis C läuft gut.<ul><li>Der Algorithmus wählt das Erlebnis D für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis C für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und C gelangen eine Runde weiter. |
| ![Runde 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png){width="200" zoomable="yes"} | **Runde 4**: Während dieser Runde werden 80% des Traffics den Erlebnissen C und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis C gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt das Erlebnis C für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis D für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse C und D gelangen eine Runde weiter. |
| ![Runde n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png){width="200" zoomable="yes"} | **Runde *n***: Im weiteren Verlauf der Aktivität zeigt sich, dass ein Erlebnis mit hoher Leistung entsteht und der Prozess fortgesetzt wird, bis ein erfolgreichstes Erlebnis vorliegt. Wenn sich das Konfidenzintervall des Erlebnisses mit der höchsten Konversionsrate nicht mit dem Konfidenzintervall anderer Erlebnisse überschneidet, wird es als Gewinner bezeichnet. Ein [Badge wird auf der Seite der Gewinneraktivität](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) und in der Liste [!UICONTROL Activity] angezeigt.<ul><li>Der Algorithmus erklärt das Erlebnis C zum klaren Gewinner.</li></ul>An diesem Punkt ordnet der Algorithmus 80 % des Traffics Erlebnis C zu, während 20 % des Traffics weiterhin auf zufälliger Basis allen Erlebnissen (A, B, C und D) zugeordnet werden. C erhält insgesamt 85 % des Traffics. In dem unwahrscheinlichen Fall, dass das Konfidenzintervall des Gewinners erneut anfängt, andere Intervalle zu überdecken, kehrt der Algorithmus zu dem Verhalten der obigen Runde 4 zurück.<P>**Wichtig**: Wenn Sie während des Prozesses vorzeitig einen Gewinner manuell auswählen, wäre es einfach gewesen, das falsche Erlebnis auszuwählen. Daher empfiehlt es sich unbedingt, so lange zu warten, bis der Algorithmus das „siegreiche“ Erlebnis ermittelt hat. |

>[!NOTE]
>
>Wenn eine Aktivität nur über zwei Erlebnisse verfügt, erhalten beide Erlebnisse gleichen Traffic, bis [!DNL Target] ein erfolgreichstes Erlebnis mit 75 % Konfidenz findet. An diesem Punkt werden zwei Drittel des Traffics an den Gewinner und ein Drittel an den Verlierer weitergeleitet. Danach werden, wenn ein Erlebnis 95 % der Konfidenz erreicht, 90 % des Traffics dem Gewinner zugeordnet und 10 % werden dem Verlierer zugeordnet. [!DNL Target] sendet immer einen gewissen Traffic an das &quot;Verlierererlebnis&quot;, um am Ende falsche Positivwerte zu vermeiden (d. h., einige Erkundungen beizubehalten).

Nachdem eine [!UICONTROL Auto-Allocate] -Aktivität aktiviert wurde, sind die folgenden Vorgänge über die Tar[!DNL]get-Benutzeroberfläche nicht zulässig:

* Umschalten des Modus „Traffic-Zuordnung“ auf „Manuell“
* Ändern des Zielmetriktyps
* Ändern von Optionen im Bedienfeld &quot;[!UICONTROL Advanced Settings]&quot;

## Erfahren Sie, wie die automatische Zuordnung funktioniert

Weitere Informationen finden Sie unter [Automatische Zuordnung kann Ihnen schnellere Testergebnisse und einen höheren Umsatz liefern als ein manueller Test](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md).

## Einschränkungen  {#section_5C83F89F85C14FD181930AA420435E1D}

Beachten Sie beim Arbeiten mit [!UICONTROL Auto-Allocate] die folgenden Informationen:

### Die Funktion [!UICONTROL Auto-Allocate] funktioniert nur mit einer erweiterten Metrikeinstellung: [!UICONTROL Increment Count and Keep User in Activity]

Die folgenden erweiterten Metrikeinstellungen werden nicht unterstützt: [!UICONTROL Increment Count], [!UICONTROL Release User], [!UICONTROL Allow Reentry and Increment Count] und [!UICONTROL Release User and Bar from Reentry].

### Häufig wiederkehrende Besucher können die Konversionsraten von Erlebnissen erhöhen.

Wenn ein Besucher, der Erlebnis A anzeigt, häufig zurückkehrt und mehrere Male konvertiert, wird die Konversionsrate (CR) von Erlebnis A künstlich erhöht. Vergleichen Sie dieses Ergebnis mit Erlebnis B, bei dem Besucher konvertieren, aber nicht häufig zurückkehren. Daher sieht das CR von Erlebnis A besser aus als das CR von Erlebnis B, sodass neue Besucher eher A als B zugeordnet werden. Wenn Sie sich dafür entscheiden, einmal pro Teilnehmer zu zählen, ist die CR von A und CR von B möglicherweise identisch.

Wenn wiederkehrende Besucher zufällig verteilt werden, wird ihre Wirkung auf die Konversionsrate wahrscheinlich eher ausgeglichen. Um diese Auswirkung zu beschränken, sollten Sie die Änderung der Zählmethode der Zielmetrik erwägen, um jeden Teilnehmer nur einmal zu zählen.

### Unterscheidet zwischen Leistungsstarken und nicht zwischen Leistungsschwachen.

[!UICONTROL Auto-Allocate] kann gut zwischen leistungsstarken Erlebnissen unterscheiden (und einen Gewinner finden). Es kann vorkommen, dass Sie nicht genug zwischen den leistungsschwachen Erlebnissen unterscheiden können.

Wenn Sie eine statistisch signifikante Differenzierung zwischen allen Erlebnissen erstellen möchten, sollten Sie möglicherweise den manuellen Traffic-Zuordnungsmodus in Erwägung ziehen.

### Zeitkorrelierte (oder je nach Kontext variierende) Konversionsraten beeinflussen die Zuordnungsmengen.

Einige Faktoren, die während eines standardmäßigen A/B-Tests ignoriert werden können, da sie sich gleichmäßig auf alle Erlebnisse auswirken, können in einer [!UICONTROL Auto-Allocate] -Aktivität nicht ignoriert werden. Der Algorithmus reagiert auf die beobachteten Konversionsraten.

Nachfolgend finden Sie Beispiele für Faktoren, die sich ungleichmäßig auf die Erlebnisleistung auswirken können:

* Erlebnisse mit variierender kontextueller Relevanz (Zeit, Ort, Geschlecht usw.).

  Beispiel:

   * &quot;Gott sei Dank ist es Freitag&quot; führt zu höheren Konversionen am Freitag.
   * &quot;Sprungstart für Ihren Montag&quot;hat eine höhere Konversion am Montag.
   * &quot;Für einen Winter an der Ostküste aufrüsten&quot;bietet höhere Konversionsraten an Standorten an der Ostküste oder im Winter.

  Die Verwendung von Erlebnissen mit variierender kontextueller Relevanz kann die Ergebnisse in einem [!UICONTROL Auto-Allocate]-Test stärker verfälschen als in einem A/B-Test, da der A/B-Test die Ergebnisse über einen längeren Zeitraum analysiert.

* Erlebnisse mit variierenden Verzögerungen in der Konversion, möglicherweise aufgrund der Dringlichkeit der Nachricht.

  Zum Beispiel signalisiert „30 Prozent Rabatt nur noch heute“ dem Besucher, noch heute zu konvertieren, während „50 Prozent Rabatt auf Ihren ersten Einkauf“ nicht denselben Handlungsdruck auslöst.

## Häufig gestellte Fragen   {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Lesen Sie bei der Arbeit mit [!UICONTROL Auto-Allocate] -Aktivitäten die folgenden häufig gestellten Fragen und Antworten:

### Unterstützt [!UICONTROL Analytics for Target] (A4T) [!UICONTROL Auto-Allocate] Aktivitäten?

Ja. Weitere Informationen finden Sie unter [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

### Werden wiederkehrende Besucher automatisch zu leistungsstarken Erlebnissen weitergeleitet?

Nein. Nur neue Besucher werden automatisch zugeordnet. Wiederkehrende Besucher sehen weiterhin ihr ursprüngliches Erlebnis, um die Gültigkeit des A/B-Tests zu schützen.

### Wie behandelt der Algorithmus falsch-positive Ergebnisse?

Der Algorithmus garantiert eine Konfidenz von 95 % oder eine Falsch-positiv-Rate von 5 %, wenn Sie warten, bis ein Gewinnerabzeichen angezeigt wird.

### Wann beginnt [!UICONTROL Auto-Allocate] mit der Zuordnung von Traffic?

Der Algorithmus setzt ein, nachdem sämtliche Erlebnisse in der Aktivität mindestens 1.000 Besucher und 50 Konversionen erreicht haben.

### Wie aggressiv wertet der Algorithmus aus?

80 % des Traffics werden mit [!UICONTROL Auto-Allocate] und 20 % des Traffics werden zufällig bereitgestellt. Wenn ein Gewinner ermittelt wurde, erhält er 80 % des Traffics, während alle Erlebnisse weiterhin Traffic im Rahmen der 20 % erhalten, einschließlich des erfolgreichsten Erlebnisses.

### Werden verlorene Erlebnisse überhaupt angezeigt?

Ja. Die Multi-Armed Bandit-Methode stellt sicher, dass mindestens 20 % des Datenverkehrs für die Erforschung von Änderungsmustern oder Konversionsraten in allen Erlebnissen reserviert werden.

### Was passiert mit Aktivitäten mit langen Konversionsverzögerungen?

Solange alle Erlebnisse, die optimiert werden, ähnliche Verzögerungen aufweisen, entspricht das Verhalten einer Aktivität mit einem schnelleren Konversionszyklus. Es dauert jedoch länger, den Schwellenwert für 50 Konversionen zu erreichen, bevor der Traffic-Zuordnungsprozess beginnt.

### Wie unterscheidet sich [!UICONTROL Auto-Allocate] von [!UICONTROL Automated Personalization]?

[!UICONTROL Automated Personalization] verwendet die Profilattribute jedes Besuchers, um das beste Erlebnis zu ermitteln. Dadurch wird die Aktivität für den jeweiligen Besucher nicht nur optimiert, sondern auch personalisiert.

[!UICONTROL Auto-Allocate] dagegen ist ein A/B-Test, der einen aggregierten Gewinner ergibt (das beliebteste Erlebnis, aber nicht unbedingt das effektivste Erlebnis für jeden Besucher).

### Erhöhen wiederkehrende Besucher die Konversionsrate in meiner Erfolgsmetrik?

Derzeit bevorzugt die Logik Besucher, die schnell konvertieren oder häufiger besuchen, da diese Besucher die Gesamtkonversionsrate des Erlebnisses, zu dem sie gehören, vorübergehend erhöhen. Der Algorithmus passt sich häufig von selbst an, sodass die Steigerung der Konversionsrate bei jeder Momentaufnahme verstärkt wird. Wenn die Site zahlreiche wiederkehrende Besucher erhält, können ihre Konversionen die Gesamtkonversionsrate für das Erlebnis, zu dem sie gehören, potenziell erhöhen. Es bestehen gute Chancen, dass wiederkehrende Besucher per Zufall verteilt werden; in diesem Fall wird die Gesamtwirkung (Anstieg) ausgeglichen. Um diese Auswirkung zu beschränken, sollten Sie die Änderung der Zählmethode der Erfolgsmetrik erwägen, um jeden Teilnehmer nur einmal zu zählen.

### Kann ich den Rechner für die Stichprobengröße verwenden, wenn ich [!UICONTROL Auto-Allocate] verwende, um zu schätzen, wie lange die Aktivität dauert, um den Gewinner zu identifizieren?

Sie können den vorhandenen [!DNL Adobe Target] [Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) verwenden, um eine Schätzung der Laufzeit des Tests zu erhalten. (Wie bei herkömmlichen A/B-Tests wenden Sie die Bonferroni-Korrektur an, wenn Sie mehr als zwei Angebote oder mehr als eine Konversionsmetrik/Hypothese testen.) Dieser Rechner ist für herkömmliche A/B-Tests mit festem Horizont konzipiert und liefert nur eine Schätzung. Die Verwendung des Taschenrechners für eine [!UICONTROL Auto-Allocate] -Aktivität ist optional, da [!UICONTROL Auto-Allocate] einen Gewinner festlegt. Sie müssen keinen festen Zeitpunkt auswählen, um die Testergebnisse anzuzeigen. Die bereitgestellten Werte sind immer statistisch gültig.

Interne [!DNL Adobe] Experimente haben Folgendes gefunden:

* Beim Testen von genau zwei Erlebnissen ermittelt [!UICONTROL Auto-Allocate] schneller einen Gewinner als beim Test mit festem Horizont (d. h. dem vom Stichprobengrößenrechner empfohlenen Zeitrahmen), wenn der Leistungsunterschied zwischen den Erlebnissen groß ist. [!UICONTROL Auto-Allocate] benötigt jedoch möglicherweise mehr Zeit, um einen Gewinner zu identifizieren, wenn der Leistungsunterschied zwischen den Erlebnissen gering ist. In diesen Fällen wären Tests mit festem Horizont in der Regel ohne ein statistisch signifikantes Ergebnis beendet worden.
* Beim Testen von mehr als zwei Erlebnissen ermittelt [!UICONTROL Auto-Allocate] schneller einen Gewinner als beim Festen Horizont-Test (d. h. dem vom Stichprobengrößenrechner empfohlenen Zeitrahmen), wenn ein einzelnes Erlebnis alle anderen Erlebnisse deutlich übertrifft. Wenn zwei oder mehr Erlebnisse beide im Vergleich zu anderen Erlebnissen &quot;gewinnen&quot;, aber eng miteinander übereinstimmen, erfordert [!UICONTROL Auto-Allocate] möglicherweise zusätzliche Zeit, um zu ermitteln, welche höher ist. In diesen Fällen wären Tests mit festgelegtem Horizont normalerweise zu dem Schluss gekommen, dass die &quot;erfolgreichsten&quot;Erlebnisse besser waren als die Erlebnisse mit geringerer Leistung, aber nicht ermittelt hätten, welches Erlebnis überlegen war.

### Sollte ich ein leistungsschwaches Erlebnis aus einer [!UICONTROL Auto-Allocate] -Aktivität entfernen, um einen Gewinner zu bestimmen?

Es gibt wirklich keinen Grund, ein leistungsschwaches Erlebnis zu entfernen. [!UICONTROL Auto-Allocate] liefert automatisch öfter leistungsstarke Erlebnisse und liefert weniger häufig leistungsschwache Erlebnisse. Wenn Sie ein leistungsschwaches Erlebnis in der Aktivität lassen, wirkt sich dies nicht wesentlich auf die Geschwindigkeit aus, mit der ein Gewinner ermittelt wird.

20 % der Besucher werden zufällig über alle Erlebnisse verteilt. Der Traffic, der für ein leistungsschwaches Erlebnis bereitgestellt wird, ist minimal (20 % geteilt durch die Anzahl der Erlebnisse).

### Kann ich die Zielmetrik in der Mitte durch eine [!UICONTROL Auto-Allocate] -Aktivität ändern? {#change-metric}

[!DNL Adobe] rät davon ab, die Zielmetrik während einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. [!DNL Adobe] garantiert nicht, was passiert, wenn Sie die Zielmetrik in einer Aktivität ändern, nachdem sie ausgeführt wird.

Diese Empfehlung gilt für [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten, die entweder [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

### Kann ich die Berichtsquelle in der Mitte durch eine [!UICONTROL Auto-Allocate] -Aktivität ändern? {#change-reporting}

[!DNL Adobe] rät davon ab, die Berichtsquelle während der Ausführung einer Aktivität zu ändern. Es ist zwar möglich, die Berichtsquelle (von [!DNL Target] in A4T oder umgekehrt) während einer Aktivität mithilfe der [!DNL Target] -Benutzeroberfläche zu ändern, Sie sollten jedoch immer eine neue Aktivität starten. [!DNL Adobe] garantiert nicht, was passiert, wenn Sie die Berichtsquelle in einer Aktivität ändern, nachdem sie ausgeführt wird.

Diese Empfehlung gilt für [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten, die entweder [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

### Kann ich die Option [!UICONTROL Reset Report Data] beim Ausführen einer [!UICONTROL Auto-Allocate] -Aktivität verwenden?

Die Verwendung der Option [!UICONTROL Reset Report Data] für [!UICONTROL Auto-Allocate] -Aktivitäten wird nicht empfohlen. Obwohl die sichtbaren Berichtsdaten entfernt werden, werden mit dieser Option nicht alle Trainings-Datensätze aus dem Modell [!UICONTROL Auto-Allocate] entfernt. Anstatt die Option [!UICONTROL Reset Report Data] für [!UICONTROL Auto-Allocate] -Aktivitäten zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität. (Diese Anleitung gilt auch für [!UICONTROL Auto-Target] - und [!UICONTROL Automated Personalization] -Aktivitäten.)

### Wie erstellt [!UICONTROL Auto-Allocate] Modelle in Bezug auf Umgebungen?

[!UICONTROL Auto-Allocate] erstellt Modelle nur basierend auf dem Traffic- und Konversionsverhalten, das nur in der Standardumgebung aufgezeichnet wurde. Standardmäßig ist [!UICONTROL Production] die Standardumgebung, aber die Standardumgebung kann in [!DNL Target] ([Administration > Umgebungen](/help/main/administrating-target/environments.md)) geändert werden.

Tritt ein Treffer in einer anderen (nicht standardmäßigen) Umgebung auf, wird der Traffic entsprechend dem beobachteten Konversionsverhalten in der Standardumgebung verteilt. Das Ergebnis dieses Treffers (Konversion oder Nicht-Konversion) wird zu Berichtszwecken aufgezeichnet, aber nicht im Modell [!UICONTROL Auto-Allocate] berücksichtigt.

Bei Auswahl einer anderen Umgebung zeigt der Bericht Traffic und Konversionen für diese Umgebung an. Die für einen Bericht ausgewählte Standardumgebung ist die für das gesamte Konto ausgewählte Standardeinstellung. Die Standardumgebung kann nicht pro Aktivität festgelegt werden.

### Kann eine [!UICONTROL Auto-Allocate] -Aktivität das Lookback-Fenster im Verlauf eines Tests anpassen, um Trends im Zeitverlauf zu ändern?

Kann die Aktivität beispielsweise den Monat Dezember berücksichtigen, um zu entscheiden, wie Traffic zugeordnet werden soll, anstatt sich die September-Besucherdaten anzusehen (wann der Test begonnen hat)?

Nein, [!UICONTROL Auto-Allocate] berücksichtigt die Leistung der gesamten Aktivität.

### Zeigt [!UICONTROL Auto-Allocate] einem wiederkehrenden Besucher ein erfolgreichstes Erlebnis an, wenn sich das erfolgreichste Erlebnis von dem unterscheidet, das der Besucher bei der Qualifizierung für die Aktivität gesehen hat?

[!UICONTROL Auto-Allocate] verwendet Sticky-Entscheidungen aus denselben Gründen wie [!UICONTROL A/B Test]-Aktivitäten. Die Traffic-Zuordnung funktioniert nur für neue Besucher.

## Schulungsvideos {#section_893E5B36DC4A415C9B1D287F51FCCB83}

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitäts-Workflow - Targeting (2:14) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video sind Informationen zur Einrichtung der Traffic-Zuordnung enthalten.

* Zuweisen einer Zielgruppe zur Aktivität
* Regulieren von Traffic nach oben oder unten
* Auswählen der Zuordnungsmethode für den Traffic
* Zuweisen von Traffic zu verschiedenen Erlebnissen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Erstellen von A/B-Tests (8:36) ![Tutorial-Zeichen](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten Target-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird. [!UICONTROL Auto-Allocate] wird ab 04:45 besprochen.

* Erstellen einer A/B-Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
