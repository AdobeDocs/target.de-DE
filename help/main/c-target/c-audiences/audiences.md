---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; Zielgruppentargeting; Zielgruppenberichterstellung; Zielgruppenbericht; Segment; benutzerdefinierte Profilparameter; Zielgruppendefinition; Zielgruppenliste
description: Learn how to use audiences in [!DNL Adobe Target].
title: How Do I Use the Audience List?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: f984f2db3ccfb02629ddfd4f3c5f957256bd9f6a
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 22%

---

# Erstellen von Zielgruppen

Audiences in [!DNL Adobe Target] determine who sees content and experiences in a targeted activity.

Zielgruppen werden überall dort eingesetzt, wo Targeting zur Verfügung steht. When targeting an activity, you have the following options:

* Select a reusable audience from the [!UICONTROL Audiences] list
* [Create an activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) and target it
* [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) um eine Ad-hoc-Zielgruppe zu erstellen

Sie können auch von [!DNL Adobe Analytics] erfasste Zielgruppendaten für die Echtzeit-Zielgruppenbestimmung und -Personalisierung in [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Anwendungen verwenden. Siehe [Experience Cloud-Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) im *Handbuch für die Komponenten der zentralen Experience Cloud* Benutzeroberfläche.

Es gibt zwei Arten von Zielgruppen in [!DNL Target]:

* **Zielgruppen-Targeting** Wird verwendet, um verschiedene Inhalte für verschiedene Arten von Besuchern bereitzustellen.
* **Reporting-Zielgruppen:** Wird verwendet, um zu bestimmen, wie verschiedene Besuchertypen auf denselben Inhalt reagieren, damit Sie Ihre Testergebnisse analysieren können.

  In [!DNL Target] können Sie Berichtszielgruppen nur dann konfigurieren, wenn Sie [!DNL Target] als Berichtsquelle verwenden. Wenn Sie [Adobe Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, müssen Sie Ihre Reporting-Zielgruppen in [!DNL Analytics] konfigurieren.

## [!UICONTROL Audiences] verwenden {#use-list}

Um auf die [!UICONTROL Audiences] zuzugreifen, klicken Sie in der oberen Menüleiste auf **[!UICONTROL Audiences]**:

![[!UICONTROL Audiences] Liste](assets/audiences_list.png)

Die [!UICONTROL Audiences] enthält die Zielgruppen, die Sie in Ihren Aktivitäten verwenden können. Use the [!UICONTROL Audiences] list to create, edit, duplicate, copy, or combine audiences. The list also shows the source where the audience was created:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

  >[!NOTE]
  >
  >The [!DNL Adobe Experience Platform] source is available to all [!DNL Target] customers using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}. Audiences available from the [!DNL Adobe Experience Platform] can be used as is or [combined with existing audiences](/help/main/c-target/combining-multiple-audiences.md).
  >
  >Users must have [!UICONTROL Approver] or above status in [!DNL Target] to configure [!DNL Target] [!UICONTROL Destinations] cards in AEP/RTCDP ([!DNL Real-time Customer Data Platform]).
  >
  >For more information see [Use audiences from Adobe Experience Platform](#aep).

Predefined audiences, such as &quot;[!UICONTROL New Visitors]&quot; and &quot;[!UICONTROL Returning Visitors],&quot; cannot be renamed.

When working with audiences that were originally created in [!DNL Experience Cloud] or [!DNL Adobe Experience Platform], [!DNL Target] alerts you if you reference an audience in [!DNL Target] activities that have later been deleted in [!DNL Experience Cloud] or [!DNL Adobe Experience Platform].

* If an audience was deleted in [!DNL Experience Cloud] or [!DNL Adobe Experience Platform], a warning icon in both the [!UICONTROL Audience] list and the audience picker displays. A tool-tip in the [!DNL Target] UI also indicates that the audience was deleted in [!DNL Experience Cloud] or [!DNL Adobe Experience Platform].
* Wenn Sie versuchen, mehrere Zielgruppen mit einer gelöschten Zielgruppe zu kombinieren oder eine Aktivität zu speichern, die auf eine gelöschte Zielgruppe verweist, wird eine Warnmeldung angezeigt.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. When creating an audience, drag the attributes you want to use to target your activity into the audience builder window. If the desired attribute does not display, the attribute has not been fired by an mbox. Andere benutzerdefinierte Mbox-Parameter sind in der Dropdown-Liste [!UICONTROL Custom Parameters] verfügbar.

Verwenden Sie die Schaltfläche [!UICONTROL Filters] , um die [!UICONTROL Audiences] nach Quelle zu filtern: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud] und [!DNL Adobe Experience Platform].

![Option „Filter“ in der [!UICONTROL Audiences] Liste](assets/filters.png)

Durchsuchen Sie Ihre [!UICONTROL Search audiences] mithilfe des [!UICONTROL Audiences]. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Audiences] nach Zielgruppenname oder nach dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Anzeigen von Zielgruppendefinitionen {#section_11B9C4A777E14D36BA1E925021945780}

Sie können Details zur Zielgruppendefinition auf einer Popup-Karte an verschiedenen Stellen in der [!DNL Target]-Benutzeroberfläche anzeigen, ohne die Zielgruppe zu öffnen. Diese Funktion gilt für Zielgruppen, die in [!DNL Target Standard/Premium] erstellt wurden, und Zielgruppen, die aus [!DNL Target Classic] importiert oder über die API erstellt wurden.

Beispielsweise kann die folgende Karte für die Zielgruppendefinition durch Klicken auf das [!UICONTROL View Details] für die gewünschte Zielgruppe aufgerufen werden:

![Aktivitäten > Zielgruppendefinition](assets/audience_definition_list.png)

Sie können auf die folgende Karte zur Zielgruppendefinition zugreifen, indem Sie auf der [!UICONTROL View Details] einer Aktivität auf das Symbol [!UICONTROL Overview] klicken:

![Aktivitäten > Zielgruppendefinition](assets/view-details-activity-overview.png)

The audience definition card shows they audience&#39;s type, source, and attributes. Click **[!UICONTROL View full details]** to see other activities that reference that audience, if applicable. If you are viewing an audience definition card from an activity&#39;s [!UICONTROL Overview] page, click **[!UICONTROL Audience Usage]**.

The audience usage information can help you avoid accidental impact to other activities while editing audiences. Information includes [!UICONTROL Live Activities], [!UICONTROL Inactive Activities], [!UICONTROL Archived Activities], and [!UICONTROL Syncing Activities]. This feature is available for all audiences (Library audiences and [activity-only audiences](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

If an audience is [combined with another audience](/help/main/c-target/combining-multiple-audiences.md) and the combined audience is used to create an activity, the usage information for both audiences lists that newly created activity.

![audience_definition_list_usage Bild](assets/audience_definition_list_usage.png)

<!--
The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/main/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/main/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/main/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/main/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.
-->

## Verwenden von Zielgruppen aus [!DNL Adobe Experience Platform] {#aep}

Die Verwendung der in [!DNL Adobe Experience Platform] erstellten Zielgruppen liefert umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen.

Weitere Informationen finden Sie unter &quot;[&#x200B; von Zielgruppen [!DNL Adobe Experience Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#aep).

## Schulungsvideo: Verwenden von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/29395?captions=ger)
