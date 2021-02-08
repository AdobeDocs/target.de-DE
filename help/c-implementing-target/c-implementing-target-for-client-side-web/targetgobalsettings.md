---
keywords: serverstate;targetGlobalSettings;targetGlobalSettings;globalSettings;global settings;at.js;function;clientCode;clientcode;serverDomain;serverdomain;cookieDomain;cookiedomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle ContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;Opt-out;selectorsPollingTimeout;dataProviders;Hybrid-Personalisierung;deviceLifetime
description: Verwenden Sie die Funktion targetGlobalSettings() für die Adobe Target at.js-JavaScript-Bibliothek, um Einstellungen zu überschreiben, anstatt die Zielgruppe-Benutzeroberfläche oder REST-APIs zu verwenden.
title: Wie verwende ich die Funktion targetGlobalSettings()?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1753'
ht-degree: 36%

---


# targetGlobalSettings()

Sie können Einstellungen in der at.js-Bibliothek mithilfe von „`targetGlobalSettings()`“ überschreiben, anstatt die Einstellungen in der Benutzeroberfläche von [!DNL Target] Standard/Premium oder durch Verwendung von REST-APIs zu konfigurieren.

In einigen Fällen, besonders bei der Bereitstellung von at.js über [!DNL Dynamic Tag Management] (DTM), ist es von Vorteil, einige Einstellungen zu überschreiben.

## Einstellungen {#section_42C759AE9B524A43B8659018677224B8}

Folgende Einstellungen können überschrieben werden:

### bodyHiddenStyle

* **Typ**: String
* **Standardwert**: body { opacity: 0 }
* **Beschreibung**: Wird nur verwendet, wenn  `globalMboxAutocreate === true` die Wahrscheinlichkeit des Flackerns minimiert wird.

   Weitere Informationen finden Sie unter [Verwaltung von Flackern mit „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md).

### bodyHidingEnabled

* **Typ**: Boolesch
* **Standardwert**: true
* **Beschreibung**: Dient zum Steuern des Flackerns, wenn Angebot bereitgestellt  `target-global-mbox` werden, die im Visual Experience Composer (auch als visuelle Angebot bezeichnet) erstellt wurden.

### clientCode

* **Typ**: String
* **Standardwert**: Über die Benutzeroberfläche eingestellter Wert.
* **Beschreibung**: Stellt den Clientcode dar.

### cookieDomain

* **Typ**: String
* **Standardwert**: Falls möglich, auf die Domäne der obersten Ebene einstellen.
* **Beschreibung**: Stellt die Domäne dar, die beim Speichern von Cookies verwendet wird.

### crossDomain

* **Typ**: String
* **Standardwert**: Über die Benutzeroberfläche eingestellter Wert.
* **Beschreibung**: Gibt an, ob die domänenübergreifende Verfolgung aktiviert ist. Folgende Werte sind zulässig: deaktiviert, aktiviert oder nur x-only.

### cspScriptNonce

* **Typ**: Siehe  [Content Security-](#content-security) Richtlinie weiter unten.
* **Standardwert**: Siehe  [Content Security-](#content-security) Richtlinie weiter unten.
* **Beschreibung**: Siehe  [Content Security-](#content-security) Richtlinie weiter unten.

### cspStyleNonce

* **Typ**: Siehe  [Content Security-](#content-security) Richtlinie weiter unten.
* **Standardwert**: Siehe  [Content Security-](#content-security) Richtlinie weiter unten.
* **Beschreibung**: Siehe  [Content Security-](#content-security) Richtlinie weiter unten.

### dataProviders

* **Typ**: Siehe  [Datenanbieter ](#data-providers) weiter unten.
* **Standardwert**: Siehe  [Datenanbieter ](#data-providers) weiter unten.
* **Beschreibung**: Siehe  [Datenanbieter ](#data-providers) weiter unten.

### defaultContentHiddenStyle

* **Typ**: String
* **Standardwert**: Sichtbarkeit: ausgeblendet
* **Beschreibung**: Wird nur zum Umbrechen von Mboxes verwendet, die DIV mit dem Klassennamen &quot;mboxDefault&quot;verwenden und über  `mboxCreate()`,  `mboxUpdate()`oder  `mboxDefine()` zum Ausblenden von Standardinhalten ausgeführt werden.

### defaultContentVisibleStyle

* **Typ**: String
* **Standardwert**: Sichtbarkeit: visible
* **Beschreibung**: Wird nur zum Umbrechen von Mboxes verwendet, die DIV mit dem Klassennamen &quot;mboxDefault&quot;verwenden und über  `mboxCreate()`oder  `mboxUpdate()`zur Anzeige angewendeter Angebot, sofern vorhanden, oder  `mboxDefine()` zur Anzeige von Standardinhalten ausgeführt werden.

### deviceIdLifetime

* **Typ**: Nummer
* **Standardwert**: 63244800000 ms = 2 Jahre
* **Beschreibung**: Die Zeitdauer  `deviceId` wird in Cookies beibehalten.

>[!NOTE]
>
>Die Einstellung deviceIdLifetime kann in at.js Version 2.3.1 oder höher überschrieben werden.

### aktiviert

* **Typ**: Boolesch
* **Standardwert**: true
* **Beschreibung**: Wenn diese Option aktiviert ist, wird automatisch eine  [!DNL Target] Anforderung zum Abrufen von Erlebnissen und zur DOM-Manipulation zum Rendern der Erlebnisse ausgeführt. Außerdem können [!DNL Target]-Aufrufe manuell über `getOffer(s)` / `applyOffer(s)` ausgeführt werden.

   Bei Deaktivierung werden [!DNL Target]-Anforderungen nicht automatisch oder manuell ausgeführt.

### globalMboxAutoCreate

* **Typ**: Nummer
* **Standardwert**: Über die Benutzeroberfläche eingestellter Wert.
* **Beschreibung**: Gibt an, ob die globale Mbox-Anforderung ausgelöst werden soll.

### imsOrgId

* **Typ**: Sting
* **Standardwert**: true
* **Beschreibung**: Stellt die IMS-ORG-ID dar.

### optoutEnabled

* **Typ**: Boolesch
* **Standardwert**: false
* **Beschreibung**: Gibt an, ob Zielgruppe die Besucher-API- `isOptedOut()` Funktion aufrufen soll. Diese Funktion ist Teil der Aktivierung für Gerätediagramme.

### overrideMboxEdgeServer

* **Typ**: Boolesch
* **Standardwert**: true (true), beginnend mit at.js Version 1.6.2)
* **Beschreibung**: Gibt an, ob  `<clientCode>.tt.omtrdc.net` Domäne oder  `mboxedge<clusterNumber>.tt.omtrdc.net` Domäne verwendet werden soll.

   Wenn dieser Wert true ist, wird `mboxedge<clusterNumber>.tt.omtrdc.net`-Domäne in einem Cookie gespeichert. Derzeit nicht mit [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) funktioniert, wenn at.js-Versionen vor at.js 1.8.2 und at.js 2.3.1 verwendet werden. Wenn dies ein Problem für Sie ist, sollten Sie in Erwägung ziehen, at.js auf eine neuere, unterstützte Version zu aktualisieren.[](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)

### overrideMboxEdgeServerTimeout

* **Typ**: Nummer
* **Standardwert**: 1860000 => 31 Minuten
* **Beschreibung**: Gibt die Cookie-Lebensdauer an, die den  `mboxedge<clusterNumber>.tt.omtrdc.net` Wert enthält.

### pageLoadEnabled

* **Typ**: Boolesch
* **Standardwert**: true
* **Beschreibung**: Wenn diese Option aktiviert ist, werden Erlebnisse automatisch abgerufen, die beim Laden der Seite zurückgegeben werden müssen.

### secureOnly

* **Typ**: Boolesch
* **Standardwert**: false
* **Beschreibung**: Gibt an, ob at.js nur HTTPS verwenden oder je nach Seitenprotokoll zwischen HTTP und HTTPS wechseln darf.

### selectorsPollingTimeout

* **Typ**: Nummer
* **Standardwert**: 5000 ms = 5 s
* **Beschreibung**: In at.js 0.9.6 wurde diese neue Einstellung  [!DNL Target] eingeführt, die über  `targetGlobalSettings`überschrieben werden kann.

   Die Einstellung `selectorsPollingTimeout` gibt an, wie lange der Client bereit ist zu warten, bis alle von Selektoren identifizierten Elemente auf der Seite angezeigt werden.

   Über Visual Experience Composer (VEC) erstellte Aktivitäten haben Angebote, die Selektoren enthalten.

### serverDomain

* **Typ**: String
* **Standardwert**: Über die Benutzeroberfläche eingestellter Wert.
* **Beschreibung**: Stellt den Edge-Server der Zielgruppe dar.

### serverState

* **Typ**: Siehe  [Hybrid-](#server-state) Personalisierung unten.
* **Standardwert**: Siehe  [Hybrid-](#server-state) Personalisierung unten.
* **Beschreibung**: Siehe  [Hybrid-](#server-state) Personalisierung unten.

### Zeitüberschreitung

* **Typ**: Nummer
* **Standardwert**: Über die Benutzeroberfläche eingestellter Wert.
* **Beschreibung**: Stellt die Zeitüberschreitung der  [!DNL Target] Edge-Anforderung dar.

### viewsEnabled

* **Typ**: Boolesch
* **Standardwert**: true
* **Beschreibung**: Wenn diese Option aktiviert ist, werden automatisch Ansichten abgerufen, die beim Laden der Seite zurückgegeben werden müssen. Ansichten werden in at.js 2 unterstützt.*x*, zur Verfügung.

### visitorApiTimeout

* **Typ**: Nummer
* **Standardwert**: 2000 ms = 2 s
* **Beschreibung**: Stellt den  [!UICONTROL Besucher-] APIrequest-Timeout dar.

## Nutzung {#section_9AD6FA3690364F7480C872CB55567FB0}

Diese Funktion kann definiert werden, bevor at.js geladen wird oder in **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL at.js-Einstellungen bearbeiten]** > **[!UICONTROL Codeeinstellungen]** > **[!UICONTROL Bibliothekskopfzeile]**.

Die Bibliothekskopfzeile ermöglicht es Ihnen, JavaScript ohne Formvorgabe zu verwenden. Der Anpassungscode sollte dem folgenden Beispiel ähneln:

```javascript
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## Datenanbieter {#data-providers}

Mit dieser Einstellung können Kunden Daten von Drittdatenanbietern sammeln, beispielsweise Demandbase, BlueKai und benutzerspezifische Services, und die Daten an Target als Mbox-Parameter in der globalen Mbox-Anfrage weitergeben. Sie unterstützt die Sammlung von Daten von mehreren Anbietern über asynchrone und synchrone Anfragen. Mit diesem Ansatz ist es ein Leichtes, Flicker- oder Standardinhalte zu verwalten und gleichzeitig unabhängige Timeouts für die einzelnen Anbieter festzulegen, um die Auswirkungen auf die Seitenleistung zu begrenzen

>[!NOTE]
>
>Datenanbieter erfordert [!DNL at.js] 1.3 oder höher.

Weitere Informationen dazu finden Sie in den folgenden Videos:

| Video | Beschreibung |
|--- |--- |
| [Verwenden von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-feature-video-use.html) | Mit der Datenanbieterfunktion können Sie Dateien von Drittanbietern einfach an Target übergeben. Ein Drittanbieter kann ein Wetterdienst, ein DMP oder sogar Ihr eigener Web-Service sein. Anschließend können Sie diese Daten zur Erstellung von Zielgruppen und zielgerichtetem Inhalt und zur Aufwertung des Benutzerprofils verwenden. |
| [Implementieren von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Implementierungsdetails und Beispiele zur Verwendung der dataProviders-Funktion von Adobe Target, um Daten von Drittanbietern abzurufen und in der Target-Anfrage zu übergeben. |

Die Einstellung `window.targetGlobalSettings.dataProviders` entspricht einer Reihe von Datenanbietern.

Jeder Datenanbieter weist die folgende Struktur auf:

| Schlüssel | Typ | Beschreibung |
|--- |--- |--- |
| name | Zeichenfolge | Name des Anbieters. |
| version | Zeichenfolge | Anbieterversion. Dieser Schlüssel wird für die Anbieterentwicklung verwendet. |
| Zeitüberschreitung | Nummer | Gibt die Anbieter-Zeitüberschreigung an, wenn es sich hierbei um eine Netzwerkanfrage handelt.  Dieser Schlüssel ist optional. |
| provider | Funktion | Die Funktion, welche die Logik zum Abrufen der Anbieterdaten enthält.<br>Die Funktion weist einen einzigen erforderlichen Parameter auf: `callback`. Der Parameter „callback“ ist eine Funktion, die nur aufgerufen werden sollte, wenn die Daten erfolgreich abgerufen wurden oder ein Fehler vorliegt.<br>Der Callback erwartet zwei Parameter:<ul><li>error: Gibt an, ob ein Fehler aufgetreten ist. Wenn alles in Ordnung ist, sollte dieser Parameter auf „null“ festgelegt sein.</li><li>params: Ein JSON-Objekt, das für die Parameter steht, die in einer Target-Anfrage gesendet werden.</li></ul> |

Im folgenden Beispiel wird gezeigt, wo der Datenanbieter die Synchronisierungsausführung verwendet:

```javascript
var syncDataProvider = { 
  name: "simpleDataProvider", 
  version: "1.0.0", 
  provider: function(callback) { 
    callback(null, {t1: 1}); 
  } 
}; 
  
window.targetGlobalSettings = { 
  dataProviders: [ 
    syncDataProvider 
  ] 
};
```

Nach den at.js-Prozessen vom Typ `window.targetGlobalSettings.dataProviders` enthält die Target-Anfrage einen neuen Parameter: `t1=1`.

Im folgenden Beispiel sehen Sie, ob die Parameter, die Sie zur Target-Anfrage hinzufügen möchten, von einem Drittanbieterservice, so wie BlueKai, Demandbase usw., abgerufen werden:

```javascript
var blueKaiDataProvider = { 
   name: "blueKai", 
   version: "1.0.0", 
   provider: function(callback) { 
      // simulating network request 
     setTimeout(function() { 
       callback(null, {t1: 1, t2: 2, t3: 3}); 
     }, 1000); 
   } 
} 
  
window.targetGlobalSettings = { 
   dataProviders: [ 
      blueKaiDataProvider 
   ] 
};
```

Nach den at.js-Prozessen vom Typ `window.targetGlobalSettings.dataProviders` enthält die Target-Anfrage zusätzliche Parameter: `t1=1`, `t2=2` und `t3=3`.

Das folgende Beispiel verwendet Datenanbieter, um API-Daten über das Wetter zu sammeln und als Parameter in einer Target-Anfrage zu senden. Die Target-Anfrage weist zusätzliche Parameter auf, beispielsweise `country` und `weatherCondition`.

```javascript
var weatherProvider = { 
      name: "weather-api", 
      version: "1.0.0", 
      timeout: 2000, 
      provider: function(callback) { 
        var API_KEY = "caa84fc6f5dc77b6372d2570458b8699"; 
        var lat = 44.426767399999996; 
        var lon = 26.1025384; 
        var url = "//api.openweathermap.org/data/2.5/weather?lang=en"; 
        var data = { 
          lat: lat, 
          lon: lon, 
          appId: API_KEY 
        } 
 
        $.ajax({ 
          type: "GET", 
                url: url, 
          dataType: "json", 
          data: data, 
          success: function(data) { 
            console.log("Weather data", data); 
            callback(null, { 
              country: data.sys.country, 
              weatherCondition: data.weather[0].main 
            }); 
          }, 
          error: function(err) { 
            console.log("Error", err); 
            callback(err); 
          } 
        });         
      } 
    }; 
 
    window.targetGlobalSettings = { 
      dataProviders: [weatherProvider] 
    };
```

Beachten Sie Folgendes, wenn Sie die Einstellung `dataProviders` verwenden.

* Wenn die `window.targetGlobalSettings.dataProviders` hinzugefügten Datenanbieter asynchron sind, werden sie parallel ausgeführt. Die Besucher-API-Anfrage wird parallel mit den `window.targetGlobalSettings.dataProviders` hinzugefügten Funktionen ausgeführt, um eine minimale Wartezeit zu ermöglichen.
* at.js versucht nicht, die Daten zwischenzuspeichern. Wenn der Datenanbieter die Daten nur einmal abruft, sollte er sicherstellen, dass die Daten zwischengespeichert werden, und die Cachedaten für den zweiten Aufruf verarbeiten, wenn die Anbieterfunktion aufgerufen wird.

## Content Security Policy {#content-security}

&quot;at.js 2.3.0+&quot;unterstützt das Festlegen von Content Security Policy-Nonces für SCRIPT- und STYLE-Tags, die beim Anwenden von bereitgestellten Zielgruppe-Angeboten an das Seiten-DOM angehängt werden.

Die SCRIPT- und STYLE-Nonces sollten vor dem Laden von at.js 2.3.0 entsprechend in `targetGlobalSettings.cspScriptNonce` und `targetGlobalSettings.cspStyleNonce` eingestellt werden. Siehe Beispiel unten:

```javascript
...
<head>
 <script nonce="<script_nonce_value>">
window.targetGlobalSettings = {
  cspScriptNonce: "<csp_script_nonce_value>",
  cspStyleNonce: "<csp_style_nonce_value>"
};
 </script>
 <script nonce="<script_nonce_value>" src="at.js"></script>
...
</head>
...
```

Nachdem die Einstellungen `cspScriptNonce` und `cspStyleNonce` festgelegt wurden, legt at.js 2.3.0+ diese auf allen SCRIPT- und STYLE-Tags, die beim Anwenden von Zielgruppen-Angeboten an das DOM angehängt werden, als nonce-Attribute fest.

## Hybrid-Personalisierung {#server-state}

`serverState` ist eine Einstellung in at.js v2.2+, die zur Optimierung der Seitenleistung verwendet werden kann, wenn eine Hybridintegration der Zielgruppe implementiert wird. Hybrid-Integration bedeutet, dass Sie sowohl at.js v2.2+ auf Client- als auch Versand-API oder ein Zielgruppe-SDK auf Serverseite verwenden, um Erlebnisse bereitzustellen. `serverState` gibt at.js v2.2+ die Möglichkeit, Erlebnisse direkt aus Inhalten anzuwenden, die auf dem Server abgerufen und als Teil der bereitzustellenden Seite an den Client zurückgegeben werden.

### Voraussetzungen

Sie müssen über eine Hybridintegration von [!DNL Target] verfügen.

* **Serverseitig**: Sie müssen die neuen  [Versand-](https://developers.adobetarget.com/api/delivery-api/) APIs oder  [Zielgruppe-SDKs](https://developers.adobetarget.com/api/delivery-api/#section/SDKs) verwenden.
* **Clientseitig**: Sie müssen  [at.js Version 2.2 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) verwenden.

### Codebeispiele

Um besser zu verstehen, wie dies funktioniert, sehen Sie sich bitte die Codebeispiele unten an, die Sie auf Ihrem Server haben würden. Der Code setzt voraus, dass Sie das SDK [Zielgruppe Node.js](https://github.com/adobe/target-nodejs-sdk) verwenden.

```javascript
// First, we fetch the offers via Target Node.js SDK API, as usual
const targetResponse = await targetClient.getOffers(options);
// A successfull response will contain Target Delivery API request and response objects, which we need to set as serverState
const serverState = {
  request: targetResponse.request,
  response: targetResponse.response
};
// Finally, we should set window.targetGlobalSettings.serverState in the returned page, by replacing it in a page template, for example
const PAGE_TEMPLATE = `
<!doctype html>
<html>
<head>
  ...
  <script>
    window.targetGlobalSettings = {
      overrideMboxEdgeServer: true,
      serverState: ${JSON.stringify(serverState, null, " ")}
    };
  </script>
  <script src="at.js"></script>
</head>
...
</html>
`;
// Return PAGE_TEMPLATE to the client ...
```

Ein Beispiel für ein Objekt `serverState`-JSON für die Ansicht-Vorab-Abfrage sieht wie folgt aus:

```
{
 "request": {
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "context": {
   "channel": "web",
   "timeOffsetInMinutes": 0
  },
  "experienceCloud": {
   "analytics": {
    "logging": "server_side",
    "supplementalDataId": "7D3AA246CC99FD7F-1B3DD2E75595498E"
   }
  },
  "prefetch": {
   "views": [
    {
     "address": {
      "url": "my.testsite.com/"
     }
    }
   ]
  }
 },
 "response": {
  "status": 200,
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "client": "testclient",
  "edgeHost": "mboxedge21.tt.omtrdc.net",
  "prefetch": {
   "views": [
    {
     "name": "home",
     "key": "home",
     "options": [
      {
       "type": "actions",
       "content": [
        {
         "type": "setHtml",
         "selector": "#app > DIV.app-container:eq(0) > DIV.page-container:eq(0) > DIV:nth-of-type(2) > SECTION.section:eq(0) > DIV.container:eq(1) > DIV.heading:eq(0) > H1.title:eq(0)",
         "cssSelector": "#app > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(2) > SECTION:nth-of-type(1) > DIV:nth-of-type(2) > DIV:nth-of-type(1) > H1:nth-of-type(1)",
         "content": "<span style=\"color:#FF0000;\">Latest</span> Products for 2020"
        }
       ],
       "eventToken": "t0FRvoWosOqHmYL5G18QCZNWHtnQtQrJfmRrQugEa2qCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
       "responseTokens": {
        "profile.memberlevel": "0",
        "geo.city": "dublin",
        "activity.id": "302740",
        "experience.name": "Experience B",
        "geo.country": "ireland"
       }
      }
     ],
     "state": "J+W1Fq18hxliDDJonTPfV0S+mzxapAO3d14M43EsM9f12A6QaqL+E3XKkRFlmq9U"
    }
   ]
  }
 }
}
```

Nachdem die Seite im Browser geladen wurde, wendet at.js alle [!DNL Target]-Angebot von `serverState` sofort an, ohne Netzwerkaufrufe gegen die [!DNL Target]-Kante auszulösen. Darüber hinaus verhindert at.js nur die DOM-Elemente, für die im serverseitigen Inhalt [!DNL Target]-Angebot verfügbar sind, was sich positiv auf die Seitenladeleistung und das Endbenutzererlebnis auswirkt.

### Wichtige Hinweise

Beachten Sie bei Verwendung von `serverState` Folgendes:

* Zurzeit unterstützt at.js v2.2 nur die Bereitstellung von Erlebnissen über serverState für:

   * VEC-erstellte Aktivitäten, die beim Laden der Seite ausgeführt werden.
   * Vorab abgerufene Ansichten.

      Bei SPA mit den Ansichten [!DNL Target] und `triggerView()` in der at.js-API speichert at.js v2.2 den Inhalt für alle auf dem Server vorab abgerufenen Ansichten zwischen und wendet diese an, sobald jede Ansicht über `triggerView()` ausgelöst wird, ohne dass weitere inhaltliche Abrufe an die Zielgruppe ausgelöst werden.

   * **Hinweis**: Derzeit werden auf der Serverseite abgerufene Mboxes in nicht unterstützt  `serverState`.

* Beim Anwenden von `serverState `Angeboten berücksichtigt at.js die Einstellungen `pageLoadEnabled` und `viewsEnabled`, z. B. werden keine Angebot zum Laden der Seite angewendet, wenn `pageLoadEnabled` den Wert false hat.

   Aktivieren Sie zum Aktivieren dieser Einstellungen den Umschalter unter **[!UICONTROL Administration] > [!UICONTROL Implementierung] > [!UICONTROL Bearbeiten] > [!UICONTROL Seitenladevorgang aktiviert]**.

   ![Einstellungen für &quot;Seitenladeaktivierung&quot;](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

* Wenn Sie `serverState` und `<script>`-Tags im zurückgegebenen Inhalt verwenden, stellen Sie sicher, dass Ihr HTML-Inhalt `<\/script>` anstelle von `</script>` verwendet. Wenn Sie `</script>` verwenden, interpretiert der Browser `</script>` als Ende eines Inline-SKRIPT und es kann die HTML-Seite beschädigen.

### Zusätzliche Ressourcen

Weitere Informationen zur Funktionsweise von `serverState` finden Sie in den folgenden Ressourcen:

* [Beispielcode](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [Beispiel-App für eine Einzelseitenanwendung (SPA) mit  `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
