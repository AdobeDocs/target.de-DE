---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations verwendet auf der Grundlage von Schlüsseln den Verhaltenskontext des Besuchers, um relevante Ergebnisse in Adobe Target Recommendations-Aktivitäten anzuzeigen.
title: Stützen der Empfehlung auf einen Empfehlungsschlüssel
feature: criteria
mini-toc-levels: 2
translation-type: tm+mt
source-git-commit: ab44de312d86432450ccee1ba42a7df77fbeed0b
workflow-type: tm+mt
source-wordcount: '2692'
ht-degree: 72%

---


# Stützen der Empfehlung auf einen Empfehlungsschlüssel

Recommendations based on keys use visitor behavior context to show relevant results in [!DNL Adobe Target] [!DNL Recommendations] activities.

Es gibt zwei Arten von Recommendations:

* **Beliebtheit:** Führt Elemente gemäß „Am häufigsten angezeigt“, „Topverkäufe“ und „Top-Metriken“ auf. Der Schlüssel ist leer für die Beliebtheitskriterien.
* **Schlüsselbasiert:** Bildet den Rest der Kriterien. Recommendations bietet eine vielfältige Reihe an Auswahlmöglichkeiten in Bezug auf den Schlüsseltyp. Die Möglichkeiten reichen von „Aktueller Artikel“ bis hin zu „Profilparameter“, wodurch Sie den Schlüssel der zu empfehlenden Werte programmgesteuert festlegen können. Sie können mehrere Kriterien miteinander vergleichen, indem Sie festlegen, dass die einzelnen Kriterien auf einem unterschiedlichen Schlüssel basieren.

Jedes Kriterium ist in seinem eigenen Register definiert. Der Traffic wird gleichmäßig auf die verschiedenen Kriterientests verteilt. Anders ausgedrückt wird der Traffic bei zwei vorliegenden Kriterien gleichmäßig zwischen diesen aufgeteilt. Wenn Sie über zwei Kriterien und zwei Entwürfe verfügen, wird der Traffic gleichmäßig zwischen diesen vier Kombinationen aufgeteilt. Sie können auch den Prozentsatz der Websitebesucher festlegen, denen zum Vergleich der standardmäßige Inhalt gezeigt wird. In diesem Fall sieht ein angegebener Prozentsatz von Besuchern den Standardinhalt und der Rest wird auf die Kriterien- und Entwurfskombinationen verteilt.

1. Create a new criteria, or select an existing criteria and click **[!UICONTROL Edit]**.
1. To change the recommendation key, select the new key from the [!UICONTROL Recommendation Key] drop-down list, then click **[!UICONTROL Save]** or **[!UICONTROL Update]**.

   Da sich unterschiedliche Logiken auf unterschiedliche Empfehlungsschlüssel beziehen, werden unterschiedliche Empfehlungen auf unterschiedlichen Seitentypen platziert. Weitere Informationen zu den einzelnen Empfehlungsschlüsseln finden Sie in den folgenden Abschnitten.

## Empfehlungsschlüssel

Die folgenden Empfehlungsschlüssel stehen in der Dropdown-Liste [!UICONTROL Empfehlungsschlüssel] zur Verfügung:

### Aktueller Artikel

Die Empfehlung wird vom Artikel bestimmt, den der Besucher momentan ansieht.

Recommendations zeigt andere Artikel an, die den Besucher aufgrund seiner derzeitigen Artikelwahl ebenfalls interessieren könnten.

Wenn diese Option ausgewählt ist, muss der `entity.id`-Wert als Parameter in der Anzeige-Mbox weitergeleitet werden.

#### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

#### Verwendung auf Ihrer Site

* Seiten mit einzelnen Artikeln, beispielsweise Produktseiten.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Aktuelle Kategorie

Die Empfehlung wird von der Produktkategorie bestimmt, die der Besucher momentan ansieht.

In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt.

Wenn diese Option ausgewählt ist, muss der `entity.categoryId`-Wert als Parameter an die Anzeige-Mbox weitergeleitet werden.

#### Logik (Kriterien)

* Topverkäufe
* Am häufigsten angezeigt

#### Verwendung auf Ihrer Site

* Seiten mit einer Kategorie.
* NICHT auf Seiten ohne Suchergebnisse verwenden.

### Benutzerspezifisches Attribut  {#custom}

Die Empfehlung wird anhand eines Artikels ermittelt, der im Besucherprofil gespeichert ist, entweder mithilfe des Attributs user.*x* oder Profile.*x* Attribute.

Wurde diese Option ausgewählt, muss der Wert `entity.id` im Profilattribut enthalten sein.

Wenn Sie Empfehlungen auf Grundlage von benutzerspezifischen Attributen erstellen, müssen Sie das benutzerspezifische Attribut auswählen und anschließend den Empfehlungstyp festlegen.

Zusätzlich zur Ausgabe Ihrer eigenen benutzerspezifischen Kriterien können Sie in Echtzeit filtern. So können Sie beispielsweise Ihre empfohlenen Elemente so begrenzen, dass nur die Favoritenkategorie oder -marke eines Besuchers angezeigt wird. Dadurch können Sie Offline-Berechnungen mit der Echtzeitfilterung kombinieren.

This functionality means that you can use [!DNL Target] to add personalization on top of your offline calculated recommendations or custom-curated lists. Dadurch lässt sich die Leistung Ihrer Datenwissenschaftler und Ihrer Datenrecherche mit der bewährten Bereitstellung, der Laufzeitfilterung, den A/B-Tests, dem Targeting, der Berichterstellung, den Integrationen und mehr von Adobe kombinieren.

Wenn benutzerdefinierten Kriterien Einschlussregeln hinzugefügt werden, wandelt dies auf der Grundlage eines Besuchers andernfalls statische Empfehlungen in dynamische Empfehlungen um.

* Benutzerdefinierte Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.
* Sie können [Sammlungen](/help/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der speziellen Regeln für „Preis“ und „Bestand“) können auf die gleiche Weise wie alle anderen Kriterien genutzt werden.

Mögliche Nutzungsszenarien:

* Sie möchten Filme aus einer benutzerdefiniert-kuratierten Liste nur dann empfehlen, wenn sie der Besucher noch nicht gesehen hat.
* Sie möchten einen Offline-Algorithmus ausführen und die Ergebnisse verwenden, um Ihre Empfehlung zu verbessern. Dabei müssen Sie jedoch sicherstellen, dass vergriffene Artikel niemals empfohlen werden.
* Sie möchten nur die Artikel einbeziehen, die aus der Favoritenkategorie dieses Besuchers stammen.

#### Logik (Kriterien)

* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Gesamtverhalten]
* [!UICONTROL Am häufigsten angezeigt]
* [!UICONTROL Topverkäufe]

Wenn der Schlüssel ein benutzerspezifisches Profilattribut ist und der Algorithmustyp „Am häufigsten angezeigt“ oder „Topverkäufe“ lautet, wird eine neue Dropdownliste namens „Nach eindeutigem Wert gruppieren von“ angezeigt, in der eine Liste bekannter Entitätsattribute (mit Ausnahme von ID, category, margin, value, inventory und environment) vorhanden ist. Dieses Feld ist ein Pflichtfeld.

#### Verwendung auf Ihrer Site

* Kann auf beliebigen Seiten verwendet werden.

#### Benutzerspezifischer Empfehlungsschlüssel

Sie können Empfehlungen auf dem Wert eines benutzerdefinierten Profilattributs basieren. Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Besucher zuletzt der Warteschlange hinzugefügt hat.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Dropdownliste **[!UICONTROL Empfehlungsschlüssel]** aus (z. B. „Zuletzt zur Watchlist hinzugefügt“).
1. Wählen Sie dann Ihre **[!UICONTROL Empfehlungslogik]** aus (z. B. „Personen, die das ansahen, sahen auch dies an“).

   ![Neues Kriteriendialogfeld erstellen](/help/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Wenn Ihr benutzerdefiniertes Profilattribut nicht direkt mit einer Entitäts-ID übereinstimmt, müssen Sie [!DNL Recommendations] erläutern, wie die Übereinstimmung mit einer Entität erfolgen soll. Angenommen, Sie möchten die wichtigsten Verkaufselemente aus der beliebtesten Marke eines Besuchers anzeigen.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Dropdownliste **[!UICONTROL Empfehlungsschlüssel]** aus (z. B. „Lieblingsmarke“).

1. Wählen Sie dann die **[!UICONTROL Empfehlungslogik]**, die Sie mit diesem Schlüssel verwenden möchten (z. B. „Topverkäufe“).

   Die Option [!UICONTROL Gruppieren nach individuellem Wert] wird angezeigt.

1. Wählen Sie das Entitätsattribut aus, das dem ausgewählten Schlüssel entspricht. In diesem Fall stimmt „Lieblingsmarke“ mit `entity.brand` überein.

   [!DNL Recommendations] erstellt nun für jede Marke eine Liste der Topverkäufe und zeigt den Besucher die entsprechende Liste „Topverkäufe“ basierend auf dem Wert an, der im Profilattribut „Lieblingsmarke“ des Besuchers gespeichert ist.

   ![Neues Kriteriendialogfeld erstellen 2](/help/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Zuletzt gekaufter Artikel

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor gekauft wurde. Dies wird automatisch erfasst, und es müssen keine Werte auf der Seite weitergereicht werden.

#### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

#### Verwendung auf Ihrer Site

* Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.
* NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

### Zuletzt angezeigter Artikel

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor angezeigt wurde. Dies wird automatisch erfasst, und es müssen keine Werte auf der Seite weitergereicht werden.

#### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

#### Verwendung auf Ihrer Site

* Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.
* NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

### Am häufigsten angezeigter Artikel

Die Empfehlung wird von dem Artikel bestimmt, der am häufigsten angezeigt wurde, wobei dieselbe Methode wie für die bevorzugte Kategorie verwendet wird.

Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Ansicht
* 5 Punkte für alle folgenden Ansichten
* Am Ende der Sitzung alle Werte durch 2 teilen

Beispiel: Die Anzeige von Surfbrett A und Surfbrett B in einer Sitzung führt zu folgendem Ergebnis: A: 10 und B: 5. Am Ende der Sitzung ist das Ergebnis A: 5 und B: 2,5. Wenn Sie dieselben Artikel in der nächsten Sitzung anzeigen, ändern sich die Werte in A: 15 und B: 7,5.

#### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

#### Verwendung auf Ihrer Site

* Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

### Favoritenkategorie

Die Empfehlung wird von der Kategorie bestimmt, die am meisten Aktivität verzeichnete, wobei dieselbe Methode wie für den am häufigsten angezeigten Artikel verwendet wird, statt Produkten jedoch Kategorien bewertet werden.

Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Kategorieansicht
* 5 Punkte für alle folgenden Ansichten

Kategorien, die zum ersten Mal besucht werden, erhalten 10 Punkte. Für nachfolgende Besuche derselben Kategorie werden 5 Punkte vergeben. Bei jedem Besuch werden nicht aktuelle Kategorien, die zuvor besucht wurden, um 1 reduziert.

Beispiel: Die Anzeige von Kategorie A und Kategorie B in einer Sitzung führt zu folgendem Ergebnis: A: 9 und B: 10. Wenn Sie in der nächsten Sitzung dieselben Elemente ansehen, ändern sich die Werte in A: 20 B: 9.

#### Logik (Kriterien)

* [!UICONTROL Topverkäufe]
* [!UICONTROL Am häufigsten angezeigt]

#### Verwendung auf Ihrer Site

* Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

### Beliebtheit

Die Empfehlung wird von den am meisten bevorzugten Artikeln auf Ihrer Site bestimmt. Unter „Popularität“ fallen Topverkäufe und die am häufigsten nach Mbox-Daten angezeigten Artikel sowie bei der Verwendung von Adobe Analytics alle verfügbaren Metriken im Produktbericht. Die Artikel werden je nach ausgewählter Recommendations-Logik in eine Rangfolge gebracht.

#### Logik (Kriterien)

* [!UICONTROL Topverkäufe]
* [!UICONTROL Am häufigsten angezeigt]
* Produktberichtsmetriken (bei der Verwendung von Adobe Analytics)

#### Verwendung auf Ihrer Site

* Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

### Vor Kurzem aufgerufene Artikel  {#recently-viewed}

Nutzt den Verlauf des Benutzers (sitzungsübergreifend) für die Anzeige der letzten *x* vom Besucher angesehenen Artikel, basierend auf der Anzahl x der im Entwurf vorhandenen Plätze.

Das Kriterium „Kürzlich angezeigte Elemente“ liefert jetzt Ergebnisse speziell für die jeweilige [Umgebung](/help/administrating-target/hosts.md). Wenn zwei Sites zu unterschiedlichen Umgebungen gehören und ein Besucher zwischen den beiden Sites wechselt, zeigt jede Site nur die jeweiligen Elemente der entsprechenden Umgebung an. Wenn zwei Sites in derselben Umgebung enthalten sind und ein Besucher zwischen ihnen wechselt, erhält er die kürzlich angezeigten Elemente für beide Sites.

#### Verwendung auf Ihrer Site

* Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

>[!NOTE]
>
>Vor Kurzem aufgerufene Artikel  berücksichtigt sowohl globale Ausschlüsse als auch die ausgewählte Sammlungseinstellung für die Aktivität. Wenn ein Artikel durch einen globalen Ausschluss ausgeschlossen oder nicht in der ausgewählten Sammlung enthalten ist, wird er nicht angezeigt. Daher sollte bei Verwendung des Kriteriums „Vor Kurzem aufgerufene Artikel“ die Einstellung „Alle Sammlungen“ verwendet werden.

## Empfehlungslogik

[!DNL Target Recommendations] verwendet komplexe Algorithmen, um zu ermitteln, wann die Aktionen eines Benutzers den für Ihre Aktivität festgelegten Kriterien entsprechen. Der Empfehlungsschlüssel bestimmt die verfügbaren Optionen der Empfehlungslogik.

Die folgende Empfehlungslogik (Kriterien) steht in der Dropdown-Liste [!UICONTROL Empfehlungslogik] zur Verfügung:

### Artikel/Medien mit ähnlichen Attributen

Empfiehlt auf Grundlage von aktueller Seitenaktivität oder früherem Besucherverhalten Artikel oder Medien, die eine Ähnlichkeit zu anderen Artikeln oder Medien aufweisen.

Wenn Sie Elemente/Medien mit ähnlichen Attributen auswählen, haben Sie die Möglichkeit, Regeln zur Ähnlichkeit von Inhalten festzulegen.

Die Verwendung der Ähnlichkeit von Inhalten zum Generieren von Empfehlungen ist besonders wirksam für neue Artikel, die in Empfehlungen mit Personen, die dies angesehen haben, sahen dies an, und anderer Logik, die auf dem bisherigen Verhalten basiert, nicht angezeigt werden. Anhand der Ähnlichkeit von Inhalten können sinnvolle Empfehlungen für neue Benutzer erstellt werden, für die noch keine historischen Daten oder Einkäufe verzeichnet wurden.

Weitere Informationen finden Sie unter [Ähnlichkeit](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity)von Inhalten.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Am häufigsten angezeigt

Zeigt die Artikel oder Medien an, die am häufigsten auf Ihrer Site angezeigt werden.

Mit dieser Logik können Sie Empfehlungen basierend auf den am häufigsten angezeigten Artikeln auf Ihrer Site anzeigen, um die Konversionen für andere Elemente zu erhöhen. Beispielsweise könnte eine Mediensite Empfehlungen für die am häufigsten angezeigten Videos auf ihrer Startseite anzeigen, um Besucher dazu anzuregen, sich weitere Videos anzusehen.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktuelle Kategorie
* Benutzerspezifisches Attribut 
* Favoritenkategorie
* Beliebtheit

### Personen, die das kauften, kauften dies

Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel.

Mit dieser Logik können Sie Querverkaufsmöglichkeiten erhöhen, indem Sie beispielsweise eine Empfehlung auf einer Zusammenfassungsseite des Einkaufswagens anzeigen, die Artikel anzeigt, die andere Käufer ebenfalls gekauft haben. Wenn der Besucher z. B. einen Anzug kauft, könnte die Empfehlung weitere Artikel anzeigen, die andere Besucher zusammen mit dem Anzug gekauft haben, z. B. Krawatten, Kleiderschuhe und Gurtbänder. Wenn Besucher ihre Käufe überprüfen, geben Sie ihnen zusätzliche Empfehlungen.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Benutzerspezifisches Attribut 
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das ansahen, kauften dies

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. Dieses Kriterium gibt andere Produkte zurück, die Personen nach dem Ansehen dieses Artikels gekauft haben. Das angegebene Produkt ist nicht in der Ergebnismenge enthalten.

Mit dieser Logik können Sie Querverkaufsmöglichkeiten erhöhen, indem Sie z. B. eine Empfehlung auf einer Produktseite anzeigen, die Artikel anzeigt, die andere Besucher gekauft haben. Wenn der Besucher z. B. einen Angelpol anzeigt, könnte die Empfehlung weitere Artikel anzeigen, die andere Besucher gekauft haben, wie z. B. Angelschachteln, Geflügel und Fischköpfe. Wenn Besucher Ihre Site durchsuchen, geben Sie ihnen zusätzliche Kaufempfehlungen.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Benutzerspezifisches Attribut 
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Personen, die das ansahen, sahen auch dies an

Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird.

Mit dieser Logik können Sie zusätzliche Konvertierungsmöglichkeiten erstellen, indem Sie Artikel empfehlen, die andere Besucher, die einen Artikel angesehen haben, ebenfalls angesehen haben. Besucher, die beispielsweise Fahrräder auf Ihrer Site Ansicht haben, können sich auch Fahrradhelme, Fahrradsätze, Schlösser usw. ansehen. Sie können eine Empfehlung mit dieser Logik erstellen, die andere Produkte vorschlägt, um den Umsatz zu steigern.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Benutzerspezifisches Attribut 
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Site-Affinität

Empfiehlt Artikel auf Grundlage der Wahrscheinlichkeit eines Zusammenhangs zwischen Artikeln. Sie können dieses Kriterium anhand des Reglers „Einschlussregeln“ konfigurieren und festlegen, wie viele Daten gesammelt werden sollen, bevor eine Empfehlung angezeigt wird. Wenn Sie zum Beispiel Sehr stark auswählen, werden nur Produkte mit der höchsten Wahrscheinlichkeit einer Übereinstimmung empfohlen.

Beispiel: Sie legen eine sehr starke Affinität fest und Ihr Entwurf umfasst fünf Artikel, von denen drei den Schwellenwert für einen wahrscheinlichen Zusammenhang übersteigen. Die zwei Artikel, die die Voraussetzung nicht erfüllen, werden nicht in Ihren Empfehlungen angezeigt und durch von Ihnen definierte Ersatzartikel ausgetauscht. Die Artikel mit der stärksten Affinität werden zuerst angezeigt.

Beispielsweise kann ein Online-Händler Artikel bei nachfolgenden Besuchen empfehlen, an denen ein Besucher während vergangener Sitzungen Interesse gezeigt hat. Die Aktivität für die Sitzung jedes Besuchers wird erfasst, um eine Affinität basierend auf einem Neuigkeits- und Häufigkeitsmodell zu berechnen. Wenn dieser Besucher zu Ihrer Site zurückkehrt, wird die Site-Affinität verwendet, um Empfehlungen anzuzeigen, die auf früheren Aktionen auf Ihrer Site basieren.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel

### Topverkäufe

Zeigt die Artikel an, die in den am häufigsten abgeschlossenen Bestellungen enthalten sind. Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung.

Mit dieser Logik können Sie Empfehlungen für Artikel mit Top-Verkaufs auf Ihrer Site erstellen, um die Umrechnung und den Umsatz zu steigern. Diese Logik eignet sich besonders für erstmalige Besucher Ihrer Site.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Favoritenkategorie
* Beliebtheit

### Benutzerbasiertes Recommendations

Empfiehlt Artikel basierend auf dem Browsen, Anzeigen und Kaufverlauf jedes Besuchers. Diese Elemente werden allgemein als &quot;Empfohlen für Sie&quot;bezeichnet.

Mithilfe dieser Kriterien können Sie personalisierte Inhalte und Erlebnisse sowohl für neue als auch für wiederkehrende Besucher bereitstellen. Die Liste der Empfehlungen wird mit der neuesten Aktivität des Besuchers gewichtet und während der Sitzung aktualisiert und personalisiert, während der Benutzer Ihre Site besucht.

Sowohl Ansichten als auch Einkäufe werden zur Bestimmung der empfohlenen Artikel verwendet. Der angegebene Empfehlungsschlüssel (z. B. &quot;Aktuelles Element&quot;) wird verwendet, um die von Ihnen gewählten Einschlussregel-Filter anzuwenden.

Sie können zum Beispiel:

* Ausschließen von Artikeln, die bestimmte Kriterien nicht erfüllen (Produkte nicht vorrätig, Artikel, die vor mehr als 30 Tagen veröffentlicht wurden, Filme mit R usw.).
* Begrenzen Sie die eingeschlossenen Elemente auf eine einzige Kategorie oder auf die aktuelle Kategorie.

Diese Logik kann mit den folgenden Empfehlungsschlüsseln verwendet werden:

* Aktueller Artikel
* Zuletzt gekaufter Artikel
* Zuletzt angezeigter Artikel
* Am häufigsten angezeigter Artikel