---
keywords: Einstellungen;Priorität
description: Erfahren Sie, wie Adobe [!DNL Target] bestimmt, welche Aktivität (oder welche Aktivitäten) je nach welcher [!DNL Target] und welche Funktion zur Erstellung von Aktivitäten Sie verwenden.
title: Funktionsweise [!DNL Target] Weisen Sie verschiedenen Aktivitäten Priorität zu?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 87%

---

# Priorität

Je nachdem, welche Target-Oberfläche und welche Funktion zum Erstellen von Aktivitäten Sie verwenden (Visual Experience Composer oder formularbasierter Composer), bestimmt Target, welche Aktivität (bzw. welche Aktivitäten) für eine Seite anders bereitgestellt werden soll(en).

## Nur Target Standard/Premium Visual Experience Composer oder formularbasierter Composer mit globaler Funktionalität [!DNL Target] Nur Anfrage {#section_4A0A317DFED345649B58B0CB5B410C8B}

Wenn Ihr Unternehmen ausschließlich Target Standard/Premium und den Visual Experience Composer verwendet, können Inhalte von mehreren Aktivitäten für denselben Aufruf zurückgegeben werden. Aktivitäten werden mithilfe des folgenden Entscheidungsflusses bereitgestellt:

1. Der Target-Server-Aufruf kommt mit Informationen zur URL zu Target.
1. Target zieht jede Aktivität, die auf dieser URL ausgeführt wird.
1. Target versucht, dem Besucher Aktivitäten zuzuordnen.

   Wenn sich der Besucher bereits in einem A/B-Test oder Multivarianztest befindet, wird er diesem Test zugeordnet, bis er konvertiert. Wenn er sich zuvor in einer Erlebnisziel-Aktivität befand, muss er erneut zugeordnet werden. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Inhalte für alle Aktivitäten und Erlebnisse, die dem Besucher entsprechen, werden auf der Seite zurückgegeben.
1. Wenn die Inhalte für jede Aktivität auf eine andere  [CSS-Auswahl](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) verweist, werden alle Inhalte angezeigt.

   Wenn es eine Überschneidung oder eine duplizierte CSS-Auswahl gibt, werden die Aktivitätsinhalte mit der höchsten Priorität angezeigt. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

   >[!IMPORTANT]
   >
   >Target gibt den Inhalt für alle Aktivitäten auf der Seite zurück, ausgehend vom Inhalt mit der niedrigsten Priorität, der dann von jeder Aktivität mit zunehmender Priorität überschrieben wird. In den meisten Fällen führt dies dazu, dass der Inhalt mit der höchsten Priorität angezeigt wird. Wenn jedoch eine Aktivität mit niedrigerer Priorität die DOM-Struktur für die Seite ändert, kann es sein, dass die Aktivität mit höherer Priorität die Seitenstruktur nicht erkennt und der Inhalt mit niedrigerer Priorität angezeigt wird. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

1. Wenn mehrere Aktivitäten dieselbe Prioritätsstufe teilen, treten die zwei folgenden Kollisionen auf:

   * Wenn eine Aktivität über eine Zielgruppenansprache verfügt, wird diese Aktivität angezeigt.
   * Wenn alle oder keine Aktivitäten ein Targeting aufweisen, wird die zuerst genehmigte Aktivität angezeigt.

## Formularbasierter Composer in Target Standard/Premium und [!DNL Target] Visual Experience Composer für Standard/Premium {#section_4620253E1CE942DD830724C7822B175F}

>[!NOTE]
>
>Diese Informationen gelten auch für alle laufenden Kampagnen, die in [!DNL Target Classic] erstellt wurden.

Wenn Ihr Unternehmen den formularbasierten Composer und den Visual Experience Composer in Target Standard/Premium verwendet, können Inhalte von mehreren Visual Experience Composer-Aktivitäten, jedoch nur eine Aktivität von Target Classic oder den formularbasierten Arbeitsabläufen, bereitgestellt werden. Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. Der Target-Server-Aufruf kommt mit Informationen zum [!DNL Target] Anfrage und URL.
1. Target Classic und Standard ziehen alle Aktivitäten, die damit ausgeführt werden [!DNL Target] -Anfrage.
1. Target versucht, dem Besucher Aktivitäten zuzuordnen.

   Wenn sich der Besucher bereits in einem A/B-Test oder Multivarianztest befindet, wird er diesem Test zugeordnet, bis er konvertiert. Wenn er sich zuvor in einer Erlebnisziel-Aktivität befand, muss er erneut zugeordnet werden. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Wenn eine formularbasierte Aktivität die höchste Priorität hat, werden diese Aktivitätsinhalte zusammen mit allen übereinstimmenden Aktivitätsinhalten aus Visual Experience Composer-Aktivitäten zurückgegeben.
1. Wenn eine Visual Experience Composer-Aktivität die höchste Priorität hat, werden Inhalte von allen übereinstimmenden Visual Experience Composer-Aktivitäten zurückgegeben, jedoch keine Target Classic- oder formularbasierten Aktivitätsinhalte.

   Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

**Beispiel**

Wenn von zwei Aktivitäten eine auf den Marken-Suchbegriff „Nike“ und die zweite auf den generischen Suchbegriff „Turnschuh“ abzielt, werden die Prioritäten beider Aktivitäten überprüft. Wenn die Nike-Aktivität eine höhere Priorität aufweist, so wird dieser Inhalt angezeigt. Wenn die Turnschuh-Aktivität eine höhere Priorität aufweist, so wird der Inhalt dieser Aktivität angezeigt.

Verfügen beide Zielaktivitäten über die gleiche Priorität, wird diejenige angezeigt, die zuletzt aufgerufen wurde. Wenn der Besucher neu auf der Seite ist, wird die zuletzt aktivierte Aktivität angezeigt.

## Formularbasierter Composer in Target Standard/Premium mit nicht globaler Funktionalität [!DNL Target] Anforderungen {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

>[!NOTE]
>
>Diese Informationen gelten auch für alle laufenden Kampagnen, die in Target Classic erstellt wurden.

Wenn Ihr Unternehmen [!DNL Target] andere Anfragen als die globale [!DNL Target] -Anfrage im formularbasierten Composer können pro Aufruf nur Inhalte von einer Aktivität zurückgegeben werden. Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. Die [!DNL Target] Server-Aufruf wird gesendet [!DNL Target] mit Informationen zu [!DNL Target] Anfrage und URL.
1. [!DNL Target] ruft alle Aktivitäten ab, die in ausgeführt werden. [!DNL Target] -Anfrage.
1. [!DNL Target] versucht, den Besucher der Aktivität mit der höchsten Priorität zuzuordnen.

   Wenn sich der Besucher bereits in einem A/B-Test oder Multivarianztest befindet, wird er diesem Test zugeordnet, bis er konvertiert. Wenn er sich zuvor in einer Erlebnisziel-Aktivität befand, muss er erneut zugeordnet werden. Sind die Zielgruppenregeln erfüllt, fällt der Besucher in diese Aktivitäten und in spezifische Erlebnisse.

1. Wenn mehrere Aktivitäten dieselbe Prioritätsstufe teilen, treten die zwei folgenden Kollisionen auf:

   * Wenn eine Aktivität über eine Zielgruppenansprache verfügt, wird diese Aktivität angezeigt.
   * Wenn alle oder keine Aktivitäten ein Targeting aufweisen, wird die zuerst genehmigte Aktivität angezeigt.

## Beispiele {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Abhängig von Ihren Einstellungen variieren auch die Prioritätswerte. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren. Weitere Informationen finden Sie unter  [Aktivitätseinstellungen](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

**Zwei Target Classic-Kampagnen verwenden nicht globale Target-Anforderungen**

* Kampagne 1: homePageHero, offer1, Priorität hoch
* Kampagne 2: homePageHero, offer2, Priorität niedrig

Antwort: offer1

**Zwei Aktivitäten verwenden nur Angebote, die für unterschiedliche Selektoren im Visual Experience Composer erstellt wurden**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector2, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

**Zwei Aktivitäten verwenden nur Angebote, die für denselben Selektor im Visual Experience Composer erstellt wurden**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector1, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

>[!NOTE]
>
>Dies ist dieselbe Antwort wie im zweiten oben genannten Anwendungsfall, da Target Classic keine Auswahlkollisionen verwaltet. Target Standard erfasst ein solches Verhalten und andere Anwendungsfälle, wenn Selektoren sowohl in DOM als auch visuell kollidieren könnten (dies wird normalerweise auf der Bearbeitungsebene des Erlebnisses oder im Kampagnensimulationsmodus durchgeführt).

**Zwei Aktivitäten verwenden im Visual Experience Composer erstellte Angebote und zwei Target Classic-Kampagnen**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, mittelhoch
* Aktivität 2: target-global-mbox, selector2, visualExpCompOffer2, Priorität niedrig
* Kampagne 1: target-global-mbox, offer1, Priorität hoch
* Kampagne 2: target-global-mbox, offer2, Priorität niedrig

Antwort: offer1, visualExpCompOffer2, visualExpCompOffer1

>[!NOTE]
>
>Für die Reihenfolge kombinierter Antworten gilt: Klassische Inhalte kommen zuerst (wie im Anwendungsfall 1 wird nur eine klassische Antwort bereitgestellt), dann bietet der Visual Experience Composer Antworten, die mit umgekehrter Priorität festgelegt werden.

## Schulungsvideo: Aktivitätseinstellungen (3:02)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
