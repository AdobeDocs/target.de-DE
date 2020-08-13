---
keywords: customer relationship management;customer record service;crs;crm;mbox3rdpartyid;customer attributes;targeting;csv;crm;adobe experience cloud people
description: Informationen zum Verwenden von Unternehmenskundendaten aus einer CRM-Datenbank für das Targeting von Inhalten in Adobe Target mithilfe von Kundenattributen im Adobe Experience Cloud People-Core-Service.
title: Kundenattribute in Adobe Target
feature: visitor profiles
subtopic: Getting Started
topic: Standard
uuid: fc3c9a02-30d7-43df-838d-10ce1aa17f16
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 39%

---


# Kundenattribute {#customer-attributes}

Information about using enterprise customer data from Customer Relationship Management (CRM) databases for content targeting in [!DNL Adobe Target] by using customer attributes in the [!DNL Adobe Enterprise Cloud People] core service.

Enterprise customer data collected through multiple sources and stored inside CRM databases can be used in [!DNL Target] to strategically deliver the most relevant content to customers, specifically focusing on returning customers. Audiences and customer attributes in the [!DNL People] core service (formerly Profiles and Audiences) brings together data collection and analysis with testing and optimization, making data and insights actionable.

## Customer attributes overview {#section_B4099971FA4B48598294C56EAE86B45A}

[Customer Attributes](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) in the [!DNL People] core service is part of the [!DNL Adobe Experience Cloud] and provides enterprises a tool to push their customer data to the [!DNL Experience Cloud] platform.

In [!DNL Experience Cloud] integrierte Daten sind für alle [!DNL Experience Cloud]-Workflows verfügbar. [!DNL Target] verwendet diese Daten für das Targeting rückkehrender Kunden basierend auf Attributen. [!DNL Adobe Analytics] verwendet diese Attribute, und sie können für die Analyse und Segmentierung herangezogen werden.

![crs-Beispiel](/help/c-target/c-visitor-profile/assets/crs.png)

Consider the following information as your work with customer attributes and [!DNL Target]:

* There are some prerequisite requirements that you must meet before you can use the [!UICONTROL Customer attributes] feature in the [!DNL People] core service. For more information, see &quot;Prerequisites for uploading Customer Attributes&quot; in [Customer attributes](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in the *Experience Cloud and Core Services Product documentation*.

   >[!NOTE]
   >
   >[!DNL at.js] (any version) or [!DNL mbox.js] version 58 or later is required.

* [!DNL Adobe] garantiert nicht, dass 100 % der Kundenattributdaten (Besucher-Profil) aus CRM-Datenbanken an die Daten des Unternehmens gesendet werden [!DNL Experience Cloud] und somit für das Targeting in [!DNL Target]der Datenbank zur Verfügung stehen. In unserem aktuellen Design besteht die Möglichkeit, dass ein kleiner Anteil der Daten (bis zu 0,1 % der großen Produktionschargen) möglicherweise nicht an Bord mitgeführt wird.
* The lifetime of customer attributes data imported from the [!DNL Experience Cloud] to [!DNL Target] depends on the lifetime of the visitor profile, which is 14 days by default. Weitere Informationen finden Sie unter  [Lebensdauer des Besucherprofils](../../c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* If the `vst.*` parameters are the only thing identifying the visitor, the existing &quot;authenticated&quot; profile will not be fetched as long as `authState` is UNAUTHENTICATED (0). The profile will come into play only if `authState` is changed to AUTHENTICATED (1).

   For example, if the `vst.myDataSource.id` parameter is used to identify the visitor (where `myDataSource` is the data source alias) and there is no MCID or third-party ID, using the parameter `vst.myDataSource.authState=0` won&#39;t fetch the profile that might have been created through a Customer Attributes import. If the desired behavior is to fetch the authenticated profile, the `vst.myDataSource.authState` must have the value of 1 (AUTHENTICATED).

* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

## Zugriff auf Kundenattribute im Hauptdienst &quot;Personen&quot;

1. Klicken Sie im [!DNL Adobe Experience Cloud]Menü auf das Symbol ( ![Menüsymbol](/help/c-target/c-visitor-profile/assets/menu-icon.png) ) und dann auf **[!UICONTROL Personen]**.

   ![Personen](/help/c-target/c-visitor-profile/assets/people.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Kundenattribute]** .

   ![Registerkarte &quot;Kundenattribute&quot;](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Customer attribute workflow for Target {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Führen Sie die folgenden Schritte aus, um CRM-Daten in [!DNL Target] zu verwenden, wie unten dargestellt:

![crm-Arbeitsablauf](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Detailed instructions for completing each of the following tasks can be found in [Create a customer attribute source and upload the data file](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html) in the *Experience Cloud and Core Services Product Documentation*.

1. Erstellen einer Datendatei.

   Exportieren Sie die Kundendaten aus Ihrem CRM-System in das CSV-Format, um eine .csv-Datei zu erstellen. Alternativ kann eine ZIP- oder GZIP-Datei für den Upload erstellt werden. Stellen Sie sicher, dass die erste Zeile der CSV-Datei die Kopfzeile und alle Zeilen (Kundendaten) die gleiche Anzahl von Einträgen aufweisen.

   Die folgende Abbildung zeigt eine Beispieldatendatei für Unternehmenskunden:

   ![crs-Beispiel](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   Die folgende Abbildung zeigt eine Beispiel für eine CSV-Datei für Unternehmenskunden:

   ![CSV-Beispiel](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Erstellen der Attributquelle und Hochladen der Datendatei.

   Geben Sie einen Namen und eine Beschreibung der Datenquelle und die Alias-ID an. The alias Id is a unique ID to be used in your Customer Attribute code in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >Der Name der Datenquelle und der Attributname dürfen keinen Punkt enthalten.

   Ihre Datendatei muss den Anforderungen für das Hochladen der Datei entsprechen und darf 100 MB nicht überschreiten. Wenn Ihre Datei zu groß ist oder Sie Daten haben, die regelmäßig hochgeladen werden müssen, können Sie stattdessen eine FTP-Verbindung mit Ihren Dateien herstellen.

   * **HTTPS:** Sie können die .csv-Datendatei per Drag &amp; Drop verschieben oder auf **[!UICONTROL Durchsuchen]** klicken, um sie aus Ihrem Dateisystem hochzuladen.
   * **FTP:** Klicken Sie auf den FTP-Link, um die Datei über FTP [hochzuladen](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Der erste Schritt besteht darin, ein Kennwort für den von Adobe bereitgestellten FTP-Server anzugeben. Specify the password, then click **[!UICONTROL Done]**.

   Übertragen Sie nun Ihre CSV-/ZIP-/GZIP-Datei auf den FTP-Server. Nachdem die Dateiübertragung erfolgreich war, erstellen Sie eine neue Datei mit demselben Namen und der Erweiterung .fin. Übertragen Sie diese leere Datei auf den Server. This indicates a End Of Transfer and the [!DNL Experience Cloud] starts to process the data file.

1. Prüfen des Schemas.

   Der Prüfungsprozess ermöglicht die Zuordnung von Anzeigenamen und Beschreibungen zu den hochgeladenen Attributen (Zeichenfolgen, Ganzzahlen, Zahlen usw.). Ordnen Sie die einzelnen Attribute dem jeweils korrekten Datentyp und Anzeigenamen und der korrekten Beschreibung zu.

   Click **[!UICONTROL Save]** after the schema validation is complete. Die Zeit für den Datei-Upload variiert je nach Größe.

   ![Schema überprüfen](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema hochladen](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Konfigurieren von Abonnements und Aktivieren der Attributquelle.

   Klicken Sie auf **[!UICONTROL Abonnement hinzufügen]** und wählen Sie die Lösung zum Abonnieren dieser Attribute aus. [Abonnement](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/subscription.html) konfigurieren richtet den Datenfluss zwischen der [!DNL Experience Cloud] und den Lösungen ein. Durch die Aktivierung der Attributquelle können die Daten an die abonnierten Lösungen übertragen werden. Die von Ihnen hochgeladenen Kundendatensätze werden mit den von Ihrer Website oder Anwendung eingehenden ID-Signalen abgeglichen.

   ![Lösung konfigurieren](/help/c-target/c-visitor-profile/assets/solution.png)

   ![Aktivieren](/help/c-target/c-visitor-profile/assets/activate.png)

   Beachten Sie beim Ausführen dieses Schritts die folgenden Einschränkungen:

   * Die maximale Dateigröße pro Upload mithilfe der HTTP-Methode beträgt 100 MB.
   * Die maximale Dateigröße pro Upload mithilfe der FTP-Methode beträgt 4 GB.
   * Die Anzahl der zum Abonnieren zulässigen Attribute: 5 für [!DNL Target Standard] und 200 für [!DNL Target Premium].

## Verwenden von Kundenattributen in Target {#section_107E3A0F0EC7478E82E6DBD17B30B756}

Sie können Kundenattribute in [!DNL Target] wie folgt verwenden:

### Erstellen von Targeting-Zielgruppen

In [!DNL Target] können Sie beim Erstellen einer Zielgruppe im Bereich Besucherprofil ein Kundenattribut auswählen.  Alle Kundenattribute haben das Präfix &lt; data_source_name > in der Liste. Sie können die Attribute beim Aufbau von Zielgruppen beliebig mit anderen Datenattributen kombinieren.

![Zielgruppe](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### Erstellen von Profilskripten mithilfe von Token

Kundenattribute können in Profilskripten mithilfe des Formats `crs.get('<Datasource Name>.<Attribute name>')` referenziert werden.

Dieses Profilskript kann direkt in Angeboten verwendet werden, um Attribute bereitzustellen, die zum aktuellen Besucher gehören.

### Verwenden von mbox3rdPartyID auf Ihrer Website für eine erfolgreiche Implementierung und Verwendung

Pass `mbox3rdPartyId` as a parameter to the global mbox inside the `targetPageParams()` method. The value of `mbox3rdPartyId` should be set to the customer ID that was present in the CSV data file.

```
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Verwenden des Experience Cloud ID-Service

Wenn Sie den Experience Cloud ID-Service verwenden, müssen Sie eine Kunden-ID und einen Authentifizierungsstatus festlegen, um Kundenattribute im Targeting zu verwenden. For more information, see [Customer IDs and Authentication State](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) in the *Experience Cloud Identity Service Help*.

Weitere Informationen zum Verwenden von Kundenattributen in [!DNL Target] finden Sie unter den folgenden Ressourcen:

* [Erstellen Sie eine Kundenattributquelle und laden Sie die Datendatei](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html) in der *Experience Cloud-Produktdokumentation hoch.*
* [Kundenattribute: Je mehr Details, desto besser die Verbindung](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) im *Digital Marketing-Blog*

## Issues frequently encountered by customers {#section_BE0F70E563F64294B17087DE2BC1E74C}

You might encounter the following issues when working with customer attributes and [!DNL Target].

>[!NOTE]
>
>Issues 1 and 2 cause approximately 60% of problems in this area. Problem 3 verursacht ca. 30 % der Probleme. Problem 4 verursacht ungefähr 5 % der Probleme. Die restlichen 5 % werden durch verschiedene andere Ursachen hervorgerufen.

### Problem 1: Kundenattribute werden entfernt, da das Profil zu groß ist

Es gibt zwar keine Zeichenbeschränkung für ein bestimmtes Feld im Profil des Benutzers, wenn das Profil jedoch umfangreicher als 64 K ist, wird es durch Entfernen der ältesten Attribute so lange abgeschnitten, bis das Profil wieder kleiner als 64 K ist.

### Issue 2: Attributes not listing in the Audience Library in [!DNL Target], even after several days

Dies ist normalerweise ein Pipeline-Verbindungsproblem. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 3: Versand funktioniert nicht auf Grundlage des Attributs

Das Profil wurde in Edge noch nicht aktualisiert. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 4: Implementierungsfragen

Beachten Sie die folgenden Implementierungsprobleme:

* Die Besucher-ID wurde nicht korrekt übergeben. The ID was passed in `mboxMCGVID` instead of `setCustomerId`.
* Die Besucher-ID wurde korrekt übergeben, aber der Status der AUTHENTIFIZIERUNG wurde nicht auf „Authentifiziert“ festgelegt.
* `mbox3rdPartyId` wurde nicht korrekt weitergeleitet.

### Issue 5: `mboxUpdate` not performed properly

`mboxUpdate` wurde nicht ordnungsgemäß mit `mbox3rdPartyId` ausgeführt.

### Issue 6: Customer attributes are not being imported into [!DNL Target]

If you cannot find Customer Attributes data in Target, ensure that the import occurred within the last *x* days where *x* is the Target [Visitor Profile Lifetime](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) value (14 days by default).

## Training video: Upload Offline Data using Customer Attributes {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8} ![Tutorial badge](/help/assets/tutorial.png)

This video shows you how to import offline CRM, help desk, point-of-sale, and other marketing data into the [!DNL Experience Cloud People] service and associate it with visitors using their known IDs.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
