---
keywords: Ergebniserfassung;Ergebnis
description: Erfahren Sie mehr über die Interaktionsmetrik „Capture Score“ in Adobe [!DNL Target], die einen aggregierten Wert basierend auf dem Wert berechnet, der den auf der Website besuchten Seiten zugewiesen wurde.
title: Was ist die Metrik „Capture Score“?
feature: Success Metrics
exl-id: 3446cdef-7ee0-40dd-bf17-27def56668d4
TQID: 'https://experienceleague.adobe.com/iqCPEY9x7Lg9TlAhxn8e-B1XOnUfNgUWFdOf8Bw2F3w'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: eb2bfbe8-b0f3-4cc3-ae8d-af79179585eb
    internal-label: Success metrics
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 8c6f23b495228ab930e6649aa2f9e6dae506cae2
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 13%
---
# Ergebniserfassung {#capture-score}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie die Metrik „Interaktionsbewertung erfassen“ den Wert eines Besuchs berechnet und wie Sie einer Seite einen Wert zuweisen.

>[!ENDSHADEBOX]

Die Metrik „Interaktion mit Score erfassen“ in [!DNL Adobe Target] berechnet einen aggregierten Score auf der Grundlage des Werts, der den Seiten zugewiesen wurde, die eine Besucherin oder ein Besucher auf Ihrer Website ansieht. Die Punktzahl beginnt an dem Punkt, an dem der Besucher die erste Anzeige [!DNL Target] Anfrage der Aktivität sieht.

Das folgende Beispiel zeigt, wie die Punktzahl in einer Aktivität berechnet wird, die zwei Erlebnisse testet, eines mit einem Katzenbild und eines mit einem Hundebild.

![Seitenfluss des Katzenerlebnisbesuchs mit einer Bewertung für jede Seite](assets/example_score.png)

In diesem Beispiel sieht der erste Besucher das Katzenerlebnis. Angenommen, eine globale [!DNL Target]-Anfrage wird basierend auf dem Wert der Seite in einem Seitenwert übergeben. Wenn der Marketing-Experte die Interaktion mit der Seitenanzahl anhand einer Erfolgsmetrik erfasst hat, die mit **einer Target-Anfrage** verknüpft ist, wird der Besuchswert für jede Anfrage kumuliert, die nach der Anzeigeanfrage um das Katzenbild angezeigt wird.

Die erste Seite addiert 1 zum Score, die zweite Seite 0,25, die dritte 0,10 und die vierte 0,10, insgesamt 1,45. Diese Summe kann entweder als Währung oder als Punkte interpretiert werden. Bei einem separaten Besuch sieht ein Besucher das Hundeerlebnis. Obwohl dieser Besucher weniger Seiten aufruft, liegt der Wert bei 2,10, was größer ist als der andere Besuch, da der Besucher wertvollere Seiten angesehen hat.

Sie können Erwerbskosten und Partnerlinkkosten über AdBoxes und Weiterleitungen mit einbeziehen. Siehe hierzu auch den folgenden Seitenfluss. In diesem Beispiel übergeben beide [!DNL Target] auf der Artikelseite einen -Wert, der möglicherweise eine bekannte CPM darstellt.

![Seitenfluss mit Akquisitionskosten und Umsatz durch Affiliate-Links als Scores weitergegeben](assets/example_score2.png)

## Zuweisen einer Seitenbewertung

Sie können jeder Seite auf Ihrer Site nach persönlichem Ermessen einen Wert zuweisen. Beispielsweise kann eine Kochseite auf ihren Funktionsartikelseiten Anzeigen für mehr Geld verkaufen als im Erlebnisabschnitt. Die Funktionsartikel sind dann wertvoller als der Abschnitt Erlebnis . Mit einem Seitenwert können Sie einen allgemeinen „Wert“ eines Besuchs entwickeln, sodass eine Person, die mehr Funktionsartikel liest, mehr „Punkte“ erhält als eine Person, die nur die Erlebnisse durchsucht.

Es gibt zwei Methoden zur Zuweisung eines Ergebnisses zu einer Seite:

* Erstellen Sie in der [!DNL Target] einen Parameter namens `mboxPageValue`.

  Beispiel: `('global_mbox', 'mboxPageValue=10');`

  Der angegebene Wert wird jedes Mal zur Punktzahl hinzugefügt, wenn die Seite mit dieser [!DNL Target]-Anfrage angezeigt wird. Wenn mehrere Anfragen auf der Seite Score-Werte enthalten, ist der Score für die Seite die Summe aller Anfragewerte. `mboxPageValue` ist ein reservierter Parameter, der zur Übergabe von Werten in einer [!DNL Target] verwendet wird, um einen Interaktionswert zu erfassen. Es können positive and negative Werte übergeben werden. Die Summe wird am Ende jedes Besuchs berechnet, um die Gesamtbewertung des Besuchs zu ermitteln.

* Übergeben Sie den `?mboxPageValue=n` Parameter in der URL der Seite.

  Beispiel: `https://www.mydomain.com?mboxPageValue=5`

  Der angegebene Wert wird für jede [!DNL Target] auf der Seite zum Score hinzugefügt. Wenn Sie beispielsweise den Parameter `?mboxPageValue=10` übergeben und sich drei [!DNL Target] auf der Seite befinden, hat die Seite einen Wert von 30.

>[!NOTE]
>
>Der Zähler beginnt mit der ersten Anzeigeanforderung der Aktivität, nicht mit der Eingabeanforderung, und [!DNL Target] Anforderungen, die sich oberhalb dieser Anforderung befinden, werden nicht in die Bewertung einbezogen. Wenn Sie z. B. die Aktivität auf der Homepage eingeben, für die keine Display-Anforderung vorhanden ist, und dann eine Verknüpfung zu einer Katalogseite herstellen, die eine Display-Anforderung enthält, beginnt der Zähler, wenn Sie zur Katalogseite wechseln.

Es empfiehlt sich, in der [!DNL Target]-Anfrage Werte zuzuweisen. Mit dieser Methode können Sie die von Ihnen gemessenen Werte abhängig vom Inhalt jeder Anfrage präzise festlegen.

>[!NOTE]
>
>Um die Wartung zu vereinfachen, können Sie die Seitenbewertungswertzuweisungen Ihrer Site in der [!DNL at.js] mit einer bedingten JavaScript-Logik konfigurieren. Durch diesen Ansatz müssen Sie Ihren Seiten keinen weiteren Code hinzufügen. Wenden Sie sich an Ihren Berater, wenn Sie weitere Hilfe benötigen.

Sie können auch beide Methoden miteinander kombinieren. Dies könnte jedoch zu einem unerwartet hohen Ergebnis führen. Sie weisen beispielsweise jeder von drei [!DNL Target] Anfragen den Wert 10 und einer vierten Anfrage keinen Score zu und übergeben dann den URL-Parameter `?mboxPageValue=5`. Der Seitenwert beträgt 50:30 für die drei Anfragen mit zugewiesenen Werten plus 20 für den URL-Parameter (5 für jede der vier Anfragen auf der Seite).

Sie können auch negative Werte für Seiten vergeben, die Sie Geld kosten und auf den Besucher keine positive Wirkung haben. Negative Werte wirken sich auch auf die Gesamtpunktzahl aus. Diese Technik kann auf einer Seite verwendet werden, die Besucher durch eine Anzeige erreichen, damit Sie wissen, wie viel der CPC war. Es kann auch auf einer Support- oder Kontaktseite verwendet werden, auf der Besucher anrufen oder Hilfe anfordern können.
