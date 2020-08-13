---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Versionshinweise zum Java-SDK von Adobe Target.
title: Versionshinweise zum Java-SDK von Adobe Target.
feature: release notes
topic: Standard
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
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

Im folgenden Abschnitt finden Sie weitere Informationen zu Version 1.1.0 des Java SDK der Zielgruppe:

### Hinzugefügt:

* Unterstützung für die Proxy-Konfiguration hinzugefügt aufgrund eines Open-Source-Beitrags von @hisham-hassan.

## Version 1.0.1 (11. November 2019)

Im folgenden Abschnitt finden Sie weitere Informationen zu Version 1.0.1 des Java SDK der Zielgruppe:

### Fest

* Senden Sie zusätzliche Daten-IDs in einer Zielgruppe-Anforderung, selbst wenn kein Besucher-API-Cookie vorhanden ist.

## Version 1.0.0 (31. Oktober 2019)

Die folgenden Abschnitte enthalten weitere Informationen über Version 1.0.0 des Java SDK der Zielgruppe:

### Hinzugefügt:

* [API](https://developers.adobetarget.com/api/delivery-api/) -Unterstützung für Zielgruppe Ansicht Versand v1, einschließlich Seitenladevorgang und Ansicht-Vorabruf.
   * Volle Unterstützung für die Bereitstellung aller in Visual Experience Composer (VEC) erstellten Angebot.
* Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung bereits abgerufener Inhalte ermöglichen.
* Unterstützung für die Leistungsoptimierung bei Hybrid- [!DNL Target] Integrationen über `serverState`[!DNL Target] die Bereitstellung sowohl auf Server- als auch auf Client-Ebene.
   * Wir führen eine Einstellung ein, `serverState` die Erlebnisse enthält, die serverseitig abgerufen werden, sodass at.js v2.2+ keinen zusätzlichen Server-Aufruf zum Abrufen der Erlebnisse durchführt. Dieser Ansatz optimiert die Seitenladeleistung.
* Open Source auf GitHub als [Zielgruppe Java SDK](https://github.com/adobe/target-java-sdk).
* Validierung der Argumente der SDK-API-Methode.
* Es wurden README-, Samples- und Komponententests hinzugefügt.
* Es wurden CoC-, Beitragsrichtlinien-, PR- und Ausgabenvorlagen hinzugefügt.

