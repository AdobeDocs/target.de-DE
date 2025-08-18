---
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQ;FAQs;Automated Personalization;Kontrolle;Standarderlebnis;Best Practices
description: Erkunden Sie eine Liste häufig gestellter Fragen (FAQs) und Antworten zu [!UICONTROL Automated Personalization] (AP)-Aktivitäten in [!UICONTROL Adobe Target].
title: Wie finde ich häufig gestellte Fragen zu [!UICONTROL Automated Personalization] Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 21%

---

# Häufig gestellte Fragen zu Automated Personalization

Konsultieren Sie bei Problemen mit [!UICONTROL Automated Personalization] in [!DNL Adobe Target] die folgenden häufig gestellten Fragen und Antworten.

## Kann ich ein bestimmtes Erlebnis als Kontrolle in einer [!UICONTROL Automated Personalization] angeben?

+++Details anzeigen

Sie können beim Erstellen einer [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP)- oder [AT)-Aktivität ein ](/help/main/c-activities/auto-target/auto-target-to-optimize.md) als Steuerelement auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## Wie kann ich [!UICONTROL Automated Personalization] mit einem Standarderlebnis vergleichen? {#section_46C1A620A2384C2C8392D6716DD18495}

+++Details anzeigen

Es gibt keine schlüsselfertige Option zum Vergleichen von [!UICONTROL Automated Personalization] mit einem Standarderlebnis. Wenn jedoch als Problemumgehung im Rahmen der Gesamtaktivität ein Standardangebot oder -erlebnis vorhanden ist, klicken Sie zum besseren Verständnis der Ausgangsleistung in Berichten auf das Segment &quot;[!UICONTROL Control]&quot; und suchen Sie dieses Angebot im resultierenden Bericht auf Angebotsebene. Die für dieses Angebot aufgezeichnete Konversionsrate kann mit der Konversionsrate des gesamten Segments „Random Forest“ verglichen werden. Somit lässt sich vergleichen, welche Leistung die Maschine im Vergleich zum Standardangebot erbringt.

+++

## Wie lauten die Best Practices zum Einrichten einer [!UICONTROL Automated Personalization] Aktivität? {#section_E155B26282BE49B58EA2683413D11DE6}

+++Details anzeigen

* Wenn Sie eine Seite mit niedrigerem Traffic personalisieren möchten oder strukturelle Änderungen am personalisierten Erlebnis vornehmen möchten, sollten Sie eine [!UICONTROL Auto-Target] -Aktivität anstelle von [!UICONTROL Automated Personalization] verwenden. Siehe [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* Erwägen Sie, eine [!UICONTROL A/B Test] zwischen den Angeboten und Standorten durchzuführen, die Sie in Ihrer [!UICONTROL Automated Personalization]-Aktivität verwenden möchten, um sicherzustellen, dass der Standort und die Angebote eine Auswirkung auf das Optimierungsziel haben. Wenn eine [!UICONTROL A/B Test] Aktivität keinen signifikanten Unterschied nachweist, erzeugt [!UICONTROL Automated Personalization] wahrscheinlich auch keine Steigerung.

   * Wenn ein A/B…N-Test keine statistisch signifikanten Unterschiede zwischen den Erlebnissen zeigt, sind wahrscheinlich eine oder mehrere der folgenden Situationen verantwortlich:

      * Die Angebote unterscheiden sich wahrscheinlich nicht ausreichend voneinander.
      * Die ausgewählten Standorte wirken sich nicht auf die Erfolgsmetrik aus.
      * Das Optimierungsziel liegt zu weit im Konversionstrichter, um von den gewählten Angeboten beeinflusst zu werden.

* Stellen Sie sicher, dass Sie die [Traffic-Schätzung](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) verwenden, um ein Gefühl dafür zu bekommen, wie lange es dauert, bis Personalisierungsmodelle in Ihrer [!UICONTROL Automated Personalization]-Aktivität erstellt werden.
* Entscheiden Sie basierend auf Ihren Zielen über die Zuordnung zwischen Kontrolle und Zielgruppe, bevor Sie die Aktivität beginnen.

  Es gibt drei Szenarien, die je nach Ziel Ihrer Aktivität und der von Ihnen ausgewählten Art der Kontrolle zu berücksichtigen sind:

   * **Zufallserlebnisse als Kontrolle und Aktivitätsziel besteht darin, die Effektivität des Personalisierungsalgorithmus zu testen**: Wenn Sie den Personalisierungsalgorithmus auswerten möchten, möchten Sie sich ein genaueres Bild vom Anstieg machen. Sie möchten höchstwahrscheinlich auch vergleichen, wie hoch die Konversionsrate für Ihre Erlebnisse oder Angebote ist, wenn Sie einfach eine [!UICONTROL A/B Test] durchgeführt haben (eine zufällig bereitgestellte Kontrolle). In diesem Fall wird eine Zuordnung von 50 % zu einer Kontrollgruppe von zufällig bereitgestellten Erlebnissen empfohlen.
   * **Sie „zufällige Erlebnisse“ als Kontrolle und Ihr Aktivitätsziel, den personalisierten Traffic zu maximieren**: Wenn Sie mit dem Algorithmus vertraut sind und die maximale Menge an Traffic personalisieren möchten, wird eine Zuordnung von 10 % bis 30 % zur Kontrolle empfohlen. Der Nachteil ist hier die Genauigkeit, die Sie in Ihren Aufstiegsinformationen sehen. Die Konfidenzintervalle Ihres Kontroll-Traffics sind größer, da weniger Traffic zu ihnen fließt.
   * **Als Kontrolle ein spezifisches Erlebnis mit beliebigem Ziel**: Wenn Sie ein bestimmtes Erlebnis mit den Personalisierungsmodellen vergleichen möchten, wird eine Zuordnung von 10 % bis 30 % zur Kontrolle empfohlen. Wenn Sie nur ein Erlebnis als Kontrolle auswählen, wird dieser Traffic nicht über jedes Angebot oder Erlebnis in der Aktivität verteilt.

* Targeting-Regeln sollten sparsam verwendet werden, da sie die Optimierungsfähigkeit des Modells beeinträchtigen können.
* Berichtsgruppen können den Erfolg Ihrer [!UICONTROL Automated Personalization]-Aktivität einschränken. Verwenden von Berichtsgruppen nur unter bestimmten Bedingungen:

   * Verwenden Sie Berichtsgruppen nur, wenn die folgenden Bedingungen erfüllt sind:

      * Sie planen, während der Ausführung der Aktivität neue Angebote zu ersetzen oder hinzuzufügen.
      * Die Angebote in der Berichtsgruppe sprechen dieselben Besucher an.
      * Die Angebote in dieser Berichtsgruppe weisen etwa dieselbe Gesamtansprechrate auf.

   * Es gibt keine Personalisierung zwischen Angeboten in einer Berichtsgruppe. Die Angebote werden vom Personalisierungsmodell alle gleich behandelt.
   * Legen Sie niemals alle Angebote in einer Aktivität in einer einzelnen Berichtsgruppe ab. Dadurch werden alle Angebote allen Besuchern in der Aktivität nach dem Zufallsprinzip bereitgestellt.

+++

## Welche Beschränkungen gibt es in [!UICONTROL Automated Personalization]? {#section_08BA09ED51B547299963C94FE6417CFA}

+++Details anzeigen

[!DNL Target] hat eine feste Grenze von 30.000 Erlebnissen, funktioniert aber am besten, wenn weniger als 10.000 Erlebnisse erstellt werden.

Diese Beschränkung gilt selbst dann, wenn bei der Aktivität die Option [!UICONTROL Disalow Duplicates] aktiviert ist.

Weitere Informationen zu Zeichenbeschränkungen und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.), die Aktivitäten und andere Elemente in [!DNL Target] betreffen, finden Sie unter [Beschränkungen](/help/main/r-troubleshooting-target/target-limits.md).

+++

## Wie wird die Kundenansprache auf Angebotsebene implementiert?  {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++Details anzeigen

Sobald der Besucher zur entsprechenden Position gelangt, wird der Satz der möglichen Angebote, die dem Besucher angezeigt werden, anhand der Regeln vom Typ „Kundenansprache auf Angebotsebene“ bestimmt. Anschließend wählt der Algorithmus aus diesen Angeboten das Angebot aus, von dem das Modell den besten erwarteten Umsatz oder die beste Konversionschance vorhersagt. Das Targeting von Angeboten wirkt sich auf die Effektivität [!DNL Target] Machine-Learning-Algorithmen aus und sollte daher so sparsam wie möglich eingesetzt werden.

+++

## Warum zeigt meine [!UICONTROL Automated Personalization] keine Steigerung an? {#section_BFA07C8C258F45318F73A461B8F32737}

+++Details anzeigen

Es sind vier Faktoren erforderlich, damit eine [!UICONTROL Automated Personalization] Aktivität eine Steigerung generiert:

* Die Angebote an den einzelnen Standorten müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Standorte müssen sich an einem Ort befinden, der einen Unterschied zum Optimierungsziel macht.
* Es müssen genügend Traffic- und Teststärke in der Aktivität vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe einer einfachen, nicht personalisierten [!UICONTROL A/B Test]-Aktivität sicherzustellen, dass der Inhalt und die Speicherorte, aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtansprechraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die A/B-Testergebnisse eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, ist es wahrscheinlich, dass eine personalisierte Aktivität erfolgreich ist. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. Normalerweise liegt das Problem darin, dass die Angebote oder Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

Weitere Informationen finden Sie unter [Fehlerbehebung bei der automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## Wie ordnet [!UICONTROL Automated Personalization] den Traffic meiner Aktivität zu? {#section_4369364F77804E0D9B78BEE551DA5659}

+++Details anzeigen

[!UICONTROL Automated Personalization] leitet Besucher zu dem Erlebnis mit der höchsten prognostizierten Erfolgsmetrik, basierend auf den für jedes Modell erstellten [Zufällige ](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)), weiter. Diese Prognose basiert auf den spezifischen Informationen des Besuchers und dem Besuchskontext.

Angenommen, eine [!UICONTROL Automated Personalization] hat zwei Standorte mit jeweils zwei Angeboten. An der ersten Position weist Angebot A eine prognostizierte Konversionsrate von 3 % für einen bestimmten Besucher auf, während Angebot B eine prognostizierte Konversionsrate von 1 % aufweist. An der zweiten Position weist Angebot C eine prognostizierte Konversionsrate von 2 % für denselben Besucher auf, während Angebot D eine prognostizierte Konversionsrate von 5 % aufweist. Daher stellt [!UICONTROL Automated Personalization] diesem Besucher ein Erlebnis mit Angebot A und Angebot D bereit.

+++

## Wann sollte ich meine [!UICONTROL Automated Personalization] anhalten? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++Details anzeigen

[!UICONTROL Automated Personalization] kann als „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre [!UICONTROL Automated Personalization] zu stoppen. Wenn Sie wesentliche Änderungen an den Inhalten vornehmen möchten, die den derzeit in Ihrer [!UICONTROL Automated Personalization] enthaltenen Angeboten nicht ähnlich sind, empfiehlt es sich, eine neue Aktivität zu starten. Das Starten einer neuen Aktivität hilft anderen Benutzern, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten zu verwechseln oder in Beziehung zu setzen.

+++

## Wie lange sollte ich warten, bis Modelle erstellt werden? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++Details anzeigen

Die Zeit, die zum Erstellen von Modellen in Ihrer Aktivität benötigt wird, hängt in der Regel vom Traffic zu Ihren ausgewählten Aktivitäts-Standorten und Ihrer Erfolgsmetrik der Aktivität ab. Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) um die erwartete Zeitdauer für die Erstellung von Modellen in Ihrer Aktivität zu bestimmen.

+++

## Ein Modell wird innerhalb meiner [!UICONTROL Automated Personalization] erstellt. Sind die Besuche bei diesem Erlebnis personalisiert? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++Details anzeigen

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

+++

## Wann kann ich die Ergebnisse meiner [!UICONTROL Automated Personalization]-Aktivität anzeigen? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++Details anzeigen

Sie können die Ergebnisse Ihrer [!UICONTROL Automated Personalization]-Aktivität anzeigen, sobald Sie über mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, für das Modelle erstellt wurden.

+++

## Wie kann ich die Zeit verkürzen, die für die Erstellung von Modellen in meiner [!UICONTROL Automated Personalization]-Aktivität benötigt wird? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++Details anzeigen

Überprüfen Sie die Einrichtung Ihrer Aktivität und stellen Sie fest, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, mit der Modelle erstellt werden.

* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität löschen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an den Standorten Ihrer Aktivitäten auftreten, desto schneller können Modelle erstellt werden.

+++

## Warum sehen Besucher Erlebnisse für eine [!UICONTROL Automated Personalization] Aktivität, die sie nicht sehen sollten? {#section_41CECEAE0881446A8D9F3B016857914B}

+++Details anzeigen

[!UICONTROL Automated Personalization] Aktivitäten werden einmal pro Sitzung ausgewertet. Wenn es aktive Sitzungen gibt, die sich für ein bestimmtes Erlebnis qualifiziert haben, und jetzt neue Angebote hinzugefügt wurden, sehen Besucher den neuen Inhalt zusammen mit den zuvor angezeigten Angeboten. Da sich diese Besucher zuvor für diese Erlebnisse qualifiziert haben, sehen sie diese Erlebnisse während der Sitzung weiterhin. Um dies bei jedem Seitenbesuch auszuwerten, sollten Sie zum Aktivitätstyp [!UICONTROL Experience Targeting] (XT) wechseln.

+++

## Kann ich die Zielmetrik inmitten einer [!UICONTROL Automated Personalization] ändern? {#change-metric}

+++Details anzeigen

[!DNL Adobe] empfiehlt nicht, die Zielmetrik inmitten einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. [!DNL Adobe] übernehmen keine Garantie dafür, was passiert, wenn die Zielmetrik in einer Aktivität nach deren Ausführung geändert wird.

Diese Empfehlung gilt für [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Automated Personalization]-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

## Kann ich die Option [!UICONTROL Reset Report Data] während der Ausführung einer [!UICONTROL Automated Personalization] verwenden?

+++Details anzeigen

[!DNL Adobe] empfiehlt nicht, die Option [!UICONTROL Reset Report Data] für [!UICONTROL Automated Personalization] Aktivitäten zu verwenden. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem [!UICONTROL Automated Personalization]. Anstatt die Option [!UICONTROL Reset Report Data] für [!UICONTROL Automated Personalization] Aktivitäten zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität. Diese Leitlinien gelten auch für [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].

+++

## Wie erstellt [!UICONTROL Automated Personalization] Modelle in Bezug auf Umgebungen?

+++Details anzeigen

Es wird ein Modell erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic und dem Versand des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

Der Traffic eines zweiten Modellsatzes wird für jede Modellierungsgruppe ([!UICONTROL Automated Personalization]) oder jedes Erlebnis ([!UICONTROL Auto-Target]) erstellt. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

Anforderungen werden daher unabhängig von der Umgebung mit demselben Modell bereitgestellt. Die Pluralität des Traffics sollte jedoch aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte erfolgreichste Erlebnis mit dem Verhalten in der realen Welt übereinstimmt.

+++
