---
keywords: globale Mbox-Parameter;targetPageParams;Abfrage-Zeichenfolge;array;json;dtm
description: Erfahren Sie, wie Sie mit der Funktion targetPageParams zusätzliche Targeting- oder Kontextdaten an die Adobe [!DNL Target] globale Mbox weitergeben können.
title: Wie übergebe ich Parameter an eine globale Mbox?
feature: 'at.js '
role: Developer
exl-id: 37d143af-83a8-48fd-91eb-58f21f8c7b94
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 60%

---

# Übergeben von Parametern an eine globale Mbox

Die JavaScript-Funktion `targetPageParams` wird verwendet, um Parameter an die globale Mbox in [!DNL Adobe Target] zu übergeben. Dies ist in jedem Szenario erforderlich, in dem zusätzliche Targeting-/Kontextinformationen an [!DNL Target] weitergegeben werden sollen.

Verwenden Sie beispielsweise in einer [!DNL Recommendations]-Aktivität die Parameter, um das aktuelle Produkt oder die aktuelle Kategorie, die angezeigt wird, darzustellen.

Der Code zum Aufrufen der JavaScript-Funktion muss vor der globalen Mbox auf der Seite stehen, unabhängig davon, ob die globale Mbox als Teil von at.js ausgelöst oder manuell im Seiten-Code eingefügt wird.

>[!NOTE]
>
>Wenn Sie allen mboxes auf der Seite Parameter hinzufügen möchten, nicht nur der globalen Mbox, verwenden Sie die Funktion [targetPageParamsAll()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md).

Um Parameter an `target-global-mbox` zu übergeben, können Sie die Funktion `targetPageParams()` auf eine der folgenden Arten verwenden:

* Als Array
* Als JSON-Objekt
* Als eine durch kaufmännisches Und getrennte Liste

Verwenden Sie diese drei Methoden, um zu prüfen, ob die Parameter korrekt übergeben wurden. Sie können die Übergabe der Parameter möglicherweise auch mit dem [Adobe Experience Cloud-Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) prüfen.

Sie müssen die JavaScript-Funktion definieren, bevor Sie die globale Mbox zu der Seite hinzufügen. Der Name muss `targetPageParams` lauten.

## Abfragezeichenfolge

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
          return "p1=v1&p2=v2&p3=hello%20world";
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

## Array

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

## JSON

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
* `profile.memberStatus`=Gold
* `profile.country.city`=San Francisco
