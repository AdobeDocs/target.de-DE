---
keywords: Datenschutz;IP-Adresse;Geosegmentation;Opt-out;Optout;opt out;Datenschutz;gesetzliche Bestimmungen;DSGVO;ccpa
description: Erfahren Sie, wie Adobe  [!DNL Target]  die geltenden Datenschutzgesetze, einschließlich jener zur Erfassung und Verarbeitung von IP-Adressen, und die Bestimmungen zum Opt-out erfüllt.
title: Wie handhabt  [!DNL Target]  den Datenschutz?
feature: Privacy & Security
role: Developer
exl-id: fb632923-fa36-4553-88a6-f27860472eb6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: ht
source-wordcount: '738'
ht-degree: 100%

---

# Datenschutz

[!DNL Adobe Target] verfügt über Prozesse und Einstellungen, die es Ihnen ermöglicht, [!DNL Target] gemäß den geltenden Datenschutzgesetzen zu verwenden.

## Erfassung von Funktionsnutzungsdaten

Einzelne Funktionsnutzungsdaten werden für interne [!DNL Adobe]-Zwecke gesammelt, um zu ermitteln, ob [!DNL Target]-Funktionen wie gewünscht funktionieren oder um Funktionen zu identifizieren, die nur mäßig genutzt werden. Es werden verschiedene Latenzwerte erfasst, um Leistungsproblemen vorzubeugen. Personenbezogene Daten werden nicht erfasst.

Sie können die Erfassung der Nutzungsdaten in unseren SDKs deaktivieren, indem Sie `telemetryEnabled` in den Client-Initialisierungsoptionen auf „false“ setzen. Weitere Informationen finden Sie unter [telemetryEnabled in targetGlobalSettings](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#telemetry).

## Erfassen von IP-Adressen {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

Die IP-Adresse eines Besuchers Ihrer Website wird an das Adobe-Datenverarbeitungscenter übergeben. Abhängig von der Netzwerkkonfiguration des Besuchers entspricht die IP-Adresse nicht unbedingt der IP-Adresse des Computers des Besuchers. Bei der IP-Adresse kann es sich z. B. um die externe IP-Adresse einer Network Address Translation-(NAT-)Firewall, eines HTTP-Proxys oder eines Internet-Gateways handeln. Target speichert keine IP-Adressen oder personenbezogenen Informationen des Benutzers. IP-Adressen werden von Target nur während einer Sitzung verwendet (im Arbeitsspeicher, nie persistent).

## Ersetzen des letzten Oktetts von IP-Adressen {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe hat eine neue, in das Design integrierte Datenschutzeinstellung entwickelt, die durch Adobe Client Care für Adobe Target aktiviert werden kann. Wenn diese Einstellung aktiviert ist, wird das letzte 8-Bit-Zeichen (das Ende) der IP-Adresse ausgeblendet, sobald die IP-Adresse von Adobe erfasst wird. Diese Anonymisierung wird vor jeder weiteren Verarbeitung der IP-Adresse durchgeführt, auch vor einer optionalen Geo-Suche der IP-Adresse.

Wenn diese Funktion aktiviert ist, wird die IP-Adresse so stark anonymisiert, dass sie nicht mehr als persönliche Information identifiziert werden kann. Demzufolge kann Adobe Target in Ländern, die kein Erfassen persönlicher Informationen zulassen, unter Einhaltung der Datenschutzgesetze verwendet werden. Das Ermitteln von Information auf Stadtebene wird durch die Verschleierung der IP-Adresse wahrscheinlich merklich beeinträchtigt. Das Ermitteln von Informationen auf Regions- und Landesebene dürfte nur leicht beeinträchtigt sein.

Die folgenden Einstellungen sind verfügbar:

* Keine Verschleierung: Target blendet keinen Teil der IP-Adresse aus.
* Letztes Oktett: Target blendet das letzte Oktett der IP-Adresse aus.
* Vollständige IP-Adresse: Target blendet die gesamte IP-Adresse aus.

Target erhält die vollständige IP-Adresse und verschleiert sie entsprechend der Einstellung (sofern „Letztes Oktett“ oder „Vollständige IP“ ausgewählt ist). Target bewahrt dann die verschleierte IP-Adresse während der Sitzung im Speicher auf.

>[!NOTE]
>
>[Kontaktieren Sie die Adobe-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um festzustellen, welche Einstellung Sie aktuell verwenden, oder um die IP-Verschleierungsfunktion zu aktivieren.

## GeoSegmentation {#section_BB69F96559BD44BDA4177537C4A5345A}

Wenn Sie das Austauschen des letzten 8-Bit-Zeichens der IP-Adresse aktivieren, können die verbleibenden Werte der IP-Adresse mithilfe von Berichten in Adobe Target analysiert werden. Wenn das letzte 8-Bit-Zeichen der IP-Adresse nicht verschleiert wurde, kann die vollständige IP-Adresse in Adobe Target analysiert werden. Sie können die GeoSegmentation-Funktion verwenden, um den Besucherstandort nach geografischer Region abzugrenzen. GeoSegmentation-Daten sind nur auf Ebene der Stadt oder der Postleitzahl granular und nicht auf individueller Ebene.

Wenn IP-Adressen vollständig verschleiert werden, stehen GeoSegmentation und Geo-Targeting nicht zur Verfügung.

## Ausschluss-Link {#section_E7A62B7B99C94B3A806CB262D16E27FC}

Sie können einen Ausschluss-Link zu Ihren Sites hinzufügen, um Besuchern zu ermöglichen, die Zählung über und Inhaltsbereitstellung auszuschließen.

1. Fügen Sie den folgenden Link zu Ihrer Site hinzu:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`

1. (Abhängig von gewissen Voraussetzungen) Wenn Sie CNAME verwenden, sollte der Link den Parameter „client=`clientcode`“ enthalten, z. B.: https://my.cname.domain/optout?client=clientcode

1. Ersetzen Sie `clientcode` durch Ihren Client-Code, und fügen Sie den Text oder das Bild hinzu, das mit der Ausschluss-URL verknüpft werden soll.

Ein Besucher, der auf diesen Link klickt, wird während der Browser-Sitzung nicht in Mbox-Anforderungen einbezogen, bis er den Cookie löscht oder nach Ablauf von zwei Jahren (je nachdem, was zuerst eintritt). Dies funktioniert durch Einsetzen eines Cookies namens `disableClient` in der Domain `clientcode.tt.omtrdc.net` für den Besucher.

Auch wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden, erfolgt der Ausschluss über ein Drittanbieter-Cookie. Falls der Client nur ein Erstanbieter-Cookie verwendet, prüft Target, ob ein Ausschluss-Cookie festgelegt ist.

## Datenschutz und Datenschutzvorschriften

Informationen über die Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, den California Consumer Privacy Act (CCPA) sowie andere internationale Datenschutzbestimmungen und wie sich diese Vorschriften auf Ihr Unternehmen und Adobe Target auswirken, finden Sie unter [Datenschutz und Datenschutzvorschriften](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md).
