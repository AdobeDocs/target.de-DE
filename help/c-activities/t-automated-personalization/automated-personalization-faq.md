---
description: Liste häufig gestellter Fragen zur automatisierten Personalisierung (AP).
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQs;automatisierte Personalisierung
seo-description: Liste häufig gestellter Fragen zur automatisierten Personalisierung (AP).
seo-title: Häufig gestellte Fragen zur automatisierten Personalisierung
solution: Target
title: Häufig gestellte Fragen zur automatisierten Personalisierung
title-outputclass: Premium
topic: Premium
uuid: 4c8aadd3-75c3-4388-b838-e62576dfb955
badge: Premium
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# ![PREMIUM](/help/assets/premium.png) Häufig gestellte Fragen zur automatisierten Personalisierung{#automated-personalization-faq}

Liste häufig gestellter Fragen zur automatisierten Personalisierung (AP).

## Kann ich ein spezifisches Erlebnis angeben, das als Steuerelement verwendet werden soll?

You can select an experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern.

For more information, see [Use a specific experience as control](/help/c-activities/t-automated-personalization/experience-as-control.md).

## Wie kann ich automatisierte Personalisierung mit einem Standarderlebnis vergleichen? {#section_46C1A620A2384C2C8392D6716DD18495}

Es gibt keine Option, mit der sich der Vergleich von AP mit einem Standarderlebnis aktivieren lässt. Das Problem lässt sich jedoch umgehen, indem Sie in einem Standarderlebnis oder -angebot, das Teil der Gesamtaktivität ist, auf das Kontrollsegment in den Berichten klicken, um im daraufhin geöffneten Angebotsbericht die Grundleistung des Angebots oder Erlebnisses zu bestimmen. Die für dieses Angebot aufgezeichnete Konversionsrate kann dann für den Vergleich mit der Konversionsrate des gesamten Segments „Random Forest“ verwendet werden. Somit lässt sich vergleichen, welche Leistung die Maschine im Vergleich zum Standardangebot erbringt.

## Mithilfe welcher Best Practices kann ich eine Aktivität vom Typ „Automatisierte Personalisierung“ einrichten? {#section_E155B26282BE49B58EA2683413D11DE6}

* Wenn Sie eine Seite mit geringerem Traffic personalisieren oder strukturelle Änderungen an dem Erlebnis vornehmen möchten, das Sie personalisieren, sollten Sie ggf. das automatische Targeting anstelle der automatisierten Personalisierung verwenden. Siehe [Automatisches Targeting für personalisierte Erlebnisse](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).
* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Positionen ab, die Sie für Ihre Aktivität vom Typ „Automatisierte Personalisierung“ planen zu verwenden, um sicherzustellen, dass sich die Position(en) und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, ist das Generieren der Steigerung durch die automatisierte Personalisierung wahrscheinlich ebenfalls fehlerhaft.

   * Wenn ein A/B…N-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Mithilfe der [Traffic-Schätzung](../../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) können Sie einschätzen, wie lange es dauert, bis Personalisierungsmodelle in Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ erstellt werden.
* Legen Sie die Zuordnung zwischen der Kontrolle und dem Ziel fest, bevor Sie Ihre Aktivität auf Basis Ihrer Ziele beginnen.

   Es gibt drei Szenarien, die je nach Ziel Ihrer Aktivität und der Art der ausgewählten Kontrolle berücksichtigt werden sollten:

   * **Zufällige Erlebnisse als Ihre Kontrolle und Ihr Aktivitätsziel sollen die Effektivität des Personalisierungs-Algorithmus testen**: Wenn Ihr Ziel darin besteht, den Personalisierungs-Algorithmus auszuwerten, möchten Sie ein genaueres Bild Ihrer Steigerung haben. Darüber hinaus würden Sie wahrscheinlich mit der Konversionsrate für Ihre Erlebnisse/Angebote vergleichen, wenn Sie einfach einen A/B-Test durchgeführt haben (ein zufällig bereitgestelltes Steuerelement). In diesem Fall wird empfohlen, eine Zuordnung von 50% zu einer Kontrolle über zufällig bereitgestellte Erlebnisse zu verwenden.
   * **&quot; Zufällige Erlebnisse&quot; als Ihre Kontrolle und Ihr Aktivitätsziel besteht darin, personalisierte Traffic** zu maximieren: Wenn Sie mit dem Algorithmus zufrieden sind und die maximal personalisierte Traffic-Menge haben möchten, wird eine Zuordnung von 10% bis 30% zur Kontrolle empfohlen. Der Kompromiss hier ist die Genauigkeit, die Sie in Ihren Steigerungsinformationen sehen können (da die Konfidenzintervalle Ihres Traffic-Traffics größer sind, da weniger Traffic zu diesen Traffic-Daten geleitet wird).
   * **Spezifisches Erlebnis als Ihre Steuerung mit einem Zieltyp**: Wenn Sie ein bestimmtes Marketingexperten mit Personalisierungsmodellen vergleichen möchten, wird eine Zuordnung von 10% bis 30% zur Kontrolle empfohlen. Wenn Sie nur ein Erlebnis als Steuerelement auswählen, wird dieser Traffic nicht über alle Angebote/Erlebnisse in der Aktivität verteilt.

* Targeting-Regeln sollten sparsam verwendet werden, da sie die Optimierungsfähigkeit des Modells beeinträchtigen können.
* Berichterstellungsgruppen können den Erfolg Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ begrenzen. Sie sollten nur unter bestimmten Bedingungen verwendet werden.

   * Verwenden Sie Berichterstellungsgruppen nur dann, wenn die folgenden Bedingungen erfüllt sind: (1) Sie planen, neue Angebote zu ersetzen/hinzuzufügen, während die Aktivität läuft, (2) die Angebote in der Berichtsgruppe zielen auf dieselben Besucher ab und (3) die Angebote in dieser Berichtsgruppe besitzen dieselbe Gesamtantwortrate.
   * Es gibt keine Personalisierung zwischen den Angeboten in einer Berichtsgruppe: Die Angebote werden durch das Personalisierungsmodell alle identisch behandelt.
   * Legen Sie niemals alle Angebote in einer Aktivität in einer einzelnen Berichtsgruppe ab. Dadurch werden alle Angebote allen Besuchern in der Aktivität einheitlich nach dem Zufallsprinzip bereitgestellt.

## Welche Einschränkungen gibt es bei der automatisierten Personalisierung? {#section_08BA09ED51B547299963C94FE6417CFA}

Target besitzt eine harte Begrenzung von 30.000 Erlebnissen. Bei weniger als 10.000 erstellten Erlebnissen ist die Funktionsweise jedoch am besten.

## Wie wird die Kundenansprache auf Angebotsebene implementiert? {#section_9D7A86EA93D74E9B8C81072A681263A4}

Sobald der Besucher zur entsprechenden Position gelangt, wird der Satz der möglichen Angebote, die dem Besucher angezeigt werden, anhand der Regeln vom Typ „Kundenansprache auf Angebotsebene“ bestimmt. Anschließend wählt der Algorithmus das Angebot aus, das entsprechend der Prognose durch das Modell den besten erwarteten Umsatz oder die beste Konversionschance aufweist. Beachten Sie, dass sich das Angebots-Targeting auf die Wirksamkeit der maschinellen Lernalgorithmen von Target auswirkt und daher möglichst sparsam eingesetzt werden sollte.

## „Meine Aktivität“ zeigt keine Steigerung an. Was ist los? {#section_BFA07C8C258F45318F73A461B8F32737}

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ „Automatisierte Personalisierung“ eine Steigerung generiert:

* Die Angebote an jeder Position müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Positionen müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke in der Aktivität vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

Weitere Informationen finden Sie unter [Fehlerbehebung bei der automatisierten Personalisierung](../../c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

## Wie wird der Traffic meiner Aktivität durch die automatisierte Personalisierung zugeordnet? {#section_4369364F77804E0D9B78BEE551DA5659}

Die automatisierte Personalisierung leitet Besucher zu dem Erlebnis weiter, das die höchste prognostizierte Erfolgsmetrik basierend auf den neuesten [Random Forest](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA)-Modellen aufweist, die für die einzelnen Modelle erstellt wurden. Diese Prognose basiert auf den spezifischen Informationen des Besuchers und dem Besuchskontext.

Angenommen, eine Aktivität vom Typ „Automatisierte Personalisierung“ hatte zwei Positionen mit jeweils zwei Angeboten. An der ersten Position weist Angebot A eine prognostizierte Konversionsrate von 3 % für einen bestimmten Besucher auf, während Angebot B eine prognostizierte Konversionsrate von 1 % aufweist. An der zweiten Position weist Angebot C eine prognostizierte Konversionsrate von 2 % für denselben Besucher auf, während Angebot D eine prognostizierte Konversionsrate von 5 % aufweist. Daher würde die automatisierte Personalisierung diesem Besucher ein Erlebnis mit Angebot A und Angebot D unterbreiten.

## Wann sollte ich meine Aktivität vom Typ „Automatisierte Personalisierung“ anhalten? {#section_C51F3DAB8887463BB147373F6FE06B93}

Die automatisierte Personalisierung kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere besteht für zeitlose Inhalte keine Notwendigkeit, Ihre Aktivität vom Typ „Automatisierte Personalisierung“ anzuhalten. Wenn Sie wesentliche Änderungen an den Inhalten vornehmen möchten, die den aktuell in Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ vorhandenen Angeboten nicht ähneln, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte anzeigen, nicht verwirrt werden oder sich auf vergangene Ergebnisse mit anderen Inhalten beziehen.

## Wie lange sollte ich warten, bis Modelle erstellt werden? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

Wie lange es dauert, bis Modelle in Ihrer Aktivität erstellt werden, hängt in der Regel vom Traffic Ihrer ausgewählten Aktivitätsposition(en) und Ihrer Aktivitätserfolgsmetrik ab. Verwenden Sie stattdessen die [Traffic-Schätzung](../../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um zu bestimmen, wie lange das Erstellen von Modellen in Ihrer Aktivität erwartungsgemäß dauert.

## Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert? {#section_51EA953C6D1D4A3185FC9DD290D66621}

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

## Wann kann ich die Ergebnisse meiner Aktivität vom Typ „Automatisierte Personalisierung“ anzeigen? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

Sie können beginnen sich die Ergebnisse Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ anzusehen, sobald Sie mindestens über zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, die Modelle erstellt haben.

## Wie kann ich die für das Erstellen von Modellen in meiner Aktivität erforderliche Dauer reduzieren? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

Überprüfen Sie Ihre Aktivitätseinrichtung dahingehend, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, in der Modelle erstellt werden.

* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn die Anzahl der Erlebnisse in einer Aktivität verringert wird, wird das Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitätspositionen vorhanden sind, desto schneller werden die Modelle erstellt.

## Warum werden Besuchern Erlebnisse für eine AP-Aktivität angezeigt, die sie nicht sehen sollten? {#section_41CECEAE0881446A8D9F3B016857914B}

Aktivitäten vom Typ „Automatisierte Personalisierung“ werden einmal pro Sitzung ausgewertet. Wenn für ein bestimmtes Erlebnis qualifizierte aktive Sitzungen vorhanden waren und diesen nun neue Angebote hinzugefügt werden, wird Benutzern der neue Inhalt zusammen mit den zuvor angezeigten Angeboten angezeigt. Da sie zuvor für diese Erlebnisse qualifiziert wurden, werden sie ihnen weiterhin für die Dauer der Sitzung angezeigt. Wenn dies bei jedem einzelnen Seitenbesuch ausgewertet werden soll, sollten Sie den Erlebnis-Targeting-Aktivitätstyp (XT) ändern.
