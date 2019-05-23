---
description: 'Informationen zur Funktion adobe. target. triggerview (viewname, options) für at. js. '
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Informationen zur Funktion adobe. target. triggerview (viewname, options) für die javascript-Bibliothek von Adobe Target at. js.
seo-title: Informationen zur Funktion adobe. target. triggerview (viewname, options) für die javascript-Bibliothek von Adobe Target at. js.
solution: Target
subtopic: Erste Schritte
title: adobe.target.triggerView (viewName, options)
topic: Standard
translation-type: tm+mt
source-git-commit: 19834da75f163d6357bc9b986a23f0bc1fea6d8e

---


# adobe. target. triggerview (viewname, options) - at. js 2. x

Diese Funktion kann immer aufgerufen werden, wenn eine neue Seite geladen wird oder wenn eine Komponente auf einer Seite erneut wiedergegeben wird. `adobe.target.triggerView()` sollte für Einzelseiten-Apps (SPAs) implementiert werden, um den Visual Experience Composer (VEC) zum Erstellen von A/B-Tests und Erlebnis-Targeting(XT)-Aktivitäten verwenden zu können. Wenn `adobe.target.triggerView()` nicht auf der Site implementiert ist, kann VEC für SPAs nicht verwendet werden. Weitere Informationen finden Sie unter [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

>[!NOTE]
>
>Diese Funktion wurde mit at. js 2. x eingeführt. Diese Funktion steht für at. js Version 1 nicht zur Verfügung.*x*.

| Parameter | Typ | Erforderlich? | Beschreibung |
| --- | --- | --- | --- |
| viewName | Zeichenfolge | Ja | Geben Sie eine beliebige Zeichenfolge als Namen für Ihre Ansicht an. Der Name dieser Ansicht wird im Bedienfeld [!UICONTROL Änderungen] von VEC angezeigt, sodass Marketing-Experten Aktionen erstellen und ihre A/B- und XT-Aktivitäten ausführen können. |
| options | Objekt | Nein |
| Optionen &gt; Seite | Boolesch | Nein | **TRUE:** Der Standardwert der Seite ist „wahr“. Bei page=true werden Benachrichtigungen zum Erhöhen der Impressions-Anzahl an das [!DNL Target]-Backend gesendet.<br>**FALSE:** Wenn Seite = false, werden Benachrichtigungen nicht zur Erhöhung der Impressionsanzahl gesendet. Dies sollte verwendet werden, wenn Sie nur eine Komponente auf einer Seite mit einem Angebot neu rendern möchten. |

## Beispielaufruf von `triggerView()`, was eine Benachrichtigung an das Target-Backend sendet, um die Impressions-Anzahl zu erhöhen

```
adobe.target.triggerView("homeView")
```

## Beispielaufruf von `triggerView()`, um keine Benachrichtigungen zur Impressions-Zählung an das Target-Backend zu senden

```
adobe.target.triggerView("homeView", {page: false})
```
