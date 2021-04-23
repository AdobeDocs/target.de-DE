---
keywords: implementieren;Implementierung;Einrichten;Setup;Update eines einzelnen Profils
description: 'Daten können Sie mit der Single Profil Update API abrufen. [!DNL Target] '
title: 'Wie erhalte ich Daten mit der API für die Aktualisierung von einzelnen Profilen? [!DNL Target] '
feature: Implementierung
role: Developer
exl-id: 8331866c-0b84-4d08-83b4-f7f82c67cd21
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '193'
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
