---
keywords: MVT; Multivarianz-Test; Best Practices für Multivarianz-Test; Best Practices für MVT; MVT-Kombinationen; MVT-Berichte
description: Erfahren Sie, wie Sie die Leistung verbessern, Probleme vermeiden und bekannte Probleme korrigieren können, die beim Erstellen und Ausführen von [!UICONTROL Multivariate Test] -Aktivitäten in  [!DNL Adobe Target] auftreten können.
title: Welche Best Practices gelten für eine [!UICONTROL Multivariate Test] -Aktivität?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 57%

---

# [!UICONTROL Multivariate Test] Best Practices

Tipps zur Verbesserung der Leistung, zum Vermeiden von Problemen und zum Korrigieren bekannter Probleme, die beim Erstellen und Ausführen von [!UICONTROL Multivariate Test] -Aktivitäten (MVT) in [!DNL Adobe Target] auftreten können.

## Planung  {#section_4D4A1F6226F042379BF48DB753608579}

* Beachten Sie die Orte auf Ihrer Seite, die wahrscheinlich signifikante Ergebnisse produzieren.

  Zum Beispiel führt ein Banner oder ein Heldenbild wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Orte mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Orte auf der Seite.
* Bereiten Sie Ihre Seitenvarianzen vorab vor.

  Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Multivarianz-Test verwenden werden.

## Erstellung  {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Vermeiden Sie die Einbeziehung von mehr Kombinationen als für den Test notwendig.

  Jede getestete Kombination erhöht das Traffic-Aufkommen und die erforderliche Zeit zur Erreichung annehmbarer Ergebnisse erheblich. Wenn Sie zum Beispiel über drei Orte mit je drei Angeboten verfügen, entspricht dies 27 möglichen Kombinationen (3 x 3 x 3). Drei Orte, von denen zwei Orte drei mögliche Angebote und ein Ort zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Ort und Angebot steigt die Anzahl erheblich.

* Benennen Sie Orte und Angebote.

  Sie können jeden Ort und jedes Angebot in Ihrem Test umbenennen, sodass die Namen mehr Sinn ergeben. Die Anzahl der Angebote an jedem Ort erscheint im Orts-Header. Nützliche Namen helfen Ihnen bei der Identifizierung Ihrer Angebote bei der Überprüfung von Berichten.

* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden.

  Prüfen Sie vor der Live-Schaltung alle Erlebnisse, die durch Ihren Test generiert wurden. Stellen Sie sicher, dass es keine Kombinationen mit widersprüchlichen Behauptungen (z. B. 20 % Rabatt und 19 Euro Rabatt im selben Erlebnis) oder inkompatiblen Designs wie mit Hintergrund und Schrift derselben Farbe gibt.

* Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md), um sicherzustellen, dass Ihr Test für das Datenverkehrsaufkommen konzipiert ist, das auf Ihrer Seite anfällt.

  Stellen Sie sicher, dass die Traffic-Schätzung Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten.

* Die Alternativen jedes Elements sollten sich deutlich voneinander unterscheiden.

## Analyse  {#section_9A2118CF1039451681C13D9AE79A58AB}

* Nutzen Sie den [Location Contribution-Bericht](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) regelmäßig, um die Leistung der einzelnen Orte und Angebote zu überwachen.
* Basieren Sie Ihre Entscheidungen im Bericht [ Erlebnisleistung](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) auf den Daten, die mit den Filtern [!UICONTROL Best 5] und [!UICONTROL Worst 5] angezeigt werden.

  Der Filter [!UICONTROL All] erschwert die Gewinnung der gewünschten Informationen und es ist nicht möglich, alle Erlebnisse im Diagramm anzuzeigen. Verwenden Sie den Filter [!UICONTROL All] , wenn Sie ein bestimmtes Erlebnis betrachten möchten, das nicht zu den besten oder schlechtesten fünf zählt.

## Nachbereitung  {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Auch wenn [!DNL Target] es Ihnen ermöglicht, eine Live-Aktivität zu bearbeiten, kann die Bearbeitung einer laufenden Aktivität den Test zurücksetzen. In Berichten werden einige der Änderungen möglicherweise nicht erkannt. Es ist jedoch sicher, die Änderungen nur an den HTML-Angeboten in der Angebotsbibliothek vorzunehmen.

  Zu den spezifischen Aktionen, die Erlebnisnamen und Berichte zurücksetzen, gehören:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Speicherort
   * Bearbeiten von Rich-Text-Angeboten
   * Bearbeiten von Angeboten mit Hintergrundfarbe

* Mit der Durchführung eines oder mehrerer A/B-Tests im Anschluss an einen Multivarianz-Test können Sie den bestmöglichen Inhalt für die von Ihnen gewünschten Ergebnisse ermitteln.

  Sobald Sie ermittelt haben, welche Orte und Inhalte Sie am besten bei der Erreichung Ihrer Ziele unterstützen, können Sie einen A/B-Test ausführen, um die Ergebnisse weiter zu verfeinern. Wenn Sie beispielsweise wissen, welche Orte am wichtigsten sind, testen Sie zwei spezifische Bilder miteinander oder vergleichen Sie den Wortlaut oder die Farben eines Aktionsaufrufs.
