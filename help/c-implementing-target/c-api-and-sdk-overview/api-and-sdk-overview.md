---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informationen zu Adobe Target-serverseitigen Versand-APIs, Node.js-SDK und Zielgruppe-Recommendations-APIs.
title: Informationen zu Adobe Target-serverseitigen Versand-APIs, Node.js-SDK und Zielgruppe-Recommendations-APIs.
feature: null
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 11%

---


# Server-seitig: Target-Implementierung{#server-side-implement-target}

Information about [!DNL Adobe Target] server-side delivery APIs, Node.js SDK, and [!DNL Target Recommendations] APIs.

Der folgende Prozess wird in einer Server-seitigen Implementierung von [!DNL Target] ausgeführt:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Ihr Server sendet diese Anforderung an [!DNL Target].
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Ihr Server entscheidet, welches Erlebnis an das Client-Gerät gesendet werden soll, damit es gerendert werden kann.

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
* Nahtlose Integration mit [!DNL Adobe Experience Cloud] Produkten wie [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) und dem [!DNL Experience Cloud ID Service] Server.

## Node.js SDK

Link: [Node.js SDK](https://github.com/adobe/target-nodejs-sdk)

Das Node.js SDK ist ein ausgereiftes Software Development Kit, das die Komplexität der Verwaltung von Cookies, Sitzungen und Integration in [!DNL Experience Cloud] Produkte wie [!DNL Analytics], [!DNL Experience Cloud Visitor ID Service]und [!DNL Audience Manager]unterstützt. Hinter den Kulissen verwendet das SDK Node.js die `/rest/v1/delivery` API. Im Folgenden finden Sie einige wichtige Funktionen, die im SDK Node.js unterstützt werden:

* **Unterstützung für Prefetch und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen:** Sie können das SDK Node.js verwenden, um Erlebnisse abzurufen und sie lokal auf Ihrem Node.js-Server zu zwischenspeichern, um Serveraufrufe zu minimieren [!DNL Target] und Ihre Anwendungsleistung zu optimieren.
* **Möglichkeit zum Abrufen von VEC-erstellten Aktivitäten:** Rufen Sie serverseitig VEC-erstellte Aktivitäten ab. Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Seitenabschnitte, die personalisiert werden müssen, vorausgeblendet werden können. Auf diese Weise können Sie die Metrik [&quot;](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)Erster Inhaltsstoff&quot;Ihrer Seite optimieren, die ein wichtiger KPI für Ihr Unternehmen ist, um einen hohen Wert im [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -System zu erzielen.

## Zielgruppe Java SDK

Link: [Zielgruppe Java SDK](https://github.com/adobe/target-java-sdk)

Das Java SDK ist ein ausgereiftes Software Development Kit, das die Komplexität der Verwaltung von Cookies, Sitzungen und Integration in [!DNL Adobe Experience Cloud] Lösungen wie [!DNL Adobe Analytics], die [!DNL Experience Cloud Visitor ID Service]und [!DNL Adobe Audience Manager]die Hinter den Kulissen verwendet das Java SDK die `/rest/v1/delivery` API. Here are some notable features that are supported in the Java SDK:

* **Unterstützung für Prefetch und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung** ermöglichen: Sie können JavaSDK verwenden, um Erlebnisse abzurufen und sie lokal auf Ihrem Java-Server zwischenspeichern, um Serveraufrufe zu minimieren [!DNL Target] und Ihre Anwendungsleistung zu optimieren.
* **Möglichkeit zum Abrufen von VEC-erstellten Aktivitäten**: Rufen Sie serverseitig VEC-erstellte Aktivitäten ab. Die Antwort, die VEC-erstellte Aktivitäten enthält, enthält Selektoren, mit denen nur Seitenabschnitte, die personalisiert werden müssen, vorausgeblendet werden können. Auf diese Weise können Sie die Metrik &quot; [Erster Inhaltsstoff](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html) &quot;Ihrer Seite optimieren, die ein wichtiger KPI für Ihr Unternehmen ist, um einen hohen Wert im [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -System zu erzielen.

## Target Recommendations-APIs

Link: [Zielgruppe Recommendations APIs](https://developers.adobetarget.com/api/recommendations) und [Adobe Recommendations API-Übersicht](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html).

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
