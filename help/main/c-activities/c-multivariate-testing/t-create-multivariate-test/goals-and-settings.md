---
keywords: Aktivitätseinstellungen;Ziele und Einstellungen;Multivariate;MVT
description: Erfahren Sie, wie Sie auf der Seite [!UICONTROL Ziele und Einstellungen] in [!DNL Adobe Target]  Informationen zu den Zielen einer [!UICONTROL Multivarianz-Test]-Aktivität (MVT) angeben.
title: Wie gebe ich Ziele und Einstellungen in einer Aktivität [!UICONTROL Multivariater Test] (MVT) an?
feature: Multivariate Tests
exl-id: 823a1435-ccb9-4357-9c33-a0968d704b7a
TQID: https://experienceleague.adobe.com/FKRQnliVYaVby-SiFunkRWX7iFMi76JAP3D3TKUdMXE
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1261
ht-degree: 39%

---

# Ziele und Einstellungen ([!UICONTROL Multivarianz-])

Auf [!UICONTROL &#x200B; Seite „Ziele &#x200B;] Einstellungen“ in [!DNL Adobe Target] geben Sie Informationen zu den Zielen Ihrer [!UICONTROL Multivarianz-Test]-Aktivitäten (MVT) ein.

Die folgenden Abschnitte sind verfügbar:

* [!UICONTROL Aktivitätseinstellungen]
* [!UICONTROL Berichterstellungseinstellungen]
* [!UICONTROL Sonstige Metadaten]

Die verfügbaren Einstellungen in den einzelnen Abschnitten hängen davon ab, ob Sie [!DNL Target] oder [!DNL Analytics] als Berichtsquelle verwenden.

## Aktivitätseinstellungen {#section_DCBDC354261F420EBD4B43EA34947BAC}

Die folgenden Einstellungen sind verfügbar:

### Ziel

Geben Sie ein optionales Ziel ein. Beim Ziel kann es sich um beliebige Informationen handeln, die Ihnen und Ihren Team-Mitgliedern beim Identifizieren der Kampagne helfen.

### Priorität

Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priorität]. Sie können die Legacy-Einstellungen von [!UICONTROL Niedrig], [!UICONTROL Medium] oder [!UICONTROL Hoch] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Wenn diese Option in [!UICONTROL Administration] > [!UICONTROL Reporting] (Standard) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Niedrig], [!UICONTROL Medium] oder [!UICONTROL Hoch].

Um feinabgestimmte Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und schalten Sie dann die Option [!UICONTROL Feinabgestimmte Prioritäten aktivieren] auf „Ein“ um.

Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:

* 0 = Niedrig
* 999 = Hoch

Für Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden[!UICONTROL &#x200B; wird die Priorität „Niedrig] in 0, die Priorität [!UICONTROL Medium] in 5 und die Priorität [!UICONTROL Hoch] in 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Wenn Sie genauer unterteilte Prioritäten verwendet haben und die Option deaktivieren möchten, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden.

### Dauer

Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00 :00 Mitternacht ist. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## Berichterstellungseinstellungen {#section_13119392051044FBA6387D9B3B1C43CF}

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

[!DNL Analytics for Target] (A4T) erfordert einen Trackingserver, um Ergebnisse korrekt zu melden. Im Feld [!UICONTROL Tracking-Server] wird ein standardmäßiger Tracking-Server angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie den richtigen Tracking-Server in dieses Feld einbeziehen. Weitere Informationen finden [&#x200B; unter „Verwenden eines Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)Trackingservers“.

**[!DNL Adobe Customer Journey Analytics]**: Siehe [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) für weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target].

### Zielmetrik

Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine Metrik [!UICONTROL Konversion] und legen Sie dann die Parameter fest, die bestimmen, wann der Erfolg erzielt wird.

>[!NOTE]
>
>Wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist, ist die einzige verfügbare Zielmetrik [!UICONTROL Konversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden.

Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.

Wenn diese Option aktiviert ist[!UICONTROL &#x200B; liefert der Feld „Geschätzter Wert der Konversion] (für die Metriken [!UICONTROL Seitenbewertung] nicht verfügbar) einen Wert für Ihr Ziel, aber nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Umsatz pro Besucher], [!UICONTROL Durchschnittlicher Bestellwert], [!UICONTROL Gesamtumsatz] und [!UICONTROL Bestellungen]) verwendet die Schätzung [!UICONTROL Umsatz pro Besucher]. Der Datentyp ist eine Währung.

Nach Erreichen des Aktivitätsziels wird einem Besucher weiterhin der Aktivitätsinhalt angezeigt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dieses Verhalten unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie den Test erneut sehen.

### Zusätzliche Metriken

Erstellen Sie zusätzliche Erfolgsmetriken.

Diese Einstellung ist nicht verfügbar, wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet.

### Zielgruppen für die Berichterstellung

Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen über bestimmte Zielgruppen zu zeigen.

### Erweiterte Einstellungen {#section_E2FE441AFB324E498793ABB025ED9974}

Für Zielmetriken des Typs [!UICONTROL Multivariater Test] sind erweiterte Einstellungen verfügbar.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/Menu_AdvancedSettings.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option „Erweiterte Einstellungen“ ist nicht verfügbar.

#### Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird?

Verwenden Sie diese Option, um zu zählen, dass eine Person die Erfolgsmetrik nur dann erreicht, wenn sie zuvor eine andere Erfolgsmetrik erreicht hat. Beispielsweise ist eine Testkonvertierung möglicherweise nur gültig, wenn der Besucher auf das Angebot klickt oder vor der Konvertierung auf eine bestimmte Seite gelangt.

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.

Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine von einer anderen abhängig machen können.

Mithilfe der Option [!UICONTROL Abhängigkeit hinzufügen] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf **[!UICONTROL Erweiterte Einstellungen]**.
2. Klicken Sie auf die Option **[!UICONTROL Abhängigkeit hinzufügen]**:

   ![Abhängigkeit hinzufügen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency.png)

3. Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf **[!UICONTROL Erreicht]**, um zwischen Erreicht und Nicht erreicht umzuschalten.

   ![Abhängigkeit erreicht](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency_reached.png)

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?

Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:

* [!UICONTROL Wählen Sie Anzahl erhöhen und Benutzer in Aktivität belassen], um anzugeben, wie die Anzahl erhöht werden soll.
* [!UICONTROL Wählen Sie Anzahl erhöhen, Benutzer freigeben und erneuten Eintritt &#x200B;], um das Erlebnis anzugeben, das Benutzende sehen, wenn sie die Aktivität erneut aufrufen.
* [!UICONTROL Wählen Sie Anzahl inkrementieren, Benutzer und Leiste von Wiedereintritt freigeben], um anzugeben, was der Benutzer anstelle des Aktivitätsinhalts sieht.

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Die folgende Einstellung ist verfügbar:

### Hinweise

Geben Sie alle Informationen zu Ihrer Aktivität ein, die für Sie selbst oder andere Team-Mitglieder nützlich sind. Die [!UICONTROL Anmerkungen] lässt sich in der Größe ändern.

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

>[!VIDEO](https://video.tv.adobe.com/v/17395)
