---
description: 'Informationen zur Funktion targetPageParams() für at.js. '
keywords: targetPageParams;targetpageparams;pageParams;pageparams;Seite Parameter;Seitenparameter;at.js;Funktionen;Funktion
seo-description: Informationen zur Funktion targetPageParams() für die Adobe Target-JavaScript-Bibliothek at.js.
seo-title: Informationen zur Funktion targetPageParams() für die Adobe Target-JavaScript-Bibliothek at.js.
solution: Target
subtopic: Erste Schritte
title: targetPageParams()
topic: Standard
translation-type: tm+mt
source-git-commit: ef2c4ac78fef5889d5a6e9e053dfd36b77919dd4

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen.

Diese Funktion zeichnet sich dadurch aus, dass damit dieselbe Parameterkonfiguration für mehrere Mbox-Aufrufe verwendet werden kann. Sie muss vom Kunden definiert werden. Sie sollte ein Array an Parametern zurückgeben, die nur an die globale Mbox-Anfrage übergeben werden. Diese Funktion kann definiert werden, bevor at.js geladen wird, oder alternativ unter **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]** &gt; **[!UICONTROL at.js-Einstellungen bearbeiten]** &gt; **[!UICONTROL Codeeinstellungen]** &gt; **[!UICONTROL Bibliothekskopfzeile]**.

Verwenden Sie die Funktion „`targetPageParams()`“ auf eine der folgenden Arten, um Parameter an „target-global-mbox“ zu übergeben:

* Als eine durch kaufmännisches Und getrennte Liste
* Als Array
* Als JSON-Objekt

## Beispiele

Durch kaufmännisches Und getrennte Liste (Werte müssen URL-codiert sein):

```
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (Werte müssen nicht URL-codiert sein):

```
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (Werte müssen nicht URL-codiert sein):

```
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
