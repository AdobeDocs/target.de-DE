---
description: Informationen zu den Server-seitigen Target-Bereitstellungs- und Recommendations-APIs sowie zum NodeJS-SDK.
keywords: Server-seitig;Server-Seite;API;SDK;NodeJS;Node JS;Recommendations-API
seo-description: Informationen über apis für die seitenseitige Bereitstellung von Adobe Target-Servern, Recommendations-apis und das nodejs SDK.
seo-title: Serverseitig implementieren Sie Adobe Target
solution: Target
title: 'Server-seitig: Target-Implementierung'
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Server-seitig: Target-Implementierung{#server-side-implement-target}

Information about [!DNL Adobe Target] Server Side delivery APIs, Server Side Batch Delivery APIs, NodeJS SDK, [!DNL Target Recommendations] APIs, and [!DNL Target Classic] APIs (decommissioned).

The following process occurs in a server-side implementation of [!DNL Target]:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Your server sends that request to [!DNL Target].
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Ihr Server entscheidet, welches Erlebnis auf dem Client-Gerät bereitgestellt werden soll, damit es gerendert wird.

Das Erlebnis muss nicht in einem Browser angezeigt werden; Sie kann in einer E-Email oder Kiosk, über einen Sprecherassistenten oder über ein anderes nicht visuelles oder nicht browserbasiertes Gerät angezeigt werden. Because your server sits between the client and [!DNL Target], this type of implementation is also ideal if you need greater control and security or have complex backend processes that you want to run on your server.

Im folgenden Abschnitt werden die verschiedenen APIs und das NodeJS-SDK aufgeführt und zusätzliche Informationen bereitgestellt:

## Server-seitige Bereitstellungs-APIs

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target]Mit kann Ihre Anwendung Mbox-Aufrufe über beliebige Browser, Mobilgeräte oder sogar andere Server tätigen. The Server Side delivery API is specifically designed to integrate [!DNL Target] with any server-side platform that makes HTTP/HTTPS calls.

You can use the API to integrate your custom application with [!DNL Target]. Das ist besonders nützlich für Organisationen, die Targeting in einem nicht browserbasierten IoT-Gerät bereitstellen möchten, wie z. B. einem vernetzten TV-Gerät, einem Verkaufsautomaten oder einem digitalen Bildschirm im Geschäft.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Sie können Inhalte nur für eine einzelne Mbox abrufen.

Diese API implementiert vorhandene Mbox-Funktionen per RESTful-Methode.

Diese API verarbeitet keine Cookies oder Weiterleitungsaufrufe.

## Server-seitige Batch-Bereitstellungs-APIs

Link: [Server Side Batch Delivery APIs](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

Mit der Batch-Bereitstellungs-API kann Ihre Anwendung Inhalte für verschiedene Mboxes in einem einzelnen Aufruf anfordern. It also has a prefetch mode that enables clients like mobile apps, servers, and so forth to fetch content for multiple mboxes in one request, cache it locally, and later notify [!DNL Target] when the user visits those mboxes.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Da Sie Inhalte für mehrere Mboxes abrufen können, ist es für die Performance sinnvoller, die Batch-Mbox-API zu verwenden. Hierüber vermeiden Sie wiederholte HTTP-Anfragen, die unter Umständen viel Leistung beanspruchen.

## NodeJS-SDK

Link: [NodeJS SDK](https://www.npmjs.com/package/@adobe/target-node-client)

Aktuell ist nur ein SDK verfügbar: das NodeJS-SDK.

Das NodeJS-SDK ist ein Thin-Wrapper um das NodeJS-HTTP/HTTPS-Kernmodul herum. Im Hintergrund verwenden die NodeJS-SDK-APIs dieselben Server-seitigen Bereitstellungs-APIs.

Die Zuordnung lautet wie folgt:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations] APIs

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations)

Mit den Recommendations-APIs können Sie programmgesteuert mit den Recommendations-Servern von Target interagieren. Diese APIs können in verschiedene Anwendungs-Stacks integriert werden, um Funktionen durchzuführen, die Sie für gewöhnlich über die Benutzeroberfläche ausführen würden.

## [!DNL Target Classic] APIs

[!DNL Target Classic] Die Benutzeroberfläche und die apis wurden entfernt. Informationen über den Umstieg auf die modernen APIs von Target finden Sie unter [Übergang von veralteten Target-APIs zu Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Authoring-APIs (in denen Sie Aktivitäten, Angebote, Zielgruppen usw. erstellen) unterstützen kein Cross Origin Resource Sharing (CORS).

## Unterschiede zwischen Server-seitigen Target-Bereitstellungs-APIs und NodeJS-SDK {#section_10336B7934F54CE98E35907A4748A4A4}

Viele Kunden kennen die Unterschiede zwischen den Server-seitigen APIs und dem NodeJS-SDK nicht. Das gilt insbesondere hinsichtlich der Performance.

Folgende häufig gestellte Fragen unterstützen Sie bei der Auswahl der für Sie passenden Methode:

**Wann sollten Sie die „rohen“ Server-seitigen APIs und wann das NodeJS-SDK verwenden?**

Wenn Sie NodeJS als Backend-Technologie verwenden, ist das NodeJS-SDK die naheliegende Wahl. Das SDK übernimmt viele Details, wie z. B. Cookies, Header, Payload usw. So können Sie sich auf den Kern Ihrer Anwendung konzentrieren.

**Lassen sich durch Verwendung des NodeJS-SDKs Leistungsverbesserungen erzielen?**

Leider haben wir hierzu keine Zahlen vorliegen. In der Regel erbringt das NodeJS-SDK jedoch dank der NodeJS-Ereignis-basierten Architektur eine gute Performance. Be aware that most of the time is spent on the [!DNL Target] backend. Das NodeJS-SDK übernimmt nur einen geringen Teil der Verarbeitung. The SDK is basically responsible for packaging a [!DNL Target] request and parsing a [!DNL Target] response.
