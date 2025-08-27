---
keywords: Einschlussregeln; Aufnahmekriterien; Empfehlungen; neue Kriterien erstellen; Promotion; Promotions; dynamischer Filter; dynamisch; leere Werte; Filterregel ignorieren; statischer Filter; Filtern nach Wert; Entitätsattributübereinstimmung; Profilattributübereinstimmung; Parameterübereinstimmung; Filtern nach Wert; statischer Filter
description: Erfahren Sie, wie Sie in  [!DNL Target] Recommendations für Kriterien und Promotions Einschlussregeln erstellen.
title: Wie verwende ich dynamische und statische Einschlussregeln in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 51e484d54f4d318ea59fdfdb16d1ed7014abdfdb
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 16%

---

# Verwenden dynamischer und statischer Einschlussregeln

Erstellen Sie Einschlussregeln für Kriterien und Promotions in [!DNL Adobe Target] und fügen Sie dynamische oder statische Filterregeln hinzu, um bessere Ergebnisse für Ihre Empfehlungen zu erzielen.

Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. Sowohl Kriterien und Promotions als auch die Verwendung von Einschlussregeln werden in diesem Abschnitt behandelt.

## Filterregeln zu Kriterien und Promotions hinzufügen {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

### Filterregeln zu Kriterien hinzufügen

1. Klicken [ beim Erstellen von ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) (**[!UICONTROL Recommendations]> [!UICONTROL Criteria] > [!UICONTROL Create Criteria] >[!UICONTROL Create Criteria]**) unter **[!UICONTROL Add Filtering Rule]** auf **[!UICONTROL Inclusion Rules]**.

   ![Filterregel hinzufügen](/help/main/c-recommendations/c-algorithms/assets/add-fitering-rule.png)

1. Klicken Sie auf **Statischer Filter** Dropdown-Liste im Feld „Welchen anderen Regeln sollte die Empfehlung folgen?“ und wählen Sie dann die gewünschte Option aus der [!UICONTROL Static Filter] Dropdown-Liste.

   ![Dropdown-Liste „Statischer Filter“](/help/main/c-recommendations/c-algorithms/assets/dynamic-and-static.png)

   Die verfügbaren Optionen variieren je nach vertikalem Markt und Empfehlungsschlüssel.

### Filterregeln zu Promotions hinzufügen

1. Wählen [ beim Erstellen einer Promotion ](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14) Option **[!UICONTROL Promote by Attribute]** aus und klicken Sie dann auf **[!UICONTROL Add Filtering Rule]**.

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In den folgenden Abschnitten werden die Arten von Filteroptionen für [!UICONTROL Dynamic Filtering] und [!UICONTROL Filter by Value] sowohl für Kriterien als auch für Promotions aufgeführt:

### Dynamische Filterung

Dynamische Einschlussregeln sind leistungsfähiger als statische Einschlussregeln und liefern bessere Ergebnisse und bessere Interaktionen. Beachten Sie Folgendes:

* Dynamische Einschlussregeln liefern Empfehlungen, indem sie ein Attribut im Profilparameter eines Benutzers oder in einem Mbox-Aufruf zuordnen.

  Sie können beispielsweise eine Empfehlung vom Typ „Beliebteste Kriterien“ erstellen. Aus dem Satz der zurückgegebenen Empfehlungen können Sie alle Empfehlungen (in Echtzeit) nach einem Attribut filtern, das übergeben wird, wenn der Benutzer auf eine Seite zugreift, auf der die Empfehlungen angezeigt werden.

* Verwenden Sie statische Regeln, um zu begrenzen, welche Elemente in der Empfehlung enthalten sind (anstatt Sammlungen zu verwenden).

* Sie können so viele dynamische Einschlussregeln wie nötig erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Die folgenden Optionen stehen für die dynamische Filterung zur Verfügung:

| Dynamische Filteroption | Details |
| --- | --- |
| [[!UICONTROL Entity Attribute Matching]](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Dynamisches Filtern durch Vergleichen eines Pools potenzieller Recommendations-Elemente mit einem bestimmten Element, mit dem die Benutzenden interagiert haben.<P>Verwenden Sie [!UICONTROL Entity Attribute Matching], wenn Sie Empfehlungen anzeigen möchten, die für den Besucher am wahrscheinlichsten sind, z. B. die Lieblingsmarke des Besuchers. |
| [[!UICONTROL Profile Attribute Matching]](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Dynamisches Filtern durch Vergleichen von Elementen (Entitäten) mit einem Wert im Benutzerprofil.<P>Verwenden Sie [!UICONTROL Profile Attribute Matching], wenn Sie Empfehlungen anzeigen möchten, die einem im Besucherprofil gespeicherten Wert entsprechen, z. B. Größe oder Lieblingsmarke. |
| [[!UICONTROL Parameter Matching]](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Dynamisches Filtern durch Vergleichen von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).<P>Verwenden Sie [!UICONTROL Parameter Matching], um Inhalte zu empfehlen, die den Seitenparametern oder den Parametern des Besuchers entsprechen, z. B. Geräteabmessungen oder Geografie. |

### Nach Wert filtern

Die folgende Option ist zum Filtern nach Wert verfügbar:

| Option „Nach Wert filtern“ | Details |
| --- | --- |
| [[!UICONTROL Static Filter]](/help/main/c-recommendations/c-algorithms/static-value.md) | Geben Sie zum Filtern manuell einen oder mehrere statische Werte ein. |

## Verfügbare Operatoren {#operators}

Dynamische Kriterien und Promotions sind viel leistungsfähiger als statische Kriterien und Promotions und liefern bessere Ergebnisse und Interaktionen.

Die folgenden Beispiele bieten allgemeine Ideen dazu, wie Sie dynamische Promotions und Ausschlüsse in Ihren Marketing-Maßnahmen verwenden können:

>[!NOTE]
>
>„Liste“ erfordert, dass sowohl die Entitäten als auch die Profilattribute als Arrays gespeichert werden. Eine kommagetrennte Liste funktioniert nicht.

| Benutzerin oder Benutzer | Beispiele |
| --- | --- |
| [!UICONTROL equals any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator „ist gleich“ in dynamischen Werbeaktionen können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), andere Elemente von bewerben:<ul><li>Dieselbe Marke</li><li>Dieselbe Kategorie</li><li>Dieselbe Kategorie UND von der Hausmarke</li><li>Selber Store</li></ul> |
| [!UICONTROL does not equal any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL does not equal any of]&quot; in dynamischen Werbeaktionen können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), andere Elemente von bewerben:<ul><li>Eine andere Fernsehserie</li><li>Ein anderes Genre</li><li>Eine andere Produktreihe</li><li>Eine andere Stil-ID</li></ul> |
| [!UICONTROL is greater than or equal to any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL is greater than or equal to any of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt), andere Elemente weiterleiten, die:<ul><li>Kosten gleich oder sind teurer</li></ul> |
| [!UICONTROL is less than or equal to any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL is less than or equal to an of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt), andere Elemente weiterleiten, die:<ul><li>Die Kosten sind gleich oder billiger</li><li>Geringere Kosten ausschließen</li></ul> |
| [!UICONTROL contains any of] (Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL contains any of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt), andere Elemente weiterleiten, die:<ul><li>Titel enthält dieselbe Marke</li></ul> |
| [!UICONTROL does not contain any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator „enthält keinen von“ können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt), andere Elemente bewerben, die:<ul><li>Titel enthält kein Schimpfwort</li></ul> |
| [!UICONTROL starts with any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL starts with an of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt), andere Elemente weiterleiten, die:<ul><li>Produktname beginnt mit iPhone</li></ul> |
| [!UICONTROL ends with any of]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] und [!UICONTROL Static Filter].) | Mit dem Operator &quot;[!UICONTROL ends with an of]&quot; können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt), andere Elemente weiterleiten, die:<ul><li>Inhalt endet mit EN, was auf Englisch hinweist</li></ul> |
| [!UICONTROL is between]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator „i[!UICONTROL s between]&quot; in dynamischen Werbeaktionen können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), für andere Elemente werben, die:<ul><li>teurer</li><li>Weniger teuer</li><li>Kosten plus oder minus 30 %</li><li>Spätere Folgen in derselben Staffel</li><li>Vorherige Bücher in einer Reihe</li></ul> |
| [!UICONTROL list contains an item in]<P>(Verfügbar mit [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list contains an item in]&quot; bei der Profilattributübereinstimmung können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), andere Elemente weiterleiten, die:<ul><li>Verfügbar in der Geografie des Besuchers</li></ul>**Beispiel**: Sie möchten Elemente empfehlen, die nur im geografischen Bereich eines Besuchers verfügbar sind.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`availableGeographies list contains an item in user.currentGeography`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf der [ Seite ](#caveats) Regel erwartet. |
| [!UICONTROL list does not contain an item in]<P>(Verfügbar mit [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list does not contain an item in]&quot; bei der Profilattributübereinstimmung können Sie beim Anzeigen eines Elements auf Ihrer Website durch einen Besucher (z. B. ein Produkt, einen Artikel oder einen Film) andere Elemente ausschließen, die:<ul><li>In der Liste der letzten zehn Elemente, die der Besucher angezeigt hat</li></ul></ul>**Beispiel**: Sie möchten keine Elemente bewerben, die der Besucher kürzlich angesehen hat und an denen er kein Interesse gezeigt hat.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`id is not contained in list user.lastViewedItems`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf der [ Seite ](#caveats) Regel erwartet. |
| [!UICONTROL list contains an item in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list contains an item in]&quot; bei der Zuordnung von Profilattributen können Sie, wenn ein Besucher ein Element auf Ihrer Website aufruft (z. B. ein Sportereignis oder ein Konzert), andere Elemente bewerben, die:<ul><li>Einem der Lieblings-Teams des Besuchers zugeordnet</li></ul>**Beispiel**: Sie möchten Spiele empfehlen, die mit einem der Lieblings-Teams des Besuchers verknüpft sind.<P>Ihre Filterregel könnte wie folgt aussehen:<P>` teamsPlaying list contains an item in user.favoriteTeams`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |
| [!UICONTROL list does not contain an item in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Wenn Sie den Operator &quot;[!UICONTROL list does not contain an item in]&quot; bei der Parameterattributübereinstimmung verwenden, können Sie beim Anzeigen eines Elements auf Ihrer Website (z. B. eines Produkts, Artikels oder Films) andere Elemente ausschließen, die:<ul><li>In einer Liste verbotener Typen enthalten</li></ul>**Beispiel**: Sie möchten Elemente ausschließen, die für erwachsene Besucher verfügbar sind, z. B. Tabak und Alkohol.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`itemType is not contained in list mbox.prohibitedTypes`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |
| [!UICONTROL list contains all items in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list does not contain an item in]&quot; bei der Profilattributübereinstimmung können Sie, wenn ein Besucher ein Element auf Ihrer Website aufruft (z. B. eine Stellenausschreibung oder ein Rezept), andere Elemente weiterleiten, die:<ul><li>Eine Reihe von Fähigkeiten einschließen</li><li>Eine Reihe erforderlicher Inhaltsstoffe einschließen</li></ul>**Beispiel 1**: Angenommen, ein Besucher verfügt über bestimmte Fähigkeiten (Java, C++ und HTML). Die Elemente im Katalog sind Aufträge mit den erforderlichen Kenntnissen (Java und HTML). Sie sollten sicherstellen, dass das Besucherprofil alle erforderlichen Fähigkeiten enthält, bevor Sie den Auftrag dem Besucher empfehlen.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<P>**Beispiel 2**: Angenommen, ein Benutzer hat eine Liste von Speisekammer-Zutaten. Das Rezept enthält eine Liste der erforderlichen Zutaten. Sie sollten sicherstellen, dass das Besucherprofil alle erforderlichen Inhaltsstoffe enthält, bevor Sie dem Besucher das Rezept empfehlen.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |
| [!UICONTROL list does not contain all items in]<P>(Verfügbar mit [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].) | Mit dem Operator &quot;[!UICONTROL list does not contain all items in]&quot; bei der Zuordnung von Entitätsattributen können Sie, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Sportereignis oder ein Konzert), andere Elemente bewerben, die:<ul><li>Keine Gruppe von Teams einschließen</li></ul>**Beispiel**: Angenommen, ein Sportereignis umfasst zwei Teams. Das Besucherprofil gibt an, dass dieser Besucher keine Spiele für diese Teams anzeigen möchte. Sie möchten sicherstellen, dass Sie kein Spiel empfehlen, wenn diese Teams spielen.<P>Ihre Filterregel könnte wie folgt aussehen:<P>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<P>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |

## Umgang mit leeren Werten beim Filtern nach [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Sie können mehrere Optionen auswählen, um leere Werte zu verarbeiten, wenn Sie nach [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] nach Ausstiegskriterien und Promotions filtern.

Zuvor wurden bei einem leeren Wert keine Ergebnisse zurückgegeben. In der Dropdownliste „Wenn *x* leer ist“ können Sie die entsprechende Aktion auswählen, die ausgeführt werden solle, wenn die Kriterien leere Werte enthalten, wie in der folgenden Abbildung dargestellt:

![empty_value Bild](assets/empty_value.png)

Um die gewünschte Aktion auszuwählen, bewegen Sie den Mauszeiger über das Zahnradsymbol (![icon_gear image](assets/icon_gear.png)) und wählen Sie dann die gewünschte Aktion aus:

| Aktion | Verfügbar für | Details |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Diese Aktion ist die Standardaktion für [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching].<P>Diese Option gibt an, dass die Regel ignoriert wird. Wenn beispielsweise drei Filterregeln vorhanden sind und die dritte Regel keine Werte übergibt, können Sie die dritte Regel mit den leeren Werten einfach ignorieren, statt gar keine Ergebnisse zurückzugeben. |
| [!UICONTROL Do not show any results for this criteria]<P>(Nur Kriterien) | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Diese Aktion ist die Standardeinstellung für [!UICONTROL Entity Attribute Matching].<P>Mit dieser Aktion werden [!DNL Target] leeren Werte vor dem Hinzufügen dieser Option verarbeitet: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| [!UICONTROL Keine Elemente hochstufen<P>(Nur Promotions)] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Diese Aktion ist die Standardeinstellung für [!UICONTROL Entity Attribute Matching].<P>Mit dieser Aktion werden [!DNL Target] leeren Werte vor dem Hinzufügen dieser Option verarbeitet: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] und [!UICONTROL Parameter Matching] | Wenn ein Wert leer ist, können Sie die Verwendung eines statischen Werts festlegen. |

## Einschränkungen  {#caveats}

>[!IMPORTANT]
>
>Verschiedene Datentypattribute sind möglicherweise nicht mit dynamischen Kriterien oder Promotions kompatibel, während sie zur Laufzeit mit den Operatoren „ist gleich“ und „ist nicht gleich“ verwendet werden. Verwenden Sie [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] und [!UICONTROL Environment] Werte auf der rechten Seite, wenn die linke Seite vordefinierte Attribute oder benutzerdefinierte Attribute aufweist.

![left_right Bild](assets/left_right.png)

Die folgende Tabelle enthält wirksame Regeln und Regeln, die während der Laufzeit möglicherweise nicht kompatibel sind:

| Kompatible Regeln | Möglicherweise inkompatible Regeln |
|--- |--- |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - salesValue | salesValue - ist zwischen - 90 % und 110 % des aktuellen Elements - value |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - value | clearancePrice - ist zwischen - 90 % und 110 % des aktuellen Elements - margin |
| margin - ist zwischen - 90 % und 110 % des aktuellen Elements - margin | storeInventory - gleich - dem aktuellen Element - inventory |
| inventory - gleich - dem aktuellen Element - inventory |  |
