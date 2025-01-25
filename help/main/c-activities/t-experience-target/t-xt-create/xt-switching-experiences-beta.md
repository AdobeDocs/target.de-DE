---
keywords: Priorität;Erlebnis erstellen;Prioritäten;Erlebnis;Zielgruppe;Erlebnisse;Erlebnisse wechseln;Visual Experience Composer
description: Erfahren Sie, wie Besucher bei der Weiterentwicklung ihrer Profile in einer  [!DNL Adobe Target] [!UICONTROL Experience Targeting]XT)-Aktivität zwischen Erlebnissen wechseln können.
title: Können Besucher in einer [!UICONTROL Experience Targeting] Aktivität Erlebnisse wechseln?
feature: Experience Targeting
hide: true
hidefromtoc: true
source-git-commit: 269ab2df7538d7e93774e3687bb931c9aaac27b6
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 43%

---

# Wechsel zwischen Erlebnissen in [!UICONTROL Experience Targeting]

Mit [!UICONTROL Experience Targeting] können Sie steuern, welche Erlebnisse Besucherinnen und Besucher im Zuge der Weiterentwicklung ihrer Profile sehen.

Die folgende Liste enthält nur einige Szenarien, in denen sich die Besucherprofile weiterentwickeln können. Möglicherweise möchten Sie auf der Grundlage dieser Änderungen auch andere Inhalte präsentieren:

| Szenario | Details |
|--- |--- |
| Geografischer Standort | Wenn Besucher auf Geschäfts- oder private Reisen gehen, rufen sie Ihre Webseite oder mobile App möglicherweise von unterschiedlichen geografischen Standorten auf. |
| Kundenstatus | Besucher werden unter Umständen als potenzielle Kunden gewertet, bevor sie ein Konto erstellen oder Produkte erwerben. |
| Kategorieaffinität | Die Funktion [Kategorieaffinität](/help/main/c-target/c-visitor-profile/category-affinity.md) in [!DNL Target] erfasst automatisch die Kategorien der Besucheransicht und berechnet dann die Affinität der Besucher für die Kategorie zu Targeting-Zwecken. Besucherinnen und Besucher, die mehrere Artikel auf Ihrer Website zu einem bestimmten Thema angesehen haben, erhalten beispielsweise Inhalte, die mit diesem Thema in Verbindung stehen. |
| Wochentag | Möglicherweise möchten Sie Besuchern kurz vor dem Wochenende Inhalte zu Filmen, Restaurants oder anderen Unterhaltungsmöglichkeiten anzeigen. |

Um diese Funktionen in [!DNL Target] verwenden zu können, müssen Sie bei der Arbeit mit [!UICONTROL Experience Targeting] Aktivitäten die folgenden Informationen verstehen:

* **Die Priorität ist nach Erlebnissen sortiert, und zwar in absteigender Reihenfolge.** Wenn sich ein Besucher für mehr als zwei Zielgruppen qualifiziert, erhält dieser Besucher Inhalte aus dem Erlebnis mit höherer Priorität.
* **Besucher wechseln zwischen Erlebnissen in einer [!UICONTROL Experience Targeting] Aktivität, wenn sie sich für die Zielgruppe eines Erlebnisses mit höherer Priorität qualifizieren.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Website-Besuch aus Deutschland wechselte der Besucher zu Erlebnis B (Besucher in Deutschland).

  ![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-refresh.png)

* **Besucher wechseln auch zwischen Erlebnissen, wenn sie sich nicht mehr für ihre aktuelle Zielgruppe qualifizieren, sondern sich für ein Erlebnis mit niedrigerer Priorität qualifizieren.**
* **Wenn sich Besucherinnen und Besucher nicht mehr für ihr aktuelles Erlebnis und nicht für ein anderes Erlebnis qualifizieren, werden Standardinhalte angezeigt.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Frankreich auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nachdem Sie Ihre Website aus Frankreich angesehen haben, bleibt dieser Besucher in der ursprünglichen Erfahrung.

  ![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-refresh.png)

* **Ein Erlebnis, das auf „Alle Besucher“ ausgerichtet ist, kann als letztes Erlebnis in der [!UICONTROL Experience Targeting]-Aktivität verwendet werden, um alle Besucher zu „fangen“, die sich für kein anderes Erlebnis qualifiziert haben. Wenn ein Erlebnis, das auf „Alle Besucher“ ausgerichtet ist, nicht das letzte in der Reihenfolge ist, werden andere zielgerichtete Erlebnisse, die niedriger als dieses Erlebnis aufgeführt sind, weiterhin ausgewertet.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Besuch Ihrer Website aus Deutschland bleibt dieser Besucher in Experience A (US-Besucher).

  ![Priorität USA > Alle Besucher](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-refresh.png)

  Sollten Sie dies nicht wünschen, können Sie eine neue Zielgruppe erstellen, die explizit als Gegenteil der gewünschten Zielgruppe definiert wurde, wie im folgenden Beispiel gezeigt:

  ![Priorität USA > Nicht USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/not-us.png)

* **Bei einer [!UICONTROL Experience Targeting]-Aktivität für ein einzelnes Erlebnis bleiben Besucher in einem Erlebnis, auch wenn sie sich nicht mehr für die Zielgruppe qualifizieren, die sie in dieses Erlebnis versetzt hat.**

  Sollte dies nicht gewünscht werden, können Sie ein weiteres Erlebnis erstellen, das sich an das Gegenteil Ihrer Zielgruppe richtet (beispielsweise „nicht USA“ im Gegensatz zu „USA“).

  Als weitere Option können Sie eine [!UICONTROL A/B Test]-Aktivität für Ihre gewünschte Zielgruppe mit 100 % Traffic-Zuordnung erstellen, wie unten dargestellt:

  ![Priorität ein einziges Erlebnis](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-refresh.png)

* **Die Priorität von Erlebnissen wird durch ihre Reihenfolge (von oben nach unten) definiert, wie sie in der [!DNL Target] Benutzeroberfläche angezeigt wird.**

  Es ist dabei wichtig, Szenarien zu berücksichtigen, bei denen sich ein Besucher für mehr als eine der Zielgruppen qualifiziert. Wenn Sie beispielsweise zwei Erlebnisse haben: eine für „Vereinigte Staaten“ und eine für „New York“, qualifiziert sich ein Besucher in New York für beide Zielgruppen. Daher müssen Sie sicherstellen, dass das Erlebnis „New York“ vor dem Erlebnis „Vereinigte Staaten“ in der [!DNL Target]-Benutzeroberfläche definiert wird. Dadurch wird sichergestellt, dass das zielgerichtetere Erlebnis „New York“ die höhere Priorität hat, wie im folgenden Beispiel gezeigt:

  ![Priorität NY > USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-refresh.png)
