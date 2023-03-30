---
keywords: Erlebnis;JSON;AEM;Adobe Experience Manager;nach Adobe Target exportieren;Inhaltsfragmente;Fragmente;CF;cf;Headless;Personalisierung;Experimentierung
description: Erfahren Sie, wie Sie [!DNL Adobe Experience Manager] [!UICONTROL Inhaltsfragmente] in [!DNL Adobe Target] Aktivitäten.
title: Verwendung [!DNL Adobe Experience Manager] AEM [!UICONTROL Inhaltsfragmente]?
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Target Beta release features?"
feature: Integrations
source-git-commit: c5629159f55bf3daa09a8ddbe739dfcd6272d285
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 4%

---

# AEM [!UICONTROL Inhaltsfragmente]

Verwendung [!UICONTROL Inhaltsfragmente] (CFs) erstellt in [!DNL Adobe Experience Manager] AEM [!DNL Target] Aktivitäten zur Unterstützung der Headless-Personalisierung und -Experimentierung.

AEM Inhaltsfragmente für die Headless-Personalisierung und -Experimentierung

>[!NOTE]
>
>Diese Funktion soll am 6. April 2023 veröffentlicht werden.


>[!NOTE]
>
>Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Inhaltsfragmente] in [!DNL Target]:
> 
>* Diese Funktion erfordert, dass Sie [!DNL Adobe Experience Manager] (AEM) Kunden. Weitere Informationen finden Sie unter [Voraussetzungen](#section_AE6F0971E1574B3AA324003599B96E5A) unten.
>
>* Diese Funktion ist für die folgenden Aktivitätstypen verfügbar: [!UICONTROL A/B-Test], [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting], [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Erlebnis-Targeting] (XT). Diese Funktion ist in nicht verfügbar. [!UICONTROL Multivarianz-Test] (MVT) und [!UICONTROL Recommendations] Aktivitäten.
>
>* Sie können [!UICONTROL Inhaltsfragmente] in [!DNL Target] Aktivitäten, die [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) nur. Sie können nicht konsumieren [!UICONTROL Inhaltsfragmente] mithilfe der [!UICONTROL Visual Experience Composer] (VEC).


Weitere Informationen zu AEM [!UICONTROL Inhaltsfragmente] und [!UICONTROL Experience Fragments], siehe [AEM [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] Übersicht](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen  {#requirements}

Sie müssen über die [!UICONTROL Inhaltsfragmente] -Funktion [!DNL Target]. Darüber hinaus müssen Sie [!DNL AEM] as a Cloud Service. Ihr Kundenbetreuer kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Konfigurieren und Verwenden von [!UICONTROL Inhaltsfragmente] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Zu exportieren [!UICONTROL Inhaltsfragmente] zur Verwendung in [!DNL Target] -Aktivitäten, müssen Sie einige vorbereitende Schritte in AEM durchführen. Weitere Informationen finden Sie unter [Exportieren von Inhaltsfragmenten in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank} im *as a Cloud Service Dokumentation zu Experience Manager*. Beachten Sie, dass dieser Link am Veröffentlichungstag (6. April 2023) verfügbar sein wird.

Informationen zum Entwerfen, Erstellen, Kuratieren und Veröffentlichen [!UICONTROL Inhaltsfragmente], siehe [[!UICONTROL Inhaltsfragmente]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=en){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

## Verwenden [!UICONTROL Inhaltsfragmente] in [!DNL Target] activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach Ausführung der vorherigen Aufgaben wird die [!UICONTROL Inhaltsfragment] wird auf [!UICONTROL Angebote] Seite in [!DNL Target].

[!DNL Target] sucht derzeit nach [!UICONTROL Inhaltsfragmente] alle zehn Minuten zu importieren. Der importierte [!UICONTROL Inhaltsfragment] sollte in [!DNL Target] innerhalb von zehn Minuten, aber dieser Zeitrahmen sollte die Zukunft verkürzen.

Die [!UICONTROL Inhaltsfragment] wird in [!DNL Target] als JSON-Angebot. that [!UICONTROL Inhaltsfragment] &quot;primäre&quot;Version verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Inhaltsfragment] in [!DNL Target].

Sie können nach [!UICONTROL HTML XFs], [!UICONTROL JSON XFs]und [!UICONTROL Inhaltsfragmente] , damit Sie zwischen verschiedenen Angebotstypen unterscheiden können, die in [!DNL Target].

![Filtern nach Inhaltsfragmenttypen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über einen [!UICONTROL Inhaltsfragment] in der Liste und klicken Sie auf die [!UICONTROL Ansicht] icon ![Infosymbol](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) um weitere Informationen zu erhalten über [!UICONTROL Inhaltsfragment], einschließlich der [!UICONTROL AEM] und [!UICONTROL AEM Deep-Link]. Klicken Sie auf [!UICONTROL Nutzung von Angeboten] um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Inhaltsfragmentinformationen](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

Sie können [!UICONTROL Inhaltsfragmente] in [!DNL Target] Aktivitäten, die [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) nur. You *cannot* konsumieren [!UICONTROL Inhaltsfragmente] in [!DNL Target] Aktivitäten, die [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). [!UICONTROL Inhaltsfragmente] werden als JSON in [!DNL Target] und können nicht in Aktivitäten verwendet werden, die mit VEC erstellt wurden.

>[!TIP]
>
>Verwenden von künstlicher Intelligenz, maschinellem Lernen und Empfehlungen mit [!UICONTROL Inhaltsfragmente]:
>
>* So verwenden Sie die [!DNL Target] KI- und ML-Funktionen können Sie [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) beim Erstellen eines A/B-Tests.
>
>* [!UICONTROL Inhaltsfragmente] nicht unterstützt in [!DNL Recommendations] Aktivitäten. Verwenden Sie jedoch [!UICONTROL Inhaltsfragmente] für Empfehlungen können Sie eine [!UICONTROL A/B-Test] -Aktivität (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) oder ein [!UICONTROL Erlebnis-Targeting] (XT) und [Empfehlungen als Angebot einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).


**Zu konsumieren [!UICONTROL Inhaltsfragmente] mithilfe der [!UICONTROL Form-Based Experience Composer]:**

1. In [!DNL Target], während Sie ein Erlebnis erstellen oder bearbeiten [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), wählen Sie die Stelle auf der Seite aus, an der Sie die [!DNL AEM] Inhalt und wählen Sie **[!UICONTROL Inhaltsfragment ändern]** , um [!UICONTROL Inhaltsfragment auswählen] Liste.

   ![Bild &quot;content_fragment_list&quot;](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   Die [!UICONTROL Inhaltsfragment] Die Liste zeigt den in [!DNL AEM] , die jetzt nativ von in verfügbar ist [!DNL Target].

1. Wählen Sie die gewünschte [!UICONTROL Inhaltsfragment]Klicken Sie auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zu beachten {#considerations}

* [!DNL Target] sucht derzeit nach [!UICONTROL Inhaltsfragmente] alle zehn Minuten zu importieren. Der importierte [!UICONTROL Inhaltsfragment] sollte in [!DNL Target] innerhalb von zehn Minuten, aber dieser Zeitrahmen sollte die Zukunft verkürzen.
* Die [!UICONTROL Inhaltsfragment] wird in [!DNL Target] als JSON-Angebot. Die [!UICONTROL Inhaltsfragment] &quot;primäre&quot;Version verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Inhaltsfragment] in [!DNL Target].
* Sie können keine [!UICONTROL Inhaltsfragmente] using [!DNL Adobe I/O]. Erstellen [!UICONTROL Inhaltsfragmente] Verwendung von AEM, wie oben beschrieben.
* Wenn Sie Ihre [!UICONTROL Inhaltsfragment] in AEM [!UICONTROL Inhaltsfragment] muss veröffentlicht und nach exportiert werden [!DNL Target] erneut [!DNL Target] kann die neuesten Änderungen verwenden.