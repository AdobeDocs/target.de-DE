---
description: Informationen zu den serverseitigen Target-Bereitstellungs- und Recommendations-APIs sowie zum NodeJS-SDK.
keywords: serverseitig;Server-seitig;API;SDK;NodeJS;Node JS;Recommendations-API
seo-description: Informationen über apis für die seitenseitige Bereitstellung von Adobe Target-Servern, Recommendations-apis und das nodejs SDK.
seo-title: Serverseitig implementieren Sie Adobe Target
solution: Target
title: 'Serverseitig: Target-Implementierung'
topic: 'Recommendations '
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 385864d9daae19468c4557e51043d5b788924658

---


# Serverseitig: Target-Implementierung{#server-side-implement-target}

Informationen über [!DNL Adobe Target] apis für die serverseitige Bereitstellung, Server Side Batch Delivery apis, nodejs SDK, [!DNL Target Recommendations] apis und [!DNL Target Classic] apis (entfernt).

Der folgende Prozess erfolgt in einer serverseitigen Implementierung von [!DNL Target]:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Ihr Server sendet diese Anforderung [!DNL Target]an.
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Ihr Server entscheidet, welches Erlebnis auf dem Client-Gerät bereitgestellt werden soll, damit es gerendert wird.

Das Erlebnis muss nicht in einem Browser angezeigt werden; Sie kann in einer E-Email oder Kiosk, über einen Sprecherassistenten oder über ein anderes nicht visuelles oder nicht browserbasiertes Gerät angezeigt werden. Da sich Ihr Server zwischen dem Client befindet und [!DNL Target]dieser Typ der Implementierung auch dann sehr gut ist, wenn Sie mehr Kontrolle und Sicherheit benötigen oder komplexe Backend-Prozesse benötigen, die auf Ihrem Server ausgeführt werden sollen.

Im folgenden Abschnitt werden die verschiedenen APIs und das NodeJS-SDK aufgeführt und zusätzliche Informationen bereitgestellt:

## Serverseitige Bereitstellungs-APIs

Link: [Apis für die serverseitige Auslieferung](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

[!DNL Target]Mit kann Ihre Anwendung Mbox-Aufrufe über beliebige Browser, Mobilgeräte oder sogar andere Server tätigen. Die API für die serverseitige Bereitstellung ist speziell für die Integration [!DNL Target] mit einer serverseitigen Plattform ausgelegt, die HTTP/HTTPS-Aufrufe vornimmt.

Sie können die API verwenden, um Ihre benutzerdefinierte Anwendung zu integrieren [!DNL Target]. Das ist besonders nützlich für Organisationen, die Targeting in einem nicht browserbasierten IoT-Gerät bereitstellen möchten, wie z. B. einem vernetzten TV-Gerät, einem Verkaufsautomaten oder einem digitalen Bildschirm im Geschäft.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Sie können Inhalte nur für eine einzelne Mbox abrufen.

Diese API implementiert vorhandene Mbox-Funktionen per RESTful-Methode.

Diese API verarbeitet keine Cookies oder Weiterleitungsaufrufe.

## Serverseitige Batch-Bereitstellungs-APIs

Link: [Server Side Batch Delivery apis](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

Mit der Batch-Bereitstellungs-API kann Ihre Anwendung Inhalte für verschiedene Mboxes in einem einzelnen Aufruf anfordern. Es verfügt außerdem über einen Prefetch-Modus, mit dem Clients wie mobile Apps, Server usw. Inhalte für mehrere mboxes in einer Anforderung abrufen, lokal zwischenspeichern und später benachrichtigen [!DNL Target] können, wenn der Benutzer diese mboxes besucht.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Da Sie Inhalte für mehrere Mboxes abrufen können, ist es für die Performance sinnvoller, die Batch-Mbox-API zu verwenden. Hierüber vermeiden Sie wiederholte HTTP-Anfragen, die unter Umständen viel Leistung beanspruchen.

## NodeJS-SDK

Link: [Nodejs SDK](https://www.npmjs.com/package/@adobe/target-node-client)

Aktuell ist nur ein SDK verfügbar: das NodeJS-SDK.

Das NodeJS-SDK ist ein Thin-Wrapper um das NodeJS-HTTP/HTTPS-Kernmodul herum. Im Hintergrund verwenden die NodeJS-SDK-APIs dieselben serverseitigen Bereitstellungs-APIs.

Die Zuordnung lautet wie folgt:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations] APIs

Link: [Target-Recommendations-apis](https://developers.adobetarget.com/api/recommendations)

Mit den Recommendations-APIs können Sie programmgesteuert mit den Recommendations-Servern von Target interagieren. Diese APIs können in verschiedene Anwendungs-Stacks integriert werden, um Funktionen durchzuführen, die Sie für gewöhnlich über die Benutzeroberfläche ausführen würden.

## [!DNL Target Classic] APIs

[!DNL Target Classic] Die Benutzeroberfläche und die apis wurden entfernt. Informationen über den Umstieg auf die modernen APIs von Target finden Sie unter [Übergang von veralteten Target-APIs zu Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Authoring-APIs (in denen Sie Aktivitäten, Angebote, Zielgruppen usw. erstellen) unterstützen kein Cross Origin Resource Sharing (CORS).

## Unterschiede zwischen serverseitigen Target-Bereitstellungs-APIs und NodeJS-SDK {#section_10336B7934F54CE98E35907A4748A4A4}

Viele Kunden kennen die Unterschiede zwischen den serverseitigen APIs und dem NodeJS-SDK nicht. Das gilt insbesondere hinsichtlich der Performance.

Folgende häufig gestellte Fragen unterstützen Sie bei der Auswahl der für Sie passenden Methode:

**Wann sollten Sie die „rohen“ serverseitigen APIs und wann das NodeJS-SDK verwenden?**

Wenn Sie NodeJS als Backend-Technologie verwenden, ist das NodeJS-SDK die naheliegende Wahl. Das SDK übernimmt viele Details, wie z. B. Cookies, Header, Payload usw. So können Sie sich auf den Kern Ihrer Anwendung konzentrieren.

**Lassen sich durch Verwendung des NodeJS-SDKs Leistungsverbesserungen erzielen?**

Leider haben wir hierzu keine Zahlen vorliegen. In der Regel erbringt das NodeJS-SDK jedoch dank der NodeJS-Ereignis-basierten Architektur eine gute Performance. Beachten Sie, dass die meiste Zeit auf dem [!DNL Target] Backend ausgegeben wird. Das NodeJS-SDK übernimmt nur einen geringen Teil der Verarbeitung. Das SDK ist grundsätzlich für das Packen einer [!DNL Target] Anforderung und das Analysieren einer [!DNL Target] Antwort verantwortlich.
