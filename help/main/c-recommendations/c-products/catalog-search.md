---
keywords: Katalogsuche;Katalog;Suche;Ausschluss;Sammlung;Filter;Empfehlungen
description: Erfahren Sie, wie Sie mit dem  [!DNL Recommendations] [!UICONTROL Catalog Search] Produkte oder Inhalte finden, Elemente aus Ihrem Katalog entfernen können und vieles mehr.
title: Wie verwende ich das  [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: e60820368eb5a83470dace93acf73709b15d2f9d
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 22%

---

# [!UICONTROL Catalog Search]

Mithilfe der Seite &quot;[!UICONTROL Catalog Search]&quot; in &quot;[!DNL Adobe Recommendations]&quot; können Sie die Produkte oder Inhalte in Ihrem Katalog finden. Die einfachste Aufgabe, die Sie auf dieser Seite ausführen können, ist die Suche nach einem Element. Darüber hinaus können Sie die Umgebung ändern, Facetten filtern, Spalten in der Tabelle ändern, neue Suchfacetten hinzufügen und vieles mehr.

Kataloge beziehen sich auf den gesamten Produktsatz (Entitäten). Ihr Katalog kann viele Sammlungen enthalten, eine Möglichkeit, Ihre Produkte in logischen Gruppen zu organisieren.

## Zugriff auf [!UICONTROL Catalog Search]

1. Klicken Sie auf [!UICONTROL Catalog Search] > **[!UICONTROL Recommendations]**, um auf die Seite **[!UICONTROL Catalog Search]** zuzugreifen.

1. (Optional) Klicken Sie zum Anwenden von Filtern auf Ihre Suche auf das Symbol **[!UICONTROL Show Filters]** ( ![Filtersymbol anzeigen](/help/main/assets/icons/Filter.svg) ). Sie können nach [!UICONTROL Environment], [!UICONTROL Collections], [!UICONTROL Category], [!UICONTROL Brand], [!UICONTROL Inventory] und [!UICONTROL Value] filtern.

## Einfache Suche durchführen

1. Geben Sie einen Suchbegriff in das **[!UICONTROL Search In]** ein.

1. (Optional) Sie können Ihre Suche einschränken, indem Sie eine Suchoption aus dem Optionsmenü auswählen, das angezeigt wird, wenn Sie auf den Abwärtspfeil im [!UICONTROL Search In] klicken.

   Zu den Suchoptionen zählen:

   * ID
   * Name
   * Nachricht

1. Blättern Sie durch die Elemente in den Suchergebnissen, um Miniaturansichten und andere Produktinformationen anzuzeigen.

   >[!NOTE]
   >
   > Wenn Sie einen Katalog nach einem benutzerdefinierten Attribut mit einem numerischen Wert durchsuchen, wird das benutzerdefinierte Attribut als String-Typ (Zeichenfolge) und nicht als numerischer Wert betrachtet.
   >
   >Derzeit ist keine Funktion verfügbar, mit der Sie den Typ eines Attributs ändern können. Wenn Sie eine Änderung vornehmen müssen, eröffnen Sie ein [Supportticket](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie darin die Attribute an, deren Typ von „String“ in „numerisch“ geändert werden muss.

<!--
### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.
-->

## Anzeigen der Details eines Elements

Sie können die Details eines einzelnen Elements, einschließlich ID, Name, Nachricht, Kategorie und mehr, anzeigen, indem Sie dessen Details anzeigen.

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen.

## Entfernen eines Elements aus dem Katalog

1. Klicken Sie in den Suchergebnissen auf ein Element, um die zugehörigen Details anzuzeigen.

1. Klicken Sie auf **[!UICONTROL Remove from Catalog]**.

1. Bestätigen Sie, dass das Element entfernt werden soll.

Alle Informationen zu diesem Element werden aus dem Katalogindex entfernt. Das Element wird nur dann in Ihren Katalog aufgenommen, wenn es erneut einem Daten-Feed hinzugefügt wird. Ein gelöschtes Element muss separat aus Feeds gelöscht werden.

## Katalog aktualisieren

Der Index Ihres Katalogs wird automatisch erstellt, wenn Sie Ihren ersten Feed hochladen, und gemäß dem [&#x200B; angegebenen Zeitplan aktualisiert](/help/main/c-recommendations/c-products/feeds.md#steps).

Der Katalog wird automatisch aktualisiert, wenn Updates über Feed-Dateien, API- oder Mbox-Updates empfangen werden. Aktualisierungen werden in der Regel innerhalb einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

<!--
## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.
-->

## Ändern der Umgebung

Mit [Umgebungen](/help/main/administrating-target/environments.md) können Sie Ihre Standorte und Vorproduktionsumgebungen für eine einfache Verwaltung und getrennte Berichterstellung organisieren.

1. Klicken Sie auf das Symbol &quot;Filter anzeigen&quot; ( ![Symbol &quot;Filter anzeigen&quot; &#x200B;](/help/main/assets/icons/Filter.svg) ).

1. Wählen Sie die gewünschte Umgebung aus der Dropdown-Liste **[!UICONTROL Environment]** aus.

<!--
## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.
-->

## Ändern von Spalten

Sie können die aktiven Spalten auf der Seite &quot;[!UICONTROL Catalog Search]&quot; ändern.

1. Klicken Sie auf das Symbol &quot;**[!UICONTROL Customize Table]**&quot; ( ![Tabellensymbol anpassen](/help/main/assets/icons/ColumnSetting.svg) ).

1. Wählen Sie die gewünschten Spalten aus, die Sie anzeigen oder ausblenden möchten, oder heben Sie die Auswahl auf.

Alle Änderungen, die Sie vornehmen, bleiben sitzungsübergreifend bestehen.
