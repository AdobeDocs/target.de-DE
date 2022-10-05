---
keywords: Berichte; statistische Methode; statistische Berechnungen; Statistiken; Mittel; Konversionsrate; Umsatz pro Besucher; RPV; Konfidenzintervall; Steigerung; Naht-Test; Offline-Berechnungen
description: Hier erfahren Sie mehr über die statistischen Berechnungen, die in manuellen [!UICONTROL A/B-Test] Aktivitäten in [!DNL Adobe Target].
title: Erfahren Sie mehr über die in [!UICONTROL A/B-Test] Aktivitäten?
feature: Reports
source-git-commit: 4baa78ac1119e86002c415f09b9481ad351fdcfc
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 2%

---

# Statistische Berechnungen in A/Bn-Tests

In diesem Artikel werden die detaillierten statistischen Berechnungen dokumentiert, die bei manuellen A/Bn-Tests in [!DNL Adobe Target]. Definitionen werden für [!UICONTROL Konversionsrate], [!UICONTROL Konfidenzintervall der Konversionsrate], [!UICONTROL Steigerung], [!UICONTROL Konfidenzintervall für die Steigerung]und [!UICONTROL Konfidenz].

>[!NOTE]
>
>Die Informationen in diesem Artikel ersetzen die *Adobe Target-Berechnungen für A/B-Tests* PDF-Datei, die zuvor auf dieser Website zum Download verfügbar war.

![Zielbericht mit [!UICONTROL Konversionsrate], [!UICONTROL Durchschnittliche Steigerung und Konfidenzintervall]und [!UICONTROL Konfidenz] einer A/B-Test -Aktivität.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## Mittlere Leistung

Im folgenden Abschnitt werden die in der vorherigen Abbildung verwendeten Berechnungen erläutert.

### Konversionsrate und Umsatz pro Besucher (RPV)-Kampagnen

Die folgende Abbildung zeigt [!UICONTROL Konversionsrate], [!UICONTROL Konfidenzintervall der Konversionsrate]und die Anzahl der [!UICONTROL Konversionen] in [!DNL Target] Bericht. Die erste Zeile zeigt beispielsweise Folgendes für Erlebnis A: die [!UICONTROL Konversionsrate] ist 25,81 % mit einer [!UICONTROL Konfidenzintervall] von ±7,7 % und 32 Konversionen aufgezeichnet wurden. Da 124 Besucher das Erlebnis gesehen haben, entspricht dies 32/124 = 25,81 %.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

Konversionsrate oder **mean**, *μ<sub>ν</sub>* für jedes Erlebnis *ν* in einem Experiment definiert ist als Verhältnis der Summe der Metrik zur Anzahl der Einheiten, die dieser Metrik zugewiesen sind, *N<sub>ν</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

Hier,

* *Y<sub>iν</sub>* der Wert der Metrik für jede Einheit *i*, das einem bestimmten Erlebnis zugewiesen wurde *ν*.

* Summe über Einheiten *i* hängt von der Wahl der Zählmethode ab.

   * Wenn *[!UICONTROL Besucher]* als Zählmethodik verwendet wird, ist jede Einheit ein Unique Visitor, der für die gesamte Aktivitätsdauer als Unique Visitor definiert ist.
   * Wenn *[!UICONTROL Besuche]* als Zählmethodik verwendet wird, ist jede Einheit ein eindeutiger Besuch, der als eindeutiger Teilnehmer an einem Erlebnis während einer [!DNL Target] Sitzung (mit einer eindeutigen `sessionId`). Wenn die `sessionId` ändern oder der Besucher den Konversionsschritt erreicht, wird ein neuer Besuch gezählt.
   * Wenn *[!UICONTROL Aktivitätsimpressionen]* als Zählmethodik verwendet wird, ist jede Einheit eine eindeutige Impression, die definiert wird als jedes Mal, wenn ein Besucher eine Seite der Aktivität lädt.

## [!UICONTROL Konfidenzintervall des Mittelwerts]/[!UICONTROL Konversionsrate]

Das Konfidenzintervall der Konversionsrate wird intuitiv als Bereich möglicher Konversionsraten definiert, der mit den zugrunde liegenden Daten übereinstimmt.

Beim Ausführen von Experimenten ist die Konversionsrate für ein bestimmtes Erlebnis ein *Schätzung* der &quot;true&quot;-Konversionsrate. Quantifizierung der Unsicherheit in dieser Schätzung, [!DNL Target] verwendet ein Konfidenzintervall. [!DNL Target] meldet immer ein Konfidenzintervall von 95 %, was bedeutet, dass langfristig 95 % der berechneten Konfidenzintervalle die wahre Konversionsrate des Erlebnisses enthalten.

Ein Konfidenzintervall von 95 % der Konversionsrate *μ<sub>ν</sub>* wird als Wertebereich definiert:

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

wobei der Standardfehler für den Mittelwert als

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

wenn eine unvoreingenommene Schätzung der Standardabweichung der Stichprobe verwendet wird:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

Beachten Sie, dass bei einer Kampagne mit Konversionsrate (d. h. bei der Konversionsmetrik handelt es sich um eine binäre Kampagne) der Standardfehler auf Folgendes reduziert wird:

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## Steigerung

Die folgende Abbildung zeigt [!UICONTROL Steigerung] und [!UICONTROL Konfidenzintervall der Steigerung] in [!DNL Target] Bericht. Die Zahl stellt den Durchschnittswert des Bereichs der Steigerungsgrenzen dar, und der Pfeil spiegelt wider, ob die Steigerung positiv oder negativ ist. Der Pfeil wird grau angezeigt, bis die Konfidenz 95 % überschreitet. Nachdem die Konfidenz den Schwellenwert überschritten hat, ist der Pfeil basierend auf einer positiven oder negativen Steigerung grün oder rot.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

Die Steigerung zwischen einem Erlebnis  *ν* und das Kontrollerlebnis *ν<sub>0</sub>* ist das relative &quot;Delta&quot;in Konversionsraten, definiert als

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

wobei die einzelnen Konversionsraten wie oben definiert sind. Einfach gesagt:

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

Wenn die Konversionsrate des Kontrollerlebnisses *ν<sub>0</sub>* den Wert 0 hat, ist keine Steigerung vorhanden.

## [!DNL Confidence Interval of Lift]

Das Boxplotdiagramm im [!UICONTROL Durchschnittliche Steigerung und Konfidenzintervall] -Spalte entspricht dem Durchschnittswert und 95 % [!UICONTROL Konfidenzintervall der Steigerung]. Das Boxplotdiagramm ist grau, wenn sich das Konfidenzintervall eines bestimmten Nicht-Kontrollerlebnisses mit dem Konfidenzintervall des Kontrollerlebnisses überschneidet, und grün oder rot, wenn das Konfidenzintervall des jeweiligen Erlebnisses über oder unter dem Konfidenzintervall des Kontrollerlebnisses liegt.

Der Standardfehler der Steigerung zwischen einem Erlebnis  *ν* und das Kontrollerlebnis  *ν<sub>0</sub>* definiert als:

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="metric-average"></p>

Anschließend ist das 95% Konfidenzintervall der Steigerung:

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

Diese Berechnung verwendet die Delta-Methode und wird beschrieben. [Weitere Informationen finden Sie in diesem Dokument .](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL Konfidenz]

Die letzte Spalte zeigt die Konfidenz in einer [!DNL Target] Bericht. Die Konfidenz eines Erlebnisses ist eine Wahrscheinlichkeit (als Prozentsatz bezeichnet), ein Ergebnis zu erzielen, das weniger extrem ist als das tatsächlich beobachtete Ergebnis, da die Null-Hypothese wahr ist. In Bezug auf p-Werte lautet die angezeigte Konfidenz *1 - p-Wert*. Intuitiv bedeutet höhere Konfidenz, dass es weniger wahrscheinlich ist, dass das Kontroll- und Nicht-Kontrollerlebnis über gleiche Konversionsraten verfügt.

In [!DNL Target], einem zweiseitigen **Welch&#39;s t-Test** wird zwischen dem Testerlebnis und dem Kontrollerlebnis ausgeführt, um zu testen, ob die Test- und Kontrollerlebnisse identisch sind. Weil wir normalerweise nicht wissen, ob Stichprobengrößen und Varianzen von zwei Gruppen vor dem Experiment identisch sind, und [!DNL Target] ermöglicht Ihnen auch, ungleiche Traffic-Prozentsätze an jedes Erlebnis zu senden. Wir gehen nicht davon aus, dass die Varianz für jedes Erlebnis gleich ist. So wird Welchs t-Test anstelle des Student-T-Tests gewählt.

Um Welches t-Test durchzuführen, beginnen wir zunächst mit der Berechnung der t-Statistik und der Freiheitsgrade und führen dann einen zweiseitigen t-Test durch, um den p-Wert zu generieren. Schließlich berechnen wir die Konfidenz basierend auf dem p-Wert.

Die *t*-statistic ist definiert als die Differenz der Mittel zweier unabhängiger Zufallsvariablen, *ν* und *ν<sub>0</sub>*, geteilt durch den Standardfehler der Differenz:

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

where *μ<sub>v</sub>* und *μ<sub>v0</sub>* sind die Mittel *ν*  und *ν<sub>0</sub>* bzw. der Standardfehler der Differenz zwischen *μ<sub>v</sub>* und *μ<sub>v0</sub>* werden angegeben durch:

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

where *σ<sup>2</sup><sub>v</sub>* und *σ<sup>2</sup><sub>v<sub>0</sub></sub>* sind die Varianzen von zwei Erlebnissen *ν*  und *ν<sub>0</sub>* bzw. *N<sub>v</sub>* und *N<sub>v<sub>0</sub></sub>* sind Stichprobengrößen für *ν* und *ν<sub>0</sub>* bzw.

Für Welch-t-Tests wird der Freiheitsgrad wie folgt berechnet:

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

und des Freiheitsgrads *ν*  und *ν<sub>0</sub>* werden definiert als:

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

Dann kann der p-Wert aus dem Bereich in den Tails der *t*-distribution:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

Schließlich wurde die in [!DNL Target] definiert als:

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## Durchführen von Berechnungen offline

Der [heruntergeladene CSV-Bericht](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden.

Um diese statistischen Mengen zu berechnen, laden Sie die [Vollständige Vertrauensberechnung](/help/main/assets/complete_confidence_calculator.xlsx) Excel-Datei zur Eingabe des Aktivitätswerts.