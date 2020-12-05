---
keywords: adobe.target.getOffers;getOffers;getoffers;get offers;at.js;functions;function
description: Informationen über die Funktion adobe.target.getOffers(options) für die JavaScript-Bibliothek von Adobe Target „at.js“.
title: adobe.target.getOffers(options) - at.js 2.x
feature: client-side
translation-type: tm+mt
source-git-commit: a841c492e5d9e4bfedb20133ba32e37daf738c57
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 92%

---


# adobe.target.getOffers(options) - at.js 2.x

Mit dieser Funktion können Sie mehrere Angebote abrufen, indem Sie mehrere Mboxes übergeben. Darüber hinaus können mehrere Angebote für alle Ansichten in aktiven Aktivitäten abgerufen werden.

>[!NOTE]
>
>Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*.

| Schlüssel | Typ | Erforderlich? | Beschreibung |
| --- | --- | --- | --- |
| consumerId | Zeichenfolge | Nein | Der Standardwert ist die globale Mbox des Kunden, falls nicht angegeben. Dieser Schlüssel wird verwendet, um die zusätzliche Daten-ID für die A4T-Integration zu generieren. Dieser Schlüssel ist eine eindeutige Zeichenfolge für jeden Besucher. |
| Anfrage | Objekt | Ja | Siehe Anforderungstabelle unten. |
| Zeitüberschreitung | Nummer | Nein | Zeitüberschreitung der Anfrage. Wenn nicht angegeben, wird die standardmäßige at.js-Zeitüberschreitung verwendet. |

## Anfrage

>[!NOTE]
>
>Informationen zu den zulässigen Typen für alle unten aufgeführten Felder finden Sie in der Dokumentation [zur](http://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) Versand-API.

| Feldname | Erforderlich? | Einschränkungen | Beschreibung |
| --- | --- | --- | --- |
| Anfrage > ID | Nein |  | Entweder `tntId`, `thirdPartyId` oder `marketingCloudVisitorId` wird benötigt. |
| Anfrage > ID > thirdPartyId | Nein | Maximale Größe = 128 |  |  |
| Request > experienceCloud | Nein |  |  |
| Request > experienceCloud > analytics | Nein |  | Adobe Analytics-Integration |
| Request > experienceCloud > analytics > logging | Nein | Folgendes muss auf der Seite implementiert werden:<ul><li>Besucher-ID-Service</li><li>Appmeasurement.js</li></ul> | Die folgenden Werte werden unterstützt:<br>**client_side**: Wenn dieser Wert spezifiziert ist, wird eine Analytics-Nutzlast an den Aufrufer zurückgegeben, die über die Dateneinfüge-API an Adobe Analytics gesendet werden soll.<br>**server_side**: Dies ist der Standardwert, bei dem das Target- und Analytics-Backend die SDID zum Zusammenführen der Aufrufe für das Reporting verwendet. |
| Anfrage > Vorab abrufen | Nein |  |  |
| Anfrage > Vorab abrufen > Ansichten | Nein | Maximale Anzahl = 50<br>Name nicht leer<br>Länge des Namens `<=` 128<br>Länge des Wertes `<=` 5.000<br>Name sollte nicht mit „Profil“ beginnen<br>Unzulässige Namen: „orderId“, „orderTotal“, „productPurchasedId“ | Parameter übergeben, die zum Aufrufen relevanter Ansichten in aktiven Aktivitäten verwendet werden können. |
| Anfrage > Vorab abrufen > Ansichten > profileParameters | Nein | Maximale Anzahl = 50<br>Name nicht leer<br>Länge des Namens `<=` 128<br>Länge des Wertes `<=` 5.000<br>Name sollte nicht mit „Profil“ beginnen | Profilparameter übergeben, die zum Aufrufen relevanter Ansichten in aktiven Aktivitäten verwendet werden können. |
| Anfrage > Vorab abrufen > Ansichten > Produkt | Nein |  |  |
| Anfrage > Vorab abrufen > Ansichten > Produkt -> ID | Nein | Nicht leer<br>maximale Größe = 128 | Produkt-IDs übergeben, die zum Aufrufen relevanter Ansichten in aktiven Aktivitäten verwendet werden können. |
| Anfrage > Vorab abrufen > Ansichten > Produkt > categoryId | Nein | Nicht leer<br>maximale Größe = 128 | Produktkategorie-IDs übergeben, die zum Aufrufen relevanter Ansichten in Aktivitäten verwendet werden können. |
| Anfrage > Vorab abrufen > Ansichten > Bestellung | Nein |  |  |
| Anfrage > Vorab abrufen > Ansichten > Bestellung > ID | Nein | Maximale Länge = 250 | Bestell-IDs übergeben, die zum Aufrufen relevanter Ansichten in aktiven Aktivitäten verwendet werden können. |
| Anfrage > Vorab abrufen > Ansichten > Bestellung > Gesamtsumme | Nein | Gesamtsumme `>=` 0 | Gesamtbestellsummen übergeben, die zum Aufrufen relevanter Ansichten in aktiven Aktivitäten verwendet werden können. |
| Anfrage > Vorab abrufen > Ansichten > Bestellung > purchasedProductIds | Nein | Keine leeren Werte<br>Max. Länge jedes Wertes = 50<br>Per Komma verkettet und getrennt<br>Gesamtlänge der Produkt-IDs `<=` 250 | IDs gekaufter Produkte übergeben, die zum Aufrufen relevanter Ansichten in aktiven Aktivitäten verwendet werden können. |
| Anfrage > Ausführen | Nein |  |  |
| Anfrage > Ausführen > pageLoad | Nein |  |  |
| Anfrage > Ausführen > pageLoad > Parameter | Nein | Maximale Anzahl = 50<br>Name nicht leer<br>Länge des Namens `<=` 128<br>Länge des Wertes `<=` 5.000<br>Name sollte nicht mit „Profil“ beginnen.<br>Nicht zulässige Namen: „orderId“, „orderTotal“, „productPurchasedId“ | Angebote mit angegeben Parametern abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > pageLoad > profileParameters | Nein | Maximale Anzahl = 50<br>Name nicht leer<br>Länge des Namens `<=` 128<br>Länge des Wertes `<=`256<br>Name sollte nicht mit „Profil“ beginnen. | Angebote mit angegeben Profilparametern abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > pageLoad > Produkt | Nein |  |  |
| Anfrage > Ausführen > pageLoad > Produkt -> ID | Nein | Nicht leer<br>Maximale Größe = 128 | Angebote mit angegebenen Parametern abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > pageLoad > Produkt > categoryId | Nein | Nicht leer<br>Maximale Größe = 128 | Angebote mit angegebenen Produktkategorie-IDs abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > pageLoad > Bestellung | Nein |  |  |
| Anfrage > Ausführen > pageLoad > Bestellung > ID | Nein | Maximale Länge = 250 | Angebote mit angegebenen Bestell-IDs abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > pageLoad > Bestellung > Gesamtsumme | Nein | `>=` 0 | Angebote mit angegebenen Gesamtbestellsummen abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > pageLoad > Bestellung > purchasedProductIds | Nein | Keine leeren Werte<br>Max. Länge jedes Wertes = 50<br>Per Komma verkettet und getrennt<br>Gesamtlänge der Produkt-IDs `<=` 250 | Angebote mit angegebenen IDs gekaufter Produkte abrufen, wenn die Seite geladen wird. |
| Anfrage > Ausführen > Mboxes | Nein | Maximale Größe = 50<br>Keine Null-Elemente |  |
| Anfrage > Ausführen > Mboxes > Mbox | Ja | Nicht leer<br>Kein „-clicked“-Suffix<br>Maximale Größe = 250<br>Zulässige Zeichen: `'-, ._\/=:;&!@#$%^&*()_+|?~[]{}'` | Name der Mbox. |
| Anfrage > Ausführen > Mboxes > Mbox > Index | Ja | Nicht null<br>Eindeutig<br>`>=` 0 | Beachten Sie, dass der Index nicht die Reihenfolge darstellt, in der die Mboxes verarbeitet werden. Wie auf einer Webseite mit mehreren regionalen Mboxes kann die Reihenfolge, in der sie verarbeitet werden, nicht angegeben werden. |
| Anfrage > Ausführen > Mboxes > Mbox > Parameter | Nein | Maximale Anzahl = 50<br>Name nicht leer<br>Länge des Namens `<=` 128<br>Länge des Wertes `<=` 5.000<br>Name sollte nicht mit „Profil“ beginnen.<br>Nicht zulässige Namen: „orderId“, „orderTotal“, „productPurchasedId“ | Angebote für eine bestimmte Mbox mit den angegebenen Parametern abrufen. |
| Anfrage > Ausführen > Mboxes > Mbox > profileParameters | Nein | Maximale Anzahl = 50<br>Name nicht leer<br>Länge des Namens `<=` 128<br>Länge des Wertes `<=`256<br>Name sollte nicht mit „Profil“ beginnen. | Angebote für eine bestimmte Mbox mit den angegebenen Profilparametern abrufen. |
| Anfrage > Ausführen > Mboxes > Mbox > Produkt | Nein |  |  |
| Anfrage > Ausführen > Mboxes > Mbox > Produkt > ID | Nein | Nicht leer<br>Maximale Größe = 128 | Angebote für eine bestimmte Mbox mit den angegebenen Produkt-IDs abrufen. |
| Anfrage > Ausführen > Mboxes > Mbox > Produkt > categoryId | Nein | Nicht leer<br>Maximale Größe = 128 | Angebote für eine bestimmte Mbox mit den angegebenen Produktkategorie-IDs abrufen. |
| Anfrage > Ausführen > Mboxes > Mbox > Bestellung | Nein |  |  |
| Anfrage > Ausführen > Mboxes > Mbox > Bestellung > ID | Nein | Maximale Länge = 250 | Angebote für eine bestimmte Mbox mit den angegebenen Bestell-IDs abrufen. |
| Anfrage > Ausführen > Mboxes > Mbox > Bestellung > Gesamtsumme | Nein | `>=` 0 | Angebote für eine bestimmte Mbox mit den angegebenen Gesamtbestellsummen abrufen. |
| Anfrage > Ausführen > Mboxes > Mbox > Bestellung > purchasedProductIds | Nein | Keine leeren Werte<br>Max. Länge jedes Wertes = 50<br>Per Komma verkettet und getrennt<br>Gesamtlänge der Produkt-IDs `<=` 250 | Angebote für eine bestimmte Mbox mit den angegebenen IDs der gekauften Produkte der Bestellung abrufen. |

## Aufruf von getOffers() für alle Ansichten

```javascript
adobe.target.getOffers({
    request: {
      prefetch: {
        views: [{}]
    }
  }
});
```

## Rufen Sie getOffers() auf, um die neuesten Ansichten mit den übergebenen Parametern und Profil-Parametern abzurufen.

```javascript
adobe.target.getOffers({
  request: {
    "prefetch": {
      "views": [
        {
          "parameters": {
            "ad": "1"
          },
          "profileParameters": {
            "age": 23
          }
        }
      ]
    }
  }
});
```

## Rufen Sie getOffers() auf, um mboxes mit übergebenen Parametern und Profil-Parametern abzurufen.

```javascript
adobe.target.getOffers({
  request: {
    execute: {
      mboxes: [
        {
          index: 0,
          name: "first-mbox"
        },
        {
          index: 1,
          name: "second-mbox",
          parameters: {
            a: 1
          },
          profileParameters: {
            b: 2
          }
        }
      ]
    }
  }
});
```

## Benutzen Sie getOffers(), um die Analytics-Nutzlast von der Clientseite abzurufen.

```javascript
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

**Antwort**:

```javascript
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)an Adobe Analytics weitergeleitet werden.

## Daten aus mehreren Mboxes über getOffers() und applyOffers() abrufen und rendern {#multiple}

Mit at.js 2.x können Sie mehrere Mboxes über die `getOffers()`-API abrufen. Sie können auch Daten für mehrere Mboxes abrufen und dann `applyOffers()` zum Rendern der Daten an verschiedenen Positionen verwenden, die durch einen CSS-Selektor identifiziert werden.

Das folgende Beispiel zeigt eine einfache HTML-Seite, auf der at.js 2.x implementiert ist:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>at.js 2.x, multiple selectors and multiple mboxes</title>
  <script src="at.js"></script>
</head>
<body>
  <div id="container1">Default content 1</div>
  
  <div id="container2">Default content 2</div>

  <div id="container3">Default content 3</div>
</body>
</html>
```

Angenommen, Sie haben drei Behälter, die Sie über einen Inhalt ändern möchten, der von [!DNL Target] empfangen wurde. Sie können eine einzelne Anfrage für drei Mboxes erstellen, in der jede Mbox Inhalt in den entsprechenden Behälter rendert.

Die Anfrage und der Rendercode könnten wie folgt aussehen:

```javascript
adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "mbox1"
        },
        {
          index: 1,
          name: "mbox2"
        },
        {
          index: 2,
          name: "mbox3"
        }
      ]
    }
  }
})
.then(response => {
  // get all mboxes from response
  const mboxes = response.prefetch.mboxes;
  let count = 1;

  mboxes.forEach(el => {
    adobe.target.applyOffers({
      selector: "#container" + count,
      response: {
        prefetch: {
          mboxes: [el]
        }
      }
    });

    count += 1;
  });
});
```

Im Abschnitt `request > prefetch > mboxes` gibt es drei verschiedene Mboxes. Wenn die Anfrage erfolgreich abgeschlossen wurde, erhalten Sie die Antwort für jede Mbox aus `response > prefetch > mboxes`. Nachdem Sie über die Antworten und die Speicherorte für die Wiedergabe verfügen, können Sie `applyOffers()` aufrufen, um den von Ihnen von [!DNL Target] abgerufenen Inhalt wiederzugeben. In diesem Beispiel haben wir die folgende Zuordnung:

* Mbox 1 > CSS selector # container 1
* Mbox 2 > CSS selector # container 2
* Mbox 3 > CSS selector # container 3

In diesem Beispiel werden die CSS-Selektoren mit einer Zähl-Variablen erstellt. In einem realen Szenario könnten Sie zwischen dem CSS-Selektor und der Mbox eine andere Zuordnung verwenden.

Beachten Sie, dass dieses Beispiel `prefetch > mboxes` verwendet, Sie könnten aber auch `execute > mboxes` verwenden. Stellen Sie sicher, dass Sie bei Verwendung von Vorausholen (prefetch) in `getOffers()` auch beim Aufruf von `applyOffers()` Vorausholen verwenden sollten.

## Rufen Sie getOffers() auf, um pageLoad auszuführen

Das folgende Beispiel zeigt, wie Sie pageLoad mit getOffers() mit at.js 2 ausführen.*x* 

```javascript
adobe.target.getOffers({
    request: {
        execute: {
            pageLoad: {
                parameters: {}
            }
        }
    }
});
```
