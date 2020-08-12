---
keywords: implement;implementing;setting up;setup;page parameter;tomcat;url encoded;in-page profile attribute;mbox parameter;in-page profile attributes;script profile attribute;bulk profile update API;single file update API;customer attributes;data providers;dataprovider;data provider
description: Informationen über die verschiedenen Verfahren, die Sie verwenden können, um Daten in Target zu übertragen, einschließlich der Seitenparameter, der Profilattribute innerhalb der Seite, der Skriptprofilattribute, der Datenanbieter, der Bulk-Profilupdate-API, der Single-Profilupdate-API und der Kundenattribute.
title: Verfahren für die Datenübernahme in Target
feature: null
subtopic: Getting Started
topic: Standard
uuid: a6d64e39-6cdc-49fe-afe5-ecf7dcacf97d
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 97%

---


# Verfahren für die Datenübernahme in Target{#methods-to-get-data-into-target}

Informationen über die verschiedenen Verfahren, die Sie verwenden können, um Daten in Target zu übertragen, einschließlich der Seitenparameter, der Profilattribute innerhalb der Seite, der Skriptprofilattribute, der Datenanbieter, der Bulk-Profilupdate-API, der Single-Profilupdate-API und der Kundenattribute.

## Seitenparameter (auch „mbox-Parameter“ genannt){#section_5A297816173C4FE48DC4FE03860CB42B}

Seitenparameter sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden.

Die Seitenparameter sind nützlich, um zusätzliche Seitendaten an Target zu senden, die nicht mit dem Profil des Besuchers gespeichert werden müssen, um sie für zukünftige Targeting-Anwendungen zu verwenden. Diese Werte werden stattdessen verwendet, um die Seite oder die Aktion zu beschreiben, die der Benutzer auf der jeweiligen Seite ausgeführt hat.

### Format

Seitenparameter werden über einen Server-Aufruf als Name-Wert-Paar-Zeichenfolge an Target übergeben. Parameternamen und -werte sind anpassbar (obwohl es einige „reservierte Namen“ für spezifische Anwendungen gibt).

Beispiele:

* `page=productPage`

* `categoryId=homeLoans`

### Beispielhafte Anwendungsfälle

**Produktseiten:** Informationen über das angezeigte Produkt senden (so funktioniert Recommendations).

**Bestelldetails:** Bestell-ID, orderTotal usw. zur Auftragserfassung senden.

**Kategorieaffinität:** kategorisierte Informationen an Target senden, um Kenntnisse über die Affinität des Benutzers zu bestimmten Site-Kategorien zu erhalten.

**Daten von Drittanbietern:** Informationen aus Drittanbieter-Datenquellen, wie Wetter-Targeting-Anbieter, Kontodaten (z. B. DemandBase), demographische Daten (z. B. Experian) und mehr senden.

### Vorteile der Methode

Die Daten werden in Echtzeit an Target gesendet und können bei demselben Server-Aufruf verwendet werden, bei dem sie eingehen.

### Einschränkungen

* Erfordert ein Seiten-Code-Update (direkt oder über ein Tag-Management-System).
* Wenn die Daten für das Targeting bei einem nachfolgenden Seiten-/Server-Aufruf verwendet werden sollen, müssen sie in ein Profilskript übersetzt werden.
* Abfragezeichenfolgen dürfen nur Zeichen des [IETF-Standards](https://www.ietf.org/rfc/rfc3986.txt) (Internet Engineering Task Force) enthalten .

   Zusätzlich zu den auf der IETF-Site aufgeführten Zeichen erlaubt Target auch folgende Zeichen in Abfragezeichenfolgen:

   `&lt; > # % &quot; { } | \\ ^ \[\] \``

   Alle anderen Zeichen müssen URL-codiert sein. The standard specifies the following format ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ), as illustrated below:

   ![](assets/ietf1.png)

   Hier auch die vollständige Liste:

   ![](assets/ietf2.png)

### Beispiele für Codes

targetPageParamsAll (hängt die Parameter an alle Mbox-Aufrufe auf der Seite an):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams (hängt die Parameter an die globale Mbox auf der Seite an):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

Parameter im mboxCreate-Code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

### Links zu relevanten Informationen

Recommendations: [Implementierung nach Seitentyp](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

Bestellbestätigung: [Konversions-Tracking](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

Kategorieaffinität: [Kategorieaffinität](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)

## Profilattribute auf der Seite (auch „In-mbox-Profilattribute“ genannt) {#section_57E1C161AA7B444689B40B6F459302B6}

Inpage-Profilattribute sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben werden und im Profil des Besuchers für die zukünftige Verwendung gespeichert werden.

Die Profilattribute auf der Seite erlauben es, benutzerspezifische Daten im Profil von Target zu speichern, um sie später für ein Targeting gezielt zu segmentieren.

### Format

Inpage-Profilattribute werden über einen Server-Aufruf als Name-Wert-Paar-Zeichenfolge mit dem Präfix „profile.“ vor dem Attributnamen an Target übergeben.

Attributnamen und -werte sind anpassbar (obwohl es einige „reservierte Namen“ für bestimmte Verwendungszwecke gibt).

Beispiele:

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

### Beispielhafte Anwendungsfälle

**Anmeldeinformationen:** nicht personenbezogene Daten, die auf dem Login des Benutzers basieren, an Target weitergeben. Dies kann z. B. der Status der Mitgliedschaft, der Bestellverlauf oder mehr sein.

**Store-Info:** verfolgen, welcher Store der bevorzugte Standort dieses Benutzers ist.

**Bisherige Interaktionen**: verfolgen, was der Benutzer zuvor auf der Site getan hat, um die künftige Personalisierung vorzubereiten.

### Vorteile der Methode

Die Daten werden in Echtzeit an Target gesendet und können bei demselben Server-Aufruf verwendet werden, bei dem sie eingehen.

### Einschränkungen

Erfordert Seiten-Code-Updates (direkt oder über ein Tag-Management-System).

Attribute und Werte sind in Server-Aufrufen sichtbar, sodass ein Besucher die Werte sehen kann. Wenn Sie Informationen wie Kreditrahmen oder andere potenziell private Informationen weitergeben, ist dies möglicherweise nicht der beste Weg.

### Beispiele für Codes

targetPageParamsAll (hängt die Attribute an alle Mbox-Aufrufe auf der Seite an):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (hängt die Attribute an die globale Mbox auf der Seite an):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attribute im mboxCreate-Code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

### Links zu relevanten Informationen

[Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Besucherprofil](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)

## Skript-Profilattribute {#section_3E27B58C841448C38BDDCFE943984F8D}

Skript-Profilattribute sind Name-Wert-Paare, die in der Target-Anwendung definiert sind. Der Wert wird durch die Ausführung eines JavaScript-Snippets auf dem Target-Server über den Server-Aufruf ermittelt.

Benutzer schreiben kleine Code-Snippets, die pro Mbox-Aufruf ausgeführt werden, bevor ein Besucher für eine Zielgruppenmitgliedschaft und -aktivität ausgewertet wird.

### Format

Skript-Profilattribute werden im Abschnitt „Zielgruppen“ von Target erstellt. Jeder Attributname ist gültig und der Wert ist das Ergebnis einer JavaScript-Funktion, die vom Target-Benutzer geschrieben wurde. Den Attributnamen wird in Target automatisch ein „user. “ vorangestellt, um sie von den Profilattributen innerhalb der Seite unterscheiden zu können.

Das Code-Snippet ist in der Sprache Rhino JS geschrieben und kann Token und andere Werte referenzieren.

### Beispielhafte Anwendungsfälle

**Warenkorbabbruch:** das Profilskript auf 1 setzen, wenn der Besucher den Einkaufswagen erreicht. Wenn der Besucher einen Kauf durchführt, setzen Sie ihn auf 0 zurück. Ist der Wert =1, dann hat der Besucher einen Artikel im Warenkorb.

**Besuchsanzahl:** bei jedem neuen Besuch die Anzahl um 1 erhöhen, um zu verfolgen, wie oft ein Besucher zur Site zurückkehrt.

### Vorteile der Methode

Keine Seiten-Code-Updates erforderlich.

Wird vor Entscheidungen zu Zielgruppen- und Aktivitätsmitgliedschaften ausgeführt, sodass diese Skript-Profilattribute die Mitgliedschaft bei einem einzelnen Server-Aufruf beeinflussen können.

Kann sehr robust sein. Pro Skript können bis zu 2.000 Befehle ausgeführt werden.

### Einschränkungen

JavaScript-Kenntnisse erforderlich.

Die Ausführungsreihenfolge von Profilskripten kann nicht garantiert werden, sodass sie sich nicht aufeinander verlassen können.

Kann schwierig zu debuggen sein.

### Beispiele für Codes

Profilskripte sind ziemlich flexibel:

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### Links zu relevanten Informationen

[Profilskriptattribute](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)

## Datenanbieter {#section_14FF3BE20DAA42369E4812D8D50FBDAE}

Mit der Datenanbieterfunktion können Sie Dateien von Drittanbietern einfach an Target übergeben.

Hinweis: Datenanbieter erfordert at.js 1.3 oder höher.

### Format

Die Einstellung `window.targetGlobalSettings.dataProviders` entspricht einer Reihe von Datenanbietern.

Weitere Informationen zur Struktur für die einzelnen Datenanbieter finden Sie unter [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

### Beispielhafte Anwendungsfälle

Erfassen Sie Daten von Drittanbietern, wie z. B. einem Wetterdienst, einem DMP oder sogar Ihrem eigenen Webservice. Anschließend können Sie diese Daten zur Erstellung von Zielgruppen und zielgerichtetem Inhalt und zur Aufwertung des Benutzerprofils verwenden.

### Vorteile der Methode

Mit dieser Einstellung können Kunden Daten von Drittdatenanbietern sammeln, beispielsweise Demandbase, BlueKai und benutzerspezifische Services, und die Daten an Target als Mbox-Parameter in der globalen Mbox-Anfrage weitergeben.

Sie unterstützt die Sammlung von Daten von mehreren Anbietern über asynchrone und synchrone Anfragen.

Mit diesem Ansatz ist es ein Leichtes, Flicker- oder Standardinhalte zu verwalten und gleichzeitig unabhängige Timeouts für die einzelnen Anbieter festzulegen, um die Auswirkungen auf die Seitenleistung zu begrenzen

### Einschränkungen

Wenn die `window.targetGlobalSettings.dataProviders` hinzugefügten Datenanbieter asynchron sind, werden sie parallel ausgeführt. Die Besucher-API-Anfrage wird parallel mit den `window.targetGlobalSettings.dataProviders` hinzugefügten Funktionen ausgeführt, um eine minimale Wartezeit zu ermöglichen.

at.js versucht nicht, die Daten zwischenzuspeichern. Wenn der Datenanbieter die Daten nur einmal abruft, sollte er sicherstellen, dass die Daten zwischengespeichert werden, und die Cachedaten für den zweiten Aufruf verarbeiten, wenn die Anbieterfunktion aufgerufen wird.

### Beispiele für Codes

Unter [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) finden Sie verschiedene Beispiele.

### Links zu relevanten Informationen

Dokumentation: [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

### Schulungsvideos:

* [Verwenden von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Implementieren von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-technical-video-implement.html)

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

Fast identisch mit der Bulk-Profil-Update-API, aber ein Besucherprofil wird gleichzeitig mit einem API-Aufruf anstatt mit einer CSV-Datei aktualisiert.

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

GET und POST werden unterstützt.  `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

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

Details can be found in [Create a customer attribute source and upload the data file](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html).

### Links zu relevanten Informationen

[Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html).