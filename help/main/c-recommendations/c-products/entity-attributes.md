---
keywords: Entität Entitätsattribute; Weiterleiten von Informationen an Recommendations; Verhaltensdaten; Datenzähler; relative URL definieren; Lagerbestandsebene anzeigen; Preis festlegen; Festlegen der Gewinnspanne; benutzerdefinierte Attribute
description: Erfahren Sie, wie Sie Entitätsattribute verwenden, um Produkt- oder Inhaltsinformationen an  [!DNL Target] Recommendations zu übergeben.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
title: Wie verwende ich Entitätsattribute?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
source-git-commit: b6697eee5925cb8fa3b2fa2e107af0c617d30f94
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 48%

---

# Entitätsattribute

Verwenden Sie Entitätsattribute, um Produkt- oder Inhaltsinformationen an [!DNL Adobe Target Recommendations] zu übergeben.

Entitäten beziehen sich auf die Artikel, die Sie empfehlen möchten. Entitäten können Produkte, Inhalte (Artikel, Slideshows, Bilder, Filme und Fernsehsendungen), Stellenausschreibungen, Restaurants und so weiter umfassen.

[!DNL Recommendations] sendet die `productId` oder `productPurchasedId` (im Code als `entity.id` bezeichnet), die in den Algorithmen verwendet werden.

Beachten Sie Folgendes:

* `entity.id` muss mit den `productPurchasedId` übereinstimmen, die an die Bestellbestätigungsseite gesendet wurden, sowie mit den in [!DNL Adobe Analytics] Produktberichten verwendeten `productId`.
* Entitätsattributwerte, die Sie an übergeben, laufen [!DNL Recommendations] nach 61 Tagen ab. Adobe empfiehlt, für jedes Element im Katalog den neuesten Wert jedes Entitätsattributs mindestens einmal pro Monat an [!DNL Recommendations] zu übergeben.

Die meisten vordefinierten Parameter akzeptieren nur einen einzigen Wert, wobei neue Werte alte Werte überschreiben. Der `categoryId`-Parameter kann für jede Kategorie, in der das Produkt enthalten ist, eine kommagetrennte Liste mit Werten akzeptieren. Neue `categoryId`-Werte überschreiben die vorhandenen Werte nicht mehr, sondern werden bei einer Entitätsaktualisierung angehängt (Längenbeschränkung von 250 Zeichen).

Im Allgemeinen sieht die mBox „Display Information“ wie im folgenden Beispiel aus, wenn Sie at.js 1 verwenden.*x* mit `mboxCreate`. Bei allen Entitätsparameterattributen wird zwischen Groß- und Kleinschreibung unterschieden.

>[!NOTE]
>
>Wenn Sie at.js 2.*x*, `mboxCreate` (wie im folgenden Beispiel verwendet) wird nicht mehr unterstützt. So übergeben Sie Produkt- oder Inhaltsinformationen mithilfe von at.js 2 an [!DNL Recommendations].*x*, verwenden Sie [targetPageParams](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html?lang=de){target=_blank}. Ein Beispiel finden Sie unter [Recommendations planen und implementieren](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=de){target=_blank}.

```javascript
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=/help/baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=/help/baseball/giants-tix/giants-136px.gif', 
 
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

Die `entity.id` dürfen *keine* Leerzeichen, Schrägstriche, kaufmännische Und-Zeichen, Fragezeichen, Prozentzeichen, Kommas oder andere Satzzeichen enthalten, für die eine URL-Codierung erforderlich ist, wenn sie in einem REST-API-Aufruf übergeben wird. Bindestriche und Unterstriche sind zulässig. Wenn in einem `entity.id`[!DNL Recommendations]-Wert ungültige Satzzeichen enthalten sind, schlagen manche fehl.

Beispiel: `'entity.id=67833'`

### entity.name

Nur einzelner Wert

Der Produktname, der auf der Site angezeigt wird, wenn das Produkt empfohlen wird.

Beispiel: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Mehrere Werte werden unterstützt (kommagetrennte Liste).

Kategorie der aktuellen Seite. Die entity.categoryID kann mehrere Kategorien enthalten, z. B. einen Unterabschnitt „Cardigans“ (z. B. `womens`, `womens:sweaters`, `womens:sweaters:cardigans`). Mehrere Kategorien müssen durch Kommas getrennt werden.

Der `categoryId` ist auf 250 Zeichen begrenzt.

>[!NOTE]
>
>Um eine Empfehlung basierend auf einer Kategorie auf einer [!UICONTROL Category] anzuzeigen, kann nur ein `categoryId` an die Mbox übergeben werden, die zur Anzeige dieser bestimmten Empfehlung verwendet wird. Der Wert des `categoryId` muss genau mit dem Wert des `entity.categoryId` übereinstimmen, der auf der [!UICONTROL Product Detail] übergeben wird.

Beispiele:

* Beispiel für eine Produktdetailseite: `womens`, `womens:sweaters`, `womens:sweaters:cardigans`
* Beispiel Kategorie Seite Pullover: `womens:sweaters`
* Beispiel für Kategorieseiten-Strickjacken: `womens:sweaters:cardigans`

Bei kategoriebasierten Empfehlungen wird der Kategoriewert durch ein Komma getrennt. Alle durch Kommas getrennten Werte sind dann Kategorien. Sie können auch Unterkategorien mit einem anderen Trennzeichen, beispielsweise einem Doppelpunkt (:), definieren, um Unterkategorien innerhalb des Kategoriewerts zu trennen.

Im folgenden Code ist die Kategorie „Damen“ beispielsweise in mehrere Unterkategorien unterteilt:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Für die MBox-Bereitstellung wird der längste Attributname für den Schlüssel verwendet. Wenn eine Bindung vorhanden ist, wird das letzte Attribut verwendet. Im obigen Beispiel wird der Kategorieschlüssel `Womens:Outerwear:Jackets:Caban`.

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

Eine Botschaft zu dem in der Empfehlung angezeigten Produkt, wie zum Beispiel „Im Angebot“ oder „Ausverkauf“. Die Botschaft ist in der Regel ausführlicher als der Produktname. Verwenden Sie entity.message, um zusätzliche Informationen zu definieren, die mit dem Produkt in der Vorlage angezeigt werden.

Beispiel: `'entity.message=Family&nbsp;special'`

### entity.inventory

Nur einzelner Wert Erfordert eine Ganzzahl oder einen langen Wert.

Zeigt den Lagerbestand des Artikels.

Beispiel: `'entity.inventory=1'`

**Leere Handhabung von Lagerattributen:** Wenn Sie für den Versand eine Einschlussregel, eine Erfassungsregel oder eine Kriterieneinstellung mit `entity.inventory` > 0 oder `entity.inventory` = 0 haben und das Produkt keinen Bestand hat, bewertet [!DNL Target] diesen Wert als „TRUE“ und schließt Produkte ein, für die der Bestand nicht festgelegt ist. Daher werden Produkte mit einem nicht festgelegten Inventar in den Empfehlungsergebnissen angezeigt.

Wenn Sie eine globale Ausschlussregel mit `entity.inventory` = 0 und `entity.inventory` nicht festgelegt haben, wird diese Regel von [!DNL Target] auf TRUE gesetzt und das Produkt ausgeschlossen.

**Bekanntes Problem** Die Produktsuche stimmt nicht mit dem Versand überein, wenn keine Inventarwertattribute festgelegt sind. Beispiel: Für eine Regel mit `entity.inventory` = 0 zeigt die Produktsuche keine Produkte an, für die der Inventarwert nicht festgelegt ist.

### entity.value

Nur einzelner Wert

Definiert den Preis oder Wert des Artikels.

Beispiel: `'entity.value=15.99'`

entity.value unterstützt nur das Dezimalformat (z. B. 15.99). Das Kommaformat (15,99) wird nicht unterstützt.

### entity.margin

Nur einzelner Wert

Die Gewinnspanne oder ein anderer Wert des Artikels.

Beispiel: `'entity.margin=1.00'`

### Entität.*custom*

Mehrere Werte werden unterstützt (JSON-Array).

Definieren Sie bis zu 100 benutzerspezifische Variablen, um weitere Informationen zum Artikel bereitzustellen. Sie können jeden nicht bereits in Gebrauch befindlichen Attributnamen für die benutzerspezifischen Attribute verwenden. Sie können beispielsweise ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` erstellen, um ein Buch oder einen Film zu definieren. Ein Ticketverkäufer kann Attribute für einen Veranstaltungsort für einen sekundären Darsteller erstellen, z. B. ein Gastteam bei einem Sportereignis oder einen Eröffnungsakt in einem Konzert.

Einschränkungen:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden.
* Das Attribut entity.environment ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, entity.environment mithilfe von targetPageParams, Feed oder API zu übergeben, werden ignoriert.

Beispiele:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Benutzerdefinierte Entitätsattribute unterstützen mehrere Werte. Siehe [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) für Zeichen- und Wertbeschränkungen.

Beispiel: `'entity.secondary=["band1",&nbsp;"band2"]'`

Benutzerdefinierte Entitätsattribute mit mehreren Werten erfordern gültige JSON-Arrays. Die richtigen Syntaxinformationen finden Sie unter [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly

Nur einzelner Wert

Wird dazu verwendet zu verhindern, dass durch einen Mbox-Aufruf der Zähler für Verhaltensdaten eines Algorithmus ansteigt.

Beispiel: `'entity.event.detailsOnly=true'`

In den folgenden Beispielen werden die Katalog- und Verhaltensdaten durch den ersten Mbox-Aufruf aktualisiert. Mit dem zweiten Mbox-Aufruf wird nur der Katalog aktualisiert.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

>[!MORELIKETHIS]
>
>* [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
