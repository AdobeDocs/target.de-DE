---
keywords: AB;A/B;AB…n;Erlebnisse vergleichen;Targeting;Inhalt vergleichen;Automatisches Targeting;Automatische Zuordnung
description: Erkunden Sie die Aktivitäten von A/B-Tests in [!DNL Target] - , [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting].
title: Lernen Sie die in [!DNL Target] verfügbaren A/B-Test -Aktivitäten kennen.
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
TQID: 'https://experienceleague.adobe.com/wcflYDj0VB7dJODNO6XjFHB0PPIhN4aUrBJxbKPoNdg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: d887712962ad4e3cecd6b3b86ee33a4bcb99f2a8
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 19%
---
# A/B-Tests - Übersicht {#test-ab}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, was ein manueller A/B-Test ist, wann er anstelle eines Multivarianz-Tests verwendet wird und wie er mit den Aktivitätstypen Automatische Zuordnung und Automatisches Targeting in Beziehung steht.

>[!ENDSHADEBOX]

Eine manuelle **[!UICONTROL A/B-Test]**-Aktivität (manchmal auch als A/B…N-Test bezeichnet) vergleicht zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen, Verkäufe oder anderen von Ihnen identifizierten Metriken am besten erhöht. Verwenden Sie einen A/B-Test, um Änderungen an Ihrer Seite mit dem Design Ihrer Standardseite zu vergleichen und zu ermitteln, welches Erlebnis für das beste Ergebnis sorgt.

## Verwendung eines manuellen A/B-Tests {#when-to-use}

Verwenden Sie einen manuellen A/B-Test, wenn:

* Sie haben eine klare Hypothese dazu, wie Sie die Leistung Ihrer Seite verbessern können, basierend auf Erfolgsmetriken oder der Bereitstellung alternativer Inhalte.
* Sie möchten große Änderungen testen, z. B. neue Layouts oder grundlegend andere Behandlungen der Elemente. Wenn Ihr Testdesign nicht einfach in einzelne Seitenelemente unterteilt werden kann, sollten Sie einen A/B-Test durchführen, bevor Sie einen [Multivarianz-Test) &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).
* Sie möchten den Prozentsatz der Besucherinnen und Besucher bestimmen, die die einzelnen Erlebnisse sehen. Sie können beispielsweise den Traffic gleichmäßig auf das Steuerelement und ein zweites Erlebnis aufteilen oder ein neues, riskanteres Erlebnis testen, indem Sie es nur 5 % Ihrer Zielgruppe zeigen.

Detaillierte Informationen zum Ermitteln der optimalen Stichprobengröße für einen A/B-Test finden Sie unter [Planen Ihrer A/B-Tests](/help/main/c-activities/t-test-ab/sample-size-determination.md).

### Kombinieren von Multivarianz- und A/B-Tests

Wenn mehr als fünf Erlebnisse an zwei oder mehr Orten vorhanden sind, empfiehlt es sich, einen [MVT-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) in Betracht zu ziehen, bevor Sie Ihre A/B-Tests durchführen:

1. **Führen Sie einen Multivarianz-Test**, um zu sehen, welche Bereiche auf der Seite die Konvertierung am ehesten verbessern. Dies sind die Orte, auf die sich ein Marketer konzentrieren sollte. So kann ein Multivarianz-Test zum Beispiel zeigen, dass ein Aktionsaufruf der wichtigste Ort zur Erreichung Ihrer Ziele ist.

1. **Führen Sie einen oder mehrere A/B-** an diesen Orten aus, um die Ergebnisse weiter zu verfeinern. So können Sie beispielsweise zwei bestimmte Bilder miteinander testen oder den Wortlaut oder die Farben einer call to action vergleichen.

Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

## Typen von A/B-Test-Aktivitäten {#types}

Zusätzlich zur manuellen Aktivität **[!UICONTROL A/B-Test]** bietet [!DNL Target] zwei zusätzliche Typen von **[!UICONTROL A/B-]**: **[!UICONTROL Automatische Zuordnung]** und **[!UICONTROL Automatisches Targeting]**.

| Aktivitätstyp | Beschreibung |
| --- | --- |
| **[!UICONTROL Manueller A/B-Test]** | Vergleicht zwei oder mehr Erlebnisse, um zu prüfen, welches Erlebnis über einen zuvor definierten Testzeitraum Konversionen am meisten verbessert.<P>In diesem Abschnitt wird beschrieben, wie Sie eine manuelle **[!UICONTROL A/B-Test]**-Aktivität einrichten. Die Schritte für die anderen Arten von **[!UICONTROL A/B-Test]**-Aktivitäten sind jedoch ähnlich. |
| **[!UICONTROL Automatische Zuordnung]** | Ermittelt einen Gewinner aus zwei oder mehr Erlebnissen und leitet den Traffic dann zum Gewinner weiter, wodurch die Konversionsrate mit dem Testlauf und dem Lernen steigt.<P>Weitere Informationen zu den Vorteilen der Verwendung einer Aktivität **[!UICONTROL Automatische Zuordnung]** finden Sie unter [Automatische Zuordnung](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Wie lange sollten A/B-Tests durchgeführt werden* und [Automatische Zuordnung - Überblick](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium-Badge](/help/main/assets/premium.png) **[!UICONTROL Automatisches Targeting]** | Verwendet fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen durch Identifizierung eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen. Anschließend wird den Besuchern das passendste Erlebnis auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher bereitgestellt.<P>Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Weitere Informationen dazu, welche dieser **[!UICONTROL A/B-Test]**-Aktivitäten für Sie am besten geeignet ist, finden Sie im interaktiven Handbuch zu [Adobe Target-Aktivitäten in PDF](/help/main/c-activities/target-activities-guide.md).

>[!NOTE]
>
>Sie können Empfehlungen in **[!UICONTROL A/B-]**-, **[!UICONTROL Automatische Zuordnung]**- und **[!UICONTROL Automatisches Targeting]**-Aktivitäten (und **[!UICONTROL Experience Targeting]** (XT) einbeziehen. Weitere Informationen finden Sie unter [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen.
