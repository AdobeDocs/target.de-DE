---
keywords: Mbox;mbox3rdPartyId;Profilsynchronisierung;Profil synchronisieren
description: Erfahren Sie, wie Sie die mbox3rdPartyId verwenden, welche die Besucher-ID Ihres Unternehmens darstellt, z. B. die Mitgliedschafts-ID oder das Treueprogramm Ihres Unternehmens.
title: Wie verwende ich die Echtzeit-Profilsynchronisierung für mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 80%

---

# Echtzeit-Profilsynchronisierung für mbox3rdPartyId

Die `mbox3rdPartyId` in [!DNL Adobe Target] ist die Besucher-ID Ihres Unternehmens, wie z. B. die Mitgliedschafts-ID des Treueprogramms Ihres Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

Wenn ein Besucher auf eine Seite zugreift, auf der [!DNL Target] aktiviert ist, wird diesem eine [!DNL Target]-PCID zugewiesen. Wenn sich der Besucher anschließend anmeldet und die Implementierung die `mbox3rdPartyId` an [!DNL Target] übergibt, verknüpft [!DNL Target] die `mbox3rdPartyId` des Besuchers mit der [!DNL Target]-PCID.

Aktualisierungen werden alle 5 bis 10 Minuten mit dem Profilspeicher synchronisiert. Wenn die Sitzung des Besuchers endet, ersetzen die zusammengeführten Daten die vorherigen Daten, die mit der `mbox3rdPartyId`, wodurch ein vollständiger Datensatz mit den Aktionen dieses Besuchers erstellt wird. Wenn dasselbe Attribut in beiden IDs vorhanden ist – etwa wenn die PCID „category=hats“ und die `mbox3rdPartyId` „category=skis“ aufweisen würde oder wenn der Besucher vor dem Anmelden Erlebnis A sehen würde, in der `mbox3rdPartyId` jedoch Erlebnis B gespeichert wäre –, überschreibt das in `mbox3rdPartyId` gespeicherte Attribut das Attribut der PCID. Wenn sich der Besucher in einer Aktivität oder einem Erlebnis befand, bevor er sich angemeldet hat, in der `mbox3rdPartyId` jedoch eine andere Aktivität oder ein anderes Erlebnis gespeichert ist, wird dieser Besucher nach der Anmeldung der Aktivität und dem Erlebnis von `mbox3rdPartyId` zugeordnet.

| PCID (nicht angemeldet) | mbox3rdPartyId (angemeldet) | Zusammengeführt und in der mbox3rdPartyId gespeichert |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Aktivität 1, Erlebnis A | Aktivität 1, Erlebnis B | Aktivität 1, Erlebnis B |
| Aktivität 1 |  | Aktivität 1 |

Wenn der Besucher sich anmeldet, wird das zusammengeführte Profil beibehalten.

>[!NOTE]
>
>Wenn Sie zwischen authentifizierten (angemeldeten) Benutzern und nicht authentifizierten Benutzern unterscheiden möchten, verwenden Sie die [!DNL Adobe Experience Cloud Identity Service] (ECID) anstelle der mbox3rdPartyID. Nachdem ein Benutzer mit mbox3rdPartyID verknüpft wurde, bleibt die Verknüpfung mit dem Benutzer auch nach dem Abmelden bestehen.

>[!NOTE]
>
>[!DNL Adobe Analytics] -Ziele werden nicht verfolgt, wenn die [!DNL Adobe Experience Cloud] ID (ECID) ändert sich (z. B. der Besucher wechselt Geräte), auch wenn die [!DNL Target] -Profil kann auf Grundlage der mbox3rdPartyId zusammengeführt werden und dennoch über Aktivitätsinformationen verfügen. Für Besucher, die mit derselben ECID identifiziert werden (diejenigen, die mit demselben Gerät auf die Seite zugreifen), [!DNL Analytics for Target] (A4T) sollte erwartungsgemäß funktionieren.

## Zu beachten {#considerations}

* Wenn Ihre Seite mehrere Mboxes enthält und nur einige davon `3rdPartyID` verwenden, hat [!DNL Target] nicht für jede Besucheranfrage ein separates Besucherprofil/einen separaten Kontext. Der `3rdPartyID`-Kontext hat Vorrang vor dem PCID-Kontext. Es reicht aus, wenn eine Mbox die `3rdPartyId` weiterleitet, damit der Kontext Vorrang vor PCID erhält.

   Angenommen, ein Besucher greift auf eine Seite zu, bevor er sich anmeldet, und ein Erlebnis wird ihm angezeigt. Die globale Mbox verwendet keine `3rdPartyID`. Nach der Anmeldung sieht der Besucher eines von drei Erlebnissen mit untergeordneten Mboxes, von denen einige die `3rdPartyID` verwenden. Der Besucher besucht verschiedene Seiten auf der Site und verwendet dann die Schaltfläche „Zurück“, um zur Hauptseite zurückzukehren, auf die er vor seiner Anmeldung zugegriffen hat. Dort wird ihm ein anderes Erlebnis angezeigt. In diesem Szenario gab die globale Mbox die `3rdPartyID` nicht weiter, aber eine oder mehrere der untergeordneten Mboxes haben das getan. `3rdPartyID` hatte Vorrang vor PCID.

* Sie können Kunden-IDs von Besuchern mithilfe zweier Methoden an [!DNL Target] senden:

   1. Verwenden Sie den `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` ist der Parametername bei Verwendung von `targetPageParams` oder `targetPageParamsAll`
      * `thirdPartyId` ist der Parametername, den Sie direkt in der Payload der Bereitstellungs-API festlegen.
      * Sie können in diesem Parameter nur einen Wert senden.
   1. Verwenden Sie die Funktion `setCustomerId`/`customerIds` des ECID-Dienstes.

      * `setCustomerId` ist eine Funktion, die Sie in Client-seitigen Implementierungen (Browser) verwenden können, wenn VisitorAPI.js auf der Seite verfügbar ist.
      * `customerIds` ist der Parametername, der verwendet wird, wenn Sie ihn direkt in der Payload der Bereitstellungs-API festlegen und der normalerweise auf Server-seitigen oder IOT-Implementierungen (Internet der Dinge) ausgeführt wird.
      * Im Gegensatz zu `mbox3rdPartyId`/`thirdPartyId` können Sie bei diesem Ansatz mehrere IDs als Liste senden. Da [!DNL Target] jedoch nur eine einzige Kunden-ID pro TnT-ID unterstützt, wird die erste ID in der Liste mit einem bekannten Alias (Alias, der in der Benutzeroberfläche „Kundenattribute“ konfiguriert ist) verwendet.

   Sie können `mbox3rdPartyId`/`thirdPartyId` if [!DNL Target] ist [!DNL Adobe Experience Cloud] und Sie möchten keine Kundenattribute verwenden. Für alle anderen Fälle wird empfohlen, `setCustomerId`/`customerIds` zum Senden Ihrer Kunden-IDs.

   >[!IMPORTANT]
   >
   > Die Verwendung der beiden oben genannten Ansätze für einen einzelnen Besucher kann zu falschen Profilzusammenführungen der nicht authentifizierten und authentifizierten [!DNL Target]-Profile führen.
   >
   >Adobe rät davon ab, `mbox3rdPartyId`/`thirdPartyId` und `setCustomerID`/`customerIds` gemeinsam zu verwenden.
   >
   >Wenn Sie beide Ansätze synonym verwenden müssen, stellen Sie sicher, dass die erste ID in der von `setCustomerID`/`customerIds` wird von `thirdPartyId`/`mbox3rdPartyId` und umgekehrt.

