---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; dynamisch; Entitätsattributübereinstimmung
description: Erfahren Sie, wie Sie in [!DNL Target Recommendations] dynamisch filtern können, indem Sie einen Pool potenzieller Elemente mit einem bestimmten Element vergleichen, mit dem der Benutzer interagiert hat.
title: Wie kann ich in Recommendations-Aktivitäten nach Entitätsattributübereinstimmung filtern?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6a55260fd49e07e2b217f6becfbc778251a5d0d
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Entitätsattributübereinstimmung

Dynamisches Filtern in [!DNL Adobe Target Recommendations] durch Vergleich eines Pools potenzieller Empfehlungselemente mit einem bestimmten Element, mit dem der Benutzer interagiert hat.

>[!NOTE]
>
>Der [Prozess zum Erstellen und Verwenden von Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) für Kriterien und Promotions ist ähnlich, ebenso die Anwendungsfälle und Beispiele.

Empfehlen Sie beispielsweise nur Elemente, die mit der Marke des aktuellen Elements übereinstimmen, wie im folgenden Beispiel gezeigt:

Wenn die Mbox auf einer Brand Landingpage den Wert `entity.brand=brandA` zurückgibt, werden nur Produkte der Marke A zurückgegeben und auf dieser Seite angezeigt. Ebenso werden auf der Brand Landingpage für Marke B nur Produkte von Marke B zurückgegeben. Bei diesem Typ von dynamischer Einschlussregel muss der Benutzer nur eine Empfehlungsregel angeben, die relevante Markenergebnisse über alle Markenseiten hinweg zurückgibt, anstatt eine Kollektion oder einen statischen Filter anzugeben, der mit jedem Markennamen übereinstimmt.

Beachten Sie, dass Sie auf diesen Landingpages die `entity.brand` in der Mbox bereitstellen müssen, damit dieser Prozess funktioniert.

## Beispiele für Entitätsattributübereinstimmung

Mit [!UICONTROL Entity Attribute Matching] können Sie nur die Elemente empfehlen, die übereinstimmen, z. B.:

* Ein Attribut aus dem Element, das der Benutzer derzeit anzeigt
* Der Artikel, den der Benutzer zuletzt angesehen hat
* Der Artikel, den der Benutzer zuletzt gekauft hat
* Das Element, das der Benutzer am häufigsten angezeigt hat
* Ein Element, das in einem benutzerdefinierten Attribut im Besucherprofil gespeichert ist

### Artikel basierend auf der Marke empfehlen

Nachdem Ihre Entitätsattributregeln erstellt wurden, filtern sie alle Empfehlungen mit Attributen heraus, die nicht mit dem auf der Seite übergebenen Entitätswert übereinstimmen.

Das folgende Beispiel zeigt Empfehlungen, die mit der auf der Seite angezeigten Produktmarke übereinstimmen:

Wenn Sie eine Seite besuchen, die ein Produkt der Marke A enthält, setzt die Seite den Wert des Parameters `entity.brand` auf &quot;Marke A&quot;.

![Beispiel für Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

In den Empfehlungen auf der Seite sehen Sie nur Produkte von Marke A.

![Marke A recommendations](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Wenn Sie dann eine Produktseite von Marke B anzeigen, wird der Wert `entity.brand` auf &quot;Marke B&quot;zurückgesetzt und auf den Produktseiten von Marke B werden die empfohlenen Produkte angezeigt.

![Marke B Recommendations](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upload zu einem teureren Produkt

Angenommen, Sie sind ein Bekleidungshändler und möchten Benutzer dazu ermutigen, teurere und damit profitablere Artikel in Betracht zu ziehen. Sie können die Operatoren &quot;gleich&quot;und &quot;ist zwischen&quot;verwenden, um teurere Artikel zu bewerben, die aus derselben Kategorie und derselben Marke stammen. Ein Schuhhändler kann beispielsweise teurere Laufschuhe bewerben, um einen Besucher, der sich Laufschuhe ansieht, zu verkaufen, wie im folgenden Beispiel gezeigt:

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

### Werbung für Produkte mit privatem Etikett

Sie können dynamische und statische Filter kombinieren, um Produkte mit privaten Beschriftungen zu bewerben. So kann beispielsweise ein Bürobedarfsunternehmen Tonerkassetten der Hausmarke des Unternehmens dafür bewerben, einen gewinnbringenderen Verkauf für einen Besucher zu fördern, der Toner ansieht, und Stifte der Hausmarke des Unternehmens für einen gewinnbringenderen Verkauf für einen Besucher bewerben, der nach Stiften sucht, wie im folgenden Beispiel gezeigt:

![Hausmarke](/help/main/c-recommendations/c-algorithms/assets/housebrand-new.png)
)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
