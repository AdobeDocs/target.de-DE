---
keywords: at.js;api;release;updates;apis;sdks;server side;serverside;server-side;api;delivery api
description: Versionshinweise zu Adobe Targets serverseitigen APIs.
title: Versionshinweise zu Adobe Targets serverseitigen APIs.
feature: release notes
topic: Standard
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Versionshinweise - serverseitige APIs der Zielgruppe

Versionshinweise zu den [Adobe Target-serverseitigen APIs](https://developers.adobetarget.com/api/delivery-api/).

## V1/Versand (9. Oktober 2019)

Ein komplett neuer Versand-API-Endpunkt wurde veröffentlicht.

* New [documentation](https://developers.adobetarget.com/api/delivery-api/) is available.
* Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.
* Retrieve VEC-created activities via the API.

   Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Seitenabschnitte, die personalisiert werden müssen, vorausgeblendet werden können. Auf diese Weise können Sie die Metrik [&quot;](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)Erster Inhaltsstoff&quot;Ihrer Seite optimieren, die ein wichtiger KPI für Ihr Unternehmen ist, um einen hohen Wert im [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -System zu erzielen.

* Support for an entirely new object called Views that is used for [Single Page Applications](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) (SPAs) and [mobile applications](/help/c-target-mobile-app/target-mobile-app.md).
* Support for prefetching of views and mboxes to optimize for performance via caching.
* Support for sending notifications for prefetched views and mboxes.

>[!IMPORTANT]
>
>The legacy [/v1/mbox and /v2/batchmbox API documentation](https://developers.adobetarget.com/api/legacy-api/index.html) can still be accessed. However, new features will be developed in the new delivery API and will not be back-ported to the legacy APIs.
