---
keywords: Priorität;Erlebnis erstellen;Prioritäten;Erlebnis;Zielgruppe;Erlebnisse;Erlebnisse wechseln;Visual Experience Composer
description: Erfahren Sie, wie Besucherinnen und Besucher bei der Weiterentwicklung ihrer Profile in einer [!DNL Adobe Target]Experience [!UICONTROL Targeting](XT)-Aktivität zwischen Erlebnissen wechseln können.
title: Können Besucher in einer Experience Targeting[!UICONTROL -Aktivität zwischen Erlebnissen ]?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
    internal-label: Experience target
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 40%
---
# Wechsel zwischen Erlebnissen in [!UICONTROL Experience Targeting]

Mit [!UICONTROL Erlebnis-Targeting] können Sie steuern, welche Erlebnisse Besuchende im Laufe der Entwicklung ihrer Profile sehen.

Die folgende Liste enthält nur einige Szenarien, in denen sich die Besucherprofile weiterentwickeln können. Möglicherweise möchten Sie auf der Grundlage dieser Änderungen auch andere Inhalte präsentieren:

| Szenario | Details |
|--- |--- |
| Geografischer Standort | Wenn Besucher auf Geschäfts- oder private Reisen gehen, rufen sie Ihre Webseite oder mobile App möglicherweise von unterschiedlichen geografischen Standorten auf. |
| Kundenstatus | Besucher werden unter Umständen als potenzielle Kunden gewertet, bevor sie ein Konto erstellen oder Produkte erwerben. |
| Kategorieaffinität | Die Funktion [Kategorieaffinität](/help/main/c-target/c-visitor-profile/category-affinity.md) in [!DNL Target] erfasst automatisch die Kategorien der Besucheransicht und berechnet dann die Affinität der Besucher für die Kategorie zu Targeting-Zwecken. Besucherinnen und Besucher, die mehrere Artikel auf Ihrer Website zu einem bestimmten Thema angesehen haben, erhalten beispielsweise Inhalte, die mit diesem Thema in Verbindung stehen. |
| Wochentag | Möglicherweise möchten Sie Besuchern kurz vor dem Wochenende Inhalte zu Filmen, Restaurants oder anderen Unterhaltungsmöglichkeiten anzeigen. |

Um diese Funktionen in [!DNL Target] zu verwenden, müssen Sie bei der Arbeit mit Experience Targeting[!UICONTROL -Aktivitäten die folgenden Informationen ]:

* **Die Priorität wird von der Reihenfolge der Erlebnisse gesteuert, von oben nach unten.** Wenn sich ein Besucher für mehr als zwei Zielgruppen qualifiziert, erhält dieser Besucher Inhalte aus dem Erlebnis mit höherer Priorität.
* **Besucher wechseln zwischen Erlebnissen in einer [!UICONTROL Erlebnis-Targeting]-Aktivität, wenn sie sich für die Zielgruppe eines Erlebnisses mit höherer Priorität qualifizieren.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Website-Besuch aus Deutschland wechselte der Besucher zu Erlebnis B (Besucher in Deutschland).

  ![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Besucher wechseln auch zwischen Erlebnissen, wenn sie sich nicht mehr für ihre aktuelle Zielgruppe qualifizieren, sondern sich für ein Erlebnis mit niedrigerer Priorität qualifizieren.**
* **Wenn sich Besucherinnen und Besucher nicht mehr für ihr aktuelles Erlebnis und nicht für ein anderes Erlebnis qualifizieren, werden Standardinhalte angezeigt.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Frankreich auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nachdem Sie Ihre Website aus Frankreich angesehen haben, bleibt dieser Besucher in der ursprünglichen Erfahrung.

  ![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Ein Erlebnis, das auf „Alle Besucher“ ausgerichtet ist, kann als letztes Erlebnis in der [!UICONTROL Erlebnis-Targeting]-Aktivität verwendet werden, um alle Besucher zu „fangen“, die sich für kein anderes Erlebnis qualifiziert haben. Wenn ein Erlebnis, das auf „Alle Besucher“ ausgerichtet ist, nicht das letzte in der Reihenfolge ist, werden andere zielgerichtete Erlebnisse, die niedriger als dieses Erlebnis aufgeführt sind, weiterhin ausgewertet.**

  In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Besuch Ihrer Website aus Deutschland bleibt dieser Besucher in Experience A (US-Besucher).

  ![Priorität USA > Alle Besucher](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  Sollten Sie dies nicht wünschen, können Sie eine neue Zielgruppe erstellen, die explizit als Gegenteil der gewünschten Zielgruppe definiert wurde, wie im folgenden Beispiel gezeigt:

  ![Priorität USA > Nicht USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Mit einer Einzelerlebnis-[!UICONTROL Erlebnis-Targeting]-Aktivität bleiben Besucher in einem Erlebnis, auch wenn sie sich nicht mehr für die Zielgruppe qualifizieren, die sie in dieses Erlebnis versetzt hat.**

  Sollte dies nicht gewünscht werden, können Sie ein weiteres Erlebnis erstellen, das sich an das Gegenteil Ihrer Zielgruppe richtet (beispielsweise „nicht USA“ im Gegensatz zu „USA“).

  Als weitere Option können Sie eine [!UICONTROL A/B-Test]-Aktivität erstellen, die mit 100 % Traffic-Zuordnung auf Ihre gewünschte Zielgruppe ausgerichtet ist, wie unten dargestellt:

  ![Priorität ein einziges Erlebnis](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **Die Priorität von Erlebnissen wird durch ihre Reihenfolge (von oben nach unten) definiert, wie sie in der [!DNL Target] Benutzeroberfläche angezeigt wird.**

  Es ist dabei wichtig, Szenarien zu berücksichtigen, bei denen sich ein Besucher für mehr als eine der Zielgruppen qualifiziert. Wenn Sie beispielsweise zwei Erlebnisse haben: eine für „Vereinigte Staaten“ und eine für „New York“, qualifiziert sich ein Besucher in New York für beide Zielgruppen. Daher müssen Sie sicherstellen, dass das Erlebnis „New York“ vor dem Erlebnis „Vereinigte Staaten“ in der [!DNL Target]-Benutzeroberfläche definiert wird. Dadurch wird sichergestellt, dass das zielgerichtetere Erlebnis „New York“ die höhere Priorität hat, wie im folgenden Beispiel gezeigt:

  ![Priorität NY > USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
