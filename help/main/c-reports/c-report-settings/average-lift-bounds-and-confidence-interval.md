---
keywords: Target; Berichte; Berichtseinstellungen; Umgebung; Steigerung; Steigerungsgrenze; Varianz; Konfidenz; Steuern
description: Erfahren Sie, wie Adobe- [!DNL Target]  zu interpretieren sind, die Datenpunkte und Visualisierungsdarstellungen enthalten, damit Sie die Steigerungsgrenzen und das Konfidenzniveau Ihrer Aktivitäten besser verstehen können.
title: Wie kann ich die durchschnittliche Steigerung, Steigerungsgrenzen und das Konfidenzintervall anzeigen?
feature: Reports
exl-id: 0453aec1-cca5-462c-8eed-0d40bb4cf323
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 60%

---

# Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall

Berichte enthalten mehrere Datenpunkte und Visualisierungsdarstellungen, die Ihnen dabei helfen, die mit Ihrer [!DNL Adobe Target]-Aktivität verbundenen Steigerungsgrenzen und Konfidenzniveaus zu verstehen, um Ihnen dabei zu helfen, einen Gewinner genauer zu bestimmen.

>[!NOTE]
>
>Diese Funktion ist nur beim Anzeigen von Berichten in [!UICONTROL Table] verfügbar. Diese Funktion steht nicht für Aktivitäten zur Verfügung, die [Analytics als Berichtsquelle verwenden (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Interpretieren der Daten {#section_62C0D7E76F3D49A7B3C371C82AEF27D5}

Die folgende Abbildung zeigt [!UICONTROL Lift Bounds and Confidence Level] Informationen:

![Bericht zum durchschnittlichen Steigerungs- und Konfidenzniveau](/help/main/c-reports/c-report-settings/assets/lift-screenshot-new.png)

Zu den Informationen über Steigerung und Konfidenz in der Reporting-Benutzeroberfläche von [!DNL Target] gehören:

### Steigerung

Die große Anzahl und der Pfeil geben den erwarteten Steigerungswert an. Diese Anzahl entspricht dem Mittelpunkt des Bereichs der Steigerungsgrenzen. Der Pfeil für die erwartete Steigerung wird so lange in Grau angezeigt, bis die Konfidenz 95 % passiert. Nach diesem Schwellenwert wird der Pfeil jeweils in Abhängigkeit einer negativen oder positiven Steigerung in Rot oder Grün angezeigt.

### Limits aufheben

Hierbei handelt es sich um das 95-%-Konfidenzintervall der Steigerung. Es wird als ein Bereich unterhalb der durchschnittlichen Steigerung angezeigt. Ein Beispiel [ Berechnung ](#example) Steigerungsgrenzen finden Sie unten unter „Beispielberechnung“.

### Boxplot-Diagramm

Das Boxplot-Diagramm in der [!DNL Target]-Oberfläche stellt den erwarteten Wert und das 95-%-Konfidenzintervall der betreffenden Erfolgsmetrik dar. Sie können sich dies als eine grafische Methode zum Anzeigen der Informationen zur Steigerung und zu den Steigerungsgrenzen vorstellen.

Es gibt einige wichtige Methoden, [!DNL Target] Ihnen bei der Interpretation der Konfidenzinformationen helfen, darunter die Farbe. Das Diagramm zeigt das Konfidenzintervall eines spezifischen Erlebnisses, das sich mit dem Kontrollkonfidenzintervall überschneidet, in Grau an. Zudem zeigt es das Konfidenzintervall eines spezifischen Erlebnisses, das ober- oder unterhalb des Kontrollkonfidenzintervalls liegt, entsprechend in Grün oder Rot an.

Die Länge des Boxplotdiagramms gibt leicht nachvollziehbar an, wie groß das Konfidenzintervall ist. Wenn Sie mehr Daten in Ihrer Aktivität sammeln, verlagert und ändert sich der Balken. Das Konfidenzintervall ergibt sich aus der Varianz und dem Stichprobenumfang (Anzahl der Besucher). Je kleiner die Varianz und je größer der Stichprobenumfang, desto enger ist Ihr Konfidenzintervall.

### Confidence

Die Konfidenz eines angezeigten Erlebnisses oder Angebots ist eine Wahrscheinlichkeit (ausgedrückt als Prozentsatz), ein Ergebnis zu erhalten, das _weniger extrem_ als das tatsächlich beobachtete Ergebnis ist, _wenn die Nullhypothese wahr ist_ d. h. wenn es keinen Unterschied bei den Konversionsraten zwischen diesem Erlebnis oder Angebot und dem Kontrollerlebnis/Angebot gibt. Im Hinblick auf p-Werte ist diese angezeigte Konfidenz `1 - p-value`. Einfach ausgedrückt: Eine höhere Konfidenz deutet darauf hin, dass die Daten weniger konsistent mit der Annahme sind, dass das Angebot/Erlebnis der Kontrolle und des Nicht-Kontrollbereichs die gleichen Konversionsraten aufweisen.

## Verstehen, wie das Konfidenzintervall für die Steigerung bestimmt wird {#pdf}

Laden Sie die [Konfidenzintervall für Steigerung - PDF](/help/main/assets/confidence_interval_lift.pdf)Datei herunter, um weitere Informationen zu erhalten.

## Wie werden Steigerungsgrenzen berechnet? {#section_1D360781D972483693680BE0F07AEAD1}

Die Steigerungsgrenzen stellen 95-%-Konfidenzintervalle der Steigerung dar, die das spezifische Erlebnis oder Angebot gegenüber dem Kontrollerlebnis oder -angebot aufweist. Grob gesagt weist die tatsächliche Steigerung eine etwa 95%ige Chance auf, sich zwischen diesen Steigerungen zu befinden.

Die Steigerungsgrenzen werden mithilfe der folgenden Formel berechnet:

![lift_diagram image](assets/lift_diagram.png)

Es gibt einige zusätzliche Berechnungen, um zur Eingabe der Steigerungsgrenzen zu gelangen:

* **t-Wert:** Die kritische Statistik für unser 95%-Konfidenzniveau ist 1,96. Weitere Informationen zu [t-Werten finden Sie hier](https://en.wikipedia.org/wiki/T-statistic).
* **Steigerungsvarianz:** Der Standardfehler der Erfolgsmetrik von Erlebnis N und der Standardfehler der Erfolgsmetrik des Kontrollerlebnisses sind zum Ermitteln der Steigerungsvarianz erforderlich, was mithilfe der folgenden Formel (in der Abbildung ist die Erfolgsmetrik eine Konversion) berechnet wird.

  ![lift_variance Bild](assets/lift_variance.png)

* **Konversionsrate/Erfolgsmetrik-Standardfehler:** Der Standardfehler wird mit der folgenden Formel auf die gleiche Weise für Erlebnis N und die Kontrolle berechnet (in der Abbildung ist die Erfolgsmetrik eine Konversion). Informationen über den Standardfehler finden Sie [hier](https://en.wikipedia.org/wiki/Standard_error).

  ![STANDARD_ERROR image](assets/standard_error.png)

  >[!NOTE]
  >
  >Der Standardfehler für Aktivitäten mit Umsatzerfolgsmetriken basiert auf der Stichprobenvarianz des Umsatzes.

## Beispielberechnung {#example}

Im Folgenden finden Sie eine Beispielaktivität mit zwei Erlebnissen und den folgenden Ergebnissen:

| Erlebnis | Besucher | Konversionen | Konversionsrate |
|--- |--- |--- |--- |
| Erlebnis A (Kontrolle) | 219, 328 | 2.466 | 1,12 % |
| Erlebnis B | 218, 362 | 3.040 | 1,39 % |

Anhand unserer Formeln können wir die für die Steigerungsgrenzen erforderlichen Eingaben berechnen.

**Standardfehler für Erlebnis A (Kontrolle)**

![standard_error_a Bild](assets/standard_error_A.png)

**Standardfehler für Erlebnis B**

![standard_error_B Bild](assets/standard_error_B.png)

**Steigerungsvarianz für Erlebnis B**

![lift_variance_B Bild](assets/lift_variance_B.png)

**Steigerungsgrenzen für Erlebnis B**

Erwartete Steigerung für Erlebnis B:

![lift_bounds_B Bild](assets/lift_bounds_B.png)

Daher würden die Steigerungsgrenzen für Erlebnis B wie folgt lauten:

![lift_bounds_B2 Bild](assets/lift_bounds_B2.png)

>[!NOTE]
>
>Erwarten Sie geringfügige Abweichungen zwischen manuellen Berechnungen mit den oben genannten Formeln und den im Bericht angezeigten Zahlen. Diese Unterschiede stammen daher, dass die Seitenaufrufe für manuelle Berechnungen abgerundet werden. Die im [!DNL Target] angezeigte Steigerung basiert auf den genauen Zahlen, die aus der gesamten Interaktion und der Interaktionsanzahl ermittelt wurden. Die Interaktionszahlen können über die API des Performanceberichts abgerufen werden.

## Wann werden die Steigerungsgrenzen nicht angezeigt? {#section_C5622E1E94684DAD937249B51A9E42CC}

In bestimmten Fällen zeigt [!DNL Target] keine Steigerungsgrenzen an:

* Für Aktivitäten, wenn die Gesamtanzahl der Besuche oder Besucher niedriger als 30 ist.
* Für [!UICONTROL Auto-Allocate] Aktivitäten werden keine Steigerungsgrenzen angezeigt, bis ein Erlebnis eine Konfidenz von 60 % erreicht hat.
