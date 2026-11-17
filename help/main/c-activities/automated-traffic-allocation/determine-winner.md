---
keywords: Automatisierte Traffic-Zuordnung;Zielgruppenbestimmung;Gewinner;statistische Garantie;Konfidenz;Gewinner bestimmen;Steigerung;Konfidenz;Standard;Standarderlebnis;Automatische Zuordnung;Automatische Zuordnung
description: Erfahren Sie, wie die Ergebnisse [!UICONTROL  A/B]Aktivitäten mit automatisierter Zuordnung interpretiert werden, wobei der Schwerpunkt auf Schlüsselindikatoren wie Steigerung und Konfidenz liegt.
title: Wie interpretiere ich [!UICONTROL automatische Zuordnung] Berichte?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
TQID: 'https://experienceleague.adobe.com/o4mFGMk-M5QUvJ57kYnfjMPvVZL8l6YegJQSJyHjAxc'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f2d0aafb-18af-41a0-a32e-2788eafacc2b
    internal-label: Auto-allocate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 174d4631b6f4a481c039bd7fff52a8e70161e19e
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 3%
---
# Interpretieren [!UICONTROL automatischen Zuordnungs]Berichten {#interpret-auto-allocate-reports}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie das erfolgreichste Erlebnis einer **[!UICONTROL automatischen Zuordnungsaktivität]** ermitteln, das durch die statistische **[!UICONTROL automatische Zuordnung]** gewährleistet wird, und wie Sie die Zahlen zu Steigerung und Konfidenz im Bericht lesen.

>[!ENDSHADEBOX]

Der Bericht einer A/B **[!UICONTROL Aktivität vom Typ „Automatische Zuordnung]** in [!DNL Adobe Target] zeigt, ob die Aktivität einen Gewinner gefunden hat und wie sicher [!DNL Target] in dieses Ergebnis ist. Indikatoren wie das Siegerabzeichen, die Steigerung und die Konfidenz helfen Ihnen bei der Interpretation der Ergebnisse.

Viele Marketing-Fachleute begehen den Fehler, ein Erlebnis vorzeitig zum erfolgreichsten zu erklären, bevor die Ergebnisse einen klaren Gewinner angeben. [!DNL Target] erleichtert Ihnen die Ermittlung des Gewinners. Allgemeine Informationen zur Gewinnererklärung finden Sie unter [10 häufige Fehler bei A/B-Tests und wie diese vermieden werden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Ermitteln des erfolgreichsten Erlebnisses {#identify-winner}

Wenn Sie die Funktion **[!UICONTROL Automatische Zuordnung]** verwenden, zeigt [!DNL Target] oben auf der Aktivitätsseite ein Badge an. Das Abzeichen bedeutet „Noch kein Gewinner“, bis die Aktivität die Mindestanzahl an Konversionen mit ausreichender Sicherheit erreicht.

![Zeichen „Kein Gewinner“](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

Wenn ein eindeutiger Gewinner bekannt gegeben wird, zeigt [!DNL Target] das Abzeichen „Gewinner: Erlebnis *X*&quot; an.

![Gewinner-Abzeichen](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

Das Siegerabzeichen wird auch im Informations-Popup einer Aktivität in der Liste **[!UICONTROL Aktivitäten]** angezeigt, sodass Sie den Status einer **[!UICONTROL automatischen Zuordnung]**-Aktivität sehen können, ohne sie zu öffnen.

>[!NOTE]
>
>**[!UICONTROL Automatische Zuordnung]**-Aktivitäten sind so konzipiert, dass unter allen Optionen das beste Erlebnis ermittelt wird, nicht nur, um paarweise Vergleiche mit dem Steuerelement anzustellen.

## Statistische Garantien für [!UICONTROL Automatische Zuordnung] {#statistical-guarantees}

Am Ende einer A/B-Aktivität garantiert **[!UICONTROL Automatische Zuordnung]**, dass der ermittelte Gewinner eine effektive falsch-positive Rate von 5 % hat. Das bedeutet, dass der festgestellte Gewinner nur 5 % der Zeit nicht das beste Erlebnis aller in der Aktivität vorhandenen Erlebnisse ist.

Bei einem [A/A-Test](/help/main/c-activities/t-test-ab/aa-testing.md) (mit identischen Erfahrungen) schließt [!DNL Target] einen Test in weniger als 5 % der Fälle ab. Das erwartete Verhalten für einen A/A-Test ist die unbegrenzte Ausführung, sodass das Siegerabzeichen nie angezeigt werden sollte.

### Konfidenz und p-Werte {#confidence-p-values}

[!DNL Target] verwendet keine auf dem p-Wert basierende Konfidenz für **[!UICONTROL Automatische Zuordnung]**. Die Spalte **[!UICONTROL Konfidenz]** in einer Aktivität **[!UICONTROL Automatische Zuordnung]** zeigt innerhalb einer Fehlerspanne von 1 % die Wahrscheinlichkeit an, dass ein Erlebnis der Gewinner ist. Der Algorithmus verwendet einen minimalen detektierbaren Effekt von 1 % zwischen der besten und der zweitbesten Konversionsrate und verwendet die [Bernstein-Ungleichung](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) um diese Wahrscheinlichkeit zu berechnen.

Normale A/B-Tests berechnen Konfidenz auf der Basis von p-Werten, die die Wahrscheinlichkeit, dass ein bestimmtes Erlebnis von der Kontrolle abweicht, „lose“ berechnen. Diese P-Werte können dazu genutzt werden, um zu bestimmen, ob sich ein Erlebnis vom Kontrollelement unterscheidet. Sie können nicht verwendet werden, um zu bestimmen, ob sich ein Erlebnis von einem anderen Erlebnis (nicht dem Kontrollerlebnis) unterscheidet.

>[!IMPORTANT]
>
>[!DNL Target] zeigt einen Gewinner nach einer vordefinierten Mindestanzahl von Konversionen an. Die endgültige Entscheidung über die Auswahl des Gewinners sollte jedoch immer auf den Ergebnissen des [!DNL Adobe Target] Stichprobengrößenrechners basieren. [!DNL Target] berücksichtigt nicht die grundlegenden Konversionsraten einer Site und andere wichtige Aspekte, die in den Rechner einfließen, um die Dauer der Aktivität zu bestimmen. Daher kann es sein, dass [!DNL Target] einen Gewinner basierend auf einer Mindestanzahl von Konversionen früher als garantiert anzeigen. Weitere Informationen finden Sie unter [Rechner für den Stichprobenumfang](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Berichte zu Steigerung und Konfidenz verstehen {#lift-confidence}

Die **[!UICONTROL Berichte]** einer Aktivität **[!UICONTROL Automatische Zuordnung]** zeigt die folgenden Abbildungen an:

| Abbildung | Beschreibung |
|---|---|
| **Kontrollerlebnis** | Das erste Erlebnis (standardmäßig Erlebnis A genannt) wird immer als Kontrollerlebnis auf der Registerkarte **[!UICONTROL Berichte]** definiert. Dieses Erlebnis wird in der Modellierung, die zur Bestimmung der Leistung von Erlebnissen verwendet wird, nicht als echte statistische Kontrolle behandelt, sondern als Referenz oder Grundlinie für einige Zahlen im Bericht. |
| **Steigerung** | Der Wert für „Anstieg“ und die 95-%-Grenzen jedes Erlebnisses werden immer unter Bezugnahme auf das definierte Kontrollerlebnis berechnet. Das Kontrollerlebnis kann relativ zu sich selbst keinen Anstieg aufweisen, weshalb der Bericht für dieses Erlebnis einen leeren Wert &quot;—&quot; anzeigt.<br>Im Gegensatz zu A/B-Tests wird in Tests **[!UICONTROL Automatische Zuordnung]** kein negativer Steigerungswert gemeldet, wenn ein Erlebnis schlechter funktioniert als die definierte Kontrolle. Stattdessen wird &quot;—&quot; angezeigt. |
| **Konfidenzintervalle** | Die angezeigten **[!UICONTROL Konfidenzintervall]**-Balken stellen das 95-%-Konfidenzintervall um den geschätzten Durchschnittswert der Konversionsrate eines Erlebnisses dar. Die Balken sind im Hinblick auf das definierte „Kontrollerlebnis“ farbcodiert:<ul><li>Der Balken für das Erlebnis „Kontrolle“ ist immer grau.</li><li>Die Teile der Konfidenzintervalle, die unterhalb des Konfidenzintervalls für das Kontrollerlebnis liegen, sind rot.</li><li>Die Teile der Konfidenzintervalle, die oberhalb des Konfidenzintervalls für das Kontrollerlebnis liegen, sind grün.</li></ul> |
| **Gewinner** | Ein Gewinner wird gefunden, wenn sich das **[!UICONTROL Konfidenzintervall)]** führenden Erlebnisses zu 95 % mit keinem anderen Erlebnis überschneidet. Das erfolgreichste Erlebnis wird mit einem grünen Sternabzeichen links neben dem Erlebnisnamen und im Banner „Gewinner“ gekennzeichnet. Wenn kein Stern sichtbar ist, lautet das Banner „Noch kein Gewinner“ und es wurde noch kein Gewinner gefunden. |
| **Konfidenzzahl** | Neben dem derzeit führenden oder erfolgreichsten Erlebnis wird auch eine Zahl für „Konfidenz“ angezeigt. Diese Zahl wird nur gemeldet, bis die **[!UICONTROL Konfidenz]** des führenden Erlebnisses mindestens 60 % erreicht.<ul><li>Wenn in der Aktivität **[!UICONTROL Automatische Zuordnung]** zwei Erlebnisse vorhanden sind, stellt die Zahl das Konfidenzniveau dar, bei dem die Leistung des Erlebnisses besser ist als bei dem anderen Erlebnis.</li><li>Wenn mehr als zwei Erlebnisse vorhanden sind, stellt die Zahl das Konfidenzniveau dar, bei dem das Erlebnis eine bessere Leistung zeigt als das definierte Kontrollerlebnis.</li><li>Wenn das Kontrollerlebnis gewinnt, wird keine „Konfidenzzahl“ gemeldet.</li></ul> |

## Häufig gestellte Fragen {#faq}

Beachten Sie die folgenden Antworten auf häufig gestellte Fragen.

+++ Es waren ein paar Tage bis zur Aktivität. Warum zeigen alle Konfidenzwerte weiterhin 0 % an?

Einer der folgenden Gründe beschreibt, warum 0 % in der Spalte **[!UICONTROL Konfidenz]** des Berichts für alle Erlebnisse angezeigt wird:

* Manuelle A/B-Tests und **[!UICONTROL Automatische Zuordnung]** verwenden verschiedene Statistiken zur Anzeige **[!UICONTROL Konfidenz]**-Werte.

  Manuelle A/B-Tests verwenden p-Werte, die auf dem [Welch-t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test) basieren. Ein p-Wert ist die Wahrscheinlichkeit, den beobachteten (oder extremeren) Unterschied zwischen einem Erlebnis und der Kontrolle zu finden, da es in Wirklichkeit keinen solchen Unterschied gibt. Diese p-Werte können nur verwendet werden, um festzustellen, ob die beobachteten Daten mit einem bestimmten Erlebnis konsistent sind und die Kontrolle identisch ist. Sie können nicht verwendet werden, um zu bestimmen, ob sich ein Erlebnis von einem anderen Erlebnis (nicht dem Kontrollerlebnis) unterscheidet.

  **[!UICONTROL Automatische Zuordnung]** zeigt die Wahrscheinlichkeit an, dass ein bestimmtes Erlebnis über alle Erlebnisse in der Aktivität hinweg ein echter Gewinner ist. Nur ein erfolgreichstes Erlebnis (bei dem es sich höchstwahrscheinlich um den Gewinner handelt) hat einen Vertrauenswert ungleich null. Bei allen anderen handelt es sich höchstwahrscheinlich um Verlierer, die 0 % anzeigen.

* **[!UICONTROL Automatische Zuordnung]** zeigt erst dann Konfidenz an, wenn das erfolgreichste Erlebnis 60 % Konfidenz erlangt hat. Diese Konfidenzniveaus treten in der Regel in etwa der Hälfte der Zeit auf, die ein normaler A/B-Test benötigen würde (obwohl dieser Zeitrahmen nicht garantiert ist). Um zu bestimmen, wie lange ein normaler A/B-Test ausgeführt werden würde, verwenden Sie den [!DNL Adobe Target] [Stichprobengrößenrechner](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): Geben Sie die Konversionsrate der Kontrolle unter „Baseline-Konversionsrate“, „5 %&quot; für „Steigerung“ und 95 % für „Konfidenz“ ein. In der Regel beginnt die Konfidenz zu zeigen, nachdem jedes Erlebnis mindestens 50 % der erforderlichen Stichproben pro Erlebnis angehäuft hat. Dies gibt Ihnen eine Vorstellung davon, wann Konfidenz anfängt zu erscheinen.

* Wenn der Bericht generell 0 % ausweist, ist es wahrscheinlich zu früh in der Aktivität.

+++

+++ Sind die Abzeichen „Kein Gewinner“, „Gewinner“ und „Stern“ verfügbar für [!UICONTROL Automatische Zuordnung]-Aktivitäten, die [!UICONTROL Analytics] als Berichtsquelle (A4T) verwenden?

Die Abzeichen „Noch kein Gewinner“ und „Gewinner“ werden im Popup-Fenster mit Aktivitätsinformationen in der Liste **[!UICONTROL Aktivitäten]** angezeigt. Sie werden nicht im Bedienfeld **[!UICONTROL A4T]** in [!DNL Analysis Workspace] oder beim Anzeigen desselben Berichts in [!DNL Target] angezeigt. Wenn ein [!DNL Target] für eine Aktivität vom Typ A4T **[!UICONTROL Automatische Zuordnung]** ein Gewinner-Abzeichen „Stern“ anzeigt, ignorieren Sie dies.

Weitere Informationen zu dieser und anderen Einschränkungen finden Sie unter [Automatische Zuordnung](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *A4T-Unterstützung für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]-Aktivitäten*.

+++
