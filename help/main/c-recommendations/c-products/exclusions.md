---
keywords: Ausnahmen
description: Erfahren Sie, wie Sie in Ausschlüsse erstellen, [!DNL Target Recommendations] zu verhindern, dass Produkte oder Inhalte für Besuchende empfohlen werden.
title: Wie verwende ich Ausschlüsse in [!UICONTROL Recommendations]-Aktivitäten?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
TQID: 'https://experienceleague.adobe.com/6-PWkqq5eXAwyLcGGbSqSZmFdJa85yU3x7FPNEt8-2o'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 3883dc9752db0a2427f70cb3036fe060c440361a
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 6%
---
# Ausnahmen {#exclusions}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie Ausschlüsse in erstellen und verwalten können, [!DNL Adobe Target Recommendations] zu verhindern, dass Produkte oder Inhalte Besuchern empfohlen werden.

>[!ENDSHADEBOX]

Ein Ausschluss ist eine Untergruppe von Produkten oder Inhalten, die Besuchern nicht empfohlen werden sollten. Ausschlüsse sind für das gesamte Konto verfügbar. Im Gegensatz zu Sammlungen, die bei der Erstellung einer [!DNL Recommendations] Aktivität für jedes Erlebnis ausgewählt werden, gelten Ausschlüsse für alle Aktivitäten im gesamten Konto, und bei der Erstellung einer Aktivität kann keine Ausschlussgruppe zugewiesen werden.

Ausschlüsse werden normalerweise für Folgendes verwendet:

* Produkte, die eingestellt wurden.
* Elemente aus einem Katalog, der nicht mehr verfügbar ist. Wenn beispielsweise nur der Herbst- und der Winterkatalog online vorhanden sein sollen, können keine Artikel aus dem Sommerkatalog gekauft werden.
* Elemente, die auf den meisten Seiten oder Bildschirmen nicht empfohlen werden können (Erwachsenenprodukte, NC-17-Filme usw.).
* Produkte mit unvollständigen Metadatenfeldern (fehlende Miniaturansicht, Preis oder andere wichtige Metadaten).
* Produkte, die nie empfohlen werden sollten, z. B. eine SKU, die im System vorhanden ist, aber kein kaufbarer Artikel ist, oder eine gefälschte SKU, die das QA-Team verwendet, um einen Kauf zu simulieren, ohne etwas zu bestellen.

>[!IMPORTANT]
>
>Ausschlussregeln werden global auf alle ([) &#x200B;](/help/main/administrating-target/environments.md).
>
>Detaillierte Informationen, Beispiele und Anwendungsfallszenarien zu statischen und dynamischen Ausschlussregeln finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#inclusion-rules).

## Einen Ausschluss erstellen

Ausschlussregeln werden einmal definiert und gelten dann für jede [!DNL Recommendations] im Konto.

1. Klicken Sie **[!UICONTROL Recommendations]** > **[!UICONTROL Ausschlüsse]**, um die Liste der vorhandenen Ausschlüsse anzuzeigen.

   >[!NOTE]
   >
   >Die „Anzahl der Elemente“, die für jeden Ausschluss in der Listenansicht **[!UICONTROL Ausschlüsse]** gemeldet wird, ist die Anzahl der Produkte, die den Regeln für diesen Ausschluss in der konfigurierten standardmäßigen Recommendations-[&#x200B; (Hostgruppe](/help/main/administrating-target/hosts.md) (Umgebung) entsprechen. Informationen [&#x200B; Ändern der Standard [!DNL Recommendations]](https://experienceleague.adobe.com/de/docs/target-dev/developer/recommendations){target=_blank}Hostgruppe finden Sie im *Adobe Target* Entwicklerhandbuch unter „Planen und Implementieren“.


1. Klicken Sie auf **[!UICONTROL Filter anzeigen]**-Symbol ( ![Filtersymbol anzeigen](/help/main/assets/icons/Filter.svg) ) und wählen Sie dann die gewünschte [Umgebung](/help/main/administrating-target/environments.md) aus der Dropdown-Liste **[!UICONTROL Umgebung]**, um eine Vorschau des Ausschlussinhalts in dieser Umgebung anzuzeigen. Standardmäßig werden Ergebnisse aus der Standardhostgruppe angezeigt.

   ![Seite „Ausschlüsse“, auf der das Bedienfeld „Filter“ geöffnet ist und die Liste „Umgebung“ angezeigt wird](../assets/exclusions_2.png)

1. Klicken Sie **[!UICONTROL Ausschluss erstellen]**.

   ![Ausschlussseite mit der Schaltfläche „Ausschluss erstellen“](../assets/exclusions_1.png)

1. Geben Sie einen Ausschluss (**[!UICONTROL )]**. Sie können auch eine optionale Beschreibung eingeben.

1. Verwenden Sie den Regel-Builder, um den Ausschluss zu definieren.

   Wählen Sie einen Parameter in der Liste **[!UICONTROL Regeln]** aus, wählen Sie einen Benutzer aus und geben Sie dann einen oder mehrere Werte ein, um die Produkte zu identifizieren. Trennen Sie mehrere Werte durch Kommas.

1. Klicken Sie **[!UICONTROL Erstellen]**.

1. Klicken Sie auf das Symbol Mehr Aktionen ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben dem gewünschten Ausschluss in der Liste und dann auf die entsprechende Option: **[!UICONTROL Bearbeiten]**, **[!UICONTROL Kopieren]** oder **[!UICONTROL Löschen]**.

   ![Ausschlussliste mit geöffnetem Menü „Mehr Aktionen“ mit den Optionen Bearbeiten, Kopieren und Löschen](../assets/exclusions_3.png)

<!--
## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded.
-->


## Schulungsvideo: Erstellen von Sammlungen und Ausschlüssen in Recommendations (7:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Eine Sammlung erstellen
* Einen Ausschluss erstellen

>[!VIDEO](https://video.tv.adobe.com/v/27689)
