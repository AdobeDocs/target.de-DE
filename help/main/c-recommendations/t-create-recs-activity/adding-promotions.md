---
keywords: Promotions;vordere Promotions;hintere Promotions;Promotions-Typ;Liste der Elemente;Nach Attribut bewerben;Sammlung bewerben
description: Erfahren Sie, wie Sie hochgestufte Elemente hinzufügen und deren Platzierung in Ihren Adobe/Recommendations [!DNL Target] Designs steuern. Sie können statische und dynamische Promotions hinzufügen.
title: Wie füge ich Promotions in Recommendations-Designs hinzu?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
TQID: https://experienceleague.adobe.com/tAfKOzwjnUJgypDh-4LdVukNlTVwMS4UkvcNmCaCV0E
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 709
ht-degree: 41%

---

# Hinzufügen von Promotions

Fügen Sie hochgestufte Elemente hinzu und steuern Sie deren Platzierung in Ihren [!DNL Adobe Target Recommendations]. Sie können statische und dynamische Promotions hinzufügen.

>[!IMPORTANT]
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Detaillierte Informationen, Beispiele und Anwendungsfallszenarien finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Beim Erstellen einer [!DNL Recommendations]-Aktivität haben Sie die Möglichkeit, beworbene Artikel in Ihr [!DNL Recommendations]-Design einzufügen. Promotions nutzen verfügbare Slots in einem Design und haben Vorrang vor Kriterienergebnissen und Sicherungsempfehlungen. Wenn Ihr Design zum Beispiel über sechs Slots verfügt und Sie zwei davon für Promotions einsetzen, stehen vier Slots für Artikel zur Verfügung, die anhand von Kriterien empfohlen werden.

Promotions werden in Bezug auf Artikeln dedupliziert, die von den Kriterien für Ihre Aktivität empfohlen werden, sodass ein Artikel nicht doppelt in einer einzelnen Empfehlungsablage angezeigt wird.

Sie können einzelne Artikel bewerben, Artikel dynamisch bewerben, Artikel auf Grundlage von Attributen bewerben oder Sammlungen bewerben.

![[!UICONTROL Option &quot;] Promotion“ und [!UICONTROL Rückwärtsförderung] in [!DNL Target] Benutzeroberfläche](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Durch die Verwendung von Promotions ändert sich die CSV-Struktur und -Ausgabe. Diese Änderungen können sich auf externe Prozesse auswirken, bei denen CSV involviert ist, wie zum Beispiel E-Mail.

1. Klicken Sie auf **[!UICONTROL Seite]** Optionen“ auf den Umschalter **[!UICONTROL Vordere]** oder **[!UICONTROL Zurück]**.

   Die folgende Abbildung zeigt den Umschalter [!UICONTROL Vordere &#x200B;]&quot; in der Position „Ein“.

   ![Hinzufügen von Optionen für die Vorwärts-Promotion &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   Sie können Promotions sowohl vor *als auch* nach Ihren Kriterienergebnissen einfügen.

1. Legen Sie die Anzahl der Design-Slots fest, die für beworbene Artikel verwendet werden sollen.

   Je nach [!DNL Recommendations]-Design können Sie bis zu 20 Slots verwenden. Jeder von Ihnen genutzte Slot steht nicht mehr für Empfehlungen, die auf Grundlage Ihrer Kriterien zurückgegeben werden, zur Verfügung.

1. Legen Sie ein Start- und Enddatum für Ihre beworbenen Artikel fest.

   Wenn Sie kein Startdatum festlegen, beginnt die Promotion sofort. Wenn Sie kein Enddatum festlegen, läuft die Promotion auf unbestimmte Zeit.

1. Wählen Sie einen **[!UICONTROL Promotion-Typ]** aus.

   * Wählen Sie **[!UICONTROL Liste der Elemente]** und geben Sie die `entity.id` Werte (durch Kommas getrennt) der spezifischen Elemente ein, die Sie hochstufen möchten.

   * Wählen Sie **[!UICONTROL Hervorheben nach Attribut]** aus und fügen Sie Regeln hinzu, um die Attribute der Artikel zu definieren, die beworben werden sollen.

     Bei Auswahl von [!UICONTROL Nach Attribut &#x200B;] Sie dynamische Übereinstimmungen erstellen. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Wählen Sie **[!UICONTROL Sammlung hervorheben]** aus und wählen Sie eine Sammlung von Artikeln aus, die beworben werden soll.

     Sie können auch neue Sammlungen erstellen, die für Promotions verwendet werden sollen. Weitere Informationen [&#x200B; Sie unter &#x200B;](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) erstellen .

   Wenn Sie **[!UICONTROL Liste der Artikel]** als **[!UICONTROL Promotion-Typ]** ausgewählt haben, können Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Elementreihenfolge Randomisieren]** aktivieren.

   Die standardmäßige Sortierreihenfolge für [!UICONTROL Liste von Elementen] basiert auf der Reihenfolge, die Sie in der [!DNL Target]-Benutzeroberfläche oder API eingegeben haben. Wenn Ihre Liste mehr Elemente enthält als die Anzahl der Slots, die Sie für Promotions festgelegt haben, [!UICONTROL &#x200B; die Option &quot;] zuordnen“ die hochgestuften Elemente, die in Ihrem Design angezeigt werden, zufällig. Die Auswahl dieser Option führt [!DNL Target] zufällige Auswahl der für Promotions in der Vorlage aktivierten Elemente aus dem gesamten Promotion-Set bei jedem Treffer.

   Wenn Ihre Entitäten nicht über ein `entity.value`-Attribut verfügen (Sie verkaufen beispielsweise keine Produkte), können Sie einen numerischen Wert in das `entity.value`-Attribut übergeben, z. B. das Veröffentlichungsdatum. In diesem Fall können hochgestufte Elemente basierend auf dem letzten Veröffentlichungsdatum in absteigender Reihenfolge hochgestuft werden. Das Attribut `entity.value` ist vom Typ „double“ und akzeptiert keine Zeichenfolgen.

   Wenn Sie die Option **[!UICONTROL Nach Attribut bewerben]** oder **[!UICONTROL Sammlung bewerben]** ausgewählt haben, ist die Option zum Randomisieren der Reihenfolge nicht anwendbar.

   Beim Hochstufen bestimmter Elemente mit den Optionen [!UICONTROL Nach Attribut &#x200B;] oder [!UICONTROL Sammlung &#x200B;]) basiert die Standardreihenfolge für die Darstellung von Elementen auf dem `entity.value` Attribut in absteigender numerischer Reihenfolge.

   Die folgende Tabelle zeigt die Unterschiede zwischen diesen Optionen:

   | Promotion-Typ | Standardsortierung | Sicherungssortierung | Dynamische Filteroption |
   | --- | --- | --- | --- |
   | [!UICONTROL Liste der Elemente] | In der Target-Benutzeroberfläche/API eingegebene Reihenfolge | Zufällig (wenn über Benutzeroberfläche/API ausgewählt) | Nein |
   | [!UICONTROL Hochstufen nach Attribut] | `entity.value` (absteigend) | Keine Randomisierung | Ja |
   | [!UICONTROL Sammlung hochstufen] | `entity.value` (absteigend) | Keine Randomisierung | Nein |

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Promotions gelten für alle Erlebnisse in der Aktivität.
