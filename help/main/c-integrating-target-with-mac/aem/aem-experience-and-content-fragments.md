---
keywords: AEM;Experience Manager;Adobe Experience Manager;integrieren;Integration;Experience Fragments;Inhaltsfragmente
description: Erfahren Sie, wie Sie Experience Fragments und Inhaltsfragmente aus  [!DNL Adobe Experience Manager]  in  [!DNL Adobe Target] -Aktivitäten verwenden.
title: Wie verwende ich [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] aus  [!DNL Adobe Experience Manager]  (AEM)?
feature: Integrations
source-git-commit: 0135831b56c48b0adca49e843c5ddd6574358aa4
workflow-type: ht
source-wordcount: '396'
ht-degree: 100%

---

# Übersicht über [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] aus AEM

Verwenden Sie [!UICONTROL Experience Fragments] (XFs) und [!UICONTROL Inhaltsfragmente] (CFs), die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten zur Optimierung oder Personalisierung.

>[!NOTE]
>
>Beachten Sie bei der Arbeit mit [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmenten] aus AEM in [!DNL Target] Folgendes:
> 
>* Diese Funktionen erfordern, dass Sie Kundin oder Kunde von [!DNL Adobe Experience Manager] (AEM) sind. Stellen Sie sicher, dass Sie die Anforderungen für jeden Fragmenttyp erfüllen: [Experience Fragment](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md#requirements) oder [Inhaltsfragment](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md#requirements).
>
>* Diese Funktionen sind für die folgenden Aktivitätstypen verfügbar: [!UICONTROL A/B-Test], [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting], [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Experience Targeting] (XT). Diese Funktion ist nicht verfügbar in Aktivitäten des Typs [!UICONTROL Multivariater Test] (MVT) und [!UICONTROL Recommendations].
>* Mit dem [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) können Sie [!UICONTROL Experience Fragments] in [!DNL Target]-Aktivitäten verwenden.
>
>* Sie können [!UICONTROL Inhaltsfragmente] nur im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden.


Durch die Verwendung von in [!DNL AEM] erstellten [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmenten] in [!DNL Target]-Aktivitäten können Sie die Benutzerfreundlichkeit und Leistungsfähigkeit von [!DNL AEM] mit den leistungsstarken Funktionen für künstliche Intelligenz (KI) und maschinelles Lernen (ML) in [!DNL Target] kombinieren, um Erlebnisse in großem Umfang zu testen und zu personalisieren.

[!DNL AEM] kombiniert all Ihre Inhalte und Kreativelemente an einem zentralen Ort, um Sie bei Ihrer Personalisierungsstrategie zu unterstützen. Mit [!DNL AEM] können Sie von einem zentralen Ort aus problemlos Inhalte für Desktops, Tablets und Smartphones erstellen, ohne Code zu schreiben. Es ist nicht erforderlich, Seiten für jedes Gerät zu erstellen. [!DNL AEM] nimmt Ihre Inhalte und passt jedes Erlebnis automatisch für jedes Gerät an.

Mit [!DNL Target] können Sie personalisierte Erlebnisse in großem Umfang bereitstellen. Dies erfolgt auf der Grundlage einer Kombination aus regelbasierten und AI-gestützten Ansätzen des maschinellen Lernens, zu denen Verhaltens-, Kontext- und Offline-Variablen zählen. [!DNL Target] ermöglicht Ihnen die problemlose Einrichtung und Ausführung von Aktivitäten des Typs [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) und [Multivariater Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT), um die besten Angebote, Inhalte und Erlebnisse zu bestimmen.

[!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind ein großer Schritt vorwärts, um bei der Erstellung und Verwaltung von Inhalten und Erlebnissen die Optimierungs- und Personalisierungsfachleute einzubinden, die Geschäftsergebnisse mithilfe von [!DNL Target] optimieren.

## Was ist der Unterschied zwischen [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmenten]?

[!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] können auf der Oberfläche ähnlich aussehen, aber jeder Fragmenttyp spielt Schlüsselrollen in unterschiedlichen Anwendungsfällen.

Weitere Informationen dazu, wo [!UICONTROL Inhaltsfragmente] und [!UICONTROL Experience Fragments] sich ähnlich sind und wo sie sich unterscheiden, sowie dazu, wann und wie welcher Typ verwendet wird, finden Sie unter [Grundlegendes zu [!UICONTROL Inhaltsfragmenten] und [!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/content-fragments/understand-content-fragments-and-experience-fragments.html?lang=de){target=_blank} in the [AEM Sites videos and tutorials guide](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/overview.html?lang=de){target=_blank}.