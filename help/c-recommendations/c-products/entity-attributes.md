---
keywords: entity;entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
description: Verwenden Sie Entitätsattribute, um Produkt- oder Inhaltsinformationen an Adobe Target Recommendations weiterzugeben.
title: Entitätsattribute
feature: entities
uuid: 27672881-a79c-4271-9a61-defddb9a5249
translation-type: tm+mt
source-git-commit: ed4f132dbf1ac8614f4aac8bd29b39b3dfbce2fe
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 90%

---


# ![PREMIUM](/help/assets/premium.png) Entitätsattribute{#entity-attributes}

Verwenden Sie Entitätsattribute, um Produkt- oder Inhaltsinformationen an  weiterzuleiten.

[!DNL Recommendations] sendet die `productId` oder `productPurchasedId` (`entity.id` im Code), die in den Algorithmen verwendet wird.

>[!NOTE]
>
>* `entity.id` muss mit der `productPurchasedId` an die Bestellbestätigungsseite gesendeten und der in Adobe Analytics-Produktberichten verwendeten `productId` übereinstimmen.
   >
   >
* Bereitgestellte Entitätsattributwerte laufen nach 61 Tagen ab. Dies bedeutet, dass Sie sicherstellen sollten, dass der neueste Wert jedes Entitätsattributs mindestens einmal pro Monat an Zielempfehlungen für jedes Element in Ihrem Katalog übergeben wird.


Von den meisten vorab definierten Parametern wird nur ein einzelner Wert akzeptiert, wobei neue Werte die alten überschreiben. Der `categoryId`-Parameter kann für jede Kategorie, in der das Produkt enthalten ist, eine kommagetrennte Liste mit Werten akzeptieren. Neue `categoryId`-Werte überschreiben die vorhandenen Werte nicht mehr, sondern werden bei einer Entitätsaktualisierung angehängt (Längenbeschränkung von 250 Zeichen).

Im Allgemeinen kann die Mbox mit den Anzeigeinformationen wie im folgenden Beispiel aussehen, wenn Sie at.js 1 verwenden.*x* mit `mboxCreate`.

>[!NOTE]
>
>* Wenn Sie at.js 2 verwenden.*x*, `mboxCreate` (wie im folgenden Beispiel verwendet) wird nicht mehr unterstützt. So geben Sie Produkt- oder Inhaltsinformationen mit at.js 2 an Recommendations weiter.*x*, verwenden Sie [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md). Ein Beispiel hierfür finden Sie unter Recommendations [planen und implementieren](/help/c-recommendations/plan-implement.md).

>



Bei allen Entitätsparameterattributen wird zwischen Groß- und Kleinschreibung unterschieden.

```
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=../baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=../baseball/giants-tix/giants-136px.gif', 
 
'entity.message=FAMILY SPECIAL', 
 
'entity.value=15.99', 
 
'entity.inventory=1' 
 
); 
 
</script>
```

>[!NOTE]
>
>Relative URLs werden für `pageUrl` und `thumbnailUrl` im Gegensatz zu absoluten URLs bevorzugt, da die Empfehlungen aus allen Umgebungen auf Ihrer Site Daten empfangen. Durch die Verwendung von relativen URLs werden fest codierte Links auf Staging- oder Entwicklungsserver vermieden.

Wenn sich die Mbox auf einer Produktseite befindet, können Sie sowohl die Produkt-ID als auch die Kategorie-ID aufnehmen. Der gewählte Algorithmus bestimmt, was angezeigt wird. Die Produkt-ID wird für Affinitätsalgorithmen und die Kategorie-ID für Kategoriealgorithmen verwendet.

## Verfügbare Variablen

Die folgende Liste beschreibt die verfügbaren Variablen.

### entity.id

Nur einzelner Wert.

Dieser erforderliche Parameter identifiziert das Produkt. Diese alphanumerische ID muss für alle [!DNL Adobe Experience Cloud] -Produkte gleich sein, einschließlich [!DNL Analytics], damit die verschiedenen Produkte das Element erkennen und Daten darüber austauschen.

`entity.id`-Werte dürfen keine Schrägstriche, Kaufmännisches-Und-Zeichen, Fragezeichen, Prozentsymbole, Kommas oder andere Satzzeichen enthalten, die eine URL-Kodierung erfordern, wenn sie in einem REST-API-Aufruf übergeben werden. Binde- und Unterstriche sind zulässig. Wenn in einem `entity.id`[!DNL Recommendations]-Wert ungültige Satzzeichen enthalten sind, schlagen manche fehl.

Beispiel: `'entity.id=67833'`

### entity.name

Nur einzelner Wert

Der Produktname, der auf der Site angezeigt wird, wenn das Produkt empfohlen wird.

Beispiel: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Mehrere Werte werden unterstützt (kommagetrennte Liste).

Kategorie der aktuellen Seite. Sie kann mehrere Kategorien umfassen, wie eine weitere Unterteilung in Strickjacken (d. h. Damen, Damen:Pullover, Damen:Pullover:Strickjacken). Mehrere Kategorien sollten durch Kommas abgetrennt werden.

`categoryId`ist auf 250 Zeichen begrenzt.

>[!NOTE]
>
>Um eine Empfehlung basierend auf einer Kategorie auf einer [!UICONTROL Kategorie]-Seite anzuzeigen, kann nur eine `categoryId` an die Mbox weitergegeben werden, die zur Anzeige dieser Empfehlung verwendet wird. Der Wert der `categoryId` muss exakt mit dem Wert von `entity.categoryId` übereinstimmen, der auf der Seite [!UICONTROL Produktdetails] übergeben wird.

Beispiele:

* Beispielseite mit Produktdetails: womens, womens:sweaters, womens:sweaters:cardigans
* Beispielseite für Kategorie „Sweater“: womens:sweaters
* Beispielseite für Kategorie „Cardigans“: womens:sweaters

Bei kategoriebasierten Empfehlungen wird ein Komma verwendet, um Kategoriewerte zu trennen. Alle durch Kommas getrennten Werte sind dann Kategorien. Sie können auch Unterkategorien mit einem anderen Trennzeichen, beispielsweise einem Doppelpunkt (:), definieren, um Unterkategorien innerhalb des Kategoriewerts zu trennen.

Im folgenden Code ist die Kategorie „Womens“ beispielsweise in mehrere Unterkategorien unterteilt:

```
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban’, 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Für die MBox-Bereitstellung wird der längste Attributname für den Schlüssel verwendet. Wenn eine Bindung vorhanden ist, wird das letzte Attribut verwendet. Im obigen Beispiel lautet der Kategorieschlüssel Womens:Outerwear:Jackets:Caban.

### entity.brand

Nur einzelner Wert

Zeigt den Markennamen eines Artikels an.

Beispiel: `'entity.brand=brandxyz'`

### entity.pageUrl

Nur einzelner Wert

Definiert die relative URL der Seite, auf der der Artikel zum Kauf angeboten wird.

Beispiel: `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'`

### entity.thumbnailUrl

Nur einzelner Wert

Definiert die relative URL zum Miniaturbild, das mit dem Artikel angezeigt wird.

Beispiel: `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'`

### entity.message

Nur einzelner Wert

Eine Botschaft zu dem in der Empfehlung angezeigten Produkt, wie zum Beispiel „Im Angebot“ oder „Ausverkauf“. Die Botschaft ist in der Regel ausführlicher als der Produktname. Kann zur Definition zusätzlicher Informationen zur Anzeige mit dem Produkt in der Vorlage verwendet werden.

Beispiel: `'entity.message=Family&nbsp;special'`

### entity.inventory

Nur einzelner Wert Erfordert eine Ganzzahl oder einen langen Wert.

Zeigt den Lagerbestand des Artikels.

Beispiel: `'entity.inventory=1'`

**Handhabung von leeren Lagerattributen:** Wenn Sie für die Bereitstellung eine Einschlussregel, eine Sammlungsregel oder eine Kriterieneinstellung mit `entity.inventory`„> 0“ oder `entity.inventory`„= 0“ festlegen und das Produkt den Bestand nicht enthält, [!DNL Target] wird dies auf TRUE gesetzt und enthält Produkte, bei denen der Bestand nicht eingestellt ist. Dies geschieht standardmäßig, damit auch Produkte, deren Inventar nicht festgelegt ist, in Empfehlungsergebnissen angezeigt werden.

Wenn Sie eine globale Ausschlussregel mit `entity.inventory` = 0 und `entity.inventory` nicht festgelegt haben, wird diese Regel von [!DNL Target] auf TRUE gesetzt und das Produkt ausgeschlossen.

**Bekanntes Problem:** Die Produktsuche ist nicht mit der Bereitstellung für nicht festgelegte Bestandswertattribute konsistent. Bei einer Regel mit `entity.inventory` = 0 zeigt die Produktsuche keine Produkte an, bei denen der Bestandswert nicht festgelegt ist.

### entity.value

Nur einzelner Wert

Definiert den Preis oder Wert des Artikels.

Beispiel: `'entity.value=15.99'`

### entity.margin

Nur einzelner Wert

Die Gewinnspanne oder ein anderer Wert des Artikels.

Beispiel: `'entity.margin=1.00'`

### entity.*custom*

Mehrere Werte werden unterstützt (JSON-Array).

Definieren Sie bis zu 100 benutzerspezifische Variablen, um weitere Informationen zum Artikel bereitzustellen. Sie können jeden nicht bereits in Gebrauch befindlichen Attributnamen für die benutzerspezifischen Attribute verwenden. Möglicherweise möchten Sie ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` erstellen, um damit ein Buch oder einen Film zu kategorisieren. Oder ein Ticketverkäufer kann Attribute zur Halle einrichten, um über einen zusätzlichen Auftritt, z. B. ein weiteres Team, das bei einer Sportveranstaltung mitwirkt, oder die Vorgruppe bei einem Konzert, zu informieren.

Einschränkungen:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden.
* Das Attribut entity.environment ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, entity.environment mit targetPageParams, Feed oder API zu übermitteln, werden ignoriert.

Beispiele:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Benutzerdefinierte Entitätsattribute unterstützen mehrere Werte. Siehe [Benutzerdefinierte Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) für Zeichen- und Wertbeschränkungen.

Beispiel: `'entity.secondary=["band1",&nbsp;"band2"]'`

>[!NOTE]
>
>Benutzerdefinierte Entitätsattribute mit mehreren Werten erfordern gültige JSON-Arrays. Informationen zu korrekten Syntaxinformationen finden Sie unter „Benutzerdefinierte Entitätsattribute“.

### entity.event.detailsOnly

Nur einzelner Wert

Wird dazu verwendet zu verhindern, dass durch einen Mbox-Aufruf der Zähler für Verhaltensdaten eines Algorithmus ansteigt.

Beispiel: `'entity.event.detailsOnly=true'`

In den unten gezeigten Beispielen werden Katalog- und Verhaltensdaten mit dem Mbox-Aufruf aktualisiert. Mit dem zweiten Mbox-Aufruf wird lediglich der Katalog aktualisiert.

```
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

## Verwandte Themen:

* [Benutzerdefinierte Entitätsattribute](../../c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
