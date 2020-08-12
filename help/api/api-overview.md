---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Informationen zu Adobe Target-APIs, einschließlich Admin-, Versand-, Berichte- und Profil-APIs.
title: Übersicht über die Adobe Target API
feature: null
topic: APIs
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Übersicht über die Adobe Target API

[!DNL Adobe Target] APIs können nach Typ gruppiert werden.

| API-Typ | Was es Ihnen ermöglicht | Download-Link | Weitere hilfreiche Links |
| --- | --- | --- |--- |
| Admin | Erstellen, ändern und löschen Sie Aktivitäten, Audiencen, Angebote und andere Objekte (einschließlich [!DNL Recommendations] Entitäten, Kriterien, Entwürfe usw.). Die [!DNL Recommendations] APIs sind eine Art Admin-API.) | <UL><li>[Zielgruppe Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Use Recommendations APIs](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target Tutorials* |
| Bereitstellung | Retrieve optimized and personalized content from [!DNL Target] for delivery to an end user. | [Target Delivery API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Berichterstellung | Exportieren Sie Aktivitäten und andere Berichte. | Berichte-APIs sind in der [Zielgruppe Admin API Postman-Sammlung](https://developers.adobetarget.com/api/#admin-postman-collection)enthalten. |  |
| Profil | Abrufen und Ändern von in Adobe Target gespeicherten Profilen. | [Zielgruppe Profil API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Es gibt wichtige Unterschiede zwischen [!DNL Target] Admin-APIs (einschließlich der [!DNL Recommendations] APIs) und [!DNL Target] Versand-APIs:
>
>* Mit Admin-APIs können Sie verschiedene Aspekte konfigurieren, [!DNL Target] die Sie auch in der [!DNL Target] Benutzeroberfläche konfigurieren können. Für Admin-APIs ist eine Authentifizierung erforderlich.
   >
   >
* Mit Versand-APIs können Sie Inhalte abrufen. Versand-APIs erfordern keine Authentifizierung.
>
>
Um [!DNL Target] Admin-APIs zu verwenden, müssen Sie zunächst die Authentifizierung mit der Adobe I/O konfigurieren. Weitere Informationen finden Sie unter [Authentifizierung](https://docs.adobe.com/content/help/en/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target-Tutorials* konfigurieren.
