---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung; Traffic
description: Erfahren Sie mehr über Fehlerbehebungsthemen und häufig gestellte Fragen zu [!UICONTROL Auto-Target] -Aktivitäten.
title: Wie kann ich eine Fehlerbehebung für [!UICONTROL Auto-Target] -Aktivitäten durchführen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 29%

---

# [!UICONTROL Auto-Target] FAQs und Fehlerbehebung

Fehlerbehebung und häufig gestellte Fragen (FAQs) zu [!UICONTROL Auto-Target] -Aktivitäten in [!DNL Adobe Target].

## [!UICONTROL Auto-Target] Häufig gestellte Fragen {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Lesen Sie bei der Arbeit mit [!UICONTROL Auto-Target] -Aktivitäten die folgenden häufig gestellten Fragen und Antworten:

### Was sind die Best Practices zum Einrichten einer [!UICONTROL Auto-Target] -Aktivität?

+++Antwort
* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik vom Typ [!UICONTROL Revenue per Visit] (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen Kontroll- und personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Bestimmen Sie, ob Sie über ausreichend Traffic für die Seite verfügen, auf der Ihre [!UICONTROL Auto-Target] -Aktivität ausgeführt wird, damit Personalisierungsmodelle in einer angemessenen Zeit erstellt werden können.
* Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie keine Erlebnisse ändern oder Profilattribute hinzufügen oder entfernen, während die Aktivität aktiv ist.
* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Orten ab, die Sie für Ihre [!UICONTROL Auto-Target] -Aktivität verwenden möchten, um sicherzustellen, dass sich die Orte und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, kann [!UICONTROL Auto-Target] wahrscheinlich auch keine Steigerung generieren.

  Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während der Aktivität keine wesentlichen Änderungen an den Erlebnissen vorzunehmen.

+++

### Empfiehlt [!UICONTROL Adobe] die Verwendung von [!UICONTROL Auto Target] mit einer 90(Control)/10(Targeted)-Aufteilung, bis die Modelle erstellt wurden?

+++Antwort
Die optimale Aufteilung der Traffic-Zuordnung hängt davon ab, was Sie erreichen möchten.

Wenn Sie so viel Traffic wie möglich personalisieren möchten, können Sie während der Lebensdauer der Aktivität an der 90-%-Zielzuordnung und der 10-%-Kontrolle festhalten. Wenn Sie ein Experiment durchführen möchten, in dem Sie vergleichen, wie personalisierte Algorithmen mit der Kontrolle funktionieren, ist eine 50/50-Aufteilung für die Lebensdauer der Aktivität am besten.

Best Practice ist es auf jeden Fall, die Aufteilung der Traffic-Zuordnung während der Lebensdauer einer Aktivität nicht zu ändern, damit die Besucher nicht zwischen Targeting- und Kontrollerlebnissen verschoben werden.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Wenn ein Besucher **nicht** die [!UICONTROL Auto-Target] -Aktivität sieht und konvertiert, zählt dann die Konversion in meiner Aktivität?

+++Antwort
Nein, nur Besucher, die sich für die [!UICONTROL Auto-Target] -Aktivität qualifizieren und diese anzeigen, werden in der Berichterstellung gezählt.

+++

### Warum generiert meine [!UICONTROL Auto-Target] -Aktivität anscheinend keine Steigerung.

+++Antwort
Es sind vier Faktoren erforderlich, damit eine [!UICONTROL Auto-Target] -Aktivität eine Steigerung generiert:

* Die Angebote müssen so unterschiedlich sein, dass sie Besucher beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die für das Optimierungsziel von Bedeutung ist.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. In der Regel ist das Problem auf die Angebote und Standorte zurückzuführen, die keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Bedeutung erkannt zu werden.

+++

### Wann sollte ich meine [!UICONTROL Auto-Target] -Aktivität stoppen?

+++Antwort
[!UICONTROL Auto-Target] kann als &quot;Always on&quot;-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte müssen Sie Ihre [!UICONTROL Auto-Target] -Aktivität nicht stoppen.

Wenn Sie wesentliche Änderungen am Inhalt Ihrer [!UICONTROL Auto-Target] -Aktivität vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu starten, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

+++

### Wie lange sollte ich warten, bis Modelle erstellt werden? {#how-long}

+++Antwort
Wie lange es dauert, bis in Ihrer [!UICONTROL Auto-Target] -Aktivität Modelle erstellt werden, hängt normalerweise vom Traffic Ihrer ausgewählten Aktivitätsstandorte und den Konversionsraten ab, die mit Ihrer Aktivitätserfolgsmetrik verknüpft sind.

[!UICONTROL Auto-Target] versucht nicht, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, bis mindestens 50 Konversionen für dieses Erlebnis vorhanden sind. Darüber hinaus wird das Modell nicht verwendet, um Traffic auf personalisierte Weise bereitzustellen, wenn das erstellte Modell von unzureichender Qualität ist (was durch die Offline-Auswertung von &quot;Test&quot;-Daten unter Verwendung von [einer Metrik namens AUC](https://de.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve) ermittelt wird).

Einige weitere Punkte, die Sie bezüglich der Modellerstellung von [!UICONTROL Auto-Target] beachten sollten:

* Nachdem eine Aktivität live ist, berücksichtigt [!UICONTROL Auto-Target] beim Erstellen von Modellen bis zu den letzten 45 Tagen zufällig bereitgestellter Daten. So können Sie z. B. Traffic steuern und zusätzliche zufällig bereitgestellte zusätzliche Daten, die vom Algorithmus ausgegeben werden.
* Wenn [!UICONTROL Revenue per Visit] Ihre Erfolgsmetrik ist, erfordern diese Aktivitäten aufgrund der höheren Datenvarianz, die normalerweise im Besuchsumsatz im Vergleich zur Konversionsrate vorhanden ist, normalerweise mehr Daten zum Erstellen von Modellen.
* Da Modelle auf Erlebnisbasis basieren, bedeutet das Ersetzen eines Erlebnisses durch ein anderes, dass ausreichend Traffic (mindestens 50 Konversionen) für das neue Erlebnis gesammelt werden muss, bevor personalisierte Modelle neu erstellt werden können.

+++

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

+++Antwort
Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung beginnt.

+++

### Wann kann ich mit der Untersuchung der Ergebnisse meiner [!UICONTROL Auto-Target] -Aktivität beginnen?

+++Antwort
Sie können die Ergebnisse Ihres [!UICONTROL Auto-Target]-Tests überprüfen, nachdem Sie mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) erstellt haben, die Modelle erstellt haben.

+++

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

+++Antwort
Sie können beim Erstellen einer [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP)- oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT)-Aktivität ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Kann ich die Zielmetrik in der Mitte durch eine [!UICONTROL Auto-Target] -Aktivität ändern? {#change-metric}

+++Antwort
Adobe rät davon ab, die Zielmetrik während einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. Adobe garantiert nicht, was passiert, wenn Sie die Zielmetrik in einer Aktivität ändern, nachdem sie ausgeführt wird.

Diese Empfehlung gilt für [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten, die entweder [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

### Kann ich die Option [!UICONTROL Reset Report Data] beim Ausführen einer [!UICONTROL Auto-Target] -Aktivität verwenden?

+++Antwort
Die Verwendung der Option [!UICONTROL Reset Report Data] für [!UICONTROL Auto-Target] -Aktivitäten wird nicht empfohlen. Obwohl die sichtbaren Berichtsdaten entfernt werden, werden mit dieser Option nicht alle Trainings-Datensätze aus dem Modell [!UICONTROL Auto-Target] entfernt. Anstatt die Option [!UICONTROL Reset Report Data] für [!UICONTROL Auto-Target] -Aktivitäten zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität.

Diese Anleitung gilt auch für [!UICONTROL Auto-Allocate] - und [!UICONTROL Automated Personalization] -Aktivitäten.

+++

### Was passiert, wenn ich ein einzelnes Erlebnis aus einer [!UICONTROL Auto-Target] -Aktivität entferne?

+++Antwort
[!DNL Target] erstellt ein Modell pro Erlebnis. Wenn Sie also ein Erlebnis entfernen, wird durch [!DNL Target] ein Modell mit einer geringeren Anzahl erstellt und die Modelle für die anderen Erlebnisse werden nicht beeinflusst.

Angenommen, Sie haben eine [!UICONTROL Auto-Target] -Aktivität mit acht Erlebnissen und Sie mögen die Leistung eines Erlebnisses nicht. Sie können dieses Erlebnis entfernen, es wirkt sich nicht auf die Modelle der sieben verbleibenden Erlebnisse aus.

+++

## Fehlerbehebung [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, die bei der Verwendung von [!UICONTROL Auto-Target] auftreten können, sowie einige empfohlene Lösungen.

### Meine [!UICONTROL Auto-Target] -Aktivität braucht zu lange, um Modelle zu erstellen.

+++ Empfehlungen zur Fehlerbehebung
Es gibt verschiedene Aktivitätseinrichtungsänderungen, die die erwartete Zeit zum Erstellen von Modellen verringern können, darunter die Anzahl der Erlebnisse in Ihrer [!UICONTROL Auto-Target] -Aktivität, der Traffic auf Ihrer Site und Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung und sehen Sie, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf [!UICONTROL RPV] gesetzt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die für die Erstellung von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl von Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen in Ihren Aktivitätsstandorten vorhanden sind, desto schneller werden Modelle erstellt.

+++

### Meine [!UICONTROL Auto-Target] -Aktivität generiert keine Steigerung.

+++ Empfehlungen zur Fehlerbehebung
Es sind vier Faktoren erforderlich, damit eine [!UICONTROL Auto-Target] -Aktivität eine Steigerung generiert:

* Die Angebote müssen so unterschiedlich sein, dass sie Besucher beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die für das Optimierungsziel von Bedeutung ist.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn Modelle nicht für alle Erlebnisse erstellt wurden, beliefert Ihre [!UICONTROL Auto-Target] -Aktivität weiterhin zufällig einen signifikanten Teil der Besuche, um zu versuchen, alle Modelle schnellstmöglich zu erstellen. Wenn keine Modelle erstellt wurden, personalisiert [!UICONTROL Auto-Target] den Traffic nicht.

Stellen Sie als Nächstes mithilfe eines einfachen, nicht personalisierten A/B-Tests sicher, dass die Angebote und die Aktivitätsstandorte wirklich einen Unterschied zu den Gesamt-Reaktionsraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die Ergebnisse eines A/B-Tests eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, funktioniert eine personalisierte Aktivität wahrscheinlich. Personalization kann auch dann funktionieren, wenn es keine Unterschiede bei den Gesamt-Antwortraten der Erlebnisse gibt. In der Regel ist das Problem auf die Angebote und Standorte zurückzuführen, die keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Bedeutung erkannt zu werden.

+++

### Metriken, die von einer Konversionsmetrik abhängig sind, werden nicht konvertiert.

+++ Empfehlungen zur Fehlerbehebung
Dies ist zu erwarten.

Sobald in einer [!UICONTROL Auto-Target] -Aktivität eine Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Nachziel handelt) konvertiert wurde, wird der Benutzer aus dem Erlebnis freigesetzt und die Aktivität wird neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist von C1 abhängig. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 konvertiert und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da bei der Konvertierung von C1 der Besucher freigegeben wird.

+++
