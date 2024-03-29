---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung; Traffic
description: Erkunden Sie Fehlerbehebungsthemen und häufig gestellte Fragen zu [!UICONTROL Automatisches Targeting] Aktivitäten.
title: Fehlerbehebung [!UICONTROL Automatisches Targeting] Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '1925'
ht-degree: 40%

---

# [!UICONTROL Automatisches Targeting] Häufig gestellte Fragen und Fehlerbehebung

Fehlerbehebung und häufig gestellte Fragen (FAQ) zu [!UICONTROL Automatisches Targeting] Aktivitäten in [!DNL Adobe Target].

## [!UICONTROL Häufig gestellte Fragen zum automatischen Targeting] {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Konsultieren Sie bei Problemen mit [!UICONTROL automatischen Targeting]-Aktivitäten die folgenden häufig gestellten Fragen und Antworten:

### Wie lauten die Best Practices zum Einrichten einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]?

+++Antwort
* Entscheiden Sie, ob der Geschäftswert eines [!UICONTROL Umsatz pro Besuch] (RPV) Die Erfolgsmetrik ist die zusätzlichen Traffic-Anforderungen wert. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen Kontroll- und personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Bestimmen Sie, ob Sie über ausreichend Traffic für die Seite verfügen, auf der Ihre [!UICONTROL Automatisches Targeting] -Aktivität ausgeführt werden, damit Personalisierungsmodelle innerhalb einer angemessenen Zeit erstellt werden können.
* Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie keine Erlebnisse ändern oder Profilattribute hinzufügen oder entfernen, während die Aktivität aktiv ist.
* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Orten ab, die Sie in Ihrer [!UICONTROL Automatisches Targeting] -Aktivität, um sicherzustellen, dass sich die Standorte und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, [!UICONTROL Automatisches Targeting] kann wahrscheinlich auch keine Steigerung generieren.

  Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während der Aktivität keine wesentlichen Änderungen an den Erlebnissen vorzunehmen.

+++

### Does [!UICONTROL Adobe] empfiehlt die Verwendung von [!UICONTROL Automatisches Targeting] mit einer 90(Control)/10(Targeted)-Aufteilung, bis die Modelle erstellt werden?

+++Antwort Die optimale Traffic-Zuordnung hängt davon ab, was Sie erreichen möchten.

Wenn Sie so viel Traffic wie möglich personalisieren möchten, können Sie während der Lebensdauer der Aktivität an der 90-%-Zielzuordnung und der 10-%-Kontrolle festhalten. Wenn Sie ein Experiment durchführen möchten, in dem Sie vergleichen, wie personalisierte Algorithmen mit der Kontrolle funktionieren, ist eine 50/50-Aufteilung für die Lebensdauer der Aktivität am besten.

Best Practice ist es auf jeden Fall, die Aufteilung der Traffic-Zuordnung während der Lebensdauer einer Aktivität nicht zu ändern, damit die Besucher nicht zwischen Targeting- und Kontrollerlebnissen verschoben werden.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Wenn ein Besucher **not** die [!UICONTROL Automatisches Targeting] Aktivität und Konversionen, zählt die Konversion in meiner Aktivität?

++ + Antwort Nein, nur Besucher, die sich für die [!UICONTROL Automatisches Targeting] -Aktivitäten in Berichten gezählt werden.

+++

### Warum nicht meine [!UICONTROL Automatisches Targeting] -Aktivität eine Steigerung zu erzeugen.

+++Antwort Für eine [!UICONTROL Automatisches Targeting] -Aktivität zur Steigerung:

* Die Angebote müssen so unterschiedlich sein, dass sie Besucher beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die für das Optimierungsziel von Bedeutung ist.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. In der Regel ist das Problem auf die Angebote und Standorte zurückzuführen, die keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Bedeutung erkannt zu werden.

+++

### Wann sollte ich meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anhalten?

+++Antwort
[!UICONTROL Automatisches Targeting] kann als &quot;Always on&quot;-Personalisierung verwendet werden, die ständig optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzuhalten.

Wenn Sie wesentliche Änderungen am Inhalt in Ihrer [!UICONTROL Automatisches Targeting] -Aktivität verwenden, empfiehlt es sich, eine neue Aktivität zu starten, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

+++

### Wie lange sollte ich warten, bis Modelle erstellt werden? {#how-long}

+++Antwort Die Zeit, die benötigt wird, um Modelle in Ihrer [!UICONTROL Automatisches Targeting] -Aktivität hängt normalerweise vom Traffic Ihrer ausgewählten Aktivitätsstandorte und den Konversionsraten ab, die mit Ihrer Aktivitätserfolgsmetrik verknüpft sind.

[!UICONTROL Automatisches Targeting] versucht nicht, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, bis mindestens 50 Konversionen für dieses Erlebnis vorhanden sind. Wenn das erstellte Modell außerdem von unzureichender Qualität ist (bestimmt durch Offline-Auswertung von &quot;Test&quot;-Daten, wird [eine Metrik namens AUC](https://de.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), wird das Modell nicht verwendet, um Traffic auf personalisierte Weise bereitzustellen.

Darüber hinaus sind auch die folgenden Punkte bei der Modellerstellung durch [!UICONTROL automatisches Targeting] zu berücksichtigen:

* Nach der Live-Schaltung einer Aktivität [!UICONTROL Automatisches Targeting] berücksichtigt bis zu den letzten 45 Tagen zufällig bereitgestellter Daten beim Versuch, Modelle zu erstellen. So können Sie z. B. Traffic steuern und zusätzliche zufällig bereitgestellte zusätzliche Daten, die vom Algorithmus ausgegeben werden.
* Aktivitäten mit der Erfolgsmetrik [!UICONTROL Umsatz pro Besuch] benötigen in der Regel mehr Daten zum Erstellen von Modellen. Dies liegt daran, dass die Datenvarianz bei „Umsatz pro Besuch“ normalerweise höher als bei „Konversionsrate“ ist.
* Da Modelle auf Erlebnisbasis basieren, bedeutet das Ersetzen eines Erlebnisses durch ein anderes, dass ausreichend Traffic (mindestens 50 Konversionen) für das neue Erlebnis gesammelt werden muss, bevor personalisierte Modelle neu erstellt werden können.

+++

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

++ + Antwort Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung beginnt.

+++

### Wann kann ich anfangen, die Ergebnisse meiner [!UICONTROL Automatisches Targeting] Aktivität?

+++Antwort Sie können beginnen, die Ergebnisse Ihrer [!UICONTROL Automatisches Targeting] testen, nachdem Sie mindestens zwei Erlebnisse mit erstellten Modellen (grünes Häkchen) für das Erlebnis erstellt haben, für das Modelle erstellt wurden.

+++

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

+++Antwort Sie können beim Erstellen eines [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Kann ich die Zielmetrik in der Mitte durch eine [!UICONTROL Automatisches Targeting] Aktivität? {#change-metric}

++ + Antwort Adobe rät davon ab, die Zielmetrik mitten in einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. Adobe garantiert nicht, was passiert, wenn Sie die Zielmetrik in einer Aktivität ändern, nachdem sie ausgeführt wird.

Diese Empfehlung gilt gleichermaßen für [!UICONTROL automatische Zuordnungs]-, [!UICONTROL automatische Targeting]- und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

### Kann ich die [!UICONTROL Berichtsdaten zurücksetzen] -Option beim Ausführen einer [!UICONTROL Automatisches Targeting] Aktivität?

+++Antwort Verwenden der [!UICONTROL Berichtsdaten zurücksetzen] -Option für [!UICONTROL Automatisches Targeting] -Aktivitäten nicht vorgeschlagen werden. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem [!UICONTROL automatischen Targeting]-Modell. Statt für eine [!UICONTROL automatische Targeting]-Aktivität die Option [!UICONTROL Berichtsdaten zurücksetzen] zu verwenden, empfiehlt sich die Erstellung einer neuen Aktivität und die Deaktivierung der ursprünglichen Aktivität.

Diese Leitlinien gelten auch für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automated Personalization] Aktivitäten.

+++

### Was passiert, wenn ich ein einzelnes Erlebnis aus einer [!UICONTROL Automatisches Targeting] Aktivität?

+++Antwort
[!DNL Target] erstellt ein Modell pro Erlebnis, sodass das Entfernen eines Erlebnisses bedeutet [!DNL Target] erstellt ein weniger Modell und wirkt sich nicht auf Modelle für die anderen Erlebnisse aus.

Angenommen, Sie haben eine [!UICONTROL automatische Targeting]-Aktivität mit acht Erlebnissen, und die Performance eines dieser Erlebnisse sagt Ihnen gar nicht zu. Sie können dieses Erlebnis entfernen, es wirkt sich nicht auf die Modelle der sieben verbleibenden Erlebnisse aus.

+++

## Fehlerbehebung für [!UICONTROL Automatisches Targeting] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, denen Sie bei der Verwendung von [!UICONTROL Automatisches Targeting] und einige Lösungsvorschläge.

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] braucht zu lange, um Modelle zu erstellen.

+++ Empfehlungen zur Fehlerbehebung Es gibt verschiedene Aktivitätseinrichtungsänderungen, die die erwartete Zeit zum Erstellen von Modellen verringern können, einschließlich der Anzahl der Erlebnisse in Ihren [!UICONTROL Automatisches Targeting] Aktivität, den Traffic zu Ihrer Site und Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung und sehen Sie, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu erhöhen, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf [!UICONTROL RPV]können Sie zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die für die Erstellung von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl von Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen in Ihren Aktivitätsstandorten vorhanden sind, desto schneller werden Modelle erstellt.

+++

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] generiert keine Steigerung.

+++Empfehlungen zur Fehlerbehebung Es sind vier Faktoren erforderlich für eine [!UICONTROL Automatisches Targeting] -Aktivität zur Steigerung:

* Die Angebote müssen so unterschiedlich sein, dass sie Besucher beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die für das Optimierungsziel von Bedeutung ist.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn die Modelle nicht für alle Erlebnisse erstellt sind, verarbeitet Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] weiterhin zufallsbasiert einen signifikanten Teil an Besuchen, um zu versuchen, alle Modelle schnellstmöglich zu erstellen. Ohne erstellte Modelle wird der Traffic mit [!UICONTROL Automatisches Targeting] nicht personalisiert.

Stellen Sie als Nächstes mithilfe eines einfachen, nicht personalisierten A/B-Tests sicher, dass die Angebote und die Aktivitätsstandorte wirklich einen Unterschied zu den Gesamt-Reaktionsraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die Ergebnisse eines A/B-Tests eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, funktioniert eine personalisierte Aktivität wahrscheinlich. Personalisierung kann auch dann funktionieren, wenn es keine Unterschiede in den Gesamt-Antwortraten der Erlebnisse gibt. In der Regel ist das Problem auf die Angebote und Standorte zurückzuführen, die keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Bedeutung erkannt zu werden.

+++

### Metriken, die von einer Konversionsmetrik abhängig sind, werden nicht konvertiert.

++ + Vorschläge zur Fehlerbehebung Dies ist zu erwarten.

In einer [!UICONTROL Automatisches Targeting] Aktivität, sobald eine Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Nachziel handelt) konvertiert wurde, wird der Benutzer aus dem Erlebnis freigesetzt und die Aktivität wird neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist von C1 abhängig. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 konvertiert und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da bei der Konvertierung von C1 der Besucher freigegeben wird.

+++
