---
keywords: collection;Targeting
description: Eine Sammlung ist ein Satz von Produkten oder Artikeln in Adobe Target, die für die Empfehlung infrage kommen.
title: Sammlungen in Adobe Target
feature: entities
uuid: aa1afdcf-e51c-4e44-a229-3c21fc9d0514
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 99%

---


# ![PREMIUM](/help/assets/premium.png) Sammlungen {#collections}

Eine Sammlung ist ein Satz von Produkten oder Artikeln, die für die Empfehlung infrage kommen.

Im Allgemeinen ist eine Sammlung ein Satz von ähnlichen oder verwandten Artikeln, wie zum Beispiel eine Sammlung eines einzigen Produkts. Sie können jedoch beliebige Artikel in einer Kategorie gruppieren, wenn dies für Ihr Geschäft sinnvoll ist, wie zum Beispiel Produkte in einer bestimmten Preisspanne bzw. mit einer bestimmten Farbe, oder Artikel, die wahrscheinlich in einer bestimmten geografischen Region interessant sind.

Verwenden Sie Sammlungen, um Ihre Produkte in logischen Behältern zu organisieren. Wenn zum Beispiel einige Artikel in einer Region verfügbar sind, in einer anderen jedoch nicht, sollten Sie eventuell eine Sammlung erstellen, die die Artikel weglässt, die für Besucher in der Region nicht verfügbar sind. Sie können Sammlungen auch verwenden, um Saisonartikel oder beliebige andere organisatorische Parameter, die für Ihr Geschäft relevant sind, zu organisieren.

Die für jedes Kriterium innerhalb der Empfehlung erzeugte [Reserveempfehlung](/help/c-recommendations/c-algorithms/backup-recs.md) verwendet ebenfalls die Sammlung, sodass nur Artikel aus der Sammlung in die Reserveempfehlung aufgenommen werden. Mit Sammlungen können Sie sicherstellen, dass nur Produkte an einem Ort angezeigt werden, für die dies Sinn macht.

Sammlungen werden stets neu erstellt oder aktualisiert, wenn die einzelnen Kriterien ausgeführt werden.

Sie können Ihre Artikel in Katalogen gruppieren und dann separate Empfehlungen für jede Sammlung erstellen.

Inklusionskriterien ermöglichen Ihnen etwas Ähnliches wie eine Sammlung, sie müssen jedoch jedes Mal eingerichtet werden, wenn Sie eine Aktivität erstellen. Sammlungen ermöglichen Ihnen, einen Satz von Artikeln auf einmal zu erstellen und diesen dann zu jeder passenden Gelegenheit zu verwenden, ohne dass Sie diesen erneut einrichten müssen.

Wenn Sie eine [!DNL Recommendations]-Aktivität erstellen oder bearbeiten, erscheint der Sammlungsname neben der Bezeichnung [!UICONTROL Kriterien] auf dem Aktivitätendiagramm.

>[!NOTE]
>
>Sammlungen werden nicht angewendet, wenn der Empfehlungsschlüssel [!UICONTROL Zuletzt aufgerufene Artikel] verwendet wird.

## Sammlung erstellen {#task_1256DFF6842141FCAADD9E1428EF7F08}

Erstellen Sie eine Sammlung, um die Produkte zu organisieren, die Sie in Ihren Empfehlungen anzeigen möchten.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Sammlungen]**, um die Liste vorhandener Sammlungen anzuzeigen.

   ![Sammlungsliste](assets/collections_list.png)

   Die für jede Sammlung in der [!UICONTROL Sammlungslistenansicht] gemeldete „Anzahl an Elementen“ ist die Anzahl der Produkte, die mit den Regeln für diese Sammlung in der konfigurierten Standard-Umgebungs-[Hostgruppe](/help/administrating-target/hosts.md) (Umgebung) übereinstimmen. Siehe [Einstellungen](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) zum Ändern der Standardhostgruppe.

1. Klicken Sie auf **[!UICONTROL Sammlung erstellen]**.

1. (Bedingt) Wählen Sie eine Umgebung aus dem **[!UICONTROL Umgebungs-]** Filter, während Sie eine Sammlung erstellen (oder aktualisieren), um eine Vorschau der Inhalte der Sammlung in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Sammlung erstellen](/help/c-recommendations/c-products/assets/CreateCollection.png)

1. Geben Sie einen **[!UICONTROL Namen]** für die Sammlung ein.

   Sie können je nach Wunsch auch eine **[!UICONTROL Beschreibung eingeben]**.

1. Legen Sie die Regeln fest, die für den Aufbau der Sammlung verwendet werden.

   Ihre Sammlung kann beispielsweise auf einer Produkt-ID oder Kategorie, Marge oder einem anderen Parameter in der Liste basieren.

   Sie können Regeln hinzufügen, um eine Sammlung durch mehrere Parameter zu definieren. Mehrere Regeln werden mit UND verknüpft. Alle angegebenen Regeln müssen eingehalten werden, damit die Sammlung angewendet wird.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Erstellen einer Sammlung mit der erweiterten Suche

Sie können Sammlungen auch über „Erweiterte Suche“ auf der Seite [Katalogsuche](/help/c-recommendations/c-products/catalog-search.md) erstellen ([!UICONTROL Empfehlungen] > [!UICONTROL Katalogsuche] > [!UICONTROL Erweiterte Suche]).

![Speichern unter, Dialogfeld](/help/c-recommendations/c-products/assets/save-as-dialog.png)

Nachdem Sie eine Suche mit &quot;id > contains&quot; erstellt haben, können Sie z. B. auf [!UICONTROL Speichern unter] > [!UICONTROL Sammlung] klicken.

>[!IMPORTANT]
>
>Bei der Funktion „Erweiterte Suche“ wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die zum Zeitpunkt der Auslieferung zurückgegebenen Produkte basieren jedoch auf der Suche mit Unterscheidung zwischen Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Kollektionen auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt.

## Schulungsvideo: Sammlungen und Ausschlüsse in Recommendations erstellen (07:05) ![Tutorial badge](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)