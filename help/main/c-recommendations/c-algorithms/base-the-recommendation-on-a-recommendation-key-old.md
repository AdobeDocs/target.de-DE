---
keywords: Empfehlungsschlüssel;Empfehlungslogik;aktuelle Kategorie;benutzerdefiniertes Attribut;Zuletzt gekaufter Artikel;Zuletzt angezeigter Artikel;Am häufigsten angezeigter Artikel;Bevorzugte Kategorie;Beliebtheit;Zuletzt angezeigter Artikel;Zuletzt gekauft;Zuletzt angezeigt;Am häufigsten angezeigt;Favorit;Zuletzt angezeigt
description: Erfahren Sie, wie Sie Empfehlungen verwenden können, die auf Schlüsseln basieren, die den Kontext des Besucherverhaltens verwenden, um relevante Ergebnisse in Adobe [!DNL Target] Recommendations-Aktivitäten anzuzeigen.
title: Wie stütze ich die Empfehlung auf einen Empfehlungsschlüssel?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '3845'
ht-degree: 33%

---

# Stützen einer Empfehlung auf einen Empfehlungsschlüssel

Auf Algorithmen basierende Recommendations verwenden den Kontext des Besucherverhaltens, um relevante Ergebnisse in [!DNL Adobe Target] [!DNL Recommendations] anzuzeigen.

Jeder Algorithmustyp bietet verschiedene Algorithmen, die für seinen Typ geeignet sind, wie in der folgenden Tabelle gezeigt:

| Algorithmustyp | Verwendungszeitpunkt | Verfügbare Algorithmen |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Empfehlungen auf der Grundlage des Warenkorbinhalts des Benutzers aussprechen. | <ul><li>Menschen, die sich diese ansahen, sahen sich diese an</li><li>Leute, die sich diese ansahen, kauften sie</li><li>Leute, die das kauften, kauften das</li></ul> |
| [!UICONTROL Popularity-Based] | Empfehlungen auf der Grundlage der allgemeinen Popularität eines Elements auf Ihrer Website oder auf der Grundlage der Popularität von Elementen innerhalb der Lieblings- oder am häufigsten angezeigten Kategorie, Marke, Genre usw. | <ul><li>Am häufigsten auf der Website angezeigt</li><li>Am häufigsten angezeigt nach Kategorie</li><li>Am häufigsten angezeigt nach Elementattribut</li><li>Top-Verkäufer auf der Website</li><li>Topverkäufe nach Kategorie</li><li>Topverkäufe nach Artikelattribut</li><li>Am besten nach Analytics-Metrik</li></ul> |
| [!UICONTROL Item-Based] | Empfehlungen geben, basierend auf der Suche nach ähnlichen Elementen, die der Benutzer gerade anzeigt oder kürzlich angeschaut hat. | <ul><li>Personen, die das ansahen, sahen auch dies an</li><li>Personen, die das ansahen, kauften dies</li><li>Personen, die das kauften, kauften dies</li><li>Elemente mit ähnlichen Attributen</li></ul> |
| [!UICONTROL User-Based] | Empfehlungen auf der Grundlage des Benutzerverhaltens aussprechen. | <ul><li>Vor Kurzem aufgerufene Artikel </li><li>Empfohlen für</li></ul> |
| [!UICONTROL Custom Criteria] | Empfehlungen basierend auf einer benutzerdefinierten Datei, die Sie hochladen. | <ul><li>Benutzerdefinierter Algorithmus</li></ul> |

Jedes Kriterium ist in seinem eigenen Register definiert. Der Traffic wird gleichmäßig auf die verschiedenen Kriterientests verteilt. Anders ausgedrückt wird der Traffic bei zwei vorliegenden Kriterien gleichmäßig zwischen diesen aufgeteilt. Wenn Sie über zwei Kriterien und zwei Entwürfe verfügen, wird der Traffic gleichmäßig zwischen diesen vier Kombinationen aufgeteilt. Sie können auch den Prozentsatz der Websitebesucher festlegen, denen zum Vergleich der standardmäßige Inhalt gezeigt wird. In diesem Fall wird dem angegebenen Prozentsatz der Besucher der Standardinhalt angezeigt, und der Rest wird zwischen Ihren Kriterien und Designkombinationen aufgeteilt.

Weitere Informationen zum Erstellen von Kriterien und zum Definieren der Algorithmustypen und -algorithmen finden Sie unter [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Verschiedene Recommendations-Algorithmen eignen sich zur Platzierung auf verschiedenen Seitentypen. In den folgenden Abschnitten finden Sie weitere Informationen zu den einzelnen Algorithmustypen und den verfügbaren Algorithmen.

## Warenkorb-basiert {#cart-based}

Der Algorithmustyp [!UICONTROL Cart-Based] ermöglicht die Empfehlung von Artikeln basierend auf dem Inhalt des aktuellen Warenkorbs des Besuchers. Die Empfehlungsschlüssel werden über [mbox-Parameter bereitgestellt, die in kommagetrennten Werten `cartIds`](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=de){target=_blank} sind. Nur die ersten 10 Werte werden berücksichtigt.

Die Warenkorb-basierte Empfehlungslogik ähnelt dem benutzerbasierten Algorithmus &quot;[!UICONTROL Recommended For You]&quot; und den artikelbasierten Algorithmen &quot;[!UICONTROL People Who Viewed These, Bought Those]&quot; und &quot;[!UICONTROL People Who Bought These, Bought Those]&quot;.

[!DNL Target] verwendet kollaborative Filtertechniken, um Ähnlichkeiten für jedes Element im Warenkorb des Besuchers zu ermitteln, und kombiniert diese Verhaltens-Ähnlichkeiten dann über jedes Element hinweg, um eine zusammengeführte Liste zu erhalten.

[!DNL Target] können Marketing-Fachleute auch festlegen, ob das Besucherverhalten innerhalb einer einzelnen Sitzung oder über mehrere Sitzungen hinweg betrachtet werden soll:

* **[!UICONTROL Single Session]**: Basierend auf dem, was andere Besucher innerhalb einer einzelnen Sitzung getan haben.

  Das Betrachten des Verhaltens innerhalb einer einzelnen Sitzung kann sinnvoll sein, wenn es ein Gefühl dafür gibt, dass Produkte je nach Nutzung, Anlass oder Ereignis stark miteinander „übereinstimmen“. Ein Besucher kauft beispielsweise einen Drucker und benötigt möglicherweise auch Tinte und Papier. Oder ein Besucher kauft Erdnussbutter und könnte auch Brot und Gelee benötigen.

* **[!UICONTROL Across Sessions]**: Basierend auf den Aktionen anderer Besucher in mehreren Sitzungen.

  Das Betrachten des Verhaltens über mehrere Sitzungen hinweg kann sinnvoll sein, wenn es ein Gefühl dafür gibt, dass Produkte stark auf der Grundlage der Präferenzen oder Geschmäcker der Besucher miteinander „übereinstimmen“. Zum Beispiel mag ein Besucher Star Wars und könnte auch Indiana Jones mögen, auch wenn der Besucher nicht unbedingt beide Filme in derselben Sitzung sehen möchte. Oder ein Besucher mag das Brettspiel „Codenames“ und könnte auch das Brettspiel „Avalon“ mögen, auch wenn der Besucher nicht beide Spiele gleichzeitig spielen kann. 

[!DNL Target] empfiehlt für jeden Besucher basierend auf den Artikeln im aktuellen Warenkorb, unabhängig davon, ob Sie das Besucherverhalten innerhalb einer einzelnen Sitzung oder über mehrere Sitzungen hinweg betrachten.

Die folgenden Algorithmen sind mit dem [!UICONTROL Cart-Based] Algorithmustyp verfügbar:

### [!UICONTROL People Who Viewed This, Viewed Those]

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird.

Diese Logik gibt andere Produkte zurück, die Personen nach der Ansicht dieses Produkts angesehen haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie zusätzliche Konversionsmöglichkeiten erstellen, indem Sie Elemente empfehlen, die andere Besucher, die ein Element angesehen haben, auch angesehen haben. Besucher, die auf Ihrer Site Rennräder anzeigen, können sich beispielsweise auch Fahrradhelme, Fahrradkits, Schlösser usw. ansehen. Mit dieser Logik können Sie eine Empfehlung erstellen, die andere Produkte zur Umsatzsteigerung empfiehlt.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Leute, die sich das ansahen, kauften diese

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Dieses Kriterium gibt andere Produkte zurück, die Personen nach dem Ansehen dieses Artikels gekauft haben. Das angegebene Produkt ist nicht in der Ergebnismenge enthalten.

Diese Logik gibt andere Produkte zurück, die nach dem Anzeigen dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie die Crossselling-Möglichkeiten verbessern, indem Sie z. B. eine Empfehlung auf einer Produktseite anzeigen, die Artikel anzeigt, die andere Besucher, die den gekauften Artikel angesehen haben. Wenn der Besucher beispielsweise einen Angelstock betrachtet, könnte die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher gekauft haben, z. B. Angelkästen, Watvögel und Angelköder. Wenn Besucher Ihre Website durchsuchen, können Sie ihnen zusätzliche Kaufempfehlungen geben.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Leute, die das kauften, kauften das

Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel.

Diese Logik gibt andere Produkte zurück, die nach dem Kauf dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie die Crossselling-Möglichkeiten verbessern, indem Sie beispielsweise eine Empfehlung auf einer Warenkorb-Zusammenfassungsseite anzeigen, die Artikel anzeigt, die andere Käufer ebenfalls gekauft haben. Wenn der Besucher beispielsweise einen Anzug kauft, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, z. B. Krawatten, Kleiderschuhe und Manschettenknöpfe. Wenn Besucher ihre Käufe überprüfen, geben Sie ihnen zusätzliche Empfehlungen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

## [!UICONTROL Popularity-Based]

Mit dem Algorithmustyp [!UICONTROL Popularity-Based] können Sie Empfehlungen auf der Grundlage der allgemeinen Popularität eines Elements auf Ihrer Site oder auf der Grundlage der Popularität von Elementen innerhalb der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. eines Benutzers aussprechen.

Die folgenden Algorithmen sind mit dem [!UICONTROL Popularity-Based] Algorithmustyp verfügbar:

### Am häufigsten auf der Website angezeigt {#most-viewed}

Die Empfehlung wird durch das Element bestimmt, das am häufigsten angezeigt wurde. Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Ansicht
* 5 Punkte für alle folgenden Ansichten
* Am Ende der Sitzung alle Werte durch 2 teilen

Beispiel: Die Anzeige von Surfbrett A und Surfbrett B in einer Sitzung führt zu folgendem Ergebnis: A: 10 und B: 5. Wenn die Sitzung beendet ist, haben Sie A: 5, B: 2.5. Wenn Sie dieselben Elemente in der nächsten Sitzung anzeigen, ändern sich die Werte in A: 15 B: 7,5.

Verwenden Sie diesen Algorithmus für allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Anzeigen.

### Am häufigsten angezeigt nach Kategorie {#most-viewed-category}

Die Empfehlung wird von der Kategorie bestimmt, die am meisten Aktivität verzeichnete, wobei dieselbe Methode wie für den am häufigsten angezeigten Artikel verwendet wird, statt Produkten jedoch Kategorien bewertet werden.

Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Kategorieansicht
* 5 Punkte für alle folgenden Ansichten

Kategorien, die zum ersten Mal besucht werden, erhalten 10 Punkte. Für nachfolgende Besuche derselben Kategorie werden 5 Punkte vergeben. Bei jedem Besuch werden nicht aktuelle Kategorien, die zuvor besucht wurden, um 1 reduziert.

Beispiel: Die Anzeige von Kategorie A und Kategorie B in einer Sitzung führt zu folgendem Ergebnis: A: 9 und B: 10. Wenn Sie in der nächsten Sitzung dieselben Elemente ansehen, ändern sich die Werte in A: 20 B: 9.

Verwenden Sie diesen Algorithmus für allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Anzeigen.

Wenn Sie den Algorithmus Am häufigsten angezeigt nach Kategorie auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktuelle Kategorie
* Favoritenkategorie

### Am häufigsten angezeigt nach Elementattribut

Empfiehlt Elemente oder Medien, die den am häufigsten angezeigten Elementen oder Medien auf Ihrer Site ähneln.

Mit diesem Algorithmus können Sie auswählen, auf welchem Elementattribut die Empfehlung basieren soll, z. B. „Name“ oder „Marke“.

Wählen Sie dann aus, welche im Besucherprofil gespeicherten Profilattribute übereinstimmen sollen, z. B. „Lieblingsmarke“, „Zuletzt zum Warenkorb hinzugefügt“ oder „Am häufigsten angezeigt“.

### Top-Verkäufer auf der Website {#top-sellers}

Zeigt die Artikel an, die in den am häufigsten abgeschlossenen Bestellungen auf der gesamten Website enthalten sind. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung.

Mit diesem Algorithmus können Sie Empfehlungen für meistverkaufte Artikel auf Ihrer Site erstellen, um die Konversionen und den Umsatz zu steigern. Diese Logik eignet sich besonders für Erstbesucher Ihrer Site.

### Topverkäufe nach Kategorie

Zeigt die Artikel an, die in den am häufigsten abgeschlossenen Bestellungen nach Kategorie enthalten sind. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung.

Mit diesem Algorithmus können Sie basierend auf der Kategorie Empfehlungen für die meistverkauften Artikel auf Ihrer Site erstellen, um Konversionen und Umsätze zu steigern. Diese Logik eignet sich besonders für Erstbesucher Ihrer Site.

Wenn Sie den Algorithmus Am häufigsten angezeigt nach Kategorie auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktuelle Kategorie
* Favoritenkategorie

### Topverkäufe nach Artikelattribut

Empfiehlt Artikel oder Medien, die den meistgekauften Artikeln oder Medien auf Ihrer Site ähnlich sind.

Mit diesem Algorithmus können Sie auswählen, auf welchem Elementattribut die Empfehlung basieren soll, z. B. „Name“ oder „Marke“.

Wählen Sie dann aus, welche im Besucherprofil gespeicherten Profilattribute übereinstimmen sollen, z. B. „Lieblingsmarke“, „Zuletzt zum Warenkorb hinzugefügt“ oder „Am häufigsten angezeigt“.

### Am besten nach Analytics-Metrik

Zeigt das „Top x“ an, wobei *x* eine beliebige [!DNL Analytics]-Metrik ist. Bei der Verwendung von Verhaltensdaten aus Mboxes können Sie „Am häufigsten verkauft“ oder „Am häufigsten angezeigt“ (x = „verkauft“ oder x = „angezeigt„) verwenden. Wenn Sie Verhaltensdaten aus [!DNL Adobe Analytics] verwenden, können Sie x = „Hinzufügen zum Warenkorb“ oder eine andere [!DNL Analytics] Metrik verwenden.

## [!UICONTROL Item-Based]

Mit dem [!UICONTROL Item-Based] Empfehlungstyp können Sie Empfehlungen geben, indem Sie ähnliche Elemente finden wie ein Element, das der Benutzer gerade anzeigt oder kürzlich angesehen hat.

Die folgenden Algorithmen sind mit dem [!UICONTROL Item-Based] Algorithmustyp verfügbar:

### Personen, die das ansahen, sahen auch dies an {#viewed-viewed}

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird.

Diese Logik gibt andere Produkte zurück, die Personen nach der Ansicht dieses Produkts angesehen haben. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie zusätzliche Konversionsmöglichkeiten erstellen, indem Sie Elemente empfehlen, die andere Besucher, die ein Element angesehen haben, auch angesehen haben. Besucher, die auf Ihrer Site Rennräder anzeigen, können sich beispielsweise auch Fahrradhelme, Fahrradkits, Schlösser usw. ansehen. Mit dieser Logik können Sie eine Empfehlung erstellen, die andere Produkte zur Umsatzsteigerung empfiehlt.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das ansahen, kauften dies {#viewed-bought}

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Dieses Kriterium gibt andere Produkte zurück, die Personen nach dem Ansehen dieses Artikels gekauft haben. Das angegebene Produkt ist nicht in der Ergebnismenge enthalten.

Diese Logik gibt andere Produkte zurück, die nach dem Anzeigen dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie die Crossselling-Möglichkeiten verbessern, indem Sie z. B. eine Empfehlung auf einer Produktseite anzeigen, die Artikel anzeigt, die andere Besucher, die den gekauften Artikel angesehen haben. Wenn der Besucher beispielsweise einen Angelstock betrachtet, könnte die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher gekauft haben, z. B. Angelkästen, Watvögel und Angelköder. Wenn Besucher Ihre Website durchsuchen, können Sie ihnen zusätzliche Kaufempfehlungen geben.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das kauften, kauften dies {#bought-bought}

Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel.

Diese Logik gibt andere Produkte zurück, die nach dem Kauf dieses Produkts gekauft wurden. Das angegebene Produkt ist nicht im Ergebnissatz enthalten.

Mit dieser Logik können Sie die Crossselling-Möglichkeiten verbessern, indem Sie beispielsweise eine Empfehlung auf einer Warenkorb-Zusammenfassungsseite anzeigen, die Artikel anzeigt, die andere Käufer ebenfalls gekauft haben. Wenn der Besucher beispielsweise einen Anzug kauft, kann die Empfehlung zusätzliche Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, z. B. Krawatten, Kleiderschuhe und Manschettenknöpfe. Wenn Besucher ihre Käufe überprüfen, geben Sie ihnen zusätzliche Empfehlungen.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Elemente mit ähnlichen Attributen {#similar-attributes}

Empfiehlt auf Grundlage von aktueller Seitenaktivität oder früherem Besucherverhalten Artikel oder Medien, die eine Ähnlichkeit zu anderen Artikeln oder Medien aufweisen.

Wenn Sie Elemente/Medien mit ähnlichen Attributen auswählen, haben Sie die Möglichkeit, Inhaltsähnlichkeitsregeln festzulegen.

Die Verwendung der Inhaltsähnlichkeit zum Generieren von Empfehlungen ist besonders effektiv für neue Elemente, die wahrscheinlich nicht in Empfehlungen angezeigt werden, wenn Personen verwendet werden, die dies, das und andere Logiken basierend auf vergangenem Verhalten angezeigt haben. Anhand der Ähnlichkeit von Inhalten können sinnvolle Empfehlungen für neue Benutzer erstellt werden, für die noch keine historischen Daten oder Einkäufe verzeichnet wurden.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Recommendations-Schlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

Weitere Informationen finden Sie unter [Inhaltsähnlichkeit](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

## [!UICONTROL User-Based]

Mit dem Algorithmustyp Benutzerbasiert können Sie Empfehlungen auf der Grundlage des Benutzerverhaltens geben.

Die folgenden Algorithmen sind mit dem [!UICONTROL User-Based] Algorithmustyp verfügbar:

### Vor Kurzem aufgerufene Artikel {#recently-viewed}

Nutzt den Verlauf des Benutzers (sitzungsübergreifend) für die Anzeige der letzten *x* vom Besucher angesehenen Artikel, basierend auf der Anzahl x der im Entwurf vorhandenen Plätze.

Der Algorithmus „Kürzlich angezeigte Elemente“ gibt ein für eine bestimmte ([) spezifisches Ergebnis ](/help/main/administrating-target/hosts.md). Wenn zwei Sites zu unterschiedlichen Umgebungen gehören und ein Besucher zwischen den beiden Sites wechselt, zeigt jede Site nur die jeweiligen Elemente der entsprechenden Umgebung an. Wenn sich zwei Sites in derselben Umgebung befinden und ein Besucher zwischen den beiden Sites wechselt, sieht der Besucher für beide Sites die gleichen zuletzt angezeigten Elemente.

>[!NOTE]
>
>Sie können die [!UICONTROL Recently Viewed Items] nicht für Sicherungsempfehlungen verwenden.

[!UICONTROL Recently Viewed Items]/Medien können so gefiltert werden, dass nur Elemente mit einem bestimmten Attribut angezeigt werden.

* Kürzlich angesehene Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.
* Sie können [Sammlungen](/help/main/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der Sonderregeln für Preis und Inventar) auf die gleiche Weise wie alle anderen Kriterien verwenden.

Zu den möglichen Anwendungsfällen gehört, dass ein multinationales Unternehmen mit mehreren Unternehmen über eine Besucheransicht von Elementen über mehrere digitale Eigenschaften verfügen kann. In diesem Fall können Sie die kürzlich angezeigten Elemente so begrenzen, dass nur die entsprechende Eigenschaft angezeigt wird, wo sie angezeigt wurden. Dadurch wird verhindert, dass kürzlich angesehene Elemente auf der Website einer anderen digitalen Eigenschaft angezeigt werden.

Verwenden Sie diesen Algorithmus für allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Anzeigen.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] berücksichtigt sowohl die globalen Einstellungen für Ausschlüsse als auch die ausgewählten Sammlungseinstellungen für die Aktivität. Wenn ein Element durch einen globalen Ausschluss ausgeschlossen wird oder nicht in der ausgewählten Sammlung enthalten ist, wird es nicht angezeigt. Daher sollte bei Verwendung eines [!UICONTROL Recently Viewed Items] im Allgemeinen die Einstellung „Alle Sammlungen“ verwendet werden.

### Empfohlen für {#recommended-for-you}

Empfiehlt Artikel basierend auf dem Browse-, Anzeige- und Kaufverlauf jedes Besuchers.

Dieser Algorithmus ermöglicht die Bereitstellung personalisierter Inhalte und Erlebnisse für neue und wiederkehrende Besucher. Die Liste der Recommendations wird mit der neuesten Aktivität des Besuchers gewichtet. Sie wird während der Sitzung aktualisiert und im Laufe des Browsens mehr personalisiert.

Sowohl Ansichten als auch Käufe werden verwendet, um die empfohlenen Artikel zu bestimmen. Der angegebene Empfehlungsschlüssel (z. B. Aktuelles Element) wird zum Anwenden aller von Ihnen ausgewählten Einschlussregelfilter verwendet.

Sie können zum Beispiel:

* Ausschließen von Artikeln, die bestimmte Kriterien nicht erfüllen (nicht vorrätige Produkte, Artikel, die vor mehr als 30 Tagen veröffentlicht wurden, Filme mit der Bewertung „R“ usw.).
* Eingeschlossene Elemente auf eine einzelne Kategorie oder die aktuelle Kategorie beschränken.

Wenn Sie diesen Algorithmus auswählen, können Sie die folgenden Filterschlüssel auswählen:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

## Benutzerdefinierte Kriterien {#custom}

Mit dem Algorithmustyp Benutzerdefinierte Kriterien können Sie Empfehlungen auf der Grundlage einer benutzerdefinierten Datei geben, die Sie hochladen.

Die Empfehlung wird anhand eines Artikels ermittelt, der im Besucherprofil gespeichert ist, entweder mithilfe des Attributs user.*x* oder Profile.*x* Attribute.

Wurde diese Option ausgewählt, muss der Wert `entity.id` im Profilattribut enthalten sein.

Wenn Sie Empfehlungen auf Grundlage von benutzerspezifischen Attributen erstellen, müssen Sie das benutzerspezifische Attribut auswählen und anschließend den Empfehlungstyp festlegen.

Zusätzlich zur Ausgabe Ihrer eigenen benutzerspezifischen Kriterien können Sie in Echtzeit filtern. So können Sie beispielsweise Ihre empfohlenen Elemente so begrenzen, dass nur die Favoritenkategorie oder -marke eines Besuchers angezeigt wird. Dadurch können Sie Offline-Berechnungen mit der Echtzeitfilterung kombinieren.

Diese Funktion bedeutet, dass Sie [!DNL Target] verwenden können, um zusätzlich zu Ihren offline berechneten Empfehlungen oder benutzerdefinierten Listen eine Personalisierung hinzuzufügen. Dadurch lässt sich die Leistung Ihrer Datenwissenschaftler und Ihrer Datenrecherche mit der bewährten Bereitstellung, der Laufzeitfilterung, den A/B-Tests, dem Targeting, der Berichterstellung, den Integrationen und mehr von Adobe kombinieren.

Wenn benutzerdefinierten Kriterien Einschlussregeln hinzugefügt werden, wandelt dies auf der Grundlage eines Besuchers andernfalls statische Empfehlungen in dynamische Empfehlungen um.

* Benutzerdefinierte Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.
* Sie können [Sammlungen](/help/main/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der Sonderregeln für Preis und Inventar) auf die gleiche Weise wie alle anderen Kriterien verwenden.

Mögliche Nutzungsszenarien:

* Sie möchten Filme aus einer benutzerdefiniert-kuratierten Liste nur dann empfehlen, wenn sie der Besucher noch nicht gesehen hat.
* Sie möchten einen Offline-Algorithmus ausführen und die Ergebnisse für Ihre Empfehlungen verwenden. Sie müssen jedoch sicherstellen, dass nicht vorrätige Elemente nie empfohlen werden.
* Sie möchten nur die Artikel einbeziehen, die aus der Favoritenkategorie dieses Besuchers stammen.

## Empfehlungsschlüssel {#keys}

Die folgenden Empfehlungsschlüssel sind in der Dropdown-Liste [!UICONTROL Recommendation Key] verfügbar:

### Aktueller Artikel {#current-item}

Die Empfehlung wird vom Artikel bestimmt, den der Besucher momentan ansieht.

Recommendations zeigt andere Artikel an, die den Besucher aufgrund seiner derzeitigen Artikelwahl ebenfalls interessieren könnten.

Wenn diese Option ausgewählt ist, muss der `entity.id`-Wert als Parameter in der Anzeige-Mbox weitergeleitet werden.

Kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Verwenden Sie den [!UICONTROL Current Item] Recommendations-Schlüssel auf Ihrer Site unter:

* Seiten mit einzelnen Artikeln, beispielsweise Produktseiten.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Zuletzt gekaufter Artikel {#last-purchased}

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor gekauft wurde. Dies wird automatisch erfasst, sodass keine Werte auf der Seite übergeben werden müssen.

Kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Verwenden Sie den [!UICONTROL Last Purchased Item] Recommendations-Schlüssel auf Ihrer Site unter:

* Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.
* NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

#### Schlüssel für benutzerdefinierte Empfehlungen

Sie können Empfehlungen auf dem Wert eines benutzerdefinierten Profilattributs basieren. Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Besucher zuletzt der Warteschlange hinzugefügt hat.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Dropdown-Liste **[!UICONTROL Recommendation Key]** aus (z. B. „Zuletzt angezeigt zu Watchlist hinzugefügt„).
1. Wählen Sie dann Ihre **[!UICONTROL Recommendation Logic]** aus (z. B. „Personen, die dies angesehen haben, haben das angezeigt„).

   ![Neues Kriteriendialogfeld erstellen](/help/main/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Wenn Ihr benutzerdefiniertes Profilattribut nicht direkt mit einer Entitäts-ID übereinstimmt, müssen Sie [!DNL Recommendations] erläutern, wie die Übereinstimmung mit einer Entität erfolgen soll. Angenommen, Sie möchten die meistverkauften Artikel der Lieblingsmarke eines Besuchers anzeigen.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Dropdown-Liste **[!UICONTROL Recommendation Key]** aus (z. B. „Favoritenmarke„).

1. Wählen Sie dann die **[!UICONTROL Recommendation Logic]** aus, die Sie mit diesem Schlüssel verwenden möchten (z. B. „Topverkäufe„).

   Die Option [!UICONTROL Group By Unique Value Of] wird angezeigt.

1. Wählen Sie das Entitätsattribut aus, das dem ausgewählten Schlüssel entspricht. In diesem Fall entspricht „Lieblingsmarke“ `entity.brand`.

   [!DNL Recommendations] erstellt jetzt für jede Marke eine Liste „Topverkäufe“ und zeigt dem Besucher die entsprechende Liste „Topverkäufe“ an, die auf dem im Markenprofilattribut des Besuchers gespeicherten Wert basiert.

   ![Neues Kriteriendialogfeld erstellen 2](/help/main/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Zuletzt angezeigter Artikel {#last-viewed}

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor angezeigt wurde. Dies wird automatisch erfasst, sodass keine Werte auf der Seite übergeben werden müssen.

Kann mit den folgenden Algorithmen verwendet werden:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Verwenden Sie den [!UICONTROL Last Viewed Item] Recommendations-Schlüssel auf Ihrer Site unter:

* Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.
* NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

### Am häufigsten angezeigter Artikel {#most-viewed-logic}

Zeigt die Elemente oder Medien an, die am häufigsten auf Ihrer Site angezeigt werden.

Mit dieser Logik können Sie Empfehlungen anzeigen, die auf den am häufigsten angezeigten Elementen auf Ihrer Site basieren, um die Konversionen für andere Elemente zu erhöhen. Beispielsweise könnte eine Medien-Website auf ihrer Startseite Empfehlungen für die am häufigsten angezeigten Videos anzeigen, um Besucher zum Ansehen zusätzlicher Videos zu ermutigen.

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

Verwenden Sie den [!UICONTROL Current Category] Recommendations-Schlüssel auf Ihrer Site unter:

* Seiten mit einer Kategorie.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Favoritenkategorie {#favorite-category}

Die Empfehlung wird durch die bevorzugte Produktkategorie des Besuchers bestimmt.

In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt.

Wenn diese Option ausgewählt ist, muss der `entity.categoryId`-Wert als Parameter an die Anzeige-Mbox weitergeleitet werden.

Dieser Empfehlungsschlüssel kann mit den folgenden Algorithmen verwendet werden:

* Topverkäufe
* Am häufigsten angezeigt

Verwenden Sie den [!UICONTROL Current Category] Recommendations-Schlüssel auf Ihrer Site unter:

* Seiten mit einer Kategorie.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Site-Affinität {#site-affinity}

Empfiehlt Artikel auf Grundlage der Wahrscheinlichkeit eines Zusammenhangs zwischen Artikeln. Sie können dieses Kriterium anhand des Reglers „Einschlussregeln“ konfigurieren und festlegen, wie viele Daten gesammelt werden sollen, bevor eine Empfehlung angezeigt wird. Wenn Sie beispielsweise sehr stark auswählen, werden die Produkte mit der höchsten Sicherheit für eine Übereinstimmung empfohlen.

Beispiel: Sie legen eine sehr starke Affinität fest und Ihr Entwurf umfasst fünf Artikel, von denen drei den Schwellenwert für einen wahrscheinlichen Zusammenhang übersteigen. Die zwei Artikel, die die Voraussetzung nicht erfüllen, werden nicht in Ihren Empfehlungen angezeigt und durch von Ihnen definierte Ersatzartikel ausgetauscht. Die Artikel mit der stärksten Affinität werden zuerst angezeigt.

Beispielsweise kann ein Online-Händler Artikel für nachfolgende Besuche empfehlen, an denen ein Besucher während früherer Sitzungen Interesse gezeigt hat. Die Aktivität der einzelnen Besuchersitzungen wird erfasst, um eine Affinität anhand eines Neuigkeits- und Häufigkeitsmodells zu berechnen. Wenn dieser Besucher zu Ihrer Site zurückkehrt, wird die Site-Affinität verwendet, um Empfehlungen anzuzeigen, die auf früheren Aktionen auf Ihrer Site basieren.

Bei manchen Kunden mit diversen Produktsammlungen und vielfältigem Site-Verhalten kann es sein, dass die besten Ergebnisse mit einer schwachen Site-Affinität erzielt werden.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel
