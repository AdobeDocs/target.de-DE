---
description: Tipps zur Verbesserung der Leistung, Vermeiden von Problemen und Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von Multivarianz-Test-Aktivitäten in Adobe Target auftreten könnten.
keywords: MVT; Multivariater Test; Best Practices für Multivariater Test; Best Practices für MVT; MVT-Kombinationen; MVT-Berichte
seo-description: Tipps zur Verbesserung der Leistung, Vermeiden von Problemen und Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von Multivarianz-Test-Aktivitäten in Adobe Target auftreten könnten.
seo-title: Best Practices für Multivarianz-Tests mit Adobe Target
solution: Target
title: Best Practices für Multivarianz-Tests
topic: Standard
uuid: 4468a2eb-3fc1-4bc5-85ac-90cc02db4fbb
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Best Practices für Multivarianz-Tests{#multivariate-test-best-practices}

Tips to help you improve performance, avoid issues, and correct known issues that might occur when creating and running Multivariate Test (MVT) activities in [!DNL Adobe Target].

## Planung {#section_4D4A1F6226F042379BF48DB753608579}

* Beachten Sie die Orte auf Ihrer Seite, die wahrscheinlich signifikante Ergebnisse produzieren.

   Beispielsweise führt ein Banner oder ein Heldenbild wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Orte mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Orte auf der Seite.
* Bereiten Sie Ihre Seitenvariationen vorab vor.

   Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Multivarianz-Test verwenden werden.

## Erstellung {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Vermeiden Sie die Einbeziehung von mehr Kombinationen als für den Test notwendig.

   Jede getestete Kombination erhöht das Traffic-Aufkommen und die erforderliche Zeit zur Erreichung annehmbarer Ergebnisse erheblich. Wenn Sie beispielsweise drei Orte mit drei Angeboten haben, gibt es 27 mögliche Kombinationen (3 x 3 x 3). Drei Orte, an denen zwei Orte drei mögliche Angebote enthalten und ein Ort zwei Angebote enthält, stellen 18 Optionen bereit (3 x 3 x 2). Mit jedem zusätzlichen Ort und Angebot steigt die Anzahl erheblich.

* Benennen Sie Orte und Angebote.

   Sie können jeden Ort und jedes Angebot in Ihrem Test umbenennen, sodass die Namen mehr Sinn ergeben. Die Anzahl der Angebote an jedem Ort erscheint im Orts-Header. Sinnvoll sind Namen, die Ihnen dabei helfen, Ihre Angebote bei der Auswertung von Berichten zu identifizieren.

* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden.

   Prüfen Sie vor der Live-Schaltung alle Erlebnisse, die durch Ihren Test generiert wurden. Stellen Sie sicher, dass es keine Kombinationen mit widersprüchlichen Behauptungen (zum Beispiel 20 % Rabatt und 19 $ Rabatt im selben Erlebnis) oder inkompatiblen Entwürfen wie gleiche Farbe für Hintergrund und Schrift gibt.

* Use the [Traffic Estimator](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) to make sure that your test is designed for the amount of traffic your page receives.

   Vergewissern Sie sich, dass die Traffic-Schätzung Ihre Testkonfiguration freigibt, sodass Sie die gewünschten Ergebnisse erhalten.
* Es wird empfohlen, dass sich die Alternativen der einzelnen Elemente deutlich voneinander unterscheiden.

## Analyse {#section_9A2118CF1039451681C13D9AE79A58AB}

* Make frequent use of the [Location Contribution report](/help/c-reports/location-contribution-report.md) to monitor the performance of each location and each offer.
* In the [Experience Performance report](/help/c-reports/experience-performance-report.md), base your decisions on the data shown using the Best 5 and Worst 5 filters.

   The [!UICONTROL All] filter makes it difficult to extract the desired information, and not all experiences can display in the graph. Use the [!UICONTROL All] filter if you want to look at a specific experience that is not in the best or worst five.

## Nachbereitung {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Although [!DNL Target] allows you to edit a live activity, be aware that editing an activity that is in progress could reset the test. Berichte erkennen also möglicherweise manche Änderungen nicht. Es ist jedoch sicher, die Änderungen nur an den HTML-Angeboten in der Angebotsbibliothek vorzunehmen.

   Spezifische Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
   * Bearbeiten von Rich-Text-Angeboten
   * Bearbeiten von Angeboten mit Hintergrundfarbe

* Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

   Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie zum Beispiel wissen, welche Orte am wichtigsten sind, können Sie zwei spezifische Bilder vergleichend testen oder Wortlaut bzw. Farben eines Aktionsaufrufs vergleichen.

