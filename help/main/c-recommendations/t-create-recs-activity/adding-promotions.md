---
keywords: Promotions;vordere Promotions;hintere Promotions;Promotions-Typ;Liste der Elemente;Nach Attribut bewerben;Sammlung bewerben
description: Erfahren Sie, wie Sie hochgestufte Elemente hinzufügen und deren Platzierung in Ihren Adobe [!DNL Target] Recommendations-Designs steuern. Sie können statische und dynamische Promotions hinzufügen.
title: Wie kann ich in Recommendations Designs Promotions hinzufügen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 40%

---

# Hinzufügen von Promotions

Fügen Sie hochgestufte Elemente hinzu und steuern Sie deren Platzierung in Ihren [!DNL Adobe Target Recommendations]. Sie können statische und dynamische Promotions hinzufügen.

>[!IMPORTANT]
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Detaillierte Informationen, Beispiele und Anwendungsfallszenarien finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Beim Erstellen einer [!DNL Recommendations]-Aktivität haben Sie die Möglichkeit, beworbene Artikel in Ihr [!DNL Recommendations]-Design einzufügen. Promotions nutzen verfügbare Slots in einem Design und haben Vorrang vor Kriterienergebnissen und Sicherungsempfehlungen. Wenn Ihr Design zum Beispiel über sechs Slots verfügt und Sie zwei davon für Promotions einsetzen, stehen vier Slots für Artikel zur Verfügung, die anhand von Kriterien empfohlen werden.

Promotions werden in Bezug auf Artikeln dedupliziert, die von den Kriterien für Ihre Aktivität empfohlen werden, sodass ein Artikel nicht doppelt in einer einzelnen Empfehlungsablage angezeigt wird.

Sie können einzelne Artikel bewerben, Artikel dynamisch bewerben, Artikel auf Grundlage von Attributen bewerben oder Sammlungen bewerben.

![[!UICONTROL Front Promotion]- und [!UICONTROL Back Promotion] in [!DNL Target] Benutzeroberfläche](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Durch die Verwendung von Promotions ändert sich die CSV-Struktur und -Ausgabe. Diese Änderungen können sich auf externe Prozesse auswirken, bei denen CSV involviert ist, wie zum Beispiel E-Mail.

1. Klicken Sie auf der Seite **[!UICONTROL Options]** auf den Umschalter **[!UICONTROL Front Promotion]** oder **[!UICONTROL Back Promotion]** .

   Die folgende Abbildung zeigt den [!UICONTROL Front Promotion]-Umschalter in der Position „Ein“.

   ![Hinzufügen von Optionen für die Vorwärts-Promotion ](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   Sie können Promotions sowohl vor *als auch* nach Ihren Kriterienergebnissen einfügen.

1. Legen Sie die Anzahl der Design-Slots fest, die für beworbene Artikel verwendet werden sollen.

   Je nach [!DNL Recommendations]-Design können Sie bis zu 20 Slots verwenden. Jeder von Ihnen genutzte Slot steht nicht mehr für Empfehlungen, die auf Grundlage Ihrer Kriterien zurückgegeben werden, zur Verfügung.

1. Legen Sie ein Start- und Enddatum für Ihre beworbenen Artikel fest.

   Wenn Sie kein Startdatum festlegen, beginnt die Promotion sofort. Wenn Sie kein Enddatum festlegen, läuft die Promotion auf unbestimmte Zeit.

1. **[!UICONTROL Promotion Type]** auswählen.

   * Wählen Sie **[!UICONTROL List of items]** aus und geben Sie die `entity.id` Werte (durch Kommas getrennt) der spezifischen Elemente ein, die Sie hochstufen möchten.

   * Wählen Sie **[!UICONTROL Promote by attribute]** aus und fügen Sie Regeln hinzu, um die Attribute der Elemente zu definieren, die Sie hochstufen möchten.

     Wenn Sie [!UICONTROL Promote by Attribute] auswählen, können Sie dynamische Übereinstimmungen erstellen. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Wählen Sie **[!UICONTROL Promote a collection]** und die Sammlung von Elementen aus, die Sie hochstufen möchten.

     Sie können auch neue Sammlungen erstellen, die für Promotions verwendet werden sollen. Weitere Informationen [ Sie unter ](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) erstellen .

   Wenn Sie **[!UICONTROL List of Items]** als **[!UICONTROL Promotion Type]** ausgewählt haben, können Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Randomize Item Order]** aktivieren.

   Die standardmäßige Sortierreihenfolge für [!UICONTROL List of Items] basiert auf der Reihenfolge, die Sie in der [!DNL Target]-Benutzeroberfläche oder API eingegeben haben. Wenn Ihre Liste mehr Elemente enthält als die Anzahl der Slots, die Sie für Werbeaktionen festgelegt haben, werden die in Ihrem Design angezeigten beworbenen Elemente durch die Option [!UICONTROL Randomize Item Order] randomisiert. Die Auswahl dieser Option führt [!DNL Target] zufällige Auswahl der für Promotions in der Vorlage aktivierten Elemente aus dem gesamten Promotion-Set bei jedem Treffer.

   Wenn Ihre Entitäten nicht über ein `entity.value`-Attribut verfügen (Sie verkaufen beispielsweise keine Produkte), können Sie einen numerischen Wert in das `entity.value`-Attribut übergeben, z. B. das Veröffentlichungsdatum. In diesem Fall können hochgestufte Elemente basierend auf dem letzten Veröffentlichungsdatum in absteigender Reihenfolge hochgestuft werden. Das Attribut `entity.value` ist vom Typ „double“ und akzeptiert keine Zeichenfolgen.

   Wenn Sie die Option **[!UICONTROL Promote by Attribute]** oder **[!UICONTROL Promote a Collection]** ausgewählt haben, ist die Option zum Randomisieren der Reihenfolge nicht anwendbar.

   Beim Hochstufen bestimmter Elemente mit den Optionen [!UICONTROL Promote by Attribute] oder [!UICONTROL Promote a Collection] basiert die Standardreihenfolge, in der die Elemente angezeigt werden, auf dem Attribut `entity.value` in absteigender numerischer Reihenfolge.

   Die folgende Tabelle zeigt die Unterschiede zwischen diesen Optionen:

   | Promotion-Typ | Standardsortierung | Sicherungssortierung | Dynamische Filteroption |
   | --- | --- | --- | --- |
   | [!UICONTROL List of Items] | In der Target-Benutzeroberfläche/API eingegebene Reihenfolge | Zufällig (wenn über Benutzeroberfläche/API ausgewählt) | Nein |
   | [!UICONTROL Promote by Attribute] | `entity.value` (absteigend) | Keine Randomisierung | Ja |
   | [!UICONTROL Promote a Collection] | `entity.value` (absteigend) | Keine Randomisierung | Nein |

1. Klicken Sie auf **[!UICONTROL Save]**.

Promotions gelten für alle Erlebnisse in der Aktivität.
