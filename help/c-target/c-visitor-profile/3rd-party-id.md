---
description: Die „mbox3rdPartyID“ ist die Besucher-ID Ihres Unternehmens, etwa die Mitgliedschafts-ID für das Treueprogramm des Unternehmens.
keywords: Mbox; MboxdrittanbieterID; Profilsynchronisierung; Profil synchronisieren; PCID
seo-description: 'Informationen über Echtzeitprofile '
seo-title: Profilsynchronisierung in Echtzeit für mbox 3 rdpartyid in Adobe Target
solution: Target
title: Echtzeit-Profilsynchronisation für mbox3rdPartyID
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: 647776170531230a0d0f0aa3d97565fbb75bc963

---


# Echtzeit-Profilsynchronisation für mbox3rdPartyID{#real-time-profile-syncing-for-mbox-rdpartyid}

Die „mbox3rdPartyID“ ist die Besucher-ID Ihres Unternehmens, etwa die Mitgliedschafts-ID für das Treueprogramm des Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

When a visitor accesses a page on which [!DNL Target] is enabled, that visitor is assigned a [!DNL Target] PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyID to [!DNL Target], [!DNL Target] connects that visitor's mbox3rdPartyID with the [!DNL Target] PCID.

Aktualisierungen werden alle drei bis fünf Minuten mit der Datenbank synchronisiert. Wenn sich der Besucher abmeldet, ersetzen die zusammengeführten die vorher gespeicherten Daten, die der „mbox3rdPartyID“ zugeordnet waren, wobei ein vollständigerer Datensatz der Aktionen des Besuchers entsteht. Wenn dasselbe Attribut in beiden IDs vorhanden ist - etwa wenn die PCID „category=hats“ und die „mbox3rdPartyID“ „category=skis“ aufweisen würden oder wenn der Besucher vor dem Anmelden Erlebnis A sehen würde, in der „mbox3rdPartyID“ jedoch Erlebnis B gespeichert wäre - überschreibt das Attribut in „mbox3rdPartyID“ das Attribut der PCID. Wenn sich der Besucher in einer Aktivität oder einem Erlebnis befand, bevor er sich angemeldet hat, in der „mbox3rdPartyID“ jedoch eine andere Aktivität oder ein anderes Erlebnis gespeichert ist, wird dieser Besucher nach der Anmeldung der „mbox3rdPartyID“-Aktivität und dem „mbox3rdPartyID“-Erlebnis zugeordnet.

| PCID (nicht angemeldet) | mbox3rdPartyID (angemeldet) | Zusammengeführt und in der mbox3rdPartyID gespeichert |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Aktivität 1, Erlebnis A | Aktivität 1, Erlebnis B | Aktivität 1, Erlebnis B |
| Aktivität 1 |  | Aktivität 1 |

Wenn der Besucher sich anmeldet, wird das zusammengeführte Profil beibehalten.

>[!NOTE]
>
>[!DNL Adobe Analytics]-Ziele werden nicht verfolgt, wenn sich die [!DNL Adobe Experience Cloud] ID (MID) ändert (z. B. der Besucher ändert das Gerät), auch wenn das [!DNL Target]-Profil möglicherweise auf der Grundlage der mbox3rdPartyID zusammengeführt wird und trotzdem über Aktivitätsinformationen verfügt. Für Besucher, die mit derselben MID identifiziert werden (diejenigen, die mit demselben Gerät auf die Seite zugreifen), sollte [!DNL Analytics for Target] (A4T) wie erwartet funktionieren.

## Zu beachten {#considerations}

Wenn Ihre Seite mehrere mboxes enthält und nur einige verwenden 3 rdpartyid, verfügt Target nicht über ein separates Besucherprofil/einen separaten Kontext für jede Besucheranforderung. Der 3 rdpartyid-Kontext hat Vorrang vor dem PCID-Kontext. Es reicht aus, dass eine mbox 3 rdpartyid weiterleitet, damit der Kontext Vorrang vor PCID erhält.

Angenommen, ein Besucher greift auf eine Seite zu, bevor er sich anmeldet und ein Erlebnis sieht. Die globale Mbox verwendet nicht 3 rdpartyid. Nach der Anmeldung sieht der Besucher eines von drei Erlebnissen mit untergeordneten mboxes, von denen einige 3 rdpartyid verwenden. Der Besucher besucht verschiedene Seiten auf der Site und verwendet dann die Schaltfläche "Zurück" , um zur Hauptseite zurückzukehren, auf die zugegriffen wurde, bevor sich die Anmeldung erfolgt und ein anderes Erlebnis angezeigt wird. In diesem Szenario gab die globale Mbox nicht 3 rdpartyid an, aber eine oder mehrere der untergeordneten mboxes wurden aufgerufen. 3 Rdpartyid hat Vorrang vor PCID.
