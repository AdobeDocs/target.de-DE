---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Steigerung; Ad-hoc; Report Builder; Konfidenz
description: Ermitteln Sie Antworten auf Fragen zur Steigerung und zum Vertrauen bei der Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten.
title: Wo finde ich Informationen zur Steigerung und zum Vertrauen in A4T?
feature: Analytics for Target (A4T)
exl-id: 42fd179b-944a-4a0a-b299-85ea4a7ea244
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 41%

---

# Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig nach Steigerung und Vertrauen gefragt werden, wenn [!DNL Adobe Analytics] als Berichte für [!DNL Adobe Target] (A4T) verwendet wird.

## Kann ich Offline-Berechnungen für A4T durchführen? {#section_55B5B750E17D414CAECBEECE27B15D81}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich. Weitere Informationen finden Sie unter „Durchführen von Offline-Berechnungen für Analytics für Target (A4T)“ in [Konfidenzniveau und Konfidenzintervall](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Wie wird die Steigerung berechnet? {#section_8CAE788EED5646C4B1D64A0D22070734}

Die Steigerung ist die prozentuale Differenz zwischen den Ergebnissen Ihrer Kontrollseite und einer erfolgreichen Testvariante.

## Wie wird die Konfidenz berechnet?   {#section_97DB24D833E742988318CA65DA65DAD9}

Die Konfidenzniveau ist die Wahrscheinlichkeit, dass die gemessene Konversionsrate von der Konversionsrate der Siegerseite aus anderen Gründen als reinem Zufall abweicht.

## Warum kann ich Steigerung und Konfidenz nicht in errechneten Metriken anzeigen?   {#lift-confidence}

Berechnete Metriken werden derzeit nicht in den Funktionen Steigerung und Konfidenz unterstützt. Analytics berechnet Metriken auf Aggregat- und nicht auf Besucher-Ebene. Konfidenz ist vor allem eine Berechnung auf Besucher-Ebene.

Nicht berechnete (Standard-)Ereignis werden in Steigerung und Konfidenz unterstützt. Sie werden in der Steigerungsfunktion zum Zähler. der Zähler kann keine Berechnung selbst sein. Der Nenner sind die normalisierenden Metriken (Impressionen, Besuche oder Besucher). Beispiele für Standard-Ereignis sind Bestellungen, Umsatz, Aktivitäten-Konversionen, benutzerdefinierte Ereignis 1-1000 usw. Allgemeine Optimierungsmetriken wie die Konversationsrate (Bestellungen/Besucher) und RPV (Umsatz/Besucher) werden in Steigerung und Konfidenz unterstützt.

Beispiele für nicht unterstützte Metriken oder Anwendungsfälle:

* Durchschnittlicher Bestellwert (Umsatz/Bestellung, pro Besucher). AOV wird nicht unterstützt, da der Zähler eine berechnete Metrik ist. Stattdessen wird empfohlen, die beiden einflussreichen Metriken von AOV - Umsatz pro Besucher und Konversionsrat zu berücksichtigen.
* Berechnete Metriken, die die Summe der standardmäßigen Ereignis darstellen. Sie können z. B. zehn verschiedene Interessentenformulare in zehn separate Ereignis nachverfolgen und diese dann zusammen hinzufügen, um die Gesamtzahl der Interessenteneinsendungen zu erhalten. Eine empfohlene Methode zur Verfolgung dieser Ereignis ist die Implementierung eines einzigen Ereignisses zur Interessentenübermittlung in Analytics und dann die Verwendung eines eVar zur Erfassung des Interessentenformulartyps. Die Verwendung dieser Methode erfordert weniger Variablen und stellt sicher, dass Sie die Metrik für die Übermittlung einzelner Interessenten in den Steigerungs- und Konfidenzfunktionen verwenden können.

## Wie verwaltet A4T Konfidenzberechnungen?   {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T verwendet nicht binäre Metrikberechnungen mit Daten der Quadratsumme. Die Varianz wird mit den Daten der Quadratsumme errechnet. Extreme Bestellungen werden nicht berücksichtigt. Bei der Konfidenzberechnung wird außerdem keine Bonferroni-Korrektur für mehrere Angebot angewendet.

## Funktionieren die Steigerung und die Konfidenz mit Ad Hoc und Report Builder? Wenn es nicht nativ ist, kann ich es dann selbst hinzufügen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Steigerung und Konfidenz funktionieren nicht mit Ad Hoc oder Report Builder und können nicht selbst für kontinuierliche Variablen errechnet werden. Es ist möglich, sie für binäre Metriken manuell zu errechnen.
