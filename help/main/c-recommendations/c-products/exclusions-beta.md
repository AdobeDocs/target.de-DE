---
keywords: Ausnahmen
description: Erfahren Sie, wie Sie Ausschlüsse in erstellen. [!DNL Target Recommendations] um zu verhindern, dass Besucher Produkte oder Inhalte empfehlen.
title: Wie verwende ich Ausnahmen in [!UICONTROL Recommendations] Aktivitäten?
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6eaf89ef71ea3448584dcdadc926c45dba77504
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 26%

---

# Ausnahmen

Erstellen eines Ausschlusses in [!DNL Adobe Target Recommendations] um zu verhindern, dass Besucher Produkte oder Inhalte empfehlen. Ein Ausschluss ist eine Untergruppe von Produkten oder Inhalten, die Besuchern nicht empfohlen werden sollten.

Ausschlüsse sind für das gesamte Konto verfügbar. Im Gegensatz zu Sammlungen, bei denen Sie bei der Erstellung eines [!UICONTROL Recommendations] -Aktivität, gelten Ausschlüsse für alle Aktivitäten im gesamten Konto. Es gibt keine Option, während der Erstellung einer Aktivität eine Ausschlussgruppe zuzuweisen.

Beispiele für die Verwendung von Ausschlüssen:

* Produkte, die eingestellt wurden.
* Der Herbst- und Winterkatalog ist jetzt der einzige Katalog, der online verfügbar sein sollte. Alle Artikel aus dem Sommerkatalog stehen nicht mehr zum Kauf zur Verfügung.
* Artikel, die auf den meisten Seiten oder Bildschirmen nicht empfohlen werden können (Produkte für Erwachsene, Filme mit NC-17 usw.).
* Produkte mit unvollständigen Metadatenfeldern (fehlende Miniaturansicht, Preis oder andere wichtige Metadaten).
* Produkte, die nie empfohlen werden sollten (möglicherweise existiert im System eine SKU für etwas, aber es ist kein Artikel, der gekauft werden kann. Oder vielleicht ist es eine falsche SKU für das QA-Team, einen Kauf zu simulieren, ohne tatsächlich etwas zu bestellen usw.).

>[!IMPORTANT]
>
>Ausschlussregeln werden global auf alle angewendet [Umgebungen](/help/main/administrating-target/environments.md).
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarios finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Einen Ausschluss erstellen

1. Klicks **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** , um die Liste der vorhandenen Ausschlüsse anzuzeigen.

   ![exclusions_list-Bild](assets/exclusions-list.png)

   Die &quot;Anzahl Elemente&quot;, die für jeden Ausschluss auf der [!UICONTROL Exclusions] Die Listenansicht ist die Anzahl der Produkte, die mit den Regeln für diesen Ausschluss innerhalb der konfigurierten standardmäßigen Recommendations übereinstimmen. [Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung). Siehe [Planung und Umsetzung [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank} im *Adobe Target-Entwicklerhandbuch* für Informationen zum Ändern der Standard-Hostgruppe.

1. (Bedingt) Klicken Sie auf die [!UICONTROL Filter] und wählen Sie dann das gewünschte [Umgebung](/help/main/administrating-target/environments.md) aus dem **[!UICONTROL Environment]** Dropdown-Liste beim Erstellen (oder Aktualisieren) eines Ausschlusses, um eine Vorschau des Ausschlussinhalts in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Ausschluss erstellen](/help/main/c-recommendations/c-products/assets/choose-environment.png)

1. Klicken Sie auf **[!UICONTROL Create Exclusion]**.

   ![Dialogfeld &quot;Ausschluss erstellen&quot;](/help/main/c-recommendations/c-products/assets/create-exclusion.png)

1. Einen Ausschluss eingeben **[!UICONTROL Name]** und geben Sie eine optionale Beschreibung ein.

1. Verwenden Sie den Rule Builder, um Ihre Ausnahmen zu erstellen.

   Wählen Sie aus der Regelliste einen Parameter aus, wählen Sie einen Operator und geben Sie dann einen oder mehrere Werte ein, anhand derer die Produkte identifiziert werden sollen. Trennen Sie mehrere Werte durch Kommas.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Erstellen eines Ausschlusses mit der erweiterten Suche

Sie können Ausschlüsse auch mithilfe von [!UICONTROL Advanced Search] auf [Katalogsuche](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Dialogfeld &quot;Speichern unter&quot;](/help/main/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie beispielsweise eine Suche mit &quot;id > contains&quot; erstellt haben, können Sie auf [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>Die [!UICONTROL Advanced Search] -Funktion unterscheidet nicht zwischen Groß- und Kleinschreibung. Die zum Zeitpunkt des Versands zurückgegebenen Produkte basieren jedoch auf der Suche, bei der zwischen Groß- und Kleinschreibung unterschieden wird. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Ausschlüsse auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Ausschluss mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszuschließen, werden nur Produkte mit dem Zusatz „urlaub“ ausgeschlossen. Produkte, die „Urlaub“ enthalten, werden nicht ausgeschlossen.

## Einen Ausschluss bearbeiten, kopieren oder löschen

Klicken Sie auf **Ellipse** neben dem gewünschten Ausschluss in der Liste und klicken Sie dann auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Optionen: Bearbeiten, Kopieren und Löschen](/help/main/c-recommendations/c-products/assets/edit-copy-delete.png)

Sie können einen vorhandenen Ausschluss kopieren, um einen doppelten Ausschluss zu erstellen, den Sie dann ändern können. Mit dieser Option können Sie einen ähnlichen Ausschluss mit geringerem Aufwand erstellen.

Beachten Sie, dass Ausschlüsse für das gesamte Konto verfügbar sind. Beachten Sie diese Einschränkung, bevor Sie einen Ausschluss löschen. Gelöschte Ausschlüsse können nicht wiederhergestellt werden.

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)