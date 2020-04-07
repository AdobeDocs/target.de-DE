---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: b5191230c76135d5299754e72c9651d018086e60

---


# Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T{#lift-and-confidence-a-t-faq}

Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Kann ich Offline-Berechnungen für A4T durchführen? {#section_55B5B750E17D414CAECBEECE27B15D81}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich. Weitere Informationen finden Sie unter „Durchführen von Offline-Berechnungen für Analytics für Target (A4T)“ in [Konfidenzniveau und Konfidenzintervall](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Wie wird die Steigerung berechnet? {#section_8CAE788EED5646C4B1D64A0D22070734}

Die Steigerung ist die prozentuale Differenz zwischen den Ergebnissen Ihrer Kontrollseite und einer erfolgreichen Testvariante.

## Wie wird die Konfidenz berechnet?  {#section_97DB24D833E742988318CA65DA65DAD9}

Die Konfidenzniveau ist die Wahrscheinlichkeit, dass die gemessene Konversionsrate von der Konversionsrate der Siegerseite aus anderen Gründen als reinem Zufall abweicht.

## Warum kann ich Steigerung und Konfidenz nicht in errechneten Metriken anzeigen?  {#section_D3E44E24782A409DBD88AE4D1595CB58}

Steigerung und Konfidenz werden derzeit nicht mit berechneten Metriken unterstützt. In den meisten Fällen ist dies jedoch kein Problem, da der im A4T-Bericht berechnete Konversionsrate bereits eine berechnete Metrik ist, bei der der Nenner die normalisierende Metrik ist (Instanzen, Besuche, Besucher). Wenn Sie beispielsweise die Bestellmetrik auswählen und die Normalisierungsmetrik Besucher ist, wird der Konversionsrate (Bestellungen/Besucher) automatisch über den A4T-Berichte berechnet. Die resultierende Steigerungsmetrik spiegelt den Unterschied in diesem Konversionsrate in den Texterlebnissen im Vergleich zum Standard wider.

Die am häufigsten für die Optimierung berechneten Metriken lassen sich in eine von zwei Kategorien unterteilen: Aggregat-Metriken und andere Konversionsberechnungen, z. B. durchschnittlicher Bestellwert (AOV).

Aggregat-Metriken werden verwendet, wenn ein Unternehmen eindeutige Ereignis verwendet, um verschiedene &quot;Aromen&quot;der Speicherkonvertierung zu erfassen. Wenn Ihr Ziel z. B. darin besteht, Interessentenformularsendungen zu fördern und Sie über 10 verschiedene Interessentenformulare verfügen, kann eine Firma eindeutige Ereignis zur Zählung der einzelnen Formularkonvertierungstypen erstellen. Um die Gesamtanzahl aller gesendeten Interessentenformulare anzuzeigen, müssen sie eine einfache errechnete Metrik erstellen, um sie alle zusammen hinzuzufügen. Eine bessere, modernere Methode zur Verfolgung dieses Problems besteht darin, ein einzelnes Ereignis für die Interessentenübermittlung in Analytics zu implementieren und dann eine eVar zur Erfassung des Interessentenformulartyps zu verwenden. Bei Verwendung dieser Methode sind weniger Variablen erforderlich, sodass keine individuellen Metriken mehr Aggregat werden müssen und Sie weiterhin die Möglichkeit haben, eine holistische Interessentenformularumrechnung zu sehen und diese mithilfe der eVar nach Interessententypen zu unterteilen. Dadurch entfällt auch die Notwendigkeit von Aggregat-Metriken bei der Bewertung der Leistung einer Zielgruppe-Aktivität.

Eine andere häufig verwendete berechnete Metrik, der durchschnittliche Bestellwert, wird derzeit nicht mit Steigerung und Konfidenz unterstützt, da die Normalisierungsmetrik keine Standardmetrik ist (Instanzen, Besuche, Besucher). Stattdessen sollten Sie die beiden einflussreichen Metriken AOV, Umsatz pro Besucher und Konversionsrat im Auge behalten.

## Wie verwaltet A4T Konfidenzberechnungen?  {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T verwendet nicht binäre Metrikberechnungen mit Daten der Quadratsumme. Die Varianz wird mit den Daten der Quadratsumme errechnet. Extreme Bestellungen werden nicht berücksichtigt.

Es können alle Analytics-Segmente für den Bericht übernommen werden. So können Sie die „extreme Bestellung“ zu den anderen Segmentoptionen hinzufügen. Eine Metrik kann außerdem zum Beschränken von Elementen zusammengestellt werden, zum Beispiel, wie oft ein Besucher konvertiert.

## Funktionieren die Steigerung und die Konfidenz mit Ad Hoc und Report Builder? Wenn es nicht nativ ist, kann ich es dann selbst hinzufügen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Steigerung und Konfidenz funktionieren nicht mit Ad Hoc oder Report Builder und können nicht selbst für kontinuierliche Variablen errechnet werden. Es ist möglich, sie für binäre Metriken manuell zu errechnen.
