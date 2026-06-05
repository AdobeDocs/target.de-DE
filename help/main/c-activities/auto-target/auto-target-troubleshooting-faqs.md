---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung; Traffic
description: Erfahren Sie mehr über Fehlerbehebungsthemen und häufig gestellte Fragen zu [!UICONTROL automatischen Targeting]-Aktivitäten.
title: Wie kann ich Fehler bei Aktivitäten [!UICONTROL &#x200B; automatisches Targeting &#x200B;]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
TQID: https://experienceleague.adobe.com/LXOa1Ma0y8VbncCPN1Az33p-GDsd-bW-BDqJjSGbVQU
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1982
ht-degree: 30%

---

# [!UICONTROL Automatisches Targeting] häufig gestellte Fragen und Fehlerbehebung

Fehlerbehebung und häufig gestellte Fragen (FAQs) zu [!UICONTROL automatischen Targeting]-Aktivitäten in [!DNL Adobe Target].

## [!UICONTROL Automatisches Targeting] Häufig gestellte Fragen {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Konsultieren Sie bei Problemen mit automatischen Targeting[!UICONTROL -Aktivitäten die folgenden häufig gestellten Fragen &#x200B;] Antworten:

### Wie lauten die Best Practices zum Einrichten einer [!UICONTROL automatischen Targeting]-Aktivität?

+++Antwort
* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik [!UICONTROL Umsatz pro Besuch] (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen Kontroll- und personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Stellen Sie fest, ob ausreichend Traffic zu der Seite vorhanden ist, auf der Ihre [!UICONTROL Automatisches Targeting]-Aktivität ausgeführt wird, damit Personalisierungsmodelle in angemessener Zeit erstellt werden können.
* Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie während der Live-Aktivität keine Erlebnisse ändern oder Profilattribute hinzufügen oder entfernen.
* Erwägen Sie, eine A/B-Aktivität zwischen den Angeboten und Standorten durchzuführen, die Sie in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] verwenden möchten, um sicherzustellen, dass die Standorte und Angebote Auswirkungen auf das Optimierungsziel haben. Wenn in einer A/B-Aktivität kein signifikanter Unterschied nachgewiesen wird[!UICONTROL &#x200B; generiert &#x200B;]Automatisches Targeting“ wahrscheinlich auch keine Steigerung.

  Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während der Aktivität keine wesentlichen Änderungen an den Erlebnissen vorzunehmen.

+++

### Empfiehlt [!UICONTROL Adobe] die Verwendung von [!UICONTROL Automatisches Targeting] mit einer Aufteilung von 90 (Kontrolle) zu 10 (Targeting), bis die Modelle erstellt werden?

+++Antwort 
Wie Ihre optimale Aufteilung der Traffic-Zuordnung aussieht, hängt davon ab, was Sie erreichen möchten.

Wenn es Ihr Ziel ist, so viel Traffic wie möglich zu personalisieren, können Sie während der Lebensdauer der Aktivität bei der zielgerichteten Zuordnung von 90 % und der Kontrolle von 10 % bleiben. Wenn Sie ein Experiment durchführen möchten, in dem die Leistung personalisierter Algorithmen mit der Kontrolle verglichen wird, empfiehlt sich während der Lebensdauer der Aktivität eine Aufteilung von 50/50.

Best Practice ist es auf jeden Fall, die Aufteilung der Traffic-Zuordnung während der Lebensdauer einer Aktivität nicht zu ändern, damit die Besucher nicht zwischen Targeting- und Kontrollerlebnissen verschoben werden.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Wenn ein Besucher **nicht** die Aktivität vom Typ [!UICONTROL Automatisches Targeting] sieht und konvertiert, zählt dann die Konversion in meiner Aktivität?

+++Antwort
Nein, es werden nur die Besucher im Bericht gezählt, die sich für die Aktivität [!UICONTROL Automatisches Targeting] qualifizieren und sie anzeigen.

+++

### Warum generiert meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anscheinend keine Steigerung.

+++Antwort
Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automatisches Targeting] eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. In der Regel liegt das Problem daran, dass die Angebote und Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

### Wann sollte ich meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anhalten?

+++Antwort
[!UICONTROL Automatisches Targeting] kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzuhalten.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

+++

### Wie lange sollte ich warten, bis Modelle erstellt werden? {#how-long}

+++Antwort
Die Zeit, die zum Erstellen von Modellen in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] benötigt wird, hängt in der Regel vom Traffic an den ausgewählten Aktivitätsspeicherorten und den Konversionsraten ab, die mit Ihrer Erfolgsmetrik für die Aktivität verknüpft sind.

[!UICONTROL Automatisches Targeting] versucht erst dann, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, wenn mindestens 50 Konversionen für dieses Erlebnis vorhanden sind. Außerdem wird das Modell nicht zur personalisierten Bereitstellung von Traffic verwendet, wenn die Qualität des erstellten Modells unzureichend ist (die Qualität wird durch Offline-Auswertung vorgehaltener „Test“-Daten mithilfe [einer Metrik namens AUC](https://de.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve) bestimmt).

Darüber hinaus sind auch die folgenden Punkte bei [!UICONTROL &#x200B; Modellerstellung &#x200B;] automatischen Targetings zu berücksichtigen:

* Nachdem eine Aktivität live ist[!UICONTROL &#x200B; berücksichtigt „Automatisches Targeting] beim Versuch, Modelle zu erstellen, die zufällig bereitgestellten Daten der letzten 45 Tage. Beispielsweise Kontroll-Traffic sowie einige zusätzliche, zufällig bereitgestellte Daten, die vom Algorithmus vorgehalten werden.
* Wenn [!UICONTROL Umsatz pro Besuch] Ihre Erfolgsmetrik ist, benötigen diese Aktivitäten in der Regel mehr Daten zum Erstellen von Modellen. Dies liegt daran, dass die Datenvarianz bei „Umsatz pro Besuch“ normalerweise höher als bei „Konversionsrate“ ist.
* Da Modelle für einzelne Erlebnisse erstellt werden, bedeutet der Austausch eines Erlebnisses durch ein anderes, dass für das neue Erlebnis ausreichend Traffic (mindestens 50 Konversionen) erfasst werden muss, bevor das personalisierte Modell neu erstellt werden kann.

+++

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

+++Antwort
Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

+++

### Ab wann kann ich die Ergebnisse meiner Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen?

+++Antwort
Sie können die Ergebnisse Ihres Tests für [!UICONTROL Automatisches Targeting] anzeigen, sobald Sie über mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, für das Modelle erstellt wurden.

+++

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

+++Antwort
Sie können bei der Erstellung einer [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Kann ich die Zielmetrik inmitten einer automatischen Targeting[!UICONTROL Aktivität &#x200B;]? {#change-metric}

+++Antwort
Adobe rät davon ab, die Zielmetrik inmitten einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. Adobe übernimmt keine Garantie dafür, was passiert, wenn Sie die Zielmetrik in einer Aktivität nach deren Ausführung ändern.

Diese Empfehlung gilt für [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

### Kann ich die Option [!UICONTROL Berichtsdaten zurücksetzen] während ich eine Aktivität vom Typ [!UICONTROL Automatisches Targeting] ausführe?

+++Antwort
Die Verwendung [!UICONTROL &#x200B; Option „Berichtsdaten zurücksetzen] für [!UICONTROL Automatisches Targeting]-Aktivitäten wird nicht empfohlen. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem Modell [!UICONTROL Automatisches Targeting]. Statt für Aktivitäten vom Typ [!UICONTROL Berichtsdaten zurücksetzen] die Option [!UICONTROL Automatisches Targeting] zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität.

Diese Anleitung gilt auch für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automated Personalization]-Aktivitäten.

+++

### Was passiert, wenn ich ein einzelnes Erlebnis aus einer Aktivität vom Typ [!UICONTROL Automatisches Targeting] entferne?

+++Antwort
[!DNL Target] erstellt für jedes Erlebnis ein eigenes Modell. Wenn Sie also ein Erlebnis entfernen, erstellt [!DNL Target] ein Modell weniger. Dies wirkt sich nicht auf die Modelle der anderen Erlebnisse aus.

Angenommen, Sie haben eine [!UICONTROL Automatisches Targeting]-Aktivität mit acht Erlebnissen, und die Performance eines dieser Erlebnisse sagt Ihnen gar nicht zu. Sie können dieses Erlebnis entfernen. Dies wirkt sich nicht auf die Modelle der sieben verbleibenden Erlebnisse aus.

+++

## Fehlerbehebung [!UICONTROL Automatisches Targeting] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen bei der Verwendung von [!UICONTROL Automatisches Targeting] sowie einige Lösungsvorschläge.

### Meine [!UICONTROL Automatisches Targeting]-Aktivität dauert zu lange, um Modelle zu erstellen.

+++Empfehlungen zur Fehlerbehebung
Es gibt mehrere Änderungen beim Einrichten von Aktivitäten, die die erwartete Zeit zum Erstellen von Modellen reduzieren können, einschließlich der Anzahl der Erlebnisse in Ihrer [!UICONTROL automatischen Targeting]-Aktivität, des Traffics auf Ihrer Site und Ihrer ausgewählten Erfolgsmetrik.

**Lösung:** Überprüfen Sie die Einrichtung Ihrer Aktivität und stellen Sie fest, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf [!UICONTROL RPV] eingestellt ist, können Sie zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die Traffic-Anforderungen, die zum Erstellen von Modellen erforderlich sind, da eine Mindestanzahl von Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an den Standorten Ihrer Aktivitäten auftreten, desto schneller können Modelle erstellt werden.

+++

### Meine [!UICONTROL Automatisches Targeting]-Aktivität generiert keine Steigerung.

+++Empfehlungen zur Fehlerbehebung
Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automatisches Targeting] eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn nicht für alle Erlebnisse Modelle erstellt wurden,  Ihre Aktivität vom Typ „Automatisches Targeting nach wie vor einen erheblichen Teil der Besuche aus, um zu versuchen, alle Modelle so schnell wie möglich zu erstellen. Wenn keine Modelle erstellt werden, personalisiert [!UICONTROL automatisches &#x200B;]) den Traffic nicht.

Stellen Sie anschließend mithilfe eines einfachen, nicht personalisierten A/B-Tests sicher, dass die Angebote und die Aktivitäts-Speicherorte tatsächlich einen Unterschied zu den Gesamtansprechraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die Ergebnisse eines A/B-Tests eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. In der Regel liegt das Problem daran, dass die Angebote und Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

### Jede von einer Konversionsmetrik abhängige Metrik konvertiert nie.

+++Empfehlungen zur Fehlerbehebung
Dieses Ergebnis ist zu erwarten.

In einer [!UICONTROL automatischen Targeting]-Aktivität wird der Benutzer nach der Konvertierung einer Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Post-Ziel handelt) aus dem Erlebnis entlassen und die Aktivität neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 hängt von C1 ab. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da der Besucher beim Konvertieren von C1 freigeschaltet wird.

+++
