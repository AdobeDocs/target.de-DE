---
description: Fügen Sie Promotionsartikel hinzu und steuern Sie deren Platzierung in Ihren Recommendations-Designs. Sie können statische und dynamische Promotions hinzufügen.
keywords: promotions; front promotions; back promotions; Promotions-Typ
seo-description: Fügen Sie beworbene Artikel hinzu und steuern Sie ihre Platzierung in Ihren Adobe Target Recommendations-Entwürfen. Sie können statische und dynamische Promotions hinzufügen.
seo-title: Fügen Sie Promotions in Adobe Target Recommendations-Entwürfen hinzu.
solution: Target
title: Hinzufügen von Promotions
title-outputclass: premium
topic: Premium
uuid: 732bf2c2-0cc7-4d5d-9919-9fe668344d39
badge: premium
translation-type: tm+mt
source-git-commit: e8e6dcadf307209abcc712798b714af0a5be2e7e

---


# ![PREMIUM](/help/assets/premium.png) Promotions hinzufügen{#add-promotions}

Fügen Sie Promotionsartikel hinzu und steuern Sie deren Platzierung in Ihren Recommendations-Designs. Sie können statische und dynamische Promotions hinzufügen.

>[!IMPORTANT]
>
>Statische und dynamische Ausschlussregeln sind leistungsstarke Funktionen, die Ihnen beim Marketing helfen können. Ausführliche Informationen, Beispiele und Anwendungsszenarios finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Beim Erstellen einer [!DNL Recommendations]-Aktivität haben Sie die Möglichkeit, beworbene Artikel in Ihr [!DNL Recommendations]-Design einzufügen. Promotions nutzen verfügbare Slots in einem Design und haben Vorrang vor Kriterienergebnissen und Sicherungsempfehlungen. Wenn Ihr Design zum Beispiel über sechs Slots verfügt und Sie zwei davon für Promotions einsetzen, stehen vier Slots für Artikel zur Verfügung, die anhand von Kriterien empfohlen werden.

Promotions werden zu Artikeln dedupliziert, die den Kriterien für Ihre Aktivität entsprechen, sodass ein gegebenes Element in einer einzigen Empfehlungsablage nicht doppelt angezeigt wird.

Sie können einzelne Artikel bewerben, Artikel dynamisch bewerben, Artikel auf Grundlage von Attributen bewerben oder Sammlungen bewerben.

![](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Durch die Verwendung von Promotions ändert sich die CSV-Struktur und -Ausgabe. Diese Änderungen können sich auf externe Prozesse auswirken, bei denen CSV involviert ist, wie zum Beispiel E-Mail.

1. On the **[!UICONTROL Options]** page, click the **[!UICONTROL Front Promotion]** or **[!UICONTROL Back Promotion]** toggle.

   The following illustration shows the [!UICONTROL Front Promotion] toggle in the "On" position.

   ![Optionen für Vorwärts-Promotion hinzufügen](/help/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   Sie können Promotions sowohl vor *als auch* nach Ihren Kriterienergebnissen einfügen.
1. Legen Sie die Anzahl der Design-Slots fest, die für beworbene Artikel verwendet werden sollen.

   Je nach [!DNL Recommendations]-Design können Sie bis zu 20 Slots verwenden. Jeder von Ihnen genutzte Slot steht nicht mehr für Empfehlungen, die auf Grundlage Ihrer Kriterien zurückgegeben werden, zur Verfügung.

1. Legen Sie ein Start- und Enddatum für Ihre beworbenen Artikel fest.

   Wenn Sie kein Startdatum festlegen, beginnt die Promotion sofort. Wenn Sie kein Enddatum festlegen, wird die Promotion unbegrenzt lange ausgeführt.

1. Wählen Sie einen **[!UICONTROL Promotion-Typ]** aus.

   * Wählen Sie **[!UICONTROL Liste der Artikel]** aus, und geben Sie die `entity.id`-Werte der einzelnen Artikel, die beworben werden sollen, durch Kommas getrennt ein.

      Wenn Ihre Liste mehr Artikel enthält, als Slots für die Promotion festgelegt sind, können Sie das Kontrollkästchen **[!UICONTROL Elementreihenfolge randomisieren]aktivieren, damit die Anzeige der beworbenen Artikel in Ihrem Design variiert wird.** Wenn Sie diese Option auswählen, wählen Target zufällig die Anzahl der Elemente aus, die für Promotions in der Vorlage aus der gesamten Promotion für jeden Besuch aktiviert wurden.

   * Wählen Sie **[!UICONTROL Hervorheben nach Attribut]aus und fügen Sie Regeln hinzu, um die Attribute der Artikel zu definieren, die beworben werden sollen.**

      Wenn Sie „Hervorheben nach Attribut“ auswählen, können Sie dynamische Übereinstimmungen erstellen. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Wählen Sie **[!UICONTROL Sammlung hervorheben]** aus und wählen Sie eine Sammlung von Artikeln aus, die beworben werden soll. Sie können auch neue Sammlungen erstellen, die für Promotions verwendet werden sollen. Siehe [Erstellen einer Sammlung](../../c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) für weitere Informationen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Promotions gelten für alle Erlebnisse in der Aktivität.
