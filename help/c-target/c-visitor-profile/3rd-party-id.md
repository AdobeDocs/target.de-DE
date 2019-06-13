---
description: Die „mbox3rdPartyID“ ist die Besucher-ID Ihres Unternehmens, etwa die Mitgliedschafts-ID für das Treueprogramm des Unternehmens.
keywords: Mbox; MboxdrittanbieterID; Profilsynchronisierung; Profil synchronisieren
seo-description: Die „mbox3rdPartyID“ ist die Besucher-ID Ihres Unternehmens, etwa die Mitgliedschafts-ID für das Treueprogramm des Unternehmens.
seo-title: Echtzeit-Profilsynchronisation für mbox3rdPartyID
solution: Target
title: Echtzeit-Profilsynchronisation für mbox3rdPartyID
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Echtzeit-Profilsynchronisation für mbox3rdPartyID{#real-time-profile-syncing-for-mbox-rdpartyid}

Die „mbox3rdPartyID“ ist die Besucher-ID Ihres Unternehmens, etwa die Mitgliedschafts-ID für das Treueprogramm des Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

Wenn ein Besucher auf eine Seite zugreift, auf der Target aktiviert ist, wird diesem eine Target-PCID zugewiesen. Wenn sich der Besucher anschließend anmeldet und die Implementierung die „mbox3rdPartyID“ an Target übergibt, verknüpft Target die „mbox3rdPartyID“ des Besuchers mit der Target-PCID.

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
