---
keywords: Katalogsuche;Katalog;Suche;Ausschluss;Sammlung;Filter
description: Erfahren Sie, wie Sie die Recommendations-Katalogsuche verwenden können, um Produkte oder Inhalte zu finden, Sammlungen oder Ausschlüsse zu erstellen, Elemente aus Ihrem Katalog zu entfernen und vieles mehr.
title: Wie verwende ich die Recommendations-Katalogsuche?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 22%

---

# Katalogsuche

Die [!UICONTROL Catalog Search] Seite in [!DNL Adobe Recommendations] hilft Ihnen, die Produkte oder Inhalte in Ihrem Katalog zu finden. Die einfachste Aufgabe, die Sie auf dieser Seite ausführen können, besteht darin, nach einem Element zu suchen. Darüber hinaus können Sie die Umgebung ändern, Suchergebnisse in Sammlungen oder Ausschlüssen speichern, Filterfacetten hinzufügen und Spalten in der Tabelle ändern, neue Suchfacetten hinzufügen und vieles mehr.

Kataloge beziehen sich auf den gesamten Produktsatz (Entitäten). Ihr Katalog kann viele Sammlungen enthalten, sodass Sie Ihre Produkte in logischen Buckets organisieren können.

## Zugriff auf die Katalogsuche

Um auf die Seite [!UICONTROL Catalog Search] zuzugreifen, klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Katalogsuchseite](/help/main/c-recommendations/c-products/assets/catalog-search.png)

## Nach einem Element suchen

Sie können eine einfache Suche oder eine erweiterte Suche verwenden, um Elemente in Ihrem Katalog zu finden.

### Einfache Suche durchführen

1. Geben Sie einen Suchbegriff in das **[!UICONTROL Search Products]** ein.

1. (Optional) Sie können Ihre Suche einschränken, indem Sie eine Suchoption aus dem Optionsmenü auswählen, das angezeigt wird, wenn Sie auf den Abwärtspfeil im Suchfeld klicken.

   ![SearchProductsMenu-Bild](assets/searchproductsmenu.png)

   Zu den Suchoptionen zählen:

   * ALL - Durchsucht alle anderen Suchkriterien mithilfe der OR-Logik.
   * Name
   * Marke
   * Kategorie
   * ID
   * Nachricht

1. Sie können jetzt durch die Elemente in den Suchergebnissen scrollen, um Miniaturansichten und andere Produktinformationen anzuzeigen.

   Die folgende Abbildung zeigt die Ergebnisse für „bike“ mit der Option Alle.

   ![Katalogsuche für Fahrrad](/help/main/c-recommendations/c-products/assets/bike-results.png)

   Die neben „Produkte“ angezeigte Nummer ist die Anzahl der Produkte, die von den insgesamt in der angegebenen Umgebung verfügbaren Produkten dem Suchbegriff entsprechen.

   Beachten Sie, dass Sie die Funktion zum automatischen Vervollständigen der Suche verwenden können. In der folgenden Abbildung werden durch die Eingabe von „bike“ alle Produkte zurückgegeben, die das Wort „bike“ enthalten.

   ![Suche automatisch vervollständigen](/help/main/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >Wenn Sie einen Katalog nach einem benutzerdefinierten Attribut mit einem numerischen Wert durchsuchen, wird das benutzerdefinierte Attribut als String-Typ (Zeichenfolge) und nicht als numerischer Wert betrachtet.
   >
   >Derzeit gibt es keine Funktion, mit der Sie den Typ eines Attributs ändern können. Wenn Sie eine Änderung vornehmen müssen, eröffnen Sie ein [Supportticket](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie darin die Attribute an, deren Typ von „String“ in „numerisch“ geändert werden muss.

1. Sie können auch Filter verwenden, um das gewünschte Produkt zu finden. Im folgenden Beispiel werden durch Erweitern der [!UICONTROL Collections] und Auswahl von „Bike Tools“ alle Bike Tools in Ihrem Katalog angezeigt.

   ![Fahrradwerkzeuge](/help/main/c-recommendations/c-products/assets/bike-results-3.png)

1. Sie können in der Ergebnisliste weiter suchen, indem Sie einen Suchbegriff eingeben, z. B. „Kette“.

   ![Suche nach Kette](/help/main/c-recommendations/c-products/assets/bike-results-4.png)

### Durchführen einer erweiterten Suche {#advanced-search}

Sie können [!UICONTROL Advanced Search] verwenden, um Ihre Suchergebnisse weiter zu verfeinern oder Ihre Suchergebnisse als [Sammlung](/help/main/c-recommendations/c-products/collections.md) oder [Ausschluss](/help/main/c-recommendations/c-products/exclusions.md) zu speichern.

1. Klicken Sie auf den Link **[!UICONTROL Advanced Search]** .

   ![Seite für die erweiterte Suche](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Verwenden Sie die Dropdown-Listen, um den Parameter, den Operator und die Werte für Ihre Suche anzugeben.

1. (Optional) Klicken Sie auf **[!UICONTROL Add Rule]** , um eine zusätzliche Suchregel hinzuzufügen.

   Jede zusätzliche Suchregel ist mit dem AND-Operator verknüpft.

1. Klicken Sie auf **[!UICONTROL Search]**.

1. (Optional) Klicken Sie auf **[!UICONTROL Save As]** und dann auf **[!UICONTROL Collection]** oder **[!UICONTROL Exclusion]**.

   ![Als Optionen speichern](/help/main/c-recommendations/c-products/assets/save-as.png)

   Weitere Informationen finden Sie [Erstellen einer Sammlung oder eines Ausschlusses basierend auf der erweiterten Suche](#save-as) unten.

## Details eines Elements anzeigen

Sie können die Details eines einzelnen Elements, einschließlich ID, Name, Nachricht, Kategorie und mehr, anzeigen, indem Sie dessen Details anzeigen.

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

   ![Produktdetails](/help/main/c-recommendations/c-products/assets/bike-results-5.png)

## Entfernen eines Elements aus dem Katalog

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

1. Klicken Sie auf **[!UICONTROL Remove from Catalog]**.

1. Bestätigen Sie, dass Sie das Element entfernen möchten.

Alle Informationen zu diesem Element werden aus dem Katalogindex entfernt. Das Element wird nur dann in Ihren Katalog aufgenommen, wenn es erneut in einem Daten-Feed hinzugefügt wird. Ein gelöschtes Element muss separat aus Feeds gelöscht werden.

## Katalog aktualisieren

Der Index Ihres Katalogs wird automatisch erstellt, wenn Sie Ihren ersten Feed hochladen, und gemäß dem [ Zeitplan aktualisiert](/help/main/c-recommendations/c-products/feeds.md#steps).

Der Katalog wird automatisch aktualisiert, wenn Updates über Feed-Dateien, API- oder Mbox-Updates empfangen werden. Aktualisierungen sind normalerweise in einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

## Erstellen einer Sammlung oder eines Ausschlusses basierend auf der erweiterten Suche {#save-as}

Sie können [Sammlungen](/help/main/c-recommendations/c-products/collections.md) oder [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md) mithilfe von [!UICONTROL Advanced Search] auf der [!UICONTROL Catalog Search] Seite ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]) erstellen.

1. Führen Sie eine [erweiterte Suche](#advanced-search) durch.

1. Klicken Sie auf **[!UICONTROL Save As]** und dann auf **[!UICONTROL Collection]** oder **[!UICONTROL Exclusion]**.

   ![Als Optionen speichern](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >Bei der [!UICONTROL Advanced Search]-Funktion wird nicht zwischen Groß- und Kleinschreibung unterschieden. Bei Produkten, die zum Zeitpunkt des Versands zurückgegeben werden, wird jedoch zwischen Groß- und Kleinschreibung unterschieden. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie beim Erstellen von Sammlungen oder Ausschlüssen auf der Grundlage von Ergebnissen mithilfe der [!UICONTROL Advanced Search] auf die Groß-/Kleinschreibung. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt. Ausschlüsse werden in ähnlicher Weise gehandhabt.

## Ändern der Umgebung

[Umgebungen](/help/main/administrating-target/environments.md) ermöglichen Ihnen das Organisieren Ihrer Sites und Vorproduktionsumgebungen für einfaches Management und separates Reporting.

1. Klicken Sie auf den Link Umgebung .

   ![Umgebungs-Link](/help/main/c-recommendations/c-products/assets/environment.png)

1. Wählen Sie die gewünschte Umgebung aus.

## Ändern der Seite Katalogsuche (Filter und Spalten)

Sie können die verfügbaren Filter und Spalten auf der Seite [!UICONTROL Catalog Search] für die aktuelle Sitzung vorübergehend ändern.

### Filter ändern

Sie können der [!UICONTROL Catalog Search] zusätzliche Filterfacetten hinzufügen.

1. Klicken Sie im Bedienfeld **[!UICONTROL Filters]** auf **[!UICONTROL Modify]**.

   ![Link „Filter ändern“](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Wählen Sie die gewünschten Suchfacetten (ID, Name, Nachricht usw.) aus und klicken Sie dann auf **[!UICONTROL Save]**.

   ![Filter hinzufügen](/help/main/c-recommendations/c-products/assets/add-filters.png)

Beachten Sie, dass die zusätzlichen Filterfacetten nur in der aktuellen Sitzung verfügbar sind.

### Spalten ändern

Sie können die aktiven Spalten auf der [!UICONTROL Catalog Search] vorübergehend ändern.

1. Klicken Sie auf den Link **[!UICONTROL Columns]** .

   ![Spaltenoptionen](/help/main/c-recommendations/c-products/assets/columns.png)

1. (Bedingt) Um die Reihenfolge der aktiven Spalten neu anzuordnen, ziehen Sie die Spalten per Drag-and-Drop in die gewünschte Reihenfolge im **[!UICONTROL Active Columns]**.

1. (Bedingt) Ziehen Sie Elemente wie gewünscht per Drag-and-Drop aus dem **[!UICONTROL Active Columns]** in den **[!UICONTROL Inactive Columns]** (und umgekehrt).

   Sie können auch auf das Löschsymbol ( x ) neben der Spalte klicken, die Sie aus dem aktiven in den inaktiven Abschnitt verschieben möchten.

Beachten Sie, dass alle von Ihnen vorgenommenen Änderungen nur für die aktuelle Sitzung gelten.
