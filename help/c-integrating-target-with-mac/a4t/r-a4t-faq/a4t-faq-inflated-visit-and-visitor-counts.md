---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; überhöht; Besuch; Besucher; partieller Treffer; verwaist; Waise; partielle Treffer
description: Finden Sie Antworten auf Fragen zu erhöhten Besuchs- und Besucher-Zählungen bei der Verwendung von Analytics for [!DNL Target] (A4T). Erfahren Sie, wie Sie "partielle Daten"minimieren.
title: Wo finde ich FAQs zu überhöhten Besuchs- und Besucher-Zählungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 61%

---

# Überhöhte Besuchs- und Besucherzahlen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Warum zeigen meine Analytics-Daten Besuche an, zu denen es keine Seitenansichten oder anderen Variablenwerte gibt? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Wenn [!DNL Adobe Analytics] zur Messung von [!DNL Target]-Aktivitäten (als A4T bezeichnet) verwendet wird, erfasst [!DNL Analytics] Daten, die nicht verfügbar sind, wenn keine [!DNL Target]-Aktivität auf der Seite vorhanden ist. Der Grund dafür ist, dass [!DNL Target]-Aktivitäten ihre Aufrufe zu Beginn der Seite vornehmen, während [!DNL Analytics] seine Datenerfassungsaufrufe für gewöhnlich am Ende der Seite auslöst. Bei der bisherigen Implementierung von A4T enthält die Adobe diese zusätzlichen Daten, sobald eine [!DNL Target]-Aktivität aktiv war.

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Was sind Treffer mit partiellen Daten? {#section_59A203E289564576BF6821F96B0B9E11}

Zu einem Treffer mit partiellen Daten kommt es, wenn ein [!DNL Target]-Tag zu Beginn der Seite ausgelöst wird, jedoch nicht das [!DNL Analytics]-Tag am Ende der Seite. Es gibt verschiedene Gründe dafür. In der bisherigen Implementierung von [!DNL A4T] enthält die Adobe partielle Daten zu diesen Treffern, sobald eine [!DNL Target]-Aktivität aktiv war. In Zukunft enthält die Adobe diese zusätzlichen Daten nur, wenn die Tags [!DNL Target] und [!DNL Analytics] ausgelöst wurden.

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## In meinen Besuchszahlen gibt es einen starken Anstieg. Wie kann ich feststellen, ob diese Besuche durch Treffer mit partiellen Daten verursacht werden? {#section_28506672C6224ED18AC74F6A02F6F811}

Um einen partiellen Datenbericht zu erhalten, wenden Sie sich an die [Adobe-Kundenunterstützung](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In der Benutzeroberfläche von [!DNL Analytics] ist diese Information nicht angegeben.

## Welche möglichen Ursachen gibt es für Treffer mit partiellen Daten? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Treffer mit partiellen Daten resultieren meist aus einer fehlerhaften Implementierung (z. B. wenn Report Suite-IDs nicht übereinstimmen). Es gibt auch ganz normale Ursachen, wie zum Beispiel langsame Seiten, Seitenfehler, Umleitungsangebote in einer Aktivität oder veraltete Bibliotheksversionen.

Mehr darüber erfahren Sie unter „Welche Ursachen gibt es für partielle Daten?“ in  [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Ich habe Treffer mit partiellen Daten. Wie kann ich meine Daten bereinigen?   {#section_CBE778A9D07A469E8FF98F68BACC7124}

Sie können eine virtuelle Report Suite erstellen, um historische partielle Daten aus Ihren Berichten auszuschließen.

Weitere Informationen dazu finden Sie unter „Wie kann man historische Trends ohne partielle Daten anzeigen?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Gibt es irgendeine Möglichkeit, zu verhindern, dass meine Seiten Treffer mit partiellen Daten generieren? {#section_4B00E7E618444BE98A0798DE98F08B21}

Nach dem 14. November 2016 umfasst die Adobe nur Daten, wenn sowohl die Tags [!DNL Target] als auch [!DNL Analytics] ausgelöst wurden. Diese Änderung ist nicht rückwirkend. Wenn Ihre Verlaufsberichte überhöhte Zählerwerte anzeigen, können Sie diese durch Erstellen einer Virtual Report Suite aus Ihren Berichten ausschließen. Siehe &quot;Wie kann ich historische Trends ohne partielle Daten Ansicht?&quot; in [Minimieren der Zählung überhöhter Besuche und Besucher in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

Es gibt auch Maßnahmen, die Sie ergreifen können, um Treffer mit partiellen Daten zu minimieren. Weitere Informationen dazu finden Sie unter „Welche empfohlenen Vorgehensweisen gibt es, um partielle Daten zu reduzieren?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Wenn Treffer mit partiellen Daten aus Berichte entfernt werden, verlieren Sie dann nicht wertvolle [!DNL Target]- oder Analytics-Daten? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Die Aufnahme von partiellen Daten in den Berichte [!DNL Analytics] bietet zwar zusätzliche Informationen, stellt aber auch eine Inkonsistenz mit historischen Daten aus Zeiträumen dar, in denen keine [!DNL Target]-Aktivitäten ausgeführt wurden. Das Einschließen von partiellen Trefferdaten kann für [!DNL Analytics]-Benutzer, die Trends im Laufe der Zeit analysieren, Probleme verursachen.

Es gibt auch Maßnahmen, die Sie ergreifen können, um Treffer mit partiellen Daten zu minimieren. Weitere Informationen dazu finden Sie unter „Welche empfohlenen Vorgehensweisen gibt es, um partielle Daten zu reduzieren?“ in [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Gibt es bestimmte Typen von [!DNL Target]-Aktivitäten, die häufiger Treffer mit partiellen Daten verursachen? {#section_69837442A9B84366BEFDA4588B31E574}

Umleitungsangebote senden einen Benutzer unverzüglich auf eine andere Seite - was bedeutet, dass der [!DNL Analytics]-Aufruf auf der ersten Seite nicht ausgelöst wird.
