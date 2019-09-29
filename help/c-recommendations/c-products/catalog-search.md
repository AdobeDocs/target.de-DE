---
description: Die Katalogsuche hilft Ihnen dabei, Produkte oder Inhalte in Ihrem Katalog zu finden.
keywords: Katalog; suchen
seo-description: Die Katalogsuche in Adobe Target hilft Ihnen dabei, Produkte oder Inhalte in Ihrem Katalog zu finden.
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

Um auf die Katalogsuche zuzugreifen, klicken Sie auf **[!UICONTROL Recommendations]** &gt; **[!UICONTROL Katalogsuche]**.

Sie können die Suche verfeinern, indem Sie eine Suchoption aus dem Menü „Optionen“ auswählen, das eingeblendet wird, wenn Sie im Suchfeld auf den Abwärtspfeil klicken.

![](assets/searchproductsmenu.png)

Zu den Suchoptionen zählen:

* ALLE
* Name
* Marke
* Kategorie
* ID
* Nachricht

**[!UICONTROL ALLE]** durchsucht alle anderen Suchkriterien mithilfe der ODER-Logik.

Klicken Sie in den Suchergebnissen auf den **[!UICONTROL Umgebungsfilter]**, um die [Umgebung der Produktions-Hostgruppe](/help/administrating-target/hosts.md) anzugeben, deren Katalog Sie anzeigen. Sie können die Elemente in den Suchergebnissen auch durchblättern, um Miniaturen und andere Produktinformationen anzuzeigen.

Die neben „Produkte“ angezeigte Nummer ist die Anzahl der Produkte, die von den insgesamt in der angegebenen Umgebung verfügbaren Produkten dem Suchbegriff entsprechen.

Der Katalog wird automatisch aktualisiert, wenn Updates über Feed-Dateien, API- oder Mbox-Updates empfangen werden. Aktualisierungen sind normalerweise in einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

## Erstellen einer Sammlung oder eines Ausschlusses basierend auf der erweiterten Suche

Sie können [Sammlungen](/help/c-recommendations/c-products/collections.md) oder [Ausschlüsse](/help/c-recommendations/c-products/exclusions.md) mithilfe der erweiterten Suche auf der Seite „Katalogsuche“ ([!UICONTROL Empfehlungen] &gt; [!UICONTROL Katalogsuche] &gt; [!UICONTROL Erweiterte Suche]) erstellen.

![Speichern unter](/help/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie eine Suche mit "id &gt; contains" erstellt haben, können Sie zum Beispiel auf [!UICONTROL Speichern unter] &gt; [!UICONTROL Sammlung oder Ausschluss] klicken.

>[!IMPORTANT]
>
>Bei der Funktion „Erweiterte Suche“ wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die zum Zeitpunkt der Auslieferung zurückgegebenen Produkte basieren jedoch auf der Suche mit Unterscheidung zwischen Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Kollektionen oder Ausschlüsse auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt. Ausschlüsse werden in ähnlicher Weise gehandhabt.
