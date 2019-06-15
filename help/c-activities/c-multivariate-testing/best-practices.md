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
source-git-commit: 25ec122f7ab577f89e2330155599077e684605aa

---


# Best Practices für Multivarianz-Tests{#multivariate-test-best-practices}

Tipps zur Verbesserung der Leistung, Vermeidung von Problemen und Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von Multivarianz-Tests (MVT) auftreten [!DNL Adobe Target]können.

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

* Verwenden Sie die [Traffic-Schätzung](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) , um sicherzustellen, dass Ihr Test für den Traffic entworfen wurde, den Ihre Seite erhält.

   Vergewissern Sie sich, dass die Traffic-Schätzung Ihre Testkonfiguration freigibt, sodass Sie die gewünschten Ergebnisse erhalten.
* Es wird empfohlen, dass sich die Alternativen der einzelnen Elemente deutlich voneinander unterscheiden.

## Analyse {#section_9A2118CF1039451681C13D9AE79A58AB}

* Verwenden Sie den [Location Contribution-Bericht](/help/c-reports/location-contribution-report.md) häufig, um die Leistung jeder Position und jedes Angebots zu überwachen.
* Basieren Sie im [Experience Performance-Bericht](/help/c-reports/experience-performance-report.md)auf den Daten, die mit den Filter &quot;Beste 5&quot; und&quot; Schlechteste 5&quot; angezeigt werden.

   Mit dem Filter [!UICONTROL &quot;Alle&quot;] ist es schwierig, die gewünschten Informationen zu extrahieren, und nicht alle Erlebnisse können im Diagramm angezeigt werden. Verwenden Sie den [!UICONTROL Filter &quot;Alle&quot;] , wenn Sie ein spezifisches Erlebnis betrachten möchten, das sich nicht in den besten oder schlechtesten fünf unterscheidet.

## Nachbereitung {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Auch wenn [!DNL Target] Sie eine Live-Aktivität bearbeiten können, sollten Sie beachten, dass die Bearbeitung einer aktiven Aktivität den Test zurücksetzen könnte. Berichte erkennen also möglicherweise manche Änderungen nicht. Es ist jedoch sicher, die Änderungen nur an den HTML-Angeboten in der Angebotsbibliothek vorzunehmen.

   Spezifische Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
   * Bearbeiten von Rich-Text-Angeboten
   * Bearbeiten von Angeboten mit Hintergrundfarbe

* Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

   Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie zum Beispiel wissen, welche Orte am wichtigsten sind, können Sie zwei spezifische Bilder vergleichend testen oder Wortlaut bzw. Farben eines Aktionsaufrufs vergleichen.

