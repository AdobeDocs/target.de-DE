---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; überhöht; Besuch; Besucher; partieller Treffer; verwaist; Waise; partielle Treffer
description: Hier finden Sie Antworten auf Fragen zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics für [!DNL Target]  (A4T). Erfahren Sie, wie Sie "partielle Daten"minimieren.
title: Wo finde ich häufig gestellte Fragen zu überhöhten Besuchs- und Besucherzahlen mit A4T?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 45%

---

# Überhöhte Besuchs- und Besucherzahlen – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu überhöhten Besuchs- und Besucherzahlen bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## In meinen Besuchszahlen gibt es einen starken Anstieg. Wie kann ich feststellen, ob diese Besuche durch Treffer mit partiellen Daten verursacht wurden? {#section_28506672C6224ED18AC74F6A02F6F811}

+++Antwort
Sie können sich an die [Adobe-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) wenden, um einen Bericht zu partiellen Daten abzurufen. In der Benutzeroberfläche von [!DNL Analytics] ist diese Information nicht angegeben.

+++

## Welche möglichen Ursachen gibt es für Treffer mit partiellen Daten? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

+++Antwort
Treffer mit partiellen Daten sind häufig das Ergebnis einer fehlerhaften Implementierung, z. B. falsch abgestimmte Report Suite-IDs. Es gibt auch ganz normale Ursachen, wie zum Beispiel langsame Seiten, Seitenfehler, Umleitungsangebote in einer Aktivität oder veraltete Bibliotheksversionen.

+++

## Gibt es bestimmte Typen von [!DNL Target] -Aktivitäten, die häufiger zu Treffern mit partiellen Daten führen? {#section_69837442A9B84366BEFDA4588B31E574}

+++Antwort
Umleitungsangebote senden einen Benutzer unverzüglich auf eine andere Seite, was bedeutet, dass der [!DNL Analytics] -Aufruf auf der ersten Seite nicht ausgelöst wird.

+++