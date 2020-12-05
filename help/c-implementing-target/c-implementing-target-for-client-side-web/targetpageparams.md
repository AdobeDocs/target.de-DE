---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;page params;page parameters;at.js;functions;function
description: Informationen zur Funktion targetPageParams() für die Adobe Target-JavaScript-Bibliothek at.js.
title: targetPageParams()
feature: client-side
translation-type: tm+mt
source-git-commit: a841c492e5d9e4bfedb20133ba32e37daf738c57
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 88%

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen.

Diese Funktion zeichnet sich dadurch aus, dass damit dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden kann. Sie muss vom Kunden definiert werden. Sie sollte ein Array an Parametern zurückgeben, die nur an die globale Mbox-Anfrage übergeben werden. This function can be defined before at.js is loaded or in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Library Header]**.

Verwenden Sie die Funktion „`targetPageParams()`“ auf eine der folgenden Arten, um Parameter an „target-global-mbox“ zu übergeben:

* Als eine durch kaufmännisches Und getrennte Liste
* Als Array
* Als JSON-Objekt

## Beispiele

Durch kaufmännisches Und getrennte Liste (Werte müssen URL-codiert sein):

```javascript
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (Werte müssen nicht URL-codiert sein):

```javascript
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (Werte müssen nicht URL-codiert sein):

```javascript
targetPageParams = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
        "age": 26, 
        "country": { 
          "city": "San Francisco" 
        } 
      } 
  }; 
};
```
