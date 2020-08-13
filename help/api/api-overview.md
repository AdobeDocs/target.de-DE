---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Informationen zu Adobe Target-APIs, einschließlich Admin-, Versand-, Berichte- und Profil-APIs.
title: Übersicht über die Adobe Target API
feature: api
topic: APIs
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Übersicht über die Adobe Target API

[!DNL Adobe Target] APIs können nach Typ gruppiert werden.

| API type | Was es Ihnen ermöglicht | Download-Link | Weitere hilfreiche Links |
| --- | --- | --- |--- |
| Admin | Erstellen, ändern und löschen Sie Aktivitäten, Audiencen, Angebote und andere Objekte (einschließlich [!DNL Recommendations] Entitäten, Kriterien, Entwürfe usw.). Die [!DNL Recommendations] APIs sind eine Art Admin-API.) | <UL><li>[Zielgruppe Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Use Recommendations APIs](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target Tutorials* |
| Bereitstellung | Abrufen optimierter und personalisierter Inhalte vom [!DNL Target] für den Versand bis zum Endbenutzer. | [Target Delivery API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Berichterstellung | Export activity results and other reporting results. | Reporting APIs are included within the [Target Admin API Postman collection](https://developers.adobetarget.com/api/#admin-postman-collection). |  |
| Profil | Retrieve and modify user profiles stored in Adobe Target. | [Target Profile API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>There are important distinctions between [!DNL Target] Admin APIs (including the [!DNL Recommendations] APIs) and [!DNL Target] Delivery APIs:
>
>* Admin APIs let you configure various aspects of [!DNL Target] that you could also configure in the [!DNL Target] UI. Für Admin-APIs ist eine Authentifizierung erforderlich.
   >
   >
* Mit Versand-APIs können Sie Inhalte abrufen. Delivery APIs do not require authentication.
>
>
To use [!DNL Target] Admin APIs, you first need to configure authentication using Adobe I/O. For more information, see [Configure Authentication](https://docs.adobe.com/content/help/en/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target Tutorials*.
