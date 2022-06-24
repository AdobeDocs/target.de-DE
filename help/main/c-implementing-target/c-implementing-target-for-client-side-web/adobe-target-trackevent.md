---
keywords: adobe.target.trackevent; Trackevent; trackevent; Ereignis tracken; at.js; Funktionen; funktion; Preventdefault; preventdefault; Standard verhindern
description: Verwenden Sie die Funktion adobe.target.trackEvent() für die Adobe [!DNL Target] at.js-JavaScript-Bibliothek , um eine Anforderung zum Reporting von Benutzeraktionen auszulösen, z. B. Klicks und Konversionen auf Ihrer Site.
title: Wie verwende ich die Funktion adobe.target.trackEvent()?
feature: at.js
role: Developer
exl-id: 36005236-ce18-4845-b4fb-e52056018bc7
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 64%

---

# adobe.target.trackEvent(options)

Diese Funktion löst eine Anforderung zum Melden von Benutzeraktionen aus (wie beispielsweise Klicks und Konversionen). Sie übermittelt keine Aktivitäten in der Antwort.

Diese Mbox-Aufrufe für die Ereignisverfolgung können dann verwendet werden, um in den Aktivitäten Metriken zu definieren. Weitere Informationen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) und [Konversions-Tracking](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/){target=_blank}.

Hier finden Sie die Einzelheiten zur API:

| Schlüssel | Typ | Erforderlich | Beschreibung |
|--- |--- |--- |--- |
| mbox | Zeichenfolge | Ja | Mbox-Name <br>**Hinweis**: Wenn ein trackEvent() -Aufruf mit einem Mbox-Namen ausgelöst wird, der bereits auf der Seite ausgelöst wurde, wird die SDID von trackEvent() zurückgesetzt und unterscheidet sich von den Target -Aufrufen auf der Seite. Durch das Auslösen eines trackEvent() -Aufrufs mit einem anderen Mbox-Namen wird die SDID des trackEvent() -Aufrufs jedoch mit den Seitenlade-Anfrage-/triggerView() -Aufrufen auf der Seite konsistent. |
| selector | Zeichenfolge | Nein | CSS-Selektoren für die Ermittlung der HTML-Elemente Die Ereignislistener werden an die gefundenen Elemente angefügt.. |
| Typ | Zeichenfolge | Nein | Stellt einen registrierten Ereignistyp dar. Dabei kann es sich um HTML-bekannte Ereignisse wie „click“, „mousedown“ und so weiter sowie benutzerdefinierte HTML-Ereignisse handeln. |
| preventDefault | Boolesch | Nein | Gibt an, ob `event.preventDefault()` im Rückruf des Ereignislisteners verwendet werden soll. Standard ist „false“.<br>**Hinweis**: Nur `form[submit]` und `a[click]` werden unterstützt. Andere Szenarien werden aufgrund der Komplexität und der sehr großen Anzahl an zu unterstützenden Szenarien nicht unterstützt. |
| params | Objekt | Nein | Mbox-Parameter Ein Objekt aus Schlüssel-Wert-Paaren mit der folgenden Struktur:<br>`{ "param1": "value1", "param2": "value2"}` |
| Zeitüberschreitung | Nummer | Nein | Zeitüberschreitung in Millisekunden<br>Wenn nichts angegeben, wird der Standardwert verwendet:<br>`...timeoutInSeconds: 0.15...}` |
| success | Funktion | Nein | Eine Rückruffunktion, mit der signalisiert wird, dass das Ereignis gemeldet wurde |
| error | Funktion | Nein | Eine Rückruffunktion, mit der signalisiert wird, dass das Ereignis nicht gemeldet werden konnte |

## Beispiel

```javascript
<a href="https://asite.com">click me!</a> 
```

plus JavaScript-Code zur Zuweisung von `trackEvent`:

```javascript
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

Oder:

```javascript
adobe.target.trackEvent({ 
    "mbox": "clicked-cta", 
    "params": { 
        "param1": "value1" 
    } 
});
```

>[!NOTE]
>
>In dem Fall, dass die Pflichtfelder nicht festgelegt wurden, wird keine Anforderung ausgeführt und ein Fehler wird gemeldet.
