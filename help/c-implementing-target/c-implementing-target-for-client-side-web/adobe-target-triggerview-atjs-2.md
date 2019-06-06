---
description: 'Informationen zur Funktion adobe.target.triggerView (viewName, options) für at.js. '
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Informationen zur Funktion adobe.target.triggerView (viewName, options) für die JavaScript-Bibliothek von Adobe Target at.js.
seo-title: Informationen zur Funktion adobe.target.triggerView (viewName, options) für die JavaScript-Bibliothek von Adobe Target at.js.
solution: Target
subtopic: Erste Schritte
title: adobe.target.triggerView (viewName, options)
topic: Standard
translation-type: tm+mt
source-git-commit: e7ec5af38c1ea55a9cb86f0c706a024bd0f96e6e

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
| Optionen &gt; Seite | Boolesch | Nein | **TRUE:** Der Standardwert der Seite ist „wahr“. Bei page=true werden Benachrichtigungen zum Erhöhen der Impressions-Anzahl an das [!DNL Target]-Backend gesendet.<br>Wenn der Ansicht keine Aktivität oder Aktivitätsmetrik zugeordnet ist, wird keine Benachrichtigung gesendet.<br>**FALSE:** Bei page=false werden keine Benachrichtigungen zum Erhöhen der Impressions-Anzahl gesendet. Dies sollte verwendet werden, wenn Sie nur eine Komponente auf einer Seite mit einem Angebot neu rendern möchten. |

## Beispiel: True

`triggerView()` Aufruf, um eine Benachrichtigung an den Target-Back-Backend zur inkrementierten Aktivitätsimpressionen und anderen Metriken zu senden.

```
adobe.target.triggerView("homeView")
```

## Beispiel: False

`triggerView()` Keine Benachrichtigungen an das Target-Backend zur Impressionszählung gesendet.

```
adobe.target.triggerView("homeView", {page: false})
```
