---
description: Die mbox 3 rdpartyid ist die Besucher-ID Ihres Unternehmens, z. B. die Mitgliedschafts-ID für das Treueprogramm Ihres Unternehmens.
keywords: mbox; mbox 3 rdpartyid; profile syncing; profile synch; PCID
seo-description: 'Informationen über Echtzeitprofile '
seo-title: Profilsynchronisierung in Echtzeit für mbox 3 rdpartyid in Adobe Target
solution: Target
title: Profilsynchronisierung in Echtzeit für mbox 3 rdpartyid
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: f54dba622e449fb8dac44cb37ff711419f8eda4b

---


# Real-time profile syncing for mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

Die mbox 3 rdpartyid ist die Besucher-ID Ihres Unternehmens, z. B. die Mitgliedschafts-ID für das Treueprogramm Ihres Unternehmens.

Wenn sich ein Besucher bei einer Unternehmenswebsite anmeldet, erstellt das Unternehmen in der Regel eine ID, die seinem Konto, seiner Treuekarte, seiner Mitgliedsnummer oder anderen für das Unternehmen relevanten Identifikatoren zugeordnet wird.

When a visitor accesses a page on which [!DNL Target] is enabled, that visitor is assigned a [!DNL Target] PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyId to [!DNL Target], [!DNL Target] connects that visitor's mbox3rdPartyId with the [!DNL Target] PCID.

Alle drei bis fünf Minuten werden die Aktualisierungen mit der Datenbank synchronisiert. Wenn sich der Besucher auswählt, ersetzen die zusammengeführten Daten die vorherigen mit der mbox 3 rdpartyid verknüpften Daten, wodurch ein vollständigerer Datensatz zu den Aktionen dieses Besuchers erstellt wird. Wenn dasselbe Attribut in beiden IDs vorhanden ist—Beispiel: Die PCID hat category = hats und die mbox 3 rdpartyid hat category = skis oder wenn das Besucher Erlebnis A vor der Anmeldung sah, aber Erlebnis B wird in der mbox 3 rdpartyid gespeichert. —Das in der mbox 3 rdpartyid gespeicherte Attribut überschreibt das Attribut aus der PCID. Wenn sich der Besucher in einer Aktivität oder einem Erlebnis befand, bevor er sich anmeldet, aber eine andere Aktivität und ein anderes Erlebnis in der mbox 3 rdpartyid gespeichert sind, wird nach der Anmeldung dieses Besuchers der mbox 3 rdpartyid-Vorgang und -erlebnis abgelegt.

| PCID (nicht angemeldet) | mbox 3 rdpartyid (angemeldet) | Zusammengeführt und in der mbox 3 rdpartyid gespeichert |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Aktivität 1, Erlebnis A | Aktivität 1, Erlebnis B | Aktivität 1, Erlebnis B |
| Aktivität 1 |  | Aktivität 1 |

Wenn der Besucher sich anmeldet, wird das zusammengeführte Profil beibehalten.

>[!NOTE]
>
>[!DNL Adobe Analytics] Ziele werden nicht verfolgt, wenn sich die [!DNL Adobe Experience Cloud] ID (MID) ändert (z. B. ändert sich der Besucher von Geräten), auch wenn das [!DNL Target] Profil möglicherweise auf der Grundlage der mbox 3 rdpartyid zusammengeführt wird und trotzdem über Aktivitätsinformationen verfügt. Für Besucher, die mit derselben MID identifiziert werden (diejenigen, die mit demselben Gerät auf die Seite zugreifen), sollte [!DNL Analytics for Target] (A4T) wie erwartet funktionieren.

## Zu beachten {#considerations}

Wenn Ihre Seite mehrere mboxes enthält und nur einige verwenden 3 rdpartyid, verfügt Target nicht über ein separates Besucherprofil/einen separaten Kontext für jede Besucheranforderung. Der 3 rdpartyid-Kontext hat Vorrang vor dem PCID-Kontext. Es reicht aus, dass eine mbox 3 rdpartyid weiterleitet, damit der Kontext Vorrang vor PCID erhält.

Angenommen, ein Besucher greift auf eine Seite zu, bevor er sich anmeldet und ein Erlebnis sieht. Die globale Mbox verwendet nicht 3 rdpartyid. Nach der Anmeldung sieht der Besucher eines von drei Erlebnissen mit untergeordneten mboxes, von denen einige 3 rdpartyid verwenden. Der Besucher besucht verschiedene Seiten auf der Site und verwendet dann die Schaltfläche "Zurück" , um zur Hauptseite zurückzukehren, auf die zugegriffen wurde, bevor sich die Anmeldung erfolgt und ein anderes Erlebnis angezeigt wird. In diesem Szenario gab die globale Mbox nicht 3 rdpartyid an, aber eine oder mehrere der untergeordneten mboxes wurden aufgerufen. 3 Rdpartyid hat Vorrang vor PCID.
