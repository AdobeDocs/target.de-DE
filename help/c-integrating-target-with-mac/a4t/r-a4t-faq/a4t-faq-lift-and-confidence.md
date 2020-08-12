---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T
feature: null
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 50%

---


# Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T{#lift-and-confidence-a-t-faq}

Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Kann ich Offline-Berechnungen für A4T durchführen? {#section_55B5B750E17D414CAECBEECE27B15D81}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich. Weitere Informationen finden Sie unter „Durchführen von Offline-Berechnungen für Analytics für Target (A4T)“ in [Konfidenzniveau und Konfidenzintervall](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Wie wird die Steigerung berechnet? {#section_8CAE788EED5646C4B1D64A0D22070734}

Die Steigerung ist die prozentuale Differenz zwischen den Ergebnissen Ihrer Kontrollseite und einer erfolgreichen Testvariante.

## Wie wird die Konfidenz berechnet?  {#section_97DB24D833E742988318CA65DA65DAD9}

Die Konfidenzniveau ist die Wahrscheinlichkeit, dass die gemessene Konversionsrate von der Konversionsrate der Siegerseite aus anderen Gründen als reinem Zufall abweicht.

## Warum kann ich Steigerung und Konfidenz nicht in errechneten Metriken anzeigen?  {#lift-confidence}

Berechnete Metriken werden derzeit nicht in den Funktionen Steigerung und Konfidenz unterstützt. This is due to the fact that Analytics calculates metrics at an aggregate-level, rather than at a visitor-level. Konfidenz ist vor allem eine Berechnung auf Besucher-Ebene.

Non-calculated (standard) events are supported in lift and confidence. They become the numerator in the lift function; the numerator cannot be a calculation itself. Der Nenner sind die normalisierenden Metriken (Impressionen, Besuche oder Besucher). Beispiele für Standard-Ereignis sind Bestellungen, Umsatz, Aktivitäten-Konversionen, benutzerdefinierte Ereignis 1-1000 usw. Dies bedeutet, dass gängige Optimierungsmetriken wie die Konversationsrate (Bestellungen/Besucher) und RPV (Umsatz/Besucher) in Steigerung und Konfidenz unterstützt werden.

Beispiele für nicht unterstützte Metriken oder Anwendungsfälle:

* Durchschnittlicher Bestellwert (Umsatz/Bestellung, pro Besucher). AOV wird nicht unterstützt, da der Zähler eine berechnete Metrik ist. Stattdessen wird empfohlen, die beiden einflussreichen Metriken von AOV - Umsatz pro Besucher und Konversionsrat zu berücksichtigen.
* Berechnete Metriken, die die Summe der standardmäßigen Ereignis darstellen. Sie können z. B. zehn verschiedene Interessentenformulare in zehn separate Ereignis nachverfolgen und diese dann zusammen hinzufügen, um die Gesamtzahl der Interessenteneinsendungen zu erhalten. Eine empfohlene Methode zur Verfolgung dieser Ereignis ist die Implementierung eines einzigen Ereignisses zur Interessentenübermittlung in Analytics und dann die Verwendung eines eVar zur Erfassung des Interessentenformulartyps. Die Verwendung dieser Methode erfordert weniger Variablen und stellt sicher, dass Sie die Metrik für die Übermittlung einzelner Interessenten in den Steigerungs- und Konfidenzfunktionen verwenden können.

## Wie verwaltet A4T Konfidenzberechnungen?  {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T verwendet nicht binäre Metrikberechnungen mit Daten der Quadratsumme. Die Varianz wird mit den Daten der Quadratsumme errechnet. Extreme Bestellungen werden nicht berücksichtigt. Darüber hinaus wendet die Konfidenzberechnung keine Bonferroni-Korrektur für mehrere Angebot an.

## Funktionieren die Steigerung und die Konfidenz mit Ad Hoc und Report Builder? Wenn es nicht nativ ist, kann ich es dann selbst hinzufügen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Steigerung und Konfidenz funktionieren nicht mit Ad Hoc oder Report Builder und können nicht selbst für kontinuierliche Variablen errechnet werden. Es ist möglich, sie für binäre Metriken manuell zu errechnen.
