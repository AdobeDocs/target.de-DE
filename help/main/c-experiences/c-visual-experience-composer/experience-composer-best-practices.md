---
keywords: Visual Experience Composer;Best Practices für Visual Experience Composer;Einschränkungen von Visual Experience Composer;Nachteile von Visual Experience Composer;Best Practices für VEC;VEC
description: Erfahren Sie mehr über Best Practices, damit Ihre Erlebnisse bei der Verwendung von [!UICONTROL Visual Experience Composer] (VEC) wie erwartet funktionieren.
title: Was sind [!UICONTROL Visual Experience Composer] Best Practices und Einschränkungen?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
TQID: 'https://experienceleague.adobe.com/upZDSyuS9VqUmYskNXrlYazhwRHmZGBpSR-cR-qliRs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '2420'
ht-degree: 7%
---
# [!UICONTROL Visual Experience Composer] Best Practices und Einschränkungen {#vec-best-practices}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie mehr über die Best Practices, Einschränkungen und Einschränkungen, die Sie beim Erstellen von Erlebnissen im **[!UICONTROL Visual Experience Composer]** (VEC) beachten sollten.

>[!ENDSHADEBOX]

Das Befolgen dieser Verfahren hilft Erlebnissen, die in der Funktion [!DNL Adobe Target]Visual **[!UICONTROL Composer]** (VEC) erstellt wurden, wie gewünscht. Die Einschränkungen beschreiben Verhaltensweisen, die häufige Probleme verursachen können. Ihre Kenntnis hilft daher, Probleme zu vermeiden und die Leistung aufrecht zu erhalten.

## Best Practices {#best-practices}

Die folgenden Verfahren gelten für die Verwendung von VEC.

### Aktivieren des [!UICONTROL Enhanced Experience Composer] {#enable-eec}

Der **[!UICONTROL Enhanced Experience Composer]** kann auf Kontoebene aktiviert werden, wodurch er für alle im Konto erstellten Aktivitäten oder für einzelne Aktivitäten aktiviert wird.

* **Kontoebene:** Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und schalten Sie dann **[!UICONTROL Enhanced Experience Composer aktivieren]** in die Position Ein um.
* **Aktivitätsebene:** Klicken Sie beim Erstellen einer Aktivität im **[!UICONTROL Visual Experience Composer]** auf **[!UICONTROL Konfigurieren]** > **[!UICONTROL Seitenbereitstellung]** und schalten Sie dann **[!UICONTROL Enhanced Experience Composer aktivieren]** in die Position Ein um.

### Seiteneinrichtung und Laden

+++ Platzieren Sie die at.js-Referenz oben im Abschnitt `<head>` der Seite.

Wenn auch der **[!UICONTROL Besucher-API-]**) verwendet wird, platzieren Sie das Besucher-API-Skript über at.js.

+++

+++ Zulassungsliste von IP-Adressen, wenn [!UICONTROL Enhanced Experience Composer] nicht auf sicheren Seiten der Site geladen wird.

Durch die Zulassungsauflistung der IP-Adressen der [!DNL Adobe]-Server, die für den **[!UICONTROL Enhanced Experience Composer]**-Proxy verwendet werden, werden Ladeprobleme behoben. Diese IP-Adressen sind nur für die Bearbeitung von Aktivitäten erforderlich. Besucherinnen und Besucher der Website benötigen sie nicht. Die IP-Adressen sind unter [Der EEC lädt keine interne QA-URL, auf die über öffentliche IP nicht zugegriffen werden kann](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#eec-ip-addresses) in *Fehlerbehebung bei Problemen mit Enhanced Experience Composer* aufgeführt.

+++

+++ Verwenden Sie das Base-Tag auf der Website nicht, um URLs und Links aufzulösen.

VEC, einschließlich des **[!UICONTROL Enhanced Experience Composer]**, manipuliert die Website im Hintergrund über einen Proxy-Server, der alle Link-URLs aktualisiert, damit sie im Proxy funktionieren. Wenn ein Basis-Tag hinzugefügt wird, löst der Browser diese URLs erneut auf, sodass sie beschädigt erscheinen.

+++

+++ Verwenden Sie nicht die Variablen `top` oder `self` im JavaScript-Code.

Wenn der **[!UICONTROL Enhanced Experience Composer]** aktiviert ist, werden die Werte der `top`- und `self`-Variablen aktualisiert, um iframe-Busting zu deaktivieren. Verwenden Sie einen X-Frame-Options-Header, um iframe-Busting anstelle von benutzerdefiniertem JavaScript-Code hinzuzufügen.

+++

+++ Testen Sie die Website immer, wenn beim Laden der Seite Parameter hinzugefügt werden.

Beispielsweise werden die folgenden URL-Parameter verwendet, um `www.abc.com` zur Bearbeitung in einem iframe zu öffnen:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Stellen Sie sicher, dass die Website erwartungsgemäß geladen wird, nachdem Sie Parameter wie diese hinzugefügt haben.

+++

+++ Stellen Sie sicher, dass die Seite wie erwartet in einem iFrame geöffnet wird.

Deaktivieren Sie iFrame-Busting-Techniken auf der Website und überprüfen Sie, ob die Website wie erwartet in einem iFrame auf einer Platzhalterseite geöffnet wird. Beispiel:

```html
<!DOCTYPE html>
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

### Seiten-Markup

+++ Verwenden Sie eindeutige IDs für Elemente der obersten Ebene und für alle anderen Elemente, die sich gut für Tests oder die Zielgruppenbestimmung eignen.

Alles, was sich unmittelbar im Body-Element befindet, sollte eine eindeutige ID haben, sodass zumindest die übergeordneten Elemente leicht zu erkennen sind, wenn neue Elemente in den Body eingefügt werden und sich der Code bewegt.

[!DNL Target] erfordert keine IDs, aber IDs erhöhen die Zuverlässigkeit von Erlebnissen, die mit Experience Composer erstellt werden. [!DNL Target] verwendet CSS-Selektoren, um Inhalte zu ändern, wenn das Erlebnis bereitgestellt wird. Wenn ein Erlebnis bearbeitet wird, verankert **[!UICONTROL Visual Experience Composer]** den Selektor am nächsten Vorgänger des geänderten HTML-Elements, das ein ID-Attribut ungleich null aufweist. Es wird daher nicht empfohlen, einen Mechanismus zu verwenden, einschließlich JavaScript-Bibliotheken, der HTML-ID-Attribute festlegt oder ändert. Diese IDs sind möglicherweise für Experience Composer verfügbar, wenn die Aktivität erstellt wird. Wenn JavaScript sie jedoch ändert, ist die bei der Erstellung verwendete ID möglicherweise nicht verfügbar, wenn das Erlebnis ausgeführt wird. Wenn keine ID verfügbar ist, schlägt der mit dieser ID verankerte Selektor fehl.

+++

+++ Verwenden Sie beschreibende CSS-Klassennamen.

Beschreibende Klassennamen machen es einfach, die Klassen zu identifizieren, wenn CSS-Klassen im **[!UICONTROL Visual Experience Composer) bearbeitet]**. Dadurch wird sichergestellt, dass die richtigen CSS-Klassen bearbeitet werden und die Seiten erwartungsgemäß angezeigt werden.

+++

+++ Verwenden Sie beim Ausblenden oder Entfernen von Elementen nicht die `!important` CSS-Eigenschaft.

Wenn die `!important` CSS-Eigenschaft vorhanden ist, überschreiben die CSS-Regeln der Site die Änderungen, die `target.js` während des Versands vornimmt.

+++

+++ HTML-Tabellen für Seiten-Layouts vermeiden.

[!DNL Target] verwendet JavaScript zum Formatieren einer Seite. Tabellenbasierte Layouts lassen sich mit JavaScript nur schwer ändern. Tabellenbasierte Layouts werden möglicherweise nicht in allen Browsern gleich angezeigt. Die besten Ergebnisse erhalten Sie, wenn Sie Seitenlayouts mit CSS erstellen.

+++

+++ Minimieren Sie die Verwendung von iFrames.

Durch die Minimierung von iFrames wird die Seiten- und Testverwaltung vereinfacht. Der **[!UICONTROL Visual Experience Composer]** kann einige Aktionen innerhalb eines iFrames anwenden, aber einige Aktionen, wie z. B. die Größenanpassung, funktionieren nicht richtig. Seiten, die mehrere iFrames verwenden, sind schwer zu verwalten und ihre Größe zu ändern, sodass das Testen von iFrame-lastigen Seiten Probleme verursachen kann.

+++

+++ Verwenden Sie in Ankerelementen nur Text oder ein Bild-Tag.

Ein Ankerelement enthält entweder Nur-Text:

`<a>Anchor Text</a>`

oder ein Bild-Tag:

`<a href=""> <img src=""> </img> </a>`

+++

+++ Vermeiden Sie Elemente auf Blockebene innerhalb eines Inline-Elements.

Elemente auf Blockebene sollten nicht in Inline-Elementen wie Anker- und Span-Elementen verwendet werden. Dadurch verlieren die Inline-Elemente ihre Höhe und Breite, sodass das Überlagerungswerkzeug im **[!UICONTROL Visual Experience Composer]** möglicherweise nicht wie erwartet funktioniert.

+++

+++ Seien Sie beim Entfernen von Formularfeldern vorsichtig.

Bestimmte Formularfelder sind möglicherweise zur Übermittlung obligatorisch, sodass sich ihre Entfernung auf die Übermittlung auswirken könnte.

+++

+++ Behalten Sie wichtigen Text bei, der für die Zielgruppenbestimmung im HTML-Code innerhalb eines Elements verwendet werden könnte.

Beispielsweise kann der Text des Warenkorbs im VEC nicht als Ziel ausgewählt werden, wenn der Code wie folgt aussieht:

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart">
   <img alt="Shopping Cart" src="/images/ico-cart.gif"></img>
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

### Bearbeiten und Versand

+++ Ordnen Sie alle dynamischen DOM-Änderungen so bald wie möglich an, nachdem DOM bereit ist.

Wenn die Änderungen nicht angewendet werden können, bevor `target.js` das Erlebnis anwendet, kann die Inhaltsbereitstellung unterbrochen werden. Dies geschieht nur, wenn es zu einer DOM-Änderung in der Hierarchie eines zielgerichteten Elements kommt.

+++

+++ Durch die Verwendung von HTML bearbeiten zur Bearbeitung der DOM-Struktur können Selektoren beschädigt werden.

Es werden beispielsweise zwei Aktionen durchgeführt:

* Element 1 wird eine Klasse hinzugefügt.
* Die HTML von Element 1 wird bearbeitet.

Jede Änderung erstellt ein neues Element in VEC. Mit der zweiten Aktion wird Element 1 geändert. Wenn Element 1 gelöscht wird, hat die zweite Aktion also nichts mehr zu ändern, und die Änderung funktioniert nicht mehr.

Wenn ein Element mit Text und einer separaten Aktion hinzugefügt wird und dieses Element dann mit einem anderen Text bearbeitet, zeigt der Code-Editor beide Aktionen als separate Elemente an. Die Bearbeitung erstellt ein neues Element, das das ursprüngliche ändert und den bearbeiteten Text enthält. Wenn das ursprüngliche Element dann gelöscht wird, kann der bearbeitete Text das zu ändernde Element nicht finden und wird nicht angezeigt. Das zweite Element verbleibt in der Liste der Elemente, hat jedoch keine Auswirkungen auf die Seite, da das geänderte Element nicht mehr vorhanden ist.

Siehe [Element-Selektoren, die im **[!UICONTROL Visual Experience Composer“ verwendet &#x200B;]**](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#vec-selectors).

+++

+++ Verwenden Sie `<b>`- und `<i>`-Tags beim Formatieren von Textelementen mit dem Rich-Text-Editor.

* Für fett gedruckten Text verwenden Sie `<b>` anstelle von `<strong>`.
* Für kursiv gedruckten Text verwenden Sie `<i>` anstelle von `<em>`.

Die Tags `<strong>` und `<em>` können zu unerwarteten Ergebnissen führen.

+++

+++ Schließen Sie keine `mboxCreate` in Skripte ein.

`mboxCreate` verwendet `document.write`, daher wird das Einschließen in Skripte nicht empfohlen. Verwenden Sie `mboxDefine` und `mboxUpdate` für denselben Zweck.

+++

+++ Aktualisieren Sie ein HTML-Snippet nicht mit [!DNL Target], wenn das Snippet JavaScript-Code für seine Initialisierung erfordert.

Wenn eine Aktion (HTML bearbeiten) für Seitenkomponenten wie Schieberegler und Karussells ausgeführt wird, kann der Versand fehlerhaft aussehen. Der VEC führt die Aktion durch, nachdem JavaScript die Seitenkomponente instanziiert hat. Wenn der Seiteninhalt für Besuchende bereitgestellt wird, wird die Aktion jedoch angewendet, bevor die Komponente instanziiert wird. Je nach dem Skript, das die Komponente auf der Seite definiert, kann es daher sein, dass die Funktionalität der Komponente bei der Bereitstellung beeinträchtigt ist oder nicht.

Ein Versandtest, der beim ersten Mal funktioniert, garantiert nicht, dass der Versand weiterhin funktioniert, da eine Racebedingung vorliegen kann:

* Wenn eine Wettlaufsituation vorliegt, funktioniert die Bereitstellung gelegentlich.
* Wenn keine Wettlaufbedingung vorliegt, funktioniert die Lieferung immer.

Testen Sie die Seite mehrmals, um sicherzustellen, dass der Versand erwartungsgemäß funktioniert.

+++

## Einschränkungen {#caveats}

Die folgenden Einschränkungen gelten für die Verwendung des **[!UICONTROL Visual Experience Composer]** zum Entwerfen einer Aktivität.

+++ Die [!UICONTROL Verschieben]-Funktion unterstützt keinen z-Index.

Ohne Z-Indexfunktion kann ein verschobenes Element nicht über einem anderen Element platziert werden. Weitere Details finden Sie unter [Einschränkungen](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

+++

+++ Eine Neuanordnung von Elementen wirkt sich auf das Klick-Tracking aus.

Wenn ein für das Klick-Tracking markiertes Element neu angeordnet wird, ändern sich die Pfade der neu angeordneten Elemente. Daher werden Klicks auf das Element an der Stelle nachverfolgt, an der sich das ursprüngliche Element vor seiner Neuanordnung befand.

Dies geschieht, weil der Code, der den Aktivitätsinhalt bereitstellt, und der Code, der Klicks verfolgt, in einem Code enthalten sind, der an die Seite gesendet wird. Wenn eine andere Seite aufgerufen wird und dort Klick-Tracking eingerichtet ist, werden beide Code-Abschnitte an diese Seite gesendet. Wenn die Klick-Tracking-Seite eine Seitenstruktur hat, die der Seitenstruktur der Seite ähnelt, auf der der Test ausgeführt wird, kann der Testinhalt auch auf der Klick-Tracking-Seite angezeigt werden.

+++

+++ Das Einfügen eines Elements funktioniert möglicherweise nicht in einer `<div>`, die eine Mbox ist.

Wenn eine Mbox ein Angebot enthält und die Mbox falsch implementiert ist, wird ein eingefügtes Element möglicherweise als `insertBefore` und nicht als `insertAfter` angezeigt.

+++

+++ Wenn Sie sowohl ein übergeordnetes als auch ein untergeordnetes Element bearbeiten, bearbeiten Sie zuerst das übergeordnete Element.

Wenn eine Bildaktion gegen ein Element getauscht wird und der Text oder die HTML des übergeordneten Elements dann bearbeitet wird, können Versandprobleme auftreten. Der beste Arbeitsablauf besteht darin, das übergeordnete Element zu bearbeiten, bevor Sie das Bild im untergeordneten Element austauschen.

+++

+++ Wählen Sie kein Seitenelement aus, das eine Mbox als untergeordnetes Element enthält.

Wenn die Seite beispielsweise den folgenden Code enthält:

```html
<div>
  <div class="mboxDefault" >
  </div>
  <script>mboxCreate('myMbox');
</script>
</div>
```

Das äußere div-Element sollte in einem Erlebnis nicht ausgewählt werden, da die auf der Seite hartcodierte Mbox weiterhin einen Aufruf an [!DNL Target] ausführt und eine Antwort erhält. Diese Antwort beeinträchtigt die für das größere Seitenelement vorgesehene Antwort.

+++

+++ Proxy-IP-Adressen können in der Umgebung des Kunden blockiert werden.

Wenn der **[!UICONTROL Enhanced Experience Composer]** auf einer Nicht-Live-Site wie einer Staging-Umgebung verwendet wird, können Zeitüberschreitungen und Fehler bei Zugriff verweigert auftreten, wenn die Site die Proxy-IP-Adressen blockiert.

+++

## Einschränkungen {#section_F33C2EA27F2E417AA036BC199DD6C721}

Die folgenden Einschränkungen gelten für die Arbeit mit VEC.

### Seitenanforderungen

+++ Handhabung der VEC-Kompatibilität mit [!DNL Chrome] Änderungen der Erweiterungsrichtlinie.

Unter den aktualisierten [V3-Manifestrichtlinien in Google Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank} können Erweiterungen das Original-DOM nicht mehr ändern, bevor der Browser es analysiert. Daher können bestimmte Sicherheitsskripte, wie z. B. iframe-Busting-Implementierungen, das Laden von Seiten im VEC blockieren.

Um die Kompatibilität zu gewährleisten, deaktivieren Sie diese Skripte bedingt, wenn die Seite innerhalb des [!DNL Target] iFrames geladen wird. Dies kann sicher geschehen, indem Sie prüfen, ob das `window.adobeVecExtension` vorhanden ist, das beim Laden des VEC injiziert [!DNL Target].

Die folgenden Code-Snippets sind Beispiele für iframe-Busting-Code, der verhindern kann, dass eine Web-Seite im VEC geladen wird:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

Mit einer einfachen Prüfung kann überprüft werden, ob eine Web-Seite in [!DNL Target] eingebettet ist. Der Code-Ausschnitt sieht wie folgt aus:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

+++ Seiten müssen URL-Parameter akzeptieren, damit VEC funktioniert.

Einige Websites entfernen URL-Parameter von ihren Seiten, der VEC erfordert diese Parameter jedoch.

+++

+++ Wenn ein Skript als Teil von HTML verwendet wird, deklarieren Sie alle Variablen und Funktionen, auf die von außerhalb unter dem Fensternamespace zugegriffen wird.

Das Skript wird im Gültigkeitsbereich von `target.js` ausgeführt, nachdem die Seite geladen wurde, sodass keine Variable oder Funktion, die lokal deklariert ist, von außerhalb des Skriptblocks zugänglich ist.

*Falsch:*

```html
<script>
  var myVar = 123;
  function myFunc() {
    //
  }
</script>
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

+++ Die `customCode` Aktion in VEC funktioniert nicht mit [!DNL Internet Explorer] 8.

`target.js` unterstützt diese Aktion in IE8 aufgrund von IE8-Einschränkungen beim Umgang mit Skriptinhalten nicht. Wenn die Seite jQuery enthält und jQuery global für das Fensterobjekt verfügbar gemacht wird, können `target.js` die `customCode` Aktion bereitstellen. Stellen Sie sicher, dass `window.jQuery` und `window.jQuery.fn.prepend` definiert sind.

+++

### Neuanordnung von - und -Mboxes

**Ein Element kann nicht aus einem Container verschoben werden, auf den eine CSS-Eigenschaft folgt.**

+++ Das [!UICONTROL Button]-Element kann nicht zum Neuanordnen ausgewählt werden.

**[!UICONTROL Button]**-Elemente können nicht direkt zum Neuanordnen ausgewählt werden. Um die Neuanordnung zu ermöglichen, platzieren Sie die Schaltflächen in einem größeren Container.

+++

+++ Das gleiche Element nicht neu anordnen und verschieben.

Wenn ein Element an eine andere Position verschoben wurde und der übergeordnete Container dann ausgewählt wird, um die untergeordneten Elemente neu anzuordnen, ist das verschobene Element nicht betroffen und bleibt an der Position, an der es sich befindet. Die Neuordnung wird möglicherweise nicht wie gewünscht dargestellt.

+++

+++ Auf Mboxes stehen lediglich Tauschangebote zur Verfügung.

Aktionen wie **[!UICONTROL Klasse bearbeiten]** und **[!UICONTROL Neu anordnen]** sind in einer Mbox nicht zulässig.

+++

### Bilder

+++ Die [!UICONTROL Bild ändern]-Aktion funktioniert nicht für ein Bild in einem Karussell.

Wenn die Seite beispielsweise ein Karussell mit sechs Bildern enthält und ein Bild durch das zweite Bild des Karussells getauscht werden soll, funktioniert die Aktion **[!UICONTROL Bild ändern]** nicht.

Wählen Sie als Problemumgehung den übergeordneten Container aus und verwenden Sie die Aktion **[!UICONTROL HTML bearbeiten]**, um die HTML des Karussells zu bearbeiten und die Bildquelle des gewünschten Bildes zu aktualisieren.

+++

+++ Größe von Bildern kann nicht in einer Mbox geändert werden.

Wenn ein Bild in einem Mbox-Element ausgetauscht und dann die Größe entsprechend der Größe des Mbox-Elements geändert wird, ist die Größenanpassung nicht zulässig.

+++

+++ Nachdem ein Bild getauscht wurde, kann [!UICONTROL &#x200B; Aktion &#x200B;]Bearbeiten“ nicht mehr ausgewählt werden.

Nachdem das Bild getauscht wurde, kann die Scene7-URL nicht mehr bearbeitet werden.

+++

+++ Durch das Einfügen eines Bildes aus der [!UICONTROL Content]-Bibliothek (Scene7) und das Bearbeiten des HTMLS wird die Bild-URL beschädigt.

Fügen Sie ein Ankerelement im `customHeaderMessage` div mit Platzhaltertext hinzu:

```html
<a href="#">
<span> Dummy text </span>
</a>
```

Wählen Sie diesen Div mit der Aktion **[!UICONTROL Element einfügen]** aus, um ein Bild als gleichrangiges Element des Platzhaltertextes einzufügen.

Nach dem Einfügen des Bildes sieht der Code wie folgt aus:

```html
<a href="#">
<span> Dummy text </span>
<img src=""> This is inserted Image. </img>
</a>
```

Löschen Sie den Platzhaltertext.

+++

### Klick-Tracking und externe Inhalte

+++ Klick-Tracking für Ankerelemente, die etwas anderes als Text oder Bild-Tags enthalten, funktioniert nicht.

Zum Beispiel funktioniert Klick-Tracking nicht, wenn das Element JavaScript enthält.

+++

+++ Klick-Tracking wird nur auf der Seite unterstützt, auf der Erlebnisse erstellt werden, oder auf einer Weiterleitungsseite.

Obwohl **[!UICONTROL Durchsuchen]**-Modus für Klick-Tracking in VEC verfügbar ist, kann **[!UICONTROL Durchsuchen]**-Modus nicht zum Hinzufügen von Klick-Tracking auf einer Seite verwendet werden.

+++

+++ HTML-Elemente mit einer externen Quelle können nicht bearbeitet werden.

Beispiel: Video, Audio-Tags, Einbetten, iFrames und Frames.

+++
