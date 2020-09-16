---
keywords: exclusions
description: Erstellen Sie einen Ausschluss, [!DNL Adobe Target Recommendations] um zu verhindern, dass Produkte oder Inhalte für Besucher empfohlen werden.
title: Ausschlüsse in Adobe Target
feature: entities
uuid: 1970846e-37d8-4b69-a0d9-ff45bb840bef
translation-type: tm+mt
source-git-commit: af46453734f4ce185e0cd4282793a800fada8a98
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 55%

---


# Ausnahmen{#exclusions}

Erstellen Sie einen Ausschluss in, [!DNL Adobe Target Recommendations] um zu verhindern, dass Produkte oder Inhalte für Besucher empfohlen werden.

Ein Ausschluss ist eine Untergruppe von Produkten oder Inhalten, die den Besuchern nicht empfohlen werden sollten. Beispielsweise können Sie Ausschlüsse verwenden, um zu verhindern, dass Produkte oder Inhalte in Empfehlungen angezeigt werden, die eingestellt wurden oder sensibel sind (z. B. Filme mit einer Bewertung, die aufgrund von Inhaltsbewertungen nicht für alle geeignet ist).

Ausnahmen sind für das gesamte Konto verfügbar.

>[!IMPORTANT]
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarios finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Einen Ausschluss erstellen

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Ausschlüsse]**, um die Liste vorhandener Ausschlüsse anzuzeigen. 

   ![](assets/exclusions_list.png)

   Die „Anzahl der Elemente“, die für jeden Ausschluss in der [!UICONTROL Ausschluss]-Listenansicht gemeldet werden, entspricht der Anzahl der Produkte, die mit den Regeln für diesen Ausschluss in der konfigurierten Standard-Umgebungs-[Hostgruppe](/help/administrating-target/hosts.md) (Umgebung) übereinstimmen. Siehe [Einstellungen](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) zum Ändern der Standardhostgruppe.

1. Klicken Sie auf **[!UICONTROL Ausschluss erstellen]**.

1. (Bedingt) Wählen Sie eine Umgebung aus dem **[!UICONTROL Umgebungsfilter]**, während Sie einen Ausschluss erstellen (oder aktualisieren), um eine Vorschau des Ausschlusses in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Ausschluss erstellen](/help/c-recommendations/c-products/assets/CreateExclusion.png)

1. Geben Sie einen **[!UICONTROL Namen]** für den Ausschluss ein und geben Sie eine optionale Beschreibung ein.

1. Verwenden Sie den Rule Builder, um Ihre Ausnahmen zu erstellen.

   Wählen Sie aus der Regelliste einen Parameter aus, wählen Sie einen Operator und geben Sie dann einen oder mehrere Werte ein, anhand derer die Produkte identifiziert werden sollen. Trennen Sie mehrere Werte durch Kommas.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Erstellen eines Ausschlusses mit der erweiterten Suche

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Speichern unter, Dialogfeld](/help/c-recommendations/c-products/assets/save-as.png)

Nachdem Sie beispielsweise eine Suche mit „id“ > „contains“ erstellt haben, können Sie auf [!UICONTROL „Speichern unter“] > [!UICONTROL „Ausschluss“] klicken.

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. Diese Diskrepanz kann zu Verwirrung führen. Achten Sie darauf, die Groß- und Kleinschreibung zu berücksichtigen, wenn Sie Ausschlüsse auf der Grundlage von Ergebnissen mithilfe der erweiterten Suche erstellen. Wenn Sie z. B. nach „Urlaub“ suchen, werden bei der ersten Suche die Ergebnisse mit „Urlaub“ und „urlaub“ aufgelistet. Wenn Sie dann einen Ausschluss mit der Absicht erstellen, Produkte mit dem Zusatz „urlaub“ auszuschließen, werden nur Produkte mit dem Zusatz „urlaub“ ausgeschlossen. Produkte, die „Urlaub“ enthalten, werden nicht ausgeschlossen.

## Bearbeiten, Kopieren oder Löschen eines Ausschlusses

Bewegen Sie den Mauszeiger über den gewünschten Ausschluss in der Liste und klicken Sie dann auf das entsprechende Symbol: bearbeiten, kopieren oder löschen.

![Mauszeiger-Symbole für einen Ausschluss](/help/c-recommendations/c-products/assets/hover-exclusions.png)

Sie können einen vorhandenen Ausschluss kopieren, um einen Duplikat-Ausschluss zu erstellen, den Sie dann ändern können. Auf diese Weise können Sie einen ähnlichen Ausschluss mit geringerem Aufwand erstellen.

Beachten Sie, dass Ausschlüsse für das gesamte Konto verfügbar sind. Achten Sie darauf, dies zu berücksichtigen, bevor Sie einen Ausschluss löschen. Gelöschte Ausnahmen können nicht wiederhergestellt werden.

## Training video: Create collections and exclusions in Recommendations (7:05) ![Tutorial badge](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)