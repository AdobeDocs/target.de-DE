---
keywords: Empfehlungsschlüssel;Empfehlungslogik;aktuelle Kategorie;benutzerdefiniertes Attribut;Zuletzt gekaufter Artikel;Zuletzt angezeigter Artikel;Am häufigsten angezeigter Artikel;Bevorzugte Kategorie;Beliebtheit;Zuletzt angezeigter Artikel;Zuletzt gekauft;Zuletzt angezeigt;Am häufigsten angezeigt;Favorit;Zuletzt angezeigt
description: Erfahren Sie, wie Sie Recommendations basierend auf Schlüsseln verwenden können, die den Kontext des Besucherverhaltens verwenden, um relevante Ergebnisse in [!UICONTROL Recommendations]-Aktivitäten anzuzeigen.
title: Wie stütze ich die [!UICONTROL Recommendation] auf einen [!UICONTROL Recommendation-Schlüssel]?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
TQID: 'https://experienceleague.adobe.com/1gI3rMMf9s5ogc4BvBz4fMUqxed1Nqad0XoaR8SlU58'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '3740'
ht-degree: 12%
---
# Stützen einer Empfehlung auf einen Empfehlungsschlüssel {#base-on-recommendation-key}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie mehr über die Algorithmustypen, Algorithmen und Empfehlungsschlüssel, die für die Grundlage von Empfehlungen in [!DNL Adobe Target Recommendations]-Aktivitäten verfügbar sind.

>[!ENDSHADEBOX]

Algorithmusbasierte Empfehlungen verwenden den Kontext des Besucherverhaltens, um relevante Ergebnisse in [!DNL Adobe Target] [!DNL Recommendations] anzuzeigen. Jeder Algorithmustyp bietet einen eigenen Satz von Algorithmen. Eine Zusammenfassung der Algorithmustypen und ihrer Algorithmen finden Sie unter [Erste Schritte mit Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md#section_885B3BB1B43048A88A8926F6B76FC482).

Jedes Kriterium ist in seinem eigenen Register definiert. Der Traffic wird gleichmäßig auf die Kriterientests aufgeteilt: Mit zwei Kriterien wird der Traffic gleichmäßig zwischen ihnen aufgeteilt, und mit zwei Kriterien und zwei Designs wird der Traffic gleichmäßig auf die vier Kombinationen aufgeteilt. Für einen Prozentsatz der Site-Besuchenden kann auch festgelegt werden, dass sie den Standardinhalt zum Vergleich sehen. In diesem Fall wird dem angegebenen Prozentsatz der Besucher der Standardinhalt angezeigt, und der Rest wird zwischen den Kriterien und Designkombinationen aufgeteilt.

Weitere Informationen zum Erstellen von Kriterien und zum Definieren der Algorithmustypen und -algorithmen finden Sie unter [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Verschiedene Algorithmen eignen sich für verschiedene Seitentypen. In den folgenden Abschnitten werden jeder Algorithmustyp und seine Algorithmen beschrieben.

## Warenkorb-basiert {#cart-based}

Der **[!UICONTROL Warenkorb-]** Algorithmustyp empfiehlt Artikel basierend auf dem Inhalt des aktuellen Warenkorbs des Besuchers. Die Empfehlungsschlüssel werden als kommagetrennte Werte im `cartIds`[&#128279;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} () bereitgestellt. Nur die ersten 10 Werte werden berücksichtigt.

Die auf dem Warenkorb basierende Empfehlungslogik ähnelt dem benutzerbasierten Algorithmus &quot;**[!UICONTROL Recommended For You]**&quot; und den Algorithmen &quot;**[!UICONTROL People Who Viewed This, Bought That]**&quot; und &quot;**[!UICONTROL People Who Bought This, Bought That]**&quot;.

[!DNL Target] verwendet kollaborative Filtertechniken, um Ähnlichkeiten für jedes Element im Warenkorb des Besuchers zu ermitteln, und kombiniert dann die Ähnlichkeiten im Verhalten aller Elemente zu einer zusammengeführten Liste.

Marketing-Experten können auswählen, ob [!DNL Target] das Besucherverhalten innerhalb einer einzelnen oder über mehrere Sitzungen hinweg betrachten soll:

* **[!UICONTROL Einzelsitzung]**: Basierend auf den Aktionen, die andere Besucher innerhalb einer einzelnen Sitzung durchgeführt haben.

  Eine einzelne Sitzung eignet sich für Produkte, die je nach Nutzung, Anlass oder Ereignis stark „miteinander“ übereinstimmen. So benötigt ein Besucher, der einen Drucker kauft, möglicherweise auch Tinte und Papier, und ein Besucher, der Erdnussbutter kauft, benötigt möglicherweise auch Brot und Gelee.

* **[!UICONTROL Sitzungsübergreifend]**: Basierend darauf, was andere Besucher in mehreren Sitzungen getan haben.

  Mehrere Sitzungen eignen sich für Produkte, die je nach Präferenz oder Geschmack der Besucher stark „miteinander übereinstimmen“. Beispielsweise könnte ein Besucher, der Star Wars mag, auch Indiana Jones mögen, auch wenn er nicht unbedingt beide Filme in derselben Sitzung sehen möchte. Ebenso könnte ein Besucher, der das Brettspiel „Codenames“ mag, auch das Brettspiel „Avalon“ mögen, auch wenn der Besucher nicht beide Spiele gleichzeitig spielen kann.

[!DNL Target] empfiehlt für jeden Besucher basierend auf den Artikeln im aktuellen Warenkorb, unabhängig davon, ob das Besucherverhalten in einer einzelnen Sitzung oder über mehrere Sitzungen hinweg berücksichtigt wird.

Die folgenden Algorithmen sind mit dem Algorithmustyp **[!UICONTROL Warenkorb]** verfügbar:

| Algorithmus | Funktionsweise | Verwendungszeitpunkt | Empfehlungsschlüssel |
| --- | --- | --- | --- |
| **[!UICONTROL Personen, die diese angesehen haben, haben auch Folgendes angesehen]** | Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Gibt andere Produkte zurück, die sich Personen nach der Ansicht dieses Artikels angesehen haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten. | Erstellen Sie zusätzliche Konversionsmöglichkeiten, indem Sie Elemente empfehlen, die andere Besucher, die ein Element angesehen haben, auch angesehen haben. Besucher, die auf der Website Rennräder anzeigen, können sich beispielsweise auch Fahrradhelme, Fahrradkits, Schlösser usw. ansehen, sodass eine Empfehlung andere Produkte vorschlagen kann, die zur Umsatzsteigerung beitragen. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |
| **[!UICONTROL Personen, die diese angesehen haben, kauften auch]** | Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Gibt andere Produkte zurück, die von Personen nach der Ansicht dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten. | Erhöhen Sie die Crossselling-Möglichkeiten, indem Sie beispielsweise eine Empfehlung auf einer Produktseite anzeigen, die Artikel anzeigt, die andere Besucher, die den Artikel gekauft haben, angesehen haben. Wenn der Besucher eine Angelrute betrachtet, könnte die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher gekauft haben, wie Angelboxen, Watvögel und Angelköder. Wenn Besucher die Website durchsuchen, erhalten sie zusätzliche Kaufempfehlungen. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |
| **[!UICONTROL Personen, die diese gekauft haben, kauften auch]** | Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel. Gibt andere Produkte zurück, die nach dem Kauf dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten. | Erhöhen Sie die Crossselling-Möglichkeiten, indem Sie beispielsweise auf einer Warenkorb-Zusammenfassungsseite eine Empfehlung anzeigen, die Artikel anzeigt, die auch andere Käufer gekauft haben. Wenn der Besucher einen Anzug kauft, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, z. B. Krawatten, Kleiderschuhe und Manschettenknöpfe. Wenn Besucher ihre Käufe überprüfen, erhalten sie zusätzliche Empfehlungen. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |

## [!UICONTROL Beliebtheitsbasiert]

Der **[!UICONTROL Beliebtheitsbasierte]** Algorithmustyp empfiehlt Elemente basierend auf ihrer allgemeinen Beliebtheit auf der Website oder auf ihrer Beliebtheit in der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. des Benutzers.

Die folgenden Algorithmen sind mit dem Algorithmustyp **[!UICONTROL Beliebtheit]** verfügbar:

| Algorithmus | Funktionsweise | Verwendungszeitpunkt | Empfehlungsschlüssel |
| --- | --- | --- | --- |
| **[!UICONTROL Am häufigsten auf der Website angezeigt]** | Die Empfehlung wird durch den Artikel bestimmt, der basierend auf Kriterien der Neuigkeit/Häufigkeit am häufigsten angezeigt wurde. Siehe [Am häufigsten angezeigt auf der gesamten Site Bewertung](#most-viewed). | Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen. | |
| **[!UICONTROL Am häufigsten angezeigt nach Kategorie]** | Die Empfehlung wird anhand der Kategorie bestimmt, die die meiste Aktivität erhalten hat, und zwar nach derselben Methode wie für das am häufigsten angezeigte Element, mit dem Unterschied, dass Kategorien anstelle von Produkten bewertet werden. Siehe [Am häufigsten angezeigt nach Kategoriebewertung](#most-viewed-category). | Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen. | **[!UICONTROL Aktuelle Kategorie]**, **[!UICONTROL Favoritenkategorie]** |
| **[!UICONTROL Am häufigsten angezeigt nach Elementattribut]** | Empfiehlt Elemente oder Medien, die den am häufigsten angezeigten Elementen oder Medien auf der Website ähneln. Das Artikelattribut, auf dem die Empfehlung basieren soll, wird ausgewählt, z. B. „Name“ oder „Marke“. Anschließend werden die Profilattribute ausgewählt, die im Profil des Besuchers gespeichert wurden, damit sie übereinstimmen, z. B. „Favoritenmarke“, „Letzter Artikel zum Warenkorb hinzugefügt“ oder „Am häufigsten angezeigt“. | | |
| **[!UICONTROL Meist gesehen nach Profilattribut]** | Empfiehlt, die am häufigsten angezeigten Elemente nach einem Besucherprofilattribut und nicht nach Elementinformationen zu gruppieren, wie dies bei **[!UICONTROL Am häufigsten angezeigt nach Kategorie]** und **[!UICONTROL Am häufigsten angezeigt nach]** der Fall ist. [!DNL Target] führt für jeden Attributwert eine eigene Rangliste und zeigt zum Zeitpunkt der Bereitstellung jedem Besucher die Liste an, die seinem eigenen gespeicherten Wert entspricht. Siehe [Profilattributalgorithmen](#profile-attribute-algorithms). | | |
| **[!UICONTROL Topverkäufe auf der Website]** | Zeigt die Artikel an, die in den am häufigsten abgeschlossenen Bestellungen auf der gesamten Website enthalten sind. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung. | Erstellen Sie Empfehlungen für die meistverkauften Artikel auf der Website, um die Konversionen und den Umsatz zu steigern. Diese Logik eignet sich für Erstbesucher der Site. | |
| **[!UICONTROL Topverkäufe nach Kategorie]** | Zeigt die Artikel an, die in den am häufigsten abgeschlossenen Bestellungen nach Kategorie enthalten sind. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung. | Erstellen Sie Empfehlungen für die meistverkauften Artikel auf der Website basierend auf der Kategorie, um die Konversionen und den Umsatz zu steigern. Diese Logik eignet sich für Erstbesucher der Site. | **[!UICONTROL Aktuelle Kategorie]**, **[!UICONTROL Favoritenkategorie]** |
| **[!UICONTROL Topverkäufe nach Artikelattribut]** | Empfiehlt Artikel oder Medien, die den am häufigsten gekauften Artikeln oder Medien auf der Website ähneln. Das Artikelattribut, auf dem die Empfehlung basieren soll, wird ausgewählt, z. B. „Name“ oder „Marke“. Anschließend werden die Profilattribute ausgewählt, die im Profil des Besuchers gespeichert wurden, damit sie übereinstimmen, z. B. „Favoritenmarke“, „Letzter Artikel zum Warenkorb hinzugefügt“ oder „Am häufigsten angezeigt“. | | |
| **[!UICONTROL Topverkäufe nach Profilattribut]** | empfiehlt, die meistverkauften Artikel nach einem Besucherprofilattribut und nicht nach Artikelinformationen zu gruppieren, wie dies bei **[!UICONTROL Topverkäufe nach Kategorie]** und **[!UICONTROL Topverkäufe nach]** der Fall ist. [!DNL Target] führt eine separate Topseller-Liste pro Attributwert und zeigt zum Zeitpunkt der Bereitstellung jedem Besucher die Liste an, die seinem eigenen gespeicherten Wert entspricht. Siehe [Profilattributalgorithmen](#profile-attribute-algorithms). | | |
| **[!UICONTROL Am besten nach Analytics-Metrik]** | Zeigt das „Top x“ an, wobei *x* eine beliebige [!DNL Analytics]-Metrik ist. Bei Verwendung von Verhaltensdaten aus Mboxes können **[!UICONTROL Am häufigsten verkauft]** oder **[!UICONTROL Am häufigsten angezeigt]** verwendet werden (x = „verkauft“ oder x = „angezeigt„). Bei Verwendung von Verhaltensdaten aus [!DNL Adobe Analytics] kann x = „Hinzufügen zum Warenkorb“ oder eine andere [!DNL Analytics] Metrik verwendet werden. | | |

### [!UICONTROL Am häufigsten auf der Site angezeigt] Bewertung {#most-viewed}

Die Empfehlung ist das Element, das am häufigsten angesehen wurde, bestimmt durch die Kriterien für Neuigkeit/Häufigkeit wie folgt:

* 10 Punkte für erstmalige Ansicht
* 5 Punkte für alle folgenden Ansichten
* Dividieren Sie am Ende einer Sitzung alle Werte durch 2

Wenn Sie beispielsweise Surfbrett A und dann Surfbrett B in einer Sitzung anzeigen, erhalten Sie A: 10, B: 5. Wenn die Sitzung beendet wird, ist das Ergebnis A: 5, B: 2.5. Wenn dieselben Punkte in der nächsten Sitzung angezeigt werden, ändern sich die Werte in A: 15, B: 7,5.

### [!UICONTROL Am häufigsten angezeigt nach Kategorie] Bewertung {#most-viewed-category}

Die Empfehlung ist die Kategorie, die die meiste Aktivität erhalten hat. Sie verwendet dieselbe Methode wie „am häufigsten angezeigtes Element“, mit dem Unterschied, dass Kategorien anstelle von Produkten bewertet werden, mit den folgenden Kriterien für Neuigkeit/Häufigkeit:

* 10 Punkte für erstmalige Kategorieansicht
* 5 Punkte für alle folgenden Ansichten

Bei jedem Besuch wird der Score jeder nicht aktuellen Kategorie, die zuvor angesehen wurde, um 1 verringert.

Wenn Sie beispielsweise Kategorie A und dann Kategorie B in einer Sitzung anzeigen, erhalten Sie A: 9, B: 10. Wenn dieselben Punkte in der nächsten Sitzung angezeigt werden, ändern sich die Werte in A: 20, B: 9.

### Algorithmen für Profilattribute {#profile-attribute-algorithms}

>[!CONTEXTUALHELP]
>id="target_recommendations_profile_attribute"
>title="Profilattribut"
>abstract="Sie können ein Profilattribut mithilfe von Profilskripts erstellen. Nachdem ein Profilskript erstellt und aktiviert wurde, kann das entsprechende Profilattribut mit diesem Algorithmus verwendet werden."

**[!UICONTROL Am häufigsten angezeigt nach Profilattribut]** und **[!UICONTROL Topverkäufe nach Profilattribut]** hängen von einem Profilskript zum Ausfüllen des Attributs ab. Der Skriptname muss mit dem Präfix `recsAttribute` beginnen, damit [!DNL Target] ihn als `user.recsAttribute<Name>` speichert. Ein Skript kann für jedes Besuchermerkmal geschrieben werden, das für den Anwendungsfall relevant ist. Weitere Informationen zum Festlegen von Profilattributen mit Profilskripten finden Sie unter [Profilparameter](https://experienceleague.adobe.com/en/docs/target/using/audiences/visitor-profiles/profile-parameters).

Beispielsweise basiert das folgende Skript mit dem Namen `recsAttributeRegion` auf Empfehlungen zur Region des Besuchers:

```
var region = mbox.param('userRegion');
if (region) return region;
```

Ebenso basiert das folgende Skript mit dem Namen `recsAttributeLoyaltyTier` auf Empfehlungen zur Treuestufe des Besuchers:

```
var tier = mbox.param('visitorLoyaltyTier');
if (tier) return tier;
```

Nachdem das Skript erstellt und aktiviert wurde **[!UICONTROL wird der entsprechende Eintrag]** Region **[!UICONTROL oder]** Treuestufe“ in der Dropdown-Liste „Profilattribut“ des Fensters „Kriterien erstellen“ verfügbar. Das `recsAttribute` selbst wird nicht in der Dropdown-Liste angezeigt.

## [!UICONTROL Elementbasiert]

Der **[!UICONTROL Elementbasierte]** Algorithmustyp empfiehlt Elemente, die einem Element ähneln, das der Benutzer gerade anzeigt oder kürzlich angeschaut hat.

Die folgenden Algorithmen sind mit dem Algorithmustyp **[!UICONTROL Elementbasiert]** verfügbar:

| Algorithmus | Funktionsweise | Verwendungszeitpunkt | Empfehlungsschlüssel |
| --- | --- | --- | --- |
| **[!UICONTROL Personen, die dies angesehen haben, haben dies angesehen]** | Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Gibt andere Produkte zurück, die sich Personen nach der Ansicht dieses Artikels angesehen haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten. | Erstellen Sie zusätzliche Konversionsmöglichkeiten, indem Sie Elemente empfehlen, die andere Besucher, die ein Element angesehen haben, auch angesehen haben. Besucher, die auf der Website Rennräder anzeigen, können sich beispielsweise auch Fahrradhelme, Fahrradkits, Schlösser usw. ansehen, sodass eine Empfehlung andere Produkte vorschlagen kann, die zur Umsatzsteigerung beitragen. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |
| **[!UICONTROL Leute, die das angesehen haben, kauften das]** | Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Gibt andere Produkte zurück, die von Personen nach der Ansicht dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten. | Erhöhen Sie die Crossselling-Möglichkeiten, indem Sie beispielsweise eine Empfehlung auf einer Produktseite anzeigen, die Artikel anzeigt, die andere Besucher, die den Artikel gekauft haben, angesehen haben. Wenn der Besucher eine Angelrute betrachtet, könnte die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher gekauft haben, wie Angelboxen, Watvögel und Angelköder. Wenn Besucher die Website durchsuchen, erhalten sie zusätzliche Kaufempfehlungen. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |
| **[!UICONTROL Personen, die das gekauft haben, kauften das]** | Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel. Gibt andere Produkte zurück, die nach dem Kauf dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten. | Erhöhen Sie die Crossselling-Möglichkeiten, indem Sie beispielsweise auf einer Warenkorb-Zusammenfassungsseite eine Empfehlung anzeigen, die Artikel anzeigt, die auch andere Käufer gekauft haben. Wenn der Besucher einen Anzug kauft, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, z. B. Krawatten, Kleiderschuhe und Manschettenknöpfe. Wenn Besucher ihre Käufe überprüfen, erhalten sie zusätzliche Empfehlungen. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |
| **[!UICONTROL Elemente mit ähnlichen Attributen]** | Empfiehlt auf Grundlage von aktueller Seitenaktivität oder früherem Besucherverhalten Artikel oder Medien, die eine Ähnlichkeit zu anderen Artikeln oder Medien aufweisen. Wenn **[!UICONTROL Elemente mit ähnlichen Attributen]** oder **[!UICONTROL Medien mit ähnlichen Attributen]** ausgewählt ist, können Regeln für die Inhaltsähnlichkeit festgelegt werden. Weitere Informationen finden Sie unter [Inhaltsähnlichkeit](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity). | Die Ähnlichkeit von Inhalten ist für neue Elemente wirksam, die wahrscheinlich nicht in Recommendations angezeigt werden, indem **[!UICONTROL Personen, die dies angesehen haben]**, **[!UICONTROL die dies angezeigt haben]** und andere Logiken verwendet werden, die auf vergangenem Verhalten basieren. Es kann auch Empfehlungen für neue Besucher generieren, die keine früheren Käufe oder andere historische Daten haben. | **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Letzter gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |

## [!UICONTROL Benutzerbasiert]

Der **[!UICONTROL Benutzerbasiert]** Algorithmustyp empfiehlt Elemente basierend auf dem Verhalten des Benutzers.

Die folgenden Algorithmen sind mit dem Algorithmustyp **[!UICONTROL Benutzerbasiert]** verfügbar:

| Algorithmus | Funktionsweise | Verwendungszeitpunkt | Empfehlungsschlüssel |
| --- | --- | --- | --- |
| **[!UICONTROL Vor Kurzem aufgerufene Artikel]** | Nutzt den Verlauf des Benutzers (sitzungsübergreifend) für die Anzeige der letzten *x* vom Besucher angesehenen Artikel, basierend auf der Anzahl x der im Entwurf vorhandenen Plätze. Siehe [Details zu kürzlich angezeigten Elementen](#recently-viewed). | Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen. | |
| **[!UICONTROL Empfohlen für Sie]** | Empfiehlt Artikel basierend auf dem Browse-, Anzeige- und Kaufverlauf jedes Besuchers. Sowohl Ansichten als auch Käufe werden verwendet, um die empfohlenen Artikel zu bestimmen. Die Liste der Empfehlungen wird mit der neuesten Aktivität des Besuchers gewichtet, in der Sitzung aktualisiert und im Laufe des Browsens stärker personalisiert. | Stellen Sie sowohl neuen als auch wiederkehrenden Besuchern personalisierte Inhalte und Erlebnisse bereit. Der angegebene Empfehlungsschlüssel (z. B. **[!UICONTROL Aktuelles Element]**) wird verwendet, um alle Einschlussregelfilter anzuwenden, die ausgewählt wurden, um beispielsweise Elemente auszuschließen, die bestimmte Kriterien nicht erfüllen (nicht vorrätige Produkte, Artikel, die vor mehr als 30 Tagen veröffentlicht wurden, Filme mit der Einstufung „R“ usw.), oder um eingeschlossene Elemente auf eine einzelne Kategorie oder auf die aktuelle Kategorie zu beschränken. | Filterschlüssel: **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Zuletzt gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]** |

### [!UICONTROL Kürzlich angezeigte Artikel] Details {#recently-viewed}

Der **[!UICONTROL Kürzlich angezeigte Elemente]**-Algorithmus gibt Ergebnisse zurück, die für eine bestimmte [Umgebung) &#x200B;](/help/main/administrating-target/hosts.md). Wenn zwei Sites zu unterschiedlichen Umgebungen gehören und ein Besucher zwischen den beiden Sites wechselt, zeigt jede Site nur die jeweiligen Elemente der entsprechenden Umgebung an. Wenn sich zwei Sites in derselben Umgebung befinden und ein Besucher zwischen den beiden Sites wechselt, sieht der Besucher für beide Sites die gleichen zuletzt angezeigten Elemente.

Die **[!UICONTROL Zuletzt angezeigte Elemente]**-Kriterien können nicht für Sicherungsempfehlungen verwendet werden.

**[!UICONTROL Zuletzt angezeigte Elemente]** oder **[!UICONTROL Zuletzt angezeigte Medien]** können gefiltert werden, sodass nur Elemente mit einem bestimmten Attribut angezeigt werden.

* **[!UICONTROL Kürzlich angezeigt]** Kriterien sind wie andere Kriterien in Recommendations konfigurierbar.
* [Sammlungen](/help/main/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der Sonderregeln für Preis und Inventar) können auf dieselbe Weise wie bei allen anderen Kriterien verwendet werden.

Ein Anwendungsfall ist ein multinationales Unternehmen mit mehreren Unternehmen, bei dem ein Besucher Elemente über mehrere digitale Eigenschaften hinweg anzeigen kann. Zuletzt angezeigte Elemente können dann auf die Eigenschaft beschränkt sein, in der sie angezeigt wurden, sodass sie nicht auf der Site einer anderen Eigenschaft angezeigt werden.

>[!NOTE]
>
>**[!UICONTROL Kürzlich angezeigte Elemente]** berücksichtigt sowohl die globalen Ausschlusseinstellungen als auch die ausgewählte Sammlungseinstellung für die Aktivität. Wenn ein Element durch einen globalen Ausschluss ausgeschlossen wird oder nicht in der ausgewählten Sammlung enthalten ist, wird es nicht angezeigt. Daher sollte bei Verwendung der Kriterien **[!UICONTROL Zuletzt angezeigte Elemente]** im Allgemeinen die Einstellung „Alle Sammlungen“ verwendet werden.

## Benutzerdefinierte Kriterien {#custom}

Der Algorithmustyp **[!UICONTROL Benutzerdefinierte Kriterien]** empfiehlt Elemente basierend auf einer hochgeladenen benutzerdefinierten Datei.

Die Empfehlung wird durch ein Element bestimmt, das im Profil eines Besuchers gespeichert ist und entweder das Attribut user.*x* oder das Attribut profile.*x* verwendet. Wurde diese Option ausgewählt, muss der Wert `entity.id` im Profilattribut enthalten sein. Wenn Empfehlungen auf benutzerdefinierten Attributen basieren, muss zuerst das benutzerdefinierte Attribut und dann der Empfehlungstyp ausgewählt werden.

Auf die Ausgabe der benutzerdefinierten Kriterien kann eine Echtzeit-Filterung angewendet werden. Beispielsweise können die empfohlenen Elemente auf Elemente aus der Favoritenkategorie oder der Marke eines Besuchers beschränkt sein. Dies kombiniert Offline-Berechnungen mit Echtzeit-Filterung, sodass [!DNL Target] für offline berechnete Empfehlungen oder benutzerdefinierte kuratierte Listen eine Personalisierung hinzufügen können. Die Datenwissenschaft und die Forschung des Unternehmens werden dann mit der Bereitstellung, Laufzeitfilterung, A/B-Tests, Zielgruppenbestimmung, Berichterstellung und Integration von Adobe kombiniert.

Einschlussregeln für **[!UICONTROL benutzerdefinierte Kriterien]** wandeln ansonsten statische Empfehlungen in dynamische Empfehlungen um, die auf den Interessen des Besuchers basieren.

* Benutzerdefinierte Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.
* [Sammlungen](/help/main/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der Sonderregeln für Preis und Inventar) können auf dieselbe Weise wie bei allen anderen Kriterien verwendet werden.

Mögliche Anwendungsfälle sind:

* Empfehlen Sie Filme aus einer benutzerdefinierten kuratierten Liste, jedoch nur, wenn der Besucher sie noch nicht gesehen hat.
* Führen Sie einen Offline-Algorithmus aus und verwenden Sie die Ergebnisse, um die Empfehlungen zu verbessern. Stellen Sie dabei sicher, dass nicht vorrätige Elemente nie empfohlen werden.
* Nur Elemente einschließen, die aus der Lieblingskategorie dieses Besuchers stammen.

## Empfehlungsschlüssel {#keys}

Die folgenden Empfehlungsschlüssel sind in der Dropdown-Liste **[!UICONTROL Empfehlungsschlüssel]** verfügbar:

| Schlüssel | Wie er bestimmt wird | Was zu übergeben ist | Verwenden von in | Nicht verwenden bei | Algorithmen |
| --- | --- | --- | --- | --- | --- |
| **[!UICONTROL Aktuelles Element]** | Das Element, das der Besucher derzeit anzeigt. Empfehlungen zeigen andere Artikel an, die den Besucher aufgrund seiner derzeitigen Artikelwahl ebenfalls interessieren könnten. | Der `entity.id` muss als Parameter in der Display-Mbox übergeben werden. | Seiten mit einzelnen Artikeln, beispielsweise Produktseiten. | Null für Suchergebnisseiten. | **[!UICONTROL Artikel mit ähnlichen Attributen]**, **[!UICONTROL Personen, die dies angesehen haben, das gesehen haben]**, **[!UICONTROL Personen, die dies gesehen haben, das gekauft haben]**, **[!UICONTROL Personen, die dies gekauft haben, das gekauft haben]** |
| **[!UICONTROL Zuletzt gekaufter Artikel]** | Der letzte Artikel, der von jedem Unique Visitor gekauft wurde. | Keine. Dies wird automatisch erfasst. | Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen. | Produktseiten oder -seiten, die für Käufe relevant sind | **[!UICONTROL Artikel mit ähnlichen Attributen]**, **[!UICONTROL Personen, die dies angesehen haben, das gesehen haben]**, **[!UICONTROL Personen, die dies gesehen haben, das gekauft haben]**, **[!UICONTROL Personen, die dies gekauft haben, das gekauft haben]** |
| **[!UICONTROL Zuletzt angezeigter Artikel]** | Das letzte Element, das von jedem Unique Visitor angezeigt wurde. | Keine. Dies wird automatisch erfasst. | Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen. | Produktseiten oder -seiten, die für Käufe relevant sind | **[!UICONTROL Artikel mit ähnlichen Attributen]**, **[!UICONTROL Personen, die dies angesehen haben, das gesehen haben]**, **[!UICONTROL Personen, die dies gesehen haben, das gekauft haben]**, **[!UICONTROL Personen, die dies gekauft haben, das gekauft haben]** |
| **[!UICONTROL Am häufigsten angezeigter Artikel]** | Die Elemente oder Medien, die am häufigsten auf der Website angezeigt werden. Diese Logik zeigt Empfehlungen an, die auf den am häufigsten angezeigten Elementen basieren, um die Konversionen für andere Elemente zu erhöhen. Beispielsweise könnte eine Medien-Website auf ihrer Startseite Empfehlungen für die am häufigsten angezeigten Videos anzeigen, um Besucher zum Ansehen zusätzlicher Videos zu ermutigen. | | | | **[!UICONTROL Artikel mit ähnlichen Attributen]**, **[!UICONTROL Personen, die dies angesehen haben, das gesehen haben]**, **[!UICONTROL Personen, die dies gesehen haben, das gekauft haben]**, **[!UICONTROL Personen, die dies gekauft haben, das gekauft haben]** |
| **[!UICONTROL Aktuelle Kategorie]** | Die Produktkategorie, die der Besucher derzeit anzeigt. In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt. | Der `entity.categoryId` muss als Parameter an die Display-Mbox übergeben werden. | Seiten mit einer Kategorie. | Null für Suchergebnisseiten. | **[!UICONTROL Topverkäufe]**, **[!UICONTROL Am häufigsten angezeigt]** |
| **[!UICONTROL Favoritenkategorie]** | Die bevorzugte Produktkategorie des Besuchers. In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt. | Der `entity.categoryId` muss als Parameter an die Display-Mbox übergeben werden. | Seiten mit einer Kategorie. | Null für Suchergebnisseiten. | **[!UICONTROL Topverkäufe]**, **[!UICONTROL Am häufigsten angezeigt]** |

### Benutzerdefinierter Empfehlungsschlüssel

Empfehlungen können auf dem Wert eines benutzerdefinierten Profilattributs basieren. Beispielsweise können empfohlene Filme basierend auf dem Film angezeigt werden, den ein Besucher der Warteschlange zuletzt hinzugefügt hat.

1. Wählen Sie das benutzerdefinierte Profilattribut aus der Dropdown-Liste **[!UICONTROL Empfehlungsschlüssel]** aus (z. B. &quot;**[!UICONTROL Zuletzt zur Watchlist hinzugefügt]**„).

1. Wählen Sie die **[!UICONTROL Empfehlungslogik]** aus (z. B **[!UICONTROL „Personen, die dies angezeigt haben, haben das]**„).

Wenn das benutzerdefinierte Profilattribut nicht direkt mit einer einzelnen Entitäts-ID übereinstimmt, geben Sie an, wie [!DNL Recommendations] mit einer Entität übereinstimmt. So zeigen Sie beispielsweise die meistverkauften Artikel der Lieblingsmarke eines Besuchers an:

1. Wählen Sie das benutzerdefinierte Profilattribut aus der Dropdown-Liste **[!UICONTROL Empfehlungsschlüssel]** aus (z. B. „Favoritenmarke„).

1. Wählen Sie die **[!UICONTROL Empfehlungslogik]** aus, die mit diesem Schlüssel verwendet werden soll (z. B **[!UICONTROL „Topverkäufe]**).

   Die **[!UICONTROL Nach eindeutigem Wert gruppieren von]** wird angezeigt.

1. Wählen Sie das Entitätsattribut aus, das dem ausgewählten Schlüssel entspricht. In diesem Fall entspricht &quot;**[!UICONTROL Lieblingsmarke]**&quot; `entity.brand`.

   [!DNL Recommendations] erstellt jetzt für jede Marke eine Liste **[!UICONTROL Topverkäufe]** und zeigt dem Besucher die entsprechende Liste **[!UICONTROL Topverkäufe]** an, die auf dem Wert basiert, der im Profilattribut **[!UICONTROL Favoritenmarke]** des Besuchers gespeichert ist.

### [!UICONTROL Site-Affinität] {#site-affinity}

Empfiehlt Artikel auf Grundlage der Wahrscheinlichkeit eines Zusammenhangs zwischen Artikeln. Diese Kriterien können so konfiguriert werden, dass mithilfe des Schiebereglers **[!UICONTROL Einschlussregeln“ festgelegt wird, wie viele Daten erforderlich]**, bevor eine Empfehlung angezeigt wird. Wenn beispielsweise Sehr stark ausgewählt ist, werden Produkte mit der höchsten Sicherheit für eine Übereinstimmung empfohlen.

Wenn beispielsweise eine sehr starke Affinität festgelegt ist und das Design fünf Elemente enthält, von denen drei den Schwellenwert für die Verbindungsstärke erfüllen, werden die beiden Elemente, die die Mindestanforderungen für die Stärke nicht erfüllen, in den Empfehlungen nicht angezeigt und durch die definierten Sicherungselemente ersetzt. Die Artikel mit der stärksten Affinität werden zuerst angezeigt.

Ein weiteres Beispiel: Eine Online-retailer kann Elemente bei nachfolgenden Besuchen empfehlen, an denen sich ein Besucher während früherer Sitzungen interessiert hat. Die Aktivität der einzelnen Besuchersitzungen wird erfasst, um eine Affinität anhand eines Neuigkeits- und Häufigkeitsmodells zu berechnen. Wenn der Besucher zur Site zurückkehrt, wird die Site-Affinität verwendet, um Empfehlungen anzuzeigen, die auf früheren Aktionen auf der Site basieren.

Eine schwache Site-Affinität kann die besten Ergebnisse für Kunden mit verschiedenen Produktsammlungen und verschiedenen Site-Verhaltensweisen liefern.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden: **[!UICONTROL Aktueller Artikel]**, **[!UICONTROL Zuletzt gekaufter Artikel]**, **[!UICONTROL Zuletzt angezeigter Artikel]**, **[!UICONTROL Am häufigsten angezeigter Artikel]**.
