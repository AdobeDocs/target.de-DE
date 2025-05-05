---
keywords: Berichte; statistische Methodik; statistische Berechnungen; Statistiken; Mittel; Konversionsrate; Umsatz pro Besucher; RPV; Konfidenzintervall; Steigerung; Welch-T-Test; Offline-Berechnungen
description: Erfahren Sie mehr über die statistischen Berechnungen, die bei manuellen [!UICONTROL A/B Test] in verwendet werden [!DNL Adobe Target].
title: Wie kann ich mehr über die in [!UICONTROL A/B Test] Aktivitäten verwendeten statistischen Berechnungen erfahren?
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
>Die Informationen in diesem Artikel ersetzen die PDF-Datei mit den *Adobe Target-Berechnungen für A/B* Tests, die zuvor auf dieser Website zum Download verfügbar war.

![Target-Bericht, der die [!UICONTROL Conversion Rate], [!UICONTROL Average Lift and Confidence Interval] und [!UICONTROL Confidence] einer A/B-Test-Aktivität ausgibt.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## Durchschnittliche Leistung

Im folgenden Abschnitt werden die in der vorherigen Abbildung verwendeten Berechnungen erläutert.

### Konversionsrate und Umsatz pro Besucher (RPV)-Kampagnen

Die folgende Abbildung zeigt [!UICONTROL Conversion Rate], [!UICONTROL Confidence Interval of Conversion Rate] und die Anzahl der [!UICONTROL Conversions] in einem [!DNL Target]. Die erste Zeile zeigt beispielsweise, dass für Erlebnis A der [!UICONTROL Conversion Rate] bei 25,81 % liegt, wobei ein [!UICONTROL Confidence Interval] von ±7,7 % besteht und 32 Konversionen aufgezeichnet wurden. Da 124 Besucher das Erlebnis gesehen haben, entspricht dies 32/124 = 25,81 %.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

Die Konversionsrate oder **Mittelwert**, *µ<sub></sub>* für jedes Erlebnis ** in einem Experiment wird als Verhältnis der Summe der Metrik zur Anzahl der Einheiten definiert, die dieser Metrik zugewiesen sind, *N<sub></sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

Hier,

* *Y<sub>I</sub>* ist der Wert der Metrik für jede Einheit *i*, die einem bestimmten Erlebnis zugewiesen wurde **.

* Die Summe über den Einheiten *i* hängt von der gewählten Zählmethodik ab.

   * Wenn *[!UICONTROL Visitors]* als Zählmethodik verwendet wird, ist jede Einheit ein Unique Visitor , der als eindeutiger Teilnehmer an der Aktivität für die gesamte Lebensdauer der Aktivität definiert ist.
   * Wenn *[!UICONTROL Visits]* als Zählmethodik verwendet wird, ist jede Einheit ein eindeutiger Besuch, der als eindeutiger Teilnehmer eines Erlebnisses während einer [!DNL Target] Sitzung (mit eindeutigem `sessionId`) definiert ist. Wenn sich die `sessionId` ändert oder der Besucher den Konversionsschritt erreicht, wird ein neuer Besuch gezählt.
   * Wenn *[!UICONTROL Activity Impressions]* als Zählmethodik verwendet wird, ist jede Einheit eine eindeutige Impression, die jedes Mal definiert wird, wenn ein Besucher eine Seite der Aktivität lädt.

## [!UICONTROL Confidence Interval of Mean]/[!UICONTROL Conversion Rate]

Das Konfidenzintervall der Konversionsrate wird intuitiv definiert als Bereich möglicher Konversionsraten, der mit den zugrunde liegenden Daten konsistent ist.

Bei der Durchführung von Experimenten ist die Konversionsrate für ein bestimmtes Erlebnis eine *Schätzung* der „echten“ Konversionsrate. Um die Unsicherheit in dieser Schätzung zu quantifizieren, verwendet [!DNL Target] ein Konfidenzintervall. [!DNL Target] meldet immer ein Konfidenzintervall von 95 %, was bedeutet, dass am Ende 95 % der berechneten Konfidenzintervalle die tatsächliche Konversionsrate des Erlebnisses enthalten.

Ein 95 %-Konfidenzintervall der Konversionsrate *µ<sub></sub>* ist definiert als der Wertebereich:

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

wobei der Standardfehler für den Mittelwert wie folgt definiert ist

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

Wird eine unvoreingenommene Schätzung der Stichprobenstandardabweichung verwendet:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

Handelt es sich bei der Kampagne um eine Kampagne mit Konversionsrate (d. h. die Konversionsmetrik ist binär), wird der Standardfehler wie folgt reduziert:

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## Steigerung

Die folgende Abbildung zeigt [!UICONTROL Lift] und [!UICONTROL Confidence Interval of Lift] in einem [!DNL Target]. Die Zahl stellt den Durchschnitt des Bereichs der Steigerungsgrenzen dar, und der Pfeil gibt an, ob die Steigerung positiv oder negativ ist. Der Pfeil wird grau angezeigt, bis die Konfidenz um 95 % überschritten ist. Nachdem die Konfidenz den Schwellenwert überschritten hat, wird der Pfeil basierend auf einer positiven oder negativen Steigerung grün oder rot angezeigt.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

Die Steigerung zwischen einem Erlebnis *<sub>* und dem Kontrollerlebnis *0</sub>* ist das relative „Delta“ der Konversionsraten, definiert als

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

wobei die einzelnen Umrechnungskurse wie oben definiert sind. Einfacher ausgedrückt:

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

Wenn die Konversionsrate des Kontrollerlebnisses *<sub>0</sub>* 0 beträgt, gibt es keine Steigerung.

## [!DNL Confidence Interval of Lift]

Das Boxplot-Diagramm in der Spalte [!UICONTROL Average Lift and Confidence Interval] stellt den Durchschnittswert und 95 % [!UICONTROL Confidence Interval of Lift] dar. Das Boxplot-Diagramm ist grau, wenn es eine Überschneidung des Konfidenzintervalls eines bestimmten Nicht-Kontrollerlebnisses mit dem Konfidenzintervall des Kontrollerlebnisses gibt. Das Boxplot-Diagramm ist grün oder rot, wenn der Bereich des Konfidenzintervalls eines bestimmten Erlebnisses über oder unter dem Konfidenzintervall des Kontrollerlebnisses liegt.

Der Standardfehler des Anstiegs zwischen einem Erlebnis ** und dem Kontrollerlebnis *<sub>0</sub>* wird wie folgt definiert:

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="metrischer Mittelwert"></p>

Dann beträgt das 95-%-Konfidenzintervall der Steigerung:

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

Diese Berechnung verwendet die „Delta“-Methode und wird [in diesem Dokument ausführlicher beschrieben](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL Confidence]

Die letzte Spalte zeigt die Konfidenz in einem [!DNL Target]. Die Konfidenz eines Erlebnisses ist eine Wahrscheinlichkeit (als Prozentsatz bezeichnet), ein Ergebnis zu erhalten, das so extrem ist wie das beobachtete, wenn die Nullhypothese wahr ist. Im Hinblick auf p-Werte ist die angezeigte Konfidenz *1 - p-Wert*. Eine höhere Konfidenz bedeutet intuitiv, dass die Wahrscheinlichkeit, dass das Kontrollerlebnis und das Nicht-Kontrollerlebnis gleiche Konversionsraten haben, geringer ist.

[!DNL Target] wird zwischen dem Prüferlebnis und dem Kontrollerlebnis ein zweiseitiger **Welch&#39;s t-Test** durchgeführt, um zu testen, ob die Mittel der Prüf- und Kontrollerlebnisse identisch sind. Da wir vor der Durchführung des Experiments normalerweise nicht wissen, ob die Stichprobengrößen und Varianzen zweier Gruppen identisch sind, und [!DNL Target] auch die Übertragung ungleicher Prozentsätze des Traffics an jedes Erlebnis ermöglicht, gehen wir nicht davon aus, dass die Varianz für jedes Erlebnis gleich ist. So wird Welchs t-Test anstelle des Student-t-Tests gewählt.

Um Welchs t-Test durchzuführen, beginnen wir zunächst mit der Berechnung der t-Statistik und der Freiheitsgrade, dann führen wir einen zweiseitigen t-Test durch, um den p-Wert zu erzeugen. Schließlich berechnen wir die Konfidenz auf der Basis des p-Werts.

Die *t*-Statistik ist definiert als die Differenz der Mittelwerte zweier unabhängiger Zufallsvariablen, ** und *<sub>0</sub>*, geteilt durch den Standardfehler der Differenz:

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

Dabei sind *µ<sub>v</sub>* und *µ<sub>v0</sub>* die Mittel für ** bzw. *<sub>0</sub>*, und der Standardfehler der Differenz zwischen *µ<sub>v</sub>* und *<sub>v0</sub>* ergibt sich aus:

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

Dabei sind *<sub><sup>2</sup><sub>v</sub>* und *</sub></sub>*<sup>2</sup><sub>v<sub>0 </sub></sub>*die Varianzen zweier Erlebnisse&#x200B;**bzw.*<sub>0 </sub>*und* NN *v</sub>* und *Nn<sub>v<sub>0sind Stichproben fürgrößen für**&#x200B;bzw.<sub></sub>* 000.

Für Welchs t-Test wird der Freiheitsgrad wie folgt berechnet:

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

Und der Freiheitsgrad für ** und *<sub>0</sub>* wird definiert als:

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

Dann kann der p-Wert aus der Fläche in den Schwänzen der *t*-Verteilung berechnet werden:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

Schließlich wird die in [!DNL Target] gemeldete Konfidenz wie folgt definiert:

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## Durchführen von Berechnungen offline

Der [heruntergeladene CSV-Bericht](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden.

Um diese statistischen Größen zu berechnen, laden Sie die Excel[!DNL Target]Datei [Konfidenzrechner abschließen](/help/main/assets/complete_confidence_calculator.xlsx) herunter, um den Wert der Aktivität einzugeben.
