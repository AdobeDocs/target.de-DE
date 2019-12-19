---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Versionshinweise zum Java-SDK von Adobe Target.
title: Versionshinweise zum Java-SDK von Adobe Target.
topic: Standard
translation-type: tm+mt
source-git-commit: 6b49e4fb6c92da023678c1f27823458229d21711

---


# Versionshinweise - Target Java SDK

Versionshinweise zum Java-SDK für [Target](https://github.com/adobe/target-java-sdk).

Mit dem [!DNL Target] Java-SDK können Sie [!DNL Target] serverseitig bereitstellen. Mit diesem Java-SDK können Sie problemlos [!DNL Target] mit anderen [!DNL Adobe Experience Cloud] Lösungen wie dem [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]und [!DNL Adobe Audience Manager]dem

Das Java-SDK führt Best Practices ein und entfernt bei der Integration mit [!DNL Target] unserer Bereitstellungs-API Komplexitäten, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können.

Weitere Informationen zum Target Java SDK finden Sie im Adobe Tech Blog - [Serverseitige Optimierung mit dem neuen Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).

## Version 1.1.0 (16. Dezember 2019)

Im folgenden Abschnitt finden Sie weitere Informationen zur Version 1.1.0 des Target Java SDK:

### Hinzugefügt:

* Unterstützung für die Proxy-Konfiguration hinzugefügt aufgrund eines Open-Source-Beitrags von @hisham-hassan.

## Version 1.0.1 (11. November 2019)

Im folgenden Abschnitt finden Sie weitere Informationen zur Version 1.0.1 des Target Java SDK:

### Fest

* Senden Sie zusätzliche Daten-IDs in einer Target-Anforderung, selbst wenn kein Besucher-API-Cookie vorhanden ist.

## Version 1.0.0 (31. Oktober 2019)

Die folgenden Abschnitte enthalten weitere Informationen zur Version 1.0.0 des Target Java SDK:

### Hinzugefügt:

* [Unterstützung der Target View Delivery v1 API](https://developers.adobetarget.com/api/delivery-api/) , einschließlich Seitenladevorgang und Vorabruf anzeigen.
   * Volle Unterstützung für die Bereitstellung aller in Visual Experience Composer (VEC) erstellten Angebotstypen.
* Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung bereits abgerufener Inhalte ermöglichen.
* Unterstützung zur Leistungsoptimierung bei Hybrid- [!DNL Target] Integrationen über `serverState`[!DNL Target] die Bereitstellung sowohl auf Server- als auch auf Client-Ebene.
   * Wir führen eine Einstellung ein, `serverState` die Erlebnisse enthält, die serverseitig abgerufen werden, sodass at.js v2.2+ keinen zusätzlichen Server-Aufruf zum Abrufen der Erlebnisse durchführt. Dieser Ansatz optimiert die Seitenladeleistung.
* Open Source auf GitHub als [Target Java SDK](https://github.com/adobe/target-java-sdk).
* Validierung der Argumente der SDK-API-Methode.
* README-, Samples- und Komponententests wurden hinzugefügt.
* Es wurden CoC-, Beitragsrichtlinien-, PR- und Ausgabenvorlagen hinzugefügt.

