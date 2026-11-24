---
keywords: Katalogsuche;Katalog;Suche;Ausschluss;Sammlung;Filter;Recommendations
description: Erfahren Sie, wie Sie mit [!DNL Recommendations] [!UICONTROL Katalogsuche] Produkte oder Inhalte suchen, Elemente aus Ihrem Katalog entfernen und vieles mehr.
title: Wie verwende ich die [!DNL Recommendations] "[!UICONTROL " &#x200B;]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
TQID: 'https://experienceleague.adobe.com/en3hkFsDjEE86Tc-3vPSiZFy0K47SftZMN6RW0INNic'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 3883dc9752db0a2427f70cb3036fe060c440361a
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 7%
---
# [!UICONTROL Katalogsuche] {#catalog-search}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie den Katalog in durchsuchen, [!DNL Adobe Recommendations] Produkte oder Inhalte zu finden und Elemente zu filtern, anzuzeigen und zu entfernen.

>[!ENDSHADEBOX]

Die **[!UICONTROL Katalogsuche]** in [!DNL Adobe Recommendations] wird verwendet, um die Produkte oder Inhalte im Katalog zu finden. Die einfachste Aufgabe auf dieser Seite besteht darin, nach einem Element zu suchen. Die Seite ermöglicht auch das Ändern der Umgebung, das Filtern von Facetten, das Ändern der Spalten in der Tabelle und mehr.

Der Katalog ist der gesamte Produktsatz (Entitäten). Es kann viele Sammlungen enthalten, die die Produkte in logischen Gruppen organisieren.

Der Index des Katalogs wird beim Hochladen des ersten Feeds automatisch erstellt und gemäß dem [&#x200B; Zeitplan &#x200B;](/help/main/c-recommendations/c-products/feeds.md#steps).

Der Katalog wird automatisch aktualisiert, wenn Aktualisierungen über Feed-Dateien, die API- oder Mbox-Aktualisierungen empfangen werden. Aktualisierungen werden in der Regel innerhalb einer Stunde abgeschlossen. Wenn Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet wurde. Wenn keine Aktualisierungen ausgeführt werden, wird der Zeitpunkt angezeigt, zu dem das letzte Update gestartet und abgeschlossen wurde.

## Katalog durchsuchen

Verwenden Sie die Suchergebnisse, um die Elemente im Katalog zu überprüfen und bei Bedarf Elemente aus dem Katalog zu entfernen.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Katalogsuche]**.

1. (Optional) Um die Ergebnisse zu filtern, klicken Sie auf das Symbol **[!UICONTROL Filter anzeigen]** ( ![Symbol „Filter anzeigen](/help/main/assets/icons/Filter.svg) ) und wählen Sie dann die anzuwendenden Filter aus. Die verfügbaren Filter sind **[!UICONTROL Umgebung]**, **[!UICONTROL Sammlungen]**, **[!UICONTROL Kategorie]**, **[!UICONTROL Marke]**, **[!UICONTROL Inventar]** und **[!UICONTROL Wert]**.

   [Umgebungen](/help/main/administrating-target/environments.md) Organisieren von Sites und Vorproduktionsumgebungen für die Verwaltung und das separate Reporting. Um die Umgebung zu ändern, wählen Sie die gewünschte Umgebung aus der Dropdown-Liste **[!UICONTROL Umgebung]** aus.

   ![Seite „Katalogsuche“ mit hervorgehobenem Filterbedienfeld: Sammlungen, Kategorie, Marke, Inventar, Wert und erweiterte Suche](../assets/catalog_search.png)

1. Geben Sie einen Suchbegriff in das Feld **[!UICONTROL Suche in]** ein.

1. (Optional) Verfeinern Sie die Suche, indem Sie eine Suchoption aus dem Optionsmenü auswählen, das über den Abwärtspfeil im Feld **[!UICONTROL Suche in]** geöffnet wird.

   Zu den Suchoptionen zählen:

   * ID
   * Name
   * Nachricht

1. Klicken Sie auf das **[!UICONTROL Tabelle anpassen]**-Symbol ( ![Symbol Tabelle anpassen](/help/main/assets/icons/ColumnSetting.svg) ), um die aktiven Spalten auf der Seite **[!UICONTROL Katalogsuche]** zu ändern.

   ![Katalogsuchseite mit hervorgehobenem Symbol „Tabelle anpassen“](../assets/catalog_search_4.png)

1. Scrollen Sie durch die Elemente in den Suchergebnissen, um Miniaturansichten und andere Produktinformationen anzuzeigen.

   >[!NOTE]
   >
   >Bei einer Katalogsuche nach einem benutzerdefinierten Attribut mit einem numerischen Wert wird das benutzerdefinierte Attribut als String-Typ und nicht als numerischer Wert behandelt.
   >
   >Der Typ eines Attributs kann derzeit nicht geändert werden. Um eine Änderung anzufordern, [Öffnen Sie ein Kundenproblem) und verweisen Sie auf &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Attribute, deren Typ von „Zeichenfolge“ in „numerisch“ geändert werden muss.

1. Klicken Sie auf ein Element in den Suchergebnissen, um dessen Details anzuzeigen, einschließlich ID, Name, Nachricht, Kategorie und mehr.

   ![Details eines Katalogelements, das seine ID, Kategorien, Marge und andere Attribute anzeigt](../assets/catalog_search_2.png)

1. Um das Element aus dem Katalog zu entfernen, klicken Sie auf **[!UICONTROL Aus Katalog]**.

   Alle Informationen zu diesem Element werden dann aus dem Katalogindex entfernt. Das Element wird nur dann erneut in den Katalog aufgenommen, wenn es erneut in einem Daten-Feed hinzugefügt wird. Ein gelöschtes Element muss auch getrennt von den Feeds gelöscht werden.

   ![Details eines Katalogelements mit der hervorgehobenen Schaltfläche „Aus Katalog entfernen“](../assets/catalog_search_3.png)

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
