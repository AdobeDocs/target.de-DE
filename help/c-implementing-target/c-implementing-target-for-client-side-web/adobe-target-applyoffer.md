---
description: 'Informationen zur Funktion adobe. target. applyoffer (options) für at. js. '
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Informationen über die Funktion adobe. target. applyoffer (options) für die javascript-Bibliothek von Adobe Target at. js.
seo-title: Informationen über die Funktion adobe. target. applyoffer (options) für die javascript-Bibliothek von Adobe Target at. js.
solution: Target
subtopic: Erste Schritte
title: adobe.target.applyOffer(options)
topic: Standard
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# adobe.target.applyOffer(options) {#reference_BBE83F513B5B4E03BBC3F50D90864245}

Diese Funktion dient zur Anwendung der Antwortinhalte.

>[!NOTE]
>
>`applyOffer` erfordert den Parameter `mbox`. Wurde kein Mbox-Name angegeben, tritt ein Fehler auf.

Der Optionsparameter ist obligatorisch und hat die folgende Struktur:

| Schlüssel | Typ | Erforderlich | Beschreibung |
|--- |--- |--- |--- |
| mbox | Zeichenfolge | Ja | Mbox namewith<br>at. js 1.3.0 (und höher) Target erzwingt, dass der mbox-Schlüssel verwendet wird. Dieser Schlüssel war früher erforderlich. Target erzwingt seine Verwendung jedoch nun, um sicherzustellen, dass Target ordnungsgemäß validiert ist und Kunden die Funktion richtig verwenden. |
| selector | Zeichenfolge oder DOM-Element | Nein | HTML-Element oder „selector“ in CSS wird dazu verwendet, das HTML-Element zu identifizieren, in dem die Angebotsinhalte platziert werden sollten. Wenn kein „selector“ bereitgestellt wurde, geht Target davon aus, dass das zu verwendende HTML-Element HTML HEAD lautet. |
| anzeigen | Array | Ja | Eine Reihe von Aktionen, die auf das Element angewendet werden sollen |

## Beispiel {#section_D8D6A17B73DE4542937CDB687193A5CC}

Das folgende Beispiel demonstriert, wie `getOffer` und `applyOffer` gemeinsam genutzt werden:

```
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
