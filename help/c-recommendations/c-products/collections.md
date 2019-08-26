---
description: Eine Sammlung ist ein Satz von Produkten oder Artikeln, die für die Empfehlung infrage kommen.
keywords: Sammlung; Targeting
seo-description: Eine Sammlung ist eine Gruppe von Produkten oder Artikeln in Adobe Target, die für eine Empfehlung zulässig sind.
seo-title: Sammlungen in Adobe Target
solution: Target
title: Sammlungen
title-outputclass: premium
topic: Premium
uuid: aa1afdcf-e51c-4e44-a229-3c21fc9d0514
badge: premium
translation-type: tm+mt
source-git-commit: fcbeca28354a4c1203933b0e8e26927009da2626

---


# ![PREMIUM](/help/assets/premium.png) Sammlungen {#collections}

Eine Sammlung ist ein Satz von Produkten oder Artikeln, die für die Empfehlung infrage kommen.

Im Allgemeinen ist eine Sammlung ein Satz von ähnlichen oder verwandten Artikeln, wie zum Beispiel eine Sammlung eines einzigen Produkts. Sie können jedoch beliebige Artikel in einer Kategorie gruppieren, wenn dies für Ihr Geschäft sinnvoll ist, wie zum Beispiel Produkte in einer bestimmten Preisspanne bzw. mit einer bestimmten Farbe, oder Artikel, die wahrscheinlich in einer bestimmten geografischen Region interessant sind.

Verwenden Sie Sammlungen, um Ihre Produkte in logischen Behältern zu organisieren. Wenn zum Beispiel einige Artikel in einer Region verfügbar sind, in einer anderen jedoch nicht, sollten Sie eventuell eine Sammlung erstellen, die die Artikel weglässt, die für Besucher in der Region nicht verfügbar sind. Sie können Sammlungen auch verwenden, um Saisonartikel oder beliebige andere organisatorische Parameter, die für Ihr Geschäft relevant sind, zu organisieren.

The [backup recommendations](/help/c-recommendations/c-algorithms/backup-recs.md) generated for each criteria within the recommendation also uses this collection, so only items in the collection are included in the backup recommendation. Mit Sammlungen können Sie sicherstellen, dass nur Produkte an einem Ort angezeigt werden, für die dies Sinn macht.

Sammlungen werden stets neu erstellt oder aktualisiert, wenn die einzelnen Kriterien ausgeführt werden.

Sie können Ihre Artikel in Katalogen gruppieren und dann separate Empfehlungen für jede Sammlung erstellen.

Inklusionskriterien ermöglichen Ihnen etwas Ähnliches wie eine Sammlung, sie müssen jedoch jedes Mal eingerichtet werden, wenn Sie eine Aktivität erstellen. Sammlungen ermöglichen Ihnen, einen Satz von Artikeln auf einmal zu erstellen und diesen dann zu jeder passenden Gelegenheit zu verwenden, ohne dass Sie diesen erneut einrichten müssen.

Wenn Sie eine [!DNL Recommendations]-Aktivität erstellen oder bearbeiten, erscheint der Sammlungsname neben der Bezeichnung [!UICONTROL Kriterien] auf dem Aktivitätendiagramm.

>[!NOTE]
>
>Sammlungen werden nicht angewendet, wenn der Empfehlungsschlüssel [!UICONTROL Zuletzt aufgerufene Artikel] verwendet wird.

## Sammlung erstellen {#task_1256DFF6842141FCAADD9E1428EF7F08}

Erstellen Sie eine Sammlung, um die Produkte zu organisieren, die Sie in Ihren Empfehlungen anzeigen möchten.

1. Klicken **[!UICONTROL Sie auf Empfehlungen]** &gt; **[!UICONTROL Sammlungen]**, um die Liste der vorhandenen Sammlungen anzuzeigen.

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

You can also create collections using Advanced Search on the [Catalog Search](/help/c-recommendations/c-products/catalog-search.md) page ([!UICONTROL Recommendations] &gt; [!UICONTROL Catalog Search] &gt; [!UICONTROL Advanced Search]).

![Speichern unter](/help/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie eine Suche mit "id &gt; contains" erstellt haben, können Sie z. B. auf [!UICONTROL Speichern unter] &gt; [!UICONTROL Sammlung] klicken.

>[!IMPORTANT]
>
>Bei der Funktion „Erweiterte Suche“ wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die zum Zeitpunkt der Auslieferung zurückgegebenen Produkte basieren jedoch auf der Suche mit Unterscheidung zwischen Groß- und Kleinschreibung. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Kollektionen auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Katalog mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszugeben, werden nur Produkte mit dem Zusatz „urlaub“ ausgegeben. Produkte, die „Urlaub“ enthalten, werden nicht angezeigt.

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05)

Dieses Video enthält die folgenden Informationen:

* Erstellen einer Sammlung
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689?captions=ger)