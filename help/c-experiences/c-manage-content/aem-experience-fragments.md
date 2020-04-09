---
keywords: experience;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
description: Informationen zur Verwendung von in Adobe Experience Manager (AEM) erstellten Erlebnisfragmenten in Adobe Zielgruppe-Aktivitäten zur Optimierung oder Personalisierung.
title: Adobe Experience Manager (AEM)-Erlebnisfragmente in Adobe Zielgruppe
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: f243e0a74d5f4d91e399e1e64a0e0aa545517ee8

---


# AEM-Erlebnisfragmente{#aem-experience-fragments}

Information about using experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization.

>[!NOTE]
>
>Diese Funktion erfordert, dass Sie ein [!DNL Adobe Experience Manager] ([!DNL AEM]) Kunde sind. Weitere Informationen finden Sie unten unter [Anforderungen](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A).

## Überblick {#section_95A91830530F493B81C5C9CDB9B783EA}

Using experience fragments created in [!DNL AEM] in [!DNL Target] activities lets you combine the ease-of-use and power of [!DNL AEM] with powerful Automated Intelligence (AI) and Machine Learning (ML) capabilities in [!DNL Target] to test and personalize experiences at scale.

[!DNL AEM] kombiniert all Ihre Inhalte und Assets an einer zentralen Stelle, um Ihre Personalisierungsstrategie zu begünstigen. [!DNL AEM]Mit können Sie an einer Stelle problemlos Inhalte für Desktops, Tablets und mobile Geräte erstellen, ohne Code zu schreiben. Es ist nicht erforderlich, Seiten für jedes Gerät zu erstellen. [!DNL AEM] passt jedes Erlebnis automatisch mit Ihrem Inhalt an.

[!DNL Target]Mit können Sie personalisierte Erlebnisse bedarfsgerecht bereitstellen. Dies erfolgt auf der Grundlage einer Kombination aus regelbasierten und AI-gestützten Ansätzen des maschinellen Lernens, zu denen Verhaltens-, Kontext- und Offline-Variablen zählen. With [!DNL Target] you can easily set up and run [A/B Test](/help/c-activities/t-test-ab/test-ab.md) and [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activities to determine the best offers, content, and experiences.

Experience fragments represent a huge step forward to link the content/experience creators and managers to the optimization and personalization professionals who are driving business outcomes using [!DNL Target].

## Voraussetzungen  {#section_AE6F0971E1574B3AA324003599B96E5A}

You must be provisioned with the experience fragments functionality within [!DNl Target]. In addition, you must be using [!DNL AEM] 6.3 with the appropriate service pack or [!DNL AEM] 6.4 (or later). Ihr Kundenbetreuer kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

* [!DNL Adobe Experience Manager] 6.4 (oder höher).
* [!DNL Adobe Experience Manager] 6.3 SP2 (oder höher).
* [!DNL Adobe Target Standard] oder [!DNL Adobe Target Premium] Konto.
* Contact [Adobe Target Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## Creating and configuring experience fragments in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to use [!DNL AEM] experience fragments in [!DNL Target], you must perform the following steps:

### Schritt 1: Integrieren [!DNL AEM] mit [!DNL Target]

Weitere Informationen finden Sie unter:

* **[!DNL AEM]6.3 **: Entscheidung[für Adobe Analytics und Adobe-Zielgruppe](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html)in der_Dokumentation zu Adobe Experience Manager 6.3 _.
* **[!DNL AEM]6.4 **: Entscheidung[für Adobe Analytics und Adobe-Zielgruppe](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html)in der_Dokumentation zu Adobe Experience Manager 6.4 _.
* **[!DNL AEM]6.5 **: Entscheidung[für Adobe Analytics und Adobe-Zielgruppe](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html)in der *Dokumentation zu Adobe Experience Manager 6.5*.

### Schritt 2: Erlebnisfragment erstellen

Experience fragments are created in [!DNL AEM]. Weitere Informationen finden Sie unter:

* **[!DNL AEM]6.3 **:[Erlebnisfragmente](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html)in der Dokumentation zu *Adobe Experience Manager 6.3*.
* **[!DNL AEM]6.4 **:[Erlebnisfragmente](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html)in der Dokumentation zu *Adobe Experience Manager 6.4*.
* **[!DNL AEM]6.5 **:[Erlebnisfragmente](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html)in der Dokumentation zu *Adobe Experience Manager 6.5*.

### Step 3: Configure [!DNL AEM] to share the experience fragment with [!DNL Target]

1. From within [!DNL AEM], select the desired experience fragment or its containing folder, then click **[!UICONTROL Properties]**.
2. Klicken Sie auf die Registerkarte **[!UICONTROL Cloud-Services]** und wählen Sie dann in der Dropdownliste **[!UICONTROL Cloud-Servicekonfiguration]** den Eintrag **[!UICONTROL Adobe Target]** aus.

   >[!NOTE]
   >
   >The previous step assumes that someone in your organization has created the [!DNL Adobe Target] configuration.

3. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

### Schritt 4: Das Erlebnisfragment veröffentlichen und nach exportieren[!DNL Target]

Abhängig von Ihrer [!DNL AEM] Version finden Sie unter den folgenden Links schrittweise Anweisungen:

* **[!DNL AEM]6.3 **: Exportieren[eines Erlebnisfragments in Zielgruppen](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html)in der *Adobe Experience Manager 6.3*-Dokumentation.
* **[!DNL AEM]6.4 **:[Exportieren eines Erlebnisfragments in Zielgruppen](https://docs.adobe.com/content/help/en/experience-manager-64/administering/integration/experience-fragments-target.html)in der *Adobe Experience Manager 6.4*-Dokumentation.
* **[!DNL AEM]6.5 **:[Exportieren eines Erlebnisfragments in Zielgruppen](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html)in der *Adobe Experience Manager 6.5*-Dokumentation.

## Using experience fragments in DNL Target activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

After performing the preceding tasks, the experience fragment displays on the [!UICONTROL Offers] page in [!DNL Target].

>[!NOTE]
>
>[!DNL Target] sucht derzeit alle zehn Minuten nach zu importierenden Erlebnisfragmenten. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.

>[!IMPORTANT]
>
>The experience fragment is currently imported into [!DNL Target] as an HTML offer. Note that the experience fragment &quot;master&quot; version remains in [!DNL AEM]. You cannot edit the experience fragment in [!DNL Target].

Sie können den Mauszeiger über ein Erlebnisfragment in der Liste bewegen und dann auf das Symbol für die [!UICONTROL Ansicht] - ![Ansicht](assets/icon_info.png) klicken, um weitere Informationen zum Erlebnisfragment anzuzeigen, einschließlich der URL des öffentlichen Angebots und des zugehörigen [!DNL AEM] Pfads.

You can consume experience fragments in [!DNL Target] activities using the [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) or the [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>To fully utilize the [!DNL Target] AI and ML functionality, you can select [Auto-Allocate](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) while creating an A/B Test.

**So verwenden Sie Erlebnisfragmente mit VEC:**

1. Klicken Sie [!DNL Target]beim Erstellen oder Bearbeiten eines Erlebnisses im [Visual Experience Composer](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)auf die Stelle auf der Seite, auf der Sie [!DNL AEM] Inhalte einfügen möchten, und wählen Sie dann die gewünschte Option aus, um die Liste &quot;Erlebnisfragment  auswählen&quot;anzuzeigen.

   * [!UICONTROL Einfügen vor]
   * [!UICONTROL Einfügen nach]
   * [!UICONTROL Erlebnisfragment austauschen]
   The [!UICONTROL Experience Fragment] list displays all of the content created in [!DNL AEM] that is now natively available from within [!DNL Target].

   >[!NOTE]
   >
   >Die Option [!UICONTROL Mit Erlebnisfragment tauschen] ist nicht für Bilder verfügbar. Wenn Sie diese Option mit einem Bild verwenden möchten, klicken Sie auf das Containerelement, das das gewünschte Bild enthält.

   ![](assets/experience_fragment_list.png)

1. Select the desired experience fragment, then click **[!UICONTROL Done]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

   Weitere Informationen über die Konfiguration der verschiedenen Aktivitätstypen finden Sie in den folgenden Themen:

   * **A/B-Test:** [Erstellen eines A/B-Tests](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
   * **Automatische Zuordnung:** [Automatische Zuordnung](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisches Targeting:** [Automatisches Targeting für personalisierte Erlebnisse](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)
   * **Automatisierte Personalisierung (AP):**[Erstellen einer Aktivität zur automatisierten Personalisierung](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Erlebnis-Targeting (XT):** [Erstellen einer Erlebnis-Targeting-Aktivität](../../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Multivarianz-Tests (MVT):** [Erstellen eines Multivarianz-Tests](../../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendations:** [Erstellen einer Recommendations-Aktivität](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**So verwenden Sie Erlebnisfragmente mit dem Form-Based Experience Composer:**

1. In [!DNl Target], while creating or editing an experience in the [Form-Based Experience Composer](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), select the location on the page where you want to insert [!DNL AEM] content, then select **[!UICONTROL Change Experience Fragment]** to display the [!UICONTROL Choose an Experience Fragment] list.

   ![](assets/experience_fragment_list.png)

   The [!UICONTROL Experience Fragment] list displays all of the content created in [!DNL AEM] that is now natively available from within [!DNL Target].

1. Wählen Sie das gewünschte Erlebnisfragment aus und klicken Sie dann auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zu beachten {#considerations}

* [!DNL Target] sucht derzeit alle zehn Minuten nach zu importierenden Erlebnisfragmenten. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The experience fragment is currently imported into [!DNL Target] as an HTML offer. Note that the experience fragment &quot;master&quot; version remains in [!DNL AEM]. You cannot edit the experience fragment in [!DNL Target].
* Sie können JSON-Angebot als Erlebnisfragmente in importieren [!DNL Target]. Diese Angebot werden jedoch als HTML-Angebot importiert. JSON-Angebot (Erlebnisfragmente) werden derzeit nicht vollständig in der [!DNL Target] Benutzeroberfläche unterstützt.

## Schulungsvideo: Verwenden von DNL-AEM-Erlebnisfragmenten mit Adobe Zielgruppe {#section_C0EDC54063464F41A182492D2045BC64} Tutorial- ![Abzeichen](/help/assets/overview.png)

Das folgende Video zeigt Ihnen, wie Sie Erlebnisfragmente einrichten und verwenden:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>Die [!DNL AEM] deeplink-Funktion, die um 4:54 besprochen wurde, wurde entfernt.

Weitere Informationen finden Sie unter [Verwenden von Erlebnisfragmenten mit Adobe-Zielgruppe](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) auf der Seite mit Videos und Tutorials *zu* AEM-Sites.
