---
keywords: Implementierung;JavaScript-Bibliothek;js;ATJS;on-device-Entscheidungsfindung;on-device-Entscheidungsfindung;at.js;on-device;on-device;Fehlerbehebung;Fehlerbehebung
description: Erfahren Sie, wie Sie die Fehlerbehebung bei der Entscheidungsfindung auf dem Gerät mit der Bibliothek "at.js"durchführen.
title: Wie kann ich bei der Geräteentscheidung mit der JavaScript-Bibliothek "at.js"eine Fehlerbehebung durchführen?
feature: 'at.js '
role: Developer
translation-type: tm+mt
source-git-commit: 85a17944c7d5924edb1bbabb7531274249ceaaa8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Fehlerbehebung bei der Entscheidung für at.js auf dem Gerät

Führen Sie die folgenden Schritte aus, um die Fehlerbehebung bei der Geräteentscheidung in [!DNL Adobe Target] mit der JavaScript-Bibliothek at.js durchzuführen:

## Schritt 1: Konsolenprotokoll für &quot;at.js&quot;aktivieren

Wenn Sie den URL-Parameter `mboxDebug=1` anhängen, kann at.js Nachrichten in der Konsole Ihres Browsers drucken.

Alle Nachrichten enthalten das Präfix &quot;AT:&quot;, um eine bequeme Übersicht zu erhalten. Um sicherzustellen, dass ein Artefakt erfolgreich geladen wurde, sollte Ihr Konsolenprotokoll Meldungen wie die folgenden enthalten:

```
AT: LD.ArtifactProvider fetching artifact - https://assets.adobetarget.com/your-client-cide/production/v1/rules.json
AT: LD.ArtifactProvider artifact received - status=200
```

Die folgende Abbildung zeigt diese Meldungen im Konsolenprotokoll:

![Konsolenprotokoll mit Artefaktmeldungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/browser-console.png)

## Schritt 2: Überprüfen Sie den Artefaktdownload auf der Registerkarte Netzwerk Ihres Browsers

Öffnen Sie die Registerkarte Netzwerk Ihres Browsers.

So öffnen Sie beispielsweise DevTools in Google Chrome:

1. Drücken Sie Strg+Umschalt+J (Windows) bzw. Befehl+Wahl+J (Mac).
1. Navigieren Sie zur Registerkarte Netzwerk.
1. Filtern Sie Ihre Aufrufe nach Keyword &quot;rules.json&quot;, um sicherzustellen, dass nur die Artefaktregeldatei angezeigt wird.

   Darüber hinaus können Sie nach &quot;/Versand|rules.json/&quot;filtern, um alle [!DNL Target]-Aufrufe und Artefaktregeln.json anzuzeigen.

   ![Registerkarte &quot;Netzwerk&quot;in Google Chrome](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/rule-json.png)

## Schritt 3: Überprüfen des Artikeldownloads für Regeln mithilfe von benutzerdefinierten Ereignissen von at.js

Die at.js-Bibliothek löst zwei neue benutzerdefinierte Ereignis aus, um die Entscheidungsfindung auf dem Gerät zu unterstützen.

* `adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`
* `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`

Sie können sich abonnieren, um diese benutzerdefinierten Ereignis in Ihrer Anwendung auf Aktionen zu prüfen, wenn die Datei mit den Artefaktregeln erfolgreich heruntergeladen wurde oder fehlgeschlagen ist.

Das folgende Beispiel zeigt ein Codebeispiel, das Artefaktdownload-Erfolgs- und Fehler-Ereignis überwacht:

```javascript
document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED, function(e) { 
  console.log("Artifact successfully downloaded", e.detail);
}, false);

document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_FAILED, function(e) { 
  console.log("Artifact failed to download", e.detail);
}, false);
```
