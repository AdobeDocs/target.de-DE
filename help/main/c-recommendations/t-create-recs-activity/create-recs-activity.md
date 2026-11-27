---
keywords: Empfehlungen erstellen; Recommendations-Aktivität; neue Empfehlungen; Recommendations-Übersicht
description: Erfahren Sie, wie Sie mit [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) eine [!DNL Recommendations] erstellen.
title: '[!DNL Recommendations] erstellen'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
TQID: 'https://experienceleague.adobe.com/rb9any1dsbk-E-ELV56A2D6X5f0z0cTziscrajmbYDA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 3%
---
# [!DNL Recommendations] erstellen {#create-recs-activity}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine [!DNL Recommendations] [!DNL Target] Aktivität in **[!UICONTROL Visual Experience Composer]** (VEC) erstellen, indem Sie den Speicherort auswählen, um die Aktivität einzurichten.

>[!ENDSHADEBOX]

Eine [!DNL Recommendations] Aktivität zeigt empfohlene Elemente auf einer Seite an. Durch Erstellen der Aktivität in [!DNL Target] **[!UICONTROL Visual Experience Composer]** (VEC) können die Empfehlungen direkt auf einer [!DNL Target]-aktivierten Seite an der Stelle platziert werden, an der sie den Besuchern angezeigt werden sollen.

## Erstellen Sie die Aktivität und wählen Sie den Standort aus. {#create-activity}

Die Aktivitäts-URL und der Speicherort definieren die Seite und den Bereich der Seite, auf der die Empfehlungen angezeigt werden.

1. Klicken Sie im Menü **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Recommendations]**.

   ![Seite „Alle Aktivitäten“ mit hervorgehobener Option „Aktivität erstellen“ und „Recommendations“ öffnen](../assets/create_reco_1.png)

1. Wählen Sie **[!UICONTROL Visual]** aus, falls erforderlich.

   Um stattdessen den **[!UICONTROL formularbasierten Experience Composer zu verwenden]** wählen Sie **[!UICONTROL Formular]** aus. Weitere Informationen finden Sie unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md). Einen Vergleich der Komponisten, einschließlich des VEC **[!UICONTROL Single Page Application]** finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md). Informationen zu VEC-Problemen finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wählen Sie einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geben Sie die Aktivitäts-URL an und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Die Aktivitäts-URL ist die Seite, auf der die Empfehlungen angezeigt werden. [!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]), sodass `http://www.adobe.com` und `https://www.adobe.com` übereinstimmen.

   Der VEC wird geöffnet und zeigt die Seite an.

1. Klicken Sie auf das Element, in dem die Empfehlungen angezeigt werden sollen, und wählen Sie **[!UICONTROL Inhalt ersetzen]** > **[!UICONTROL Empfehlung]**.

   <!--
   * **[!UICONTROL Replace w/ Recommendations]**: Deletes the current content of the element and replaces it with the recommendations.
   * **[!UICONTROL Insert Recommendations Before]**: Places the recommendations before the element, above or to the left of it, depending on the page construction.
   * **[!UICONTROL Insert Recommendations After]**: Places the recommendations after the element, below or to the right of it, depending on the page construction.

   ![Visual Experience Composer with a selected container and the menu options Replace w/ Recommendations, Insert Recommendations Before, Insert Recommendations After, and Expand Selection](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   Use **[!UICONTROL Expand Selection]** to expand the selection to the parent container, so that it includes the desired page elements.
   -->

   Besucherinnen und Besucher, die sich für die Empfehlung qualifizieren, sehen die empfohlenen Elemente im angegebenen Bereich. Besucherinnen und Besucher, die sich nicht qualifizieren, sehen den Standardinhalt.

   >[!NOTE]
   >
   >**[!UICONTROL Recommendations]** -Aktivitäten unterstützen jeweils nur eine Änderung oder Empfehlung. Um mehrere Recommendations anzuzeigen, erstellen Sie mehrere [!DNL Recommendations] Aktivitäten oder verwenden Sie A/B- oder XT-Tests.

   ![Visual Experience Composer mit einem auf der Seite ausgewählten Bild und der im Menü angezeigten Option „Empfehlung“](../assets/create_reco_2.png)

<!--
1. Select a page type: Cart Page, Category Page, Home Page, Landing Page, Product Page, Search Results Page, Thank You Page, or Other.

   ![Select Page Type dialog box with the list of page types open](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

   The page type determines which criteria are suggested in the next section.
-->

1. Rufen Sie das Menü **[!UICONTROL Eigenschaften anzeigen]** auf und klicken Sie auf **[!UICONTROL Empfehlung auswählen]**.

   ![Bedienfeld „Empfehlung“ von Visual Experience Composer mit der Schaltfläche „Empfehlung auswählen“](../assets/create_reco_3.png)

## Kriterien auswählen {#select-criteria}

Kriterien bestimmen, welche Elemente für jeden Besucher empfohlen werden und wie sie ausgewählt werden.

1. Aktivieren Sie das Kontrollkästchen für ein oder mehrere [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).

   ![Dialogfeld „Kriterien auswählen“ mit Suchfeld, Filtersymbol, Schaltfläche „Kriterien erstellen“ und Kriterienliste mit einem ausgewählten Kriterium](../assets/create_reco_4.png)

   Wenn mehrere Kriterien ausgewählt sind, wird der Traffic gleichmäßig zwischen ihnen aufgeteilt und die Prozentsätze können nicht für jedes Kriterium geändert werden. Wenn beispielsweise zwei Kriterien ausgewählt sind und die Aktivität Standardinhalte für 20 % der Teilnehmer anzeigt, sehen 40 % der Teilnehmer die Empfehlungen der einzelnen Kriterien.

   >[!NOTE]
   >
   >Nicht alle Kriterien werden auf jeder Seite korrekt ausgeführt. Damit aktuelle Element- oder Kategorieempfehlungen kompatibel sind, muss die Seite oder Mbox `entity.id` oder `entity.categoryId` übergeben. Es ist am besten, nur kompatible Kriterien anzuzeigen. Um inkompatible Kriterien für die Aktivität verfügbar zu machen, deaktivieren Sie **[!UICONTROL Kontrollkästchen]** Kompatibel“. Dieses Kontrollkästchen wird je nach der Einstellung **[!UICONTROL Administration]** > **[!UICONTROL Recommendations]** > **[!UICONTROL Inkompatible Kriterien filtern]** möglicherweise nicht angezeigt. Weitere Informationen finden Sie unter [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

1. Optional können Sie Kriterien suchen oder erstellen:

   * Um nach einem vorhandenen Kriterium zu suchen, wenn die Liste lang ist, geben Sie in das Suchfeld ein, bis die gewünschten Kriterien angezeigt werden. Einige Kriterien werden mit [!DNL Recommendations] bereitgestellt, und das Team kann auch benutzerdefinierte Kriterien erstellen.
   * Um neue Kriterien zu erstellen, klicken Sie auf **[!UICONTROL Kriterien erstellen]** und geben Sie dann die Informationen für die neuen Kriterien ein. Siehe [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * Um Kriterien in einer Sequenz zu gruppieren, erstellen Sie eine Kriteriensequenz. Siehe [Erstellen von Kriteriensequenzen](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md).

1. Klicken Sie **[!UICONTROL Weiter]**.

## Design und Promotions auswählen {#select-design}

Ein Design ist eine Vorlage, die das Erscheinungsbild der Recommendations am ausgewählten Speicherort bestimmt, und eine Sammlung bestimmt, welche Elemente angezeigt werden können. Promotions können optional zu den Recommendations hinzugefügt werden.

1. [Entwurf auswählen](/help/main/c-recommendations/c-design-overview/design-overview.md).

   ![Wählen Sie das Dialogfeld „Design“ mit der Schaltfläche „Design erstellen“ und der Liste der Designs mit dem ausgewählten 2 x 4-Design](../assets/create_reco_5.png)

   * Um vorhandene Designs zu verwenden, aktivieren Sie das Kontrollkästchen eines oder mehrerer Designs und klicken Sie dann auf **[!UICONTROL Weiter]**. Bei der Auswahl mehrerer Kriterien kann nur ein Design ausgewählt werden.
   * Um einen benutzerdefinierten Entwurf zu erstellen, klicken Sie **[!UICONTROL Entwurf erstellen]** und geben Sie den Namen und den Code des neuen Entwurfs ein. Klicken Sie **[!UICONTROL Weiter]**, wählen Sie ein Bild aus oder laden Sie es hoch und klicken Sie dann auf **[!UICONTROL Fertig]** > **[!UICONTROL Fertig]**.

   [!DNL Target] umfasst mehrere vorkonfigurierte Designs. Weitere Informationen zu benutzerdefinierten Designs finden Sie unter [Erstellen eines Designs](/help/main/c-recommendations/c-design-overview/create-design.md#create-design) und [Anpassen eines Designs mithilfe von Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#customize-design).

1. Klicken Sie **[!UICONTROL Weiter]**.

1. Wählen Sie auf **[!UICONTROL Seite]** Optionen“ die Sammlung aus.

   Die Sammlung bestimmt, welche Elemente in den Empfehlungen angezeigt werden können. Weitere Informationen, einschließlich der Erstellung einer Sammlung, finden Sie unter [Verwenden einer Sammlung in einer Aktivität](/help/main/c-recommendations/c-products/collections.md#use-collection).

1. (Optional) Fügen Sie den Recommendations Aktionen vorne und hinten hinzu. Siehe [Hinzufügen von Promotions](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#add-promotions).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Der VEC-Bildschirm zeigt den Empfehlungsentwurf auf der Seite an.

## Überprüfen und Abschließen der Aktivität {#complete-activity}

Die Überprüfung der Empfehlungen und des Aktivitätsflusses vor dem Speichern hilft sicherzustellen, dass die richtige Zielgruppe, die richtigen Kriterien und das richtige Design vorhanden sind.

1. (Optional) Klicken Sie auf **[!UICONTROL Vorschau]**, um zu sehen, wie die Aktivität für Besuchende angezeigt wird. Dieser Modus ermöglicht die Interaktion mit den Empfehlungen, da ein Besucher mit ihnen interagieren würde. Klicken Sie **[!UICONTROL Erstellen]**, um zum VEC zurückzukehren.

1. Überprüfen Sie die Empfehlung im VEC und klicken Sie dann auf **[!UICONTROL Weiter]**.

1. Überprüfen Sie die Aktivität im Flussdiagramm, und nehmen Sie die erforderlichen Änderungen vor. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie fertig sind.

   ![Flussdiagramm für Recommendations mit der Aufteilung „Alle Besucher“ in eine Kontrollgruppe von 10 % und eine Gruppe von 90 %, die zur Sammlung „Alle Sammlungen“, zu den ausgewählten Kriterien und zum 2 x 4-Design führt](../assets/create_reco_6.png)

   Das Flussdiagramm zeigt die Zielgruppe für die Aktivität, die Erlebnisse und die Erfolgsmetriken. Aus dem Diagramm können die folgenden Änderungen vorgenommen werden:

   * **Zielgruppe**: Alle Besucher sehen die Empfehlungen standardmäßig, es kann jedoch stattdessen eine vorhandene Zielgruppe ausgewählt werden. Als Alternative zur Erstellung einer neuen Zielgruppe kann eine [Zielgruppe nur für Aktivitäten](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) erstellt werden oder [es können mehrere Zielgruppen kombiniert werden](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) um eine Ad-hoc-Zielgruppe zu erstellen.
   * **Kriterien**: Zeigen Sie die Kriterien an oder ändern Sie die Sammlung (neben der Beschriftung **[!UICONTROL Kriterien]**).
   * **Kontrollgruppe**: Ändern Sie den Prozentsatz der Eintritte, die das Kontrollerlebnis sehen. Bei einer [!DNL Recommendations] Aktivität wird die Seite der Kontrollgruppe ohne Empfehlungen angezeigt.
   * **Design**: Anzeigen des Design-Codes oder Ändern oder Entfernen des Designs.

1. Geben Sie die Aktivitätseinstellungen an, z. B. einen Namen (erforderlich) und ein Ziel (optional). Die Einstellungen, einschließlich der Regeln für den Aktivitätsnamen, finden Sie unter [Recommendations-Aktivitätseinstellungen](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#recs-activity-settings).

1. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

## Verwalten der Aktivität {#manage-activity}

Nachdem die Aktivität gespeichert wurde, wird auf der **[!UICONTROL Übersicht]** eine Zusammenfassung der Aktivität angezeigt. Auf dieser Seite sind die folgenden Aktionen verfügbar:

* Aktivieren, Bearbeiten oder QS der Aktivität.
* Geben Sie die Aktivität für den Experience Cloud-Feed frei.
* Erlebnis-URLs anzeigen und Daten herunterladen.
* den Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird.
* Ein- oder Ausblenden der Kriteriendetails und Anzeigen des Codes für die Designs.

In der Aktivität sind zwei zusätzliche Seiten verfügbar:

* **[!UICONTROL Berichte]**: Zeigt den Bericht über die Leistung der [!DNL Recommendations] Aktivität.
* **[!UICONTROL Kollisionen]**: Zeigt alle [Aktivitätskollisionen](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) an, die auftreten können. Kollisionen treten auf, wenn mehrere Aktivitäten Inhalte für dieselbe Seite bereitstellen, was dazu führen kann, dass unerwarteter Inhalt angezeigt wird.

## Schulungsvideo: Erstellen einer Recommendations-Aktivität (7:15) ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
