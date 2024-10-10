---
keywords: mehrere Zielgruppen;Erlebnisversionen;Erlebnisversionen auswählen
description: Erfahren Sie, wie Sie verschiedene Zielgruppensegmente mit Versionen desselben Erlebnisses in A/B-Aktivitäten ansprechen.
title: Kann ich mehrere Erlebnisversionen in einer A/B-Aktivität verwenden?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: ec35109b5d668a96f7e71149df7c965ce2bf3ceb
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 52%

---

# Verschiedene Erlebniszielgruppen in A/B-Tests

Sie können Versionen desselben Erlebnisses für verschiedene Zielgruppen in [!DNL Adobe Target] A/B-Aktivitäten verwenden. Sie können mehrere Zielgruppen für ein Erlebnis im [!UICONTROL Visual Experience Composer] (VEC) oder im formularbasierten Experience Composer einrichten.

Besucher können bei sich ändernden Profilen zwischen Erlebniszielgruppen wechseln. Besucher bleiben während der Lebensdauer der Aktivität nicht im selben Erlebnis.

Verwenden Sie beispielsweise auf Ihrer Site einen konstanten Entwurf für Seiten oder Produkte und möchten Sie das gleiche Erlebnis für mehrere Zielgruppen bereitstellen (beispielsweise Besucher mit unterschiedlichen Browsersprachen), können Sie mehrere Versionen des gleichen Erlebnisses erstellen. Sie können Englisch und Japanisch sprechenden Besuchern das gleiche Erlebnis bereitstellen, wobei der einzige Unterschied die Sprache ist, in der sie dem Besucher angezeigt wird. Für das Erlebnis werden unabhängig von der Sprache Daten gesammelt, sodass im Bericht die Leistung des Erlebnisses anstatt der Version aufgeführt wird.

Ohne die Möglichkeit zur Einrichtung von Erlebnisversionen müssten Sie (in diesem Beispiel) für jede Sprache eigene Tests einrichten, diese Ergebnisse dann manuell zusammenführen und anschließend versuchen herauszufinden, wie erfolgreich ein einziges Erlebnis sprachübergreifend ist. Die Ergebnisse dieser Vorgehensweise sind weniger genau. Bei einigen Tests sind diese Berechnungen möglicherweise sogar irreführend, da Benutzer randomisiert werden.

Erstellen Sie verschiedene Versionen eines Erlebnisses, erhalten Sie genauere Daten, ohne dazu auf manuelle Berechnungen und Annahmen zurückgreifen zu müssen.

## Szenario

Sie testen zwei Erlebnisse: ein Banner mit Geotargeting im Vergleich zu einem generischen Banner. Das Banner muss für jede Region unterschiedlich sein, aber der allgemeine Test besteht darin zu bestimmen, ob das Geotargeting besser ist als die Anzeige allgemeiner Inhalte. Wenn Sie für jeden Ort ein eigenes Erlebnis einrichten, messen Sie tatsächlich, wie die einzelnen Geos sich vergleichen, anstatt ob Geotargeting bei der Messung anhand des generischen Banners dazu beiträgt, Ihre Erfolgsziele zu erreichen.

In diesem Fall benötigen Sie geografisch spezifische Versionen des Erlebnisses, sodass Sie das Erlebnis mit Geotargeting gegen eine Nicht-Geo-Targeting-Kontrolle testen können.

1. [Erstellen Sie wie gewohnt eine A/B-Aktivität.](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)

   Wählen Sie während der Konfigurierung des Erlebnisses mit mehreren Versionen die Zielgruppen der einzelnen Versionen aus, wie unten dargestellt.

1. Wählen Sie das Erlebnis aus und klicken Sie auf **[!UICONTROL Configure]** > **[!UICONTROL Multiple Audiences]**.

1. Klicken Sie im Bereich Erlebniszielgruppen auf das Symbol **[!UICONTROL Add Audience]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ) und wählen Sie dann die erste Zielgruppe aus. Wiederholen Sie den Vorgang für alle weiteren Zielgruppen.

   Wenn die Zielgruppe noch nicht vorhanden ist, klicken Sie auf [Zielgruppe erstellen](/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558) und richten Sie sie ein.

   Sollte ein Benutzer mehr als einer Zielgruppe zugeordnet werden, werden Inhalte für alle Zielgruppen bereitgestellt, wovon mindestens einer aus der Liste tatsächlich auf der Seite angezeigt wird.

1. Fahren Sie mit der Einrichtung der Aktivität fort.

## Best Practices  

* Wählen Sie Zielgruppen aus, die sich gegenseitig ausschließen. Wenn die Aktivität im VEC erstellt wurde und ein Besucher mit mehr als einer Zielgruppe übereinstimmt, wird der Inhalt für jede Zielgruppe zurückgegeben, wobei der Inhalt für die zuletzt aufgelistete Zielgruppe auf der Seite angezeigt wird.
* Die in der Darstellung festgelegten Aktivitätseintrag-Zielgruppen werden mit den Erlebniszielgruppen mit dem Operator „AND“ kombiniert. Möchte ein Benutzer die Aktivität aufrufen, muss er die Kriterien einer Aktivitätszielgruppe und einer Erlebniszielgruppe erfüllen.
* Fügen Sie die gleichen Zielgruppen als Berichtsegmente hinzu. Auf diese Weise können Sie die Testergebnisse auf der hohen Ebene von Erlebnis A im Vergleich B und auf der unteren Ebene von Erlebnis A im Vergleich B nur für &quot;browser lang ja_JP&quot;anzeigen. Dies funktioniert nur bei [!DNL Target]-basierten Berichten, nicht bei [!DNL Analytics]-basierten Berichten.