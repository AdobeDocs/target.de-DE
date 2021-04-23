---
keywords: adobe. target. applyoffer; Applyoffer; applyoffer; Angebot anwenden; at.js; Funktionen; funktion
description: Verwenden Sie die JavaScript-Bibliothek "adobe.Zielgruppe.applyOffer()"für die Adobe [!DNL Target] at.js, um den Antwortinhalt anzuwenden.
title: Wie verwende ich die Funktion adobe.Zielgruppe.applyOffer()?
feature: 'at.js '
role: Developer
exl-id: d230d48f-0d6c-4f55-96a0-681dd31e8d16
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 73%

---

# adobe.target.applyOffer(options)

Diese Funktion dient zum Anwenden des Antwortinhalts mit [!DNL Adobe Target].

>[!NOTE]
>
>`applyOffer` erfordert den Parameter `mbox`. Wurde kein Mbox-Name angegeben, tritt ein Fehler auf.

Der Optionsparameter ist obligatorisch und hat die folgende Struktur:

| Schlüssel | Typ | Erforderlich | Beschreibung |
|--- |--- |--- |--- |
| mbox | Zeichenfolge | Ja | Name der Mbox<br>Bei at.js 1.3.0 (und höher) erzwingt Target die Verwendung des Mbox-Schlüssels. Dieser Schlüssel war früher erforderlich. Target erzwingt seine Verwendung jedoch nun, um sicherzustellen, dass Target ordnungsgemäß validiert ist und Kunden die Funktion richtig verwenden. |
| selector | Zeichenfolge oder DOM-Element | Nein | HTML-Element oder „selector“ in CSS wird dazu verwendet, das HTML-Element zu identifizieren, in dem die Angebotsinhalte platziert werden sollten. Wenn der Selektor nicht bereitgestellt wird, geht Zielgruppe davon aus, dass das HTML-Element HTML-HEAD verwenden sollte. |
| Angebot | Array | Ja | Eine Reihe von Aktionen, die auf das Element angewendet werden sollen |

## Beispiel {#section_D8D6A17B73DE4542937CDB687193A5CC}

Das folgende Beispiel demonstriert, wie `getOffer` und `applyOffer` gemeinsam genutzt werden:

```javascript
adobe.target.getOffer({   
  "mbox": "mbox",   
  "success": function(offers) {           
        adobe.target.applyOffer( {  
           "mbox": "mbox", 
           "offer": offers  
        } ); 
  },   
  "error": function(status, error) {           
      if (console && console.log) { 
        console.log(status); 
        console.log(error); 
      } 
  }, 
 "timeout": 5000 
}); 
```
