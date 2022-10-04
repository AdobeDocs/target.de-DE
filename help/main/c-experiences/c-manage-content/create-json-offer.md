---
keywords: Remote-Angebot;Remote-Angebot erstellen
description: Erfahren Sie, wie Sie in Adobe JSON-Angebote erstellen. [!DNL Target] zur Verwendung im formularbasierten Experience Composer. JSON-Angebote sind für SPA Frameworks oder serverseitige Integrationen nützlich.
title: Wie erstelle ich JSON-Angebote?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 38%

---

# Erstellen von JSON-Angeboten

Erstellen von JSON-Angeboten im [!UICONTROL Angebotsbibliothek] in [!DNL Adobe Target] zur Verwendung in [!UICONTROL Form-Based Experience Composer].

JSON-Angebote können in formularbasierten Aktivitäten verwendet werden, wodurch Anwendungsfälle ermöglicht werden, bei denen [!DNL Target]Die Entscheidung von ist erforderlich, um ein Angebot im JSON-Format zur Verwendung in SPA Framework oder serverseitigen Integrationen zu senden.

## JSON-Überlegungen

Beachten Sie Folgendes, wenn Sie mit JSON-Angeboten arbeiten:

* JSON-Angebote sind derzeit nur für [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT).
* JSON-Angebote können in [formularbasierte Aktivitäten](/help/main/c-experiences/form-experience-composer.md) nur.
* JSON kann direkt abgerufen werden, wenn Sie die Server-seitige API, das Mobile-SDK oder das NodeJS-SDK verwenden.
* Im Browser kann JSON NUR über at.js 1.2.3 (oder neuer) und mit  [getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank} durch Filtern von Aktionen mithilfe der `setJson` Aktion.
* JSON-Angebote werden als native JSON-Objekte und nicht als Zeichenfolgen ausgeliefert. Nutzer dieser Objekte müssen diese also nicht mehr als Zeichenfolgen behandeln und in JSON-Objekte konvertieren.
* JSON-Angebote werden im Gegensatz zu anderen Angeboten (z. B. HTML-Angeboten) nicht automatisch eingesetzt, da es sich bei JSON-Angeboten um nicht visuelle Angebote handelt. Der Entwickler muss Code schreiben, um das Angebot explizit zum Einsatz zu bringen.  [getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank}.

## Erstellen eines JSON-Angebots {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Klicken **[!UICONTROL Angebote]** > **[!UICONTROL Code-Angebote]**.

   ![Registerkarte Angebote > Code-Angebote](/help/main/c-experiences/c-manage-content/assets/code-offers-tab.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL JSON-Angebot]**.

   ![offer-json-Bild](assets/offer-json.png)

1. Geben Sie einen Angebotsnamen ein.
1. Schreiben Sie Ihren JSON-Code in das Feld **[!UICONTROL Code]** oder kopieren Sie ihn dorthin.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## JSON-Beispiel {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON-Angebote werden nur in Aktivitäten unterstützt, die mit der [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md). Die einzige Möglichkeit, JSON-Angebote zu nutzen, läuft derzeit über direkte API-Aufrufe.

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

Die Aktionsreihe hat diese Struktur:

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

Um das JSON-Angebot zu extrahieren, navigieren Sie durch Aktionen und suchen die Aktion mit der `setJson` und navigieren Sie dann durch das Inhalts-Array.

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

## JSON-Angebotsbeispiel mit Echtzeit-Kundendatenplattform-Profilattributen

Echtzeit-Kundendatenplattform-Profilattribute können für Target freigegeben werden, um sie in HTML- und JSON-Angeboten zu verwenden. (Beachten Sie, dass diese Funktion derzeit nur als Betaversion verfügbar ist.)

Anwendungsbeispiel: Als Online-Marketing-Experte möchte Grace, dass das AEP/Unified Profile Attributwerte mit Target teilt, um eine Echtzeit-Personalisierung zu ermöglichen. Durch die Verwendung von Echtzeit-Kundendatenplattform-Profilattributen kann Grace den Wert des AEP-Attributs in einem Target-Angebot mithilfe der Token-Ersetzung anzeigen. Sie kann beispielsweise entsprechend der Lieblingsfarbe eines Kunden personalisieren, indem sie `${aep.profile.favoriteColor}`oder deren Loyalitäts- und Treuepunktwert mithilfe der Token `${aep.loyalty.tier}` und `${aep.loyalty.points}`.

![offer-json-aep-shared-attribute image](assets/offer-json-aep-shared-attribute.png)

Beachten Sie im oben gezeigten Beispiel, dass die Zuweisung von Standardwerten optional ist.

## Filtern von Angeboten nach dem JSON-Angebotstyp {#section_52533555BCE6420C8A95EB4EB8907BDE}

Sie können die [!UICONTROL Angebote] Bibliothek nach dem JSON-Angebotstyp durch Klicken auf **[!UICONTROL Typ]** Dropdown-Liste aus und wählen Sie dann die **[!UICONTROL JSON]** aktivieren.

![offer-json-filter-Bild](assets/offer-json-filter.png)
