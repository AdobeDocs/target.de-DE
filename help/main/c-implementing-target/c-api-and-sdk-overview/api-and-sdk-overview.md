---
keywords: Server-seitig;Server-seitig;API;SDK;node.js;node js;node js;recommendations api;api:apis
description: Informationen zur Adobe [!DNL Target] Server-seitige Bereitstellungs-APIs, SDKs und [!DNL Target] Recommendations-APIs.
title: Informationen darüber [!DNL Target] Serverseitige Bereitstellungs-APIs und SDKs?
feature: Implement Server-side
role: Developer
exl-id: cdee007f-f54d-4cf3-9575-6319da3434a5
source-git-commit: db288fbb4ddf011b7051257fdc8126d1158c8469
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 23%

---

# Server-seitig: Target-Implementierung

Informationen über [!DNL Adobe Target] Server-seitige Bereitstellungs-APIs, SDKs und [!DNL Target Recommendations] APIs.

Der folgende Prozess wird in einer Server-seitigen Implementierung von [!DNL Target] ausgeführt:

1. Ein Client-Gerät fordert über Ihren Server ein Erlebnis an.
1. Ihr Server sendet diese Anforderung an [!DNL Target].
1. [!DNL Target] sendet die Antwort zurück an den Server.
1. Ihr Server entscheidet, welches Erlebnis an das Client-Gerät übermittelt werden soll, damit es gerendert werden kann.

Das Erlebnis muss nicht in einem Browser angezeigt werden. Das Erlebnis kann in einer E-Mail oder an einem Kiosk, über einen Sprachassistenten oder über ein anderes nicht visuelles Erlebnis oder nicht browserbasiertes Gerät angezeigt werden. Da sich Ihr Server zwischen dem Client und [!DNL Target] befindet, ist diese Art der Implementierung auch dann optimal, wenn Sie mehr Kontrolle und Sicherheit benötigen oder komplexe Backend-Prozesse haben, die auf Ihrem Server ausgeführt werden sollen.

>[!NOTE]
>
>Ein erstmaliger Besucher kann nur clientseitig initialisiert werden. Erstmaliger Besucher *cannot* Server-seitig initialisiert werden.

In den folgenden Abschnitten finden Sie weitere Informationen zu den verschiedenen APIs und dem NodeJS-SDK:

## Server-seitige Bereitstellungs-APIs

Link: [Server-seitige Bereitstellungs-APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Verwenden der [!DNL Target] Die Bereitstellungs-API bietet folgende Möglichkeiten:

* Bereitstellung von Erlebnissen über das Internet, einschließlich SPA- und Mobilkanälen sowie Nicht-Browser-basierte IoT-Geräte, wie z. B. angeschlossene TVs, Kiosks oder digitale In-store-Bildschirme.
* Stellen Sie Erlebnisse von jeder Server-seitigen Plattform oder Anwendung bereit, die HTTP/s-Aufrufe durchführen kann.
* Bereitstellen konsistenter und personalisierter Erlebnisse für einen Besucher, unabhängig davon, welcher Kanal oder welche Geräte der Besucher für die Interaktion mit Ihrem Unternehmen verwendet hat.
* Zwischenspeichern von Erlebnissen für einen Besucher innerhalb einer Sitzung auf Ihrem Server, sodass mehrere API-Aufrufe vermieden werden können, wodurch eine bessere Leistung erzielt wird.
* Nahtlose Integration mit [!DNL Adobe Experience Cloud] Produkte wie [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) und [!DNL Experience Cloud ID Service] vom Server aus.

## Server-seitige SDKs

Link: [Adobe Target SDKs](https://adobetarget-sdks.gitbook.io/docs/)

Die [!DNL Adobe Target] Das serverseitige SDK-Dokumentationsportal unterstützt Sie bei der Implementierung von [!DNL Target] auf Ihren Servern in Ihrer gewünschten Sprache.

## Target Recommendations-APIs

Link: [Target Recommendations-APIs](https://developers.adobetarget.com/api/recommendations) und [Übersicht über die Adobe Recommendations API](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html).

Mit den Recommendations-APIs können Sie programmatisch mit [!DNL Target] Recommendations-Server. Diese APIs können in eine Reihe von Anwendungsstacks integriert werden, um Funktionen auszuführen, die Sie normalerweise über die [!DNL Target] -Benutzeroberfläche.
