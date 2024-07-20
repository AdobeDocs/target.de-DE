---
keywords: Fehlerbehebung; häufig gestellte Fragen; FAQ; FAQs; automatisierte Personalisierung; Kontrolle; Standarderlebnis; Best Practices
description: Erkunden Sie eine Liste häufig gestellter Fragen (FAQs) und Antworten zu AP-Aktivitäten (0) in [!UICONTROL Adobe Target].[!UICONTROL Automated Personalization]
title: Wie finde ich häufig gestellte Fragen zu [!UICONTROL Automated Personalization] Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 22%

---

# Häufig gestellte Fragen zu Automated Personalization

Sehen Sie sich die folgenden FAQs und Antworten an, während Sie mit [!UICONTROL Automated Personalization] -Aktivitäten in [!DNL Adobe Target] arbeiten.

## Kann ich ein bestimmtes Erlebnis als Kontrollelement in einer [!UICONTROL Automated Personalization] -Aktivität angeben?

+++Siehe Details

Sie können beim Erstellen einer Aktivität vom Typ [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder vom Typ [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## Wie kann ich [!UICONTROL Automated Personalization] mit einem Standarderlebnis vergleichen? {#section_46C1A620A2384C2C8392D6716DD18495}

+++Siehe Details

Es gibt keine Option zum Vergleich von [!UICONTROL Automated Personalization] mit einem Standarderlebnis. Wenn jedoch als Problemumgehung ein Standardangebot oder -erlebnis im Rahmen der Gesamtaktivität vorhanden ist, klicken Sie zum Verständnis der Basisleistung auf das Segment &quot;[!UICONTROL Control]&quot; in den Berichten und suchen Sie dieses spezielle Angebot im resultierenden Bericht auf Angebotsebene. Die für dieses Angebot aufgezeichnete Konversionsrate kann verwendet werden, um mit der Konversionsrate des gesamten Segments &quot;Random Forest&quot;zu vergleichen. Somit lässt sich vergleichen, welche Leistung die Maschine im Vergleich zum Standardangebot erbringt.

+++

## Was sind die Best Practices zum Einrichten einer [!UICONTROL Automated Personalization] -Aktivität? {#section_E155B26282BE49B58EA2683413D11DE6}

+++Siehe Details

* Wenn Sie eine Seite mit geringerem Traffic personalisieren möchten oder strukturelle Änderungen am personalisierten Erlebnis vornehmen möchten, sollten Sie erwägen, anstelle von [!UICONTROL Automated Personalization] eine [!UICONTROL Auto-Target] -Aktivität zu verwenden. Siehe [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* Schließen Sie ggf. eine [!UICONTROL A/B Test] -Aktivität zwischen den Angeboten und Orten ab, die Sie in Ihrer [!UICONTROL Automated Personalization] -Aktivität verwenden möchten, um sicherzustellen, dass sich der Standort und die Angebote auf das Optimierungsziel auswirken. Wenn eine [!UICONTROL A/B Test] -Aktivität keinen signifikanten Unterschied aufzeigen kann, kann [!UICONTROL Automated Personalization] wahrscheinlich auch keine Steigerung generieren.

   * Wenn ein A/B...N-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen zeigt, ist wahrscheinlich eine oder mehrere der folgenden Situationen verantwortlich:

      * Die Angebote unterscheiden sich wahrscheinlich nicht ausreichend voneinander.
      * Die ausgewählten Orte wirken sich nicht auf die Erfolgsmetrik aus.
      * Das Optimierungsziel liegt zu weit im Konversionstrichter, um von Ihren ausgewählten Angeboten beeinflusst zu werden.

* Stellen Sie sicher, dass Sie die [Traffic-Schätzung](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) verwenden, damit Sie wissen, wie lange es dauert, bis Personalisierungsmodelle in Ihrer [!UICONTROL Automated Personalization] -Aktivität erstellt werden.
* Entscheiden Sie anhand Ihrer Ziele, welche Zuordnung das Kontroll- und das Targeting vor Beginn der Aktivität vornehmen soll.

  Je nach Ziel Ihrer Aktivität und ausgewähltem Kontrolltyp gibt es drei Szenarien:

   * **Zufällige Erlebnisse, da Ihr Kontroll- und Aktivitätsziel darin besteht, die Effektivität des Personalisierungsalgorithmus zu testen**: Wenn Ihr Ziel darin besteht, den Personalisierungsalgorithmus zu bewerten, möchten Sie ein genaueres Bild der Steigerung erhalten. Sie möchten außerdem mit hoher Wahrscheinlichkeit die Konversionsrate Ihrer Erlebnisse oder Angebote vergleichen, wenn Sie einfach einen [!UICONTROL A/B Test] -Wert (eine zufällig bereitgestellte Kontrolle) verwenden. In diesem Fall wird eine Zuordnung von 50 % zu einer Kontrollgruppe von zufällig bereitgestellten Erlebnissen empfohlen.
   * **&quot;Zufällige Erlebnisse&quot;, da Ihr Kontroll- und Aktivitätsziel darin besteht, den personalisierten Traffic zu maximieren**: Wenn Sie mit dem Algorithmus vertraut sind und die maximale Traffic-Menge personalisiert werden soll, wird eine Zuordnung von 10 % bis 30 % zur Kontrolle empfohlen. Der Kompromiss hier ist die Genauigkeit, die Sie in Ihren Steigerungsinformationen sehen. Die Konfidenzintervalle Ihres Kontroll-Traffics sind größer, da weniger Traffic zu ihnen geleitet wird.
   * **Als Kontrolle ein spezifisches Erlebnis mit beliebigem Ziel**: Wenn Sie ein bestimmtes Erlebnis mit den Personalisierungsmodellen vergleichen möchten, wird eine Zuordnung von 10 % bis 30 % zur Kontrolle empfohlen. Wenn Sie nur ein Erlebnis als Kontrolle auswählen, wird dieser Traffic nicht auf alle Angebote oder Erlebnisse in der Aktivität verteilt.

* Targeting-Regeln sollten sparsam verwendet werden, da sie die Optimierungsfähigkeit des Modells beeinträchtigen können.
* Berichtsgruppen können den Erfolg Ihrer [!UICONTROL Automated Personalization] -Aktivität einschränken. Verwenden Sie Berichtsgruppen nur unter bestimmten Bedingungen:

   * Verwenden Sie Berichtsgruppen nur, wenn die folgenden Bedingungen erfüllt sind:

      * Sie planen, während der Ausführung der Aktivität neue Angebote zu ersetzen oder hinzuzufügen.
      * Die Angebote in der Berichtsgruppe richten sich an dieselben Besucher.
      * Die Angebote in dieser Berichtsgruppe weisen etwa dieselbe Gesamtanmelderate auf.

   * Es gibt keine Personalisierung zwischen Angeboten in einer Berichtsgruppe. Die Angebote werden vom Personalisierungsmodell alle gleich behandelt.
   * Legen Sie niemals alle Angebote in einer Aktivität in einer einzelnen Berichtsgruppe ab. Dadurch werden alle Angebote allen Besuchern in der Aktivität gleichmäßig zufällig bereitgestellt.

+++

## Welche Beschränkungen gibt es in [!UICONTROL Automated Personalization]? {#section_08BA09ED51B547299963C94FE6417CFA}

+++Siehe Details

[!DNL Target] ist auf 30.000 Erlebnisse begrenzt, funktioniert jedoch am besten, wenn weniger als 10.000 Erlebnisse erstellt werden.

Dieselbe Beschränkung wird auch angewendet, wenn die Aktivität die [!UICONTROL Disalow Duplicates] -Option aktiviert hat.

Weitere Informationen zu Zeichenbeschränkungen und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.), die Aktivitäten und andere Elemente in [!DNL Target] betreffen, finden Sie unter [Beschränkungen](/help/main/r-troubleshooting-target/target-limits.md).

+++

## Wie wird die Kundenansprache auf Angebotsebene implementiert?  {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++Siehe Details

Sobald der Besucher zur entsprechenden Position gelangt, wird der Satz der möglichen Angebote, die dem Besucher angezeigt werden, anhand der Regeln vom Typ „Kundenansprache auf Angebotsebene“ bestimmt. Dann wählt der Algorithmus das Angebot aus, das das Modell vorhersagt, über den am besten erwarteten Umsatz oder die beste Konversionschance aus diesen Angeboten verfügt. Das Targeting von Angeboten wirkt sich auf die Wirksamkeit von [!DNL Target] maschinellen Lernalgorithmen aus und sollte daher so sparsam wie möglich verwendet werden.

+++

## Warum zeigt meine [!UICONTROL Automated Personalization] -Aktivität nicht die Steigerung an? {#section_BFA07C8C258F45318F73A461B8F32737}

+++Siehe Details

Es sind vier Faktoren erforderlich, damit eine [!UICONTROL Automated Personalization] -Aktivität eine Steigerung generiert:

* Die Angebote an jedem Ort müssen so unterschiedlich sein, dass sie Besucher beeinflussen.
* Die Orte müssen sich an einer Stelle befinden, die für das Optimierungsziel von Bedeutung ist.
* Es müssen genügend Traffic- und Teststärke in der Aktivität vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Die beste Vorgehensweise besteht darin, zunächst mithilfe einer einfachen, nicht personalisierten [!UICONTROL A/B Test] -Aktivität sicherzustellen, dass der Inhalt und die Orte, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die A/B-Testergebnisse eine statistisch signifikante Steigerung für ein oder mehrere Erlebnisse zeigen, ist es wahrscheinlich, dass eine personalisierte Aktivität erfolgreich ist. Personalization kann auch dann funktionieren, wenn es keine Unterschiede bei den Gesamt-Antwortraten der Erlebnisse gibt. In der Regel ist das Problem auf Angebote oder Standorte zurückzuführen, die keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Bedeutung erkannt zu werden.

Weitere Informationen finden Sie unter [Fehlerbehebung bei der automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## Wie ordnet [!UICONTROL Automated Personalization] den Traffic meiner Aktivität zu? {#section_4369364F77804E0D9B78BEE551DA5659}

+++Siehe Details

[!UICONTROL Automated Personalization] leitet Besucher zu dem Erlebnis weiter, das die höchste prognostizierte Erfolgsmetrik basierend auf den neuesten für jedes Modell erstellten [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) -Modellen aufweist. Diese Prognose basiert auf den spezifischen Informationen des Besuchers und dem Besuchskontext.

Angenommen, eine [!UICONTROL Automated Personalization] -Aktivität hat zwei Orte mit jeweils zwei Angeboten. An der ersten Position weist Angebot A eine prognostizierte Konversionsrate von 3 % für einen bestimmten Besucher auf, während Angebot B eine prognostizierte Konversionsrate von 1 % aufweist. An der zweiten Position weist Angebot C eine prognostizierte Konversionsrate von 2 % für denselben Besucher auf, während Angebot D eine prognostizierte Konversionsrate von 5 % aufweist. Daher liefert [!UICONTROL Automated Personalization] diesem Besucher ein Erlebnis mit Angebot A und Angebot D.

+++

## Wann sollte ich meine [!UICONTROL Automated Personalization] -Aktivität stoppen? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++Siehe Details

[!UICONTROL Automated Personalization] kann als &quot;Always on&quot;-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte müssen Sie Ihre [!UICONTROL Automated Personalization] -Aktivität nicht stoppen. Wenn Sie wesentliche Änderungen am Inhalt vornehmen möchten, die den aktuell in Ihrer [!UICONTROL Automated Personalization] -Aktivität verfügbaren Angeboten nicht ähnlich sind, empfiehlt es sich, eine neue Aktivität zu starten. Der Start einer neuen Aktivität hilft anderen Benutzern bei der Überprüfung von Berichten, vergangene Ergebnisse nicht mit anderen Inhalten zu verwechseln oder in Beziehung zu setzen.

+++

## Wie lange sollte ich warten, bis Modelle erstellt werden? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++Siehe Details

Wie lange es dauert, bis in Ihrer Aktivität Modelle erstellt werden, hängt in der Regel vom Traffic zu Ihren ausgewählten Aktivitätspositionen und Ihrer Aktivitätserfolgsmetrik ab. Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um die erwartete Zeitdauer zu bestimmen, die zum Erstellen von Modellen in Ihrer Aktivität erforderlich ist.

+++

## Ein Modell wird in meiner [!UICONTROL Automated Personalization] -Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++Siehe Details

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

+++

## Wann kann ich die Ergebnisse meiner [!UICONTROL Automated Personalization] -Aktivität anzeigen? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++Siehe Details

Sie können die Ergebnisse Ihrer [!UICONTROL Automated Personalization] -Aktivität anzeigen, nachdem Sie mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) erstellt haben, die Modelle erstellt haben.

+++

## Wie kann ich die für die Erstellung von Modellen in meiner [!UICONTROL Automated Personalization] -Aktivität benötigte Zeit verkürzen? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++Siehe Details

Überprüfen Sie Ihre Aktivitätseinrichtung und sehen Sie, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu erhöhen, mit der Modelle erstellt werden.

* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität entfernen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen in Ihren Aktivitätsstandorten vorhanden sind, desto schneller werden Modelle erstellt.

+++

## Warum werden Besuchern Erlebnisse für eine [!UICONTROL Automated Personalization] -Aktivität angezeigt, die sie nicht sehen sollten? {#section_41CECEAE0881446A8D9F3B016857914B}

+++Siehe Details

[!UICONTROL Automated Personalization] -Aktivitäten werden einmal pro Sitzung ausgewertet. Wenn es aktive Sitzungen gibt, die sich für ein bestimmtes Erlebnis qualifiziert haben und jetzt neue Angebote hinzugefügt wurden, sehen Besucher den neuen Inhalt zusammen mit den zuvor angezeigten Angeboten. Da sich diese Besucher zuvor für diese Erlebnisse qualifiziert haben, sehen sie diese Erlebnisse auch während der Sitzung. Um dies bei jedem Seitenbesuch zu bewerten, sollten Sie zum Aktivitätstyp [!UICONTROL Experience Targeting] (XT) wechseln.

+++

## Kann ich die Zielmetrik in der Mitte durch eine [!UICONTROL Automated Personalization] -Aktivität ändern? {#change-metric}

+++Siehe Details

[!DNL Adobe] rät davon ab, die Zielmetrik während einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. [!DNL Adobe] gibt keine Garantie dafür, was passiert, wenn Sie die Zielmetrik in einer Aktivität ändern, nachdem sie ausgeführt wird.

Diese Empfehlung gilt für [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten, die entweder [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

## Kann ich die Option [!UICONTROL Reset Report Data] beim Ausführen einer [!UICONTROL Automated Personalization] -Aktivität verwenden?

+++Siehe Details

[!DNL Adobe] rät von der Verwendung der [!UICONTROL Reset Report Data] -Option für [!UICONTROL Automated Personalization] -Aktivitäten ab. Obwohl die sichtbaren Berichtsdaten entfernt werden, werden mit dieser Option nicht alle Trainings-Datensätze aus dem Modell [!UICONTROL Automated Personalization] entfernt. Statt die Option [!UICONTROL Reset Report Data] für [!UICONTROL Automated Personalization] -Aktivitäten zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität. Diese Anleitung gilt auch für [!UICONTROL Auto-Allocate] - und [!UICONTROL Auto-Target] -Aktivitäten.

+++

## Wie erstellt [!UICONTROL Automated Personalization] Modelle in Bezug auf Umgebungen?

+++Siehe Details

Ein Modell wird erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic im Vergleich zum Senden des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

Der Traffic aus einem zweiten Satz von Modellen wird für jede Modellgruppe ([!UICONTROL Automated Personalization]) oder jedes Erlebnis ([!UICONTROL Auto-Target]) erstellt. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

Anforderungen werden daher unabhängig von der Umgebung mit demselben Modell bereitgestellt. Die Vielzahl von Traffic sollte jedoch aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte Gesamterlebnis mit dem realen Verhalten übereinstimmt.

+++
