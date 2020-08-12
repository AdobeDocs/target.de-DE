---
keywords: faq;frequently asked questions;analytics for target;a4T;inflated;visit;visitor;partial hit;orphaned;orphan;partial-hit
description: Dieses Thema enthält Antworten auf häufig zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Überhöhte Besuchs- und Besucherzahlen – Häufig gestellte Fragen zu A4T
feature: null
topic: Standard
uuid: 5d1b77bb-9053-4533-bd01-d6f53f0751e9
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 100%

---


# Überhöhte Besuchs- und Besucherzahlen – Häufig gestellte Fragen zu A4T{#inflated-visit-and-visitor-counts-a-t-faq}

Dieses Thema enthält Antworten auf häufig zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Warum zeigen meine Analytics-Daten Besuche an, zu denen es keine Seitenansichten oder anderen Variablenwerte gibt? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Wenn [!DNL Adobe Analytics] zum Messen von [!DNL Target]-Aktivitäten verwendet wird (was als A4T bezeichnet wird), erfasst [!DNL Analytics] zusätzliche Daten, die nur dann verfügbar sind, wenn auf der Seite eine [!DNL Target]-Aktivität vorhanden ist. Der Grund dafür ist, dass [!DNL Target]-Aktivitäten ihre Aufrufe zu Beginn der Seite vornehmen, während [!DNL Analytics] seine Datenerfassungsaufrufe für gewöhnlich am Ende der Seite auslöst. In der bisherigen Implementierung von A4T haben wir diese zusätzlichen Daten immer mit eingefügt, wenn eine [!DNL Target]-Aktivität aktiv war.

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Was sind Treffer mit partiellen Daten? {#section_59A203E289564576BF6821F96B0B9E11}

Zu einem Treffer mit partiellen Daten kommt es, wenn ein [!DNL Target]-Tag zu Beginn der Seite ausgelöst wird, jedoch nicht das [!DNL Analytics]-Tag am Ende der Seite. Dies hat verschiedene Ursachen. In der bisherigen [!DNL A4T]-Implementierung haben wir partielle Daten zu solchen Treffern immer mit erfasst, wenn eine [!DNL Target]-Aktivität aktiv war. Ab nun werden wir diese zusätzlichen Daten nur noch dann einfügen, wenn sowohl die [!DNL Target]- als auch die [!DNL Analytics]-Tags ausgelöst wurden.

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## In meinen Besuchszahlen gibt es einen starken Anstieg. Woran kann ich erkennen, ob diese aus Treffern mit partiellen Daten resultieren?  {#section_28506672C6224ED18AC74F6A02F6F811}

Um einen partiellen Datenbericht zu erhalten, wenden Sie sich an die [Adobe-Kundenunterstützung](../../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In der Benutzeroberfläche von [!DNL Analytics] ist diese Information nicht angegeben.

## Welche möglichen Ursachen gibt es für Treffer mit partiellen Daten? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Treffer mit partiellen Daten resultieren meist aus einer fehlerhaften Implementierung (z. B. wenn Report Suite-IDs nicht übereinstimmen). Es gibt auch ganz normale Ursachen, wie zum Beispiel langsame Seiten, Seitenfehler, Umleitungsangebote in einer Aktivität oder veraltete Bibliotheksversionen.

Mehr darüber erfahren Sie unter „Welche Ursachen gibt es für partielle Daten?“ in  [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Ich habe Treffer mit partiellen Daten. Wie kann ich meine Daten bereinigen?  {#section_CBE778A9D07A469E8FF98F68BACC7124}

Sie können eine virtuelle Report Suite erstellen, um historische partielle Daten aus Ihren Berichten auszuschließen.

Weitere Informationen dazu finden Sie unter „Wie kann man historische Trends ohne partielle Daten anzeigen?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Gibt es irgendeine Möglichkeit, zu verhindern, dass meine Seiten Treffer mit partiellen Daten generieren? {#section_4B00E7E618444BE98A0798DE98F08B21}

Nach dem 14. November 2016 werden wir Daten nur noch dann einfügen, wenn sowohl die [!DNL Target]- als auch die [!DNL Analytics]-Tags ausgelöst wurden. Diese Änderung ist nicht rückwirkend. Wenn in Ihren historischen Berichten überhöhte Zählerwerte angezeigt werden, die Sie nicht in Ihren Berichten aufgeführt haben möchten, können Sie eine virtuelle Report Suite erstellen. Wie Sie dazu vorgehen, erfahren Sie unter „Wie kann man historische Trends ohne partielle Daten anzeigen?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

Es gibt auch Maßnahmen, die Sie ergreifen können, um Treffer mit partiellen Daten zu minimieren. Weitere Informationen dazu finden Sie unter „Welche empfohlenen Vorgehensweisen gibt es, um partielle Daten zu reduzieren?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Wenn Treffer mit partiellen Daten aus Berichten entfernt werden, gehen dann nicht wertvolle Target- oder Analytics-Daten verloren? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Auch wenn die Aufnahme partieller Daten in [!DNL Analytics]-Berichten keinen zusätzlichen Informationswert bietet, stellt es doch die Konsistenz mit historischen Daten aus früheren Zeiträumen sicher, in denen Daten ohne laufende [!DNL Target]-Aktivitäten erfasst wurden. Dies könnte für [!DNL Analytics]-Benutzer, die Trends über größere Zeiträume analysieren, zu einem Problem werden.

Es gibt auch Maßnahmen, die Sie ergreifen können, um Treffer mit partiellen Daten zu minimieren. Weitere Informationen dazu finden Sie unter „Welche empfohlenen Vorgehensweisen gibt es, um partielle Daten zu reduzieren?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](../../../c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Gibt es bestimmte Typen von Target-Aktivitäten, die häufiger zu Treffern mit partiellen Daten führen? {#section_69837442A9B84366BEFDA4588B31E574}

Umleitungsangebote senden einen Benutzer unverzüglich auf eine andere Seite - was bedeutet, dass der [!DNL Analytics]-Aufruf auf der ersten Seite nicht ausgelöst wird.
