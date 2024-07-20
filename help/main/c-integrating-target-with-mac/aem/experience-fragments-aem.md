---
keywords: experience;json;aem;adobe experience manager;in adobe target exportieren;experience fragments;fragments;XF
description: Erfahren Sie, wie Sie [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in [!DNL Adobe Target] Aktivitäten verwenden.
title: Wie verwende ich [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
source-git-commit: 7c81362a82ca6692bb8c183b8e8fc50c6329e2e8
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 36%

---

# AEM [!UICONTROL Experience Fragments]

Verwenden Sie [!UICONTROL Experience Fragments] (XFs), die in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] -Aktivitäten erstellt wurden, um die Optimierung und Personalisierung zu unterstützen.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Experience Fragments] in [!DNL Target]:

* Für diese Funktion müssen Sie [!DNL Adobe Experience Manager] (AEM)-Kundin bzw. -Kunde sein. Weitere Informationen finden Sie unten unter [Anforderungen](#section_AE6F0971E1574B3AA324003599B96E5A).
* [!UICONTROL Experience Fragments] und [!UICONTROL Content Fragments] sind für die folgenden Aktivitätstypen verfügbar:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] und [!UICONTROL Content Fragments] sind für die folgenden Aktivitätstypen nicht verfügbar:

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* Sie können [!UICONTROL Experience Fragments] in [!DNL Target] -Aktivitäten verwenden, indem Sie den [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden.

Weitere Informationen zu AEM [!UICONTROL Experience Fragments] und [!UICONTROL Content Fragments] finden Sie unter [AEM [!UICONTROL Experience Fragments] und Übersicht über Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen  {#requirements}

Sie müssen über die Funktion [!UICONTROL Experience Fragments] in [!DNL Target] verfügen. Darüber hinaus müssen Sie [!DNL AEM] as a Cloud Service oder [!DNL AEM] 6.4 (oder höher) nutzen. Ihre Kundenkontaktperson kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

* [!DNL Adobe Experience Manager] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard]- oder [!DNL Adobe Target Premium]-Konto.

[!DNL Adobe Experience Manager] 6.3 und 6.4 haben das Ende des Lebenszyklus erreicht und werden nicht mehr unterstützt (mit Ausnahme von Kundinnen und Kunden, die erweiterte Unterstützung erworben haben).

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Erstellen und Konfigurieren von [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target] zu verwenden, müssen Sie die folgenden Schritte ausführen:

### Schritt 1: Integrieren von [!DNL AEM] mit [!DNL Target]

Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [Integration mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html?lang=de){target=_blank} im Handbuch zu *Experience Manager as a Cloud Service*.
* **Adobe I/O**: [Integration mit Adobe Target mithilfe von Adobe I/O](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html?lang=de){target=_blank} in der Dokumentation *Handbuch zur Benutzerverwaltung*.
* **[!DNL AEM]6.5**: [Einbindung in Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Einbindung in Adobe Analytics und Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 2: Erstellen des Experience Fragments

[!UICONTROL Experience Fragments] werden in [!DNL AEM] erstellt. Weitere Informationen finden Sie unter:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=de){target=_blank} in der Anleitung *Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 3: Konfigurieren Sie [!DNL AEM] für die Freigabe der [!UICONTROL Experience Fragment] für [!DNL Target]

1. Wählen Sie innerhalb von [!DNL AEM] den gewünschten Ordner [!UICONTROL Experience Fragment] oder den ihn enthaltenden Ordner aus und klicken Sie dann auf **[!UICONTROL Properties]**.
2. Klicken Sie auf die Registerkarte **[!UICONTROL Cloud Services]** und wählen Sie dann aus der Dropdownliste **[!UICONTROL Cloud Service Configuration]** die Option **[!UICONTROL Adobe Target]** aus.

   Beim vorherigen Schritt wird davon ausgegangen, dass die [!DNL Adobe Target]-Konfiguration von einem Benutzer in Ihrem Unternehmen erstellt wurde.

3. Klicken Sie auf **[!UICONTROL Save & Close]**.

### Schritt 4: Publish der [!UICONTROL Experience Fragment] und Export in [!DNL Target]

Abhängig von Ihrer [!DNL AEM]-Version finden Sie unter den folgenden Links schrittweise Anweisungen:

* **AEM as a Cloud Service**: [Exportieren von [!UICONTROL Experience Fragments] nach Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=de){target=_blank} im Handbuch *Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Exportieren von einem Experience Fragment nach Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=de){target=_blank} in der Dokumentation zu *Adobe Experience Manager 6.4*.

## Verwenden von [!UICONTROL Experience Fragments] in [!DNL Target] -Aktivitäten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach dem Ausführen der vorherigen Aufgaben wird der [!UICONTROL Experience Fragment] auf der Seite [!UICONTROL Offers] in [!DNL Target] angezeigt.

[!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Experience Fragments] zum Importieren. Der importierte [!UICONTROL Experience Fragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein, aber dieser Zeitraum sollte in Zukunft reduziert werden.

Die [!UICONTROL Experience Fragment] wird als HTML- oder JSON-Angebot in [!DNL Target] importiert. Die &quot;primäre&quot;Version von [!UICONTROL Experience Fragment] verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Experience Fragment] in [!DNL Target] nicht bearbeiten.

Sie können nach [!UICONTROL HTML XFs] und [!UICONTROL JSON XFs] filtern und suchen, um zwischen den [!UICONTROL Experience Fragment] Typen zu unterscheiden, die nach [!DNL Target] exportiert werden.

![Filtern nach Experience Fragment-Typen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über einen [!UICONTROL Experience Fragment] in der Liste bewegen und dann auf das [!UICONTROL View]-Symbol ![Info-Symbol](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) klicken, um zusätzliche Informationen über den [!UICONTROL Experience Fragment] anzuzeigen, einschließlich der [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path] und der letzten Änderungsinformationen. Klicken Sie auf den Tab [!UICONTROL Offer Usage] , um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

![Popup mit Experience Fragment-Informationen](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

Sie können [!UICONTROL Experience Fragments] in [!DNL Target] -Aktivitäten verwenden, indem Sie den [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden.


>[!TIP]
>
>Verwenden Sie künstliche Intelligenz, maschinelles Lernen und Empfehlungen mit [!UICONTROL Experience Fragments]:
>
>* Um die KI- und ML-Funktionen von [!DNL Target] in vollem Umfang zu nutzen, können Sie beim Erstellen einer Aktivität die Option [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisiertes Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) auswählen.
>
>* [!UICONTROL Experience Fragments] wird in [!DNL Recommendations] -Aktivitäten nicht unterstützt. Um jedoch [!UICONTROL Experience Fragments] für Empfehlungen zu verwenden, können Sie eine [!UICONTROL A/B Test] -Aktivität (einschließlich [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target]) oder eine [!UICONTROL Experience Targeting] -Aktivität (XT) erstellen und [Empfehlungen als Angebot einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).

**So verwenden Sie [!UICONTROL Experience Fragments] mit dem VEC:**

1. Klicken Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) auf die Stelle auf der Seite, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann die gewünschte Option aus, um die Liste [!UICONTROL Choose an Experience Fragment] anzuzeigen.

   * [!UICONTROL Insert Before]
   * [!UICONTROL Insert After]
   * [!UICONTROL Swap with Experience Fragment]

   Die Liste [!UICONTROL Experience Fragment] zeigt den in [!DNL AEM] erstellten Inhalt an, der jetzt nativ in [!DNL Target] verfügbar ist.

   >[!NOTE]
   >
   >Die Option [!UICONTROL Swap with Experience Fragment] ist für Bilder nicht verfügbar. Wenn Sie diese Option mit einem Bild verwenden möchten, klicken Sie auf das Container-Element, das das gewünschte Bild enthält.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Wählen Sie den gewünschten [!UICONTROL Experience Fragment] aus und klicken Sie dann auf **[!UICONTROL Done]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

   Weitere Informationen über die Konfiguration der verschiedenen Aktivitätstypen finden Sie in den folgenden Themen:

   * **A/B-Test:** [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Automatische Zuordnung:** [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisches Targeting:** [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automatisierte Personalisierung (AP):** [Erstellen einer Aktivität zur automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Erlebnis-Targeting (XT):** [Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Recommendations in A/B-Tests oder XT-Aktivitäten:** [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments], der als JSON in [!DNL Target] exportiert wurde, kann nicht in Aktivitäten verwendet werden, die mit VEC erstellt wurden. In VEC-basierten Aktivitäten wird nur HTML [!UICONTROL Experience Fragments] unterstützt. Wenn Sie JSON [!UICONTROL Experience Fragments] verwenden möchten, verwenden Sie sie in Aktivitäten, die mit dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) erstellt wurden.

**So verbrauchen Sie [!UICONTROL Experience Fragments] mit dem [!UICONTROL Form-based Experience Composer]:**

1. Wählen Sie in [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) die Stelle auf der Seite aus, an der Sie [!DNL AEM]-Inhalte einfügen möchten, und wählen Sie dann **[!UICONTROL Change Experience Fragment]** aus, um die Liste [!UICONTROL Choose an Experience Fragment] anzuzeigen.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   Die Liste [!UICONTROL Experience Fragment] zeigt den in [!DNL AEM] erstellten Inhalt an, der jetzt nativ in [!DNL Target] verfügbar ist.

1. Wählen Sie den gewünschten [!UICONTROL Experience Fragment] aus und klicken Sie dann auf **[!UICONTROL Save]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zusätzliche Informationen

* [!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Experience Fragments] zum Importieren. Der importierte [!UICONTROL Experience Fragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein, aber dieser Zeitraum sollte in Zukunft reduziert werden.
* Die [!UICONTROL Experience Fragment] wird als HTML- oder JSON-Angebot in [!DNL Target] importiert. Die &quot;primäre&quot;Version von [!UICONTROL Experience Fragment] verbleibt in [!DNL AEM]. Sie können die [!UICONTROL Experience Fragment] in [!DNL Target] nicht bearbeiten.
* Sie können [!UICONTROL Experience Fragments] nicht mit [!DNL Adobe I/O] erstellen. Erstellen Sie [!UICONTROL Experience Fragments] mit AEM, wie oben beschrieben.
* Wenn Sie Ihre [!UICONTROL Experience Fragment] in AEM aktualisieren, muss der [!UICONTROL Experience Fragment] erneut veröffentlicht und in [!DNL Target] exportiert werden, damit [!DNL Target] die neuesten Änderungen verwenden kann.

## Entfernen von ClientLibs und irrelevanten HTML aus [!UICONTROL Experience Fragments], die nach [!UICONTROL Target] exportiert wurden

Bei Verwendung von [!UICONTROL Experience Fragment] Angeboten mit [!DNL Target] auf einer von AEM bereitgestellten Seite enthält die Zielseite bereits alle erforderlichen Client-Bibliotheken. Beachten Sie außerdem, dass überflüssige HTML-Elemente im Angebot nicht erforderlich sind.

Manchmal umschließen ganze HTML-Seiten den [!UICONTROL Experience Fragment] und verursachen Probleme. Stellen Sie sicher, dass der [!UICONTROL Experience Fragment] ein kleines Stück HTML und keine vollständige HTML-Seite mit HTML, HEAD, BODY usw. ist.

Weitere Informationen finden Sie im folgenden Blogpost: [AEM 6.5: Entfernen von ClientLibs aus [!UICONTROL Experience Fragments], die nach Target exportiert wurden](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Schulungsvideo: Verwenden von AEM [!UICONTROL Experience Fragments] mit [!DNL Adobe Target]

Im folgenden Video erfahren Sie, wie Sie [!UICONTROL Experience Fragments] einrichten und verwenden:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>Die [!DNL AEM]-Deeplink-Funktion, die in 4:54 erläutert wurde, wurde entfernt.

Weitere Informationen finden Sie unter [Verwenden von [!UICONTROL Experience Fragments] mit Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=de) auf der Seite *AEM Sites-Videos und Tutorials* .
