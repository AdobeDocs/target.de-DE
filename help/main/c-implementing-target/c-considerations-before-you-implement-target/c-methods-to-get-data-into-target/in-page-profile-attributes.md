---
keywords: implementieren;implementieren;einrichten;Einrichtung;Seitenparameter
description: Daten abrufen [!DNL Target] Verwendung von Profilattributen innerhalb der Seite.
title: Wie erhalte ich Daten? [!DNL Target] Verwenden von Profilattributen in der Seite?
feature: Implementation
role: Developer
exl-id: c6000720-a862-4e9c-96a5-055963a79544
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 57%

---

# In-Page-Profilattribute

Profilattribute auf der Seite in [!DNL Adobe Target] (auch &quot;In-mbox-Profilattribute&quot;genannt) sind Name/Wert-Paare, die direkt über den Seiten-Code übergeben werden und im Profil des Besuchers zur zukünftigen Verwendung gespeichert werden.

Die Profilattribute auf der Seite erlauben es, benutzerspezifische Daten im Profil von Target zu speichern, um sie später für ein Targeting gezielt zu segmentieren.

## Format

Inpage-Profilattribute werden über einen Server-Aufruf als Name-Wert-Paar-Zeichenfolge mit dem Präfix „profile.“ vor dem Attributnamen an Target übergeben.

Attributnamen und -werte sind anpassbar (obwohl es einige „reservierte Namen“ für bestimmte Verwendungszwecke gibt).

### Beispiele

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

## Anwendungsbeispiele

* **Anmeldeinformationen:** nicht personenbezogene Daten, die auf dem Login des Benutzers basieren, an Target weitergeben. Diese Daten können Mitgliedsstatus, Bestellverlauf oder mehr sein.
* **Store-Info:** verfolgen, welcher Store der bevorzugte Standort dieses Benutzers ist.
* **Bisherige Interaktionen**: verfolgen, was der Benutzer zuvor auf der Site getan hat, um die künftige Personalisierung vorzubereiten.

## Vorteile der Methode

Daten werden in Echtzeit an Target gesendet und können für denselben Server-Aufruf verwendet werden, bei dem die Daten eingehen.

## Einschränkungen

Erfordert Seiten-Code-Updates (direkt oder über ein Tag-Management-System).

Attribute und Werte sind in Server-Aufrufen sichtbar, sodass ein Besucher die Werte sehen kann. Wenn Informationen wie Kreditbereiche oder andere potenziell private Informationen freigegeben werden, ist diese Methode möglicherweise nicht der beste Ansatz.

## Codebeispiele

targetPageParamsAll (hängt die Attribute an alle Mbox-Aufrufe auf der Seite an):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (hängt die Attribute an die globale Mbox auf der Seite an):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attribute im mboxCreate-Code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

## Links zu relevanten Informationen

[Profilattribute](/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Besucherprofil](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)
