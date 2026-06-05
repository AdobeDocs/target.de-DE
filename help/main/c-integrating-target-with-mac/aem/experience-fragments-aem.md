---
keywords: experience;json;aem;adobe experience manager;in adobe target exportieren;experience fragments;fragments;XF
description: Erfahren Sie, wie Sie  [!DNL Adobe Experience Manager] [!UICONTROL -Experience Fragments] in- [!DNL Adobe Target] -Aktivitäten verwenden.
title: Wie verwende ich  [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
TQID: https://experienceleague.adobe.com/-W1ELJx0ajes6BPEVIiS8q6ebmRLTTgIrxvGMUEWEaM
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1446
ht-degree: 32%

---

# AEM [!UICONTROL Experience Fragments]

Verwenden Sie [!UICONTROL Experience Fragments] (XFs), die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target] Aktivitäten, um eine Optimierung oder Personalisierung zu ermöglichen.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Experience Fragments] in [!DNL Target]:

* Für diese Funktion müssen Sie [!DNL Adobe Experience Manager] (AEM)-Kundin bzw. -Kunde sein. Weitere Informationen finden Sie unten unter [Anforderungen](#section_AE6F0971E1574B3AA324003599B96E5A).
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

Weitere Informationen zu AEM [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmenten] finden Sie in der Übersicht über [AEM [!UICONTROL Experience Fragments] und Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen {#requirements}

Sie müssen über die Funktionen [!UICONTROL Experience Fragments] in [!DNL Target] verfügen. Darüber hinaus müssen Sie [!DNL AEM] as a Cloud Service oder [!DNL AEM] 6.4 (oder höher) nutzen. Ihre Kundenkontaktperson kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

* [!DNL Adobe Experience Manager] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard]- oder [!DNL Adobe Target Premium]-Konto.

[!DNL Adobe Experience Manager] 6.3 und 6.4 haben das Ende des Lebenszyklus erreicht und werden nicht mehr unterstützt (mit Ausnahme von Kundinnen und Kunden, die erweiterte Unterstützung erworben haben).

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Erstellen und Konfigurieren von [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um [!DNL AEM]Experience [!UICONTROL Fragments] in [!DNL Target] zu verwenden, müssen Sie die folgenden Schritte ausführen:

### Schritt 1: Integrieren von [!DNL AEM] mit [!DNL Target]

Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [Integration mit Adobe Target](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target){target=_blank} im *Experience Manager as a Cloud Service* Handbuch.
* **Adobe Developer**: [Integration mit Adobe Target mithilfe von Adobe I/](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-target-ims-adobe-io.html){target=_blank} in der Dokumentation *Benutzerhandbuch*.
* **[!DNL AEM]6.5**: [Abonnieren von Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Abonnieren von Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 2: Erstellen des Experience Fragments

[!UICONTROL Experience ]) werden in [!DNL AEM] erstellt. Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=de){target=_blank} im *Handbuch zu Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.*.

### Schritt 3: Konfigurieren von [!DNL AEM] für das Freigeben [!UICONTROL Experience Fragments] in [!DNL Target]

1. Wählen Sie in [!DNL AEM] das gewünschte [!UICONTROL Experience Fragment“ oder ] zugehörigen Ordner aus und klicken Sie dann auf **[!UICONTROL Eigenschaften]**.
2. Klicken Sie auf die **[!UICONTROL Cloud Services]** und wählen Sie dann in der Dropdown-Liste **[!UICONTROL Cloud Service]** Konfiguration} die Option **[!UICONTROL Adobe Target]**.

   Beim vorherigen Schritt wird davon ausgegangen, dass die [!DNL Adobe Target]-Konfiguration von einem Benutzer in Ihrem Unternehmen erstellt wurde.

3. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

### Schritt 4: Veröffentlichen des [!UICONTROL Experience Fragment] und Exportieren nach [!DNL Target]

Abhängig von Ihrer [!DNL AEM]-Version finden Sie unter den folgenden Links schrittweise Anweisungen:

* **AEM as a Cloud Service**: [Exportieren von [!UICONTROL Experience Fragments] nach Adobe Target](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target?lang=en){target=_blank} im *Experience Manager as a Cloud Service*-Handbuch.
* **[!DNL AEM]6.5**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der *Adobe Experience Manager 6.5*-Dokumentation.
* **[!DNL AEM]6.4**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der *Adobe Experience Manager 6.4*-Dokumentation.

## Verwenden [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach dem Ausführen der zuvor genannten Aufgaben wird [!UICONTROL Experience Fragment] auf der Seite [!UICONTROL Angebote] in [!DNL Target] angezeigt.

[!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Experience Fragments] die importiert werden sollen. Das importierte [!UICONTROL Experience Fragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.

Das [!UICONTROL Experience Fragment] wird als HTML- oder JSON-Angebot in [!DNL Target] importiert. Die [!UICONTROL primäre] Version des Experience Fragments verbleibt in [!DNL AEM]. Das [!UICONTROL Experience Fragment“ kann nicht ] in [!DNL Target] bearbeitet werden.

Sie können nach [!UICONTROL HTML-XFs] und [!UICONTROL JSON-XFs] filtern und suchen, damit Sie zwischen ([!UICONTROL ) ] unterscheiden können, die nach [!DNL Target] exportiert werden.

![Filtern nach Experience Fragment-Typen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über ein [!UICONTROL Experience Fragment] in der Liste bewegen und dann auf das [!UICONTROL Ansicht]-Symbol ![Info-](/help/main/assets/icons/InfoOutline.svg) klicken, um zusätzliche Informationen zum [!UICONTROL Experience Fragment] anzuzeigen, darunter [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Angebots-ID], [!UICONTROL Angebotspfad] Informationen zur letzten Änderung. Klicken Sie [!UICONTROL [!UICONTROL Vollständige Details anzeigen]], um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Experience Fragment-Informationen](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

Sie können [!UICONTROL Experience Fragments] in [!DNL Target] Aktivitäten mit dem [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!TIP]
>
>Verwenden von künstlicher Intelligenz, maschinellem Lernen und Recommendations mit [!UICONTROL Experience Fragments]:
>
>* Um die KI- und ML-Funktionen von [!DNL Target] in vollem Umfang zu nutzen, können Sie beim Erstellen einer Aktivität die Option [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisiertes Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) auswählen.
>
>* [!UICONTROL Experience Fragments] werden in [!DNL Recommendations] Aktivitäten nicht unterstützt. Um [!UICONTROL Experience Fragments] für Recommendations zu verwenden, können Sie eine [!UICONTROL A/B-Test]-Aktivität (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) oder eine [!UICONTROL Experience Targeting] (XT)-Aktivität erstellen und [Recommendations als Angebote einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).

**So verwenden Sie [!UICONTROL Experience Fragments] mithilfe des VEC:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses in [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) an die Stelle der Seite, an der Sie [!DNL AEM] Inhalt einfügen möchten, und klicken Sie dann auf **[!UICONTROL Inhalt ersetzen]** > **[!UICONTROL Experience Fragment]**, um das Dialogfeld [!UICONTROL Experience Fragment] anzuzeigen.

   Das [!UICONTROL Experience Fragment] zeigt den Inhalt an, der in [!DNL AEM] erstellt wurde, das nun nativ in [!DNL Target] verfügbar ist.

   >[!NOTE]
   >
   >Die [!UICONTROL Inhalt ersetzen] ist für Bilder nicht verfügbar. Wenn Sie diese Option mit einem Bild verwenden möchten, klicken Sie auf das Container-Element, das das gewünschte Bild enthält.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Wählen Sie das gewünschte [!UICONTROL Experience Fragment] aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

   Weitere Informationen über die Konfiguration der verschiedenen Aktivitätstypen finden Sie in den folgenden Themen:

   * **A/B-Test:** [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Automatische Zuordnung:** [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisches Targeting:** [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automatisierte Personalisierung (AP):** [Erstellen einer Aktivität zur automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Erlebnis-Targeting (XT):** [Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Recommendations in A/B-Tests oder XT-Aktivitäten:** [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments] die in [!DNL Target] als JSON exportiert wurden, können nicht in Aktivitäten verwendet werden, die mit dem VEC erstellt wurden. Nur [!UICONTROL Experience Fragments] in VEC-basierten Aktivitäten werden unterstützt. Wenn Sie JSON (Experience [!UICONTROL ) verwenden ], verwenden Sie sie in Aktivitäten, die mit dem [formularbasierten Experience Composer) ](/help/main/c-experiences/form-experience-composer.md).

**So verwenden Sie [!UICONTROL Experience Fragments] mithilfe des [!UICONTROL formularbasierten Experience Composer]:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) an der Stelle der Seite, an der Sie [!DNL AEM] Inhalt einfügen möchten, auf das Symbol **[!UICONTROL Weitere Details]** (Symbol ![Weitere Details](/help/main/assets/icons/MoreSmall.svg) ) und wählen Sie dann **[!UICONTROL Experience Fragment ändern]** aus, um das Dialogfeld [!UICONTROL Experience Fragment ändern] anzuzeigen.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   Das [!UICONTROL Experience Fragment] zeigt den Inhalt an, der in [!DNL AEM] erstellt wurde, das nun nativ in [!DNL Target] verfügbar ist.

1. Wählen Sie das gewünschte [!UICONTROL Experience Fragment] aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zusätzliche Informationen

* [!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Experience Fragments] die importiert werden sollen. Das importierte [!UICONTROL Experience Fragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.
* Das [!UICONTROL Experience Fragment] wird als HTML- oder JSON-Angebot in [!DNL Target] importiert. Die [!UICONTROL primäre] Version des Experience Fragments verbleibt in [!DNL AEM]. Das [!UICONTROL Experience Fragment“ kann nicht ] in [!DNL Target] bearbeitet werden.
* Mit [!DNL Adobe Developer] können Sie [!UICONTROL Experience Fragments] nicht erstellen. Erstellen Sie [!UICONTROL Experience Fragments] mithilfe von AEM, wie oben beschrieben.
* Wenn Sie Ihr [!UICONTROL Experience Fragment] in AEM aktualisieren, muss das [!UICONTROL Experience Fragment] erneut veröffentlicht und in [!DNL Target] exportiert werden, damit [!DNL Target] die neuesten Änderungen verwenden kann.

## Entfernen von Client-Bibliotheken und externem HTML aus [!UICONTROL Experience Fragments], die nach [!UICONTROL Target] exportiert wurden

Bei Verwendung von [!UICONTROL Experience Fragment]-Angeboten mit [!DNL Target] auf einer von AEM bereitgestellten Seite enthält die Zielseite bereits die erforderlichen Client-Bibliotheken. Beachten Sie außerdem, dass überflüssige HTML-Elemente im Angebot nicht erforderlich sind.

Manchmal umschließen komplette HTML-Seiten das [!UICONTROL Experience Fragment] und verursachen Probleme. Stellen Sie sicher[!UICONTROL  dass das ]Experience Fragment) ein kleines Stück HTML und keine vollständige HTML-Seite mit HTML, HEAD, BODY usw. ist.

Weitere Informationen finden Sie im folgenden Blogpost: [AEM 6.5: Removing clientlibs from [!UICONTROL Experience Fragments] exported to Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser/){target=_blank}.

## Schulungsvideo: Verwenden von AEM [!UICONTROL Experience Fragments] mit [!DNL Adobe Target]

Das folgende Video zeigt Ihnen, wie Sie (Experience Fragments[!UICONTROL  einrichten und ]:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>Die [!DNL AEM] Deeplink-Funktion, die unter 4:54 erläutert wurde, wurde entfernt.

Weitere Informationen finden Sie unter [Verwenden von [!UICONTROL Experience Fragments] mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=de) auf der Seite *AEM Sites-Videos und -*.
