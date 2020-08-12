---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Release notes related to Adobe Target's Java SDK.
title: Release notes related to Adobe Target's Java SDK.
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Versionshinweise - Zielgruppe Java SDK

Versionshinweise zum Java-SDK der [Zielgruppe](https://github.com/adobe/target-java-sdk).

Mit dem [!DNL Target] Java-SDK können Sie [!DNL Target] serverseitig bereitstellen. Mit diesem Java-SDK können Sie problemlos [!DNL Target] mit anderen [!DNL Adobe Experience Cloud] Lösungen wie dem [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]und [!DNL Adobe Audience Manager]dem

Das Java-SDK führt Best Practices ein und entfernt bei der Integration mit [!DNL Target] über unsere Versand-API Komplexitäten, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können.

Erfahren Sie mehr über die Zielgruppe Java SDK auf der Adobe Tech Blog - [Serverseitige Optimierung mit der neuen Zielgruppe Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).

## Version 1.1.0 (16. Dezember 2019)

The following section provides more information about version 1.1.0 of the Target Java SDK:

### Hinzugefügt:

* Unterstützung für die Proxy-Konfiguration hinzugefügt aufgrund eines Open-Source-Beitrags von @hisham-hassan.

## Version 1.0.1 (November 11, 2019)

Im folgenden Abschnitt finden Sie weitere Informationen zu Version 1.0.1 des Java SDK der Zielgruppe:

### Fest

* Send supplemental data ID in a Target request even when there is no Visitor API cookie present.

## Version 1.0.0 (31. Oktober 2019)

The following sections provide more information about version 1.0.0 of the Target Java SDK:

### Hinzugefügt:

* [API](https://developers.adobetarget.com/api/delivery-api/) -Unterstützung für Zielgruppe Ansicht Versand v1, einschließlich Seitenladevorgang und Ansicht-Vorabruf.
   * Volle Unterstützung für die Bereitstellung aller in Visual Experience Composer (VEC) erstellten Angebot.
* Support for prefetching and notifications that allows for performance optimization by caching prefetched content.
* Support for optimizing performance in hybrid [!DNL Target] integrations via `serverState`, when [!DNL Target] is deployed both on the server-side and on the client-side.
   * Wir führen eine Einstellung ein, `serverState` die Erlebnisse enthält, die serverseitig abgerufen werden, sodass at.js v2.2+ keinen zusätzlichen Server-Aufruf zum Abrufen der Erlebnisse durchführt. Dieser Ansatz optimiert die Seitenladeleistung.
* Open sourced on GitHub as [Target Java SDK](https://github.com/adobe/target-java-sdk).
* Validation of SDK API method arguments.
* Es wurden README-, Samples- und Komponententests hinzugefügt.
* Es wurden CoC-, Beitragsrichtlinien-, PR- und Ausgabenvorlagen hinzugefügt.

