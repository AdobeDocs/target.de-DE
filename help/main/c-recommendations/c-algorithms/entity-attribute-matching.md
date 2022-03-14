---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; dynamisch; Entitätsattributübereinstimmung
description: Erfahren Sie, wie Sie in Adobe dynamisch filtern. [!DNL Target] Recommendations durch Vergleich eines Pools potenzieller Elemente mit einem bestimmten Element, mit dem der Benutzer interagiert hat.
title: Wie kann ich in Recommendations-Aktivitäten nach Entitätsattributübereinstimmung filtern?
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Entitätsattributübereinstimmung

Dynamisches Filtern in [!DNL Adobe Target] [!DNL Recommendations] indem ein Pool potenzieller Empfehlungselemente mit einem bestimmten Element verglichen wird, mit dem der Benutzer interagiert hat.

>[!NOTE]
>
>Die [Verfahren zum Erstellen und Verwenden von Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) -Kriterien und -Promotions sind ähnlich, ebenso die Anwendungsfälle und -beispiele.

Empfehlen Sie beispielsweise nur Elemente, die mit der Marke des aktuellen Elements übereinstimmen, wie im folgenden Beispiel gezeigt:

Wenn die Mbox auf einer Brand Landing Page `entity.brand=brandA`, werden nur Produkte von Marke A zurückgegeben und auf dieser Seite angezeigt. Ebenso werden auf der Brand Landingpage für Marke B nur Produkte von Marke B zurückgegeben. Bei diesem Typ von dynamischer Einschlussregel muss der Benutzer nur eine Empfehlungsregel angeben, die relevante Markenergebnisse über alle Markenseiten hinweg zurückgibt, anstatt eine Kollektion oder einen statischen Filter anzugeben, der mit jedem Markennamen übereinstimmt.

Beachten Sie, dass Sie die `entity.brand` in der Mbox auf diesen Landingpages verwenden, damit dies funktioniert.

## Beispiele für Entitätsattributübereinstimmung

[!UICONTROL Entitätsattributübereinstimmung] ermöglicht es Ihnen, nur die Elemente zu empfehlen, die übereinstimmen, z. B.:

* Ein Attribut aus dem Element, das der Benutzer derzeit anzeigt
* Der Artikel, den der Benutzer zuletzt angesehen hat
* Der Artikel, den der Benutzer zuletzt gekauft hat
* Das Element, das der Benutzer am häufigsten angezeigt hat
* Ein Element, das in einem benutzerdefinierten Attribut im Besucherprofil gespeichert ist

### Artikel basierend auf der Marke empfehlen

Nachdem Ihre Entitätsattributregeln erstellt wurden, filtern sie alle Empfehlungen mit Attributen heraus, die nicht mit dem auf der Seite übergebenen Entitätswert übereinstimmen.

Das folgende Beispiel zeigt Empfehlungen, die mit der auf der Seite angezeigten Produktmarke übereinstimmen:

Wenn Sie eine Seite besuchen, die ein Produkt der Marke A enthält, legt die Seite den Wert der `entity.brand` auf &quot;BrandA&quot;gesetzt.

![Beispiel für Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

In den Empfehlungen auf der Seite sehen Sie nur Produkte von Marke A.

![Empfehlungen für Marke A](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Wenn Sie dann eine Brand B-Produktseite anzeigen, wird die `entity.brand` wird auf &quot;Marke B&quot;zurückgesetzt, und auf den Produktseiten von Marke B werden Brand B-Produkte empfohlen.

![Empfehlungen für Marke B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upload zu einem teureren Produkt

Angenommen, Sie sind ein Bekleidungshändler und möchten Benutzer dazu ermutigen, teurere und damit profitablere Artikel in Betracht zu ziehen. Sie können die Operatoren &quot;gleich&quot;und &quot;ist zwischen&quot;verwenden, um teurere Artikel zu bewerben, die aus derselben Kategorie und derselben Marke stammen. Ein Schuhhändler kann beispielsweise teurere Laufschuhe bewerben, um einen Besucher, der sich Laufschuhe ansieht, zu verkaufen, wie im folgenden Beispiel gezeigt:

![Upload](/help/main/c-recommendations/c-algorithms/assets/upsell.png)

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

![Hausmarke](/help/main/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
