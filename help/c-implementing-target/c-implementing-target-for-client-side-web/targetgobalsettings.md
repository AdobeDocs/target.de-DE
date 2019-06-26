---
description: 'Informationen zur Funktion targetGlobalSettings() für at.js. '
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Informationen zur Funktion targetGlobalSettings() für die Adobe Target-JavaScript-Bibliothek at.js.
seo-title: Informationen zur Funktion targetGlobalSettings() für die Adobe Target-JavaScript-Bibliothek at.js.
solution: Target
subtopic: Erste Schritte
title: targetGlobalSettings()
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# targetGlobalSettings()

Sie können Einstellungen in der at.js-Bibliothek mithilfe von „`targetGlobalSettings()`“ überschreiben, anstatt die Einstellungen in der Benutzeroberfläche von [!DNL Target] Standard/Premium oder durch Verwendung von REST-APIs zu konfigurieren.

In einigen Fällen, besonders bei der Bereitstellung von at.js über [!DNL Dynamic Tag Management] (DTM), ist es von Vorteil, einige Einstellungen zu überschreiben.

## Einstellungen {#section_42C759AE9B524A43B8659018677224B8}

Folgende Einstellungen können überschrieben werden:

| Einstellungen | Typ | Standardwert | Beschreibung |
|--- |--- |--- |--- |
| clientCode | Zeichenfolge | In der Oberfläche festgelegter Wert | Steht für den Kunden-Code |
| serverDomain | Zeichenfolge | In der Oberfläche festgelegter Wert | Steht für den Target-Edge-Server |
| cookieDomain | Zeichenfolge | Möglichst auf Domäne auf oberster Ebene festlegen | Steht für die Domäne, die beim Speichern von Cookies verwendet wird |
| crossDomain | Zeichenfolge | In der Oberfläche festgelegter Wert | Gibt an, ob domänenübergreifende Verfolgung aktiviert ist oder nicht<br>Zulässige Werte sind:<ul><li>disabled</li><li>aktiviert</li><li>nur x</li></ul> |
| Zeitüberschreitung | Nummer | In der Oberfläche festgelegter Wert | Steht für Abfrage-Zeitüberschreitung des Target-Edges |
| globalMboxAutoCreate | Boolesch | In der Oberfläche festgelegter Wert | Gibt an, ob die globale Mbox-Anfrage gestellt werden soll oder nicht |
| visitorApiTimeout | Nummer | 2.000 ms = 2 s | Steht für die Anfrage-Zeitüberschreitung der Besucher-API |
| aktiviert | Boolesch | wahr | Gibt an, ob at.js als Bibliothek aktiviert ist, d. h., ob es Aktionen ausführen soll oder nicht. Der häufigste Anwendungsfall für diese Einstellung ist bei der Deaktivierung von Cookies oder anderen benutzerdefinierten Einstellungen, bei denen die Funktion von at.js deaktiviert würde. |
| defaultContentHiddenStyle | Zeichenfolge | visibility: hidden | Wird nur für das Umbrechen von Mboxes verwendet, bei denen DIV mit dem Klassennamen „mboxDefault“ eingesetzt wird und die über `mboxUpdate()`, `mboxCreate()` oder `mboxDefine()` ausgeführt werden, um Standardinhalte auszublenden. |
| defaultContentVisibleStyle | Zeichenfolge | visibility: visible | Wird nur für das Umbrechen von Mboxes verwendet, bei denen DIV mit dem Klassennamen „mboxDefault“ eingesetzt wird und die über `mboxUpdate()`, `mboxCreate()` oder `mboxDefine()` ausgeführt werden, um Standardinhalte oder angewendete Angebote einzublenden. |
| bodyHiddenStyle | Zeichenfolge | body { opacity: 0 } | Wird nur verwendet, wenn `globalMboxAutocreate === true`, um die Wahrscheinlichkeit eines Flackerns zu minimieren.<br>Weitere Informationen finden Sie unter [Verwaltung von Flackern mit „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md). |
| bodyHidingEnabled | Boolesch | wahr | Wird zur Verminderung eines Flackerns eingesetzt, wenn `target-global-mbox` verwendet wird, um in Visual Experience Composer erstellte Angebote, auch „visuelle Angebote“ genannt, bereitzustellen. |
| imsOrgId | Zeichenfolge | IMS-ORG-ID | Steht für die IMS-ORG-ID |
| secureOnly | Boolesch | false | Zeigt an, ob at.js nur HTTPS verwenden sollte oder es ermöglicht wird, dass basierend auf dem Seitenprotokoll zwischen HTTP und HTTPS umgeschaltet wird. |
| overrideMboxEdgeServer | Boolesch | true (true ab at.js, Version 1.6.2) | Zeigt an, ob die Domäne `<clientCode>.tt.omtrdc.net` oder die Domäne `mboxedge<clusterNumber>.tt.omtrdc.net` verwendet werden sollte.<br>Ist dieser Wert wahr, wird die Domäne `mboxedge<clusterNumber>.tt.omtrdc.net` in einem Cookie gespeichert. |
| overrideMboxEdgeServerTimeout | Nummer | 1860000 =&gt; 31 Minuten | Zeigt die Gültigkeitsdauer des Cookies an, in dem der Wert `mboxedge<clusterNumber>.tt.omtrdc.net` gespeichert wurde. |
| optoutEnabled | Boolesch | false | Zeigt an, ob Target die Besucher-API-Funktion `isOptedOut()` aufrufen sollte. Diese Funktion ist Teil der Aktivierung für Gerätediagramme. |
| selectorsPollingTimeout | Nummer | 5000 ms = 5 s | In at.js 0.9.6 führte Target diese neue Einstellung ein, die über `targetGlobalSettings` außer Kraft gesetzt werden kann.<br>`selectorsPollingTimeout` gibt an, wie lange der Kunde bereit ist, darauf zu warten, dass sämtliche über Selektoren identifizierten Elemente auf der Seite angezeigt werden.<br>Über Visual Experience Composer (VEC) erstellte Aktivitäten haben Angebote, die Selektoren enthalten. |
| dataProviders | Siehe „Datenanbieter“ unten. | Siehe „Datenanbieter“ unten. | Siehe „Datenanbieter“ unten. |

## Nutzung {#section_9AD6FA3690364F7480C872CB55567FB0}

Diese Funktion kann definiert werden, bevor at.js geladen wird, oder alternativ unter **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]** &gt; **[!UICONTROL at.js-Einstellungen bearbeiten]** &gt; **[!UICONTROL Codeeinstellungen]** &gt; **[!UICONTROL Bibliothekskopfzeile]**.

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
| [Verwenden von Datenanbietern in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html) | Mit der Datenanbieterfunktion können Sie Dateien von Drittanbietern einfach an Target übergeben. Ein Drittanbieter kann ein Wetterdienst, ein DMP oder sogar Ihr eigener Web-Service sein. Anschließend können Sie diese Daten zur Erstellung von Zielgruppen und zielgerichtetem Inhalt und zur Aufwertung des Benutzerprofils verwenden. |
| [Implementieren von Datenanbietern in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Implementierungsdetails und Beispiele zur Verwendung der dataProviders-Funktion von Adobe Target, um Daten von Drittanbietern abzurufen und in der Target-Anfrage zu übergeben. |

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
