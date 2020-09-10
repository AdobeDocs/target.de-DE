---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations basiert auf Schlüsseln und verwendet den Verhaltenskontext des Besuchers, um relevante Ergebnisse in Adobe Target Recommendations-Aktivitäten anzuzeigen.
title: Stützen der Empfehlung auf einen Empfehlungsschlüssel
feature: criteria
mini-toc-levels: 2
translation-type: tm+mt
source-git-commit: 00749d54d0416c57364ff648bd0911e636c84bc7
workflow-type: tm+mt
source-wordcount: '1452'
ht-degree: 97%

---


# Stützen der Empfehlung auf einen Empfehlungsschlüssel

Recommendations based on keys utilize visitor behavior context to show relevant results in [!DNL Adobe Target] [!DNL Recommendations] activities.

Es gibt zwei Arten von Recommendations:

* **Beliebtheit:** Führt Elemente gemäß „Am häufigsten angezeigt“, „Topverkäufe“ und „Top-Metriken“ auf. Der Schlüssel ist leer für die Beliebtheitskriterien.
* **Schlüsselbasiert:** Bildet den Rest der Kriterien. Recommendations bietet eine vielfältige Reihe an Auswahlmöglichkeiten in Bezug auf den Schlüsseltyp. Die Möglichkeiten reichen von „Aktueller Artikel“ bis hin zu „Profilparameter“, wodurch Sie den Schlüssel der zu empfehlenden Werte programmgesteuert festlegen können. Sie können mehrere Kriterien miteinander vergleichen, indem Sie festlegen, dass die einzelnen Kriterien auf einem unterschiedlichen Schlüssel basieren.

Jedes Kriterium ist in seinem eigenen Register definiert. Der Traffic wird gleichmäßig auf die verschiedenen Kriterientests verteilt. Anders ausgedrückt wird der Traffic bei zwei vorliegenden Kriterien gleichmäßig zwischen diesen aufgeteilt. Wenn Sie über zwei Kriterien und zwei Entwürfe verfügen, wird der Traffic gleichmäßig zwischen diesen vier Kombinationen aufgeteilt. Sie können auch den Prozentsatz der Websitebesucher festlegen, denen zum Vergleich der standardmäßige Inhalt gezeigt wird. In diesem Fall sieht ein angegebener Prozentsatz von Besuchern den Standardinhalt und der Rest wird auf die Kriterien- und Entwurfskombinationen verteilt.

1. Erstellen Sie eine neue Empfehlung oder wählen Sie eine vorhandene Empfehlung aus und klicken Sie auf **[!UICONTROL Bearbeiten]**.
1. Um den Empfehlungsschlüssel zu ändern, wählen Sie den neuen Schlüssel aus der Dropdown-Liste für [!UICONTROL Empfehlungsschlüssel] aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

   Da sich unterschiedliche Logiken auf unterschiedliche Empfehlungsschlüssel beziehen, werden unterschiedliche Empfehlungen auf unterschiedlichen Seitentypen platziert. Weitere Informationen zu den einzelnen Schlüsseln finden Sie in den folgenden Abschnitten.

## Aktueller Artikel

Die Empfehlung wird vom Artikel bestimmt, den der Besucher momentan ansieht.

Recommendations zeigt andere Artikel an, die den Besucher aufgrund seiner derzeitigen Artikelwahl ebenfalls interessieren könnten.

Wenn diese Option ausgewählt ist, muss der `entity.id`-Wert als Parameter in der Anzeige-Mbox weitergeleitet werden.

### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

### Verwendung auf Ihrer Site

Seiten mit einzelnen Artikeln, beispielsweise Produktseiten.

NICHT auf Seiten ohne Suchergebnisse verwenden.

## Aktuelle Kategorie

Die Empfehlung wird von der Produktkategorie bestimmt, die der Besucher momentan ansieht.

In Empfehlungen werden Produkte aus der angegebenen Produktkategorie angezeigt.

Wenn diese Option ausgewählt ist, muss der `entity.categoryId`-Wert als Parameter an die Anzeige-Mbox weitergeleitet werden.

### Logik (Kriterien)

* Topverkäufe
* Am häufigsten angezeigt

### Verwendung auf Ihrer Site

Seiten mit einer Kategorie.

NICHT auf Seiten ohne Suchergebnisse verwenden.

## Benutzerspezifisches Attribut  {#custom}

Die Empfehlung wird anhand eines Artikels ermittelt, der im Besucherprofil gespeichert ist, entweder mithilfe des Attributs user.*x* oder Profile.*x* Attribute.

Wurde diese Option ausgewählt, muss der Wert `entity.id` im Profilattribut enthalten sein.

### Logik (Kriterien)

* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Gesamtverhalten]
* [!UICONTROL Am häufigsten angezeigt]
* [!UICONTROL Topverkäufe]

Wenn der Schlüssel ein benutzerspezifisches Profilattribut ist und der Algorithmustyp „Am häufigsten angezeigt“ oder „Topverkäufe“ lautet, wird eine neue Dropdownliste namens „Nach eindeutigem Wert gruppieren von“ angezeigt, in der eine Liste bekannter Entitätsattribute (mit Ausnahme von ID, category, margin, value, inventory und environment) vorhanden ist. Dieses Feld ist ein Pflichtfeld.

### Verwendung auf Ihrer Site

Kann auf beliebigen Seiten verwendet werden.

### Verwenden Sie einen benutzerdefinierten Empfehlungsschlüssel.

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

## Zuletzt gekaufter Artikel

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor gekauft wurde. Dies wird automatisch erfasst, und es müssen keine Werte auf der Seite weitergereicht werden.

### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

### Verwendung auf Ihrer Site

Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.

NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

## Zuletzt angezeigter Artikel

Die Empfehlung wird durch den letzten Artikel bestimmt, der von dem jeweiligen Unique Visitor angezeigt wurde. Dies wird automatisch erfasst, und es müssen keine Werte auf der Seite weitergereicht werden.

### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

### Verwendung auf Ihrer Site

Startseite, Seite „Mein Konto“, Offsite-Werbeanzeigen.

NICHT auf Produktseiten oder Seiten verwenden, die für Einkäufe relevant sind.

## Am häufigsten angezeigter Artikel

Die Empfehlung wird von dem Artikel bestimmt, der am häufigsten angezeigt wurde, wobei dieselbe Methode wie für die bevorzugte Kategorie verwendet wird.

Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Ansicht
* 5 Punkte für alle folgenden Ansichten
* Am Ende der Sitzung alle Werte durch 2 teilen

Beispiel: Die Anzeige von Surfbrett A und Surfbrett B in einer Sitzung führt zu folgendem Ergebnis: A: 10 und B: 5. Am Ende der Sitzung ist das Ergebnis A: 5 und B: 2,5. Wenn Sie dieselben Artikel in der nächsten Sitzung anzeigen, ändern sich die Werte in A: 15 und B: 7,5.

### Logik (Kriterien)

* [!UICONTROL Artikel mit ähnlichen Attributen]
* [!UICONTROL Personen, die das ansahen, sahen auch dies an]
* [!UICONTROL Personen, die das ansahen, kauften dies]
* [!UICONTROL Personen, die das kauften, kauften dies]
* [!UICONTROL Site-Affinität]

### Verwendung auf Ihrer Site

Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

## Favoritenkategorie

Die Empfehlung wird von der Kategorie bestimmt, die am meisten Aktivität verzeichnete, wobei dieselbe Methode wie für den am häufigsten angezeigten Artikel verwendet wird, statt Produkten jedoch Kategorien bewertet werden.

Dies wird vom Neuigkeits-/Häufigkeitskriterium bestimmt, das wie folgt funktioniert:

* 10 Punkte für erstmalige Kategorieansicht
* 5 Punkte für alle folgenden Ansichten

Kategorien, die zum ersten Mal besucht werden, erhalten 10 Punkte. Für nachfolgende Besuche derselben Kategorie werden 5 Punkte vergeben. Bei jedem Besuch werden nicht aktuelle Kategorien, die zuvor besucht wurden, um 1 reduziert.

Beispiel: Die Anzeige von Kategorie A und Kategorie B in einer Sitzung führt zu folgendem Ergebnis: A: 9 und B: 10. Wenn Sie in der nächsten Sitzung dieselben Elemente ansehen, ändern sich die Werte in A: 20 B: 9.

### Logik (Kriterien)

* [!UICONTROL Topverkäufe]
* [!UICONTROL Am häufigsten angezeigt]

### Verwendung auf Ihrer Site

Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

## Beliebtheit

Die Empfehlung wird von den am meisten bevorzugten Artikeln auf Ihrer Site bestimmt. Unter „Popularität“ fallen Topverkäufe und die am häufigsten nach Mbox-Daten angezeigten Artikel sowie bei der Verwendung von Adobe Analytics alle verfügbaren Metriken im Produktbericht. Die Artikel werden je nach ausgewählter Recommendations-Logik in eine Rangfolge gebracht.

### Logik (Kriterien)

* [!UICONTROL Topverkäufe]
* [!UICONTROL Am häufigsten angezeigt]
* Produktberichtsmetriken (bei der Verwendung von Adobe Analytics)

### Verwendung auf Ihrer Site

Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

## Vor Kurzem aufgerufene Artikel  {#recently-viewed}

Nutzt den Verlauf des Benutzers (sitzungsübergreifend) für die Anzeige der letzten *x* vom Besucher angesehenen Artikel, basierend auf der Anzahl x der im Entwurf vorhandenen Plätze.

Das Kriterium „Kürzlich angezeigte Elemente“ liefert jetzt Ergebnisse speziell für die jeweilige [Umgebung](/help/administrating-target/hosts.md). Wenn zwei Sites zu unterschiedlichen Umgebungen gehören und ein Besucher zwischen den beiden Sites wechselt, zeigt jede Site nur die jeweiligen Elemente der entsprechenden Umgebung an. Wenn zwei Sites in derselben Umgebung enthalten sind und ein Besucher zwischen ihnen wechselt, erhält er die kürzlich angezeigten Elemente für beide Sites.

### Verwendung auf Ihrer Site

Allgemeine Seiten wie Startseiten oder Landingpages und Offsite-Werbeanzeigen.

>[!NOTE]
>
>Vor Kurzem aufgerufene Artikel  berücksichtigt sowohl globale Ausschlüsse als auch die ausgewählte Sammlungseinstellung für die Aktivität. Wenn ein Artikel durch einen globalen Ausschluss ausgeschlossen oder nicht in der ausgewählten Sammlung enthalten ist, wird er nicht angezeigt. Daher sollte bei Verwendung des Kriteriums „Vor Kurzem aufgerufene Artikel“ die Einstellung „Alle Sammlungen“ verwendet werden.