---
description: Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.
keywords: Implementierung;API;Profil;Profil-API-Einstellungen
seo-description: Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.
seo-title: Profil-API-Einstellungen
solution: Target
subtopic: Erste Schritte
title: Profil-API-Einstellungen
topic: Standard
uuid: 481b4a14-f10f-47cd-988d-9e6b8c4d5c00
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Profil-API-Einstellungen{#profile-api-settings}

Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.

Adobe Target erstellt und pflegt ein Profil für jeden individuellen Benutzer. Dieses Profil wird auf dem Target Edge-Cluster gespeichert und nach jedem Besuch in Echtzeit aktualisiert. Sie können Profile jedoch individuell oder per Massenaktualisierung via API aktualisieren.

Für noch mehr Sicherheit können Sie festlegen, dass beim API-Aufruf für die Massenaktualisierung ein gültiges Zugriffstoken im Header der Anforderung übergeben werden muss. Benutzer mit Genehmigerberechtigungen können API-Authentifizierungstoken generieren und aktivieren.

**So fordern Sie die Authentifizierung und so generieren Sie ein Zugriffstoken mithilfe der Target-Benutzeroberfläche:**

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]**.
1. Aktivieren oder deaktivieren Sie unter **[!UICONTROL Profil-API-Einstellungen]** in der Dropdownliste **Authentifizierung erfordern]die Authentifizierungsanforderungen.[!UICONTROL **

   ![](assets/profile_api_settings.png)

1. (Bedingt) Wenn Sie Authentifizierungsanforderungen aktiviert haben, klicken Sie auf **[!UICONTROL Profilauthentifizierungstoken generieren]**.

   ![](assets/profile_api_settings_2.png)

   Das Token läuft gemäß der Angabe im Feld [!UICONTROL Läuft ab in] ab.

   >[!NOTE]
   >
   >Sie können auch per API ein Profilauthentifizierungstoken generieren. Weitere Informationen finden Sie unter [Profile](https://developers.adobetarget.com/api/#profiles) auf der [Entwickler-Website von Adobe Target](https://developers.adobetarget.com/).

1. Kopieren Sie das Token und fügen Sie es im Header der Anforderung im folgenden Format ein: „Autorisierung“ : „Bearer“

Klicken Sie auf [!UICONTROL Profilauthentifizierungstoken erneut generieren], um das Token bei Bedarf erneut zu generieren.

>[!IMPORTANT]
>
>Wenn Sie dieses Token zurücksetzen, schlagen API-Aufrufe mit dem aktuellen Token fehl. Dies erfordert eine Aktualisierung von Skripten oder Apps, die dieses Token verwenden.

