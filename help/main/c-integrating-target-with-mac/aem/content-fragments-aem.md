---
keywords: Erlebnis;JSON;AEM;Adobe Experience Manager;in Adobe Target exportieren;Inhaltsfragmente;Fragmente;CF;cf;Headless;Personalisierung;Experimente
description: Erfahren Sie, wie Sie  [!DNL Adobe Experience Manager] [!UICONTROL &#x200B; Inhaltsfragmente &#x200B;] Aktivitäten  [!DNL Adobe Target] .
title: Wie verwende ich ( [!DNL Adobe Experience Manager] ) [!UICONTROL Inhaltsfragmente]?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
TQID: https://experienceleague.adobe.com/tb500kFSZoR3czs10Gs3EIOWEX2ybnd7tSWwDmWSMWQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 775
ht-degree: 20%

---

# AEM [!UICONTROL Inhaltsfragmente]

Verwenden Sie [!UICONTROL Inhaltsfragmente], die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target] Aktivitäten, um die Headless-Personalisierung und -Experimentierung zu unterstützen.

## Zu beachten

Beachten Sie Folgendes bei der Arbeit mit AEM [!UICONTROL Inhaltsfragmenten] in [!DNL Target]:

* Diese Funktion erfordert, dass Sie eine Kundin oder ein Kunde von [!DNL Adobe Experience Manager as a Cloud Service] sind. Weitere Informationen finden Sie unten unter [Anforderungen](#section_AE6F0971E1574B3AA324003599B96E5A).
* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind für die folgenden Aktivitätstypen verfügbar:

   * [[!UICONTROL A/B-Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Automatische Zuordnung]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Automatisches Targeting]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] sind für die folgenden Aktivitätstypen nicht verfügbar:

   * [[!UICONTROL Multivariate Tests] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* Sie können [!UICONTROL Inhaltsfragmente] nur in [!DNL Target] Aktivitäten aufnehmen, die den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden. Sie *(*) [!UICONTROL Inhaltsfragmente] in [!DNL Target] Aktivitäten mit dem [!UICONTROL Visual Experience Composer] (VEC) verwenden.

Weitere Informationen zu AEM [!UICONTROL Inhaltsfragmenten] und [!UICONTROL Experience Fragments] finden Sie unter [AEM [!UICONTROL Experience Fragments] und [!UICONTROL Inhaltsfragmente] Übersicht](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Voraussetzungen {#requirements}

Sie müssen [[!DNL AEM] as a Cloud Service verwenden](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=de){target=_blank}. Ihre Kundenkontaktperson kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

Wenden Sie sich an die [Adobe Target-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Konfigurieren und Verwenden von [!UICONTROL Inhaltsfragmenten] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um [!UICONTROL Inhaltsfragmente] zur Verwendung in [!DNL Target]-Aktivitäten zu exportieren, müssen Sie einige vorbereitende Schritte in AEM durchführen. Weitere Informationen finden Sie unter [Exportieren von Inhaltsfragmenten nach Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=de){target=_blank} in der *Dokumentation zu Experience Manager as a Cloud Service*.

Weitere Informationen zum Entwerfen, Erstellen, Kuratieren und Veröffentlichen [!UICONTROL Inhaltsfragmente] finden Sie unter [[!UICONTROL Inhaltsfragmente]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=de){target=_blank} und [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=de){target=_blank} in der [Dokumentation zu Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=de){target=_blank}.

## Verwenden [!UICONTROL Inhaltsfragmenten] in [!DNL Target] Aktivitäten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach dem Ausführen der zuvor genannten Aufgaben wird [!UICONTROL Inhaltsfragment] auf der Seite [!UICONTROL Angebote] in [!DNL Target] angezeigt.

[!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Inhaltsfragmenten] die importiert werden sollen. Das [!UICONTROL Inhaltsfragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.

Das [!UICONTROL Inhaltsfragment] wird als JSON-Angebot in [!DNL Target] importiert. Die [!UICONTROL primäre] Version des Inhaltsfragments verbleibt in [!DNL AEM]. Das [!UICONTROL Inhaltsfragment“ kann nicht &#x200B;] [!DNL Target] bearbeitet werden.

Sie können nach [!UICONTROL HTML-XFs], [!UICONTROL JSON-XFs] und [!UICONTROL Inhaltsfragmenten] filtern und suchen, damit Sie zwischen verschiedenen Angebotstypen unterscheiden können, die in [!DNL Target] exportiert werden.

![Filtern nach Inhaltsfragmenttypen: HTML oder JSON in der Target-Benutzeroberfläche](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Sie können den Mauszeiger über ein [!UICONTROL Experience Fragment] in der Liste bewegen und dann auf das [!UICONTROL Ansicht]-Symbol ![Info-](/help/main/assets/icons/InfoOutline.svg) klicken, um zusätzliche Informationen zum [!UICONTROL Inhaltsfragment] anzuzeigen, darunter [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Angebots-ID], [!UICONTROL Angebotspfad] Informationen zur letzten Änderung. Klicken Sie [!UICONTROL [!UICONTROL Vollständige Details anzeigen]], um die Aktivitäten anzuzeigen, die auf dieses Angebot verweisen.

Sie können [!UICONTROL Inhaltsfragmente] nur in [!DNL Target] Aktivitäten aufnehmen, die den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) verwenden. Sie *(*) [!UICONTROL Inhaltsfragmente] in [!DNL Target] Aktivitäten mit dem [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) verwenden. [!UICONTROL Inhaltsfragmente] werden in [!DNL Target] als JSON exportiert und können nicht in Aktivitäten verwendet werden, die mit VEC erstellt wurden.

>[!TIP]
>
>Verwenden von künstlicher Intelligenz, maschinellem Lernen und Recommendations mit [!UICONTROL Inhaltsfragmenten]:
>
>* Um die KI- und ML-Funktionen von [!DNL Target] in vollem Umfang zu nutzen, können Sie [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) beim Erstellen einer [!UICONTROL A/B-Test]-Aktivität auswählen.
>
>* [!UICONTROL Inhaltsfragmente] werden in [!DNL Recommendations] Aktivitäten nicht unterstützt. Um [!UICONTROL Inhaltsfragmente) für Recommendations &#x200B;] verwenden zu können, können Sie eine [!UICONTROL A/B-Test]-Aktivität (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) oder eine [!UICONTROL Experience Targeting] (XT)-Aktivität erstellen und [Recommendations als Angebote einschließen](/help/main/c-recommendations/recommendations-as-an-offer.md).

**So verwenden Sie [!UICONTROL Inhaltsfragmente] mithilfe des [!UICONTROL formularbasierten Experience Composer]:**

1. Klicken Sie [!DNL Target] beim Erstellen oder Bearbeiten eines Erlebnisses im [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) an die Stelle der Seite, an der Sie [!DNL AEM] Inhalt einfügen möchten, und wählen Sie dann **[!UICONTROL Inhaltsfragment ändern]** aus, um die Liste [!UICONTROL Inhaltsfragment auswählen] anzuzeigen.

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   In [!UICONTROL &#x200B; Liste „Inhaltsfragment] werden alle in [!DNL AEM] erstellten Inhalte angezeigt, die nun nativ in [!DNL Target] verfügbar sind.

1. Wählen Sie das gewünschte [!UICONTROL Inhaltsfragment] aus und klicken Sie dann auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Zusätzliche Informationen

* [!DNL Target] sucht derzeit alle zehn Minuten nach [!UICONTROL Inhaltsfragmenten] die importiert werden sollen. Das [!UICONTROL Inhaltsfragment] sollte innerhalb von zehn Minuten in [!DNL Target] verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.
* Das [!UICONTROL Inhaltsfragment] wird als JSON-Angebot in [!DNL Target] importiert. Die [!UICONTROL primäre] Version des Inhaltsfragments verbleibt in [!DNL AEM]. Das [!UICONTROL Inhaltsfragment“ kann nicht &#x200B;] [!DNL Target] bearbeitet werden.
* Mit [!DNL Adobe I/O] können Sie [!UICONTROL Inhaltsfragmente] nicht erstellen. Erstellen Sie [!UICONTROL Inhaltsfragmente] mithilfe von AEM, wie oben beschrieben.
* Wenn Sie Ihr [!UICONTROL Inhaltsfragment] in AEM aktualisieren, muss das [!UICONTROL Inhaltsfragment] erneut veröffentlicht und in [!DNL Target] exportiert werden, damit [!DNL Target] die neuesten Änderungen verwenden kann.
