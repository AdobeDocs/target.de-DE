---
keywords: targetPageParamsAll;targetpageparamsall;PageParamsAll;pageparamsall;Seite Parameter;Seitenparameter;at.js;Funktionen;Funktion
description: Informationen zur Funktion targetPageParamsAll() für die Adobe Target-JavaScript-Bibliothek at.js.
title: Informationen zur Funktion targetPageParamsAll() für die Adobe Target-JavaScript-Bibliothek at.js.
subtopic: Erste Schritte
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

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
