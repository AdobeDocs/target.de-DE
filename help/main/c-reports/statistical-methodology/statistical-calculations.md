---
keywords: Berichte; statistische Methode; statistische Berechnungen; Statistiken; Mittel; Konversionsrate; Umsatz pro Besucher; RPV; Konfidenzintervall; Steigerung; Naht-Test; Offline-Berechnungen
description: Erfahren Sie mehr über die statistischen Berechnungen, die in manuellen [!UICONTROL A/B Test] -Aktivitäten in  [!DNL Adobe Target] verwendet werden.
title: Wie kann ich mehr über die statistischen Berechnungen erfahren, die in [!UICONTROL A/B Test] -Aktivitäten verwendet werden?
feature: Reports
exl-id: 5f7377b9-0567-4b6f-8968-4696b2088d0a
source-git-commit: bb95d160940737e23022d70cbe56567f79cbf255
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 2%

---

# Statistische Berechnungen in A/Bn-Tests

In diesem Artikel werden die detaillierten statistischen Berechnungen dokumentiert, die bei manuellen A/Bn-Tests in [!DNL Adobe Target] verwendet werden. Definitionen werden für [!UICONTROL Conversion Rate], [!UICONTROL Confidence Interval of Conversion Rate], [!UICONTROL Lift], [!UICONTROL Confidence Interval for Lift] und [!UICONTROL Confidence] bereitgestellt.

>[!NOTE]
>
>Die Informationen in diesem Artikel ersetzen die PDF-Datei &quot;*Adobe Target Calculations for A/B Testing*&quot;, die zuvor auf dieser Website zum Download verfügbar war.

![Target-Bericht, der die [!UICONTROL Conversion Rate], [!UICONTROL Average Lift and Confidence Interval] und [!UICONTROL Confidence] einer A/B-Test-Aktivität anzeigt.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## Mittlere Leistung

Im folgenden Abschnitt werden die in der vorherigen Abbildung verwendeten Berechnungen erläutert.

### Konversionsrate und Umsatz pro Besucher (RPV)

Die folgende Abbildung zeigt [!UICONTROL Conversion Rate], [!UICONTROL Confidence Interval of Conversion Rate] und die Anzahl der [!UICONTROL Conversions] in einem [!DNL Target] -Bericht. Die erste Zeile zeigt beispielsweise, dass für Erlebnis A: der [!UICONTROL Conversion Rate] 25,81 % mit einem [!UICONTROL Confidence Interval] von ±7,7 % beträgt und 32 Konversionen aufgezeichnet wurden. Da 124 Besucher das Erlebnis gesehen haben, entspricht dies 32/124 = 25,81 %.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

Die Konversionsrate bzw. der Wert **Mittel**, *μ<sub>Einfügen</sub>* für jedes Erlebnis *Ausschnitt* in einem Experiment wird als Verhältnis der Summe der Metrik zur Anzahl der dieser Metrik zugewiesenen Einheiten definiert, *N<sub>Zurück</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

Hier,

* *Y<sub>iν</sub>* ist der Wert der Metrik für jede Einheit *i*, die einem bestimmten Erlebnis *ν* zugewiesen wurde.

* Die Summe der Einheiten *i* hängt von der Wahl der Zählmethode ab.

   * Wenn *[!UICONTROL Visitors]* als Zählmethodologie verwendet wird, ist jede Einheit ein Unique Visitor, der für die Dauer der Aktivität als eindeutiger Teilnehmer an der Aktivität definiert ist.
   * Wenn *[!UICONTROL Visits]* als Zählmethodik verwendet wird, ist jede Einheit ein eindeutiger Besuch, der als eindeutiger Teilnehmer eines Erlebnisses während einer [!DNL Target] Sitzung definiert wird (mit einer eindeutigen `sessionId`). Wenn sich der `sessionId` ändert oder der Besucher den Konversionsschritt erreicht, wird ein neuer Besuch gezählt.
   * Wenn *[!UICONTROL Activity Impressions]* als Zählmethodologie verwendet wird, ist jede Einheit eine eindeutige Impression, die definiert wird als jedes Laden einer beliebigen Seite der Aktivität durch einen Besucher.

## [!UICONTROL Confidence Interval of Mean]/[!UICONTROL Conversion Rate]

Das Konfidenzintervall der Konversionsrate wird intuitiv als Bereich möglicher Konversionsraten definiert, der mit den zugrunde liegenden Daten übereinstimmt.

Beim Ausführen von Experimenten ist die Konversionsrate für ein bestimmtes Erlebnis eine *Schätzung* der Konversionsrate &quot;true&quot;. Zur Quantifizierung der Unsicherheit in dieser Schätzung verwendet [!DNL Target] ein Konfidenzintervall. [!DNL Target] meldet immer ein Konfidenzintervall von 95 %, was bedeutet, dass am Ende 95 % der berechneten Konfidenzintervalle die wahre Konversionsrate des Erlebnisses enthalten.

Ein Konfidenzintervall von 95 % der Konversionsrate *μ<sub>ν</sub>* wird als Wertebereich definiert:

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

wobei der Standardfehler für den Mittelwert als

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

Wird eine unvoreingenommene Schätzung der Standardabweichung der Stichprobe verwendet:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

Wenn es sich bei der Kampagne um eine Konversionsratenkampagne handelt (d. h. die Konversionsmetrik ist binär), reduziert sich der Standardfehler auf:

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## Steigerung

Die folgende Abbildung zeigt [!UICONTROL Lift] und [!UICONTROL Confidence Interval of Lift] in einem [!DNL Target] Bericht. Die Zahl stellt den Durchschnittswert des Bereichs der Steigerungsgrenzen dar, und der Pfeil spiegelt wider, ob die Steigerung positiv oder negativ ist. Der Pfeil wird grau angezeigt, bis die Konfidenz 95 % überschreitet. Nachdem die Konfidenz den Schwellenwert überschritten hat, ist der Pfeil basierend auf einer positiven oder negativen Steigerung grün oder rot.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

Die Steigerung zwischen einem Erlebnis *CTIN* und dem Kontrollerlebnis *CTIL<sub>0</sub>* ist das relative &quot;Delta&quot;in Konversionsraten, definiert als

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

wobei die einzelnen Konversionsraten wie oben definiert sind. Einfach gesagt:

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

Wenn die Konversionsrate des Kontrollerlebnisses *darf<sub>0</sub>* 0 betragen, gibt es keine Steigerung.

## [!DNL Confidence Interval of Lift]

Das Boxplotdiagramm in der Spalte [!UICONTROL Average Lift and Confidence Interval] stellt den Durchschnittswert und 95 % [!UICONTROL Confidence Interval of Lift] dar. Der Boxplot ist grau, wenn es eine Überschneidung des Konfidenzintervalls eines bestimmten Nicht-Kontrollerlebnisses mit dem Konfidenzintervall des Kontrollerlebnisses gibt. Das Boxplot ist grün oder rot, wenn der Bereich des Konfidenzintervalls des jeweiligen Erlebnisses über oder unter dem Konfidenzintervall des Kontrollerlebnisses liegt.

Der Standardfehler der Steigerung zwischen einem Erlebnis *CTIH* und dem Kontrollerlebnis *CTA<sub>0</sub>* wird wie folgt definiert:

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="metric-average"></p>

Anschließend ist das 95% Konfidenzintervall der Steigerung:

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

Diese Berechnung verwendet die Delta-Methode und wird in diesem Dokument ](/help/main/assets/confidence_interval_lift.pdf) ausführlicher als [beschrieben.

## [!UICONTROL Confidence]

Die letzte Spalte zeigt die Konfidenz in einem [!DNL Target] -Bericht an. Die Konfidenz eines Erlebnisses ist eine Wahrscheinlichkeit (als Prozentsatz bezeichnet), ein so extremes Ergebnis zu erzielen wie das, das beobachtet wird, da die Null-Hypothese wahr ist. In Bezug auf p-Werte ist die angezeigte Konfidenz *1 - p-Wert*. Intuitiv bedeutet höhere Konfidenz, dass es weniger wahrscheinlich ist, dass das Kontroll- und Nicht-Kontrollerlebnis über gleiche Konversionsraten verfügt.

In [!DNL Target] wird zwischen dem Testerlebnis und dem Kontrollerlebnis ein zweiseitiger t-test **Welch&#39;s t-test** durchgeführt, um zu testen, ob die Test- und Kontrollerlebnisse identisch sind. Da wir in der Regel nicht wissen, ob die Stichprobengrößen und Varianzen von zwei Gruppen vor dem Ausführen des Experiments identisch sind und [!DNL Target] Ihnen auch ermöglicht, ungleiche Traffic-Prozentsätze an jedes Erlebnis zu senden, gehen wir nicht davon aus, dass die Varianz für jedes Erlebnis gleich ist. So wird Welchs t-Test anstelle des Student-T-Tests gewählt.

Um Welches t-Test durchzuführen, beginnen wir zunächst mit der Berechnung der t-Statistik und der Freiheitsgrade und führen dann einen zweiseitigen t-Test durch, um den p-Wert zu generieren. Schließlich berechnen wir die Konfidenz basierend auf dem p-Wert.

Die *t*-Statistik ist definiert als die Differenz zwischen den Mitteln zweier unabhängiger zufälliger Variablen, *ν* und *ν<sub>0</sub>*, dividiert durch den Standardfehler der Differenz:

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

Wobei *μ<sub>v</sub>* und *μ<sub>v0</sub>* die Mittel von *ν* bzw. *ν<sub>0</sub>* sind und der Standardfehler der Differenz zwischen *μ<sub>v</sub>* und *μ<sub>v0</sub>* wie folgt angegeben wird:

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

Dabei sind *σ<sup>2</sup><sub>v</sub>* und *σ<sup>2</sup><sub>v<sub>0</sub></sub>* die Varianzen zweier Erlebnisse *ν* und *ν<sub>0</sub>* bzw. *N<sub>v</sub>* und *N{1 8}v<sub>0</sub></sub>* sind Beispielgrößen für *ν* und *ν<sub>0</sub>*.<sub>

Für Welch-t-Tests wird der Freiheitsgrad wie folgt berechnet:

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

Und der Grad der Freiheit für *darf* und *darf <sub>0</sub>* wie folgt definiert werden:

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

Anschließend kann der p-Wert aus dem Bereich in den Tails der *t*-Verteilung berechnet werden:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

Schließlich wird die in [!DNL Target] gemeldete Konfidenz wie folgt definiert:

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## Durchführen von Berechnungen offline

Der [heruntergeladene CSV-Bericht](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden.

Laden Sie zur Berechnung dieser statistischen Mengen die Excel-Datei [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) herunter, um den Aktivitätswert einzugeben.
