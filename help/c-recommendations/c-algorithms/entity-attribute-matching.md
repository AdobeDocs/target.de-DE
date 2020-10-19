---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Dynamische Filterung in Adobe Target Recommendations durch Vergleich eines Pools potenzieller Empfehlungselemente mit einem bestimmten Element, mit dem der Benutzer interagiert hat.
title: Filtern nach Entitätsattribut-Übereinstimmung in Regeln für dynamische Inklusion in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Entity Attribute Match

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing a pool of potential recommendations items to a specific item that the user has interacted with.

Empfehlen Sie beispielsweise nur Artikel, die mit der Marke des aktuellen Artikels übereinstimmen, wie im folgenden Beispiel:

Wenn die mbox auf einer Landingpage zurückgegeben wird `entity.brand=Nike`, werden nur Nike-Produkte zurückgegeben und auf dieser Seite angezeigt. Ebenso werden bei der Landingpage Markenprodukte für Adidas nur Adidas zurückgegeben. Bei diesem Typ von Regeln zur dynamischen Inklusion muss der Benutzer nur eine Empfehlungsregel angeben, die die relevanten Markenergebnisse über alle Markenseiten hinweg zurückgibt, anstatt eine Sammlung oder einen statischen Filter anzugeben, der mit jedem Markennamen übereinstimmt.

## Beispiele für Übereinstimmungen von Entitätsattributen

[!UICONTROL Mit der Zuordnung] von Entitätsattributen können Sie nur die Elemente empfehlen, die übereinstimmen, z. B.:

* Ein Attribut des Elements, das der Benutzer derzeit anzeigt
* Der Artikel, den der Benutzer zuletzt angesehen hat
* Der Artikel, den der Benutzer zuletzt gekauft hat
* Der Artikel, den der Benutzer am häufigsten angesehen hat
* Ein in einem benutzerdefinierten Attribut im Profil des Besuchers gespeichertes Element

### Hochladen zu einem teureren Produkt

Angenommen, Sie sind ein Bekleidungshändler und möchten Benutzer dazu ermutigen, teurere und damit gewinnbringendere Artikel in Betracht zu ziehen. Sie können die Operatoren &quot;Gleich&quot;und &quot;Ist zwischen&quot;verwenden, um teurere Artikel zu bewerben, die aus derselben Kategorie und derselben Marke stammen. Ein Schuhhändler kann beispielsweise teurere Laufschuhe fördern, um einen Besucher, der sich Laufschuhe ansieht, zu verkaufen, wie im folgenden Codebeispiel dargestellt:

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

Sie können dynamische und statische Filter kombinieren, um Produkte für Privatbezeichnungen zu bewerben. Beispielsweise kann eine Firma für die Büroversorgung Tonerkassetten der Hausmarke der Firma für einen Besucher, der sich den Toner ansieht, für einen rentableren Verkauf werben und die Marke der Firma für einen Besucher, der sich die Stifte ansieht, fördern, um einen rentableren Verkauf zu fördern, wie im folgenden Codebeispiel dargestellt:

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
