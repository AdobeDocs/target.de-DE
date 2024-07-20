---
keywords: Aktivitätseinstellungen; Ziele und Einstellungen; Multivarianz; MVT
description: Erfahren Sie, wie Sie mit der Seite "[!UICONTROL Goals & Settings]"in  [!DNL Adobe Target]  Informationen über die Ziele einer [!UICONTROL Multivariate Test] -Aktivität (MVT) angeben.
title: Wie gebe ich Ziele und Einstellungen in einer [!UICONTROL Multivariate Test] -Aktivität (MVT) an?
feature: Multivariate Tests
exl-id: 823a1435-ccb9-4357-9c33-a0968d704b7a
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 41%

---

# Ziele und Einstellungen ([!UICONTROL Multivariate Test])

Auf der Seite [!UICONTROL Goals & Settings] in [!DNL Adobe Target] geben Sie Informationen über die Ziele Ihrer [!UICONTROL Multivariate Test] -Aktivitäten (MVT) ein.

Die folgenden Abschnitte sind verfügbar:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

Die verfügbaren Einstellungen in den einzelnen Abschnitten hängen davon ab, ob Sie [!DNL Target] oder [!DNL Analytics] als Berichtsquelle verwenden.

## Aktivitätseinstellungen {#section_DCBDC354261F420EBD4B43EA34947BAC}

Die folgenden Einstellungen sind verfügbar:

### Ziel

Geben Sie ein optionales Ziel ein. Beim Ziel kann es sich um beliebige Informationen handeln, die Ihnen und Ihren Team-Mitgliedern beim Identifizieren der Kampagne helfen.

### Priorität

Abhängig von Ihren Einstellungen variieren die [!DNL Target]-Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die veralteten Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder genauer unterteilte Prioritäten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Wenn diese Option unter [!UICONTROL Administration] > [!UICONTROL Reporting] (Standardeinstellung) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].

Um genauer unterteilte Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und stellen Sie dann die Option [!UICONTROL Enable Fine-Grained Priorities] auf die Position &quot;Ein&quot;.

Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:

* 0 = Niedrig
* 999 = Hoch

Bei Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden, wird die Priorität [!UICONTROL Low] in 0, die Priorität [!UICONTROL Medium] in 5 und die Priorität [!UICONTROL High] in 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Wenn Sie genauer unterteilte Prioritäten verwendet haben und die Option deaktivieren möchten, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden.

### Dauer

Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## Berichterstellungseinstellungen  {#section_13119392051044FBA6387D9B3B1C43CF}

Die folgenden Einstellungen sind verfügbar:

### Berichtsquelle

Geben Sie an, aus welchen Lösungsdaten erfasst werden:

* [!DNL Adobe Target]
* [!DNL Adobe Analytics]
* [!DNL Adobe Customer Journey Analytics]

Wenn in Ihren [Kontoeinstellungen](/help/main/administrating-target/reporting.md) eine Berichterstellungslösung angegeben ist, wird die angegebene Lösung verwendet und diese Einstellung ist nicht sichtbar.

Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten.

**[!DNL Adobe Analytics]**: Siehe [[!DNL Adobe Analytics]  als Berichtsquelle für  [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) , um mehr über die Unterschiede zwischen den Berichterstellungslösungen und deren Vorteile zu erfahren.

Wenn Sie [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) auswählen, wählen Sie eine [!DNL Analytics] Report Suite aus, die [!DNL Target] Aktivitätsdaten erhält. Wählen Sie dazu zunächst ein [!DNL Analytics] Unternehmen aus, an das Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Target] bereitgestellt wurden. Wenn die erwartete Report Suite nicht angezeigt wird, versuchen Sie zunächst, sich abzumelden und sich wieder bei [!DNL Adobe Experience Cloud] anzumelden, um es erneut zu versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

Für [!DNL Analytics for Target] (A4T) ist ein Tracking-Server erforderlich, um Ergebnisse korrekt zu melden. Im Feld [!UICONTROL Tracking Server] wird ein standardmäßiger Trackingserver angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie in dieses Feld den richtigen Tracking-Server einschließen. Weitere Informationen finden Sie unter [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) .

**[!DNL Adobe Customer Journey Analytics]**: Weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target] finden Sie unter [[!DNL Target] Berichterstellung in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) .

### Zielmetrik

Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine Metrik vom Typ [!UICONTROL Conversion] und legen Sie dann die Parameter fest, die bestimmen, wann ein Erfolg erreicht wird.

>[!NOTE]
>
>Wenn die Berichterstellungslösung auf &quot;[!DNL Analytics]&quot; eingestellt ist, ist die einzige verfügbare Zielmetrik &quot;[!UICONTROL Conversion]&quot;. [!DNL Analytics] -Metriken können nicht als Ziel ausgewählt werden.

Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.

Wenn diese Option aktiviert ist, bietet das Feld [!UICONTROL Estimated Value of the Conversion] (nicht verfügbar für die Metriken [!UICONTROL Page Score] ) einen Wert für Ihr Ziel, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] und [!UICONTROL Orders]) verwendet die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung.

Nach Erreichen des Aktivitätsziels sieht ein Besucher weiterhin den Aktivitätsinhalt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dieses Verhalten unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie den Test erneut sehen.

### Zusätzliche Metriken

Erstellen Sie zusätzliche Erfolgsmetriken.

Diese Einstellung ist nicht verfügbar, wenn die Berichterstellungslösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet.

### Zielgruppen für die Berichterstellung

Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen über bestimmte Zielgruppen zu zeigen.

### Erweiterte Einstellungen   {#section_E2FE441AFB324E498793ABB025ED9974}

Erweiterte Einstellungen sind für [!UICONTROL Multivariate Test] -Zielmetriken verfügbar.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/Menu_AdvancedSettings.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option für erweiterte Einstellungen ist nicht verfügbar.

#### Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird?

Verwenden Sie diese Option, um nur Personen zu zählen, die die Erfolgsmetrik erreicht haben, wenn sie zuvor eine andere Erfolgsmetrik erreicht haben. Beispielsweise kann eine Testkonversion nur dann gültig sein, wenn der Besucher auf das Angebot klickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.

Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine Abhängigkeit voneinander festlegen können.

Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf **[!UICONTROL Advanced Settings]**.
2. Klicken Sie auf die Option **[!UICONTROL Add Dependency]** :

   ![Abhängigkeit hinzufügen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency.png)

3. Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf **[!UICONTROL Reached]** , um die Einstellung zwischen Erreicht und Nicht erreicht zu wechseln.

   ![Abhängigkeit erreicht](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency_reached.png)

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?

Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:

* [!UICONTROL Select Increment Count & Keep User in Activity] , um anzugeben, wie die Anzahl erhöht wird.
* [!UICONTROL Select Increment Count, Release User & Allow Reentry] , um das Erlebnis anzugeben, das dem Benutzer angezeigt wird, wenn er die Aktivität erneut aufruft.
* [!UICONTROL Select Increment Count, Release User & Bar from Reentry] , um anzugeben, was der Benutzer anstelle des Aktivitätsinhalts sieht.

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Die folgende Einstellung ist verfügbar:

### Hinweise

Geben Sie alle Informationen über Ihre Aktivität ein, die für Sie oder andere Teammitglieder nützlich sind. Die Größe des Bereichs [!UICONTROL Notes] kann geändert werden.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätseinstellungen (3:02)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)

### Erstellen von multivariaten Tests (9:25)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Arbeitsablaufs mit drei Schritten ein Multivarianz-Test erstellt wird. Ziele und Einstellungen werden ab 7:00 erläutert.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395)
