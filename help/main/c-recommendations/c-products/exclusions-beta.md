---
keywords: Ausnahmen
description: Erfahren Sie, wie Sie in Ausschlüsse erstellen [!DNL Target Recommendations]  um zu verhindern, dass Produkte oder Inhalte für Besucher empfohlen werden.
title: Wie verwende ich Ausschlüsse in [!UICONTROL Recommendations] Aktivitäten?
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: fb3c63b4-08be-4dac-b5a1-c6c1ecd4c4b3
source-git-commit: 22b0ba18efb736b291f9b7951acd9f706beedbe1
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 18%

---

# Ausnahmen

Erstellen Sie einen Ausschluss in [!DNL Adobe Target Recommendations] , um zu verhindern, dass Produkte oder Inhalte für Besuchende empfohlen werden. Ein Ausschluss ist eine Untergruppe von Produkten oder Inhalten, die Besuchern nicht empfohlen werden sollten.

Ausschlüsse sind für das gesamte Konto verfügbar. Im Gegensatz zu Sammlungen, bei denen Sie beim Erstellen einer [!UICONTROL Recommendations] Aktivität für jedes Erlebnis eine bestimmte Sammlung angeben, gelten Ausschlüsse für alle Aktivitäten im gesamten Konto. Es gibt keine Möglichkeit, während der Erstellung einer Aktivität eine Ausschlussgruppe zuzuweisen.

Beispiele für Fälle, in denen Sie Ausschlüsse verwenden würden:

* Produkte, die eingestellt wurden.
* Der Herbst- und Winterkatalog ist jetzt der einzige Katalog, der online vorhanden sein sollte. Artikel aus dem Sommerkatalog können nicht mehr gekauft werden.
* Elemente, die auf den meisten Seiten oder Bildschirmen nicht empfohlen werden können (Erwachsenenprodukte, NC-17-Filme usw.).
* Produkte mit unvollständigen Metadatenfeldern (fehlende Miniaturansicht, Preis oder andere wichtige Metadaten).
* Produkte, die nie empfohlen werden sollten (vielleicht gibt es im System eine SKU für etwas, aber es ist kein käuflicher Artikel. Oder es ist eine falsche SKU für das QA-Team, um einen Kauf zu simulieren, ohne tatsächlich etwas zu bestellen (usw.).

>[!IMPORTANT]
>
>Ausschlussregeln werden global auf alle ([) ](/help/main/administrating-target/environments.md).
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarios finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Einen Ausschluss erstellen

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** , um die Liste der vorhandenen Ausschlüsse anzuzeigen.

   ![exclusions_list image](assets/exclusions-list.png)

   Die für jeden Ausschluss in der [!UICONTROL Exclusions] Listenansicht gemeldete „Anzahl der Elemente“ ist die Anzahl der Produkte, die den Regeln für diesen Ausschluss in der konfigurierten standardmäßigen Recommendations-[ (Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) entsprechen. Informationen [ Ändern der Standard [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank}Hostgruppe finden Sie im *Adobe Target* Entwicklerhandbuch unter „Planen und Implementieren“.

1. (Bedingt) Klicken Sie auf das Symbol [!UICONTROL Filter] und wählen Sie dann aus der Dropdown-Liste **[!UICONTROL Environment]** die gewünschte [Umgebung](/help/main/administrating-target/environments.md) aus, während Sie einen Ausschluss erstellen (oder aktualisieren), um eine Vorschau des Inhalts des Ausschlusses in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Ausschluss erstellen](/help/main/c-recommendations/c-products/assets/choose-environment.png)

1. Klicken Sie auf **[!UICONTROL Create Exclusion]**.

   ![Dialogfeld „Ausschluss erstellen“](/help/main/c-recommendations/c-products/assets/create-exclusion.png)

1. Geben Sie einen **[!UICONTROL Name]** ein und geben Sie eine optionale Beschreibung ein.

1. Verwenden Sie den Rule Builder, um Ihre Ausnahmen zu erstellen.

   Wählen Sie aus der Regelliste einen Parameter aus, wählen Sie einen Operator und geben Sie dann einen oder mehrere Werte ein, anhand derer die Produkte identifiziert werden sollen. Trennen Sie mehrere Werte durch Kommas.

1. Klicken Sie auf **[!UICONTROL Create]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

## Bearbeiten, Kopieren oder Löschen eines Ausschlusses

Klicken Sie auf **Auslassungssymbol** neben dem gewünschten Ausschluss in der Liste und dann auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

![Optionen: Bearbeiten, Kopieren und Löschen](/help/main/c-recommendations/c-products/assets/edit-copy-delete.png)

Sie können einen vorhandenen Ausschluss kopieren, um einen doppelten Ausschluss zu erstellen, den Sie dann ändern können. Mit dieser Option können Sie mit weniger Aufwand einen ähnlichen Ausschluss erstellen.

Beachten Sie, dass Ausschlüsse für das gesamte Konto verfügbar sind. Beachten Sie diesen Vorbehalt, bevor Sie einen Ausschluss löschen. Gelöschte Ausschlüsse können nicht wiederhergestellt werden.

## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)
