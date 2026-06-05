---
keywords: AEM;Experience Manager;Adobe Experience Manager;integrieren;Integration;Experience Fragments;Inhaltsfragmente
description: Erfahren Sie, wie Sie Experience Fragments und Inhaltsfragmente aus  [!DNL Adobe Experience Manager]  in  [!DNL Adobe Target] -Aktivitäten verwenden.
title: Wie verwende ich ( [!DNL Adobe Experience Manager] ) [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente]?
feature: Integrations
exl-id: 6f1a02da-8f59-4a8b-8e97-c20444ef53c8
TQID: https://experienceleague.adobe.com/OlgveSjoE0rh1orFsbEZVCSbjd3TKEk8fdBbbXtLxhA
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e6ff21d3-dec6-4298-8590-7c749fffaf78
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 40%

---

# Übersicht über [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] von AEM

Verwenden Sie [!UICONTROL Experience Fragments] (XFs) und [!UICONTROL Inhaltsfragmente] (CFs), die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target] Aktivitäten zur Optimierung und Personalisierung.

Durch die Verwendung von [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmenten] die in [!DNL AEM] erstellt wurden, in [!DNL Target] -Aktivitäten können Sie die Benutzerfreundlichkeit und Leistungsfähigkeit von [!DNL AEM] mit den leistungsstarken Funktionen für künstliche Intelligenz (KI) und maschinelles Lernen (ML) in [!DNL Target] kombinieren, um Erlebnisse in großem Umfang zu testen und zu personalisieren.

[!DNL AEM] kombiniert all Ihre Inhalte und Kreativelemente an einem zentralen Ort, um Sie bei Ihrer Personalisierungsstrategie zu unterstützen. Mit [!DNL AEM] können Sie von einem zentralen Ort aus problemlos Inhalte für Desktops, Tablets und Smartphones erstellen, ohne Code zu schreiben. Es ist nicht erforderlich, Seiten für jedes Gerät zu erstellen. [!DNL AEM] nimmt Ihre Inhalte und passt jedes Erlebnis automatisch für jedes Gerät an.

Mit [!DNL Target] können Sie personalisierte Erlebnisse in großem Umfang bereitstellen. Dies erfolgt auf der Grundlage einer Kombination aus regelbasierten und AI-gestützten Ansätzen des maschinellen Lernens, zu denen Verhaltens-, Kontext- und Offline-Variablen zählen.

[!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind ein großer Schritt vorwärts, um bei der Erstellung und Verwaltung von Inhalten und Erlebnissen die Optimierungs- und Personalisierungsfachleute einzubinden, die Geschäftsergebnisse mithilfe von [!DNL Target] optimieren.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmenten] in [!DNL Target]:
* Diese Funktionen erfordern, dass Sie Kundin oder Kunde von [!DNL Adobe Experience Manager] (AEM) sind. Stellen Sie sicher, dass Sie die Anforderungen für jeden Fragmenttyp erfüllen: [Experience Fragment](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md#requirements) oder [Inhaltsfragment](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md#requirements).
* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind für die folgenden Aktivitätstypen verfügbar:

   * [[!UICONTROL A/B-Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Automatische Zuordnung]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Automatisches Targeting]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind für die folgenden Aktivitätstypen nicht verfügbar:

   * [[!UICONTROL Multivariate Tests] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* Sie können [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten mit dem [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md).
* Sie können [!UICONTROL Inhaltsfragmente] nur in [!DNL Target] Aktivitäten aufnehmen, die den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden.

## Was ist der Unterschied zwischen [!UICONTROL Experience &#x200B;]Inhaltsfragmenten[!UICONTROL &#x200B; und &#x200B;]?

[!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] können auf der Oberfläche ähnlich aussehen, aber jeder Fragmenttyp spielt Schlüsselrollen in verschiedenen Anwendungsfällen.

Weitere Informationen dazu, wo [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] ähnlich sind und wo sie sich unterscheiden sowie dazu, wann und wie welcher Typ verwendet wird, finden Sie unter [Grundlegendes zu [!UICONTROL Inhaltsfragmenten] und [!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/content-fragments/understand-content-fragments-and-experience-fragments.html?lang=de){target=_blank} im [Handbuch zu AEM Sites-Videos und -Tutorials](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/overview.html?lang=de){target=_blank}.
