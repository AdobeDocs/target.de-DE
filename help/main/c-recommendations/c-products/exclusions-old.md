---
keywords: Ausnahmen
description: Erfahren Sie, wie Sie in Adobe- [!DNL Target]  Ausschlüsse erstellen, um zu verhindern, dass Produkte oder Inhalte für Besuchende empfohlen werden.
title: Wie verwende ich Ausschlüsse in Recommendations-Aktivitäten?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 29%

---

# Ausnahmen

Erstellen Sie einen Ausschluss in [!DNL Adobe Target Recommendations] , um zu verhindern, dass Produkte oder Inhalte für Besuchende empfohlen werden. Ein Ausschluss ist eine Untergruppe von Produkten oder Inhalten, die Besuchern nicht empfohlen werden sollten.

Ausschlüsse sind für das gesamte Konto verfügbar. Im Gegensatz zu Sammlungen, bei denen Sie beim Erstellen einer [!UICONTROL Recommendations] Aktivität für jedes Erlebnis eine bestimmte Sammlung angeben, gelten Ausschlüsse für alle Aktivitäten im gesamten Konto. Es gibt keine Möglichkeit, während der Erstellung einer Aktivität eine Ausschlussgruppe zuzuweisen.

Beispiele für Fälle, in denen Sie Ausschlüsse verwenden würden:

* Produkte, die eingestellt wurden
* Der Herbst-/Winter-Katalog ist jetzt der einzige Katalog, der online vorhanden sein sollte. Artikel aus dem Sommerkatalog können nicht mehr gekauft werden.
* Elemente, die auf den meisten Seiten/Bildschirmen nicht empfohlen werden können (für Erwachsene geeignete Produkte, NC-17-Filme usw.)
* Produkte mit unvollständigen Metadatenfeldern (fehlende Miniaturansicht, Preis oder andere wichtige Metadaten)
* Produkte, die nie empfohlen werden sollten (vielleicht gibt es eine SKU im System für etwas, aber es ist kein käuflicher Artikel, oder vielleicht ist es eine falsche SKU für das QA-Team, um einen Kauf zu simulieren, ohne tatsächlich etwas zu bestellen, usw.)

>[!IMPORTANT]
>
>Ausschlussregeln werden global auf alle Umgebungen angewendet.
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarios finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Einen Ausschluss erstellen

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** , um die Liste der vorhandenen Ausschlüsse anzuzeigen.

   ![exclusions_list image](assets/exclusions_list.png)

   Die für jeden Ausschluss in der [!UICONTROL Exclusions] Listenansicht angezeigte „Anzahl der Elemente“ entspricht der Anzahl der Produkte, die den Regeln für diesen Ausschluss in der konfigurierten standardmäßigen Recommendations-[&#x200B; (Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) entsprechen. Siehe [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=de){target=_blank} zum Ändern der Standardhostgruppe.

1. Klicken Sie auf **[!UICONTROL Create Exclusion]**.

1. (Bedingt) Wählen Sie beim Erstellen (oder Aktualisieren) eines Ausschlusses eine Umgebung aus dem **[!UICONTROL Environment]** Filter aus, um die Inhalte des Ausschlusses in dieser Umgebung in der Vorschau anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Ausschluss erstellen](/help/main/c-recommendations/c-products/assets/CreateExclusion.png)

1. Geben Sie einen **[!UICONTROL Name]** ein und geben Sie eine optionale Beschreibung ein.

1. Verwenden Sie den Rule Builder, um Ihre Ausnahmen zu erstellen.

   Wählen Sie aus der Regelliste einen Parameter aus, wählen Sie einen Operator und geben Sie dann einen oder mehrere Werte ein, anhand derer die Produkte identifiziert werden sollen. Trennen Sie mehrere Werte durch Kommas.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Erstellen eines Ausschlusses mit der erweiterten Suche

Sie können Ausschlüsse auch mithilfe von [!UICONTROL Advanced Search] auf der Seite [Katalogsuche](/help/main/c-recommendations/c-products/catalog-search.md#save-as) erstellen ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Dialogfeld „Speichern unter“](/help/main/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie eine Suche beispielsweise mit „ID > ENTHÄLT“ erstellt haben, können Sie auf [!UICONTROL Save As] > [!UICONTROL Exclusion] klicken.

>[!IMPORTANT]
>
>Bei der [!UICONTROL Advanced Search]-Funktion wird nicht zwischen Groß- und Kleinschreibung unterschieden. Bei Produkten, die zum Zeitpunkt des Versands zurückgegeben werden, wird jedoch zwischen Groß- und Kleinschreibung unterschieden. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Ausschlüsse auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Ausschluss mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszuschließen, werden nur Produkte mit dem Zusatz „urlaub“ ausgeschlossen. Produkte, die „Urlaub“ enthalten, werden nicht ausgeschlossen.

## Bearbeiten, Kopieren oder Löschen eines Ausschlusses

Bewegen Sie den Mauszeiger über den gewünschten Ausschluss in der Liste und klicken Sie dann auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Mauszeiger über Symbolen für einen Ausschluss](/help/main/c-recommendations/c-products/assets/hover-exclusions.png)

Sie können einen vorhandenen Ausschluss kopieren, um einen doppelten Ausschluss zu erstellen, den Sie dann ändern können. Auf diese Weise können Sie mit weniger Aufwand einen ähnlichen Ausschluss erstellen.

Beachten Sie, dass Ausschlüsse für das gesamte Konto verfügbar sind. Berücksichtigen Sie dies, bevor Sie einen Ausschluss löschen. Gelöschte Ausschlüsse können nicht wiederhergestellt werden.

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/35308?captions=ger)
