---
keywords: automatisierte Personalisierung;App;Zielgruppen;Ensemble;Random Forest;Multi-Armed Bandit;Thompson Sampling;ml;maschinelles Lernen
description: Verwendung von [!UICONTROL Automated Personalization] AP-Aktivitäten in [!DNL Adobe Target] , die mithilfe des erweiterten maschinellen Lernens verschiedene Angebotsvarianten den einzelnen Besuchern zuordnen.
title: Was ist eine [!UICONTROL Automated Personalization] (AP) Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 46%

---

# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] AP-Aktivitäten in [!DNL Adobe Target] Angebote oder Nachrichten kombinieren und mithilfe des erweiterten maschinellen Lernens verschiedene Angebotsvarianten den einzelnen Besuchern basierend auf ihrem individuellen Kundenprofil zuordnen, um Inhalte zu personalisieren und die Steigerung zu fördern.

>[!NOTE]
>
>Die Funktion [!UICONTROL Automatisierte Personalisierung] steht als Bestandteil der [!DNL Target Premium]-Lösung zur Verfügung. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md#premium).

Ähnlich wie [!UICONTROL Automatisches Targeting], [!UICONTROL Automated Personalization] verwendet eine [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Methode in der Datenwissenschaft, als wichtigsten Personalisierungsalgorithmus zur Bestimmung des besten Erlebnisses, das einem Besucher angezeigt werden soll. [!UICONTROL Automatisierte Personalisierung] kann während der Entdeckungsphase des Testens sehr hilfreich sein. Es ist zudem nützlich, maschinelles Lernen zu ermöglichen, um den effektivsten Inhalt zu bestimmen, wenn man unterschiedliche Besucher anspricht. Im Lauf der Zeit lernt der Algorithmus, die effektivsten Inhalte vorherzusagen, und zeigt die Inhalte an, die am wahrscheinlichsten zum Erreichen Ihrer Ziele beitragen.

Weitere Informationen zum [!UICONTROL Automated Personalization] unterscheidet sich von [!UICONTROL Automatisches Targeting], siehe [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Marketingexperten implementieren eine Datei auf ihrer Website, mit der sie auf einen beliebigen Inhalt zeigen und klicken und dann mithilfe der [!UICONTROL Visual Experience Composer] (VEC). Dann bestimmt der Algorithmus auf Basis aller Verhaltensdaten, die das System über diesen Besucher hat, automatisch, welche Inhalte jedem einzelnen Besucher gezeigt werden sollen, und liefert so eine personalisierte Erfahrung. Da sich die [!UICONTROL automatisierte Personalisierung] an Veränderungen beim Besucherverhalten anpasst, kann sie ohne ein festgelegtes Enddatum ausgeführt werden und ermöglicht dennoch eine kontinuierliche Weiterentwicklung der Personalisierung. Dieser Modus wird manchmal als &quot;Always-on&quot;bezeichnet. Der Marketer muss keine Tests durchführen, keine Ergebnisse analysieren und keinen sich daraus ergebenen Gewinner ermitteln, bevor er erkennen kann, welche Steigerung sich aus der Optimierung ergibt. Das übernimmt eine festgelegte Reihenfolge von Operationen, die dann das Ergebnis einer standardmäßigen A/B-Aktivität implementiert.

Die folgenden Begriffe und Definitionen sind hilfreich, wenn es um die [!UICONTROL automatisierte Personalisierung] geht:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Ein führender Ansatz für maschinelles Lernen. In datenwissenschaftlichen Begriffen ist es eine Ensemble-Classification- oder Regressionsmethode, die durch die Erstellung vieler Entscheidungsbäume auf der Grundlage von Besuchsattributen und Besuchsattributen funktioniert. |
| Thompson Sampling | Ziel des Thompson-Samplings ist es, zu ermitteln, welches Erlebnis insgesamt das beste (nicht personalisierte) Erlebnis ist, und gleichzeitig die &quot;Kosten&quot;für die Suche nach diesem Erlebnis zu minimieren. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

Folgendes sollte beim Einsatz der [!UICONTROL automatisierten Personalisierung] beachtet werden:

## [!UICONTROL Die automatisierte Personalisierung] verwendet einen Random Forest-Algorithmus

Random Forest ist ein führender Ansatz des maschinellen Lernens. In datenwissenschaftlichen Begriffen ist es eine Ensemble-Classification- oder Regressionsmethode, die durch die Erstellung vieler Entscheidungsbäume auf der Grundlage von Besuchsattributen und Besuchsattributen funktioniert. Within [!DNL Target]wird Random Forest verwendet, um zu bestimmen, welches Erlebnis für jeden einzelnen Besucher die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) aufweisen soll. Beispielsweise sind Besucher, die Chrome verwenden, Mitglieder der Treuestufe &quot;Gold&quot;und am Dienstag auf Ihre Site zugreifen, wahrscheinlicher, dass sie mit Erlebnis A konvertieren. Besucher aus New York konvertieren möglicherweise eher mit Erlebnis B. Weitere Informationen zu Random Forest finden Sie unter [!DNL Target], siehe [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Das Personalisierungsmodell wird bei jedem Besuch verbessert

* Der Algorithmus prognostiziert die Wahrscheinlichkeit einer Konversion (oder des geschätzten Umsatzes aus der Konversion) eines Besuchers, um das beste Erlebnis bereitzustellen.
* Ein Besucher ist zum Ende einer bestehenden Sitzung für ein neues Erlebnis qualifiziert, es sei denn, dieser Besucher gehört zur Kontrollgruppe. Wenn sich der Besucher in der Kontrollgruppe befindet, ist das Erlebnis, das der Besucher beim ersten Besuch sieht, dasselbe wie bei nachfolgenden Besuchen.
* Das angezeigte Erlebnis ändert sich innerhalb einer Sitzung nicht, um die visuelle Konsistenz zu gewährleisten.

## Das Personalisierungsmodell passt sich an Änderungen beim Besucherverhalten an

* Der &quot;mehrarmige Bandit&quot;stellt sicher, dass das Modell immer einen kleinen Teil des Traffics &quot;ausgibt&quot;, um während des gesamten Lebenszyklus der Aktivität weiter zu lernen und eine Übernutzung zuvor erlernter Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden anhand der neuesten Daten zum Besucherverhalten neu erstellt, um sicherzustellen, dass [!DNL Target] verwendet immer wechselnde Besuchervoreinstellungen.
* Wenn der Algorithmus keine Gewinnererlebnisse für einzelne Besucher bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) ermittelt.

## Das Modell optimiert kontinuierlich eine einzige Zielmetrik

* Diese Metrik kann auf Konversionen oder Umsätzen (genauer gesagt: [!UICONTROL Umsatz pro Besucher]) basieren.

## [!DNL Target] sammelt automatisch Informationen über Besucher, um Personalisierungsmodelle zu erstellen

* Weitere Informationen zu den Attributen, die für [!UICONTROL automatisches Targeting] und [!UICONTROL automatisierte Personalisierung] verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] verwendet automatisch alle[!DNL Adobe Experience Cloud] von gemeinsam genutzten Zielgruppen, um diese Personalisierungsmodelle zu erstellen

* Sie müssen nichts Spezifisches tun, um Zielgruppen zum Modell hinzuzufügen. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

## Marketer können für die Erstellung von Personalisierungsmodellen Offline-Daten, Propensity Scores oder andere benutzerdefinierte Daten hochladen

Offline-Daten wie CRM-Informationen oder Tendenzwerte bei Kunden-Abwanderungen können beim Erstellen von Personalisierungsmodellen von unschätzbarem Wert sein. Es gibt verschiedene Möglichkeiten für die Dateneingabe in die Algorithmen zur [!UICONTROL automatisierten Personalisierung] (AP) und zum [!UICONTROL automatischen Targeting].

* [Mbox-Parameter](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}
* [Profilparameter](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}
* [Serverseitige APIs für das Profil-Update](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen der [!UICONTROL automatisierten Personalisierung] und des [!UICONTROL automatischen Targetings] gesammelt und verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Schulungsvideo: Aktivitätstypen

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Automatisierte Personalisierung wird ab 5:55 besprochen.]

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
