---
description: Informationen zu den serverseitigen Target-Bereitstellungs- und Recommendations-APIs sowie zum NodeJS-SDK.
keywords: serverseitig;Server-seitig;API;SDK;NodeJS;Node JS;Recommendations-API
seo-description: Informationen zu den serverseitigen Target-Bereitstellungs- und Recommendations-APIs sowie zum NodeJS-SDK.
seo-title: 'Serverseitig: Target-Implementierung'
solution: Target
title: 'Serverseitig: Target-Implementierung'
topic: 'Recommendations '
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Serverseitig: Target-Implementierung{#server-side-implement-target}

Informationen zu serverseitigen Target-Bereitstellungs-APIs, serverseitigen Batch-Bereitstellungs-APIs, Target Recommendations-APIs, Target Classic-APIs (beendet) sowie zum NodeJS-SDK.

Im folgenden Abschnitt werden die verschiedenen APIs und das NodeJS-SDK aufgeführt und zusätzliche Informationen bereitgestellt:

## Serverseitige Bereitstellungs-APIs

Link: [Apis für die serverseitige Auslieferung](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

Mit Adobe Target kann Ihre Anwendung Mbox-Aufrufe über beliebige Browser, Mobilgeräte oder sogar andere Server tätigen. Die serverseitige Bereitstellungs-API wurde speziell dazu entwickelt, Adobe Target in beliebige serverseitige Plattformen zu integrieren, die HTTP-/HTTPS-Aufrufe durchführen.

Sie können die API verwenden, um Ihre benutzerspezifische Anwendung in Target zu integrieren. Das ist besonders nützlich für Organisationen, die Targeting in einem nicht browserbasierten IoT-Gerät bereitstellen möchten, wie z. B. einem vernetzten TV-Gerät, einem Verkaufsautomaten oder einem digitalen Bildschirm im Geschäft.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Sie können Inhalte nur für eine einzelne Mbox abrufen.

Diese API implementiert vorhandene Mbox-Funktionen per RESTful-Methode.

Diese API verarbeitet keine Cookies oder Weiterleitungsaufrufe.

## Serverseitige Batch-Bereitstellungs-APIs

Link: [Server Side Batch Delivery apis](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

Mit der Batch-Bereitstellungs-API kann Ihre Anwendung Inhalte für verschiedene Mboxes in einem einzelnen Aufruf anfordern. Sie verfügt darüber hinaus über einen Vorabruf-Modus, mit dem Clients wie Apps, Server usw. Inhalte für verschiedene Mboxes in einer Anfrage abrufen, lokal zwischenspeichern und Target später benachrichtigen können, wenn der Benutzer die entsprechenden Mboxes besucht.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Da Sie Inhalte für mehrere Mboxes abrufen können, ist es für die Performance sinnvoller, die Batch-Mbox-API zu verwenden. Hierüber vermeiden Sie wiederholte HTTP-Anfragen, die unter Umständen viel Leistung beanspruchen.

## NodeJS-SDK

Link: [Nodejs SDK](https://www.npmjs.com/package/@adobe/target-node-client)

Aktuell ist nur ein SDK verfügbar: das NodeJS-SDK.

Das NodeJS-SDK ist ein Thin-Wrapper um das NodeJS-HTTP/HTTPS-Kernmodul herum. Im Hintergrund verwenden die NodeJS-SDK-APIs dieselben serverseitigen Bereitstellungs-APIs.

Die Zuordnung lautet wie folgt:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## Target Recommendations-APIs

Link: [Target-Recommendations-apis](https://developers.adobetarget.com/api/recommendations)

Mit den Recommendations-APIs können Sie programmgesteuert mit den Recommendations-Servern von Target interagieren. Diese APIs können in verschiedene Anwendungs-Stacks integriert werden, um Funktionen durchzuführen, die Sie für gewöhnlich über die Benutzeroberfläche ausführen würden.

## Target Classic-APIs

Die Target Classic-Benutzeroberfläche und -APIs wurden eingestellt. Informationen über den Umstieg auf die modernen APIs von Target finden Sie unter [Übergang von veralteten Target-APIs zu Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Authoring-APIs (in denen Sie Aktivitäten, Angebote, Zielgruppen usw. erstellen) unterstützen kein Cross Origin Resource Sharing (CORS).

## Unterschiede zwischen serverseitigen Target-Bereitstellungs-APIs und NodeJS-SDK {#section_10336B7934F54CE98E35907A4748A4A4}

Viele Kunden kennen die Unterschiede zwischen den serverseitigen APIs und dem NodeJS-SDK nicht. Das gilt insbesondere hinsichtlich der Performance.

Folgende häufig gestellte Fragen unterstützen Sie bei der Auswahl der für Sie passenden Methode:

**Wann sollten Sie die „rohen“ serverseitigen APIs und wann das NodeJS-SDK verwenden?**

Wenn Sie NodeJS als Backend-Technologie verwenden, ist das NodeJS-SDK die naheliegende Wahl. Das SDK übernimmt viele Details, wie z. B. Cookies, Header, Payload usw. So können Sie sich auf den Kern Ihrer Anwendung konzentrieren.

**Lassen sich durch Verwendung des NodeJS-SDKs Leistungsverbesserungen erzielen?**

Leider haben wir hierzu keine Zahlen vorliegen. In der Regel erbringt das NodeJS-SDK jedoch dank der NodeJS-Ereignis-basierten Architektur eine gute Performance. Die meiste Zeit wird hierbei am Target-Backend benötigt. Das NodeJS-SDK übernimmt nur einen geringen Teil der Verarbeitung. Das SDK ist im Grunde genommen für die Paketierung einer Target-Anfrage und das Parsen einer Target-Antwort verantwortlich.
