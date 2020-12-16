---
keywords: mvt;multivariate test;multivariate test best practices;mvt best practices;mvt combinations;mvt reports
description: Tipps zur Verbesserung der Leistung, zum Vermeiden von Problemen und zum Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von Multivarianz-Test-Aktivitäten in Adobe Target auftreten könnten.
title: Best Practices für Multivarianz-Tests mit Adobe Target
feature: mvt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 100%

---


# Best Practices für Multivarianz-Tests{#multivariate-test-best-practices}

Tipps zur Verbesserung der Leistung, zum Vermeiden von Problemen und zum Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von Multivarianz-Test-Aktivitäten (MVT) in [!DNL Adobe Target] auftreten könnten.

## Planung   {#section_4D4A1F6226F042379BF48DB753608579}

* Beachten Sie die Orte auf Ihrer Seite, die wahrscheinlich signifikante Ergebnisse produzieren.

   Zum Beispiel führt ein Banner oder ein Heldenbild wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Orte mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Orte auf der Seite.
* Bereiten Sie Ihre Seitenvariationen vorab vor.

   Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Multivarianz-Test verwenden werden.

## Erstellung   {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Vermeiden Sie die Einbeziehung von mehr Kombinationen als für den Test notwendig.

   Jede getestete Kombination erhöht das Traffic-Aufkommen und die erforderliche Zeit zur Erreichung annehmbarer Ergebnisse erheblich. Wenn Sie zum Beispiel über drei Orte mit je drei Angeboten verfügen, entspricht dies 27 möglichen Kombinationen (3 x 3 x 3). Drei Orte, von denen zwei Orte drei mögliche Angebote und ein Ort zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Ort und Angebot steigt die Anzahl erheblich.

* Benennen Sie Orte und Angebote.

   Sie können jeden Ort und jedes Angebot in Ihrem Test umbenennen, sodass die Namen mehr Sinn ergeben. Die Anzahl der Angebote an jedem Ort erscheint im Orts-Header. Sinnvoll sind Namen, die Ihnen dabei helfen, Ihre Angebote bei der Auswertung von Berichten zu identifizieren.

* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden.

   Prüfen Sie vor der Live-Schaltung alle Erlebnisse, die durch Ihren Test generiert wurden. Stellen Sie sicher, dass es keine Kombinationen mit widersprüchlichen Behauptungen (zum Beispiel 20 % Rabatt und 19 $ Rabatt im selben Erlebnis) oder inkompatiblen Entwürfen wie gleiche Farbe für Hintergrund und Schrift gibt.

* Verwenden Sie die [Traffic-Schätzung](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md), um sicherzustellen, dass Ihr Test für das Datenverkehrsaufkommen konzipiert ist, das auf Ihrer Seite anfällt.

   Vergewissern Sie sich, dass die Traffic-Schätzung Ihre Testkonfiguration freigibt, sodass Sie die gewünschten Ergebnisse erhalten.
* Es wird empfohlen, dass sich die Alternativen der einzelnen Elemente deutlich voneinander unterscheiden.

## Analyse   {#section_9A2118CF1039451681C13D9AE79A58AB}

* Nutzen Sie den [Location Contribution-Bericht](/help/c-reports/location-contribution-report.md) regelmäßig, um die Leistung der einzelnen Orte und Angebote zu überwachen.
* Basieren Sie Ihre Entscheidungen im [Experience Performance-Bericht](/help/c-reports/experience-performance-report.md) auf Daten, die bei Nutzung der Filter „Beste 5“ und „Schlechteste 5“ angezeigt werden.

   Der Filter [!UICONTROL Alle] erschwert die Gewinnung der gewünschten Informationen und es ist nicht möglich, alle Erlebnisse im Diagramm anzuzeigen. Verwenden Sie den Filter [!UICONTROL Alle], wenn Sie ein spezifisches Erlebnis betrachten möchten, das nicht zu den besten oder schlechtesten fünf zählt.

## Nachbereitung   {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Obwohl [!DNL Target] Ihnen ermöglicht, eine Live-Aktivität zu bearbeiten, sollten Sie darauf achten, dass das Bearbeiten einer ausgeführten Aktivität zu einem Zurücksetzen des Tests führen kann. Berichte erkennen also möglicherweise manche Änderungen nicht. Es ist jedoch sicher, die Änderungen nur an den HTML-Angeboten in der Angebotsbibliothek vorzunehmen.

   Spezifische Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
   * Bearbeiten von Rich-Text-Angeboten
   * Bearbeiten von Angeboten mit Hintergrundfarbe

* Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

   Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie zum Beispiel wissen, welche Orte am wichtigsten sind, können Sie zwei spezifische Bilder vergleichend testen oder Wortlaut bzw. Farben eines Aktionsaufrufs vergleichen.

