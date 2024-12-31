---
keywords: Einstellungen;Priorität
description: Erfahren Sie [!DNL Adobe Target]  wie Sie festlegen, welche Aktivität (oder Aktivitäten) für eine Seite je nach  [!DNL Target]  Benutzeroberfläche und der verwendeten Funktion zur Aktivitätserstellung unterschiedlich bereitgestellt werden soll.
title: Wie weist  [!DNL Target]  verschiedenen Aktivitäten Priorität zu?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: be6e45ff301f549eb5be24a65b05c4a9c1cd6089
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 39%

---

# Priorität

[!DNL Adobe Target] bestimmt, welche Aktivität (oder Aktivitäten) für eine Seite bereitgestellt werden soll, je nachdem, welche [!DNL Target] und welche Aktivitätserstellungsfunktion ([[!UICONTROL Visual Experience Composer (VEC)]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md)) Sie verwenden.

## Nur [!UICONTROL Visual Experience Composer] oder nur mit einer globalen [!DNL Target]-Anfrage [!UICONTROL Form-Based Experience Composer] {#section_4A0A317DFED345649B58B0CB5B410C8B}

Wenn Ihr Unternehmen ausschließlich VEC verwendet, können Inhalte aus mehreren Aktivitäten für denselben Aufruf zurückgegeben werden. Aktivitäten werden mithilfe des folgenden Entscheidungsflusses bereitgestellt:

1. Der [!DNL Target]-Server-Aufruf wird mit Informationen zur URL an [!DNL Target] gesendet.
1. [!DNL Target] ruft jede Aktivität ab, die auf dieser URL ausgeführt wird.
1. [!DNL Target] versucht, den Besucher in Aktivitäten einzuordnen.

   Wenn sich der Besucher bereits in einer [!UICONTROL A/B Test]- oder [!UICONTROL Multivariate Test]-Aktivität befindet, wird er bis zur Konvertierung mit dieser Aktivität abgeglichen. Wenn sie sich zuvor in einer [!UICONTROL Experience Targeting]-Aktivität befanden, müssen sie erneut mit ihr übereinstimmen. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Inhalte für alle Aktivitäten und Erlebnisse, die dem Besucher entsprechen, werden auf der Seite zurückgegeben.
1. Wenn der Inhalt für jede Aktivität auf verschiedene [CSS-Selektoren](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) verweist, wird der gesamte Inhalt angezeigt.

   Wenn es eine Überschneidung oder eine duplizierte CSS-Auswahl gibt, werden die Aktivitätsinhalte mit der höchsten Priorität angezeigt. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

   >[!IMPORTANT]
   >
   >[!DNL Target] gibt den Inhalt für alle Aktivitäten auf der Seite zurück, beginnend mit dem Inhalt mit der niedrigsten Priorität, der dann von jeder Aktivität überschrieben wird, von der niedrigsten zur höchsten Priorität. In der Regel führt dies dazu, dass Inhalte mit der höchsten Priorität angezeigt werden. Wenn jedoch eine Aktivität mit niedrigerer Priorität die Struktur des DOM für die Seite ändert, ist es möglich, dass die Aktivität mit höherer Priorität die Seitenstruktur nicht erkennt, sodass der Inhalt mit niedrigerer Priorität angezeigt wird. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

1. Wenn mehrere Aktivitäten die gleiche Prioritätsstufe haben, gibt es zwei Zeitbrecher:

   * Wenn eine Aktivität über eine Zielgruppenansprache verfügt, wird diese Aktivität angezeigt.
   * Wenn alle oder keine Zielgruppe ausgewählt wurde, wird die zuerst genehmigte Aktivität angezeigt.

## [!UICONTROL Form-Based Experience Composer] und [!UICONTROL Visual Experience Composer] {#section_4620253E1CE942DD830724C7822B175F}

Wenn Ihr Unternehmen den [!UICONTROL Form-Based Experience Composer] (*)* VEC verwendet, können Inhalte aus mehreren [!UICONTROL Form-Based Experience Composer]- und VEC-Aktivitäten bereitgestellt werden. Zuvor konnte nur eine Aktivität aus dem formularbasierten Workflow eine Bereitstellung vornehmen. Die Anzahl der formularbasierten Aktivitäten, die eine Bereitstellung vornehmen können, ist jetzt nicht mehr begrenzt.

Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. [!DNL Target] Server-Aufruf wird an [!DNL Target] mit Informationen zur [!DNL Target]-Anfrage und -URL gesendet.
1. [!DNL Target] ruft jede Aktivität ab, die in dieser [!DNL Target] ausgeführt wird.
1. [!DNL Target] versucht, den Besucher in Aktivitäten einzuordnen.

   Wenn sich der Besucher bereits in einer [!UICONTROL A/B Test] oder [!UICONTROL Multivariate Test] Aktivität befindet, sucht er nach dem passenden Element in diesem Test, bis er konvertiert. Wenn sie sich zuvor in einer [!UICONTROL Experience Targeting]-Aktivität befanden, müssen sie erneut mit ihr übereinstimmen. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Wenn eine formularbasierte Aktivität die höchste Priorität hat, wird dieser Aktivitätsinhalt zusammen mit allen übereinstimmenden Aktivitätsinhalten aus VEC-Aktivitäten zurückgegeben.
1. Wenn eine VEC-Aktivität die höchste Priorität hat, werden Inhalte aus allen übereinstimmenden VEC-Aktivitäten zurückgegeben. Es wird jedoch kein formularbasierter Aktivitätsinhalt zurückgegeben.

   Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

**Beispiel**

Bei zwei Aktivitäten, von denen die eine auf das Markensuchbegriff „Nike“ und die andere auf das Nicht-Markenschlüsselwort „Sneakers“ abzielt, werden die Prioritäten beider Aktivitäten überprüft. Wenn die Nike-Aktivität eine höhere Priorität aufweist, so wird dieser Inhalt angezeigt. Wenn die Turnschuh-Aktivität eine höhere Priorität aufweist, so wird der Inhalt dieser Aktivität angezeigt.

Verfügen beide Zielaktivitäten über die gleiche Priorität, wird diejenige angezeigt, die zuletzt aufgerufen wurde. Wenn der Besucher neu auf der Seite ist, wird die zuletzt aktivierte Aktivität angezeigt.

## [!UICONTROL Form-Based Experience Composer] mit nicht-globalen [!DNL Target] {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

Wenn Ihr Unternehmen im formularbasierten Composer andere [!DNL Target] als die globale [!DNL Target] verwendet, können pro Aufruf nur Inhalte aus einer Aktivität zurückgegeben werden. Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. Der [!DNL Target]-Server-Aufruf wird mit Informationen zur [!DNL Target]-Anfrage und -URL an [!DNL Target] gesendet.
1. [!DNL Target] ruft jede Aktivität ab, die in dieser [!DNL Target] ausgeführt wird.
1. [!DNL Target] versucht, den Besucher in die Aktivität mit der höchsten Priorität einzuordnen.

   Wenn sich der Besucher bereits in einer [!UICONTROL A/B Test]- oder [!UICONTROL Multivariate Test]-Aktivität befindet, wird er bis zur Konvertierung mit dieser Aktivität abgeglichen. Wenn sie sich zuvor in einer [!UICONTROL Experience Targeting]-Aktivität befanden, müssen sie erneut mit ihr übereinstimmen. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Wenn mehrere Aktivitäten die gleiche Prioritätsstufe haben, gibt es zwei Zeitbrecher:

   * Wenn eine Aktivität über eine Zielgruppenansprache verfügt, wird diese Aktivität angezeigt.
   * Wenn alle oder keine Zielgruppe ausgewählt wurde, wird die zuerst genehmigte Aktivität angezeigt.

## Beispiele {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Abhängig von Ihren Einstellungen variieren auch die Prioritätswerte. Sie können die Legacy-Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren. Weitere Informationen finden Sie unter [Aktivitätseinstellungen](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

Antwort: offer1

**Zwei Aktivitäten verwenden nur Angebote, die in der [!UICONTROL Visual Experience Composer] für verschiedene Selektoren erstellt wurden**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector2, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

**Zwei Aktivitäten verwenden nur Angebote, die in der [!UICONTROL Visual Experience Composer] für denselben Selektor erstellt wurden**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector1, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

## Schulungsvideo: Aktivitätseinstellungen (3:02)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
