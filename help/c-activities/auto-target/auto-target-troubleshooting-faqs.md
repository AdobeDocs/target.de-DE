---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting;traffic
description: Fehlerbehebung und häufig gestellte Fragen zur automatischen Zielgruppe in Adobe Target.
title: Fehlerbehebung bei automatischer Zielgruppe und häufig gestellte Fragen
feature: auto-target
translation-type: tm+mt
source-git-commit: 4fcf2a799f24e9963b0790a6b90c448f369d3ea2
workflow-type: tm+mt
source-wordcount: '1830'
ht-degree: 71%

---


# ![PREMIUM](/help/assets/premium.png) Auto-Zielgruppe - Fehlerbehebung und häufig gestellte Fragen

Fehlerbehebung und häufig gestellte Fragen (FAQs) zur [!UICONTROL automatischen Zielgruppe] in [!DNL Adobe Target].

## Häufig gestellte Fragen zum automatischen Targeting {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Lesen Sie die folgenden häufig gestellten Fragen und Antworten, während Sie mit Aktivitäten der [!UICONTROL automatischen Zielgruppe] arbeiten:

### Wie lauten die Best Practices zum Einrichten einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]?

* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik vom Typ „Umsatz pro Besuch“ (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen der Kontrolle und den personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Ermitteln Sie, ob Sie über ausreichend Traffic für die Seite verfügen, auf der Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] in einer angemessenen Dauer für zu erstellende Personalisierungsmodelle ausgeführt wird.
   * Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie weder Erlebnisse ändern noch Profilattribute hinzufügen/entfernen, während die Aktivität aktiv ist.

* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Positionen ab, die Sie für Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] verwenden möchten, um sicherzustellen, dass sich die Position(en) und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, kommt es wahrscheinlich auch nicht zu einer Steigerung durch [!UICONTROL Automatisches Targeting].

   * Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während des Aktivitätsverlaufs wesentliche Änderungen an den Erlebnissen vorzunehmen.

### Empfehlen Sie, die automatische Zielgruppe mit einer 90(Control)/10(Targeting)-Aufteilung zu verwenden, bis die Modelle erstellt wurden?

Die optimale Aufteilung der Traffic-Zuordnung hängt davon ab, was Sie erreichen möchten.

Wenn Ihr Ziel darin besteht, so viel Traffic wie möglich zu personalisieren, können Sie während der gesamten Lebensdauer der Aktivität mit 90 % Targeting und 10 % Kontrolle arbeiten. Wenn Ihr Ziel darin besteht, ein Experiment durchzuführen, bei dem Sie vergleichen, wie gut personalisierte Algorithmen im Vergleich zur Steuerung funktionieren, dann ist eine Aufteilung von 50/50 für die gesamte Lebensdauer der Aktivität am besten geeignet.

Best Practice ist, die Traffic-Zuordnung während der gesamten Lebensdauer der Aktivität aufzuteilen, damit Besucher nicht zwischen zielgerichteten Erlebnissen und Kontrollerlebnissen wechseln.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

### Wenn ein Besucher die Aktivität vom Typ [!UICONTROL Automatisches Targeting] NICHT sieht und konvertiert, zählt dann die Konversion dann in meiner Aktivität?

Nein, es werden nur die Besucher im Bericht gezählt, die sich für die Aktivität vom Typ [!UICONTROL Automatisches Targeting] qualifizieren und sie anzeigen.

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] generiert offenbar keine Steigerung. Was ist los?  

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automatisierte Personalisierung] eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

### Wann sollte ich meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anhalten?

[!UICONTROL „Automatisches Targeting“] kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzuhalten.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

### Wie lange sollte ich warten, bis Modelle erstellt werden?  {#how-long}

The length of time it takes for models to build in your [!UICONTROL Auto-Target] activity typically depends on the traffic to your selected activity location(s) and conversion rates associated with you activity success metric.

[!UICONTROL Die automatische Zielgruppe] versucht nicht, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, bis mindestens 50 Konvertierungen für dieses Erlebnis vorhanden sind. Wenn das erstellte Modell von unzureichender Qualität ist (was durch die Offline-Auswertung der &quot;Test&quot;-Daten unter Verwendung [einer Metrik, AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)genannt, bestimmt wird), wird das Modell nicht dazu verwendet, Traffic auf eine personalisierte Weise zu liefern.

Einige weitere Punkte, die im Zusammenhang mit der Modellerstellung der [!UICONTROL Auto-Zielgruppe]zu beachten sind:

* Sobald eine Aktivität live ist, berücksichtigt die [!UICONTROL automatische Zielgruppe] bis zu den letzten 45 Tagen zufällig bereiteter Daten, wenn versucht wird, Modelle zu erstellen (d. h. den Traffic zu steuern, sowie einige extra zufällig bereitgestellte Daten, die von unserem Algorithmus bereitgestellt werden).
* Wenn [!UICONTROL Umsatz pro Besuch] Ihre Erfolgsmetrik ist, benötigen diese Aktivitäten in der Regel mehr Daten, um Modelle zu erstellen, da die Datenabweichung, die normalerweise im Besuchsumsatz im Vergleich zu Konversionsrat besteht, höher ist.
* Da Modelle auf der Grundlage der einzelnen Erlebnisse erstellt werden, müssen beim Ersetzen eines Erlebnisses durch ein anderes ausreichend Traffic (d. h. mindestens 50 Konversionen) für das neue Erlebnis gesammelt werden, bevor personalisierte Modelle neu erstellt werden können.

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?  

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

### Ab wann kann ich die Ergebnisse meiner Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen?

Sie können die Ergebnisse Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen, sobald Sie über mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, die Modelle erstellt haben.

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

Sie können bei der Erstellung einer [automatisierten Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/c-activities/t-automated-personalization/experience-as-control.md).

### Kann ich die Zielmetrik in der Mitte durch eine Auto-Zielgruppe-Aktivität ändern? {#change-metric}

Es wird nicht empfohlen, die Zielmetrik mitten in einer Aktivität zu ändern. Obwohl die Zielmetrik während einer Aktivität mithilfe der [!DNL Target] Benutzeroberfläche geändert werden kann, sollten Sie immer eine neue Aktivität Beginn haben. Wir garantieren nicht, was passiert, wenn Sie die Sollmetrik in einer Aktivität nach der Ausführung ändern.

Diese Empfehlung gilt für [!UICONTROL Aktivitäten mit automatisierter Zuordnung], [!UICONTROL automatischer Zielgruppe]und [!UICONTROL Automated Personalization] , die entweder [!DNL Target] oder [!DNL Analytics] (A4T) als Berichte verwenden.

### Kann ich die Option &quot;Berichtsdaten zurücksetzen&quot;beim Ausführen einer Aktivität für die automatische Zielgruppe verwenden?

Die Verwendung der Option [!UICONTROL Berichtsdaten] zurücksetzen für Aktivitäten mit [!UICONTROL automatischer Zielgruppe] wird nicht empfohlen. Obwohl die Daten des sichtbaren Berichte entfernt werden, entfernt diese Option nicht alle Schulungsdatensätze aus dem [!UICONTROL Modell der automatischen Zielgruppe] . Anstatt die Option Berichtsdaten [!UICONTROL zurücksetzen] für Aktivitäten mit [!UICONTROL automatischer Zielgruppe] zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität. (Hinweis: Diese Anleitung gilt auch für [!UICONTROL Aktivitäten mit automatisierter Zuordnung] und [!UICONTROL Automated Personalization] .)

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

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ „Automatisierte Personalisierung“ eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn die Modelle nicht für alle Erlebnisse erstellt sind, verarbeitet Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] weiterhin zufallsbasiert einen signifikanten Teil an Besuchen, um zu versuchen, alle Modelle schnellstmöglich zu erstellen. Ohne erstellte Modelle wird der Traffic mit [!UICONTROL Automatisches Targeting] nicht personalisiert.

Stellen Sie als Nächstes mithilfe eines nicht personalisierten A/B-Tests sicher, dass die Angebote und Aktivitätspositionen wirklich einen Unterschied für die Gesamtantwortraten ausmachen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

### Die von einer Konversionsmetrik abhängigen Metriken werden nicht konvertiert. 

Dieses Ergebnis ist zu erwarten.

Bei einer Aktivität vom Typ [!UICONTROL Automatisches Targeting] wird der Benutzer von dem Erlebnis abgekoppelt und die Aktivität neu gestartet, sobald eine Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder nachgelegenes Ziel handelt) konvertiert wurde.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist abhängig von C1. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 konvertiert und erst danach A1, wird A1 auch dann nicht konvertiert, da der Besucher abgekoppelt wird, sobald C1 konvertiert ist.
