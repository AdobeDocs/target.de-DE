---
description: 'Informationen zur Funktion adobe. target. sendnotifications (options) für at. js. '
seo-description: Informationen über die Funktion adobe. target. sendnotifications (options) für die javascript-Bibliothek von Adobe Target at. js.
seo-title: Informationen über die Funktion adobe. target. sendnotifications (options) für die javascript-Bibliothek von Adobe Target at. js.
solution: Target
subtopic: Erste Schritte
title: adobe. target. sendnotifications (options)
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# adobe. target. sendnotifications (options)

This function sends a notification to Target edge when an experience is rendered without using `adobe.target.applyOffer()` or `adobe.target.applyOffers()`.

>[!NOTE]
>
>Diese Funktion wurde in at. js 2.1.0 eingeführt und steht für alle Versionen über 2.1.0 zur Verfügung.

| Schlüssel | Typ | Erforderlich? | Beschreibung |
| --- | --- | --- | --- |
| consumerId | Zeichenfolge | Nein | Der Standardwert ist die globale Mbox des Kunden, falls nicht angegeben. Dieser Schlüssel wird verwendet, um die ID für zusätzliche Daten zu generieren, die für die A4T-Integration verwendet wird. |
| Anfrage | Objekt | Ja | Siehe Anfragetabelle unten. |
| Zeitüberschreitung | Nummer | Nein | Zeitüberschreitung der Abfrage. Wenn nicht angegeben, wird die standardmäßige at.js-Zeitüberschreitung verwendet. |

## Anfrage

| Feldname | Typ | Erforderlich? | Einschränkung | Beschreibung |
| --- | --- | --- | --- | --- |
| Anforderung &gt; Benachrichtigungen | Array von Objekten | Ja |  | Benachrichtigungen für den angezeigten Inhalt, angeklickte Selektoren und/oder besuchte Ansichten oder mboxes. |
| Anforderung &gt; Benachrichtigungen &gt; Adresse | Objekt | Nein |  |  |
| Anforderung &gt; Benachrichtigungen &gt; Adresse &gt; URL | Zeichenfolge | Nein |  | URL, aus der die Benachrichtigung ausgelöst wurde. |
| Anforderung &gt; Benachrichtigungen &gt; Adresse &gt; referringurl | Zeichenfolge | Nein |  | Die verweisende URL, aus der die Benachrichtigung ausgelöst wurde. |
| Anforderung &gt; Benachrichtigungen &gt; Parameter | Objekt | Nein | Die folgenden Namen sind für Parameter nicht zulässig:<ul><li>orderId</li><li>orderTotal</li><li>Productpurchasedids</li></ul>Beachten Sie Folgendes:<ul><li>Max. 50 Parameter.</li><li>Parametername darf nicht leer sein.</li><li>Max. Länge des Parameternamens 128.</li><li>Parametername darf nicht mit "profile" beginnen.</li><li>Maximale Parameterlänge 5000.</li></ul> |  |
| Anforderung &gt; Benachrichtigungen &gt; profileparameter | Objekt | Nein | Die folgenden Namen sind für Parameter nicht zulässig:<ul><li>orderId</li><li>orderTotal</li><li>Productpurchasedids</li></ul>Beachten Sie Folgendes:<ul><li>Max. 50 Parameter.</li><li>Parametername darf nicht leer sein.</li><li>Max. Länge des Parameternamens 128.</li><li>Parametername darf nicht mit "profile" beginnen.</li><li>Maximale Parameterlänge 5000.</li></ul> |  |
| Anforderung &gt; Benachrichtigungen &gt; Reihenfolge | Objekt | Nein |  | Objekt, das die Bestelldetails beschreibt. |
| Anforderung &gt; Benachrichtigungen &gt; Reihenfolge &gt; ID | Zeichenfolge | Nein | `<=` 250 Zeichen. | Bestell-ID. |
| Anforderung &gt; Benachrichtigungen &gt; Bestellung &gt; Gesamt | Zeichenfolge | Nein | `>=` 0 | Bestellsumme. |
| Anforderung &gt; Benachrichtigungen &gt; Bestellung &gt; purchasedproductids | Array von Zeichenfolge | Nein | <ul><li>Keine leeren Werte zulässig.</li><li>Jede Produkt-ID max. 50.</li><li>Produkt-IDs (durch Kommas getrennt und verkettet) sollten 250 nicht überschreiten.</li></ul> | Bestellprodukt-IDs. |
| Anforderung &gt; Benachrichtigungen &gt; Produkt | Objekt | Nein |  |  |
| Anforderung &gt; Benachrichtigungen &gt; Produkt &gt; ID | Zeichenfolge | Nein | `<=` 128 Zeichen; darf nicht leer sein. | Produkt-ID. |
| Anforderung &gt; Benachrichtigungen &gt; Produkt &gt; categoryid | Zeichenfolge | Nein | `<=` 128 Zeichen; darf nicht leer sein. | Kategorie-ID. |
| Anforderung &gt; Benachrichtigungen &gt; ID | Zeichenfolge | Ja | `<=` 200 Zeichen. | Die Benachrichtigungs-ID wird als Antwort zurückgegeben und zeigt an, dass die Benachrichtigung erfolgreich verarbeitet wurde. |
| Anforderung &gt; Benachrichtigungen &gt; impressionid | Zeichenfolge | Nein | `<= 128` Zeichen. | Die Impressions-ID wird verwendet, um die aktuelle Benachrichtigung mit einer vorherigen Benachrichtigung zu verknüpfen oder auszuführen oder eine Anforderung auszuführen. Stimmen beide überein, generiert die zweite und andere nachfolgende Anforderungen keine neue Impression für die Aktivität oder das Erlebnis. |
| Anforderung &gt; Benachrichtigungen &gt; Typ | Zeichenfolge | Ja | " click" oder "display" wird unterstützt. | Benachrichtigungstyp. |
| Anforderung &gt; Benachrichtigungen &gt; Zeitstempel | Nummer`<int64>` | Ja |  | Zeitstempel der Benachrichtigung in Millisekunden seit der UNIX-Epoche. |
| Anforderung &gt; Benachrichtigungen &gt; Tokens | Array von Zeichenfolge | Ja |  | Eine Liste der Token für angezeigte Inhalte oder angeklickte Selektoren basierend auf dem Typ der Benachrichtigung. |
| Anforderung &gt; Benachrichtigungen &gt; mbox | Objekt | Nein |  | Benachrichtigungen für die mbox. |
| Anforderung &gt; Benachrichtigungen &gt; mbox &gt; Name | Zeichenfolge | Nein | Keine leeren Werte zulässig.<br>Zulässige Zeichen: Siehe Hinweis unten. | Name der Mbox. |
| Anforderung &gt; Benachrichtigungen &gt; mbox &gt; Status | Zeichenfolge | Nein |  | mbox-Statustoken. |
| Anforderung &gt; Benachrichtigungen &gt; Ansicht | Objekt | Nein |  |  |
| Anforderung &gt; Benachrichtigungen &gt; Ansicht &gt; ID | Ganzzahl `<int64>` | Nein |  | Anzeigen Sie id. Die ID, die der Ansicht zugewiesen wurde, wenn die Ansicht über die Ansicht-API erstellt wurde. |
| Anforderung &gt; Benachrichtigungen &gt; Ansicht &gt; Name | Zeichenfolge | Nein | `<= 128` Zeichen. | Name der Ansicht. |
| Anforderung &gt; Benachrichtigungen &gt; Ansicht &gt; Schlüssel | Zeichenfolge | Nein | `<=` 512 Zeichen. | Ansichtsschlüssel. Der Schlüssel, der mit der Ansicht über die API festgelegt wurde. |
| Anforderung &gt; Benachrichtigungen &gt; Ansicht &gt; Status | Zeichenfolge | Nein |  | Statustoken anzeigen. |

**Hinweis**: Folgende Zeichen sind zulässig `Request > notifications > mbox > name`:

```
- '-, ./=`:;&!@#$%^&*()+|?~[]{}'
```

## Sendnotifications ()-Aufruf nach dem Rendern von vorab erstellten mboxes

```
function createTokens(options) {
  return options.map(e => e.eventToken);
}

function createNotification(mbox, type, tokens) {
  const id = 11111; // here we should use a random ID like UUID
  const timestamp = Date.now();
  const { name, state, parameters, profileParameters, order, product } = mbox;
  const result = {
    id,
    type,
    timestamp,
    parameters,
    profileParameters,
    order,
    product
  };

  result.mbox = { name, state };
  result.tokens = tokens;

  return result;
}

adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "a1-serverside-ab"
        }
      ]
    }
  }
})
.then(response => {
  const mboxes = response.prefetch.mboxes;
  const notifications = mboxes.map(mbox => {
    const type = "display";
    const tokens = createTokens(mbox.options);

    return createNotification(mbox, type, tokens);
  });
  
  adobe.target.sendNotifications({
    request: { notifications }
  });
})
```

>[!NOTE]
>
>If you are using Adobe Analytics, `getOffers()` with prefetch only and `sendNotifications()`, the Analytics request must be fired after `sendNotifications()` is executed. The purpose of this is to ensure that the SDID generated by `sendNotifications()` will match the SDID sent to Analytics and Target.