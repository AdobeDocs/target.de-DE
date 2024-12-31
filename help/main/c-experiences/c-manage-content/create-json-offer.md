---
keywords: JSON-Angebot;JSON-Angebot erstellen
description: Erfahren Sie, wie Sie JSON-Angebote in zur Verwendung im [!UICONTROL Form-Based Experience Composer] erstellen.
title: Wie erstelle ich JSON-Angebote?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: 98613f43c5f135a6ce61a4b8dcc7f2b372df51e2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 29%

---

# Erstellen von JSON-Angeboten

Erstellen Sie JSON-Angebote im [!UICONTROL Offer Library] in [!DNL Adobe Target] zur Verwendung im [!UICONTROL Form-Based Experience Composer].

JSON-Angebote können in formularbasierten Aktivitäten verwendet werden, um Anwendungsfälle zu ermöglichen, in denen [!DNL Target] Entscheidungsfindung erforderlich ist, um ein Angebot im JSON-Format zur Verwendung in SPA-Frameworks oder Server-seitigen Integrationen zu senden.

## JSON-Überlegungen

Beachten Sie Folgendes, wenn Sie mit JSON-Angeboten arbeiten:

* JSON-Angebote sind derzeit nur für Aktivitäten der Kategorien [!UICONTROL A/B Test], [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Experience Targeting] (XT) verfügbar.
* JSON-Angebote können nur in [formularbasierten Aktivitäten](/help/main/c-experiences/form-experience-composer.md) verwendet werden.
* JSON-Angebote können direkt abgerufen werden, wenn Sie die [Server-seitigen APIs und mobilen Node.js-, Java-, .NET- und Python-SDKs](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=de){target=_blank} verwenden.
* Im Browser können JSON-Angebote nur über at.js 1.2.3 (oder höher) und mithilfe von [getOffer() abgerufen werden](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank} indem Aktionen mithilfe der `setJson`-Aktion gefiltert werden.
* JSON-Angebote werden als native JSON-Objekte und nicht als Zeichenfolgen ausgeliefert. Nutzer dieser Objekte müssen diese also nicht mehr als Zeichenfolgen behandeln und in JSON-Objekte konvertieren.
* JSON-Angebote werden im Gegensatz zu anderen Angeboten (z. B. HTML-Angeboten) nicht automatisch eingesetzt, da es sich bei JSON-Angeboten um nicht visuelle Angebote handelt. Entwickler müssen Code schreiben, um das Angebot explizit mit [getOffer() abzurufen](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank}.

## Erstellen eines JSON-Angebots {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Klicken Sie auf **[!UICONTROL Offers]** > **[!UICONTROL Code Offers]**.

   ![Angebote > Registerkarte „Code-Angebote“](/help/main/c-experiences/c-manage-content/assets/code-offers-tab.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL JSON Offer]**.

   ![offer-json-Bild](assets/offer-json.png)

1. Geben Sie einen Angebotsnamen ein.
1. Geben Sie Ihren JSON-Code in das **[!UICONTROL Code]** ein.
1. Klicken Sie auf **[!UICONTROL Save]**.

## JSON-Beispiel {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON-Angebote werden nur in Aktivitäten unterstützt, die mit dem [formularbasierten Experience Composer) erstellt ](/help/main/c-experiences/form-experience-composer.md). Die einzige Möglichkeit, JSON-Angebote zu verwenden, besteht derzeit in direkten API-/SDK-Aufrufen.

Siehe folgendes Beispiel:

```json
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

```json
{ 
  "demo": {"a": 1, "b": 2} 
}
```

Das Aktionen-Array weist die folgende Struktur auf:

```json
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```

Um das JSON-Angebot zu extrahieren, durchlaufen Sie die Aktionen und suchen Sie die Aktion mit der `setJson` Aktion. Durchlaufen Sie anschließend das Inhalts-Array.

## Anwendungsfall {#section_85B07907B51A43239C8E3498EF58B1E5}

Angenommen, das folgende JSON-Angebot wird an Ihre Webseite geliefert:

```json
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
      "excepteur"
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      } 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```

Der folgende Code zeigt Ihnen, wie Sie auf das Attribut „Begrüßung“ zugreifen können:

```json
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

## JSON-Angebotsbeispiel mit Real-Time CDP-Profilattributen

Real-Time CDP-Profilattribute können für [!DNL Target] freigegeben werden, um sie in HTML- und JSON-Angeboten zu verwenden.

Weitere Informationen finden Sie unter [Freigeben von Real-Time CDP-Profilattributen für [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).

## Filtern von Angeboten nach dem JSON-Angebotstyp {#section_52533555BCE6420C8A95EB4EB8907BDE}

Sie können die [!UICONTROL Offers] nach dem JSON-Angebotstyp filtern, indem Sie auf die Dropdown-Liste **[!UICONTROL Type]** klicken und dann das Kontrollkästchen **[!UICONTROL JSON]** aktivieren.

![offer-json-filter-image](assets/offer-json-filter.png)
