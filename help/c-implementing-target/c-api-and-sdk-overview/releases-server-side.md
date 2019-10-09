---
description: Versionshinweise zu den serverseitigen APIs und SDKs in Adobe Target
keywords: at.js;api;release;updates;apis;sdks;serverseitig;serverseitig;api;Auslieferungs-API
seo-description: Versionshinweise zu den serverseitigen APIs von Adobe Target.
seo-title: Versionshinweise zu den serverseitigen APIs von Adobe Target.
solution: Target
title: Versionshinweise - Target-serverseitige APIs
topic: Standard
translation-type: tm+mt
source-git-commit: 9fa095b910b85f244b626c34cacdf9f4a13a6929

---


# Versionshinweise - Target-serverseitige APIs

Versionshinweise zu den [!DNL Adobe Target] serverseitigen APIs.

## V1/Auslieferung (9. Oktober 2019)

Ein komplett neuer API-Endpunkt für die Bereitstellung wurde veröffentlicht.

* New [documentation](https://developers.adobetarget.com/api/delivery-api/) is available.
* Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.
* Rufen Sie VEC-erstellte Aktivitäten über die API ab.

   Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Teile Ihrer Seite, die personalisiert werden müssen, vorausgeblendet werden können. Auf diese Weise können Sie die Metrik[" ](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)Erster Inhaltsstoff"Ihrer Seite optimieren, die ein wichtiger KPI für Ihr Unternehmen ist, um einen hohen Wert im [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -System zu erzielen.

* Unterstützung für ein völlig neues Objekt namens "Ansichten", das für [Einzelseitenanwendungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) (SPAs) und [Mobilanwendungen](/help/c-target-mobile-app/target-mobile-app.md)verwendet wird.
* Unterstützung für das Vorab-Abrufen von Ansichten und Mboxes zur Leistungsoptimierung durch Zwischenspeicherung.
* Unterstützung für das Senden von Benachrichtigungen für vorab abgerufene Ansichten und Mboxes.

>[!IMPORTANT]
>
>Auf die Dokumentation[ zur alten ](https://developers.adobetarget.com/api/legacy-api/index.html)/v1/mbox und /v2/batchmbox-API kann weiterhin zugegriffen werden. Neue Funktionen werden jedoch in der neuen Auslieferungs-API entwickelt und nicht in die alten APIs zurückportiert.
