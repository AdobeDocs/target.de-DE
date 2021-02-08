---
keywords: Priorität;Erlebnis erstellen;Prioritäten;Erlebnis;Zielgruppe;Erlebnisse;Erlebnisse wechseln;Visual Experience Composer
description: Erfahren Sie, wie Besucher in einer Adobe Target Experience Targeting (XT)-Aktivität während der Entwicklung ihrer Profil zwischen Erlebnissen wechseln können.
title: Können Besucher Erlebnisse in einer Erlebnis-Targeting-Aktivität wechseln?
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 96%

---


# Wechsel zwischen Erlebnissen im Erlebnis-Targeting

Informationen dazu, wie Besucher bei sich entwickelnden Profilen im Erlebnis-Targeting (XT) zwischen Erlebnissen wechseln können.

>[!NOTE]
>
>**21. September 2017**
>
>Mit der am 21. September 2017 veröffentlichten Version änderte sich in Target die Art und Weise, wie Benutzer in Experience Targeting (XT)-Aktivitäten in Erlebnisse eingebunden werden (Landingpage-Kampagnen in Target Classic). Bei allen neuen und vorhandenen Aktivitäten müssen die Benutzer die Erlebnis-Targeting-Regeln für alle Impressionen erfüllen, damit sie den Erlebnisinhalt weiterhin sehen können und diese Anzeige in Berichten berücksichtigt wird. Wenn sich der Benutzer zuvor nicht mehr für ein Erlebnis qualifiziert hat, wurde weiterhin der Inhalt aus dem letzten Erlebnis angezeigt, für das er sich qualifiziert hatte. Dasselbe galt für die Berücksichtigung in Berichten.
>
>Diese Änderung erfolgte automatisch im Rahmen der Veröffentlichung für alle vorhandenen Aktivitäten und für neue Aktivitäten, die nach der Veröffentlichung erstellt werden. Wenn die vorherige Methode (vor dem 21. September) verwendet werden soll, können Sie mithilfe von Profilskripten Zielgruppen erstellen, sodass ein Benutzer einmal eine Bedingung erfüllen muss, damit er künftig weiterhin in die jeweilige Zielgruppe fällt. Verwenden Sie anschließend diese Zielgruppen für die einzelnen Erlebnisse in der Aktivität.

Mit Erlebnis-Targeting können Sie steuern, welches Erlebnis sich entwickelnden Benutzern angezeigt werden soll. In der folgenden Liste finden Sie einige Beispielszenarien, in denen sich Besucherprofile so entwickeln, dass möglicherweise andere Inhalte angezeigt werden sollen:

| Szenario | Details |
|--- |--- |
| Geografischer Standort | Wenn Besucher auf Geschäfts- oder private Reisen gehen, rufen sie Ihre Webseite oder mobile App möglicherweise von unterschiedlichen geografischen Standorten auf. |
| Kundenstatus | Besucher werden unter Umständen als potenzielle Kunden gewertet, bevor sie ein Konto erstellen oder Produkte erwerben. |
| Kategorieaffinität | Die [Kategorieaffinitätsfunktion](/help/c-target/c-visitor-profile/category-affinity.md) in Target hält automatisch die Kategorien fest, die Benutzer besuchen, und berechnet anschließend zu Targeting-Zwecken die Affinität dieser Kategorien. Besuchern, die sich beispielsweise auf Ihrer Webseite mehrere Artikel zu einem bestimmten Thema angesehen haben, können mit diesem Thema verwandte Inhalte angezeigt werden. |
| Wochentag | Möglicherweise möchten Sie Besuchern kurz vor dem Wochenende Inhalte zu Filmen, Restaurants oder anderen Unterhaltungsmöglichkeiten anzeigen. |

Damit diese Funktionen in [!DNL Target] sinnvoll eingesetzt werden können, müssen für die Arbeit mit XT-Aktivitäten folgende Informationen berücksichtigt werden:

* **Die Priorität ist nach Erlebnissen sortiert, und zwar in absteigender Reihenfolge.** Wenn sich ein Besucher für mehr als zwei Zielgruppen qualifiziert, erhält dieser Besucher Inhalt aus dem Erlebnis mit der höheren Priorität.
* **In einer XT-Aktivität wechseln Besucher zwischen Erlebnissen, wenn sie sich für die Zielgruppe eines Erlebnisses mit höherer Priorität qualifizieren.**

   In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Website-Besuch aus Deutschland wechselte der Besucher zu Erlebnis B (Besucher in Deutschland).

   ![Priorität USA > Deutschland](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Besucher wechseln außerdem zwischen Erlebnissen, wenn sie sich nicht mehr für ihre aktuelle Zielgruppe qualifizieren, dafür aber für ein Erlebnis geringerer Priorität.**
* **Wenn Besucher sich nicht mehr für ihr aktuelles Erlebnis qualifizieren und sich für kein anderes Erlebnis qualifizieren, wird ihnen standardmäßiger Inhalt angezeigt.**

   In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Frankreich auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Besuch Ihrer Website aus Frankreich wird dem Besucher weiterhin das Originalerlebnis angezeigt.

   ![Priorität USA > Deutschland](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Ein Erlebnis, das auf „Alle Besucher“ abzielt, kann als das letzte Erlebnis der entsprechenden Targeting-Aktivität eingesetzt werden, um auch die Besucher zu erfassen, die bei keinem anderen Erlebnis erfasst wurden. Wenn ein Erlebnis, das auf „Alle Besucher“ abzielt, nicht das letzte in der Reihenfolge ist, werden auch andere, niedriger eingestufte zielgerichtete Erlebnisse ausgewertet.**

   In der folgenden Aktivitätseinstellung hat ein Besucher beispielsweise erst aus den USA und dann aus Deutschland auf Ihre Website zugegriffen. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach Besuch Ihrer Website aus Deutschland bleibt der Besucher Teil von Erlebnis A (Besucher in den USA).

   ![Priorität USA > Alle Besucher](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

   Sollten Sie dies nicht wünschen, können Sie eine neue Zielgruppe erstellen, die explizit als Gegenteil der gewünschten Zielgruppe definiert wurde, wie im folgenden Beispiel gezeigt:

   ![Priorität USA > Nicht USA](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Bei einer XT-Aktivität mit nur einem Erlebnis verbleiben Besucher im Erlebnis, selbst wenn sie sich nicht mehr für die Zielgruppe qualifizieren, durch die sie diesem Erlebnis zugeordnet wurden.**

   Sollte dies nicht gewünscht werden, können Sie ein weiteres Erlebnis erstellen, das sich an das Gegenteil Ihrer Zielgruppe richtet (beispielsweise „nicht USA“ im Gegensatz zu „USA“).

   Alternativ können Sie eine A/B-Aktivität erstellen, die sich mit 100-prozentiger Traffic-Zuordnung an Ihre Zielgruppe richtet, wie unten gezeigt:

   ![Priorität ein einziges Erlebnis](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **Die Priorität von Erlebnissen wird anhand der Reihenfolge (von oben nach unten) ihrer Anzeige in Target bestimmt.**

   Es ist dabei wichtig, Szenarien zu berücksichtigen, bei denen sich ein Besucher für mehr als eine der Zielgruppen qualifiziert. Wenn Sie beispielsweise über die beiden Erlebnisse „USA“ und „New York“ verfügen, qualifiziert sich ein Besucher aus New York für beide Zielgruppen. Sie müssen somit darauf achten, dass das Erlebnis „New York“ in der Target-Benutzeroberfläche vor dem Erlebnis „USA“ definiert wird. Somit ist gewährleistet, dass das zielgerichtetere Erlebnis „New York“ die höhere Priorität genießt, siehe Beispiel unten:

   ![Priorität NY > USA](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)

