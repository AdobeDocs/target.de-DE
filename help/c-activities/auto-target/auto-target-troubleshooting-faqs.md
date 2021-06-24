---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung; Traffic
description: Erfahren Sie mehr zur Fehlerbehebung und erhalten Sie Antworten auf häufig gestellte Fragen zu automatischen Targeting-Aktivitäten in Adobe Target.
title: Wie kann ich Probleme in Verbindung mit automatischen Targeting-Aktivitäten beheben?
feature: Automatisches Targeting
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: d1579a56e46b806c3e4a0cb1748e5682b0900d11
workflow-type: tm+mt
source-wordcount: '1920'
ht-degree: 100%

---

# ![PREMIUM](/help/assets/premium.png) Automatisches Targeting – Fehlerbehebung und häufig gestellte Fragen

Fehlerbehebung und häufig gestellte Fragen (FAQs) zum [!UICONTROL automatischen Targeting] in [!DNL Adobe Target].

## Häufig gestellte Fragen zum automatischen Targeting {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Konsultieren Sie bei Problemen mit [!UICONTROL automatischen Targeting]-Aktivitäten die folgenden häufig gestellten Fragen und Antworten:

### Wie lauten die Best Practices zum Einrichten einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]?

* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik vom Typ „Umsatz pro Besuch“ (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen Kontroll- und personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Ermitteln Sie, ob Sie über ausreichend Traffic für die Seite verfügen, auf der Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] in einer angemessenen Dauer für zu erstellende Personalisierungsmodelle ausgeführt wird.
   * Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie weder Erlebnisse ändern noch Profilattribute hinzufügen/entfernen, während die Aktivität aktiv ist.

* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Positionen ab, die Sie für Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] verwenden möchten, um sicherzustellen, dass sich die Position(en) und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, kommt es wahrscheinlich auch nicht zu einer Steigerung durch [!UICONTROL Automatisches Targeting].

   * Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während des Aktivitätsverlaufs wesentliche Änderungen an den Erlebnissen vorzunehmen.

### Wird die Verwendung von [!UICONTROL automatischem Targeting] mit einer Aufteilung von 90 (Kontrolle) zu 10 (Targeting) bis zur Erstellung der Modelle empfohlen?

Wie Ihre optimale Aufteilung der Traffic-Zuordnung aussieht, hängt davon ab, was Sie erreichen möchten.

Wenn es Ihr Ziel ist, so viel Traffic wie möglich zu personalisieren, können Sie während der Lebensdauer der Aktivität bei der Aufteilung von 90 % Kontrolle und 10 % Targeting bleiben. Ist es aber Ihr Ziel, ein Experiment durchzuführen, durch das verglichen werden soll, wie gut personalisierte Algorithmen gegenüber der Kontrolle abschneiden, empfiehlt sich während der Lebensdauer der Aktivität eine Aufteilung von 50/50.

Best Practice ist es auf jeden Fall, die Aufteilung der Traffic-Zuordnung während der Lebensdauer einer Aktivität nicht zu ändern, damit die Besucher nicht zwischen Targeting- und Kontrollerlebnissen verschoben werden.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

### Wenn ein Besucher die Aktivität vom Typ [!UICONTROL Automatisches Targeting] NICHT sieht und konvertiert, zählt dann die Konversion in meiner Aktivität?

Nein, es werden nur die Besucher im Bericht gezählt, die sich für die Aktivität vom Typ [!UICONTROL Automatisches Targeting] qualifizieren und sie anzeigen.

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] generiert offenbar keine Steigerung. Was ist los?

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automated Personalization] eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

### Wann sollte ich meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anhalten?

[!UICONTROL „Automatisches Targeting“] kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzuhalten.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

### Wie lange sollte ich warten, bis Modelle erstellt werden? {#how-long}

Wie lange es dauert, bis in Ihrer [!UICONTROL automatischen Targeting]-Aktivität Modelle erstellt werden, hängt in der Regel vom Traffic auf den jeweiligen Sites und der Konversionsrate der in der Aktivität festgelegten Erfolgsmetrik ab.

Das [!UICONTROL automatische Targeting] beginnt erst mit der Erstellung eines personalisierten Modells für ein bestimmtes Erlebnis, wenn mindestens 50 Konversionen für dieses Erlebnis vorhanden sind. Außerdem wird das Modell nicht zur personalisierten Bereitstellung von Traffic verwendet, wenn die Qualität des erstellten Modells unzureichend ist (die Qualität wird durch Offline-Auswertung vorgehaltener „Test“-Daten mittels der [Metrik „AUC“](https://de.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve) bestimmt).

Darüber hinaus sind auch die folgenden Punkte bei der Modellerstellung durch [!UICONTROL automatisches Targeting] zu berücksichtigen:

* Sobald eine Aktivität live ist, berücksichtigt [!UICONTROL automatisches Targeting] die zufällig bereitgestellten Daten der maximal letzten 45 Tage beim Versuch, ein Modell zu erstellen (d. h. den Kontroll-Traffic sowie einige zusätzliche, zufällig bereitgestellte Daten, die von unserem Algorithmus vorgehalten werden).
* Aktivitäten mit der Erfolgsmetrik [!UICONTROL Umsatz pro Besuch] benötigen in der Regel mehr Daten zum Erstellen von Modellen. Dies liegt daran, dass die Datenvarianz bei „Umsatz pro Besuch“ normalerweise höher als bei „Konversionsrate“ ist.
* Da Modelle für einzelne Erlebnisse erstellt werden, muss vor dem Ersatz eines Erlebnisses durch ein anderes ausreichend Traffic (mindestens 50 Konversionen) für das neue Erlebnis gesammelt worden sein, bevor das personalisierte Modell neu erstellt wird.

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

### Ab wann kann ich die Ergebnisse meiner Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen?

Sie können die Ergebnisse Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen, sobald Sie über mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, die Modelle erstellt haben.

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

Sie können bei der Erstellung einer [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/c-activities/t-automated-personalization/experience-as-control.md).

### Kann ich die Zielmetrik inmitten einer automatischen Targeting-Aktivität ändern? {#change-metric}

Von der Änderung der Zielmetrik inmitten einer Aktivität raten wir ab. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. Es ist unmöglich, vorherzusagen, was passiert, wenn die Zielmetrik einer Aktivität während deren Ausführung geändert wird.

Diese Empfehlung gilt gleichermaßen für [!UICONTROL automatische Zuordnungs]-, [!UICONTROL automatische Targeting]- und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

### Kann ich die Option „Berichtsdaten zurücksetzen“ während der Ausführung einer automatischen Targeting-Aktivität verwenden?

Die Verwendung der Option [!UICONTROL Berichtsdaten zurücksetzen] für [!UICONTROL automatische Targeting]-Aktivitäten wird nicht empfohlen. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem [!UICONTROL automatischen Targeting]-Modell. Statt für eine [!UICONTROL automatische Targeting]-Aktivität die Option [!UICONTROL Berichtsdaten zurücksetzen] zu verwenden, empfiehlt sich die Erstellung einer neuen Aktivität und die Deaktivierung der ursprünglichen Aktivität. (Hinweis: Diese Anleitung gilt auch für [!UICONTROL automatische Zuordnungs]- und [!UICONTROL Automated Personalization]-Aktivitäten.)

### Was passiert, wenn ich ein einzelnes Erlebnis aus einer automatischen Targeting-Aktivität entferne?

[!DNL Target] erstellt für jedes Erlebnis ein eigenes Modell. Wenn Sie also ein Erlebnis entfernen, erstellt [!DNL Target] einfach ein Modell weniger. Dies wirkt sich nicht auf die Modelle der anderen Erlebnisse aus.

Angenommen, Sie haben eine [!UICONTROL automatische Targeting]-Aktivität mit acht Erlebnissen, und die Performance eines dieser Erlebnisse sagt Ihnen gar nicht zu. Sie können dieses Erlebnis ohne Bedenken entfernen. Dies hat keine Auswirkung auf die Modelle der sieben verbleibenden Erlebnisse.

## Fehlerbehebung für [!UICONTROL Automatisches Targeting] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, die sich möglicherweise aus der Verwendung von [!UICONTROL Automatisches Targeting] ergeben, sowie die jeweils vorgeschlagenen Lösungen.

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] braucht zu lange, um Modelle zu erstellen.

Es gibt verschiedene Aktivitätseinrichtungsänderungen, welche die zum Erstellen von Modellen erwartete Dauer verringern können. Dazu zählen die Anzahl der Erlebnisse in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting], der Traffic auf Ihrer Site sowie Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung dahingehend, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, in der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn die Anzahl der Erlebnisse in einer Aktivität verringert wird, wird das Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitätspositionen vorhanden sind, desto schneller werden die Modelle erstellt.

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] generiert keine Steigerung.

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ „Automated Personalization“ eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn die Modelle nicht für alle Erlebnisse erstellt sind, verarbeitet Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] weiterhin zufallsbasiert einen signifikanten Teil an Besuchen, um zu versuchen, alle Modelle schnellstmöglich zu erstellen. Ohne erstellte Modelle wird der Traffic mit [!UICONTROL Automatisches Targeting] nicht personalisiert.

Stellen Sie als Nächstes mithilfe eines nicht personalisierten A/B-Tests sicher, dass die Angebote und Aktivitätspositionen wirklich einen Unterschied für die Gesamtantwortraten ausmachen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

### Die von einer Konversionsmetrik abhängigen Metriken werden nicht konvertiert.

Dieses Ergebnis ist zu erwarten.

Bei einer Aktivität vom Typ [!UICONTROL Automatisches Targeting] wird der Benutzer von dem Erlebnis abgekoppelt und die Aktivität neu gestartet, sobald eine Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder nachgelegenes Ziel handelt) konvertiert wurde.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist abhängig von C1. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 und erst danach A1 konvertiert, wird A1 auch dann nicht konvertiert, da der Besucher abgekoppelt wird, sobald C1 konvertiert ist.
