---
keywords: Visual Experience Composer;Best Practices für Visual Experience Composer;Einschränkungen von Visual Experience Composer;Nachteile von Visual Experience Composer;Best Practices für VEC;VEC
description: Erfahren Sie mehr über Best Practices, damit Ihre Erlebnisse bei der Verwendung des [!UICONTROL Visual Experience Composer] (VEC) wie erwartet funktionieren.
title: Was sind [!UICONTROL Visual Experience Composer] Best Practices und Einschränkungen?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
source-git-commit: 8c62a0e976ce075d07e1f80018c7ad7fac240eea
workflow-type: tm+mt
source-wordcount: '2435'
ht-degree: 50%

---

# [!UICONTROL Visual Experience Composer] Best Practices und Einschränkungen

Um sicherzustellen, dass Ihre Erlebnisse wie vorgesehen funktionieren, befolgen Sie die Best Practices bei der Verwendung des [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC). Beachten Sie die wichtigsten Tipps und Einschränkungen, um die Leistung zu maximieren und gängige Probleme zu vermeiden.

## Best Practices   {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

Im Folgenden finden Sie Best Practices für die Verwendung von VEC:

### Platzieren Sie die at.js-Referenz oben im `<head>` Abschnitt Ihrer Seite.

+++Details anzeigen
Wenn Sie auch die [!UICONTROL Visitor API Service] verwenden, platzieren Sie das Besucher-API-Skript über at.js.

+++

### Sie können die [!UICONTROL Enhanced Experience Composer] auf Kontoebene (aktiviert für alle im Konto erstellten Aktivitäten) oder auf individueller Aktivitätsebene aktivieren.

+++Details anzeigen
Um die [!UICONTROL Enhanced Experience Composer] auf Kontoebene zu aktivieren, klicken Sie auf [!UICONTROL [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]] und schalten Sie den [!UICONTROL Enable Enhanced Experience Composer] auf Ein um.

Um die [!UICONTROL Enhanced Experience Composer] auf Aktivitätsebene zu aktivieren, während Sie eine Aktivität im [!UICONTROL Visual Experience Composer] erstellen, klicken Sie auf [!UICONTROL Configure > [!UICONTROL Page Delivery]] und schalten Sie den [!UICONTROL Enable Enhanced Experience Composer] auf Ein um.

+++

### Auf die Zulassungsliste setzen Sie können bestimmte IP-Adressen ändern, wenn der [!UICONTROL Enhanced Experience Composer] nicht auf sicheren Seiten Ihrer Site geladen wird.

+++Details anzeigen
Probleme beim Laden des [!UICONTROL Enhanced Experience Composer] können durch die Zulassungsauflistung der folgenden IP-Adressen behoben werden. Diese IP-Adressen sind für [!DNL Adobe] Server bestimmt, die für den [!UICONTROL Enhanced Experience Composer]-Proxy verwendet werden. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Auf die Zulassungsliste setzen Besucherinnen und Besucher Ihrer Site benötigen diese IP-Adressen nicht.

Weitere Informationen finden Sie unter [The EEC will not load an internal QA URL that is not accessible on public IP](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) in *Fehlerbehebung bei Problemen mit Enhanced Experience Composer*.

+++

### Verwenden Sie eindeutige IDs für Top-Level- und sonstige Elemente, die sich gut als Test-/Targeting-Kandidaten eignen könnten.

+++Details
Alles, was sich unmittelbar innerhalb des Body-Elements befindet, muss über eine eindeutige ID verfügen. Wenn neue Elemente in den Body aufgenommen werden und Code verschoben wird, verfügen wenigstens die übergeordneten Elemente über eine einfachere Erkennungsmethode.

[!DNL Target] erfordert keine IDs, aber die Verwendung von IDs erhöht die Zuverlässigkeit von Erlebnissen, die mit Experience Composer erstellt werden. [!DNL Target] verwendet CSS-Selektoren, um Ihren Inhalt zu ändern, wenn das Erlebnis bereitgestellt wird. Wenn Sie ein Erlebnis bearbeiten, verankert die [!UICONTROL Visual Experience Composer] den Selektor am nächsten Vorgänger mit einem ID-Attribut ungleich null im geänderten HTML-Element. Es wird daher nicht empfohlen, einen Mechanismus zu verwenden, der HTML-ID-Attribute festlegt oder ändert, einschließlich JavaScript-Bibliotheken. Obwohl diese IDs dem [!DNL Target] Experience Composer möglicherweise für die Aktivitätserstellung zur Verfügung stehen, ist die ID, die bei der Erstellung des Erlebnisses verwendet wurde, möglicherweise bei der Ausführung des Erlebnisses nicht verfügbar, wenn JavaScript die ID ändert. Ist eine ID nicht verfügbar, tritt bei dem mit der ID verankerten Selector ein Fehler auf.

+++

### Benennen Sie CSS-Klassen mit einfach zu identifizierenden Bezeichnungen.

+++Details
Beim Bearbeiten von CSS-Klassen in der [!DNL Visual Experience Composer] ist es hilfreich, die Klassen mithilfe beschreibender Klassennamen einfach zu identifizieren. Dadurch wird sichergestellt, dass Sie die richtigen CSS-Klassen bearbeiten und Ihre Seiten wie erwartet angezeigt werden.

Verwenden Sie nicht die CSS-Eigenschaft `!important`, wenn Sie Elemente ausblenden oder entfernen.

Wenn die `!important` CSS-Eigenschaft vorhanden ist, werden von `target.js` während des Versands vorgenommene Änderungen von den CSS-Regeln der Site überschrieben.

+++

### Vermeiden von HTML-Tabellen für Seitenlayouts.

+++Details
[!DNL Target] verwendet JavaScript zum Formatieren einer Seite. Die Modifizierung von tabellenbasierten Layouts mit JavaScript ist kompliziert. Zudem werden tabellenbasierte Layouts möglicherweise nicht in allen Browsern gleich angezeigt. Die besten Ergebnisse erhalten Sie, wenn Sie Seitenlayouts mit CSS erstellen.

+++

### Minimieren Sie die Verwendung von iFrames.

+++Details
Es empfiehlt sich, den Einsatz von iFrames zu minimieren, um die Seiten- und Testverwaltung zu vereinfachen. Visual Experience Composer kann einige Aktionen in einem iFrame anwenden, aber einige Aktionen, z. B. das Ändern der Größe, funktionieren nicht ordnungsgemäß. Das Verwalten und Anpassen von Seiten, die mehrere iFrames verwenden, ist kompliziert. Daher kann auch das Testen von Seiten mit vielen iFrames zu Problemen führen.

+++

### Versuchen Sie, alle dynamischen DOM-Änderungen so bald wie möglich nach DOM-Bereitschaft anzuordnen.

+++Details
Wenn Ihre Änderungen nicht bis `target.js` vor der Erlebnisanwendung angewendet werden, kann die Inhaltsbereitstellung unterbrochen werden. Dies geschieht nur, wenn es zu einer DOM-Änderung in der Hierarchie eines zielgerichteten Elements kommt.

+++

### Verwenden Sie ausschließlich Text oder ein Bild-Tag in Ihren Ankerelementen.

+++Details
`<a>Anchor Text</a>`

ODER-

`<a href=""> <img src=""> </img> </a>`

+++

### Vermeiden Sie Elemente auf Blockebene innerhalb eines Inline-Elements.

+++Details
Elemente auf Blockebene sollten nicht in Inline-Elementen wie Anker, Spanne usw. verwendet werden. Dadurch verlieren Inline-Elemente ihre Höhe und Breite, sodass das Überlagerungswerkzeug im [!UICONTROL Visual Experience Composer] möglicherweise nicht wie erwartet funktioniert.

+++

### Vermeiden Sie die Verwendung des base-Tags in Ihrer Website zur Auflösung von URLs und Links.

+++Details
Der VEC manipuliert die Website im Hintergrund mithilfe eines Proxy-Servers, der die Links aktualisiert. Wenn Sie ein base-Tag hinzufügen, werden die durch den Proxy-Server verwendeten URLs erneut durch den Browser aufgelöst und fehlerhaft dargestellt.

+++

### Die Verwendung von „HTML Bearbeiten“ zur Manipulation der DOM-Struktur kann Selektoren unterbrechen.

+++Details
Wenn Sie beispielsweise zwei Aktionen durchgeführt haben:

* Hinzufügen einer Klasse zu Element 1
* Bearbeiten des HTML für Element 1

Jede Änderung erstellt ein neues Element in VEC. Da die zweite Aktion Element 1 bearbeitet, kann in der zweiten Aktion nichts mehr geändert werden, wenn Sie Element 1 löschen. Daher funktioniert die Änderung nicht mehr.

Mit anderen Worten: Wenn Sie ein Element mit Text hinzufügen und dieses Element in einer anderen Aktion mit einem anderen Text bearbeiten, dann zeigt der Code-Editor beide Aktionen als separate Elemente. Bei der Bearbeitung des Elements haben Sie ein neues Element erstellt, das das ursprünglich von Ihnen erstellte Element ändert und den bearbeiteten Text enthält. Wenn Sie dann das ursprüngliche Element löschen, kann der bearbeitete Text das Element nicht finden, das bearbeitet wurde, und wird folglich nicht angezeigt. Das zweite Element bleibt in der Liste der Elemente erhalten, doch es hat keine Auswirkung auf die Seite, weil das Element, das es ändert, nicht mehr vorhanden ist.

Siehe [Element-Selektoren, die im [!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) verwendet werden.

+++

### Verwenden Sie `<b>`- und `<i>`-Tags beim Formatieren von Textelementen mit dem Rich-Text-Editor.

+++Details
* Für fett gedruckten Text verwenden Sie `<b>` anstelle von `<strong>`.
* Für kursiv gedruckten Text verwenden Sie `<i>` anstelle von `<em>`.

Die Tags `<strong>` und `<em>` können zu unerwarteten Ergebnissen führen.

+++

### Seien Sie beim Entfernen von Formularfeldern vorsichtig.

+++Details
Bestimmte Formularfelder können Pflichtfelder für die Übermittlung sein. Das Entfernen dieser Formularfelder kann Auswirkungen auf Übermittlungen haben.

+++

### Schließen Sie keine `mboxCreate` in Skripte ein.

+++Details
Da `mboxCreate` `document.write` verwendet, ist es nicht empfehlenswert, `mboxCreate` in Skripts einzubinden. Verwenden Sie stattdessen `mboxDefine` und `mboxUpdate`, die den gleichen Zweck erfüllen.

+++

### Aktualisieren Sie kein HTML-Snippet mit [!DNL Target], wenn es JavaScript-Code für seine Initialisierung benötigt.


+++Details
Wenn eine Aktion (HTML bearbeiten) für Seitenkomponenten (wie Schieberegler, Karussells usw.) ausgeführt wird, kann der Versand fehlerhaft aussehen. Der VEC führt die Aktion durch, nachdem die Seitenkomponente von JavaScript instanziiert wurde.

Wird der Seiteninhalt jedoch für Besucher bereitgestellt, wird die Aktion vor Initialisierung der Komponente durchgeführt. Somit kann die Funktion der Komponente zum Zeitpunkt der Bereitstellung beschädigt oder in Ordnung sein. Die Funktion der Komponente hängt mit dem auf der Seite verwendeten Skript zusammen, das die Komponente definiert.

Sollten Sie die Bereitstellung prüfen und feststellen, dass sie beim ersten Versuch einwandfrei funktioniert, ist dies keine Garantie dafür, dass sie das auch weiterhin tut. Es besteht möglicherweise eine Gleichzeitigkeitsbedingung.

* Wenn eine Wettlaufsituation vorliegt, funktioniert die Bereitstellung gelegentlich.
* Wenn keine Wettlaufbedingung vorliegt, funktioniert die Lieferung immer.

Prüfen Sie Ihre Seite mehrmals, um sicherzustellen, dass die Bereitstellung wie erwartet funktioniert.

+++

### Vermeiden Sie die Verwendung eines base-Tags in Ihrer Website zur Auflösung von URLs und Links.

+++Details
Wenn Sie die [!UICONTROL Enhanced Experience Composer] verwenden, wird die Website im Hintergrund von einem Proxy-Server manipuliert, der alle Link-URLs aktualisiert, damit sie im Proxy funktionieren. Wenn Sie ein Basis-Tag hinzufügen, werden alle diese URLs vom Browser aufgelöst, sodass sie beschädigt erscheinen.

+++

### Wichtiger Text auf der Seite, der für das Targeting verwendet wird, sollte innerhalb eines Elements in HTML-Code geschrieben werden.

+++Details
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

In diesem Beispiel wird das gesamte Ankerelement im VEC ausgewählt, was sich bei der Zielgruppenbestimmung negativ auf andere Elemente auswirkt.

+++

### Verwenden Sie keine `top` oder `self` Variablen im JavaScript-Code.

+++Details
Wenn die [!UICONTROL Enhanced Experience Composer] aktiviert ist, werden die Werte der Variablen „top“ und „self“ aktualisiert, um die iFrame-Busting zu deaktivieren. Arbeiten Sie stattdessen mit einer X-Frame-Optionsüberschrift, um iframe-Busting anstatt benutzerdefinierter JavaScript-Codes einzusetzen.

+++

### Testen Sie stets Ihre Webseite, wenn für den Zeitpunkt des Ladens der Seite neue Parameter hinzugefügt werden sollen.

+++Details
Um beispielsweise `www.abc.com` zu öffnen, werden die folgenden URL-Parameter verwendet:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Diese Parameter ermöglichen die Bearbeitung in einem iframe.

Stellen Sie sicher, dass die Webseite wie erwartet lädt, nachdem solche Parameter hinzugefügt wurden.

+++

### Stellen Sie sicher, dass sich die Seite in einem iframe wie gewünscht öffnen lässt.

+++Details
Deaktivieren Sie iframe-Busting-Techniken auf Ihrer Website und überprüfen Sie, ob die Website wie erwartet innerhalb eines iframe auf einer Dummy-Seite geöffnet wird. Beispiel:

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

+++

## Einschränkungen  {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Beachten Sie die folgenden Einschränkungen bei der Verwendung des [!UICONTROL Visual Experience Composer] zum Entwerfen Ihrer Aktivität.

### Die [!UICONTROL Move]-Funktion unterstützt keinen z-Index.

+++Details
Da keine z-index-Funktionalität vorhanden ist, kann das verschobene Element nicht über ein anderes Element verschoben werden. Weitere Details finden Sie unter [Einschränkungen](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

+++

### Eine Neuanordnung von Elementen wirkt sich auf das Klick-Tracking aus.

+++Details
Wenn ein für Klick-Tracking gekennzeichnetes Element neu angeordnet wird, ändern sich die Pfade der neu angeordneten Elemente. Infolgedessen ist das Element an dem Ort, an dem sich das Originalelement vor der Neuanordnung befunden hat, das Element, dessen Klicks verfolgt werden.

Dies passiert, weil sowohl der Code zur Bereitstellung des Aktivitäteninhalts als auch der Code für das Klick-Tracking in einem einzigen Code enthalten ist, der für die Seite bereitgestellt wird. Wenn Sie zu einer anderen Seite navigieren und Klick-Tracking einrichten, dann werden der Aktivitätsinhalts-Code und der Klick-Trackingcode für diese Seite bereitgestellt. Wenn die Klick-Tracking-Seite eine ähnliche Struktur aufweist wie die Seite, auf der der Test ausgeführt wird, dann kann der Testinhalt auch auf der Klick-Tracking-Seite erscheinen.

+++

### Das Einfügen eines Elements funktioniert möglicherweise nicht in einer `<div>`, die eine Mbox ist.

+++Details
Wenn eine Mbox ein Angebot enthält, kann das Einfügen eines Elements als `insertBefore` und nicht als `insertAfter` erscheinen, wenn die Mbox falsch implementiert ist.

+++

### Beim Bearbeiten von über- und untergeordneten Elementen sollten Sie zunächst das übergeordnete Element bearbeiten.

+++Details
Wenn Sie eine Bildaktion für ein Element austauschen und anschließend den Text oder das HTML für das übergeordnete Element bearbeiten, können Bereitstellungsprobleme auftreten. Der beste Arbeitsablauf besteht darin, das übergeordnete Element zu bearbeiten, bevor Sie das Bild im untergeordneten Element austauschen.

+++

### Es kann kein Seitenelement ausgewählt werden, das eine Mbox als untergeordnetes Element enthält.

+++Details
Wenn Ihre Seite zum Beispiel Folgendes enthält:

```html
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

Das äußere div-Element sollte in einem Erlebnis nicht ausgewählt werden, da die auf der Seite hartcodierte Mbox weiterhin einen Aufruf an [!DNL Target] ausführt und eine Antwort erhält. Diese Antwort beeinträchtigt die für das größere Seitenelement vorgesehene Antwort.

+++

### Proxy-IPs können in der Kundenumgebung blockiert werden.

+++Details
Wenn Sie [!UICONTROL Enhanced Experienced Composer] auf einer Nicht-Live-Site verwenden, z. B. einer Staging-Umgebung, werden möglicherweise Zeitüberschreitungen und Fehler bei Zugriff verweigert angezeigt, wenn Ihre Site RIPs blockiert.

+++

## Einschränkungen   {#section_F33C2EA27F2E417AA036BC199DD6C721}

Beachten Sie bei der Arbeit mit VEC die folgenden Einschränkungen:

### Handhabung der VEC-Kompatibilität mit [!DNL Chrome] Änderungen der Erweiterungsrichtlinie. {#ext}

+++Details
Aufgrund aktualisierter [V3-Manifestrichtlinien in Google Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank} können Erweiterungen das ursprüngliche DOM nicht mehr ändern, bevor es vom Browser geparst wird. Daher können bestimmte Sicherheitsskripte - z. B. iframe-busting-Implementierungen - das Laden von Seiten im VEC blockieren.

Um die Kompatibilität zu gewährleisten, sollten diese Skripte bedingt deaktiviert werden, wenn die Seite innerhalb des [!DNL Target] iFrames geladen wird. Dieser Vorgang kann sicher durchgeführt werden, indem überprüft wird, ob das `window.adobeVecExtension` Objekt vorhanden ist, das während des Ladevorgangs des VEC von [!DNL Target] injiziert wird.

Die folgenden Code-Snippets sind Beispiele für iframe-Busting-Code, der dazu führen kann, dass Web-Seiten im VEC nicht geladen werden:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

Mit einer einfachen Prüfung kann überprüft werden, ob eine Web-Seite in [!DNL Target] eingebettet ist. Ein Code-Snippet sollte wie folgt aussehen:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

### Sie können ein Element nicht aus einem Container mit einer darauf folgenden CSS-Eigenschaft verschieben.

+++Details
Ein Element kann nicht außerhalb eines Behälters verschoben werden, auf den eine CSS-Eigenschaft folgt.

+++

### Sie können das [!UICONTROL Button] Element für die Neuanordnung nicht auswählen.

+++Details
[!UICONTROL Button] Elemente können nicht direkt zum Neuanordnen ausgewählt werden. Um die Neuanordnung zu ermöglichen, platzieren Sie Schaltflächen in einem größeren Container.

+++

### Auf Mboxes stehen lediglich Tauschangebote zur Verfügung.

+++Details
Aktionen wie [!UICONTROL Edit Class] und [!UICONTROL Rearrange] sind innerhalb einer Mbox nicht zulässig.

+++

### Sie sollten dasselbe Element nicht neu ordnen und verschieben.

+++Details
Wenn ein Element an einen anderen Ort verschoben wurde und Sie den übergeordneten Behälter auswählen und versuchen, die untergeordneten Elemente neu zu ordnen, ist das verschobene Element nicht betroffen und bleibt, wo es ist. Die Neuordnung wird möglicherweise nicht wie gewünscht dargestellt.

+++

### Die [!UICONTROL Change Image] Aktion funktioniert nicht für ein Bild in einem Karussell.

+++Details
Wenn Ihre Seite beispielsweise ein Karussell mit sechs Bildern enthält und Sie ein Bild mit dem zweiten Bild des Karussells austauschen möchten, funktioniert die [!UICONTROL Change Image] nicht.

Um dieses Problem zu umgehen, wählen Sie den übergeordneten Container aus und bearbeiten Sie mit der Aktion [!UICONTROL Edit HTML] die HTML des Karussells, um die Bildquelle des gewünschten Bildes zu aktualisieren.

+++

### Größe von Bildern kann nicht in einer Mbox geändert werden.

+++Details
Wenn Sie ein Bild in einem Mbox-Element tauschen und dann versuchen, die Größe des Bilds entsprechend der Mbox-Elementgröße anzupassen, ist die Größenanpassung nicht gestattet.

+++

### Nachdem Sie ein Bild ausgetauscht haben, können Sie die [!UICONTROL Edit] Aktion nicht mehr auswählen.

+++Details
Nach dem Bildtausch können Sie die Scene7-URL nicht bearbeiten.

+++

### HTML-Elemente mit einer externen Quelle können nicht bearbeitet werden.

+++Details
Beispiel: Video, Audio-Tags, Einbetten, iFrames, Frames.

+++

### Klick-Tracking für Ankerelemente, die etwas anderes als Text oder Bild-Tags enthalten, funktioniert nicht.

+++Details
Zum Beispiel funktioniert Klick-Tracking nicht, wenn das Element JavaScript enthält.

+++

### Seiten müssen URL-Parameter akzeptieren, damit VEC funktioniert.

+++Details
Einige Websites entfernen sämtliche URL-Parameter ihrer Seiten. Der VEC benötigt diese Parameter jedoch.

+++

### Bei Verwendung eines Skripts als Teil von HTML sollten alle Variablen und Funktionen, auf die von außerhalb zugegriffen wird, unter dem Namespace Window deklariert werden.

+++Details
Das Skript wird im Rahmen von `target.js` ausgeführt, nachdem die Seite geladen wurde. Somit kann auf lokal angegebene Variablen oder Funktionen von außen nicht zugegriffen werden.

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

+++

### Durch das Einfügen eines Bildes aus der [!UICONTROL Content] (Scene7) und das Bearbeiten des HTMLS wird die Bild-URL beschädigt.

+++Details
Fügen Sie ein Ankerelement innerhalb des div „customHeaderMessage“ sowie Platzhaltertext ein:

```html
<a href="#"> 
<span> Dummy text </span>
</a>
```

Wählen Sie dieses div mit der Aktion [!UICONTROL Insert Element] aus, um ein Bild als gleichrangiges Element dieses Platzhalter-Text-div einzufügen.

Nach Einfügen des Bilds sollte es wie folgt aussehen:

```html
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Löschen Sie den Platzhaltertext.

+++

### Die `customCode` Aktion in VEC funktioniert nicht mit [!DNL Internet Explorer] 8.

+++Details
Aufgrund von Einschränkungen in IE8 beim Umgang mit Skriptinhalten unterstützt `target.js` dies in IE8 nicht. Wenn die Seite jQuery enthält und global für das Fensterobjekt verfügbar gemacht wird, können `target.js` als Problemumgehung die Aktion &quot;`customCode` senden“ verwenden. Stellen Sie sicher, dass `window.jQuery` und `window.jQuery.fn.prepend` definiert sind.

+++

### Klick-Tracking wird nur auf der Seite unterstützt, auf der Erlebnisse erstellt werden, oder auf einer Weiterleitungsseite.

+++Details
Obwohl der [!UICONTROL Browse]-Modus für Klick-Tracking in VEC verfügbar ist, kann der [!UICONTROL Browse]-Modus nicht zum Hinzufügen von Klick-Tracking auf einer Seite verwendet werden.

+++
