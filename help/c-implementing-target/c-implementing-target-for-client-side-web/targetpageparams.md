---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;Seite Parameter;Seitenparameter;at.js;Funktionen;Funktion
description: Informationen zur Funktion targetPageParams() für die Adobe Target-JavaScript-Bibliothek at.js.
title: targetPageParams()
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 88%

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen.

Diese Funktion zeichnet sich dadurch aus, dass damit dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden kann. Sie muss vom Kunden definiert werden. Sie sollte ein Array an Parametern zurückgeben, die nur an die globale Mbox-Anfrage übergeben werden. Diese Funktion kann definiert werden, bevor at.js geladen wird oder in **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Bearbeiten]** > **[!UICONTROL Bibliothekskopf]**.

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
