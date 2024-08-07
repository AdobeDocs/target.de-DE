---
keywords: Ausnahmen
description: Erfahren Sie, wie Sie Ausschlüsse in Adobe [!DNL Target] Recommendations erstellen, um zu verhindern, dass Produkte oder Inhalte Besuchern empfohlen werden.
title: Wie verwende ich Ausschlüsse in Recommendations-Aktivitäten?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 28%

---

# Ausnahmen

Erstellen Sie einen Ausschluss in [!DNL Adobe Target Recommendations] , um zu verhindern, dass Produkte oder Inhalte Besuchern empfohlen werden. Ein Ausschluss ist eine Untergruppe von Produkten oder Inhalten, die Besuchern nicht empfohlen werden sollten.

Ausschlüsse sind für das gesamte Konto verfügbar. Im Gegensatz zu Sammlungen, bei denen Sie bei der Erstellung einer [!UICONTROL Recommendations] -Aktivität eine bestimmte Sammlung für jedes Erlebnis angeben, gelten Ausschlüsse für alle Aktivitäten im gesamten Konto. Es gibt keine Option, während der Erstellung einer Aktivität eine Ausschlussgruppe zuzuweisen.

Beispiele für die Verwendung von Ausschlüssen:

* Eingestellte Produkte
* Der Herbst-/Winterkatalog ist jetzt der einzige Katalog, der online verfügbar sein sollte. Alle Artikel aus dem Sommerkatalog stehen nicht mehr zum Kauf zur Verfügung.
* Artikel, die auf den meisten Seiten/Bildschirmen nicht empfohlen werden können (Produkte für Erwachsene, Filme mit NC-17 usw.)
* Produkte mit unvollständigen Metadatenfeldern (fehlende Miniaturansicht, Preis oder andere wichtige Metadaten)
* Produkte, die nie empfohlen werden sollten (möglicherweise existiert im System eine SKU für etwas, aber es ist kein Artikel, der gekauft werden kann, oder es ist eine falsche SKU für das QA-Team, einen Kauf zu simulieren, ohne tatsächlich etwas zu bestellen usw.)

>[!IMPORTANT]
>
>Ausschlussregeln werden global auf alle Umgebungen angewendet.
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarios finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Einen Ausschluss erstellen

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** , um die Liste der vorhandenen Ausschlüsse anzuzeigen.

   ![exclusions_list image](assets/exclusions_list.png)

   Die &quot;Anzahl der Elemente&quot;, die für jeden Ausschluss in der [!UICONTROL Exclusions] -Listenansicht gemeldet werden, ist die Anzahl der Produkte, die mit den Regeln für diesen Ausschluss innerhalb der konfigurierten standardmäßigen Recommendations [Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) übereinstimmen. Informationen zum Ändern der standardmäßigen Hostgruppe finden Sie unter [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} .

1. Klicken Sie auf **[!UICONTROL Create Exclusion]**.

1. (Bedingt) Wählen Sie eine Umgebung aus dem Filter **[!UICONTROL Environment]** , während Sie einen Ausschluss erstellen (oder aktualisieren), um eine Vorschau des Ausschlusses in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Ausschluss erstellen](/help/main/c-recommendations/c-products/assets/CreateExclusion.png)

1. Geben Sie einen Ausschluss **[!UICONTROL Name]** ein und geben Sie eine optionale Beschreibung ein.

1. Verwenden Sie den Rule Builder, um Ihre Ausnahmen zu erstellen.

   Wählen Sie aus der Regelliste einen Parameter aus, wählen Sie einen Operator und geben Sie dann einen oder mehrere Werte ein, anhand derer die Produkte identifiziert werden sollen. Trennen Sie mehrere Werte durch Kommas.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Erstellen eines Ausschlusses mit der erweiterten Suche

Sie können Ausschlüsse auch mit [!UICONTROL Advanced Search] auf der Seite [Katalogsuche](/help/main/c-recommendations/c-products/catalog-search.md#save-as) ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]) erstellen.

![Als Dialogfeld speichern](/help/main/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie beispielsweise eine Suche mit &quot;id > contains&quot; erstellt haben, können Sie auf [!UICONTROL Save As] > [!UICONTROL Exclusion] klicken.

>[!IMPORTANT]
>
>Bei der Funktion &quot;[!UICONTROL Advanced Search]&quot;wird nicht zwischen Groß- und Kleinschreibung unterschieden. Bei den zum Zeitpunkt des Versands zurückgegebenen Produkten wird jedoch zwischen Groß- und Kleinschreibung unterschieden. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Ausschlüsse auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Ausschluss mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszuschließen, werden nur Produkte mit dem Zusatz „urlaub“ ausgeschlossen. Produkte, die „Urlaub“ enthalten, werden nicht ausgeschlossen.

## Einen Ausschluss bearbeiten, kopieren oder löschen

Bewegen Sie den Mauszeiger über den gewünschten Ausschluss in der Liste und klicken Sie auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Maussymbole für einen Ausschluss](/help/main/c-recommendations/c-products/assets/hover-exclusions.png)

Sie können einen vorhandenen Ausschluss kopieren, um einen doppelten Ausschluss zu erstellen, den Sie dann ändern können. Auf diese Weise können Sie einen ähnlichen Ausschluss mit geringerem Aufwand erstellen.

Beachten Sie, dass Ausschlüsse für das gesamte Konto verfügbar sind. Beachten Sie dies vor dem Löschen eines Ausschlusses. Gelöschte Ausschlüsse können nicht wiederhergestellt werden.

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)
