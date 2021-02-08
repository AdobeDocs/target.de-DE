---
keywords: Visual Experience Composer;Best Practices für Visual Experience Composer;Einschränkungen von Visual Experience Composer;Nachteile von Visual Experience Composer;Best Practices für VEC;VEC
description: Hier lernen Sie bewährte Verfahren kennen, damit Ihre Erlebnisse bei der Verwendung des Visual Experience Composer (VEC) in Adobe Target erwartungsgemäß funktionieren.
title: Was sind Best Practices und Einschränkungen von Visual Experience Composer?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Best Practices und Einschränkungen von Visual Experience Composer

Durch Befolgung dieser Best Practices können Sie dafür sorgen, dass Ihre Erlebnisse erwartungsgemäß funktionieren. Es gibt auch weitere Tipps und Einschränkungen, die Sie bei der Verwendung des Visual Experience Composer (VEC) in [!DNL Adobe Target] beachten sollten.

Befolgen Sie diese Best Practices und Sie werden bei den von Ihnen entworfenen Erlebnissen nicht so schnell auf unerwartete Probleme stoßen.

## Best Practices {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

**Bei der Verwendung von „mbox.js“ Version 57 und höher sowie von „at.js“ muss die Referenz „mbox.js“ oder „at.js“ oben im Abschnitt `<head>` Ihrer Seite platziert werden.**

Möchten Sie zudem den API-Besucherdienst verwenden, platzieren Sie das Skript der Besucher-API oberhalb von „mbox.js“ oder „at.js“.

**Für „mbox.js“-Versionen, die älter sind als Version 57, muss der „mbox.js“-Code so weit unten wie möglich im Abschnitt `<head>` Ihrer Seite positioniert werden.**

Positionieren Sie „mbox.js“ am Ende des `<head>`-Abschnitts ohne weitere Deklarationen im Anschluss. Andernfalls werden alle Skript- oder Link-Tags in den Abschnitt `<body>` verschoben.

**Der Enhanced Experience Composer kann auf Kontoebene (aktiviert für alle Aktivitäten, die mit diesem Konto erstellt werden) oder individuell für einzelne Aktivitäten aktiviert werden.**

Um den Enhanced Experience Composer auf Kontoebene zu aktivieren, klicken Sie auf [!UICONTROL Administration > Visual Experience Composer] und stellen Sie dann den Schalter auf die Position &quot;Ein&quot;.

Möchten Sie den Enhanced Experience Composer für einzelne Aktivitäten aktivieren, wenn Sie eine Aktivität im Visual Experience Composer erstellen, klicken Sie auf [!UICONTROL Konfigurieren > URL] und stellen Sie den Regler auf die Position „Ein“.

**Sie können bestimmte IP-Adressen in Zulassungslisten einfügen, wenn der Enhanced Visual Experience Composer nicht auf sicheren Seiten Ihrer Site geladen wird.**

Probleme beim Laden des Enhanced Visual Experience Composer können durch Zulassungsauflistung der folgenden IP-Adressen behoben werden. Diese IP-Adressen stehen für den Server von Adobe zur Verfügung, der für den Proxy des Enhanced Experience Composer verwendet wird. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Besucher Ihrer Site benötigen diese IP-Adressen nicht auf die Zulassungsliste gesetzt.

Vereinigte Staaten: 52.55.99.45, 54.80.158.92 und 54.204.197.253

Europa, Naher Osten und Afrika (EMEA): 52.51.238.221, 52.210.199.44 und 54.72.56.50

Asien-Pazifik (APAC): 52.193.67.35, 54.199.198.109 und 54.199.241.57

**Verwenden Sie eindeutige IDs für Top-Level- und sonstige Elemente, die sich gut als Test-/Targeting-Kandidaten eignen könnten.**

Alles, was sich unmittelbar innerhalb des Body-Elements befindet, muss über eine eindeutige ID verfügen. Wenn neue Elemente in den Body aufgenommen werden und Code verschoben wird, verfügen wenigstens die übergeordneten Elemente über eine einfachere Erkennungsmethode.

Adobe Target erfordert zwar keine IDs, die Zuverlässigkeit der mit dem Experience Composer erstellten Erlebnisse wird dadurch allerdings erhöht. Target verwendet CSS-Selectors, um Ihren Inhalt zu ändern, wenn das Erlebnis bereitgestellt wird. Beim Bearbeiten eines Erlebnisses verankert der Visual Experience Composer den Selector des nächsten Vorgängers mit einem Nicht-Null-ID-Attribut mit dem zu ändernden HTML-Element. Es wird daher nicht empfohlen, einen Mechanismus zu verwenden, der HTML-ID-Attribute festlegt oder ändert, einschließlich JavaScript-Bibliotheken. Auch wenn diese IDs dem Target-Experience Composer möglicherweise für die Aktivitätserstellung zur Verfügung stehen, wenn JavaScript IDs ändert, ist die ID, die bei der Erstellung des Erlebnisses verwendet wurde, bei der Ausführung des Erlebnisses möglicherweise nicht verfügbar. Ist eine ID nicht verfügbar, tritt bei dem mit der ID verankerten Selector ein Fehler auf.

**Benennen Sie CSS-Klassen mit einfach zu identifizierenden Bezeichnungen.**

Beim Bearbeiten von CSS-Klassen im Visual Experience Composer ist es hilfreich, die Klassen anhand von beschreibenden Namen leicht identifizierbar zu machen. Dadurch wird sichergestellt, dass Sie die richtigen CSS-Klassen bearbeiten und Ihre Seiten wie erwartet angezeigt werden.

Verwenden Sie nicht die CSS-Eigenschaft `!important`, wenn Sie Elemente ausblenden oder entfernen.

Wenn die CSS-Eigenschaft „1!important1“ vorhanden ist, werden Änderungen durch „target.js“ während der Bereitstellung durch die CSS-Regeln der Site überschrieben.

**Vermeiden von HTML-Tabellen für Seitenlayouts.**

Target Standard und Premium verwenden JavaScript zur Formatierung von Seiten. Die Modifizierung von tabellenbasierten Layouts mit JavaScript ist kompliziert. Zudem werden tabellenbasierte Layouts möglicherweise nicht in allen Browsern gleich angezeigt. Die besten Ergebnisse erhalten Sie, wenn Sie Seitenlayouts mit CSS erstellen.

**Vermeiden von iFrames.**

Es empfiehlt sich, den Einsatz von iFrames zu minimieren, um die Seiten- und Testverwaltung zu vereinfachen. Der Visual Experience Composer kann einige Aktionen innerhalb eines iFrames anwenden, jedoch funktionieren einige Aktionen, wie zum Beispiel Größenanpassung, nicht richtig. Das Verwalten und Anpassen von Seiten, die mehrere iFrames verwenden, ist kompliziert. Daher kann auch das Testen von Seiten mit vielen iFrames zu Problemen führen.

**Versuchen Sie, alle dynamischen DOM-Änderungen so bald wie möglich nach DOM-Bereitschaft anzuordnen.**

Wenn Ihre Änderungen vor der Experience-Anwendung durch target.js nicht angewendet werden, ist die Bereitstellung von Inhalten möglicherweise fehlerhaft. Dies geschieht nur, wenn es zu einer DOM-Änderung in der Hierarchie eines zielgerichteten Elements kommt.

**Verwenden Sie ausschließlich Text oder ein Bild-Tag in Ihren Ankerelementen.**

`<a>Anchor Text</a>`

ODER-

`<a href=""> <img src=""> </img> </a>`

**Vermeiden Sie Elemente auf Blockebene innerhalb eines Inline-Elements.**

Elemente auf Blockebene sollten nicht innerhalb von Inline-Elementen wie Anchor, Span usw. verwendet werden. Dies würde dazu führen, dass Inline-Elemente ihre Höhe und Breite verlieren würden, sodass das Overlay-Tool in Visual Experience Composer möglicherweise nicht wie erwartet funktioniert.

**Vermeiden Sie die Verwendung des base-Tags in Ihrer Website zur Auflösung von URLs und Links.**

Der Visual Experience Composer beeinflusst die Website im Hintergrund mithilfe eines Proxy-Servers, der die Links aktualisiert hat. Wenn Sie ein base-Tag hinzufügen, werden die durch den Proxy-Server verwendeten URLs erneut durch den Browser aufgelöst und fehlerhaft dargestellt.

**Die Verwendung von „HTML Bearbeiten“ zur Manipulation der DOM-Struktur kann Selektoren unterbrechen.**

Wenn Sie beispielsweise zwei Aktionen durchgeführt haben:

* Hinzufügen einer Klasse zu Element 1
* Bearbeiten des HTML für Element 1

Jede Änderung erstellt ein neues Element im Visual Experience Composer. Da die zweite Aktion Element 1 bearbeitet, kann in der zweiten Aktion nichts mehr geändert werden, wenn Sie Element 1 löschen. Daher funktioniert die Änderung nicht mehr.

Mit anderen Worten: Wenn Sie ein Element mit Text hinzufügen und dieses Element in einer anderen Aktion mit einem anderen Text bearbeiten, dann zeigt der Code-Editor beide Aktionen als separate Elemente. Bei der Bearbeitung des Elements haben Sie ein neues Element erstellt, das das ursprünglich von Ihnen erstellte Element ändert und den bearbeiteten Text enthält. Wenn Sie dann das ursprüngliche Element löschen, kann der bearbeitete Text das Element nicht finden, das bearbeitet wurde, und wird folglich nicht angezeigt. Das zweite Element bleibt in der Liste der Elemente erhalten, doch es hat keine Auswirkung auf die Seite, weil das Element, das es ändert, nicht mehr vorhanden ist.

Siehe [Elementselektoren, die im Visual Experience Composer verwendet werden](/help/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337).

**Verwenden Sie die Tags `<b>` und `<i>`, wenn Sie Textelemente mit dem Rich-Text-Editor erstellen.**

* Für fett gedruckten Text verwenden Sie `<b>` anstelle von `<strong>`.
* Für kursiv gedruckten Text verwenden Sie `<i>` anstelle von `<em>`.

Die Tags `<strong>` und `<em>` können zu unerwarteten Ergebnissen führen.

**Seien Sie beim Entfernen von Formularfeldern vorsichtig.**

Bestimmte Formularfelder können Pflichtfelder für die Übermittlung sein. Das Entfernen dieser Formularfelder kann Auswirkungen auf Übermittlungen haben.

**Binden Sie `mboxCreate` nicht in Skripts ein.**

Da `mboxCreate` `document.write` verwendet, ist es nicht empfehlenswert, `mboxCreate` in Skripts einzubinden. Verwenden Sie stattdessen `mboxDefine` und `mboxUpdate`, die den gleichen Zweck erfüllen.

**Aktualisieren Sie ein HTML-Snippet nicht mit Target Standard, wenn es mit JavaScript-Code initialisiert werden muss.**

Wird eine Aktion (HTML bearbeiten) an Seitenkomponenten (wie Schiebereglern, Karussells usw.) durchgeführt, wird das Element nicht ordnungsgemäß dargestellt. Der Visual Experience Composer führt die Aktion aus, nachdem die Seitenkomponente von JavaScript initialisiert wurde.

Wird der Seiteninhalt jedoch für Besucher bereitgestellt, wird die Aktion vor Initialisierung der Komponente durchgeführt. Somit kann die Funktion der Komponente zum Zeitpunkt der Bereitstellung beschädigt oder in Ordnung sein. Die Funktion der Komponente hängt mit dem auf der Seite verwendeten Skript zusammen, das die Komponente definiert.

Sollten Sie die Bereitstellung prüfen und feststellen, dass sie beim ersten Versuch einwandfrei funktioniert, ist dies keine Garantie dafür, dass sie das auch weiterhin tut. Es besteht möglicherweise eine Gleichzeitigkeitsbedingung.

* Ist eine solche Gleichzeitigkeitsbedingung vorhanden, funktioniert die Bereitstellung nicht immer.
* Ist keine Gleichzeitigkeitsbedingung vorhanden, funktioniert die Bereitstellung immer.

Prüfen Sie Ihre Seite mehrmals, um sicherzustellen, dass die Bereitstellung wie erwartet funktioniert.

**Vermeiden Sie die Verwendung eines base-Tags in Ihrer Website zur Auflösung von URLs und Links.**

Bei der Verwendung von Enhanced Experience Composer wird die Webseite im Hintergrund über einen Proxyserver manipuliert, der alle Link-URLs so aktualisiert, dass sie auf dem Proxy funktionieren. Wird ein base-Tag hinzugefügt, werden all diese URLs vom Browser aufgelöst, sodass sie beschädigt zu sein scheinen.

**Wichtiger Text auf der Seite, der für das Targeting verwendet wird, sollte innerhalb eines Elements in HTML-Code geschrieben werden.**

Beispielsweise können Sie im VEC nicht auf Einkaufswagen-Text zielen, wenn Ihr Code wie folgt aussieht:

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart"> 
   <img alt="Shopping Cart"src="/images/ico-cart.gif"></img> 
   Shopping Cart: 
   <span id="HeaderCartQtyTotal">
      0 
  </span> 
  Items 
  <span id="HeaderCartPriceTotal"></span> 
</a>
```

In diesem Beispiel wurde das gesamte Ankerelement im VEC ausgewählt, was sich negativ auf andere Elemente auswirkt, wenn ein Targeting ausgeführt wird.

**Benutzen Sie die Variablen `top` und `self` nicht in JavaScript-Code.**

Wenn der Enhanced Experience Composer aktiviert ist, wird der Wert der Variablen „top“ und „self“ aktualisiert, um das iFrame-Busting zu deaktivieren. Arbeiten Sie stattdessen mit einer X-Frame-Optionsüberschrift, um iframe-Busting anstatt benutzerdefinierter JavaScript-Codes einzusetzen.

**Testen Sie stets Ihre Webseite, wenn für den Zeitpunkt des Ladens der Seite neue Parameter hinzugefügt werden sollen.**

Für das Öffnen von www.abc.com werden beispielsweise die folgenden URL-Parameter verwendet:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Diese Parameter ermöglichen die Bearbeitung in einem iframe.

Stellen Sie sicher, dass die Webseite wie erwartet lädt, nachdem solche Parameter hinzugefügt wurden.

**Stellen Sie sicher, dass sich die Seite in einem iframe wie gewünscht öffnen lässt.**

Deaktivieren Sie iframe-Busting auf Ihrer Webseite und prüfen Sie, ob sie sich auf einer Platzhalterseite in einem iframe wie gewünscht öffnen lässt. Beispiel:

```html
<!DOCTYPE 
<html> 
<html> 
<head> 
  <meta charset="utf-8"> 
  <meta name="viewport" content="width=device-width"> 
  <title>JS Bin</title> 
</head> 
<body> 
  <iframe src="https://www.homedepot.com"</iframe> 
</body> 
</html>
```

## Einschränkungen {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Beachten Sie folgende Einschränkungen bei der Verwendung von Visual Experience Composer zum Entwerfen Ihrer Aktivität.

**Die Funktion „Verschieben“ unterstützt z-index nicht.**

Da keine z-index-Funktionalität vorhanden ist, kann das verschobene Element nicht über ein anderes Element verschoben werden. Weitere Details finden Sie unter [Einschränkungen](/help/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

**Eine Neuanordnung von Elementen wirkt sich auf das Klick-Tracking aus.**

Wenn ein für Klick-Tracking gekennzeichnetes Element neu angeordnet wird, ändern sich die Pfade der neu angeordneten Elemente. Infolgedessen ist das Element an dem Ort, an dem sich das Originalelement vor der Neuanordnung befunden hat, das Element, dessen Klicks verfolgt werden.

Dies passiert, weil sowohl der Code zur Bereitstellung des Aktivitäteninhalts als auch der Code für das Klick-Tracking in einem einzigen Code enthalten ist, der für die Seite bereitgestellt wird. Wenn Sie zu einer anderen Seite navigieren und Klick-Tracking einrichten, dann werden der Aktivitätsinhalts-Code und der Klick-Trackingcode für diese Seite bereitgestellt. Wenn die Klick-Tracking-Seite eine ähnliche Struktur aufweist wie die Seite, auf der der Test ausgeführt wird, dann kann der Testinhalt auch auf der Klick-Tracking-Seite erscheinen.

**Möglicherweise lässt sich in ein `<div>`, das eine Mbox ist, kein Element einfügen.**

Enthält eine Mbox ein Angebot, kann ein einzufügendes Element als „insertBefore“ anstatt von „insertAfter“ angewendet werden, falls die Mbox nicht korrekt implementiert wurde.

**Beim Bearbeiten von über- und untergeordneten Elementen sollten Sie zunächst das übergeordnete Element bearbeiten.**

Wenn Sie eine Bildaktion für ein Element austauschen und anschließend den Text oder das HTML für das übergeordnete Element bearbeiten, können Bereitstellungsprobleme auftreten. Der beste Arbeitsablauf besteht darin, das übergeordnete Element zu bearbeiten, bevor Sie das Bild im untergeordneten Element austauschen.

**Es kann kein Seitenelement ausgewählt werden, das eine Mbox als untergeordnetes Element enthält.**

Wenn Ihre Seite zum Beispiel Folgendes enthält:

```html
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

Der äußere Div darf in keinem Erlebnis ausgewählt werden, weil die fest in die Seite codierte Mbox nach wie vor einen Aufruf an Target ausführt und eine Antwort erhält. Diese Antwort beeinträchtigt die für das größere Seitenelement vorgesehene Antwort.

**Proxy-IPs können in der Kundenumgebung blockiert werden.**

Wenn Sie den Enhanced Experience Composer auf einer nicht veröffentlichten Seite wie einer Staging-Umgebung verwenden, dann sehen Sie möglicherweise Fehlermeldungen zu Zeitüberschreitungen und Zugriffsverweigerung, wenn Ihre Site RIPs blockiert.

**Werden mehrere Seiten hinzugefügt, sind sowohl die Erlebnisleiste als auch die Seitenleiste gleichzeitig geöffnet. Dies verringert die Breite, in der Visual Experience Composer die Seite für Optimierungen anzeigen kann. Somit werden fließende Seiten aufgrund des eingeschränkten Raums möglicherweise nicht wie erwartet wiedergegeben.**

Dies kann umgangen werden, indem Erlebnisleiste und Seitenleiste durch Klicken auf die nach links zeigenden Pfeile oben minimiert werden.

## Einschränkungen {#section_F33C2EA27F2E417AA036BC199DD6C721}

**Funktion „Verschieben“**

Ein Element kann nicht außerhalb eines Behälters verschoben werden, auf den eine CSS-Eigenschaft folgt.

**Auf Mboxes stehen lediglich Tauschangebote zur Verfügung.**

Aktionen wie „Klasse bearbeiten“ und „Neu anordnen“ sind innerhalb einer Mbox nicht zulässig. mbox-Inhalt wird durch mbox.js. gesendet.

**Sie sollten dasselbe Element nicht neu ordnen und verschieben.**

Wenn ein Element an einen anderen Ort verschoben wurde und Sie den übergeordneten Behälter auswählen und versuchen, die untergeordneten Elemente neu zu ordnen, ist das verschobene Element nicht betroffen und bleibt, wo es ist. Die Neuordnung wird möglicherweise nicht wie gewünscht dargestellt.

**Die Bildtauschaktion funktioniert bei einem Bild des Karussells nicht.**

Wenn Ihre Seite beispielsweise über ein Karussell mit mehreren Bildern verfügt und Sie das Bild gegen das zweite Bild im Karussell austauschen möchten, funktioniert die Bildtauschaktion nicht.

Dies kann umgangen werden, wenn der übergeordnete Container ausgewählt und mit „HTML bearbeiten“ der HTML-Code des Karussells so bearbeitet wird, dass die Bildquelle des gewünschten Bilds aktualisiert wird.

**Größe von Bildern kann nicht in einer Mbox geändert werden.**

Wenn Sie ein Bild in einem Mbox-Element tauschen und dann versuchen, die Größe des Bilds entsprechend der Mbox-Elementgröße anzupassen, ist die Größenanpassung nicht gestattet.

**Nach dem Bildtausch können Sie die Aktion „Bearbeiten“ nicht wählen.**

Nach dem Bildtausch können Sie die Scene7-URL nicht bearbeiten.

**HTML-Elemente mit externen Quellen können nicht bearbeitet werden.**

Beispiel: Video, Audio-Tags, Einbetten, iFrames, Frames.

**Klick-Tracking für Ankerelemente, die etwas anderes als Text oder Bild-Tags enthalten, funktioniert nicht.**

Zum Beispiel funktioniert Klick-Tracking nicht, wenn das Element JavaScript enthält.

**Seiten müssen URL-Parameter akzeptieren, damit Visual Experience Composer funktioniert.**

Einige Websites entfernen sämtliche URL-Parameter ihrer Seiten. Visual Experience Composer benötigt diese Parameter jedoch.

**Verwenden Sie Skript als Teil von HTML, sollten alle Variablen und Funktionen, auf die von außen zugegriffen wird, im Namespace des Fensters angegeben werden.**

Das Skript wird nach dem Laden der Seite innerhalb des Geltungsbereichs von „target.js“ ausgeführt. Somit kann auf lokal angegebene Variablen oder Funktionen von außen nicht zugegriffen werden.

*Falsch:*

```html
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
```

*Richtig:*

```html
<script> 
  window.myVar = 123; 
  window.myFunc = function() { 
    // 
  }; 
</script>
```

**Wird ein Bild aus der Inhaltsbibliothek (Scene7) eingefügt und der HTML-Code bearbeitet, beschädigt dies die Bild-URL.**

Fügen Sie ein Ankerelement innerhalb des div „customHeaderMessage“ sowie Platzhaltertext ein:

```html
<a href="#"> 
<span> Dummy text </span>
</a>
```

Wählen Sie das div mithilfe von „Element einfügen“, um ein Bild als Geschwisterelement des div mit dem Platzhaltertext einzufügen.

Nach Einfügen des Bilds sollte es wie folgt aussehen:

```html
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Löschen Sie den Platzhaltertext.

**Die Aktion „customCode“ im Visual Experience Composer funktioniert in Internet Explorer 8 nicht.**

Aufgrund einiger Einschränkungen von IE8 bei der Handhabung von Skriptinhalten unterstützt „target.js“ diese Aktion in IE8 nicht. Enthält die Seite jQuery und wird sie im Fensterobjekt global verfügbar gemacht, kann „target.js“ die Aktion „customCode“ für die Bereitstellung nutzen. Stellen Sie sicher, dass window.jQuery und window.jQuery.fn.prepend definiert wurden.

**Klick-Tracking wird nur auf der Seite unterstützt, auf der Erlebnisse erstellt werden, oder auf einer Weiterleitungsseite.**

Zwar ist der Browse-Modus in Click Track VEC verfügbar, kann aber nicht für die Klick-Tracking auf einer Seite verwendet werden.
