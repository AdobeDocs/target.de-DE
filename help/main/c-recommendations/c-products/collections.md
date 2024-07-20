---
keywords: Sammlung; Targeting
description: Erfahren Sie, wie Sie Sammlungen von Produkten oder Elementen in [!DNL Target Recommendations] verwenden.
title: Wie verwende ich Sammlungen in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: c8bd2bb45ee8ef1a849fd9091554caec77effba0
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 40%

---

# Sammlungen

Eine Sammlung ist ein Satz von Produkten oder Artikeln, die für eine Empfehlung infrage kommen. Eine Kollektion wird definiert, indem die Bedingungen angegeben werden, die von Elementen erfüllt werden müssen, die Teil der Kollektion sein sollen.

Im Allgemeinen ist eine Sammlung ein Satz von ähnlichen oder verwandten Artikeln, wie zum Beispiel eine Sammlung eines einzigen Produkts. Sie können jedoch alle Artikel in eine Kategorie gruppieren, die für Ihr Unternehmen sinnvoll ist, z. B. Produkte in einem bestimmten Preisbereich oder in einer bestimmten Farbe oder Artikel, die in einem bestimmten geografischen Gebiet wahrscheinlich interessant sind.

Verwenden Sie Sammlungen, um Ihre Produkte in logischen Behältern zu organisieren. Wenn beispielsweise einige Elemente in einer Region, aber nicht in einer anderen verfügbar sind, können Sie eine Sammlung erstellen, die Elemente ausschließt, die in der Region des Besuchers nicht verfügbar sind. Sie können Sammlungen auch verwenden, um Saisonartikel oder beliebige andere organisatorische Parameter, die für Ihr Geschäft relevant sind, zu organisieren.

Die für jedes Kriterium innerhalb der Empfehlung erzeugte [Reserveempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md) verwendet ebenfalls die Sammlung, sodass nur Artikel aus der Sammlung in die Reserveempfehlung aufgenommen werden. Mit Sammlungen können Sie sicherstellen, dass nur Produkte an einem Ort angezeigt werden, für die dies Sinn macht.

Sammlungen werden stets neu erstellt oder aktualisiert, wenn die einzelnen Kriterien ausgeführt werden.

Sie können Ihre Artikel in Katalogen gruppieren und dann separate Empfehlungen für jede Sammlung erstellen.

Inklusionskriterien ermöglichen Ihnen etwas Ähnliches wie eine Sammlung, sie müssen jedoch jedes Mal eingerichtet werden, wenn Sie eine Aktivität erstellen. Sammlungen ermöglichen Ihnen, einen Satz von Artikeln auf einmal zu erstellen und diesen dann zu jeder passenden Gelegenheit zu verwenden, ohne dass Sie diesen erneut einrichten müssen.

Wenn Sie eine [!DNL Recommendations] -Aktivität erstellen oder bearbeiten, wird der Sammlungsname neben der [!UICONTROL Criteria] -Beschriftung im Aktivitätsdiagramm angezeigt.

>[!NOTE]
>
>Sammlungen werden bei Verwendung des Empfehlungsschlüssels [!UICONTROL Recently Viewed Items] nicht angewendet.

## Sammlung erstellen {#task_1256DFF6842141FCAADD9E1428EF7F08}

Erstellen Sie eine Sammlung, um die Produkte oder Inhalte zu organisieren, die Sie in Ihren Empfehlungen anzeigen möchten.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** , um die Liste der vorhandenen Sammlungen anzuzeigen.

   ![Sammlungsliste](assets/collections_list.png)

   Auf der Seite &quot;[!UICONTROL Collections]&quot; wird eine Liste Ihrer vorhandenen Sammlungen angezeigt. Sie erstellen neue Sammlungen, indem Sie auf die Schaltfläche [!UICONTROL Create Collection] klicken. Sie können auch vorhandene Sammlungen bearbeiten, kopieren und löschen, indem Sie den Mauszeiger über die gewünschte Sammlung bewegen und auf das gewünschte Symbol klicken.

   ![Maussymbole: Bearbeiten, Kopieren und Löschen](/help/main/c-recommendations/c-products/assets/hover-icons.png)

   Die für jede Sammlung in der Listenansicht &quot;[!UICONTROL Collections]&quot;gemeldete &quot;Anzahl von Elementen&quot;ist die Anzahl der Produkte, die mit den Regeln für diese Sammlung in der konfigurierten standardmäßigen Recommendations-[Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) übereinstimmen. Informationen zum Ändern der standardmäßigen Hostgruppe finden Sie unter [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} .

1. Klicken Sie auf **[!UICONTROL Create Collection]**.

1. (Bedingt) Wählen Sie beim Erstellen (oder Aktualisieren) einer Sammlung eine Umgebung aus dem Filter **[!UICONTROL Environment]** , um eine Vorschau des Inhalts der Sammlung in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Sammlung erstellen](/help/main/c-recommendations/c-products/assets/CreateCollection.png)

1. Geben Sie einen **[!UICONTROL Name]** für die Sammlung ein.

   Sie können auch einen optionalen Wert **[!UICONTROL Description]** eingeben.

1. Legen Sie die Regeln fest, die für den Aufbau der Sammlung verwendet werden.

   Ihre Sammlung kann beispielsweise auf einer Produkt-ID oder Kategorie, Marge oder einem anderen Parameter in der Liste basieren.

   Sie können Regeln hinzufügen, um eine Sammlung durch mehrere Parameter zu definieren. Mehrere Regeln werden mit einem UND-Operator verbunden. Alle angegebenen Regeln müssen eingehalten werden, damit die Sammlung angewendet wird.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Erstellen einer Sammlung mit der erweiterten Suche

Sie können Sammlungen auch mithilfe der erweiterten Suche auf der Seite [Katalogsuche](/help/main/c-recommendations/c-products/catalog-search.md#save-as) ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]) erstellen.

![Als Dialogfeld speichern](/help/main/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie beispielsweise eine Suche mit &quot;id > contains&quot; erstellt haben, können Sie auf [!UICONTROL Save As] > [!UICONTROL Collection] klicken.

>[!IMPORTANT]
>
>Bei der Funktion „Erweiterte Suche“ wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die zum Zeitpunkt der Auslieferung zurückgegebenen Produkte basieren jedoch auf der Suche mit Unterscheidung zwischen Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Kollektionen auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt.

## Bearbeiten, Kopieren oder Löschen einer Sammlung

Bewegen Sie den Mauszeiger über die gewünschte Sammlung in der Liste und klicken Sie auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Maussymbole für eine Sammlung](/help/main/c-recommendations/c-products/assets/hover-collections.png)

Sie können eine vorhandene Sammlung kopieren, um eine doppelte Sammlung zu erstellen, die Sie dann ändern können. Auf diese Weise können Sie einen ähnlichen Ausschluss mit geringerem Aufwand erstellen.

Beachten Sie, dass Sammlungen für das gesamte Konto verfügbar sind. Beachten Sie dies vor dem Löschen einer Sammlung. Gelöschte Sammlungen können nicht wiederhergestellt werden.

## Verwenden einer Sammlung in einer Recommendations-Aktivität

1. Erstellen Sie eine Sammlung mit einer der oben genannten Methoden.

1. Klicken Sie auf **[!UICONTROL Activities]** und [erstellen Sie eine neue Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) -Aktivität oder bearbeiten Sie eine vorhandene Aktivität.

1. Nachdem Sie ein Kriterium und einen Entwurf ausgewählt haben, wird die Seite &quot;[!UICONTROL Options]&quot;angezeigt, auf der Sie die gewünschte Sammlung auswählen.

   ![Sammlungsoption auswählen](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Bedingt) Um eine vorhandene Sammlungseinstellung zu ändern, klicken Sie auf der Seite **[!UICONTROL Experiences]** (Schritt 2 des dreiteiligen geführten Workflows) auf eine Stelle, an der Sie Empfehlungen platziert haben, klicken Sie auf **[!UICONTROL Change Collection]** und wählen Sie dann die gewünschte Sammlung aus.

   ![Option &quot;Sammlung ändern&quot;](/help/main/c-recommendations/c-products/assets/change-collection.png)

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)
