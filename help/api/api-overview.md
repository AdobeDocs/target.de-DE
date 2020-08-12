---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Information about Adobe Target APIs, including the Admin, Delivery, Reporting, and Profile APIs.
title: Übersicht über die Adobe Target API
topic: APIs
translation-type: tm+mt
source-git-commit: 84cd5d41655baaaadeba63954858730ce956e039
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# Adobe Target API overview

Adobe Target-APIs können nach Typ gruppiert werden.

| API-Typ | Was es Ihnen ermöglicht | Download-Link | Weitere hilfreiche Links |
| --- | --- | --- |--- |
| Admin | Erstellen, ändern und löschen Sie Aktivitäten, Audiencen, Angebote und andere Objekte (einschließlich [!DNL Recommendations] Entitäten, Kriterien, Entwürfe usw.). Die [!DNL Recommendations] APIs sind eine Art Admin-API.) | <UL><li>[Zielgruppe Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Recommendations APIs](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target-Tutorials verwenden* |
| Bereitstellung | Abrufen optimierter und personalisierter Inhalte vom [!DNL Target] für den Versand bis zum Endbenutzer. | [Zielgruppe Versand API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Berichterstellung | Exportieren Sie Aktivitäten und andere Berichte. | Berichte-APIs sind in der [Zielgruppe Admin API Postman-Sammlung](https://developers.adobetarget.com/api/#admin-postman-collection)enthalten. |  |
| Profil | Abrufen und Ändern von in Adobe Target gespeicherten Profilen. | [Zielgruppe Profil API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Beachten Sie die Unterscheidung zwischen **Admin-APIs** (einschließlich der [!DNL Recommendations] APIs), mit denen Sie verschiedene Aspekte von Adobe Target konfigurieren können, und **Versand-APIs**, mit denen Sie Inhalte abrufen können. Admin-APIs erfordern eine Authentifizierung, Versand-APIs dagegen nicht.
>
>Um Adobe Target Admin-APIs zu verwenden, müssen Sie zunächst die Authentifizierung mit der Adobe I/O konfigurieren. Weitere Informationen finden Sie unter [Authentifizierung](https://docs.adobe.com/content/help/en/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target-Tutorials* konfigurieren.
