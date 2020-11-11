---
keywords: adobe.target.triggerView;triggerView;triggerview;trigger view;at.js;functions;function;viewName;viewname;view name
description: Informationen zur Funktion adobe.target.triggerView (viewName, options) für die JavaScript-Bibliothek von Adobe Target at.js.
title: adobe.target.triggerView (viewName, options) - at.js 2.x
feature: client-side
translation-type: tm+mt
source-git-commit: 5c7ab4af3d4290ef8fa53ed51ed1c2e8336e02f9
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 92%

---


# adobe.target.triggerView (viewName, options) - at.js 2.x

Diese Funktion kann immer aufgerufen werden, wenn eine neue Seite geladen wird oder wenn eine Komponente auf einer Seite erneut wiedergegeben wird. `adobe.target.triggerView()` sollte für Einzelseiten-Apps (SPAs) implementiert werden, um den Visual Experience Composer (VEC) zum Erstellen von A/B-Tests und Erlebnis-Targeting(XT)-Aktivitäten verwenden zu können. Wenn `adobe.target.triggerView()` nicht auf der Site implementiert ist, kann VEC für SPAs nicht verwendet werden. Weitere Informationen finden Sie unter [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

>[!NOTE]
>
>Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*.

| Parameter | Typ | Erforderlich? | Beschreibung |
| --- | --- | --- | --- |
| viewName | Zeichenfolge | Ja | Geben Sie eine beliebige Zeichenfolge als Namen für Ihre Ansicht an. Der Name dieser Ansicht wird im Bedienfeld [!UICONTROL Änderungen] von VEC angezeigt, sodass Marketing-Experten Aktionen erstellen und ihre A/B- und XT-Aktivitäten ausführen können. |
| options | Objekt | Nein |  |
| Optionen > Seite | Boolesch | Nein | **TRUE:** Der Standardwert der Seite ist „wahr“. Bei page=true werden Benachrichtigungen zum Erhöhen der Impressions-Anzahl an das [!DNL Target]-Backend gesendet.<br>Eine Benachrichtigung wird immer standardmäßig gesendet, wenn ein Aufruf erfolgt, es sei denn, &quot;Optionen&quot;> &quot;Seite&quot;ist auf &quot;false&quot;gesetzt. `triggerView`<br>**FALSE:** Bei page=false werden keine Benachrichtigungen zum Erhöhen der Impressions-Anzahl gesendet. Dies sollte verwendet werden, wenn Sie nur eine Komponente auf einer Seite mit einem Angebot neu rendern möchten. |

## Beispiel: True

Aufruf von `triggerView()`, um eine Benachrichtigung an das Target-Backend zur Erhöhung der Aktivitätsimpressionen und anderer Metriken zu senden.

```
adobe.target.triggerView("homeView")
```

## Beispiel: False

Aufruf von `triggerView()`, um keine Benachrichtigungen zur Impressions-Zählung an das Target-Backend zu senden.

```
adobe.target.triggerView("homeView", {page: false})
```
