---
keywords: Automatisierte Traffic-Zuordnung;Zielgruppenbestimmung;Gewinner;statistische Garantie;Konfidenz;Gewinner bestimmen;Steigerung;Konfidenz;Standard;Standarderlebnis;Automatische Zuordnung;Automatische Zuordnung
description: Erfahren Sie, wie Sie [!UICONTROL Auto-Allocate] Ergebnisse der A/B-Aktivität interpretieren und sich dabei auf Schlüsselindikatoren wie Steigerung und Konfidenz konzentrieren.
title: Wie interpretiere ich [!UICONTROL Auto-Allocate] Berichte?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 20%

---

# Interpretieren [!UICONTROL Auto-Allocate] Berichte

Interpretieren Sie die Ergebnisse einer [!UICONTROL Auto-Allocate] A/B-Aktivität in [!UICONTROL Adobe Target], indem Sie wichtige Indikatoren wie Steigerung und Konfidenz untersuchen.

Viele Marketingexperten machen den Fehler, ein Erlebnis vorzeitig zum Gewinner zu erklären, bevor endgültige Ergebnisse vorliegen. [!DNL Target] erleichtert Ihnen die Ermittlung des Gewinners.

Allgemeine Informationen zur Gewinnererklärung finden Sie unter [10 häufige Fehler bei A/B-Tests und wie diese vermieden werden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Ermitteln des erfolgreichsten Erlebnisses {#section_24007470CF5B4D30A06610CE8DD23CE3}

Bei Verwendung der [!UICONTROL Auto-Allocate]-Funktion zeigt [!DNL Target] oben auf der Seite der Aktivität ein Badge mit der Bezeichnung „Noch kein Gewinner“ an, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Konfidenz erreicht.

![Zeichen „Kein Gewinner“](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

Wenn ein eindeutiger Gewinner bekannt gegeben wird, zeigt [!DNL Target] das Abzeichen „Gewinner: Erlebnis *X*&quot; an.

![Gewinner-Abzeichen](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

>[!NOTE]
>
>[!UICONTROL Auto-Allocate] Aktivitäten sind so konzipiert, dass sie das beste Erlebnis unter allen Optionen finden und nicht nur paarweise Vergleiche mit Kontrolle durchführen.

## Statistische [!UICONTROL Auto-Allocate] {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Am Ende einer A/B-Aktivität garantiert [!UICONTROL Auto-Allocate], dass der ermittelte Gewinner eine effektive falsch-positive Rate von 5 % hat. Das bedeutet, dass der festgestellte Gewinner nur 5 % der Zeit nicht das beste Erlebnis aller in der Aktivität vorhandenen Erlebnisse ist. Bei einem [A/A-Test](/help/main/c-activities/t-test-ab/aa-testing.md) (mit identischen Erfahrungen) schließt [!DNL Target] einen Test in weniger als 5 % der Fälle ab. Zu erwarten ist, dass der A/A-Test (mit identischen Erlebnissen) unbegrenzt lange läuft, ohne dass ein Siegerabzeichen angezeigt wird.

[!DNL Target] verwendet keine auf dem p-Wert basierende Konfidenz für [!UICONTROL Auto-Allocate].

In der Spalte [!UICONTROL Confidence] in einer [!UICONTROL Auto-Allocate] Aktivität wird die Wahrscheinlichkeit, dass ein Erlebnis der Gewinner ist, innerhalb einer Fehlerspanne von 1 % angezeigt. Der Algorithmus verwendet einen minimalen detektierbaren Effekt von 1 % zwischen der besten und der zweitbesten Konversionsrate. Der Algorithmus verwendet [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) um diese Wahrscheinlichkeit zu berechnen.

Bei normalen A/B-Tests wird die Konfidenz basierend auf P-Werten berechnet. [!UICONTROL Auto-Allocate] verwendet keine p-Werte. Mit P-Werten wird „grob“ die Wahrscheinlichkeit berechnet, mit der ein bestimmtes Erlebnis vom Kontrollelement abweicht. Diese P-Werte können dazu genutzt werden, um zu bestimmen, ob sich ein Erlebnis vom Kontrollelement unterscheidet. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

>[!IMPORTANT]
>
>[!DNL Target] zeigt einen Gewinner nach einer vordefinierten Mindestanzahl von Konversionen an. Die endgültige Entscheidung zur Auswahl des Gewinners sollte jedoch immer auf den Ergebnissen des [!DNL Adobe Target] Stichprobengrößenrechners basieren. [!DNL Target] berücksichtigt nicht die grundlegenden Konversionsraten einer Site und andere wichtige Aspekte, die in den Rechner einfließen, um die Dauer der Aktivität zu bestimmen. Daher kann es sein, dass [!DNL Target] einen Gewinner basierend auf einer Mindestanzahl von Konversionen früher als garantiert anzeigen. Weitere Informationen finden Sie unter [Rechner für den Stichprobenumfang](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Grundlegendes zum Reporting über Steigerung und Konfidenz bei [!UICONTROL Auto-Allocate] Aktivitäten {#lift-confidence}

In [!UICONTROL Auto-Allocate] Aktivitäten wird das erste Erlebnis (standardmäßig Erlebnis A genannt) immer als „Kontrollerlebnis“ auf der Registerkarte [!UICONTROL Reports] definiert. Dieses Erlebnis wird in der Modellierung, die zur Bestimmung der Leistung von Erlebnissen verwendet wird, nicht als echte statistische Kontrolle behandelt, sondern als Referenz oder Grundlinie für einige Zahlen im Bericht.

Der numerische Wert „Anstieg“ und die 95-%-Grenzen für jedes Erlebnis werden immer unter Bezugnahme auf das definierte Kontrollerlebnis berechnet. Das definierte Erlebnis „Kontrolle“ kann keinen Anstieg relativ zu sich selbst haben, sodass für dieses Erlebnis ein leerer Wert &quot;—&quot; gemeldet wird. Im Gegensatz zu A/B-Tests wird bei [!UICONTROL Auto-Allocate], wenn ein Erlebnis eine schlechtere Leistung als die definierte Kontrolle aufweist, kein negativer Steigerungswert gemeldet. Stattdessen wird &quot;—&quot; angezeigt.

Die angezeigten [!UICONTROL Confidence Interval] stellen das 95-%-Konfidenzintervall um die mittlere Schätzung der Konversionsrate eines Erlebnisses dar. Diese Balken sind auch im Hinblick auf das definierte „Kontrollerlebnis“ farbcodiert. Die Leiste des Erlebnisses „Kontrolle“ ist immer grau gefärbt. Die Teile der Konfidenzintervalle unterhalb des Konfidenzintervalls des Kontrollerlebnisses sind rot und die Teile der Konfidenzintervalle oberhalb des Kontrollerlebnisses grün gefärbt.

Ein Gewinner wird gefunden, wenn sich die 95%ige [!UICONTROL Confidence Interval] des führenden Erlebnisses mit keinen anderen Erlebnissen überschneidet. Das erfolgreichste Erlebnis wird mit einem grünen Sternabzeichen links neben dem Erlebnisnamen und im Banner „Gewinner“ gekennzeichnet. Wenn kein Stern sichtbar ist, lautet das Banner „Noch kein Gewinner“ und es wurde noch kein Gewinner gefunden.

Neben dem derzeit führenden oder erfolgreichsten Erlebnis wird auch eine Zahl für „Konfidenz“ angezeigt. Diese Zahl wird nur gemeldet, bis die [!UICONTROL Confidence] des führenden Erlebnisses mindestens 60 % erreicht. Wenn in der [!UICONTROL Auto-Allocate] Aktivität zwei Erlebnisse vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, bei dem das Erlebnis eine bessere Leistung zeigt als das andere Erlebnis. Wenn mehr als zwei Erlebnisse in der [!UICONTROL Auto-Allocate] vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, bei dem die Leistung des Erlebnisses besser ist als bei dem definierten Kontrollerlebnis. Wenn das Kontrollerlebnis gewinnt, wird keine „Konfidenzzahl“ gemeldet.

## Häufig gestellte Fragen   {#section_C8E068512A93458D8C006760B1C0B6A2}

Beachten Sie die folgenden Antworten auf häufig gestellte Fragen:

### Es waren ein paar Tage bis zur Aktivität. Warum zeigen alle Konfidenzwerte weiterhin 0 % an?

Einer der folgenden Gründe beschreibt, warum 0 % für alle Aktivitäten in der [!UICONTROL Confidence] des Berichts angezeigt wird:

* Manuelle A/B-Tests und [!UICONTROL Auto-Allocate] verwenden verschiedene Statistiken zur Anzeige von [!UICONTROL Confidence].

  Manuelle A/B-Tests verwenden p-Werte, die auf dem [Welch-t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test) basieren. Ein P-Wert gibt die Wahrscheinlichkeit an, den beobachteten (oder einen extremeren) Unterschied zwischen einem Erlebnis und dem Kontrollelement zu erhalten, wobei in Wirklichkeit kein solcher Unterschied vorliegt. Diese P-Werte können nur verwendet werden, um festzustellen, ob die beobachteten Daten mit einem bestimmten Erlebnis im Einklang stehen und das Kontrollelement identisch ist. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

  [!UICONTROL Auto-Allocate] zeigt die Wahrscheinlichkeit, dass ein bestimmtes Erlebnis für alle Erlebnisse in der Aktivität ein echter Gewinner ist. Nur ein erfolgreichstes Erlebnis (bei dem es sich höchstwahrscheinlich um den Gewinner handelt) hat einen Vertrauenswert ungleich null. Bei allen anderen handelt es sich höchstwahrscheinlich um Verlierer, die 0 % anzeigen.

* [!UICONTROL Auto-Allocate] zeigt erst dann Konfidenz, wenn das erfolgreichste Erlebnis 60 % Konfidenz erlangt hat. Diese Konfidenzniveaus treten in der Regel in etwa der Hälfte der Zeit auf, die ein normaler A/B-Test benötigen würde (obwohl dieser Zeitrahmen nicht garantiert ist). Um zu bestimmen, wie lange ein normaler A/B-Test ausgeführt werden würde, verwenden Sie den [!DNL Adobe Target] [Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): Stecken Sie die Konversionsrate des Steuerelements in „Baseline-Konversionsrate“, „5 %&quot; für „Steigerung“ und 95 % für „Konfidenz“. Typischerweise wird die Konfidenz angezeigt, nachdem jedes Erlebnis mindestens 50 % der erforderlichen Stichproben pro Erlebnis sammeln konnte. Dies gibt Ihnen eine Vorstellung davon, wann Konfidenz anfängt zu erscheinen.

* Wird im Bericht überall der Wert 0 % angezeigt, ist die Aktivität höchstwahrscheinlich noch nicht lange genug online.

### Sind die Abzeichen „Kein Gewinner“, „Gewinner“ und „Stern“ verfügbar für [!UICONTROL Auto-Allocate] Aktivitäten, die [!UICONTROL Analytics as the reporting source] (A4T) verwenden?

Die Abzeichen „Noch kein Gewinner“ und „Gewinner“ sind derzeit nicht im [!UICONTROL A4T] in [!DNL Analysis Workspace] verfügbar. Diese Abzeichen sind auch dann nicht verfügbar, wenn derselbe Bericht in [!DNL Target] angezeigt wird. Ein Gewinner-Abzeichen „Stern“, das in einem [!DNL Target] für eine [!UICONTROL Auto-Allocate]-Aktivität mit A4T angezeigt wird, sollte ignoriert werden.

Weitere Informationen zu dieser und anderen Einschränkungen finden Sie unter [Automatische Zuordnung](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *A4T-Unterstützung für [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten*.
