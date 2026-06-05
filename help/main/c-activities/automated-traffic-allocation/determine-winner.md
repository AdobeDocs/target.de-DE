---
keywords: Automatisierte Traffic-Zuordnung;Zielgruppenbestimmung;Gewinner;statistische Garantie;Konfidenz;Gewinner bestimmen;Steigerung;Konfidenz;Standard;Standarderlebnis;Automatische Zuordnung;Automatische Zuordnung
description: Erfahren Sie, wie die Ergebnisse [!UICONTROL  A/B]Aktivitäten mit automatisierter Zuordnung interpretiert werden, wobei der Schwerpunkt auf Schlüsselindikatoren wie Steigerung und Konfidenz liegt.
title: Wie interpretiere ich [!UICONTROL automatische Zuordnung] Berichte?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
TQID: https://experienceleague.adobe.com/o4mFGMk-M5QUvJ57kYnfjMPvVZL8l6YegJQSJyHjAxc
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1253
ht-degree: 20%

---

# Interpretieren [!UICONTROL automatischen Zuordnungs]Berichten

Interpretieren Sie die Ergebnisse einer A/B[!UICONTROL Aktivität vom Typ „Automatische Zuordnung] in [!UICONTROL Adobe Target] anhand wichtiger Indikatoren, einschließlich Steigerung und Konfidenz.

Viele Marketingexperten machen den Fehler, ein Erlebnis vorzeitig zum Gewinner zu erklären, bevor endgültige Ergebnisse vorliegen. [!DNL Target] erleichtert Ihnen die Ermittlung des Gewinners.

Allgemeine Informationen zur Gewinnererklärung finden Sie unter [10 häufige Fehler bei A/B-Tests und wie diese vermieden werden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Ermitteln des erfolgreichsten Erlebnisses {#section_24007470CF5B4D30A06610CE8DD23CE3}

Bei Verwendung der Funktion [!UICONTROL Automatische Zuordnung] zeigt [!DNL Target] oben auf der Seite der Aktivität ein Badge mit der Bezeichnung „Noch kein Gewinner“ an, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Konfidenz erreicht.

![Zeichen „Kein Gewinner“](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

Wenn ein eindeutiger Gewinner bekannt gegeben wird, zeigt [!DNL Target] das Abzeichen „Gewinner: Erlebnis *X*&quot; an.

![Gewinner-Abzeichen](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

>[!NOTE]
>
>[!UICONTROL Automatische Zuordnung]-Aktivitäten sind so konzipiert, dass das beste Erlebnis unter allen Optionen gefunden wird und nicht nur paarweise Vergleiche mit dem Kontrollerlebnis durchgeführt werden.

## Statistische Garantien für [!UICONTROL Automatische Zuordnung] {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Am Ende einer A/B-Aktivität garantiert [!UICONTROL Automatische Zuordnung], dass der ermittelte Gewinner eine effektive falsch-positive Rate von 5 % hat. Das bedeutet, dass der festgestellte Gewinner nur 5 % der Zeit nicht das beste Erlebnis aller in der Aktivität vorhandenen Erlebnisse ist. Bei einem [A/A-Test](/help/main/c-activities/t-test-ab/aa-testing.md) (mit identischen Erfahrungen) schließt [!DNL Target] einen Test in weniger als 5 % der Fälle ab. Zu erwarten ist, dass der A/A-Test (mit identischen Erlebnissen) unbegrenzt lange läuft, ohne dass ein Siegerabzeichen angezeigt wird.

[!DNL Target] verwendet keine auf dem p-Wert basierende Konfidenz für [!UICONTROL Automatische Zuordnung].

Die Spalte [!UICONTROL Konfidenz] in einer Aktivität [!UICONTROL Automatische Zuordnung] zeigt die Wahrscheinlichkeit, dass ein Erlebnis der Gewinner ist, innerhalb einer Fehlerspanne von 1 % an. Der Algorithmus verwendet einen minimalen detektierbaren Effekt von 1 % zwischen der besten und der zweitbesten Konversionsrate. Der Algorithmus verwendet [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) um diese Wahrscheinlichkeit zu berechnen.

Bei normalen A/B-Tests wird die Konfidenz basierend auf P-Werten berechnet. [!UICONTROL Automatische Zuordnung] verwendet keine p-Werte. Mit P-Werten wird „grob“ die Wahrscheinlichkeit berechnet, mit der ein bestimmtes Erlebnis vom Kontrollelement abweicht. Diese P-Werte können dazu genutzt werden, um zu bestimmen, ob sich ein Erlebnis vom Kontrollelement unterscheidet. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

>[!IMPORTANT]
>
>[!DNL Target] zeigt einen Gewinner nach einer vordefinierten Mindestanzahl von Konversionen an. Die endgültige Entscheidung zur Auswahl des Gewinners sollte jedoch immer auf den Ergebnissen des [!DNL Adobe Target] Stichprobengrößenrechners basieren. [!DNL Target] berücksichtigt nicht die grundlegenden Konversionsraten einer Site und andere wichtige Aspekte, die in den Rechner einfließen, um die Dauer der Aktivität zu bestimmen. Daher kann es sein, dass [!DNL Target] einen Gewinner basierend auf einer Mindestanzahl von Konversionen früher als garantiert anzeigen. Weitere Informationen finden Sie unter [Rechner für den Stichprobenumfang](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Verstehen der Berichterstellung zu Steigerung und Konfidenz in [!UICONTROL automatischen Zuordnungs]-Aktivitäten {#lift-confidence}

In [!UICONTROL automatischen Zuordnungs]-Aktivitäten wird das erste Erlebnis (standardmäßig Erlebnis A genannt) immer als Kontrollerlebnis auf der Registerkarte [!UICONTROL Berichte] definiert. Dieses Erlebnis wird in der Modellierung, die zur Bestimmung der Leistung von Erlebnissen verwendet wird, nicht als echte statistische Kontrolle behandelt, sondern als Referenz oder Grundlinie für einige Zahlen im Bericht.

Der numerische Wert „Anstieg“ und die 95-%-Grenzen für jedes Erlebnis werden immer unter Bezugnahme auf das definierte Kontrollerlebnis berechnet. Das definierte Erlebnis „Kontrolle“ kann keinen Anstieg relativ zu sich selbst haben, sodass für dieses Erlebnis ein leerer Wert &quot;—&quot; gemeldet wird. Im Gegensatz zu A/B-Tests wird bei [!UICONTROL automatischen Zuordnungstests] wenn ein Erlebnis eine schlechtere Leistung als die definierte Kontrolle aufweist, kein negativer Steigerungswert gemeldet. Stattdessen wird &quot;—&quot; angezeigt.

Die angezeigten [!UICONTROL Konfidenzintervall]-Balken stellen das 95-%-Konfidenzintervall um die mittlere Schätzung der Konversionsrate eines Erlebnisses dar. Diese Balken sind auch im Hinblick auf das definierte „Kontrollerlebnis“ farbcodiert. Die Leiste des Erlebnisses „Kontrolle“ ist immer grau gefärbt. Die Teile der Konfidenzintervalle unterhalb des Konfidenzintervalls des Kontrollerlebnisses sind rot und die Teile der Konfidenzintervalle oberhalb des Kontrollerlebnisses grün gefärbt.

Ein Gewinner wird gefunden, wenn das 95%ige [!UICONTROL Konfidenzintervall“ des führenden Erlebnisses ] andere Erlebnisse überschneidet. Das erfolgreichste Erlebnis wird mit einem grünen Sternabzeichen links neben dem Erlebnisnamen und im Banner „Gewinner“ gekennzeichnet. Wenn kein Stern sichtbar ist, lautet das Banner „Noch kein Gewinner“ und es wurde noch kein Gewinner gefunden.

Neben dem derzeit führenden oder erfolgreichsten Erlebnis wird auch eine Zahl für „Konfidenz“ angezeigt. Diese Zahl wird nur gemeldet, bis die „Konfidenz[!UICONTROL  des führenden Erlebnisses ] mindestens 60 % erreicht. Wenn in der Aktivität [!UICONTROL Automatische Zuordnung] zwei Erlebnisse vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, bei dem die Leistung des Erlebnisses besser ist als bei dem anderen Erlebnis. Wenn in der Aktivität [!UICONTROL Automatische Zuordnung] mehr als zwei Erlebnisse vorhanden sind, stellt diese Zahl das Konfidenzniveau dar, bei dem die Leistung des Erlebnisses besser ist als bei dem definierten Kontrollerlebnis. Wenn das Kontrollerlebnis gewinnt, wird keine „Konfidenzzahl“ gemeldet.

## Häufig gestellte Fragen {#section_C8E068512A93458D8C006760B1C0B6A2}

Beachten Sie die folgenden Antworten auf häufig gestellte Fragen:

### Es waren ein paar Tage bis zur Aktivität. Warum zeigen alle Konfidenzwerte weiterhin 0 % an?

Die folgenden Gründe erläutern, warum für sämtliche Aktivitäten in der Spalte [!UICONTROL Konfidenz] des Berichts der Wert 0 % angezeigt wird:

* Manuelle A/B-Tests und [!UICONTROL Automatische Zuordnung] verwenden verschiedene Statistiken zur Anzeige [!UICONTROL Konfidenz]-Werte.

  Manuelle A/B-Tests verwenden p-Werte, die auf dem [Welch-t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test) basieren. Ein P-Wert gibt die Wahrscheinlichkeit an, den beobachteten (oder einen extremeren) Unterschied zwischen einem Erlebnis und dem Kontrollelement zu erhalten, wobei in Wirklichkeit kein solcher Unterschied vorliegt. Diese P-Werte können nur verwendet werden, um festzustellen, ob die beobachteten Daten mit einem bestimmten Erlebnis im Einklang stehen und das Kontrollelement identisch ist. Die Werte können nicht genutzt werden, um festzustellen, ob ein Erlebnis sich von einem anderen Erlebnis unterscheidet, das nicht das Kontrollerlebnis ist.

  [!UICONTROL Automatische Zuordnung] zeigt die Wahrscheinlichkeit an, dass ein bestimmtes Erlebnis über alle Erlebnisse in der Aktivität hinweg ein echter Gewinner ist. Nur ein erfolgreichstes Erlebnis (bei dem es sich höchstwahrscheinlich um den Gewinner handelt) hat einen Vertrauenswert ungleich null. Bei allen anderen handelt es sich höchstwahrscheinlich um Verlierer, die 0 % anzeigen.

* [!UICONTROL Automatische Zuordnung] zeigt erst dann Konfidenz an, wenn das erfolgreichste Erlebnis 60 % Konfidenz erlangt hat. Diese Konfidenzniveaus treten in der Regel in etwa der Hälfte der Zeit auf, die ein normaler A/B-Test benötigen würde (obwohl dieser Zeitrahmen nicht garantiert ist). Um zu bestimmen, wie lange ein normaler A/B-Test ausgeführt werden würde, verwenden Sie den [!DNL Adobe Target] [Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): Stecken Sie die Konversionsrate des Steuerelements in „Baseline-Konversionsrate“, „5 %&quot; für „Steigerung“ und 95 % für „Konfidenz“. Typischerweise wird die Konfidenz angezeigt, nachdem jedes Erlebnis mindestens 50 % der erforderlichen Stichproben pro Erlebnis sammeln konnte. Dies gibt Ihnen eine Vorstellung davon, wann Konfidenz anfängt zu erscheinen.

* Wird im Bericht überall der Wert 0 % angezeigt, ist die Aktivität höchstwahrscheinlich noch nicht lange genug online.

### Sind die Abzeichen „Kein Gewinner“, „Gewinner“ und „Stern“ verfügbar für Aktivitäten [!UICONTROL Automatische Zuordnung], die [!UICONTROL Analytics als Berichtsquelle] (A4T) verwenden?

Die Abzeichen „Noch kein Gewinner“ und „Gewinner“ sind derzeit nicht im Bedienfeld [!UICONTROL A4T] in [!DNL Analysis Workspace] verfügbar. Diese Abzeichen sind auch dann nicht verfügbar, wenn derselbe Bericht in [!DNL Target] angezeigt wird. Ein Gewinner-Abzeichen „Stern“, das in einem [!DNL Target] Bericht für eine Aktivität [!UICONTROL Automatische Zuordnung] mit A4T angezeigt wird, sollte ignoriert werden.

Weitere Informationen zu dieser und anderen Einschränkungen finden Sie unter [Automatische Zuordnung](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *A4T-Unterstützung für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]-Aktivitäten*.
