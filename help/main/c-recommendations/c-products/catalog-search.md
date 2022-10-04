---
keywords: Katalogsuche; Katalog; Suche; Ausschluss; Sammlung; Filter
description: Erfahren Sie, wie Sie mit der Recommendations-Katalogsuche Produkte oder Inhalte suchen, Sammlungen oder Ausschlüsse erstellen, Elemente aus Ihrem Katalog entfernen und vieles mehr.
title: Wie verwende ich die Recommendations-Katalogsuche?
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 22%

---

# ![PREMIUM](/help/main/assets/premium.png) Katalogsuche

Die [!UICONTROL Katalogsuche] Seite in [!DNL Adobe Recommendations] hilft Ihnen, die Produkte oder Inhalte in Ihrem Katalog zu finden. Die einfachste Aufgabe, die Sie auf dieser Seite ausführen können, ist die Suche nach einem Element. Darüber hinaus können Sie die Umgebung ändern, Suchergebnisse in Sammlungen oder Ausschlüssen speichern, Filterfacetten hinzufügen, Spalten in der Tabelle ändern, neue Suchfacetten hinzufügen und vieles mehr.

Kataloge beziehen sich auf den gesamten Produktsatz (Entitäten). Ihr Katalog kann viele Sammlungen enthalten, um Ihre Produkte in logischen Behältern zu organisieren.

## Zugriff auf Katalogsuche

So greifen Sie auf die [!UICONTROL Katalogsuche] Seite, klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Katalogsuche]**.

![Katalogsuchseite](/help/main/c-recommendations/c-products/assets/catalog-search.png)

## Nach einem Element suchen

Sie können eine einfache Suche oder eine erweiterte Suche verwenden, um Elemente in Ihrem Katalog zu finden.

### Einfache Suche durchführen

1. Geben Sie einen Suchbegriff in die **[!UICONTROL Suchprodukte]** -Feld.

1. (Optional) Sie können die Suche verfeinern, indem Sie eine Suchoption aus dem Optionsmenü auswählen, das angezeigt wird, wenn Sie im Suchfeld auf den Abwärtspfeil klicken.

   ![searchproductsmenu image](assets/searchproductsmenu.png)

   Zu den Suchoptionen zählen:

   * ALLE - Durchsucht alle anderen Suchkriterien mithilfe der OR-Logik.
   * Name
   * Marke
   * Kategorie
   * ID
   * Nachricht

1. Sie können jetzt durch die Elemente in den Suchergebnissen blättern, um Miniaturansichten und andere Produktinformationen anzuzeigen.

   Die folgende Abbildung zeigt die Ergebnisse für &quot;bike&quot;mit der Option Alle .

   ![Katalogsuche für Fahrrad](/help/main/c-recommendations/c-products/assets/bike-results.png)

   Die neben „Produkte“ angezeigte Nummer ist die Anzahl der Produkte, die von den insgesamt in der angegebenen Umgebung verfügbaren Produkten dem Suchbegriff entsprechen.

   Beachten Sie, dass Sie die Funktion zum automatischen Vervollständigen der Suche verwenden können. In der folgenden Abbildung werden durch die Eingabe von &quot;bik&quot;alle Produkte zurückgegeben, die das Wort &quot;bike&quot;enthalten.

   ![Automatische Suche](/help/main/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >Wenn Sie einen Katalog nach einem benutzerdefinierten Attribut mit einem numerischen Wert durchsuchen, wird das benutzerdefinierte Attribut als String-Typ (Zeichenfolge) und nicht als numerischer Wert betrachtet.
   >
   >Derzeit gibt es keine Funktion, mit der Sie den Typ eines Attributs ändern können. Wenn Sie eine Änderung vornehmen müssen, eröffnen Sie ein [Supportticket](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie darin die Attribute an, deren Typ von „String“ in „numerisch“ geändert werden muss.

1. Sie können auch Filter verwenden, um das gewünschte Produkt zu finden. Im folgenden Beispiel wird die [!UICONTROL Sammlungen] Facette und Auswahl von &quot;Bike Tools&quot;, alle Fahrradwerkzeuge in Ihrem Katalog anzeigen.

   ![Fahrradwerkzeuge](/help/main/c-recommendations/c-products/assets/bike-results-3.png)

1. Sie können in der Ergebnisliste weiter suchen, indem Sie einen Suchbegriff eingeben, z. B. &quot;chain&quot;.

   ![Suche nach Kette](/help/main/c-recommendations/c-products/assets/bike-results-4.png)

### Erweiterte Suche durchführen {#advanced-search}

Sie können [!UICONTROL Erweiterte Suche] , um Ihre Suchergebnisse weiter zu verfeinern oder Ihre Suchergebnisse als [collection](/help/main/c-recommendations/c-products/collections.md) oder [Ausschluss](/help/main/c-recommendations/c-products/exclusions.md).

1. Klicken Sie auf **[!UICONTROL Erweiterte Suche]** Link.

   ![Erweiterte Suchseite](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Verwenden Sie die Dropdown-Listen, um den Parameter, den Operator und die Werte für Ihre Suche anzugeben.

1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** , um eine zusätzliche Suchregel hinzuzufügen.

   Jede zusätzliche Suchregel wird mit dem UND -Operator verknüpft.

1. Klicken Sie auf **[!UICONTROL Suchen]**.

1. (Optional) Klicken Sie auf **[!UICONTROL Speichern unter]** Klicken Sie auf **[!UICONTROL Sammlung]** oder **[!UICONTROL Ausschluss]**.

   ![Als Optionen speichern](/help/main/c-recommendations/c-products/assets/save-as.png)

   Weitere Informationen finden Sie unter [Erstellen einer Sammlung oder eines Ausschlusses basierend auf der erweiterten Suche](#save-as) unten.

## Details eines Elements anzeigen

Sie können die Details eines einzelnen Elements, einschließlich ID, Name, Nachricht, Kategorie und mehr, anzeigen, indem Sie dessen Details anzeigen.

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

   ![Produktdetails](/help/main/c-recommendations/c-products/assets/bike-results-5.png)

## Entfernen eines Artikels aus dem Katalog

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

1. Klicken **[!UICONTROL Aus Katalog entfernen]**.

1. Bestätigen Sie, dass Sie das Element entfernen möchten.

Alle Informationen zu diesem Element werden aus dem Katalogindex entfernt. Das Element wird nur dann in Ihren Katalog aufgenommen, wenn es erneut in einem Daten-Feed hinzugefügt wird. Ein gelöschtes Element muss separat aus Feeds gelöscht werden.

## Katalog aktualisieren

Der Index Ihres Katalogs wird automatisch erstellt, wenn Sie Ihren ersten Feed hochladen, und entsprechend der Variablen [angegebener Zeitplan](/help/main/c-recommendations/c-products/feeds.md#steps).

Der Katalog wird automatisch aktualisiert, wenn Updates über Feed-Dateien, API- oder Mbox-Updates empfangen werden. Aktualisierungen sind normalerweise in einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

## Erstellen einer Sammlung oder eines Ausschlusses basierend auf der erweiterten Suche {#save-as}

Sie können [Sammlungen](/help/main/c-recommendations/c-products/collections.md) oder [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) mithilfe der erweiterten Suche auf der Seite „Katalogsuche“ ([!UICONTROL Empfehlungen] > [!UICONTROL Katalogsuche] > [!UICONTROL Erweiterte Suche]) erstellen.

1. Führen Sie eine [erweiterte Suche](#advanced-search).

1. Klicken **[!UICONTROL Speichern unter]** Klicken Sie auf **[!UICONTROL Sammlung]** oder **[!UICONTROL Ausschluss]**.

   ![Als Optionen speichern](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >Die [!UICONTROL Erweiterte Suche] die Funktionalität unterscheidet nicht zwischen Groß- und Kleinschreibung; Die zum Zeitpunkt des Versands zurückgegebenen Produkte basieren jedoch auf der Suche nach Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie bei der Erstellung von Kollektionen oder Ausschlüssen, die auf Ergebnissen basieren, unter Verwendung der [!UICONTROL Erweiterte Suche] Funktionalität. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt. Ausschlüsse werden in ähnlicher Weise gehandhabt.

## Umgebung ändern

[Umgebungen](/help/main/administrating-target/environments.md) Sie können Ihre Sites und Umgebungen vor der Produktion organisieren, um eine einfache Verwaltung und separate Berichterstattung zu ermöglichen.

1. Klicken Sie auf den Link Umgebung .

   ![Umgebungslink](/help/main/c-recommendations/c-products/assets/environment.png)

1. Wählen Sie die gewünschte Umgebung aus.

## Seite &quot;Katalogsuche&quot;ändern (Filter und Spalten)

Sie können die verfügbaren Filter und Spalten im [!UICONTROL Katalogsuche] Seite für die aktuelle Sitzung.

### Filter ändern

Sie können zusätzliche Filterfacetten zum [!UICONTROL Katalogsuche] Seite.

1. Im **[!UICONTROL Filter]** Bereich, klicken Sie **[!UICONTROL Ändern]**.

   ![Filterlink ändern](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Wählen Sie die gewünschten Suchfacetten aus (ID, Name, Nachricht usw.) und klicken Sie auf **[!UICONTROL Speichern]**.

   ![Filter hinzufügen](/help/main/c-recommendations/c-products/assets/add-filters.png)

Beachten Sie, dass die zusätzlichen Filterfacetten nur in der aktuellen Sitzung verfügbar sind.

### Spalten ändern

Sie können die aktiven Spalten der [!UICONTROL Katalogsuche] Seite.

1. Klicken Sie auf **[!UICONTROL Spalten]** Link.

   ![Spaltenoptionen](/help/main/c-recommendations/c-products/assets/columns.png)

1. (Bedingt) Um die Reihenfolge der aktiven Spalten neu anzuordnen, ziehen Sie die Spalten in die **[!UICONTROL Aktive Spalten]** in der gewünschten Reihenfolge.

1. (Bedingt) Ziehen Sie Elemente per Drag-and-Drop aus dem **[!UICONTROL Aktive Spalten]** der **[!UICONTROL Inaktive Spalten]** (und umgekehrt).

   Sie können auch auf das Löschsymbol ( x ) neben der Spalte klicken, die Sie vom aktiven zum inaktiven Abschnitt verschieben möchten.

Beachten Sie, dass alle Änderungen, die Sie vornehmen, nur für die aktuelle Sitzung gelten.
