---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; überhöht; Besuch; Besucher; partieller Treffer; verwaist; Waise; partielle Treffer
description: Ermitteln Sie Antworten auf Fragen zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics für [!DNL Target] (A4T). Erfahren Sie, wie Sie "partielle Daten"minimieren.
title: Wo finde ich häufig gestellte Fragen zu überhöhten Besuchs- und Besucherzahlen mit A4T?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 64%

---

# Überhöhte Besuchs- und Besucherzahlen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Warum zeigen meine Analytics-Daten Besuche an, zu denen es keine Seitenansichten oder anderen Variablenwerte gibt? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Wann [!DNL Adobe Analytics] wird verwendet, um [!DNL Target] Aktivitäten (als A4T bezeichnet), [!DNL Analytics] erfasst Daten, die nicht verfügbar sind, wenn keine [!DNL Target] -Aktivität auf der Seite. Der Grund dafür ist, dass [!DNL Target]-Aktivitäten ihre Aufrufe zu Beginn der Seite vornehmen, während [!DNL Analytics] seine Datenerfassungsaufrufe für gewöhnlich am Ende der Seite auslöst. In der bisherigen Implementierung von A4T hat Adobe diese zusätzlichen Daten immer einbezogen, wenn eine [!DNL Target]-Aktivität aktiv war.

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Was sind Treffer mit partiellen Daten? {#section_59A203E289564576BF6821F96B0B9E11}

Zu einem Treffer mit partiellen Daten kommt es, wenn ein [!DNL Target]-Tag zu Beginn der Seite ausgelöst wird, jedoch nicht das [!DNL Analytics]-Tag am Ende der Seite. Es gibt verschiedene Gründe, warum diese Situation eintritt. Im [!DNL A4T] -Implementierung bis heute umfasst die Adobe partielle Daten zu diesen Treffern, sobald eine [!DNL Target] -Aktivität aktiv war. In Zukunft werden diese zusätzlichen Daten in Adobe nur noch dann enthalten sein, wenn beide [!DNL Target] und [!DNL Analytics] -Tags wurden ausgelöst.

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## In meinen Besuchszahlen gibt es einen starken Anstieg. Wie kann ich feststellen, ob diese Besuche durch Treffer mit partiellen Daten verursacht wurden? {#section_28506672C6224ED18AC74F6A02F6F811}

Um einen partiellen Datenbericht zu erhalten, wenden Sie sich an die [Adobe-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In der Benutzeroberfläche von [!DNL Analytics] ist diese Information nicht angegeben.

## Welche möglichen Ursachen gibt es für Treffer mit partiellen Daten? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Treffer mit partiellen Daten resultieren meist aus einer fehlerhaften Implementierung (z. B. wenn Report Suite-IDs nicht übereinstimmen). Es gibt auch ganz normale Ursachen, wie zum Beispiel langsame Seiten, Seitenfehler, Umleitungsangebote in einer Aktivität oder veraltete Bibliotheksversionen.

Mehr darüber erfahren Sie unter „Welche Ursachen gibt es für partielle Daten?“ in  [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Ich habe Treffer mit partiellen Daten. Wie kann ich meine Daten bereinigen?  {#section_CBE778A9D07A469E8FF98F68BACC7124}

Sie können eine virtuelle Report Suite erstellen, um historische partielle Daten aus Ihren Berichten auszuschließen.

Weitere Informationen dazu finden Sie unter „Wie kann man historische Trends ohne partielle Daten anzeigen?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Gibt es irgendeine Möglichkeit, zu verhindern, dass meine Seiten Treffer mit partiellen Daten generieren? {#section_4B00E7E618444BE98A0798DE98F08B21}

Nach dem 14. November 2016 umfasst die Adobe nur Daten, wenn sowohl die [!DNL Target] und [!DNL Analytics] -Tags wurden ausgelöst. Diese Änderung ist nicht rückwirkend. Wenn in Ihren historischen Berichten überhöhte Zählerwerte angezeigt werden, können Sie diese aus Ihren Berichten ausschließen, indem Sie eine Virtual Report Suite erstellen. Siehe &quot;Wie kann ich historische Trends ohne partielle Daten anzeigen?&quot; in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

Es gibt auch Maßnahmen, die Sie ergreifen können, um Treffer mit partiellen Daten zu minimieren. Weitere Informationen dazu finden Sie unter „Welche empfohlenen Vorgehensweisen gibt es, um partielle Daten zu reduzieren?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Wenn Treffer mit partiellen Daten aus Berichten entfernt werden, verlieren Sie dann nicht wertvolle [!DNL Target] oder Analytics-Daten? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Einschließen partieller Daten in [!DNL Analytics] Die Berichterstellung liefert zwar zusätzliche Informationen, stellt aber auch eine Inkonsistenz mit historischen Daten aus früheren Zeiträumen sicher, in denen keine [!DNL Target] -Aktivitäten ausgeführt werden. Das Einschließen von partiellen Treffer-Daten kann Probleme bei der [!DNL Analytics] Benutzer, die Trends im Zeitverlauf analysieren.

Es gibt auch Maßnahmen, die Sie ergreifen können, um Treffer mit partiellen Daten zu minimieren. Weitere Informationen dazu finden Sie unter „Welche empfohlenen Vorgehensweisen gibt es, um partielle Daten zu reduzieren?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Gibt es bestimmte Typen von [!DNL Target] Aktivitäten, die häufiger Treffer mit partiellen Daten verursachen? {#section_69837442A9B84366BEFDA4588B31E574}

Umleitungsangebote senden einen Benutzer unverzüglich auf eine andere Seite - was bedeutet, dass der [!DNL Analytics]-Aufruf auf der ersten Seite nicht ausgelöst wird.
