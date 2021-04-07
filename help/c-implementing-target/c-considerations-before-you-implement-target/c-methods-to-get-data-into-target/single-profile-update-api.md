---
keywords: implementieren;Implementierung;Einrichten;Setup;Update eines einzelnen Profils
description: Daten mit der Single Profil Update API in die Zielgruppe laden
title: Wie erhalte ich Daten mithilfe der API für die Aktualisierung von Profilen in die Zielgruppe?
feature: Implementierung
role: Developer
translation-type: tm+mt
source-git-commit: e8c25685341319fea4381386cad1ce0c5b80face
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 45%

---

# Single-Profil-API

Fast identisch mit der Massen-Profil-Update-API, aber ein Besucher-Profil wird gleichzeitig aktualisiert, in einer Linie im API-Aufruf und nicht mit einer CSV-Datei.

## Format

Der Besucher muss über die Target-Werte mboxPC oder mboxThirdPartyId identifiziert werden. Die Experience Cloud ID (ECID) wird nicht unterstützt.

## Beispielhafte Anwendungsfälle

Sie möchten die Zielgruppe in Echtzeit aktualisieren, wenn ein Besucher eine Offline-Aktion ausführt. Zu den Aktionen gehören das Erreichen eines Call-Centers, die Finanzierung eines Kredits, die Verwendung einer Treuekarte im Geschäft, der Zugriff auf einen Kiosk usw.

## Vorteile der Methode

Keine Begrenzung der Anzahl der Profilattribute.

Profilattribute, die über die Website gesendet werden, können über die API aktualisiert werden und umgekehrt.

## Einschränkungen

Begrenzung auf 1.000.000 (1 Million) API-Aufrufe pro 24-Stunden-Zeitraum

Aktualisiert nur Profile. Kann kein Profil für einen potenziellen Benutzer erstellen, den Target noch nicht gesehen hat.

## Codebeispiele

GET und POST werden unterstützt.   `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

## Links zu relevanten Informationen

[Update von Profilen](https://developers.adobetarget.com/api/#updating-profiles)