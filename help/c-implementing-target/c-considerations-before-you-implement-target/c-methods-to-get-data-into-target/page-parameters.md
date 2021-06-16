---
keywords: implementieren;implementieren;einrichten;Einrichtung;Seitenparameter
description: Rufen Sie Daten mithilfe von Seitenparametern in [!DNL Target] ab.
title: Wie erhalte ich Daten unter [!DNL Target] Verwendung von Seitenparametern?
feature: Implementierung
role: Developer
exl-id: a285eadc-b71e-49a8-9071-397ada283baf
source-git-commit: c91465cccc244d79b6540004237a5ce7156233bb
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 46%

---

# Seitenparameter

Seitenparameter (auch &quot;Mbox-Parameter&quot;genannt) sind Name/Wert-Paare, die direkt über den Seiten-Code übergeben werden und nicht im Besucherprofil zur zukünftigen Verwendung gespeichert werden.

Seitenparameter sind nützlich, um Seitendaten an Target zu senden, die nicht mit dem Profil des Besuchers gespeichert werden müssen, um sie für zukünftige Targeting-Anwendungen nutzen zu können. Diese Werte werden stattdessen verwendet, um die Seite oder die Aktion zu beschreiben, die der Benutzer auf der jeweiligen Seite ausgeführt hat.

## Format

Seitenparameter werden über einen Server-Aufruf als Name-Wert-Paar-Zeichenfolge an Target übergeben. Parameternamen und -werte sind anpassbar (obwohl es einige „reservierte Namen“ für spezifische Anwendungen gibt).

### Beispiele

* `page=productPage`

* `categoryId=homeLoans`

## Anwendungsbeispiele

* **Produktseiten**: Senden Sie Informationen über das angezeigte Produkt (so funktioniert Recommendations).
* **Bestelldetails**: Bestell-ID, orderTotal usw. zur Auftragserfassung senden
* **Kategorieaffinität:** kategorisierte Informationen an Target senden, um Kenntnisse über die Affinität des Benutzers zu bestimmten Site-Kategorien zu erhalten.
* **Daten von Drittanbietern:** Informationen aus Drittanbieter-Datenquellen, wie Wetter-Targeting-Anbieter, Kontodaten (z. B. DemandBase), demographische Daten (z. B. Experian) und mehr senden.

## Vorteile der Methode

Daten werden in Echtzeit an Target gesendet und können für denselben Server-Aufruf verwendet werden, für den die Daten eingehen.

## Einschränkungen

* Erfordert ein Seiten-Code-Update (direkt oder über ein Tag-Management-System).
* Wenn die Daten für die Zielgruppenbestimmung bei einem nachfolgenden Seiten-/Server-Aufruf verwendet werden müssen, müssen sie in ein Profilskript übersetzt werden.
* Abfragezeichenfolgen dürfen nur Zeichen des [IETF-Standards](https://www.ietf.org/rfc/rfc3986.txt) (Internet Engineering Task Force) enthalten .

   Zusätzlich zu den auf der IETF-Site erwähnten Zeichen erlaubt Target die folgenden Zeichen in Abfragezeichenfolgen:

   ```< > # % " { } | \ ^ [ ] ` ```

   Alle anderen Zeichen müssen URL-codiert sein. Der Standard gibt das folgende Format an ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ):

   ![](assets/ietf1.png)

   Hier auch die vollständige Liste:

   ![](assets/ietf2.png)

## Codebeispiele

targetPageParamsAll (hängt die Parameter an alle Mbox-Aufrufe auf der Seite an):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams (hängt die Parameter an die globale Mbox auf der Seite an):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

Parameter im mboxCreate-Code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

## Links zu relevanten Informationen

Recommendations: [Implementierung nach Seitentyp](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

Bestellbestätigung: [Konversions-Tracking](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

Kategorieaffinität: [Kategorieaffinität](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)
