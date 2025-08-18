---
keywords: AB;A/B;AB…n;Erlebnisse vergleichen;Targeting;Inhalt vergleichen;Automatisches Targeting;Automatische Zuordnung
description: Erfahren Sie mehr über die verschiedenen Arten von A/B-Test -Aktivitäten in Adobe [!DNL Target]  Manuell, Automatische Zuordnung und Automatisches Targeting. Wählen Sie die für Sie richtige aus.
title: Welche Arten von A/B-Aktivitäten sind in Target verfügbar?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: 974746e25724abf0e5edd3884331ec0975e5352e
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 24%

---

# A/B-Tests - Übersicht

Eine manuelle [!UICONTROL A/B Test] vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.

>[!NOTE]
>
>Zusätzlich zur manuellen [!UICONTROL A/B Test] (Standard) (siehe diesen Abschnitt) bietet [!DNL Target] zwei weitere Arten von [!UICONTROL A/B Test]: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]. Weitere Informationen finden [ unter „Arten von A/B](#types)Testaktivitäten“.

Eine manuelle [!UICONTROL A/B Test] (manchmal auch als A/B…N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am besten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

Manuelle A/B-Tests sind nützlich, wenn Sie anhand von Erfolgsmetriken oder alternativen Inhaltsbereitstellungen eine klare Hypothese darüber haben, wie Sie die Leistung Ihrer Seite verbessern können.

Manuelle A/B-Tests eignen sich für große Änderungen, die mit neuen Layouts oder grundlegend anderen Behandlungen der Elemente verbunden sein können. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente zerfällt, sollten Sie vor einem (multivariaten [) einen A/B-Test ](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Wenn Sie Ihren A/B-Test einrichten, können Sie den Prozentsatz der Besucher ermitteln, die die einzelnen Erlebnisse sehen. Sie könnten beispielsweise den Traffic gleichmäßig zwischen dem Kontrollerlebnis und einem zweiten Erlebnis aufteilen, oder Sie könnten ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wenn mehr als fünf Erlebnisse an zwei oder mehr Orten vorhanden sind, empfiehlt es sich, einen [MVT-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) in Betracht zu ziehen, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Orte, auf die sich ein Marketer konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Speicherorte und Inhalte für Ihre Ziele am nützlichsten sind, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. So können Sie beispielsweise zwei bestimmte Bilder miteinander testen oder den Wortlaut oder die Farben einer call to action vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Test-Aktivitäten {#types}

Zusätzlich zur manuellen [!UICONTROL A/B Test] (siehe diesen Abschnitt) bietet [!DNL Target] zwei weitere Arten von A/B-Testaktivitäten: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergleicht zwei oder mehr Erlebnisse, um zu sehen, welches beste Erlebnis die Konversionen während eines vorab festgelegten Testzeitraums verbessert.<P>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle [!UICONTROL A/B Test]-Aktivität einrichten. Die Schritte für die anderen Arten von [!UICONTROL A/B Test]-Aktivitäten sind jedoch ähnlich. |
| [!UICONTROL Auto-Allocate] | Ermittelt einen Gewinner aus zwei oder mehr Erlebnissen und leitet den Traffic dann zum Gewinner weiter, wodurch die Konversionsrate mit dem Testlauf und dem Lernen steigt.<P>Weitere Informationen zu den Vorteilen der Verwendung einer [!UICONTROL Auto-Allocate]-Aktivität finden Sie unter [Automatische Zuordnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Wie lange sollten A/B-Tests durchgeführt werden* und [Automatische Zuordnung - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium-Badge](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Verwendet fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen durch Identifizierung eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen. Anschließend wird den Besuchern das passendste Erlebnis auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher bereitgestellt.<P>Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen dazu, welche dieser [!UICONTROL A/B Test] Aktivitäten für Sie am besten geeignet ist, finden Sie im interaktiven Handbuch zu [Adobe Target-Aktivitäten in PDF](/help/main/c-activities/target-activities-guide.md).

Die Schritte zum Erstellen der drei Arten von [!UICONTROL A/B Test] sind ähnlich. Um eine [!UICONTROL Auto-Allocate]- oder [!UICONTROL Auto-Target]-Aktivität zu erstellen, [ Sie zunächst eine A/B-Test -Aktivität ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md). Wenn Sie jedoch zur [!UICONTROL Targeting] gelangen, wählen Sie die gewünschte Traffic-Zuordnungsmethode aus, wie unten dargestellt:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Recommendations in A/B-Aktivitäten einschließen

Sie können Empfehlungen in [!UICONTROL A/B Test]-, [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten (und [!UICONTROL Experience Targeting] (XT)-Aktivitäten) einbeziehen. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

Für diese Funktion ist eine [Target Premium-Lizenz erforderlich](/help/main/c-intro/intro.md#premium)

## Schulungsvideo: Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
