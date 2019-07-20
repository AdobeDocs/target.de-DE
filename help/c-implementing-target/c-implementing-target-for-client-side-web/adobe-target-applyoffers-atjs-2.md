---
description: 'Informationen zur Funktion adobe.target.applyOffers(options) für at.js. '
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Informationen zur Funktion adobe.target.applyOffers(options) für die JavaScript-Bibliothek von Adobe Target at.js.
seo-title: Informationen zur Funktion adobe.target.applyOffers(options) für die JavaScript-Bibliothek von Adobe Target at.js.
solution: Target
subtopic: Erste Schritte
title: adobe.target.applyOffers(options)
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# adobe.target.applyOffers(options) - at.js 2.x

Mit dieser Funktion können Sie mehr als ein Angebot, das von `adobe.target.getOffers()` abgerufen wurde, anwenden.

>[!NOTE]
>
>Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*.

| Schlüssel | Typ | Erforderlich? | Beschreibung |
| --- | --- | --- | --- |
| selector | Zeichenfolge | Nein | HTML-Element oder „selector“ in CSS wird dazu verwendet, das HTML-Element zu identifizieren, in dem [!DNL Target] die Angebotsinhalte platzieren soll. Wenn kein „selector“ bereitgestellt wurde, geht [!DNL Target] davon aus, dass das zu verwendende HTML-Element HTML HEAD lautet. |
| Antwort | Objekt | Ja | Antwortobjekt von `getOffers()`.<br>Siehe Anfragetabelle unten. |

## Antwort

| Feldname | Beschreibung |
| --- | --- |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Optionen &gt; Inhalt | Beachten Sie, dass der Inhalt von „Option“ nicht klar definiert ist und direkt vom Optionstyp/von der Vorlagenstruktur abhängt. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Optionen &gt; Typ | Optionstyp. Spiegelt den Typ des Feldes „Inhalt“ wider. Der unterstützte Typ ist „Aktionen“. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Status | Ein Status-Token „verdunkelte Ansicht“, das mit der Anzeigebenachrichtigung für die Ansicht weitergeleitet werden sollte |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Optionen &gt; responseTokens | Enthält die Zuordnung von `responseTokens`, die gesammelt wurden, währen die aktuelle Option verarbeitet wurde. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Analyse &gt; Nutzlast | Analysenutzlast für die Client-seitige Integration, die nach Anwendung der Ansicht an Analytics gesendet werden sollten. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Verfolgen | Das Objekt, das alle Trace-Daten für den Vorab-Aufruf pro Ansicht enthält.<br>Das Trace-Objekt enthält auch eine Version für die Nachverfolgung.<br>Das Trace-Objekt enthält auch Details zur aktuellen Ansicht. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Optionen &gt; eventToken | Die Ereignisprotokollierung erfolgt pro Option. Für jede angewendete Option sollte das entsprechende Ereignis-Token zur Liste der Benachrichtigungs-Token hinzugefügt werden. Beachten Sie, dass eine Ansicht aus mehreren Optionen besteht. Wenn alle Optionen angewendet und angezeigt wurden, müssen alle `eventTokens` in die Benachrichtigung einbezogen werden. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Name | Der für Menschen lesbare Anzeigename. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Metriken | Berichtsmetriken, die überwacht werden sollen und dann [!DNL Target] darüber benachrichtigen. Derzeit wird nur die Klickmetrik unterstützt. Wenn ein Klick auf das Element erfolgt, sollten die entsprechenden `eventTokens` erfasst und eine Benachrichtigung gesendet werden. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; Schlüssel | Der Schlüssel oder Fingerabdruck, mit dem die Ansicht identifiziert wird. |
| Antwort &gt; Vorab abrufen &gt; Ansichten &gt; ID | ID der Ansicht. |
| Antwort &gt; Benachrichtigungen &gt; ID | Benachrichtigungs-ID. |
| Antwort &gt; Benachrichtigungen &gt; Ereignisse &gt; Typ | Der Typ der Benachrichtigung, des Klicks oder der Anzeige. |
| Antwort &gt; Benachrichtigungen &gt; Ereignisse &gt; Verfolgen | Die Verfolgung des Benachrichtigungsereignisses. |
| Antwort &gt; Benachrichtigungen &gt; Ereignisse &gt; Token | Das Token, das mit dem Benachrichtigungsereignis gesendet wurde. |
| Antwort &gt; Benachrichtigungen &gt; Ereignisse &gt; Zeitstempel | Der Zeitstempel, der mit dem Benachrichtigungsereignis gesendet wurde. |
| Antwort &gt; Benachrichtigungen &gt; Ereignisse &gt; errorCode | Wenn die Benachrichtigung fehlschlägt, zeigt der Code den Grund für den Fehler an. |
| Antwort &gt; Benachrichtigungen &gt; Ereignisse | Die Ereignisse, die für die aktuelle Benachrichtigung protokolliert wurden oder nicht protokolliert werden konnten. |
| Antwort &gt; Benachrichtigungen | Gibt die protokollierten oder fehlgeschlagenen Benachrichtigungen an. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Verfolgen | Das Objekt, das alle Trace-Daten für jede einzelne Mbox-Anfrage enthält. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; responseTokens | Enthält Zuordnung von `responseTokens` einer bestimmten Mbox-Anfragesausführung. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Option &gt; Inhalt | Beachten Sie, dass der Inhalt von „Option“ nicht klar definiert ist und direkt vom Optionstyp/von der Vorlagenstruktur abhängt. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Option &gt; Typ | Optionstyp. Spiegelt den Typ des Feldes „Inhalt“ wider. Unterstützt werden: HTML, Redirect, JSON und dynamisch. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Optionen | Antwortoption. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Metriken &gt; eventToken | Token des Klickereignisses. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Metriken &gt; Typ | "click" |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Metriken | Enthält eine Liste der `clickThrough`-Metriken. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Mbox | Der Name der Mbox. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Index | Gibt an, dass mit diesem Index der Anfrage die Antwort für Mbox ist. |
| Antwort &gt; Ausführen &gt; Mboxes &gt; Mbox &gt; Analyse &gt; Nutzlast | Analysenutzlast für die Client-seitige Integration, die nach Anwendung der Mbox an Analytics gesendet werden sollten. (Siehe Abschnitt „Kampagnen mit A4T“.) |
| Antwort &gt; Ausführen &gt; Mboxes | Liste der ausgeführten Mboxes. |
| Antwort &gt; Ausführen &gt; pageLoad &gt; Optionen &gt; Inhalt | Beachten Sie, dass der Inhalt von „Option“ nicht klar definiert ist und direkt vom Optionstyp/von der Vorlagenstruktur abhängt. |
| Antwort &gt; Ausführen &gt; pageLoad &gt; Optionen &gt; Typ | Optionstyp. Spiegelt den Typ des Feldes „Inhalt“ wider. Unterstützt werden: HTML, Redirect, JSON, dynamisch und Aktionen. |
| Antwort &gt; Ausführen &gt; pageLoad &gt; Optionen | Optionen, die nicht nach Ansichten gruppiert werden (target-global-mbox + Optionen von Aktivitäten mit Ansichten, die nicht nach Ansichten gruppiert werden). |
| Antwort &gt; Ausführen &gt; pageLoad &gt; Metriken | Klicken Sie auf Metriken, die nicht einer bestimmten Ansicht zugeordnet wurden. |
| Antwort &gt; Ausführen &gt; pageLoad &gt; Verfolgen | Das Objekt, das alle Trace-Daten für die pageLoad-Anfrage enthält. |
| Antwort &gt; Ausführen &gt; pageLoad &gt; Analyse &gt; Nutzlast | Analysenutzlast für die Client-seitige Integration, die nach Anwendung der Inhalte beim Seitenladen an Analytics gesendet werden sollten. (Siehe Abschnitt „Kampagnen mit A4T“.) |

## Beispiel: applyOffers()-Aufruf

```
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

## Beispielaufruf einer Promise-Verkettung mit `getOffers()` und `applyOffers()`, da diese Funktionen auf Promise basieren.

```
adobe.target.getOffers({...})
.then(response => adobe.target.applyOffers({ response: response }))
.then(() => console.log("Success"))
.catch(error => console.log("Error", error));
```
