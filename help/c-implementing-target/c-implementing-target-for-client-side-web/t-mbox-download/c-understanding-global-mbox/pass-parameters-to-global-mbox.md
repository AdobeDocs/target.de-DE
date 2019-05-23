---
description: Die JavaScript-Funktion targetPageParams wird verwendet, um Parameter an die globale Mbox zu übergeben. Dies ist in allen Szenarien erforderlich, in denen zusätzliche Targeting- bzw. Kontextinformationen an Target übergeben werden müssen.
keywords: globale Mbox-Parameter;targetPageParams;Abfragezeichenfolge;Array;JSON;DTM;Dynamic Tag Management
seo-description: Die JavaScript-Funktion targetPageParams wird verwendet, um Parameter an die globale Mbox zu übergeben. Dies ist in allen Szenarien erforderlich, in denen zusätzliche Targeting- bzw. Kontextinformationen an Target übergeben werden müssen.
seo-title: Übergeben von Parametern an eine globale Mbox
solution: Target
subtopic: Erste Schritte
title: Übergeben von Parametern an eine globale Mbox
topic: Standard
uuid: 058f0ef5-037a-4daf-8a1e-a9c7ecc7f0bd
translation-type: tm+mt
source-git-commit: b45a1a141e9e1d229ed3f92b8124d3edf3bc3042

---


# Übergeben von Parametern an eine globale Mbox{#pass-parameters-to-a-global-mbox}

Die JavaScript-Funktion targetPageParams wird verwendet, um Parameter an die globale Mbox zu übergeben. Dies ist in allen Szenarien erforderlich, in denen zusätzliche Targeting- bzw. Kontextinformationen an Target übergeben werden müssen.

Beispiel: Verwenden Sie in einer Recommendations-Aktivität die Parameter zur Darstellung des aktuellen Produkts oder der Kategorie, die angezeigt wird.

Der Code zum Aufrufen der JavaScript-Funktion muss auf der Seite vor die globale Mbox gestellt werden, unabhängig davon, ob die globale Mbox als Teil der „mbox.js“ aktiviert wird oder manuell im Seiten-Code eingefügt wird.

>[!NOTE]
>
>Wenn Sie Parameter zu allen Mboxes auf der Seite hinzufügen möchten, nicht nur zur globalen Mbox, verwenden Sie die Funktion [targetPageParamsAll()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) (nur at.js).

Um Parameter an `target-global-mbox` zu übergeben, können Sie die Funktion `targetPageParams()` auf eine der folgenden Arten verwenden:

* Als Array
* Als JSON-Objekt
* Als eine durch kaufmännisches Und getrennte Liste

Verwenden Sie diese drei Methoden, um zu prüfen, ob die Parameter korrekt übergeben wurden. Sie können die Übergabe der Parameter möglicherweise auch mit dem [Adobe Experience Cloud-Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger.html) prüfen.

Sie müssen die JavaScript-Funktion definieren, bevor Sie die globale Mbox zu der Seite hinzufügen. Der Name muss `targetPageParams` lauten.

**Abfragezeichenfolge**

```
p1=v1&p2=v2&p3=hello%20world
```

* Name: `targetPageParams`
* Ausgabewert: mit „&amp;“ getrennte Parameter mit URL-codierten Parameterwerten.

   Beispiel:  

   In diesem Beispiel hat p3 den Wert `hello world`, der URL-codiert ist.

Das folgende Beispiel zeigt, wie der Code für die Seite aussehen könnte:

```
<html> 
  <head> 
    <title>Title here..</title> 
    <script type="text/javascript"> 
        function targetPageParams() { 
           
<b>return "p1=v1&p2=v2&p3=hello%20world"</b>; 
        } 
    </script> 
    <script src="mbox.js" type="text/javascript"></script> 
  </head> 
  <body>Body here... 
  </body> 
</html>
```

In diesem Beispiel werden die folgenden Daten an die Mbox-Edge gesendet:

* p1=v1
* p2=v2
* p3=hello world

**Array**

```
<!--window.-->targetPageParams = function() { 
  return ["a=1", "b=2", "c=hello world"]; 
}; 
```

Die Werte müssen nicht URL-codiert sein. Wenn beispielsweise ein Wert ein Leerzeichen enthält, dann muss dieses Leerzeichen nicht codiert werden.

In diesem Beispiel werden die folgenden Daten an die Mbox-Edge gesendet:

* a=1
* b=2
* c=hello world

**JSON**

JSON ist eine leistungsstarke Methode zur Übergabe von Parametern. Target verwendet die JSON-Objektschlüssel, um komplizierte Strukturen in einfache Parameter abzuflachen.

```
<!--window.-->targetPageParams = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
                  "memberStatus": Gold, 
                  "country": { 
                                "city": "San Francisco" 
                            } 
              } 
  }; 
}; 
```

Die Werte müssen nicht URL-codiert sein. Beispiel: Bei „San Francisco“ muss das Leerzeichen nicht codiert werden. Ein Leerzeichen genügt.

In diesem Beispiel werden die folgenden Daten an die Mbox-Edge gesendet:

* a=1
* b=2
* `profile.age`=26
* `profile.country.city`=San Francisco