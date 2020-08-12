---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Informationen zu Adobe Target-APIs, einschließlich Admin-, Versand-, Berichte- und Profil-APIs.
title: Übersicht über die Adobe Target API
topic: APIs
translation-type: tm+mt
source-git-commit: 240c0f36bf39ee16d8d8e1b66ad6bed54b4f1fed
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Adobe Target API overview

[!DNL Adobe Target] APIs can be grouped according to type.

| API-Typ | What it enables you to do | Download-Link | Other helpful links |
| --- | --- | --- |--- |
| Admin | Create, modify, and delete activities, audiences, offers, and other objects (including [!DNL Recommendations] entities, criteria, designs, and so on. The [!DNL Recommendations] APIs are a type of admin API.) | <UL><li>[Target Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Recommendations APIs](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target-Tutorials verwenden* |
| Bereitstellung | Abrufen optimierter und personalisierter Inhalte vom [!DNL Target] für den Versand bis zum Endbenutzer. | [Zielgruppe Versand API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Berichterstellung | Export activity results and other reporting results. | Berichte-APIs sind in der [Zielgruppe Admin API Postman-Sammlung](https://developers.adobetarget.com/api/#admin-postman-collection)enthalten. |  |
| Profil | Abrufen und Ändern von in Adobe Target gespeicherten Profilen. | [Target Profile API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>There are important distinctions between [!DNL Target] Admin APIs (including the [!DNL Recommendations] APIs) and [!DNL Target] Delivery APIs:
>
>* Admin APIs let you configure various aspects of [!DNL Target] that you could also configure in the [!DNL Target] UI. Für Admin-APIs ist eine Authentifizierung erforderlich.
   >
   >
* Mit Versand-APIs können Sie Inhalte abrufen. Versand-APIs erfordern keine Authentifizierung.
>
>
Um [!DNL Target] Admin-APIs zu verwenden, müssen Sie zunächst die Authentifizierung mit der Adobe I/O konfigurieren. Weitere Informationen finden Sie unter [Authentifizierung](https://docs.adobe.com/content/help/en/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target-Tutorials* konfigurieren.
