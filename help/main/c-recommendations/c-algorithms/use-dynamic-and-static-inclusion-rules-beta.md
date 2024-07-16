---
keywords: Einschlussregeln; Aufnahmekriterien; Empfehlungen; neue Kriterien erstellen; Promotion; Promotions; dynamischer Filter; dynamisch; leere Werte; Filterregel ignorieren; statischer Filter; Filtern nach Wert; Entitätsattributübereinstimmung; Profilattributübereinstimmung; Parameterübereinstimmung; Filtern nach Wert; statischer Filter
description: Erfahren Sie, wie Sie Einschlussregeln in  [!DNL Target] Recommendations für Kriterien und Promotions erstellen.
title: Wie verwende ich dynamische und statische Einschlussregeln in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
mini-toc-levels: 3
hide: true
hidefromtoc: true
source-git-commit: 84f2ea906dcab939b3892b11eabf96494f4514cb
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 16%

---

# Verwenden dynamischer und statischer Einschlussregeln

Erstellen Sie Einschlussregeln für Kriterien und Promotions in [!DNL Adobe Target] und fügen Sie dynamische oder statische Filterregeln hinzu, um bessere Ergebnisse für Ihre Empfehlungen zu erzielen.

Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. Kriterien und Promotions sowie die Verwendung von Einschlussregeln werden in diesem Abschnitt behandelt.

## Hinzufügen von Filterregeln zu Kriterien und Promotions {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

### Hinzufügen von Filterregeln zu Kriterien

1. Klicken Sie beim Erstellen von Kriterien ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) (**[!UICONTROL Recommendations]> [!UICONTROL Criteria] > [!UICONTROL Create Criteria] >[!UICONTROL Create Criteria]**) unter **[!UICONTROL Inclusion Rules]** auf **[!UICONTROL Add Filtering Rule]**.[

   ![Filterregel hinzufügen](/help/main/c-recommendations/c-algorithms/assets/add-fitering-rule.png)

1. Klicken Sie auf die Dropdownliste **Statischer Filter** im Feld &quot;Welche anderen Regeln sollte die Empfehlung beachten&quot;und wählen Sie dann die gewünschte Option aus der Dropdownliste [!UICONTROL Static Filter] aus.

   ![Dropdown-Liste &quot;Statischer Filter&quot;](/help/main/c-recommendations/c-algorithms/assets/dynamic-and-static.png)

   Die verfügbaren Optionen variieren je nach vertikalem Markt und Empfehlungsschlüssel.

### Hinzufügen von Filterregeln zu Promotions

1. Wählen Sie beim Erstellen von [ einer Promotion ](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14) die Option **[!UICONTROL Promote by Attribute]** und klicken Sie dann auf **[!UICONTROL Add Filtering Rule]**.

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In den folgenden Abschnitten werden die Filteroptionen für [!UICONTROL Dynamic Filtering] und [!UICONTROL Filter by Value] für Kriterien und Promotions aufgelistet:

### Dynamische Filterung

Dynamische Einschlussregeln sind leistungsstärker als statische Einschlussregeln und liefern bessere Ergebnisse und Interaktionen. Beachten Sie Folgendes:

* Dynamische Einschlussregeln liefern Empfehlungen, indem sie ein Attribut im Profilparameter eines Benutzers oder in einem Mbox-Aufruf abgleichen.

  Sie können beispielsweise die Empfehlung &quot;Bevorzugte Kriterien&quot;erstellen. Aus dem Satz der zurückgegebenen Empfehlungen können Sie alle Empfehlungen (in Echtzeit) nach einem Attribut filtern, das übergeben wird, wenn der Benutzer auf eine Seite zugreift, auf der die Empfehlungen angezeigt werden.

* Verwenden Sie statische Regeln, um zu begrenzen, welche Artikel in der Empfehlung enthalten sind (anstatt Sammlungen zu verwenden).

* Sie können so viele dynamische Einschlussregeln wie nötig erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Die folgenden Optionen stehen für die dynamische Filterung zur Verfügung:

| Dynamische Filteroption | Details |
| --- | --- |
| [[!UICONTROL Entity Attribute Matching]](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Dynamisches Filtern durch Vergleich eines Pools potenzieller Empfehlungselemente mit einem bestimmten Element, mit dem die Benutzer interagiert haben.<P>Verwenden Sie [!UICONTROL Entity Attribute Matching] , wenn Sie Empfehlungen anzeigen möchten, die am ehesten an den Besucher appellieren, z. B. an die Lieblingsmarke des Besuchers. |
| [[!UICONTROL Profile Attribute Matching]](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Dynamisches Filtern durch Vergleich von Elementen (Entitäten) mit einem Wert im Benutzerprofil.<P>Verwenden Sie [!UICONTROL Profile Attribute Matching] , wenn Sie Empfehlungen anzeigen möchten, die mit einem im Besucherprofil gespeicherten Wert übereinstimmen, z. B. Größe oder Lieblingsmarke. |
| [[!UICONTROL Parameter Matching]](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Dynamisches Filtern per Vergleich von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).<P>Verwenden Sie [!UICONTROL Parameter Matching] , um Inhalte zu empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Gerätedimensionen oder Geolokation. |

### Nach Wert filtern

Die folgende Option ist zum Filtern nach Wert verfügbar:

| Option &quot;Filtern nach Wert&quot; | Details |
| --- | --- |
| [[!UICONTROL Static Filter]](/help/main/c-recommendations/c-algorithms/static-value.md) | Geben Sie einen oder mehrere zu filternde statische Werte manuell ein. |

## Verfügbare Operatoren {#operators}

Dynamische Kriterien und Promotions sind viel leistungsfähiger als statische Kriterien und Promotions und liefern bessere Ergebnisse und Interaktionen.

Die folgenden Beispiele enthalten allgemeine Ideen zur Verwendung dynamischer Promotions und Ausschlüsse in Ihren Marketing-Maßnahmen:

| Benutzerin oder Benutzer | Beispiele |
| --- | --- |
| [!UICONTROL equals any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Wenn Sie den Operator &quot;gleich&quot;in dynamischen Promotions verwenden, können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, weitere Elemente bewerben, die folgende Kriterien erfüllen:<ul><li>Dieselbe Marke</li><li>Dieselbe Kategorie</li><li>Dieselbe Kategorie UND von der Hausmarke</li><li>Derselbe Store</li></ul> |
| [!UICONTROL does not equal any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Wenn Sie den Operator &quot;[!UICONTROL does not equal any of]&quot;in dynamischen Promotions verwenden, können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, weitere Elemente bewerben, die folgende Kriterien erfüllen:<ul><li>Eine andere Fernsehserie</li><li>Ein anderes Genre</li><li>Eine andere Produktserie</li><li>Eine andere Stil-ID</li></ul> |
| [!UICONTROL is greater than or equal to any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL is greater than or equal to any of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Kosten gleich oder teurer</li></ul> |
| [!UICONTROL is less than or equal to any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL is less than or equal to an of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Gleiche Kosten oder niedrigere Kosten</li><li>Niedrigere Artikel ausschließen</li></ul> |
| [!UICONTROL contains any of] (Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL contains any of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Der Titel enthält dieselbe Marke</li></ul> |
| [!UICONTROL does not contain any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;enthält keinen von&quot;können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Titel enthält kein Sweet-Wort</li></ul> |
| [!UICONTROL starts with any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL starts with an of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Der Produktname beginnt mit iPhone</li></ul> |
| [!UICONTROL ends with any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL ends with an of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Inhalt endet mit EN, was die englische Sprache angibt</li></ul> |
| [!UICONTROL is between]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;i[!UICONTROL s between]&quot;in dynamischen Promotions können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, weitere Elemente bewerben, die folgende Kriterien erfüllen:<ul><li>Mehr</li><li>Weniger teuer</li><li>Kosten plus oder minus 30 %</li><li>Spätere Episoden in derselben Saison</li><li>Vorherige Bücher in einer Reihe</li></ul> |
| [!UICONTROL list contains an item in]<P>(Verfügbar mit [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list contains an item in]&quot;beim Profilattributabgleich können Sie weitere Elemente bewerben, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt:<ul><li>Verfügbar in der Geografie des Besuchers</li></ul>**Beispiel**: Sie möchten Elemente empfehlen, die nur im geografischen Bereich eines Besuchers verfügbar sind.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`availableGeographies list contains an item in user.currentGeography`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf der [rechten Seite](#caveats) der Regel erwartet. |
| [!UICONTROL list does not contain an item in]<P>(Verfügbar mit [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list does not contain an item in]&quot;bei der Profilattributübereinstimmung können Sie andere Elemente ausschließen, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. ein Produkt, einen Artikel oder einen Film):<ul><li>In der Liste der letzten zehn Elemente, die der Besucher angezeigt hat</li></ul></ul>**Beispiel**: Sie möchten keine Artikel bewerben, die der Besucher kürzlich angesehen hat und für die er kein Interesse gezeigt hat.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`id is not contained in list user.lastViewedItems`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf der [rechten Seite](#caveats) der Regel erwartet. |
| [!UICONTROL list contains an item in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list contains an item in]&quot; beim Profilattributabgleich können Sie weitere Elemente bewerben, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. ein Sportereignis oder -konzert):<ul><li>Einer der Lieblingsteams des Besuchers zugeordnet</li></ul>**Beispiel**: Sie möchten Spiele empfehlen, die mit einem der Lieblingsteams des Besuchers verknüpft sind.<P>Ihre Filterregel könnte wie folgt aussehen:<P>` teamsPlaying list contains an item in user.favoriteTeams`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [beiden Seiten](#caveats) der Regel erwartet. |
| [!UICONTROL list does not contain an item in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Wenn Sie den Operator &quot;[!UICONTROL list does not contain an item in]&quot; bei der Parameterattributübereinstimmung verwenden, können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, andere Elemente ausschließen, die Folgendes sind:<ul><li>In einer Liste verbotener Typen enthalten</li></ul>**Beispiel**: Sie möchten Elemente ausschließen, die für Erwachsene verfügbar sind, wie Tabak und Alkohol.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`itemType is not contained in list mbox.prohibitedTypes`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [beiden Seiten](#caveats) der Regel erwartet. |
| [!UICONTROL list contains all items in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list does not contain an item in]&quot; bei der Profilattributübereinstimmung können Sie weitere Elemente bewerben, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. eine Auftragswahl oder ein Rezept):<ul><li>Kenntnisse einschließen</li><li>Eine Reihe erforderlicher Zutaten einschließen</li></ul>**Beispiel 1**: Angenommen, ein Besucher verfügt über eine Reihe von Fähigkeiten (Java, C++ und HTML). Die Artikel im Katalog sind Aufträge mit erforderlichen Fähigkeiten (Java und HTML). Sie möchten sicherstellen, dass das Besucherprofil alle erforderlichen Fähigkeiten enthält, bevor Sie den Auftrag dem Besucher empfehlen.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<P>**Beispiel 2**: Angenommen, ein Benutzer verfügt über eine Liste von Inhaltsstoffen für die Auswahl. Das Rezept enthält eine Liste erforderlicher Zutaten. Sie möchten sicherstellen, dass das Besucherprofil alle erforderlichen Inhaltsstoffe enthält, bevor Sie dem Besucher das Rezept empfehlen.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [beiden Seiten](#caveats) der Regel erwartet. |
| [!UICONTROL list does not contain all items in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list does not contain all items in]&quot; bei der Entitätsattributübereinstimmung können Sie weitere Elemente bewerben, die angezeigt werden, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. Sportveranstaltungen oder -konzerte):<ul><li>Schließen Sie keine Gruppe von Teams ein.</li></ul>**Beispiel**: Angenommen, ein Sportereignis umfasst zwei Teams. Das Besucherprofil gibt an, dass dieser Besucher keine Spiele für diese Teams anzeigen möchte. Sie möchten sicherstellen, dass Sie kein Spiel empfehlen, wenn diese Teams spielen.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [beiden Seiten](#caveats) der Regel erwartet. |

## Umgang mit leeren Werten beim Filtern nach [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Sie können mehrere Optionen auswählen, um leere Werte beim Filtern nach [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] für Ausstiegskriterien und -Promotions zu verarbeiten.

Zuvor wurden bei einem leeren Wert keine Ergebnisse zurückgegeben. In der Dropdownliste „Wenn *x* leer ist“ können Sie die entsprechende Aktion auswählen, die ausgeführt werden solle, wenn die Kriterien leere Werte enthalten, wie in der folgenden Abbildung dargestellt:

![empty_value image](assets/empty_value.png)

Um die gewünschte Aktion auszuwählen, bewegen Sie den Mauszeiger über das Zahnradsymbol (![icon_Zahnradbild](assets/icon_gear.png)) und wählen Sie dann die gewünschte Aktion aus:

| Aktion | Verfügbar für | Details |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Diese Aktion ist die Standardeinstellung für [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].<P>Diese Option gibt an, dass die Regel ignoriert wird. Wenn beispielsweise drei Filterregeln vorhanden sind und die dritte Regel keine Werte übergibt, können Sie die dritte Regel mit den leeren Werten einfach ignorieren, statt gar keine Ergebnisse zurückzugeben. |
| [!UICONTROL Do not show any results for this criteria]<P>(Nur Kriterien) | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Diese Aktion ist die Standardeinstellung für [!UICONTROL Entity Attribute Matching].<P>Durch diese Aktion wird bestimmt, wie [!DNL Target] leere Werte vor dem Hinzufügen dieser Option verarbeitet hat: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| [!UICONTROL Bewerben Sie keine Elemente.<P>(Nur Promotions)] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Diese Aktion ist die Standardeinstellung für [!UICONTROL Entity Attribute Matching].<P>Durch diese Aktion wird bestimmt, wie [!DNL Target] leere Werte vor dem Hinzufügen dieser Option verarbeitet hat: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Wenn ein Wert leer ist, können Sie die Verwendung eines statischen Werts festlegen. |

## Einschränkungen  {#caveats}

>[!IMPORTANT]
>
>Verschiedene Datentypattribute sind möglicherweise nicht mit dynamischen Kriterien oder Promotions kompatibel, während sie zur Laufzeit mit den Operatoren „ist gleich“ und „ist nicht gleich“ verwendet werden. Verwenden Sie die Werte [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] und [!UICONTROL Environment] klug auf der rechten Seite, wenn die linke Seite vordefinierte Attribute oder benutzerdefinierte Attribute aufweist.

![Bild links_rechts](assets/left_right.png)

Die folgende Tabelle enthält wirksame Regeln und Regeln, die während der Laufzeit möglicherweise nicht kompatibel sind:

| Kompatible Regeln | Potenziell inkompatible Regeln |
|--- |--- |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - salesValue | salesValue - ist zwischen - 90 % und 110 % des aktuellen Elements - value |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - value | clearancePrice - ist zwischen - 90 % und 110 % des aktuellen Elements - margin |
| margin - ist zwischen - 90 % und 110 % des aktuellen Elements - margin | storeInventory - gleich - dem aktuellen Element - inventory |
| inventory - gleich - dem aktuellen Element - inventory |  |
