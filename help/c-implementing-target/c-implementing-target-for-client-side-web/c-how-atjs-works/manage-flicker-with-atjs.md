---
description: Informationen dazu, wie mit der JavaScript-Bibliothek at.js beim Laden von Seiten oder Anwendungen von Target ein Flackern vermieden wird.
keywords: Flackern;at.js;Implementierung
seo-description: Informationen dazu, wie mit der Adobe Target JavaScript-Bibliothek at.js beim Laden von Seiten oder Anwendungen von Target ein Flackern vermieden wird.
seo-title: Verwaltung von Flackern mit Adobe Target at.js
solution: Target
title: Verwaltung von Flackern mit „at.js“
topic: Standard
uuid: 65f67c4a-a931-4e0d-80d9-29ab67b62573
translation-type: tm+mt
source-git-commit: c94b1a1e735810ef4119781c3e051b632d140614

---


# Verwaltung von Flackern mit „at.js“{#how-at-js-manages-flicker}

Informationen dazu, wie mit der JavaScript-Bibliothek at.js beim Laden von Seiten oder Anwendungen von Target ein Flackern vermieden wird.

Ein Flackern tritt dann auf, wenn Besuchern vorübergehend Standardinhalt angezeigt wird, bevor dieser durch den Inhalt der entsprechenden Aktivität ersetzt werden konnte. Das Auftreten eines solchen Flackerns ist nicht wünschenswert, da es die Besucher möglicherweise verwirrt.

## Verwenden einer automatisch erstellten globalen Mbox {#section_C502170D551C4F52AAFD8E82C41BB63A}

Wenn Sie die Einstellung [Globale Mbox automatisch erstellen](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/understanding-global-mbox.md#concept_76AC0EC995A048238F3220F53773DB13) bei der Konfigurierung von at.js aktivieren, reduziert at.js Flackern durch Ändern der Deckkrafteinstellung beim Laden der Seite. Wenn at.js geladen wird, wird die Deckkraft des <body> Elements auf „0“ gesetzt, wodurch die Seite für Besucher anfänglich unsichtbar gemacht wird. Nachdem die Antwort von Target eingeht oder ein Fehler in der Target-Anfrage erkannt wird, setzt at.js die Deckkraft wieder auf 1. So wird gewährleistet, dass der Besucher die Seite erst sieht, nachdem der Inhalt Ihrer Aktivitäten angewendet wurde.

Wenn Sie die Einstellung bei der Konfiguration von at.js aktivieren, wird die Deckkraft des HTML-BODY von at.js auf 0 gesetzt. Nach Eingang einer Antwort von Target wird die Transparenz des HTML-BODY von at.js auf 1 zurückgesetzt.

Mit einer Deckkraft von 0 ist der Seiteninhalt nicht sichtbar, sodass Flackern verhindert wird. Der Browser kann die Seite jedoch bereits rendern und lädt alle nötigen Assets wie CSS, Bilder usw.

Wenn die Deckkraft von 0 in Ihrer Implementierung nicht funktioniert, können Sie Flackern auch verhindern, indem Sie `bodyHiddenStyle` anpassen und `body {visibility:hidden !important}` festlegen. Sie können entweder den Body-Wert `{opacity:0 !important`} oder `body {visibility:hidden !important}` verwenden, je nachdem, was in Ihrer Situation besser funktioniert.

Die folgende Abbildung zeigt die Aufrufe „Hide Body“ und „Show Body“ sowohl in at.js 1.*x* als auch in at.js 2.x.

**at.js 2.x**

![Target-Ablauf: at.js-Seitenlade-Anfrage](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-flow-page-load-request.png)

**at.js 1.*x***

![](assets/target-flow2.png)

Weitere Informationen zum Überschreiben mit `bodyHiddenStyle` finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Vermeiden von Flackern beim asynchronen Laden von at.js

Das asynchrone Laden von at.js eignet sich hervorragend, um zu verhindern, dass das Rendern des Browsers blockiert wird. Bei dieser Technik kann es jedoch zu Flackereffekten auf der Webseite kommen.

Sie können das Flackern verhindern, indem Sie einen vorab ausgeblendeten Ausschnitt verwenden, der sichtbar ist, nachdem die relevanten HTML-Elemente von [!DNL Target] personalisiert wurden. Es wird empfohlen, einen Tag-Manager wie Adobe DTM oder das neue Adobe Launch zu verwenden, um den vorab ausgeblendeten Ausschnitt hinzuzufügen. Der Ausschnitt muss vor dem Laden von at.js hinzugefügt werden.

Der Code für den vorab ausgeblendeten Ausschnitt lautet wie folgt:

```
;(function(win, doc, style, timeout) {
  var STYLE_ID = 'at-body-style';

  function getParent() {
    return doc.getElementsByTagName('head')[0];
  }

  function addStyle(parent, id, def) {
    if (!parent) {
      return;
    }

    var style = doc.createElement('style');
    style.id = id;
    style.innerHTML = def;
    parent.appendChild(style);
  }

  function removeStyle(parent, id) {
    if (!parent) {
      return;
    }

    var style = doc.getElementById(id);

    if (!style) {
      return;
    }

    parent.removeChild(style);
  }

  addStyle(getParent(), STYLE_ID, style);
  setTimeout(function() {
    removeStyle(getParent(), STYLE_ID);
  }, timeout);
}(window, document, "body {opacity: 0 !important}", 3000));
```

Standardmäßig wird durch den Ausschnitt der gesamte HTML-BODY vorab ausgeblendet. Ein einigen Fällen sollten nur bestimmte HTML-Elemente vorab ausgeblendet werden und nicht die gesamte Seite. Dazu können Sie den Stilparameter anpassen. Er kann durch einen Parameter ersetzt werden, der nur bestimmte Teile der Seite vorab ausblendet.

Beispiel: Sie haben zwei Bereiche, die durch die IDs container-1 und container-2 identifiziert werden. In diesem Fall kann der Stil wie folgt ersetzt werden:

```
#container-1, #container-2 {opacity: 0 !important}
```

Anstelle der Standardeinstellung:

```
body {opacity: 0 !important}
```

## Flackern in at.js 2.x für triggerView() verwalten

Wenn Sie `triggerView()` benutzen, um zielgerichtete Inhalte in Ihrer SPA anzuzeigen, wird das Flackern vorkonfiguriert gehandhabt. Das bedeutet, dass die Pre-hiding-Logik nicht manuell hinzugefügt werden muss. Stattdessen blendet at.js 2.x im Voraus den Ort aus, an dem Ihre Ansicht angezeigt werden muss, bevor der zielgerichtete Inhalt angewendet wird.

## Flackern mit getOffer() und applyOffer() verwalten

Da es sich sowohl bei `getOffer()` als auch bei `applyOffer()` um einfache APIs handelt, sind keine Mechanismen zur Flackerverhinderung integriert. Sie können einen Selektor oder ein HTML-Element als Option an `applyOffer()` übermitteln. In diesem Fall fügt `applyOffer()` den Aktivitätsinhalt diesem Element zu, wobei Sie jedoch gewährleisten müssen, dass das Element vor dem Aufruf von `getOffer()` und `applyOffer()` vollständig ausgeblendet wurde.

```
document.documentElement.style.opacity = "0";
 
adobe.target.getOffer({
    mbox: 'target-global-mbox',
    success: function(offer) {
        adobe.target.applyOffer({
            mbox: 'target-global-mbox',
            offer: offer
        });
 
        document.documentElement.style.opacity = "1";
    },
    error: function() {
        document.documentElement.style.opacity = "1";        
    }
});
```

## Verwenden einer regionalen Mbox mit mboxCreate() in at.js 1.x (in at.js 2.x nicht unterstützt)

Wenn Sie eine regionale Mbox-Implementierung verwenden, können Sie mit `mboxCreate()` mit Ihrer Seite ähnlich dem folgenden Beispielcode arbeiten:

```
<div class="mboxDefault">
Some default content
</div>
<script>
mboxCreate('some-mbox');
</script>
```

Wurden die Seiten ordnungsgemäß bereitgestellt, verhindert at.js ein Flackern, indem die Eigenschaft CSS-„Sichtbarkeit“ des Elements mit mboxDefault-Klasse automatisch umgestellt wird.