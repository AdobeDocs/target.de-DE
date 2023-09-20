---
keywords: Priorität;Erlebnis erstellen;Prioritäten;Erlebnis;Zielgruppe;Erlebnisse;Erlebnisse wechseln;Visual Experience Composer
description: Erfahren Sie, wie Besucher in einer [!DNL Adobe Target] [!UICONTROL Erlebnis-Targeting] (XT) -Aktivität, während sich ihre Profile entwickeln.
title: Können Besucher Erlebnisse in einem [!UICONTROL Erlebnis-Targeting] Aktivität?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 44%

---

# Wechsel zwischen Erlebnissen in [!UICONTROL Erlebnis-Targeting]

Mit [!UICONTROL Erlebnis-Targeting]können Sie steuern, welches Erlebnis Besucher sehen, während sich ihre Profile entwickeln.

Die folgende Liste enthält nur einige Szenarien, in denen sich die Besucherprofile entwickeln können und Sie möglicherweise unterschiedliche Inhalte basierend auf diesen Änderungen präsentieren möchten:

| Szenario | Details |
|--- |--- |
| Geografischer Standort | Wenn Besucher auf Geschäfts- oder private Reisen gehen, rufen sie Ihre Webseite oder mobile App möglicherweise von unterschiedlichen geografischen Standorten auf. |
| Kundenstatus | Besucher werden unter Umständen als potenzielle Kunden gewertet, bevor sie ein Konto erstellen oder Produkte erwerben. |
| Kategorieaffinität | Die [Kategorieaffinität](/help/main/c-target/c-visitor-profile/category-affinity.md) Funktion in [!DNL Target] erfasst automatisch die von Besuchern angezeigten Kategorien und berechnet dann zu Targeting-Zwecken die Affinität der Besucher für diese Kategorie. Beispielsweise werden Besuchern, die mehrere Artikel zu einem bestimmten Thema auf Ihrer Website angesehen haben, Inhalte zu diesem Thema angezeigt. |
| Wochentag | Möglicherweise möchten Sie Besuchern kurz vor dem Wochenende Inhalte zu Filmen, Restaurants oder anderen Unterhaltungsmöglichkeiten anzeigen. |

So verwenden Sie diese Funktionen in [!DNL Target]ist es wichtig, die folgenden Informationen bei der Arbeit mit [!UICONTROL Erlebnis-Targeting] Aktivitäten:

* **Die Priorität ist nach Erlebnissen sortiert, und zwar in absteigender Reihenfolge.** Wenn ein Besucher für mehr als zwei Zielgruppen qualifiziert ist, erhält er Inhalte aus dem Erlebnis mit höherer Priorität.
* **Besucher wechseln in einem [!UICONTROL Erlebnis-Targeting] Aktivität, wenn sie sich für die Zielgruppe eines Erlebnisses mit höherer Priorität qualifizieren.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Website-Besuch aus Deutschland wechselte der Besucher zu Erlebnis B (Besucher in Deutschland).

  ![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Besucher wechseln auch zwischen Erlebnissen, wenn sie sich nicht mehr für ihre aktuelle Zielgruppe qualifizieren, sich aber für ein Erlebnis mit niedrigerer Priorität qualifizieren.**
* **Wenn Besucher sich nicht mehr für ihr aktuelles Erlebnis qualifizieren und sich nicht für ein anderes Erlebnis qualifizieren, sehen sie Standardinhalte.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Frankreich auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Besuch Ihrer Website aus Frankreich bleibt dieser Besucher im Originalerlebnis.

  ![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Ein Erlebnis, das auf &quot;Alle Besucher&quot;abzielt, kann als das letzte Erlebnis im [!UICONTROL Erlebnis-Targeting] -Aktivität, um alle Besucher zu &quot;erfassen&quot;, die sich für kein anderes Erlebnis qualifiziert haben. Wenn ein Erlebnis, das auf &quot;Alle Besucher&quot;ausgerichtet ist, nicht das letzte in der Reihenfolge ist, werden weitere zielgerichtete Erlebnisse, die unter diesem Erlebnis aufgeführt sind, weiterhin ausgewertet.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Besuch Ihrer Website aus Deutschland bleibt dieser Besucher in Erlebnis A (US-Besucher).

  ![Priorität USA > Alle Besucher](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  Sollten Sie dies nicht wünschen, können Sie eine neue Zielgruppe erstellen, die explizit als Gegenteil der gewünschten Zielgruppe definiert wurde, wie im folgenden Beispiel gezeigt:

  ![Priorität USA > Nicht USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Mit nur einem Erlebnis [!UICONTROL Erlebnis-Targeting] -Aktivität, bleiben Besucher im Erlebnis, selbst wenn sie sich nicht mehr für die Zielgruppe qualifizieren, durch die sie in dieses Erlebnis gelangt sind.**

  Sollte dies nicht gewünscht werden, können Sie ein weiteres Erlebnis erstellen, das sich an das Gegenteil Ihrer Zielgruppe richtet (beispielsweise „nicht USA“ im Gegensatz zu „USA“).

  Als weitere Option können Sie eine [!UICONTROL A/B-Test] Aktivität, die mit 100 % Traffic-Zuordnung auf Ihre gewünschte Zielgruppe ausgerichtet ist, wie unten dargestellt:

  ![Priorität ein einziges Erlebnis](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **[!DNL Target]Die Priorität von Erlebnissen wird anhand der Reihenfolge (von oben nach unten) ihrer Anzeige in bestimmt.**

  Es ist dabei wichtig, Szenarien zu berücksichtigen, bei denen sich ein Besucher für mehr als eine der Zielgruppen qualifiziert. Wenn Sie beispielsweise über zwei Erlebnisse verfügen: eines für &quot;USA&quot;und eines für &quot;New York&quot;, qualifiziert sich ein Besucher in New York für beide Zielgruppen. Daher müssen Sie sicherstellen, dass das Erlebnis &quot;New York&quot;vor dem Erlebnis &quot;USA&quot;im [!DNL Target] Benutzeroberfläche. Dadurch wird sichergestellt, dass das zielgerichtetere Erlebnis &quot;New York&quot;die höhere Priorität hat, wie im folgenden Beispiel gezeigt:

  ![Priorität NY > USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
