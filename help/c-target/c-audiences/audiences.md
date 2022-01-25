---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; Zielgruppentargeting; Zielgruppenberichterstellung; Zielgruppenbericht; Segment; benutzerdefinierte Profilparameter; Zielgruppendefinition; Zielgruppenliste
description: Erfahren Sie, wie Sie Zielgruppen in [!DNL Adobe Target].
title: Wie verwende ich die Zielgruppenliste?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: 91bfeb8896fd3ddc7d198481db317bde04b05f79
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 33%

---

# Erstellen von Zielgruppen

Zielgruppen in [!DNL Adobe Target] bestimmen, wer Inhalte und Erlebnisse in einer zielgerichteten Aktivität sieht.

Zielgruppen werden überall dort eingesetzt, wo Targeting zur Verfügung steht. Für die Zielgruppenbestimmung einer Aktivität stehen folgende Optionen zur Verfügung:

* Wählen Sie eine wiederverwendbare Zielgruppe aus dem [!UICONTROL Zielgruppen] Liste
* [Aktivitätsspezifische Zielgruppe erstellen](/help/c-target/creating-activity-only-audience.md) und Zielgruppe
* [Kombinieren mehrerer Zielgruppen](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) Erstellen einer Ad-hoc-Zielgruppe

Sie können auch Zielgruppendaten verwenden, die von [!DNL Adobe Analytics] für Echtzeit-Targeting und Personalisierung in [!DNL Target] und andere [!DNL Adobe Experience Cloud] Anwendungen. Siehe [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) im *Zentrale Experience Cloud-Schnittstellenkomponenten* Handbuch.

Es gibt zwei Arten von Zielgruppen in [!DNL Target]:

* **Zielgruppen auswählen:** Dient zur Bereitstellung unterschiedlicher Inhalte für verschiedene Besuchertypen.
* **Berichtszielgruppen:** Wird verwendet, um zu bestimmen, wie verschiedene Besuchertypen auf denselben Inhalt reagieren, damit Sie Ihre Testergebnisse analysieren können.

   In [!DNL Target] können Sie Berichtszielgruppen nur dann konfigurieren, wenn Sie [!DNL Target] als Berichtsquelle verwenden. Wenn Sie [ Adobe Analytics als Berichtsquelle](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, müssen Sie Ihre Berichterstellungszielgruppen in [!DNL Analytics] konfigurieren.

## Verwenden Sie die [!UICONTROL Zielgruppen] Liste {#use-list}

Wenn Sie auf die Liste [!UICONTROL Zielgruppen] zugreifen möchten, klicken Sie in der oberen Menüzeile auf **[!UICONTROL Zielgruppen]**:

![Zielgruppenliste](assets/audiences_list.png)

Die [!UICONTROL Zielgruppen] enthält die Zielgruppen, die Sie in Ihren Aktivitäten verwenden können. Verwenden Sie die [!UICONTROL Zielgruppen] Liste zum Erstellen, Bearbeiten, Duplizieren, Kopieren oder Kombinieren von Zielgruppen. In der Liste wird zudem aufgeführt, in welcher Quelle die Zielgruppe erstellt wurde:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >Die [!DNL Adobe Experience Platform] -Quelle für alle [!DNL Target] -Kunden, die [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md). In der [!DNL Adobe Experience Platform] kann wie besehen oder verwendet werden [in Kombination mit vorhandenen Zielgruppen](/help/c-target/combining-multiple-audiences.md).
   >
   >Benutzer müssen [!UICONTROL Genehmiger] oder über dem Status in [!DNL Target] zum Konfigurieren [!DNL Target] [!UICONTROL Ziele] Karten in AEP/RTCDP ([!DNL Real-Time Customer Data Platform]).

Vordefinierte Zielgruppen, z. B.[!UICONTROL Neue Besucher]&quot; und &quot;[!UICONTROL Wiederkehrende Besucher],&quot; kann nicht umbenannt werden.

Beim Arbeiten mit Zielgruppen, die ursprünglich in erstellt wurden [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform], [!DNL Target] Warnungen, wenn Sie auf eine Zielgruppe in [!DNL Target] Aktivitäten, die später in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform].

* Wenn eine Zielgruppe in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform], ein Warnsymbol in beiden [!UICONTROL Zielgruppe] und die Zielgruppenauswahl angezeigt. Eine QuickInfo im [!DNL Target] Die Benutzeroberfläche zeigt auch an, dass die Zielgruppe in [!DNL Experience Cloud] oder [!DNL Adobe Experience Platform].
* Wenn Sie versuchen, mehrere Zielgruppen mit einer gelöschten Zielgruppe zu kombinieren oder eine Aktivität zu speichern, die auf eine gelöschte Zielgruppe verweist, wird eine Warnmeldung angezeigt.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Erstellen einer Zielgruppe die Attribute, die Sie für das Targeting Ihrer Aktivität verwenden möchten, in das Audience Builder-Fenster. Wenn das gewünschte Attribut nicht angezeigt wird, wurde das Attribut nicht von einer Mbox ausgelöst. In der Dropdownliste [!UICONTROL Benutzerdefinierte Parameter] sind weitere benutzerdefinierte Mbox-Parameter verfügbar.

Verwenden Sie die [!UICONTROL Filter] Schaltfläche zum Filtern der [!UICONTROL Zielgruppen] Liste nach Quelle: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud]und [!DNL Adobe Experience Platform].

![Filteroption im [!UICONTROL Zielgruppen] Liste](assets/filters.png)

Verwenden Sie die [!UICONTROL Zielgruppen durchsuchen] zum Durchsuchen Ihres [!UICONTROL Zielgruppen] Liste. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Zielgruppenliste] nach Zielgruppennamen oder dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Anzeigen von Zielgruppendefinitionen {#section_11B9C4A777E14D36BA1E925021945780}

Sie können Details zur Zielgruppendefinition auf einer Pop-up-Karte an verschiedenen Stellen in der [!DNL Target] Benutzeroberfläche, ohne die Zielgruppe zu öffnen. Diese Funktion gilt für Zielgruppen, die in [!DNL Target Standard/Premium] und aus importierten Zielgruppen [!DNL Target Classic] oder über API erstellt wurde.

Beispielsweise kann auf die folgende Zielgruppendefinitionskarte zugegriffen werden, indem Sie auf die [!UICONTROL Details anzeigen] für die gewünschte Zielgruppe:

![Aktivitäten > Zielgruppendefinition](assets/audience_definition_list.png)

Auf die folgende Zielgruppendefinitionskarte können Sie durch Klicken auf die [!UICONTROL Details anzeigen] Symbol auf der Seite [!UICONTROL Übersicht] Seite:

![Aktivitäten > Zielgruppendefinition](assets/view-details-activity-overview.png)

Auf der Karte zur Zielgruppendefinition werden Typ, Quelle und Attribute der Zielgruppe angezeigt. Klicken **[!UICONTROL Vollständige Details anzeigen]** , um gegebenenfalls andere Aktivitäten anzuzeigen, die auf diese Zielgruppe verweisen. Wenn Sie eine Zielgruppendefinitionskarte aus einer Aktivität anzeigen [!UICONTROL Übersicht] Seite, klicken Sie auf **[!UICONTROL Zielgruppennutzung]**.

Mithilfe der Informationen zur Zielgruppennutzung können Sie beim Bearbeiten von Zielgruppen unbeabsichtigte Auswirkungen auf andere Aktivitäten vermeiden. Informationen enthalten [!UICONTROL Live-Aktivitäten], [!UICONTROL Inaktive Aktivitäten], [!UICONTROL Archivierte Aktivitäten]und [!UICONTROL Synchronisieren von Aktivitäten]. Diese Funktion ist für alle Zielgruppen (Bibliothekszielgruppen und  [Zielgruppen vom Typ „Nur Aktivität“](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)) verfügbar.

Wenn eine Zielgruppe [kombiniert mit einer anderen Zielgruppe](/help/c-target/combining-multiple-audiences.md) und die kombinierte Zielgruppe zum Erstellen einer Aktivität verwendet wird, werden in den Nutzungsinformationen für beide Zielgruppen die neu erstellte Aktivität aufgelistet.

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
