---
description: Die Funktion „Automatisch zuweisen“ identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.
keywords: automatisierte Traffic-Zuordnung; Targeting; Anzahl erhöhen und Benutzer in Aktivität belassen; Traffic-Zuordnung
seo-description: Die Funktion „Automatisch zuweisen“ identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.
seo-title: Automatisch zuweisen
solution: Target
title: Automatisch zuweisen
topic: Standard
uuid: e8aee4d7-2b99-4e1f-8004-2efc820658b5
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Automatisch zuweisen{#auto-allocate}

Die automatisierte Zuordnung identifiziert einen Gewinner aus zwei oder mehr Erlebnissen und führt automatisch mehr Traffic zum Gewinner durch, um die Konversionen zu steigern, während der Test weiter ausgeführt und erlernen wird.

>[!IMPORTANT]
>
>Die „Automatische Zuordnung“ unterstützt keine [!DNL Target for Analytics]-Berichterstellung (A4T).

Beim [Erstellen einer A/B-Aktivität mit einem geleiteten Arbeitsablauf mit drei Schritten](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) können Sie die Option [!UICONTROL Automatisch dem besten Erlebnis zuordnen] wählen.

## Die Herausforderung {#section_85D5A03637204BACA75E19646162ACFF}

Mit A/B-Standardtests sind Kosten verbunden. Sie müssen Traffic generieren, um die Leistung jedes einzelnen Erlebnisses zu messen und durch Analysen die erfolgreichsten Erlebnisse herauszufinden. Die Verteilung von Traffic bleibt auch dann festgelegt, wenn Sie erkennen, dass einige Erlebnisse andere übertreffen. Außerdem ist es schwierig, die Stichprobengröße korrekt zu bestimmen, und die Aktivität muss komplett durchlaufen, bevor Sie einen Sieger finden. Nachdem Sie all das durchgeführt haben, besteht immer noch die Möglichkeit, dass der ermittelte Sieger kein wirklicher Sieger ist.

## Die Lösung: Automatisch zuweisen {#section_98388996F0584E15BF3A99C57EEB7629}

Die Funktion „Automatisierte Zuordnung“ senkt diese Kosten sowie die Kosten für die Bestimmung eines erfolgreichsten Erlebnisses. Die Funktion „Automatisierte Zuordnung“ überwacht die Zielmetrikleistung aller Erlebnisse und sendet proportional mehr neue Teilnehmer an Erlebnisse mit einer hohen Leistung. Es wird ausreichend Traffic für die Erkundung der anderen Erlebnisse reserviert. Sie können die Vorteile des Tests an Ihren Ergebnissen erkennen, selbst wenn die Aktivität gerade ausgeführt wird: Die Optimierung erfolgt parallel zum Lernen.

Die Funktion „Automatisierte Zuordnung“ überführt Besucher nach und nach zu den erfolgreichsten Erlebnissen, anstatt dass Sie mit dem Bestimmen eines Siegers warten müssen, bis die Aktivität abgeschlossen ist. Sie profitieren schneller von Steigerungen, da den Aktivitätsteilnehmern, die zu weniger erfolgreichen Erlebnissen geleitet worden wären, nun potenziell erfolgreiche Erlebnisse angezeigt werden.

Ein normaler A/B-Test zeigt nur den paarweisen Vergleich von Herausforderern mit Kontrollelementen. Wenn eine Aktivität beispielsweise über die Erlebnisse A, B, C und D verfügt, wobei A das Kontrollelement darstellt, wird im Rahmen eines normalen A/B-Tests in Target A mit B, A mit C und A mit D verglichen.

In solchen Tests setzen die meisten Produkte - inklusive Target - einen Student-T-Test ein, um eine P-Wert-basierte Konfidenz zu erhalten. Mithilfe dieses Konfidenzwerts wird dann ermittelt, ob sich der Herausforderer ausreichend vom Kontrollelement unterscheidet. In Target werden jedoch nicht automatisch implizierte Vergleiche (B mit C, B mit D und C mit D) durchgeführt, die erforderlich sind, um das Gewinnererlebnis zu ermitteln. Aus diesem Grund müssen Marketingexperten die Ergebnisse manuell analysieren, um das Gewinnererlebnis zu ermitteln.

Die automatisierte Zuordnung führt alle impliziten Vergleiche über alle Erlebnisse hinweg durch und ergibt dann einen „wahren“ Gewinner. Es gibt in diesem Test keinen Bedarf für ein „Kontrollerlebnis“.

Mit der automatisierten Zuordnung werden neue Besucher auf vernünftige Weise den verschiedenen Erlebnissen zugeordnet, bis das Konfidenzintervall des besten Erlebnisses nicht mehr Intervalle anderer Erlebnisse überdeckt. Normalerweise könnte dieses Vorgehen zu falsch positiven Ergebnissen führen, aber die automatisierte Zuweisung verwendet Konfidenzintervalle, die auf der [Bernstein-Ungleichung](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) basieren, um wiederholte Auswertungen zu kompensieren. An diesem Punkt haben wir einen echten Gewinner. Wenn die automatische Zuordnung gestoppt wird, wenn die Besucher, die auf die Seite gelangen, keine erhebliche Zeitabhängigkeit aufweisen, besteht mindestens eine 95% ige Wahrscheinlichkeit, dass die automatische Zuordnung ein Erlebnis zurückgibt, dessen wahre Antwort nicht unter 1% liegt (relativ), um weniger als die wahre Antwort des Gewinn-Erlebnisses zu erhalten.

## Verwendung der Funktion „Automatisierte Zuordnung“ im Vergleich zu A/B oder zu automatisierter Personalisierung {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Die Funktion **Automatisierte Zuordnung** verwenden Sie, wenn Sie Ihre Aktivitäten von Anfang an optimieren und so schnell wie möglich feststellen möchten, welche die erfolgreichsten Erlebnisse sind. Durch eine häufigere Darstellung von leistungsstarken Erlebnissen wird die Gesamtleistung der Aktivität gesteigert.
* Verwenden Sie einen standardmäßigen **[A/B-Test](../../c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)**, wenn Sie die Leistung aller Erlebnisse vor der Optimierung Ihrer Site charakterisieren möchten. Ein A/B-Test hilft Ihnen dabei, alle Ihre Erlebnisse in einer Reihenfolge zu ordnen, während die automatisierte Traffic-Zuordnung Spitzenreiter findet, jedoch keine Differenzierung unter den weniger leistungsstarken Erlebnissen garantiert.
* Verwenden Sie [Automatisierte Personalisierung](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9), wenn Sie Optimierungsalgorithmen mit höchster Komplexität wünschen, zum Beispiel Modelle für maschinelles Lernen, die Vorhersagen auf der Basis von individuellen Profilattributen aufbauen. Die automatisierte Traffic-Zuordnung betrachtet das zusammentreffende Verhalten von Erlebnissen (wie A/B-Standardtests) und unterscheidet nicht zwischen den Besuchern.

## Wesentliche Vorteile   {#section_0913BF06F73C4794862561388BBDDFF0}

* Behält die Genauigkeit eines A/B-Tests bei
* Ermittelt einen statistisch bedeutenden Sieger schneller als mit manuellen A/B-Tests
* Bietet höhere durchschnittliche Kampagnensteigerungen im Vergleich zu manuellen A/B-Tests

## Terminologie {#section_670F8785BA894745B43B6D4BFF953188}

Bei Erörterungen zur automatisierten Zuordnung sind die folgenden Begriffe hilfreich:

**Multi-Armed Bandit:** Eine [Multi-Armed Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit)-Vorgehensweise („Mehrarmiger Bandit“) zur Optimierung gleicht forschendes Lernen und die Verwertung dieses Lernens aus.

## So funktioniert der Algorithmus {#section_ADB69A1C7352462D98849F2918D4FF7B}

Die Gesamtlogik hinter der automatisierten Zuordnung beinhaltet sowohl die gemessene Leistung (z. B. Konversionsrate) als auch Konfidenzintervalle der kumulativen Daten. Im Gegensatz zum normalen A/B-Test, bei dem Traffic gleichmäßig zwischen Erlebnissen aufgeteilt wird, ändert die „Automatisierte Zuordnung“ die Zuordnung von Traffic zu den verschiedenen Erlebnissen.

* 80 % der Besucher werden mithilfe der unten beschriebenen intelligenten Logik zugeordnet.
* 20 % der Besucher werden auf zufälliger Basis den verschiedenen Erlebnissen zugeordnet, um eine Anpassung an sich änderndes Besucherverhalten zu ermöglichen.

Die Multi-Armed Bandit-Methode hält einige Erlebnisse für die Erforschung frei, während die leistungsstarken Erlebnisse ausgewertet werden. Es werden mehr neue Besucher in leistungsstärkere Erlebnisse platziert, und gleichzeitig wird die Reaktionsfähigkeit auf sich ändernde Bedingungen beibehalten. Diese Modelle werden mindestens einmal pro Stunde aktualisiert, um sicherzustellen, dass das Modell auf die neuesten Daten reagiert.

Sobald mehr Besucher an der Aktivität teilnehmen, erweisen sich einige Erlebnisse als erfolgreicher und erhalten mehr Traffic. 20 Prozent des Datenverkehrs werden weiterhin per Zufall verteilt, um alle Erlebnisse zu erforschen. Wenn ein Erlebnis mit einer schlechteren Leistung anfängt, sich zu verbessern, erhält es mehr Traffic. Oder: Wenn eine erfolgreiche Aktivität nachlässt, wird diesem Erlebnis weniger Traffic zugeordnet. Zum Beispiel wenn ein Ereignis dazu führt, dass Besucher nach anderen Informationen auf Ihrer Medienwebsite suchen oder wenn Wochenendverkäufe auf Ihrer Retail-Website unterschiedliche Ergebnisse liefern.

Die folgende Abbildung zeigt, wie der Algorithmus während eines Tests mit vier Erlebnissen möglicherweise funktioniert:

![](assets/auto-allocate.png)

Die Abbildung zeigt, wie sich der den einzelnen Erlebnissen zugeordnete Traffic ändert, während die Aktivität mehrere Runden durchläuft, bis ein Gewinner gefunden ist.

| Rund | Beschreibung |
|--- |--- |
| ![Aufwärmrunde](/help/c-activities/automated-traffic-allocation/assets/aa-phase-0.png) | **Aufwärmrunde (0)**: Während der Aufwärmrunde wird für jedes Erlebnis gleich viel Traffic zugeteilt, bis jedes Erlebnis in der Aktivität mindestens 1.000 Besucher und 50 Konversionen aufweist.<ul><li>Erlebnis A = 25 %</li><li>Erlebnis B = 25 %</li><li>Erlebnis C = 25 %</li><li>Erlebnis D = 25 %</li></ul>Nachdem jedes Erlebnis 1.000 Besucher und 50 Konversionen erreicht hat, startet Target die automatisierte Zuordnung von Traffic. Sämtliche Zuordnungen werden in Runden vorgenommen, wobei für jede Runde zwei Erlebnisse herausgesucht werden.<br>Nur zwei Erlebnisse gelangen in die nächste Runde: D und C.<br> Dies bedeutet, dass nun 80% des Traffics gleichmäßig auf diese beiden Erlebnisse verteilt werden, während die anderen beiden Erlebnisse zwar weiterhin teilnehmen, aber ihnen nur noch 20% des Traffics auf zufälliger Basis zugeordnet werden, wenn neue Besucher an der Aktivität teilnehmen.<br>Sämtliche Zuordnungen werden stündlich aktualisiert (erkennbar an der Rundenangabe auf der X-Achse in der Abbildung oben). Nach jeder Runde werden die kumulativen Daten verglichen. |
| ![Runde 1](/help/c-activities/automated-traffic-allocation/assets/aa-phase-1.png) | **Runde 1**: Während dieser Runde werden 80% des Traffics den Erlebnissen C und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis den Erlebnissen A, B, C und D zugeordnet (jeweils 5 %). Während dieser Runde werden beim Erlebnis A gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt das Erlebnis D für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der Markierung auf der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis A für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und A gelangen eine Runde weiter. |
| ![Runde 2](/help/c-activities/automated-traffic-allocation/assets/aa-phase-2.png) | **Runde 2**: Während dieser Runde werden 80% des Traffics den Erlebnissen A und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis B gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt das Erlebnis D für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der Markierung auf der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis B für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und B gelangen eine Runde weiter. |
| ![Runde 3](/help/c-activities/automated-traffic-allocation/assets/aa-phase-3.png) | **Runde 3**: Während dieser Runde werden 80% des Traffics den Erlebnissen B und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis D weiterhin gute Leistungen verzeichnet und auch das Erlebnis C läuft gut.<ul><li>Der Algorithmus wählt das Erlebnis D für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der Markierung auf der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis C für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse D und C gelangen eine Runde weiter. |
| ![Runde 4](/help/c-activities/automated-traffic-allocation/assets/aa-phase-4.png) | **Runde 4**: Während dieser Runde werden 80% des Traffics den Erlebnissen C und D zugeordnet (jeweils 40%). 20 % des Traffics werden auf zufälliger Basis zugeordnet, das heißt A, B, C und D erhalten jeweils 5 % des Traffics. Während dieser Runde werden beim Erlebnis C gute Leistungen verzeichnet.<ul><li>Der Algorithmus wählt das Erlebnis C für die nächste Runde aus, da es die höchste Konversionsrate erzielt hat (erkennbar an der Markierung auf der vertikalen Skala jeder Aktivität).</li><li>Außerdem wählt der Algorithmus auch das Erlebnis D für die nächste Runde aus, da es die höchste Obergrenze des Bernstein-95-%-Konfidenzintervalls der verbleibenden Erlebnisse erreicht hat.</li></ul>Die Erlebnisse C und D gelangen eine Runde weiter. |
| ![Runde n](/help/c-activities/automated-traffic-allocation/assets/aa-phase-n.png) | **Runde n**: Im weiteren Verlauf der Aktivität zeigt sich, dass ein Erlebnis die besten Leistungen erreicht. Dieser Prozess geht so lange weiter, bis ein „siegreiches“ Erlebnis ermittelt ist. Wenn sich das Konfidenzintervall des Erlebnisses mit der höchsten Konversionsrate nicht mit dem Konfidenzintervall anderer Erlebnisse überschneidet, ist es der Gewinner und eine [Markierung wird auf der Seite der Aktivität](/help/c-activities/automated-traffic-allocation/determine-winner.md) und in der Aktivitätsliste angezeigt.<ul><li>Der Algorithmus erklärt das Erlebnis C zum klaren Gewinner</li></ul>An diesem Punkt ordnet der Algorithmus 80 % des Traffics Erlebnis C zu, während 20 % des Traffics weiterhin auf zufälliger Basis allen Erlebnissen (A, B, C und D) zugeordnet werden. C erhält insgesamt 85 % des Traffics. In dem unwahrscheinlichen Fall, dass das Konfidenzintervall des Gewinners erneut anfängt, andere Intervalle zu überdecken, kehrt der Algorithmus zu dem Verhalten der obigen Runde 4 zurück.<br>**Wichtig**: Wenn Sie während des Prozesses vorzeitig einen Gewinner manuell auswählen, riskieren Sie, das falsche Erlebnis auszuwählen. Daher empfiehlt es sich unbedingt, so lange zu warten, bis der Algorithmus das „siegreiche“ Erlebnis ermittelt hat. |

Verfügt die Aktivität nur über zwei Erlebnisse, erhalten beide gleich große Anteile des Traffics, bis Target das Erlebnis mit 90 % Konfidenz ermitteln konnte. Ab diesem Zeitpunkt werden 70 % des Traffics an das Gewinnerlerlebnis und 30 % an das andere Erlebnis weitergeleitet. Wird eine Konfidenz von 95 % erzielt, werden 100 % des Traffics an das Gewinnerlerlebnis weitergeleitet und 0 % an das übrige Erlebnis.

Wenn das Modell für eine automatisierte Zuordnungsaktivität bereit ist (alle Erlebnisse haben mindestens 1.000 Besucher und 50 Konversionen), sind folgende Vorgänge über die Benutzeroberfläche nicht mehr zulässig:

* Umschalten des Modus „Traffic-Zuordnung“ auf „Manuell“
* Ändern des Zielmetriktyps
* Ändern der Optionen im Bedienfeld „Erweiterte Einstellungen“

## Einschränkungen {#section_5C83F89F85C14FD181930AA420435E1D}

**A/B-Aktivitäten mit automatisierter Zuordnung werden in Analytics for Target (A4T) nicht mehr unterstützt**

Ab Version 16.10.1.0 (vom 25. Oktober 2016) unterstützt Target nicht mehr Analytics als Berichtsquelle für A/B-Aktivitäten mit automatisierter Zuordnung. Alle noch aktiven A/B-Aktivitäten mit automatischer Zuordnung, bei denen A4T aktiviert ist, werden auf den manuellen Modus umgestellt (gleichmäßige Zuordnung von Traffic).

**Die Funktion „Automatisierte Zuordnung“ arbeitet mit nur einer einzigen erweiterten Metrikeinstellung: „Anzahl erhöhen und Benutzer in Aktivität belassen“.**

Die folgenden erweiterten Metrikeinstellungen werden nicht unterstützt: „Anzahl erhöhen“, „Benutzer freigeben“, „Wiedereintritt erlauben und Anzahl erhöhen“ sowie „Benutzer freigeben und an Wiedereintritt hindern“.

**Häufig wiederkehrende Besucher können die Konversionsraten von Erlebnissen erhöhen.**

Wenn ein Besucher, der Erlebnis A anzeigt, häufig zurückkehrt und mehrere Male konvertiert, wird die Konversionsrate (CR) von Erlebnis A künstlich erhöht. Vergleichen Sie dies mit Erlebnis B, wo Besucher konvertieren, jedoch nicht häufig zurückkehren. Daher sieht die CR von A besser aus als die CR von B, sodass neue Besucher wahrscheinlich eher zu A als zu B geleitet werden. Wenn Sie jeden Teilnehmer nur einmal zählen, sind die CR von A und die CR von B möglicherweise identisch.

Wenn wiederkehrende Besucher zufällig verteilt werden, wird ihre Wirkung auf die Konversionsrate wahrscheinlich eher ausgeglichen. Um diese Auswirkung zu beschränken, sollten Sie die Änderung der Zählmethode der Zielmetrik erwägen, um jeden Teilnehmer nur einmal zu zählen.

**Differenziert zwischen High Performern, nicht zwischen Low Performern.**

Die automatisierte Zuordnung kann gut zwischen leistungsstarken Erlebnissen unterscheiden (und einen Sieger ermitteln). Es kann vorkommen, dass Sie nicht genug zwischen den leistungsschwachen Erlebnissen unterscheiden können.

Wenn Sie eine statistisch signifikante Differenzierung zwischen allen Erlebnissen erzeugen möchten, sollten Sie die manuelle Zuordnungsmethode für den Traffic in Betracht ziehen.

**Zeitkorrelierte (oder je nach Kontext variierende) Konversionsraten beeinflussen die Zuordnungsmengen.**

Einige Faktoren, die während eines normalen A/B-Tests ignoriert werden dürfen, da sie sich auf alle Erlebnisse gleichmäßig auswirken, können bei einem Test mit automatisierter Zuordnung nicht ignoriert werden. Der Algorithmus ist gegenüber den beobachteten Konversionsraten empfindlich. Nachfolgend finden Sie Beispiele für Faktoren, die sich ungleichmäßig auf die Erlebnisleistung auswirken können:

* Erlebnisse mit variierender kontextueller (Zeit, Standort, Geschlecht usw.) Relevanz.

   Beispiel:

   * „Zum Glück ist Freitag“ führt an Freitagen zu höheren Konversionen.
   * „Starthilfe für Ihren Montag“ hat an Montagen höhere Konversionen.
   * „Machen Sie sich bereit für den Winter an der Ostküste“ bietet in Regionen an der Ostküste oder in vom Winter geplagten Regionen eine höhere Konversion.

Diese Faktoren können die Ergebnisse eines Tests mit automatisierter Zuordnung stärker als die eines A/B-Tests verfälschen, da der A/B-Test die Ergebnisse über einen längeren Zeitraum analysiert.

* Erlebnisse mit variierenden Verzögerungen in der Konversion, möglicherweise aufgrund der Dringlichkeit der Nachricht.

   Zum Beispiel signalisiert „30 Prozent Rabatt nur noch heute“ dem Besucher, noch heute zu konvertieren, während „50 Prozent Rabatt auf Ihren ersten Einkauf“ nicht denselben Handlungsdruck auslöst.

## Häufig gestellte Fragen {#section_0E72C1D72DE74F589F965D4B1763E5C3}

**Werden wiederkehrende Besucher automatisch zu leistungsstarken Erlebnissen weitergeleitet?**

Nein. Nur neue Besucher werden automatisch zugeordnet. Wiederkehrende Besucher sehen weiterhin ihr ursprüngliches Erlebnis. Dies schützt die Gültigkeit des A/B-Tests.

**Wie behandelt der Algorithmus falsch-positive Ergebnisse?**

Der Algorithmus garantiert eine Konfidenz von 95 % oder eine Falsch-positiv-Rate von 5 %, wenn Sie warten, bis ein Gewinnerabzeichen angezeigt wird.

**Ab wann wird bei automatischer Zuordnung Traffic zugeordnet?**

Der Algorithmus setzt ein, nachdem sämtliche Erlebnisse in der Aktivität mindestens 1.000 Besucher und 50 Konversionen erreicht haben.

**Wie aggressiv wertet der Algorithmus aus?**

80 % des Traffics werden mittels automatisierter Zuordnung und 20 % des Traffics auf zufälliger Basis zugeteilt. Wenn ein Gewinner ermittelt ist, erhält dieser die gesamten 80 %, während alle Erlebnisse, einschließlich des Gewinners, ihren jeweiligen Anteil an den 20 % des Traffics erhalten.

**Werden sehr schwache Erlebnisse überhaupt angezeigt?**

Ja. Die Multi-Armed Bandit-Methode stellt sicher, dass mindestens 20 % des Datenverkehrs für die Erforschung von Änderungsmustern oder Konversionsraten in allen Erlebnissen reserviert werden.

**Was passiert mit Aktivitäten mit langen Konversionsverzögerungen?**

Solange alle Erlebnisse, die optimiert werden, ähnliche Verzögerungen aufweisen, ist das Verhalten wie bei einer Aktivität mit schnellerem Konversionszyklus, auch wenn es länger dauert, den Grenzwert von 50 Konversionen zu erreichen, ab dem die Traffic-Zuordnung beginnt.

**Worin unterscheidet sich automatisierte Zuordnung von automatisierter Personalisierung?**

Bei der automatisierten Personalisierung werden die Profilattribute aller Besucher verwendet, um das beste Erlebnis zu bestimmen. Dadurch wird die Aktivität für den jeweiligen Besucher nicht nur optimiert, sondern auch personalisiert.

Bei der automatisierten Zuordnung handelt es sich jedoch um einen A/B-Test, der einen Gesamtgewinner erzeugt (das beliebteste Erlebnis, das nicht zwingend für jeden Benutzer das effektivste Erlebnis sein muss).

**Erhöhen wiederkehrende Besucher die Konversionsrate in meiner Erfolgsmetrik?**

Derzeit bevorzugt die Logik Besucher, die schnell konvertieren oder die Site häufiger besuchen. Dies beruht darauf, dass solche Besucher die Gesamtkonversionsrate des Erlebnisses, zu dem sie gehören, vorübergehend erhöhen. Der Algorithmus passt sich häufig von selbst an, sodass die Steigerung der Konversionsrate bei jeder Momentaufnahme verstärkt wird. Wenn die Site viele wiederkehrende Besucher verzeichnet, können deren Konversionen die Gesamtkonversionsrate für das Erlebnis, zu dem sie gehören, möglicherweise erhöhen. Es bestehen gute Chancen, dass wiederkehrende Besucher per Zufall verteilt werden; in diesem Fall wird die Gesamtwirkung (Anstieg) ausgeglichen. Um diese Auswirkung zu beschränken, sollten Sie die Änderung der Zählmethode der Erfolgsmetrik erwägen, um jeden Teilnehmer nur einmal zu zählen.

**Kann ich den Stichprobengrößenrechner verwenden, wenn ich mit der automatischen Zuordnung schätzen möchte, wie lange die Aktivität zur Identifizierung des Gewinners benötigt wird?**

Sie können den vorhandenen [Rechner für die Stichprobengröße](https://docs.adobe.com/content/target-microsite/testcalculator.html) mit einer passend angewendeten Bonferroni-Korrektur verwenden, um eine Schätzung der Laufzeit des Tests zu erhalten. Bei unseren Experimenten haben wir festgestellt, dass die automatisierte Zuordnungsaktivität wesentlich früher endet, als diese Stichprobengröße.

**Sollte ich ein leistungsschwaches Erlebnis aus einer automatischen Zuordnung entfernen, um einen Gewinner zu bestimmen?**

Es gibt keinen Grund, ein leistungsschwaches Erlebnis zu entfernen. Die automatisierte Zuordnung bietet automatisch leistungsstarke Erlebnisse und liefert leistungsschwache Erlebnisse weniger häufig. Wenn Sie ein leistungsschwaches Erlebnis in der Aktivität hinterlassen, wird die Geschwindigkeit zur Ermittlung eines Gewinners nicht wesentlich beeinträchtigt.

20% der Besucher werden zufällig allen Erlebnissen zugewiesen. Der Traffic, der für ein leistungsschwaches Erlebnis bereitgestellt wird, ist minimal (20% geteilt durch die Anzahl der Erlebnisse).

## Schulungsvideos {#section_893E5B36DC4A415C9B1D287F51FCCB83}

Die folgenden Videos enthalten weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Arbeitsablauf für Aktivitäten – Targeting (2:14)

In diesem Video sind Informationen zur Einrichtung der Traffic-Zuordnung enthalten.

* Zuweisen einer Zielgruppe zur Aktivität
* Regulieren von Traffic nach oben oder unten
* Auswählen der Zuordnungsmethode für den Traffic
* Zuweisen von Traffic zu verschiedenen Erlebnissen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Erstellen von A/B-Tests (8:36)

In diesem Video wird gezeigt, wie mithilfe des geleiteten Target-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird. Automatisierte Traffic-Zuordnung wird ab 4:45 besprochen.

* Erstellen einer A/B-Aktivität in Adobe Target
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)