---
keywords: at.js;api;release;updates;apis;sdks;server side;serverside;server-side;api;delivery api
description: Versionshinweise zu Adobe Targets serverseitigen APIs.
title: Release notes related to Adobe Target's server-side APIs.
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Release notes - Target server-side APIs

Versionshinweise zu den [Adobe Target-serverseitigen APIs](https://developers.adobetarget.com/api/delivery-api/).

## V1/Versand (9. Oktober 2019)

An entirely new delivery API endpoint has been released.

* New [documentation](https://developers.adobetarget.com/api/delivery-api/) is available.
* Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.
* Retrieve VEC-created activities via the API.

   Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Seitenabschnitte, die personalisiert werden müssen, vorausgeblendet werden können. Auf diese Weise können Sie die Metrik [&quot;](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)Erster Inhaltsstoff&quot;Ihrer Seite optimieren, die ein wichtiger KPI für Ihr Unternehmen ist, um einen hohen Wert im [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -System zu erzielen.

* Unterstützung für ein völlig neues Objekt namens &quot;Ansichten&quot;, das für [Einzelseitenanwendungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) (SPAs) und [Mobilanwendungen](/help/c-target-mobile-app/target-mobile-app.md)verwendet wird.
* Unterstützung für das Vorab-Abrufen von Ansichten und Mboxes zur Leistungsoptimierung durch Zwischenspeicherung.
* Unterstützung für das Senden von Benachrichtigungen für bereits abgerufene Ansichten und Mboxes.

>[!IMPORTANT]
>
>Auf die Dokumentation [zur Legacy-API](https://developers.adobetarget.com/api/legacy-api/index.html) /v1/mbox und /v2/batchmbox-API kann weiterhin zugegriffen werden. Neue Funktionen werden jedoch in der neuen Versand-API entwickelt und nicht in die alten APIs zurückportiert.
