---
keywords: API;API;API;Admin API;Versand-API;Berichterstellungs-API;Profil-API
description: Adobe suchen [!DNL Target] APIs, einschließlich der APIs Admin, Versand, Reporting und Profil .
title: Wo finde ich mich? [!DNL Target] API- und SDK-Dokumentation?
feature: APIs/SDKs
role: Developer
exl-id: 2a0232cc-9a6a-42f4-afb6-4b3e2b13939c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# Adobe [!DNL Target] API-Übersicht

[!DNL Adobe Target] APIs können nach Typ gruppiert werden: Admin-, Versand-, Reporting- und Profil-APIs.

| API-Typ | Was es Ihnen ermöglicht | Downloadlink | Weitere hilfreiche Links |
| --- | --- | --- |--- |
| Admin | Erstellen, Ändern und Löschen von Aktivitäten, Zielgruppen, Angeboten und anderen Objekten (einschließlich [!DNL Recommendations] Entitäten, Kriterien, Designs usw. Die [!DNL Recommendations] APIs sind eine Art Admin-API.) | <UL><li>[Target Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Verwenden von Recommendations-APIs](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target Tutorials* |
| Bereitstellung | Abrufen optimierter und personalisierter Inhalte aus [!DNL Target] für die Bereitstellung an einen Endbenutzer. | [Target Delivery API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Berichterstellung | Exportieren Sie Aktivitätsergebnisse und andere Berichtsergebnisse. | Reporting-APIs sind in der [Target Admin API Postman-Sammlung](https://developers.adobetarget.com/api/#admin-postman-collection). |  |
| Profil | Abrufen und Ändern von in Adobe Target gespeicherten Benutzerprofilen. | [Target Profile API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Es gibt wichtige Unterschiede zwischen [!DNL Target] Admin-APIs (einschließlich [!DNL Recommendations] APIs) und [!DNL Target] Bereitstellungs-APIs:
>
>* Mit Admin-APIs können Sie verschiedene Aspekte von [!DNL Target] , die Sie auch in der [!DNL Target] Benutzeroberfläche. Für Admin-APIs ist eine Authentifizierung erforderlich.
>
>* Mit Bereitstellungs-APIs können Sie Inhalte abrufen. Bereitstellungs-APIs erfordern keine Authentifizierung.
>
>Verwendung [!DNL Target] Administrator-APIs müssen Sie zunächst die Authentifizierung mithilfe von Adobe I/O konfigurieren. Weitere Informationen finden Sie unter [Authentifizierung konfigurieren](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target Tutorials*.
