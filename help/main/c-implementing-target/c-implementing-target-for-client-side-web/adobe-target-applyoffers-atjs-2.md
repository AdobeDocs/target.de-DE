---
keywords: adobe.target.applyoffer;Applyoffer;applyangebote;Angebote anwenden;at.js;Funktionen; funktion
description: Verwenden Sie die Funktion adobe.target.applyOffers() für die Adobe [!DNL Target] JavaScript-Bibliothek at.js , um mehrere Angebote in der Antwort anzuwenden. (at.js 2.x)
title: Wie verwende ich die Funktion adobe.target.applyOffers()?
feature: at.js
role: Developer
exl-id: a6f4c755-e5a0-4228-90f3-0f9d3b092cd8
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 88%

---

# adobe.target.applyOffers(options) - at.js 2.x

Mit dieser Funktion können Sie mehr als ein Angebot, das von `adobe.target.getOffers()` abgerufen wurde, anwenden.

>[!NOTE]
>
>Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*.

| Schlüssel | Typ | Erforderlich? | Beschreibung |
| --- | --- | --- | --- |
| selector | Zeichenfolge | Nein | HTML-Element oder „selector“ in CSS wird dazu verwendet, das HTML-Element zu identifizieren, in dem [!DNL Target] die Angebotsinhalte platzieren soll. Wenn kein Selektor bereitgestellt wird, [!DNL Target] geht davon aus, dass das zu verwendende HTML-Element HTML HEAD ist. |
| Antwort | Objekt | Ja | Antwortobjekt von `getOffers()`.<br>Siehe Anfragetabelle unten. |

## Antwort

>[!NOTE]
>
>Lesen Sie die [Dokumentation zur Bereitstellungs-API](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) für Informationen zu den akzeptablen Typen für alle unten aufgeführten Felder.

| Feldname | Beschreibung |
| --- | --- |
| Antwort > Vorab abrufen > Ansichten > Optionen > Inhalt | Beachten Sie, dass der Inhalt von „Option“ nicht klar definiert ist und direkt vom Optionstyp/von der Vorlagenstruktur abhängt. |
| Antwort > Vorab abrufen > Ansichten > Optionen > Typ | Optionstyp. Spiegelt den Typ des Feldes „Inhalt“ wider. Der unterstützte Typ ist „Aktionen“. |
| Antwort > Vorab abrufen > Ansichten > Status | Ein Status-Token „verdunkelte Ansicht“, das mit der Anzeigebenachrichtigung für die Ansicht weitergeleitet werden sollte |
| Antwort > Vorab abrufen > Ansichten > Optionen > responseTokens | Enthält die Zuordnung von `responseTokens`, die gesammelt wurden, währen die aktuelle Option verarbeitet wurde. |
| Antwort > Vorab abrufen > Ansichten > Analyse > Nutzlast | Analysenutzlast für die Client-seitige Integration, die nach Anwendung der Ansicht an Analytics gesendet werden sollten. |
| Antwort > Vorab abrufen > Ansichten > Verfolgen | Das Objekt, das alle Trace-Daten für den Vorab-Aufruf pro Ansicht enthält.<br>Das Trace-Objekt enthält auch eine Version für die Nachverfolgung.<br>Das Trace-Objekt enthält auch Details zur aktuellen Ansicht. |
| Antwort > Vorab abrufen > Ansichten > Optionen > eventToken | Die Ereignisprotokollierung erfolgt pro Option. Für jede angewendete Option sollte das entsprechende Ereignis-Token zur Liste der Benachrichtigungs-Token hinzugefügt werden. Beachten Sie, dass eine Ansicht aus mehreren Optionen besteht. Wenn alle Optionen angewendet und angezeigt wurden, müssen alle `eventTokens` in die Benachrichtigung einbezogen werden. |
| Antwort > Vorab abrufen > Ansichten > Name | Der für Menschen lesbare Anzeigename. |
| Antwort > Vorab abrufen > Ansichten > Metriken | Berichtsmetriken, die überwacht werden sollen und dann [!DNL Target] darüber benachrichtigen. Derzeit wird nur die Klickmetrik unterstützt. Wenn ein Klick auf das Element erfolgt, sollten die entsprechenden `eventTokens` erfasst und eine Benachrichtigung gesendet werden. |
| Antwort > Vorab abrufen > Ansichten > Schlüssel | Der Schlüssel oder Fingerabdruck, mit dem die Ansicht identifiziert wird. |
| Antwort > Vorab abrufen > Ansichten > ID | ID der Ansicht. |
| Antwort > Benachrichtigungen > ID | Benachrichtigungs-ID. |
| Antwort > Benachrichtigungen > Ereignisse > Typ | Der Typ der Benachrichtigung, des Klicks oder der Anzeige. |
| Antwort > Benachrichtigungen > Ereignisse > Verfolgen | Die Verfolgung des Benachrichtigungsereignisses. |
| Antwort > Benachrichtigungen > Ereignisse > Token | Das Token, das mit dem Benachrichtigungsereignis gesendet wurde. |
| Antwort > Benachrichtigungen > Ereignisse > Zeitstempel | Der Zeitstempel, der mit dem Benachrichtigungsereignis gesendet wurde. |
| Antwort > Benachrichtigungen > Ereignisse > errorCode | Wenn die Benachrichtigung fehlschlägt, zeigt der Code den Grund für den Fehler an. |
| Antwort > Benachrichtigungen > Ereignisse | Die Ereignisse, die für die aktuelle Benachrichtigung protokolliert wurden oder nicht protokolliert werden konnten. |
| Antwort > Benachrichtigungen | Gibt die protokollierten oder fehlgeschlagenen Benachrichtigungen an. |
| Antwort > Ausführen > Mboxes > Mbox > Verfolgen | Das Objekt, das alle Trace-Daten für jede einzelne Mbox-Anfrage enthält. |
| Antwort > Ausführen > Mboxes > Mbox > responseTokens | Enthält Zuordnung von `responseTokens` einer bestimmten Mbox-Anfragesausführung. |
| Antwort > Ausführen > Mboxes > Mbox > Option > Inhalt | Beachten Sie, dass der Inhalt von „Option“ nicht klar definiert ist und direkt vom Optionstyp/von der Vorlagenstruktur abhängt. |
| Antwort > Ausführen > Mboxes > Mbox > Option > Typ | Optionstyp. Spiegelt den Typ des Feldes „Inhalt“ wider. Unterstützt werden: HTML, Redirect, JSON und dynamisch. |
| Antwort > Ausführen > Mboxes > Mbox > Optionen | Antwortoption. |
| Antwort > Ausführen > Mboxes > Mbox > Metriken > eventToken | Token des Klickereignisses. |
| Antwort > Ausführen > Mboxes > Mbox > Metriken > Typ | &quot;click&quot; |
| Antwort > Ausführen > Mboxes > Mbox > Metriken | Enthält eine Liste der `clickThrough`-Metriken. |
| Antwort > Ausführen > Mboxes > Mbox > Mbox | Der Name der Mbox. |
| Antwort > Ausführen > Mboxes > Mbox > Index | Gibt an, dass mit diesem Index der Anfrage die Antwort für Mbox ist. |
| Antwort > Ausführen > Mboxes > Mbox > Analyse > Nutzlast | Analysenutzlast für die Client-seitige Integration, die nach Anwendung der Mbox an Analytics gesendet werden sollten. (Siehe Abschnitt „Kampagnen mit A4T“.) |
| Antwort > Ausführen > Mboxes | Liste der ausgeführten Mboxes. |
| Antwort > Ausführen > pageLoad > Optionen > Inhalt | Beachten Sie, dass der Inhalt von „Option“ nicht klar definiert ist und direkt vom Optionstyp/von der Vorlagenstruktur abhängt. |
| Antwort > Ausführen > pageLoad > Optionen > Typ | Optionstyp. Spiegelt den Typ des Feldes „Inhalt“ wider. Unterstützt werden: HTML, Redirect, JSON, dynamisch und Aktionen. |
| Antwort > Ausführen > pageLoad > Optionen | Optionen, die nicht nach Ansichten gruppiert werden (target-global-mbox + Optionen von Aktivitäten mit Ansichten, die nicht nach Ansichten gruppiert werden). |
| Antwort > Ausführen > pageLoad > Metriken | Klicken Sie auf Metriken, die nicht einer bestimmten Ansicht zugeordnet wurden. |
| Antwort > Ausführen > pageLoad > Verfolgen | Das Objekt, das alle Trace-Daten für die pageLoad-Anfrage enthält. |
| Antwort > Ausführen > pageLoad > Analyse > Nutzlast | Analysenutzlast für die Client-seitige Integration, die nach Anwendung der Inhalte beim Seitenladen an Analytics gesendet werden sollten. (Siehe Abschnitt „Kampagnen mit A4T“.) |

## Beispiel: applyOffers()-Aufruf

```javascript
adobe.target.applyOffers({response:{
  "execute": {
    "pageLoad": {
      "options": [{
        "type": "html",
        "content": "page-load"
      },
      {
        "type": "actions",
        "content": [{
          "type": "setHtml",
          "content": "<h1>Container 1</h1>",
          "selector": "#container1",
          "cssSelector": "#container1"
        },
        {
          "type": "setHtml",
          "content": "<h3>Container 3</h3>",
          "selector": "#container3",
          "cssSelector": "#container3"
        }]
      }],
 
 
      "metrics": [{
        "type": "click",
        "selector": "#container1",
        "eventToken": "page-load-click-metric" 
      }]
    }
  }
}});
```

## Beispielaufrufe der Promise-Verkettung mit `getOffers()` und `applyOffers()`, da diese Funktionen auf Promise basieren

```javascript
adobe.target.getOffers({...})
.then(response => adobe.target.applyOffers({ response: response }))
.then(() => console.log("Success"))
.catch(error => console.log("Error", error));
```

Weitere Beispiele zur Verwendung von getOffers() finden Sie in den getOffers [Dokumentation](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/at-js-implementation/functions-overview/adobe-target-getoffers-atjs-2.html)

### Beispiel für Seitenladeanforderung


```javascript
adobe.target.getOffers({
    request: {
        execute: {
            pageLoad: {}
        }
    }
}).
then(response => adobe.target.applyOffers({ response: response }))
.then(() => console.log("Success"))
.catch(error => console.log("Error", error));
```
