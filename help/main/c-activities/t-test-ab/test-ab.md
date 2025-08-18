---
keywords: AB;A/B;AB…n;Erlebnisse vergleichen;Targeting;Inhalt vergleichen;Automatisches Targeting;Automatische Zuordnung
description: Erkunden Sie die Aktivitäten von A/B [!DNL Target] Tests in [!UICONTROL Manual], [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].
title: Lernen Sie die in verfügbaren A/B-Test-Aktivitäten  [!DNL Target].
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: 974746e25724abf0e5edd3884331ec0975e5352e
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 21%

---

# A/B-Tests - Übersicht

Eine manuelle [!UICONTROL A/B Test] (manchmal auch als A/B…N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am besten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

>[!TIP]
>
>Zusätzlich zur [!UICONTROL Manual]-Aktivität [!UICONTROL A/B Test] (Standard) (siehe diesen Artikel) bietet [!DNL Target] zwei weitere Arten von [!UICONTROL A/B Test]-Aktivitäten: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]. Weitere Informationen finden [ unter „Arten von A/B](#types)Testaktivitäten“.

Manuelle A/B-Tests sind nützlich, wenn Sie anhand von Erfolgsmetriken oder alternativen Inhaltsbereitstellungen eine klare Hypothese darüber haben, wie Sie die Leistung Ihrer Seite verbessern können.

Manuelle A/B-Tests eignen sich für große Änderungen, die mit neuen Layouts oder grundlegend anderen Behandlungen der Elemente verbunden sein können. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente unterteilt werden kann, sollten Sie einen A/B-Test durchführen, bevor Sie einen [Multivarianz-Test) ](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Wenn Sie Ihren A/B-Test einrichten, können Sie den Prozentsatz der Besucher ermitteln, die die einzelnen Erlebnisse sehen. Sie können beispielsweise den Traffic gleichmäßig auf das Steuerelement und ein zweites Erlebnis aufteilen oder ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

>[!NOTE]
>
>Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wenn mehr als fünf Erlebnisse an zwei oder mehr Orten vorhanden sind, empfiehlt es sich, einen [MVT-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) in Betracht zu ziehen, bevor Sie Ihre A/B-Tests durchführen. Der Multivariater Test zeigt, welche Bereiche auf der Seite aller Wahrscheinlichkeit nach die Konversion verbessern. Dies sind die Orte, auf die sich ein Marketer konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist. Nachdem Sie ermittelt haben, welche Speicherorte und Inhalte für Ihre Ziele am nützlichsten sind, können Sie einen A/B-Test durchführen, um die Ergebnisse weiter zu verfeinern. So können Sie beispielsweise zwei bestimmte Bilder miteinander testen oder den Wortlaut oder die Farben einer call to action vergleichen. Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Test-Aktivitäten {#types}

Zusätzlich zur manuellen [!UICONTROL A/B Test] bietet [!DNL Target] zwei zusätzliche Arten von [!UICONTROL A/B Testing]: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].

| Aktivitätstyp | Beschreibung |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergleicht zwei oder mehr Erlebnisse, um zu prüfen, welches Erlebnis über einen zuvor definierten Testzeitraum Konversionen am meisten verbessert.<P>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle [!UICONTROL A/B Test]-Aktivität einrichten. Die Schritte für die anderen Arten von [!UICONTROL A/B Test]-Aktivitäten sind jedoch ähnlich. |
| [!UICONTROL Auto-Allocate] | Ermittelt einen Gewinner aus zwei oder mehr Erlebnissen und leitet den Traffic dann zum Gewinner weiter, wodurch die Konversionsrate mit dem Testlauf und dem Lernen steigt.<P>Weitere Informationen zu den Vorteilen der Verwendung einer [!UICONTROL Auto-Allocate]-Aktivität finden Sie unter [Automatische Zuordnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Wie lange sollten A/B-Tests durchgeführt werden* und [Automatische Zuordnung - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium-Badge](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Verwendet fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen durch Identifizierung eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen. Anschließend wird den Besuchern das passendste Erlebnis auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher bereitgestellt.<P>Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen dazu, welche dieser [!UICONTROL A/B Test] Aktivitäten für Sie am besten geeignet ist, finden Sie im interaktiven Handbuch zu [Adobe Target-Aktivitäten in PDF](/help/main/c-activities/target-activities-guide.md).

Die Schritte zum Erstellen der drei Arten von [!UICONTROL A/B Test] sind ähnlich. So erstellen Sie eine [!UICONTROL Auto-Allocate] oder [!UICONTROL Auto-Target] Aktivität:

1. Erstellen [ zunächst eine A/B-Test -Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).
1. Wenn Sie zur Seite [!UICONTROL Targeting] gelangen, klicken Sie auf das [!UICONTROL Traffic Allocation] und wählen Sie dann die gewünschte Traffic-Zuordnungsmethode im rechten Bereich aus, wie unten dargestellt:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experience]

   ![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

## Recommendations in A/B-Aktivitäten einschließen

Sie können Empfehlungen in [!UICONTROL A/B Test]-, [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten (und [!UICONTROL Experience Targeting] (XT)-Aktivitäten) einbeziehen. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen.
