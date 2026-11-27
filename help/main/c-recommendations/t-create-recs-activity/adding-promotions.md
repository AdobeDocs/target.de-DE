---
keywords: Promotions;vordere Promotions;hintere Promotions;Promotions-Typ;Liste der Elemente;Nach Attribut bewerben;Sammlung bewerben
description: Erfahren Sie, wie Sie hochgestufte Elemente hinzufügen und deren Platzierung in Ihren Adobe [!DNL Target] Recommendations-Designs steuern. Sie können statische und dynamische Promotions hinzufügen.
title: Wie füge ich Promotions in Recommendations-Designs hinzu?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
TQID: 'https://experienceleague.adobe.com/tAfKOzwjnUJgypDh-4LdVukNlTVwMS4UkvcNmCaCV0E'
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
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 3%
---
# Hinzufügen von Promotions {#add-promotions}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie einem [!DNL Recommendations]-Design hochgestufte Elemente hinzufügen und wie deren Sortierreihenfolge bestimmt wird.

>[!ENDSHADEBOX]

Bei Promotions werden zusätzlich zu den durch die Kriterien empfohlenen Elementen bestimmte Elemente in einem [!DNL Recommendations] Design platziert. Sie nutzen verfügbare Slots im Design und haben Vorrang vor Kriterienergebnissen und Backup-Empfehlungen. Wenn beispielsweise ein Design sechs Slots hat und zwei davon für Promotions verwendet werden, bleiben vier Slots für Artikel übrig, die auf der Grundlage von Kriterien empfohlen werden.

Promotions werden anhand der von den Kriterien für die Aktivität empfohlenen Elemente dedupliziert, sodass ein bestimmtes Element nicht zweimal in einem einzigen Recommendations-Tray angezeigt wird.

![Ändern des Promotion-Dialogfelds mit deaktivierten Umschaltern „Vordere Promotion“ und „Hintere Promotion“](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Durch die Verwendung von Promotions wird die CSV-Struktur und -Ausgabe geändert. Diese Änderungen können sich auf jeden externen Prozess auswirken, der CSV umfasst, z. B. E-Mail.

## Hinzufügen einer Promotion {#add-promotion}

Eine Promotion definiert, welche Elemente beworben werden, wie viele Design-Slots sie verwenden und in welchem Zeitraum sie angezeigt werden.

1. Klicken Sie auf **[!UICONTROL Seite]** Optionen“ auf den Umschalter **[!UICONTROL Vordere]** oder **[!UICONTROL Zurück]**.

   Die folgende Abbildung zeigt den Umschalter **[!UICONTROL Vordere]**&quot; in der Position „Ein“. Promotions können sowohl vor als auch nach den Kriterienergebnissen eingefügt werden.

   ![Ändern Sie das Dialogfeld für die Promotion, wobei der Umschalter für die vordere Promotion aktiviert ist und die Optionen für Design-Slots, Planung und Promotion-Typ angezeigt werden](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

1. Legen Sie die **[!UICONTROL Anzahl der Design-Slots]** fest, die für hochgestufte Elemente verwendet werden sollen.

   Je nach [!DNL Recommendations] können bis zu 20 Steckplätze genutzt werden. Jeder verwendete Slot wird für die basierend auf den Kriterien zurückgegebenen Empfehlungen nicht mehr verfügbar sein.

1. Legen Sie **hochgestuften Elemente ein**- und **Enddatum** fest.

   Wenn kein Startdatum festgelegt ist, beginnt die Promotion sofort. Wenn kein Enddatum festgelegt ist, wird die Promotion unbegrenzt ausgeführt.

1. Wählen Sie einen **[!UICONTROL Promotion-Typ]**:

   * **[!UICONTROL Liste der Elemente]**: Geben Sie die `entity.id` Werte der heraufzustufenden Elemente getrennt durch Kommas ein.
   * **[!UICONTROL Nach Attribut bewerben]**: Fügen Sie Regeln hinzu, um die Attribute der zu bewerbenden Elemente zu definieren. Diese Option ermöglicht dynamische Übereinstimmungen durch statische und dynamische Einschlussregeln. Detaillierte Informationen, Beispiele und Anwendungsfallszenarien finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#inclusion-rules).
   * **[!UICONTROL Sammlung bewerben]**: Wählen Sie die Sammlung der zu bewerbenden Elemente aus. Für Promotions können neue Sammlungen erstellt werden. Siehe [Erstellen einer Sammlung](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08).

   Der Promotion-Typ bestimmt auch die Sortierreihenfolge der hochgestuften Elemente. Siehe [Promotion-Typen und Sortierreihenfolge](#promotion-sort-order).

   ![Dialogfeld „Promotion ändern“ mit hervorgehobenen Optionen für den Promotion-Typ: Liste von Elementen, Nach Attribut bewerben und Sammlung bewerben](/help/main/c-recommendations/t-create-recs-activity/assets/promotion_type.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Promotions gelten für alle Erlebnisse in der Aktivität.

## Promotion-Typen und Sortierreihenfolge {#promotion-sort-order}

Die Sortierreihenfolge der hochgestuften Elemente hängt vom Promotion-Typ ab, wie die folgende Tabelle zeigt.

| Promotion-Typ | Standardsortierung | Sicherungssortierung | Dynamische Filteroption |
| --- | --- | --- | --- |
| **[!UICONTROL Liste der Elemente]** | Auf der [!DNL Target]-Benutzeroberfläche oder API eingegebene Reihenfolge | Zufällig (wenn über die Benutzeroberfläche oder API ausgewählt) | Nein |
| **[!UICONTROL Hochstufen nach Attribut]** | `entity.value` (absteigend) | Keine Randomisierung | Ja |
| **[!UICONTROL Sammlung hochstufen]** | `entity.value` (absteigend) | Keine Randomisierung | Nein |

* **[!UICONTROL Liste der Elemente]**: Die standardmäßige Sortierreihenfolge ist die Reihenfolge, die in der [!DNL Target]-Benutzeroberfläche oder API eingegeben wurde. Für **[!UICONTROL Typ ist]** Kontrollkästchen „Elementreihenfolge zuordnen“ verfügbar. Wenn die Liste mehr Elemente enthält als die Anzahl der Slots, die für Promotions festgelegt wurden, bestimmt diese Option nach dem Zufallsprinzip, welche hochgestuften Elemente im Design angezeigt werden. Bei jedem Treffer wählt [!DNL Target] nach dem Zufallsprinzip die für Promotions in der Vorlage aktivierten Elemente aus dem gesamten Promotion-Set aus.
* **[!UICONTROL Nach Attribut bewerben]** und **[!UICONTROL Sammlung bewerben]**: Die Standardreihenfolge basiert auf dem `entity.value` Attribut in absteigender numerischer Reihenfolge. Die Randomisierung der Reihenfolge ist nicht anwendbar.

Wenn die Entitäten kein `entity.value` haben (z. B. das Unternehmen verkauft keine Produkte), kann ein numerischer Wert wie das Veröffentlichungsdatum an das `entity.value` Attribut übergeben werden. Die hochgestuften Elemente werden dann nach dem letzten Veröffentlichungsdatum in absteigender Reihenfolge sortiert. Das Attribut `entity.value` ist vom Typ double und akzeptiert keine Zeichenfolgen.
