---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Dynamische Filterung in Adobe Target Recommendations durch Vergleich eines Pools potenzieller Empfehlungselemente mit einem bestimmten Element, mit dem der Benutzer interagiert hat.
title: Filtern nach Entitätsattribut-Übereinstimmung in Regeln für dynamische Inklusion in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 60b71c426b61bb16a23976da9a03926f8e73cf6c
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Entity Attribute Match

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing a pool of potential recommendations items to a specific item that the user has interacted with.

>[!NOTE]
>
>The [process for creating and using inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) for criteria and promotions is similar, as are the use cases and examples.

Empfehlen Sie beispielsweise nur Artikel, die mit der Marke des aktuellen Artikels übereinstimmen, wie im folgenden Beispiel:

Wenn die mbox auf einer Landingpage mit einer Marke zurückgegeben wird `entity.brand=brandA`, werden nur Produkte der Marke A zurückgegeben und auf dieser Seite angezeigt. Ebenso werden bei der Landingpage Markenbezeichnung B nur Produkte der Marke B zurückgegeben. Bei diesem Typ von Regeln für die dynamische Inklusion muss der Benutzer nur eine Empfehlungsregel angeben, die die relevanten Markenergebnisse über alle Markenseiten hinweg zurückgibt, anstatt eine Sammlung oder einen statischen Filter anzugeben, der mit jedem Markennamen übereinstimmt.

Beachten Sie, dass Sie die `entity.brand` in der mbox auf diesen Landingpages bereitstellen müssen, damit dies funktioniert.

## Beispiele für die Zuordnung von Entitätsattributen

[!UICONTROL Mit der Zuordnung] von Entitätsattributen können Sie nur die Elemente empfehlen, die übereinstimmen, z. B.:

* Ein Attribut des Elements, das der Benutzer derzeit anzeigt
* Der Artikel, den der Benutzer zuletzt angesehen hat
* Der Artikel, den der Benutzer zuletzt gekauft hat
* Der Artikel, den der Benutzer am häufigsten angesehen hat
* Ein in einem benutzerdefinierten Attribut im Profil des Besuchers gespeichertes Element

### Artikel nach Marke empfehlen

Nach der Erstellung der Entitätsattributregeln werden alle Empfehlungen mit Attributen herausgefiltert, die nicht mit dem auf der Seite weitergeleiteten Entitätswert übereinstimmen.

Das folgende Beispiel zeigt Empfehlungen, die mit der auf der Seite angezeigten Produktmarke übereinstimmen:

Wenn Sie eine Seite besuchen, die ein Produkt der Marke A enthält, setzt die Seite den Wert des `entity.brand` Parameters auf &quot;Marke A&quot;.

![Beispielaufruf für Zielgruppen](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

In den Empfehlungen auf der Seite sehen Sie nur Produkte der Marke A.

![Empfehlungen für Marke A](/help/c-recommendations/c-algorithms/assets/brandA.png)

Wenn Sie dann eine Ansicht einer Produkt-Seite der Marke B vornehmen, wird der `entity.brand` Wert auf &quot;Marke B&quot;zurückgesetzt, und Sie sehen die auf den Produktseiten der Marke B empfohlenen Produkte.

![Empfehlungen für Marke B](/help/c-recommendations/c-algorithms/assets/brandB.png)

### Hochladen zu einem teureren Produkt

Angenommen, Sie sind ein Bekleidungshändler und möchten Benutzer dazu ermutigen, teurere und damit gewinnbringendere Artikel in Betracht zu ziehen. Sie können die Operatoren &quot;Gleich&quot;und &quot;Ist zwischen&quot;verwenden, um teurere Artikel zu bewerben, die aus derselben Kategorie und derselben Marke stammen. Ein Schuhhändler kann beispielsweise teurere Laufschuhe fördern, um einen Besucher, der sich Laufschuhe ansieht, zu verkaufen, wie im folgenden Beispiel:

![Upsell](/help/c-recommendations/c-algorithms/assets/upsell.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

### Förderung von Produkten mit privatem Etikett

Sie können dynamische und statische Filter kombinieren, um Produkte für Privatbezeichnungen zu bewerben. Beispielsweise kann eine Firma für die Büroversorgung Tonerkassetten der Hausmarke der Firma für einen Besucher, der sich den Toner ansieht, für einen rentableren Verkauf werben und die Marke der Firma für einen Besucher, der sich die Stifte ansieht, fördern, um einen rentableren Verkauf zu fördern, wie im folgenden Beispiel:

![Hausmarke](/help/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
