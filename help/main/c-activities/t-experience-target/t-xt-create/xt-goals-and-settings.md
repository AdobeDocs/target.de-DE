---
keywords: Aktivitätseinstellungen;Ziele und Einstellungen für Erlebnis-Targeting;XT-Ziele und -Einstellungen;Erlebnis-Targeting;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie auf der Seite [!UICONTROL Goals & Settings] in  [!DNL Adobe Target]  Informationen zu den Zielen einer [!UICONTROL Experience Targeting] (XT)-Aktivität angeben.
title: Wie gebe ich [!UICONTROL Goals & Settings] in einer [!UICONTROL Experience Targeting] Aktivität an?
feature: Experience Targeting
exl-id: 80cb7eff-4e9c-43d7-a3d8-7a9de79c91b9
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 38%

---

# Ziele und Einstellungen in [!UICONTROL Experience Targeting] (XT)-Aktivitäten

Auf der Seite [!UICONTROL Goals & Settings] geben Sie Informationen zu den Testzielen ein:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

Die verfügbaren Einstellungen hängen davon ab, ob Sie [!DNL Target] oder [!DNL Analytics] als Berichtsquelle verwenden.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Die folgenden Einstellungen sind verfügbar:

### [!UICONTROL Objective]

Geben Sie ein optionales Ziel ein. Beim Ziel kann es sich um beliebige Informationen handeln, die Ihnen und Ihren Team-Mitgliedern beim Identifizieren der Kampagne helfen.

### [!UICONTROL Priority]

Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die Legacy-Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Standort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Wenn diese Option in [!UICONTROL Administration] nicht aktiviert ist (Standard), geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].

Um die feinabgestimmten Prioritäten zu aktivieren, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Reporting]** und schalten Sie die Option [!UICONTROL Enable Fine-Grained Priorities] auf „Ein“.

Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:

* 0 = Niedrig
* 999 = Hoch

Für Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden, wird [!UICONTROL Low] Priorität in 0, [!UICONTROL Medium] in 5 und [!UICONTROL High] in 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Wenn Sie genauer unterteilte Prioritäten verwendet haben und die Option deaktivieren möchten, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden.

### [!UICONTROL Duration]

Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität beendet werden, wenn sie deaktiviert ist, oder Sie können ein Datum und eine Uhrzeit für das Ende der Aktivität festlegen. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00 :00 Mitternacht ist. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

Die folgenden Einstellungen sind verfügbar:

### [!UICONTROL Reporting Source]

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

### [!UICONTROL Goal Metric]

Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Conversion] Metrik aus und legen Sie dann die Parameter fest, die bestimmen, wann der Erfolg erzielt wird.

Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>Wenn die Reporting-Lösung auf [!DNL Analytics] eingestellt ist, ist die einzige verfügbare Zielmetrik [!UICONTROL Conversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden.

Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.

Wenn diese Option aktiviert ist, liefert das Feld [!UICONTROL Estimated Value of the Conversion] (für [!UICONTROL Page Score] Metriken nicht verfügbar) einen Wert für Ihr Ziel, aber nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] und [!UICONTROL Orders]) nutzt die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung.

Nach Erreichen des Aktivitätsziels wird einem Besucher weiterhin der Aktivitätsinhalt angezeigt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dieses Verhalten unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie den Test erneut sehen.

### [!UICONTROL Additional Metrics]

Erstellen Sie zusätzliche Erfolgsmetriken.

Diese Einstellung ist nicht verfügbar, wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet.

### [!UICONTROL Audiences for Reporting]

Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen über bestimmte Zielgruppen zu zeigen.

Diese Einstellung ist nicht verfügbar, wenn Sie [!DNL Analytics] als Berichtslösung auswählen. Die für die [!DNL Analytics] Report Suite definierte Zielgruppe wird angewendet.

## [!UICONTROL Other Meta Data]

Geben Sie alle Informationen zu Ihrer Aktivität ein, die für Sie selbst oder andere Team-Mitglieder nützlich sind. Die Größe des [!UICONTROL Notes] Fensterbereichs kann geändert werden.

## [!UICONTROL Advanced Settings] {#section_E2FE441AFB324E498793ABB025ED9974}

Für [!UICONTROL Experience Targeting] Zielmetriken sind erweiterte Einstellungen verfügbar.

![Erweiterte Einstellungen](/help/main/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Wenn Sie [!DNL Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option [!UICONTROL Advanced Settings] ist nicht verfügbar.

Die folgenden Einstellungen sind verfügbar:

### [!UICONTROL Which success metric must be reached before incrementing this metric?]

Verwenden Sie diese Option, um Besuchende nur dann als Erfolge der Erfolgsmetrik zu zählen, wenn sie zuvor eine andere Erfolgsmetrik erreicht haben. Beispielsweise ist eine Testkonvertierung möglicherweise nur gültig, wenn der Besucher vor der Konvertierung auf das Angebot klickt oder eine bestimmte Seite erreicht.

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.

Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.

Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Nachdem Sie zusätzliche Metriken hinzugefügt haben, klicken Sie auf **[!UICONTROL Advanced Settings]**.
2. Klicken Sie auf **[!UICONTROL Add Dependency]**:

   ![Option „Abhängigkeit hinzufügen“](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf **[!UICONTROL Reached]** , um zwischen [!UICONTROL Reached] und [!UICONTROL Not Reached] umzuschalten.

   ![Abhängigkeits-Dialogfenster „Metriken hinzufügen“](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

### [!UICONTROL What will happen after a user encounters this goal metric?]

Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:

* Wählen Sie [!UICONTROL Increment Count & Keep User in Activity] aus, um anzugeben, wie die Anzahl erhöht werden soll.
* Wählen Sie [!UICONTROL Increment Count, Release User & Allow Reentry] aus, um das Erlebnis anzugeben, das Benutzenden angezeigt wird, wenn sie die Aktivität erneut aufrufen.
* Wählen Sie [!UICONTROL Increment Count, Release User & Bar from Reentry] aus, um festzulegen, was dem Benutzer anstelle des Aktivitätsinhalts angezeigt wird.

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Schulungsvideo: Aktivitätseinstellungen (3:02)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
