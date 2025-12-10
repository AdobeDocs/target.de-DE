---
keywords: Customer Relationship Management;Kundeneintragsdienst;crs;crm;mbox3rdPartyID;Kundenattribute;Targeting;CSV;crm;Adobe Experience Cloud People
description: Erfahren Sie, wie Sie Enterprise-Kundendaten aus einer CRM-Datenbank (Customer Relationship Management) für das Content-Targeting in  [!DNL Adobe Target] verwenden.
title: Was sind Kundenattribute und wie verwende ich sie?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: 0b17b61bb60162af6bc35246219355077ab6bf44
workflow-type: tm+mt
source-wordcount: '1502'
ht-degree: 29%

---

# Kundenattribute

Informationen zur Verwendung von Enterprise-Kundendaten aus CRM-Datenbanken (Customer Relationship Management) für das Content-Targeting in [!DNL Adobe Target] mithilfe von Kundenattributen im [!DNL Adobe Experience Cloud People]-Service.

Unternehmenskundendaten, die über mehrere Quellen erfasst und in CRM-Datenbanken gespeichert werden, können [!DNL Target] verwendet werden, um Kunden strategisch die relevantesten Inhalte bereitzustellen, wobei der Schwerpunkt auf wiederkehrenden Kunden liegt. Zielgruppen und Kundenattribute im [!DNL People]-Service (früher Profile und Zielgruppen) führen die Datenerfassung und -analyse mit Tests und Optimierung zusammen, sodass Daten und Erkenntnisse umsetzbar sind.

## Übersicht über Kundenattribute {#section_B4099971FA4B48598294C56EAE86B45A}

[Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html) im [!DNL People]-Service ist Teil der [!DNL Adobe Experience Cloud] und bietet Unternehmen ein Tool, mit dem sie ihre Kundendaten an die [!DNL Experience Cloud]-Plattform übertragen können.

In [!DNL Experience Cloud] integrierte Daten sind für alle [!DNL Experience Cloud]-Workflows verfügbar. [!DNL Target] verwendet diese Daten für die Zielgruppenbestimmung der wiederkehrenden Kundinnen und Kunden auf der Grundlage von Attributen. [!DNL Adobe Analytics] verwendet diese Attribute, und sie können für die Analyse und Segmentierung herangezogen werden.

![CRS-Beispiel](/help/main/c-target/c-visitor-profile/assets/crs.png)

Beachten Sie die folgenden Informationen bei der Arbeit mit Kundenattributen und -[!DNL Target]:

* Es gibt einige Voraussetzungen, die Sie erfüllen müssen, bevor Sie die [!UICONTROL Customer Attributes] im [!DNL People]-Service verwenden können. Weitere Informationen finden Sie unter „Voraussetzungen für das Hochladen von Kundenattributen“ in [Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) im *Handbuch für die Benutzeroberfläche und Administration* Experience Cloud.
* Beachten Sie die Einschränkungen beim Hochladen von Dateien, wie in [Datendateien und -quellen für Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=de) im Handbuch zur *Benutzeroberfläche und Administration von* in Experience Cloud dokumentiert. Als Best Practice gilt:

   * Laden Sie einzelne große Dateien hoch (innerhalb der [angegebenen &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=de)). Einzelne große Dateien werden gegenüber mehreren kleineren Dateien bevorzugt.
   * Wenn Sie den Upload in mehrere Dateien aufteilen müssen, stellen Sie sicher, dass die Dateien vollständig verarbeitet sind, bevor Sie neue Dateien senden. Stellen Sie sicher, dass jede Datei in einem Batch vollständig verarbeitet ist, bevor Sie die nächste Datei im Batch übermitteln.

* [!DNL Adobe] garantiert nicht, dass 100 % der Kundenattributdaten (Besucherprofil) aus CRM-Datenbanken in die [!DNL Experience Cloud] integriert werden und somit für die Targeting-Verwendung in [!DNL Target] verfügbar sind. Beim aktuellen Design besteht die Möglichkeit, dass ein kleiner Prozentsatz der Daten (bis zu 0,1 % bei großen Produktionschargen) nicht für das Targeting erfasst wird.
* Die Lebensdauer von Kundenattributdaten, die von [!DNL Experience Cloud] nach [!DNL Target] importiert werden, hängt von der Lebensdauer des Besucherprofils ab, die standardmäßig 14 Tage beträgt. Weitere Informationen finden Sie unter [Lebensdauer von Besucherprofilen](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Wenn die `vst.*` das einzige sind, das den Besucher identifiziert, wird das vorhandene „authentifizierte“ Profil nicht abgerufen, solange `authState` NICHT AUTHENTIFIZIERT ist (0). Das Profil kommt nur ins Spiel, wenn `authState` in AUTHENTICATED (1) geändert wird.

  Wenn beispielsweise der Parameter `vst.myDataSource.id` zur Identifizierung des Besuchers verwendet wird (wobei `myDataSource` der Datenquellenalias ist) und es keine MCID oder Drittanbieter-ID gibt, ruft der Parameter `vst.myDataSource.authState=0` das Profil nicht ab, das möglicherweise durch einen Kundenattribut-Import erstellt wurde. Wenn das gewünschte Verhalten darin besteht, das authentifizierte Profil abzurufen, muss der `vst.myDataSource.authState` den Wert 1 (AUTHENTICATED) haben.

* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

## Zugreifen auf Kundenattribute im Personen-Service

1. Klicken Sie in [!DNL Experience Cloud] auf das Menüsymbol ( ![Menüsymbol](/help/main/c-target/c-visitor-profile/assets/menu-icon.png) ) und dann auf **[!UICONTROL People]**.

   ![Personen](/help/main/c-target/c-visitor-profile/assets/people.png)

1. Klicken Sie auf **[!UICONTROL Customer Attributes]**.

   ![Registerkarte Kundenattribute](/help/main/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Arbeitsablauf für Kundenattribute für [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Führen Sie die folgenden Schritte aus, um CRM-Daten in [!DNL Target] zu verwenden, wie unten dargestellt:

![CRM-Workflow](/help/main/c-target/c-visitor-profile/assets/crm_workflow.png)

Experience Cloud Detaillierte Anweisungen zum Ausführen der folgenden Aufgaben finden Sie unter [Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html) im Handbuch zur *Benutzeroberfläche und Administration von*.

1. Erstellen Sie eine Datendatei

   Exportieren Sie Kundendaten aus Ihrem CRM in das CSV-Format, um eine CSV-Datei zu erstellen. Alternativ kann eine ZIP- oder GZIP-Datei für den Upload erstellt werden. Stellen Sie sicher, dass die erste Zeile der CSV-Datei die Kopfzeile ist und alle Zeilen (Kundendaten) die gleiche Anzahl von Einträgen aufweisen.

   Die folgende Abbildung zeigt eine Beispiel-Kundendatendatei für ein Unternehmen:

   ![CRS-Beispiel](/help/main/c-target/c-visitor-profile/assets/CRS_sample.png)

   Die folgende Abbildung zeigt ein Beispiel für eine CSV-Datei für Unternehmenskunden:

   ![CSV-Beispiel](/help/main/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Erstellen der Attributquelle und Hochladen der Datendatei.

   Geben Sie einen Namen und eine Beschreibung der Datenquelle und die Alias-ID an. Die Alias-ID ist eine eindeutige ID, die im Kundenattributcode in `VisitorAPI.js` verwendet werden soll.

   >[!IMPORTANT]
   >
   >Der Name der Datenquelle und der Attributname dürfen keinen Punkt enthalten.

   Ihre Datendatei muss den Anforderungen zum Hochladen von Dateien entsprechen und darf 100 MB nicht überschreiten. Wenn Ihre Datei zu groß ist oder Sie Daten haben, die regelmäßig hochgeladen werden müssen, können Sie stattdessen Ihre Dateien per FTP hochladen.

   * **HTTPS:** Sie können die CSV-Datendatei per Drag-and-Drop verschieben oder auf **[!UICONTROL Browse]** klicken, um sie aus Ihrem Dateisystem hochzuladen.
   * **FTP:** Klicken Sie auf den FTP-Link, um [die Datei über FTP hochzuladen](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Der erste Schritt besteht darin, ein Kennwort für den von Adobe bereitgestellten FTP-Server anzugeben. Geben Sie das Kennwort an und klicken Sie dann auf **[!UICONTROL Done]**.

   Übertragen Sie nun Ihre CSV-/ZIP-/GZIP-Datei auf den FTP-Server. Nachdem diese Dateiübertragung erfolgreich abgeschlossen wurde, erstellen Sie eine Datei mit demselben Namen und einer `.fin`. Übertragen Sie diese leere Datei auf den Server. Dies gibt das Ende der Übertragung an und der [!DNL Experience Cloud] beginnt mit der Verarbeitung der Datendatei.

1. Prüfen Sie das Schema.

   Der Prüfungsprozess ermöglicht die Zuordnung von Anzeigenamen und Beschreibungen zu den hochgeladenen Attributen (Zeichenfolgen, Ganzzahlen, Zahlen usw.). Ordnen Sie die einzelnen Attribute dem jeweils korrekten Datentyp und Anzeigenamen und der korrekten Beschreibung zu.

   Klicken Sie nach Abschluss der Schemavalidierung auf **[!UICONTROL Save]** . Die Zeit für den Datei-Upload variiert je nach Größe.

   ![Schema validieren](/help/main/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema hochladen](/help/main/c-target/c-visitor-profile/assets/upload1.png)

1. Konfigurieren Sie Abonnements und aktivieren Sie die Attributquelle

   Klicken Sie auf **[!UICONTROL Add Subscription]** und wählen Sie dann die Lösung aus, um diese Attribute zu abonnieren. [Abonnements konfigurieren](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) richtet den Datenfluss zwischen dem [!DNL Experience Cloud] und den Lösungen ein. Durch die Aktivierung der Attributquelle können die Daten an die abonnierten Lösungen übertragen werden. Die von Ihnen hochgeladenen Kundeneinträge werden mit den von Ihrer Website oder Anwendung eingehenden ID-Signalen abgeglichen.

   ![Lösung konfigurieren](/help/main/c-target/c-visitor-profile/assets/solution.png)

   ![Aktivieren](/help/main/c-target/c-visitor-profile/assets/activate.png)

   Beachten Sie beim Ausführen dieses Schritts die folgenden Einschränkungen:

   * Die maximale Dateigröße pro Upload mithilfe der HTTP-Methode beträgt 100 MB.
   * Die maximale Dateigröße pro Upload mithilfe der FTP-Methode beträgt 4 GB.
   * Die Anzahl der zum Abonnieren zulässigen Attribute: 5 für [!DNL Target Standard] und 200 für [!DNL Target Premium].

## Verwenden von Kundenattributen in [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

Sie können Kundenattribute in [!DNL Target] wie folgt verwenden:

### Zielgruppen erstellen

In [!DNL Target] können Sie beim Erstellen einer Zielgruppe im Abschnitt [!UICONTROL Visitor Profile] ein Kundenattribut auswählen. Alle Kundenattribute haben das Präfix &lt; data_source_name > in der Liste. Sie können die Attribute beim Aufbau von Zielgruppen beliebig mit anderen Datenattributen kombinieren.

![Zielgruppe](/help/main/c-target/c-visitor-profile/assets/TargetAudience.png)

### Erstellen von Profilskripten mit Token

Kundenattribute können in Profilskripten mithilfe des Formats `crs.get('<Datasource Name>.<Attribute name>')` referenziert werden.

Dieses Profilskript kann direkt in Angeboten verwendet werden, um Attribute bereitzustellen, die zum aktuellen Besucher gehören.

### Verwenden Sie mbox3rdPartyID in Ihrer Website für eine erfolgreiche Implementierung und Verwendung

Übergeben Sie `mbox3rdPartyId` als Parameter an die globale Mbox innerhalb der `targetPageParams()`. Für den Wert von `mbox3rdPartyId` sollte die Kunden-ID festgelegt werden, die in der CSV-Datendatei vorhanden war.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Verwenden des Experience Cloud ID-Service

Wenn Sie den Experience Cloud ID-Service verwenden, müssen Sie eine Kunden-ID und einen Authentifizierungsstatus festlegen, um Kundenattribute für die Zielgruppenbestimmung zu verwenden. Weitere Informationen finden Sie unter [Kunden-IDs und Authentifizierungsstatus](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) im *Handbuch für den Experience Cloud ID-*.

Weitere Informationen zur Verwendung von Kundenattributen in [!DNL Target] finden Sie in den folgenden Ressourcen:

* [Erstellen und Hochladen von Kundenattributdaten](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) im Handbuch zur *Benutzeroberfläche und Administration von Experience Cloud*

## Häufig auftretende Probleme von Kunden {#section_BE0F70E563F64294B17087DE2BC1E74C}

Beim Arbeiten mit Kundenattributen und -[!DNL Target] können folgende Probleme auftreten.

>[!NOTE]
>
>Die Probleme 1 und 2 verursachen etwa 60 % der Probleme in diesem Bereich. Problem 3 verursacht etwa 30 % der Probleme. Problem 4 verursacht etwa 5 % der Probleme. Die restlichen 5 % werden durch verschiedene andere Ursachen hervorgerufen.

### Problem 1: Kundenattribute werden entfernt, da das Profil zu groß ist

Es gibt zwar keine Zeichenbeschränkung für ein bestimmtes Feld im Profil des Benutzers, wenn das Profil jedoch umfangreicher als 64 K ist, wird es durch Entfernen der ältesten Attribute so lange abgeschnitten, bis das Profil wieder kleiner als 64 K ist.

### Problem 2: Attribute werden in [!DNL Target] nicht in der Zielgruppenbibliothek aufgelistet, auch nicht nach mehreren Tagen

Dies ist normalerweise ein Pipeline-Verbindungsproblem. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 3: Versand funktioniert nicht basierend auf dem Attribut

Das Profil wurde in Edge noch nicht aktualisiert. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 4: Implementierungsprobleme

Beachten Sie die folgenden Implementierungsprobleme:

* Die Besucher-ID wurde nicht korrekt übergeben. Die ID wurde in `mboxMCGVID` anstelle von `setCustomerId` übergeben.
* Die Besucher-ID wurde korrekt übergeben, aber der Status der AUTHENTIFIZIERUNG wurde nicht auf „Authentifiziert“ festgelegt.
* `mbox3rdPartyId` wurde nicht korrekt weitergeleitet.

### Problem 5: `mboxUpdate` nicht ordnungsgemäß ausgeführt

`mboxUpdate` wurde nicht ordnungsgemäß mit `mbox3rdPartyId` durchgeführt.

### Problem 6: Kundenattribute werden nicht in [!DNL Target] importiert

Wenn Sie in Target keine Kundenattributdaten finden können, stellen Sie sicher, dass der Import innerhalb der letzten *x* Tage erfolgte, wobei *x* der Target-Wert [Lebensdauer des Besucherprofils](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) ist (standardmäßig 14 Tage).

## Schulungsvideo: Hochladen von Offline-Daten mit Kundenattributen ![Tutorial-Badge](/help/main/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In diesem Video erfahren Sie, wie Sie Offline-CRM-, Helpdesk-, Point-of-Sale- und andere Marketing-Daten in den [!DNL Experience Cloud People]-Service importieren und mit Besuchern mithilfe ihrer bekannten IDs verknüpfen.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
