---
description: Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Steigerung; Ad-hoc; Report Builder; Konfidenz
seo-description: Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
seo-title: Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T
solution: Target
title: Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T{#lift-and-confidence-a-t-faq}

Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Kann ich Offline-Berechnungen für A4T durchführen? {#section_55B5B750E17D414CAECBEECE27B15D81}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich. Weitere Informationen finden Sie unter „Durchführen von Offline-Berechnungen für Analytics für Target (A4T)“ in [Konfidenzniveau und Konfidenzintervall](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Wie wird die Steigerung berechnet? {#section_8CAE788EED5646C4B1D64A0D22070734}

Die Steigerung ist die prozentuale Differenz zwischen den Ergebnissen Ihrer Kontrollseite und einer erfolgreichen Testvariante.

## Wie wird die Konfidenz berechnet? {#section_97DB24D833E742988318CA65DA65DAD9}

Die Konfidenzniveau ist die Wahrscheinlichkeit, dass die gemessene Konversionsrate von der Konversionsrate der Siegerseite aus anderen Gründen als reinem Zufall abweicht.

## Warum kann ich Steigerung und Konfidenz nicht in errechneten Metriken anzeigen? {#section_D3E44E24782A409DBD88AE4D1595CB58}

Steigerung und Konfidenz können derzeit nicht für errechnete Metriken generiert werden. In den meisten Fällen sollte dies jedoch kein Problem sein, da die Steigerung durch die Normalisierungsmetrik normalisiert wird. Wenn Sie beispielsweise die Steigerung für Bestellungen auswählen und die Normalisierungsmetrik „Besuche“ lautet, wird die Steigerung auf dem Verhältnis der beiden errechnet. Das ist dann die Konversionsrate.

## Wie verwaltet A4T Konfidenzberechnungen? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T verwendet nicht binäre Metrikberechnungen mit Daten der Quadratsumme. Die Varianz wird mit den Daten der Quadratsumme errechnet. Extreme Bestellungen werden nicht berücksichtigt.

Es können alle Analytics-Segmente für den Bericht übernommen werden. So können Sie die „extreme Bestellung“ zu den anderen Segmentoptionen hinzufügen. Eine Metrik kann außerdem zum Beschränken von Elementen zusammengestellt werden, zum Beispiel, wie oft ein Besucher konvertiert.

## Funktionieren die Steigerung und die Konfidenz mit Ad Hoc und Report Builder? Wenn es nicht nativ ist, kann ich es dann selbst hinzufügen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Steigerung und Konfidenz funktionieren nicht mit Ad Hoc oder Report Builder und können nicht selbst für kontinuierliche Variablen errechnet werden. Es ist möglich, sie für binäre Metriken manuell zu errechnen.
