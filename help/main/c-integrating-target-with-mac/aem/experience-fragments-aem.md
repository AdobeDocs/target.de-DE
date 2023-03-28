---
keywords: experience;json;aem;adobe experience manager;in adobe target exportieren;experience fragments;fragments;XF
description: Erfahren Sie, wie Sie [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in [!DNL Adobe Target] Aktivitäten.
title: Verwendung [!DNL Adobe Experience Manager] AEM [!UICONTROL Experience Fragments]?
feature: Integrations
source-git-commit: 0135831b56c48b0adca49e843c5ddd6574358aa4
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 32%

---

# AEM [!UICONTROL Experience Fragments]

Verwendung [!UICONTROL Experience Fragments] (XFs) erstellt in [!DNL Adobe Experience Manager] AEM [!DNL Target] Aktivitäten zur Optimierung oder Personalisierung.

>[!NOTE]
>
>Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Experience Fragments] in [!DNL Target]:
> 
>* Diese Funktion erfordert, dass Sie [!DNL Adobe Experience Manager] (AEM) Kunden. Weitere Informationen finden Sie unter [Voraussetzungen](#section_AE6F0971E1574B3AA324003599B96E5A) unten.
>* Diese Funktion ist für die folgenden Aktivitätstypen verfügbar: [!UICONTROL A/B-Test], [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting], [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Erlebnis-Targeting] (XT). Diese Funktion ist in nicht verfügbar. [!UICONTROL Multivarianz-Test] (MVT) und [!UICONTROL Recommendations] Aktivitäten.
>
>* Sie können [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten, die [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).


Weitere Informationen zu AEM [!UICONTROL Experience Fragments] und Inhaltsfragmente, siehe [AEM [!UICONTROL Experience Fragments] Übersicht über Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen  {#requirements}

Sie müssen über die [!UICONTROL Experience Fragments] -Funktion [!DNL Target]. Darüber hinaus müssen Sie [!DNL AEM] as a Cloud Service oder [!DNL AEM] 6.4 (oder höher). Ihr Kundenbetreuer kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5.
* [!DNL Adobe Experience Manager] 6.4.
* [!DNL Adobe Target Standard]- oder [!DNL Adobe Target Premium]-Konto.

[!DNL Adobe Experience Manager] 6.3 und 6.4 haben das Ende des Lebenszyklus erreicht und werden nicht mehr unterstützt (mit Ausnahme von Kunden, die erweiterte Unterstützung erworben haben).

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Erstellen und Konfigurieren [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Zur Verwendung [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target]müssen Sie die folgenden Schritte ausführen:

### Schritt 1: Integrieren von [!DNL AEM] mit [!DNL Target]

Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [Integration mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html){target=_blank} im *Experience Manager as a Cloud Service* Handbuch.
* **Adobe I/O**: [Integration mit Adobe Target mithilfe von Adobe I/O](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html?lang=de){target=_blank} in der Dokumentation zum *Verwalten von Benutzerhandbüchern*.
* **[!DNL AEM]6.5**: [Abonnieren von Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Abonnieren von Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 2: Experience Fragment erstellen

[!UICONTROL Experience Fragments] werden in [!DNL AEM]. Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=en){target=_blank} im *Experience Manager as a Cloud Service* Handbuch.
* **[!DNL AEM]6.5:** [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der *Adobe Experience Manager 6.5*-Dokumentation.
* **[!DNL AEM]6.4:** [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der *Adobe Experience Manager 6.4*-Dokumentation.

### Schritt 3: Konfigurieren [!DNL AEM] , um das Experience Fragment für freizugeben [!DNL Target]

1. Von innen [!DNL AEM], wählen Sie das gewünschte Experience Fragment oder den Ordner aus, der es enthält, und klicken Sie dann auf **[!UICONTROL Eigenschaften]**.
2. Klicken Sie auf die Registerkarte **[!UICONTROL Cloud-Services]** und wählen Sie dann in der Dropdown-Liste **[!UICONTROL Cloud-Service-Konfiguration]** den Eintrag **[!UICONTROL Adobe Target]** aus.

   Beim vorherigen Schritt wird davon ausgegangen, dass die [!DNL Adobe Target]-Konfiguration von einem Benutzer in Ihrem Unternehmen erstellt wurde.

3. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

### Schritt 4: Veröffentlichen Sie das Experience Fragment und exportieren Sie es in [!DNL Target]

Abhängig von Ihrer [!DNL AEM]-Version finden Sie unter den folgenden Links schrittweise Anweisungen:

* **AEM as a Cloud Service**: [Exportieren [!UICONTROL Experience Fragments] zu Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=en){target=_blank} im *Experience Manager as a Cloud Service* Handbuch.
* **[!DNL AEM]6.5**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=en){target=_blank} in der *Adobe Experience Manager 6.5*-Dokumentation.
* **[!DNL AEM]6.4**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der *Adobe Experience Manager 6.4*-Dokumentation.

## Verwenden [!UICONTROL Experience Fragments] in [!DNL Target] activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach Ausführung der vorherigen Aufgaben wird das Experience Fragment auf der [!UICONTROL Angebote] Seite in [!DNL Target].

[!DNL Target] sucht derzeit nach [!UICONTROL Experience Fragments] alle zehn Minuten zu importieren. Das importierte Experience Fragment sollte in [!DNL Target] innerhalb von zehn Minuten, aber dieser Zeitrahmen sollte die Zukunft verkürzen.

Das Experience Fragment wird in [!DNL Target] als HTML- oder JSON-Angebot. Diese &quot;primäre&quot;Version des Experience Fragment bleibt in [!DNL AEM]. Sie können das Experience Fragment nicht in [!DNL Target] bearbeiten.

Sie können nach [!UICONTROL HTML XFs] und [!UICONTROL JSON XFs] , um Sie bei der Unterscheidung zwischen Experience Fragment-Typen zu unterstützen, die nach [!DNL Target].

![Filtern nach Experience Fragment-Typen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über ein Experience Fragment in der Liste bewegen und dann auf die Schaltfläche [!UICONTROL Ansicht] icon ![Infosymbol](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) um zusätzliche Informationen zum Experience Fragment anzuzeigen, einschließlich dessen [!UICONTROL Name], [!UICONTROL Typ], [!UICONTROL Angebots-ID], [!UICONTROL Angebotspfad]und Informationen zu letzten Änderungen. Klicken Sie auf [!UICONTROL Nutzung von Angeboten] um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Experience Fragment-Informationen](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

Sie können [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten, die [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).


>[!TIP]
>
>Verwenden von künstlicher Intelligenz, maschinellem Lernen und Empfehlungen mit [!UICONTROL Experience Fragments]:
>
>* So verwenden Sie die [!DNL Target] KI- und ML-Funktionen können Sie [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) beim Erstellen eines A/B-Tests.
>
>* [!UICONTROL Experience Fragments] nicht unterstützt in [!DNL Recommendations] Aktivitäten. Verwenden Sie jedoch [!UICONTROL Experience Fragments] für Empfehlungen können Sie eine [!UICONTROL A/B-Test] -Aktivität (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) oder ein [!UICONTROL Erlebnis-Targeting] (XT) und [Empfehlungen als Angebot einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).


**So verwenden Sie Erlebnisfragmente mit dem VEC:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) an die Stelle der Seite, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann die gewünschte Option aus, um die Liste [!UICONTROL Experience Fragment auswählen] anzuzeigen.

   * [!UICONTROL Einfügen vor]
   * [!UICONTROL Einfügen nach]
   * [!UICONTROL Mit Experience Fragment tauschen]

   Die [!UICONTROL Experience Fragment] Die Liste zeigt den in [!DNL AEM] , die jetzt nativ von in verfügbar ist [!DNL Target].

   >[!NOTE]
   >
   >Die Option [!UICONTROL Mit Experience Fragment tauschen] ist nicht für Bilder verfügbar. Wenn Sie diese Option mit einem Bild verwenden möchten, klicken Sie auf das Container-Element, das das gewünschte Bild enthält.

   ![experience_fragment_list -Bild](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Wählen Sie das gewünschte Experience Fragment aus und klicken Sie dann auf **[!UICONTROL Fertig]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

   Weitere Informationen über die Konfiguration der verschiedenen Aktivitätstypen finden Sie in den folgenden Themen:

   * **A/B-Test:** [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Automatische Zuordnung:** [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisches Targeting:** [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automatisierte Personalisierung (AP):** [Erstellen einer Aktivität zur automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Erlebnis-Targeting (XT):** [Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Recommendations in A/B-Tests oder XT-Aktivitäten:** [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments] als JSON exportiert in [!DNL Target] kann nicht in Aktivitäten verwendet werden, die mit dem VEC erstellt wurden; nur HTML [!UICONTROL Experience Fragments] werden in VEC-basierten Aktivitäten unterstützt. Wenn Sie JSON verwenden möchten [!UICONTROL Experience Fragments], verwenden Sie sie in Aktivitäten, die mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

**So verwenden Sie Erlebnisfragmente mit dem Form-Based Experience Composer:**

1. Klicken Sie in [!DNL Target] Target beim Erstellen oder Bearbeiten eines Erlebnisses in [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) an die Stelle der Seite, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann **[!UICONTROL Experience Fragment ändern]** aus, um die Liste [!UICONTROL Experience Fragment auswählen] anzuzeigen.

   ![experience_fragment_list -Bild](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   Die [!UICONTROL Experience Fragment] Die Liste zeigt den in [!DNL AEM] , die jetzt nativ von in verfügbar ist [!DNL Target].

1. Wählen Sie das gewünschte Experience Fragment aus und klicken Sie dann auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zu beachten {#considerations}

* [!DNL Target] sucht derzeit nach [!UICONTROL Experience Fragments] alle zehn Minuten zu importieren. Das importierte Experience Fragment sollte in [!DNL Target] innerhalb von zehn Minuten, aber dieser Zeitrahmen sollte die Zukunft verkürzen.
* Das Experience Fragment wird in [!DNL Target] als HTML- oder JSON-Angebot. Die &quot;primäre&quot;Version des Experience Fragment bleibt in [!DNL AEM]. Sie können das Experience Fragment nicht bearbeiten in [!DNL Target].
* Sie können keine [!UICONTROL Experience Fragments] using [!DNL Adobe I/O]. Erstellen [!UICONTROL Experience Fragments] Verwendung von AEM, wie oben beschrieben.
* Wenn Sie Ihr Experience Fragment in AEM aktualisieren, muss das Experience Fragment veröffentlicht und in exportiert werden [!DNL Target] erneut [!DNL Target] kann die neuesten Änderungen verwenden.

## Entfernen von ClientLibs und irrelevanten HTML aus [!UICONTROL Experience Fragments] exportiert [!UICONTROL Target]

Bei Verwendung von Experience Fragment-Angeboten mit [!DNL Target] auf einer von AEM bereitgestellten Seite enthält die Zielseite bereits alle erforderlichen Client-Bibliotheken. Beachten Sie auch, dass auch keine irreführenden HTML-Elemente im Angebot erforderlich sind.

Manchmal umschließen ganze HTML-Seiten das Experience Fragment und verursachen Probleme. Stellen Sie sicher, dass das Experience Fragment ein kleines Stück HTML und keine vollständige HTML-Seite mit HTML, HEAD, BODY usw. ist.

Weitere Informationen finden Sie im folgenden Blogpost: [AEM 6.5: Entfernen von ClientLibs aus [!UICONTROL Experience Fragments] in Target exportiert](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Schulungsvideo: Verwenden von AEM [!UICONTROL Experience Fragments] mit [!DNL Adobe Target]

Im folgenden Video erfahren Sie, wie Sie [!UICONTROL Experience Fragments]:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>Die [!DNL AEM]-Deeplink-Funktion, die in 4:54 erläutert wurde, wurde entfernt.

Weitere Informationen finden Sie unter [Verwenden [!UICONTROL Experience Fragments] mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=de) auf *Videos und Tutorials zu AEM Sites* Seite.