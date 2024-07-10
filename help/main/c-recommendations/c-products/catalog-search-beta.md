---
keywords: Katalogsuche; Katalog; Suche; Ausschluss; Sammlung; Filter; Empfehlungen
description: Erfahren Sie, wie Sie die [!DNL Recommendations] [!UICONTROL Catalog Search] um Produkte oder Inhalte zu finden, entfernen Sie Elemente aus Ihrem Katalog und vieles mehr.
title: Wie verwende ich die [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 6b0175b1-0eee-498d-8a08-513cf6695114
source-git-commit: 16a7c11e8b9b1a08b1e467519f997d0b05e47529
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 21%

---

# [!UICONTROL Catalog Search]

Die [!UICONTROL Catalog Search] Seite in [!DNL Adobe Recommendations] hilft Ihnen, die Produkte oder Inhalte in Ihrem Katalog zu finden. Die einfachste Aufgabe, die Sie auf dieser Seite ausführen können, ist die Suche nach einem Element. Darüber hinaus können Sie die Umgebung ändern, Facetten filtern, Spalten in der Tabelle ändern, neue Suchfacetten hinzufügen und vieles mehr.

Kataloge beziehen sich auf den gesamten Produktsatz (Entitäten). Ihr Katalog kann viele Sammlungen enthalten, um Ihre Produkte in logischen Behältern zu organisieren.

## Zugriff [!UICONTROL Catalog Search]

So greifen Sie auf die [!UICONTROL Catalog Search] Seite, klicken **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Katalogsuchseite](/help/main/c-recommendations/c-products/assets/catalog-search-new.png)

## Einfache Suche durchführen

1. Geben Sie einen Suchbegriff in die **[!UICONTROL Search In]** -Feld.

1. (Optional) Sie können Ihre Suche verfeinern, indem Sie eine Suchoption aus dem Optionsmenü auswählen, das angezeigt wird, wenn Sie auf den Abwärtspfeil im [!UICONTROL Search In] -Feld.

   Zu den Suchoptionen zählen:

   * ID
   * Name
   * Nachricht

1. Scrollen Sie durch die Elemente in den Suchergebnissen, um Miniaturansichten und andere Produktinformationen anzuzeigen.

   >[!NOTE]
   >
   > Wenn Sie einen Katalog nach einem benutzerdefinierten Attribut mit einem numerischen Wert durchsuchen, wird das benutzerdefinierte Attribut als String-Typ (Zeichenfolge) und nicht als numerischer Wert betrachtet.
   >
   >Es ist derzeit keine Funktion verfügbar, mit der Sie den Typ eines Attributs ändern können. Wenn Sie eine Änderung vornehmen müssen, eröffnen Sie ein [Supportticket](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie darin die Attribute an, deren Typ von „String“ in „numerisch“ geändert werden muss.

   Sie können auch Filter verwenden, um die gewünschten Produkte zu finden. Klicken Sie beispielsweise auf das **[!UICONTROL Show Filters]** Symbol ( ![Symbol Filter anzeigen](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ), erweitern Sie die [!UICONTROL Collections] und anschließend eine oder mehrere Sammlungen auswählen, werden alle Produkte angezeigt, die zu den ausgewählten Sammlungen in Ihrem Katalog gehören.

<!-- ### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.-->

## Details eines Elements anzeigen

Sie können die Details eines einzelnen Elements, einschließlich ID, Name, Nachricht, Kategorie und mehr, anzeigen, indem Sie dessen Details anzeigen.

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

## Entfernen eines Artikels aus dem Katalog

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

1. Klicken Sie auf **[!UICONTROL Remove from Catalog]**.

1. Bestätigen Sie, dass Sie das Element entfernen möchten.

Alle Informationen zu diesem Element werden aus dem Katalogindex entfernt. Das Element wird nur dann in Ihren Katalog aufgenommen, wenn es erneut in einem Daten-Feed hinzugefügt wird. Ein gelöschtes Element muss separat aus Feeds gelöscht werden.

## Katalog aktualisieren

Der Index Ihres Katalogs wird automatisch erstellt, wenn Sie Ihren ersten Feed hochladen, und entsprechend der Variablen [angegebener Zeitplan](/help/main/c-recommendations/c-products/feeds.md#steps).

Der Katalog wird automatisch aktualisiert, wenn Updates über Feed-Dateien, API- oder Mbox-Updates empfangen werden. Aktualisierungen sind in der Regel innerhalb einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

<!-- ## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.-->

## Umgebung ändern

[Umgebungen](/help/main/administrating-target/environments.md) Sie können Ihre Sites und Umgebungen vor der Produktion organisieren, um eine einfache Verwaltung und separate Berichterstattung zu ermöglichen.

1. Klicken Sie auf das Symbol Filter anzeigen ( ![Symbol Filter anzeigen](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ).

1. Wählen Sie die gewünschte Umgebung aus dem **[!UICONTROL Environment]** Dropdown-Liste.

<!-- ## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.-->

## Spalten ändern

Sie können die aktiven Spalten der [!UICONTROL Catalog Search] Seite.

1. Klicken Sie auf **[!UICONTROL Customize Table]** Symbol (  ![Symbol &quot;Tabelle anpassen&quot;](/help/main/c-recommendations/c-products/assets/icon-customize-table.png) ).

1. Aktivieren oder deaktivieren Sie die gewünschten Spalten, die Sie ein- oder ausblenden möchten.

Beachten Sie, dass alle Änderungen, die Sie vornehmen, nur für die aktuelle Sitzung gelten.
