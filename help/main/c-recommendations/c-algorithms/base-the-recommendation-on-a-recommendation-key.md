---
keywords: Empfehlungsschlüssel; Empfehlungslogik; aktuelle Kategorie; benutzerdefiniertes Attribut; zuletzt gekaufter Artikel; zuletzt angezeigter Artikel; am häufigsten angezeigter Artikel; am häufigsten angezeigter Artikel; Favoritenkategorie; Beliebtheit; kürzlich angezeigter Artikel; zuletzt gekaufter Artikel; zuletzt gekauft; zuletzt angesehen; am häufigsten angesehen; am häufigsten angesehen
description: Erfahren Sie, wie Sie Empfehlungen basierend auf Schlüsseln verwenden, die Besucherverhaltenskontext verwenden, um relevante Ergebnisse in Adobe [!DNL Target] Recommendations-Aktivitäten anzuzeigen.
title: Wie Basiere ich die Empfehlung auf einem Empfehlungsschlüssel?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '3845'
ht-degree: 33%

---

# Stützen einer Empfehlung auf einen Empfehlungsschlüssel

Recommendations basierend auf Algorithmen verwendet den Besucherverhaltenskontext, um relevante Ergebnisse in [!DNL Adobe Target] [!DNL Recommendations] -Aktivitäten anzuzeigen.

Jeder Algorithmustyp bietet verschiedene für seinen Typ geeignete Algorithmen, wie in der folgenden Tabelle dargestellt:

| Algorithmustyp | Verwendungsbereiche | Verfügbare Algorithmen |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Machen Sie Empfehlungen basierend auf den Inhalten des Warenkorbs des Benutzers. | <ul><li>Personen, die diese ansahen, sahen diese an</li><li>Personen, die diese ansahen, kauften diese</li><li>Personen, die diese kauften, kauften diese</li></ul> |
| [!UICONTROL Popularity-Based] | Machen Sie Empfehlungen basierend auf der allgemeinen Beliebtheit eines Artikels auf Ihrer Site oder auf der Beliebtheit von Artikeln in der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. eines Benutzers. | <ul><li>Am häufigsten angezeigt auf der gesamten Site</li><li>Am häufigsten angezeigt nach Kategorie</li><li>Am häufigsten nach Elementattribut angezeigt</li><li>Topverkäufe auf der gesamten Site</li><li>Topverkäufe nach Kategorie</li><li>Topverkäufe nach Elementattribut</li><li>Top nach Analytics-Metrik</li></ul> |
| [!UICONTROL Item-Based] | Empfehlungen aussprechen, die darauf basieren, ähnliche Artikel wie ein Artikel zu finden, den der Benutzer gerade ansieht oder kürzlich angesehen hat. | <ul><li>Personen, die das ansahen, sahen auch dies an</li><li>Personen, die das ansahen, kauften dies</li><li>Personen, die das kauften, kauften dies</li><li>Elemente mit ähnlichen Attributen</li></ul> |
| [!UICONTROL User-Based] | Empfehlungen basierend auf dem Benutzerverhalten erstellen. | <ul><li>Vor Kurzem aufgerufene Artikel </li><li>Empfohlen für Sie</li></ul> |
| [!UICONTROL Custom Criteria] | Machen Sie Empfehlungen basierend auf einer von Ihnen hochgeladenen benutzerdefinierten Datei. | <ul><li>Benutzerspezifischer Algorithmus</li></ul> |

Jedes Kriterium ist in seinem eigenen Register definiert. Der Traffic wird gleichmäßig auf die verschiedenen Kriterientests verteilt. Anders ausgedrückt wird der Traffic bei zwei vorliegenden Kriterien gleichmäßig zwischen diesen aufgeteilt. Wenn Sie über zwei Kriterien und zwei Entwürfe verfügen, wird der Traffic gleichmäßig zwischen diesen vier Kombinationen aufgeteilt. Sie können auch den Prozentsatz der Websitebesucher festlegen, denen zum Vergleich der standardmäßige Inhalt gezeigt wird. In diesem Fall wird dem angegebenen Prozentsatz der Besucher der Standardinhalt angezeigt und der Rest wird zwischen Ihren Kriterien und Designkombinationen aufgeteilt.

Weitere Informationen zum Erstellen von Kriterien und zum Definieren der Algorithmustypen und Algorithmen finden Sie unter [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Verschiedene Empfehlungsalgorithmen eignen sich für die Platzierung auf verschiedenen Seitentypen. Weitere Informationen zu den einzelnen Algorithmustypen und den verfügbaren Algorithmen finden Sie in den folgenden Abschnitten.

## Warenkorbbasiert {#cart-based}

Der Algorithmustyp [!UICONTROL Cart-Based] ermöglicht die Empfehlung von Artikeln, die auf dem Inhalt des aktuellen Warenkorbs des Besuchers basieren. Die Empfehlungsschlüssel werden über den Parameter [mbox `cartIds`](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} in kommagetrennten Werten bereitgestellt. Nur die ersten 10 Werte werden berücksichtigt.

Die auf dem Warenkorb basierende Empfehlungslogik ähnelt dem benutzerbasierten Algorithmus &quot;[!UICONTROL Recommended For You]&quot; und den artikelbasierten Algorithmen &quot;[!UICONTROL People Who Viewed These, Bought Those]&quot; und &quot;[!UICONTROL People Who Bought These, Bought Those]&quot;.

[!DNL Target] verwendet kollaborative Filtermethoden, um die Ähnlichkeiten für jedes Element im Warenkorb des Besuchers zu ermitteln. Anschließend werden diese Ähnlichkeiten beim Verhalten für jedes Element kombiniert, um eine zusammengeführte Liste zu erhalten.

Mit [!DNL Target] können Marketing-Experten auch das Besucherverhalten innerhalb einer einzelnen Sitzung oder sitzungsübergreifend betrachten:

* **[!UICONTROL Single Session]**: Basiert auf dem, was andere Besucher innerhalb einer einzelnen Sitzung unternommen haben.

  Wenn Sie sich das Verhalten innerhalb einer einzelnen Sitzung ansehen, kann es sinnvoll sein, wenn es den Eindruck gibt, dass Produkte sich stark auf der Grundlage einer Nutzung, eines Ereignisses oder eines Ereignisses &quot;verbinden&quot;. Beispielsweise kauft ein Besucher einen Drucker und benötigt möglicherweise auch Tinte und Papier. Oder ein Besucher kauft Erdnussbutter und benötigt möglicherweise auch Brot und Gelee.

* **[!UICONTROL Across Sessions]**: Basiert auf dem, was andere Besucher über mehrere Sitzungen hinweg unternommen haben.

  Wenn Sie sich das Verhalten über mehrere Sitzungen hinweg ansehen, kann es sinnvoll sein, wenn es den Eindruck gibt, dass Produkte stark aufeinander abgestimmt sind, basierend auf der Präferenz oder dem Geschmack des Besuchers. Zum Beispiel mag ein Besucher Star Wars und vielleicht auch Indiana Jones, auch wenn der Besucher nicht unbedingt beide Filme in derselben Sitzung sehen möchte. Oder ein Besucher mag das Brettspiel &quot;Codenames&quot; und könnte auch das Brettspiel &quot;Avalon&quot;, auch wenn der Besucher nicht beide Spiele gleichzeitig spielen kann. 

[!DNL Target] gibt Empfehlungen für jeden Besucher basierend auf den Artikeln im aktuellen Warenkorb heraus, unabhängig davon, ob Sie sich das Besucherverhalten innerhalb einer einzelnen Sitzung oder sitzungsübergreifend ansehen.

Die folgenden Algorithmen sind mit dem Algorithmustyp [!UICONTROL Cart-Based] verfügbar:

### [!UICONTROL People Who Viewed This, Viewed Those]

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird.

Diese Logik gibt andere Produkte zurück, die von Personen nach der Anzeige dieses Produkts angesehen wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie zusätzliche Konversionsmöglichkeiten erstellen, indem Sie Artikel empfehlen, die auch andere Besucher angezeigt haben, die einen Artikel angesehen haben. Besucher, die beispielsweise Fahrräder auf Ihrer Site sehen, können sich auch Fahrradhelme, Fahrradkits, Schlösser usw. ansehen. Sie können eine Empfehlung mit dieser Logik erstellen, die vorschlägt, dass andere Produkte Ihnen bei der Umsatzsteigerung helfen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das ansahen, kauften diese

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Dieses Kriterium gibt andere Produkte zurück, die Personen nach dem Ansehen dieses Artikels gekauft haben. Das angegebene Produkt ist nicht in der Ergebnismenge enthalten.

Diese Logik gibt andere Produkte zurück, die Kunden nach Ansicht dieses Produkts gekauft haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie Querverkaufsmöglichkeiten erhöhen, indem Sie eine Empfehlung auf einer Produktseite anzeigen, die beispielsweise Artikel anzeigt, die andere Besucher, die den Artikel angesehen haben, gekauft haben. Wenn der Besucher beispielsweise einen Angelpol anzeigt, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher gekauft haben, wie z. B. Kästen, Gewässer und Fischköpfe. Wenn Besucher Ihre Site besuchen, erhalten sie zusätzliche Kaufempfehlungen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das kauften, kauften dies

Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel.

Diese Logik gibt andere Produkte zurück, die Kunden nach dem Kauf dieses Produkts gekauft haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie die Verkaufsmöglichkeiten erhöhen, indem Sie eine Empfehlung auf einer Warenkorbübersichtsseite anzeigen, auf der beispielsweise Artikel angezeigt werden, die auch von anderen Käufern gekauft wurden. Wenn der Besucher z. B. einen Anzug kauft, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, wie z. B. Krawatten, Kleiderschuhe und Links. Wenn Besucher ihre Käufe überprüfen, geben Sie ihnen zusätzliche Empfehlungen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

## [!UICONTROL Popularity-Based]

Mit dem Algorithmustyp [!UICONTROL Popularity-Based] können Sie Empfehlungen basierend auf der allgemeinen Beliebtheit eines Elements auf Ihrer Site oder auf der Beliebtheit von Elementen in der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. eines Benutzers abgeben.

Die folgenden Algorithmen sind mit dem Algorithmustyp [!UICONTROL Popularity-Based] verfügbar:

### Am häufigsten angezeigt auf der gesamten Site {#most-viewed}

Die Empfehlung wird durch den Artikel bestimmt, der am häufigsten angezeigt wurde. Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Ansicht
* 5 Punkte für alle folgenden Ansichten
* Am Ende der Sitzung alle Werte durch 2 teilen

Beispiel: Die Anzeige von Surfbrett A und Surfbrett B in einer Sitzung führt zu folgendem Ergebnis: A: 10 und B: 5. Wenn die Sitzung beendet wird, haben Sie A: 5, B: 2,5. Wenn Sie dieselben Elemente in der nächsten Sitzung anzeigen, ändern sich die Werte in A: 15 B: 7,5.

Verwenden Sie diesen Algorithmus auf allgemeinen Seiten, wie z. B. Startseiten, Landingpages und Offsite-Anzeigen.

### Am häufigsten angezeigt nach Kategorie {#most-viewed-category}

Die Empfehlung wird von der Kategorie bestimmt, die am meisten Aktivität verzeichnete, wobei dieselbe Methode wie für den am häufigsten angezeigten Artikel verwendet wird, statt Produkten jedoch Kategorien bewertet werden.

Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Kategorieansicht
* 5 Punkte für alle folgenden Ansichten

Kategorien, die zum ersten Mal besucht werden, erhalten 10 Punkte. Für nachfolgende Besuche derselben Kategorie werden 5 Punkte vergeben. Bei jedem Besuch werden nicht aktuelle Kategorien, die zuvor besucht wurden, um 1 reduziert.

Beispiel: Die Anzeige von Kategorie A und Kategorie B in einer Sitzung führt zu folgendem Ergebnis: A: 9 und B: 10. Wenn Sie in der nächsten Sitzung dieselben Elemente ansehen, ändern sich die Werte in A: 20 B: 9.

Verwenden Sie diesen Algorithmus auf allgemeinen Seiten, wie z. B. Startseiten, Landingpages und Offsite-Anzeigen.

Wenn Sie den Algorithmus Am häufigsten angezeigt nach Kategorie auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktuelle Kategorie
* Favoritenkategorie

### Am häufigsten nach Elementattribut angezeigt

Empfiehlt Artikel oder Medien, die den am häufigsten angezeigten Artikeln oder Medien auf Ihrer Site ähneln.

Mit diesem Algorithmus können Sie auswählen, auf welchem Elementattribut die Empfehlung basieren soll, z. B. &quot;Name&quot;oder &quot;Marke&quot;.

Anschließend wählen Sie aus, welche Profilattribute im Besucherprofil übereinstimmen sollen, z. B. &quot;Lieblingsmarke&quot;, &quot;Zuletzt zum Warenkorb hinzugefügter Artikel&quot;oder &quot;Am häufigsten angezeigte Anzeige&quot;.

### Topverkäufe auf der gesamten Site {#top-sellers}

Zeigt die Artikel an, die in den am häufigsten abgeschlossenen Bestellungen auf der gesamten Site enthalten sind. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung.

Mit diesem Algorithmus können Sie Empfehlungen für die am häufigsten verkauften Artikel auf Ihrer Site erstellen, um die Konversion und den Umsatz zu steigern. Diese Logik ist besonders für erstmalige Besucher Ihrer Site geeignet.

### Topverkäufe nach Kategorie

Zeigt die Artikel an, die zu den am häufigsten abgeschlossenen Bestellungen gehören, nach Kategorie. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung.

Mit diesem Algorithmus können Sie Empfehlungen für die am häufigsten verkauften Artikel auf Ihrer Site basierend auf der Kategorie erstellen, um die Konversion und den Umsatz zu steigern. Diese Logik ist besonders für erstmalige Besucher Ihrer Site geeignet.

Wenn Sie den Algorithmus Am häufigsten angezeigt nach Kategorie auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktuelle Kategorie
* Favoritenkategorie

### Topverkäufe nach Elementattribut

Empfiehlt Artikel oder Medien, die den am häufigsten gekauften Artikeln oder Medien auf Ihrer Site ähneln.

Mit diesem Algorithmus können Sie auswählen, auf welchem Elementattribut die Empfehlung basieren soll, z. B. &quot;Name&quot;oder &quot;Marke&quot;.

Anschließend wählen Sie aus, welche Profilattribute im Besucherprofil übereinstimmen sollen, z. B. &quot;Lieblingsmarke&quot;, &quot;Zuletzt zum Warenkorb hinzugefügter Artikel&quot;oder &quot;Am häufigsten angezeigte Anzeige&quot;.

### Top nach Analytics-Metrik

Zeigt den &quot;Top x&quot;an, wobei *x* eine beliebige [!DNL Analytics] -Metrik ist. Bei der Verwendung von Verhaltensdaten aus Mboxes können Sie &quot;Topverkäufe&quot;oder &quot;Am häufigsten angezeigt&quot;verwenden (x = &quot;Verkauf&quot;oder x = &quot;Angezeigt&quot;). Wenn Sie Verhaltensdaten aus [!DNL Adobe Analytics] verwenden, können Sie x = &quot;Hinzufügen zum Warenkorb&quot;oder eine andere [!DNL Analytics] -Metrik verwenden.

## [!UICONTROL Item-Based]

Mit dem Empfehlungstyp [!UICONTROL Item-Based] können Sie Empfehlungen dazu abgeben, wie Sie ähnliche Artikel wie einen Artikel finden, den der Benutzer gerade anzeigt oder kürzlich angesehen hat.

Die folgenden Algorithmen sind mit dem Algorithmustyp [!UICONTROL Item-Based] verfügbar:

### Personen, die das ansahen, sahen auch dies an {#viewed-viewed}

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird.

Diese Logik gibt andere Produkte zurück, die von Personen nach der Anzeige dieses Produkts angesehen wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie zusätzliche Konversionsmöglichkeiten erstellen, indem Sie Artikel empfehlen, die auch andere Besucher angezeigt haben, die einen Artikel angesehen haben. Besucher, die beispielsweise Fahrräder auf Ihrer Site sehen, können sich auch Fahrradhelme, Fahrradkits, Schlösser usw. ansehen. Sie können eine Empfehlung mit dieser Logik erstellen, die vorschlägt, dass andere Produkte Ihnen bei der Umsatzsteigerung helfen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das ansahen, kauften dies {#viewed-bought}

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Dieses Kriterium gibt andere Produkte zurück, die Personen nach dem Ansehen dieses Artikels gekauft haben. Das angegebene Produkt ist nicht in der Ergebnismenge enthalten.

Diese Logik gibt andere Produkte zurück, die Kunden nach Ansicht dieses Produkts gekauft haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie Querverkaufsmöglichkeiten erhöhen, indem Sie eine Empfehlung auf einer Produktseite anzeigen, die beispielsweise Artikel anzeigt, die andere Besucher, die den Artikel angesehen haben, gekauft haben. Wenn der Besucher beispielsweise einen Angelpol anzeigt, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher gekauft haben, wie z. B. Kästen, Gewässer und Fischköpfe. Wenn Besucher Ihre Site besuchen, erhalten sie zusätzliche Kaufempfehlungen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das kauften, kauften dies {#bought-bought}

Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel.

Diese Logik gibt andere Produkte zurück, die Kunden nach dem Kauf dieses Produkts gekauft haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie die Verkaufsmöglichkeiten erhöhen, indem Sie eine Empfehlung auf einer Warenkorbübersichtsseite anzeigen, auf der beispielsweise Artikel angezeigt werden, die auch von anderen Käufern gekauft wurden. Wenn der Besucher z. B. einen Anzug kauft, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, wie z. B. Krawatten, Kleiderschuhe und Links. Wenn Besucher ihre Käufe überprüfen, geben Sie ihnen zusätzliche Empfehlungen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Elemente mit ähnlichen Attributen {#similar-attributes}

Empfiehlt auf Grundlage von aktueller Seitenaktivität oder früherem Besucherverhalten Artikel oder Medien, die eine Ähnlichkeit zu anderen Artikeln oder Medien aufweisen.

Wenn Sie Elemente/Medien mit ähnlichen Attributen auswählen, können Sie Regeln zur Ähnlichkeit von Inhalten festlegen.

Die Verwendung der Ähnlichkeit von Inhalten zum Generieren von Empfehlungen ist besonders effektiv für neue Artikel, die in Empfehlungen mit Personen, die dies ansahen, sahen auch dies an, und anderen Logiken basierend auf dem bisherigen Verhalten nicht angezeigt werden. Anhand der Ähnlichkeit von Inhalten können sinnvolle Empfehlungen für neue Benutzer erstellt werden, für die noch keine historischen Daten oder Einkäufe verzeichnet wurden.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

Weitere Informationen finden Sie unter [Ähnlichkeit von Inhalten](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

## [!UICONTROL User-Based]

Mit dem benutzerbasierten Algorithmustyp können Sie Empfehlungen basierend auf dem Benutzerverhalten abgeben.

Die folgenden Algorithmen sind mit dem Algorithmustyp [!UICONTROL User-Based] verfügbar:

### Vor Kurzem aufgerufene Artikel {#recently-viewed}

Nutzt den Verlauf des Benutzers (sitzungsübergreifend) für die Anzeige der letzten *x* vom Besucher angesehenen Artikel, basierend auf der Anzahl x der im Entwurf vorhandenen Plätze.

Der Algorithmus &quot;Kürzlich angezeigte Elemente&quot;gibt Ergebnisse zurück, die für eine bestimmte [Umgebung](/help/main/administrating-target/hosts.md) spezifisch sind. Wenn zwei Sites zu unterschiedlichen Umgebungen gehören und ein Besucher zwischen den beiden Sites wechselt, zeigt jede Site nur die jeweiligen Elemente der entsprechenden Umgebung an. Wenn sich zwei Sites in derselben Umgebung befinden und ein Besucher zwischen den beiden Sites wechselt, werden dem Besucher dieselben kürzlich angezeigten Elemente für beide Sites angezeigt.

>[!NOTE]
>
>Sie können die [!UICONTROL Recently Viewed Items] -Kriterien nicht für Reserveempfehlungen verwenden.

[!UICONTROL Recently Viewed Items]/Medien können so gefiltert werden, dass nur Elemente mit einem bestimmten Attribut angezeigt werden.

* Kürzlich angesehene Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.
* Sie können [Sammlungen](/help/main/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der speziellen Regeln für &quot;Preis&quot;und &quot;Bestand&quot;) auf dieselbe Weise wie andere Kriterien verwenden.

Mögliche Anwendungsfälle sind beispielsweise, dass ein multinationales Unternehmen mit mehreren Unternehmen über mehrere digitale Eigenschaften hinweg über Elemente für die Besucheransicht verfügt. In diesem Fall können Sie die kürzlich angezeigten Elemente so begrenzen, dass nur die entsprechende Eigenschaft angezeigt wird, wo sie angezeigt wurden. Dadurch wird verhindert, dass kürzlich angezeigte Elemente auf der Site einer anderen digitalen Eigenschaft angezeigt werden.

Verwenden Sie diesen Algorithmus auf allgemeinen Seiten, wie z. B. Startseiten, Landingpages und Offsite-Anzeigen.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] berücksichtigt sowohl die globalen Ausschlüsse als auch die ausgewählte Sammlungseinstellung für die Aktivität. Wenn ein Element durch einen globalen Ausschluss ausgeschlossen oder nicht in der ausgewählten Sammlung enthalten ist, wird es nicht angezeigt. Daher sollte bei Verwendung eines [!UICONTROL Recently Viewed Items] -Kriteriums im Allgemeinen die Einstellung &quot;Alle Sammlungen&quot;verwendet werden.

### Empfohlen für Sie {#recommended-for-you}

Empfiehlt Artikel basierend auf dem Browsen, Anzeigen und Kaufverlauf jedes Besuchers.

Mit diesem Algorithmus können Sie personalisierte Inhalte und Erlebnisse für neue und wiederkehrende Besucher bereitstellen. Die Liste der Empfehlungen wird der neuesten Aktivität des Besuchers zugeordnet. Sie wird in der Sitzung aktualisiert und personalisiert, sobald der Benutzer Ihre Site durchsucht.

Sowohl Ansichten als auch Käufe werden zur Bestimmung der empfohlenen Artikel verwendet. Der angegebene Empfehlungsschlüssel (z. B. &quot;Aktuelles Element&quot;) wird verwendet, um von Ihnen ausgewählte Einschlussregelfilter anzuwenden.

Sie können zum Beispiel:

* Ausschließen von Artikeln, die bestimmte Kriterien nicht erfüllen (nicht vorrätige Produkte, vor mehr als 30 Tagen veröffentlichte Artikel, Filme mit R usw.).
* Begrenzen Sie die eingeschlossenen Elemente auf eine Kategorie oder die aktuelle Kategorie.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Filterschlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

## Benutzerdefinierte Kriterien {#custom}

Mit dem Algorithmustyp Benutzerspezifische Kriterien können Sie Empfehlungen basierend auf einer von Ihnen hochgeladenen benutzerdefinierten Datei erstellen.

Die Empfehlung wird anhand eines Artikels ermittelt, der im Besucherprofil gespeichert ist, entweder mithilfe des Attributs user.*x* oder Profile.*x* Attribute.

Wurde diese Option ausgewählt, muss der Wert `entity.id` im Profilattribut enthalten sein.

Wenn Sie Empfehlungen auf Grundlage von benutzerspezifischen Attributen erstellen, müssen Sie das benutzerspezifische Attribut auswählen und anschließend den Empfehlungstyp festlegen.

Zusätzlich zur Ausgabe Ihrer eigenen benutzerspezifischen Kriterien können Sie in Echtzeit filtern. So können Sie beispielsweise Ihre empfohlenen Elemente so begrenzen, dass nur die Favoritenkategorie oder -marke eines Besuchers angezeigt wird. Dadurch können Sie Offline-Berechnungen mit der Echtzeitfilterung kombinieren.

Diese Funktion bedeutet, dass Sie mit [!DNL Target] zusätzlich zu Ihren offline berechneten Empfehlungen oder benutzerdefiniert-kuratierten Listen Personalisierungen hinzufügen können. Dadurch lässt sich die Leistung Ihrer Datenwissenschaftler und Ihrer Datenrecherche mit der bewährten Bereitstellung, der Laufzeitfilterung, den A/B-Tests, dem Targeting, der Berichterstellung, den Integrationen und mehr von Adobe kombinieren.

Wenn benutzerdefinierten Kriterien Einschlussregeln hinzugefügt werden, wandelt dies auf der Grundlage eines Besuchers andernfalls statische Empfehlungen in dynamische Empfehlungen um.

* Benutzerdefinierte Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.
* Sie können [Sammlungen](/help/main/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der speziellen Regeln für &quot;Preis&quot;und &quot;Bestand&quot;) auf dieselbe Weise wie andere Kriterien verwenden.

Mögliche Nutzungsszenarien:

* Sie möchten Filme aus einer benutzerdefiniert-kuratierten Liste nur dann empfehlen, wenn sie der Besucher noch nicht gesehen hat.
* Sie möchten einen Offline-Algorithmus ausführen und die Ergebnisse verwenden, um Ihre Empfehlungen zu optimieren. Sie müssen jedoch sicherstellen, dass nicht vorrätige Artikel niemals empfohlen werden.
* Sie möchten nur die Artikel einbeziehen, die aus der Favoritenkategorie dieses Besuchers stammen.

## Empfehlungsschlüssel {#keys}

Die folgenden Empfehlungsschlüssel sind in der Dropdownliste [!UICONTROL Recommendation Key] verfügbar:

### Aktueller Artikel {#current-item}

Die Empfehlung wird vom Artikel bestimmt, den der Besucher momentan ansieht.

Recommendations zeigt andere Artikel an, die den Besucher aufgrund seiner derzeitigen Artikelwahl ebenfalls interessieren könnten.

Wenn diese Option ausgewählt ist, muss der `entity.id`-Wert als Parameter in der Anzeige-Mbox weitergeleitet werden.

Kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Verwenden Sie den Empfehlungsschlüssel [!UICONTROL Current Item] auf Ihrer Site auf:

* Seiten mit einzelnen Artikeln, beispielsweise Produktseiten.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Zuletzt gekaufter Artikel {#last-purchased}

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor gekauft wurde. Dies wird automatisch erfasst, sodass keine Werte auf der Seite übergeben werden müssen.

Kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Verwenden Sie den Empfehlungsschlüssel [!UICONTROL Last Purchased Item] auf Ihrer Site auf:

* Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.
* NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

#### Benutzerdefinierter Empfehlungsschlüssel

Sie können Empfehlungen auf dem Wert eines benutzerdefinierten Profilattributs basieren. Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Besucher zuletzt der Warteschlange hinzugefügt hat.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Dropdownliste **[!UICONTROL Recommendation Key]** aus (z. B. &quot;Zuletzt zur Watchlist hinzugefügt&quot;).
1. Wählen Sie dann Ihren &quot;**[!UICONTROL Recommendation Logic]**&quot;(z. B. &quot;Personen, die das ansahen, sahen auch dies an&quot;).

   ![Neues Kriteriendialogfeld erstellen](/help/main/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Wenn Ihr benutzerdefiniertes Profilattribut nicht direkt mit einer Entitäts-ID übereinstimmt, müssen Sie [!DNL Recommendations] erläutern, wie die Übereinstimmung mit einer Entität erfolgen soll. Angenommen, Sie möchten die meistverkauften Artikel einer Lieblingsmarke eines Besuchers anzeigen.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Dropdownliste **[!UICONTROL Recommendation Key]** aus (z. B. &quot;Lieblingsmarke&quot;).

1. Wählen Sie dann die **[!UICONTROL Recommendation Logic]** aus, die Sie mit diesem Schlüssel verwenden möchten (z. B. &quot;Topverkäufe&quot;).

   Die Option [!UICONTROL Group By Unique Value Of] wird angezeigt.

1. Wählen Sie das Entitätsattribut aus, das dem von Ihnen ausgewählten Schlüssel entspricht. In diesem Fall entspricht &quot;Lieblingsmarke&quot;`entity.brand`.

   [!DNL Recommendations] erstellt nun für jede Marke eine Liste der Topverkäufe und zeigt dem Besucher die entsprechende Liste der &quot;Topverkäufe&quot;basierend auf dem Wert an, der im Profilattribut &quot;Lieblingsmarke&quot;des Besuchers gespeichert ist.

   ![Neues Kriteriendialogfeld erstellen 2](/help/main/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Zuletzt angezeigter Artikel {#last-viewed}

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor angezeigt wurde. Dies wird automatisch erfasst, sodass keine Werte auf der Seite übergeben werden müssen.

Kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Verwenden Sie den Empfehlungsschlüssel [!UICONTROL Last Viewed Item] auf Ihrer Site auf:

* Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.
* NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

### Am häufigsten angezeigter Artikel {#most-viewed-logic}

Zeigt die Artikel oder Medien an, die am häufigsten auf Ihrer Site angezeigt werden.

Mit dieser Logik können Sie Empfehlungen basierend auf den am häufigsten angezeigten Artikeln auf Ihrer Site anzeigen, um Konversionen für andere Elemente zu erhöhen. Beispielsweise könnte eine Medien-Site Empfehlungen für die am häufigsten angezeigten Videos auf ihrer Startseite anzeigen, um Besucher dazu zu ermutigen, sich zusätzliche Videos anzusehen.

Dieser Empfehlungsschlüssel kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

### Aktuelle Kategorie {#current-category}

Die Empfehlung wird von der Produktkategorie bestimmt, die der Besucher momentan ansieht.

In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt.

Wenn diese Option ausgewählt ist, muss der `entity.categoryId`-Wert als Parameter an die Anzeige-Mbox weitergeleitet werden.

Dieser Empfehlungsschlüssel kann mit den folgenden Algorithmen verwendet werden:

* Topverkäufe
* Am häufigsten angezeigt

Verwenden Sie den Empfehlungsschlüssel [!UICONTROL Current Category] auf Ihrer Site auf:

* Seiten mit einer Kategorie.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Favoritenkategorie {#favorite-category}

Die Empfehlung wird von der bevorzugten Produktkategorie des Besuchers bestimmt.

In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt.

Wenn diese Option ausgewählt ist, muss der `entity.categoryId`-Wert als Parameter an die Anzeige-Mbox weitergeleitet werden.

Dieser Empfehlungsschlüssel kann mit den folgenden Algorithmen verwendet werden:

* Topverkäufe
* Am häufigsten angezeigt

Verwenden Sie den Empfehlungsschlüssel [!UICONTROL Current Category] auf Ihrer Site auf:

* Seiten mit einer Kategorie.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Site-Affinität {#site-affinity}

Empfiehlt Artikel auf Grundlage der Wahrscheinlichkeit eines Zusammenhangs zwischen Artikeln. Sie können dieses Kriterium anhand des Reglers „Einschlussregeln“ konfigurieren und festlegen, wie viele Daten gesammelt werden sollen, bevor eine Empfehlung angezeigt wird. Wenn Sie beispielsweise Sehr stark auswählen, werden die Produkte mit der höchsten Wahrscheinlichkeit einer Übereinstimmung empfohlen.

Beispiel: Sie legen eine sehr starke Affinität fest und Ihr Entwurf umfasst fünf Artikel, von denen drei den Schwellenwert für einen wahrscheinlichen Zusammenhang übersteigen. Die zwei Artikel, die die Voraussetzung nicht erfüllen, werden nicht in Ihren Empfehlungen angezeigt und durch von Ihnen definierte Ersatzartikel ausgetauscht. Die Artikel mit der stärksten Affinität werden zuerst angezeigt.

Ein Online-Händler kann beispielsweise Artikel in nachfolgenden Besuchen empfehlen, an denen ein Besucher während früherer Sitzungen Interesse gezeigt hat. Die Aktivität für jede Besuchersitzung wird erfasst, um eine Affinität basierend auf einem Neuigkeits- und Häufigkeitsmodell zu berechnen. Wenn dieser Besucher zu Ihrer Site zurückkehrt, wird die Site-Affinität verwendet, um Empfehlungen basierend auf früheren Aktionen auf Ihrer Site anzuzeigen.

Bei manchen Kunden mit diversen Produktsammlungen und vielfältigem Site-Verhalten kann es sein, dass die besten Ergebnisse mit einer schwachen Site-Affinität erzielt werden.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel
