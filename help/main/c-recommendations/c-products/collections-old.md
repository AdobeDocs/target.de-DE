---
keywords: Sammlung; Targeting
description: Erfahren Sie, wie Sie Sammlungen von Produkten oder Elementen in  [!DNL Target Recommendations] verwenden.
title: Wie verwende ich Sammlungen in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 41%

---

# Sammlungen

Eine Sammlung ist ein Satz von Produkten oder Elementen, die für eine Empfehlung geeignet sind. Eine Auflistung wird definiert, indem die Bedingungen angegeben werden, die von Elementen erfüllt werden müssen, damit sie Teil der Auflistung sind.

Im Allgemeinen ist eine Sammlung ein Satz von ähnlichen oder verwandten Artikeln, wie zum Beispiel eine Sammlung eines einzigen Produkts. Sie können jedoch beliebige Artikel in einer Kategorie gruppieren, die für Ihr Unternehmen sinnvoll ist, wie z. B. Produkte in einer bestimmten Preisklasse oder Farbe oder Artikel, die in einem bestimmten geografischen Gebiet interessant sein könnten.

Verwenden Sie Sammlungen, um Ihre Produkte in logischen Behältern zu organisieren. Wenn beispielsweise einige Elemente in einer Region, aber nicht in einer anderen Region verfügbar sind, können Sie eine Sammlung erstellen, die Elemente ausschließt, die in der Region des Besuchers nicht verfügbar sind. Sie können Sammlungen auch verwenden, um Saisonartikel oder beliebige andere organisatorische Parameter, die für Ihr Geschäft relevant sind, zu organisieren.

Die für jedes Kriterium innerhalb der Empfehlung erzeugte [Reserveempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md) verwendet ebenfalls die Sammlung, sodass nur Artikel aus der Sammlung in die Reserveempfehlung aufgenommen werden. Mit Sammlungen können Sie sicherstellen, dass nur Produkte an einem Ort angezeigt werden, für die dies Sinn macht.

Sammlungen werden stets neu erstellt oder aktualisiert, wenn die einzelnen Kriterien ausgeführt werden.

Sie können Ihre Artikel in Katalogen gruppieren und dann separate Empfehlungen für jede Sammlung erstellen.

Inklusionskriterien ermöglichen Ihnen etwas Ähnliches wie eine Sammlung, sie müssen jedoch jedes Mal eingerichtet werden, wenn Sie eine Aktivität erstellen. Sammlungen ermöglichen Ihnen, einen Satz von Artikeln auf einmal zu erstellen und diesen dann zu jeder passenden Gelegenheit zu verwenden, ohne dass Sie diesen erneut einrichten müssen.

Beim Erstellen oder Bearbeiten einer [!DNL Recommendations] Aktivität wird der Sammlungsname neben der [!UICONTROL Criteria] im Aktivitätsdiagramm angezeigt.

>[!NOTE]
>
>Sammlungen werden bei Verwendung des [!UICONTROL Recently Viewed Items] Empfehlungsschlüssels nicht angewendet.

## Sammlung erstellen {#task_1256DFF6842141FCAADD9E1428EF7F08}

Erstellen Sie eine Sammlung, um die Produkte oder Inhalte zu organisieren, die Sie in Ihren Empfehlungen anzeigen möchten.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** , um die Liste der vorhandenen Sammlungen anzuzeigen.

   ![Sammlungsliste](assets/collections_list.png)

   Auf der Seite [!UICONTROL Collections] wird eine Liste Ihrer vorhandenen Sammlungen angezeigt. Durch Klicken auf die Schaltfläche [!UICONTROL Create Collection] erstellen Sie neue Sammlungen. Sie können auch vorhandene Sammlungen bearbeiten, kopieren und löschen, indem Sie den Mauszeiger über die gewünschte Sammlung bewegen und auf das gewünschte Symbol klicken.

   ![Mauszeiger-Symbole: Bearbeiten, Kopieren und Löschen](/help/main/c-recommendations/c-products/assets/hover-icons.png)

   Die für jede Sammlung in der [!UICONTROL Collections] Listenansicht gemeldete „Anzahl der Elemente“ ist die Anzahl der Produkte, die den Regeln für diese Sammlung in der konfigurierten standardmäßigen Recommendations-[ (Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) entsprechen. Siehe [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=de){target=_blank} zum Ändern der Standardhostgruppe.

1. Klicken Sie auf **[!UICONTROL Create Collection]**.

1. (Bedingt) Wählen Sie beim Erstellen (oder Aktualisieren) einer Sammlung eine Umgebung aus dem **[!UICONTROL Environment]** Filter aus, um die Inhalte der Sammlung in dieser Umgebung in der Vorschau anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Sammlung erstellen](/help/main/c-recommendations/c-products/assets/CreateCollection.png)

1. Geben Sie einen **[!UICONTROL Name]** für die Sammlung ein.

   Sie können auch eine optionale **[!UICONTROL Description]** eingeben.

1. Legen Sie die Regeln fest, die für den Aufbau der Sammlung verwendet werden.

   Ihre Sammlung kann beispielsweise auf einer Produkt-ID oder Kategorie, Marge oder einem anderen Parameter in der Liste basieren.

   Sie können Regeln hinzufügen, um eine Sammlung durch mehrere Parameter zu definieren. Mehrere Regeln werden mit einem AND-Operator verbunden. Alle angegebenen Regeln müssen eingehalten werden, damit die Sammlung angewendet wird.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Erstellen einer Sammlung mit der erweiterten Suche

Sie können Sammlungen auch mithilfe der erweiterten Suche auf der Seite [Katalogsuche](/help/main/c-recommendations/c-products/catalog-search.md#save-as) erstellen ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Dialogfeld „Speichern unter“](/help/main/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie eine Suche beispielsweise mit „ID > ENTHÄLT“ erstellt haben, können Sie auf [!UICONTROL Save As] > [!UICONTROL Collection] klicken.

>[!IMPORTANT]
>
>Bei der Funktion „Erweiterte Suche“ wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die zum Zeitpunkt der Auslieferung zurückgegebenen Produkte basieren jedoch auf der Suche mit Unterscheidung zwischen Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Kollektionen auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt.

## Bearbeiten, Kopieren oder Löschen einer Sammlung

Bewegen Sie den Mauszeiger über die gewünschte Sammlung in der Liste und klicken Sie dann auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Mauszeiger-Symbole für eine Sammlung](/help/main/c-recommendations/c-products/assets/hover-collections.png)

Sie können eine vorhandene Sammlung kopieren, um eine doppelte Sammlung zu erstellen, die Sie dann ändern können. Auf diese Weise können Sie mit weniger Aufwand einen ähnlichen Ausschluss erstellen.

Beachten Sie, dass Sammlungen im gesamten Konto verfügbar sind. Berücksichtigen Sie dies, bevor Sie eine Sammlung löschen. Gelöschte Sammlungen können nicht wiederhergestellt werden.

## Verwenden einer Sammlung in einer Recommendations -Aktivität

1. Erstellen Sie eine Sammlung mit einer der oben genannten Methoden.

1. Klicken Sie auf **[!UICONTROL Activities]** und [Erstellen einer neuen Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md)Aktivität oder bearbeiten Sie eine vorhandene Aktivität.

1. Nachdem Sie ein Kriterium und einen Entwurf ausgewählt haben, wird die [!UICONTROL Options] angezeigt, auf der Sie die gewünschte Sammlung auswählen.

   ![Sammlungsoption auswählen](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Bedingt) Um eine vorhandene Sammlungseinstellung zu ändern, klicken Sie auf der **[!UICONTROL Experiences]** Seite (Schritt 2 des dreiteiligen geleiteten Workflows) auf eine Stelle, an der Sie Empfehlungen platziert haben, klicken Sie auf **[!UICONTROL Change Collection]** und wählen Sie dann die gewünschte Sammlung aus.

   ![Option „Sammlung ändern“](/help/main/c-recommendations/c-products/assets/change-collection.png)

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)
