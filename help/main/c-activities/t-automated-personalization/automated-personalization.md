---
keywords: Automated Personalization;App;Zielgruppen;Ensemble;Random Forest;Multi-Armed Bandit;Thompson-Stichprobenverfahren;ml;maschinelles Lernen
description: Erfahren Sie, wie Sie [!UICONTROL Automated Personalization] (AP)-Aktivitäten in verwenden [!DNL Adobe Target]  die mithilfe von erweitertem maschinellem Lernen verschiedene Angebotsvarianten für jeden Besucher abgleichen.
title: Was ist eine [!UICONTROL Automated Personalization] (AP)-Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
TQID: https://experienceleague.adobe.com/BBtKgNRTlqNFFoAjr1LQkhHyZeAlXG2h8D7bsndh4kQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1003
ht-degree: 31%

---

# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP)-Aktivitäten in [!DNL Adobe Target] kombinieren Angebote oder Nachrichten und ordnen den einzelnen Besuchern basierend auf ihrem individuellen Kundenprofil durch erweitertes maschinelles Lernen verschiedene Angebotsvarianten zu, um Inhalte zu personalisieren und die Steigerung zu fördern.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md#premium).

Ähnlich wie [!UICONTROL Auto-Target] verwendet [!UICONTROL Automated Personalization] einen [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Datenwissenschafts-Ensemble-Methode, als wichtigsten Personalisierungsalgorithmus, um das beste Erlebnis für einen Besucher zu ermitteln. [!UICONTROL Automated Personalization] kann in der Erkennungsphase von Tests nützlich sein. Es ist zudem nützlich, maschinelles Lernen zu ermöglichen, um den effektivsten Inhalt zu bestimmen, wenn man unterschiedliche Besucher anspricht. Im Lauf der Zeit lernt der Algorithmus, die effektivsten Inhalte vorherzusagen, und zeigt die Inhalte an, die am wahrscheinlichsten zum Erreichen Ihrer Ziele beitragen.

Weitere Informationen zu den Unterschieden zwischen [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Marketing-Experten implementieren eine Datei auf ihrer Site, damit sie auf einen beliebigen Inhalt zeigen und klicken können. Anschließend können sie mithilfe des [!UICONTROL Visual Experience Composer] (VEC) visuell zusätzliche Inhaltsoptionen für diesen Bereich erstellen und auswählen. Dann bestimmt der Algorithmus auf Basis aller Verhaltensdaten, die das System über diesen Besucher hat, automatisch, welche Inhalte jedem einzelnen Besucher gezeigt werden sollen, und liefert so eine personalisierte Erfahrung. Da [!UICONTROL Automated Personalization] sich an Änderungen im Besucherverhalten anpassen können, kann sie ohne festgelegtes Enddatum ausgeführt werden, um eine kontinuierliche Steigerung und Personalisierung bereitzustellen. Dieser Modus wird manchmal als „Always-on“ bezeichnet. Der Marketer muss keine Tests durchführen, keine Ergebnisse analysieren und keinen sich daraus ergebenen Gewinner ermitteln, bevor er erkennen kann, welche Steigerung sich aus der Optimierung ergibt. Das übernimmt eine festgelegte Reihenfolge von Operationen, die dann das Ergebnis einer standardmäßigen A/B-Aktivität implementiert.

Die folgenden Begriffe sind bei der Erörterung von [!UICONTROL Automated Personalization] hilfreich:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Ein führender Ansatz für maschinelles Lernen. In datenwissenschaftlicher Hinsicht handelt es sich um eine Ensemble-Klassifizierungs- oder Regressionsmethode, bei der viele Entscheidungsbäume basierend auf Besucher- und Besuchsattributen erstellt werden. |
| Thompson Sampling | Das Ziel des Thompson-Stichprobenverfahrens besteht darin, festzustellen, welches Erlebnis insgesamt am besten ist (nicht personalisiert), und gleichzeitig die „Kosten“ für das Auffinden dieses Erlebnisses zu minimieren. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

Beachten Sie bei der Verwendung von [!UICONTROL Automated Personalization] die folgenden Details:

## [!UICONTROL Automated Personalization] verwendet einen Algorithmus der zufälligen Gesamtstruktur zur Personalisierung

Random Forest ist ein führender Ansatz für maschinelles Lernen. In datenwissenschaftlicher Hinsicht handelt es sich um eine Ensemble-Klassifizierungs- oder Regressionsmethode, bei der viele Entscheidungsbäume basierend auf Besucher- und Besuchsattributen erstellt werden. In [!DNL Target] wird mithilfe der Zufallsstruktur bestimmt, welches Erlebnis für jeden einzelnen Besucher die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) aufweist. Besucherinnen und Besucher, die beispielsweise Chrome verwenden, Mitglieder des Treueprogramms Gold sind und dienstags auf Ihre Website zugreifen, konvertieren möglicherweise eher mit Erlebnis A. Besucherinnen und Besucher aus New York konvertieren möglicherweise eher mit Erlebnis B. Weitere Informationen zu Random Forest in [!DNL Target] finden Sie unter [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Das Personalisierungsmodell wird für jeden Besuch optimiert

* Der Algorithmus sagt die Konversionswahrscheinlichkeit eines Besuchers (oder den geschätzten Umsatz aus der Konversion) voraus, um das beste Erlebnis zu erzielen.
* Ein Besucher hat am Ende einer vorhandenen Sitzung Anspruch auf ein neues Erlebnis, es sei denn, er gehört zur Kontrollgruppe. Wenn sich der Besucher in der Kontrollgruppe befindet, entspricht das Erlebnis, das der Besucher beim ersten Besuch sieht, dem Erlebnis bei nachfolgenden Besuchen.
* Das präsentierte Erlebnis ändert sich innerhalb einer Sitzung nicht, um die visuelle Konsistenz zu wahren.

## Das Personalisierungsmodell passt sich an Änderungen im Besucherverhalten an

* Der mehrarmige Bandit stellt sicher, dass das Modell immer einen kleinen Teil des Traffics „ausgibt“, um während des gesamten Lebens der Aktivität weiter zu lernen und eine Übernutzung zuvor gelernter Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden mit den neuesten Daten zum Besucherverhalten neu erstellt, um sicherzustellen, dass [!DNL Target] immer die sich ändernden Besuchervoreinstellungen verwendet.
* Wenn der Algorithmus keine Gewinnererlebnisse für einzelne Besucher bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) ermittelt.

## Das Modell optimiert kontinuierlich eine einzelne Zielmetrik

* Diese Metrik kann konversionsbasiert oder umsatzbasiert sein (genauer gesagt, [!UICONTROL Revenue per Visitor]).

## [!DNL Target] erfasst automatisch Informationen über Besucher, um die Personalisierungsmodelle zu erstellen

* Weitere Informationen zu den in [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] verwendeten Attributen finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] verwendet automatisch alle [!DNL Adobe Experience Cloud] freigegebenen Zielgruppen, um die Personalisierungsmodelle zu erstellen

* Sie müssen nichts Bestimmtes tun, um Zielgruppen zum Modell hinzuzufügen. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

## Marketing-Experten können Offline-Daten, Tendenzwerte oder andere benutzerdefinierte Daten hochladen, um Personalisierungsmodelle zu erstellen

Offline-Daten wie CRM-Informationen oder Tendenzwerte zur Kundenabwanderung können beim Erstellen von Personalisierungsmodellen unglaublich wertvoll sein. Es gibt mehrere Möglichkeiten, Daten in [!UICONTROL Automated Personalization] (AP) einzugeben und Personalisierungsalgorithmen zu [!UICONTROL Auto-Target].

* [Mbox-Parameter](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}
* [Profilparameter](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}
* [Serverseitige APIs für Profilupdate](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}

Informationen zu den automatisch von [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] Personalisierungsalgorithmen erfassten und verwendeten Daten finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Schulungsvideo: Aktivitätstypen

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Automated Personalization] wird ab 5 Uhr :55.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/29397?captions=ger)
