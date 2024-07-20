---
keywords: Erlebnis;JSON;AEM;Adobe Experience Manager;in Adobe Target exportieren;Inhaltsfragmente;Fragmente;CF;cf;Headless;Personalisierung;Experimente
description: Erfahren Sie, wie Sie [!DNL Adobe Experience Manager] [!UICONTROL Content Fragments] in [!DNL Adobe Target] Aktivitäten verwenden.
title: Wie verwende ich [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments]?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 21%

---

# AEM [!UICONTROL Content Fragments]

Verwenden Sie [!UICONTROL Content Fragments] (CFs), die in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] -Aktivitäten erstellt wurden, um die Headless-Personalisierung und -Experimentierung zu unterstützen.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Content Fragments] in [!DNL Target]:

* Diese Funktion erfordert, dass Sie eine Kundin oder ein Kunde von [!DNL Adobe Experience Manager as a Cloud Service] sind. Weitere Informationen finden Sie unten unter [Anforderungen](#section_AE6F0971E1574B3AA324003599B96E5A).
* [!UICONTROL Experience Fragments] und [!UICONTROL Content Fragments] sind für die folgenden Aktivitätstypen verfügbar:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] und [!UICONTROL Content Fragments] sind für die folgenden Aktivitätstypen nicht verfügbar:

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* Sie können [!UICONTROL Content Fragments] nur mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) in [!DNL Target] -Aktivitäten verwenden. Sie *können* [!UICONTROL Content Fragments] nicht in [!DNL Target] -Aktivitäten mit dem [!UICONTROL Visual Experience Composer] (VEC) verbrauchen.

Weitere Informationen zu AEM [!UICONTROL Content Fragments] und [!UICONTROL Experience Fragments] finden Sie unter [AEM [!UICONTROL Experience Fragments] und [!UICONTROL Content Fragments] Überblick](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen  {#requirements}

Darüber hinaus müssen Sie [[!DNL AEM]  as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=de){target=_blank} verwenden. Ihre Kundenkontaktperson kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Konfigurieren und Verwenden von [!UICONTROL Content Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um [!UICONTROL Content Fragments] zur Verwendung in [!DNL Target] -Aktivitäten zu exportieren, müssen Sie einige vorläufige Schritte in AEM ausführen. Weitere Informationen finden Sie unter [Exportieren von Inhaltsfragmenten nach Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=de){target=_blank} in der *Dokumentation zu Experience Manager as a Cloud Service*.

Informationen zum Entwerfen, Erstellen, Kuratieren und Veröffentlichen von [!UICONTROL Content Fragments] finden Sie unter [[!UICONTROL Content Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=de){target=_blank} und [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=de){target=_blank} in der Dokumentation zu [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=de){target=_blank}.

## Verwenden von [!UICONTROL Content Fragments] in [!DNL Target] -Aktivitäten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach dem Ausführen der vorherigen Aufgaben wird der [!UICONTROL Content Fragment] auf der Seite [!UICONTROL Offers] in [!DNL Target] angezeigt.

[!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Content Fragments] zum Importieren. Der importierte [!UICONTROL Content Fragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein, aber dieser Zeitraum sollte in Zukunft reduziert werden.

Die [!UICONTROL Content Fragment] wird als JSON-Angebot in [!DNL Target] importiert. Die &quot;primäre&quot;Version von [!UICONTROL Content Fragment] verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Content Fragment] in [!DNL Target] nicht bearbeiten.

Sie können nach [!UICONTROL HTML XFs], [!UICONTROL JSON XFs] und [!UICONTROL Content Fragments] filtern und suchen, um zwischen verschiedenen Angebotstypen zu unterscheiden, die nach [!DNL Target] exportiert werden.

![Filtern nach Inhaltsfragmenttypen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über einen [!UICONTROL Content Fragment] in der Liste bewegen und dann auf das [!UICONTROL View]-Symbol ![Info-Symbol](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) klicken, um weitere Informationen über den [!UICONTROL Content Fragment] anzuzeigen, einschließlich dessen [!UICONTROL AEM path] und [!UICONTROL AEM deep link]. Klicken Sie auf den Tab [!UICONTROL Offer Usage] , um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Informationen zu Inhaltsfragmenten](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

Sie können [!UICONTROL Content Fragments] nur mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) in [!DNL Target] -Aktivitäten verwenden. Sie *können* [!UICONTROL Content Fragments] nicht in [!DNL Target] -Aktivitäten verwenden, die den [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) verwenden. [!UICONTROL Content Fragments] wird als JSON in [!DNL Target] exportiert und kann nicht in Aktivitäten verwendet werden, die mit VEC erstellt wurden.

>[!TIP]
>
>Verwenden Sie künstliche Intelligenz, maschinelles Lernen und Empfehlungen mit [!UICONTROL Content Fragments]:
>
>* Um die KI- und ML-Funktionen von [!DNL Target] vollständig zu verwenden, können Sie beim Erstellen einer [!UICONTROL A/B Test] -Aktivität die Option [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) auswählen.
>
>* [!UICONTROL Content Fragments] wird in [!DNL Recommendations] -Aktivitäten nicht unterstützt. Um jedoch [!UICONTROL Content Fragments] für Empfehlungen zu verwenden, können Sie eine [!UICONTROL A/B Test] -Aktivität (einschließlich [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]) oder eine [!UICONTROL Experience Targeting] -Aktivität (XT) erstellen und [Empfehlungen als Angebot einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).

**So verbrauchen Sie [!UICONTROL Content Fragments] mit dem [!UICONTROL Form-based Experience Composer]:**

1. Wählen Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) die Stelle auf der Seite aus, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann **[!UICONTROL Change Content Fragment]** aus, um die Liste [!UICONTROL Choose a Content Fragment] anzuzeigen.

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   Die Liste [!UICONTROL Content Fragment] zeigt den in [!DNL AEM] erstellten Inhalt an, der jetzt nativ in [!DNL Target] verfügbar ist.

1. Wählen Sie den gewünschten [!UICONTROL Content Fragment] aus und klicken Sie dann auf **[!UICONTROL Save]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zusätzliche Informationen

* [!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Content Fragments] zum Importieren. Der importierte [!UICONTROL Content Fragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein, aber dieser Zeitraum sollte in Zukunft reduziert werden.
* Die [!UICONTROL Content Fragment] wird als JSON-Angebot in [!DNL Target] importiert. Die &quot;primäre&quot;Version von [!UICONTROL Content Fragment] verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Content Fragment] in [!DNL Target] nicht bearbeiten.
* Sie können [!UICONTROL Content Fragments] nicht mit [!DNL Adobe I/O] erstellen. Erstellen Sie [!UICONTROL Content Fragments] mit AEM, wie oben beschrieben.
* Wenn Sie Ihre [!UICONTROL Content Fragment] in AEM aktualisieren, muss der [!UICONTROL Content Fragment] erneut veröffentlicht und in [!DNL Target] exportiert werden, damit [!DNL Target] die neuesten Änderungen verwenden kann.
