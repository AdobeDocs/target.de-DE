---
keywords: automated traffic allocation;targeting;winner;statistical guarantee;confidence;determine winner;lift;confidence;default;default experience
description: Den Gewinner in einer A/B-Aktivität mit automatisierter Zuordnung erkennen Sie an Indikatoren in der Target-Benutzeroberfläche.
title: Ermitteln eines Gewinners
topic: Standard
uuid: 0bcc11b2-44bd-450c-a504-a8ff7a4d72e6
translation-type: tm+mt
source-git-commit: cda0765d79e370d8639d2a3177bf26be624d91c1

---


# Berichte zur automatischen Zuordnung interpretieren {#determine-a-winner}

Interpretieren Sie die Ergebnisse einer A/B-Aktivität mit automatisierter Zuordnung, indem Sie wichtige Indikatoren wie Steigerung und Konfidenz in der Target-Benutzeroberfläche untersuchen.

Viele Marketingexperten machen den Fehler, ein Erlebnis vorzeitig zum Gewinner zu erklären, bevor endgültige Ergebnisse vorliegen. Wir haben es nun leichter für Sie gemacht, den Gewinner zu ermitteln.

## Identifizieren Sie das erfolgreichste Erlebnis. {#section_24007470CF5B4D30A06610CE8DD23CE3}

Bei der Verwendung der Funktion [!UICONTROL „Automatisierte Zuordnung“] zeigt [!DNL Target] oben auf der Seite der Aktivität ein Abzeichen mit „Noch kein Gewinner“ an, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Konfidenz erreicht hat.

![Zeichen „Kein Gewinner“](/help/c-activities/automated-traffic-allocation/assets/no-winner.png)

Wenn ein eindeutiger Gewinner feststeht, zeigt [!DNL Target] „Gewinner: Erlebnis X“ an.

![](assets/auto_traffic_winner.png)

>[!NOTE]
>
>Aktivitäten mit Automatisierte Zuordnung dienen dazu, das beste Erlebnis aus allen Optionen zu ermitteln, anstatt nur paarweise Vergleiche mit Kontrollwerten durchzuführen.

## Statistical guarantees of Auto-Allocate {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Nach Abschluss einer A/B-Aktivität garantiert die automatische Zuordnung, dass der ermittelte Gewinner eine effektive Falsch-positiv-Rate von 5 % aufweist. Das bedeutet, dass der festgestellte Gewinner nur 5 % der Zeit nicht das beste Erlebnis aller in der Aktivität vorhandenen Erlebnisse ist. Für einen A/A-Test (mit identischen Erlebnissen) schließen wir einen Test nach weniger als 5 % der Zeit ab. Zu erwarten ist, dass der A/A-Test (mit identischen Erlebnissen) unbegrenzt lange läuft, ohne dass ein Siegerabzeichen angezeigt wird.

Wir verwenden keine p-Wert-basierte Konfidenz für automatisierte Zuordnung.

Die Spalte „Konfidenz“ in einer Aktivität mit automatisierter Zuordnung (siehe folgende Abbildung) zeigt mit einer Fehlerspanne von 1 %, wie wahrscheinlich ein Erlebnis der Gewinner ist (d. h., der Algorithmus verwendet einen minimalen nachweisbaren Effekt von 1 % zwischen der besten und der zweitbesten Konversionsrate). Beachten Sie, dass der Algorithmus diese Wahrscheinlichkeit anhand der [Bernstein-Ungleichheit](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) berechnet.

Bei normalen A/B-Tests wird die Konfidenz basierend auf P-Werten berechnet. Für die automatische Zuordnung werden keine P-Werte verwendet. Mit P-Werten wird „grob“ die Wahrscheinlichkeit berechnet, mit der ein bestimmtes Erlebnis vom Kontrollelement abweicht. Diese P-Werte können dazu genutzt werden, um zu bestimmen, ob sich ein Erlebnis vom Kontrollelement unterscheidet. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

Die folgende Abbildung zeigt eine Aktivität, zu der noch kein Gewinner feststeht:

![](assets/no_winner.png)

Diese Abbildung zeigt eine Aktivität, zu der es einen Gewinner gibt:

![](assets/winner_found.png)

>[!IMPORTANT]
>
>Target zeigt einen Gewinner nach einer vordefinierten Mindestanzahl an Konversionen an. Die endgültige Entscheidung, den Gewinner auszuwählen, sollte sich jedoch immer auf die Ergebnisse des Adobe Target- [Stichprobengrößenrechners](https://docs.adobe.com/content/target-microsite/testcalculator.html)stützen. Target berücksichtigt nicht die grundlegenden Konversionsraten einer Site und andere wichtige Aspekte, die in den Rechner eingespeist werden, um die Dauer der Aktivität zu bestimmen. Daher könnte Target aufgrund einer Mindestanzahl von Konversionen einen Gewinner früher als erforderlich anzeigen. Weitere Informationen finden Sie unter [Stichprobengrößenrechner](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Informationen zu Steigerungs- und Vertrauensberichten in Aktivitäten mit automatisierter Zuordnung {#lift-confidence}

Bei Aktivitäten mit automatisierter Zuordnung wird das erste Erlebnis (standardmäßig Erlebnis A genannt) auf der Registerkarte &quot;Berichte&quot;immer als Kontrollerlebnis definiert. Dieses Erlebnis wird bei der Modellierung zur Bestimmung der Leistung von Erlebnissen nicht als echte statistische Kontrolle behandelt, sondern als Referenz oder Grundlage für einige Zahlen im Bericht.

Der numerische Wert &quot;Steigerung&quot;und die Grenzen von 95 % für jedes Erlebnis werden immer unter Bezugnahme auf das definierte Erlebnis &quot;Kontrolle&quot;berechnet. Das definierte Kontrollerlebnis kann keine Steigerung im Verhältnis zu sich selbst aufweisen. Daher wird für dieses Erlebnis ein leerer &quot;—&quot;-Wert gemeldet. Im Gegensatz zu A/B-Tests wird bei Tests mit automatisierter Zuordnung kein negativer Steigerungswert gemeldet, wenn ein Erlebnis schlechter als die definierte Kontrolle ausfällt. stattdessen wird &quot;—&quot;angezeigt.

Die angezeigten Vertrauensbereich-Balken repräsentieren das Konfidenzintervall von 95 % um die mittlere Schätzung der Konversionsrate eines Erlebnisses. Diese sind auch in Bezug auf das definierte Kontrollerlebnis farbkodiert. Die Leiste des Erlebnisses &quot;Control&quot;ist immer grau gefärbt. Die Teile der Konfidenzintervalle unter dem Konfidenzintervall des &quot;Control&quot;-Erlebnisses sind rot und die Teile der Konfidenzintervalle über dem Kontrollerlebnis grün.

Ein Gewinner wird gefunden, wenn sich das 95 %-Vertrauensintervall des führenden Erlebnisses nicht mit anderen Erlebnissen überschneidet. Das Gewinner-Erlebnis wird mit einem grünen Sternzeichen links neben dem Erlebnisnamen und im Banner &quot;Gewinner&quot;gekennzeichnet. Wenn kein Stern sichtbar ist, lautet das Banner &quot;Noch kein Gewinner&quot;und ein Gewinner wurde noch nicht gefunden.

Neben dem derzeit führenden oder erfolgreichsten Erlebnis wird auch eine &quot;Konfidenz&quot;angezeigt. Diese Zahl wird erst gemeldet, wenn die Konfidenz des führenden Erlebnisses mindestens 60 % erreicht hat. Wenn genau zwei Erlebnisse im Experiment mit automatisierter Zuordnung vorhanden sind, stellt diese Zahl das Vertrauensniveau dar, dass das Erlebnis eine bessere Leistung erzielt als das andere Erlebnis. Wenn im Experiment mit der automatischen Zuordnung mehr als zwei Erlebnisse vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, das das Erlebnis besser abschneidet als das definierte Kontrollerlebnis. Wenn das Kontrollerlebnis gewinnt, wird keine &quot;Konfidenz&quot;angegeben.

## Häufig gestellte Fragen {#section_C8E068512A93458D8C006760B1C0B6A2}

**Die Aktivität ist seit mehreren Tagen online. Warum werden sämtliche Konfidenzwerte noch immer mit 0 % angegeben?**

Die folgenden Gründe erläutern, warum für sämtliche Aktivitäten in der Spalte [!UICONTROL Konfidenz] des Berichts der Wert 0 % angezeigt wird:

* Bei manuellen A/B-Tests und der automatischen Zuordnung werden verschiedene Statistiken zur Anzeige der Konfidenzwerte eingesetzt.

   Für A/B-Tests werden P-Werte verwendet, die auf [Student-T-Tests](https://en.wikipedia.org/wiki/Student%27s_t-test) basieren. Ein P-Wert gibt die Wahrscheinlichkeit an, den beobachteten (oder einen extremeren) Unterschied zwischen einem Erlebnis und dem Kontrollelement zu erhalten, wobei in Wirklichkeit kein solcher Unterschied vorliegt. Diese P-Werte können nur verwendet werden, um festzustellen, ob die beobachteten Daten mit einem bestimmten Erlebnis im Einklang stehen und das Kontrollelement identisch ist. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

   Bei der automatischen Zuordnung wird die Wahrscheinlichkeit gezeigt, mit der ein bestimmtes Erlebnis aus allen Erlebnissen als Gewinner hervorgeht. Das bedeutet, dass nur ein erfolgreichstes Erlebnis (dasjenige Erlebnis, das am wahrscheinlichsten als Gewinner hervorgeht) über einen Wert verfügt, der nicht 0 ist. Alle anderen Erlebnisse werden als wahrscheinliche Verlierer eingestuft und mit dem Wert 0 % angezeigt.

* Die Konfidenz wird in der automatischen Zuordnung nur angezeigt, nachdem das erfolgreichste Erlebnis einen Wert von mehr als 60 % erzielen konnte. Diese Konfidenzniveaus treten in der Regel in etwa der Hälfte der Zeit auf, die ein normaler A/B-Test dauern würde (obwohl dies nicht garantiert wird). To determine how long a normal A/B test would run, please use a [sample size calculator](https://docs.adobe.com/content/target-microsite/testcalculator.html): plug control&#39;s conversion-rate in &quot;Baseline conversion rate,&quot; &quot;5%&quot; for &quot;Lift,&quot; and 95% for &quot;Confidence.&quot; Typischerweise wird die Konfidenz angezeigt, nachdem jedes Erlebnis mindestens 50 % der erforderlichen Stichproben pro Erlebnis sammeln konnte. Somit erhalten Sie einen Überblick darüber, wann die Konfidenz höchstwahrscheinlich angezeigt wird.
* Wird im Bericht überall der Wert 0 % angezeigt, ist die Aktivität höchstwahrscheinlich noch nicht lange genug online.

