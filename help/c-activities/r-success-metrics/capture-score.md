---
keywords: Ergebniserfassung;Ergebnis
description: Erfahren Sie mehr über die Interaktionsmetrik Ergebniserfassung in Adobe [!DNL Target] zur Berechnung eines aggregierten Wertes basierend auf dem Wert, der den auf der Site besuchten Seiten zugewiesen wird.
title: Was ist die Metrik Ergebniserfassung?
feature: Erfolgsmetriken
exl-id: 3446cdef-7ee0-40dd-bf17-27def56668d4
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 48%

---

# Ergebniserfassung

Die Interaktionsmetrik Ergebniserfassung in [!DNL Adobe Target] berechnet ein aggregiertes Ergebnis basierend auf dem Wert, der den auf der Site besuchten Seiten zugewiesen wird, ab dem Zeitpunkt, zu dem der Besucher die erste Anzeige-Anforderung der Kampagne sieht [!DNL Target].

Im folgenden Beispiel wird gezeigt, wie die Bewertungsinteraktion in einer Kampagne berechnet wird, in der zwei Erlebnisse (mit dem Bild einer Katze und dem Bild eines Hundes) geprüft werden.

![](assets/example_score.png)

In diesem Beispiel wird dem Benutzer zuerst die Katze angezeigt. Angenommen, eine globale [!DNL Target] -Anfrage übergibt einen Seitenergebnis basierend auf dem Wert der Seite. Wenn der Marketingexperte die Seitenzahlinteraktion mit einer mit `**any Target request**` verknüpften Erfolgsmetrik erfasst hat, wird die Besuchszahl bei allen Anforderungen, die nach der Anzeigenanforderung für das Katzenbild gesehen werden, gesammelt.

Die erste Seite fügt 1 zum Ergebnis hinzu, die zweite Seite 0,25, die dritte 0,10 und die vierte 0,10, insgesamt 1,45. Dies kann entweder als Währung oder als Punkte interpretiert werden. Bei einem weiteren Besuch findet der Besucher das Hundebild vor. Der Benutzer hat zwar weniger Seiten besucht, das Ergebnis ist aber mit 2,10 höher als beim anderen Besuch, da der Besucher wertvollere Seiten besucht hat.

Sie können Erwerbskosten und Partnerlinkkosten über AdBoxes und Weiterleitungen mit einbeziehen. Siehe hierzu auch den folgenden Seitenfluss. Beachten Sie, dass in diesem Beispiel beide [!DNL Target]-Anforderungen auf der Artikelseite eine Punktzahl übergeben, die möglicherweise ein bekanntes CPM darstellt.

![](assets/example_score2.png)

## Zuweisen eines Seitenergebnisses

Sie können jeder Seite auf Ihrer Site nach persönlichem Ermessen einen Wert zuweisen. Zum Beispiel lassen sich auf einer Koch-Site möglicherweise auf den Sonderseiten mehr Geld mit Werbung generieren als im Erlebnisbereich. Möglicherweise befinden sich im Sonderbereich wertvollere Artikel als im Erlebnisbereich. Mit der Seitenzahl können Sie eine Bewertung des Gesamtwerts des Besuchs ermitteln, sodass Personen, die mehr Sonderartikel lesen, mehr Punkte erhalten, als jemand, der nur durch die Seiten blättert.

Es gibt zwei Methoden zur Zuweisung eines Ergebnisses zu einer Seite:

* Erstellen Sie in der [!DNL Target]-Anfrage einen Parameter mit dem Namen `mboxPageValue`.

   Beispiel: `('global_mbox', 'mboxPageValue=10');`

   Der angegebene Wert wird dem Ergebnis jedes Mal hinzugefügt, wenn die Seite mit dieser [!DNL Target] -Anforderung angezeigt wird. Wenn mehrere Anforderungen auf der Seite Bewertungswerte enthalten, entspricht das Ergebnis für die Seite der Gesamtsumme aller Anforderungswerte. `mboxPageValue` ist ein reservierter Parameter, der zum Übergeben von Werten in einer Target-Anfrage zum Erfassen eines Interaktionswerts verwendet wird. Es können positive and negative Werte übergeben werden. Die Summe wird am Ende jedes Besuchs berechnet, um das Gesamtergebnis für den Besuch zu errechnen.

* Geben Sie den Parameter `?mboxPageValue=n` in die URL der Seite ein.

   Beispiel: `https://www.mydomain.com?mboxPageValue=5`

   Bei Verwendung dieser Methode wird der angegebene Wert zum Ergebnis für jede [!DNL Target]-Anfrage auf der Seite hinzugefügt. Wenn Sie beispielsweise den Parameter `?mboxPageValue=10`übergeben und es drei [!DNL Target] -Anforderungen auf der Seite gibt, beträgt das Ergebnis für die Seite 30.

>[!NOTE]
>
>Target-Anforderungen, die sich oberhalb der ersten Anzeige-[!DNL Target]-Anforderung der Aktivität befinden, werden nicht in das Ergebnis aufgenommen.

Es empfiehlt sich, Werte in der [!DNL Target] -Anfrage zuzuweisen. Auf diese Weise können Sie die von Ihnen gemessenen Werte in Abhängigkeit vom Inhalt der einzelnen Anforderungen genauer bestimmen.

>[!NOTE]
>
>Zur einfacheren Wartung können Sie die Wertezuweisungen des Seitenergebnisses Ihrer Site in der Datei [!DNL at.js] mit bedingter JavaScript-Logik konfigurieren. So müssen Sie keinen weiteren Code zu Ihren Seiten hinzufügen. Wenden Sie sich an Ihren Berater, wenn Sie weitere Hilfe benötigen.

Sie können auch beide Methoden miteinander kombinieren. Dies könnte jedoch zu einem unerwartet hohen Ergebnis führen. Wenn Sie z. B. drei [!DNL Target]-Anforderungen den Wert 10 und einer vierten Anforderung kein Ergebnis zuweisen und dann den URL-Parameter `?mboxPageValue=5` übergeben, beträgt das Seitenergebnis 50, 30 für die drei Anforderungen mit zugewiesenen Werten, und 5 für jede der vier Anforderungen auf der Seite.

Der Zähler beginnt mit der ersten Anzeigeanforderung, nicht mit der Eintragsanforderung. Wenn Sie beispielsweise die Aktivität auf der Homepage ohne Anzeigeanforderung und dann einen Link auf die Katalogseite mit einer Anzeigeanforderung eingeben, beginnt der Zähler beim Wechsel zur Katalogseite.

Sie können auch negative Werte für Seiten vergeben, die Sie Geld kosten und auf den Besucher keine positive Wirkung haben. Die negativen Werte gehen ebenfalls in das Gesamtergebnis ein. Diese Methode kann für Seiten verwendet werden, die Benutzer von einer Werbung aus erreichen. So können Sie die Höhe des CPC erkennen. Sie eignet sich auch für eine Support- oder Kontaktseite, bei deren Besuch mit einer nachfolgenden Supportanfrage zu rechnen ist.
