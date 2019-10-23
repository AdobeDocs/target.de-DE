---
description: Die „mbox3rdPartyId“ ist die Besucher-ID Ihres Unternehmens, wie z. B. die Mitgliedschafts-ID des Treueprogramms Ihres Unternehmens.
keywords: Mbox; mbox3rdPartyId; Profilsynchronisierung; Profil synchronisieren
seo-description: 'Informationen über Echtzeitprofile '
seo-title: Synchronisierung von Echtzeitprofilen für mbox3rdPartyId in Adobe Target
solution: Target
title: Echtzeit-Profilsynchronisierung für mbox3rdPartyId
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: 34809d458b4e43e5ed9715803541a81754ee7e0f

---


# Echtzeit-Profilsynchronisierung für mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

Die „mbox3rdPartyId“ ist die Besucher-ID Ihres Unternehmens, wie z. B. die Mitgliedschafts-ID des Treueprogramms Ihres Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

Wenn ein Besucher auf eine Seite zugreift, auf der [!DNL Target] aktiviert ist, wird diesem eine [!DNL Target]-PCID zugewiesen. Wenn sich der Besucher anschließend anmeldet und die Implementierung die „mbox3rdPartyId“ an [!DNL Target] übergibt, verknüpft [!DNL Target] die „mbox3rdPartyId“ des Besuchers mit der [!DNL Target]-PCID.

Alle drei bis fünf Minuten werden die Aktualisierungen mit der Datenbank synchronisiert. Wenn sich der Besucher abmeldet, ersetzen die zusammengeführten Daten die früheren, der „mbox3rdPartyId“ zugeordneten Daten, wodurch der Datensatz mit Besucheraktionen ergänzt wird. Wenn dasselbe Attribut in beiden IDs vorhanden ist, überschreibt das Attribut in „mbox3rdPartyId“ das Attribut der PCID. Das wäre beispielsweise der Fall, wenn die PCID „category=hats“ und die „mbox3rdPartyId“ „category=skis“ aufweisen oder wenn der Besucher vor dem Anmelden Erlebnis A sieht, in der „mbox3rdPartyId“ jedoch Erlebnis B gespeichert ist. Wenn sich der Besucher in einer Aktivität oder einem Erlebnis befand, bevor er sich angemeldet hat, in der „mbox3rdPartyId“ jedoch eine andere Aktivität oder ein anderes Erlebnis gespeichert ist, wird dieser Besucher nach der Anmeldung der Aktivität und dem Erlebnis von „mbox3rdPartyId“ zugeordnet.

| PCID (nicht angemeldet) | mbox3rdPartyId (angemeldet) | Zusammengeführt und in der mbox3rdPartyId gespeichert |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Aktivität 1, Erlebnis A | Aktivität 1, Erlebnis B | Aktivität 1, Erlebnis B |
| Aktivität 1 |  | Aktivität 1 |

Wenn der Besucher sich anmeldet, wird das zusammengeführte Profil beibehalten.

>[!NOTE]
>
>Wenn Sie zwischen authentifizierten (angemeldeten) Benutzern und nicht authentifizierten Benutzern unterscheiden möchten, verwenden Sie anstelle von mbox3rdPartyID den Adobe Experience Cloud-Identitätsdienst (ECID). Nachdem ein Benutzer mit der mbox3rdPartyID verknüpft wurde, bleibt er auch nach dem Abmelden mit dem Benutzer verknüpft.

>[!NOTE]
>
>[!DNL Adobe Analytics] Ziele werden nicht verfolgt, wenn sich die [!DNL Adobe Experience Cloud] ID (EDID) ändert (z. B. wenn der Besucher die Geräte wechselt), auch wenn das [!DNL Target] Profil basierend auf der mbox3rdPartyId zusammengeführt werden kann und immer noch Aktivitätsinformationen enthält. For visitors identified with the same EDID (those who access the page with the same device), [!DNL Analytics for Target] (A4T) should work as expected.

## Zu beachten {#considerations}

Wenn Ihre Seite mehrere Mboxes enthält und nur einige 3rdPartyID verwenden, hat Target nicht für jede Besucheranfrage ein separates Besucherprofil/einen separaten Kontext. Der 3rdPartyID-Kontext hat Vorrang vor dem PCID-Kontext. Es reicht aus, wenn eine Mbox die 3rdPartyID weiterleitet, damit der Kontext Vorrang vor PCID erhält.

Angenommen, ein Besucher greift auf eine Seite zu, bevor er sich anmeldet, und ein Erlebnis wird ihm angezeigt. Die globale Mbox verwendet keine 3rdPartyID. Nach der Anmeldung sieht der Besucher eines von drei Erlebnissen mit untergeordneten Mboxes, von denen einige die 3rdPartyID verwenden. Der Besucher besucht verschiedene Seiten auf der Site und verwendet dann die Schaltfläche „Zurück“, um zur Hauptseite zurückzukehren, auf die er vor seiner Anmeldung zugegriffen hat. Dort wird ihm ein anderes Erlebnis angezeigt. In diesem Szenario gab die globale Mbox die 3rdPartyID nicht weiter, aber eine oder mehrere der untergeordneten Mboxes haben das getan. 3rdPartyID hatte Vorrang vor PCID.
