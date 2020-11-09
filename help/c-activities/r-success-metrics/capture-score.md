---
keywords: capture score;score
description: Die Einsatzmetrik "Ergebniserfassung"berechnet einen aggregierten Wert basierend auf dem Wert, der den auf der Site besuchten Zielgruppen zugewiesen wird, ab dem Zeitpunkt, zu dem der Besucher die Anfrage zur ersten Anzeige der Kampagne anzeigt.
title: Ergebniserfassung
feature: success metrics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 51%

---


# Ergebniserfassung{#capture-score}

The Capture Score engagement metric calculates an aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the campaign&#39;s first display [!DNL Target] request.

Im folgenden Beispiel wird gezeigt, wie die Bewertungsinteraktion in einer Kampagne berechnet wird, in der zwei Erlebnisse (mit dem Bild einer Katze und dem Bild eines Hundes) geprüft werden.

![](assets/example_score.png)

In diesem Beispiel wird dem Benutzer zuerst die Katze angezeigt. Assume that a global [!DNL Target] request passes in a page score based on the value of the page. If the marketer has captured page count engagement on a success metric associated with `**any Target request**`, the visit score accumulates for any request seen after the display request around the cat image.

Die erste Seite fügt 1 zum Ergebnis hinzu, die zweite Seite 0,25, die dritte 0,10 und die vierte 0,10, insgesamt 1,45. Dies kann entweder als Währung oder als Punkte interpretiert werden. Bei einem weiteren Besuch findet der Besucher das Hundebild vor. Der Benutzer hat zwar weniger Seiten besucht, das Ergebnis ist aber mit 2,10 höher als beim anderen Besuch, da der Besucher wertvollere Seiten besucht hat.

Sie können Erwerbskosten und Partnerlinkkosten über AdBoxes und Weiterleitungen mit einbeziehen. Siehe hierzu auch den folgenden Seitenfluss. Notice that, in this example, both [!DNL Target] requests on the article page pass a score, possibly representing a known CPM.

![](assets/example_score2.png)

**Zuweisen eines Seitenergebnisses**

Sie können jeder Seite auf Ihrer Site nach persönlichem Ermessen einen Wert zuweisen. Zum Beispiel lassen sich auf einer Koch-Site möglicherweise auf den Sonderseiten mehr Geld mit Werbung generieren als im Erlebnisbereich. Möglicherweise befinden sich im Sonderbereich wertvollere Artikel als im Erlebnisbereich. Mit der Seitenzahl können Sie eine Bewertung des Gesamtwerts des Besuchs ermitteln, sodass Personen, die mehr Sonderartikel lesen, mehr Punkte erhalten, als jemand, der nur durch die Seiten blättert.

Es gibt zwei Methoden zur Zuweisung eines Ergebnisses zu einer Seite:

* Erstellen Sie in der [!DNL Target] Anforderung einen Parameter namens `mboxPageValue`.

   Beispiel: `('global_mbox', 'mboxPageValue=10');`

   The specified value is added to the score every time the page with that [!DNL Target] request is viewed. Wenn mehrere Anforderungen auf der Seite Ergebniswerte enthalten, entspricht das Ergebnis für die Seite der Gesamtwert aller Anforderungswerte. `mboxPageValue` ist ein reservierter Parameter, der zum Übergeben von Werten in einer Zielgruppe-Anforderung verwendet wird, um eine Interaktionsbewertung zu erfassen. Es können positive and negative Werte übergeben werden. Die Summe wird am Ende jedes Besuchs berechnet, um das Gesamtergebnis für den Besuch zu errechnen.

* Geben Sie den Parameter `?mboxPageValue=n` in die URL der Seite ein.

   Beispiel: `https://www.mydomain.com?mboxPageValue=5`

   Using this method, the specified value is added to the score for each [!DNL Target] request on the page. For example, if you pass the parameter `?mboxPageValue=10`and there are three [!DNL Target] requests on the page, the score for the page is 30.

>[!NOTE]
>
>Zielgruppen, die sich oberhalb der ersten Display- [!DNL Target] Anforderung der Aktivität befinden, werden nicht in das Ergebnis einbezogen.

Best practice is to assign values in the [!DNL Target] request. Auf diese Weise können Sie die Werte, die Sie messen, genau bestimmen, je nach Inhalt der einzelnen Anforderungen.

>[!NOTE]
>
>Zur einfacheren Wartung können Sie die Wertezuweisungen des Seitenergebnisses Ihrer Site in der Datei [!DNL at.js] oder [!DNL mbox.js] mit bedingter JavaScript-Logik konfigurieren. So müssen Sie keinen weiteren Code zu Ihren Seiten hinzufügen. Wenden Sie sich an Ihren Berater, wenn Sie weitere Hilfe benötigen.

Sie können auch beide Methoden miteinander kombinieren. Dies könnte jedoch zu einem unerwartet hohen Ergebnis führen. For example, if you assign a value of 10 to each of three [!DNL Target] requests and no score to a fourth request, then pass the URL parameter `?mboxPageValue=5`, your page score will be 50, 30 for the three requests with assigned values, and then 5 for each of the four requests on the page.

Der Zähler Beginn mit der ersten Anzeigeanforderung, nicht mit der Einstiegsanforderung. Wenn Sie z. B. die Aktivität auf der Homepage ohne Display-Anforderung eingeben und dann mit der Katalogseite, die eine Display-Anforderung enthält, verknüpfen, beginnt der Zähler, wenn Sie zur Katalogseite wechseln.

Sie können auch negative Werte für Seiten vergeben, die Sie Geld kosten und auf den Besucher keine positive Wirkung haben. Die negativen Werte gehen ebenfalls in das Gesamtergebnis ein. Diese Methode kann für Seiten verwendet werden, die Benutzer von einer Werbung aus erreichen. So können Sie die Höhe des CPC erkennen. Sie eignet sich auch für eine Support- oder Kontaktseite, bei deren Besuch mit einer nachfolgenden Supportanfrage zu rechnen ist.
