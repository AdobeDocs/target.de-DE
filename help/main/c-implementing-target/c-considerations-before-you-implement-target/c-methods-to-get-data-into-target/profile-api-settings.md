---
keywords: Implementierung;API;Profil;Profil-API-Einstellungen;Authentifizierungstoken
description: Erfahren Sie, wie Sie die Authentifizierung für Batch-Aktualisierungen über Adobe konfigurieren [!DNL Target] APIs erstellen und ein Profilauthentifizierungstoken generieren.
title: Wie kann ich mithilfe der Profil-API-Einstellungen Batch-Aktualisierungen aktivieren oder deaktivieren?
feature: APIs/SDKs
role: Developer
exl-id: 6346e11b-0853-47f1-9706-69e8635a6f25
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 61%

---

# Profil-API-Einstellungen

Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen über [!DNL Adobe Target] APIs erstellen und ein Profilauthentifizierungstoken generieren.

[!DNL Adobe Target] erstellt und pflegt ein Profil für jeden individuellen Benutzer. Dieses Profil wird im [!DNL Target] Edge-Cluster und wird in Echtzeit nach jedem Besuch aktualisiert; Sie können ein Profil jedoch einzeln oder stapelweise über die API aktualisieren.

Für noch mehr Sicherheit können Sie festlegen, dass beim API-Aufruf für die Massenaktualisierung ein gültiges Zugriffstoken im Header der Anforderung übergeben werden muss.

**So fordern Sie die Authentifizierung und so generieren Sie ein Zugriffstoken mithilfe der Target-Benutzeroberfläche:**

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. under **[!UICONTROL Profil-API]** Folie **[!UICONTROL Authentifizierung erforderlich]** Wechsel zur aktivierten oder deaktivierten Position.

   ![](assets/profile_api_settings.png)

1. (Bedingt) Wenn Sie Authentifizierungsanforderungen aktiviert haben, klicken Sie auf **[!UICONTROL Neues Profilauthentifizierungstoken generieren]**.

   ![](assets/profile_api_settings_2.png)

   Das Token läuft gemäß der Angabe im Feld [!UICONTROL Läuft ab in] ab.

   Für die Generierung eines Authentifizierungstokens benötigen Sie eine der folgenden Benutzerberechtigungen:

   * Mindestens die Berechtigung [!UICONTROL Bearbeiter] (oder [!UICONTROL Genehmiger])

      Weitere Informationen für [!DNL Target Standard]-Kunden finden Sie unter [Festlegen von Rollen und Berechtigungen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) für *Benutzer*. Weitere Informationen für [!DNL Target Premium]-Kunden finden Sie unter [Konfigurieren von Enterprise-Berechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Administratorrolle auf der Ebene Arbeitsbereich/Produktprofil

      Arbeitsbereiche stehen nur [!DNL Target Premium]-Kunden zur Verfügung. Weitere Informationen finden Sie unter [Konfigurieren von Enterprise-Berechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Administratorrechte (Berechtigung „Sysadmin“) auf der [!DNL Adobe Target]-Produktebene
   >[!NOTE]
   >
   >Sie können auch per API ein Profilauthentifizierungstoken generieren. Weitere Informationen finden Sie unter [Profile](https://developers.adobetarget.com/api/#profiles) auf der [Adobe Target-Entwickler-Website](https://developers.adobetarget.com/).

1. Kopieren Sie das Token und fügen Sie es im Header der Anforderung im folgenden Format ein: „Autorisierung“ : „Bearer“

Klicken [!UICONTROL Neues Profilauthentifizierungstoken generieren] , um das Token nach Bedarf neu zu generieren.

>[!IMPORTANT]
>
>Wenn Sie dieses Token zurücksetzen, schlagen API-Aufrufe mit dem aktuellen Token fehl. Dies erfordert eine Aktualisierung von Skripten oder Apps, die dieses Token verwenden.
