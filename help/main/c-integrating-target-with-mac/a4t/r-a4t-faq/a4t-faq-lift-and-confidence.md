---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Steigerung; Ad-hoc; Report Builder; Konfidenz
description: Hier finden Sie Antworten auf Fragen zur Steigerung und Konfidenz bei der Verwendung von Analytics für  [!DNL Target] A4T). Mit A4T können Sie Analytics-Berichte für - [!DNL Target]  verwenden.
title: Wo finde ich Informationen über Steigerung und Konfidenz mit A4T?
feature: Analytics for Target (A4T)
exl-id: 42fd179b-944a-4a0a-b299-85ea4a7ea244
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 25%

---

# Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zur Steigerung und Konfidenz gestellt werden, wenn [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) verwendet wird.

## Kann ich Offline-Berechnungen für A4T durchführen? {#section_55B5B750E17D414CAECBEECE27B15D81}

+++Antwort
Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich. Weitere Informationen finden Sie unter [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

+++

## Wie wird die Steigerung berechnet? {#section_8CAE788EED5646C4B1D64A0D22070734}

+++Antwort
Die Steigerung ist die prozentuale Differenz zwischen den Ergebnissen Ihrer Kontrollseite und einer erfolgreichen Testvariante.

+++

## Wie wird die Konfidenz berechnet?  {#section_97DB24D833E742988318CA65DA65DAD9}

+++Antwort
Das Konfidenzniveau ist eine prozentuale Wahrscheinlichkeit, die `1 - p-value` entspricht, wobei die `p-value` aus einem t-Test berechnet wird. Siehe [Statistische Berechnungen in A/Bn-](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

+++

## Warum kann ich Steigerung und Konfidenz nicht in errechneten Metriken anzeigen?  {#lift-confidence}

+++Antwort
Berechnete Metriken werden derzeit in Funktionen für Steigerung und Konfidenz nicht unterstützt. Analytics berechnet Metriken auf aggregierter Ebene und nicht auf Besucherebene. Insbesondere die Konfidenz ist eine Berechnung auf Besucherebene.

Nicht berechnete (Standard-)Ereignisse werden bei Steigerung und Konfidenz unterstützt. Sie werden in der Auftriebsfunktion zum Zähler; der Zähler kann nicht selbst eine Berechnung sein. Der Nenner sind die normalisierenden Metriken (Impressions, Besuche oder Besucher). Einige Beispiele für Standardereignisse sind Bestellungen, Umsatz, Aktivitätskonversionen, benutzerdefinierte Ereignisse 1-1000 usw. Gängige Optimierungsmetriken wie Gesprächsrate (Bestellungen/Besucher) und RPV (Umsatz/Besucher) werden für Steigerung und Konfidenz unterstützt.

Beispiele für nicht unterstützte Metriken oder Anwendungsfälle sind:

* Durchschnittlicher Bestellwert (Umsatz/Bestellung, pro Besucher). AOV wird nicht unterstützt, da der Zähler eine berechnete Metrik ist. Stattdessen wird empfohlen, die beiden beeinflussenden Metriken der AOV zu berücksichtigen - Umsatz pro Besucher und Konversionsrate.
* Berechnete Metriken, die die Summe der Standardereignisse darstellen. Sie können beispielsweise zehn verschiedene Lead-Formulare in zehn separate Ereignisse verfolgen und diese dann zusammenfügen, um insgesamt Lead-Übermittlungen zu erhalten. Eine empfohlene Methode zum Nachverfolgen dieser Ereignisse besteht darin, ein einzelnes Lead-Übermittlungsereignis in Analytics zu implementieren und dann eine eVar zu verwenden, um den Typ des Lead-Formulars zu erfassen. Die Verwendung dieser Methode erfordert weniger Variablen und stellt sicher, dass Sie die einzelne Lead-Übermittlungsmetrik in Aufstiegs- und Konfidenzfunktionen verwenden können.

+++

## Wie verwaltet A4T Konfidenzberechnungen?  {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

+++Antwort
[!DNL Adobe Analytics] behandelt alle Metriken als nicht-binär und berechnet daher Konfidenz-/p-Werte auf eine Weise, die sich von der Verwendung binärer Metriken in einem regulären t-Test unterscheidet. Insbesondere ermöglichen die von A4T verwendeten Berechnungen jedem Benutzer ein kontinuierliches metrisches Ergebnis (nicht nur 1 oder 0 für jeden Benutzer), sodass die Varianz (oder die damit verbundene Standardabweichung) für jedes Erlebnis entsprechend berechnet werden muss. Extreme Bestellungen werden nicht berücksichtigt. Außerdem wird bei der Konfidenzberechnung keine Bonferroni-Korrektur für mehrere Angebote angewendet.

+++

## Funktionieren die Steigerung und die Konfidenz mit Ad Hoc und Report Builder? Wenn es nicht nativ ist, kann ich es dann selbst hinzufügen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

+++Antwort
Steigerung und Konfidenz funktionieren nicht mit Ad Hoc oder Report Builder und können nicht selbst für kontinuierliche Variablen errechnet werden. Es ist möglich, sie für binäre Metriken manuell zu errechnen.
+++
