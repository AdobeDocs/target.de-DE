---
keywords: Einschlussregeln; Aufnahmekriterien; Empfehlungen; neue Kriterien erstellen; Promotion; Promotions; dynamischer Filter; dynamisch; leere Werte; Filterregel ignorieren; statischer Filter; Filtern nach Wert; Entitätsattributübereinstimmung; Profilattributübereinstimmung; Parameterübereinstimmung; Filtern nach Wert; statischer Filter
description: Erfahren Sie, wie Sie in [!DNL Target] Recommendations für Kriterien und Promotions Einschlussregeln erstellen.
title: Verwenden dynamischer und statischer Einschlussregeln
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
TQID: 'https://experienceleague.adobe.com/PM9h863-uQWm3wrU7OVWfmnqQgyUGmF7QFpTUaAZuCQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 7%
---
# Verwenden dynamischer und statischer Einschlussregeln {#inclusion-rules}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie in [!DNL Adobe Target Recommendations] dynamische und statische Filterregeln zu Kriterien und Promotions hinzufügen.

>[!ENDSHADEBOX]

Einschlussregeln grenzen die Elemente ein, die in Empfehlungen angezeigt werden können. Sie werden für Kriterien und Promotions in [!DNL Adobe Target] mit dynamischen oder statischen Filterregeln erstellt. Der Prozess, die Anwendungsfälle und die Beispiele für sind bei Kriterien und Promotions ähnlich, sodass diese Seite beide abdeckt.

## Filterregeln hinzufügen {#add-filtering-rules}

Die folgenden Schritte fügen Kriterien eine Filterregel hinzu.

1. Klicken [ beim Erstellen von ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#create-criteria) (**[!UICONTROL Empfehlungen]** > **[!UICONTROL Kriterien]** > **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**) **[!UICONTROL Filterregel hinzufügen]** unter **[!UICONTROL Einschlussregeln]**.

   ![Filterregel hinzufügen](/help/main/c-recommendations/c-algorithms/assets/add-fitering-rule.png)

1. Klicken Sie im Feld „Welchen anderen Regeln sollte die Empfehlung entsprechen?“ auf **[!UICONTROL Dropdown-Liste „Statischer Filter]** und wählen Sie dann die gewünschte Option aus.

   ![Dropdown-Liste „Statischer Filter“](/help/main/c-recommendations/c-algorithms/assets/dynamic-and-static.png)

   Die verfügbaren Optionen variieren je nach vertikalem Markt und Empfehlungsschlüssel.

Um einer Promotion eine Filterregel hinzuzufügen, wählen Sie beim Erstellen der Promotion **[!UICONTROL Nach Attribut]**[ aus ](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) klicken Sie dann auf **[!UICONTROL Filterregel hinzufügen]**.

## Filtertypen {#filter-types}

In den folgenden Abschnitten werden die Filteroptionen für **[!UICONTROL Dynamische Filterung]** und **[!UICONTROL Nach Wert filtern]** sowohl für Kriterien als auch für Promotions beschrieben.

### Dynamische Filterung

Dynamische Einschlussregeln passen sich an den Besucher oder die Anfrage an, während statische Einschlussregeln feste Werte verwenden.

* Dynamische Einschlussregeln liefern Empfehlungen, indem sie ein -Attribut in einem Profilparameter des Benutzers oder in einem Mbox-Aufruf zuordnen.

  Beispielsweise kann eine Empfehlung des Typs „Beliebteste Kriterien“ erstellt werden. Aus dem Satz der zurückgegebenen Empfehlungen kann jede Empfehlung (in Echtzeit) anhand eines Attributs herausgefiltert werden, das übergeben wird, wenn der Benutzer auf eine Seite zugreift, auf der die Empfehlungen angezeigt werden.

* Es können beliebig viele dynamische Einschlussregeln erstellt werden. Die Einschlussregeln sind mit einem AND-Operator verknüpft, sodass alle Regeln erfüllt sein müssen, damit ein Element in einer Empfehlung enthalten ist.

Die folgenden Optionen stehen für die dynamische Filterung zur Verfügung:

| Dynamische Filteroption | Details |
| --- | --- |
| [**[!UICONTROL Entitätsattributübereinstimmung]**](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Dynamisches Filtern durch Vergleichen eines Pools potenzieller empfohlener Elemente mit einem bestimmten Element, mit dem der Besucher interagiert hat.<P>Verwenden Sie **[!UICONTROL Entitätsattributabgleich]** um Empfehlungen anzuzeigen, die den Besucher mit hoher Wahrscheinlichkeit ansprechen, z. B. die Lieblingsmarke des Besuchers. |
| [**[!UICONTROL Profilattributübereinstimmung]**](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Dynamisches Filtern durch Vergleichen von Elementen (Entitäten) mit einem Wert im Profil des Besuchers.<P>Verwenden Sie **[!UICONTROL Profilattributabgleich]** um Empfehlungen anzuzeigen, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. Größe oder Lieblingsmarke. |
| [**[!UICONTROL Parameterübereinstimmung]**](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Dynamisches Filtern durch Vergleichen von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).<P>Verwenden Sie **[!UICONTROL Parameterübereinstimmung]** um Inhalte zu empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Geräteabmessungen oder Geografie. |

### Nach Wert filtern

Statische Regeln beschränken, welche Elemente in der Empfehlung enthalten sind, anstatt Sammlungen zu verwenden. Die folgende Option ist zum Filtern nach Wert verfügbar:

| Option „Nach Wert filtern“ | Details |
| --- | --- |
| [**[!UICONTROL Statischer Filter]**](/help/main/c-recommendations/c-algorithms/static-value.md) | Filtert nach einem oder mehreren statischen Werten, die manuell eingegeben werden. |

## Verfügbare Operatoren {#operators}

Die folgenden Beispiele zeigen, wie dynamische Promotions und Ausschlüsse für das Marketing verwendet werden können.

>[!NOTE]
>
>Die „list“-Operatoren erfordern, dass sowohl die Entitäten als auch die Profilattribute als Arrays gespeichert werden. Eine kommagetrennte Liste funktioniert nicht.

| Benutzerin oder Benutzer | Verfügbar in | Beispiele |
|--- |--- |--- |
| **[!UICONTROL Entspricht einem von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), können dynamische Promotions, die den Operator „Gleich“ verwenden, andere Elemente über Folgendes bewerben:<ul><li>Dieselbe Marke</li><li>Dieselbe Kategorie</li><li>Dieselbe Kategorie UND von der Hausmarke</li><li>Selber Store</li></ul> |
| **[!UICONTROL Entspricht keinem von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), können dynamische Promotions, die den Operator &quot;**[!UICONTROL entspricht keinem von]** verwenden, andere Elemente über Folgendes bewerben:<ul><li>Eine andere Fernsehserie</li><li>Ein anderes Genre</li><li>Eine andere Produktreihe</li><li>Eine andere Stil-ID</li></ul> |
| **[!UICONTROL ist größer oder gleich einem von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt), kann der Operator &quot;**[!UICONTROL ist größer oder gleich einem von]** andere Elemente bewerben, die:<ul><li>Kosten gleich oder sind teurer</li></ul> |
| **[!UICONTROL ist kleiner oder gleich einem der folgenden Werte]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt), kann der Operator &quot;**[!UICONTROL ist kleiner oder gleich einem von]** andere Elemente bewerben, die:<ul><li>Die Kosten sind gleich oder billiger</li></ul> |
| **[!UICONTROL enthält beliebige von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt), kann der Operator &quot;**[!UICONTROL enthält beliebige von]** andere Elemente weiterleiten, die:<ul><li>Titel enthält dieselbe Marke</li></ul> |
| **[!UICONTROL enthält keinen von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt), kann der Operator &quot;**[!UICONTROL enthält keine von]** andere Elemente weiterleiten, die:<ul><li>Titel enthält kein Schimpfwort</li></ul> |
| **[!UICONTROL Beginnt mit einem von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt), kann der Operator &quot;**[!UICONTROL beginnt mit einem von]** andere Elemente weiterleiten, die:<ul><li>Produktname beginnt mit iPhone</li></ul> |
| **[!UICONTROL Endet mit einem von]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]**, **[!UICONTROL Parameterabgleich]** und **[!UICONTROL statischer Filter]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt), kann der Operator &quot;**[!UICONTROL endet mit einem von]** andere Elemente weiterleiten, die:<ul><li>Der Inhalt endet mit EN, was die englische Sprache angibt</li></ul> |
| **[!UICONTROL liegt zwischen]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Wenn ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), können dynamische Promotions, die den Operator &quot;**[!UICONTROL ist zwischen]** verwenden, für andere Elemente werben, die:<ul><li>teurer</li><li>Weniger teuer</li><li>Kosten plus oder minus 30 %</li><li>Spätere Folgen in derselben Staffel</li><li>Vorherige Bücher in einer Reihe</li></ul> |
| **[!UICONTROL Liste enthält ein Element in]** (Liste auf der rechten Seite) | **[!UICONTROL Profilattributübereinstimmung]** und **[!UICONTROL Parameterübereinstimmung]** | Wenn bei der Zuordnung von Profilattributen ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), kann der Operator &quot;**[!UICONTROL Liste enthält ein Element in]**&quot; andere Elemente weiterleiten, die:<ul><li>Verfügbar in der Geografie des Besuchers</li></ul>**Beispiel**: Empfehlen Sie Elemente, die nur im geografischen Bereich des Besuchers verfügbar sind.<P>Die Filterregel könnte wie folgt aussehen:<P>`availableGeographies list contains an item in user.currentGeography`<P>**Hinweis**: Wenn dieser Operator verwendet wird, wird eine Liste auf der [ Seite ](#caveats) Regel erwartet. |
| **[!UICONTROL Liste enthält kein Element in]** (Liste auf der rechten Seite) | **[!UICONTROL Profilattributübereinstimmung]** und **[!UICONTROL Parameterübereinstimmung]** | Wenn bei der Zuordnung von Profilattributen ein Besucher ein Element auf der Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), kann der Operator &quot;**[!UICONTROL Liste enthält kein Element in]**&quot; andere Elemente ausschließen, die:<ul><li>In der Liste der letzten zehn Elemente, die der Besucher angezeigt hat</li></ul>**Beispiel**: Elemente, die der Besucher kürzlich angesehen und an denen er kein Interesse gezeigt hat, werden nicht beworben.<P>Die Filterregel könnte wie folgt aussehen:<P>`id is not contained in list user.lastViewedItems`<P>**Hinweis**: Wenn dieser Operator verwendet wird, wird eine Liste auf der [ Seite ](#caveats) Regel erwartet. |
| **[!UICONTROL Liste enthält ein Element in]** (Listen auf beiden Seiten) | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Wenn bei der Zuordnung von Profilattributen ein Besucher ein Element auf der Website aufruft (z. B. ein Sportereignis oder ein Konzert), kann der Operator &quot;**[!UICONTROL Liste enthält ein Element in]**&quot; andere Elemente bewerben, die:<ul><li>Einer der Lieblingsmannschaften des Besuchers zugeordnet</li></ul>**Beispiel**: Empfehlen Sie Spiele, die einem der Lieblingsteams des Besuchers zugeordnet sind.<P>Die Filterregel könnte wie folgt aussehen:<P>`teamsPlaying list contains an item in user.favoriteTeams`<P>**Hinweis**: Wenn dieser Operator verwendet wird, wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |
| **[!UICONTROL Liste enthält kein Element in]** (Listen auf beiden Seiten) | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Wenn ein Besucher bei der Parameterübereinstimmung ein Element auf der Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film), kann der Operator &quot;**[!UICONTROL Liste enthält kein Element in]** andere Elemente ausschließen, die:<ul><li>In einer Liste verbotener Typen enthalten</li></ul>**Beispiel**: Elemente, die nur für erwachsene Besucher verfügbar sind, wie Tabak und Alkohol, sind ausgeschlossen.<P>Die Filterregel könnte wie folgt aussehen:<P>`itemType is not contained in list mbox.prohibitedTypes`<P>**Hinweis**: Wenn dieser Operator verwendet wird, wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |
| **[!UICONTROL Liste enthält alle Elemente in]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Wenn bei der Zuordnung von Profilattributen ein Besucher ein Element auf der Website aufruft (z. B. eine Stellenausschreibung oder ein Rezept), kann der Operator &quot;**[!UICONTROL enthält alle Elemente in]**&quot; andere Elemente hochstufen, die:<ul><li>Eine Reihe von Fähigkeiten einschließen</li><li>Eine Reihe erforderlicher Inhaltsstoffe einschließen</li></ul>**Beispiel 1**: Ein Besucher verfügt über eine Reihe von Kenntnissen (Java, C++ und HTML). Die Elemente im Katalog sind Aufträge mit den erforderlichen Kenntnissen (Java und HTML). Das Besucherprofil muss alle erforderlichen Fähigkeiten enthalten, bevor der Auftrag dem Besucher empfohlen wird.<P>Die Filterregel könnte wie folgt aussehen:<P>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<P>**Beispiel 2**: Ein Benutzer hat eine Liste von Speisekammer-Zutaten. Das Rezept enthält eine Liste der erforderlichen Zutaten. Das Besucherprofil muss alle erforderlichen Zutaten enthalten, bevor das Rezept dem Besucher empfohlen wird.<P>Die Filterregel könnte wie folgt aussehen:<P>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<P>**Hinweis**: Wenn dieser Operator verwendet wird, wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |
| **[!UICONTROL Liste enthält nicht alle Elemente in]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Wenn bei der Zuordnung von Entitätsattributen ein Besucher ein Element auf der Website anzeigt (z. B. ein Sportereignis oder ein Konzert), kann der Operator &quot;**[!UICONTROL Liste enthält nicht alle]** Elemente“ andere Elemente bewerben, die:<ul><li>Keine Gruppe von Teams einschließen</li></ul>**Beispiel**: Ein Sportereignis umfasst zwei Teams. Das Profil des Besuchers gibt an, dass dieser Besucher keine Spiele für diese Teams anzeigen möchte. Daher darf ein Spiel nicht empfohlen werden, wenn diese Teams spielen.<P>Die Filterregel könnte wie folgt aussehen:<P>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<P>**Hinweis**: Wenn dieser Operator verwendet wird, wird eine Liste auf [ Seiten ](#caveats) Regel erwartet. |

## Verarbeiten leerer Werte {#empty-values}

Es stehen mehrere Optionen zur Verfügung, um leere Werte bei der Filterung nach **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** für Kriterien und Promotions zu verarbeiten.

Zuvor wurden bei einem leeren Wert keine Ergebnisse zurückgegeben. Die Dropdown-Liste *Wenn x* leer ist“ gibt die Aktion an, die ausgeführt werden soll, wenn die Kriterien leere Werte aufweisen, wie in der folgenden Abbildung dargestellt:

![Optionen für leere Werte](/help/main/c-recommendations/c-algorithms/assets/empty_value.png)

Um die gewünschte Aktion auszuwählen, bewegen Sie den Mauszeiger über das Zahnradsymbol ( ![Zahnradsymbol](/help/main/c-recommendations/c-algorithms/assets/icon_gear.png) ) und wählen Sie dann die gewünschte Aktion aus:

| Aktion | Verfügbar für | Details |
|--- |--- |--- |
| **[!UICONTROL Diese Filterregel ignorieren]** | **[!UICONTROL Profilattributübereinstimmung]** und **[!UICONTROL Parameterübereinstimmung]** | Diese Aktion ist die Standardaktion für **[!UICONTROL Profilattributübereinstimmung]** und **[!UICONTROL Parameterübereinstimmung]**.<P>Die Regel wird ignoriert. Wenn es beispielsweise drei Filterregeln gibt und die dritte Regel keine Werte übergibt, kann die dritte Regel mit den leeren Werten ignoriert werden, anstatt keine Ergebnisse zurückzugeben. |
| **[!UICONTROL Für diese Kriterien keine Ergebnisse anzeigen]**<P>(Nur Kriterien) | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Diese Aktion ist die Standardaktion für **[!UICONTROL Entitätsattributübereinstimmung]**.<P>[!DNL Target] Mit dieser Aktion werden leere Werte behandelt, bevor diese Option hinzugefügt wurde: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| **[!UICONTROL Keine Elemente hochstufen]**<P>(Nur Promotions) | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Diese Aktion ist die Standardaktion für **[!UICONTROL Entitätsattributübereinstimmung]**.<P>Diese Aktion behandelt leere Werte, [!DNL Target] vor dem Hinzufügen dieser Option verarbeitet wurden: Es werden keine Ergebnisse für diese Promotion angezeigt. |
| **[!UICONTROL Einen statischen Wert verwenden]** | **[!UICONTROL Entitätsattributabgleich]**, **[!UICONTROL Profilattributabgleich]** und **[!UICONTROL Parameterabgleich]** | Ein statischer Wert kann verwendet werden, wenn ein Wert leer ist. |

## Einschränkungen {#caveats}

>[!IMPORTANT]
>
>Verschiedene Datentypattribute sind in dynamischen Kriterien oder Promotions zur Laufzeit möglicherweise nicht mit den Operatoren „ist gleich“ und „ist nicht gleich“ kompatibel. Wenn die linke Seite über vordefinierte Attribute oder benutzerdefinierte Attribute verfügt, wählen Sie die Werte **[!UICONTROL Wert]**, **[!UICONTROL Spanne]**, **[!UICONTROL Inventar]** und **[!UICONTROL Umgebung]** auf der rechten Seite sorgfältig aus.

![Linke und rechte Seite einer Filterregel](/help/main/c-recommendations/c-algorithms/assets/left_right.png)

Die folgende Tabelle zeigt kompatible Regeln und Regeln, die zur Laufzeit möglicherweise nicht kompatibel sind:

| Kompatible Regeln | Potenziell inkompatible Regeln |
|--- |--- |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - salesValue | salesValue - ist zwischen - 90 % und 110 % des aktuellen Elements - value |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - value | clearancePrice - ist zwischen - 90 % und 110 % des aktuellen Elements - margin |
| margin - ist zwischen - 90 % und 110 % des aktuellen Elements - margin | storeInventory - gleich - dem aktuellen Element - inventory |
| inventory - gleich - dem aktuellen Element - inventory |  |
