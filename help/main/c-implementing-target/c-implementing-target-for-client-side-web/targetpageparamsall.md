---
keywords: targetPageParamsAll;targetpageparamsall;PageParamsAll;pageparamsall;Seite Parameter;Seitenparameter;at.js;Funktionen;Funktion
description: Verwenden Sie die Funktion targetPageParamsAll() für die Adobe [!DNL Target] at.js-JavaScript-Bibliothek , um Parameter von außerhalb des Anforderungscodes an alle Mboxes anzuhängen.
title: Wie verwende ich die Funktion targetPageParamsAll()?
feature: at.js
role: Developer
exl-id: 58fbb62e-30da-486f-b771-6452ad5e27e6
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 72%

---

# targetPageParamsAll()

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an alle Mboxes anfügen.

Dies ist sehr nützlich, wenn dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden soll. Sie muss vom Kunden definiert werden. Sie sollte ein Array von Parametern zurückgeben, die an alle Mbox-Aufrufe auf der Seite übergeben werden. Diese Funktion kann definiert werden, bevor at.js geladen wird oder in **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Bearbeiten]** > **[!UICONTROL Codeeinstellungen]** > **[!UICONTROL Bibliothekskopfzeile]**.

Verwenden Sie die Funktion „targetPageParamsAll()“ auf eine der folgenden Arten, um Parameter an „target-global-mbox“ zu übergeben:

* Als eine durch kaufmännisches Und getrennte Liste
* Als Array
* Als JSON-Objekt

## Beispiele

Durch kaufmännisches Und getrennte Liste (Werte müssen URL-codiert sein):

```javascript
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (Werte müssen nicht URL-codiert sein):

```javascript
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (Werte müssen nicht URL-codiert sein):

```javascript
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
