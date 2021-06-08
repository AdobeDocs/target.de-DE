---
keywords: automatisierte Traffic-Zuordnung; Targeting; Gewinner; statistische Garantie; Konfidenz; Gewinner bestimmen; Steigerung; Konfidenz; Standard; Standarderlebnis; automatische Zuordnung; automatische Zuordnung
description: Erfahren Sie, wie Sie die Ergebnisse einer A/B-Aktivität mit automatisierter Zuordnung in Adobe [!DNL Target] interpretieren können, indem Sie wichtige Indikatoren untersuchen, darunter Steigerung und Konfidenz.
title: Wie interpretiere ich Berichte mit automatisierter Zuordnung?
feature: Automatische Zuordnung
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
source-git-commit: 4c696f55f56a116cff61c2c307f750e72cc0107c
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 47%

---

# Interpretieren der automatischen Zuordnungsberichte

Interpretieren Sie die Ergebnisse einer [!UICONTROL Automatisierte Zuordnung] A/B-Aktivität in [!UICONTROL Adobe Target], indem Sie wichtige Indikatoren untersuchen, einschließlich Steigerung und Konfidenz.

Viele Marketingexperten machen den Fehler, ein Erlebnis vorzeitig zum erfolgreichsten zu erklären, bevor endgültige Ergebnisse vorliegen. Wir haben es nun leichter für Sie gemacht, den Gewinner zu ermitteln.

>[!NOTE]
>
>Allgemeine Informationen zur Gewinnerdeklaration finden Sie unter [Zehn häufige Fehler bei A/B-Tests und wie diese vermieden werden](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Erlebnis mit dem Gewinner identifizieren {#section_24007470CF5B4D30A06610CE8DD23CE3}

Bei der Verwendung der Funktion [!UICONTROL „Automatisierte Zuordnung“] zeigt [!DNL Target] oben auf der Seite der Aktivität ein Abzeichen mit „Noch kein Gewinner“ an, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Konfidenz erreicht hat.

![Zeichen „Kein Gewinner“](/help/c-activities/automated-traffic-allocation/assets/no-winner.png)

Wenn ein eindeutiger Gewinner feststeht, zeigt [!DNL Target] „Gewinner: Erlebnis X“ an.

![](assets/winner.png)

>[!NOTE]
>
>Aktivitäten mit Automatisierte Zuordnung dienen dazu, das beste Erlebnis aus allen Optionen zu ermitteln, anstatt nur paarweise Vergleiche mit Kontrollwerten durchzuführen.

## Statistische Garantien für die automatische Zuordnung {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Nach Abschluss einer A/B-Aktivität garantiert die automatische Zuordnung, dass der ermittelte Gewinner eine effektive Falsch-positiv-Rate von 5 % aufweist. Das bedeutet, dass der festgestellte Gewinner nur 5 % der Zeit nicht das beste Erlebnis aller in der Aktivität vorhandenen Erlebnisse ist. Für einen A/A-Test (mit identischen Erlebnissen) schließen wir einen Test nach weniger als 5 % der Zeit ab. Zu erwarten ist, dass der A/A-Test (mit identischen Erlebnissen) unbegrenzt lange läuft, ohne dass ein Siegerabzeichen angezeigt wird.

Wir verwenden keine p-Wert-basierte Konfidenz für automatisierte Zuordnung.

Die Spalte „Konfidenz“ in einer Aktivität mit automatisierter Zuordnung (siehe folgende Abbildung) zeigt mit einer Fehlerspanne von 1 %, wie wahrscheinlich ein Erlebnis der Gewinner ist (d. h., der Algorithmus verwendet einen minimalen nachweisbaren Effekt von 1 % zwischen der besten und der zweitbesten Konversionsrate). Beachten Sie, dass der Algorithmus diese Wahrscheinlichkeit anhand der [Bernstein-Ungleichheit](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) berechnet.

Bei normalen A/B-Tests wird die Konfidenz basierend auf P-Werten berechnet. Für die automatische Zuordnung werden keine P-Werte verwendet. Mit P-Werten wird „grob“ die Wahrscheinlichkeit berechnet, mit der ein bestimmtes Erlebnis vom Kontrollelement abweicht. Diese P-Werte können dazu genutzt werden, um zu bestimmen, ob sich ein Erlebnis vom Kontrollelement unterscheidet. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

>[!IMPORTANT]
>
>Target zeigt einen Gewinner nach einer vordefinierten Mindestanzahl von Konversionen an. Die endgültige Entscheidung zur Auswahl des Gewinners sollte jedoch immer auf den Ergebnissen des Adobe Target [Stichprobengrößenrechners](https://experienceleague.adobe.com/tools/calculator/testcalculator.html) basieren. Target berücksichtigt nicht die grundlegenden Konversionsraten einer Site und andere wichtige Aspekte, die in den Rechner eingespeist werden, um die Dauer der Aktivität zu bestimmen. Daher kann Target auf der Grundlage einer Mindestanzahl von Konversionen einen Gewinner anzeigen, der früher als angezeigt wurde. Weitere Informationen finden Sie unter [Stichprobengrößenrechner](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Verstehen Sie die Berichte zu Steigerung und Konfidenz in Aktivitäten mit automatisierter Zuordnung {#lift-confidence}

In Aktivitäten mit automatisierter Zuordnung wird das erste Erlebnis (standardmäßig Erlebnis A genannt) immer als Kontrollerlebnis auf der Registerkarte Berichte definiert. Dieses Erlebnis wird bei der Modellierung, die zur Ermittlung der Erlebnisleistung verwendet wird, nicht als echte statistische Kontrolle behandelt, sondern als Referenz oder Grundlage für einige Zahlen im Bericht behandelt.

Der numerische Wert &quot;Steigerung&quot;und die 95-%-Grenzen für jedes Erlebnis werden immer mit Bezug auf das definierte Kontrollerlebnis berechnet. Das definierte Kontrollerlebnis kann keine Steigerung im Verhältnis zu sich selbst aufweisen. Daher wird für dieses Erlebnis ein leerer &quot;—&quot;-Wert gemeldet. Im Gegensatz zu A/B-Tests wird bei Tests mit automatisierter Zuordnung kein negativer Steigerungswert gemeldet, wenn ein Erlebnis schlechter abschneidet als die definierte Kontrolle. stattdessen &quot;—&quot;angezeigt.

Die angezeigten Konfidenzintervallbalken stellen das Konfidenzintervall von 95 % um die mittlere Schätzung der Konversionsrate eines Erlebnisses dar. Diese sind auch in Bezug auf das definierte Kontrollerlebnis farbcodiert. Die Leiste des Kontrollerlebnisses ist immer grau gefärbt. Die Abschnitte der Konfidenzintervalle unterhalb des Konfidenzintervalls des Kontrollerlebnisses sind rot und die Teile der Konfidenzintervalle über dem Kontrollerlebnis sind grün.

Ein Gewinner wird gefunden, wenn sich das 95-%-Konfidenzintervall des führenden Erlebnisses nicht mit anderen Erlebnissen überschneidet. Das erfolgreichste Erlebnis wird mit einem grünen Sternzeichen links neben dem Erlebnisnamen und im Banner &quot;Gewinner&quot;gekennzeichnet. Wenn kein Stern sichtbar ist, lautet das Banner &quot;Noch kein Gewinner&quot;und ein Gewinner wurde noch nicht gefunden.

Neben dem derzeit führenden oder erfolgreichsten Erlebnis wird auch eine &quot;Konfidenz&quot;gemeldet. Diese Zahl wird nur gemeldet, bis die Konfidenz des führenden Erlebnisses mindestens 60 % erreicht hat. Wenn genau zwei Erlebnisse im Experiment &quot;Automatische Zuordnung&quot;vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, dass das Erlebnis eine bessere Leistung erzielt als das andere Erlebnis. Wenn im Experiment zur automatischen Zuordnung mehr als zwei Erlebnisse vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, dass das Erlebnis eine bessere Leistung erzielt als das definierte Kontrollerlebnis. Wenn das Kontrollerlebnis gewinnt, wird keine &quot;Konfidenz&quot;-Zahl gemeldet.

## Häufig gestellte Fragen   {#section_C8E068512A93458D8C006760B1C0B6A2}

**Die Aktivität ist seit mehreren Tagen online. Warum werden sämtliche Konfidenzwerte noch immer mit 0 % angegeben?**

Die folgenden Gründe erläutern, warum für sämtliche Aktivitäten in der Spalte [!UICONTROL Konfidenz] des Berichts der Wert 0 % angezeigt wird:

* Bei manuellen A/B-Tests und der automatischen Zuordnung werden verschiedene Statistiken zur Anzeige der Konfidenzwerte eingesetzt.

   Für A/B-Tests werden P-Werte verwendet, die auf [Student-T-Tests](https://en.wikipedia.org/wiki/Student%27s_t-test) basieren. Ein P-Wert gibt die Wahrscheinlichkeit an, den beobachteten (oder einen extremeren) Unterschied zwischen einem Erlebnis und dem Kontrollelement zu erhalten, wobei in Wirklichkeit kein solcher Unterschied vorliegt. Diese P-Werte können nur verwendet werden, um festzustellen, ob die beobachteten Daten mit einem bestimmten Erlebnis im Einklang stehen und das Kontrollelement identisch ist. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

   Bei der automatischen Zuordnung wird die Wahrscheinlichkeit gezeigt, mit der ein bestimmtes Erlebnis aus allen Erlebnissen als Gewinner hervorgeht. Das bedeutet, dass nur ein erfolgreichstes Erlebnis (dasjenige Erlebnis, das am wahrscheinlichsten als Gewinner hervorgeht) über einen Wert verfügt, der nicht 0 ist. Alle anderen Erlebnisse werden als wahrscheinliche Verlierer eingestuft und mit dem Wert 0 % angezeigt.

* Die Konfidenz wird in der automatischen Zuordnung nur angezeigt, nachdem das erfolgreichste Erlebnis einen Wert von mehr als 60 % erzielen konnte. Diese Konfidenzwerte treten in der Regel in etwa der Hälfte der Zeit auf, die ein normaler A/B-Test dauern würde (obwohl dies nicht garantiert ist). Um festzustellen, wie lange ein normaler A/B-Test ausgeführt werden würde, verwenden Sie einen [Stichprobengrößenrechner](https://experienceleague.adobe.com/tools/calculator/testcalculator.html): Konversionsrate der Kontrolle in &quot;Baseline-Konversionsrate&quot;, &quot;5 %&quot;für &quot;Steigerung&quot;und &quot;Konfidenz&quot;in 95 %. Typischerweise wird die Konfidenz angezeigt, nachdem jedes Erlebnis mindestens 50 % der erforderlichen Stichproben pro Erlebnis sammeln konnte. Somit erhalten Sie einen Überblick darüber, wann die Konfidenz höchstwahrscheinlich angezeigt wird.
* Wird im Bericht überall der Wert 0 % angezeigt, ist die Aktivität höchstwahrscheinlich noch nicht lange genug online.
