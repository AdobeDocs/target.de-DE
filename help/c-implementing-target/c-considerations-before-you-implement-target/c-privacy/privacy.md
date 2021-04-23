---
keywords: Privatsphäre;IP-Adresse;Geosegmentation;Opt-out;Optout;Ausschluss;Datenschutz;Regierungsvorschriften;gdpr;ccpa
description: Erfahren Sie, wie Adobe [!DNL Target] die geltenden Datenschutzgesetze einhält, einschließlich der Erfassung und Bearbeitung von IP-Adressen und Abmeldeanweisungen.
title: 'Wie geht man mit Datenschutzproblemen um? [!DNL Target] '
feature: Datenschutz und Sicherheit
role: Developer
exl-id: fb632923-fa36-4553-88a6-f27860472eb6
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 73%

---

# Datenschutz

[!DNL Adobe Target] bietet Prozesse und Einstellungen, die Ihnen die Verwendung von unter Einhaltung der geltenden Datenschutzgesetze ermöglichen.[!DNL Target]

## Sammlung von IP-Adressen {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

Die IP-Adresse eines Besuchers Ihrer Website wird an das Adobe-Datenverarbeitungscenter übergeben. Abhängig von der Netzwerkkonfiguration des Besuchers entspricht die IP-Adresse nicht unbedingt der IP-Adresse des Computers des Besuchers. Bei der IP-Adresse kann es sich z. B. um die externe IP-Adresse einer Network Address Translation-(NAT-)Firewall, eines HTTP-Proxys oder eines Internet-Gateways handeln. Target speichert keine IP-Adressen oder personenbezogenen Informationen des Benutzers. IP-Adressen werden von Target nur während der Dauer der Sitzung verwendet (im Arbeitsspeicher, nie persistent).

## Ersetzen des letzten Oktetts der IP-Adressen {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe hat eine neue, in das Design integrierte Datenschutzeinstellung entwickelt, die durch Adobe Client Care für Adobe Target aktiviert werden kann. Wenn diese Einstellung aktiviert ist, wird das letzte 8-Bit-Zeichen (das Ende) der IP-Adresse ausgeblendet, sobald die IP-Adresse durch Adobe erfasst wird. Diese Anonymisierung wird vor jeder weiteren Verarbeitung der IP-Adresse durchgeführt, auch vor einer optionalen Geo-Suche für die IP-Adresse.

Wenn diese Funktion aktiviert ist, wird die IP-Adresse so stark anonymisiert, dass sie nicht mehr als persönliche Information identifiziert werden kann. Demzufolge kann Adobe Target in Ländern, die kein Erfassen persönlicher Informationen zulassen, unter Einhaltung der Datenschutzgesetze verwendet werden. Das Ermitteln von Information auf Stadtebene wird durch die Verschleierung der IP-Adresse wahrscheinlich merklich beeinträchtigt. Das Ermitteln von Informationen auf Regions- und Landesebene dürfte nur leicht beeinträchtigt sein.

Die folgenden Einstellungen sind verfügbar:

* Keine Verschleierung: Zielgruppe verdeckt keinen Teil der IP-Adresse.
* Letztes Oktett: Zielgruppe verbirgt das letzte Oktett der IP-Adresse.
* Vollständige IP: Zielgruppe blendet die gesamte IP-Adresse aus.

Zielgruppe empfängt die vollständige IP-Adresse und verschleiert sie (sofern auf Letztes Oktett oder Vollständige IP festgelegt) wie angegeben. Zielgruppe speichert dann die verschleierte IP-Adresse während der Sitzungsdauer im Speicher.

>[!NOTE]
>
>[Wenden Sie sich an Adobe Client ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Caret, um zu ermitteln, welche Einstellung Sie aktuell verwenden, oder um die IP-Verschleierungsfunktion zu aktivieren.

## GeoSegmentation {#section_BB69F96559BD44BDA4177537C4A5345A}

Wenn Sie das Austauschen des letzten 8-Bit-Zeichens der IP-Adresse aktivieren, können die verbleibenden Werte der IP-Adresse mithilfe von Berichten in Adobe Target analysiert werden. Wenn das letzte 8-Bit-Zeichen der IP-Adresse nicht verschleiert wurde, kann die vollständige IP-Adresse in Adobe Target analysiert werden. Sie können die GeoSegmentation-Funktion verwenden, um den Besucherstandort nach geografischer Region abzugrenzen. GeoSegmentation-Daten sind nur auf Ebene der Stadt oder der Postleitzahl granular und nicht auf individueller Ebene.

Wenn IP-Adressen vollständig verschleiert werden, stehen GeoSegmentation und Geo-Targeting nicht zur Verfügung.

## Ausschluss-Link {#section_E7A62B7B99C94B3A806CB262D16E27FC}

Sie können einen Ausschluss-Link zu Ihren Sites hinzufügen, um Besuchern zu ermöglichen, die Zählung über und Inhaltsbereitstellung auszuschließen.

1. Fügen Sie den folgenden Link zu Ihrer Site hinzu:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`
1. Ersetzen Sie den Text `clientcode` durch Ihren Empfehlungen-Client-Code, und fügen Sie den Text oder das Bild hinzu, das mit der Ausschluss-URL verknüpft werden soll.

Ein Besucher, der auf diesen Link klickt, wird während der Browser-Sitzung nicht in Mbox-Anforderungen einbezogen, bis er den Cookie löscht oder nach Ablauf von zwei Jahren (je nachdem, was zuerst eintritt). Dies funktioniert durch Einsetzen eines Cookies namens `disableClient` in der Domäne `clientcode.tt.omtrdc.net` für den Besucher.

Auch wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden, erfolgt der Ausschluss über ein Drittanbieter-Cookie. Falls der Client nur ein Erstanbieter-Cookie verwendet, prüft Target, ob ein Ausschluss-Cookie festgelegt ist.

## Vorschriften zur Privatsphäre und zum Datenschutz

Informationen zur Datenschutzverordnung (GDPR) der Europäischen Vereinigung, zum kalifornischen Verbraucherschutzgesetz (CCPA) und anderen internationalen Datenschutzvorschriften sowie zu deren Auswirkungen auf Ihr Unternehmen und Adobe Target finden Sie unter [Datenschutzbestimmungen und Datenschutzbestimmungen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md).
