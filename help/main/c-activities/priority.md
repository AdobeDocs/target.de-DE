---
keywords: Einstellungen;Priorität
description: Erfahren Sie, wie [!DNL Adobe Target] bestimmt, welche Aktivität (oder Aktivitäten) für eine Seite unterschiedlich bereitgestellt werden soll, je nachdem, welche [!DNL Target] und welche Aktivitätserstellungsfunktion Sie verwenden.
title: Wie weist [!DNL Target] den verschiedenen Aktivitäten Priorität zu?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
TQID: 'https://experienceleague.adobe.com/KSkJ1CDkd4hgwnLQ1RKn8l8r2MDIO-6flcHcdN0c0oQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 7eede3484d524e87127de9147aa786484fc87c7d
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 22%
---
# Priorität {#priority}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie [!DNL Adobe Target] je nach Experience Composer und Typ der verwendeten [!DNL Target]-Anfrage entscheidet, welche Aktivitäten an eine Seite gesendet werden sollen.

>[!ENDSHADEBOX]

[!DNL Adobe Target] bestimmt, welche Aktivität (oder Aktivitäten) für eine Seite bereitgestellt werden soll, je nachdem, welche [!DNL Target] und welche Aktivitätserstellungsfunktion ([**[!UICONTROL Visual Experience Composer (VEC)]**](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md)) Sie verwenden. Die folgende Tabelle fasst die drei Fälle zusammen, die in den folgenden Abschnitten beschrieben werden.

| Szenario | Aktivitäten, die Folgendes bieten können | Zurückgegebener Inhalt |
|---|---|---|
| **[!UICONTROL Nur Visual Experience]** oder **[!UICONTROL Form-Based Experience Composer]** nur mit einer globalen [!DNL Target] | Mehrere | Inhalt aller übereinstimmenden Aktivitäten. Wenn sich Selektoren überschneiden, wird der Inhalt der Aktivität mit der höchsten Priorität angezeigt. |
| **[!UICONTROL Form-Based Experience]** und **[!UICONTROL Visual Experience Composer]** | Mehrere | Wenn eine formularbasierte Aktivität die höchste Priorität hat, werden ihr Inhalt und der Inhalt aller entsprechenden VEC-Aktivitäten angezeigt. Wenn eine VEC-Aktivität die höchste Priorität hat, wird nur der Inhalt aller entsprechenden VEC-Aktivitäten angezeigt. |
| **[!UICONTROL Form-Based Experience Composer]** mit nicht globalen [!DNL Target] | Eins pro Anruf | Inhalt der Matching-Aktivität mit der höchsten Priorität. |

## VEC oder [!UICONTROL Form-Based Experience Composer] mit einer globalen Anfrage {#section_4A0A317DFED345649B58B0CB5B410C8B}

Wenn Ihr Unternehmen ausschließlich VEC verwendet, können Inhalte aus mehreren Aktivitäten für denselben Aufruf zurückgegeben werden. Aktivitäten werden mithilfe des folgenden Entscheidungsflusses bereitgestellt:

1. Der [!DNL Target]-Server-Aufruf erreicht [!DNL Target]. Der Aufruf enthält Informationen zur URL der angeforderten Seite.
1. [!DNL Target] ruft jede Aktivität ab, die auf dieser URL ausgeführt wird. Diese Aktivitäten sind die Kandidaten für die Bereitstellung.
1. [!DNL Target] versucht, den Besucher mit den Kandidatenaktivitäten abzugleichen.

   {{visitor-matching}}

1. Inhalte für alle Aktivitäten und Erlebnisse, mit denen der Besucher übereinstimmt, werden an die Seite zurückgegeben, sodass Inhalte aus mehreren Aktivitäten für denselben Aufruf bereitgestellt werden können.
1. [!DNL Target] vergleicht die [CSS-Selektoren](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md) auf die der Inhalt jeder Aktivität verweist. Wenn die Aktivitäten auf verschiedene Selektoren verweisen, werden alle Inhalte angezeigt.
1. Wenn sich ein Selektor überschneidet oder dupliziert wird, wird der Inhalt der Aktivität mit der höchsten Priorität angezeigt.

   >[!IMPORTANT]
   >
   >[!DNL Target] gibt den Inhalt für alle Aktivitäten auf der Seite zurück, beginnend mit dem Inhalt mit der niedrigsten Priorität, der dann von jeder Aktivität überschrieben wird, von der niedrigsten zur höchsten Priorität. In der Regel führt dies dazu, dass Inhalte mit der höchsten Priorität angezeigt werden. Wenn jedoch eine Aktivität mit niedrigerer Priorität die Struktur des DOM für die Seite ändert, erkennt die Aktivität mit höherer Priorität die Seitenstruktur möglicherweise nicht, sodass der Inhalt mit niedrigerer Priorität angezeigt wird.

1. Wenn mehrere Aktivitäten eine Prioritätsstufe gemeinsam haben, wird ein Tiebreak angewendet. Wenn nur eine der Aktivitäten Audience-Zielgruppenbestimmung hat, wird diese Aktivität angezeigt. Wenn für alle oder keine der Aktivitäten eine Zielgruppenbestimmung gilt, wird die zuerst genehmigte Aktivität angezeigt.
1. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

## [!UICONTROL Form-Based Experience Composer] und VEC {#section_4620253E1CE942DD830724C7822B175F}

Wenn Ihr Unternehmen den [!UICONTROL formularbasierten Experience Composer] *und* VEC verwendet, können Inhalte aus mehreren [!UICONTROL formularbasierten Experience Composer]- und VEC-Aktivitäten bereitgestellt werden. Zuvor konnte nur eine Aktivität aus dem formularbasierten Workflow eine Bereitstellung vornehmen. Die Anzahl der formularbasierten Aktivitäten, die eine Bereitstellung vornehmen können, ist jetzt nicht mehr begrenzt.

Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. Der [!DNL Target]-Server-Aufruf erreicht [!DNL Target]. Der Aufruf enthält Informationen zur [!DNL Target] und zur URL.
1. [!DNL Target] ruft jede Aktivität ab, die in dieser [!DNL Target] ausgeführt wird. Diese Aktivitäten sind die Kandidaten für die Bereitstellung.
1. [!DNL Target] versucht, den Besucher mit den Kandidatenaktivitäten abzugleichen.

   {{visitor-matching}}

1. [!DNL Target] prüft, welche der übereinstimmenden Aktivitäten die höchste Priorität hat und ob diese Aktivität im [!UICONTROL Form-Based Experience Composer] oder in VEC erstellt wurde.
1. Wenn eine formularbasierte Aktivität die höchste Priorität hat, wird ihr Inhalt zusammen mit dem Inhalt aller entsprechenden VEC-Aktivitäten zurückgegeben.
1. Wenn eine VEC-Aktivität die höchste Priorität hat, wird der Inhalt aller passenden VEC-Aktivitäten zurückgegeben, jedoch kein formularbasierter Aktivitätsinhalt.
1. Die Ergebnisse sämtlicher Aktivitäten, die auf der Seite ausgeführt werden, werden in den Berichten gezählt und dargestellt.

**Beispiel**

Es gibt zwei Aktivitäten: eine zielt auf das gebrandete Suchbegriff „Nike“ und die andere auf das nicht gebrandete Keyword „Sneakers“ ab. Die Prioritäten beider Aktivitäten werden überprüft. Wenn die Nike-Aktivität eine höhere Priorität hat, wird ihr Inhalt angezeigt. Wenn die Turnschuh-Aktivität eine höhere Priorität aufweist, so wird der Inhalt dieser Aktivität angezeigt.

Verfügen beide Zielaktivitäten über die gleiche Priorität, wird diejenige angezeigt, die zuletzt aufgerufen wurde. Wenn der Besucher neu auf der Seite ist, wird die zuletzt aktivierte Aktivität angezeigt.

## [!UICONTROL Form-Based Experience Composer] mit nicht globalen Anfragen {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

Wenn Ihr Unternehmen im formularbasierten Composer andere [!DNL Target] als die globale [!DNL Target] verwendet, können pro Aufruf nur Inhalte aus einer Aktivität zurückgegeben werden. Die Aktivitätsbereitstellung wird anhand des folgenden Entscheidungsablaufs bestimmt:

1. Der [!DNL Target]-Server-Aufruf erreicht [!DNL Target]. Der Aufruf enthält Informationen zur [!DNL Target] und zur URL.
1. [!DNL Target] ruft jede Aktivität ab, die in dieser [!DNL Target] ausgeführt wird. Diese Aktivitäten sind die Kandidaten für die Bereitstellung.
1. [!DNL Target] versucht, den Besucher in die Kandidatenaktivität mit der höchsten Priorität einzuordnen.

   {{visitor-matching}}

1. Wenn mehrere Aktivitäten eine Prioritätsstufe gemeinsam haben, wird ein Tiebreak angewendet. Wenn nur eine der Aktivitäten Audience-Zielgruppenbestimmung hat, wird diese Aktivität angezeigt. Wenn für alle oder keine der Aktivitäten eine Zielgruppenbestimmung gilt, wird die zuerst genehmigte Aktivität angezeigt.
1. Inhalte aus dieser einzelnen Aktivität werden an die Seite zurückgegeben.

## Beispiele {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Abhängig von Ihren Einstellungen variieren auch die Prioritätswerte. Sie können die Legacy-Einstellungen von **[!UICONTROL Niedrig]**, **[!UICONTROL Medium]** oder **[!UICONTROL Hoch]** verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren. Weitere Informationen finden Sie unter [Aktivitätseinstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC).

**Zwei Aktivitäten verwenden nur Angebote, die in [!UICONTROL Visual Experience Composer] für verschiedene Selektoren erstellt wurden**

* Aktivität 1: target-global-mbox, selector1, visualExpCompOffer1, Priorität niedrig
* Aktivität 2: target-global-mbox, selector2, visualExpCompOffer2, Priorität hoch

Antwort: visualExpCompOffer1, visualExpCompOffer2

**Zwei Aktivitäten verwenden nur Angebote, die in [!UICONTROL Visual Experience Composer] für denselben Selektor erstellt wurden**

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

>[!VIDEO](https://video.tv.adobe.com/v/3507950?captions=ger)
