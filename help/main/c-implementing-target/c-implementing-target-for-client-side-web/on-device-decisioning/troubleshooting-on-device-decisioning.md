---
keywords: Implementierung;JavaScript-Bibliothek;js;at.js;On-Device Decisioning;on device decisioning;at.js;on-device;on device;Fehlerbehebung;Problembehebung
description: Erfahren Sie, wie Sie mit der at.js-Bibliothek eine Fehlerbehebung bei Entscheidungen auf dem Gerät durchführen.
title: Wie kann ich eine Fehlerbehebung bei der On-Device-Entscheidungsfindung mit der JavaScript-Bibliothek at.js durchführen?
feature: at.js
role: Developer
exl-id: 76bb9393-1560-455b-9d95-91576faee1f2
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# Fehlerbehebung bei der geräteinternen Entscheidungsfindung für at.js

Führen Sie die folgenden Schritte aus, um eine Fehlerbehebung bei der gerätebezogenen Entscheidungsfindung in [!DNL Adobe Target] mit der JavaScript-Bibliothek at.js:

## Schritt 1: Konsolenprotokoll für at.js aktivieren

Anfügen des URL-Parameters `mboxDebug=1` ermöglicht at.js das Drucken von Nachrichten in der Browser-Konsole.

Alle Nachrichten enthalten das Präfix &quot;AT:&quot;, um einen einfachen Überblick zu erhalten. Um sicherzustellen, dass ein Artefakt erfolgreich geladen wurde, sollte Ihr Konsolenprotokoll Meldungen ähnlich den folgenden enthalten:

```
AT: LD.ArtifactProvider fetching artifact - https://assets.adobetarget.com/your-client-cide/production/v1/rules.json
AT: LD.ArtifactProvider artifact received - status=200
```

Die folgende Abbildung zeigt diese Meldungen im Konsolenprotokoll:

![Konsolenprotokoll mit Artefaktmeldungen](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/browser-console.png)

## Schritt 2: Überprüfen Sie den Download des Regelartefakts auf der Registerkarte &quot;Netzwerk&quot;Ihres Browsers.

Öffnen Sie die Registerkarte Netzwerk Ihres Browsers.

So öffnen Sie beispielsweise DevTools in Google Chrome:

1. Drücken Sie Strg+Umschalt+J (Windows) bzw. Befehlstaste+Wahltaste+J (Mac).
1. Navigieren Sie zur Registerkarte Netzwerk .
1. Filtern Sie Ihre Aufrufe nach dem Keyword &quot;rules.json&quot;, um sicherzustellen, dass nur die Datei mit den Artefaktregeln angezeigt wird.

   Darüber hinaus können Sie nach &quot;/delivery|rules.json/&quot;filtern, um alle [!DNL Target] Aufrufe und Artefakt rules.json.

   ![Registerkarte &quot;Netzwerk&quot;in Google Chrome](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/rule-json.png)

## Schritt 3: Überprüfen des Herunterladens des Regelartefakts mit benutzerdefinierten at.js-Ereignissen

Die at.js-Bibliothek sendet zwei neue benutzerspezifische Ereignisse, um die Entscheidungsfindung auf dem Gerät zu unterstützen.

* `adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`
* `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`

Sie können diese benutzerdefinierten Ereignisse in Ihrer Anwendung abonnieren, um sie bei Erfolg oder Fehlschlagen des Dateidownloads für Artefaktregeln zu überwachen.

Das folgende Beispiel zeigt ein Beispiel für Code, der auf Erfolgs- und Fehlerereignisse beim Artefakt-Download wartet:

```javascript
document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED, function(e) { 
  console.log("Artifact successfully downloaded", e.detail);
}, false);

document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_FAILED, function(e) { 
  console.log("Artifact failed to download", e.detail);
}, false);
```
