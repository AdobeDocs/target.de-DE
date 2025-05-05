---
keywords: Sammlung; Targeting
description: Erfahren Sie, wie Sie Sammlungen von Produkten oder Elementen in  [!DNL Target Recommendations] verwenden.
title: Wie verwende ich Sammlungen in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: be9cb6da17f125c127d64ed8f9002987188fdf3d
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 25%

---

# Sammlungen

Eine Sammlung ist ein Satz von Produkten oder Elementen, die für eine Empfehlung geeignet sind. Eine Auflistung wird definiert, indem die Bedingungen angegeben werden, die von Elementen erfüllt werden müssen, damit sie Teil der Auflistung sind.

Im Allgemeinen ist eine Sammlung ein Satz von ähnlichen oder verwandten Artikeln, wie zum Beispiel eine Sammlung eines einzigen Produkts. Sie können jedoch beliebige Artikel in einer Kategorie gruppieren, die für Ihr Unternehmen sinnvoll ist, wie z. B. Produkte in einer bestimmten Preisklasse oder Farbe oder Artikel, die in einem bestimmten geografischen Gebiet interessant sein könnten.

Verwenden Sie Sammlungen, um Ihre Produkte in logischen Behältern zu organisieren. Wenn beispielsweise einige Elemente in einer Region, aber nicht in einer anderen Region verfügbar sind, können Sie eine Sammlung erstellen, die Elemente ausschließt, die in der Region des Besuchers nicht verfügbar sind. Sie können Sammlungen auch verwenden, um Saisonartikel oder beliebige andere organisatorische Parameter, die für Ihr Geschäft relevant sind, zu organisieren.

[Sicherungsempfehlungen](/help/main/c-recommendations/c-algorithms/backup-recs.md), die für jedes Kriterium in der Empfehlung generiert werden, verwenden ebenfalls diese Sammlung, sodass nur Elemente in der Sammlung in die Sicherungsempfehlung aufgenommen werden. Mit Sammlungen können Sie sicherstellen, dass nur Produkte an einem Ort angezeigt werden, für die dies Sinn macht.

Sammlungen werden stets neu erstellt oder aktualisiert, wenn die einzelnen Kriterien ausgeführt werden.

Sie können Ihre Artikel in Katalogen gruppieren und dann separate Empfehlungen für jede Sammlung erstellen.

Inklusionskriterien ermöglichen Ihnen etwas Ähnliches wie eine Sammlung, sie müssen jedoch jedes Mal eingerichtet werden, wenn Sie eine Aktivität erstellen. Mit Sammlungen können Sie einen Satz von Elementen einmal erstellen und dann immer verwenden, wenn dies sinnvoll ist, ohne ihn erneut einrichten zu müssen.

Beim Erstellen oder Bearbeiten einer [!DNL Recommendations] Aktivität wird der Sammlungsname neben der [!UICONTROL Criteria] im Aktivitätsdiagramm angezeigt.

>[!NOTE]
>
>* Sammlungsregeln gelten für Empfehlungselemente, die nach der Ausführung der Kriterien generiert werden. Sie wirken sich nur auf Entitätsempfehlungen (Entity Recommendations, ERs) in der Ausgabe aus, nicht auf den Schlüssel.
>
>* Sammlungen werden bei Verwendung des [!UICONTROL Recently Viewed Items] Empfehlungsschlüssels nicht angewendet.

## Sammlung erstellen {#task_1256DFF6842141FCAADD9E1428EF7F08}

Erstellen Sie eine Sammlung, um die Produkte oder Inhalte zu organisieren, die Sie in Ihren Empfehlungen anzeigen möchten.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** , um die Liste der vorhandenen Sammlungen anzuzeigen.

   Auf der Seite [!UICONTROL Collections] wird eine Liste Ihrer vorhandenen Sammlungen angezeigt. Durch Klicken auf die Schaltfläche [!UICONTROL Create Collection] erstellen Sie neue Sammlungen. Sie können auch vorhandene Sammlungen bearbeiten, kopieren und löschen, indem Sie auf das Symbol Mehr Aktionen ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben der gewünschten Sammlung und dann auf die gewünschte Option klicken.

   Die für jede Sammlung in der [!UICONTROL Collections] Listenansicht gemeldete „Anzahl der Elemente“ ist die Anzahl der Produkte, die den Regeln für diese Sammlung in der konfigurierten standardmäßigen Recommendations-[ (Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) entsprechen. Siehe [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=de){target=_blank}, um die Standard-Hostgruppe zu ändern.

1. Klicken Sie auf **[!UICONTROL Create Collection]**.

1. Geben Sie einen **[!UICONTROL Name]** für die Sammlung ein.

   Sie können auch eine optionale **[!UICONTROL Description]** eingeben.

1. (Bedingt) Wählen Sie [ Filter „Umgebung](/help/main/administrating-target/environments.md) aus dem **[!UICONTROL Environment]** beim Erstellen (oder Aktualisieren) einer Sammlung aus, um die Inhalte der Sammlung in dieser Umgebung in der Vorschau anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

1. Legen Sie die Regeln fest, die für den Aufbau der Sammlung verwendet werden.

   Ihre Sammlung kann beispielsweise auf einer Produkt-ID oder Kategorie, Marge oder einem anderen Parameter in der Liste basieren.

   Sie können Regeln hinzufügen, um eine Sammlung durch mehrere Parameter zu definieren. Mehrere Regeln werden mit einem AND-Operator verbunden. Alle angegebenen Regeln müssen eingehalten werden, damit die Sammlung angewendet wird.

1. Klicken Sie auf **[!UICONTROL Create]**.

<!-- ## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. -->

## Bearbeiten, Kopieren oder Löschen einer Sammlung

Klicken Sie auf ![ ( Symbol „Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben der gewünschten Sammlung in der Liste und klicken Sie dann auf das entsprechende Symbol: [!UICONTROL Edit], [!UICONTROL Copy] oder [!DNL Delete].

Sie können eine vorhandene Sammlung kopieren, um eine doppelte Sammlung zu erstellen, die Sie dann ändern können. Auf diese Weise können Sie mit weniger Aufwand eine ähnliche Sammlung erstellen.

Beachten Sie, dass Sammlungen im gesamten Konto verfügbar sind. Berücksichtigen Sie dies, bevor Sie eine Sammlung löschen. Gelöschte Sammlungen können nicht wiederhergestellt werden.

## Verwenden einer Sammlung in einer [!DNL Recommendations] Aktivität

1. Erstellen Sie eine Sammlung mit einer der oben genannten Methoden.

1. Klicken Sie auf **[!UICONTROL Activities]** und [Erstellen einer neuen Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md)Aktivität oder bearbeiten Sie eine vorhandene Aktivität.

1. Nachdem Sie ein Kriterium und einen Entwurf ausgewählt haben, wird die [!UICONTROL Options] angezeigt, auf der Sie die gewünschte Sammlung auswählen können.

1. (Bedingt) Um eine vorhandene Sammlungseinstellung zu ändern, klicken Sie auf der **[!UICONTROL Experiences]** (Schritt 1 des dreiteiligen geleiteten Workflows) auf eine Stelle, an der Sie Empfehlungen platziert haben, klicken Sie auf **[!UICONTROL Change Collection]** und wählen Sie dann die gewünschte Sammlung aus.
