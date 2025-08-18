---
keywords: Targeting; a4t;geo; geotargeting; Genauigkeit von Geotargeting; Land; Bundesland; Stadt; Postleitzahl; dma; Mobilnetzbetreiber; Stadtvorwahl; Regionalcode; Landesvorwahl; Metrocode; Profilskripts; Geotargeting Profilskripts; Geotargeting mobiler Geräte
description: Erfahren Sie, wie Sie Zielgruppen in erstellen [!DNL Adobe Target]  um Benutzende basierend auf ihrer geografischen Position anzusprechen.
title: Kann ich Besuchende nach Standort auswählen?
feature: Audiences
solution: Target,Analytics
exl-id: e4a71a4d-e8f3-4f94-a1a7-fd250f4d5095
source-git-commit: 195028613dec0294c816703b9145e720e3209d74
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 42%

---

# Geo

Verwenden Sie Zielgruppen in [!DNL Adobe Target] , um Benutzer basierend auf ihrer geografischen Position anzusprechen.

Mit Geolokalisierungsparametern können Sie Aktivitäten und Erlebnisse basierend auf der Geografie Ihrer Besuchenden auswählen. Sie können Besucher anhand ihres Standortes (Land, Bundesland, Stadt, Postleitzahl, Breitengrad, Längengrad, DMA oder Mobilnetzbetreiber) ein- oder ausschließen. Diese Daten werden mit jeder [!DNL Target]-Anfrage gesendet und basieren auf der IP-Adresse des Besuchers. Diese Parameter können wie Targeting-Werte ausgewählt werden.

## Erstellen einer Zielgruppe mit Geo-Targeting {#section_49CBFFAAC8694C4AAD3DE4B2DB7B05DE}

1. Klicken Sie in der [!DNL Target] auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Geo]** per Drag-and-Drop in den Bereich Audience Builder .

1. Klicken Sie auf **[!UICONTROL Select]** und wählen Sie dann eine der folgenden Optionen aus:

   * [!UICONTROL Country/Region]
   * [!UICONTROL State]
   * [!UICONTROL City]
   * [!UICONTROL Zip Code]
   * [!UICONTROL Longitude]
   * [!UICONTROL Latitude]
   * [!UICONTROL DMA]
   * [!UICONTROL Mobile Carrier]

   Die Geoinformationen eines Besuchers werden anhand der Ursprungs-IP-Adresse einer [!DNL Target]-Standortanfrage (mBox-Anfrage) bestimmt. Die IP-zu-Geo-Auflösung erfolgt beim ersten Aufruf einer neuen Sitzung. Das bedeutet: Wenn sich die IP-Adresse eines Besuchers während einer Besuchssitzung ändert, basieren die Geoinformationen weiterhin auf der IP-Adresse des ersten Aufrufs.

   [!UICONTROL Mobile Carrier] nutzt [!DNL Target] die IP-Adressregistrierungsdaten (dem der Block von IP-Adressen gehört), um den entsprechenden Mobilnetzbetreiber mithilfe von [Länder-Codes (MCC) und Mobilfunknetzcodes (MNC)](https://www.mcc-mnc.com) zu ermitteln.

1. Geben Sie einen Operator und den entsprechenden Wert an.
1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Done]**.

Die folgende Abbildung zeigt eine Zielgruppe für Benutzer, die von einem Breitengrad größer als 44° und einem Längengrad kleiner als 22° auf die Aktivität zugreifen.

![target_geo-Bild](assets/target_geo.png)

## Genauigkeit {#section_D63D5FFCB49C42F9933AFD0BD7C79DF1}

Die Genauigkeit von Geotargeting hängt von verschiedenen Faktoren ab. WLAN-Verbindungen sind genauer als Mobilfunknetze. Wenn ein Besucher eine Mobilfunkdatenverbindung verwendet, kann die Genauigkeit der Geo-Suche durch den Standort, die Datenbeziehung des Anbieters zu [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester) und andere Faktoren beeinflusst werden. Durch Mobilfunkmasten gestützte Netzwerkverbindungen sind in der Regel weniger genau als kabelgebundene oder WLAN-Verbindungen. Außerdem kann die IP-Adresse eines Besuchers dem ISP-Standort des Besuchers zugeordnet werden, der möglicherweise nicht mit dem tatsächlichen Standort des Besuchers übereinstimmt. Einige Probleme mit der geografischen Lage auf Mobilgeräten können mithilfe der [Geolocation-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) gelöst werden.

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

## Verwenden von Geotargeting in Profilskripten {#section_92C93138542C4A94997E3F4BE3F5DA28}

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

## Verwenden von Geotargeting-Werten als Token {#section_E7F7FDF62C3B4934A6565D04B24655F6}

Sie können `profile.geolocation` Werte direkt als Token in Angeboten, Plug-ins usw. verwenden.

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

Die folgenden Fragen werden häufig zum Geo-Targeting gestellt:

### Wie gebe ich den Breiten- und Längengrad an?

+++Details anzeigen
* Der Wert für Breiten- und Längengrad sollte ein numerischer Wert in Grad sein.
* Der Wert für Breiten- und Längengrad kann eine maximale Genauigkeit von fünf Dezimalstellen haben.
* Der Wert für den Breitengrad muss zwischen -90 und 90 liegen.
* Der Wert für den Längengrad muss zwischen -180 und 180 liegen.

+++

### Wie funktioniert Geotargeting für Mobilgeräte?

+++Details anzeigen
Die meisten Benutzer mobiler Geräte greifen über WLAN auf Inhalte zu, was bedeutet, dass das IP-basierte Geotargeting von [!DNL Target] genauso präzise ist wie auf einem Desktop. Funkzellenbasierte Verbindungen können ungenauer sein, da die IP-Adresse des Besuchers auf der Funkzelle basiert, bei der das Signal erfasst wird. Einige Probleme mit der geografischen Lage auf Mobilgeräten können mithilfe der [Geolocation-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) gelöst werden.

+++

### Wie behandelt die Geo-Funktion Besucher von AOL?

+++Details anzeigen
Aufgrund der Art und Weise, wie AOL seinen Traffic weiterleitet, können [!DNL Target] ihn nur auf Länderebene ansprechen. So richtet sich beispielsweise eine an Frankreich gerichtete Kampagne erfolgreich an AOL-Nutzer in Frankreich. Doch eine auf Paris ausgerichtete Kampagne richtet sich nicht erfolgreich an alle Pariser Nutzer. Wenn Sie Ihr Targeting speziell auf AOL-Benutzer ausrichten möchten, können Sie das Feld Region auf „aol“ einstellen. Sie können Ihr Targeting auf AOL-Benutzer in den USA ausrichten, indem Sie zwei Targeting-Bedingungen festlegen - das Land muss genau mit „USA“ und die Region genau mit „aol“ übereinstimmen.

+++

### Welche Standort-Granularität bietet Geo-Targeting?

+++Details anzeigen
* Land - global
* Bundesland/-staat/Region - global
* Ort - global
* Postleitzahl - USA, Deutschland, Kanada
* DMA/ITV (GB) - USA, GB
* Mobilnetzbetreiber - global

+++

### Wie kann ich meine Aktivitäten als Benutzer von einem anderen Standort testen?

+++Details anzeigen
* **at.js 1.*x***: Sie können Ihre IP-Adresse mit einer IP-Adresse von einem anderen Speicherort überschreiben und den `mboxOverride.browserIp url`-Parameter verwenden. Wenn sich Ihr Unternehmen beispielsweise in Großbritannien befindet, Ihre globale Kampagne jedoch auf Besucher in Auckland, Neuseeland, ausgerichtet ist, verwenden Sie diesen URL-Stil unter der Annahme, dass `60.234.0.39` eine IP-Adresse in Auckland ist:

  `https://www.mycompany.com?mboxOverride.browserIp=60.234.0.39`

  Löschen Sie Ihre Cookies, bevor Sie die Aktivität testen.

  >[!NOTE]
  >
  >`mboxOverride.browserIp` wird in at.js 1 unterstützt.*x*, zur Verfügung. Diese Funktion wird in at.js 2 nicht unterstützt.*x*.

* **at.js 2.*x***: Überschreiben Ihrer IP-Adresse mit at.js 2.*x* installieren Sie eine Browser-Erweiterung/-Plug-in (z. B. den X-Forwarded-For-Header für Chrome oder Firefox). Mit dieser Erweiterung können Sie die Kopfzeile „x-forwarded-for“ in Ihren Seitenanfragen übergeben.

+++

### Wie werden Gebiete wie Puerto Rico und Hongkong in die Geo-Targeting-Struktur eingeordnet?

+++Details anzeigen
Puerto Rico, Hongkong und andere Gebiete werden als separate Länderwerte verarbeitet.

+++

### Erfasst (und speichert) [!DNL Target] Informationen wie Postleitzahl, wenn die Aktivität auf Funktionen zum Targeting von Orten abzielt?

+++Details anzeigen
Nein, [!DNL Target] verwendet Geodaten nur während der Sitzung, dann werden die Daten verworfen.

+++

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
