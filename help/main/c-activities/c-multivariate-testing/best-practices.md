---
keywords: MVT; Multivarianz-Test; Best Practices für Multivarianz-Test; Best Practices für MVT; MVT-Kombinationen; MVT-Berichte
description: Erfahren Sie, wie Sie die Leistung verbessern, Probleme vermeiden und bekannte Probleme korrigieren, die beim Erstellen und Ausführen von [!UICONTROL Multivarianz-Test]-Aktivitäten in [!DNL Adobe Target] auftreten könnten.
title: Was sind die Best Practices für eine Aktivität [!UICONTROL Multivarianz-Test]?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
TQID: 'https://experienceleague.adobe.com/nQEf5GZ8-zVZakygPtMAYWk-xoJPdcycFbzCNKTqJ-k'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 30%
---
# [!UICONTROL Multivarianz-Test] Best Practices {#mvt-best-practices}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine Aktivität vom Typ &quot;**[!UICONTROL Test“ planen, erstellen, analysieren]** weiterverfolgen, um zuverlässige Ergebnisse zu erhalten.

>[!ENDSHADEBOX]

Mit den folgenden Tipps können Sie die Leistung verbessern, Probleme vermeiden und bekannte Probleme korrigieren, die beim Erstellen und Ausführen von **[!UICONTROL Multivarianz-Test]**-Aktivitäten (MVT) in [!DNL Adobe Target] auftreten können.

## Planung {#plan}

* **Verwenden Sie mindestens drei Elemente im Test.**

  Wenn die Anzahl der Elemente niedriger ist, führen Sie eine Reihe von A/B-Tests durch. Weitere Informationen finden Sie unter [Verwendung von Multivarianz-Tests vs. A/B](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#when-to-use-mvt).

* **Achten Sie auf den Traffic, den Sie normalerweise erhalten, einschließlich der Anzahl der Impressionen und Konversionen.**

  MVT erfordert ausreichend Traffic, um nützliche Ergebnisse zu generieren. Diese Informationen helfen, die Wahrscheinlichkeit zu reduzieren, einen Test mit Anforderungen zu entwerfen, die den Traffic Ihrer Site überschreiten.

* **Achten Sie auf die Stellen auf Ihrer Seite, die wahrscheinlich zu signifikanten Ergebnissen führen.**

  Ein Banner oder ein Hero-Bild führt wahrscheinlich zu mehr Konversionen als eine Änderung in der Fußzeile. Wenn Sie weniger einflussreiche Orte mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Orte auf der Seite.

* **Halten Sie die Elemente voneinander unabhängig.**

  Testen Sie z. B. Ihr Layout und Ihren Inhalt nicht im selben Test.

* **Untersuchen Sie den HTML-Code auf den Seiten, die Sie testen möchten.**

  Stellen Sie sicher, dass die HTML-Elemente auf Ihrer Site keine doppelten DOM-IDs haben. Doppelte IDs können dazu führen, dass derselbe Inhalt an mehr als einen Ort geliefert wird.

* **Vorbereiten von Seitenvarianten im Voraus.**

  Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Multivarianz-Test verwenden werden.

* **Planen Sie zusätzliche Zeit für die QS ein.**

  Die Anzahl der Erlebnisse steigt, sodass die Qualitätssicherung länger dauert.

## Erstellen {#create}

* **Schließen Sie nicht mehr Kombinationen ein, als für den Test erforderlich sind.**

  Jede getestete Kombination erhöht das Traffic-Aufkommen und die erforderliche Zeit zur Erreichung annehmbarer Ergebnisse erheblich. Wenn Sie zum Beispiel über drei Orte mit je drei Angeboten verfügen, entspricht dies 27 möglichen Kombinationen (3 x 3 x 3). Drei Orte, von denen zwei Orte drei mögliche Angebote und ein Ort zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Ort und Angebot steigt die Anzahl erheblich.

* **Benennen Sie Standorte und Angebote.**

  Sie können jeden Ort und jedes Angebot in Ihrem Test umbenennen, sodass die Namen mehr Sinn ergeben. Die Anzahl der Angebote an jedem Ort erscheint im Orts-Header. Nützliche Namen helfen Ihnen, Ihre Angebote bei der Prüfung von Berichten zu identifizieren.

* **Nutzen Sie die Vorschaufunktionen, um unerwünschte Inhaltskombinationen zu vermeiden.**

  Prüfen Sie vor der Live-Schaltung alle Erlebnisse, die durch Ihren Test generiert wurden. Achten Sie darauf, dass keine Kombinationen mit widersprüchlichen Angaben (z. B. 20 % Rabatt und 19 $ Rabatt im selben Erlebnis) oder inkompatiblen Designs wie Hintergrund und Schriftart derselben Farbe vorhanden sind.

* **Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#traffic-estimator) um sicherzustellen, dass Ihr Test für den Traffic-Umfang konzipiert ist, den Ihre Seite erhält.**

  Stellen Sie sicher, dass **[!UICONTROL Traffic-Schätzung]** Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten können.

* **Machen Sie die Alternativen der einzelnen Elemente deutlich voneinander unterschiedlich.**

  Obwohl dies nicht erforderlich ist, empfiehlt es sich, für jedes Element dieselbe Anzahl von Alternativen zu verwenden.

## Analyse {#analyze}

* **Verwenden Sie regelmäßig den Bericht &quot;[Standort-Beitrag](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md)**, um die Leistung der einzelnen Standorte und Angebote zu überwachen.

* **Stützen Sie im [Erlebnisleistungsbericht](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) Ihre Entscheidungen auf die angezeigten Daten, indem Sie die Filter [!UICONTROL Best 5] und [!UICONTROL Worst 5] verwenden.**

  Der **[!UICONTROL Alle]**-Filter erschwert das Extrahieren der gewünschten Informationen, sodass nicht alle Erlebnisse im Diagramm angezeigt werden können. Verwenden Sie den **[!UICONTROL Alle]**-Filter, wenn Sie ein bestimmtes Erlebnis betrachten möchten, das nicht in den besten oder schlechtesten fünf liegt.

## Folgemaßnahmen {#follow-up}

* Auch wenn [!DNL Target] die Bearbeitung einer Live-Aktivität ermöglicht, **kann die Bearbeitung einer laufenden Aktivität den Test zurücksetzen.** In Berichten werden einige der Änderungen möglicherweise nicht erkannt. Änderungen an HTML-Angeboten können nur in der Angebotsbibliothek vorgenommen werden.

  Zu den spezifischen Aktionen zum Zurücksetzen von Erlebnisnamen und Berichten gehören:

  * Hinzufügen eines neuen Orts.
  * Löschen eines Orts.
  * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
  * Bearbeiten von Rich-Text-Angeboten
  * Bearbeiten von Angeboten mit Hintergrundfarbe

* **Wenn die Report Suite beim Bearbeiten einer Aktivität, die [!DNL Analytics] Metriken verwendet, nicht geladen wird (ein Zahlenauswahlfeld wird angezeigt),** die Metriken zu [!DNL Target] Metriken und dann erneut zu den [!DNL Analytics] Metriken wechseln. Die Berichtssuite sollte jetzt geladen werden.

* **Führen Sie einen MVT-Test mit einem oder mehreren A/B-** durch, um den bestmöglichen Inhalt für die gewünschten Ergebnisse zu ermitteln. Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie beispielsweise wissen, welche Orte am wichtigsten sind, testen Sie zwei bestimmte Bilder gegeneinander oder vergleichen Sie den Wortlaut oder die Farben einer call to action.
