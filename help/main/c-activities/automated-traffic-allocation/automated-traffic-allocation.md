---
keywords: Automatisierte Traffic-Zuordnung;Zielgruppenbestimmung;Anzahl inkrementieren und Benutzer in Aktivität halten;Traffic-Zuordnung;automatische Zuordnung;automatische Zuordnung
description: Erfahren Sie, wie Sie eine [!UICONTROL Automatische Zuordnung]-Aktivität in verwenden [!DNL Adobe Target]  die einen Gewinner aus zwei oder mehr Erlebnissen identifiziert und dem Gewinner automatisch mehr Traffic zuweist.
title: Was ist eine Aktivität [!UICONTROL Automatische Zuordnung]?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
TQID: https://experienceleague.adobe.com/V5ZS2vBGVilH0-4bacB4x7iQi8M6qroLe3R9LNMoVEc
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 3756
ht-degree: 34%

---

# [!UICONTROL Automatische Zuordnung] Übersicht

Eine Aktivität [!UICONTROL Automatische Zuordnung] in [!DNL Adobe Target] identifiziert einen Gewinner aus zwei oder mehr Erlebnissen und ordnet automatisch dem Gewinner mehr Traffic zu, um die Konversionen während der Fortführung des Tests und des Lernens zu erhöhen.

Wählen [ beim Erstellen einer A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)Aktivität mithilfe des Drei-Schritte-Workflows die Option **[!UICONTROL Nach bestem Erlebnis automatisch zuordnen]** auf der Seite **[!UICONTROL Targeting]** (Schritt 2).

## Die Herausforderung {#section_85D5A03637204BACA75E19646162ACFF}

Mit A/B-Standardtests sind Kosten verbunden. Sie müssen Traffic generieren, um die Leistung jedes einzelnen Erlebnisses zu messen und durch Analysen die erfolgreichsten Erlebnisse zu ermitteln. Die Verteilung von Traffic bleibt auch dann festgelegt, wenn Sie erkennen, dass einige Erlebnisse andere übertreffen. Außerdem ist es schwierig, die Stichprobengröße korrekt zu bestimmen, und die Aktivität muss komplett durchlaufen, bevor Sie einen Sieger finden. Und es besteht immer noch eine Chance, dass der ermittelte Gewinner kein wahrer Gewinner ist.

## Die Lösung: [!UICONTROL Automatische Zuordnung] {#section_98388996F0584E15BF3A99C57EEB7629}

Eine Aktivität [!UICONTROL Automatische Zuordnung] reduziert diese Kosten und den Mehraufwand für die Bestimmung eines erfolgreichsten Erlebnisses. [!UICONTROL Automatische Zuordnung] überwacht die Leistung aller Erlebnisse bei der Zielmetrik und sendet proportional mehr neue Teilnehmer zu den leistungsstarken Erlebnissen. Es wird ausreichend Traffic für die Erkundung der anderen Erlebnisse reserviert. Sie können die Vorteile des Tests an Ihren Ergebnissen erkennen, selbst wenn die Aktivität gerade ausgeführt wird: Die Optimierung erfolgt parallel zum Lernen.

[!UICONTROL Automatische Zuordnung] verlagert Besucher schrittweise auf das erfolgreichste Erlebnis, anstatt warten zu müssen, bis eine Aktivität beendet wird, um einen Gewinner zu ermitteln. Sie profitieren schneller von Steigerungen, da den Aktivitätsteilnehmern, die zu weniger erfolgreichen Erlebnissen geleitet worden wären, nun potenziell erfolgreiche Erlebnisse angezeigt werden.

Ein normaler A/B-Test in [!DNL Target] zeigt nur paarweise Vergleiche von Herausforderern mit der Kontrolle. Wenn beispielsweise eine Aktivität die Erlebnisse A, B, C und D aufweist, wobei A die Kontrolle ist, würde ein normaler [!DNL Target]-A/B-Test A mit B, A mit C und A mit D vergleichen.

Bei solchen Tests verwenden die meisten Produkte, einschließlich [!DNL Target], einen [Welchs t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank}, um ein auf p-Werten basierendes Vertrauen herzustellen. Mithilfe dieses Konfidenzwerts wird dann ermittelt, ob sich der Herausforderer ausreichend vom Kontrollelement unterscheidet. [!DNL Target] führt jedoch nicht automatisch die impliziten Vergleiche (B versus C, B versus D und C versus D) durch, die erforderlich sind, um das „beste“ Erlebnis zu finden. Aus diesem Grund müssen Marketingexperten die Ergebnisse manuell analysieren, um das Gewinnererlebnis zu ermitteln.

[!UICONTROL Automatische Zuordnung] führt alle impliziten Vergleiche über Erlebnisse hinweg durch und erzeugt einen „echten“ Gewinner. Es gibt in diesem Test keinen Bedarf für ein „Kontrollerlebnis“.

[!UICONTROL Automatische Zuordnung] Weist neuen Besuchern auf intelligente Weise Erlebnisse zu, bis sich das Konfidenzintervall des besten Erlebnisses nicht mit dem Konfidenzintervall eines anderen Erlebnisses überschneidet. Normalerweise könnte dieser Prozess falsch-positive Ergebnisse hervorrufen, aber [!UICONTROL Automatische Zuordnung] verwendet Konfidenzintervalle, die auf der [Bernstein-Ungleichung](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29){target=_blank} basieren und wiederholte Auswertungen kompensieren. An dieser Stelle gibt es einen wahren Gewinner. Wenn die [!UICONTROL Automatische Zuordnung] beendet wird, sofern es keine wesentliche Zeitabhängigkeit zu den Besucherinnen und Besuchern gibt, die auf die Seite gelangen, besteht eine Chance von mindestens 95 %, dass [!UICONTROL Automatische Zuordnung] ein Erlebnis zurückgibt, dessen wahre Antwort nicht schlechter als 1 % (relativ) weniger als die wahre Antwort des erfolgreichsten Erlebnisses ist.

## Wann die Aktivität [!UICONTROL Automatische Zuordnung] versus [!UICONTROL A/B-Test] oder [!UICONTROL Automated Personalization] verwendet werden sollte {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Die Funktion **[!UICONTROL Automatisierte Zuordnung]** verwenden Sie, wenn Sie Ihre Aktivitäten von Anfang an optimieren und so schnell wie möglich feststellen möchten, welche die erfolgreichsten Erlebnisse sind. Wenn Sie häufiger Erlebnisse mit hoher Performance bereitstellen, wird die Gesamtleistung der Aktivität gesteigert.
* Verwenden Sie einen standardmäßigen **[A/B](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** Test, wenn Sie die Leistung aller Erlebnisse charakterisieren möchten, bevor Sie Ihre Site optimieren. Mit einem A/B-Test können Sie alle Ihre Erlebnisse nach Rang ordnen, während [!UICONTROL Automatische Zuordnung] die besten Ergebnisse findet, aber keine Unterscheidung zwischen den leistungsschwächeren gewährleistet.
* Verwenden Sie [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) wenn Sie Optimierungsalgorithmen mit höchster Komplexität benötigen, z. B. Modelle für maschinelles Lernen, die Prognosen basierend auf einzelnen Profilattributen erstellen. [!UICONTROL Automatische Zuordnung] untersucht das aggregierte Verhalten von Erlebnissen (genau wie Standard-A/B-Tests) und unterscheidet nicht zwischen Besuchern.

## Die wichtigsten Vorteile von [!UICONTROL Automatische Zuordnung] {#section_0913BF06F73C4794862561388BBDDFF0}

* Behält die Genauigkeit eines A/B-Tests bei
* Ermittelt einen statistisch bedeutenden Sieger schneller als mit manuellen A/B-Tests
* Bietet höhere durchschnittliche Kampagnensteigerungen im Vergleich zu manuellen A/B-Tests

## Terminologie {#section_670F8785BA894745B43B6D4BFF953188}

Die folgenden Begriffe sind bei der Diskussion von [!UICONTROL Automatische Zuordnung] hilfreich:

**Multi-Armed Bandit:** Eine [Multi-Armed Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank}-Vorgehensweise („Mehrarmiger Bandit“) zur Optimierung gleicht forschendes Lernen und die Verwertung dieses Lernens aus.

## Funktionsweise des Algorithmus {#section_ADB69A1C7352462D98849F2918D4FF7B}

Die allgemeine Logik hinter [!UICONTROL Automatische Zuordnung] umfasst sowohl die gemessene Leistung (z. B. Konversionsrate) als auch Konfidenzintervalle der kumulativen Daten. Im Gegensatz zu einem standardmäßigen A/B-Test, bei dem der Traffic gleichmäßig auf die Erlebnisse aufgeteilt wird[!UICONTROL  ändert die ]Automatische Zuordnung) die Traffic-Zuordnung zwischen den Erlebnissen.

* 80 % der Besucher werden mithilfe der unten beschriebenen intelligenten Logik zugeordnet.
* 20 % der Besucher werden nach dem Zufallsprinzip allen Erlebnissen zugewiesen, um sich an das sich ändernde Besucherverhalten anzupassen.

Die Multi-Armed Bandit-Methode hält einige Erlebnisse für die Erforschung frei, während die leistungsstarken Erlebnisse ausgewertet werden. Es werden mehr neue Besucher in leistungsstärkere Erlebnisse platziert, und gleichzeitig wird die Reaktionsfähigkeit auf sich ändernde Bedingungen beibehalten. Diese Modelle werden mindestens einmal pro Stunde aktualisiert, um sicherzustellen, dass das Modell auf die neuesten Daten reagiert.

Sobald mehr Besucher an der Aktivität teilnehmen, erweisen sich einige Erlebnisse als erfolgreicher und erhalten mehr Traffic. 20 Prozent des Datenverkehrs werden weiterhin per Zufall verteilt, um alle Erlebnisse zu erforschen. Wenn ein Erlebnis mit einer schlechteren Leistung anfängt, sich zu verbessern, erhält es mehr Traffic. Oder: Wenn eine erfolgreiche Aktivität nachlässt, wird diesem Erlebnis weniger Traffic zugeordnet. Zum Beispiel wenn ein Ereignis dazu führt, dass Besucher nach anderen Informationen auf Ihrer Medienwebsite suchen oder wenn Wochenendverkäufe auf Ihrer Retail-Website unterschiedliche Ergebnisse liefern.

Die folgende Abbildung zeigt, wie der Algorithmus bei einem Test mit vier Erlebnissen funktionieren könnte (klicken Sie hier, um die Abbildung zu erweitern):

![Bild automatisch zuweisen](assets/auto-allocate.png){width="600" zoomable="yes"}

Die Abbildung zeigt, wie sich der den einzelnen Erlebnissen zugeordnete Traffic ändert, während die Aktivität mehrere Runden durchläuft, bis ein Gewinner gefunden ist.

| Round | Beschreibung |
|--- |--- |
| ![Aufwärmrunde](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png){width="200" zoomable="yes"} | **Aufwärmrunde (0)**: Während der Aufwärmrunde wird für jedes Erlebnis gleich viel Traffic zugeteilt, bis jedes Erlebnis in der Aktivität mindestens 1.000 Besucher und 50 Konversionen aufweist.<ul><li>Erlebnis A = 25 %</li><li>Erlebnis B = 25 %</li><li>Erlebnis C = 25 %</li><li>Erlebnis D = 25 %</li></ul>Nachdem jedes Erlebnis 1.000 Besucher und 50 Konversionen erreicht hat, startet [!DNL Target] die automatische Traffic-Zuordnung. Sämtliche Zuordnungen werden in Runden vorgenommen, wobei für jede Runde zwei Erlebnisse herausgesucht werden.<br>Nur zwei Erlebnisse gehen in die nächste Runde über: D und C<br>Vorwärts bedeutet, dass die beiden Erlebnisse zu 80 % dem Traffic gleich zugewiesen werden. Die beiden anderen Erlebnisse sind weiterhin Teil der Teilnahme, werden aber nur als Teil der 20-%-Traffic-Zuordnung bereitgestellt, wenn neue Besucher in die Aktivität eintreten.<br>Sämtliche Zuordnungen werden stündlich aktualisiert (erkennbar an der Rundenangabe auf der X-Achse in der Abbildung oben). Nach jeder Runde werden die kumulativen Daten verglichen. |
| ![Runde 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png){width="200" zoomable="yes"} | **Runde 1**: Während dieser Runde werden 80% des Traffics den Erlebnissen C und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis den Erlebnissen A, B, C und D zugeordnet (jeweils 5 %). Während dieser Runde werden beim Erlebnis A gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt Erlebnis D aus, um in die nächste Runde zu wechseln, da er die höchste Konversionsrate hat (wie durch die vertikale Skala jeder Aktivität angegeben).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis A für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und A gelangen eine Runde weiter. |
| ![Runde 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png){width="200" zoomable="yes"} | **Runde 2**: Während dieser Runde werden 80% des Traffics den Erlebnissen A und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis B gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt Erlebnis D aus, um in die nächste Runde zu wechseln, da er die höchste Konversionsrate hat (wie durch die vertikale Skala jeder Aktivität angegeben).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis B für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und B gelangen eine Runde weiter. |
| ![Runde 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png){width="200" zoomable="yes"} | **Runde 3**: Während dieser Runde werden 80% des Traffics den Erlebnissen B und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis D weiterhin gute Leistungen verzeichnet und auch das Erlebnis C läuft gut.<ul><li>Der Algorithmus wählt Erlebnis D aus, um in die nächste Runde zu wechseln, da er die höchste Konversionsrate hat (wie durch die vertikale Skala jeder Aktivität angegeben).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis C für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und C gelangen eine Runde weiter. |
| ![Runde 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png){width="200" zoomable="yes"} | **Runde 4**: Während dieser Runde werden 80% des Traffics den Erlebnissen C und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis C gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt Erlebnis C aus, um in die nächste Runde zu gelangen, da es die höchste Konversionsrate aufweist (wie durch die vertikale Skala jeder Aktivität angegeben).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis D für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse C und D gelangen eine Runde weiter. |
| ![Runde n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png){width="200" zoomable="yes"} | **Round *n***: Im Laufe der Aktivität beginnt ein leistungsstarkes Erlebnis zu entstehen, und der Prozess wird fortgesetzt, bis es ein erfolgreichstes Erlebnis gibt. Wenn sich das Konfidenzintervall des Erlebnisses mit der höchsten Konversionsrate nicht mit dem Konfidenzintervall eines anderen Erlebnisses überschneidet, wird es als Gewinner gekennzeichnet. Auf [ Seite der erfolgreichsten Aktivität und in der Liste ](/help/main/c-activities/automated-traffic-allocation/determine-winner.md)Aktivität[!UICONTROL  wird ] Abzeichen angezeigt.<ul><li>Der Algorithmus erklärt das Erlebnis C zum klaren Gewinner.</li></ul>An diesem Punkt ordnet der Algorithmus 80 % des Traffics Erlebnis C zu, während 20 % des Traffics weiterhin auf zufälliger Basis allen Erlebnissen (A, B, C und D) zugeordnet werden. C erhält insgesamt 85 % des Traffics. In dem unwahrscheinlichen Fall, dass das Konfidenzintervall des Gewinners erneut anfängt, andere Intervalle zu überdecken, kehrt der Algorithmus zu dem Verhalten der obigen Runde 4 zurück.<P>**Wichtig**: Wenn Sie früher im Prozess manuell einen Gewinner ausgewählt haben, wäre es einfach gewesen, das falsche Erlebnis auszuwählen. Daher empfiehlt es sich unbedingt, so lange zu warten, bis der Algorithmus das „siegreiche“ Erlebnis ermittelt hat. |

>[!NOTE]
>
>Wenn eine Aktivität nur zwei Erlebnisse hat, erhalten beide Erlebnisse gleichen Traffic, bis [!DNL Target] mit 75 % Zuversicht ein erfolgreichstes Erlebnis findet. Zu diesem Zeitpunkt werden zwei Drittel des Traffics dem Gewinner und ein Drittel dem Verlierer zugewiesen. Wenn danach ein Erlebnis 95 % Vertrauen erreicht, werden 90 % des Traffics dem Gewinner und 10 % dem Verlierer zugewiesen. [!DNL Target] sendet immer etwas Traffic an das „Verlierer“-Erlebnis, um am Ende falsch positive Ergebnisse zu vermeiden (d. h. einige Exploration aufrechtzuerhalten).

Nachdem eine Aktivität [!UICONTROL Automatische Zuordnung] aktiviert wurde, sind die folgenden Vorgänge in der Tar-[!DNL]-Benutzeroberfläche nicht mehr zulässig:

* Umschalten des Modus „Traffic-Zuordnung“ auf „Manuell“
* Ändern des Zielmetriktyps
* Ändern von Optionen im Bedienfeld [!UICONTROL Erweiterte Einstellungen]

## So funktioniert die automatische Zuordnung

Weitere Informationen finden Sie unter [Durch automatische Zuordnung erhalten Sie schneller Testergebnisse und mehr Umsätze als mit manuellen Tests](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md).

## Einschränkungen {#section_5C83F89F85C14FD181930AA420435E1D}

Beachten Sie bei der Arbeit mit „Automatische Zuordnung[!UICONTROL  die folgenden Informationen]:

### Die [!UICONTROL Automatische Zuordnung] funktioniert mit nur einer erweiterten Metrikeinstellung: [!UICONTROL Anzahl erhöhen und Benutzer in Aktivität halten]

Die folgenden erweiterten Metrikeinstellungen werden nicht unterstützt: [!UICONTROL Anzahl erhöhen], [!UICONTROL Benutzer freigeben], [!UICONTROL Erneuten Eintritt erlauben und Anzahl erhöhen] und [!UICONTROL Benutzer freigeben und bei erneuten Eintritt sperren].

### Häufig wiederkehrende Besucher können die Konversionsraten von Erlebnissen in die Höhe treiben.

Wenn ein Besucher, der Erlebnis A anzeigt, häufig zurückkehrt und mehrere Male konvertiert, wird die Konversionsrate (CR) von Erlebnis A künstlich erhöht. Vergleichen Sie dieses Ergebnis mit Erlebnis B, bei dem Besucher konvertieren, aber nicht oft zurückkehren. Daher sieht die CR von Erlebnis A besser aus als die CR von Erlebnis B, sodass neue Besucher eher A als B zugewiesen werden. Wenn Sie sich dafür entscheiden, einmal pro Teilnehmer zu zählen, können die CR von A und CR von B identisch sein.

Wenn wiederkehrende Besucher zufällig verteilt werden, wird ihre Wirkung auf die Konversionsrate wahrscheinlich eher ausgeglichen. Um diese Auswirkung zu beschränken, sollten Sie die Änderung der Zählmethode der Zielmetrik erwägen, um jeden Teilnehmer nur einmal zu zählen.

### Unterscheidet zwischen leistungsstarken und nicht zwischen leistungsschwachen Anbietern.

[!UICONTROL Automatische Zuordnung] eignet sich gut zur Unterscheidung zwischen Erlebnissen mit hoher Leistung (und zur Ermittlung eines Gewinners). Es kann vorkommen, dass Sie nicht genug zwischen den leistungsschwachen Erlebnissen unterscheiden können.

Wenn Sie eine statistisch signifikante Unterscheidung zwischen allen Erlebnissen vornehmen möchten, sollten Sie den Modus für die manuelle Traffic-Zuordnung verwenden.

### Zeitkorrelierte (oder kontextuell variierende) Konversionsraten können die Zuteilungsbeträge verfälschen.

Einige Faktoren, die bei einem standardmäßigen A/B-Test ignoriert werden können, da sie alle Erlebnisse gleichermaßen betreffen, können bei einer Aktivität [!UICONTROL Automatische Zuordnung] nicht ignoriert werden. Der Algorithmus ist gegenüber den beobachteten Konversionsraten empfindlich.

Nachfolgend finden Sie Beispiele für Faktoren, die sich ungleichmäßig auf die Erlebnisleistung auswirken können:

* Erlebnisse mit unterschiedlicher kontextueller Relevanz (Zeit, Ort, Geschlecht usw.).

  Beispiel:

   * „Gott sei Dank ist Freitag“ führt zu höheren Konversionen am Freitag.
   * „Jump-start your Monday“ hat am Montag eine höhere Konversionsrate.
   * „Gear up for an East-Coast winter“ bietet höhere Konversionsraten an Ost- oder Winterstandorten.

  Die Verwendung von Erlebnissen mit unterschiedlicher kontextueller Relevanz kann die Ergebnisse in einem [!UICONTROL Automatische Zuordnung]-Test stärker verfälschen als in einem A/B-Test, da der A/B-Test die Ergebnisse über einen längeren Zeitraum analysiert.

* Erlebnisse mit variierenden Verzögerungen in der Konversion, möglicherweise aufgrund der Dringlichkeit der Nachricht.

  Zum Beispiel signalisiert „30 Prozent Rabatt nur noch heute“ dem Besucher, noch heute zu konvertieren, während „50 Prozent Rabatt auf Ihren ersten Einkauf“ nicht denselben Handlungsdruck auslöst.

## Häufig gestellte Fragen {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Konsultieren Sie bei Problemen mit automatischen Zuordnungs[!UICONTROL -Aktivitäten die folgenden häufig gestellten Fragen ] Antworten:

### Unterstützt [!UICONTROL Analytics for Target] (A4T) [!UICONTROL automatische Zuordnung]-Aktivitäten?

Ja. Weitere Informationen finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

### Werden wiederkehrende Besucher automatisch Erlebnissen mit hoher Leistung zugewiesen?

Nein. Nur neue Besucher werden automatisch zugeordnet. Wiederkehrende Besucher sehen weiterhin ihr ursprüngliches Erlebnis, um die Gültigkeit des A/B-Tests zu schützen.

### Wie behandelt der Algorithmus falsch-positive Ergebnisse?

Der Algorithmus garantiert eine Konfidenz von 95 % oder eine Falsch-positiv-Rate von 5 %, wenn Sie warten, bis ein Gewinnerabzeichen angezeigt wird.

### Wann beginnt [!UICONTROL Automatische Zuordnung] mit der Traffic-Zuordnung?

Der Algorithmus setzt ein, nachdem sämtliche Erlebnisse in der Aktivität mindestens 1.000 Besucher und 50 Konversionen erreicht haben.

### Wie aggressiv nutzt der Algorithmus aus?

80 % des Traffics werden mit [!UICONTROL Automatische Zuordnung] und 20 % des Traffics wird nach dem Zufallsprinzip bereitgestellt. Wenn ein Gewinner ermittelt wurde, gehen 80 % des Traffics an ihn, während alle Erlebnisse im Rahmen der 20 % weiterhin Traffic erhalten, einschließlich des erfolgreichsten Erlebnisses.

### Werden überhaupt Erlebnisse gezeigt?

Ja. Die Multi-Armed Bandit-Methode stellt sicher, dass mindestens 20 % des Datenverkehrs für die Erforschung von Änderungsmustern oder Konversionsraten in allen Erlebnissen reserviert werden.

### Was passiert mit Aktivitäten mit langen Konversionsverzögerungen?

Solange alle optimierten Erlebnisse ähnliche Verzögerungen aufweisen, ist das Verhalten dasselbe wie bei einer Aktivität mit schnellerem Konversionszyklus. Es dauert jedoch länger, bis der Konversionsschwellenwert von 50 erreicht ist, bevor der Traffic-Zuordnungsprozess beginnt.

### Wie unterscheidet sich [!UICONTROL Automatische Zuordnung] von [!UICONTROL Automated Personalization]?

[!UICONTROL Automated Personalization] verwendet die Profilattribute jedes Besuchers, um das beste Erlebnis zu ermitteln. Dadurch wird die Aktivität für den jeweiligen Besucher nicht nur optimiert, sondern auch personalisiert.

[!UICONTROL Automatische Zuordnung] ist dagegen ein A/B-Test, der einen aggregierten Gewinner erzeugt (das beliebteste Erlebnis, aber nicht unbedingt das effektivste Erlebnis für jeden Besucher).

### Erhöhen wiederkehrende Besucher die Konversionsrate in meiner Erfolgsmetrik?

Derzeit bevorzugt die Logik Besucher, die schnell konvertieren oder öfter besuchen, da solche Besucher die Gesamtkonversionsrate des Erlebnisses, zu dem sie gehören, vorübergehend erhöhen. Der Algorithmus passt sich häufig von selbst an, sodass die Steigerung der Konversionsrate bei jeder Momentaufnahme verstärkt wird. Wenn die Website viele wiederkehrende Besucher erhält, können deren Konversionen möglicherweise die Gesamtkonversionsrate für das Erlebnis, zu dem sie gehören, in die Höhe treiben. Es bestehen gute Chancen, dass wiederkehrende Besucher per Zufall verteilt werden; in diesem Fall wird die Gesamtwirkung (Anstieg) ausgeglichen. Um diese Auswirkung zu beschränken, sollten Sie die Änderung der Zählmethode der Erfolgsmetrik erwägen, um jeden Teilnehmer nur einmal zu zählen.

### Kann ich den Stichprobengrößenrechner bei Verwendung von [!UICONTROL Automatische Zuordnung] verwenden, um zu schätzen, wie lange die Aktivität dauert, um den Gewinner zu ermitteln?

Sie können den vorhandenen [!DNL Adobe Target] ([) verwenden](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) um eine Schätzung der Dauer des Tests zu erhalten. (Wie bei herkömmlichen A/B-Tests wird die Bonferroni-Korrektur angewendet, wenn Sie mehr als zwei Angebote oder mehr als eine Konversionsmetrik/Hypothese testen.) Dieser Rechner ist für herkömmliche A/B-Tests mit festem Horizont konzipiert und bietet nur eine Schätzung. Die Verwendung des Taschenrechners für eine Aktivität [!UICONTROL Automatische Zuordnung] ist optional, da [!UICONTROL Automatische Zuordnung] für Sie einen Gewinner bestimmt. Sie müssen keinen festen Zeitpunkt auswählen, um sich die Testergebnisse anzusehen. Die angegebenen Werte sind immer statistisch gültig.

Interne [!DNL Adobe] haben Folgendes ergeben:

* Wenn Sie genau zwei Erlebnisse testen[!UICONTROL  findet die ] „Automatische Zuordnung“ schneller einen Gewinner als Tests mit festem Zeithorizont (d. h. den vom Stichprobengrößenrechner vorgeschlagenen Zeitrahmen), wenn der Leistungsunterschied zwischen Erlebnissen groß ist. Bei der [!UICONTROL automatischen Zuordnung] kann jedoch mehr Zeit erforderlich sein, um einen Gewinner zu ermitteln, wenn der Leistungsunterschied zwischen Erlebnissen gering ist. In diesen Fällen wären Fixed-Horizon-Tests in der Regel ohne ein statistisch signifikantes Ergebnis beendet worden.
* Beim Testen von mehr als zwei Erlebnissen findet [!UICONTROL Automatische Zuordnung] schneller einen Gewinner als Tests mit festem Zeithorizont (d. h. der vom Stichprobengrößenrechner vorgeschlagene Zeitrahmen), wenn ein einzelnes Erlebnis alle anderen Erlebnisse deutlich übertrifft. Wenn zwei oder mehr Erlebnisse beide im Vergleich zu anderen Erlebnissen „gewinnen“, aber eng aufeinander abgestimmt sind, kann [!UICONTROL Automatische Zuordnung] zusätzliche Zeit erfordern, um zu ermitteln, welches Erlebnis besser ist. In diesen Fällen hätten Tests mit festem Zeithorizont normalerweise zu dem Schluss geführt, dass die „erfolgreichsten“ Erlebnisse besser waren als die Erlebnisse mit schlechterer Leistung, aber nicht herausgefunden, welches Erlebnis überlegen war.

### Sollte ich ein Erlebnis mit unzureichender Leistung aus einer Aktivität [!UICONTROL Automatische Zuordnung] entfernen, um den Prozess der Gewinnerbestimmung zu beschleunigen?

Es gibt wirklich keinen Grund, ein leistungsschwaches Erlebnis zu beseitigen. [!UICONTROL Automatische Zuordnung] stellt automatisch häufiger Erlebnisse mit hoher Leistung bereit und seltener Erlebnisse mit geringer Leistung. Ein unterdurchschnittliches Erlebnis in der Aktivität hat keine signifikanten Auswirkungen auf die Geschwindigkeit, um einen Gewinner zu bestimmen.

20 % der Besucher werden zufällig über alle Erlebnisse verteilt. Der Traffic, der einem Erlebnis mit unzureichender Leistung zugewiesen wird, ist minimal (20 % dividiert durch die Anzahl der Erlebnisse).

### Kann ich die Zielmetrik inmitten einer Aktivität mit automatisierter [!UICONTROL  ändern]? {#change-metric}

[!DNL Adobe] empfiehlt nicht, die Zielmetrik inmitten einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. [!DNL Adobe] garantiert nicht, was passiert, wenn Sie die Zielmetrik in einer Aktivität nach deren Ausführung ändern.

Diese Empfehlung gilt für [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

### Kann ich die Berichtsquelle mittendrin durch eine Aktivität [!UICONTROL Automatische Zuordnung] ändern? {#change-reporting}

[!DNL Adobe] empfiehlt nicht, die Berichtsquelle inmitten einer Aktivität zu ändern. Obwohl es möglich ist, die Berichtsquelle (von [!DNL Target] zu A4T oder umgekehrt) während einer Aktivität über die [!DNL Target]-Benutzeroberfläche zu ändern, sollten Sie immer eine neue Aktivität starten. [!DNL Adobe] garantiert nicht, was passiert, wenn Sie die Berichtsquelle in einer Aktivität ändern, nachdem sie ausgeführt wird.

Diese Empfehlung gilt für [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

### Kann ich die Option [!UICONTROL Berichtsdaten zurücksetzen] während ich eine Aktivität [!UICONTROL Automatische Zuordnung] ausführe?

Die Verwendung [!UICONTROL  Option „Berichtsdaten zurücksetzen] für [!UICONTROL automatische Zuordnung]-Aktivitäten wird nicht empfohlen. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem Modell [!UICONTROL Automatische Zuordnung]. Statt für eine Aktivität des Typs „Automatische Zuordnung[!UICONTROL  die Option ]Berichtsdaten zurücksetzen[!UICONTROL  zu verwenden, ] eine neue Aktivität erstellt und die ursprüngliche Aktivität deaktiviert. (Diese Anleitung gilt auch für [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization]-Aktivitäten.)

### Wie erstellt [!UICONTROL Automatische Zuordnung] Modelle in Bezug auf Umgebungen?

[!UICONTROL Automatische Zuordnung] erstellt Modelle nur basierend auf dem Traffic- und Konversionsverhalten, das in der Standardumgebung aufgezeichnet wurde. Standardmäßig ist [!UICONTROL Produktion] die Standardumgebung, aber die Standardumgebung kann in [!DNL Target] geändert werden [Administration > Umgebungen](/help/main/administrating-target/environments.md).

Wenn ein Treffer in einer anderen (nicht standardmäßigen) Umgebung auftritt, wird der Traffic entsprechend dem beobachteten Konversionsverhalten in der Standardumgebung verteilt. Das Ergebnis dieses Treffers (Konversion oder Nicht-Konversion) wird zu Berichtszwecken aufgezeichnet, aber im Modell [!UICONTROL Automatische Zuordnung] nicht berücksichtigt.

Bei Auswahl einer anderen Umgebung zeigt der Bericht Traffic und Konversionen für diese Umgebung an. Die standardmäßig ausgewählte Umgebung für einen Bericht ist die Standardeinstellung, die für das gesamte Konto ausgewählt ist. Die Standardumgebung kann nicht für jede Aktivität festgelegt werden.

### Kann mit [!UICONTROL  Aktivität Automatische Zuordnung ] Lookback-Fenster während eines Tests angepasst werden, um Veränderungen im Zeitverlauf zu berücksichtigen?

Kann die Aktivität beispielsweise den Monat Dezember heranziehen, um zu entscheiden, wie der Traffic zugeordnet werden soll, anstatt sich die Besucherdaten vom September anzusehen (als der Test begann)?

Nein, [!UICONTROL Automatische Zuordnung] berücksichtigt die Leistung der gesamten Aktivität.

### Wird [!UICONTROL Automatische Zuordnung] einem wiederkehrenden Besucher das erfolgreichste Erlebnis angezeigt, wenn sich das erfolgreichste Erlebnis von dem unterscheidet, das der Besucher bei der Qualifizierung für die Aktivität gesehen hat?

[!UICONTROL Automatische Zuordnung] verwendet Sticky Decisioning aus denselben Gründen, aus denen [!UICONTROL A/B-Test]-Aktivitäten persistent sind. Die Traffic-Zuordnung funktioniert nur für neue Besucher.

## Schulungsvideos {#section_893E5B36DC4A415C9B1D287F51FCCB83}

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitäts-Workflow - Targeting (2:14) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video sind Informationen zur Einrichtung der Traffic-Zuordnung enthalten.

* Zuweisen einer Zielgruppe zur Aktivität
* Regulieren von Traffic nach oben oder unten
* Auswählen der Zuordnungsmethode für den Traffic
* Zuweisen von Traffic zu verschiedenen Erlebnissen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Erstellen von A/B-Tests (:36) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten Target-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird. [!UICONTROL Automatische Zuordnung] wird ab 4 :45 erläutert.

* Erstellen einer A/B-Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
