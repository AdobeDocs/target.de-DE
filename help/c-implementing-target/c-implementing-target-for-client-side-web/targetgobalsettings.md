---
keywords: serverstate;targetGlobalSettings;targetglobalsettings;globalSettings;globalsettings;global settings;at.js;functions;function;clientCode;clientcode;serverDomain;serverdomain;cookieDomain;cookiedomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle;defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;selectorsPollingTimeout;dataProviders;Hybrid Personalization
description: Informationen zur Funktion targetGlobalSettings() für die Adobe Target-JavaScript-Bibliothek at.js.
title: Informationen zur Funktion targetGlobalSettings() für die Adobe Target-JavaScript-Bibliothek at.js.
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a24d932f02d49ff11da6299eb46d73f4f385b866
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 63%

---


# targetGlobalSettings()

Sie können Einstellungen in der at.js-Bibliothek mithilfe von „`targetGlobalSettings()`“ überschreiben, anstatt die Einstellungen in der Benutzeroberfläche von [!DNL Target] Standard/Premium oder durch Verwendung von REST-APIs zu konfigurieren.

In einigen Fällen, besonders bei der Bereitstellung von at.js über [!DNL Dynamic Tag Management] (DTM), ist es von Vorteil, einige Einstellungen zu überschreiben.

## Einstellungen {#section_42C759AE9B524A43B8659018677224B8}

Folgende Einstellungen können überschrieben werden:

| Einstellungen | Typ | Standardwert | Beschreibung |
|--- |--- |--- |--- |
| serverState | Siehe &quot;Hybrid-Personalisierung&quot;weiter unten. | Siehe &quot;Hybrid-Personalisierung&quot;weiter unten. | Siehe &quot;Hybrid-Personalisierung&quot;weiter unten. |
| clientCode | Zeichenfolge | In der Oberfläche festgelegter Wert | Steht für den Kunden-Code |
| serverDomain | Zeichenfolge | In der Oberfläche festgelegter Wert | Steht für den Target-Edge-Server |
| cookieDomain | Zeichenfolge | Möglichst auf Domäne auf oberster Ebene festlegen | Steht für die Domäne, die beim Speichern von Cookies verwendet wird |
| crossDomain | Zeichenfolge | In der Oberfläche festgelegter Wert | Gibt an, ob domänenübergreifende Verfolgung aktiviert ist oder nicht<br>Zulässige Werte sind:<ul><li>disabled</li><li>aktiviert</li><li>nur x</li></ul> |
| Zeitüberschreitung | Nummer | In der Oberfläche festgelegter Wert | Steht für Abfrage-Zeitüberschreitung des Target-Edges |
| globalMboxAutoCreate | Boolesch | In der Oberfläche festgelegter Wert | Gibt an, ob die globale Mbox-Anfrage gestellt werden soll oder nicht |
| visitorApiTimeout | Nummer | 2.000 ms = 2 s | Steht für die Anfrage-Zeitüberschreitung der Besucher-API |
| aktiviert | Boolesch | wahr | Wenn diese Option aktiviert ist, wird automatisch eine Zielgruppe zum Abrufen von Erlebnissen und zur DOM-Manipulation zum Rendern der Erlebnisse ausgeführt. Darüber hinaus können Zielgruppen-Aufrufe manuell über `getOffer(s)` / `applyOffer(s)`<br>Bei Deaktivierung werden Zielgruppen nicht automatisch oder manuell ausgeführt |
| pageLoadEnabled | Boolesch | wahr | Bei Aktivierung werden Erlebnisse automatisch abgerufen, die beim Laden der Seite zurückgegeben werden müssen |
| viewsEnabled | Boolesch | wahr | Wenn diese Option aktiviert ist, werden automatisch Ansichten abgerufen, die beim Laden der Seite zurückgegeben werden müssen. Ansichten werden in at.js 2 unterstützt.*x*, zur Verfügung |
| defaultContentHiddenStyle | Zeichenfolge | visibility: hidden | Wird nur für das Umbrechen von Mboxes verwendet, bei denen DIV mit dem Klassennamen „mboxDefault“ eingesetzt wird und die über `mboxUpdate()`, `mboxCreate()` oder `mboxDefine()` ausgeführt werden, um Standardinhalte auszublenden. |
| defaultContentVisibleStyle | Zeichenfolge | visibility: visible | Wird nur für das Umbrechen von Mboxes verwendet, bei denen DIV mit dem Klassennamen „mboxDefault“ eingesetzt wird und die über `mboxUpdate()`, `mboxCreate()` oder `mboxDefine()` ausgeführt werden, um Standardinhalte oder angewendete Angebote einzublenden. |
| bodyHiddenStyle | Zeichenfolge | body { opacity: 0 } | Wird nur verwendet, wenn `globalMboxAutocreate === true`, um die Wahrscheinlichkeit eines Flackerns zu minimieren.<br>Weitere Informationen finden Sie unter [Verwaltung von Flackern mit „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md). |
| bodyHidingEnabled | Boolesch | wahr | Wird zur Verminderung eines Flackerns eingesetzt, wenn `target-global-mbox` verwendet wird, um in Visual Experience Composer erstellte Angebote, auch „visuelle Angebote“ genannt, bereitzustellen. |
| imsOrgId | Zeichenfolge | IMS-ORG-ID | Steht für die IMS-ORG-ID |
| secureOnly | Boolesch | false | Zeigt an, ob at.js nur HTTPS verwenden sollte oder es ermöglicht wird, dass basierend auf dem Seitenprotokoll zwischen HTTP und HTTPS umgeschaltet wird. |
| overrideMboxEdgeServer | Boolesch | true (true ab at.js, Version 1.6.2) | Zeigt an, ob die Domäne `<clientCode>.tt.omtrdc.net` oder die Domäne `mboxedge<clusterNumber>.tt.omtrdc.net` verwendet werden sollte.<br>Ist dieser Wert wahr, wird die Domäne `mboxedge<clusterNumber>.tt.omtrdc.net` in einem Cookie gespeichert.. Derzeit nicht mit [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) |
| overrideMboxEdgeServerTimeout | Nummer | 1860000 => 31 Minuten | Zeigt die Gültigkeitsdauer des Cookies an, in dem der Wert `mboxedge<clusterNumber>.tt.omtrdc.net` gespeichert wurde. |
| optoutEnabled | Boolesch | false | Zeigt an, ob Target die Besucher-API-Funktion `isOptedOut()` aufrufen sollte. Diese Funktion ist Teil der Aktivierung für Gerätediagramme. |
| selectorsPollingTimeout | Nummer | 5000 ms = 5 s | In at.js 0.9.6 führte Target diese neue Einstellung ein, die über `targetGlobalSettings` außer Kraft gesetzt werden kann.<br>`selectorsPollingTimeout` gibt an, wie lange der Kunde bereit ist, darauf zu warten, dass sämtliche über Selektoren identifizierten Elemente auf der Seite angezeigt werden.<br>Über Visual Experience Composer (VEC) erstellte Aktivitäten haben Angebote, die Selektoren enthalten. |
| dataProviders | Siehe „Datenanbieter“ unten. | Siehe „Datenanbieter“ unten. | Siehe „Datenanbieter“ unten. |
| cspScriptNonce | Siehe &quot;Content Security Policy&quot; weiter unten. | Siehe &quot;Content Security Policy&quot; weiter unten. | Siehe &quot;Content Security Policy&quot; weiter unten. |
| cspStyleNonce | Siehe &quot;Content Security Policy&quot; weiter unten. | Siehe &quot;Content Security Policy&quot; weiter unten. | Siehe &quot;Content Security Policy&quot; weiter unten. |

## Nutzung {#section_9AD6FA3690364F7480C872CB55567FB0}

Diese Funktion kann definiert werden, bevor at.js geladen wird, oder alternativ unter **[!UICONTROL Einrichten]** > **[!UICONTROL Implementierung]** > **[!UICONTROL at.js-Einstellungen bearbeiten]** > **[!UICONTROL Codeeinstellungen]** > **[!UICONTROL Bibliothekskopfzeile]**.

Die Bibliothekskopfzeile ermöglicht es Ihnen, JavaScript ohne Formvorgabe zu verwenden. Der Anpassungscode sollte dem folgenden Beispiel ähneln:

```
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

```
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

```
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

```
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

Die SCRIPT- und STYLE-Nonces sollten vor dem Laden von at.js 2.3.0 in `targetGlobalSettings.cspScriptNonce` und `targetGlobalSettings.cspStyleNonce` entsprechend eingestellt werden. Siehe Beispiel unten:

```
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

Nachdem Sie die Einstellungen `cspScriptNonce` und `cspStyleNonce` Einstellungen festgelegt haben, legt at.js 2.3.0+ diese auf allen SCRIPT- und STYLE-Tags, die beim Anwenden von Zielgruppe-Angeboten an das DOM angehängt werden, als Nonce-Attribute fest.

## Hybrid-Personalisierung {#server-state}

`serverState` ist eine Einstellung in at.js v2.2+, die zur Optimierung der Seitenleistung verwendet werden kann, wenn eine Hybridintegration der Zielgruppe implementiert wird. Hybrid-Integration bedeutet, dass Sie sowohl at.js v2.2+ auf Client- als auch Versand-API oder ein Zielgruppe-SDK auf Serverseite verwenden, um Erlebnisse bereitzustellen. `serverState` gibt at.js v2.2+ die Möglichkeit, Erlebnisse direkt aus Inhalten anzuwenden, die auf dem Server abgerufen und als Teil der bereitzustellenden Seite an den Client zurückgegeben werden.

### Voraussetzungen

Sie müssen über eine Hybridintegration von verfügen [!DNL Target].

* **Serverseitig**:  Sie müssen die neuen [Versand-API](https://developers.adobetarget.com/api/delivery-api/) oder [Zielgruppe-SDKs](https://developers.adobetarget.com/api/delivery-api/#section/SDKs)verwenden.
* **Clientseitig**: Sie müssen [at.js Version 2.2 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)verwenden.

### Codebeispiele

Um besser zu verstehen, wie dies funktioniert, sehen Sie sich bitte die Codebeispiele unten an, die Sie auf Ihrem Server haben würden. Der Code setzt voraus, dass Sie das [Zielgruppe Node.js SDK](https://github.com/adobe/target-nodejs-sdk)verwenden.

```
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

Ein Beispiel für ein `serverState` JSON-Objekt für die Ansicht vor dem Abrufen sieht wie folgt aus:

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

Nach dem Laden der Seite im Browser wendet at.js alle [!DNL Target] Angebot sofort an, ohne dass Netzwerkaufrufe an die `serverState` [!DNL Target] Kante ausgelöst werden. Darüber hinaus verhindert at.js nur die DOM-Elemente, für die im serverseitig abgerufenen Inhalt [!DNL Target] Angebot verfügbar sind, was sich positiv auf die Seitenladeleistung und das Endbenutzererlebnis auswirkt.

### Wichtige Hinweise

Consider the following when using `serverState`:

* Zurzeit unterstützt at.js v2.2 nur die Bereitstellung von Erlebnissen über serverState für:

   * VEC-erstellte Aktivitäten, die beim Laden der Seite ausgeführt werden.
   * Vorab abgerufene Ansichten.

      Bei SPAs, die [!DNL Target] Ansichten und die at.js-API verwenden, speichert at.js v2.2 den Inhalt für alle auf dem Server vorab abgerufenen Ansichten zwischen und wendet diese an, sobald jede Ansicht ausgelöst wird, `triggerView()` `triggerView()`ohne dass zusätzliche inhaltliche Abrufe an die Zielgruppe ausgelöst werden.

   * **Hinweis**:  Derzeit werden auf der Serverseite abgerufene Mboxes in nicht unterstützt `serverState`.

* Beim Anwenden von `serverState `Angeboten berücksichtigt at.js `pageLoadEnabled` und `viewsEnabled` Einstellungen, z. B. werden keine Angebot zum Laden der Seite angewendet, wenn die `pageLoadEnabled` Einstellung &quot;false&quot;ist.

   Um diese Einstellungen zu aktivieren, aktivieren Sie den Umschalter unter &quot; **[UICONTROL-Einstellungen&quot;> &quot;Implementierung&quot;> &quot;Einstellungen bearbeiten&quot;> &quot;Seitenladevorgang aktiviert]**&quot;.

   ![Einstellungen für &quot;Seitenladeaktivierung&quot;](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

### Zusätzliche Ressourcen

Weitere Informationen zur `serverState` Funktionsweise finden Sie in den folgenden Ressourcen:

* [Beispielcode](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [Beispiel-App für Einzelseitenanwendung (SPA) mit `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
