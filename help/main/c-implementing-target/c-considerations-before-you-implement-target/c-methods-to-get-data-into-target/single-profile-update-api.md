---
keywords: implementieren;implementieren;einrichten;Setup;Single Profile Update
description: Daten abrufen [!DNL Target] Verwendung der API für die Aktualisierung einzelner Profile.
title: Wie erhalte ich Daten? [!DNL Target] Verwenden der Single-Profile-Update-API?
feature: Implementation
role: Developer
exl-id: 8331866c-0b84-4d08-83b4-f7f82c67cd21
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 46%

---

# API zur Aktualisierung von einzelnen Profilen

Fast identisch mit der Bulk Profile Update API, aber ein Besucherprofil wird gleichzeitig aktualisiert, und zwar in Übereinstimmung mit dem API-Aufruf und nicht mit einer CSV-Datei.

## Format

Der Besucher muss über die Target-Werte mboxPC oder mboxThirdPartyId identifiziert werden. Die Experience Cloud ID (ECID) wird nicht unterstützt.

## Beispielhafte Anwendungsfälle

Sie möchten Target in Echtzeit aktualisieren, wenn ein Besucher eine Offline-Aktion ausführt. Zu den Aktionen gehören das Erreichen eines Callcenters, die Finanzierung eines Darlehens, die Verwendung einer Treuekarte im Geschäft, der Zugriff auf einen Kiosk usw.

## Vorteile der Methode

Keine Begrenzung der Anzahl der Profilattribute.

Profilattribute, die über die Website gesendet werden, können über die API aktualisiert werden und umgekehrt.

## Einschränkungen

Begrenzung auf 1.000.000 (1 Million) API-Aufrufe pro 24-Stunden-Zeitraum

Aktualisiert nur Profile. Kann kein Profil für einen potenziellen Benutzer erstellen, den Target noch nicht gesehen hat.

## Codebeispiele

GET und POST werden unterstützt.  `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

>[!MORELIKETHIS]
>
>* [Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles)

