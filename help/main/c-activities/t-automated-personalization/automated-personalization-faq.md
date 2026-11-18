---
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQ;FAQs;Automated Personalization;Kontrolle;Standarderlebnis;Best Practices
description: Erkunden Sie eine Liste häufig gestellter Fragen (FAQs) und Antworten zu [!UICONTROL Automated Personalization] (AP)-Aktivitäten in [!UICONTROL Adobe Target].
title: Wie finde ich häufig gestellte Fragen zu [!UICONTROL Automated Personalization]-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
TQID: 'https://experienceleague.adobe.com/cYdFwvkJDlfGYdcxql9iWGwNiTed4Lb2kC7JdN7xgdo'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 6%
---
# Häufig gestellte Fragen zu Automated Personalization {#ap-faq}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Antworten auf häufig gestellte Fragen zu **[!UICONTROL Automated Personalization]**-Aktivitäten.

>[!ENDSHADEBOX]

In den folgenden Fragen und Antworten wird beschrieben, wie Sie **[!UICONTROL Automated Personalization]**-Aktivitäten in [!DNL Adobe Target] einrichten, wie die Personalisierungsmodelle erstellt werden, wie der Traffic zugewiesen wird und wie die Ergebnisse gelesen werden.

## Einrichten einer Aktivität {#set-up-an-activity}

+++ Wie lauten die Best Practices zum Einrichten einer [!UICONTROL Automated Personalization]-Aktivität?

* Achten Sie genau auf die *Aktivitäts-Form* (Anzahl der Standorte × Anzahl der Angebote), nicht nur auf die Gesamtzahl der Erlebnisse. Die kartesischen Kombinationen von Speicherorten und Angeboten wirken sich stärker auf die Leistung während der Bearbeitung aus als auf die Anzahl der Erlebnisse. Um eine optimale Leistung und Verwaltbarkeit zu erzielen, beschränken Sie die Aktivitäten von **[!UICONTROL Automated Personalization]** und **[!UICONTROL Automatisches Targeting]** auf 4-6 Standorte mit 4-6 Angeboten pro Standort, wie in der Frage „Welche Beschränkungen gibt es in Automated Personalization?“ beschrieben. in diesem Abschnitt. Größere Konfigurationen werden nicht empfohlen und können zu langsamem Laden oder Bearbeiten im **[!UICONTROL Visual Experience Composer“]**.
* Wenn Sie eine Seite mit niedrigerem Traffic personalisieren oder strukturelle Änderungen an dem zu personalisierenden Erlebnis vornehmen möchten, sollten Sie eine [**[!UICONTROL Automatisches Targeting &#x200B;]**-Aktivität &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md)**[!UICONTROL &#x200B; Automated Personalization &#x200B;]**&#x200B;verwenden.
* Erwägen Sie die Ausführung einer **[!UICONTROL A/B-]**-Aktivität zwischen den Angeboten und Standorten, die Sie in Ihrer **[!UICONTROL Automated Personalization]**-Aktivität verwenden möchten, um zu bestätigen, dass die Standorte und Angebote Auswirkungen auf das Optimierungsziel haben. Wenn die Aktivität **[!UICONTROL A/B]** keinen signifikanten Unterschied zeigt, kann **[!UICONTROL Automated Personalization]** wahrscheinlich auch keine Steigerung erzeugen.

  Wenn ein A/B…N-Test keine statistisch signifikanten Unterschiede zwischen den Erlebnissen zeigt, sind wahrscheinlich eine oder mehrere der folgenden Situationen verantwortlich:

  * Die Angebote unterscheiden sich wahrscheinlich nicht ausreichend voneinander.
  * Die von Ihnen ausgewählten Standorte haben keine Auswirkungen auf die Erfolgsmetrik.
  * Das Optimierungsziel in der Konversions-funnel ist zu weit reichend, um von den gewählten Angeboten beeinflusst zu werden.

* Mit der [Traffic-Schätzung](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator) erhalten Sie einen Eindruck davon, wie lange es dauert, bis Personalisierungsmodelle in Ihrer **[!UICONTROL Automated Personalization]**-Aktivität erstellt werden.
* Entscheiden Sie basierend auf Ihren Zielen über die Zuordnung zwischen der Kontrolle und dem Zieldatenverkehr, bevor Sie die Aktivität beginnen. In der folgenden Tabelle sind die drei zu berücksichtigenden Szenarien aufgelistet, basierend auf dem Ziel Ihrer Aktivität und dem von Ihnen ausgewählten Steuerelementtyp.

  | Kontroll- und Aktivitätsziel | Empfohlene Zuordnung zum Steuerelement | Details |
  | --- | --- | --- |
  | **[!UICONTROL Zufällige Erlebnisse]** als Kontrolle. Ziel ist es, die Effektivität des Personalisierungsalgorithmus zu testen | 50% | Dieses Ziel erfordert ein genaueres Bild des Auftriebs. Sie möchten höchstwahrscheinlich auch die Konversionsrate Ihrer Erlebnisse oder Angebote mit der Rate vergleichen, die ein einfacher **[!UICONTROL A/B-Test]** (eine zufällig bereitgestellte Kontrolle) ergeben würde. |
  | **[!UICONTROL Zufällige Erlebnisse]** als Kontrolle und das Ziel ist die Maximierung des personalisierten Traffics | 10 % bis 30 % | Verwenden Sie diese Option, wenn Sie mit dem Algorithmus vertraut sind und den maximalen Traffic personalisieren möchten. Der Nachteil ist die Genauigkeit Ihrer Aufstiegsinformationen: Die Konfidenzintervalle des Kontroll-Traffics sind größer, da weniger Traffic zu ihnen fließt. |
  | **[!UICONTROL Spezifisches Erlebnis]** als Kontrolle mit einem der beiden Ziele | 10 % bis 30 % | Verwenden Sie diese Option, um ein bestimmtes marketergesteuertes Erlebnis mit den Personalisierungsmodellen zu vergleichen. Wenn Sie nur ein Erlebnis als Kontrolle auswählen, wird dieser Traffic nicht auf alle Angebote oder Erlebnisse in der Aktivität verteilt. |

* Verwenden Sie Targeting-Regeln so sparsam wie möglich, da sie die Möglichkeit des Modells zur Optimierung beeinträchtigen können. Weitere Informationen finden Sie unter [Targeting von Automated Personalization-Angeboten](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).
* Berichtsgruppen können den Erfolg Ihrer **[!UICONTROL Automated Personalization]**-Aktivität einschränken. Daher sollten Sie diese nur unter bestimmten Bedingungen verwenden. Weitere Informationen finden Sie unter [Berichtsgruppen für Angebote in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

  * Verwenden Sie Berichtsgruppen nur, wenn alle folgenden Bedingungen erfüllt sind:

    * Sie planen, Angebote während der Ausführung der Aktivität zu ersetzen oder hinzuzufügen.
    * Die Angebote in der Berichtsgruppe sprechen dieselben Besucher an.
    * Die Angebote in der Berichtsgruppe weisen etwa dieselbe Gesamtansprechrate auf.

  * Es gibt keine Personalisierung zwischen Angeboten in einer Berichtsgruppe. Das Personalisierungsmodell behandelt alle Angebote gleich.
  * Legen Sie niemals alle Angebote in einer Aktivität in einer einzelnen Berichtsgruppe ab. Dadurch werden alle Angebote allen Besuchern in der Aktivität nach dem Zufallsprinzip bereitgestellt.

+++

+++ Welche Beschränkungen gibt es in [!UICONTROL Automated Personalization]?

[!DNL Target] hat eine feste Grenze von 30.000 Erlebnissen, funktioniert aber am besten, wenn weniger als 10.000 Erlebnisse erstellt werden. Die gleiche Beschränkung gilt, wenn für die Aktivität die Option **[!UICONTROL Duplikate nicht zulassen]** aktiviert ist.

Obwohl **[!UICONTROL Aktivitäten vom Typ &quot;Automated Personalization]** und **[!UICONTROL Automatisches Targeting]** eine große Anzahl von Erlebnissen unterstützen können, hängt die Leistung bei der Bearbeitung stark von der *Aktivitäts-* ab (Anzahl der Standorte × Anzahl der Angebote). Bestimmte Konfigurationen erstellen große kartesische Kombinationen, die sich erheblich auf die Auslastung und Bearbeitungsleistung auswirken können, selbst unterhalb der dokumentierten Erlebnisbeschränkungen.

Um eine optimale Leistung und Verwaltbarkeit zu erzielen, beschränken Sie die **[!UICONTROL Aktivitäten von]** und **[!UICONTROL Automatisches Targeting]** auf 4-6 Standorte mit 4-6 Angeboten pro Standort. Größere Konfigurationen werden nicht empfohlen und können in der [!DNL Target] Benutzeroberfläche eingeschränkt sein.

In der aktuellen [!DNL Target]-Benutzeroberfläche werden die Aktivitäten **[!UICONTROL Automated Personalization]** und **[!UICONTROL Automatisches Targeting]** direkt im Schritt **[!UICONTROL Erlebnisse]** konfiguriert. [!DNL Target] können Inline-Warnungen anzeigen oder das Speichern einer Aktivität verhindern, wenn die Konfiguration die unterstützten Schwellenwerte überschreitet, und die Aktivitäts-Form bei **[!UICONTROL Weiter]**, **[!UICONTROL Speichern]** und **[!UICONTROL Veröffentlichen]** erneut überprüfen.

Weitere Informationen zu Zeichenbeschränkungen und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.), die Aktivitäten und andere Elemente in [!DNL Target] betreffen, finden Sie unter [Beschränkungen](/help/main/r-troubleshooting-target/target-limits.md).

+++

+++ Kann ich ein bestimmtes Erlebnis angeben, das als Steuerelement in einer [!UICONTROL Automated Personalization]-Aktivität verwendet werden soll?

Sie können beim Erstellen einer [**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview) (AP)- oder [**[!UICONTROL Automatisches Targeting]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT)-Aktivität ein bestimmtes Erlebnis als Steuerelement.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentsatz zu diesem Erlebnis leiten. Anschließend können Sie die Leistungsberichte des personalisierten Traffics mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Auswählen des Steuerelementerlebnisses](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

+++ Wie wird das Targeting auf Angebotsebene implementiert?

Bei Ankunft jedes Besuchers bestimmen die Targeting-Regeln auf Angebotsebene die Menge der Angebote, die der Besucher sehen kann. Der Algorithmus wählt dann aus diesen Angeboten das Angebot aus, das das Modell vorhersagt und das den besten erwarteten Umsatz oder die beste Konversionschance hat. Das Targeting von Angeboten wirkt sich auf die Effektivität der [!DNL Target] Machine-Learning-Algorithmen aus. Verwenden Sie diese daher so sparsam wie möglich. Weitere Informationen finden Sie unter [Targeting von Automated Personalization-Angeboten](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

+++

## Modellerstellung und Traffic-Zuordnung {#models-and-traffic}

+++ Wie ordnet [!UICONTROL Automated Personalization] den Traffic meiner Aktivität zu?

**[!UICONTROL Automated Personalization]** leitet Besucher zu dem Erlebnis um, das die höchste prognostizierte Erfolgsmetrik aufweist, basierend auf den neuesten [Zufällige &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)). Diese Prognose basiert auf den spezifischen Informationen und dem Besuchskontext des Besuchers.

Angenommen, eine **[!UICONTROL Automated Personalization]**-Aktivität hat zwei Standorte mit jeweils zwei Angeboten. An der ersten Position weist Angebot A eine prognostizierte Konversionsrate von 3 % für einen bestimmten Besucher auf, während Angebot B eine prognostizierte Konversionsrate von 1 % aufweist. An der zweiten Position weist Angebot C eine prognostizierte Konversionsrate von 2 % für denselben Besucher auf, während Angebot D eine prognostizierte Konversionsrate von 5 % aufweist. Daher stellt **[!UICONTROL Automated Personalization]** diesem Besucher ein Erlebnis mit Angebot A und Angebot D bereit.

+++

+++ Wie erstellt [!UICONTROL Automated Personalization] Modelle in Bezug auf Umgebungen?

Es wird ein Modell erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic und dem Versand des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

Für jede Berichtsgruppe (**[!UICONTROL Automated Personalization]**) oder jedes Erlebnis (automatisches **[!UICONTROL ) wird ein zweiter Modellsatz]**. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

Anforderungen werden daher unabhängig von der Umgebung mit demselben Modell bereitgestellt. Die Pluralität des Traffics sollte jedoch aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte erfolgreichste Erlebnis mit dem Verhalten in der realen Welt übereinstimmt.

+++

+++ Wie lange sollte ich warten, bis Modelle erstellt werden?

Die Zeit, die zum Erstellen von Modellen in Ihrer Aktivität benötigt wird, hängt in der Regel vom Traffic zu Ihren ausgewählten Aktivitäts-Standorten und von Ihrer Erfolgsmetrik der Aktivität ab. Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator) um die erwartete Zeitdauer für die Erstellung von Modellen in Ihrer Aktivität zu bestimmen.

+++

+++ Wie kann ich die Zeit verkürzen, die zum Erstellen von Modellen in meiner [!UICONTROL Automated Personalization]-Aktivität benötigt wird?

Überprüfen Sie die Einrichtung Ihrer Aktivität auf Änderungen, die die Geschwindigkeit der Modellerstellung verbessern. Ändern Sie beispielsweise eine RPV-Erfolgsmetrik in „Konversion“, wählen Sie eine Erfolgsmetrik aus, die Ihren Aktivitätserlebnissen in der Vertriebs-funnel näher kommt, legen Sie einige Erlebnisse aus der Aktivität ab oder verwenden Sie eine Seite mit höherem Traffic. Weitere Informationen finden Sie unter [Fehlerbehebung bei Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md).

+++

+++ Ein Modell wird innerhalb meiner Aktivität [!UICONTROL Automated Personalization] erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

Nein. In Ihrer Aktivität müssen mindestens zwei Modelle erstellt werden, damit die Personalisierung gestartet wird.

+++

## Ergebnisse und Steigerung {#results-and-lift}

+++ Wann kann ich die Ergebnisse meiner [!UICONTROL Automated Personalization]-Aktivität anzeigen?

Sie können die Ergebnisse Ihrer **[!UICONTROL Automated Personalization]**-Aktivität anzeigen, nachdem für mindestens zwei Erlebnisse Modelle erstellt wurden (durch ein grünes Häkchen gekennzeichnet).

+++

+++ Warum wird für meine Aktivität [!UICONTROL Automated Personalization] keine Steigerung angezeigt?

Für eine **[!UICONTROL Automated Personalization]**-Aktivität sind vier Faktoren erforderlich, um eine Steigerung zu generieren:

* Die Angebote an den einzelnen Standorten müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Standorte müssen an einem Ort sein, der einen Unterschied zum Optimierungsziel macht.
* Es müssen genügend Traffic- und Teststärke in der Aktivität vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Am besten stellen Sie zunächst mithilfe einer einfachen, nicht personalisierten **[!UICONTROL A/B-Test]**-Aktivität sicher, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, tatsächlich einen Unterschied zu den Gesamtansprechraten darstellen. Eine vollständige Anleitung finden Sie unter [Fehlerbehebung bei Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md).

+++

+++ Wie kann ich [!UICONTROL Automated Personalization] mit einem Standarderlebnis vergleichen?

Es gibt keine schlüsselfertige Option zum Vergleichen von **[!UICONTROL Automated Personalization]** mit einem Standarderlebnis. Wenn als Problemumgehung ein Standardangebot oder -erlebnis als Teil der Aktivität vorhanden ist, klicken Sie auf das **[!UICONTROL Kontrolle]**-Segment in Berichten und suchen Sie dieses Angebot im resultierenden Bericht auf Angebotsebene. Die für dieses Angebot erfasste Konversionsrate kann mit der Konversionsrate des gesamten Segments „Random Forest“ verglichen werden. Dieser Vergleich zeigt die Leistung des Modells im Vergleich zum Standardangebot.

+++

## Verwalten einer Live-Aktivität {#manage-live-activity}

+++ Wann sollte ich meine [!UICONTROL Automated Personalization]-Aktivität stoppen?

**[!UICONTROL Automated Personalization]** kann als „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre **[!UICONTROL Automated Personalization]**-Aktivität anzuhalten. Wenn Sie wesentliche Änderungen an den Inhalten vornehmen möchten, die nicht den Angeboten ähneln, die sich derzeit in Ihrer Aktivität befinden, empfiehlt es sich, eine neue Aktivität zu starten. Das Starten einer neuen Aktivität hilft anderen Benutzenden, die Berichte überprüfen, dabei, vergangene Ergebnisse nicht mit anderen Inhalten zu verwechseln oder in Beziehung zu setzen.

+++

+++ Kann ich die Zielmetrik inmitten einer [!UICONTROL Automated Personalization]-Aktivität ändern?

[!DNL Adobe] empfiehlt nicht, die Zielmetrik inmitten einer Aktivität zu ändern. Obwohl es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie stattdessen eine neue Aktivität starten . [!DNL Adobe] garantiert nicht, was passiert, wenn Sie die Zielmetrik in einer Aktivität nach deren Ausführung ändern.

Diese Empfehlung gilt für **[!UICONTROL Automatische Zuordnung]**, **[!UICONTROL Automatisches Targeting]** und **[!UICONTROL Automated Personalization]**-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

+++ Kann ich die Option [!UICONTROL Berichtsdaten zurücksetzen] während der Ausführung einer [!UICONTROL Automated Personalization]-Aktivität verwenden?

Es wird [!DNL Adobe] nicht empfohlen, für **[!UICONTROL Automated Personalization**&#x200B;[!UICONTROL &#x200B; Aktivitäten die Option &#x200B;]&#x200B;**Berichtsdaten zurücksetzen]** zu verwenden. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem Modell **[!UICONTROL Automated Personalization]**. Statt die Option **[!UICONTROL Berichtsdaten zurücksetzen]** zu verwenden, eine neue Aktivität erstellen und die ursprüngliche Aktivität deaktivieren. Diese Anleitung gilt auch für Aktivitäten **[!UICONTROL Automatische Zuordnung]** und **[!UICONTROL Automatisches Targeting]**.

+++

+++ Warum sehen Besucherinnen und Besucher Erlebnisse für eine [!UICONTROL Automated Personalization]-Aktivität, die sie nicht sehen sollten?

**[!UICONTROL Automated Personalization]**-Aktivitäten werden einmal pro Sitzung ausgewertet. Wenn es aktive Sitzungen gibt, die sich für ein bestimmtes Erlebnis qualifiziert haben, und ihnen seitdem neue Angebote hinzugefügt wurden, sehen Besucher den neuen Inhalt zusammen mit den zuvor angezeigten Angeboten. Diese Besucher haben sich zuvor für diese Erlebnisse qualifiziert, sodass sie diese Erlebnisse während der Sitzung weiterhin sehen. Um die Aktivität bei jedem Seitenbesuch auszuwerten, ändern Sie in den Aktivitätstyp **[!UICONTROL Erlebnis-Targeting]** (XT).

+++
