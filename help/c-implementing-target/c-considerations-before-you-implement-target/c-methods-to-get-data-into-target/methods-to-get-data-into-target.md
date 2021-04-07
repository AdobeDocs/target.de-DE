---
keywords: implementieren;Implementierung;einrichten;Einrichtung;Seitenparameter;Tomcat;URL-encoded;In-page-Profilattribut;Mbox-Parameter;In-page-Profilattribute;Skript-Profilattribut;Bulk-Profilupdate-API;API für einzelne Dateiaktualisierungen;Kundenattribute;Datenanbieter;Daten-Anbieter;Datenanbieter
description: Daten in Zielgruppe abrufen (Seitenparameter, Profil-Attribute, Skript-Profil-Attribute, Datenanbieter, Single- und Bulk-Profil-Update-APIs, Kundenattribute).
title: Wie erhalte ich Daten in die Zielgruppe?
feature: Implementierung
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: 70d4c5b4166081751246e867d90d43b67efa5469
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 86%

---

# Methodenübersicht

Informationen zu den verschiedenen Methoden, mit denen Sie Daten in [!DNL Adobe Target] abrufen können.

Zu den verfügbaren Methoden gehören:

| Methode | Details |
| --- | --- |
| [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br>Seitenparameter (auch „mbox-Parameter“ genannt) | Seitenparameter sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden.<br>Die Seitenparameter sind nützlich, um zusätzliche Seitendaten an Target zu senden, die nicht mit dem Profil des Besuchers gespeichert werden müssen, um sie für zukünftige Targeting-Anwendungen zu verwenden. Diese Werte werden stattdessen verwendet, um die Seite oder die Aktion zu beschreiben, die der Benutzer auf der jeweiligen Seite ausgeführt hat. |
| [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br>Profilattribute auf der Seite (auch „In-mbox-Profilattribute“ genannt) | Inpage-Profilattribute sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben werden und im Profil des Besuchers für die zukünftige Verwendung gespeichert werden.<br>Die Profilattribute auf der Seite erlauben es, benutzerspezifische Daten im Profil von Target zu speichern, um sie später für ein Targeting gezielt zu segmentieren. |
| [Skript-Profilattribute](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | Skript-Profilattribute sind Name-Wert-Paare, die in der Target-Anwendung definiert sind. Der Wert wird durch die Ausführung eines JavaScript-Snippets auf dem Target-Server über den Server-Aufruf ermittelt.<br>Benutzer schreiben kleine Code-Snippets, die pro Mbox-Aufruf ausgeführt werden, bevor ein Besucher für eine Zielgruppenmitgliedschaft und -aktivität ausgewertet wird. |
| [Datenanbieter](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | Datenanbieter sind eine Funktion, mit der Sie Daten von Drittanbietern einfach an die Zielgruppe weitergeben können. |
| Bulk-Profil-Update-API | Senden Sie über die API eine CSV-Datei an Target mit Aktualisierungen des Besucherprofils für viele Besucher. Jedes Besucherprofil kann mit mehreren In-Page-Profilattributen in einem Aufruf aktualisiert werden. |
| Single-Profil-API | Fast identisch mit der Massen-Profil-Update-API, aber ein Besucher-Profil wird gleichzeitig aktualisiert, in einer Linie im API-Aufruf und nicht mit einer CSV-Datei. |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. |







## Bulk-Profil-Update-API {#section_92AB4820A5624C669D9A1F1B6220D4FA}

Senden Sie über die API eine CSV-Datei an Target mit Aktualisierungen des Besucherprofils für viele Besucher. Jedes Besucherprofil kann mit mehreren In-Page-Profilattributen in einem Aufruf aktualisiert werden.

Diese Option ähnelt sehr stark den Kundenattributen, weist aber einige Unterschiede dazu auf:

* Kundenattribute verwenden einen FTP-Upload, während die Target Bulk-Profil-Update-API eine HTTP POST-API verwendet.
* Die Daten der Kundenattribute können mit Analytics geteilt werden. Bulk-Profil-Update ist nur in Target verwendbar.
* Kundenattribute unterstützen die Erstellung eines Profils für einen Benutzer, den Target noch nicht gesehen hat. Die Bulk-Profil-Update-API aktualisiert nur bestehende Target-Profile.
* Kundenattribute erfordern die Verwendung der Experience Cloud ID (ECID). Die Bulk-Profil-Update-API benötigt entweder die TNT ID oder die `mbox3rdPartyId`.
* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

### Format

Die CSV-Datei muss sich auf jeden Besucher über seine Target-PCID oder mboxThirdPartyId beziehen. Die Experience Cloud ID (ECID) wird nicht unterstützt. Alle Profilattribute/-werte werden über die API angelegt und aktualisiert. Details zum Format finden Sie in der API-Dokumentation.

### Beispielhafte Anwendungsfälle

Ihr CRM oder ein anderes internes System speichert wertvolle Daten über Ihre Besucher, die Sie konsistent in Target aktualisieren möchten, ohne die Profildaten in Ihrer Seitenimplementierung freizugeben.

### Vorteile der Methode

Keine Begrenzung der Anzahl der Profilattribute.

Profilattribute, die über die Website gesendet werden, können über die API aktualisiert werden und umgekehrt.

### Einschränkungen

Die Batch-Datei muss kleiner als 50 MB sein. Außerdem sollte die Gesamtzeilenzahl 500.000 Zeilen pro Upload nicht überschreiten.

Die Anzahl der Zeilen, die Sie über einen Zeitraum von 24 Stunden in nachfolgenden Batches hochladen können, ist unbegrenzt. Allerdings kann der Importverlauf während der Geschäftszeiten gedrosselt werden, um sicherzustellen, dass andere Prozesse effizient ablaufen.

Aufeinanderfolgende [V2-Batchupdate-Aufrufe](https://developers.adobetarget.com/api/#updating-profiles) ohne dazwischenliegende Mbox-Aufrufe für dieselben thirdPartyIds überschreiben die Eigenschaften, die im ersten Batchupdate-Aufruf aktualisiert wurden.

### Beispiele für Codes

Siehe [Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles).

### Links zu relevanten Informationen

[Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles)

## Single-Profil-API {#section_5D7A9DD7019F40E9AEF2F66F7F345A8D}

Fast identisch mit der Massen-Profil-Update-API, aber ein Besucher-Profil wird gleichzeitig aktualisiert, in einer Linie im API-Aufruf und nicht mit einer CSV-Datei.

### Format

Der Besucher muss über die Target-Werte mboxPC oder mboxThirdPartyId identifiziert werden. Die Experience Cloud ID (ECID) wird nicht unterstützt.

### Beispielhafte Anwendungsfälle

Sie möchten Target in Echtzeit aktualisieren, wenn ein Besucher eine Offline-Aktion durchführt, beispielsweise den Anruf beim Callcenter, die Finanzierung eines Darlehens, die Verwendung einer Kundenkarte in einem Geschäft, den Zutritt zu einem Kiosk usw.

### Vorteile der Methode

Keine Begrenzung der Anzahl der Profilattribute.

Profilattribute, die über die Website gesendet werden, können über die API aktualisiert werden und umgekehrt.

### Einschränkungen

Begrenzung auf 1.000.000 (1 Million) API-Aufrufe pro 24-Stunden-Zeitraum

Aktualisiert nur Profile. Kann kein Profil für einen potenziellen Benutzer erstellen, den Target noch nicht gesehen hat.

### Beispiele für Codes

GET und POST werden unterstützt.   `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

### Links zu relevanten Informationen

[Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles)

## Kundenattribute {#section_C47FC7980A9A4608BD1A5F0BD900FA70}

Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target.

Target Standard-Kunden können 5 Attribute nutzen, Target Premium-Kunden hingegen 200 Attribute.

### Format

Eine CSV-Datei mit Experience Cloud IDs (ECIDs) und Attributname-Wert-Paaren wird per FTP oder manuell in die Experience Cloud-UI hochgeladen.

### Beispielhafte Anwendungsfälle

Ihr CRM-System oder ein anderes internes System speichert wertvolle Informationen, die Sie mit der Experience Cloud von Adobe teilen möchten, einschließlich Target und Analytics.

### Vorteile der Methode

Das Hochladen von Kundendaten erzeugt in Target einen Profileintrag für diesen Besucher, auch wenn Target den Besucher noch nicht gesehen hat.

Dieselben Daten stehen automatisch in Target und Analytics zur Verfügung.

FTP kann eine einfachere Implementierungsmethode als API sein.

### Einschränkungen

Target Standard-Kunden können 5 Attribute nutzen, Target Premium-Kunden hingegen 200 Attribute.

Kann nur Werte über Kundenattribute aktualisieren, nicht auf der Seite.

Erfordert die Implementierung von Experience Cloud ID (ECID).

### Beispiele für Codes

Details finden Sie unter [Erstellen Sie eine Kundenattributquelle und laden Sie die Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) hoch.

### Links zu relevanten Informationen

[Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
