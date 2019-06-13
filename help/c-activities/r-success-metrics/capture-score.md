---
description: Mit dem Interaktionstyp Ergebniserfassung wird ein kumuliertes Ergebnis auf Grundlage des den auf der Site besuchten Seiten zugewiesenen Wertes ab dem Zeitpunkt errechnet, zu dem der Besucher die Anzeige-Mbox der Kampagne zum ersten Mal anzeigt.
keywords: Ergebniserfassung;Ergebnis
seo-description: Mit dem Interaktionstyp Ergebniserfassung wird ein kumuliertes Ergebnis auf Grundlage des den auf der Site besuchten Seiten zugewiesenen Wertes ab dem Zeitpunkt errechnet, zu dem der Besucher die Anzeige-Mbox der Kampagne zum ersten Mal anzeigt.
seo-title: Ergebniserfassung
solution: Target
subtopic: Erste Schritte
title: Ergebniserfassung
topic: Standard
uuid: 977454ad-da32-449a-a8c9-1f3c75220be6
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Ergebniserfassung{#capture-score}

Mit dem Interaktionstyp Ergebniserfassung wird ein kumuliertes Ergebnis auf Grundlage des den auf der Site besuchten Seiten zugewiesenen Wertes ab dem Zeitpunkt errechnet, zu dem der Besucher die Anzeige-Mbox der Kampagne zum ersten Mal anzeigt.

Im folgenden Beispiel wird gezeigt, wie die Bewertungsinteraktion in einer Kampagne berechnet wird, in der zwei Erlebnisse (mit dem Bild einer Katze und dem Bild eines Hundes) geprüft werden.

![](assets/example_score.png)

In diesem Beispiel wird dem Benutzer zuerst die Katze angezeigt. Wir gehen davon aus, dass eine globale Mbox in die Bewertung auf Grundlage des Wertes auf der Seite einbezogen wird. Wenn der Marketing-Experte die Seitenzahlinteraktion mit einer mit `**any mbox**` verbundenen Erfolgsmetrik erfasst hat, wird die Besuchszahl bei jeder erfassten Mbox-Anfrage hinter der Anzeige-Mbox um das Katzenbild hochgeschaltet.

Die erste Seite fügt 1 zum Ergebnis hinzu, die zweite Seite 0,25, die dritte 0,10 und die vierte 0,10, insgesamt 1,45. Dies kann entweder als Währung oder als Punkte interpretiert werden. Bei einem weiteren Besuch findet der Besucher das Hundebild vor. Der Benutzer hat zwar weniger Seiten besucht, das Ergebnis ist aber mit 2,10 höher als beim anderen Besuch, da der Besucher wertvollere Seiten besucht hat.

Sie können Erwerbskosten und Partnerlinkkosten über AdBoxes und Weiterleitungen mit einbeziehen. Siehe hierzu auch den folgenden Seitenfluss. Beachten Sie, dass in diesem Beispiel beide Mboxes auf der Artikelseite ein Ergebnis erzielen, das möglicherweise einer bekannten CPM entspricht.

![](assets/example_score2.png)

**Zuweisen eines Seitenergebnisses**

Sie können jeder Seite auf Ihrer Site nach persönlichem Ermessen einen Wert zuweisen. Zum Beispiel lassen sich auf einer Koch-Site möglicherweise auf den Sonderseiten mehr Geld mit Werbung generieren als im Erlebnisbereich. Möglicherweise befinden sich im Sonderbereich wertvollere Artikel als im Erlebnisbereich. Mit der Seitenzahl können Sie eine Bewertung des Gesamtwerts des Besuchs ermitteln, sodass Personen, die mehr Sonderartikel lesen, mehr Punkte erhalten, als jemand, der nur durch die Seiten blättert.

Es gibt zwei Methoden zur Zuweisung eines Ergebnisses zu einer Seite:

* Erstellen Sie im Mbox-Code einen Mbox-Parameter mit der Bezeichnung `mboxPageValue`.

   Beispiel: `('global_mbox', 'mboxPageValue=10');`

   Der angegebene Wert wird jedes Mal, wenn die Seite mit dieser Mbox aufgerufen wird, zum Gesamtergebnis hinzugefügt. Wenn mehrere Mboxes auf der Seite Ergebniswerte enthalten, so entspricht das Ergebnis für die Seite dem Gesamtwert aller Mboxes. `mboxPageValue` ist ein reservierter Parameter zur Übergabe von Werten an eine mbox, um ein Interaktionsergebnis zu erfassen. Es können positive and negative Werte übergeben werden. Die Summe wird am Ende jedes Besuchs berechnet, um das Gesamtergebnis für den Besuch zu errechnen.

* Geben Sie den Parameter `?mboxPageValue=n` in die URL der Seite ein.

   Beispiel: `https://www.mydomain.com?mboxPageValue=5`

   Bei Anwendung dieser Methode wird der angegebene Wert zum Ergebnis für jede Mbox auf der Seite hinzugefügt. Wenn Sie zum Beispiel den Parameter `?mboxPageValue=10` eingeben und sich auf der Seite drei Mboxes befinden, beträgt das Ergebnis für die Seite 30.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Mboxes, die sich oberhalb der ersten Anzeige-Mbox der Kampagne befinden, werden im Ergebnis nicht berücksichtigt.

Die Best Practice ist, Werte im Mbox-Code zuzuweisen. So können Sie die gemessenen Werte genauer erfassen - abhängig vom Inhalt jeder mbox.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Zur einfacheren Wartung können Sie die Wertezuweisungen des Seitenergebnisses Ihrer Site in der Datei [!DNL at.js] oder [!DNL mbox.js] mit bedingter JavaScript-Logik konfigurieren. So müssen Sie keinen weiteren Code zu Ihren Seiten hinzufügen. Wenden Sie sich an Ihren Berater, wenn Sie weitere Hilfe benötigen.

Sie können auch beide Methoden miteinander kombinieren. Dies könnte jedoch zu einem unerwartet hohen Ergebnis führen. Wenn Sie beispielsweise den drei Mboxes den Wert 10, einer vierten Mbox kein Ergebnis zuweisen und den URL-Parameter `?mboxPageValue=5` übergeben, wird das Seitenergebnis 50, 30 für die ersten drei Mboxes mit zugewiesenem Wert, und 5 für jede der vier weiteren Mboxes auf der Seite betragen.

Der Zähler beginnt mit der ersten Anzeige-Mbox und nicht mit der Einstieg-Mbox. Wenn Sie also die Kampagne auf der Homepage ohne Display-Mbox beginnen, verknüpfen Sie sie mit einer Katalogseite mit einer Display-Mbox. Der Zähler startet, wenn Sie zur Katalogseite navigieren.

Sie können auch negative Werte für Seiten vergeben, die Sie Geld kosten und auf den Besucher keine positive Wirkung haben. Die negativen Werte gehen ebenfalls in das Gesamtergebnis ein. Diese Methode kann für Seiten verwendet werden, die Benutzer von einer Werbung aus erreichen. So können Sie die Höhe des CPC erkennen. Sie eignet sich auch für eine Support- oder Kontaktseite, bei deren Besuch mit einer nachfolgenden Supportanfrage zu rechnen ist.
