---
keywords: MVT; Multivarianz-Test; Best Practices für Multivarianz-Test; Best Practices für MVT; MVT-Kombinationen; MVT-Berichte
description: Erfahren Sie, wie Sie die Leistung verbessern, Probleme vermeiden und bekannte Probleme korrigieren, die beim Erstellen und Ausführen von [!UICONTROL Multivariate Test] in auftreten können [!DNL Adobe Target].
title: Welche Best Practices gibt es für eine [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 57%

---

# Best Practices für [!UICONTROL Multivariate Test]

Tipps zur Verbesserung der Leistung, zum Vermeiden von Problemen und Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von [!UICONTROL Multivariate Test] (MVT)-Aktivitäten in [!DNL Adobe Target] auftreten könnten.

## Planung  {#section_4D4A1F6226F042379BF48DB753608579}

* Beachten Sie die Orte auf Ihrer Seite, die wahrscheinlich signifikante Ergebnisse produzieren.

  Zum Beispiel führt ein Banner oder ein Hero Image wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Orte mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Orte auf der Seite.
* Bereiten Sie Ihre Seitenvarianzen vorab vor.

  Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Multivarianz-Test verwenden werden.

## Erstellung  {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Vermeiden Sie die Einbeziehung von mehr Kombinationen als für den Test notwendig.

  Jede getestete Kombination erhöht das Traffic-Aufkommen und die erforderliche Zeit zur Erreichung annehmbarer Ergebnisse erheblich. Wenn Sie zum Beispiel über drei Orte mit je drei Angeboten verfügen, entspricht dies 27 möglichen Kombinationen (3 x 3 x 3). Drei Orte, von denen zwei Orte drei mögliche Angebote und ein Ort zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Ort und Angebot steigt die Anzahl erheblich.

* Benennen Sie Orte und Angebote.

  Sie können jeden Ort und jedes Angebot in Ihrem Test umbenennen, sodass die Namen mehr Sinn ergeben. Die Anzahl der Angebote an jedem Ort erscheint im Orts-Header. Nützliche Namen helfen Ihnen, Ihre Angebote bei der Prüfung von Berichten zu identifizieren.

* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden.

  Prüfen Sie vor der Live-Schaltung alle Erlebnisse, die durch Ihren Test generiert wurden. Achten Sie darauf, dass keine Kombinationen mit widersprüchlichen Angaben (z. B. 20 % Rabatt und 19 $ Rabatt im selben Erlebnis) oder inkompatiblen Designs wie Hintergrund und Schriftart derselben Farbe vorhanden sind.

* Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md), um sicherzustellen, dass Ihr Test für das Datenverkehrsaufkommen konzipiert ist, das auf Ihrer Seite anfällt.

  Stellen Sie sicher, dass die Traffic-Schätzung Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten.

* Die Alternativen der einzelnen Elemente sollten sich deutlich voneinander unterscheiden.

## Analyse  {#section_9A2118CF1039451681C13D9AE79A58AB}

* Verwenden Sie regelmäßig den Bericht [Standortbeitrag](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md), um die Leistung der einzelnen Standorte und Angebote zu überwachen.
* Stützen [ im Experience](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md)Leistungsbericht Ihre Entscheidungen auf die angezeigten Daten, indem Sie die [!UICONTROL Best 5]- und [!UICONTROL Worst 5] verwenden.

  Der [!UICONTROL All] erschwert die Extraktion der gewünschten Informationen, und es können nicht alle Erlebnisse im Diagramm angezeigt werden. Verwenden Sie den [!UICONTROL All] Filter, wenn Sie ein bestimmtes Erlebnis betrachten möchten, das nicht in den besten oder schlechtesten fünf liegt.

## Nachbereitung  {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Auch wenn Sie mit [!DNL Target] eine Live-Aktivität bearbeiten können, kann das Bearbeiten einer laufenden Aktivität den Test zurücksetzen. In Berichten werden einige der Änderungen möglicherweise nicht erkannt. Es ist jedoch sicher, die Änderungen nur an den HTML-Angeboten in der Angebotsbibliothek vorzunehmen.

  Spezifische Aktionen zum Zurücksetzen von Erlebnisnamen und Berichten:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
   * Bearbeiten von Rich-Text-Angeboten
   * Bearbeiten von Angeboten mit Hintergrundfarbe

* Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

  Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie beispielsweise wissen, welche Orte am wichtigsten sind, testen Sie zwei bestimmte Bilder gegeneinander oder vergleichen Sie den Wortlaut oder die Farben einer call to action.
