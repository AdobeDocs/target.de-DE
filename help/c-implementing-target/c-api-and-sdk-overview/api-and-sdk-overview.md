---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informationen zu Adobe Target-serverseitigen Versand-APIs, Node.js-SDK und Zielgruppe-Recommendations-APIs.
title: Informationen zu Adobe Target-serverseitigen Versand-APIs, Node.js-SDK und Zielgruppe-Recommendations-APIs.
feature: server-side
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 11%

---


# Server-seitig: Target-Implementierung{#server-side-implement-target}

Informationen zu [!DNL Adobe Target] serverseitigen Versand-APIs, Node.js-SDKs und [!DNL Target Recommendations] APIs.

Der folgende Prozess wird in einer Server-seitigen Implementierung von [!DNL Target] ausgeführt:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Ihr Server sendet diese Anforderung an [!DNL Target].
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Your server makes the decision on which experience to deliver to the client device for it to render.

Das Erlebnis muss nicht in einem Browser angezeigt werden. Das Erlebnis kann in einer E-Mail oder einem Kiosk, über einen Sprachassistenten oder über ein anderes nicht visuelles Erlebnis oder ein nicht browserbasiertes Gerät angezeigt werden. Da sich Ihr Server zwischen dem Client und [!DNL Target] befindet, ist diese Art der Implementierung auch dann optimal, wenn Sie mehr Kontrolle und Sicherheit benötigen oder komplexe Backend-Prozesse haben, die auf Ihrem Server ausgeführt werden sollen.

Die folgenden Abschnitte enthalten weitere Informationen zu den verschiedenen APIs und dem NodeJS SDK:

## Server-seitige Bereitstellungs-APIs

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Mithilfe der [!DNL Target] Versand-API können Sie:

* Stellen Sie Erlebnisse über das Web, einschließlich SPAs, mobile Kanal sowie Nicht-Browser-basierte IoT-Geräte wie angeschlossene TVs, Kiosks oder digitale Bildschirme im Store bereit.
* Stellen Sie Erlebnisse von jeder serverseitigen Plattform oder Anwendung bereit, die HTTP/s-Aufrufe ausführen kann.
* Stellen Sie einem Besucher konsistente und personalisierte Erlebnisse zur Verfügung, unabhängig davon, welcher Kanal bzw. welche Geräte der Besucher verwendet hat, um mit Ihrem Unternehmen in Kontakt zu treten.
* Cache-Erlebnisse für einen Besucher innerhalb einer Serversitzung, sodass mehrere API-Aufrufe vermieden werden können, wodurch eine höhere Leistung erzielt wird.
* Seamlessly integrate with [!DNL Adobe Experience Cloud] products, such as [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM), and the [!DNL Experience Cloud ID Service] from the server side.

## Node.js SDK

Link: [Node.js SDK](https://github.com/adobe/target-nodejs-sdk)

Das Node.js SDK ist ein ausgereiftes Software Development Kit, das die Komplexität der Verwaltung von Cookies, Sitzungen und Integration in [!DNL Experience Cloud] Produkte wie [!DNL Analytics], [!DNL Experience Cloud Visitor ID Service]und [!DNL Audience Manager]unterstützt. Hinter den Kulissen verwendet das SDK Node.js die `/rest/v1/delivery` API. Im Folgenden finden Sie einige wichtige Funktionen, die im SDK Node.js unterstützt werden:

* **Unterstützung für Prefetch und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen:** Sie können das SDK Node.js verwenden, um Erlebnisse abzurufen und sie lokal auf Ihrem Node.js-Server zu zwischenspeichern, um Serveraufrufe zu minimieren [!DNL Target] und Ihre Anwendungsleistung zu optimieren.
* **Möglichkeit zum Abrufen von VEC-erstellten Aktivitäten:** Rufen Sie serverseitig VEC-erstellte Aktivitäten ab. Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Seitenabschnitte, die personalisiert werden müssen, vorausgeblendet werden können. This helps optimize your page&#39;s [First Contentful Paint metric](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html), which is an important KPI for your business to achieve a high score in the [Google PageRank](https://en.wikipedia.org/wiki/PageRank) system.

## Target Java SDK

Link: [Target Java SDK](https://github.com/adobe/target-java-sdk)

The Java SDK is a sophisticated software development kit that removes the complexities of managing cookies, sessions, and integrating with [!DNL Adobe Experience Cloud] solutions, such as [!DNL Adobe Analytics], the [!DNL Experience Cloud Visitor ID Service], and [!DNL Adobe Audience Manager]. Behind the scenes, the Java SDK uses the `/rest/v1/delivery` API. Here are some notable features that are supported in the Java SDK:

* **Support for prefetch and notifications that allow you to optimize for performance via caching**: You can use the JavaSDK to retrieve experiences and cache them locally on your Java server with the purpose of minimizing server calls to [!DNL Target] and optimizing your application performance.
* **Ability to retrieve VEC-created activities**: Retrieve VEC-created activities on the server-side. Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Seitenabschnitte, die personalisiert werden müssen, vorausgeblendet werden können. This helps optimize your page&#39;s [First Contentful Paint](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html) metric, which is an important KPI for your business to achieve a high score in the [Google PageRank](https://en.wikipedia.org/wiki/PageRank) system.

## Target Recommendations-APIs

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations) and [Adobe Recommendations API Overview](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html).

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
