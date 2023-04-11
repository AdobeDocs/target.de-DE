---
keywords: Erlebnis;JSON;AEM;Adobe Experience Manager;in Adobe Target exportieren;Inhaltsfragmente;Fragmente;CF;cf;Headless;Personalisierung;Experiment
description: Erfahren Sie, wie Sie  [!DNL Adobe Experience Manager] [!UICONTROL Inhaltsfragmente] in  [!DNL Adobe Target] -Aktivitäten verwenden.
title: Wie verwende ich [!UICONTROL Inhaltsfragmente] aus  [!DNL Adobe Experience Manager]  (AEM)?
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Target Beta release features?"
feature: Integrations
source-git-commit: 47e1c7290011c21fd0710280d35c862a81b4f558
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 84%

---

# AEM-[!UICONTROL Inhaltsfragmente]

Verwendung [!UICONTROL Inhaltsfragmente] (CFs) erstellt in [!DNL Adobe Experience Manager] AEM [!DNL Target] Aktivitäten zur Unterstützung der Headless-Personalisierung und -Experimentierung.

>[!NOTE]
>
>Diese Funktion wird am 12. April 2023 veröffentlicht.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM-[!UICONTROL Inhaltsfragmenten] in [!DNL Target]:

* Diese Funktion erfordert, dass Sie [!DNL Adobe Experience Manager as a Cloud Service] -Kunden. Weitere Informationen finden Sie unten unter [Anforderungen](#section_AE6F0971E1574B3AA324003599B96E5A).
* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind für die folgenden Aktivitätstypen verfügbar:

   * [[!UICONTROL A/B-Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Automatische Zuordnung]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Automatisches Targeting]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Erlebnis-Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] für die folgenden Aktivitätstypen nicht verfügbar sind:

   * [[!UICONTROL Multivariate Tests] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* Sie können [!UICONTROL Inhaltsfragmente] nur in [!DNL Target]-Aktivitäten aufnehmen, die den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden. Sie können [!UICONTROL Inhaltsfragmente] *nicht* in [!DNL Target]-Aktivitäten aufnehmen, die [!UICONTROL Visual Experience Composer] (VEC) verwenden.

Weitere Informationen zu [!UICONTROL Inhaltsfragmenten] und [!UICONTROL Experience Fragments] aus AEM finden Sie in der [Übersicht über [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] aus AEM](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen  {#requirements}

Sie müssen über die Funktionen für [!UICONTROL Inhaltsfragmente] in [!DNL Target] verfügen. Darüber hinaus müssen Sie [[!DNL AEM] as a Cloud Service](https://experienceleague.corp.adobe.com/docs/experience-manager-cloud-service.html){target=_blank}. Ihre Kundenkontaktperson kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Konfigurieren und Verwenden von [!UICONTROL Inhaltsfragmenten] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um [!UICONTROL Inhaltsfragmente] zur Verwendung in [!DNL Target]-Aktivitäten zu exportieren, müssen Sie einige vorbereitende Schritte in AEM durchführen. Weitere Informationen finden Sie unter [Exportieren von Inhaltsfragmenten in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=de){target=_blank} im *as a Cloud Service Dokumentation zu Experience Manager*. Dieser Link wird am Veröffentlichungstag (12. April 2023) verfügbar sein.

Informationen zum Entwerfen, Erstellen, Kuratieren und Veröffentlichen von [!UICONTROL Inhaltsfragmenten] finden Sie unter [[!UICONTROL Inhaltsfragmente]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=de){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=de){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=de){target=_blank}.

## Verwenden von [!UICONTROL Inhaltsfragmenten] in [!DNL Target]-Aktivitäten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach dem Ausführen der zuvor genannten Aufgaben wird das [!UICONTROL Inhaltsfragment] auf der Seite [!UICONTROL Angebote] in [!DNL Target] angezeigt.

[!DNL Target] sucht derzeit alle zehn Minuten nach zu importierenden [!UICONTROL Inhaltsfragmenten]. Das importierte [!UICONTROL Inhaltsfragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.

Das [!UICONTROL Inhaltsfragment] wird als JSON-Angebot in [!DNL Target] exportiert. Die „primäre“ Version des [!UICONTROL Inhaltsfragments] verbleibt in [!DNL AEM]. Sie können das [!UICONTROL Inhaltsfragment] nicht in [!DNL Target] bearbeiten.

Sie können nach [!UICONTROL HTML-XFs], [!UICONTROL JSON-XFs] und [!UICONTROL Inhaltsfragmenten] filtern und suchen, damit Sie zwischen verschiedenen Angebotstypen unterscheiden können, die in [!DNL Target] exportiert werden.

![Filtern nach Inhaltsfragmenttypen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über ein [!UICONTROL Inhaltsfragment] in der Liste bewegen und auf das Symbol [!UICONTROL Ansicht] ![Info icon](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) klicken, um weitere Informationen über das [!UICONTROL Inhaltsfragment] zu erhalten, einschließlich seines [!UICONTROL AEM-Pfads] und [!UICONTROL AEM-Deep-Links]. Klicken Sie auf die Registerkarte [!UICONTROL Angebotsnutzung], um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Informationen zu Inhaltsfragmenten](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

Sie können [!UICONTROL Inhaltsfragmente] nur in [!DNL Target]-Aktivitäten aufnehmen, die den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden. Sie können [!UICONTROL Inhaltsfragmente] *nicht* in [!DNL Target]-Aktivitäten aufnehmen, die [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) verwenden. [!UICONTROL Inhaltsfragmente] werden als JSON-Dateien in [!DNL Target] exportiert und können nicht in Aktivitäten verwendet werden, die mit VEC erstellt wurden.

>[!TIP]
>
>Verwenden von künstlicher Intelligenz, maschinellem Lernen und Recommendations mit [!UICONTROL Inhaltsfragmenten]:
>
>* So verwenden Sie die [!DNL Target] KI- und ML-Funktionen können Sie [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) beim Erstellen einer [!UICONTROL A/B-Test] Aktivität.
>
>* [!UICONTROL Inhaltsfragmente] werden in [!DNL Recommendations]-Aktivitäten nicht unterstützt. Um [!UICONTROL Inhaltsfragmente] für Recommendations nutzen zu können, können Sie eine [!UICONTROL A/B-Test]-Aktivität (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) oder eine [!UICONTROL Erlebnis-Targeting] (XT)-Aktivität erstellen und [Recommendations als Angebote einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).


**So verwenden Sie [!UICONTROL Inhaltsfragmente] mit dem [!UICONTROL formularbasierten Experience Composer]:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) an die Stelle der Seite, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann **[!UICONTROL Inhaltsfragment ändern]** aus, um die Liste [!UICONTROL Inhaltsfragment auswählen] anzuzeigen.

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   In der Liste [!UICONTROL Inhaltsfragmente] werden alle in [!DNL AEM] erstellten Inhalte angezeigt, die nun nativ in [!DNL Target] verfügbar sind.

1. Wählen Sie das gewünschte [!UICONTROL Inhaltsfragment] aus und klicken Sie dann auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zusätzliche Informationen

* [!DNL Target] sucht derzeit alle zehn Minuten nach zu importierenden [!UICONTROL Inhaltsfragmenten]. Das importierte [!UICONTROL Inhaltsfragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.
* Das [!UICONTROL Inhaltsfragment] wird als JSON-Angebot in [!DNL Target] exportiert. Die „primäre“ Version des [!UICONTROL Inhaltsfragments] verbleibt in [!DNL AEM]. Sie können das [!UICONTROL Inhaltsfragment] nicht in [!DNL Target] bearbeiten.
* Sie können keine [!UICONTROL Inhaltsfragmente] mit [!DNL Adobe I/O] erstellen. Erstellen Sie [!UICONTROL Inhaltsfragmente] mithilfe von AEM, wie oben beschrieben.
* Wenn Sie Ihr [!UICONTROL Inhaltsfragment] in AEM aktualisieren, muss das [!UICONTROL Inhaltsfragment] erneut veröffentlicht und in [!DNL Target] exportiert werden, damit [!DNL Target] die neuesten Änderungen verwenden kann.