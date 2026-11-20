---
keywords: Entität Entitätsattribute; Weiterleiten von Informationen an Recommendations; Verhaltensdaten; Datenzähler; relative URL definieren; Lagerbestandsebene anzeigen; Preis festlegen; Festlegen der Gewinnspanne; benutzerdefinierte Attribute
description: Erfahren Sie, wie Sie Entitätsattribute verwenden, um Produkt- oder Inhaltsinformationen an [!DNL Target] Recommendations zu übergeben.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
title: Wie verwende ich Entitätsattribute?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
TQID: 'https://experienceleague.adobe.com/GXQOxQxTV0vTYsWy9Ky9wPNEqoRSAhIA5zlBd4Cr4Ec'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 5ed511322cc9f04c349471f8ad84a17526d4925f
workflow-type: tm+mt
source-wordcount: '1173'
ht-degree: 28%
---
# Entitätsattribute {#entity-attributes}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, welche Entitätsattribute Produkt- oder Inhaltsinformationen an [!DNL Adobe Target Recommendations] übergeben und wie Sie die einzelnen Attribute definieren.

>[!ENDSHADEBOX]

Verwenden Sie Entitätsattribute, um Produkt- oder Inhaltsinformationen an [!DNL Adobe Target Recommendations] zu übergeben, wo sie in Designs angezeigt und in Einschlussregeln, Sammlungen und Ausschlüssen verwendet werden können. Entitäten sind die Elemente, die Sie empfehlen möchten, z. B. Produkte, Inhalte (Artikel, Slideshows, Bilder, Filme und Fernsehsendungen), Auftragslisten, Restaurants und so weiter. [!DNL Recommendations] sendet die `productId` oder `productPurchasedId` (im Code als `entity.id` bezeichnet), die in den Algorithmen verwendet werden.

Beachten Sie Folgendes:

* `entity.id` muss mit den `productPurchasedId` übereinstimmen, die an die Bestellbestätigungsseite gesendet wurden, sowie mit den in [!DNL Adobe Analytics] Produktberichten verwendeten `productId`.
* Entitätsattributwerte, die Sie an übergeben, laufen [!DNL Recommendations] nach 61 Tagen ab. Adobe empfiehlt, für jedes Element im Katalog den neuesten Wert jedes Entitätsattributs mindestens einmal pro Monat an [!DNL Recommendations] zu übergeben.

Die meisten vordefinierten Parameter akzeptieren nur einen einzigen Wert, wobei neue Werte alte Werte überschreiben. Der `categoryId` ist die Ausnahme (siehe [entity.categoryId](#entity-category-id)).

Im Allgemeinen sieht die mBox „Display Information“ wie im folgenden Beispiel aus, wenn Sie at.js 1.*x* mit `mboxCreate` verwenden. Bei allen Entitätsparameterattributen wird zwischen Groß- und Kleinschreibung unterschieden.

Wenn Sie at.js 2.*x* verwenden, wird `mboxCreate` (wie im folgenden Beispiel verwendet) nicht mehr unterstützt. Um Produkt- oder Inhaltsinformationen mithilfe von at.js 2.x *an [!DNL Recommendations] zu*, verwenden Sie [targetPageParams](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html){target=_blank}. Ein Beispiel finden Sie unter [Recommendations planen und implementieren](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

+++ Beispiel einer Mbox, die Entitätsattribute übergibt

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

+++

>[!NOTE]
>
>Relative URLs werden für `pageUrl` und `thumbnailUrl` im Gegensatz zu absoluten URLs bevorzugt, da die Empfehlungen aus allen Umgebungen auf Ihrer Site Daten empfangen. Durch die Verwendung von relativen URLs werden fest codierte Links auf Staging- oder Entwicklungsserver vermieden.

Wenn sich die Mbox auf einer Produktseite befindet, können Sie sowohl die Produkt-ID als auch die Kategorie-ID angeben. Der ausgewählte Algorithmus bestimmt, welcher angezeigt wird. Die Produkt-ID wird für Affinitätsalgorithmen und die Kategorie-ID für Kategoriealgorithmen verwendet.

## Verfügbare Variablen

In der folgenden Tabelle sind die verfügbaren Variablen aufgeführt. Unterabschnitte nach der Tabelle enthalten weitere Informationen über die Variablen, die sie benötigen.

| Variable | Werte | Beschreibung | Beispiel |
|---|---|---|---|
| `entity.id` | Nur ein Wert. Erforderlich. | Identifiziert das Produkt. Siehe [entity.id](#entity-id). | `'entity.id=67833'` |
| `entity.name` | Nur ein Wert. | Der Produktname, der bei der Empfehlung des Produkts auf der Website angezeigt wird. | `'entity.name=Giants& vs& Rockies& 5/12'` |
| `entity.categoryId` | Mehrere Werte (kommagetrennte Liste). | Die Kategorie der aktuellen Seite. Siehe [entity.categoryId](#entity-category-id). | `'entity.categoryId=womens:sweaters'` |
| `entity.brand` | Nur ein Wert. | Zeigt den Markennamen eines Artikels an. | `'entity.brand=brandxyz'` |
| `entity.pageUrl` | Nur ein Wert. | Definiert die relative URL der Seite, auf der der Artikel zum Kauf angeboten wird. | `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'` |
| `entity.thumbnailUrl` | Nur ein Wert. | Definiert die relative URL zum Miniaturbild, das mit dem Artikel angezeigt wird. | `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'` |
| `entity.message` | Nur ein Wert. | Eine Botschaft zu dem in der Empfehlung angezeigten Produkt, wie zum Beispiel „Im Angebot“ oder „Ausverkauf“. Die Botschaft ist in der Regel ausführlicher als der Produktname. Verwenden Sie `entity.message`, um zusätzliche Informationen zu definieren, die mit dem Produkt in der Vorlage angezeigt werden sollen. | `'entity.message=Family&nbsp;special'` |
| `entity.inventory` | Nur ein Wert. Erfordert eine Ganzzahl oder einen langen Wert. | Zeigt den Lagerbestand des Artikels. Siehe [entity.inventory](#entity-inventory). | `'entity.inventory=1'` |
| `entity.value` | Nur ein Wert. | Definiert den Preis oder Wert des Artikels. Es wird nur das Dezimalformat unterstützt (z. B. 15.99). Das Kommaformat (15,99) wird nicht unterstützt. | `'entity.value=15.99'` |
| `entity.margin` | Nur ein Wert. | Die Gewinnspanne oder ein anderer Wert des Artikels. | `'entity.margin=1.00'` |
| `entity.`*custom* | Mehrere Werte (JSON-Array). | Benutzerdefinierte Variablen, die zusätzliche Informationen zum Element bereitstellen. Siehe [entity.*custom*](#entity-custom). | `'entity.secondary=Rockies'` |
| `entity.event.detailsOnly` | Nur ein Wert. | Verhindert, dass durch einen Mbox-Aufruf Verhaltensdatenzähler für einen Algorithmus erhöht werden. Siehe [entity.event.detailsOnly](#entity-event-details-only). | `'entity.event.detailsOnly=true'` |

### entity.id {#entity-id}

Die alphanumerische ID muss für alle [!DNL Adobe Experience Cloud] Produkte gleich sein, die für die Erkennung des Elements und die Freigabe von Daten durch die verschiedenen Produkte verwendet werden, einschließlich [!DNL Analytics].

Die `entity.id` dürfen *keine* Leerzeichen, Schrägstriche, kaufmännische Und-Zeichen, Fragezeichen, Prozentzeichen, Kommas oder andere Satzzeichen enthalten, für die eine URL-Codierung erforderlich ist, wenn sie in einem REST-API-Aufruf übergeben wird. Bindestriche und Unterstriche sind zulässig. Wenn in einem `entity.id`[!DNL Recommendations]-Wert ungültige Satzzeichen enthalten sind, schlagen manche fehl.

### entity.categoryId {#entity-category-id}

Der `entity.categoryId` kann mehrere Kategorien enthalten, z. B. einen Unterabschnitt „Cardigans“ (z. B. `womens`, `womens:sweaters`, `womens:sweaters:cardigans`). Mehrere Kategorien müssen durch Kommas getrennt werden. Neue `categoryId` überschreiben keine vorhandenen Werte, sondern werden bei der Aktualisierung der Entität angehängt. Der `categoryId` ist auf 250 Zeichen begrenzt.

>[!NOTE]
>
>Um eine Empfehlung basierend auf einer Kategorie auf einer **[!UICONTROL Kategorie]**-Seite anzuzeigen, kann nur ein `categoryId` an die Mbox übergeben werden, die zur Anzeige dieser bestimmten Empfehlung verwendet wird. Der Wert des `categoryId` muss genau mit dem Wert des `entity.categoryId` übereinstimmen, der auf der Seite **[!UICONTROL Produktdetails“]** wurde.

Beispiele:

* Beispiel für eine Produktdetailseite: `womens`, `womens:sweaters`, `womens:sweaters:cardigans`
* Beispiel Kategorie Seite Pullover: `womens:sweaters`
* Beispiel für Kategorieseiten-Strickjacken: `womens:sweaters:cardigans`

Bei kategoriebasierten Empfehlungen wird der Kategoriewert durch ein Komma getrennt. Alle durch Kommas getrennten Werte sind dann Kategorien. Sie können auch Unterkategorien mit einem anderen Trennzeichen, beispielsweise einem Doppelpunkt (:), definieren, um Unterkategorien innerhalb des Kategoriewerts zu trennen.

Im folgenden Code ist die Kategorie „Damen“ beispielsweise in mehrere Unterkategorien unterteilt:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...');
```

Für die MBox-Bereitstellung wird der längste Attributname für den Schlüssel verwendet. Wenn eine Bindung vorhanden ist, wird das letzte Attribut verwendet. Im obigen Beispiel wird der Kategorieschlüssel `Womens:Outerwear:Jackets:Caban`.

### entity.inventory {#entity-inventory}

**Leere Handhabung von Lagerattributen:** Wenn Sie für den Versand eine Einschlussregel, eine Erfassungsregel oder eine Kriterieneinstellung mit `entity.inventory` > 0 oder `entity.inventory` = 0 haben und das Produkt keinen Bestand hat, bewertet [!DNL Target] diesen Wert als „TRUE“ und schließt Produkte ein, für die der Bestand nicht festgelegt ist. Daher werden Produkte mit einem nicht festgelegten Inventar in den Empfehlungsergebnissen angezeigt.

Wenn Sie eine globale Ausschlussregel mit `entity.inventory` = 0 und `entity.inventory` nicht festgelegt haben, wird diese Regel von [!DNL Target] auf TRUE gesetzt und das Produkt ausgeschlossen.

>[!NOTE]
>
>**Bekanntes Problem** Die Produktsuche stimmt nicht mit dem Versand überein, wenn keine Inventarwertattribute festgelegt sind. Beispiel: Für eine Regel mit `entity.inventory` = 0 zeigt die Produktsuche keine Produkte an, für die der Inventarwert nicht festgelegt ist.

### entity.*custom* {#entity-custom}

Sie können bis zu 100 benutzerdefinierte Variablen definieren. Sie können jeden nicht bereits in Gebrauch befindlichen Attributnamen für die benutzerspezifischen Attribute verwenden. Sie können beispielsweise ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` erstellen, um ein Buch oder einen Film zu definieren. Ein Ticketverkäufer kann Attribute für einen Veranstaltungsort für einen sekundären Darsteller erstellen, z. B. ein Gastteam bei einem Sportereignis oder einen Eröffnungsakt in einem Konzert.

Einschränkungen:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden.
* Das Attribut `entity.environment` ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, `entity.environment` mit `targetPageParams`, Feed oder API zu übergeben, werden ignoriert.

Beispiele:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Benutzerdefinierte Entitätsattribute unterstützen mehrere Werte. Siehe [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) für Zeichen- und Wertbeschränkungen.

Beispiel: `'entity.secondary=["band1",&nbsp;"band2"]'`

Benutzerdefinierte Entitätsattribute mit mehreren Werten erfordern gültige JSON-Arrays. Die richtigen Syntaxinformationen finden Sie unter [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly {#entity-event-details-only}

Verwenden Sie diesen Parameter, um zu verhindern, dass durch einen Mbox-Aufruf Verhaltensdatenzähler für einen Algorithmus erhöht werden.

In den folgenden Beispielen werden mit dem ersten Mbox-Aufruf die Katalog- und Verhaltensdaten aktualisiert. Mit dem zweiten Mbox-Aufruf wird nur der Katalog aktualisiert.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york', 'entity.id = 123', 'entity.inventory = 4' )
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york', 'entity.id = 123', 'entity.inventory = 4', 'entity.event.detailsOnly=true' )
```
