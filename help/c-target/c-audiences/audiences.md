---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; Zielgruppentargeting; Zielgruppenberichterstellung; Zielgruppenbericht; Segment; benutzerdefinierte Profilparameter; Zielgruppendefinition; Zielgruppenliste
description: Erfahren Sie, wie Sie die Liste [!UICONTROL Zielgruppen] in [!DNL Adobe Target] verwenden.
title: Wie verwende ich die Zielgruppenliste?
feature: Zielgruppen
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: f7d73de376c2345b628e3ebadb1d4ab4dc598693
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 34%

---

# Erstellen von Zielgruppen

Zielgruppen in [!DNL Adobe Target] bestimmen, wer Inhalte und Erlebnisse in einer zielgerichteten Aktivität sieht.

Zielgruppen werden überall dort eingesetzt, wo Targeting zur Verfügung steht. Für die Zielgruppenbestimmung einer Aktivität stehen folgende Optionen zur Verfügung:

* Wählen Sie eine wiederverwendbare Zielgruppe aus der Liste [!UICONTROL Zielgruppen] aus.
* [Aktivitätsspezifische ](/help/c-target/creating-activity-only-audience.md) Zielgruppen erstellen und ansprechen
* [Kombinieren mehrerer ](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) Zielgruppen zur Erstellung einer Ad-hoc-Zielgruppe

Sie können auch Zielgruppendaten verwenden, die von [!DNL Adobe Analytics] für Echtzeit-Targeting und Personalisierung in [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Anwendungen erfasst wurden. Siehe [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) im Handbuch *Experience Cloud Central Interface Components* .

Es gibt zwei Arten von Zielgruppen in [!DNL Target]:

* **Targeting-Zielgruppen:** Dient zur Bereitstellung unterschiedlicher Inhalte für verschiedene Besuchertypen.
* **Berichtszielgruppen:** Wird verwendet, um zu bestimmen, wie verschiedene Besuchertypen auf denselben Inhalt reagieren, damit Sie Ihre Testergebnisse analysieren können.

   In [!DNL Target] können Sie Berichtszielgruppen nur dann konfigurieren, wenn Sie [!DNL Target] als Berichtsquelle verwenden. Wenn Sie [ Adobe Analytics als Berichtsquelle](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, müssen Sie Ihre Berichterstellungszielgruppen in [!DNL Analytics] konfigurieren.

## Verwenden Sie die Liste [!UICONTROL Zielgruppen] .

Wenn Sie auf die Liste [!UICONTROL Zielgruppen] zugreifen möchten, klicken Sie in der oberen Menüzeile auf **[!UICONTROL Zielgruppen]**:

![Zielgruppenliste](assets/audiences_list.png)

Die Liste [!UICONTROL Zielgruppen] enthält die Zielgruppen, die Sie in Ihren Aktivitäten verwenden können. Verwenden Sie die Liste [!UICONTROL Zielgruppen] , um Zielgruppen zu erstellen, zu bearbeiten, zu duplizieren, zu kopieren oder zu kombinieren. In der Liste wird zudem aufgeführt, in welcher Quelle die Zielgruppe erstellt wurde:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >Die Quelle [!DNL Adobe Experience Platform] befindet sich in einem Beta-Testprogramm, steht jedoch allen [!DNL Target]-Kunden zur Verfügung, die das [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) verwenden. In [!DNL Adobe Experience Platform] verfügbare Zielgruppen können unverändert oder [in Kombination mit vorhandenen Zielgruppen](/help/c-target/combining-multiple-audiences.md) verwendet werden.

Vordefinierte Zielgruppen wie &quot;[!UICONTROL Neue Besucher]&quot;und &quot;[!UICONTROL Wiederkehrende Besucher]&quot;können nicht umbenannt werden.

Beim Arbeiten mit Zielgruppen, die ursprünglich in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] erstellt wurden, werden Sie von [!DNL Target] benachrichtigt, wenn Sie auf eine Zielgruppe in [!DNL Target] -Aktivitäten verweisen, die später in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] gelöscht wurden.

* Wenn eine Zielgruppe in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] gelöscht wurde, wird sowohl in der Liste [!UICONTROL Zielgruppe] ein Warnsymbol angezeigt als auch die Zielgruppenauswahl. Eine QuickInfo in der Benutzeroberfläche [!DNL Target] zeigt auch an, dass die Zielgruppe in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform] gelöscht wurde.
* Wenn Sie versuchen, mehrere Zielgruppen mit einer gelöschten Zielgruppe zu kombinieren oder eine Aktivität zu speichern, die auf eine gelöschte Zielgruppe verweist, wird eine Warnmeldung angezeigt.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Erstellen einer Zielgruppe die Attribute, die Sie für das Targeting Ihrer Aktivität verwenden möchten, in das Audience Builder-Fenster. Wenn das gewünschte Attribut nicht angezeigt wird, wurde das Attribut nicht von einer Mbox ausgelöst. In der Dropdownliste [!UICONTROL Benutzerdefinierte Parameter] sind weitere benutzerdefinierte Mbox-Parameter verfügbar.

Verwenden Sie die Schaltfläche [!UICONTROL Filter] , um die Liste [!UICONTROL Zielgruppen] nach Quelle zu filtern: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud] und [!DNL Adobe Experience Platform].

![Filteroption in der   Zielgruppenliste](assets/filters.png)

Verwenden Sie das Feld [!UICONTROL Zielgruppen suchen] , um die Liste [!UICONTROL Zielgruppen] zu durchsuchen. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Zielgruppenliste] nach Zielgruppennamen oder dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Anzeigen von Zielgruppendefinitionen {#section_11B9C4A777E14D36BA1E925021945780}

Sie können Details zur Zielgruppendefinition auf einer Pop-up-Karte an verschiedenen Stellen in der [!DNL Target] -Benutzeroberfläche anzeigen, ohne die Zielgruppe zu öffnen. Diese Funktion gilt für Zielgruppen, die in [!DNL Target Standard/Premium] erstellt wurden, sowie für Zielgruppen, die aus [!DNL Target Classic] importiert oder über API erstellt wurden.

Beispielsweise wird auf die folgende Zielgruppendefinitionskarte zugegriffen, indem Sie für die gewünschte Zielgruppe auf das Symbol [!UICONTROL Details anzeigen] klicken:

![Aktivitäten > Zielgruppendefinition](assets/audience_definition_list.png)

Auf die folgende Zielgruppendefinitionskarte kann durch Klicken auf das Symbol [!UICONTROL Details anzeigen] auf der Seite [!UICONTROL Übersicht] einer Aktivität zugegriffen werden:

![Aktivitäten > Zielgruppendefinition](assets/view-details-activity-overview.png)

Auf der Karte zur Zielgruppendefinition werden Typ, Quelle und Attribute der Zielgruppe angezeigt. Klicken Sie auf **[!UICONTROL Vollständige Details anzeigen]** , um weitere Aktivitäten anzuzeigen, die auf diese Zielgruppe verweisen (falls zutreffend). Wenn Sie eine Zielgruppendefinitionskarte auf der Seite [!UICONTROL Übersicht] einer Aktivität anzeigen, klicken Sie auf **[!UICONTROL Zielgruppennutzung]**.

Mithilfe der Informationen zur Zielgruppennutzung können Sie beim Bearbeiten von Zielgruppen unbeabsichtigte Auswirkungen auf andere Aktivitäten vermeiden. Zu den Informationen gehören [!UICONTROL Live-Aktivitäten], [!UICONTROL Inaktive Aktivitäten], [!UICONTROL Archivierte Aktivitäten] und [!UICONTROL Synchronisierungsaktivitäten]. Diese Funktion ist für alle Zielgruppen (Bibliothekszielgruppen und  [Zielgruppen vom Typ „Nur Aktivität“](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)) verfügbar.

Wenn eine Zielgruppe [mit einer anderen Zielgruppe](/help/c-target/combining-multiple-audiences.md) kombiniert ist und die kombinierte Zielgruppe zum Erstellen einer Aktivität verwendet wird, werden in den Nutzungsinformationen für beide Zielgruppen die neu erstellte Aktivität aufgelistet.

![](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## Schulungsvideo: Verwenden von Zielgruppen ![Tutorial-Badge](/help/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/17398)
