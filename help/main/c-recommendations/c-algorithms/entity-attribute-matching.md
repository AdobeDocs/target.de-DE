---
keywords: Einschlussregeln; Einschlusskriterien; Recommendations; Promotion; Promotions; Dynamische Filterung; Dynamische Zuordnung von Entitätsattributen
description: Erfahren Sie, wie Sie dynamisch in  [!DNL Target Recommendations]  filtern können, indem Sie einen Pool potenzieller Elemente mit einem bestimmten Element vergleichen, mit dem der Benutzer interagiert hat.
title: Wie filtere ich nach der Zuordnung von Entitätsattributen in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Entitätsattributübereinstimmung

Dynamisches Filtern in [!DNL Adobe Target Recommendations] durch Vergleichen eines Pools potenzieller Recommendations-Elemente mit einem bestimmten Element, mit dem der Benutzer interagiert hat.

>[!NOTE]
>
>Der [Prozess zum Erstellen und Verwenden von ](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) für Kriterien und Promotions ist ähnlich, ebenso wie die Anwendungsfälle und Beispiele.

Empfehlen Sie beispielsweise nur Elemente, die der Marke des aktuellen Elements entsprechen, wie im folgenden Beispiel gezeigt:

Wenn die Mbox auf einer Brand Landing Page `entity.brand=brandA` zurückgibt, werden nur Brand A-Produkte zurückgegeben und auf dieser Seite angezeigt. Auf der Landingpage der Marke B werden auch nur Produkte der Marke B zurückgegeben. Bei dieser Art von dynamischer Einschlussregel muss der Benutzer nur eine Empfehlungsregel angeben, die relevante Markenergebnisse über alle Markenseiten hinweg zurückgibt, anstatt eine Sammlung oder einen statischen Filter anzugeben, um jeden Markennamen abzugleichen.

Beachten Sie, dass Sie die `entity.brand` in der Mbox auf diesen Landingpages bereitstellen müssen, damit dieser Prozess funktioniert.

## Beispiele für den Abgleich von Entitätsattributen

[!UICONTROL Entity Attribute Matching] können Sie nur die Elemente empfehlen, die übereinstimmen, z. B.:

* Ein Attribut aus dem Element, das der Benutzer derzeit anzeigt
* Das Element, das der Benutzer zuletzt angezeigt hat
* Der Artikel, den der Benutzer zuletzt gekauft hat
* Das Element, das der Benutzer am häufigsten angezeigt hat
* Ein Element, das in einem benutzerdefinierten Attribut im Besucherprofil gespeichert ist

### Empfohlene Artikel basierend auf der Marke

Nachdem die Entitätsattributregeln erstellt wurden, werden alle Recommendations mit Attributen herausgefiltert, die nicht mit dem auf der Seite übergebenen Entitätswert übereinstimmen.

Das folgende Beispiel zeigt Empfehlungen, die mit der auf der Seite gezeigten Produktmarke übereinstimmen:

Wenn Sie eine Seite besuchen, die ein Produkt von Marke A enthält, setzt die Seite den Wert des `entity.brand` auf „Marke A“.

![Beispiel für Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

In den Empfehlungen auf der Seite werden nur Produkte von Marke A angezeigt.

![Empfehlungen für Marke A](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Wenn Sie dann eine Produktseite von Marke B aufrufen, wird der `entity.brand` auf „Marke B“ zurückgesetzt und es werden auf den Produktseiten von Marke B empfohlene Produkte von Marke B angezeigt.

![Empfehlungen für Marke B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling auf ein teureres Produkt

Angenommen, Sie sind ein Bekleidungseinzelhändler und möchten die Benutzer ermutigen, teurere und daher profitablere Artikel in Betracht zu ziehen. Sie können die Operatoren „ist gleich“ und „ist zwischen“ verwenden, um für teurere Artikel zu werben, die aus derselben Kategorie und derselben Marke stammen. Ein Schuheinzelhändler kann beispielsweise teurere Laufschuhe bewerben, um einem Besucher, der Laufschuhe anschaut, einen Upsell zu bieten, wie im folgenden Beispiel dargestellt:

![Upselling](/help/main/c-recommendations/c-algorithms/assets/upsell-new.png)

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

### Förderung von Eigenmarkenprodukten

Sie können dynamische und statische Filter kombinieren, um Private-Label-Produkte zu bewerben. So kann ein Bürozulieferer beispielsweise Tonerkassetten der Hausmarke des Unternehmens bewerben, um einen profitableren Verkauf für einen Besucher zu erzielen, der Toner betrachtet. Außerdem kann er Stifte der Hausmarke des Unternehmens fördern, um einen profitableren Verkauf für einen Besucher zu ermöglichen, der Stifte betrachtet, wie im folgenden Beispiel dargestellt:

![Hausmarke](/help/main/c-recommendations/c-algorithms/assets/housebrand-new.png)
)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
