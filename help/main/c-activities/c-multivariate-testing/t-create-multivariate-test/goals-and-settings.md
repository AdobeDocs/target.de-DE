---
keywords: Aktivitätseinstellungen;Ziele und Einstellungen;Multivariate;MVT
description: Erfahren Sie, wie Sie auf der Seite [!UICONTROL Goals & Settings] in  [!DNL Adobe Target]  Informationen zu den Zielen einer [!UICONTROL Multivariate Test] (MVT)-Aktivität angeben können.
title: Wie gebe ich Ziele und Einstellungen in einer [!UICONTROL Multivariate Test] (MVT)-Aktivität an?
feature: Multivariate Tests
exl-id: 823a1435-ccb9-4357-9c33-a0968d704b7a
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 38%

---

# Ziele und Einstellungen [!UICONTROL Multivariate Test]

Auf der [!UICONTROL Goals & Settings] Seite in [!DNL Adobe Target] geben Sie Informationen zu den Zielen Ihrer [!UICONTROL Multivariate Test] (MVT)-Aktivitäten ein.

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

Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die Legacy-Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Wenn diese Option in [!UICONTROL Administration] > [!UICONTROL Reporting] (Standard) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].

Um die feinabgestimmten Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und schalten Sie die Option [!UICONTROL Enable Fine-Grained Priorities] auf „Ein“.

Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:

* 0 = Niedrig
* 999 = Hoch

Für Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden, wird [!UICONTROL Low] Priorität in 0, [!UICONTROL Medium] Priorität in 5 und [!UICONTROL High] Priorität in 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Wenn Sie genauer unterteilte Prioritäten verwendet haben und die Option deaktivieren möchten, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden.

### Dauer

Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00 :00 Mitternacht ist. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## Berichterstellungseinstellungen  {#section_13119392051044FBA6387D9B3B1C43CF}

Die folgenden Einstellungen sind verfügbar:

### Berichtsquelle

Geben Sie an, aus welcher Lösung Daten erfasst werden:

* [!DNL Adobe Target]
* [!DNL Adobe Analytics]
* [!DNL Adobe Customer Journey Analytics]

Wenn in Ihren [Kontoeinstellungen“ eine Berichtslösung angegeben ist](/help/main/administrating-target/reporting.md) wird die angegebene Lösung verwendet, und diese Einstellung ist nicht sichtbar.

Sie können Ihre Berichtsquelle nicht ändern, nachdem die Aktivität live geschaltet wurde, um die Konsistenz der Berichte zu gewährleisten.

**[!DNL Adobe Analytics]**: Unter [[!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) erfahren Sie mehr über die Unterschiede zwischen den Berichtslösungen und deren Vorteile.

Bei der Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) wählen Sie eine [!DNL Analytics] Report Suite aus, um [!DNL Target] Aktivitätsdaten zu erhalten. Wählen Sie dazu zunächst eines der [!DNL Analytics] Unternehmen aus, mit denen Ihr Konto verknüpft ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Target] bereitgestellt wurden. Wenn die erwartete Report Suite nicht angezeigt wird, versuchen Sie zunächst, sich abzumelden und sich wieder bei der [!DNL Adobe Experience Cloud] anzumelden, um es dann erneut zu versuchen. Wenn die Report Suite noch fehlt, wenden Sie sich an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) erfordert einen Trackingserver, um Ergebnisse korrekt zu melden. Im Feld [!UICONTROL Tracking Server] wird ein standardmäßiger Tracking-Server angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie den richtigen Tracking-Server in dieses Feld einbeziehen. Weitere Informationen finden [&#x200B; unter „Verwenden eines Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)Trackingservers“.

**[!DNL Adobe Customer Journey Analytics]**: Siehe [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) für weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target].

### Zielmetrik

Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Conversion] Metrik aus und legen Sie dann die Parameter fest, die bestimmen, wann der Erfolg erzielt wird.

>[!NOTE]
>
>Wenn die Reporting-Lösung auf [!DNL Analytics] eingestellt ist, ist die einzige verfügbare Zielmetrik [!UICONTROL Conversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden.

Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.

Wenn diese Option aktiviert ist, liefert das Feld [!UICONTROL Estimated Value of the Conversion] (für die [!UICONTROL Page Score] Metriken nicht verfügbar) einen Wert für Ihr Ziel, aber nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] und [!UICONTROL Orders]) nutzt die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung.

Nach Erreichen des Aktivitätsziels wird einem Besucher weiterhin der Aktivitätsinhalt angezeigt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dieses Verhalten unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie den Test erneut sehen.

### Zusätzliche Metriken

Erstellen Sie zusätzliche Erfolgsmetriken.

Diese Einstellung ist nicht verfügbar, wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet.

### Zielgruppen für die Berichterstellung

Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen über bestimmte Zielgruppen zu zeigen.

### Erweiterte Einstellungen   {#section_E2FE441AFB324E498793ABB025ED9974}

Für [!UICONTROL Multivariate Test] Zielmetriken sind erweiterte Einstellungen verfügbar.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/Menu_AdvancedSettings.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option „Erweiterte Einstellungen“ ist nicht verfügbar.

#### Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird?

Verwenden Sie diese Option, um zu zählen, dass eine Person die Erfolgsmetrik nur dann erreicht, wenn sie zuvor eine andere Erfolgsmetrik erreicht hat. Beispielsweise ist eine Testkonvertierung möglicherweise nur gültig, wenn der Besucher auf das Angebot klickt oder vor der Konvertierung auf eine bestimmte Seite gelangt.

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.

Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine von einer anderen abhängig machen können.

Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Nachdem Sie zusätzliche Metriken hinzugefügt haben, klicken Sie auf **[!UICONTROL Advanced Settings]**.
2. Klicken Sie auf die Option **[!UICONTROL Add Dependency]** :

   ![Abhängigkeit hinzufügen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency.png)

3. Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf **[!UICONTROL Reached]** , um zwischen Erreichen und Nicht erreicht umzuschalten.

   ![Abhängigkeit erreicht](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency_reached.png)

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?

Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:

* [!UICONTROL Select Increment Count & Keep User in Activity], um anzugeben, wie die Anzahl erhöht wird.
* [!UICONTROL Select Increment Count, Release User & Allow Reentry], um das Erlebnis festzulegen, das Benutzenden angezeigt wird, wenn sie die Aktivität erneut aufrufen.
* [!UICONTROL Select Increment Count, Release User & Bar from Reentry], um anzugeben, was der Benutzer anstelle des Aktivitätsinhalts sieht.

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Die folgende Einstellung ist verfügbar:

### Hinweise

Geben Sie alle Informationen zu Ihrer Aktivität ein, die für Sie selbst oder andere Team-Mitglieder nützlich sind. Die Größe des [!UICONTROL Notes] Fensterbereichs kann geändert werden.

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

### Erstellen von Multivarianz-Tests (9:25)

In diesem Video wird gezeigt, wie Sie mit dem [!DNL Target] dreistufigen Workflow einen Multivarianz-Test erstellen. Die Ziele und Einstellungen werden ab 7 :00 erläutert.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/30168?captions=ger)
