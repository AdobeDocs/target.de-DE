---
keywords: customer relationship management;customer record service;crs;crm;mbox3rdpartyid;customer attributes;targeting;csv;crm;adobe experience cloud people
description: Informationen zum Verwenden von Unternehmenskundendaten aus einer CRM-Datenbank für das Targeting von Inhalten in Adobe Target mithilfe von Kundenattributen im Adobe Experience Cloud People-Core-Service.
title: Kundenattribute in Adobe Target
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 40%

---


# Kundenattribute {#customer-attributes}

Informationen zur Verwendung von Unternehmenskundendaten aus CRM-Datenbanken (Customer Relationship Management) für Content-Targeting in [!DNL Adobe Target] durch Verwendung von Kundenattributen im [!DNL Adobe Enterprise Cloud People]-Hauptdienst.

Daten von Unternehmenskunden, die über mehrere Quellen erfasst und in CRM-Datenbanken gespeichert werden, können in [!DNL Target] verwendet werden, um den Kunden strategisch die relevantesten Inhalte bereitzustellen, wobei der Schwerpunkt auf zurückkehrenden Kunden liegt. Audiencen und Kundenattribute im [!DNL People]-Hauptdienst (ehemals Profil und Audiencen) verbinden Datenerfassung und Analyse mit Test und Optimierung, sodass Daten und Erkenntnisse umsetzbar sind.

## Übersicht über Kundenattribute {#section_B4099971FA4B48598294C56EAE86B45A}

[Kundenattribute ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html) im  [!DNL People] Hauptdienst sind Teil des ,  [!DNL Adobe Experience Cloud] und Unternehmen können ihre Kundendaten auf die  [!DNL Experience Cloud] Plattform übertragen.

In [!DNL Experience Cloud] integrierte Daten sind für alle [!DNL Experience Cloud]-Workflows verfügbar. [!DNL Target] verwendet diese Daten für das Targeting rückkehrender Kunden basierend auf Attributen. [!DNL Adobe Analytics] verwendet diese Attribute, und sie können für die Analyse und Segmentierung herangezogen werden.

![crs-Beispiel](/help/c-target/c-visitor-profile/assets/crs.png)

Berücksichtigen Sie die folgenden Informationen bei Ihrer Arbeit mit Kundenattributen und [!DNL Target]:

* Es gibt einige Voraussetzungen, die erfüllt sein müssen, bevor Sie die Funktion [!UICONTROL Kundenattribute] im [!DNL People]-Hauptdienst verwenden können. Weitere Informationen finden Sie unter &quot;Voraussetzungen für das Hochladen von Kundenattributen&quot;in [Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in der *Experience Cloud- und Core Services-Produktdokumentation*.

   >[!NOTE]
   >
   >[!DNL at.js] (beliebige Version) oder  [!DNL mbox.js] Version 58 oder höher erforderlich.

* [!DNL Adobe] garantiert nicht, dass 100 % der Kundenattributdaten (Besucher-Profil) aus CRM-Datenbanken an die Daten des Unternehmens gesendet werden  [!DNL Experience Cloud] und somit für das Targeting in  [!DNL Target]der Datenbank zur Verfügung stehen. In unserem aktuellen Design besteht die Möglichkeit, dass ein kleiner Anteil der Daten (bis zu 0,1 % der großen Produktionschargen) möglicherweise nicht an Bord mitgeführt wird.
* Die Lebensdauer der vom [!DNL Experience Cloud] bis [!DNL Target] importierten Kundenattributdaten hängt von der Lebensdauer des Besucher-Profils ab, die standardmäßig 14 Tage beträgt. Weitere Informationen finden Sie unter  [Lebensdauer des Besucherprofils](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Wenn die `vst.*`-Parameter das einzige Element sind, das den Besucher identifiziert, wird das vorhandene &quot;authentifizierte&quot;Profil nicht abgerufen, solange `authState` UNAUTHENTICATED (0) ist. Das Profil kommt nur dann ins Spiel, wenn `authState` in AUTHENTICATED (1) geändert wird.

   Wenn beispielsweise der Parameter `vst.myDataSource.id` zum Identifizieren des Besuchers verwendet wird (wobei `myDataSource` der Datenquellenalias ist) und keine MCID oder Drittanbieter-ID vorhanden ist, ruft der Parameter `vst.myDataSource.authState=0` das Profil nicht ab, das möglicherweise über einen Kundenattributimport erstellt wurde. Wenn Sie das authentifizierte Profil abrufen möchten, muss `vst.myDataSource.authState` den Wert 1 haben (AUTHENTICATED).

* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

## Zugriff auf Kundenattribute im Hauptdienst &quot;Personen&quot;

1. Klicken Sie in [!DNL Adobe Experience Cloud] auf das Menüsymbol ( ![Menüsymbol](/help/c-target/c-visitor-profile/assets/menu-icon.png) ) und dann auf **[!UICONTROL Personen]**.

   ![Personen](/help/c-target/c-visitor-profile/assets/people.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Kundenattribute]**.

   ![Registerkarte &quot;Kundenattribute&quot;](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Arbeitsablauf für Kundenattribute für die Zielgruppe {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Führen Sie die folgenden Schritte aus, um CRM-Daten in [!DNL Target] zu verwenden, wie unten dargestellt:

![crm-Arbeitsablauf](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Detaillierte Anweisungen zum Ausführen der folgenden Aufgaben finden Sie unter [Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in der *Experience Cloud- und Core Services-Produktdokumentation*.

1. Erstellen einer Datendatei.

   Exportieren Sie die Kundendaten aus Ihrem CRM-System in das CSV-Format, um eine .csv-Datei zu erstellen. Alternativ kann eine ZIP- oder GZIP-Datei für den Upload erstellt werden. Stellen Sie sicher, dass die erste Zeile der CSV-Datei die Kopfzeile und alle Zeilen (Kundendaten) die gleiche Anzahl von Einträgen aufweisen.

   Die folgende Abbildung zeigt eine Beispieldatendatei für Unternehmenskunden:

   ![crs-Beispiel](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   Die folgende Abbildung zeigt eine Beispiel für eine CSV-Datei für Unternehmenskunden:

   ![CSV-Beispiel](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Erstellen der Attributquelle und Hochladen der Datendatei.

   Geben Sie einen Namen und eine Beschreibung der Datenquelle und die Alias-ID an. Die Alias-ID ist eine eindeutige ID, die im Kundenattributcode in `VisitorAPI.js` verwendet wird.

   >[!IMPORTANT]
   >
   >Der Name der Datenquelle und der Attributname dürfen keinen Punkt enthalten.

   Ihre Datendatei muss den Anforderungen für das Hochladen der Datei entsprechen und darf 100 MB nicht überschreiten. Wenn Ihre Datei zu groß ist oder Sie Daten haben, die regelmäßig hochgeladen werden müssen, können Sie stattdessen eine FTP-Verbindung mit Ihren Dateien herstellen.

   * **HTTPS:** Sie können die .csv-Datendatei per Drag &amp; Drop verschieben oder auf &quot; **** Durchsuchen&quot;klicken, um sie aus Ihrem Dateisystem hochzuladen.
   * **FTP:** Klicken Sie auf den FTP-Link, um die Datei über FTP  [hochzuladen](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Der erste Schritt besteht darin, ein Kennwort für den von Adobe bereitgestellten FTP-Server anzugeben. Geben Sie das Kennwort ein und klicken Sie dann auf **[!UICONTROL Fertig]**.

   Übertragen Sie nun Ihre CSV-/ZIP-/GZIP-Datei auf den FTP-Server. Nachdem die Dateiübertragung erfolgreich war, erstellen Sie eine neue Datei mit demselben Namen und der Erweiterung .fin. Übertragen Sie diese leere Datei auf den Server. Dies bedeutet, dass die Datendatei am Ende der Übertragung und die [!DNL Experience Cloud]-Beginn verarbeitet werden.

1. Prüfen des Schemas.

   Der Prüfungsprozess ermöglicht die Zuordnung von Anzeigenamen und Beschreibungen zu den hochgeladenen Attributen (Zeichenfolgen, Ganzzahlen, Zahlen usw.). Ordnen Sie die einzelnen Attribute dem jeweils korrekten Datentyp und Anzeigenamen und der korrekten Beschreibung zu.

   Klicken Sie nach Abschluss der Schema-Überprüfung auf **[!UICONTROL Speichern]**. Die Zeit für den Datei-Upload variiert je nach Größe.

   ![Schema überprüfen](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema hochladen](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Konfigurieren von Abonnements und Aktivieren der Attributquelle.

   Klicken Sie auf **[!UICONTROL Abonnement hinzufügen]** und wählen Sie die Lösung zum Abonnieren dieser Attribute aus. [Durch die Konfiguration von ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) Abonnements wird der Datenfluss zwischen dem  [!DNL Experience Cloud] und den Lösungen sichergestellt. Durch die Aktivierung der Attributquelle können die Daten an die abonnierten Lösungen übertragen werden. Die von Ihnen hochgeladenen Kundendatensätze werden mit den von Ihrer Website oder Anwendung eingehenden ID-Signalen abgeglichen.

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

Übergeben Sie `mbox3rdPartyId` als Parameter an die globale Mbox innerhalb der `targetPageParams()`-Methode. Der Wert von `mbox3rdPartyId` sollte auf die Kunden-ID eingestellt werden, die in der CSV-Datendatei vorhanden war.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Verwenden des Experience Cloud ID-Service

Wenn Sie den Experience Cloud ID-Service verwenden, müssen Sie eine Kunden-ID und einen Authentifizierungsstatus festlegen, um Kundenattribute im Targeting zu verwenden. Weitere Informationen finden Sie unter [Kunden-IDs und Authentifizierungsstatus](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in der *Hilfe zum Experience Cloud-Identitätsdienst*.

Weitere Informationen zum Verwenden von Kundenattributen in [!DNL Target] finden Sie unter den folgenden Ressourcen:

* [Erstellen Sie eine Kundenattributquelle und laden Sie die ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) Datendatei in die  *Experience Cloud-Produktdokumentation hoch.*
* [Kundenattribute: Je mehr Details, desto besser die Verbindung](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) im *Digital Marketing-Blog*

## Häufige Probleme bei Kunden {#section_BE0F70E563F64294B17087DE2BC1E74C}

Beim Arbeiten mit Kundenattributen und [!DNL Target] treten möglicherweise die folgenden Probleme auf.

>[!NOTE]
>
>Die Probleme 1 und 2 verursachen etwa 60 % der Probleme in diesem Bereich. Problem 3 verursacht ca. 30 % der Probleme. Problem 4 verursacht ungefähr 5 % der Probleme. Die restlichen 5 % werden durch verschiedene andere Ursachen hervorgerufen.

### Problem 1: Kundenattribute werden entfernt, da das Profil zu groß ist

Es gibt zwar keine Zeichenbeschränkung für ein bestimmtes Feld im Profil des Benutzers, wenn das Profil jedoch umfangreicher als 64 K ist, wird es durch Entfernen der ältesten Attribute so lange abgeschnitten, bis das Profil wieder kleiner als 64 K ist.

### Problem 2: Attribute, die nicht in der Audience-Bibliothek in [!DNL Target] aufgeführt sind, auch nach mehreren Tagen

Dies ist normalerweise ein Pipeline-Verbindungsproblem. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 3: Versand funktioniert nicht auf Grundlage des Attributs

Das Profil wurde in Edge noch nicht aktualisiert. Bitten Sie zur Lösung das Kundenattribute-Team, den Feed erneut zu veröffentlichen.

### Problem 4: Implementierungsfragen

Beachten Sie die folgenden Implementierungsprobleme:

* Die Besucher-ID wurde nicht korrekt übergeben. Die ID wurde in `mboxMCGVID` anstelle von `setCustomerId` weitergegeben.
* Die Besucher-ID wurde korrekt übergeben, aber der Status der AUTHENTIFIZIERUNG wurde nicht auf „Authentifiziert“ festgelegt.
* `mbox3rdPartyId` wurde nicht korrekt weitergeleitet.

### Problem 5: `mboxUpdate` nicht ordnungsgemäß ausgeführt

`mboxUpdate` wurde nicht ordnungsgemäß mit `mbox3rdPartyId` ausgeführt.

### Problem 6: Kundenattribute werden nicht nach [!DNL Target] importiert

Wenn Sie Kundenattributdaten nicht in der Zielgruppe finden können, stellen Sie sicher, dass der Import innerhalb der letzten *x* Tage erfolgte, bei denen *x* der Zielgruppe [Besucher Profil Lifetime](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) (standardmäßig 14 Tage) ist.

## Schulungsvideo: Offline-Daten mit Kundenattributen hochladen ![Tutorial-Zeichen](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In diesem Video erfahren Sie, wie Sie Offline-CRM-, Help Desk-, Point-of-Sale- und andere Marketing-Daten in den [!DNL Experience Cloud People]-Dienst importieren und mit den bekannten IDs mit Besuchern verknüpfen.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
