---
keywords: Einschlussregeln; Aufnahmekriterien; Empfehlungen; neue Kriterien erstellen; Promotion; Promotions; dynamischer Filter; dynamisch; leere Werte; Filterregel ignorieren; statischer Filter; Filtern nach Wert; Entitätsattributübereinstimmung; Profilattributübereinstimmung; Parameterübereinstimmung; Filtern nach Wert; statischer Filter
description: Erfahren Sie, wie Sie in Adobe Einschlussregeln erstellen. [!DNL Target] Recommendations für Kriterien und Promotions. Um bessere Ergebnisse zu erzielen, fügen Sie dynamischere oder statische Filterregeln hinzu.
title: Wie verwende ich dynamische und statische Einschlussregeln in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '2093'
ht-degree: 16%

---

# Verwenden dynamischer und statischer Einschlussregeln

Informationen zum Erstellen von Einschlussregeln für Kriterien und Promotions in [!DNL Adobe Target] und fügen Sie dynamische oder statische Filterregeln hinzu, um bessere Ergebnisse für Ihre Empfehlungen zu erzielen.

Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. Kriterien und Promotions sowie die Verwendung von Einschlussregeln werden in diesem Abschnitt behandelt.

## Hinzufügen von Filterregeln zu Kriterien {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Klicken Sie beim [Erstellen von Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) auf **[!UICONTROL Filterregel hinzufügen]** unter **[!UICONTROL Einschlussregeln]**.

![include_options_new image](assets/inclusion_options_new.png)

Die verfügbaren Optionen variieren je nach vertikalem Markt und Empfehlungsschlüssel.

## Hinzufügen von Filterregeln zu Promotions  {#section_D59AFB62E2EE423086281CF5D18B1076}

Wählen Sie beim [Erstellen einer Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14) die Option **[!UICONTROL Hervorheben nach Attribut]** aus und klicken Sie dann auf **[!UICONTROL Filterregel hinzufügen]**.

![include_options-Bild](assets/inclusion_options.png)

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In den folgenden Abschnitten werden die Filteroptionen für [!UICONTROL Dynamische Filterung] und [!UICONTROL Nach Wert filtern] für Kriterien und Promotions:

### Dynamische Filterung

Dynamische Einschlussregeln sind leistungsstärker als statische Einschlussregeln und liefern bessere Ergebnisse und Interaktionen. Beachten Sie Folgendes:

* Dynamische Einschlussregeln liefern Empfehlungen, indem sie ein Attribut im Profilparameter eines Benutzers oder in einem Mbox-Aufruf abgleichen.

   Sie können beispielsweise die Empfehlung &quot;Bevorzugte Kriterien&quot;erstellen. Aus dem Satz der zurückgegebenen Empfehlungen können Sie alle Empfehlungen (in Echtzeit) nach einem Attribut filtern, das übergeben wird, wenn der Benutzer auf eine Seite zugreift, auf der die Empfehlungen angezeigt werden.

* Verwenden Sie statische Regeln, um zu begrenzen, welche Artikel in der Empfehlung enthalten sind (anstatt Sammlungen zu verwenden).

* Sie können so viele dynamische Einschlussregeln wie nötig erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Die folgenden Optionen stehen für die dynamische Filterung zur Verfügung:

| Dynamische Filteroption | Details |
| --- | --- |
| [Entitätsattributübereinstimmung](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Dynamisches Filtern durch Vergleich eines Pools potenzieller Empfehlungselemente mit einem bestimmten Element, mit dem die Benutzer interagiert haben.<br>Verwendung [!UICONTROL Entitätsattributübereinstimmung] , wenn Sie Empfehlungen anzeigen möchten, die am ehesten an den Besucher appellieren, z. B. an die Lieblingsmarke des Besuchers. |
| [Profilattributübereinstimmung](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Dynamisches Filtern durch Vergleich von Elementen (Entitäten) mit einem Wert im Benutzerprofil.<br>Verwendung [!UICONTROL Profilattributübereinstimmung] wenn Sie Empfehlungen anzeigen möchten, die mit einem im Besucherprofil gespeicherten Wert übereinstimmen, z. B. Größe oder Lieblingsmarke. |
| [Parameterübereinstimmung](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Dynamisches Filtern per Vergleich von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).<br>Verwendung [!UICONTROL Parameterübereinstimmung] , um Inhalte zu empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Gerätedimensionen oder Geolokation. |

### Nach Wert filtern

Die folgende Option ist zum Filtern nach Wert verfügbar:

| Option &quot;Filtern nach Wert&quot; | Details |
| --- | --- |
| [Statischer Filter](/help/main/c-recommendations/c-algorithms/static-value.md) | Geben Sie einen oder mehrere zu filternde statische Werte manuell ein. |

## Verfügbare Operatoren {#operators}

Dynamische Kriterien und Promotions sind viel leistungsfähiger als statische Kriterien und Promotions und liefern bessere Ergebnisse und Interaktionen.

Die folgenden Beispiele enthalten allgemeine Ideen zur Verwendung dynamischer Promotions und Ausschlüsse in Ihren Marketing-Maßnahmen:

| Benutzerin oder Benutzer | Beispiele |
| --- | --- |
| Gleich<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Wenn Sie den Operator &quot;gleich&quot;in dynamischen Promotions verwenden, können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, weitere Elemente bewerben, die folgende Kriterien erfüllen:<ul><li>Dieselbe Marke</li><li>Dieselbe Kategorie</li><li>Dieselbe Kategorie UND von der Hausmarke</li><li>Derselbe Store</li></ul> |
| Does Not Equal<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Wenn Sie den Operator &quot;ist nicht gleich&quot;in dynamischen Promotions verwenden, können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, weitere Elemente bewerben, die folgende Kriterien erfüllen:<ul><li>Eine andere Fernsehserie</li><li>Ein anderes Genre</li><li>Eine andere Produktserie</li><li>Eine andere Stil-ID</li></ul> |
| Enthält keine Unterzeichenfolge<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Mit dem Operator &quot;enthält keine Unterzeichenfolge&quot;können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Titel enthält kein Sweet-Wort</li></ul> |
| Beginnt mit<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Mit dem Operator &quot;beginnt mit&quot;können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Produktname beginnt mit iPhone</li></ul> |
| Endet in<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Mit dem Operator &quot;endet mit&quot;können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Inhalt endet mit EN, was die englische Sprache angibt</li></ul> |
| Is Greater Than Or Equal To<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt) anzeigt, können Sie mit dem Operator &quot;größer oder gleich&quot;weitere Elemente bewerben, die:<ul><li>Kosten gleich oder teurer</li></ul> |
| Is Less Than Or Equal To<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung, Parameterübereinstimmung und statischem Filter.) | Mit dem Operator &quot;ist kleiner oder gleich&quot;können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt) anzeigt, weitere Elemente bewerben, die:<ul><li>Kosten gleich oder billiger</li><li>Niedrigere Artikel ausschließen</li></ul> |
| Ist zwischen<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung und Parameterübereinstimmung.) | Wenn Sie den Operator &quot;Ist zwischen&quot;in dynamischen Promotions verwenden, können Sie, wenn ein Besucher auf Ihrer Website ein Element (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, weitere Elemente bewerben, die folgende Kriterien erfüllen:<ul><li>Mehr</li><li>Weniger teuer</li><li>Kosten plus oder minus 30 %</li><li>Spätere Episoden in derselben Saison</li><li>Vorherige Bücher in einer Reihe</li></ul> |
| Ist in der Liste enthalten<br>(Verfügbar mit Profilattributübereinstimmung und Parameterübereinstimmung.) | Mit dem Operator &quot;ist in der Liste enthalten&quot;bei der Profilattributübereinstimmung können Sie weitere Elemente bewerben, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. ein Produkt, einen Artikel oder einen Film):<ul><li>Verfügbar in der Geografie des Besuchers</li></ul>**Beispiel**: Sie möchten nur Elemente empfehlen, die in der geografischen Region eines Besuchers verfügbar sind.<br>Ihre Filterregel könnte wie folgt aussehen:<br>`availableGeographies list contains an item in user.currentGeography`<br>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste im [rechts](#caveats) der Regel. |
| ist nicht in der Liste enthalten<br>(Verfügbar mit Profilattributübereinstimmung und Parameterübereinstimmung.) | Mit dem Operator &quot;ist nicht in der Liste enthalten&quot;bei der Profilattributübereinstimmung können Sie andere Elemente ausschließen, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. ein Produkt, einen Artikel oder einen Film):<ul><li>In der Liste der letzten zehn Elemente, die der Besucher angezeigt hat</li></ul></ul>**Beispiel**: Sie möchten keine Artikel bewerben, die der Besucher kürzlich angesehen hat und für die er kein Interesse gezeigt hat.<br>Ihre Filterregel könnte wie folgt aussehen:<br>`id is not contained in list user.lastViewedItems`<br>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste im [rechts](#caveats) der Regel. |
| Liste enthält ein Element in<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung und Parameterübereinstimmung.) | Mit dem Operator &quot;list contains an item in&quot;beim Profilattributabgleich können Sie weitere Elemente bewerben, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. ein Sportereignis oder -konzert):<ul><li>Einer der Lieblingsteams des Besuchers zugeordnet</li></ul>**Beispiel**: Sie möchten Spiele empfehlen, die mit einem der Lieblingsteams des Besuchers verbunden sind.<br>Ihre Filterregel könnte wie folgt aussehen:<br>` teamsPlaying list contains an item in user.favoriteTeams`<br>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste erwartet in [beiderseits](#caveats) der Regel. |
| Liste enthält kein Element in<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung und Parameterübereinstimmung.) | Mithilfe des Operators &quot;list enthält kein Element in&quot; bei der Parameterattributübereinstimmung können Sie andere Elemente ausschließen, die folgende Elemente enthalten, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. ein Produkt, einen Artikel oder einen Film):<ul><li>In einer Liste verbotener Typen enthalten</li></ul>**Beispiel**: Sie möchten Artikel ausschließen, die für Erwachsene verfügbar sind, wie Tabak und Alkohol.<br>Ihre Filterregel könnte wie folgt aussehen:<br>`itemType is not contained in list mbox.prohibitedTypes`<br>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste erwartet in [beiderseits](#caveats) der Regel. |
| Liste enthält alle Elemente in<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung und Parameterübereinstimmung.) | Mithilfe des Operators &quot;Liste enthält alle Elemente in&quot;beim Profilattributabgleich können Sie weitere Elemente bewerben, die angezeigt werden, wenn ein Besucher auf Ihrer Website ein Element anzeigt (z. B. eine Auftragseinsendung oder ein Rezept):<ul><li>Kenntnisse einschließen</li><li>Eine Reihe erforderlicher Zutaten einschließen</li></ul>**Beispiel 1**: Angenommen, ein Besucher verfügt über eine Reihe von Fähigkeiten (Java, C++ und HTML). Die Artikel im Katalog sind Aufträge mit erforderlichen Fähigkeiten (Java und HTML). Sie möchten sicherstellen, dass das Besucherprofil alle erforderlichen Fähigkeiten enthält, bevor Sie den Auftrag dem Besucher empfehlen.<br>Ihre Filterregel könnte wie folgt aussehen:<br>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<br>**Beispiel 2**: Angenommen, ein Benutzer verfügt über eine Liste von Inhaltsstoffen für die Auswahl. Das Rezept enthält eine Liste erforderlicher Zutaten. Sie möchten sicherstellen, dass das Besucherprofil alle erforderlichen Inhaltsstoffe enthält, bevor Sie dem Besucher das Rezept empfehlen.<br>Ihre Filterregel könnte wie folgt aussehen:<br>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<br>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste erwartet in [beiderseits](#caveats) der Regel. |
| Liste enthält nicht alle Elemente in<br>(Verfügbar mit Entitätsattributübereinstimmung, Profilattributübereinstimmung und Parameterübereinstimmung.) | Mithilfe des Operators &quot;Liste enthält nicht alle Elemente in&quot;bei der Entitätsattributübereinstimmung können Sie weitere Elemente bewerben, wenn ein Besucher ein Element auf Ihrer Website anzeigt (z. B. Sportveranstaltungen oder -konzerte):<ul><li>Schließen Sie keine Gruppe von Teams ein.</li></ul>**Beispiel**: Angenommen, eine Sportveranstaltung umfasst zwei Teams. Das Besucherprofil gibt an, dass dieser Besucher keine Spiele für diese Teams anzeigen möchte. Sie möchten sicherstellen, dass Sie kein Spiel empfehlen, wenn diese Teams spielen.<br>Ihre Filterregel könnte wie folgt aussehen:<br>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<br>**Hinweis**: Bei Verwendung dieses Operators wird eine Liste erwartet in [beiderseits](#caveats) der Regel. |

## Umgang mit leeren Werten beim Filtern nach Entitätsattributübereinstimmung, Profilattributübereinstimmung und Parameterübereinstimmung {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Sie können mehrere Optionen auswählen, um leere Werte beim Filtern nach [!UICONTROL Entitätsattributübereinstimmung], [!UICONTROL Profilattributübereinstimmung]und [!UICONTROL Parameterübereinstimmung] für Ausstiegskriterien und -aktionen.

Zuvor wurden bei einem leeren Wert keine Ergebnisse zurückgegeben. In der Dropdownliste „Wenn *x* leer ist“ können Sie die entsprechende Aktion auswählen, die ausgeführt werden solle, wenn die Kriterien leere Werte enthalten, wie in der folgenden Abbildung dargestellt:

![Bild mit leerem Wert](assets/empty_value.png)

Um die gewünschte Aktion auszuwählen, bewegen Sie den Mauszeiger über das Zahnradsymbol (![icon_Zahnradbild](assets/icon_gear.png)) und wählen Sie dann die gewünschte Aktion aus:

| Aktion | Verfügbar für | Details |
|--- |--- |--- |
| [!UICONTROL Diese Filterregel ignorieren] | [!UICONTROL Profilattributübereinstimmung] und [!UICONTROL Parameterübereinstimmung] | Diese Aktion ist standardmäßig für [!UICONTROL Profilattributübereinstimmung] und [!UICONTROL Parameterübereinstimmung].<br>Diese Option gibt an, dass die Regel ignoriert wird. Wenn beispielsweise drei Filterregeln vorhanden sind und die dritte Regel keine Werte übergibt, können Sie die dritte Regel mit den leeren Werten einfach ignorieren, statt gar keine Ergebnisse zurückzugeben. |
| [!UICONTROL Für dieses Kriterium keine Ergebnisse anzeigen]<br>(Nur Kriterien) | [!UICONTROL Entitätsattributübereinstimmung], [!UICONTROL Profilattributübereinstimmung]und [!UICONTROL Parameterübereinstimmung] | Diese Aktion ist standardmäßig für [!UICONTROL Entitätsattributübereinstimmung].<br>Mit dieser Aktion wird [!DNL Target] leere Werte vor dem Hinzufügen dieser Option verarbeitet werden: Für dieses Kriterium werden keine Ergebnisse angezeigt. |
| [!UICONTROL keine Artikel bewerben<br>(Nur Promotions)] | [!UICONTROL Entitätsattributübereinstimmung], [!UICONTROL Profilattributübereinstimmung]und [!UICONTROL Parameterübereinstimmung] | Diese Aktion ist standardmäßig für [!UICONTROL Entitätsattributübereinstimmung].<br>Mit dieser Aktion wird [!DNL Target] leere Werte vor dem Hinzufügen dieser Option verarbeitet werden: Für dieses Kriterium werden keine Ergebnisse angezeigt. |
| [!UICONTROL Statischen Wert verwenden] | [!UICONTROL Entitätsattributübereinstimmung], [!UICONTROL Profilattributübereinstimmung]und [!UICONTROL Parameterübereinstimmung] | Wenn ein Wert leer ist, können Sie die Verwendung eines statischen Werts festlegen. |

## Einschränkungen  {#caveats}

>[!IMPORTANT]
>
>Verschiedene Datentypattribute sind möglicherweise nicht mit dynamischen Kriterien oder Promotions kompatibel, während sie zur Laufzeit mit den Operatoren „ist gleich“ und „ist nicht gleich“ verwendet werden. Verwendung [!UICONTROL Wert], [!UICONTROL Marge], [!UICONTROL Bestand]und [!UICONTROL Umgebung] Werte weisen auf der rechten Seite eine intelligente Einstellung auf, wenn die linke Seite über vordefinierte Attribute oder benutzerdefinierte Attribute verfügt.

![Bild links_rechts](assets/left_right.png)

Die folgende Tabelle enthält wirksame Regeln und Regeln, die während der Laufzeit möglicherweise nicht kompatibel sind:

| Kompatible Regeln | Potenziell inkompatible Regeln |
|--- |--- |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - salesValue | salesValue - ist zwischen - 90 % und 110 % des aktuellen Elements - value |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - value | clearancePrice - ist zwischen - 90 % und 110 % des aktuellen Elements - margin |
| margin - ist zwischen - 90 % und 110 % des aktuellen Elements - margin | storeInventory - gleich - dem aktuellen Element - inventory |
| inventory - gleich - dem aktuellen Element - inventory |  |
