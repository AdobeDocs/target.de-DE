---
keywords: Einstellungen;Priorität
description: Erfahren Sie mehr [!DNL Adobe Target] bestimmt, welche Aktivität (oder welche Aktivitäten) je nach welcher [!DNL Target] und welche Funktion zur Erstellung von Aktivitäten Sie verwenden.
title: Funktionsweise [!DNL Target] Weisen Sie den verschiedenen Aktivitäten Priorität zu?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: f935b963d8686ca8991544a96720adfc32b1083e
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 33%

---

# Priorität

[!DNL Adobe Target] bestimmt, welche Aktivität (oder welche Aktivitäten) je nach welcher [!DNL Target] und welche Funktion zur Erstellung von Aktivitäten ([[!UICONTROL Visual Experience Composer (VEC)]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md)) verwenden.

## [!DNL Target Standard/Premium] [!UICONTROL Visual Experience Composer] nur oder [!UICONTROL Form-Based Experience Composer] mit einer globalen [!DNL Target] Nur Anfrage {#section_4A0A317DFED345649B58B0CB5B410C8B}

Wenn Ihr Unternehmen [!DNL Target Standard/Premium] und ausschließlich VEC können Inhalte von mehreren Aktivitäten für denselben Aufruf zurückgegeben werden. Aktivitäten werden mithilfe des folgenden Entscheidungsflusses bereitgestellt:

1. Die [!DNL Target] Server-Aufruf wird gesendet [!DNL Target] mit Informationen zur URL.
1. [!DNL Target] ruft alle Aktivitäten ab, die mit dieser URL ausgeführt werden.
1. [!DNL Target] versucht, den Besucher Aktivitäten zuzuordnen.

   Wenn der Besucher bereits in einer [!UICONTROL A/B Test] oder [!UICONTROL Multivariate Test] -Aktivität, werden sie mit dieser Aktivität abgeglichen, bis sie konvertiert werden. Wenn sie sich zuvor in einer [!UICONTROL Experience Targeting] -Aktivität, müssen sie erneut übereinstimmen. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Inhalte für alle Aktivitäten und Erlebnisse, die dem Besucher entsprechen, werden auf der Seite zurückgegeben.
1. Wenn der Inhalt für jede Aktivität auf unterschiedliche [CSS-Selektoren](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337), werden alle Inhalte angezeigt.

   Wenn es eine Überschneidung oder eine duplizierte CSS-Auswahl gibt, werden die Aktivitätsinhalte mit der höchsten Priorität angezeigt. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

   >[!IMPORTANT]
   >
   >[!DNL Target] gibt den Inhalt für alle Aktivitäten auf der Seite zurück, beginnend mit dem Inhalt mit der niedrigsten Priorität, der dann von jeder Aktivität mit der niedrigsten bis zur höchsten Priorität überschrieben wird. Normalerweise führt dies dazu, dass der Inhalt mit der höchsten Priorität angezeigt wird. Wenn jedoch eine Aktivität mit niedrigerer Priorität die DOM-Struktur für die Seite ändert, kann es sein, dass die Aktivität mit höherer Priorität die Seitenstruktur nicht erkennt, sodass der Inhalt mit niedrigerer Priorität angezeigt wird. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

1. Wenn mehrere Aktivitäten die Prioritätsstufe teilen, gibt es zwei Auslöser:

   * Wenn eine Aktivität über eine Zielgruppenansprache verfügt, wird diese Aktivität angezeigt.
   * Wenn alle oder keine Aktivitäten über Targeting verfügen, wird die zuerst genehmigte Aktivität angezeigt.

## [!DNL Target Standard/Premium] [!UICONTROL Form-Based Experience Composer] und [!DNL Target Standard/Premium] [!UICONTROL Visual Experience Composer] {#section_4620253E1CE942DD830724C7822B175F}

>[!NOTE]
>
>Diese Informationen gelten auch für alle laufenden Aktivitäten, die in [!DNL Target Classic].

Wenn Ihr Unternehmen die [!UICONTROL Form-Based Experience Composer] *und* VEC, Inhalt aus mehreren [!UICONTROL Form-Based Experience Composer] und VEC-Aktivitäten bereitstellen können. Zuvor konnte nur eine Aktivität aus dem formularbasierten Workflow bereitgestellt werden. Die Anzahl der formularbasierten Aktivitäten, die bereitgestellt werden können, ist nicht mehr begrenzt.

Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. [!DNL Target] Server-Aufruf wird gesendet [!DNL Target] mit Informationen zu [!DNL Target] Anfrage und URL.
1. [!DNL Target Standard/Premium] ruft alle Aktivitäten ab, die in ausgeführt werden. [!DNL Target] -Anfrage.
1. [!DNL Target] versucht, den Besucher Aktivitäten zuzuordnen.

   Wenn der Besucher bereits in einer [!UICONTROL A/B Test] oder [!UICONTROL Multivariate Test] -Aktivität, stimmen sie mit diesem Test überein, bis sie konvertieren. Wenn sie sich zuvor in einer [!UICONTROL Experience Targeting] -Aktivität, müssen sie erneut übereinstimmen. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Wenn eine formularbasierte Aktivität die höchste Priorität hat, wird dieser Aktivitätsinhalt zusammen mit allen übereinstimmenden Aktivitätsinhalten aus VEC-Aktivitäten zurückgegeben.
1. Wenn eine VEC-Aktivität die höchste Priorität hat, werden Inhalte von allen übereinstimmenden VEC-Aktivitäten zurückgegeben, jedoch keine [!DNL Target Classic] oder formularbasierter Aktivitätsinhalt zurückgegeben wird.

   Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

**Beispiel**

Wenn Sie über zwei Aktivitäten verfügen, eine auf den Marken-Suchbegriff &quot;Nike&quot;und die zweite auf den Markenbegriff &quot;Turnschuhe&quot;ausgerichtet ist, werden die Prioritäten beider Aktivitäten überprüft. Wenn die Nike-Aktivität eine höhere Priorität aufweist, so wird dieser Inhalt angezeigt. Wenn die Turnschuh-Aktivität eine höhere Priorität aufweist, so wird der Inhalt dieser Aktivität angezeigt.

Verfügen beide Zielaktivitäten über die gleiche Priorität, wird diejenige angezeigt, die zuletzt aufgerufen wurde. Wenn der Besucher neu auf der Seite ist, wird die zuletzt aktivierte Aktivität angezeigt.

## [!DNL Target Standard/Premium] [!UICONTROL Form-Based Experience Composer] mit nicht global [!DNL Target] requests {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

>[!NOTE]
>
>Diese Informationen gelten auch für alle laufenden Aktivitäten, die in [!DNL Target Classic].

Wenn Ihr Unternehmen [!DNL Target] andere Anfragen als die globale [!DNL Target] -Anfrage im formularbasierten Composer können pro Aufruf nur Inhalte von einer Aktivität zurückgegeben werden. Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. Die [!DNL Target] Server-Aufruf wird gesendet [!DNL Target] mit Informationen zu [!DNL Target] Anfrage und URL.
1. [!DNL Target] ruft alle Aktivitäten ab, die in ausgeführt werden. [!DNL Target] -Anfrage.
1. [!DNL Target] versucht, den Besucher mit der Aktivität mit der höchsten Priorität abzugleichen.

   Wenn der Besucher bereits in einer [!UICONTROL A/B Test] oder [!UICONTROL Multivariate Test] -Aktivität, werden sie mit dieser Aktivität abgeglichen, bis sie konvertiert werden. Wenn sie sich zuvor in einer [!UICONTROL Experience Targeting] -Aktivität, müssen sie erneut übereinstimmen. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Wenn mehrere Aktivitäten die Prioritätsstufe teilen, gibt es zwei Auslöser:

   * Wenn eine Aktivität über eine Zielgruppenansprache verfügt, wird diese Aktivität angezeigt.
   * Wenn alle oder keine Aktivitäten über Targeting verfügen, wird die zuerst genehmigte Aktivität angezeigt.

## Beispiele {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Abhängig von Ihren Einstellungen variieren auch die Prioritätswerte. Sie können die veralteten Einstellungen von [!UICONTROL Low], [!UICONTROL Medium]oder [!UICONTROL High]oder Sie können genauer unterteilte Prioritäten von 0 bis 999 festlegen. Weitere Informationen finden Sie unter [Aktivitätseinstellungen](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

**Zwei [!DNL Target Classic] -Aktivitäten verwenden nicht globale [!DNL Target] requests**

* Aktivität 1: homePageHero, offer1, Priorität hoch
* Aktivität 2: homePageHero, offer2, Priorität niedrig

Antwort: offer1

**Zwei Aktivitäten verwenden nur Angebote, die in der [!UICONTROL Visual Experience Composer] für verschiedene Selektoren**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector2, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

**Zwei Aktivitäten verwenden nur Angebote, die in der [!UICONTROL Visual Experience Composer] für denselben Selektor**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector1, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

>[!NOTE]
>
>Dies ist die gleiche Antwort wie im zweiten oben genannten Anwendungsfall, da [!DNL Target Classic] hat keine Auswahlkollisionen verarbeitet. [!DNL Target Standard/Premium] erfasst ein solches Verhalten und andere Anwendungsfälle, wenn Selektoren sowohl im DOM als auch visuell kollidieren könnten (in der Regel auf Erlebnis-Editor-Ebene oder im Aktivitätssimulationsmodus).

**Zwei Aktivitäten verwenden Angebote, die in der [!UICONTROL Visual Experience Composer] und zwei [!DNL Target Classic] activities**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, mittelhoch
* Aktivität 2: target-global-mbox, selector2, visualExpCompOffer2, Priorität niedrig
* Aktivität 1: target-global-mbox, offer1, Priorität hoch
* Aktivität 2: target-global-mbox, offer2, Priorität niedrig

Antwort: offer1, visualExpCompOffer2, visualExpCompOffer1

>[!NOTE]
>
>Die Reihenfolge der kombinierten Antworten lautet: [!DNL Target Classic] Inhalt wird zuerst angezeigt. Nur eine [!DNL Target Classic] die Antwort wie in Nutzungsszenario 1 bereitgestellt wird, und [!UICONTROL Visual Experience Composer] bieten Antworten, die nach umgekehrter Priorität geordnet sind.

## Schulungsvideo: Aktivitätseinstellungen (3:02)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
