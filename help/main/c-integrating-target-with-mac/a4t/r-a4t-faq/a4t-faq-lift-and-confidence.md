---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Steigerung; Ad-hoc; Report Builder; Konfidenz
description: Antworten auf Fragen zur Steigerung und Konfidenz bei der Verwendung von Analytics für [!DNL Target] (A4T). Mit A4T können Sie Analytics-Reporting für [!DNL Target] Aktivitäten.
title: Wo finde ich Informationen über Steigerung und Konfidenz mit A4T?
feature: Analytics for Target (A4T)
exl-id: 42fd179b-944a-4a0a-b299-85ea4a7ea244
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 28%

---

# Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Steigerung und Konfidenz bei der Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T).

## Kann ich Offline-Berechnungen für A4T durchführen? {#section_55B5B750E17D414CAECBEECE27B15D81}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich. Weitere Informationen finden Sie unter „Durchführen von Offline-Berechnungen für Analytics für Target (A4T)“ in [Konfidenzniveau und Konfidenzintervall](/help/main/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Wie wird die Steigerung berechnet? {#section_8CAE788EED5646C4B1D64A0D22070734}

Die Steigerung ist die prozentuale Differenz zwischen den Ergebnissen Ihrer Kontrollseite und einer erfolgreichen Testvariante.

## Wie wird die Konfidenz berechnet?  {#section_97DB24D833E742988318CA65DA65DAD9}

Das Konfidenzniveau ist eine in Prozent ausgedrückte Wahrscheinlichkeit, die gleich `1 - p-value`, wobei `p-value` wird anhand eines t-Tests berechnet. Siehe [Konversionsrate](/help/main/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Warum kann ich Steigerung und Konfidenz nicht in errechneten Metriken anzeigen?  {#lift-confidence}

Berechnete Metriken werden derzeit nicht in Steigerungs- und Konfidenzfunktionen unterstützt. Analytics berechnet Metriken auf aggregierter Ebene und nicht auf Besucherebene. Konfidenz ist insbesondere eine Berechnung auf Besucherebene.

Nicht berechnete (standardmäßige) Ereignisse werden in Steigerung und Konfidenz unterstützt. Sie werden zum Zähler in der Steigerungsfunktion. Der Zähler kann keine Berechnung selbst sein. Der Nenner sind die normalisierenden Metriken (Impressionen, Besuche oder Besucher). Beispiele für Standardereignisse sind Bestellungen, Umsatz, Aktivitätskonversionen, benutzerspezifische Ereignisse 1-1000 usw. Allgemeine Optimierungsmetriken wie die Konversationsrate (Bestellungen/Besucher) und RPV (Umsatz/Besucher) werden in Steigerung und Konfidenz unterstützt.

Beispiele für nicht unterstützte Metriken oder Anwendungsfälle sind:

* Durchschnittlicher Bestellwert (Umsatz/Bestellung, pro Besucher). AOV wird nicht unterstützt, da der Zähler eine berechnete Metrik ist. Stattdessen wird empfohlen, die beiden beeinflussenden Metriken von AOV zu berücksichtigen: Umsatz pro Besucher und Konversionsrate.
* Berechnete Metriken, die die Summe der Standardereignisse darstellen. Sie können beispielsweise zehn verschiedene Lead-Formulare in zehn separate Ereignisse verfolgen und sie dann zusammen hinzufügen, um die Gesamtzahl der Lead-Übermittlungen zu erhalten. Eine empfohlene Methode zur Verfolgung dieser Ereignisse besteht darin, ein einzelnes Lead-Sendeereignis in Analytics zu implementieren und dann einen eVar zu verwenden, um den Typ des Lead-Formulars zu erfassen. Die Verwendung dieser Methode erfordert weniger Variablen und stellt sicher, dass Sie die einzelne Metrik für die Übermittlung von Leads in Steigerungs- und Konfidenzfunktionen verwenden können.

## Wie verwaltet A4T Konfidenzberechnungen?  {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

[!DNL Adobe Analytics] behandelt alle Metriken als nicht binär und berechnet daher Konfidenz-/p-Werte auf eine Weise, die sich von der Verwendung binärer Metriken in einem regulären t-Test unterscheidet. Insbesondere ermöglichen die von A4T verwendeten Berechnungen jedem Benutzer ein kontinuierliches Metrikergebnis (nicht nur 1 oder 0 für jeden Benutzer), sodass die Varianz (oder die Standardabweichung) für jedes Erlebnis entsprechend berechnet werden muss. Extreme Bestellungen werden nicht berücksichtigt. Außerdem wird bei der Konfidenzberechnung keine Bonferroni-Korrektur für mehrere Angebote angewendet.

## Funktionieren die Steigerung und die Konfidenz mit Ad Hoc und Report Builder? Wenn es nicht nativ ist, kann ich es dann selbst hinzufügen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Steigerung und Konfidenz funktionieren nicht mit Ad Hoc oder Report Builder und können nicht selbst für kontinuierliche Variablen errechnet werden. Es ist möglich, sie für binäre Metriken manuell zu errechnen.