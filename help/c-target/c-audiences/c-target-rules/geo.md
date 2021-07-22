---
keywords: Targeting; a4t;geo; geotargeting; Genauigkeit von Geotargeting; Land; Bundesland; Stadt; Postleitzahl; dma; Mobilnetzbetreiber; Stadtvorwahl; Regionalcode; Landesvorwahl; Metrocode; Profilskripts; Geotargeting Profilskripts; Geotargeting mobiler Geräte
description: Erfahren Sie, wie Sie in [!DNL Adobe Target] Zielgruppen erstellen, um Benutzer anhand ihres geografischen Standorts anzusprechen.
title: Kann ich Besucher nach Standort ansprechen?
feature: Zielgruppen
solution: Target,Analytics
exl-id: e4a71a4d-e8f3-4f94-a1a7-fd250f4d5095
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 50%

---

# Geo

Verwenden Sie Zielgruppen in [!DNL Adobe Target], um Benutzer anhand ihres geografischen Standorts auszuwählen.

Mit Geo-Positionsparametern können Sie Aktivitäten und Erlebnisse anhand der geografischen Daten Ihrer Besucher ansprechen. Sie können Besucher anhand ihres Standortes (Land, Bundesland, Stadt, Postleitzahl, Breitengrad, Längengrad, DMA oder Mobilnetzbetreiber) ein- oder ausschließen. Diese Daten werden bei jeder [!DNL Target]-Anfrage gesendet und basieren auf der IP-Adresse des Besuchers. Diese Parameter können wie Targeting-Werte ausgewählt werden.

## Erstellen einer Zielgruppe mit Geotargeting {#section_49CBFFAAC8694C4AAD3DE4B2DB7B05DE}

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Geo]** in den Bereich Audience Builder .

1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

   * [!UICONTROL Land/Region]
   * [!UICONTROL Status]
   * [!UICONTROL Stadt]
   * [!UICONTROL Postleitzahl]
   * [!UICONTROL Längengrad]
   * [!UICONTROL Breitengrad]
   * [!UICONTROL DMA]
   * [!UICONTROL Mobilnetzbetreiber]

   Die IP-Adresse eines Besuchers wird mit einer Mbox-Anfrage einmal pro Besuch (Sitzung) übermittelt, um Geotargeting-Parameter für den betreffenden Besucher aufzulösen.

   Für [!UICONTROL Mobilnetzbetreiber] verwendet [!DNL Target] die IP-Adressregistrierungsdaten (der Eigentümer des IP-Adressblocks ist), um den entsprechenden Mobilnetzbetreiber mithilfe von [Mobile Country Codes (MCC) und Mobile Network Codes (MNC)](https://www.mcc-mnc.com) zu bestimmen.

1. Geben Sie einen Operator und den entsprechenden Wert an.
1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

Die folgende Abbildung zeigt eine Zielgruppe, die Benutzer auswählt, die von einem Breitengrad größer als 44° und einem Längengrad kleiner als 22° auf die Aktivität zugreifen.

![](assets/target_geo.png)

## Genauigkeit {#section_D63D5FFCB49C42F9933AFD0BD7C79DF1}

Die Genauigkeit von Geotargeting hängt von verschiedenen Faktoren ab. WLAN-Verbindungen sind genauer als Mobilfunknetze. Wenn der Besucher eine mobile Datenverbindung nutzt, kann die Genauigkeit der Standortsuche durch den Standort, die Datenbeziehung zwischen dem Anbieter und [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester) und anderen Faktoren beeinflusst werden. Durch Mobilfunkmasten gestützte Netzwerkverbindungen sind in der Regel weniger genau als kabelgebundene oder WLAN-Verbindungen. Außerdem kann die IP-Adresse eines Besuchers dem ISP-Standort des Besuchers zugeordnet werden, der möglicherweise nicht mit dem tatsächlichen Standort des Besuchers übereinstimmt. Einige Probleme mit dem mobilen geografischen Standort können mit der [Geolocation-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) behoben werden.

In der folgenden Tabelle finden Sie Informationen zur Genauigkeit IP-basierter Standortdaten von [DigitalEnvoy](https://www.digitalelement.com/solutions/) für kabelgebundene oder WLAN-Internetverbindungen. DigitalEnvoy bietet die präzisesten Daten in der Branche. Die Gesamtgenauigkeit beläuft sich auf 99,9 % auf Länderebene und auf bis zu 97 % auf Stadtebene. Die Daten zur Genauigkeit sind nicht für durch Mobilfunkmasten gestützte Netzwerke gültig.

| Land | Land | Stadt | Region |
|--- |--- |--- |--- |
| USA | 99,99 % | 96 % | 94 % |
| Kanada | 99,99 % | 96 % | 94 % |
| Europa | 99,99 % |  |  |
| GB | 99,99 % |  | 87 % |
| Deutschland | 99,99 % | 95 % | 93 % |
| Skandinavien | 99 % | ~ 91-93 % | ~ 85 % |
| Spanien | 99,99 % | ~ 90 % | ~ 85-99 % |
| Asien | 99 % | ~ 95 % | ~ 91-93 % |
| Japan | 99,99 % | ~ 95 % | ~ 91-93 % |
| Australien | 99,99 % | 94 % | 91 % |

## Geotargeting in Profilskripten verwenden {#section_92C93138542C4A94997E3F4BE3F5DA28}

Sie können Geoinformationen für Profilskripts verwenden.

Beispiele:

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`

Sie können beispielsweise einen Zielausdruck mit der Bezeichnung „From North America“ mit folgendem Code schreiben:

`return profile.geolocation.country == 'united states' || profile.geolocation.country == 'canada' || profile.geolocation.country == 'mexico';`

## Geotargeting-Werte als Token verwenden {#section_E7F7FDF62C3B4934A6565D04B24655F6}

Sie können `profile.geolocation` -Werte direkt als Token in Angeboten, Plugins usw. verwenden.

Beispiele:

* `${profile.geolocation.country}`
* `${profile.geolocation.state}`
* `${profile.geolocation.city}`
* `${profile.geolocation.zip}`
* `${profile.geolocation.dma}`
* `${profile.geolocation.domainName}`
* `${profile.geolocation.ispName}`
* `${profile.geolocation.connectionSpeed}`
* `${profile.geolocation.mobileCarrier}`
* `${profile.geolocation.latitude}`
* `${profile.geolocation.longitude}`

## Häufig gestellte Fragen zum Geotargeting {#section_DD308A53AF0F48FA8C81423580561FE7}

Die folgenden Fragen werden häufig zum Geotargeting gestellt:

### Wie kann ich den Längen- und Breitengrad festlegen?

* Der Wert für Breiten- und Längengrad sollte ein numerischer Wert in Grad sein.
* Der Wert für Breiten- und Längengrad kann eine maximale Genauigkeit von fünf Dezimalstellen haben.
* Der Wert für den Breitengrad muss zwischen -90 und 90 liegen.
* Der Wert für den Längengrad muss zwischen -180 und 180 liegen.

### Wie funktioniert Geotargeting für Mobilgeräte?

Die meisten Benutzer von Mobilgeräten greifen über WLAN auf Inhalte zu. Das bedeutet, dass das IP-basierte Geotargeting von [!DNL Target] genauso präzise ist wie auf einem Desktop. Funkzellenbasierte Verbindungen können ungenauer sein, da die IP-Adresse des Besuchers auf der Funkzelle basiert, bei der das Signal erfasst wird. Einige Probleme mit dem mobilen geografischen Standort können mit der [Geolocation-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) behoben werden.

### Wie geht die Geo-Funktion mit Besuchern von AOL um?

Aufgrund der Art und Weise, wie AOL seinen Traffic verwaltet, kann [!DNL Target] nur auf Landesebene für diese Zielgruppen sorgen. Eine Kampagne, die beispielsweise auf Frankreich ausgerichtet ist, richtet sich erfolgreich an AOL-Benutzer in Frankreich. Eine auf Paris abzielende Kampagne zielt jedoch nicht erfolgreich auf AOL-Benutzer in Paris ab. Wenn Sie Ihr Targeting speziell auf AOL-Benutzer ausrichten möchten, können Sie das Feld Region auf „aol“ einstellen. Sie können Ihr Targeting auf AOL-Benutzer in den USA ausrichten, indem Sie zwei Targeting-Bedingungen festlegen - das Land muss genau mit „USA“ und die Region genau mit „aol“ übereinstimmen.

### Welche Ortsgenauigkeit bietet das Geotargeting?

* Land - global
* Bundesland/-staat/Region - global
* Ort - global
* Postleitzahl - USA, Deutschland, Kanada
* DMA/ITV (GB) - USA, GB
* Mobilnetzbetreiber - global

### Wie kann ich meine Aktivitäten als Benutzer von einem anderen Standort testen?

* **at.js 1.*x***: Sie können Ihre IP-Adresse durch eine IP-Adresse von einem anderen Standort ersetzen und den  `mboxOverride.browserIp url` Parameter verwenden. Wenn sich Ihr Unternehmen beispielsweise in Großbritannien befindet, Ihre globalen Kampagnen jedoch auf Besucher in Auckland in Neuseeland abzielen, verwenden Sie diesen URL-Stil unter der Annahme, dass `60.234.0.39` eine IP-Adresse in Auckland ist:

   `https://www.mycompany.com?mboxOverride.browserIp=60.234.0.39`

   Löschen Sie die Cookies, bevor Sie die Aktivität testen.

   >[!NOTE]
   >
   >`mboxOverride.browserIp` wird in at.js 1. unterstützt.*x*, zur Verfügung. Diese Funktion wird in at.js 2 nicht unterstützt.*x*.

* **at.js 2.*x***: So überschreiben Sie Ihre IP-Adresse mit at.js 2.*x*, installieren Sie eine Browsererweiterung/-Plug-in (z. B. X-Forwarded-For-Header für Chrome oder Firefox). Mit dieser Erweiterung können Sie den Header x-forwarded-for in Ihren Seitenanfragen übergeben.

### Wie werden Gebiete wie Puerto Rico und Hongkong der Geotargeting-Struktur zugeordnet?

Puerto Rico, Hongkong und andere Gebiete werden als separate Länderwerte verarbeitet.

### Erfasst (und speichert) [!DNL Target] Informationen wie die Postleitzahl, wenn Aktivitäten mit Targeting-Funktionen für geografische Standorte angesprochen werden?

Nein, [!DNL Target] verwendet nur während der Sitzung Geodaten, dann werden die Daten verworfen.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
