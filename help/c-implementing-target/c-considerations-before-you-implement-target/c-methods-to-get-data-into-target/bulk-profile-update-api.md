---
keywords: implementieren;Implementierung;Einrichten;Einrichten;Bulk-Profil-Aktualisierung
description: 'Daten werden mit der Bulk Profil Update API abgerufen. [!DNL Target] '
title: 'Wie kann ich Daten mit der Bulk Profil Update API abrufen? [!DNL Target] '
feature: Implementierung
role: Developer
exl-id: 068658fc-7082-425a-87c1-dd0de03cdc71
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 82%

---

# Bulk-Profil-Update-API

Senden Sie über die API eine CSV-Datei an [!DNL Adobe Target] mit Besucher-Profil-Updates für viele Besucher. Jedes Besucherprofil kann mit mehreren In-Page-Profilattributen in einem Aufruf aktualisiert werden.

Diese Option ähnelt den Kundenattributen mit einigen Unterschieden:

* Kundenattribute verwenden einen FTP-Upload, während die Target Bulk-Profil-Update-API eine HTTP POST-API verwendet.
* Die Daten der Kundenattribute können mit Analytics geteilt werden. Bulk-Profil-Update ist nur in Target verwendbar.
* Kundenattribute unterstützen die Erstellung eines Profils für einen Benutzer, den Target noch nicht gesehen hat. Die Bulk-Profil-Update-API aktualisiert nur bestehende Target-Profile.
* Kundenattribute erfordern die Verwendung der Experience Cloud ID (ECID). Die Bulk-Profil-Update-API benötigt entweder die TNT ID oder die `mbox3rdPartyId`.
* Folgende Zeichen können nicht gesendet werden `mbox3rdPartyID`: Plus-Zeichen (+) und Schrägstrich (/).

## Format

Die CSV-Datei muss sich auf jeden Besucher über seine Target-PCID oder mboxThirdPartyId beziehen. Die Experience Cloud ID (ECID) wird nicht unterstützt. Alle Profilattribute/-werte werden über die API angelegt und aktualisiert. Details zum Format finden Sie in der API-Dokumentation.

## Verwendungsbeispiele

Ihr CRM oder ein anderes internes System speichert wertvolle Daten über Ihre Besucher, die Sie konsistent in Target aktualisieren möchten, ohne die Profildaten in Ihrer Seitenimplementierung freizugeben.

## Vorteile der Methode

Keine Begrenzung der Anzahl der Profilattribute.

Profilattribute, die über die Website gesendet werden, können über die API aktualisiert werden und umgekehrt.

## Einschränkungen

Die Batch-Datei muss kleiner als 50 MB sein. Außerdem sollte die Gesamtzeilenzahl 500.000 Zeilen pro Upload nicht überschreiten.

Die Anzahl der Zeilen, die Sie über einen Zeitraum von 24 Stunden in nachfolgenden Batches hochladen können, ist unbegrenzt. Allerdings kann der Importverlauf während der Geschäftszeiten gedrosselt werden, um sicherzustellen, dass andere Prozesse effizient ablaufen.

Aufeinanderfolgende [V2-Batchupdate-Aufrufe](https://developers.adobetarget.com/api/#updating-profiles) ohne dazwischenliegende Mbox-Aufrufe für dieselben thirdPartyIds überschreiben die Eigenschaften, die im ersten Batchupdate-Aufruf aktualisiert wurden.

## Codebeispiele

Siehe [Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles).

### Links zu relevanten Informationen

[Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles)
