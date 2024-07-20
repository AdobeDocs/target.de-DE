---
keywords: Promotions; Vorwärts-Promotions; Rückwärts-Promotions; Promotions-Typ; Liste der Artikel; Anzeigen nach Attribut; Anzeigen einer Sammlung
description: Erfahren Sie, wie Sie beworbene Artikel hinzufügen und deren Platzierung in Ihren Adobe [!DNL Target] Recommendations-Designs steuern können. Sie können statische und dynamische Promotions hinzufügen.
title: Wie füge ich Promotions in Recommendations-Designs hinzu?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 40%

---

# Hinzufügen von Promotions

Fügen Sie Promotionsartikel hinzu und steuern Sie deren Platzierung in Ihren [!DNL Adobe Target Recommendations]-Designs. Sie können statische und dynamische Promotions hinzufügen.

>[!IMPORTANT]
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarien finden Sie unter [Dynamische und statische Einschlussregeln verwenden](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Beim Erstellen einer [!DNL Recommendations]-Aktivität haben Sie die Möglichkeit, beworbene Artikel in Ihr [!DNL Recommendations]-Design einzufügen. Promotions nutzen verfügbare Slots in einem Design und haben Vorrang vor Kriterienergebnissen und Sicherungsempfehlungen. Wenn Ihr Design zum Beispiel über sechs Slots verfügt und Sie zwei davon für Promotions einsetzen, stehen vier Slots für Artikel zur Verfügung, die anhand von Kriterien empfohlen werden.

Promotions werden in Bezug auf Artikeln dedupliziert, die von den Kriterien für Ihre Aktivität empfohlen werden, sodass ein Artikel nicht doppelt in einer einzelnen Empfehlungsablage angezeigt wird.

Sie können einzelne Artikel bewerben, Artikel dynamisch bewerben, Artikel auf Grundlage von Attributen bewerben oder Sammlungen bewerben.

Optionen ![[!UICONTROL Front Promotion] und [!UICONTROL Back Promotion] in der [!DNL Target] Benutzeroberfläche](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Durch die Verwendung von Promotions ändert sich die CSV-Struktur und -Ausgabe. Diese Änderungen können sich auf externe Prozesse auswirken, bei denen CSV involviert ist, wie zum Beispiel E-Mail.

1. Klicken Sie auf der Seite **[!UICONTROL Options]** auf den Umschalter **[!UICONTROL Front Promotion]** oder **[!UICONTROL Back Promotion]** .

   Die folgende Abbildung zeigt den Umschalter [!UICONTROL Front Promotion] in der Position &quot;Ein&quot;.

   ![Hinzufügen von Optionen für die Vorwärts-Promotion ](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   Sie können Promotions sowohl vor *als auch* nach Ihren Kriterienergebnissen einfügen.

1. Legen Sie die Anzahl der Design-Slots fest, die für beworbene Artikel verwendet werden sollen.

   Je nach [!DNL Recommendations]-Design können Sie bis zu 20 Slots verwenden. Jeder von Ihnen genutzte Slot steht nicht mehr für Empfehlungen, die auf Grundlage Ihrer Kriterien zurückgegeben werden, zur Verfügung.

1. Legen Sie ein Start- und Enddatum für Ihre beworbenen Artikel fest.

   Wenn Sie kein Startdatum festlegen, beginnt die Promotion sofort. Wenn Sie kein Enddatum festlegen, läuft die Promotion auf unbestimmte Zeit.

1. Wählen Sie einen **[!UICONTROL Promotion Type]** aus.

   * Wählen Sie **[!UICONTROL List of items]** aus und geben Sie die `entity.id` -Werte der einzelnen Artikel, die beworben werden sollen, durch Kommas getrennt ein.

   * Wählen Sie **[!UICONTROL Promote by attribute]** aus und fügen Sie Regeln hinzu, um die Attribute der Artikel zu definieren, die beworben werden sollen.

     Wenn Sie &quot;[!UICONTROL Promote by Attribute]&quot; auswählen, können Sie dynamische Übereinstimmungen erstellen. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Wählen Sie &quot;**[!UICONTROL Promote a collection]**&quot;und wählen Sie die Sammlung der Artikel aus, die beworben werden sollen.

     Sie können auch neue Sammlungen erstellen, die für Promotions verwendet werden sollen. Weitere Informationen finden Sie unter [Erstellen einer Sammlung](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) .

   Wenn Sie **[!UICONTROL List of Items]** als **[!UICONTROL Promotion Type]** auswählen, können Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Randomize Item Order]** aktivieren.

   Die standardmäßige Sortierreihenfolge für [!UICONTROL List of Items] basiert auf der Reihenfolge, die Sie in der Benutzeroberfläche oder API von [!DNL Target] eingegeben haben. Wenn Ihre Liste mehr Artikel enthält, als Slots für Promotions festgelegt sind, werden die beworbenen Artikel, die in Ihrem Design angezeigt werden, durch die Option [!UICONTROL Randomize Item Order] zufällig omisiert. Wenn Sie diese Option wählen, wählen Sie [!DNL Target] zufällig die für Promotions aktivierten Elemente in der Vorlage aus dem gesamten Promotion-Satz bei jedem Treffer aus.

   Wenn Ihre Entitäten nicht über das Attribut `entity.value` verfügen (z. B. wenn Sie keine Produkte verkaufen), können Sie einen numerischen Wert an das Attribut `entity.value` übergeben, z. B. das Veröffentlichungsdatum. In diesem Fall können beworbene Artikel basierend auf dem letzten Veröffentlichungsdatum in absteigender Reihenfolge beworben werden. Das Attribut `entity.value` hat den Typ &quot;double&quot;. Es akzeptiert keine Zeichenfolgen.

   Wenn Sie die Option **[!UICONTROL Promote by Attribute]** oder **[!UICONTROL Promote a Collection]** ausgewählt haben, ist die Option zum Zufälligen der Reihenfolge nicht anwendbar.

   Beim Weiterleiten bestimmter Elemente mithilfe der Optionen [!UICONTROL Promote by Attribute] oder [!UICONTROL Promote a Collection] basiert die Standardreihenfolge, in der die Elemente angezeigt werden, auf dem Attribut `entity.value` in absteigender numerischer Reihenfolge.

   Die folgende Tabelle zeigt die Unterschiede zwischen diesen Optionen:

   | Art der Promotion | Standardsortierung | Sicherungssortierung | Dynamische Filteroption |
   | --- | --- | --- | --- |
   | [!UICONTROL List of Items] | Reihenfolge der Eingabe in der Target-Benutzeroberfläche/-API | Zufällig (bei Auswahl über Benutzeroberfläche/API) | Nein |
   | [!UICONTROL Promote by Attribute] | `entity.value` (absteigende Reihenfolge) | Keine Randomisierung | Ja |
   | [!UICONTROL Promote a Collection] | `entity.value` (absteigende Reihenfolge) | Keine Randomisierung | Nein |

1. Klicken Sie auf **[!UICONTROL Save]**.

Promotions gelten für alle Erlebnisse in der Aktivität.
