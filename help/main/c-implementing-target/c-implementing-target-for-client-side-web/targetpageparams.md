---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;Seite Parameter;Seitenparameter;at.js;Funktionen;Funktion
description: Verwenden Sie die Funktion targetPageParams() für die Adobe [!DNL Target] JavaScript-Bibliothek at.js , um Parameter von außerhalb des Anforderungscodes an die globale Mbox anzuhängen.
title: Wie verwende ich die Funktion targetPageParams()?
feature: at.js
role: Developer
exl-id: 0772b400-626c-45d8-a4b5-a12691978cf3
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 72%

---

# targetPageParams()

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen.

Diese Funktion zeichnet sich dadurch aus, dass damit dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden kann. Sie muss vom Kunden definiert werden. Sie sollte ein Array an Parametern zurückgeben, die nur an die globale Mbox-Anfrage übergeben werden. Diese Funktion kann definiert werden, bevor at.js geladen wird oder in **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Bearbeiten]** > **[!UICONTROL Bibliothekskopfzeile]**.

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
