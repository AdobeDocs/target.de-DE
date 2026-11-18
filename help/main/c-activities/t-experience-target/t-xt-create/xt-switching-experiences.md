---
keywords: Priorität;Erlebnis erstellen;Prioritäten;Erlebnis;Zielgruppe;Erlebnisse;Erlebnisse wechseln;Visual Experience Composer
description: Erfahren Sie, wie Besucherinnen und Besucher bei der Weiterentwicklung ihrer Profile in einer [!DNL Adobe Target]Experience [!UICONTROL Targeting] (XT)-Aktivität zwischen Erlebnissen wechseln können.
title: Können Besucher in einer Experience Targeting[!UICONTROL -Aktivität zwischen Erlebnissen &#x200B;]?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
TQID: 'https://experienceleague.adobe.com/4bBukCristluFUClhewMcSsNMTPjLjXEqM1QyyropKU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
    internal-label: Experience target
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: aaa094f4f36b6088ca180637d8054b6d5ff59d60
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 20%
---
# Wechsel zwischen Erlebnissen in [!UICONTROL Experience Targeting] {#switching-experiences}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie die Priorität in einer **[!UICONTROL Erlebnis-Targeting]**-Aktivität funktioniert und wann Besucher im Zuge der Weiterentwicklung ihrer Profile zwischen Erlebnissen wechseln.

>[!ENDSHADEBOX]

Mit **[!UICONTROL Erlebnis-Targeting]** können Sie steuern, welche Erlebnisse Besuchende im Laufe der Entwicklung ihrer Profile sehen. Das Profil eines Besuchers kann sich auf verschiedene Weise ändern. Möglicherweise möchten Sie auf der Grundlage dieser Änderungen andere Inhalte präsentieren. In der folgenden Tabelle sind einige Beispiele aufgeführt:

| Szenario | Details |
|--- |--- |
| Geografischer Standort | Wenn Besucher auf Geschäfts- oder private Reisen gehen, rufen sie Ihre Webseite oder mobile App möglicherweise von unterschiedlichen geografischen Standorten auf. |
| Kundenstatus | Besucher werden unter Umständen als potenzielle Kunden gewertet, bevor sie ein Konto erstellen oder Produkte erwerben. |
| Kategorieaffinität | Die [Kategorieaffinität](/help/main/c-target/c-visitor-profile/category-affinity.md) in [!DNL Target] erfasst automatisch die Kategorien, die Besucher anzeigen, und berechnet dann die Affinität der Besucher für jede Kategorie zu Targeting-Zwecken. Besucherinnen und Besucher, die mehrere Artikel auf Ihrer Website zu einem bestimmten Thema angesehen haben, erhalten beispielsweise Inhalte, die mit diesem Thema in Verbindung stehen. |
| Wochentag | Möglicherweise möchten Sie Besuchern kurz vor dem Wochenende Inhalte zu Filmen, Restaurants oder anderen Unterhaltungsmöglichkeiten anzeigen. |

Um diese Funktionen in [!DNL Target] zu verwenden, müssen Sie bei der Arbeit mit Experience Targeting **[!UICONTROL -Aktivitäten die folgenden Informationen]**.

## Bereitstellung von Besuchern {#how-visitors-are-served}

Die Reihenfolge der Erlebnisse in der [!DNL Target]-Benutzeroberfläche von oben nach unten steuert ihre Priorität, definieren Sie also das zielgerichtetere Erlebnis vor dem umfassenderen. Die folgende Tabelle fasst zusammen, was Besucherinnen und Besucher in den einzelnen Situationen sehen.

| Situation | Was der Besucher sieht |
|--- |--- |
| Der Besucher qualifiziert sich für mehr als eine Zielgruppe. | Der Inhalt des Erlebnisses, das die höhere Priorität hat. |
| Der Besucher beginnt damit, sich für die Zielgruppe eines Erlebnisses mit höherer Priorität zu qualifizieren. | Der Besucher wechselt zum Erlebnis mit höherer Priorität. |
| Der Besucher qualifiziert sich nicht mehr für die aktuelle Zielgruppe, sondern für ein Erlebnis mit niedrigerer Priorität. | Der Besucher wechselt zum Erlebnis mit niedrigerer Priorität. |
| Der Besucher qualifiziert sich nicht mehr für das aktuelle Erlebnis und nicht mehr für ein anderes Erlebnis. | Standardinhalt. |
| Der Besucher hat sich für kein anderes Erlebnis qualifiziert, und das letzte Erlebnis ist auf „Alle Besucher“ ausgerichtet. | Das Erlebnis „Alle Besucher“. Dieses Erlebnis „fängt“ die Besucher, die sich für kein anderes Erlebnis qualifiziert haben. |
| Ein Erlebnis, das auf „Alle Besucher“ ausgerichtet ist, ist nicht das letzte in der Reihenfolge. | Die zielgerichteten Erlebnisse, die niedriger als das Erlebnis „Alle Besucher“ aufgelistet sind, werden weiterhin ausgewertet. |
| Die Aktivität verfügt über ein einzelnes Erlebnis, und der Besucher qualifiziert sich nicht mehr für seine Zielgruppe. | Der Besucher verbleibt im Erlebnis. |

## Beispiele {#examples}

Die folgenden Beispiele veranschaulichen diese Situationen.

### Priorität: New York und Vereinigte Staaten

Wenn Sie zwei Erlebnisse haben, eine für „Vereinigte Staaten“ und eine für „New York“, qualifiziert sich ein Besucher in New York für beide Zielgruppen. Daher müssen Sie in der [!DNL Target] Benutzeroberfläche das Erlebnis „New York“ vor dem Erlebnis „Vereinigte Staaten“ definieren. Dadurch wird sichergestellt, dass das zielgerichtetere Erlebnis „New York“ die höhere Priorität hat, wie im folgenden Beispiel gezeigt:

![Priorität NY > USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-refresh.png)

### Wechsel zu einem Erlebnis mit höherer Priorität: USA zu Deutschland

Im folgenden Aktivitäts-Setup hat ein Besucher Ihre Website aus den USA aufgerufen, ist dann nach Deutschland gereist und hat Ihre Website ein zweites Mal besucht. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Website-Besuch aus Deutschland wechselte der Besucher zu Erlebnis B (Besucher in Deutschland).

![Priorität USA > Deutschland](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-refresh.png)

### Verlassen des Publikums: USA nach Frankreich

Bei der folgenden Aktivitätseinrichtung hat ein Besucher Ihre Website aus den USA aufgerufen, ist dann nach Frankreich gereist und hat Ihre Website ein zweites Mal besucht. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nachdem Sie Ihre Website aus Frankreich angesehen haben, bleibt dieser Besucher in der ursprünglichen Erfahrung.

![Priority US > Deutschland, Besucher aus Frankreich](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-refresh.png)

### Erlebnis für alle Besucher

Im folgenden Aktivitäts-Setup hat ein Besucher Ihre Website aus den USA aufgerufen, ist dann nach Deutschland gereist und hat Ihre Website ein zweites Mal besucht. Während des ersten Besuchs qualifizierte er sich für Erlebnis A (Besucher in den USA). Nach dem Besuch Ihrer Website aus Deutschland bleibt dieser Besucher in Experience A (US-Besucher).

![Priorität USA > Alle Besucher](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-refresh.png)

Sollten Sie dies nicht wünschen, können Sie eine neue Zielgruppe erstellen, die explizit als Gegenteil der gewünschten Zielgruppe definiert wurde, wie im folgenden Beispiel gezeigt:

![Priorität USA > Nicht USA](/help/main/c-activities/t-experience-target/t-xt-create/assets/not-us.png)

### Aktivität mit einem Erlebnis

Mit einer Einzelerlebnis-**[!UICONTROL (Erlebnis-Targeting]**-Aktivität bleiben Besucher in einem Erlebnis, auch wenn sie sich nicht mehr für die Zielgruppe qualifizieren, die sie in dieses Erlebnis versetzt hat. Wenn dies nicht wünschenswert ist, können Sie ein weiteres Erlebnis erstellen, das auf die inverse Zielgruppe ausgerichtet ist (z. B. „Nicht die Vereinigten Staaten“ im Gegensatz zu „die Vereinigten Staaten„). Als weitere Option können Sie eine **[!UICONTROL A/B-Test]**-Aktivität erstellen, die mit 100 % Traffic-Zuordnung auf Ihre gewünschte Zielgruppe ausgerichtet ist, wie im folgenden Beispiel gezeigt:

![Priorität ein einziges Erlebnis](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-refresh.png)
