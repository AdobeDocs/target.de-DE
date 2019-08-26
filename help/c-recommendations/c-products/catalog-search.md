---
description: Die Katalogsuche hilft Ihnen dabei, Produkte oder Inhalte in Ihrem Katalog zu finden.
keywords: Katalog; suchen
seo-description: Mit der Katalogsuche in Adobe Target können Sie die Produkte oder Inhalte in Ihrem Katalog suchen.
seo-title: Katalogsuche in Adobe Target
solution: Target
title: Katalogsuche
title-outputclass: premium
topic: Premium
uuid: e0876963-5905-4850-a615-953e435f26e9
badge: premium
translation-type: tm+mt
source-git-commit: afb87e3e23b44133982e55fdc7650250e6bf8b3a

---


# ![PREMIUM](/help/assets/premium.png) Katalogsuche {#catalog-search}

Die Katalogsuche hilft Ihnen dabei, Produkte oder Inhalte in Ihrem Katalog zu finden.

Um auf Katalogsuche zuzugreifen, klicken **[!UICONTROL Sie auf Recommendations]** &gt; **[!UICONTROL Katalogsuche]**.

Sie können die Suche verfeinern, indem Sie eine Suchoption aus dem Menü „Optionen“ auswählen, das eingeblendet wird, wenn Sie im Suchfeld den Pfeil nach unten betätigen.

![](assets/searchproductsmenu.png)

Zu den Suchoptionen zählen:

* ALLE
* Name
* Marke
* Kategorie
* ID
* Nachricht

**[!UICONTROL ALLE]** durchsucht alle anderen Suchkriterien mithilfe der OR-Logik.

In the search results, you click the **[!UICONTROL Environment]** filter to specify the production [host group environment](/help/administrating-target/hosts.md) whose catalog you are displaying. Sie können die Elemente in den Suchergebnissen auch durchblättern, um Miniaturen und andere Produktinformationen anzuzeigen.

Die neben „Produkte“ angezeigte Nummer ist die Anzahl der Produkte, die von den insgesamt in der angegebenen Umgebung verfügbaren Produkten dem Suchbegriff entsprechen.

Der Katalog wird automatisch aktualisiert, wenn Updates über Feed-Dateien, API oder mbox-Updates empfangen werden. Aktualisierungen werden in der Regel in einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

## Erstellen Sie eine Sammlung oder einen Ausschluss basierend auf der erweiterten Suche.

You can create [collections](/help/c-recommendations/c-products/collections.md) or [exclusions](/help/c-recommendations/c-products/exclusions.md) using Advanced Search on the Catalog Search page ([!UICONTROL Recommendations] &gt; [!UICONTROL Catalog Search] &gt; [!UICONTROL Advanced Search]).

![Speichern unter](/help/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie eine Suche mit "id &gt; contains" erstellt haben, können Sie zum Beispiel auf [!UICONTROL Speichern unter] &gt; [!UICONTROL Sammlung oder Ausschluss] klicken.

>[!IMPORTANT]
>
>Bei der Funktion „Erweiterte Suche“ wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die zum Zeitpunkt der Auslieferung zurückgegebenen Produkte basieren jedoch auf der Suche mit Unterscheidung zwischen Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Kollektionen oder Ausschlüsse auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt. Ausschlüsse werden in ähnlicher Weise gehandhabt.
