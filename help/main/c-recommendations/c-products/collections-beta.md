---
keywords: Sammlung; Targeting
description: Erfahren Sie, wie Sie Sammlungen von Produkten oder Elementen in [!DNL Target Recommendations].
title: Wie verwende ich Sammlungen in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 31cf23a52c331eabad0e5f6423eeeca84df87625
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 26%

---

# Sammlungen

Eine Sammlung ist ein Satz von Produkten oder Artikeln, die für eine Empfehlung infrage kommen. Eine Kollektion wird definiert, indem die Bedingungen angegeben werden, die von Elementen erfüllt werden müssen, die Teil der Kollektion sein sollen.

Im Allgemeinen ist eine Sammlung ein Satz von ähnlichen oder verwandten Artikeln, wie zum Beispiel eine Sammlung eines einzigen Produkts. Sie können jedoch alle Artikel in eine Kategorie gruppieren, die für Ihr Unternehmen sinnvoll ist, z. B. Produkte in einem bestimmten Preisbereich oder in einer bestimmten Farbe oder Artikel, die in einem bestimmten geografischen Gebiet wahrscheinlich interessant sind.

Verwenden Sie Sammlungen, um Ihre Produkte in logischen Behältern zu organisieren. Wenn beispielsweise einige Elemente in einer Region, aber nicht in einer anderen verfügbar sind, können Sie eine Sammlung erstellen, die Elemente ausschließt, die in der Region des Besuchers nicht verfügbar sind. Sie können Sammlungen auch verwenden, um Saisonartikel oder beliebige andere organisatorische Parameter, die für Ihr Geschäft relevant sind, zu organisieren.

[Reserveempfehlungen](/help/main/c-recommendations/c-algorithms/backup-recs.md) , die für jedes Kriterium innerhalb der Empfehlung generiert wurden, verwenden auch diese Sammlung, sodass nur Artikel aus der Sammlung in die Reserveempfehlung aufgenommen werden. Mit Sammlungen können Sie sicherstellen, dass nur Produkte an einem Ort angezeigt werden, für die dies Sinn macht.

Sammlungen werden stets neu erstellt oder aktualisiert, wenn die einzelnen Kriterien ausgeführt werden.

Sie können Ihre Artikel in Katalogen gruppieren und dann separate Empfehlungen für jede Sammlung erstellen.

Inklusionskriterien ermöglichen Ihnen etwas Ähnliches wie eine Sammlung, sie müssen jedoch jedes Mal eingerichtet werden, wenn Sie eine Aktivität erstellen. Mit Sammlungen können Sie einen Satz von Elementen einmal erstellen und ihn dann immer dann verwenden, wenn dies sinnvoll ist, ohne ihn erneut einrichten zu müssen.

Wenn Sie eine [!DNL Recommendations] -Aktivität wird der Sammlungsname neben dem [!UICONTROL Criteria] im Aktivitätsdiagramm.

>[!NOTE]
>
>Sammlungen werden bei Verwendung der [!UICONTROL Recently Viewed Items] Empfehlungsschlüssel.

## Sammlung erstellen {#task_1256DFF6842141FCAADD9E1428EF7F08}

Erstellen Sie eine Sammlung, um die Produkte oder Inhalte zu organisieren, die Sie in Ihren Empfehlungen anzeigen möchten.

1. Klicks **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** , um die Liste der vorhandenen Sammlungen anzuzeigen.

   ![Sammlungsliste](assets/collections-list.png)

   Die [!UICONTROL Collections] zeigt eine Liste Ihrer vorhandenen Sammlungen an. Sie erstellen neue Sammlungen, indem Sie auf die [!UICONTROL Create Collection] Schaltfläche. Sie können auch vorhandene Sammlungen bearbeiten, kopieren und löschen, indem Sie auf das Suchsymbol neben der gewünschten Sammlung klicken und dann auf die gewünschte Option klicken.

   Die &quot;Anzahl Elemente&quot;, die für jede Sammlung auf der [!UICONTROL Collections] Die Listenansicht ist die Anzahl der Produkte, die mit den Regeln für diese Sammlung innerhalb der konfigurierten standardmäßigen Recommendations übereinstimmen. [Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung). Siehe [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} , um die standardmäßige Hostgruppe zu ändern.

1. Klicken Sie auf **[!UICONTROL Create Collection]**.

   ![Sammlung erstellen](/help/main/c-recommendations/c-products/assets/create-collection.png)

1. Geben Sie einen **[!UICONTROL Name]** für die Sammlung.

   Sie können auch eine optionale **[!UICONTROL Description]**.

1. (Bedingt) Wählen Sie eine [Umgebung](/help/main/administrating-target/environments.md) aus dem **[!UICONTROL Environment]** beim Erstellen (oder Aktualisieren) einer Sammlung filtern, um die Inhalte der Sammlung in dieser Umgebung in der Vorschau anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

1. Legen Sie die Regeln fest, die für den Aufbau der Sammlung verwendet werden.

   Ihre Sammlung kann beispielsweise auf einer Produkt-ID oder Kategorie, Marge oder einem anderen Parameter in der Liste basieren.

   Sie können Regeln hinzufügen, um eine Sammlung durch mehrere Parameter zu definieren. Mehrere Regeln werden mit einem UND-Operator verbunden. Alle angegebenen Regeln müssen eingehalten werden, damit die Sammlung angewendet wird.

1. Klicken Sie auf **[!UICONTROL Create]**.

<!-- ## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. -->

## Bearbeiten, Kopieren oder Löschen einer Sammlung

Klicken Sie auf **Ellipse** neben der gewünschten Sammlung in der Liste und klicken Sie dann auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Maussymbole: Bearbeiten, Kopieren und Löschen](/help/main/c-recommendations/c-products/assets/hover-icons-new.png)

Sie können eine vorhandene Sammlung kopieren, um eine doppelte Sammlung zu erstellen, die Sie dann ändern können. Auf diese Weise können Sie eine ähnliche Sammlung mit geringerem Aufwand erstellen.

Beachten Sie, dass Sammlungen für das gesamte Konto verfügbar sind. Beachten Sie dies vor dem Löschen einer Sammlung. Gelöschte Sammlungen können nicht wiederhergestellt werden.

## Verwenden Sie eine Sammlung in einer [!DNL Recommendations] activity

1. Erstellen Sie eine Sammlung mit einer der oben genannten Methoden.

1. Klicks **[!UICONTROL Activities]** und [Erstellen einer neuen Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) oder eine bestehende Aktivität bearbeiten.

1. Nachdem Sie ein Kriterium und einen Entwurf ausgewählt haben, wird die [!UICONTROL Options] wird angezeigt, wo Sie die gewünschte Sammlung auswählen.

   ![Sammlungsoption auswählen](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Bedingt) Um eine vorhandene Sammlungseinstellung zu ändern, klicken Sie auf **[!UICONTROL Experiences]** Seite (Schritt 2 des dreiteiligen geführten Workflows), klicken Sie auf eine Stelle, an der Sie Empfehlungen platziert haben, und klicken Sie auf **[!UICONTROL Change Collection]** und wählen Sie dann die gewünschte Sammlung aus.

   ![Option &quot;Sammlung ändern&quot;](/help/main/c-recommendations/c-products/assets/change-collection.png)