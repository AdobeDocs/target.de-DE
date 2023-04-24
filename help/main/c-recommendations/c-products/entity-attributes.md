---
keywords: Entität Entitätsattribute; Weiterleiten von Informationen an Recommendations; Verhaltensdaten; Datenzähler; relative URL definieren; Lagerbestandsebene anzeigen; Preis festlegen; Festlegen der Gewinnspanne; benutzerdefinierte Attribute
description: Erfahren Sie, wie Sie mithilfe von Entitätsattributen Produkt- oder Inhaltsinformationen an weitergeben können. [!DNL Target] Recommendations.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
title: Wie verwende ich Entitätsattribute?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
source-git-commit: 2a25fdb42ce4470f9126b7e0e7f6fd9e60c350e5
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 54%

---

# Entitätsattribute

Verwenden Sie Entitätsattribute, um Produkt- oder Inhaltsinformationen an [!DNL Adobe Target Recommendations].

Entitäten beziehen sich auf die Artikel, die Sie empfehlen möchten. Entitäten können Produkte, Inhalte (Artikel, Diashows, Bilder, Filme und Fernsehsendungen), Stellenausschreibungen, Restaurants usw. umfassen.

[!DNL Recommendations] sendet die `productId` oder `productPurchasedId` (`entity.id` im Code), die in den Algorithmen verwendet wird.

Beachten Sie Folgendes:

* `entity.id` muss mit dem `productPurchasedId` an die Bestellbestätigungsseite gesendet werden und die `productId` verwendet in [!DNL Adobe Analytics] Produktberichte.
* Entitätsattributwerte, an die Sie übergeben [!DNL Recommendations] nach 61 Tagen ablaufen. Adobe empfiehlt, den neuesten Wert jedes Entitätsattributs an [!DNL Recommendations] mindestens einmal pro Monat für jeden Artikel in Ihrem Katalog.

Die meisten vordefinierten Parameter akzeptieren nur einen einzigen Wert, wobei neue Werte alte Werte überschreiben. Der `categoryId`-Parameter kann für jede Kategorie, in der das Produkt enthalten ist, eine kommagetrennte Liste mit Werten akzeptieren. Neue `categoryId`-Werte überschreiben die vorhandenen Werte nicht mehr, sondern werden bei einer Entitätsaktualisierung angehängt (Längenbeschränkung von 250 Zeichen).

Im Allgemeinen sieht die Mbox mit den Anzeigeinformationen wie im folgenden Beispiel aus, wenn Sie at.js 1 verwenden.*x* mit `mboxCreate`. Bei allen Entitätsparameterattributen wird zwischen Groß- und Kleinschreibung unterschieden.

>[!NOTE]
>
>Wenn Sie at.js 2.*x*, `mboxCreate` (wie im folgenden Beispiel verwendet) wird nicht mehr unterstützt. So übergeben Sie Produkt- oder Inhaltsinformationen an [!DNL Recommendations] Verwendung von at.js 2.*x*, verwenden [targetPageParams](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html){target=_blank}. For an example, see [Plan and implement Recommendations](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

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

Die `entity.id` Werte müssen *not* enthält Schrägstriche, Und-Zeichen, Fragezeichen, Prozentsymbole, Kommas oder andere Satzzeichen, die bei der Übergabe in einen REST-API-Aufruf eine URL-Codierung erfordern. Bindestriche und Unterstriche sind zulässig. Wenn in einem `entity.id`[!DNL Recommendations]-Wert ungültige Satzzeichen enthalten sind, schlagen manche fehl.

Beispiel: `'entity.id=67833'`

### entity.name

Nur einzelner Wert

Der Produktname, der auf der Site angezeigt wird, wenn das Produkt empfohlen wird.

Beispiel: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Mehrere Werte werden unterstützt (kommagetrennte Liste).

Kategorie der aktuellen Seite. Die entity.categoryID kann mehrere Kategorien enthalten, z. B. einen Unterabschnitt für Strickjacken (z. B. Damen, Damen:Pullover, Damen).:sweaters:Kardigans). Mehrere Kategorien müssen durch Kommas getrennt werden.

Die `categoryId` -Wert auf 250 Zeichen begrenzt ist.

>[!NOTE]
>
>Um eine Empfehlung basierend auf einer Kategorie auf einer [!UICONTROL Kategorie]-Seite anzuzeigen, kann nur eine `categoryId` an die Mbox weitergegeben werden, die zur Anzeige dieser Empfehlung verwendet wird. Der Wert der `categoryId` muss exakt mit dem Wert von `entity.categoryId` übereinstimmen, der auf der Seite [!UICONTROL Produktdetails] übergeben wird.

Beispiele:

* Beispiel für eine Produktdetailseite: Damen, Damen:Pullover, Damen:sweaters:Kardigans
* Beispielseite für Kategorie „Sweater“: womens:sweaters
* Beispiel für Kategorieseiten-Cardigans: Damen:sweaters:Kardigans

Bei kategoriebasierten Empfehlungen wird der Kategoriewert durch ein Komma getrennt. Alle durch Kommas getrennten Werte sind dann Kategorien. Sie können auch Unterkategorien mit einem anderen Trennzeichen, beispielsweise einem Doppelpunkt (:), definieren, um Unterkategorien innerhalb des Kategoriewerts zu trennen.

Im folgenden Code wird beispielsweise die Kategorie &quot;Frauen&quot;in mehrere Unterkategorien unterteilt:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Für die MBox-Bereitstellung wird der längste Attributname für den Schlüssel verwendet. Wenn eine Bindung vorhanden ist, wird das letzte Attribut verwendet. Im obigen Beispiel lautet der Kategorieschlüssel Womens .:Outerwear:Jacken: Caban.

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

Eine Botschaft zu dem in der Empfehlung angezeigten Produkt, wie zum Beispiel „Im Angebot“ oder „Ausverkauf“. Die Botschaft ist in der Regel ausführlicher als der Produktname. Verwenden Sie entity.message , um zusätzliche Informationen zu definieren, die mit dem Produkt in der Vorlage angezeigt werden.

Beispiel: `'entity.message=Family&nbsp;special'`

### entity.inventory

Nur einzelner Wert Erfordert eine Ganzzahl oder einen langen Wert.

Zeigt den Lagerbestand des Artikels.

Beispiel: `'entity.inventory=1'`

**Umgang mit leeren Inventarattributen:** Für die Bereitstellung, wenn Sie über eine Einschlussregel, Sammlungsregel oder Kriterieneinstellung mit `entity.inventory` > 0 oder `entity.inventory` = 0 und der Lagerbestand des Produkts nicht festgelegt ist, [!DNL Target] bewertet diesen Wert mit TRUE und schließt Produkte ein, bei denen das Inventar nicht festgelegt ist. Daher werden Produkte mit nicht festgelegtem Inventar in Empfehlungsergebnissen angezeigt.

Wenn Sie eine globale Ausschlussregel mit `entity.inventory` = 0 und `entity.inventory` nicht festgelegt haben, wird diese Regel von [!DNL Target] auf TRUE gesetzt und das Produkt ausgeschlossen.

**Bekanntes Problem:** Die Produktsuche ist nicht mit der Bereitstellung für Inventarwertattribute konsistent, die nicht festgelegt sind. Beispiel: für eine Regel mit `entity.inventory` = 0 , zeigt die Produktsuche keine Produkte an, bei denen der Bestandswert nicht festgelegt ist.

### entity.value

Nur einzelner Wert

Definiert den Preis oder Wert des Artikels.

Beispiel: `'entity.value=15.99'`

entity.value unterstützt nur das Dezimalformat (z. B. 15.99). Das Kommaformat (15,99) wird nicht unterstützt.

### entity.margin

Nur einzelner Wert

Die Gewinnspanne oder ein anderer Wert des Artikels.

Beispiel: `'entity.margin=1.00'`

### entity.*custom*

Mehrere Werte werden unterstützt (JSON-Array).

Definieren Sie bis zu 100 benutzerspezifische Variablen, um weitere Informationen zum Artikel bereitzustellen. Sie können jeden nicht bereits in Gebrauch befindlichen Attributnamen für die benutzerspezifischen Attribute verwenden. Sie können beispielsweise ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` um ein Buch oder einen Film zu definieren. Ein Ticketverkäufer kann Attribute für einen Veranstaltungsort für einen zusätzlichen Auftritt erstellen, z. B. ein weiteres Team, das bei einer Sportveranstaltung mitwirkt, oder eine Vorgruppe bei einem Konzert.

Einschränkungen:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden.
* Das Attribut entity.environment ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, entity.environment mit targetPageParams, Feed oder API zu übermitteln, werden ignoriert.

Beispiele:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Benutzerdefinierte Entitätsattribute unterstützen mehrere Werte. Siehe [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) für Zeichen- und Wertbeschränkungen.

Beispiel: `'entity.secondary=["band1",&nbsp;"band2"]'`

Benutzerdefinierte Entitätsattribute mit mehreren Werten erfordern gültige JSON-Arrays. Informationen zur korrekten Syntax finden Sie unter [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly

Nur einzelner Wert

Wird dazu verwendet zu verhindern, dass durch einen Mbox-Aufruf der Zähler für Verhaltensdaten eines Algorithmus ansteigt.

Beispiel: `'entity.event.detailsOnly=true'`

In den Beispielen unten aktualisiert der erste Mbox-Aufruf den Katalog und die Verhaltensdaten. Der zweite Mbox-Aufruf aktualisiert nur den Katalog.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

>[!MORELIKETHIS]
>
>* [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)

