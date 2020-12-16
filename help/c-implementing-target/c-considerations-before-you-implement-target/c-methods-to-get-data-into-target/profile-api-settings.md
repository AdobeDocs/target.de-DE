---
keywords: implementation;api;profile;profile api settings;authentication token
description: Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen über Adobe Target APIs und generieren Sie ein Profil-Authentifizierungstoken.
title: Profil-API-Einstellungen in Adobe Target
feature: api
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 40%

---


# Profil-API-Einstellungen

Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen über Adobe Target APIs und generieren Sie ein Profil-Authentifizierungstoken.

[!DNL Adobe Target] erstellt und pflegt ein Profil für jeden individuellen Benutzer. Dieses Profil wird im Edge-Cluster [!DNL Target] gespeichert und nach jedem Besuch in Echtzeit aktualisiert. Sie können ein Profil jedoch einzeln oder stapelweise über die API aktualisieren.

Für noch mehr Sicherheit können Sie festlegen, dass beim API-Aufruf für die Massenaktualisierung ein gültiges Zugriffstoken im Header der Anforderung übergeben werden muss.

**So fordern Sie die Authentifizierung und so generieren Sie ein Zugriffstoken mithilfe der Target-Benutzeroberfläche:**

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Schieben Sie unter **[!UICONTROL Profil-API]** den Umschalter **[!UICONTROL Authentifizierung erforderlich]** zur aktivierten oder deaktivierten Position.

   ![](assets/profile_api_settings.png)

1. (Bedingt) Wenn Sie die Authentifizierungsanforderungen aktiviert haben, klicken Sie auf **[!UICONTROL Neues Profil-Authentifizierungstoken erstellen]**.

   ![](assets/profile_api_settings_2.png)

   Das Token läuft gemäß der Angabe im Feld [!UICONTROL Läuft ab in] ab.

   Sie benötigen eine der folgenden Benutzerberechtigungen, um ein Authentifizierungstoken zu generieren:

   * Mindestens [!UICONTROL Berechtigung &quot;Editor]&quot;(oder [!UICONTROL Genehmiger])

      Weitere Informationen für [!DNL Target Standard]-Kunden finden Sie unter [Rollen und Berechtigungen angeben](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Benutzer*. Weitere Informationen für [!DNL Target Premium]-Kunden finden Sie unter [Unternehmensberechtigungen konfigurieren](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Administratorrolle auf der Profil-/Arbeitsbereich-Ebene

      Arbeitsflächen stehen nur für [!DNL Target Premium]-Kunden zur Verfügung. Weitere Informationen finden Sie unter [Unternehmensberechtigungen konfigurieren](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Administratorrechte (Berechtigung &quot;Sysadmin&quot;) auf der [!DNL Adobe Target]-Produktebene
   >[!NOTE]
   >
   >Sie können auch per API ein Profilauthentifizierungstoken generieren. Weitere Informationen finden Sie unter [Profile](https://developers.adobetarget.com/api/#profiles) auf der [Adobe Target-Entwickler-Website](https://developers.adobetarget.com/).

1. Kopieren Sie das Token und fügen Sie es im Header der Anforderung im folgenden Format ein: „Autorisierung“ : „Bearer“

Klicken Sie auf [!UICONTROL Neues Profil-Authentifizierungstoken erstellen], um das Token nach Bedarf neu zu generieren.

>[!IMPORTANT]
>
>Wenn Sie dieses Token zurücksetzen, schlagen API-Aufrufe mit dem aktuellen Token fehl. Dies erfordert eine Aktualisierung von Skripten oder Apps, die dieses Token verwenden.
