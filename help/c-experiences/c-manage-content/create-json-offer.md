---
keywords: remote offer;create remote offer
description: Erstellen Sie JSON-Angebote in der Angebotsbibliothek für die Verwendung im formularbasierten Experience Composer.
title: Erstellen von JSON-Angeboten
feature: offers
topic: Standard
uuid: 4ae3ca34-7661-4c1d-a132-fc446e653b90
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 100%

---


# Erstellen von JSON-Angeboten{#create-json-offers}

Erstellen Sie JSON-Angebote in der Angebotsbibliothek für die Verwendung im formularbasierten Experience Composer.

JSON-Angebote können in formularbasierten Aktivitäten verwendet werden, wodurch Anwendungsfälle ermöglicht werden, bei denen die Entscheidung von Target erforderlich ist, ein Angebot im JSON-Format zur Nutzung in SPA-Frameworks oder Server-seitigen Integrationen zu senden.

Beachten Sie Folgendes, wenn Sie mit JSON-Angeboten arbeiten:

* JSON-Angebote sind derzeit nur für AB- und XT-Aktivitäten verfügbar.
* JSON-Angebote können nur in formularbasierten Aktivitäten verwendet werden.
* JSON kann direkt abgerufen werden, wenn Sie die Server-seitige API, das Mobile-SDK oder das NodeJS-SDK verwenden.
* Im Browser kann JSON NUR über at.js 1.2.3 (oder neuer) und mit  [getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) abgerufen werden, indem Aktionen mit der Aktion `setJson` gefiltert werden.
* JSON-Angebote werden als native JSON-Objekte und nicht als Zeichenfolgen ausgeliefert. Nutzer dieser Objekte müssen diese also nicht mehr als Zeichenfolgen behandeln und in JSON-Objekte konvertieren.
* JSON-Angebote werden im Gegensatz zu anderen Angeboten (z. B. HTML-Angeboten) nicht automatisch eingesetzt, da es sich bei JSON-Angeboten um nicht visuelle Angebote handelt. Der Entwickler muss Code schreiben, um das Angebot explizit zum Einsatz zu bringen.  [getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md).
* Wenn Sie mbox.js verwenden, werden JSON-Angebote nicht unterstützt.

## Erstellen eines JSON-Angebots {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.
1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL JSON-Angebot]**.

   ![](assets/offer-json.png)

1. Geben Sie einen Angebotsnamen ein.
1. Schreiben Sie Ihren JSON-Code in das Feld **[!UICONTROL Code]** oder kopieren Sie ihn dorthin.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Beispiel {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON-Angebote werden nur bei Aktivitäten unterstützt, die mit dem formularbasierten Experience Composer erstellt wurden. Die einzige Möglichkeit, JSON-Angebote zu nutzen, läuft derzeit über direkte API-Aufrufe.

Siehe folgendes Beispiel:

```
adobe.target.getOffer({ 
  mbox: "some-mbox", 
  success: function(actions) { 
    console.log('Success', actions); 
  }, 
  error: function(status, error) { 
    console.log('Error', status, error); 
  } 
});
```

Die Aktionen, die an den Erfolgs-Callback übergeben werden, sind eine Reihe von Objekten. Angenommen, wir haben ein einzelnes JSON-Angebot mit folgendem Inhalt:

```
{ 
  "demo": {"a": 1, "b": 2} 
}
```

Die Aktionsreihe hat diese Struktur:

```
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```

Um das JSON-Angebot zu extrahieren, navigieren Sie durch Aktionen und suchen die Aktion mit `setJson`. Dann navigieren Sie durch die Inhaltsreihe.

## Nutzungsszenario {#section_85B07907B51A43239C8E3498EF58B1E5}

Angenommen, das folgende JSON-Angebot wird an Ihre Webseite geliefert:

```
{ 
    "_id": "5a65d24d8fafc966921e9169", 
    "index": 0, 
    "guid": "7c006504-c6f7-468d-a46f-f72531ea454c", 
    "isActive": true, 
    "balance": "$2,075.06", 
    "picture": "https://placehold.it/32x32", 
    "tags": [ 
      "esse", 
      "commodo", 
      "excepteur", 
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      }, 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```

Der folgende Code zeigt Ihnen, wie Sie auf das Attribut „Begrüßung“ zugreifen können:

```
adobe.target.getOffer({   
  "mbox": "name_of_mbox", 
  "params": {}, 
  "success": function(offer) {           
        console.log(offer[0].content[0].greeting); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

## Filterung von Angeboten nach dem JSON-Angebotstyp  {#section_52533555BCE6420C8A95EB4EB8907BDE}

Sie können die Angebotsbibliothek nach dem JSON-Angebotstyp filtern, indem Sie auf die Dropdownliste **[!UICONTROL Typ]** klicken und dann das Kontrollkästchen **[!UICONTROL JSON]** aktivieren.

![](assets/offer-json-filter.png)

