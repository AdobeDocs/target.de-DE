---
description: Informationen zum Verwenden von Unternehmenskundendaten aus einer Customer Relationship Management-Datenbank für das Targeting von Inhalten in Adobe Target mithilfe von Kundenattributen im Adobe Core-Service „Profile und Zielgruppen“.
keywords: Kundendatensatzdienst; crs; crm; MboxdrittanbieterID; Kundenattribute; Targeting
seo-description: Informationen zum Verwenden von Unternehmenskundendaten aus einer Customer Relationship Management-Datenbank für das Targeting von Inhalten in Adobe Target mithilfe von Kundenattributen im Adobe Core-Service „Profile und Zielgruppen“.
seo-title: Kundenattribute in Adobe Target
solution: Target
subtopic: Erste Schritte
title: Kundenattribute
topic: Standard
uuid: fc3c9a02-30d7-43df-838d-10ce1aa17f16
translation-type: tm+mt
source-git-commit: 8ec84183de4c5a7c2a7a1f30e0196cd021ce937f

---


# Kundenattribute {#customer-attributes}

Information about using enterprise customer data from a customer relationship management (CRM) databases for content targeting in [!DNL Adobe Target] by using customer attributes in the [!DNL Adobe Enterprise Cloud] core service.

Über mehrere Quellen gesammelte und in einer CRM-Datenbank gespeicherte Unternehmenskundendaten können in [!DNL Target] verwendet werden, um die relevantesten Inhalte strategisch für Kunden bereitzustellen, insbesondere mit dem Schwerpunkt auf Bestandskunden. Im Core-Service [!DNL Audiences] (früher „Profile und Zielgruppen“) kommen zu Erfassung und Analyse von Daten Tests und Optimierung hinzu, um die Umsetzbarkeit von Daten und Insights zu gewährleisten.

## Customer attributes overview {#section_B4099971FA4B48598294C56EAE86B45A}

The Audiences core service is part of the [!DNL Adobe Experience Cloud] and provides enterprises a tool to push their customer data to the [!DNL Experience Cloud] platform. In [!DNL Experience Cloud] integrierte Daten sind für alle [!DNL Experience Cloud]-Workflows verfügbar. [!DNL Target] verwendet diese Daten für das Targeting rückkehrender Kunden basierend auf Attributen. [!DNL Adobe Analytics] verwendet diese Attribute, und sie können für die Analyse und Segmentierung herangezogen werden.

![](assets/crs.png)

Consider the following information as your work with customer attributes and [!DNL Target]:

* There are some prerequisite requirements that you must meet before you can use the [!UICONTROL Customer attributes] feature in the [!DNL Audiences] core service. For more information, see "Prerequisites for uploading Customer Attributes" in [Customer attributes](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html) in the *Experience Cloud Product documentation*.

   >[!NOTE]
   >
   >[!DNL at.js] (beliebige Version) oder [!DNL mbox.js] Version 58 oder höher erforderlich.

* Adobe does not guarantee that 100% of customer attribute (visitor profile) data from CRM databases will be onboarded to the [!DNL Experience Cloud] and, thus, be available for use for targeting in [!DNL Target]. In unserem aktuellen Design besteht die Möglichkeit, dass ein geringer Prozentsatz der Daten nicht integriert wird.
* The lifetime of customer attributes data imported from the [!DNL Experience Cloud] to [!DNL Target] depends on the lifetime of the visitor profile, which is 14 days by default. Weitere Informationen finden Sie unter  [Lebensdauer des Besucherprofils](../../c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* If the `vst.*` parameters are the only thing identifying the visitor, the existing "authenticated" profile will not be fetched as long as `authState` is UNAUTHENTICATED (0). Das Profil kommt nur ins Spiel, wenn `authState` in UNAUTHENTICATED (1) geändert wird.

   For example, if the `vst.myDataSource.id` parameter is used to identify the visitor (where `myDataSource` is the data source alias) and there is no MCID or third-party ID, using the parameter `vst.myDataSource.authState=0` won't fetch the profile that might have been created through a Customer Attributes import. Wenn das gewünschte Verhalten darin bestehen soll, das authentifizierte Profil aufzurufen, muss `vst.myDataSource.authState` den Wert 1 (AUTHENTICATED) haben.

* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

## Customer attribute workflow for Target {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Führen Sie die folgenden Schritte aus, um CRM-Daten in [!DNL Target] zu verwenden, wie unten dargestellt:

![](assets/crm_workflow.png)

Detailed instructions for completing each of the following tasks can be found in [Create a customer attribute source and upload the data file](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html) in the *Experience Cloud Product Documentation*.

1. Erstellen einer Datendatei.

   Exportieren Sie die Kundendaten aus Ihrem CRM-System in das CSV-Format, um eine .csv-Datei zu erstellen. Alternativ kann eine ZIP- oder GZIP-Datei für den Upload erstellt werden. Stellen Sie sicher, dass die erste Zeile der CSV-Datei die Kopfzeile und alle Zeilen (Kundendaten) die gleiche Anzahl von Einträgen aufweisen.

   ![](assets/CRS_sample.png)

   ![](assets/CRS_CSV_sample.png)

1. Erstellen der Attributquelle und Hochladen der Datendatei.

   Geben Sie einen Namen und eine Beschreibung der Datenquelle und die Alias-ID an. The alias Id is a unique ID to be used in your Customer Attribute code in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >Der Name der Datenquelle und der Attributname dürfen keinen Punkt enthalten.

   Mithilfe der HTTP-Methode können Datendateien mit einer Größe von bis zu 100 MB hochgeladen werden. Dateien mit einer Größe von mehr als 100 MB bis zu 4 GB können über FTP hochgeladen werden.

   * **HTTPS:** You can drag-and-drop the .csv data file or click **[!UICONTROL Browse]** to upload from your file system.
   * **FTP:** Click the FTP link to [upload the file through FTP](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Der erste Schritt besteht darin, ein Kennwort für den von Adobe bereitgestellten FTP-Server anzugeben. Specify the password, then click **[!UICONTROL Done]**.

      Übertragen Sie nun Ihre CSV-/ZIP-/GZIP-Datei auf den FTP-Server. Nachdem die Dateiübertragung erfolgreich war, erstellen Sie eine neue Datei mit demselben Namen und der Erweiterung .fin. Übertragen Sie diese leere Datei auf den Server. This indicates a End Of Transfer and the [!DNL Experience Cloud] starts to process the data file.

1. Prüfen des Schemas.

   Der Prüfungsprozess ermöglicht die Zuordnung von Anzeigenamen und Beschreibungen zu den hochgeladenen Attributen (Zeichenfolgen, Ganzzahlen, Zahlen usw.). Ordnen Sie die einzelnen Attribute dem jeweils korrekten Datentyp und Anzeigenamen und der korrekten Beschreibung zu.

   Click **[!UICONTROL Save]** after the schema validation is complete. Die Zeit für den Datei-Upload variiert je nach Größe.

   ![](assets/SchemaValidate.png)

   ![](assets/upload1.png)

1. Konfigurieren von Abonnements und Aktivieren der Attributquelle.

   Klicken Sie auf **[!UICONTROL Abonnement hinzufügen]** und wählen Sie die Lösung zum Abonnieren dieser Attribute aus. [Durch die Konfiguration von Abonnements](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/subscription.html) wird der Datenfluss zwischen der [!DNL Experience Cloud] und den Lösungen eingerichtet. Durch die Aktivierung der Attributquelle können die Daten an die abonnierten Lösungen übertragen werden. Die von Ihnen hochgeladenen Kundendatensätze werden mit den von Ihrer Website oder Anwendung eingehenden ID-Signalen abgeglichen.

   ![](assets/solution.png)

   ![](assets/activate.PNG)

   Beachten Sie beim Ausführen dieses Schritts die folgenden Einschränkungen:

   * Die maximale Dateigröße pro Upload mithilfe der HTTP-Methode beträgt 100 MB.
   * Die maximale Dateigröße pro Upload mithilfe der FTP-Methode beträgt 4 GB.
   * Die Anzahl der zum Abonnieren zulässigen Attribute: 5 für [!DNL Target Standard] und 200 für [!DNL Target Premium].

## Verwenden von Kundenattributen in Target {#section_107E3A0F0EC7478E82E6DBD17B30B756}

Sie können Kundenattribute in [!DNL Target] wie folgt verwenden:

### Erstellen von Targeting-Zielgruppen

In [!DNL Target] können Sie beim Erstellen einer Zielgruppe im Bereich Besucherprofil ein Kundenattribut auswählen.  Alle Kundenattribute haben das Präfix &lt; data_source_name &gt; in der Liste. Sie können die Attribute beim Aufbau von Zielgruppen beliebig mit anderen Datenattributen kombinieren.

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

Beim Arbeiten mit Kundenattributen und [!DNL Target] stoßen Sie möglicherweise auf die folgenden Probleme:

| Fehler | Details |
|--- |--- |
| Kundenattribute werden entfernt, weil das Profil zu groß ist | Es gibt zwar keine Zeichenbeschränkung für ein bestimmtes Feld im Profil des Benutzers, wenn das Profil jedoch umfangreicher als 64 K ist, wird es durch Entfernen der ältesten Attribute so lange abgeschnitten, bis das Profil wieder kleiner als 64 K ist. |
| Attribute werden nicht in der Zielgruppenbibliothek in [!DNL Target] aufgelistet, selbst nach mehreren Tagen nicht | Dies ist normalerweise ein Pipeline-Verbindungsproblem. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen. |
| Auf dem Attribut basierende Bereitstellung funktioniert nicht | Das Profil wurde in Edge noch nicht aktualisiert. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen. |
| Implementierungsprobleme | Beachten Sie die folgenden Implementierungsprobleme:<ul><li>Die Besucher-ID wurde nicht korrekt übergeben. The ID was passed in `mboxMCGVID` instead of `setCustomerId`.</li><li>Die Besucher-ID wurde korrekt übergeben, aber der Status der AUTHENTIFIZIERUNG wurde nicht auf „Authentifiziert“ festgelegt.</li><li>`mbox3rdPartyId` wurde nicht korrekt weitergeleitet.</li> |
| `mboxUpdate` wurde nicht ordnungsgemäß durchgeführt | `mboxUpdate` wurde nicht ordnungsgemäß mit `mbox3rdPartyId` ausgeführt. |
| Kundenattribute werden nicht in Target importiert | If you cannot find Customer Attributes data in Target, ensure that the import occurred within the last *x* days where *x* is the Target [Visitor Profile Lifetime](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) value (14 days by default). |

Probleme in den Zeilen 1 und 2 oben verursachen ca. 60 % der Probleme in diesem Bereich. Probleme in Zeile 3 verursachen ca. 30 % der Probleme. Das Problem in Zeile 4 ist die Ursache für ca. 5 % der Probleme. Die restlichen 5 % werden durch verschiedene andere Ursachen hervorgerufen.

## Schulungsvideo: Hochladen von Offline-Daten mithilfe von Kundenattributen {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

Dieses Video zeigt, wie Sie Offline-CRM-, Helpdesk-, Point-of-Sale- und andere Marketingdaten in den People-Service der Experience Cloud importieren und sie Besuchern anhand ihrer IDs zuordnen können.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/?captions=ger)
