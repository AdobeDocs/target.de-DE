---
description: Versionshinweise zum Adobe Target-SDK Node.js
keywords: at.js;sdk;node.js;release;updates;sdks;serverseitig;serverseitig;nodejs
seo-description: Versionshinweise zu den serverseitigen APIs von Adobe Target.
seo-title: Versionshinweise zum Adobe Target-SDK Node.js.
solution: Target
title: Versionshinweise - SDK für Target Node.js
topic: Standard
translation-type: tm+mt
source-git-commit: 5f05f218e5fdea26827b86cb7fbea05ac6349014

---


# Versionshinweise - SDK für Target Node.js

Versionshinweise zum [Adobe Target-SDK](https://github.com/adobe/target-nodejs-sdk)"Node.js".

Mit dem SDK "Target Node.js"können Sie [!DNL Target] serverseitig bereitstellen.

Dieses Node.js-SDK unterstützt Sie bei der einfachen Integration [!DNL Target] mit anderen [!DNL Adobe Experience Cloud] Lösungen, z. B. [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]und [!DNL Adobe Audience Manager].

Das Node.js-SDK führt Best Practices ein und entfernt bei der Integration mit [!DNL Target] über unsere Bereitstellungs-API Komplexität, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können.

Weitere Informationen zum SDK "Target Node.js"finden Sie im Adobe Tech Blog - [Open Sourcing the New Adobe Target Node.js SDK](https://medium.com/adobetech/open-sourcing-the-new-adobe-target-node-js-sdk-b6feafd828bc).

## Version 1.0.0 (9. Oktober 2019)

Die folgenden Abschnitte enthalten weitere Informationen über Version 1.0.0 des SDK für Target Node.js:

### Hinzugefügt:

* Unterstützung der Target View Delivery v1 API, einschließlich Seitenladevorgang und Vorabruf anzeigen.
* Volle Unterstützung für die Bereitstellung aller im Visual Experience Composer (VEC) erstellten Angebotstypen.
* Unterstützung für Vorab-Abruf und Benachrichtigungen zur Leistungsoptimierung durch Zwischenspeicherung vorab abgerufener Inhalte.
* Unterstützung für die Leistungsoptimierung bei Hybrid- [!DNL Target] Integrationen, `serverState` wenn sowohl serverseitig als auch clientseitig bereitgestellt [!DNL Target] wird.

   Wir führen eine Einstellung ein, `serverState` die Erlebnisse enthält, die serverseitig abgerufen werden, sodass at.js v2.2+ keinen zusätzlichen Server-Aufruf zum Abrufen der Erlebnisse durchführt. Dieser Ansatz optimiert die Seitenladeleistung.

* Open Source auf GitHub als [Target Node.js SDK](https://github.com/adobe/target-nodejs-sdk).
* Neue API-Methode[ ](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientsendnotifications)sendNotifications() zum Senden von angezeigten/angeklickten Benachrichtigungen an [!DNL Target] Inhalte, die über [getOffers()](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers)im Voraus abgerufen werden.
* Vereinfachte API-Anforderungserstellung für Ansicht mit interner Feldautomatisierung mit Standardangaben (z. B. `request.id``request.context`usw.).
* Validierung der Argumente der SDK-API-Methode.
* README, Beispiele und Komponententests wurden aktualisiert.
* Neuer CI-Fluss mit GitHub-Aktionen eingerichtet.
* CoC-, Beitragsrichtlinien-, PR- und Ausgabenvorlagen hinzugefügt

### Änderung von

* Projekt umbenannt in `target-nodejs-sdk`.
* Umfassende Umgestaltung, Ersetzen der Target BatchMbox v2 API durch die Target View Delivery v1 API.
* [create() API-Methodenargumente](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientcreate) wurden geändert, wodurch redundante Verschachtelungen entfernt wurden (siehe Deklaration der alten Methode [hier](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)).
* [Die Argumente der getOffers()-API-Methode](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) wurden geändert (siehe Deklaration der alten Methode [hier](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)).
* Die `getTargetCookieName()` API-Methode wurde durch `TargetCookieName` Accessor ersetzt. Siehe [TargetClient-Dienstprogrammzugänge](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors).
* Die `getTargetLocationHintCookieName()` API-Methode wurde durch `TargetLocationHintCookieName` Accessor ersetzt.  Siehe [TargetClient-Dienstprogrammzugänge](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors).

### Entfernt

* API-Unterstützung für Target BatchMbox v2.
* Die API-Methode[ ](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer)getOffer() wurde entfernt. Verwenden Sie stattdessen die API-Methode[ ](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers)getOffers().

