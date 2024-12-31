---
keywords: Ergebniserfassung;Ergebnis
description: Erfahren Sie mehr über die Interaktionsmetrik „Capture Score“ in Adobe [!DNL Target]  die einen aggregierten Wert berechnet, der auf den Werten basiert, die den auf der Website besuchten Seiten zugewiesen wurden.
title: Was ist die Metrik „Capture Score“?
feature: Success Metrics
exl-id: 3446cdef-7ee0-40dd-bf17-27def56668d4
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 48%

---

# Ergebniserfassung

Die Metrik Engagement des Capture Score in [!DNL Adobe Target] berechnet einen aggregierten Wert basierend auf dem Wert, der den auf der Website besuchten Seiten zugewiesen wurde, und zwar ab dem Punkt, an dem der Besucher die erste Anzeige [!DNL Target] Anfrage der Kampagne zum ersten Mal sieht.

Im folgenden Beispiel wird gezeigt, wie die Bewertungsinteraktion in einer Kampagne berechnet wird, in der zwei Erlebnisse (mit dem Bild einer Katze und dem Bild eines Hundes) geprüft werden.

![example_score image](assets/example_score.png)

In diesem Beispiel wird dem Benutzer zuerst die Katze angezeigt. Angenommen, eine globale [!DNL Target]-Anfrage wird basierend auf dem Wert der Seite in einem Seitenwert übergeben. Wenn der Marketing-Experte die Interaktion mit der Seitenanzahl anhand einer Erfolgsmetrik erfasst hat, die mit der `**any Target request**` verknüpft ist, wird der Besuchswert für alle Anfragen kumuliert, die nach der Anzeigeanfrage um das Katzenbild angezeigt werden.

Die erste Seite fügt 1 zum Ergebnis hinzu, die zweite Seite 0,25, die dritte 0,10 und die vierte 0,10, insgesamt 1,45. Dies kann entweder als Währung oder als Punkte interpretiert werden. Bei einem weiteren Besuch findet der Besucher das Hundebild vor. Der Benutzer hat zwar weniger Seiten besucht, das Ergebnis ist aber mit 2,10 höher als beim anderen Besuch, da der Besucher wertvollere Seiten besucht hat.

Sie können Erwerbskosten und Partnerlinkkosten über AdBoxes und Weiterleitungen mit einbeziehen. Siehe hierzu auch den folgenden Seitenfluss. Beachten Sie, dass in diesem Beispiel beide [!DNL Target] auf der Artikelseite einen -Wert übergeben, der möglicherweise eine bekannte CPM darstellt.

![example_score2 Bild](assets/example_score2.png)

## Zuweisen einer Seitenbewertung

Sie können jeder Seite auf Ihrer Site nach persönlichem Ermessen einen Wert zuweisen. Zum Beispiel lassen sich auf einer Koch-Site möglicherweise auf den Sonderseiten mehr Geld mit Werbung generieren als im Erlebnisbereich. Möglicherweise befinden sich im Sonderbereich wertvollere Artikel als im Erlebnisbereich. Mit der Seitenzahl können Sie eine Bewertung des Gesamtwerts des Besuchs ermitteln, sodass Personen, die mehr Sonderartikel lesen, mehr Punkte erhalten, als jemand, der nur durch die Seiten blättert.

Es gibt zwei Methoden zur Zuweisung eines Ergebnisses zu einer Seite:

* Erstellen Sie in der [!DNL Target] einen Parameter namens `mboxPageValue`.

  Beispiel: `('global_mbox', 'mboxPageValue=10');`

  Der angegebene Wert wird jedes Mal zur Punktzahl hinzugefügt, wenn die Seite mit dieser [!DNL Target]-Anfrage angezeigt wird. Wenn mehrere Anfragen auf der Seite Score-Werte enthalten, ist der Score für die Seite die Summe aller Anfragewerte. `mboxPageValue` ist ein reservierter Parameter, der zur Übergabe von Werten in einer Target-Anfrage verwendet wird, um einen Interaktionswert zu erfassen. Es können positive and negative Werte übergeben werden. Die Summe wird am Ende jedes Besuchs berechnet, um das Gesamtergebnis für den Besuch zu errechnen.

* Geben Sie den Parameter `?mboxPageValue=n` in die URL der Seite ein.

  Beispiel: `https://www.mydomain.com?mboxPageValue=5`

  Mit dieser Methode wird der angegebene Wert für jede [!DNL Target] auf der Seite zum Score hinzugefügt. Wenn Sie beispielsweise den Parameter übergeben `?mboxPageValue=10`und es drei [!DNL Target] auf der Seite gibt, lautet der Score für die Seite 30.

>[!NOTE]
>
>Target-Anfragen, die sich oberhalb der ersten Anzeige [!DNL Target] Anfrage der Aktivität befinden, werden nicht in die Bewertung einbezogen.

Best Practice ist es, in der [!DNL Target] Werte zuzuweisen. Auf diese Weise können Sie die von Ihnen gemessenen Werte abhängig vom Inhalt jeder Anfrage präzise festlegen.

>[!NOTE]
>
>Um die Wartung zu vereinfachen, können Sie die Seitenbewertungswertzuweisungen Ihrer Site in der [!DNL at.js] mit einer bedingten JavaScript-Logik konfigurieren. So müssen Sie keinen weiteren Code zu Ihren Seiten hinzufügen. Wenden Sie sich an Ihren Berater, wenn Sie weitere Hilfe benötigen.

Sie können auch beide Methoden miteinander kombinieren. Dies könnte jedoch zu einem unerwartet hohen Ergebnis führen. Wenn Sie beispielsweise jeder von drei [!DNL Target] Anfragen den Wert 10 und einer vierten Anfrage den Wert „Kein Score“ zuweisen und dann den URL-Parameter &quot;`?mboxPageValue=5`&quot; übergeben, beträgt der Seitenwert 50, 30 für die drei Anfragen mit den zugewiesenen Werten und 5 für jede der vier Anfragen auf der Seite.

Der Zähler beginnt mit der ersten Anzeigeanforderung, nicht mit der Eingabeanforderung. Wenn Sie z. B. die Aktivität auf der Homepage eingeben, für die keine Display-Anforderung vorhanden ist, und dann eine Verknüpfung zu einer Katalogseite herstellen, die eine Display-Anforderung enthält, beginnt der Zähler, wenn Sie zur Katalogseite wechseln.

Sie können auch negative Werte für Seiten vergeben, die Sie Geld kosten und auf den Besucher keine positive Wirkung haben. Die negativen Werte gehen ebenfalls in das Gesamtergebnis ein. Diese Methode kann für Seiten verwendet werden, die Benutzer von einer Werbung aus erreichen. So können Sie die Höhe des CPC erkennen. Sie eignet sich auch für eine Support- oder Kontaktseite, bei deren Besuch mit einer nachfolgenden Supportanfrage zu rechnen ist.
