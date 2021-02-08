---
keywords: serverseitig;serverseitig;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Erfahren Sie mehr über die Adobe Target Server-Side Versand APIs, SDKs und Zielgruppe Recommendations APIs.
title: Wo kann ich Informationen zu Zielgruppe Server-Side Versand APIs und SDKs erhalten?
feature: Implement Server-side
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---


# Server-seitig: Target-Implementierung

Informationen zu den APIs für serverseitige Versand, SDKs und [!DNL Target Recommendations]-APIs.[!DNL Adobe Target]

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

Das Portal für die serverseitige SDK-Dokumentation unterstützt Sie bei der Implementierung von [!DNL Target] auf Ihren Servern in Ihrer gewünschten Sprache.[!DNL Adobe Target]

## Target Recommendations-APIs

Link: [Zielgruppe Recommendations APIs](https://developers.adobetarget.com/api/recommendations) und [Adobe Recommendations API-Übersicht](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html).

Mit den Recommendations-APIs können Sie programmatisch mit [!DNL Target] Recommendations-Servern interagieren. Diese APIs können in eine Reihe von Anwendungsstapeln integriert werden, um Funktionen auszuführen, die Sie normalerweise über die [!DNL Target]-Benutzeroberfläche ausführen würden.
