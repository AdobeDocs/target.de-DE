---
keywords: Customer Relationship Management;Customer Record Service;crs;crm;mbox3rdpartyid;Kundenattribute;Targeting;csv;crm;Adobe Experience Cloud People
description: Erfahren Sie, wie Sie Enterprise-Kundendaten aus einer CRM-Datenbank (Customer Relationship Management) für Content-Targeting in [!DNL Adobe Target] verwenden.
title: Was sind Kundenattribute und wie verwende ich sie?
feature: Zielgruppen
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: c19163020cdcb41a17ea6b65b5b500fadc9c7512
workflow-type: tm+mt
source-wordcount: '1496'
ht-degree: 36%

---

# Kundenattribute

Informationen zur Verwendung von Unternehmenskundendaten aus CRM-Datenbanken (Customer Relationship Management) für Content-Targeting in [!DNL Adobe Target] durch Verwendung von Kundenattributen im [!DNL Adobe Enterprise Cloud People]-Dienst.

Enterprise-Kundendaten, die über mehrere Quellen erfasst und in CRM-Datenbanken gespeichert werden, können in [!DNL Target] verwendet werden, um strategisch die relevantesten Inhalte für Kunden bereitzustellen, insbesondere mit dem Schwerpunkt auf Bestandskunden. Zielgruppen und Kundenattribute im [!DNL People]-Dienst (ehemals Profile und Zielgruppen) verbinden die Datenerfassung und -analyse mit Tests und Optimierung, sodass Daten und Erkenntnisse umsetzbar sind.

## Übersicht über Kundenattribute {#section_B4099971FA4B48598294C56EAE86B45A}

[Kundenattribute ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=de) im  [!DNL People] Dienst sind Teil von  [!DNL Adobe Experience Cloud] und bieten Unternehmen ein Tool, um ihre Kundendaten auf die  [!DNL Experience Cloud] Plattform zu übertragen.

In [!DNL Experience Cloud] integrierte Daten sind für alle [!DNL Experience Cloud]-Workflows verfügbar. [!DNL Target] verwendet diese Daten für das Targeting von Bestandskunden basierend auf Attributen. [!DNL Adobe Analytics] verwendet diese Attribute, und sie können für die Analyse und Segmentierung herangezogen werden.

![crs-Beispiel](/help/c-target/c-visitor-profile/assets/crs.png)

Beachten Sie die folgenden Informationen bei Ihrer Arbeit mit Kundenattributen und [!DNL Target]:

* Es gibt einige Voraussetzungen, die Sie erfüllen müssen, bevor Sie die Funktion [!UICONTROL Kundenattribute] im [!DNL People]-Dienst verwenden können. Weitere Informationen finden Sie unter &quot;Voraussetzungen für das Hochladen von Kundenattributen&quot;in [Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in der *Dokumentation zu Experience Cloud Services und Administration*.

   >[!NOTE]
   >
   >[!DNL at.js] (beliebige Version) oder  [!DNL mbox.js] Version 58 oder höher erforderlich.

* [!DNL Adobe] garantiert nicht, dass 100 % der Kundenattributdaten (Besucherprofildaten) aus CRM-Datenbanken in die integriert werden  [!DNL Experience Cloud] und daher für das Targeting in  [!DNL Target]verfügbar sind. Beim aktuellen Design besteht die Möglichkeit, dass ein kleiner Anteil der Daten (bis zu 0,1 % der großen Produktions-Batches) nicht integriert wird.
* Die Lebensdauer der von [!DNL Experience Cloud] bis [!DNL Target] importierten Kundenattributdaten hängt von der Lebensdauer des Besucherprofils ab, die standardmäßig 14 Tage beträgt. Weitere Informationen finden Sie unter [Lebensdauer des Besucherprofils](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Wenn die Parameter `vst.*` das einzige Element sind, das den Besucher identifiziert, wird das vorhandene &quot;authentifizierte&quot;Profil nicht abgerufen, solange `authState` UNAUTHENTICATED (0) ist. Das Profil kommt nur ins Spiel, wenn `authState` in AUTHENTICATED (1) geändert wird.

   Wenn beispielsweise der Parameter `vst.myDataSource.id` verwendet wird, um den Besucher zu identifizieren (wobei `myDataSource` der Alias für die Datenquelle ist), und es keine MCID oder Drittanbieter-ID gibt, ruft die Verwendung des Parameters `vst.myDataSource.authState=0` nicht das Profil ab, das möglicherweise durch einen Kundenattribut-Import erstellt wurde. Wenn das gewünschte Verhalten darin besteht, das authentifizierte Profil abzurufen, muss das `vst.myDataSource.authState` den Wert 1 (AUTHENTICATED) haben.

* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

## Zugriff auf Kundenattribute im People-Dienst

1. Klicken Sie in [!DNL Adobe Experience Cloud] auf das Menüsymbol ( ![Menüsymbol](/help/c-target/c-visitor-profile/assets/menu-icon.png) ) und klicken Sie dann auf **[!UICONTROL Personen]**.

   ![Personen](/help/c-target/c-visitor-profile/assets/people.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Kundenattribute]** .

   ![Registerkarte &quot;Kundenattribute&quot;](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Kundenattribut-Workflow für [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Führen Sie die folgenden Schritte aus, um CRM-Daten in [!DNL Target] zu verwenden, wie unten dargestellt:

![crm-Workflow](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Detaillierte Anweisungen zum Abschließen der folgenden Aufgaben finden Sie unter [Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in der *Dokumentation zu Experience Cloud Services und Administration*.

1. Erstellen einer Datendatei.

   Exportieren Sie die Kundendaten aus Ihrem CRM-System in das CSV-Format, um eine .csv-Datei zu erstellen. Alternativ kann eine ZIP- oder GZIP-Datei für den Upload erstellt werden. Stellen Sie sicher, dass die erste Zeile der CSV-Datei die Kopfzeile ist und alle Zeilen (Kundendaten) dieselbe Anzahl Einträge aufweisen.

   Die folgende Abbildung zeigt eine Beispieldatei für Unternehmenskundendaten:

   ![crs-Beispiel](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   Die folgende Abbildung zeigt eine CSV-Beispieldatei für Unternehmenskunden:

   ![CSV-Beispiel](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Erstellen der Attributquelle und Hochladen der Datendatei.

   Geben Sie einen Namen und eine Beschreibung der Datenquelle und die Alias-ID an. Die Alias-ID ist eine eindeutige ID, die im Kundenattribut-Code in `VisitorAPI.js` verwendet wird.

   >[!IMPORTANT]
   >
   >Der Name der Datenquelle und der Attributname dürfen keinen Punkt enthalten.

   Ihre Datendatei muss den Anforderungen für das Hochladen der Datei entsprechen und darf 100 MB nicht überschreiten. Wenn Ihre Datei zu groß ist oder Sie Daten haben, die wiederkehrend hochgeladen werden müssen, können Sie stattdessen Ihre Dateien FTP-Konto einrichten.

   * **HTTPS:** Sie können die .csv-Datendatei per Drag-and-Drop verschieben oder auf  **** Durchsuchen klicken, um sie aus Ihrem Dateisystem hochzuladen.
   * **FTP:** Klicken Sie auf den FTP-Link, um die Datei über FTP  [hochzuladen](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Der erste Schritt besteht darin, ein Kennwort für den von Adobe bereitgestellten FTP-Server anzugeben. Geben Sie das Kennwort ein und klicken Sie dann auf **[!UICONTROL Fertig]**.

   Übertragen Sie nun Ihre CSV-/ZIP-/GZIP-Datei auf den FTP-Server. Nachdem diese Dateiübertragung erfolgreich war, erstellen Sie eine Datei mit demselben Namen und einer `.fin` -Erweiterung. Übertragen Sie diese leere Datei auf den Server. Dies bedeutet, dass das Ende der Übertragung und [!DNL Experience Cloud] mit der Verarbeitung der Datendatei beginnt.

1. Prüfen des Schemas.

   Der Prüfungsprozess ermöglicht die Zuordnung von Anzeigenamen und Beschreibungen zu den hochgeladenen Attributen (Zeichenfolgen, Ganzzahlen, Zahlen usw.). Ordnen Sie die einzelnen Attribute dem jeweils korrekten Datentyp und Anzeigenamen und der korrekten Beschreibung zu.

   Klicken Sie nach Abschluss der Schemavalidierung auf **[!UICONTROL Speichern]**. Die Zeit für den Datei-Upload variiert je nach Größe.

   ![Schema überprüfen](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema hochladen](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Konfigurieren von Abonnements und Aktivieren der Attributquelle.

   Klicken Sie auf **[!UICONTROL Abonnement hinzufügen]** und wählen Sie die Lösung zum Abonnieren dieser Attribute aus. [Konfigurieren von ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) Abonnements ermöglicht den Datenfluss zwischen den Lösungen  [!DNL Experience Cloud] und . Durch die Aktivierung der Attributquelle können die Daten an die abonnierten Lösungen übertragen werden. Die von Ihnen hochgeladenen Kundendatensätze werden mit den von Ihrer Website oder Anwendung eingehenden ID-Signalen abgeglichen.

   ![Lösung konfigurieren](/help/c-target/c-visitor-profile/assets/solution.png)

   ![Aktivieren](/help/c-target/c-visitor-profile/assets/activate.png)

   Beachten Sie beim Ausführen dieses Schritts die folgenden Einschränkungen:

   * Die maximale Dateigröße pro Upload mithilfe der HTTP-Methode beträgt 100 MB.
   * Die maximale Dateigröße pro Upload mithilfe der FTP-Methode beträgt 4 GB.
   * Die Anzahl der zum Abonnieren zulässigen Attribute: 5 für [!DNL Target Standard] und 200 für [!DNL Target Premium].

## Kundenattribute in [!DNL Target] verwenden {#section_107E3A0F0EC7478E82E6DBD17B30B756}

Sie können Kundenattribute in [!DNL Target] wie folgt verwenden:

### Erstellen von Targeting-Zielgruppen

In [!DNL Target] können Sie beim Erstellen einer Zielgruppe im Bereich Besucherprofil ein Kundenattribut auswählen.  Alle Kundenattribute haben das Präfix &lt; data_source_name > in der Liste. Sie können die Attribute beim Aufbau von Zielgruppen beliebig mit anderen Datenattributen kombinieren.

![Zielgruppe](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### Erstellen von Profilskripten mithilfe von Token

Kundenattribute können in Profilskripten mithilfe des Formats `crs.get('<Datasource Name>.<Attribute name>')` referenziert werden.

Dieses Profilskript kann direkt in Angeboten verwendet werden, um Attribute bereitzustellen, die zum aktuellen Besucher gehören.

### Verwenden von mbox3rdPartyID auf Ihrer Website für eine erfolgreiche Implementierung und Verwendung

Übergeben Sie `mbox3rdPartyId` als Parameter an die globale Mbox innerhalb der `targetPageParams()` -Methode. Der Wert von `mbox3rdPartyId` sollte auf die Kunden-ID festgelegt werden, die in der CSV-Datendatei vorhanden war.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Verwenden des Experience Cloud ID-Service

Wenn Sie den Experience Cloud-ID-Dienst verwenden, müssen Sie eine Kunden-ID und einen Authentifizierungsstatus festlegen, um Kundenattribute beim Targeting zu verwenden. Weitere Informationen finden Sie unter [Kunden-IDs und Authentifizierungsstatus](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in der *Hilfe zum Experience Cloud-ID-Dienst*.

Weitere Informationen zum Verwenden von Kundenattributen in [!DNL Target] finden Sie unter den folgenden Ressourcen:

* [Erstellen Sie eine Kundenattributquelle und laden Sie die ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) Datendatei in die Dokumentation zu  *Experience Cloud Services und Administration hoch.*
* [Kundenattribute: Je mehr Details, desto besser die Verbindung](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) im *Digital Marketing-Blog*

## Häufig von Kunden aufgetretene Probleme {#section_BE0F70E563F64294B17087DE2BC1E74C}

Beim Arbeiten mit Kundenattributen und [!DNL Target] treten möglicherweise die folgenden Probleme auf.

>[!NOTE]
>
>Die Probleme 1 und 2 verursachen ca. 60 % der Probleme in diesem Bereich. Problem 3 verursacht ca. 30 % der Probleme. Problem 4 verursacht ca. 5 % der Probleme. Die restlichen 5 % werden durch verschiedene andere Ursachen hervorgerufen.

### Problem 1: Kundenattribute werden entfernt, da das Profil zu groß ist

Es gibt zwar keine Zeichenbeschränkung für ein bestimmtes Feld im Profil des Benutzers, wenn das Profil jedoch umfangreicher als 64 K ist, wird es durch Entfernen der ältesten Attribute so lange abgeschnitten, bis das Profil wieder kleiner als 64 K ist.

### Problem 2: Attribute werden nicht in der Zielgruppenbibliothek in [!DNL Target] aufgelistet, selbst nach mehreren Tagen nicht

Dies ist normalerweise ein Pipeline-Verbindungsproblem. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 3: Versand funktioniert nicht auf der Basis des Attributs

Das Profil wurde in Edge noch nicht aktualisiert. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 4: Implementierungsprobleme

Beachten Sie die folgenden Implementierungsprobleme:

* Die Besucher-ID wurde nicht korrekt übergeben. Die ID wurde in `mboxMCGVID` anstelle von `setCustomerId` übergeben.
* Die Besucher-ID wurde korrekt übergeben, aber der Status der AUTHENTIFIZIERUNG wurde nicht auf „Authentifiziert“ festgelegt.
* `mbox3rdPartyId` wurde nicht korrekt weitergeleitet.

### Problem 5: `mboxUpdate` nicht ordnungsgemäß ausgeführt

`mboxUpdate` wurde nicht ordnungsgemäß mit `mbox3rdPartyId` ausgeführt.

### Problem 6: Kundenattribute werden nicht nach [!DNL Target] importiert

Wenn Sie in Target keine Kundenattributdaten finden können, stellen Sie sicher, dass der Import innerhalb der letzten *x* Tage erfolgte, bei denen *x* der Wert für Target [Besucherprofil-Lebensdauer](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) ist (standardmäßig 14 Tage).

## Schulungsvideo: Hochladen von Offline-Daten mithilfe von Kundenattributen ![Tutorial-Badge](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In diesem Video erfahren Sie, wie Sie Offline-CRM-, Helpdesk-, Point-of-Sale- und andere Marketing-Daten in den [!DNL Experience Cloud People]-Dienst importieren und sie mit Besuchern verknüpfen, die ihre bekannten IDs verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
