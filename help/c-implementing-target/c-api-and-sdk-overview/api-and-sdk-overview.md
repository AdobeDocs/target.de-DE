---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informationen zu Adobe Target-serverseitigen Versand-APIs, SDKs und Zielgruppe-Recommendations-APIs.
title: Informationen zu Adobe Target-serverseitigen Versand-APIs, Node.js-SDK und Zielgruppe-Recommendations-APIs.
feature: server-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 20%

---


# Server-seitig: Target-Implementierung{#server-side-implement-target}

Informationen zu den APIs für serverseitige Versand, SDKs und [!DNL Adobe Target]-APIs.[!DNL Target Recommendations]

Der folgende Prozess wird in einer Server-seitigen Implementierung von [!DNL Target] ausgeführt:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Ihr Server sendet diese Anforderung an [!DNL Target].
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Ihr Server entscheidet, welches Erlebnis an das Client-Gerät gesendet werden soll, damit es gerendert werden kann.

Das Erlebnis muss nicht in einem Browser angezeigt werden. Das Erlebnis kann in einer E-Mail oder einem Kiosk, über einen Sprachassistenten oder über ein anderes nicht visuelles Erlebnis oder ein nicht browserbasiertes Gerät angezeigt werden. Da sich Ihr Server zwischen dem Client und [!DNL Target] befindet, ist diese Art der Implementierung auch dann optimal, wenn Sie mehr Kontrolle und Sicherheit benötigen oder komplexe Backend-Prozesse haben, die auf Ihrem Server ausgeführt werden sollen.

>[!NOTE]
>
>Ein erstmaliger Besucher kann nur clientseitig initialisiert werden. Ein erstmaliger Besucher *kann nicht* serverseitig initialisiert werden.

Die folgenden Abschnitte enthalten weitere Informationen zu den verschiedenen APIs und dem NodeJS SDK:

## Server-seitige Bereitstellungs-APIs

Link: [Serverseitige Versand-APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Mithilfe der Versand-API [!DNL Target] können Sie:

* Stellen Sie Erlebnisse für das Web, einschließlich SPA, mobile Kanal und Nicht-Browser-basierte IoT-Geräte bereit, wie z. B. angeschlossene TVs, Kiosks oder digitale In-Store-Bildschirme.
* Stellen Sie Erlebnisse von jeder serverseitigen Plattform oder Anwendung bereit, die HTTP/s-Aufrufe ausführen kann.
* Stellen Sie einem Besucher konsistente und personalisierte Erlebnisse zur Verfügung, unabhängig davon, welcher Kanal bzw. welche Geräte der Besucher verwendet hat, um mit Ihrem Unternehmen in Kontakt zu treten.
* Cache-Erlebnisse für einen Besucher innerhalb einer Serversitzung, sodass mehrere API-Aufrufe vermieden werden können, wodurch eine höhere Leistung erzielt wird.
* Integrieren Sie nahtlos in [!DNL Adobe Experience Cloud]-Produkte wie [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) und [!DNL Experience Cloud ID Service] vom Server.

## Serverseitige SDKs

Link: [Adobe Target SDKs](https://adobetarget-sdks.gitbook.io/docs/)

Das Portal für die serverseitige SDK-Dokumentation unterstützt Sie bei der Implementierung von [!DNL Adobe Target] auf Ihren Servern in Ihrer gewünschten Sprache.[!DNL Target]

## Target Recommendations-APIs

Link: [Zielgruppe Recommendations APIs](https://developers.adobetarget.com/api/recommendations) und [Adobe Recommendations API-Übersicht](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html).

Mit den Recommendations-APIs können Sie programmatisch mit [!DNL Target] Recommendations-Servern interagieren. Diese APIs können in eine Reihe von Anwendungsstapeln integriert werden, um Funktionen auszuführen, die Sie normalerweise über die [!DNL Target]-Benutzeroberfläche ausführen würden.
