---
keywords: Target; Berichte; Berichtseinstellungen; Umgebung; Steigerung; Steigerungsgrenze; Varianz; Konfidenz; Steuern
description: Erfahren Sie, wie Sie Adobe [!DNL Target] berichte interpretieren, die Datenpunkte und Visualisierungsdarstellungen enthalten, damit Sie die Steigerungsgrenzen und das Konfidenzniveau Ihrer Aktivitäten besser verstehen können.
title: Wie kann ich die durchschnittliche Steigerung, die Steigerungsgrenzen und das Konfidenzintervall anzeigen?
feature: Reports
exl-id: 0453aec1-cca5-462c-8eed-0d40bb4cf323
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 60%

---

# Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall

Berichte enthalten verschiedene Datenpunkte und Visualisierungsdarstellungen, die Ihnen helfen, die Steigerungsgrenzen und das Konfidenzniveau zu verstehen, die mit Ihrer [!DNL Adobe Target] -Aktivität verknüpft sind, um einen Gewinner genauer zu bestimmen.

>[!NOTE]
>
>Diese Funktion ist nur verfügbar, wenn Berichte in der Ansicht [!UICONTROL Table] angezeigt werden. Diese Funktion steht nicht für Aktivitäten zur Verfügung, die [Analytics als Berichtsquelle verwenden (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Interpretieren der Daten {#section_62C0D7E76F3D49A7B3C371C82AEF27D5}

Die folgende Abbildung zeigt [!UICONTROL Lift Bounds and Confidence Level] Informationen:

![Bericht zum durchschnittlichen Steigerungs- und Konfidenzniveau](/help/main/c-reports/c-report-settings/assets/lift-screenshot-new.png)

Zu den Steigerungs- und Konfidenzinformationen in der Berichterstellungs-Benutzeroberfläche von [!DNL Target] gehören:

### Steigerung

Die große Anzahl und der Pfeil geben den erwarteten Steigerungswert an. Diese Anzahl entspricht dem Mittelpunkt des Bereichs der Steigerungsgrenzen. Der Pfeil für die erwartete Steigerung wird so lange in Grau angezeigt, bis die Konfidenz 95 % passiert. Nach diesem Schwellenwert wird der Pfeil jeweils in Abhängigkeit einer negativen oder positiven Steigerung in Rot oder Grün angezeigt.

### Steigerungsgrenzen

Hierbei handelt es sich um das 95-%-Konfidenzintervall der Steigerung. Es wird als ein Bereich unterhalb der durchschnittlichen Steigerung angezeigt. Unter [Beispielberechnung](#example) unten finden Sie ein Beispiel dafür, wie diese Steigerungsgrenzen berechnet werden.

### Boxplotdiagramm

Das Boxplotdiagramm in der [!DNL Target] -Oberfläche stellt den erwarteten Wert und das 95-%-Konfidenzintervall der betreffenden Erfolgsmetrik dar. Sie können sich dies als eine grafische Methode zum Anzeigen der Informationen zur Steigerung und zu den Steigerungsgrenzen vorstellen.

Es gibt einige wichtige Möglichkeiten, wie Sie mit [!DNL Target] die Konfidenzinformationen interpretieren können. Eine davon ist Farbe. Das Diagramm zeigt das Konfidenzintervall eines spezifischen Erlebnisses, das sich mit dem Kontrollkonfidenzintervall überschneidet, in Grau an. Zudem zeigt es das Konfidenzintervall eines spezifischen Erlebnisses, das ober- oder unterhalb des Kontrollkonfidenzintervalls liegt, entsprechend in Grün oder Rot an.

Die Länge des Boxplotdiagramms gibt leicht nachvollziehbar an, wie groß das Konfidenzintervall ist. Wenn Sie mehr Daten in Ihrer Aktivität sammeln, verlagert und ändert sich der Balken. Das Konfidenzintervall ergibt sich aus der Varianz und dem Stichprobenumfang (Anzahl der Besucher). Je kleiner die Varianz und je größer der Stichprobenumfang, desto enger ist Ihr Konfidenzintervall.

### Konfidenz

Die Konfidenz eines angezeigten Erlebnisses oder Angebots ist eine Wahrscheinlichkeit (ausgedrückt als Prozentsatz), ein Ergebnis zu erhalten, das _weniger extrem_ ist als das tatsächlich beobachtete Ergebnis, _wenn die Null-Hypothese wahr ist_, d. h. wenn es keinen Unterschied in den Konversionsraten zwischen diesem Erlebnis oder Angebot und dem Kontrollerlebnis/Angebot gibt. In Bezug auf p-Werte ist diese angezeigte Konfidenz `1 - p-value`. Einfach ausgedrückt zeigt eine höhere Konfidenz, dass die Daten weniger konsistent mit der Annahme sind, dass das Kontroll- und Nicht-Kontrollangebot/-Erlebnis über gleiche Konversionsraten verfügen.

## Erfahren Sie, wie das Konfidenzintervall für die Steigerung ermittelt wird. {#pdf}

Laden Sie die PDF-Datei &quot;[Konfidenzintervall für die Steigerung&quot;](/help/main/assets/confidence_interval_lift.pdf) herunter, um weitere Informationen zu erhalten.

## Wie werden Steigerungsgrenzen berechnet? {#section_1D360781D972483693680BE0F07AEAD1}

Die Steigerungsgrenzen stellen 95-%-Konfidenzintervalle der Steigerung dar, die das spezifische Erlebnis oder Angebot gegenüber dem Kontrollerlebnis oder -angebot aufweist. Grob gesagt weist die tatsächliche Steigerung eine etwa 95%ige Chance auf, sich zwischen diesen Steigerungen zu befinden.

Die Steigerungsgrenzen werden mithilfe der folgenden Formel berechnet:

![Lift_diagramm image](assets/lift_diagram.png)

Es gibt einige zusätzliche Berechnungen, um zur Eingabe der Steigerungsgrenzen zu gelangen:

* **t-Wert:** Die kritische Statistik für unser Konfidenzniveau von 95 % ist 1,96. Weitere Informationen zu [t-Werten finden Sie hier](https://en.wikipedia.org/wiki/T-statistic).
* **Steigerungsvarianz:** Der Standardfehler der Erfolgsmetrik von Erlebnis N und der Standardfehler der Erfolgsmetrik des Kontrollerlebnisses sind zum Ermitteln der Steigerungsvarianz erforderlich, was mithilfe der folgenden Formel (in der Abbildung ist die Erfolgsmetrik eine Konversion) berechnet wird.

  ![Bild der Steigerung_Varianz](assets/lift_variance.png)

* **Konversionsrate/Erfolgsmetrik-Standardfehler:** Der Standardfehler wird mit der folgenden Formel auf die gleiche Weise für Erlebnis N und die Kontrolle berechnet (in der Abbildung ist die Erfolgsmetrik eine Konversion). Informationen über den Standardfehler finden Sie [hier](https://en.wikipedia.org/wiki/Standard_error).

  ![standard_error image](assets/standard_error.png)

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

![standard_error_A image](assets/standard_error_A.png)

**Standardfehler für Erlebnis B**

![standard_error_B image](assets/standard_error_B.png)

**Steigerungsvarianz für Erlebnis B**

![lift_variance_B image](assets/lift_variance_B.png)

**Steigerungsgrenzen für Erlebnis B**

Erwartete Steigerung für Erlebnis B:

![lift_bounds_B image](assets/lift_bounds_B.png)

Daher würden die Steigerungsgrenzen für Erlebnis B wie folgt lauten:

![lift_bounds_B2 image](assets/lift_bounds_B2.png)

>[!NOTE]
>
>Erwarten Sie geringfügige Abweichungen zwischen manuellen Berechnungen mit den oben genannten Formeln und den im Bericht angezeigten Zahlen. Diese Unterschiede stammen daher, dass die Seitenaufrufe für manuelle Berechnungen abgerundet werden. Die im [!DNL Target] -Bericht angezeigte Steigerung basiert auf den genauen Zahlen, die aus der Interaktion insgesamt und der Interaktionsanzahl ermittelt wurden. Die Interaktionszahlen können über die API des Performanceberichts abgerufen werden.

## Wann werden Steigerungsgrenzen nicht angezeigt? {#section_C5622E1E94684DAD937249B51A9E42CC}

In bestimmten Fällen zeigt [!DNL Target] keine Steigerungsgrenzen an:

* Für Aktivitäten, wenn die Gesamtanzahl der Besuche oder Besucher niedriger als 30 ist.
* Für Aktivitäten vom Typ [!UICONTROL Auto-Allocate] werden keine Steigerungsgrenzen angezeigt, bis ein Erlebnis eine Konfidenz von 60 % erreicht hat.
