---
keywords: Einschlussregeln; Aufnahmekriterien; Empfehlungen; neue Kriterien erstellen; Promotion; Promotions; dynamischer Filter; dynamisch; leere Werte; Filterregel ignorieren; statischer Filter; Filtern nach Wert; Entitätsattributübereinstimmung; Profilattributübereinstimmung; Parameterübereinstimmung; Filtern nach Wert; statischer Filter
description: Erfahren Sie, wie Sie in Adobe Target Recommendations Inklusionsregeln für Kriterien und Promotions erstellen. hinzufügen Sie zusätzliche dynamische oder statische Filterregeln, um bessere Ergebnisse zu erzielen.
title: Wie verwende ich dynamische und statische Einschlussregeln in Recommendations?
feature: Recommendations
mini-toc-levels: 3
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 41%

---


# ![PREMIUM](/help/assets/premium.png) Verwenden dynamischer und statischer Einschlussregeln{#use-dynamic-and-static-inclusion-rules}

Informationen zum Erstellen von Einschlussregeln für Kriterien und Promotions in [!DNL Adobe Target] und zum Hinzufügen zusätzlicher Regeln für das dynamische oder statische Filtern, um bessere Ergebnisse für Ihre Empfehlungen zu erzielen.

>[!NOTE]
>
>Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. In diesem Abschnitt werden sowohl Kriterien als auch Promotions und die Verwendung von Inklusionsregeln behandelt.

## Hinzufügen von Filterregeln zu Kriterien {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Klicken Sie beim [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) auf **[!UICONTROL Filterregel hinzufügen]** unter **[!UICONTROL Einschlussregeln]**.

![](assets/inclusion_options_new.png)

Die verfügbaren Optionen variieren je nach vertikalem Markt und Empfehlungsschlüssel.

## Hinzufügen von Filterregeln zu Promotions   {#section_D59AFB62E2EE423086281CF5D18B1076}

Wählen Sie beim [Erstellen einer Promotion](/help/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14) die Option **[!UICONTROL Hervorheben nach Attribut]** aus und klicken Sie dann auf **[!UICONTROL Filterregel hinzufügen]**.

![](assets/inclusion_options.png)

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In den folgenden Abschnitten werden die Filteroptionen für [!UICONTROL Dynamische Filter] und [!UICONTROL Nach Wert] für Kriterien und Promotions Liste:

### Dynamische Filterung

Dynamische Inklusionsregeln sind leistungsfähiger als statische Inklusionsregeln und bieten bessere Ergebnisse und Interaktionen. Beachten Sie Folgendes:

* Dynamische Inklusionsregeln liefern Empfehlungen, indem sie einem Attribut im Profil-Parameter eines Benutzers oder in einem Mbox-Aufruf entsprechen.

   Sie können beispielsweise eine Empfehlung &quot;Bevorzugte Kriterien&quot;erstellen und dann die zurückgegebenen Empfehlungen herausfiltern und dann alle Empfehlungen (in Echtzeit) nach einem Attribut filtern, das weitergegeben wird, wenn der Benutzer auf eine Seite zugreift, auf der die Empfehlungen angezeigt werden.

* Verwenden Sie statische Regeln, um zu begrenzen, welche Artikel in der Empfehlung enthalten sind (anstatt Sammlungen zu verwenden).

* Sie können so viele dynamische Einschlussregeln wie nötig erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Die folgenden Optionen stehen für die dynamische Filterung zur Verfügung:

| Dynamische Filteroption | Details |
| --- | --- |
| [Entitätsattributübereinstimmung](/help/c-recommendations/c-algorithms/entity-attribute-matching.md) | Sie können dynamisch filtern, indem Sie einen Pool potenzieller Empfehlungselemente mit einem bestimmten Element vergleichen, mit dem die Benutzer interagiert haben.<br>Verwenden Sie  [!UICONTROL Entitätsattribut-] Übereinstimmung, wenn Sie Empfehlungen anzeigen möchten, die am ehesten für den Besucher von Interesse sind, z. B. die Lieblingsmarke des Besuchers. |
| [Profilattributübereinstimmung](/help/c-recommendations/c-algorithms/profile-attribute-matching.md) | Sie können Elemente (Entitäten) dynamisch mit einem Wert im Profil des Benutzers vergleichen.<br>Verwenden Sie  [!UICONTROL Profil Attribute ] Matchingings, wenn Sie Empfehlungen anzeigen möchten, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. Größe oder Lieblingsmarke. |
| [Parameterübereinstimmung](/help/c-recommendations/c-algorithms/parameter-matching.md) | Dynamisches Filtern durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anforderung (API oder mbox).<br>Verwenden Sie  [!UICONTROL Parameter ] Matchinging, um Inhalte zu empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Geräteabmessungen oder Geo-Position. |

### Nach Wert filtern

Die folgende Option ist zum Filtern nach Wert verfügbar:

| Filtern nach Wert, Option | Details |
| --- | --- |
| [Statischer Filter](/help/c-recommendations/c-algorithms/static-value.md) | Geben Sie manuell einen oder mehrere statische Werte zum Filtern ein. |

## Dynamische Kriterien und Werbebeispiele

Dynamische Kriterien und Promotions sind viel leistungsfähiger als statische Kriterien und Promotions und liefern bessere Ergebnisse und Interaktionen.

Die folgenden Beispiele bieten allgemeine Ideen dazu, wie Sie dynamische Promotions in Ihren Marketingbemühungen einsetzen können:

| Operator | Beispiele |
| --- | --- |
| Gleich | Wenn ein Besucher einen Artikel auf Ihrer Website (z. B. ein Produkt, einen Artikel oder Film) anzeigt, können Sie mit dem Operator &quot;Gleich&quot;in dynamischen Promotions andere Artikel bewerben aus:<ul><li>dieselbe Marke</li><li>dieselbe Kategorie</li><li>dieselbe Kategorie UND von der Hausmarke</li><li>dasselbe Geschäft</li></ul> |
| Ist nicht gleich | Wenn ein Besucher einen Artikel auf Ihrer Website (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, können Sie mit dem Operator &quot;ist nicht gleich&quot;in dynamischen Promotions andere Artikel bewerben aus:<ul><li>andere TV-Serie</li><li>anderes Genre</li><li>andere Produktserie</li><li>andere Stil-ID</li></ul> |
| Ist zwischen | Wenn ein Besucher einen Artikel auf Ihrer Website (z. B. ein Produkt, einen Artikel oder einen Film) mit dem Operator &quot;ist zwischen&quot;in dynamischen Promotions anzeigt, können Sie andere Artikel bewerben, die Folgendes sind:<ul><li>teurer</li><li>billiger</li><li>kostet plus oder minus 30 %</li><li>spätere Episoden in derselben Staffel</li><li>vorherige Bücher einer Folge</li></ul> |

## Handhabung leerer Werte beim Filtern nach Entitäts-Attributübereinstimmung, Profil-Attributübereinstimmung und Parameterübereinstimmung {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Sie können mehrere Optionen auswählen, um leere Werte beim Filtern nach [!UICONTROL Entitätsattribut-Übereinstimmung], [!UICONTROL Profil-Attributzuordnung] und [!UICONTROL Parameterzuordnung] für Ausstiegskriterien und Promotions zu verarbeiten.

Zuvor wurden bei einem leeren Wert keine Ergebnisse zurückgegeben. In der Dropdownliste „Wenn *x* leer ist“ können Sie die entsprechende Aktion auswählen, die ausgeführt werden solle, wenn die Kriterien leere Werte enthalten, wie in der folgenden Abbildung dargestellt:

![](assets/empty_value.png)

Um die gewünschte Aktion auszuwählen, bewegen Sie den Mauszeiger über das Zahnradsymbol (![](assets/icon_gear.png)) und wählen Sie dann die gewünschte Aktion aus:

| Aktion | Verfügbar für | Details |
|--- |--- |--- |
| [!UICONTROL Diese Filterregel ignorieren] | [!UICONTROL Profil Attribute ] [!UICONTROL MatchingandParameter Matching] | Dies ist die Standardaktion für [!UICONTROL Profil-Attributzuordnung] und [!UICONTROL Parameterzuordnung].<br>Diese Option gibt an, dass die Regel ignoriert wird. Wenn beispielsweise drei Filterregeln vorhanden sind und die dritte Regel keine Werte übergibt, können Sie die dritte Regel mit den leeren Werten einfach ignorieren, statt gar keine Ergebnisse zurückzugeben. |
| [!UICONTROL Keine Ergebnisse für dieses Kriterium]<br> anzeigen (nur Kriterien) | [!UICONTROL Entitätsattributübereinstimmung],  [!UICONTROL Profil-Attributübereinstimmung] und  [!UICONTROL Parameterübereinstimmung] | Dies ist die Standardaktion für [!UICONTROL Entitätsattribut-Übereinstimmung].<br>[!DNL Target]Durch diese Aktion wird bestimmt, wie leere Werte vor dem Hinzufügen dieser Option verarbeitet hat: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| [!UICONTROL Keine Artikel<br> bewerben (nur Promotions)] | [!UICONTROL Entitätsattributübereinstimmung],  [!UICONTROL Profil-Attributübereinstimmung] und  [!UICONTROL Parameterübereinstimmung] | Dies ist die Standardaktion für [!UICONTROL Entitätsattribut-Übereinstimmung].<br>[!DNL Target]Durch diese Aktion wird bestimmt, wie leere Werte vor dem Hinzufügen dieser Option verarbeitet hat: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| [!UICONTROL Statischen Wert verwenden] | [!UICONTROL Entitätsattributübereinstimmung],  [!UICONTROL Profil-Attributübereinstimmung] und  [!UICONTROL Parameterübereinstimmung] | Wenn ein Wert leer ist, können Sie die Verwendung eines statischen Werts festlegen. |

## Einschränkungen {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Verschiedene Datentypattribute sind möglicherweise nicht mit dynamischen Kriterien oder Promotions kompatibel, während sie zur Laufzeit mit den Operatoren „ist gleich“ und „ist nicht gleich“ verwendet werden. Verwenden Sie die Werte [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] und [!UICONTROL Umgebung] genau auf der rechten Seite, wenn die linke Seite über vordefinierte Attribute oder benutzerdefinierte Attribute verfügt.

![](assets/left_right.png)

Die folgende Tabelle enthält wirksame Regeln und Regeln, die während der Laufzeit möglicherweise nicht kompatibel sind:

| Kompatible Regeln | Potenziell inkompatible Regeln |
|--- |--- |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - salesValue | salesValue - ist zwischen - 90 % und 110 % des aktuellen Elements - value |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - value | clearancePrice - ist zwischen - 90 % und 110 % des aktuellen Elements - margin |
| margin - ist zwischen - 90 % und 110 % des aktuellen Elements - margin | storeInventory - gleich - dem aktuellen Element - inventory |
| inventory - gleich - dem aktuellen Element - inventory |  |
