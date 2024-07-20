---
keywords: automatisierte Personalisierung;App;Zielgruppen;Ensemble;Random Forest;Multi-Armed Bandit;Thompson Sampling;ml;maschinelles Lernen
description: Erfahren Sie, wie Sie in [!DNL Adobe Target] Aktivitäten mit dem Typ [!UICONTROL Automated Personalization] (AP) verwenden, die mithilfe des erweiterten maschinellen Lernens verschiedene Angebotsvarianten den einzelnen Besuchern zuordnen.
title: Was ist eine AP-Aktivität (0)?[!UICONTROL Automated Personalization]
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 28%

---

# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP)-Aktivitäten in [!DNL Adobe Target] kombinieren Angebote oder Nachrichten und verwenden das erweiterte maschinelle Lernen, um den einzelnen Besuchern basierend auf ihrem individuellen Kundenprofil verschiedene Angebotsvarianten zuzuordnen, um die Inhalte zu personalisieren und die Steigerung zu fördern.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] ist als Teil der [!DNL Target Premium] -Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md#premium).

Ähnlich wie bei [!UICONTROL Auto-Target] verwendet [!UICONTROL Automated Personalization] einen [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Methode in der Datenwissenschaft, als wichtigsten Personalisierungsalgorithmus, um das beste Erlebnis für die Anzeige eines Besuchers zu ermitteln. [!UICONTROL Automated Personalization] kann in der Entdeckungsphase des Testens nützlich sein. Es ist zudem nützlich, maschinelles Lernen zu ermöglichen, um den effektivsten Inhalt zu bestimmen, wenn man unterschiedliche Besucher anspricht. Im Lauf der Zeit lernt der Algorithmus, die effektivsten Inhalte vorherzusagen, und zeigt die Inhalte an, die am wahrscheinlichsten zum Erreichen Ihrer Ziele beitragen.

Weitere Informationen dazu, wie sich [!UICONTROL Automated Personalization] von [!UICONTROL Auto-Target] unterscheidet, finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Marketingexperten implementieren eine Datei auf ihrer Website, mit der sie auf einen beliebigen Inhalt zeigen und klicken und dann mithilfe des VEC (0) visuell zusätzliche Inhaltsoptionen für diesen Bereich erstellen und auswählen können. [!UICONTROL Visual Experience Composer] Dann bestimmt der Algorithmus auf Basis aller Verhaltensdaten, die das System über diesen Besucher hat, automatisch, welche Inhalte jedem einzelnen Besucher gezeigt werden sollen, und liefert so eine personalisierte Erfahrung. Da sich [!UICONTROL Automated Personalization] an Änderungen im Besucherverhalten anpassen kann, kann es ohne ein festgelegtes Enddatum ausgeführt werden, um eine kontinuierliche Steigerung und Personalisierung zu ermöglichen. Dieser Modus wird manchmal als &quot;Always-on&quot;bezeichnet. Der Marketer muss keine Tests durchführen, keine Ergebnisse analysieren und keinen sich daraus ergebenen Gewinner ermitteln, bevor er erkennen kann, welche Steigerung sich aus der Optimierung ergibt. Das übernimmt eine festgelegte Reihenfolge von Operationen, die dann das Ergebnis einer standardmäßigen A/B-Aktivität implementiert.

Die folgenden Begriffe sind bei der Erörterung von [!UICONTROL Automated Personalization] nützlich:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Ein führender Ansatz für maschinelles Lernen. In datenwissenschaftlichen Begriffen ist es eine Ensemble-Classification- oder Regressionsmethode, die durch die Erstellung vieler Entscheidungsbäume auf der Grundlage von Besuchsattributen und Besuchsattributen funktioniert. |
| Thompson Sampling | Ziel des Thompson-Samplings ist es, zu ermitteln, welches Erlebnis insgesamt das beste (nicht personalisierte) Erlebnis ist, und gleichzeitig die &quot;Kosten&quot;für die Suche nach diesem Erlebnis zu minimieren. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

Beachten Sie bei Verwendung von [!UICONTROL Automated Personalization] die folgenden Details:

## [!UICONTROL Automated Personalization] verwendet einen Random Forest-Algorithmus zur Personalisierung

Random Forest ist ein führender Ansatz des maschinellen Lernens. In datenwissenschaftlichen Begriffen ist es eine Ensemble-Classification- oder Regressionsmethode, die durch die Erstellung vieler Entscheidungsbäume auf der Grundlage von Besuchsattributen und Besuchsattributen funktioniert. Innerhalb von [!DNL Target] wird Random Forest verwendet, um zu bestimmen, welches Erlebnis die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) für jeden bestimmten Besucher aufweist. Beispielsweise können Besucher, die Chrome verwenden, Mitglieder des Treueprogramms &quot;Gold&quot;sind und am Dienstag auf Ihre Site zugreifen, mit höherer Wahrscheinlichkeit mit Erlebnis A konvertieren. Besucher aus New York können eher mit Erlebnis B konvertieren. Weitere Informationen zu Random Forest in [!DNL Target] finden Sie unter [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Das Personalisierungsmodell wird für jeden Besuch optimiert

* Der Algorithmus prognostiziert die Wahrscheinlichkeit einer Konversion (oder des geschätzten Umsatzes aus der Konversion) eines Besuchers, um das beste Erlebnis bereitzustellen.
* Ein Besucher ist zum Ende einer bestehenden Sitzung für ein neues Erlebnis qualifiziert, es sei denn, dieser Besucher gehört zur Kontrollgruppe. Wenn sich der Besucher in der Kontrollgruppe befindet, ist das Erlebnis, das der Besucher beim ersten Besuch sieht, dasselbe wie bei nachfolgenden Besuchen.
* Das angezeigte Erlebnis ändert sich innerhalb einer Sitzung nicht, um die visuelle Konsistenz zu gewährleisten.

## Das Personalisierungsmodell passt sich an Änderungen im Besucherverhalten an

* Der &quot;mehrarmige Bandit&quot;stellt sicher, dass das Modell immer einen kleinen Teil des Traffics &quot;ausgibt&quot;, um während des gesamten Lebenszyklus der Aktivität weiter zu lernen und eine Übernutzung zuvor erlernter Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden anhand der neuesten Daten zum Besucherverhalten neu erstellt, um sicherzustellen, dass [!DNL Target] immer wechselnde Besucherpräferenzen verwendet.
* Wenn der Algorithmus keine Gewinnererlebnisse für einzelne Besucher bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) ermittelt.

## Das Modell optimiert kontinuierlich eine einzige Zielmetrik

* Diese Metrik kann auf Konversionen oder Umsätzen basieren (genauer gesagt: [!UICONTROL Revenue per Visitor]).

## [!DNL Target] erfasst automatisch Informationen über Besucher, um die Personalisierungsmodelle zu erstellen

* Weitere Informationen zu den Attributen, die in [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] verwendet werden, finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] verwendet automatisch alle [!DNL Adobe Experience Cloud] freigegebenen Zielgruppen zum Erstellen der Personalisierungsmodelle

* Sie müssen nichts Spezifisches tun, um Zielgruppen zum Modell hinzuzufügen. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

## Marketer können Offline-Daten, Tendenzwerte oder andere benutzerdefinierte Daten hochladen, um Personalisierungsmodelle zu erstellen

Offline-Daten wie CRM-Informationen oder Tendenzwerte bei Kunden-Abwanderungen können beim Erstellen von Personalisierungsmodellen von unschätzbarem Wert sein. Es gibt mehrere Möglichkeiten, Daten in die Personalisierungsalgorithmen [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] einzugeben.

* [mbox-Parameter](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}
* [Profilparameter](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}
* [Server-seitige APIs für Profil-Update](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] erfasst und verwendet werden, finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Schulungsvideo: Aktivitätstypen

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Automated Personalization] wird ab 05:55 besprochen.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
