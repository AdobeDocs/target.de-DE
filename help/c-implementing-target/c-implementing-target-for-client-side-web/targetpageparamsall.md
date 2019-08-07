---
description: 'Informationen zur Funktion targetPageParamsAll() für at.js. '
keywords: Targetpageparamsall; targetpageparamsall; Pageparamsall; pageparamsall; page params; page parameters; at. js; Funktionen; function
seo-description: Informationen zur Funktion targetPageParamsAll() für die Adobe Target-JavaScript-Bibliothek at.js.
seo-title: Informationen zur Funktion targetPageParamsAll() für die Adobe Target-JavaScript-Bibliothek at.js.
solution: Target
subtopic: Erste Schritte
title: targetPageParamsAll()
topic: Standard
translation-type: tm+mt
source-git-commit: ef2c4ac78fef5889d5a6e9e053dfd36b77919dd4

---


# targetPageParamsAll()

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an alle Mboxes anfügen.

Dies ist sehr nützlich, wenn dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden soll. Sie muss vom Kunden definiert werden. Sie sollte ein Array von Parametern zurückgeben, die an alle Mbox-Aufrufe auf der Seite übergeben werden. Diese Funktion kann definiert werden, bevor at.js geladen wird, oder alternativ unter **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]** &gt; **[!UICONTROL at.js-Einstellungen bearbeiten]** &gt; **[!UICONTROL Codeeinstellungen]** &gt; **[!UICONTROL Bibliothekskopfzeile]**.

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
