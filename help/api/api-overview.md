---
keywords: api;apis;admin api;Versand-API;Berichte-API;Profil-API
description: Suchen Sie nach Adobe [!DNL Target] APIs, einschließlich Admin-, Versand-, Berichte- und Profil-APIs.
title: Wo finde ich die  [!DNL Target] API- und SDK-Dokumentation?
feature: APIs/SDKs
role: Developer
exl-id: 2a0232cc-9a6a-42f4-afb6-4b3e2b13939c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---

# API-Übersicht über die Adobe [!DNL Target]

[!DNL Adobe Target] APIs können nach Typ gruppiert werden: Admin-, Versand-, Berichte- und Profil-APIs.

| API-Typ | Was es Ihnen ermöglicht | Download-Link | Weitere hilfreiche Links |
| --- | --- | --- |--- |
| Admin | Erstellen, ändern und löschen Sie Aktivitäten, Audiencen, Angebote und andere Objekte (einschließlich [!DNL Recommendations]-Entitäten, Kriterien, Entwürfe usw.). Die [!DNL Recommendations]-APIs sind eine Art Admin-API.) | <UL><li>[Zielgruppe Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Verwenden der Recommendations ](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) APIs in  *Adobe Target-Tutorials* |
| Bereitstellung | Abrufen optimierter und personalisierter Inhalte von [!DNL Target] für Versand an Endbenutzer. | [Zielgruppe Versand API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Berichterstellung | Exportieren Sie Aktivitäten und andere Berichte. | Berichte-APIs sind in der [Zielgruppe Admin API Postman-Sammlung](https://developers.adobetarget.com/api/#admin-postman-collection) enthalten. |  |
| Profil | Abrufen und Ändern von in Adobe Target gespeicherten Profilen. | [Zielgruppe Profil API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Es gibt wichtige Unterscheidungen zwischen [!DNL Target] Admin-APIs (einschließlich der [!DNL Recommendations]-APIs) und [!DNL Target] Versand-APIs:
>
>* Mit Admin-APIs können Sie verschiedene Aspekte von [!DNL Target] konfigurieren, die Sie auch in der [!DNL Target]-Benutzeroberfläche konfigurieren können. Für Admin-APIs ist eine Authentifizierung erforderlich.
   >
   >
* Mit Versand-APIs können Sie Inhalte abrufen. Versand-APIs erfordern keine Authentifizierung.
>
>
Um [!DNL Target] Admin-APIs zu verwenden, müssen Sie zunächst die Authentifizierung mit Adobe I/O konfigurieren. Weitere Informationen finden Sie unter [Authentifizierung konfigurieren](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target-Tutorials>.*
