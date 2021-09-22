---
keywords: Mbox; mbox3rdPartyId; Profilsynchronisierung; Profil synchronisieren
description: Erfahren Sie, wie Sie die mbox3rdPartyId verwenden, die die Besucher-ID Ihres Unternehmens darstellt, z. B. die Mitgliedschafts-ID oder das Treueprogramm Ihres Unternehmens.
title: Wie verwende ich die Echtzeit-Profilsynchronisierung für mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 21%

---

# Echtzeit-Profilsynchronisierung für mbox3rdPartyId

Die `mbox3rdPartyId` in [!DNL Adobe Target] ist die Besucher-ID Ihres Unternehmens, z. B. die Mitgliedschafts-ID für das Treueprogramm Ihres Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

Wenn ein Besucher auf eine Seite zugreift, auf der [!DNL Target] aktiviert ist, wird diesem eine [!DNL Target]-PCID zugewiesen. Wenn sich der Besucher anschließend anmeldet und die Implementierung die `mbox3rdPartyId` an [!DNL Target] übergibt, verbindet [!DNL Target] die `mbox3rdPartyId` des Besuchers mit der [!DNL Target]-PCID.

Alle drei bis fünf Minuten werden die Aktualisierungen mit der Datenbank synchronisiert. Wenn sich der Besucher abmeldet, ersetzen die zusammengeführten Daten die vorherigen Daten, die mit `mbox3rdPartyId` verknüpft sind, und erstellen so einen vollständigen Datensatz der Aktionen dieses Besuchers. Wenn dasselbe Attribut in beiden IDs vorhanden ist - z. B. hat die PCID category=hats und `mbox3rdPartyId` hat category=skis oder wenn der Besucher Erlebnis A vor der Anmeldung gesehen hat, Erlebnis B jedoch in `mbox3rdPartyId` gespeichert ist - überschreibt das Attribut, das in `mbox3rdPartyId` gespeichert ist, das Attribut aus der PCID. Wenn sich der Besucher in einer Aktivität oder einem Erlebnis befand, bevor er sich angemeldet hat, aber in `mbox3rdPartyId` eine andere Aktivität und ein anderes Erlebnis gespeichert sind, wird dieser Besucher nach der Anmeldung in die Aktivität und das Erlebnis `mbox3rdPartyId` eingefügt.

| PCID (nicht angemeldet) | mbox3rdPartyId (angemeldet) | Zusammengeführt und in der mbox3rdPartyId gespeichert |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Aktivität 1, Erlebnis A | Aktivität 1, Erlebnis B | Aktivität 1, Erlebnis B |
| Aktivität 1 |  | Aktivität 1 |

Wenn der Besucher sich anmeldet, wird das zusammengeführte Profil beibehalten.

>[!NOTE]
>
>Wenn Sie zwischen authentifizierten (angemeldeten) Benutzern und nicht authentifizierten Benutzern unterscheiden möchten, verwenden Sie die [!DNL Adobe Experience Cloud Identity Service] (ECID) anstelle der mbox3rdPartyID. Nachdem ein Benutzer mit mbox3rdPartyID verknüpft wurde, bleibt er auch nach dem Abmelden mit dem Benutzer verknüpft.

>[!NOTE]
>
>[!DNL Adobe Analytics] -Ziele werden nicht verfolgt, wenn sich die  [!DNL Adobe Experience Cloud] ID (EDID) ändert (z. B. wenn der Besucher die Geräte ändert), auch wenn das  [!DNL Target] Profil möglicherweise auf der Grundlage der mbox3rdPartyId zusammengeführt wird und trotzdem über Aktivitätsinformationen verfügt. Für Besucher, die mit derselben EDID identifiziert werden (diejenigen, die mit demselben Gerät auf die Seite zugreifen), sollte [!DNL Analytics for Target] (A4T) erwartungsgemäß funktionieren.

## Zu beachten {#considerations}

* Wenn Ihre Seite mehrere Mboxes enthält und nur einige `3rdPartyID` verwenden, hat [!DNL Target] kein separates Besucherprofil/keinen separaten Kontext für jede Besucheranforderung. Der Kontext `3rdPartyID` hat Vorrang vor dem PCID-Kontext. Es reicht aus, wenn eine Mbox `3rdPartyId` übergibt, damit ihr Kontext Vorrang vor PCID hat.

   Angenommen, ein Besucher greift auf eine Seite zu, bevor er sich anmeldet und ein Erlebnis sieht. Die globale Mbox verwendet keine `3rdPartyID`. Nach der Anmeldung sieht der Besucher eines von drei Erlebnissen mit untergeordneten Mboxes, von denen einige `3rdPartyID` verwenden. Der Besucher besucht verschiedene Seiten auf der Site und verwendet dann die Schaltfläche „Zurück“, um zur Hauptseite zurückzukehren, auf die er vor seiner Anmeldung zugegriffen hat. Dort wird ihm ein anderes Erlebnis angezeigt. In diesem Szenario hat die globale Mbox `3rdPartyID` nicht übergeben, aber eine oder mehrere der untergeordneten Mboxes haben dies getan. `3rdPartyID` Vorrang vor PCID.

* Sie können Kunden-IDs von Besuchern auf [!DNL Target] mithilfe zweier Methoden senden:

   1. Verwenden Sie den `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` ist der Parametername bei Verwendung von  `targetPageParams` oder  `targetPageParamsAll`
      * `thirdPartyId` ist der Parametername, den Sie direkt in der Payload der Bereitstellungs-API festgelegt haben.
      * Sie können in diesem Parameter nur einen Wert senden.
   1. Verwenden Sie die Funktion `setCustomerId`/`customerIds` des ECID-Dienstes.

      * `setCustomerId` ist eine Funktion, die Sie in clientseitigen (Browser) Implementierungen verwenden können, wenn VisitorAPI.js auf der Seite verfügbar ist.
      * `customerIds` ist der Parametername, der verwendet wird, wenn Sie ihn direkt in der Payload der Bereitstellungs-API festlegen und normalerweise auf serverseitigen oder IOT-Implementierungen (Internet der Dinge) ausgeführt wird.
      * Im Gegensatz zu `mbox3rdPartyId`/`thirdPartyId` können Sie bei diesem Ansatz mehrere IDs als Liste senden. Da [!DNL Target] jedoch nur eine einzige Kunden-ID pro TnT-ID unterstützt, wird die erste ID in der Liste mit einem bekannten Alias (Alias, der in der Benutzeroberfläche &quot;Kundenattribute&quot;konfiguriert ist) verwendet.

   >[!IMPORTANT]
   >
   > Die Verwendung der beiden oben genannten Ansätze für einen einzelnen Besucher kann zu falschen Profilzusammenführungen der nicht authentifizierten und authentifizierten [!DNL Target]-Profile führen.
   >
   >Adobe rät davon ab, `mbox3rdPartyId`/`thirdPartyId` und `setCustomerID`/`customerIds` gemeinsam zu verwenden.
   >
   >Wenn Sie beide Ansätze synonym verwenden müssen, stellen Sie sicher, dass die erste ID in der von `setCustomerID`/`customerIds` verwendeten Liste der von `thirdPartyId`/`mbox3rdPartyId` verwendeten entspricht und umgekehrt.

