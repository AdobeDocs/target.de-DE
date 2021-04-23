---
keywords: implementieren;Implementierung;Einrichtung;Einrichtung;Seitenparameter
description: Daten unter  [!DNL Target] mithilfe von Inpage-Profil-Attributen abrufen.
title: Wie erhalte ich Daten unter  [!DNL Target] Verwendung von In-Page-Profil-Attributen?
feature: Implementierung
role: Developer
exl-id: c6000720-a862-4e9c-96a5-055963a79544
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 56%

---

# Seitenspezifische Profil-Attribute

Seitenspezifische Profil-Attribute in [!DNL Adobe Target] (auch &quot;In-mbox-Profil-Attribute&quot;genannt) sind Namens-/Wertpaare, die direkt über den Seitencode weitergeleitet werden und im Profil des Besuchers für die zukünftige Verwendung gespeichert werden.

Die Profilattribute auf der Seite erlauben es, benutzerspezifische Daten im Profil von Target zu speichern, um sie später für ein Targeting gezielt zu segmentieren.

## Format

Inpage-Profilattribute werden über einen Server-Aufruf als Name-Wert-Paar-Zeichenfolge mit dem Präfix „profile.“ vor dem Attributnamen an Target übergeben.

Attributnamen und -werte sind anpassbar (obwohl es einige „reservierte Namen“ für bestimmte Verwendungszwecke gibt).

### Beispiele

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

## Verwendungsbeispiele

* **Anmeldeinformationen:** nicht personenbezogene Daten, die auf dem Login des Benutzers basieren, an Target weitergeben. Diese Daten können Mitgliedsstatus, Bestellverlauf oder mehr sein.
* **Store-Info:** verfolgen, welcher Store der bevorzugte Standort dieses Benutzers ist.
* **Bisherige Interaktionen**: verfolgen, was der Benutzer zuvor auf der Site getan hat, um die künftige Personalisierung vorzubereiten.

## Vorteile der Methode

Daten werden in Echtzeit an die Zielgruppe gesendet und können für denselben Serveraufruf verwendet werden, für den die Daten eingehen.

## Einschränkungen

Erfordert Seiten-Code-Updates (direkt oder über ein Tag-Management-System).

Attribute und Werte sind in Server-Aufrufen sichtbar, sodass ein Besucher die Werte sehen kann. Bei der Freigabe von Informationen wie Kreditbereichen oder anderen potenziell privaten Informationen ist diese Methode möglicherweise nicht der beste Ansatz.

## Codebeispiele

targetPageParamsAll (hängt die Attribute an alle Mbox-Aufrufe auf der Seite an):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (hängt die Attribute an die globale Mbox auf der Seite an):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attribute im mboxCreate-Code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

## Links zu relevanten Informationen

[Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Besucherprofil](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)
