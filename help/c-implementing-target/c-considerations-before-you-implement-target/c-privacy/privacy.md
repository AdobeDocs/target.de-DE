---
keywords: privacy;ip address;geosegmentation;opt out;optout;opt-out;data privacy;government regulations;regulations
description: Adobe Target bietet Prozesse und Einstellungen, die Ihnen die Verwendung von Target unter Einhaltung der geltenden Datenschutzgesetze ermöglichen.
title: Datenschutz
subtopic: Getting Started
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: 78984fffbc43b6ada6c39a9395ebf247d6b8ef4f

---


# Datenschutz{#privacy}

Adobe Target bietet Prozesse und Einstellungen, die Ihnen die Verwendung von Target unter Einhaltung der geltenden Datenschutzgesetze ermöglichen.

## Sammlung von IP-Adressen {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

Die IP-Adresse eines Besuchers Ihrer Website wird an das Adobe-Datenverarbeitungscenter übergeben. Abhängig von der Netzwerkkonfiguration des Besuchers entspricht die IP-Adresse nicht unbedingt der IP-Adresse des Computers des Besuchers. Bei der IP-Adresse kann es sich z. B. um die externe IP-Adresse einer Network Address Translation-(NAT-)Firewall, eines HTTP-Proxys oder eines Internet-Gateways handeln. Target speichert keine IP-Adressen oder personenbezogenen Informationen des Benutzers. IP-Adressen werden von Target nur während der Dauer der Sitzung verwendet (im Arbeitsspeicher, nie persistent).

## Ersetzen des letzten Oktetts von IP-Adressen {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe hat eine neue, in das Design integrierte Datenschutzeinstellung entwickelt, die durch Adobe Client Care für Adobe Target aktiviert werden kann. Wenn diese Einstellung aktiviert ist, wird das letzte 8-Bit-Zeichen (das Ende) der IP-Adresse ausgeblendet, sobald die IP-Adresse durch Adobe erfasst wird. Diese Anonymisierung wird vor jeder weiteren Verarbeitung der IP-Adresse durchgeführt, auch vor einer optionalen Geo-Suche für die IP-Adresse.

Wenn diese Funktion aktiviert ist, wird die IP-Adresse so stark anonymisiert, dass sie nicht mehr als persönliche Information identifiziert werden kann. Demzufolge kann Adobe Target in Ländern, die kein Erfassen persönlicher Informationen zulassen, unter Einhaltung der Datenschutzgesetze verwendet werden. Das Ermitteln von Information auf Stadtebene wird durch die Verschleierung der IP-Adresse wahrscheinlich merklich beeinträchtigt. Das Ermitteln von Informationen auf Regions- und Landesebene dürfte nur leicht beeinträchtigt sein.

Die folgenden Einstellungen sind verfügbar:

* Keine Verschleierung: Target blendet keinen Teil der IP-Adresse aus.
* Letztes Oktett: Target blendet das letzte Oktett der IP-Adresse aus.
* Vollständige IP: Target blendet die gesamte IP-Adresse aus.

Target empfängt die vollständige IP-Adresse und verschleiert sie (sofern als Letztes Oktett oder Vollständige IP festgelegt) wie angegeben. Target speichert dann die verschleierte IP-Adresse für die Dauer der Sitzung im Speicher.

>[!NOTE]
>
>[Wenden Sie sich an den Adobe ClientCare](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) , um zu ermitteln, welche Einstellung Sie derzeit verwenden, oder um die IP-Verschleierungsfunktion zu aktivieren.

## GeoSegmentation {#section_BB69F96559BD44BDA4177537C4A5345A}

Wenn Sie das Austauschen des letzten 8-Bit-Zeichens der IP-Adresse aktivieren, können die verbleibenden Werte der IP-Adresse mithilfe von Berichten in Adobe Target analysiert werden. Wenn das letzte 8-Bit-Zeichen der IP-Adresse nicht verschleiert wurde, kann die vollständige IP-Adresse in Adobe Target analysiert werden. Sie können die GeoSegmentation-Funktion verwenden, um den Besucherstandort nach geografischer Region abzugrenzen. GeoSegmentation-Daten sind nur auf Ebene der Stadt oder der Postleitzahl granular und nicht auf individueller Ebene.

Wenn IP-Adressen vollständig verschleiert werden, stehen GeoSegmentation und Geo-Targeting nicht zur Verfügung.

## Opt-out link {#section_E7A62B7B99C94B3A806CB262D16E27FC}

Sie können einen Ausschluss-Link zu Ihren Sites hinzufügen, um Besuchern zu ermöglichen, die Zählung über und Inhaltsbereitstellung auszuschließen.

1. Fügen Sie den folgenden Link zu Ihrer Site hinzu:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`
1. Ersetzen Sie den Text `clientcode` durch Ihren Empfehlungen-Client-Code, und fügen Sie den Text oder das Bild hinzu, das mit der Ausschluss-URL verknüpft werden soll.

Ein Besucher, der auf diesen Link klickt, wird während der Browser-Sitzung nicht in Mbox-Anforderungen einbezogen, bis er den Cookie löscht oder nach Ablauf von zwei Jahren (je nachdem, was zuerst eintritt). Dies funktioniert durch Einsetzen eines Cookies namens `disableClient` in der Domäne `clientcode.tt.omtrdc.net` für den Besucher.

Auch wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden, erfolgt der Ausschluss über ein Drittanbieter-Cookie. Falls der Client nur ein Erstanbieter-Cookie verwendet, prüft Target, ob ein Ausschluss-Cookie festgelegt ist.

## Vorschriften zur Privatsphäre und zum Datenschutz

See [Privacy and data protection regulations](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) for information about the European Union&#39;s General Data Protection Regulation (GDPR), the California Consumer Privacy Act (CCPA), and other international privacy requirements, and how these regulations impact your organization and Adobe Target.
