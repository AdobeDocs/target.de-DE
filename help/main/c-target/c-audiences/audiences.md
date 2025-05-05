---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; Zielgruppentargeting; Zielgruppenberichterstellung; Zielgruppenbericht; Segment; benutzerdefinierte Profilparameter; Zielgruppendefinition; Zielgruppenliste
description: Erfahren Sie, wie Sie -Zielgruppen in  [!DNL Adobe Target].
title: Wie verwende ich die Audience-Liste?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 22%

---

# Erstellen von Zielgruppen

Zielgruppen in [!DNL Adobe Target] bestimmen, wer die Inhalte und Erlebnisse einer zielgerichteten Aktivität sieht.

Zielgruppen werden überall dort eingesetzt, wo Targeting zur Verfügung steht. Beim Targeting einer Aktivität stehen die folgenden Optionen zur Verfügung:

* Wählen Sie in der [!UICONTROL Audiences]-Liste eine wiederverwendbare Zielgruppe aus
* [Erstellen einer aktivitätsspezifischen Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) und Targeting
* [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) um eine Ad-hoc-Zielgruppe zu erstellen

Sie können auch von [!DNL Adobe Analytics] erfasste Zielgruppendaten für die Echtzeit-Zielgruppenbestimmung und -Personalisierung in [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Anwendungen verwenden. Siehe [Experience Cloud-Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) im *Handbuch für zentrale Experience Cloud-Schnittstellenkomponenten*.

Es gibt zwei Arten von Zielgruppen in [!DNL Target]:

* **Zielgruppen-Targeting** Wird verwendet, um verschiedene Inhalte für verschiedene Arten von Besuchern bereitzustellen.
* **Reporting-Zielgruppen:** Wird verwendet, um zu bestimmen, wie verschiedene Besuchertypen auf denselben Inhalt reagieren, damit Sie Ihre Testergebnisse analysieren können.

  In [!DNL Target] können Sie Berichtszielgruppen nur dann konfigurieren, wenn Sie [!DNL Target] als Berichtsquelle verwenden. Wenn Sie [Adobe Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, müssen Sie Ihre Reporting-Zielgruppen in [!DNL Analytics] konfigurieren.

## [!UICONTROL Audiences] verwenden {#use-list}

Um auf die [!UICONTROL Audiences] zuzugreifen, klicken Sie in der oberen Menüleiste auf **[!UICONTROL Audiences]**:

![[!UICONTROL Audiences] Liste](assets/audiences_list.png)

Die [!UICONTROL Audiences] enthält die Zielgruppen, die Sie in Ihren Aktivitäten verwenden können. Verwenden Sie die [!UICONTROL Audiences], um Zielgruppen zu erstellen, zu bearbeiten, zu duplizieren, zu kopieren oder zu kombinieren. In der Liste wird auch die Quelle angezeigt, in der die Zielgruppe erstellt wurde:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

  >[!NOTE]
  >
  >Die [!DNL Adobe Experience Platform] steht allen Kundinnen und Kunden zur Verfügung, [!DNL Target] die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} verwenden. Zielgruppen, die im [!DNL Adobe Experience Platform] verfügbar sind, können unverändert oder ([ mit bestehenden Zielgruppen kombiniert) ](/help/main/c-target/combining-multiple-audiences.md).
  >
  >Benutzende müssen mindestens [!UICONTROL Approver] Status in haben, [!DNL Target] sie [!DNL Target] [!UICONTROL Destinations] Karten in AEP/RTCDP ([!DNL Real-time Customer Data Platform]) konfigurieren können.
  >
  >Weitere Informationen finden Sie unter [Verwenden von Zielgruppen aus Adobe Experience Platform](#aep).

Vordefinierte Zielgruppen wie &quot;[!UICONTROL New Visitors]&quot; und &quot;[!UICONTROL Returning Visitors]&quot; können nicht umbenannt werden.

Beim Arbeiten mit Audiences, die ursprünglich in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] erstellt wurden, werden Sie [!DNL Target] benachrichtigt, wenn Sie in [!DNL Target] Aktivitäten, die später in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] gelöscht wurden, auf eine Audience verweisen.

* Wenn eine Zielgruppe in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] gelöscht wurde, wird ein Warnsymbol sowohl in der [!UICONTROL Audience] als auch in der Zielgruppenauswahl angezeigt. Eine QuickInfo in der [!DNL Target]-Benutzeroberfläche weist auch darauf hin, dass die Zielgruppe in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] gelöscht wurde.
* Wenn Sie versuchen, mehrere Zielgruppen mit einer gelöschten Zielgruppe zu kombinieren oder eine Aktivität zu speichern, die auf eine gelöschte Zielgruppe verweist, wird eine Warnmeldung angezeigt.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Erstellen einer Zielgruppe die Attribute, die Sie für Ihre Aktivität verwenden möchten, in das Fenster des Zielgruppen-Builders. Wenn das gewünschte Attribut nicht angezeigt wird, wurde das Attribut nicht von einer Mbox ausgelöst. Andere benutzerdefinierte Mbox-Parameter sind in der Dropdown-Liste [!UICONTROL Custom Parameters] verfügbar.

Verwenden Sie die Schaltfläche [!UICONTROL Filters] , um die [!UICONTROL Audiences] nach Quelle zu filtern: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud] und [!DNL Adobe Experience Platform].

![Option „Filter“ in der [!UICONTROL Audiences] Liste](assets/filters.png)

Durchsuchen Sie Ihre [!UICONTROL Audiences] mithilfe des [!UICONTROL Search audiences]. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Audiences] nach Zielgruppenname oder nach dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Anzeigen von Zielgruppendefinitionen {#section_11B9C4A777E14D36BA1E925021945780}

Sie können Details zur Zielgruppendefinition auf einer Popup-Karte an verschiedenen Stellen in der [!DNL Target]-Benutzeroberfläche anzeigen, ohne die Zielgruppe zu öffnen. Diese Funktion gilt für Zielgruppen, die in [!DNL Target Standard/Premium] erstellt wurden, und Zielgruppen, die aus [!DNL Target Classic] importiert oder über die API erstellt wurden.

Beispielsweise kann die folgende Karte für die Zielgruppendefinition durch Klicken auf das [!UICONTROL View Details] für die gewünschte Zielgruppe aufgerufen werden:

![Aktivitäten > Zielgruppendefinition](assets/audience_definition_list.png)

Sie können auf die folgende Karte zur Zielgruppendefinition zugreifen, indem Sie auf der [!UICONTROL Overview] einer Aktivität auf das Symbol [!UICONTROL View Details] klicken:

![Aktivitäten > Zielgruppendefinition](assets/view-details-activity-overview.png)

Die Karte zur Zielgruppendefinition zeigt den Typ, die Quelle und die Attribute der Zielgruppe an. Klicken Sie auf **[!UICONTROL View full details]** , um ggf. andere Aktivitäten anzuzeigen, die auf diese Zielgruppe verweisen. Wenn Sie eine Karte zur Zielgruppendefinition auf der [!UICONTROL Overview] einer Aktivität anzeigen, klicken Sie auf **[!UICONTROL Audience Usage]**.

Mithilfe der Informationen zur Zielgruppennutzung können Sie beim Bearbeiten von Zielgruppen versehentliche Auswirkungen auf andere Aktivitäten vermeiden. Zu den Informationen gehören [!UICONTROL Live Activities], [!UICONTROL Inactive Activities], [!UICONTROL Archived Activities] und [!UICONTROL Syncing Activities]. Diese Funktion ist für alle Zielgruppen verfügbar (Bibliotheks-Zielgruppen und [Nur-Aktivität-Zielgruppen](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Wenn eine Zielgruppe [mit einer anderen Zielgruppe kombiniert](/help/main/c-target/combining-multiple-audiences.md) und die kombinierte Zielgruppe zum Erstellen einer Aktivität verwendet wird, werden in den Nutzungsinformationen für beide Zielgruppen diese neu erstellte Aktivität aufgeführt.

![audience_definition_list_usage Bild](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/main/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/main/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/main/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/main/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## Verwenden von Audiences aus [!DNL Adobe Experience Platform] {#aep}

Die Verwendung der in [!DNL Adobe Experience Platform] erstellten Zielgruppen liefert umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen.

Weitere Informationen finden Sie unter &quot;[ von Zielgruppen [!DNL Adobe Experience Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#aep).

## Schulungsvideo: Verwenden von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/29395?captions=ger)
