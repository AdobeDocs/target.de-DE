---
keywords: adobe.target.trackEvent;trackEvent;trackevent;track event;at.js;functions;function;preventDefault;preventdefault;prevent default
description: Informationen zur Funktion adobe.target.trackEvent(options) für die JavaScript-Bibliothek von Adobe Target at.js.
title: adobe.target.trackEvent(options)
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 78%

---


# adobe.target.trackEvent(options)

Diese Funktion löst eine Anforderung zum Melden von Benutzeraktionen aus (wie beispielsweise Klicks und Konversionen). Sie übermittelt keine Aktivitäten in der Antwort.

Diese Mbox-Aufrufe für die Ereignisverfolgung können dann verwendet werden, um in den Aktivitäten Metriken zu definieren. Weitere Informationen finden Sie unter [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) und [Konversions-Tracking](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).

Hier finden Sie die Einzelheiten zur API:

| Schlüssel | Typ | Erforderlich | Beschreibung |
|--- |--- |--- |--- |
| mbox | Zeichenfolge | Ja | Mbox-<br>**NameHinweis**: Wenn ein trackEvent()-Aufruf mit einem Mbox-Namen ausgelöst wird, der bereits auf der Seite ausgelöst wurde, wird die SDID von trackEvent() zurückgesetzt und unterscheidet sich von den Seitenaufrufen für die Zielgruppe. Durch das Auslösen eines trackEvent()-Aufrufs mit einem anderen Mbox-Namen wird die SDID des trackEvent()-Aufrufs jedoch konsistent mit dem Seitenlade-Request/triggerView()-Aufruf auf der Seite gehalten. |
| selector | Zeichenfolge | Nein | CSS-Selektoren für die Ermittlung der HTML-Elemente Die Ereignislistener werden an die gefundenen Elemente angefügt.. |
| Typ | Zeichenfolge | Nein | Stellt einen registrierten Ereignistyp dar. Dabei kann es sich um HTML-bekannte Ereignisse wie „click“, „mousedown“ und so weiter sowie benutzerdefinierte HTML-Ereignisse handeln. |
| preventDefault | Boolesch | Nein | Gibt an, ob `event.preventDefault()` im Rückruf des Ereignislisteners verwendet werden soll. Standard ist „false“.<br>**Hinweis:** Nur `form[submit] and `a[click] werden unterstützt. Andere Szenarien werden aufgrund der Komplexität und der sehr großen Anzahl an zu unterstützenden Szenarien nicht unterstützt. |
| params | Objekt | Nein | Mbox-Parameter Ein Objekt aus Schlüssel-Wert-Paaren mit der folgenden Struktur:<br>`{ "param1": "value1", "param2": "value2"}` |
| Zeitüberschreitung | Nummer | Nein | Zeitüberschreitung in Millisekunden<br>Wenn nichts angegeben, wird der Standardwert verwendet:<br>`...timeoutInSeconds: 0.15...}` |
| success | Funktion | Nein | Eine Rückruffunktion, mit der signalisiert wird, dass das Ereignis gemeldet wurde |
| error | Funktion | Nein | Eine Rückruffunktion, mit der signalisiert wird, dass das Ereignis nicht gemeldet werden konnte |

## Beispiel

```
<a href="https://asite.com">click me!</a> 
```

plus JavaScript-Code zur Zuweisung von `trackEvent`:

```
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

Oder:

```
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