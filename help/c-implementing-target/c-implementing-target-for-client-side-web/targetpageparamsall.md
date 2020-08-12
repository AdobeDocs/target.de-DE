---
keywords: targetPageParamsAll;targetpageparamsall;PageParamsAll;pageparamsall;page params;page parameters;at.js;functions;function
description: Informationen zur Funktion targetPageParamsAll() für die Adobe Target-JavaScript-Bibliothek at.js.
title: Informationen zur Funktion targetPageParamsAll() für die Adobe Target-JavaScript-Bibliothek at.js.
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 88%

---


# targetPageParamsAll()

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an alle Mboxes anfügen.

Dies ist sehr nützlich, wenn dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden soll. Sie muss vom Kunden definiert werden. Sie sollte ein Array von Parametern zurückgeben, die an alle Mbox-Aufrufe auf der Seite übergeben werden. This function can be defined before at.js is loaded or in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

Verwenden Sie die Funktion „targetPageParamsAll()“ auf eine der folgenden Arten, um Parameter an „target-global-mbox“ zu übergeben:

* Als eine durch kaufmännisches Und getrennte Liste
* Als Array
* Als JSON-Objekt

## Beispiele

Durch kaufmännisches Und getrennte Liste (Werte müssen URL-codiert sein):

```
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (Werte müssen nicht URL-codiert sein):

```
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (Werte müssen nicht URL-codiert sein):

```
targetPageParamsAll = function() { 
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
