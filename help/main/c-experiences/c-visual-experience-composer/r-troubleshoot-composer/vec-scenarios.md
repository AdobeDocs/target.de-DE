---
keywords: Recommendations
description: Erfahren Sie mehr über gängige Szenarien, die zeigen, wie Änderungen an Ihrer Seite in Visual Experience Composer (VEC) die Anzeige eines Erlebnisses in Adobe Target beeinträchtigen.
title: Was sind einige gängige Szenarien für die Seitenmodifizierung?
feature: Visual Experience Composer (VEC)
exl-id: 7a05fbf9-3427-436e-a54f-4f1dd16d885a
TQID: 'https://experienceleague.adobe.com/BI2SnUU5ilCf0auld15q1rpCrnLoPEwbe1fZO6G1quc'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 4%
---
# Szenarien für die Seitenmodifizierung {#vec-scenarios}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie anhand von sieben Szenarien mit Beispielen, wie Änderungen an einer Seite außerhalb von [!DNL Target] die Anzeige eines Erlebnisses durch [!DNL Target] beeinflussen.

>[!ENDSHADEBOX]

Der [!DNL Target]-Selektor bestimmt, wo ein Erlebnis angezeigt wird. Wenn eine Seite außerhalb von [!DNL Target] geändert wird, können sich die Änderungen auf die Fähigkeit von [!DNL Target] auswirken, diesen Speicherort zu finden und das Erlebnis anzuzeigen.

Der Selektor funktioniert immer mit einer eindeutigen Klasse, die keiner ID entspricht. Wenn dem Element keine Klasse zugewiesen ist, zählt der Selektor die vorherigen gleichrangigen Elemente mit demselben Tag-Namen.

>[!NOTE]
>
>In den Szenarien werden Listenelemente als Beispiele verwendet, die Konzepte gelten jedoch für alle Elemente.

In der folgenden Tabelle sind die Szenarien zusammengefasst. In jedem Szenario wird der Selektor `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`.

| Szenario | Angewendete Aktion | Grund |
|---|---|---|
| Ein Element mit einem anderen Klassennamen vor dem ausgewählten Element einfügen | Ja | `li.women-section:eq(0)` ist nicht betroffen |
| Element mit demselben Klassennamen wie das ausgewählte Element einfügen | Nein | Ein neues Element nimmt die erste Position ein, wodurch der Selektor unterbrochen wird |
| Element nach dem ausgewählten Element einfügen | Ja | Das neue Element wird an derselben Position relativ zum übergeordneten Element hinzugefügt |
| Element unmittelbar vor dem ausgewählten Element entfernen | Ja | Die Klasse des ausgewählten Elements wird nicht geändert |
| Das Element unmittelbar nach dem ausgewählten Element entfernen | Ja | Die Klasse des ausgewählten Elements wird nicht geändert |
| Ausgewähltes Element entfernen | Ja | Das Element wurde erfolgreich entfernt |
| Klasse des ausgewählten Elements umbenennen | Nein | `class` wurde nicht gefunden |

## Ein Element mit einem anderen Klassennamen vor dem ausgewählten Element einfügen

Ein neues Element wird als gleichrangiges Element des Elements im [!DNL Target] eingefügt. Wenn die erste Klasse für das Element von JavaScript hinzugefügt wurde, schlägt der Versand fehl und die Aktion wird nicht angewendet.

**Eingefügtes Element:**

```html
<li class="kids-section">Kids</li>
```

**Ausgewähltes Element:**

`<li class="women-section">Women</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis** Der Selektor funktioniert erwartungsgemäß, da `li.women-section:eq(0)` nicht betroffen ist.

**before:**

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul>
</div>
```

**after:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

## Element mit demselben Klassennamen wie das ausgewählte Element einfügen

Eine Liste wird eingefügt, während ein Element einer Liste ausgewählt wird.

**Eingefügtes Element:**

```html
<ul class="nav">
   <li class="item"> Sale </li>
   <li class="item"> Offers </li>
</ul>
```

**Ausgewähltes Element:**

`<li class="women-section">Women</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:** Der Selektor funktioniert nicht. `ul.nav:eq(0)` verweist nun auf ein dynamisch hinzugefügtes Element, das nicht verfügbar ist, sodass die Aktion nicht angewendet wird. Wenn nach dem Erstellen der Aktivität ein ähnliches Listenelement dynamisch oder manuell mit derselben Klasse hinzugefügt wird, wird ein neues Element an die erste Position verschoben, wodurch der Selektor unterbrochen wird.

**before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

**Nach (versucht):**

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

## Element nach dem ausgewählten Element einfügen

Nach dem ausgewählten Listenelement wird eine Liste eingefügt.

**Eingefügtes Element:**

```html
<ul class="nav">
   <li class="men-section"> Men Clothes</li>
   <li class="women-section"> Women Clothes</li>
</ul>
```

**Ausgewähltes Element:**

`<li class="women-section">Women Shoes</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis** Das Einfügen einer Liste nach der Liste, die mit dem ausgewählten Element endet, funktioniert erwartungsgemäß. Das neue Element wird an derselben Position hinzugefügt wie das ausgewählte Element relativ zum übergeordneten Element.

**before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>       <li class="women-section">Women Shoes</li>
    </ul>
</div>
```

**after:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>
        <li class="women-section">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## Element unmittelbar vor dem ausgewählten Element entfernen

Das Listenelement, bevor das ausgewählte Element gelöscht wird.

**Entferntes Element:**

```html
<li class="men-section"> Men </li>
```

**Ausgewähltes Element:**

`<li class="women-section">Women</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** Das Element wurde erfolgreich entfernt, da die Klasse des ausgewählten Elements nicht geändert wird.

**before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**after:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Das Element unmittelbar nach dem ausgewählten Element entfernen

Das Listenelement, nachdem das ausgewählte Element gelöscht wurde.

**Entferntes Element:**

```html
<li class="kids-section">Kids</li>
```

**Ausgewähltes Element:**

`<li class="women-section">Women</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** Das Element wurde erfolgreich entfernt, da die Klasse des ausgewählten Elements nicht geändert wird und das entfernte Element eine eindeutige Klasse innerhalb seiner übergeordneten Unterstruktur hat.

**before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Kids</li>
    </ul>
</div>
```

**after:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Ausgewähltes Element entfernen

Das ausgewählte Listenelement wird gelöscht.

**Entferntes Element:**

```html
<li class="women-section">Women</li>
```

**Ausgewähltes Element:**

`<li class="women-section">Women</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Ergebnis:** Das Element wurde erfolgreich entfernt.

**before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**after:**

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## Klasse des ausgewählten Elements umbenennen

Die Klasse des ausgewählten Listenelements wird geändert.

**Geändertes Element:**

```html
<li class="women-section">Women</li>
```

**Ausgewähltes Element:**

`<li class="women-section">Women</li>`

**selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** Die Klasse kann nicht umbenannt werden, da `class` nicht gefunden wurde.

**before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**Nach (versucht):**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div> 
```
