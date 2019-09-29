---
description: Informationen zu den Server-seitigen Target-Bereitstellungs- und Recommendations-APIs sowie zum NodeJS-SDK.
keywords: Server-seitig;Server-Seite;API;SDK;NodeJS;Node JS;Recommendations-API
seo-description: Informationen zu den Server-seitigen Adobe Target-Bereitstellungs- und Recommendations-APIs sowie zum NodeJS-SDK.
seo-title: Adobe Target Server-seitig implementieren
solution: Target
title: 'Server-seitig: Target-Implementierung'
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Server-seitig: Target-Implementierung{#server-side-implement-target}

Informationen zu [!DNL Adobe Target]Server-seitigen Target-Bereitstellungs-APIs, Server-seitigen Batch-Bereitstellungs-APIs, NodeJS-SDK,[!DNL Target Recommendations] APIs und [!DNL Target Classic]-APIs (beendet).

Der folgende Prozess wird in einer Server-seitigen Implementierung von [!DNL Target] ausgeführt:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Ihr Server sendet diese Anforderung an [!DNL Target].
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Ihr Server entscheidet, welches Erlebnis auf dem Client-Gerät bereitgestellt werden soll, damit es gerendert wird.

Das Erlebnis muss nicht in einem Browser angezeigt werden. Es kann auch in einer E-Mail oder an einem Kiosk, über einen Sprachassistenten oder über ein anderes nicht visuelles Erlebnis oder nicht browserbasiertes Gerät angezeigt werden. Da sich Ihr Server zwischen dem Client und [!DNL Target] befindet, ist diese Art der Implementierung auch dann optimal, wenn Sie mehr Kontrolle und Sicherheit benötigen oder komplexe Backend-Prozesse haben, die auf Ihrem Server ausgeführt werden sollen.

Im folgenden Abschnitt werden die verschiedenen APIs und das NodeJS-SDK aufgeführt und zusätzliche Informationen bereitgestellt:

## Server-seitige Bereitstellungs-APIs

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/#server-side-delivery)

`/rest/v1/mbox`

Mit [!DNL Target] kann Ihre Anwendung Mbox-Aufrufe über beliebige Browser, Mobilgeräte oder sogar andere Server tätigen. Die Server-seitige Bereitstellungs-API wurde speziell dazu entwickelt, [!DNL Target] in beliebige Server-seitige Plattformen zu integrieren, die HTTP-/HTTPS-Aufrufe durchführen.

Sie können die API verwenden, um Ihre benutzerspezifische Anwendung in [!DNL Target] zu integrieren. Das ist besonders nützlich für Organisationen, die Targeting in einem nicht browserbasierten IoT-Gerät bereitstellen möchten, wie z. B. einem vernetzten TV-Gerät, einem Verkaufsautomaten oder einem digitalen Bildschirm im Geschäft.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Sie können Inhalte nur für eine einzelne Mbox abrufen.

Diese API implementiert vorhandene Mbox-Funktionen per RESTful-Methode.

Diese API verarbeitet keine Cookies oder Weiterleitungsaufrufe.

## Server-seitige Batch-Bereitstellungs-APIs

Link: [Server Side Batch Delivery APIs](https://developers.adobetarget.com/api/#server-side-batch-delivery)

`/rest/v2/batchmbox`

Mit der Batch-Bereitstellungs-API kann Ihre Anwendung Inhalte für verschiedene Mboxes in einem einzelnen Aufruf anfordern. Sie verfügt darüber hinaus über einen Vorabruf-Modus, mit dem Clients wie Apps, Server usw. Inhalte für verschiedene Mboxes in einer Anfrage abrufen, lokal zwischenspeichern und später [!DNL Target] benachrichtigen können, wenn der Benutzer die entsprechenden Mboxes besucht.

Dieser Endpunkt kann Angebote nur für gewöhnliche Mboxes zurückgeben. Da Sie Inhalte für mehrere Mboxes abrufen können, ist es für die Performance sinnvoller, die Batch-Mbox-API zu verwenden. Hierüber vermeiden Sie wiederholte HTTP-Anfragen, die unter Umständen viel Leistung beanspruchen.

## NodeJS-SDK

Link: [NodeJS SDK](https://www.npmjs.com/package/@adobe/target-node-client)

Aktuell ist nur ein SDK verfügbar: das NodeJS-SDK.

Das NodeJS-SDK ist ein Thin-Wrapper um das NodeJS-HTTP/HTTPS-Kernmodul herum. Im Hintergrund verwenden die NodeJS-SDK-APIs dieselben Server-seitigen Bereitstellungs-APIs.

Die Zuordnung lautet wie folgt:

* `MarketingCloudClient.getOffer() \*- invokes \*/res/v1/mbox endpoint`
* `MarketingCloudClient.getOffers() \*- invokes \*/res/v2/batchmbox endpoint`

## [!DNL Target Recommendations]-APIs

Link: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations)

Mit den Recommendations-APIs können Sie programmgesteuert mit den Recommendations-Servern von Target interagieren. Diese APIs können in verschiedene Anwendungs-Stacks integriert werden, um Funktionen durchzuführen, die Sie für gewöhnlich über die Benutzeroberfläche ausführen würden.

## [!DNL Target Classic]-APIs

Die [!DNL Target Classic]-Benutzeroberfläche und -APIs wurden eingestellt. Informationen über den Umstieg auf die modernen APIs von Target finden Sie unter [Übergang von veralteten Target-APIs zu Adobe I/O](../../c-implementing-target/c-api-and-sdk-overview/target-api-documentation.md#concept_3A31E26C8FAF49598152ACFE088BD4D2).

>[!NOTE]
>Authoring-APIs (in denen Sie Aktivitäten, Angebote, Zielgruppen usw. erstellen) unterstützen kein Cross Origin Resource Sharing (CORS).

## Unterschiede zwischen Server-seitigen Target-Bereitstellungs-APIs und NodeJS-SDK {#section_10336B7934F54CE98E35907A4748A4A4}

Viele Kunden kennen die Unterschiede zwischen den Server-seitigen APIs und dem NodeJS-SDK nicht. Das gilt insbesondere hinsichtlich der Performance.

Folgende häufig gestellte Fragen unterstützen Sie bei der Auswahl der für Sie passenden Methode:

**Wann sollten Sie die „rohen“ Server-seitigen APIs und wann das NodeJS-SDK verwenden?**

Wenn Sie NodeJS als Backend-Technologie verwenden, ist das NodeJS-SDK die naheliegende Wahl. Das SDK übernimmt viele Details, wie z. B. Cookies, Header, Payload usw. So können Sie sich auf den Kern Ihrer Anwendung konzentrieren.

**Lassen sich durch Verwendung des NodeJS-SDKs Leistungsverbesserungen erzielen?**

Leider haben wir hierzu keine Zahlen vorliegen. In der Regel erbringt das NodeJS-SDK jedoch dank der NodeJS-Ereignis-basierten Architektur eine gute Performance. Die meiste Zeit wird hierbei am [!DNL Target]-Backend benötigt. Das NodeJS-SDK übernimmt nur einen geringen Teil der Verarbeitung. Das SDK ist im Grunde genommen für die Paketierung einer [!DNL Target]-Anfrage und das Parsen einer [!DNL Target]-Antwort verantwortlich.
