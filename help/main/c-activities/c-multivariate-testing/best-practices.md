---
keywords: MVT; Multivarianz-Test; Best Practices für Multivarianz-Test; Best Practices für MVT; MVT-Kombinationen; MVT-Berichte
description: Erfahren Sie, wie Sie die Leistung verbessern, Probleme vermeiden und bekannte Probleme korrigieren, die beim Erstellen und Ausführen von [!UICONTROL Multivarianz-Test]-Aktivitäten in auftreten  [!DNL Adobe Target].
title: Welche Best Practices gibt es für [!UICONTROL &#x200B; Aktivität „Multivariater &#x200B;]"?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
TQID: https://experienceleague.adobe.com/nQEf5GZ8-zVZakygPtMAYWk-xoJPdcycFbzCNKTqJ-k
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 625
ht-degree: 55%

---

# [!UICONTROL Multivarianz-Test] Best Practices

Tipps zur Verbesserung der Leistung, zum Vermeiden von Problemen und Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von [!UICONTROL Multivarianz-Test]&#x200B;(MVT)-Aktivitäten in [!DNL Adobe Target] auftreten könnten.

## Planung {#section_4D4A1F6226F042379BF48DB753608579}

* Beachten Sie die Orte auf Ihrer Seite, die wahrscheinlich signifikante Ergebnisse produzieren.

  Zum Beispiel führt ein Banner oder ein Hero Image wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Orte mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Orte auf der Seite.
* Bereiten Sie Ihre Seitenvarianzen vorab vor.

  Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Multivarianz-Test verwenden werden.

## Erstellung {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Vermeiden Sie die Einbeziehung von mehr Kombinationen als für den Test notwendig.

  Jede getestete Kombination erhöht das Traffic-Aufkommen und die erforderliche Zeit zur Erreichung annehmbarer Ergebnisse erheblich. Wenn Sie zum Beispiel über drei Orte mit je drei Angeboten verfügen, entspricht dies 27 möglichen Kombinationen (3 x 3 x 3). Drei Orte, von denen zwei Orte drei mögliche Angebote und ein Ort zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Ort und Angebot steigt die Anzahl erheblich.

* Benennen Sie Orte und Angebote.

  Sie können jeden Ort und jedes Angebot in Ihrem Test umbenennen, sodass die Namen mehr Sinn ergeben. Die Anzahl der Angebote an jedem Ort erscheint im Orts-Header. Nützliche Namen helfen Ihnen, Ihre Angebote bei der Prüfung von Berichten zu identifizieren.

* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden.

  Prüfen Sie vor der Live-Schaltung alle Erlebnisse, die durch Ihren Test generiert wurden. Achten Sie darauf, dass keine Kombinationen mit widersprüchlichen Angaben (z. B. 20 % Rabatt und 19 $ Rabatt im selben Erlebnis) oder inkompatiblen Designs wie Hintergrund und Schriftart derselben Farbe vorhanden sind.

* Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md), um sicherzustellen, dass Ihr Test für das Datenverkehrsaufkommen konzipiert ist, das auf Ihrer Seite anfällt.

  Stellen Sie sicher, dass die Traffic-Schätzung Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten.

* Die Alternativen der einzelnen Elemente sollten sich deutlich voneinander unterscheiden.

## Analyse {#section_9A2118CF1039451681C13D9AE79A58AB}

* Verwenden Sie regelmäßig den Bericht [Standortbeitrag](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md), um die Leistung der einzelnen Standorte und Angebote zu überwachen.
* Stützen [&#x200B; im Experience](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md)Leistungsbericht Ihre Entscheidungen auf die angezeigten Daten, indem Sie die Filter [!UICONTROL Best 5] und [!UICONTROL Worst 5] verwenden.

  Der [!UICONTROL Alle]-Filter erschwert das Extrahieren der gewünschten Informationen, sodass nicht alle Erlebnisse im Diagramm angezeigt werden können. Verwenden Sie den [!UICONTROL Alle]-Filter, wenn Sie ein bestimmtes Erlebnis betrachten möchten, das nicht in den besten oder schlechtesten fünf liegt.

## Nachbereitung {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Auch wenn Sie mit [!DNL Target] eine Live-Aktivität bearbeiten können, kann das Bearbeiten einer laufenden Aktivität den Test zurücksetzen. In Berichten werden einige der Änderungen möglicherweise nicht erkannt. Es ist jedoch sicher, die Änderungen nur an den HTML-Angeboten in der Angebotsbibliothek vorzunehmen.

  Spezifische Aktionen zum Zurücksetzen von Erlebnisnamen und Berichten:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
   * Bearbeiten von Rich-Text-Angeboten
   * Bearbeiten von Angeboten mit Hintergrundfarbe

* Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

  Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie beispielsweise wissen, welche Orte am wichtigsten sind, testen Sie zwei bestimmte Bilder gegeneinander oder vergleichen Sie den Wortlaut oder die Farben einer call to action.
