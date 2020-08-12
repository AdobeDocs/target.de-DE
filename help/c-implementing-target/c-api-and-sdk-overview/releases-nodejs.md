---
keywords: at.js;sdk;node.js;release;updates;sdks;server side;serverside;server-side;nodejs
description: Versionshinweise zu Adobe Targets serverseitigen APIs.
title: Versionshinweise zum Adobe Target-SDK "Node.js".
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---


# Versionshinweise - Zielgruppe Node.js SDK

Versionshinweise zum [Adobe Target-SDK](https://github.com/adobe/target-nodejs-sdk)&quot;Node.js&quot;.

Mit dem Zielgruppe Node.js-SDK können Sie [!DNL Target] serverseitig bereitstellen.

Dieses Node.js-SDK unterstützt Sie bei der einfachen Integration [!DNL Target] mit anderen [!DNL Adobe Experience Cloud] Lösungen, z. B. [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]und [!DNL Adobe Audience Manager].

Das Node.js-SDK führt Best Practices ein und entfernt bei der Integration mit [!DNL Target] über unsere Versand-API Komplexität, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können.

Learn more about the Target Node.js SDK on the Adobe Tech Blog - [Open Sourcing the New Adobe Target Node.js SDK](https://medium.com/adobetech/open-sourcing-the-new-adobe-target-node-js-sdk-b6feafd828bc).

## Version 1.0.0 (October 9, 2019)

The following sections provide more information about version 1.0.0 of the Target Node.js SDK:

### Hinzugefügt:

* Target View Delivery v1 API support, including Page Load and View prefetch.
* Volle Unterstützung für die Bereitstellung aller im Visual Experience Composer (VEC) erstellten Angebot.
* Unterstützung für Vorab-Abruf und Benachrichtigungen zur Leistungsoptimierung durch Zwischenspeicherung vorab abgerufener Inhalte.
* Unterstützung für die Leistungsoptimierung bei Hybrid- [!DNL Target] Integrationen, `serverState` wenn sowohl serverseitig als auch clientseitig bereitgestellt [!DNL Target] wird.

   Wir führen eine Einstellung ein, `serverState` die Erlebnisse enthält, die serverseitig abgerufen werden, sodass at.js v2.2+ keinen zusätzlichen Server-Aufruf zum Abrufen der Erlebnisse durchführt. Dieser Ansatz optimiert die Seitenladeleistung.

* Open Source auf GitHub als [Zielgruppe Node.js SDK](https://github.com/adobe/target-nodejs-sdk).
* Neue API-Methode [](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientsendnotifications) sendNotifications() zum Senden von angezeigten/angeklickten Benachrichtigungen an [!DNL Target] Inhalte, die über [getOffers()](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers)im Voraus abgerufen werden.
* Vereinfachte Erstellung von Ansicht Versand-API-Anfragen mit automatischer Feldausfüllung mit Standardeinstellungen (z. B. `request.id``request.context`usw.).
* Validierung der Argumente der SDK-API-Methode.
* README, Beispiele und Komponententests wurden aktualisiert.
* Neuer CI-Fluss mit GitHub-Aktionen eingerichtet.
* CoC-, Beitragsrichtlinien-, PR- und Ausgabenvorlagen hinzugefügt

### Änderung von

* Projekt umbenannt in `target-nodejs-sdk`.
* Umfassende Umgestaltung, Ersetzen der Zielgruppe BatchMbox v2 API durch die Zielgruppe Ansicht Versand v1 API.
* [create() API-Methodenargumente](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientcreate) wurden geändert, wodurch redundante Verschachtelungen entfernt wurden (siehe Deklaration der alten Methode [hier](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)).
* [Die Argumente der getOffers()-API-Methode](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) wurden geändert (siehe Deklaration der alten Methode [hier](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)).
* Die `getTargetCookieName()` API-Methode wurde durch `TargetCookieName` Accessor ersetzt. Siehe [TargetClient-Dienstprogrammzugänge](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors).
* The `getTargetLocationHintCookieName()` API method has been replaced with `TargetLocationHintCookieName` accessor.  See [TargetClient utility accessors](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors).

### Entfernt

* API-Unterstützung für Zielgruppe BatchMbox v2.
* Die API-Methode [](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer) getOffer() wurde entfernt. Verwenden Sie stattdessen die API-Methode [](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) getOffers().

