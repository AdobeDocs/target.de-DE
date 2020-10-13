---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: Informationen zum Erstellen von Inklusionsregeln in Adobe Target Recommendations für Kriterien und Promotions sowie zum Hinzufügen zusätzlicher Regeln zum dynamischen oder statischen Filtern, um bessere Ergebnisse zu erzielen.
title: Dynamische und statische Inklusionsregeln in Adobe Target Recommendations verwenden
feature: criteria
mini-toc-levels: 3
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
translation-type: tm+mt
source-git-commit: 2d7435c420326a7eb1a59c95befa87b06c7614c8
workflow-type: tm+mt
source-wordcount: '2125'
ht-degree: 34%

---


# ![PREMIUM](/help/assets/premium.png) Verwenden dynamischer und statischer Einschlussregeln{#use-dynamic-and-static-inclusion-rules}

Informationen zum Erstellen von Einschlussregeln für Kriterien und Promotions in Adobe Target und zum Hinzufügen zusätzlicher Regeln für das dynamische oder statische Filtern, um bessere Ergebnisse für Ihre Empfehlungen zu erzielen.

Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. In diesem Thema werden sowohl Kriterien und Promotions als auch die Verwendung von Einschlussregeln behandelt.

## Hinzufügen von Filterregeln zu Kriterien {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Klicken Sie beim [Erstellen von Kriterien](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) auf **[!UICONTROL Filterregel hinzufügen]** unter **[!UICONTROL Einschlussregeln]**.

![](assets/inclusion_options_new.png)

Die verfügbaren Optionen variieren je nach vertikalem Markt und Empfehlungsschlüssel.

## Hinzufügen von Filterregeln zu Promotions  {#section_D59AFB62E2EE423086281CF5D18B1076}

Wählen Sie beim [Erstellen einer Promotion](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14) die Option **[!UICONTROL Hervorheben nach Attribut]** aus und klicken Sie dann auf **[!UICONTROL Filterregel hinzufügen]**.

![](assets/inclusion_options.png)

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In der folgenden Tabelle werden die Filteroptionstypen für Kriterien und Promotions aufgelistet:

### Dynamische Filterung

Dynamische Inklusionsregeln sind leistungsfähiger als statische Inklusionsregeln und bieten bessere Ergebnisse und Interaktionen. Beachten Sie Folgendes:

* Dynamische Inklusionsregeln liefern Empfehlungen, indem sie einem Attribut im Profil-Parameter eines Benutzers oder in einem Mbox-Aufruf entsprechen.

   Sie können beispielsweise eine Empfehlung zu bevorzugten Kriterien erstellen und dann aus dem Satz der zurückgegebenen Empfehlungen alle in Echtzeit nach einem Attribut filtern, das beim Zugriff des Benutzers auf eine Seite, auf der die Empfehlungen angezeigt werden, weitergegeben wird.

* Verwenden Sie statische Regeln, um zu begrenzen, welche Artikel in der Empfehlung enthalten sind (anstelle von Sammlungen).

* Sie können so viele dynamische Einschlussregeln wie nötig erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Die folgenden Optionen stehen für die dynamische Filterung zur Verfügung:

#### Entitätsattributübereinstimmung

Sie können dynamisch filtern, indem Sie einen Pool potenzieller Empfehlungselemente mit einem bestimmten Element vergleichen, mit dem die Benutzer interagiert haben.

Empfehlen Sie beispielsweise nur Artikel, die mit der Marke des aktuellen Artikels übereinstimmen, wie im folgenden Beispiel:

Wenn die mbox auf einer Landingpage zurückgegeben wird `entity.brand=Nike`, werden nur Nike-Produkte zurückgegeben und auf dieser Seite angezeigt. Ebenso werden bei der Landingpage der Marke Adidas nur Adidas-Produkte zurückgegeben. Bei diesem Typ von Regeln zur dynamischen Inklusion muss der Benutzer nur eine Empfehlungsregel angeben, die die relevanten Markenergebnisse über alle Markenseiten hinweg zurückgibt, anstatt eine Sammlung oder einen statischen Filter anzugeben, der mit jedem Markennamen übereinstimmt.

#### Profilattributübereinstimmung

Sie können Elemente (Entitäten) dynamisch mit einem Wert im Profil des Benutzers vergleichen.

Verwenden Sie die [!UICONTROL Profil-Attributübereinstimmung] , wenn Sie Empfehlungen anzeigen möchten, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. der Größe oder der Lieblingsmarke.

Die folgenden Szenarien zeigen, wie Sie [!UICONTROL Profil-Attributzuordnung]verwenden können:

* Eine Firma, die Brillen verkauft, speichert die bevorzugte Rahmenfarbe eines Besuchers als &quot;Walnuss&quot;. Für diesen bestimmten Besucher werden nur Blasen-Rahmen zurückgegeben, die mit &quot;Walnuss&quot;farblich übereinstimmen.
* Ein Profil-Parameter kann für die Bekleidungsgröße (z. B. klein, mittel oder groß) eines Besuchers beim Navigieren auf der Website Ihrer Firma definiert werden. Eine Empfehlung kann so eingestellt werden, dass sie mit diesem Profil-Parameter übereinstimmt und nur die vom Benutzer bevorzugten Bekleidungsgrößen zurückgibt.

Weitere Beispiele und Anleitungen finden Sie unter Beispiele für [Profil-Attributzuordnung](#section_9873E2F22E094E479569D05AD5BB1D40) .

#### Parameterübereinstimmung

Dynamisches Filtern durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anforderung (API oder mbox).

Empfehlen Sie beispielsweise nur Inhalte, die mit dem Seitenparameter &quot;Branche&quot;oder anderen Parametern übereinstimmen, wie z. B. Geräteabmessungen oder Geolocation, wie in den folgenden Beispielen.

* Mbox-Parameter für Bildschirmbreite und -höhe können zur Zielgruppe von mobilen Besuchern und zur Empfehlung von Mobilgeräten und Zubehör verwendet werden.
* Regionale Geo-Positionsparameter können verwendet werden, um Empfehlungen für Tools während des Winters zurückzugeben. Schneeflocken und andere Schneefälle können für Besucher in Bereichen empfohlen werden, in denen es schneit, aber nicht für Besucher in Gebieten, in denen es nicht schneit.

>[!NOTE]
>
>Wenn die Aktivität vor dem 31. Oktober 2016 erstellt wurde, schlägt ihr Versand fehl, wenn der Filter &quot;Parameterübereinstimmung&quot;verwendet wird. So umgehen Sie das Problem:
>
>* Erstellen Sie eine neue Aktivität und fügen Sie Ihre Kriterien darin hinzu.
>* Verwenden Sie Kriterien, die den Filter „Parameterübereinstimmung“ nicht enthalten.
>* Entfernen Sie den Filter „Parameterübereinstimmung“ aus Ihren Kriterien.


Verfügbare Operatoren:

* gleich
* ist nicht gleich
* enthält
* „Enthält nicht“
* beginnt mit
* endet mit
* größer als oder gleich
* kleiner als oder gleich
* ist zwischen

### Nach Wert filtern

Die folgende Option ist für die dynamische Filterung verfügbar:

#### Statischer Filter

Geben Sie manuell einen oder mehrere statische Werte zum Filtern ein.

Beispielsweise nur empfohlene Inhalte mit der MPAA-Einstufung „G“ oder „PG“.

Verfügbare Operatoren:

* gleich
* ist nicht gleich
* enthält
* „Enthält nicht“
* beginnt mit
* endet mit
* Wert vorhanden
* Wert nicht vorhanden
* größer als oder gleich
* kleiner als oder gleich

>[!NOTE]
>
>Wenn Sie wissen, wie die Einschlussregeln vor der Target 17.6.1-Version (Juni 2017) konfiguriert waren, werden Sie bemerken, dass einige der Optionen und Operatoren sich geändert haben. Es werden nur die Operatoren angezeigt, die auf die ausgewählte Option angewendet werden können. Zudem wurden einige Operatoren umbenannt („stimmt überein“ heißt jetzt „gleich“), um die Konsistenz und die Intuitivität zu erhöhen. Alle vorhandenen Ausschlussregeln, die vor dieser Version erstellt worden sind, wurden automatisch in die neue Struktur migriert. Es ist keine Neustrukturierung Ihrerseits nötig.

Sie können so viele Einschlussregeln wie benötigt erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

## Dynamische Kriterien und Werbebeispiele

Dynamische Kriterien und Promotions sind deutlich leistungsstärker als statische Kriterien und Promotions und liefern bessere Ergebnisse und Interaktionen.

Die folgenden Beispiele zeigen Verwendungsmöglichkeiten dynamischer Promotions als Marketing-Maßnahmen:

### Gleich

Wenn ein Besucher einen Artikel auf Ihrer Website (z. B. ein Produkt, einen Artikel oder Film) anzeigt, können Sie mit dem Operator &quot;Gleich&quot;in dynamischen Promotions andere Artikel bewerben aus:

* dieselbe Marke
* dieselbe Kategorie
* dieselbe Kategorie UND von der Hausmarke
* dasselbe Geschäft

### Ist nicht gleich

Wenn ein Besucher einen Artikel auf Ihrer Website (z. B. ein Produkt, einen Artikel oder einen Film) anzeigt, können Sie mit dem Operator &quot;ist nicht gleich&quot;in dynamischen Promotions andere Artikel bewerben aus:

* andere TV-Serie
* anderes Genre
* andere Produktserie
* andere Stil-ID

### Ist zwischen

Wenn ein Besucher einen Artikel auf Ihrer Website (z. B. ein Produkt, einen Artikel oder einen Film) mit dem Operator &quot;ist zwischen&quot;in dynamischen Promotions anzeigt, können Sie andere Artikel bewerben, die Folgendes sind:

* teurer
* billiger
* kostet plus oder minus 30 %
* spätere Episoden in derselben Staffel
* vorherige Bücher einer Folge

## Handling empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching {#section_7D30E04116DB47BEA6FF840A3424A4C8}

You can choose several options to handle empty values when filtering by [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], and [!UICONTROL Parameter Matching] for exit criteria and promotions.

Zuvor wurden bei einem leeren Wert keine Ergebnisse zurückgegeben. In der Dropdownliste „Wenn *x* leer ist“ können Sie die entsprechende Aktion auswählen, die ausgeführt werden solle, wenn die Kriterien leere Werte enthalten, wie in der folgenden Abbildung dargestellt:

![](assets/empty_value.png)

Um die gewünschte Aktion auszuwählen, bewegen Sie den Mauszeiger über das Zahnradsymbol (![](assets/icon_gear.png)) und wählen Sie dann die gewünschte Aktion aus:

| Aktion | Verfügbar für | Details |
|--- |--- |--- |
| Diese Filterregel ignorieren | Profilattributübereinstimmung<br>Parameterübereinstimmung | Dies ist die Standardaktion für die Profilattribut- und Parameterübereinstimmung.<br>Diese Option gibt an, dass die Regel ignoriert wird. Wenn beispielsweise drei Filterregeln vorhanden sind und die dritte Regel keine Werte übergibt, können Sie die dritte Regel mit den leeren Werten einfach ignorieren, statt gar keine Ergebnisse zurückzugeben. |
| Keine Artikel bewerben | Entity Attribute<br>MatchingProfile Attribute<br>MatchingParameter Matching | Dies ist die Standardaktion für die Entitätsattributübereinstimmung.<br>[!DNL Target]Durch diese Aktion wird bestimmt, wie leere Werte vor dem Hinzufügen dieser Option verarbeitet hat: Für diese Kriterien werden keine Ergebnisse angezeigt. |
| Statischen Wert verwenden | Entitätsattributübereinstimmung<br>Profilattributübereinstimmung<br>Parameterübereinstimmung | Wenn ein Wert leer ist, können Sie die Verwendung eines statischen Werts festlegen. |

## Profil-Attributzuordnungsbeispiele {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profil Attribute Matching] ermöglicht es Ihnen, nur die Elemente zu empfehlen, die mit einem Attribut aus dem Profil des Besuchers übereinstimmen, wie in den folgenden Beispielen.

### Beispiel 1: Artikel von der Lieblingsmarke des Benutzers empfehlen

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. Wenn ein Besucher mit einer solchen Regel nach Laufshorts von einer bestimmten Marke sucht, werden nur Empfehlungen angezeigt, die mit der Lieblingsmarke des jeweiligen übereinstimmen (dem unter `profile.favoritebrand` im Profil des Benutzers gespeicherten Wert).

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Beispiel 2: Zuordnen von Arbeitsplätzen zu Arbeitssuchenden

Angenommen, Sie versuchen, Arbeitsplätze mit Arbeitssuchenden zu verbinden. Sie möchten nur Arbeitsplätze empfehlen, die sich in derselben Stadt wie der Arbeitsuchende befinden.

Sie können Einschlussregeln verwenden, um den Standort eines Arbeitsuchenden vom Profil seines Besuchers zu einer Stellenauflistung zuzuordnen, wie im folgenden Beispiel dargestellt:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Beispiel 3: Bekleidung empfehlen, die der Größe eines Besuchers entspricht

Schauen wir uns ein Beispiel an, um Kleidungsstücke zu empfehlen, die der im Profil des Besuchers festgelegten Bekleidungsgröße entsprechen.

Die Produktseite sendet `entity.size` im mbox-Aufruf (roter Pfeil in der Abbildung unten).

Sie können ein [Profil-Skript](/help/c-target/c-visitor-profile/profile-parameters.md) erstellen, um die Profil und Werte des Besuchers von der letzten Seite zu erfassen, die der Besucher besucht hat.

Beispiel:

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

Das Profil-Skript erfasst den `entity.size` Wert aus der mbox mit dem Namen `target-global-mbox` und gibt ihn als Profil-Attribut mit dem Namen `user.size` (blauer Pfeil in unten stehender Abbildung) zurück.

![mbox-groß-Aufruf](/help/c-recommendations/c-algorithms/assets/size.png)

Klicken Sie beim Erstellen der Empfehlungskriterien auf [!UICONTROL Hinzufügen Filterregel]und wählen Sie [!UICONTROL Profil-Attributübereinstimmung].

![Profil-Attributübereinstimmung Abbildung](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

Wenn Ihr `user.size` Profil in geladen wurde, wird es in der Dropdown-Liste zur Übereinstimmung angezeigt, wenn Sie die Regel so einrichten, dass der im mbox-Aufruf ( [!DNL Target]) übergebene Wert mit dem Profil-Skriptnamen (`size``user.size`) übereinstimmt.

Sie können dann &quot;size&quot;als Wert/Profil auswählen, der in &quot;user.size&quot;gespeichert ist, um die Zuordnung Ihres Attributes zu ändern.

Nach der Erstellung der Profil-Attributregeln werden alle Empfehlungen mit Attributen herausgefiltert, die nicht mit dem gespeicherten Profil-Attribut des Besuchers übereinstimmen.

### Beispiel 4: Artikel nach Größe empfehlen

Sehen Sie sich eine Website an, auf der Fans verkauft werden, um ein Beispiel dafür zu erhalten, wie die Zuordnung von Profil-Attributen Empfehlungen beeinflusst.

Wenn ein Besucher auf verschiedene Fächerbilder auf dieser Website klickt, legt jede Seite den Wert des `entity.size` Parameters fest, je nachdem, ob die Größe des Fans im Bild klein oder groß ist.

Angenommen, Sie haben ein Profil-Skript erstellt, um zu verfolgen und zu zählen, wie oft der Wert auf klein oder groß eingestellt `entity.size` ist.

Wenn der Besucher dann zur Startseite zurückkehrt, werden ihm gefilterte Empfehlungen angezeigt, je nachdem, ob mehr kleine Fans oder große Fans angeklickt wurden.

Recommendations auf der Grundlage der Anzeige von mehr kleinen Fans auf der Website:

![Empfehlungen für kleine Fans](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations auf der Grundlage der Anzeige größerer Fans auf der Website:

![Empfehlungen für große Fans](/help/c-recommendations/c-algorithms/assets/large-fans.png)

## Beispiele für Übereinstimmungen von Entitätsattributen

[!UICONTROL Die Zuordnung] von Entitätsattributen ermöglicht es Ihnen, nur die Artikel zu empfehlen, die mit einem Attribut übereinstimmen, entweder mit dem Artikel, den der Benutzer gerade anzeigt, dem Artikel, den er zuletzt gekauft hat, dem Artikel, den der Benutzer am häufigsten angezeigt hat, oder mit einem Artikel, der in einem benutzerdefinierten Attribut im Profil des Besuchers gespeichert ist, wie in den folgenden Beispielen dargestellt.

### Beispiel 5: Hochladen zu einem teureren Produkt

Angenommen, Sie sind ein Bekleidungshändler und möchten Benutzer dazu ermutigen, teurere und damit gewinnbringendere Artikel in Betracht zu ziehen. Sie können die Operatoren &quot;Gleich&quot;und &quot;Ist zwischen&quot;verwenden, um teurere Artikel zu bewerben, die aus derselben Kategorie und derselben Marke stammen. Beispielsweise kann ein Schuhhändler teurere Laufschuhe fördern, um einen Besucher, der Laufschuhe betrachtet, zu verkaufen.

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

### Beispiel 6: Förderung von Produkten mit privatem Etikett

Sie können dynamische und statische Filter kombinieren, um Produkte für Privatbezeichnungen zu bewerben. Eine Firma für die Büroversorgung kann beispielsweise Tonerkassetten der Hausmarke der Firma fördern, um einen rentableren Verkauf für einen Besucher zu fördern, der sich Toner ansieht - und um die Marke der Firma zu fördern, um einen profitableren Verkauf für einen Besucher zu fördern, der sich Stifte ansieht.

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```

## Einschränkungen {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Verschiedene Datentypattribute sind möglicherweise nicht mit dynamischen Kriterien oder Promotions kompatibel, während sie zur Laufzeit mit den Operatoren „ist gleich“ und „ist nicht gleich“ verwendet werden. You should use [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory], and [!UICONTROL Environment] values wisely on the right hand side if the left hand side has predefined attributes or custom attributes.

![](assets/left_right.png)

Die folgende Tabelle enthält wirksame Regeln und Regeln, die während der Laufzeit möglicherweise nicht kompatibel sind:

| Kompatible Regeln | Potenziell inkompatible Regeln |
|--- |--- |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - salesValue | salesValue - ist zwischen - 90 % und 110 % des aktuellen Elements - value |
| value - ist zwischen - 90 % und 110 % des aktuellen Elements - value | clearancePrice - ist zwischen - 90 % und 110 % des aktuellen Elements - margin |
| margin - ist zwischen - 90 % und 110 % des aktuellen Elements - margin | storeInventory - gleich - dem aktuellen Element - inventory |
| inventory - gleich - dem aktuellen Element - inventory |  |
