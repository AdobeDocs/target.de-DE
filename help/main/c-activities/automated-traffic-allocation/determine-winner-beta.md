---
keywords: automatisierte Traffic-Zuordnung; Targeting; Gewinner; statistische Garantie; Konfidenz; Gewinner bestimmen; Steigerung; Konfidenz; Standard; Standarderlebnis; automatische Zuordnung; automatische Zuordnung
description: Erfahren Sie, wie Sie [!UICONTROL Auto-Allocate] A/B-Aktivitätsergebnisse interpretieren und sich dabei auf Schlüsselindikatoren wie Steigerung und Konfidenz konzentrieren.
title: Wie interpretiere ich [!UICONTROL Auto-Allocate]-Berichte?
feature: Auto-Allocate
hide: true
hidefromtoc: true
source-git-commit: 5fc18c6d3b493ea0a58048cc20ce3a6c2ffb7d14
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 20%

---

# Interpretieren von [!UICONTROL Auto-Allocate] -Berichten

Interpretieren Sie die Ergebnisse einer [!UICONTROL Auto-Allocate] A/B-Aktivität in [!UICONTROL Adobe Target], indem Sie wichtige Indikatoren untersuchen, einschließlich Steigerung und Konfidenz.

Viele Marketingexperten machen den Fehler, ein Erlebnis vorzeitig zum Gewinner zu erklären, bevor endgültige Ergebnisse vorliegen. [!DNL Target] erleichtert es Ihnen, den Gewinner zu bestimmen.

Allgemeine Informationen zum Deklarieren eines Gewinners finden Sie unter [Zehn häufige Fehler bei A/B-Tests und wie diese vermieden werden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Erlebnis mit dem Gewinner identifizieren {#section_24007470CF5B4D30A06610CE8DD23CE3}

Bei Verwendung der Funktion [!UICONTROL Auto-Allocate] zeigt [!DNL Target] oben auf der Seite der Aktivität ein Abzeichen mit &quot;Noch kein Gewinner&quot;an, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Konfidenz erreicht hat.

![Zeichen „Kein Gewinner“](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

Wenn ein eindeutiger Gewinner feststeht, zeigt [!DNL Target] das Zeichen &quot;Gewinner: Erlebnis *X*&quot;an.

![Gewinnerabzeichen](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

>[!NOTE]
>
>[!UICONTROL Auto-Allocate] -Aktivitäten dienen dazu, das beste Erlebnis aus allen Optionen zu finden und nicht nur paarweise Vergleiche mit Kontrollwerten durchzuführen.

## Statistische Garantien von [!UICONTROL Auto-Allocate] {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Am Ende einer A/B-Aktivität garantiert [!UICONTROL Auto-Allocate], dass der ermittelte Gewinner eine effektive Falsch-Positiv-Rate von 5 % aufweist. Das bedeutet, dass der festgestellte Gewinner nur 5 % der Zeit nicht das beste Erlebnis aller in der Aktivität vorhandenen Erlebnisse ist. Für einen [A/A-Test](/help/main/c-activities/t-test-ab/aa-testing.md) (mit identischen Erlebnissen) schließt [!DNL Target] einen Test ab, der weniger als 5 % der Zeit beträgt. Zu erwarten ist, dass der A/A-Test (mit identischen Erlebnissen) unbegrenzt lange läuft, ohne dass ein Siegerabzeichen angezeigt wird.

[!DNL Target] verwendet keine p-Wert-basierte Konfidenz für [!UICONTROL Auto-Allocate].

Die Spalte [!UICONTROL Confidence] in einer [!UICONTROL Auto-Allocate] -Aktivität zeigt die Wahrscheinlichkeit an, mit der ein Erlebnis der Gewinner ist, innerhalb einer Fehlergrenze von 1 %. Der Algorithmus verwendet einen minimalen erkennbaren Effekt von 1 % zwischen den besten und den zweitbesten Konversionsraten. Der Algorithmus verwendet [Bernstein-Ungleichung](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29), um diese Wahrscheinlichkeit zu berechnen.

Bei normalen A/B-Tests wird die Konfidenz basierend auf P-Werten berechnet. [!UICONTROL Auto-Allocate] verwendet keine p-Werte. Mit P-Werten wird „grob“ die Wahrscheinlichkeit berechnet, mit der ein bestimmtes Erlebnis vom Kontrollelement abweicht. Diese P-Werte können dazu genutzt werden, um zu bestimmen, ob sich ein Erlebnis vom Kontrollelement unterscheidet. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

>[!IMPORTANT]
>
>[!DNL Target] zeigt einen Gewinner nach einer vordefinierten Mindestanzahl von Konversionen an. Die endgültige Entscheidung, den Gewinner auszuwählen, sollte sich jedoch immer auf die Ergebnisse des [!DNL Adobe Target] Stichprobengrößenrechners beziehen. [!DNL Target] berücksichtigt nicht die grundlegenden Konversionsraten einer Site und andere wichtige Aspekte, die in den Rechner eingespeist werden, um die Dauer der Aktivität zu bestimmen. Daher kann [!DNL Target] basierend auf einer Mindestanzahl von Konversionen einen Gewinner anzeigen, der früher als angezeigt wurde. Weitere Informationen finden Sie unter [Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Informationen zur Steigerung und Konfidenz in [!UICONTROL Auto-Allocate] -Aktivitäten {#lift-confidence}

In [!UICONTROL Auto-Allocate] -Aktivitäten wird das erste Erlebnis (standardmäßig Erlebnis A genannt) immer als Kontrollerlebnis auf der Registerkarte [!UICONTROL Reports] definiert. Dieses Erlebnis wird bei der Modellierung, die zur Ermittlung der Erlebnisleistung verwendet wird, nicht als echte statistische Kontrolle behandelt, sondern als Referenz oder Grundlage für einige Zahlen im Bericht behandelt.

Der numerische Wert &quot;Steigerung&quot;und die 95-%-Grenzen für jedes Erlebnis werden immer mit Bezug auf das definierte Kontrollerlebnis berechnet. Das definierte Kontrollerlebnis kann keine Steigerung im Verhältnis zu sich selbst aufweisen. Daher wird für dieses Erlebnis ein leerer &quot;—&quot;-Wert gemeldet. Im Gegensatz zu A/B-Tests wird bei [!UICONTROL Auto-Allocate]-Tests kein negativer Steigerungswert gemeldet, wenn ein Erlebnis schlechter abschneidet als die definierte Kontrolle. Stattdessen wird &quot;—&quot;angezeigt.

Die angezeigten [!UICONTROL Confidence Interval] -Balken stellen das Konfidenzintervall von 95 % um die mittlere Schätzung der Konversionsrate eines Erlebnisses dar. Diese Balken sind auch in Bezug auf das definierte Kontrollerlebnis farbcodiert. Die Leiste des Kontrollerlebnisses ist immer grau gefärbt. Die Abschnitte der Konfidenzintervalle unterhalb des Konfidenzintervalls des Kontrollerlebnisses sind rot und die Abschnitte der Konfidenzintervalle über dem Kontrollerlebnis sind grün.

Ein Gewinner wird gefunden, wenn sich die 95 % [!UICONTROL Confidence Interval] des führenden Erlebnisses nicht mit anderen Erlebnissen überschneiden. Das erfolgreichste Erlebnis wird mit einem grünen Sternzeichen links neben dem Erlebnisnamen und im Banner &quot;Gewinner&quot;gekennzeichnet. Wenn kein Stern sichtbar ist, lautet das Banner &quot;Noch kein Gewinner&quot;und ein Gewinner wurde noch nicht gefunden.

Neben dem derzeit führenden oder erfolgreichsten Erlebnis wird auch eine &quot;Konfidenz&quot;gemeldet. Diese Zahl wird nur gemeldet, bis die [!UICONTROL Confidence] des führenden Erlebnisses mindestens 60 % erreicht hat. Wenn in der [!UICONTROL Auto-Allocate] -Aktivität zwei Erlebnisse vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, dass das Erlebnis eine bessere Leistung erzielt als das andere Erlebnis. Wenn mehr als zwei Erlebnisse in der [!UICONTROL Auto-Allocate] -Aktivität vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, dass das Erlebnis eine bessere Leistung erzielt als das definierte &quot;Kontrollerlebnis&quot;. Wenn das Kontrollerlebnis gewinnt, wird keine &quot;Konfidenz&quot;-Zahl gemeldet.

## Häufig gestellte Fragen   {#section_C8E068512A93458D8C006760B1C0B6A2}

Beachten Sie die folgenden Antworten auf häufig gestellte Fragen:

### Die Aktivität ist seit einigen Tagen aktiv. Warum werden bei allen Konfidenzwerten immer noch 0 % angezeigt?

Die folgenden Gründe beschreiben, warum 0 % für alle Aktivitäten in der Spalte [!UICONTROL Confidence] des Berichts angezeigt wird:

* Manuelle A/B-Tests und [!UICONTROL Auto-Allocate] verwenden unterschiedliche Statistiken, um [!UICONTROL Confidence] -Werte anzuzeigen.

  Manuelle A/B-Tests verwenden P-Werte, die auf dem t-Test von [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test) basieren. Ein P-Wert gibt die Wahrscheinlichkeit an, den beobachteten (oder einen extremeren) Unterschied zwischen einem Erlebnis und dem Kontrollelement zu erhalten, wobei in Wirklichkeit kein solcher Unterschied vorliegt. Diese P-Werte können nur verwendet werden, um festzustellen, ob die beobachteten Daten mit einem bestimmten Erlebnis im Einklang stehen und das Kontrollelement identisch ist. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

  [!UICONTROL Auto-Allocate] zeigt die Wahrscheinlichkeit, mit der ein bestimmtes Erlebnis für alle Erlebnisse in der Aktivität als wahr Sieger gilt. Nur ein erfolgreichstes Erlebnis (das höchstwahrscheinlich der Gewinner ist) hat einen Konfidenzwert ungleich null. Bei allen anderen handelt es sich höchstwahrscheinlich um Verlierer und um 0 %.

* [!UICONTROL Auto-Allocate] beginnt, die Konfidenz erst anzuzeigen, nachdem das erfolgreichste Erlebnis 60 % Konfidenz gesammelt hat. Diese Konfidenzwerte treten in der Regel in etwa der Hälfte der Zeit auf, die ein normaler A/B-Test dauern würde (obwohl dieser Zeitraum nicht garantiert ist). Um zu bestimmen, wie lange ein normaler A/B-Test dauern würde, verwenden Sie den [!DNL Adobe Target] [Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): Plug-in-Konversionsrate der Kontrolle in &quot;Baseline-Konversionsrate&quot;, &quot;5%&quot;für &quot;Steigerung&quot;und 95% für &quot;Konfidenz&quot;. Typischerweise wird die Konfidenz angezeigt, nachdem jedes Erlebnis mindestens 50 % der erforderlichen Stichproben pro Erlebnis sammeln konnte. So erhalten Sie eine Vorstellung davon, wann die Konfidenz erscheint.

* Wird im Bericht überall der Wert 0 % angezeigt, ist die Aktivität höchstwahrscheinlich noch nicht lange genug online.

### Sind die Abzeichen &quot;Kein Gewinner&quot;, &quot;Gewinner&quot;und &quot;Stern&quot;für [!UICONTROL Auto-Allocate] Aktivitäten verfügbar, die [!UICONTROL Analytics as the reporting source] (A4T) verwenden?

Die Abzeichen &quot;Noch kein Gewinner&quot;und &quot;Gewinner&quot;sind derzeit nicht im Bedienfeld [!UICONTROL A4T] in [!DNL Analysis Workspace] verfügbar. Diese Abzeichen sind auch nicht verfügbar, wenn derselbe Bericht in [!DNL Target] angezeigt wird. Ein Zeichen für den Gewinner &quot;star&quot;, das in einem [!DNL Target] -Bericht für eine [!UICONTROL Auto-Allocate] -Aktivität mit A4T angezeigt wird, sollte ignoriert werden.

Weitere Informationen zu diesen und anderen Einschränkungen und Notizen finden Sie unter [Automatische Zuordnung](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *A4T-Unterstützung für [!UICONTROL Auto-Allocate] - und [!UICONTROL Auto-Target] -Aktivitäten*.