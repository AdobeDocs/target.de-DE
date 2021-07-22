---
keywords: Mbox; mbox3rdPartyId; Profilsynchronisierung; Profil synchronisieren
description: Erfahren Sie, wie Sie die mbox3rdPartyId verwenden, die die Besucher-ID Ihres Unternehmens darstellt, z. B. die Mitgliedschafts-ID oder das Treueprogramm Ihres Unternehmens.
title: Wie verwende ich die Echtzeit-Profilsynchronisierung für mbox3rdPartyId?
feature: Zielgruppen
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: c19163020cdcb41a17ea6b65b5b500fadc9c7512
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 61%

---

# Echtzeit-Profilsynchronisierung für mbox3rdPartyId

Die mbox3rdPartyId in [!DNL Adobe Target] ist die Besucher-ID Ihres Unternehmens, z. B. die Mitgliedschafts-ID für das Treueprogramm Ihres Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

Wenn ein Besucher auf eine Seite zugreift, auf der [!DNL Target] aktiviert ist, wird diesem eine [!DNL Target]-PCID zugewiesen. Wenn sich der Besucher anschließend anmeldet und die Implementierung die „mbox3rdPartyId“ an [!DNL Target] übergibt, verknüpft [!DNL Target] die „mbox3rdPartyId“ des Besuchers mit der [!DNL Target]-PCID.

Alle drei bis fünf Minuten werden die Aktualisierungen mit der Datenbank synchronisiert. Wenn sich der Besucher abmeldet, ersetzen die zusammengeführten Daten die vorherigen Daten, die mit der mbox3rdPartyId verknüpft sind, und erstellen so einen vollständigen Datensatz der Aktionen dieses Besuchers. Wenn dasselbe Attribut in beiden IDs vorhanden ist, überschreibt das Attribut in „mbox3rdPartyId“ das Attribut der PCID. Das wäre beispielsweise der Fall, wenn die PCID „category=hats“ und die „mbox3rdPartyId“ „category=skis“ aufweisen oder wenn der Besucher vor dem Anmelden Erlebnis A sieht, in der „mbox3rdPartyId“ jedoch Erlebnis B gespeichert ist. Wenn sich der Besucher in einer Aktivität oder einem Erlebnis befand, bevor er sich angemeldet hat, in der „mbox3rdPartyId“ jedoch eine andere Aktivität oder ein anderes Erlebnis gespeichert ist, wird dieser Besucher nach der Anmeldung der Aktivität und dem Erlebnis von „mbox3rdPartyId“ zugeordnet.

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

Wenn Ihre Seite mehrere Mboxes enthält und nur einige 3rdPartyID verwenden, verfügt [!DNL Target] nicht über ein separates Besucherprofil/Kontext für jede Besucheranfrage. Der 3rdPartyID-Kontext hat Vorrang vor dem PCID-Kontext. Es reicht aus, wenn eine Mbox die 3rdPartyID weiterleitet, damit der Kontext Vorrang vor PCID erhält.

Angenommen, ein Besucher greift auf eine Seite zu, bevor er sich anmeldet und ein Erlebnis sieht. Die globale Mbox verwendet keine 3rdPartyID. Nach der Anmeldung sieht der Besucher eines von drei Erlebnissen mit untergeordneten Mboxes, von denen einige die 3rdPartyID verwenden. Der Besucher besucht verschiedene Seiten auf der Site und verwendet dann die Schaltfläche „Zurück“, um zur Hauptseite zurückzukehren, auf die er vor seiner Anmeldung zugegriffen hat. Dort wird ihm ein anderes Erlebnis angezeigt. In diesem Szenario gab die globale Mbox die 3rdPartyID nicht weiter, aber eine oder mehrere der untergeordneten Mboxes haben das getan. 3rdPartyID hatte Vorrang vor PCID.
