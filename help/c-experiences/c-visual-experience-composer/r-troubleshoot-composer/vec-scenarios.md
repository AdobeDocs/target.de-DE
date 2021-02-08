---
keywords: Recommendations
description: Hier werden gängige Szenarien erläutert, die zeigen, wie sich Änderungen, die im Visual Experience Composer (VEC) an Ihrer Seite vorgenommen wurden, auf die Fähigkeit Adobe Targets zur Anzeige eines Erlebnisses auswirken.
title: Was sind einige häufige Szenarien zur Seitenanpassung?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 90%

---


# Szenarien für die Seitenmodifizierung

Die Szenarien in diesem Thema zeigen, wie sich an Ihrer Seite vorgenommene Änderungen auf die Fähigkeit von Adobe Target auswirken, ein Erlebnis anzuzeigen.

Der Target-Selektor legt fest, wo ein Erlebnis angezeigt wird. Wenn eine Seite außerhalb von Target modifiziert wird, können sich die Änderungen auf die Fähigkeit von Target auswirken, das Erlebnis anzuzeigen.

Bei der Verwendung des Selektors entspricht die eindeutige Klasse nicht der ID. Der Selektor funktioniert immer mit einer eindeutigen Klasse. Wenn dem Element keine Klasse zugewiesen ist, berechnet der Selektor die Anzahl der früheren Geschwisterelemente, die denselben Tag-Namen aufweisen.

>[!NOTE]
>
>Obwohl diese Szenarien Listenelemente als Beispiele verwenden, gelten die Konzepte für jedes Element.

## Szenario: Vor dem ausgewählten Element wird ein Element mit einem anderen Klassennamen eingefügt {#section_298F661F72384F6AB957D5885A99D822}

In diesem Beispiel wird ein neues Element als Geschwisterelement des Elements im Target-Selektor eingefügt.

Es besteht die Möglichkeit, dass am Element vorhandene erste Klasse durch JavaScript hinzugefügt wird. In diesem Fall scheitert die Bereitstellung und die Aktion wird nicht angewendet.

**Eingefügtes Element:**

```html
<li class="kids-section">Kids</li>
```

**Ausgewählt:**

`<li class="women-section">Women</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

Der Selektor funktioniert wie erwartet, da `li.women-section:eq(0)` nicht betroffen ist.

Bevor:

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul> 
</div>
```

Nachher:

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

## Szenario: Es wird ein Element mit demselben Klassennamen wie das ausgewählte Element eingefügt {#section_0969B88C2F154E648D9969C8C85EF55A}

Bei diesem Szenario wird versucht, eine Liste einzufügen, wenn ein Listenelement ausgewählt ist.

**Eingefügtes Element:**

```html
<ul class="nav"> 
   <li class="item"> Sale </li> 
   <li> class="item"> Offers </li> 
</ul>
```

**Ausgewählt**

`<li class="women-section">Women</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

Der Selektor funktioniert nicht, weil `ul.nav:eq(0)` ein dynamisch hinzugefügtes Element bereitstellt. Das Element ist nicht verfügbar und die Aktion wird nicht angewendet. Wenn ein ähnliches Listenelement mit derselben Klasse nach der Erstellung einer Aktivität dynamisch oder manuell hinzugefügt wird, wird ein neues Element an der ersten Position erstellt. Dadurch wird der Selektor gestoppt.

Bevor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

Nach (versucht):

```html
<div id="wrap">
     <ul class="nav">
        <li class="item"> Sale</li>
        <li> class="item"> Offers</li>
     </ul>
     <ul class="nav">
       <li class="men-section"> Men</li>
       <li class="women-section">Women</li>
    </ul>
</div>
```

## Szenario: Es wird ein Element nach dem ausgewählten Element eingefügt {#section_15B07B84BEE94ED39D85BBBE0733E170}

Bei diesem Szenario wird nach dem ausgewählten Element ein Listenelement eingefügt.

**Eingefügtes Element:**

```html
<ul class="nav"> 
   <li class="men-section"> Men Clothes</li> 
   <li class="women-section"> Women Clothes</li> 
</ul>
```

**Ausgewählt:**

`<li class="women-section">Women Shoes</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

In diesem Fall funktioniert das Einfügen einer Liste nach einer Liste, die mit dem ausgewählten Listenelement endet, wie erwartet. Das neue Element wird relativ zum übergeordneten Element an derselben Position wie das ausgewählte Element hinzugefügt.

Bevor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>       <li class="women">Women Shoes</li>
    </ul>
</div>
```

Nachher:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>
        <li class="women">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## Szenario: Das Element unmittelbar vor einem weiteren Element wird entfernt {#section_F193674F04F84AA593EAA1137C880EBA}

Bei diesem Szenario wird das Listenelement vor dem ausgewählten Element gelöscht.

**Entferntes Element:**

```html
<li class="men-section"> Men </li>
```

**Ausgewählt:**

`<li class="women-section">Women</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

Das Element wird erfolgreich entfernt, weil die Klasse des ausgewählten Elements nicht verändert wird.

Bevor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

Nachher:

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Szenario: Das Element unmittelbar nach einem anderen Element wird entfernt {#section_F83B51BE54924FB58679D512DAF1EBB2}

Bei diesem Szenario wird das Listenelement nach dem ausgewählten Element gelöscht.

**Entferntes Element:**

```html
<li class="kids-section">Kids</li>
```

**Ausgewählt:**

`<li class="women-section">Women</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

Das Element wird erfolgreich entfernt, weil die Klasse des ausgewählten Elements nicht verändert wird. Das entfernte Element enthält eine einzigartige Klasse innerhalb des übergeordneten Teilbaums.

Bevor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Women</li>
    </ul>
</div>
```

Nachher:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Szenario: Das ausgewählte Element wird entfernt {#section_1989CF1E2C344CC5963084ED83C18F9C}

Bei diesem Szenario wird das ausgewählte Listenelement entfernt.

**Entferntes Element:**

```html
<li class="women-shoes">Women</li>
```

**Ausgewählt:**

`<li class="women-shoes">Women</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

Das Element wurde erfolgreich entfernt.

Bevor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```

Nachher

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## Szenario: Die Klasse des ausgewählten Elements wird umbenannt   {#section_79D244C588BA452DB8E433D82B7F63EA}

Bei diesem Szenario wird die Klasse des ausgewählten Listenelements umbenannt.

**Geändertes Element:**

```html
<li class="women-section">Women</li>
```

**Ausgewählt:**

`<li class="women-section">Women</li>`

Selektor: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:**

Die Elementklasse kann nicht umbenannt werden, weil `class` nicht gefunden wurde.

Bevor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

Nach (versucht):

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```
