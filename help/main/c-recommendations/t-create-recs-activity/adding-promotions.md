---
keywords: Promotions; Vorwärts-Promotions; Rückwärts-Promotions; Promotions-Typ; Liste der Artikel; Anzeigen nach Attribut; Anzeigen einer Sammlung
description: Erfahren Sie, wie Sie beworbene Artikel hinzufügen und ihre Platzierung in Ihrer Adobe steuern können. [!DNL Target] Recommendations-Designs. Sie können statische und dynamische Promotions hinzufügen.
title: Wie füge ich Promotions in Recommendations-Designs hinzu?
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 50%

---

# ![PREMIUM](/help/main/assets/premium.png) Promotions hinzufügen

Fügen Sie Promotionsartikel hinzu und steuern Sie deren Platzierung in Ihren [!DNL Adobe Target Recommendations]-Designs. Sie können statische und dynamische Promotions hinzufügen.

>[!IMPORTANT]
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarien finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Beim Erstellen einer [!DNL Recommendations]-Aktivität haben Sie die Möglichkeit, beworbene Artikel in Ihr [!DNL Recommendations]-Design einzufügen. Promotions nutzen verfügbare Slots in einem Design und haben Vorrang vor Kriterienergebnissen und Sicherungsempfehlungen. Wenn Ihr Design zum Beispiel über sechs Slots verfügt und Sie zwei davon für Promotions einsetzen, stehen vier Slots für Artikel zur Verfügung, die anhand von Kriterien empfohlen werden.

Promotions werden in Bezug auf Artikeln dedupliziert, die von den Kriterien für Ihre Aktivität empfohlen werden, sodass ein Artikel nicht doppelt in einer einzelnen Empfehlungsablage angezeigt wird.

Sie können einzelne Artikel bewerben, Artikel dynamisch bewerben, Artikel auf Grundlage von Attributen bewerben oder Sammlungen bewerben.

![[!UICONTROL Vorwärts-Promotion] und [!UICONTROL Rückwärts-Promotion] Optionen in [!DNL Target] Benutzeroberfläche](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Durch die Verwendung von Promotions ändert sich die CSV-Struktur und -Ausgabe. Diese Änderungen können sich auf externe Prozesse auswirken, bei denen CSV involviert ist, wie zum Beispiel E-Mail.

1. Klicken Sie auf der Seite **[!UICONTROL Optionen]** auf die Schaltfläche **[!UICONTROL Vorwärts-Promotion]** oder **[!UICONTROL Rückwärts-Promotion]**.

   Die folgende Abbildung zeigt den Umschalter [!UICONTROL „Vorwärts-Promotion“] in der aktivierten Position.

   ![Hinzufügen von Optionen für die Vorwärts-Promotion ](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   Sie können Promotions sowohl vor *als auch* nach Ihren Kriterienergebnissen einfügen.

1. Legen Sie die Anzahl der Design-Slots fest, die für beworbene Artikel verwendet werden sollen.

   Je nach [!DNL Recommendations]-Design können Sie bis zu 20 Slots verwenden. Jeder von Ihnen genutzte Slot steht nicht mehr für Empfehlungen, die auf Grundlage Ihrer Kriterien zurückgegeben werden, zur Verfügung.

1. Legen Sie ein Start- und Enddatum für Ihre beworbenen Artikel fest.

   Wenn Sie kein Startdatum festlegen, beginnt die Promotion sofort. Wenn Sie kein Enddatum festlegen, läuft die Promotion auf unbestimmte Zeit.

1. Wählen Sie einen **[!UICONTROL Promotion-Typ]** aus.

   * Wählen Sie **[!UICONTROL Liste der Artikel]** aus, und geben Sie die `entity.id`-Werte der einzelnen Artikel, die beworben werden sollen, durch Kommas getrennt ein.

   * Wählen Sie **[!UICONTROL Hervorheben nach Attribut]** aus und fügen Sie Regeln hinzu, um die Attribute der Artikel zu definieren, die beworben werden sollen.

      Wenn Sie [!UICONTROL Hervorheben nach Attribut], können Sie dynamische Übereinstimmungen erstellen. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Wählen Sie **[!UICONTROL Sammlung hervorheben]** aus und wählen Sie eine Sammlung von Artikeln aus, die beworben werden soll.

      Sie können auch neue Sammlungen erstellen, die für Promotions verwendet werden sollen. Siehe [Kollektion erstellen](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) für weitere Informationen.
   Wenn Sie **[!UICONTROL Liste der Elemente]** als **[!UICONTROL Promotion-Typ]** können Sie die **[!UICONTROL Elementreihenfolge randomisieren]** aktivieren, falls gewünscht.

   Die standardmäßige Sortierreihenfolge für [!UICONTROL Liste der Elemente] basiert auf der Reihenfolge, die Sie in der [!DNL Target] Benutzeroberfläche oder API. Wenn Ihre Liste mehr Artikel enthält, als Slots für Promotions festgelegt sind, wird die [!UICONTROL Elementreihenfolge randomisieren] -Option randomisiert die beworbenen Elemente, die in Ihrem Design angezeigt werden. Die Auswahl dieser Option führt zu [!DNL Target] zufällige Auswahl der für Promotions aktivierten Elemente in der Vorlage aus dem gesamten Promotion-Satz bei jedem Treffer.

   Wenn Ihre Entitäten nicht über eine `entity.value` -Attribut verwenden (Sie verkaufen beispielsweise keine Produkte), können Sie einen numerischen Wert in die `entity.value` -Attribut, z. B. das Veröffentlichungsdatum. In diesem Fall können beworbene Artikel basierend auf dem letzten Veröffentlichungsdatum in absteigender Reihenfolge beworben werden. Die `entity.value` -Attribut vom Typ &quot;double&quot; ist; es akzeptiert keine Zeichenfolgen.

   Wenn Sie die Option **[!UICONTROL Hervorheben nach Attribut]** oder **[!UICONTROL Weiterleiten einer Sammlung]** -Option, ist die Option zur Randomisierung der Bestellung nicht verfügbar.

   Wenn Sie bestimmte Artikel mit dem [!UICONTROL Hervorheben nach Attribut] oder [!UICONTROL Weiterleiten einer Sammlung] -Optionen, basiert die Standardreihenfolge, in der die Elemente angezeigt werden, auf der `entity.value` -Attribut in absteigender numerischer Reihenfolge angezeigt.

   Die folgende Tabelle zeigt die Unterschiede zwischen diesen Optionen:

   | Art der Promotion | Standardsortierung | Sicherungssortierung | Dynamische Filteroption |
   | --- | --- | --- | --- |
   | [!UICONTROL Liste der Elemente] | Reihenfolge der Eingabe in der Target-Benutzeroberfläche/-API | Zufällig (bei Auswahl über Benutzeroberfläche/API) | Nein |
   | [!UICONTROL Hervorheben nach Attribut] | `entity.value` (absteigende Reihenfolge) | Keine Randomisierung | Ja |
   | [!UICONTROL Weiterleiten einer Sammlung] | `entity.value` (absteigende Reihenfolge) | Keine Randomisierung | Nein |

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Promotions gelten für alle Erlebnisse in der Aktivität.
