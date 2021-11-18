---
keywords: benutzerspezifische Ereignisse; at.js; Anforderung fehlgeschlagen; Anforderung erfolgreich; Inhalt-Rendering fehlgeschlagen; Erfolgreiches Rendering von Inhalten; Bibliothek geladen; Request starten; Start des Inhalts-Rendervorgangs; kein Content Rendering von Angeboten; Redirect von Inhalts-Rendering
description: Verwenden benutzerdefinierter Ereignisse für die Adobe [!DNL Target] at.js-JavaScript-Bibliothek, die benachrichtigt werden soll, wenn eine Mbox-Anforderung oder ein Angebot erfolgreich war oder fehlgeschlagen ist.
title: Wie verwende ich benutzerdefinierte at.js-Ereignisse?
feature: at.js
role: Developer
exl-id: 4073210b-b782-48a7-8b69-29eb5cd98fd5
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 83%

---

# Benutzerdefinierte at.js-Ereignisse

Informationen zu `at.js custom events`, die Sie darüber informieren, ob eine Mbox-Anforderung oder ein Angebot erfolgreich war oder fehlgeschlagen ist.

In der Vergangenheit ließ mbox.js (jetzt nicht mehr unterstützt) anderen auf der Seite ausgeführten JavaScript-Code nicht wissen, was hinter den Kulissen geschieht. Dank der Weiterentwicklung von at.js konnten wir dieses Problem glücklicherweise beheben.

Laut unseren Kunden gibt es mehrere Szenarien, über die sie gerne informiert werden möchten, darunter:

* Fehlschlagen einer Mbox-Abfrage aufgrund einer Zeitüberschreitung, des falschen Status-Codes, eines JSON-Parsingfehlers usw.
* Erfolg einer Mbox-Abfrage
* Fehlschlagen der Wiedergabe eines Angebots aufgrund eines fehlenden Wrapper-Mbox-Elements, eines nicht gefundenen Selektors usw.
* Erfolg der Angebotswiedergabe. Anwendung von DOM-Änderungen.

Vordefinierte Ereignisse mit einer Struktur, die die Extrahierung von erforderlichen Daten je nach Ereignistyp ermöglicht

Sicherstellung, dass Ereignisse in verschiedenen Szenarien eingesetzt werden können, benutzerdefinierte Ereignisse über ein Nutzlastobjekt verfügen, das der Detaileinheit des Ereignisobjekts zugeordnet ist (und an den Handler übermittelt wird). Des Weiteren auch das Verhindern der Übermittlung von Zeichenfolgen wie Ereignisnamen. Die Ereignisse werden mithilfe des `adobe.target.event`-Namespace als Konstanten dargestellt.

## Struktur {#section_0E5C9A13DE234A5DAECBCBF9F23F94FE}

| Schlüssel | Typ | Beschreibung |
|--- |--- |--- |
| Typ | Zeichenfolge | Es gibt verschiedene Szenarien, in denen Sie über die Unterstützung in Bezug auf die Ablaufverfolgungs-, Debugging- und Anpassungsinteraktionen mit at.js benachrichtigt werden möchten.<br>Jedes im Folgenden aufgeführte benutzerspezifische Ereignis besitzt zwei Formate: eine „Konstante“ und einen „Zeichenfolgenwert“.<ul><li>**Konstante:** `adobe.target.event.` vorangestellt, in Großbuchstaben dargestellt, enthalten Unterstriche. Verwenden Sie die Konstante, um benutzerspezifische Ereignisse zu abonnieren, *nachdem* at.js geladen, jedoch *bevor* die Mbox-Antwort empfangen wurde.</li><li>**Zeichenfolgenwerte:** Kleinbuchstaben, enthalten Gedankenstriche. Verwenden Sie den Zeichenfolgenwert, um benutzerspezifische Ereignisse zu abonnieren, *bevor* at.js geladen wird.</li></ul>**Anforderung fehlgeschlagen**<br> Konstante: `adobe.target.event.REQUEST_FAILED`<br>Zeichenfolgenwert: `at-request-failed`<br>Beschreibung: Eine Mbox-Anfrage schlug aufgrund eines Timeouts, eines falschen Status-Codes, eines JSON-Analysefehlers usw. fehl.<br>**Anfrage war erfolgreich**<br> Konstante: `adobe.target.event.REQUEST_SUCCEEDED`<br>Zeichenfolgenwert: `at-request-succeeded`<br>Beschreibung: Eine Mbox-Anfrage war erfolgreich.<br>**Inhaltswiedergabe fehlgeschlagen**<br> Konstante: `adobe.target.event.CONTENT_RENDERING_FAILED`<br>Zeichenfolgenwert: `at-content-rendering-failed`<br>Beschreibung: Fehlschlagen der Wiedergabe eines Angebots aufgrund eines fehlenden Wrapper-Mbox-Elements, eines nicht gefundenen Selektors usw.<br>**Inhaltswiedergabe erfolgreich**<br> Konstante: `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`<br>Zeichenfolgenwert: `at-content-rendering-succeeded`<br>Beschreibung: Das Angebot wurde erfolgreich wiedergegeben. Anwendung von DOM-Änderungen.<br>**Bibliothek geladen**<br> Konstante: `adobe.target.event.LIBRARY_LOADED`<br>Zeichenfolgenwert: `at-library-loaded`<br>Beschreibung: Es ist ideal, dieses Ereignis zu verfolgen, nachdem at.js vollständig geladen wurde. Mit diesem Ereignis können Sie die Ausführung der globalen Mbox anpassen. Sie können dieses Ereignis auch verwenden, um die globale Mbox zu deaktivieren und dieses Ereignis anschließend zu überwachen, um die globale Mbox später auszulösen.<br>**Beginn Anfrage**<br> Konstante: `adobe.target.event.REQUEST_START`<br>Zeichenfolgenwert: `at-request-start`<br>Beschreibung: Dieses Ereignis wird ausgelöst, bevor eine HTTP-Anfrage ausgeführt wird. Sie können dieses Ereignis für Leistungsmessungen mit der Resource Timing-API verwenden.<br>**Beginn Wiedergabe**<br> Konstante: `adobe.target.event.CONTENT_RENDERING_START`<br>Zeichenfolgenwert: `at-content-rendering-start`<br>Beschreibung: Dieses Ereignis wird ausgelöst, bevor die Auswahl des Selektors gestartet wird und der Inhalt auf der Seite wiedergegeben wird. Sie können dieses Ereignis verwenden, um den Inhaltsdarstellungsfortschritt nachzuverfolgen.<br>**Inhaltswiedergabe, keine Angebote**<br> Konstante: `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`<br>Zeichenfolgenwert: `at-content-rendering-no-offers`<br>Beschreibung: Dieses Ereignis wird ausgelöst, wenn keine Angebote zurückgegeben werden.<br>**Inhaltswiedergabe, Redirect**<br> Konstante: `adobe.target.event.CONTENT_RENDERING_REDIRECT`<br>Zeichenfolgenwert: `at-content-rendering-redirect`<br>Beschreibung: Dieses Ereignis wird ausgelöst, wenn ein Angebot eine Weiterleitungsanfrage ist und Target zu einer anderen URL umleitet. |
| mbox | Zeichenfolge | Name der Mbox |
| message | Zeichenfolge | Enthält für Menschen lesbare Beschreibungen, beispielsweise zu Geschehnissen, zur Fehlermeldung usw. |
| Verfolgung | Objekt | Enthält `sessionId` und `deviceId`. In einigen Fällen fehlt die `deviceId` möglicherweise, weil [!DNL Target] sie nicht vom Edge-Server abrufen konnte. |
| Typ | Zeichenfolge | **Entscheidungsartefakt auf dem Gerät erfolgreich**<br> Konstante:<br>`adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`<br>Zeichenfolgenwert: `artifactDownloadSucceeded`<br>Beschreibung: Wird aufgerufen, wenn das Entscheidungsartefakt auf dem Gerät erfolgreich heruntergeladen wurde.<br>**Entscheidungsartefakt auf dem Gerät fehlgeschlagen**<br> Konstante: `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`<br>Zeichenfolgenwert: `artifactDownloadFailed`<br>Beschreibung: Wird aufgerufen, wenn das Entscheidungsartefakt auf dem Gerät nicht heruntergeladen werden konnte. |

## Nutzung {#section_0500FF09D3A04450B5DC8F85C6F793E0}

```javascript
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(event) { 
  console.log('Event', event); 
});
```

## Schulungsvideo: Antwort-Token und benutzerdefinierte at.js-Ereignisse ![Tutorial-Badge](/help/assets/tutorial.png) {#section_ED304A7137DC42A4BDCD6D57C989F1FA}

Sehen Sie sich das folgende Video an, um zu erfahren, wie Sie Antworttoken und benutzerspezifische at.js-Ereignisse nutzen können, um Profilinformationen aus Target an Drittanbietersysteme zu übergeben.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
