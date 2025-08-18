---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung; Traffic
description: Erfahren Sie mehr über Fehlerbehebungsthemen und häufig gestellte Fragen zu [!UICONTROL Auto-Target].
title: Wie kann ich Fehler bei [!UICONTROL Auto-Target] Aktivitäten beheben?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 32%

---

# Häufig gestellte Fragen zu [!UICONTROL Auto-Target] und Fehlerbehebung

Fehlerbehebung und häufig gestellte Fragen (FAQs) zu [!UICONTROL Auto-Target] in [!DNL Adobe Target].

## Häufig gestellte Fragen zu [!UICONTROL Auto-Target] {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Konsultieren Sie bei Problemen mit [!UICONTROL Auto-Target] die folgenden häufig gestellten Fragen und Antworten:

### Wie lauten die Best Practices zum Einrichten einer [!UICONTROL Auto-Target] Aktivität?

+++Antwort
* Entscheiden Sie, ob der Geschäftswert einer [!UICONTROL Revenue per Visit] (RPV)-Erfolgsmetrik die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen Kontroll- und personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Stellen Sie fest, ob ausreichend Traffic zu der Seite vorhanden ist, auf der Ihre [!UICONTROL Auto-Target] ausgeführt wird, damit Personalisierungsmodelle in angemessener Zeit erstellt werden können.
* Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie während der Live-Aktivität keine Erlebnisse ändern oder Profilattribute hinzufügen oder entfernen.
* Erwägen Sie den Abschluss einer A/B-Aktivität zwischen den Angeboten und Standorten, die Sie in Ihrer [!UICONTROL Auto-Target]-Aktivität verwenden möchten, um sicherzustellen, dass die Standorte und Angebote Auswirkungen auf das Optimierungsziel haben. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigt, generiert [!UICONTROL Auto-Target] wahrscheinlich auch keine Steigerung.

  Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während der Aktivität keine wesentlichen Änderungen an den Erlebnissen vorzunehmen.

+++

### Wird [!UICONTROL Adobe] die Verwendung von [!UICONTROL Auto Target] mit einer Aufteilung von 90 (Kontrolle) zu 10 (Targeting) empfohlen, bis die Modelle erstellt werden?

+++Antwort 
Wie Ihre optimale Aufteilung der Traffic-Zuordnung aussieht, hängt davon ab, was Sie erreichen möchten.

Wenn es Ihr Ziel ist, so viel Traffic wie möglich zu personalisieren, können Sie während der Lebensdauer der Aktivität bei der zielgerichteten Zuordnung von 90 % und der Kontrolle von 10 % bleiben. Wenn Sie ein Experiment durchführen möchten, in dem die Leistung personalisierter Algorithmen mit der Kontrolle verglichen wird, empfiehlt sich während der Lebensdauer der Aktivität eine Aufteilung von 50/50.

Best Practice ist es auf jeden Fall, die Aufteilung der Traffic-Zuordnung während der Lebensdauer einer Aktivität nicht zu ändern, damit die Besucher nicht zwischen Targeting- und Kontrollerlebnissen verschoben werden.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Wenn ein Besucher **nicht** die [!UICONTROL Auto-Target] Aktivität sieht und konvertiert, zählt dann die Konversion in meiner Aktivität?

+++Antwort
Nein, es werden nur die Besucher im Bericht gezählt, die sich für die [!UICONTROL Auto-Target]-Aktivität qualifizieren und sie anzeigen.

+++

### Warum scheint meine [!UICONTROL Auto-Target]-Aktivität keine Steigerung zu erzeugen?

+++Antwort
Es sind vier Faktoren erforderlich, damit eine [!UICONTROL Auto-Target] Aktivität eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. In der Regel liegt das Problem daran, dass die Angebote und Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

### Wann sollte ich meine [!UICONTROL Auto-Target] anhalten?

+++Antwort
[!UICONTROL Auto-Target] kann als „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre [!UICONTROL Auto-Target] zu stoppen.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer [!UICONTROL Auto-Target]-Aktivität vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

+++

### Wie lange sollte ich warten, bis Modelle erstellt werden? {#how-long}

+++Antwort
Wie lange es dauert, bis in Ihrer [!UICONTROL Auto-Target]-Aktivität Modelle erstellt werden, hängt in der Regel vom Traffic auf den ausgewählten Aktivitätsstandorten und den Konversionsraten Ihrer Aktivitätserfolgsmetrik ab.

[!UICONTROL Auto-Target] versucht erst dann, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, wenn mindestens 50 Konversionen für dieses Erlebnis vorhanden sind. Außerdem wird das Modell nicht zur personalisierten Bereitstellung von Traffic verwendet, wenn die Qualität des erstellten Modells unzureichend ist (die Qualität wird durch Offline-Auswertung vorgehaltener „Test“-Daten mithilfe [einer Metrik namens AUC](https://de.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve) bestimmt).

Einige weitere Punkte, die Sie bei der Modellerstellung von [!UICONTROL Auto-Target] beachten sollten:

* Nachdem eine Aktivität live ist, berücksichtigt [!UICONTROL Auto-Target] beim Versuch, Modelle zu erstellen, die zufällig bereitgestellten Daten der maximal letzten 45 Tage. Beispielsweise Kontroll-Traffic sowie einige zusätzliche, zufällig bereitgestellte Daten, die vom Algorithmus vorgehalten werden.
* Wenn [!UICONTROL Revenue per Visit] Ihre Erfolgsmetrik ist, benötigen diese Aktivitäten in der Regel mehr Daten zum Erstellen von Modellen. Dies liegt daran, dass die Datenvarianz bei „Umsatz besucht“ normalerweise höher als bei „Konversionsrate“ ist.
* Da Modelle für einzelne Erlebnisse erstellt werden, bedeutet der Austausch eines Erlebnisses durch ein anderes, dass für das neue Erlebnis ausreichend Traffic (mindestens 50 Konversionen) erfasst werden muss, bevor das personalisierte Modell neu erstellt werden kann.

+++

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

+++Antwort
Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

+++

### Ab wann kann ich die Ergebnisse meiner [!UICONTROL Auto-Target]-Aktivität anzeigen?

+++Antwort
Sie können die Ergebnisse Ihres [!UICONTROL Auto-Target]-Tests überprüfen, nachdem Sie mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) haben, das Modelle erstellt hat.

+++

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

+++Antwort
Sie können bei der Erstellung einer [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Kann ich die Zielmetrik inmitten einer [!UICONTROL Auto-Target] ändern? {#change-metric}

+++Antwort
Adobe rät davon ab, die Zielmetrik inmitten einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. Adobe übernimmt keine Garantie dafür, was passiert, wenn Sie die Zielmetrik in einer Aktivität nach deren Ausführung ändern.

Diese Empfehlung gilt für [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

### Kann ich die Option [!UICONTROL Reset Report Data] während der Ausführung einer [!UICONTROL Auto-Target] verwenden?

+++Antwort
Die Verwendung der Option [!UICONTROL Reset Report Data] für [!UICONTROL Auto-Target] Aktivitäten wird nicht empfohlen. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem [!UICONTROL Auto-Target]. Anstatt die Option [!UICONTROL Reset Report Data] für [!UICONTROL Auto-Target] Aktivitäten zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität.

Diese Leitlinien gelten auch für [!UICONTROL Auto-Allocate] und [!UICONTROL Automated Personalization].

+++

### Was passiert, wenn ich ein einzelnes Erlebnis aus einer [!UICONTROL Auto-Target]-Aktivität entferne?

+++Antwort
[!DNL Target] erstellt für jedes Erlebnis ein eigenes Modell. Wenn Sie also ein Erlebnis entfernen, erstellt [!DNL Target] ein Modell weniger. Dies wirkt sich nicht auf die Modelle der anderen Erlebnisse aus.

Angenommen, Sie haben eine [!UICONTROL Auto-Target] Aktivität mit acht Erlebnissen, und die Performance eines dieser Erlebnisse sagt Ihnen gar nicht zu. Sie können dieses Erlebnis entfernen. Dies wirkt sich nicht auf die Modelle der sieben verbleibenden Erlebnisse aus.

+++

## Fehlerbehebung [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, mit denen Sie bei der Verwendung von [!UICONTROL Auto-Target] konfrontiert sein könnten, sowie einige Lösungsvorschläge.

### Meine [!UICONTROL Auto-Target]-Aktivität braucht zu lange, um Modelle zu erstellen.

+++Empfehlungen zur Fehlerbehebung
Es gibt mehrere Änderungen beim Einrichten von Aktivitäten, die die erwartete Zeit zum Erstellen von Modellen reduzieren können, einschließlich der Anzahl der Erlebnisse in Ihrer [!UICONTROL Auto-Target], des Traffics auf Ihrer Site und Ihrer ausgewählten Erfolgsmetrik.

**Lösung:** Überprüfen Sie die Einrichtung Ihrer Aktivität und stellen Sie fest, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf [!UICONTROL RPV] gesetzt ist, kann dann auf Konversion gewechselt werden? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die Traffic-Anforderungen, die zum Erstellen von Modellen erforderlich sind, da eine Mindestanzahl von Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an den Standorten Ihrer Aktivitäten auftreten, desto schneller können Modelle erstellt werden.

+++

### Meine [!UICONTROL Auto-Target] Aktivität erzeugt keine Steigerung.

+++Empfehlungen zur Fehlerbehebung
Es sind vier Faktoren erforderlich, damit eine [!UICONTROL Auto-Target] Aktivität eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn nicht für alle Erlebnisse Modelle erstellt wurden, übernimmt Ihre [!UICONTROL Auto-Target]-Aktivität dennoch nach dem Zufallsprinzip einen erheblichen Teil der Besuche, um zu versuchen, alle Modelle so schnell wie möglich zu erstellen. Wenn keine Modelle erstellt werden, personalisiert [!UICONTROL Auto-Target] den Traffic nicht.

Stellen Sie anschließend mithilfe eines einfachen, nicht personalisierten A/B-Tests sicher, dass die Angebote und die Aktivitäts-Speicherorte tatsächlich einen Unterschied zu den Gesamtansprechraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die Ergebnisse eines A/B-Tests eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. In der Regel liegt das Problem daran, dass die Angebote und Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

### Jede von einer Konversionsmetrik abhängige Metrik konvertiert nie.

+++Empfehlungen zur Fehlerbehebung
Dieses Ergebnis ist zu erwarten.

In einer [!UICONTROL Auto-Target] Aktivität wird der Benutzer nach der Konvertierung einer Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Post-Ziel handelt) aus dem Erlebnis entlassen und die Aktivität neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 hängt von C1 ab. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da der Besucher beim Konvertieren von C1 freigeschaltet wird.

+++
