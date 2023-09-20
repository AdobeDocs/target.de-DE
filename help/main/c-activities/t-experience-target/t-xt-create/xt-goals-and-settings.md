---
keywords: Aktivitätseinstellungen;Ziele und Einstellungen für Erlebnis-Targeting;XT-Ziele und -Einstellungen;Erlebnis-Targeting;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie die [!UICONTROL Ziele und Einstellungen] Seite in [!DNL Adobe Target] , um Informationen über die Ziele eines [!UICONTROL Erlebnis-Targeting] (XT).
title: Anleitung [!UICONTROL Ziele und Einstellungen] in einer [!UICONTROL Erlebnis-Targeting] Aktivität?
feature: Experience Targeting
exl-id: 80cb7eff-4e9c-43d7-a3d8-7a9de79c91b9
source-git-commit: d7c1bbbbc8d1dcc45ac09a09f6b3be01f7542384
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 51%

---

# Ziele und Einstellungen in [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten

Die [!UICONTROL Ziele und Einstellungen] -Seite geben Sie Informationen zu den Zielen des Tests ein:

* [!UICONTROL Aktivitätseinstellungen]
* [!UICONTROL Berichterstellungseinstellungen ]
* [!UICONTROL Sonstige Metadaten]

Die verfügbaren Einstellungen hängen davon ab, ob Sie [!DNL Target] oder [!DNL Analytics] als Berichtsquelle.

## [!UICONTROL Aktivitätseinstellungen] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Die folgenden Einstellungen sind verfügbar:

### [!UICONTROL Ziel]

Geben Sie ein optionales Ziel ein. Beim Ziel kann es sich um beliebige Informationen handeln, die Ihnen und Ihren Team-Mitgliedern beim Identifizieren der Kampagne helfen.

### [!UICONTROL Priorität]

Abhängig von Ihren Einstellungen wird die [!DNL Target] Benutzeroberfläche und Optionen für [!UICONTROL Priorität] variieren. Sie können die veralteten Einstellungen von [!UICONTROL Niedrig], [!UICONTROL Mittel]oder [!UICONTROL Hoch]oder Sie können genauer unterteilte Prioritäten von 0 bis 999 festlegen.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Wenn diese Option nicht aktiviert ist in [!UICONTROL Administration] (Standardeinstellung), geben Sie eine Priorität an: [!UICONTROL Niedrig], [!UICONTROL Mittel]oder [!UICONTROL Hoch].

Um genauer unterteilte Prioritäten festzulegen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Berichterstellung]**, und schalten Sie dann die [!UICONTROL Aktivieren genauer Prioritätensetzung] auf die Position &quot;Ein&quot;.

Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:

* 0 = Niedrig
* 999 = Hoch

Für Aktivitäten, die in früheren Versionen von [!DNL Target], [!UICONTROL Niedrig] die Priorität in 0 umgewandelt wird, [!UICONTROL Mittel] in 5 umgewandelt wird und [!UICONTROL Hoch] wird in 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Wenn Sie genauer unterteilte Prioritäten verwendet haben und die Option deaktivieren möchten, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden.

### [!UICONTROL Dauer]

Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei ihrer Deaktivierung enden oder ein Datum und eine Uhrzeit für das Ende der Aktivität festlegen. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## [!UICONTROL Berichterstellungseinstellungen ] {#section_13119392051044FBA6387D9B3B1C43CF}

Die folgenden Einstellungen sind verfügbar:

### [!UICONTROL Berichtsquelle]

Festlegen, ob Daten erfasst werden sollen von [!DNL Target] oder von [!DNL Adobe Analytics]. Informationen über die Unterschiede zwischen den Berichterstellungslösungen und deren jeweilige Vorteile finden Sie unter [Adobe Analytics als Berichterstellungsquelle für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Bei Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T), wählen Sie eine [!DNL Analytics] Report Suite, die empfangen wird [!DNL Target] Aktivitätsdaten. Wählen Sie dazu zunächst einen der [!DNL Analytics] Unternehmen, an die Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Nur Report Suites, für die eine Verbindung hergestellt wurde [!DNL Target] stehen zur Auswahl zur Verfügung. Wenn die erwartete Report Suite nicht angezeigt wird, melden Sie sich zunächst ab und dann wieder bei der [!DNL Adobe Experience Cloud] erneut versuchen. Wenn die Report Suite weiterhin in der Liste fehlt, wenden Sie sich an [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) erfordert einen Tracking-Server, um die Ergebnisse korrekt zu melden. Ein standardmäßiger Trackingserver wird im [!UICONTROL Tracking-Server] -Feld. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie in dieses Feld den richtigen Tracking-Server einschließen. Siehe [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) für weitere Informationen.

Sollte in Ihren Kontoeinstellungen eine Berichterstellungslösung angegeben sein, wird die angegebene Lösung verwendet und diese Einstellung ist nicht sichtbar.

>[!NOTE]
>
>Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten.

### [!UICONTROL Zielmetrik]

Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Konversion] und legen Sie dann die Parameter fest, die bestimmen, wann ein Erfolg erreicht wird.

Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>Wenn die Berichtslösung auf [!DNL Analytics], lautet die einzige verfügbare Zielmetrik . [!UICONTROL Konversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden.

Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.

Wenn diese Option aktiviert ist, wird die [!UICONTROL Geschätzter Wert der Konversion] Feld (nicht verfügbar für [!UICONTROL Seitenergebnis] Metriken) einen Wert für Ihr Ziel bereitstellt, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Umsatz pro Besucher], [!UICONTROL Durchschnittlicher Bestellwert], [!UICONTROL Gesamtverkäufe], und [!UICONTROL Bestellungen]), verwendet die Schätzung [!UICONTROL Umsatz pro Besucher]. Der Datentyp ist eine Währung.

Nach Erreichen des Aktivitätsziels sieht ein Besucher weiterhin den Aktivitätsinhalt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dieses Verhalten unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie den Test erneut sehen.

### [!UICONTROL Zusätzliche Metriken]

Erstellen Sie zusätzliche Erfolgsmetriken.

Diese Einstellung ist nicht verfügbar, wenn die Berichterstellungslösung auf [!DNL Analytics]. In diesem Fall werden die für die [!DNL Analytics] Report Suite angewendet werden.

### [!UICONTROL Zielgruppen für die Berichterstellung]

Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen über bestimmte Zielgruppen zu zeigen.

Diese Einstellung ist nicht verfügbar, wenn Sie [!DNL Analytics] als Berichterstellungslösung. Die für die [!DNL Analytics] Report Suite angewendet wird.

## [!UICONTROL Andere Metadaten]

Geben Sie alle Informationen über Ihre Aktivität ein, die für Sie oder andere Teammitglieder nützlich sind. Die [!UICONTROL Hinweise] -Bereich kann angepasst werden.

## [!UICONTROL Erweiterte Einstellungen] {#section_E2FE441AFB324E498793ABB025ED9974}

Erweiterte Einstellungen sind verfügbar für [!UICONTROL Erlebnis-Targeting] Zielmetriken.

![Erweiterte Einstellungen](/help/main/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Wenn Sie [!DNL Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die [!UICONTROL Erweiterte Einstellungen] ist nicht verfügbar.

Die folgenden Einstellungen sind verfügbar:

### [!UICONTROL Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird?]

Verwenden Sie diese Option, um Besucher nur dann als die Erfolgsmetrik erreicht zu zählen, wenn sie zuvor eine andere Erfolgsmetrik erreicht haben. Beispielsweise kann eine Testkonversion nur dann gültig sein, wenn der Besucher auf das Angebot klickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.

Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.

Mithilfe der Option [!UICONTROL Abhängigkeit hinzufügen] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf **[!UICONTROL Erweiterte Einstellungen]**.
2. Klicken Sie auf **[!UICONTROL Abhängigkeit hinzufügen]**:

   ![Option „Abhängigkeit hinzufügen“](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Verschieben Sie die gewünschte Metrik per Drag-and-drop vom linken Bereich in den rechten Bereich. Klicken Sie dann auf **[!UICONTROL Erreicht]**[!UICONTROL , um die Einstellung zwischen Erreicht und Nicht erreicht zu wechseln].

   ![Abhängigkeits-Dialogfenster „Metriken hinzufügen“](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

### [!UICONTROL Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?]

Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:

* Wählen Sie [!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen] aus, um festzulegen, wie die Anzahl erhöht wird.
* Wählen Sie [!UICONTROL Anzahl erhöhen, Benutzer freigeben und Wiedereintritt erlauben] aus, um festzulegen, welches Erlebnis dem Benutzer angezeigt wird, wenn er die Aktivität wieder aufnimmt.
* Wählen Sie [!UICONTROL Anzahl erhöhen, Benutzer freigeben und an Wiedereintritt hindern] aus, um festzulegen, was dem Benutzer statt der Aktivitätsinhalte angezeigt wird.

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Schulungsvideo: Aktivitätseinstellungen (3:02)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
