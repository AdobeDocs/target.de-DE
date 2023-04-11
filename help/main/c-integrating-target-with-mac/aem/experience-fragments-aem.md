---
keywords: experience;json;aem;adobe experience manager;in adobe target exportieren;experience fragments;fragments;XF
description: Erfahren Sie, wie Sie  [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in  [!DNL Adobe Target] -Aktivitäten verwenden.
title: Wie verwende ich  [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
source-git-commit: 47e1c7290011c21fd0710280d35c862a81b4f558
workflow-type: tm+mt
source-wordcount: '1352'
ht-degree: 73%

---

# AEM [!UICONTROL Experience Fragments]

Verwendung [!UICONTROL Experience Fragments] (XFs) erstellt in [!DNL Adobe Experience Manager] AEM [!DNL Target] Aktivitäten zur Optimierung und Personalisierung.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Experience Fragments] in [!DNL Target]:

* Für diese Funktion müssen Sie [!DNL Adobe Experience Manager] (AEM)-Kundin bzw. -Kunde sein. Weitere Informationen finden Sie unten unter [Anforderungen](#section_AE6F0971E1574B3AA324003599B96E5A).
* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind für die folgenden Aktivitätstypen verfügbar:

   * [[!UICONTROL A/B-Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Automatische Zuordnung]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Automatisches Targeting]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Erlebnis-Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] für die folgenden Aktivitätstypen nicht verfügbar sind:

   * [[!UICONTROL Multivariate Tests] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* Sie können [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten, die [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

Weitere Informationen zu AEM [!UICONTROL Experience Fragments] und Inhaltsfragmenten finden Sie in der [Übersicht über AEM [!UICONTROL Experience Fragments] und Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen  {#requirements}

Sie müssen über die Funktionen für [!UICONTROL Experience Fragments] in [!DNL Target] verfügen. Darüber hinaus müssen Sie [!DNL AEM] as a Cloud Service oder [!DNL AEM] 6.4 (oder höher) nutzen. Ihre Kundenkontaktperson kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard] oder [!DNL Adobe Target Premium] account

[!DNL Adobe Experience Manager] 6.3 und 6.4 haben das Ende des Lebenszyklus erreicht und werden nicht mehr unterstützt (mit Ausnahme von Kundinnen und Kunden, die erweiterte Unterstützung erworben haben).

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Erstellen und Konfigurieren von [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target] verwenden zu können, müssen Sie die folgenden Schritte ausführen:

### Schritt 1: Integrieren von [!DNL AEM] mit [!DNL Target]

Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [Integration mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html?lang=de){target=_blank} im Handbuch zu *Experience Manager as a Cloud Service*.
* **Adobe I/O**: [Integration mit Adobe Target mithilfe von Adobe I/O](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html?lang=de){target=_blank} in der Dokumentation *Handbuch zur Benutzerverwaltung*.
* **[!DNL AEM]6.5**: [Einbindung in Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Einbindung in Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 2: Erstellen des Experience Fragments

[!UICONTROL Experience Fragments] werden in [!DNL AEM] erstellt. Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=de){target=_blank} im Handbuch zu *Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5:** [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4:** [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 3: Konfigurieren von [!DNL AEM] für das Freigeben von Experience Fragments in [!DNL Target]

1. Wählen Sie in [!DNL AEM] das gewünschte Experience Fragment oder den Ordner aus, der dieses Fragment enthält, und klicken Sie dann auf **[!UICONTROL Eigenschaften]**.
2. Klicken Sie auf die Registerkarte **[!UICONTROL Cloud-Services]** und wählen Sie dann in der Dropdown-Liste **[!UICONTROL Cloud-Service-Konfiguration]** den Eintrag **[!UICONTROL Adobe Target]** aus.

   Beim vorherigen Schritt wird davon ausgegangen, dass die [!DNL Adobe Target]-Konfiguration von einem Benutzer in Ihrem Unternehmen erstellt wurde.

3. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

### Schritt 4: Veröffentlichen Sie die [!UICONTROL Experience Fragment] und exportieren sie in [!DNL Target]

Abhängig von Ihrer [!DNL AEM]-Version finden Sie unter den folgenden Links schrittweise Anweisungen:

* **AEM as a Cloud Service**: [Exportieren von [!UICONTROL Experience Fragments] nach Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=de){target=_blank} im Handbuch zu *Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

## Verwenden von [!UICONTROL Experience Fragments] in [!DNL Target]-Aktivitäten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach Ausführung der vorherigen Aufgaben wird die [!UICONTROL Experience Fragment] wird auf [!UICONTROL Angebote] Seite in [!DNL Target].

[!DNL Target] sucht derzeit alle zehn Minuten nach zu importierenden [!UICONTROL Experience Fragments]. Der importierte [!UICONTROL Experience Fragment] sollte in [!DNL Target] innerhalb von zehn Minuten, aber dieser Zeitrahmen sollte die Zukunft verkürzen.

Die [!UICONTROL Experience Fragment] wird in [!DNL Target] als HTML- oder JSON-Angebot. Die [!UICONTROL Experience Fragment] &quot;primäre&quot;Version verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Experience Fragment] in [!DNL Target].

Sie können nach [!UICONTROL HTML-XFs] und [!UICONTROL JSON-XFs] filtern und suchen, damit Sie zwischen Experience Fragment-Typen unterscheiden können, die nach [!DNL Target] exportiert werden.

![Filtern nach Experience Fragment-Typen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über eine [!UICONTROL Experience Fragment] in der Liste und klicken Sie auf die [!UICONTROL Ansicht] icon ![Infosymbol](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) um weitere Informationen zu erhalten über [!UICONTROL Experience Fragment], einschließlich der [!UICONTROL Name], [!UICONTROL Typ], [!UICONTROL Angebots-ID], [!UICONTROL Angebotspfad]und Informationen zu letzten Änderungen. Klicken Sie auf die Registerkarte [!UICONTROL Nutzung von Angeboten], um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Experience Fragment-Informationen](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

Sie können [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten, die [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).


>[!TIP]
>
>Verwenden von künstlicher Intelligenz, maschinellem Lernen und Recommendations mit [!UICONTROL Experience Fragments]:
>
>* So verwenden Sie die [!DNL Target] KI- und ML-Funktionen können Sie [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) beim Erstellen einer Aktivität.
>
>* [!UICONTROL Experience Fragments] werden in [!DNL Recommendations]-Aktivitäten nicht unterstützt. Um [!UICONTROL Experience Fragments] für Recommendations zu verwenden, können Sie eine [!UICONTROL A/B-Test]-Aktivität (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) oder eine [!UICONTROL Experience-Targeting] (XT)-Aktivität erstellen und [Recommendations als Angebote einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).


**So verwenden Sie [!UICONTROL Experience Fragments] mit dem VEC:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) an die Stelle der Seite, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann die gewünschte Option aus, um die Liste [!UICONTROL Experience Fragment auswählen] anzuzeigen.

   * [!UICONTROL Einfügen vor]
   * [!UICONTROL Einfügen nach]
   * [!UICONTROL Mit Experience Fragment tauschen]

   In der Liste [!UICONTROL Experience Fragments] werden alle in [!DNL AEM] erstellten Inhalte angezeigt, die nun nativ in [!DNL Target] verfügbar sind.

   >[!NOTE]
   >
   >Die Option [!UICONTROL Mit Experience Fragment tauschen] ist nicht für Bilder verfügbar. Wenn Sie diese Option mit einem Bild verwenden möchten, klicken Sie auf das Container-Element, das das gewünschte Bild enthält.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Wählen Sie die gewünschte [!UICONTROL Experience Fragment]Klicken Sie auf **[!UICONTROL Fertig]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

   Weitere Informationen über die Konfiguration der verschiedenen Aktivitätstypen finden Sie in den folgenden Themen:

   * **A/B-Test:** [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Automatische Zuordnung:** [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisches Targeting:** [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automatisierte Personalisierung (AP):** [Erstellen einer Aktivität zur automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Erlebnis-Targeting (XT):** [Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Recommendations in A/B-Tests oder XT-Aktivitäten:** [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments], die in [!DNL Target] als JSON-Dateien exportiert wurden, können nicht in Aktivitäten verwendet werden, die mit dem VEC erstellt wurden. Nur [!UICONTROL Experience Fragments] in HTML werden in VEC-basierten Aktivitäten unterstützt. Wenn Sie JSON verwenden möchten [!UICONTROL Experience Fragments], verwenden Sie sie in Aktivitäten, die mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

**So verwenden Sie [!UICONTROL Experience Fragments][!UICONTROL  mit dem formularbasierten Experience Composer]:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) an die Stelle der Seite, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann **[!UICONTROL Experience Fragment ändern]** aus, um die Liste [!UICONTROL Experience Fragment auswählen] anzuzeigen.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   In der Liste [!UICONTROL Experience Fragments] werden alle in [!DNL AEM] erstellten Inhalte angezeigt, die nun nativ in [!DNL Target] verfügbar sind.

1. Wählen Sie die gewünschte [!UICONTROL Experience Fragment]Klicken Sie auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zusätzliche Informationen

* [!DNL Target] sucht derzeit alle zehn Minuten nach zu importierenden [!UICONTROL Experience Fragments]. Der importierte [!UICONTROL Experience Fragment] sollte in [!DNL Target] innerhalb von zehn Minuten, aber dieser Zeitrahmen sollte die Zukunft verkürzen.
* Die [!UICONTROL Experience Fragment] wird in [!DNL Target] als HTML- oder JSON-Angebot. Die [!UICONTROL Experience Fragment] &quot;primäre&quot;Version verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Experience Fragment] in [!DNL Target].
* Mit [!DNL Adobe I/O] können Sie keine [!UICONTROL Experience Fragments] erstellen. Sie müssen [!UICONTROL Experience Fragmente] mithilfe von AEM erstellen, wie oben beschrieben.
* Wenn Sie Ihre [!UICONTROL Experience Fragment] in AEM [!UICONTROL Experience Fragment] muss veröffentlicht und nach exportiert werden [!DNL Target] erneut [!DNL Target] kann die neuesten Änderungen verwenden.

## Entfernen von ClientLibs und externem HTML-Code aus nach [!UICONTROL Target] exportierten [!UICONTROL Experience Fragments]

Bei Verwendung von [!UICONTROL Experience Fragment] Angebote mit [!DNL Target] auf einer von AEM bereitgestellten Seite enthält die Zielseite bereits alle erforderlichen Client-Bibliotheken. Beachten Sie außerdem, dass überflüssige HTML-Elemente im Angebot nicht erforderlich sind.

Manchmal umschließen ganze HTML-Seiten die [!UICONTROL Experience Fragment] und Probleme verursachen. Stellen Sie sicher, dass [!UICONTROL Experience Fragment] ist ein kleines Stück HTML und keine vollständige HTML-Seite mit HTML, HEAD, BODY und so weiter.

Weitere Informationen finden Sie im folgenden Blogpost: [AEM 6.5: Removing ClientLibs from [!UICONTROL Experience Fragments] exported to Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Schulungsvideo: Verwenden von AEM-[!UICONTROL Experience Fragments] mit [!DNL Adobe Target]

Das folgende Video zeigt Ihnen, wie Sie [!UICONTROL Experience Fragments] einrichten und verwenden:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>Die [!DNL AEM]-Deeplink-Funktion, die in 4:54 erläutert wurde, wurde entfernt.

Weitere Informationen finden Sie unter [Verwenden von [!UICONTROL Experience Fragments] mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=de) auf der Seite *Videos und Tutorials für AEM Sites*.