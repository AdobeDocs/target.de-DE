---
keywords: implementation;api;profile;profile api settings;authentication token
description: Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.
title: Profil-API-Einstellungen
subtopic: Getting Started
topic: Standard
uuid: 481b4a14-f10f-47cd-988d-9e6b8c4d5c00
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 64%

---


# Profil-API-Einstellungen{#profile-api-settings}

Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.

[!DNL Adobe Target] erstellt und pflegt ein Profil für jeden individuellen Benutzer. This profile is stored on the [!DNL Target] edge cluster and is updated in real time after every visit, however, you can update a profile individually or in bulk via API.

Für noch mehr Sicherheit können Sie festlegen, dass beim API-Aufruf für die Massenaktualisierung ein gültiges Zugriffstoken im Header der Anforderung übergeben werden muss. Users with [!UICONTROL Approver] permissions can generate and enable profile API authentication tokens.

**So fordern Sie die Authentifizierung und so generieren Sie ein Zugriffstoken mithilfe der Target-Benutzeroberfläche:**

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Schieben Sie unter **[!UICONTROL Profil-API]** den Umschalter **[!UICONTROL Authentifizierung]** erforderlich auf die aktivierte oder deaktivierte Position.

   ![](assets/profile_api_settings.png)

1. (Conditional) If you enabled authentication requirements, click **[!UICONTROL Generate New Pfofile Authentication Token]**.

   ![](assets/profile_api_settings_2.png)

   Das Token läuft gemäß der Angabe im Feld [!UICONTROL Läuft ab in] ab.

   >[!NOTE]
   >
   >Sie können auch per API ein Profilauthentifizierungstoken generieren. Weitere Informationen finden Sie unter [Profile](https://developers.adobetarget.com/api/#profiles) auf der [Adobe Target-Entwickler-Website](https://developers.adobetarget.com/).

1. Kopieren Sie das Token und fügen Sie es im Header der Anforderung im folgenden Format ein: „Autorisierung“ : „Bearer“

Click [!UICONTROL Generate New Profile Authentication Token] to regenerate the token as needed.

>[!IMPORTANT]
>
>Wenn Sie dieses Token zurücksetzen, schlagen API-Aufrufe mit dem aktuellen Token fehl. Dies erfordert eine Aktualisierung von Skripten oder Apps, die dieses Token verwenden.
