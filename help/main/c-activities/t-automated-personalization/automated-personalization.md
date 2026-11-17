---
keywords: Automated Personalization;App;Zielgruppen;Ensemble;Random Forest;Multi-Armed Bandit;Thompson-Stichprobenverfahren;ml;maschinelles Lernen
description: Erfahren Sie, wie Sie [!UICONTROL Automated Personalization]-Aktivitäten (AP) in [!DNL Adobe Target] verwenden, die mithilfe des erweiterten maschinellen Lernens verschiedene Angebotsvarianten für jede Besucherin und jeden Besucher abgleichen.
title: Was ist eine [!UICONTROL Automated Personalization]-Aktivität (AP)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
TQID: 'https://experienceleague.adobe.com/BBtKgNRTlqNFFoAjr1LQkhHyZeAlXG2h8D7bsndh4kQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 15%
---
# [!UICONTROL Automated Personalization] (AP) {#automated-personalization-overview}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie eine **[!UICONTROL Automated Personalization]**-Aktivität den Angebotsvarianten jedes Besuchers entspricht und was bei der Verwendung zu beachten ist.

>[!ENDSHADEBOX]

>[!NOTE]
>
>**[!UICONTROL Automated Personalization]** ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md#premium).

**[!UICONTROL Automated Personalization]** (AP)-Aktivitäten in [!DNL Adobe Target] kombinieren Angebote oder Nachrichten und passen mithilfe des erweiterten maschinellen Lernens basierend auf ihrem individuellen Kundenprofil verschiedene Angebotsvarianten an einzelne Besuchende an, um Inhalte zu personalisieren und die Steigerung zu fördern.

Marketing-Experten implementieren eine Datei auf ihrer Site, damit sie auf beliebige Inhalte zeigen und klicken können, und erstellen dann mit dem **[!UICONTROL Visual Experience Composer]** (VEC) visuell zusätzliche Inhaltsoptionen für diesen Bereich. Der Algorithmus bestimmt dann automatisch, welcher Inhalt für jeden Besucher bereitgestellt werden soll, basierend auf allen Verhaltensdaten, die das System über diesen Besucher hat.

**[!UICONTROL Automated Personalization]** passt sich an Änderungen im Besucherverhalten an, sodass es ohne festgelegtes Enddatum ausgeführt werden kann, um eine fortlaufende Steigerung und Personalisierung bereitzustellen. Dieser Modus wird manchmal als „Always-on“ bezeichnet. Der Marketer muss keinen Test durchführen, die Ergebnisse analysieren und dann einen Gewinner liefern, bevor er die Steigerung realisiert. **[!UICONTROL Automated Personalization]** ist auch in der Discovery-Phase von Tests und bei der Auswahl verschiedener Besucher hilfreich. Weitere Informationen zu den Unterschieden zwischen automatischem **[!UICONTROL und]** finden Sie [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Die folgenden Begriffe sind bei der Diskussion von **[!UICONTROL Automated Personalization hilfreich]**:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Ein führender Ansatz für maschinelles Lernen. In datenwissenschaftlicher Hinsicht handelt es sich um eine Ensemble-Klassifizierungs- oder Regressionsmethode, bei der viele Entscheidungsbäume basierend auf Besucher- und Besuchsattributen erstellt werden. |
| Thompson Sampling | Das Ziel des Thompson-Stichprobenverfahrens besteht darin, festzustellen, welches Erlebnis insgesamt am besten ist (nicht personalisiert), und gleichzeitig die „Kosten“ für das Auffinden dieses Erlebnisses zu minimieren. Beim Thompson-Stichprobenverfahren wird immer ein Gewinner ausgewählt, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Funktionsweise des Personalisierungsmodells {#how-ap-works}

**[!UICONTROL Automated Personalization]** verwendet zur Personalisierung einen Algorithmus der zufälligen Gesamtstruktur. Random Forest ist ein führender Ansatz für maschinelles Lernen. In datenwissenschaftlicher Hinsicht handelt es sich um eine Ensemble-Klassifizierungs- oder Regressionsmethode, bei der viele Entscheidungsbäume basierend auf Besucher- und Besuchsattributen erstellt werden. In [!DNL Target] wird mithilfe der Zufallsstruktur bestimmt, welches Erlebnis für jeden einzelnen Besucher die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) aufweist.

Besucherinnen und Besucher, die beispielsweise Chrome verwenden, Mitglieder des Treueprogramms Gold sind und dienstags auf Ihre Website zugreifen, konvertieren möglicherweise eher mit Erlebnis A. Besucherinnen und Besucher aus New York konvertieren möglicherweise eher mit Erlebnis B.

Weitere Informationen zu Random Forest in [!DNL Target] finden Sie unter [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

| Aspekt | Funktionsweise |
|---|---|
| **Optimierung für jeden Besuch** | Der Algorithmus sagt die Wahrscheinlichkeit voraus, mit der ein Besucher konvertiert wird (oder den geschätzten Umsatz aus der Konversion), um das beste Erlebnis zu bieten. Ein Besucher hat Anspruch auf ein neues Erlebnis am Ende einer vorhandenen Sitzung, es sei denn, er gehört zur Kontrollgruppe. Ein Besucher in der Kontrollgruppe sieht dasselbe Erlebnis wie beim ersten Besuch. Das Erlebnis ändert sich innerhalb einer Sitzung nicht, um die visuelle Konsistenz zu wahren. |
| **Anpassung an Änderungen im Besucherverhalten** | Der mehrarmige Bandit gibt immer einen kleinen Teil des Traffics aus, um während des ganzen Aktivitätslebens weiter zu lernen und eine Übernutzung der bereits erlernten Trends zu verhindern. Die zugrunde liegenden Modelle werden alle 24 Stunden mit den neuesten Daten zum Besucherverhalten neu erstellt. Wenn der Algorithmus keine Gewinnererlebnisse für einzelne Besucher ermitteln kann, zeigt er das insgesamt beste Erlebnis an, das mithilfe des [Thompson-Stichprobenverfahrens](https://en.wikipedia.org/wiki/Thompson_sampling) ermittelt wurde, während er weiterhin nach personalisierten Gewinnern sucht. |
| **Zielmetrik** | Das Modell optimiert kontinuierlich eine einzelne Zielmetrik, die konversionsbasiert oder umsatzbasiert sein kann (genauer gesagt, &quot;**[!UICONTROL pro Besuch]**). |
| **Daten und Audiences** | [!DNL Target] erfasst automatisch Informationen über Besucher, um die Personalisierungsmodelle zu erstellen. Weitere Informationen zu den in {**[!UICONTROL }Automatisches Targeting]** und **[!UICONTROL Automated Personalization]** verwendeten Attributen finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md). [!DNL Target] verwendet auch automatisch alle [!DNL Adobe Experience Cloud] freigegebenen Zielgruppen. Daher müssen Sie nichts Bestimmtes tun, um Zielgruppen zum Modell hinzuzufügen. Weitere Informationen finden Sie unter [Experience Cloud-Zielgruppen](/help/main/c-integrating-target-with-mac/mmp.md). |
| **Benutzerdefinierte Daten** | Marketing-Experten können Offline-Daten wie CRM-Informationen oder Tendenzwerte zur Kundenabwanderung oder andere benutzerdefinierte Daten hochladen, um Personalisierungsmodelle zu erstellen. Die Daten können mit [Mbox-Parametern](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}, [Profilparametern](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank} oder [Server-seitigen APIs für die Profilaktualisierung) &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}. |

## Schulungsvideo: Aktivitätstypen {#training-video}

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. **[!UICONTROL Automated Personalization]** wird ab 17:55 Uhr besprochen.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
