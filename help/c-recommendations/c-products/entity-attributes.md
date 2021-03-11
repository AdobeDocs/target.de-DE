---
keywords: Entität Entitätsattribute; Weiterleiten von Informationen an Recommendations; Verhaltensdaten; Datenzähler; relative URL definieren; Lagerbestandsebene anzeigen; Preis festlegen; Festlegen der Gewinnspanne; benutzerdefinierte Attribute
description: Erfahren Sie, wie Sie Entitätsattribute verwenden, um Produkt- oder Inhaltsinformationen an Zielgruppe Recommendations zu übermitteln.
title: Wie verwende ich Entitätsattribute?
feature: Recommendations
translation-type: tm+mt
source-git-commit: 9f844f6a6fb1d0da6790706e7a49130d69e779d9
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 57%

---


# ![PREMIUM](/help/assets/premium.png) Entitätsattribute

Verwenden Sie Entitätsattribute, um Produkt- oder Inhaltsinformationen an [!DNL Adobe Target Recommendations] weiterzugeben.

Entitäten beziehen sich auf die Artikel, die Sie empfehlen möchten. Entitäten können Produkte, Inhalte (Artikel, Diashows, Bilder, Filme und Fernsehsendungen), Stellenangebote, Restaurants usw. umfassen.

[!DNL Recommendations] sendet die `productId` oder `productPurchasedId` (`entity.id` im Code), die in den Algorithmen verwendet wird.

Beachten Sie Folgendes:

* `entity.id` muss mit der  `productPurchasedId` gesendeten Bestellbestätigungsseite und der  `productId` in  [!DNL Adobe Analytics] Produktberichten verwendeten übereinstimmen.
* An [!DNL Recommendations] übergebene Entitätsattributwerte laufen nach 61 Tagen ab. Adobe empfiehlt, den neuesten Wert jedes Entitätsattributs mindestens einmal pro Monat an [!DNL Recommendations] für jedes Element in Ihrem Katalog zu übergeben.

Die meisten vordefinierten Parameter akzeptieren nur einen einzelnen Wert, wobei neue Werte alte Werte überschreiben. Der `categoryId`-Parameter kann für jede Kategorie, in der das Produkt enthalten ist, eine kommagetrennte Liste mit Werten akzeptieren. Neue `categoryId`-Werte überschreiben die vorhandenen Werte nicht mehr, sondern werden bei einer Entitätsaktualisierung angehängt (Längenbeschränkung von 250 Zeichen).

Im Allgemeinen sieht die Mbox mit den Anzeigeinformationen wie im folgenden Beispiel aus, wenn Sie at.js 1 verwenden.*xwith*  `mboxCreate`. Bei allen Entitätsparameterattributen wird die Groß-/Kleinschreibung beachtet.

>[!NOTE]
>
>Wenn Sie at.js 2 verwenden.*x*,  `mboxCreate` (wie im folgenden Beispiel verwendet) wird nicht mehr unterstützt. So geben Sie Produkt- oder Inhaltsinformationen mit at.js 2 an [!DNL Recommendations] weiter.*x*, verwenden Sie  [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md). Ein Beispiel finden Sie unter [Planen und Implementieren von Recommendations](/help/c-recommendations/plan-implement.md).

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

Die Werte für `entity.id` dürfen keine Zeichen für Schrägstriche, Umrandungen, Fragezeichen, Prozentzeichen, Kommas oder andere Interpunktionszeichen enthalten, die bei der Übergabe eines REST-API-Aufrufs eine URL-Kodierung erfordern. ** Bindestriche und Unterstriche sind zulässig. Wenn in einem `entity.id`[!DNL Recommendations]-Wert ungültige Satzzeichen enthalten sind, schlagen manche fehl.

Beispiel: `'entity.id=67833'`

### entity.name

Nur einzelner Wert

Der Produktname, der auf der Site angezeigt wird, wenn das Produkt empfohlen wird.

Beispiel: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Mehrere Werte werden unterstützt (kommagetrennte Liste).

Kategorie der aktuellen Seite. Die entity.categoryID kann mehrere Kategorien enthalten, z. B. einen Unterabschnitt &quot;Strickjacken&quot;(z. B. Damen, Damen:Pullover, Damen:Pullover:Strickjacken). Mehrere Kategorien müssen durch Kommas getrennt werden.

Der Wert `categoryId` ist auf 250 Zeichen begrenzt.

>[!NOTE]
>
>Um eine Empfehlung basierend auf einer Kategorie auf einer [!UICONTROL Kategorie]-Seite anzuzeigen, kann nur eine `categoryId` an die Mbox weitergegeben werden, die zur Anzeige dieser Empfehlung verwendet wird. Der Wert der `categoryId` muss exakt mit dem Wert von `entity.categoryId` übereinstimmen, der auf der Seite [!UICONTROL Produktdetails] übergeben wird.

Beispiele:

* Beispielseite mit Produktdetails: womens, womens:sweaters, womens:sweaters:cardigans
* Beispielseite für Kategorie „Sweater“: womens:sweaters
* Beispielseite für Kategorie „Cardigans“: womens:sweaters

Bei Kategorien-basierten Empfehlungen wird der Wert der Kategorie durch ein Komma getrennt. Alle durch Kommas getrennten Werte sind dann Kategorien. Sie können auch Unterkategorien mit einem anderen Trennzeichen, beispielsweise einem Doppelpunkt (:), definieren, um Unterkategorien innerhalb des Kategoriewerts zu trennen.

Im folgenden Code wird die Kategorie der Frau beispielsweise in mehrere Unterkategorien unterteilt:

```javascript
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

Eine Botschaft zu dem in der Empfehlung angezeigten Produkt, wie zum Beispiel „Im Angebot“ oder „Ausverkauf“. Die Botschaft ist in der Regel ausführlicher als der Produktname. Verwenden Sie entity.message, um zusätzliche Informationen zu definieren, die zusammen mit dem Produkt in der Vorlage angezeigt werden sollen.

Beispiel: `'entity.message=Family&nbsp;special'`

### entity.inventory

Nur einzelner Wert Erfordert eine Ganzzahl oder einen langen Wert.

Zeigt den Lagerbestand des Artikels.

Beispiel: `'entity.inventory=1'`

**Handhabung von leeren Lagerbestandsattributen:** Wenn Sie zum Versand eine Einschlussregel, eine Erfassungsregel oder eine Kriterieneinstellung mit  `entity.inventory` > 0 oder  `entity.inventory` = 0 haben und das Produkt keinen Bestand eingestellt hat, wird dieser Wert mit TRUE  [!DNL Target] ausgewertet und umfasst Produkte, bei denen der Bestand nicht eingestellt ist. Aus diesem Grund werden Produkte mit nicht eingestelltem Bestand in den Empfehlungsergebnissen angezeigt.

Wenn Sie eine globale Ausschlussregel mit `entity.inventory` = 0 und `entity.inventory` nicht festgelegt haben, wird diese Regel von [!DNL Target] auf TRUE gesetzt und das Produkt ausgeschlossen.

**Bekanntes Problem: Die** Produktsuche stimmt nicht mit dem Versand für nicht eingestellte Lagerwertattribute überein. Beispielsweise zeigt die Produktsuche bei einer Regel mit `entity.inventory` = 0 keine Produkte an, bei denen der Bestandserhaltungswert nicht eingestellt ist.

### entity.value

Nur einzelner Wert

Definiert den Preis oder Wert des Artikels.

Beispiel: `'entity.value=15.99'`

entity.value unterstützt nur das Dezimalformat (z. B. 15.99). Das Komma-Format (15,99) wird nicht unterstützt.

### entity.margin

Nur einzelner Wert

Die Gewinnspanne oder ein anderer Wert des Artikels.

Beispiel: `'entity.margin=1.00'`

### entity.*custom*

Mehrere Werte werden unterstützt (JSON-Array).

Definieren Sie bis zu 100 benutzerspezifische Variablen, um weitere Informationen zum Artikel bereitzustellen. Sie können jeden nicht bereits in Gebrauch befindlichen Attributnamen für die benutzerspezifischen Attribute verwenden. Sie können beispielsweise ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` erstellen, um ein Buch oder einen Film zu definieren. Ein Ticketverkäufer kann Attribute für einen Veranstaltungsort eines Ereignisses für einen Sekundärdarsteller erstellen, z. B. ein Besuchsteam in einem Ereignis oder eine Eröffnungsveranstaltung in einem Konzert.

Einschränkungen:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden.
* Das Attribut entity.environment ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, entity.Umgebung mit targetPageParams, Feed oder API zu übergeben, werden ignoriert.

Beispiele:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Benutzerdefinierte Entitätsattribute unterstützen mehrere Werte. Siehe [Benutzerdefinierte Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) für Zeichen- und Wertbeschränkungen.

Beispiel: `'entity.secondary=["band1",&nbsp;"band2"]'`

Benutzerdefinierte Entitätsattribute mit mehreren Werten erfordern gültige JSON-Arrays. Die richtigen Syntaxinformationen finden Sie unter [Benutzerspezifische Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly

Nur einzelner Wert

Wird dazu verwendet zu verhindern, dass durch einen Mbox-Aufruf der Zähler für Verhaltensdaten eines Algorithmus ansteigt.

Beispiel: `'entity.event.detailsOnly=true'`

In den unten stehenden Beispielen werden Katalog- und Verhaltensdaten mit dem ersten Mbox-Aufruf aktualisiert. Beim zweiten Mbox-Aufruf wird nur der Katalog aktualisiert.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

>[!MORELIKETHIS]
>
>* [Benutzerdefinierte Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)

