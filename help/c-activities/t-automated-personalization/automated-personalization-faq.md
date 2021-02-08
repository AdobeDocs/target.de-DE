---
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQ;FAQ;FAQ;Automatisierte Personalisierung;Steuerung;Standarderfahrung;Best Practices
description: Hier finden Sie eine Liste häufig gestellter Fragen und Antworten zu Automated Personalization-Aktivitäten in Adobe Target.
title: Wie kann ich FAQs zu Automated Personalization-Aktivitäten finden?
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 83%

---


# ![Häufig gestellte Fragen zur ](/help/assets/premium.png) automatisierten Personalisierung

Liste häufig gestellter Fragen zur automatisierten Personalisierung (AP).

## Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

Sie können bei der Erstellung einer [automatisierten Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie im Abschnitt zur [Verwendung eines bestimmten Erlebnisses als Kontrollerlebnis](/help/c-activities/t-automated-personalization/experience-as-control.md).

## Wie kann ich automatisierte Personalisierung mit einem Standarderlebnis vergleichen? {#section_46C1A620A2384C2C8392D6716DD18495}

Es gibt keine Option, mit der sich der Vergleich von AP mit einem Standarderlebnis aktivieren lässt. Das Problem lässt sich jedoch umgehen, indem Sie in einem Standarderlebnis oder -angebot, das Teil der Gesamtaktivität ist, auf das Kontrollsegment in den Berichten klicken, um im daraufhin geöffneten Angebotsbericht die Grundleistung des Angebots oder Erlebnisses zu bestimmen. Die für dieses Angebot aufgezeichnete Konversionsrate kann dann für den Vergleich mit der Konversionsrate des gesamten Segments „Random Forest“ verwendet werden. Somit lässt sich vergleichen, welche Leistung die Maschine im Vergleich zum Standardangebot erbringt.

## Mithilfe welcher Best Practices kann ich eine Aktivität vom Typ „Automatisierte Personalisierung“ einrichten?   {#section_E155B26282BE49B58EA2683413D11DE6}

* Wenn Sie eine Seite mit geringerem Traffic personalisieren oder strukturelle Änderungen an dem Erlebnis vornehmen möchten, das Sie personalisieren, sollten Sie ggf. das automatische Targeting anstelle der automatisierten Personalisierung verwenden. Siehe  [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md).
* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Positionen ab, die Sie für Ihre Aktivität vom Typ „Automatisierte Personalisierung“ planen zu verwenden, um sicherzustellen, dass sich die Position(en) und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, ist das Generieren der Steigerung durch die automatisierte Personalisierung wahrscheinlich ebenfalls fehlerhaft.

   * Wenn ein A/B…N-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Mithilfe der  [Traffic-Schätzung](/help/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) können Sie einschätzen, wie lange es dauert, bis Personalisierungsmodelle in Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ erstellt werden.
* Legen Sie die Zuordnung zwischen dem Kontroll- und Zielgruppe fest, bevor Sie Ihre Aktivität basierend auf Ihren Zielen starten.

   Je nach dem Ziel Ihrer Aktivität und der Art der gewählten Kontrolle gibt es drei Szenarien:

   * **Zufällige Erlebnisse, wenn es Ihr Kontroll- und Aktivitätsziel ist, die Effektivität des Personalisierungsalgorithmus zu testen**: Wenn Ihr Ziel darin besteht, den Personalisierungsalgorithmus zu beurteilen, benötigen Sie eine genauere Darstellung Ihrer Steigerung. Darüber hinaus möchten Sie wahrscheinlich wissen, wie die Konversionsrate für Ihre Erlebnisse/Angebote wäre, wenn Sie einfach einen A/B-Test durchführten (eine zufällig bereitgestellte Kontrolle). In diesem Fall wird eine Zuordnung von 50 % zu einer Kontrollgruppe von zufällig bereitgestellten Erlebnissen empfohlen.
   * **Zufällige Erlebnisse, wenn es Ihr Kontroll- und Aktivitätsziel ist, personalisierten Traffic zu maximieren**: Wenn Sie mit dem Algorithmus zufrieden sind und eine maximale Menge an Traffic personalisiert haben möchten, wird eine Kontrollzuordnung von 10 % bis 30 % empfohlen. Der Nachteil hier ist die geringere Genauigkeit, die Sie in Ihren Steigerungsinformationen erhalten (die Konfidenzintervalle Ihres Kontroll-Traffics sind größer, da weniger Traffic zur Kontrollmenge geleitet wird).
   * **Als Kontrolle ein spezifisches Erlebnis mit beliebigem Ziel**: Wenn Sie ein bestimmtes Erlebnis mit den Personalisierungsmodellen vergleichen möchten, wird eine Zuordnung von 10 % bis 30 % zur Kontrolle empfohlen. Wenn Sie nur ein einziges Erlebnis als Kontrolle auswählen, wird dieser Traffic nicht über alle Angebote/Erlebnisse in der Aktivität verteilt.

* Targeting-Regeln sollten sparsam verwendet werden, da sie die Optimierungsfähigkeit des Modells beeinträchtigen können.
* Berichterstellungsgruppen können den Erfolg Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ begrenzen. Sie sollten nur unter bestimmten Bedingungen verwendet werden.

   * Verwenden Sie Berichterstellungsgruppen nur dann, wenn die folgenden Bedingungen erfüllt sind: (1) Sie planen, neue Angebote zu ersetzen/hinzuzufügen, während die Aktivität läuft, (2) die Angebote in der Berichtsgruppe zielen auf dieselben Besucher ab und (3) die Angebote in dieser Berichtsgruppe besitzen dieselbe Gesamtantwortrate.
   * Es gibt keine Personalisierung zwischen den Angeboten in einer Berichtsgruppe: Die Angebote werden durch das Personalisierungsmodell alle identisch behandelt.
   * Legen Sie niemals alle Angebote in einer Aktivität in einer einzelnen Berichtsgruppe ab. Dadurch werden alle Angebote allen Besuchern in der Aktivität einheitlich nach dem Zufallsprinzip bereitgestellt.

## Häufig gestellte Fragen  

Lesen Sie die folgenden häufig gestellten Fragen und Antworten, während Sie mit [!UICONTROL Automated Personalization]-Aktivitäten arbeiten:

### Welche Einschränkungen gibt es bei der automatisierten Personalisierung?   {#section_08BA09ED51B547299963C94FE6417CFA}

Target besitzt eine harte Begrenzung von 30.000 Erlebnissen. Bei weniger als 10.000 erstellten Erlebnissen ist die Funktionsweise jedoch am besten.

### Wie wird die Kundenansprache auf Angebotsebene implementiert?   {#section_9D7A86EA93D74E9B8C81072A681263A4}

Sobald der Besucher zur entsprechenden Position gelangt, wird der Satz der möglichen Angebote, die dem Besucher angezeigt werden, anhand der Regeln vom Typ „Kundenansprache auf Angebotsebene“ bestimmt. Anschließend wählt der Algorithmus das Angebot aus, das entsprechend der Prognose durch das Modell den besten erwarteten Umsatz oder die beste Konversionschance aufweist. Beachten Sie, dass sich das Angebots-Targeting auf die Wirksamkeit der maschinellen Lernalgorithmen von Target auswirkt und daher möglichst sparsam eingesetzt werden sollte.

### „Meine Aktivität“ zeigt keine Steigerung an. Was ist los? {#section_BFA07C8C258F45318F73A461B8F32737}

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ „Automatisierte Personalisierung“ eine Steigerung generiert:

* Die Angebote an jeder Position müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Positionen müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke in der Aktivität vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

Weitere Informationen finden Sie unter [Fehlerbehebung bei der automatisierten Personalisierung](/help/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

### Wie wird der Traffic meiner Aktivität durch die automatisierte Personalisierung zugeordnet? {#section_4369364F77804E0D9B78BEE551DA5659}

Die automatisierte Personalisierung leitet Besucher zu dem Erlebnis weiter, das die höchste prognostizierte Erfolgsmetrik basierend auf den neuesten [Random Forest](/help/c-activities/t-automated-personalization/algo-random-forest.md)-Modellen aufweist, die für die einzelnen Modelle erstellt wurden. Diese Prognose basiert auf den spezifischen Informationen des Besuchers und dem Besuchskontext.

Angenommen, eine Aktivität vom Typ „Automatisierte Personalisierung“ hatte zwei Positionen mit jeweils zwei Angeboten. An der ersten Position weist Angebot A eine prognostizierte Konversionsrate von 3 % für einen bestimmten Besucher auf, während Angebot B eine prognostizierte Konversionsrate von 1 % aufweist. An der zweiten Position weist Angebot C eine prognostizierte Konversionsrate von 2 % für denselben Besucher auf, während Angebot D eine prognostizierte Konversionsrate von 5 % aufweist. Daher würde die automatisierte Personalisierung diesem Besucher ein Erlebnis mit Angebot A und Angebot D unterbreiten.

### Wann sollte ich meine Aktivität vom Typ „Automatisierte Personalisierung“ anhalten?   {#section_C51F3DAB8887463BB147373F6FE06B93}

Die automatisierte Personalisierung kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere besteht für zeitlose Inhalte keine Notwendigkeit, Ihre Aktivität vom Typ „Automatisierte Personalisierung“ anzuhalten. Wenn Sie wesentliche Änderungen an den Inhalten vornehmen möchten, die den aktuell in Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ vorhandenen Angeboten nicht ähneln, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte anzeigen, nicht verwirrt werden oder sich auf vergangene Ergebnisse mit anderen Inhalten beziehen.

### Wie lange sollte ich warten, bis Modelle erstellt werden?   {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

Wie lange es dauert, bis Modelle in Ihrer Aktivität erstellt werden, hängt in der Regel vom Traffic Ihrer ausgewählten Aktivitätsposition(en) und Ihrer Aktivitätserfolgsmetrik ab. Verwenden Sie stattdessen die [Traffic-Schätzung](/help/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um zu bestimmen, wie lange das Erstellen von Modellen in Ihrer Aktivität erwartungsgemäß dauert.

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert? {#section_51EA953C6D1D4A3185FC9DD290D66621}

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

### Wann kann ich die Ergebnisse meiner Aktivität vom Typ „Automatisierte Personalisierung“ anzeigen?   {#section_05DB5ACAE6AD429C9510766A7268EE2C}

Sie können beginnen sich die Ergebnisse Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ anzusehen, sobald Sie mindestens über zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, die Modelle erstellt haben.

### Wie kann ich die für das Erstellen von Modellen in meiner Aktivität erforderliche Dauer reduzieren?   {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

Überprüfen Sie Ihre Aktivitätseinrichtung dahingehend, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, in der Modelle erstellt werden.

* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn die Anzahl der Erlebnisse in einer Aktivität verringert wird, wird das Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitätspositionen vorhanden sind, desto schneller werden die Modelle erstellt.

### Warum werden Besuchern Erlebnisse für eine AP-Aktivität angezeigt, die sie nicht sehen sollten? {#section_41CECEAE0881446A8D9F3B016857914B}

Aktivitäten vom Typ „Automatisierte Personalisierung“ werden einmal pro Sitzung ausgewertet. Wenn für ein bestimmtes Erlebnis qualifizierte aktive Sitzungen vorhanden waren und diesen nun neue Angebote hinzugefügt werden, wird Benutzern der neue Inhalt zusammen mit den zuvor angezeigten Angeboten angezeigt. Da sie zuvor für diese Erlebnisse qualifiziert wurden, werden sie ihnen weiterhin für die Dauer der Sitzung angezeigt. Wenn dies bei jedem einzelnen Seitenbesuch ausgewertet werden soll, sollten Sie den Erlebnis-Targeting-Aktivitätstyp (XT) ändern.

### Kann ich die Zielmetrik in der Mitte einer Automated Personalization-Aktivität ändern? {#change-metric}

Es wird nicht empfohlen, die Zielmetrik mitten in einer Aktivität zu ändern. Obwohl es möglich ist, die Zielmetrik während einer Aktivität mithilfe der [!DNL Target]-Benutzeroberfläche zu ändern, sollten Sie immer eine neue Aktivität Beginn haben. Wir garantieren nicht, was passiert, wenn Sie die Sollmetrik in einer Aktivität nach der Ausführung ändern.

Diese Empfehlung gilt für die Aktivitäten [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatische Zielgruppe] und [!UICONTROL Automated Personalization], die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichte-Quelle verwenden.

### Kann ich beim Ausführen einer Automated Personalization-Aktivität die Option Berichtsdaten zurücksetzen verwenden?

Die Verwendung der Option [!UICONTROL Berichtsdaten zurücksetzen] für [!UICONTROL Automated Personalization]-Aktivitäten wird nicht empfohlen. Obwohl die Daten des sichtbaren Berichte entfernt werden, entfernt diese Option nicht alle Schulungsdatensätze aus dem [!UICONTROL Automated Personalization]-Modell. Anstatt die Option [!UICONTROL Berichtsdaten zurücksetzen] für [!UICONTROL Automated Personalization]-Aktivitäten zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität. (Hinweis: Diese Anleitung gilt auch für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe].)

### Wie erstellt Automated Personalization Modelle in Bezug auf Umgebung?

Ein Modell wird erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic im Vergleich zum Senden des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu identifizieren. Bei diesem Modell werden Treffer und Konversionen nur in der Standard-Umgebung berücksichtigt.

Traffic aus einem zweiten Satz von Modellen wird für jede Modellgruppe (AP) oder Erlebnis (AT) erstellt. Bei jedem dieser Modelle werden Treffer und Konversionen in allen Umgebung berücksichtigt.

Anfragen werden daher unabhängig von der Umgebung mit demselben Modell bedient, aber die Datenverkehrsvielfalt sollte von der Standardeinstellung ausgehen, um sicherzustellen, dass das identifizierte, insgesamt erfolgreichste Erlebnis mit dem realen Verhalten in Einklang steht.
