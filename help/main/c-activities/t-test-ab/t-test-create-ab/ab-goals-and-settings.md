---
keywords: Aktivitätseinstellungen;A/B-Ziele und -Einstellungen;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie auf der Seite [!UICONTROL Ziele und Einstellungen] A/B-Aktivitätsziele definieren können.
title: Wie gebe ich Ziele und Einstellungen in einer [!DNL Target] A/B-Aktivität an?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
TQID: 'https://experienceleague.adobe.com/X3JDvfXDHM2rAOodEY5N9TVO-tBpz4vNDUvhOpC0XZ4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: abab6b3e464bb9f294e9c3c455dca1f57bb0d458
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 24%
---
# Ziele und Einstellungen {#ab-goals-and-settings}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, was Sie auf der Seite **[!UICONTROL Ziele und Einstellungen]** einer A/B-, Erlebnis-Targeting- (XT) oder Multivarianz-Test- (MVT)-Aktivität festlegen können: die Aktivitätseinstellungen, die Reporting-Einstellungen, die erweiterten Einstellungen und die Hinweise.

>[!ENDSHADEBOX]

Auf **[!UICONTROL Seite „Ziele]** Einstellungen“ in [!DNL Adobe Target] geben Sie Informationen zu den Zielen der Aktivität an.

Die verfügbaren Einstellungen hängen davon ab, ob Sie Target oder [Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) verwenden.

Die gleichen Einstellungen gelten für [!UICONTROL Erlebnis-Targeting] (XT)- und [!UICONTROL Multivarianz-Test]&#x200B;(MVT)-Aktivitäten, mit Ausnahme der [Statistische Methodik](#section_statistical-methodology), die nur für A/B-Aktivitäten verfügbar ist.

* [Aktivitätseinstellungen](#section_DCBDC354261F420EBD4B43EA34947BAC): Ziel, Priorität und Dauer
* [Reporting-Einstellungen](#section_13119392051044FBA6387D9B3B1C43CF): Berichtsquelle, Zielmetrik, zusätzliche Metriken und Zielgruppen
* [Erweiterte Einstellungen](#section_E2FE441AFB324E498793ABB025ED9974): Abhängigkeiten und was passiert, nachdem ein Besucher das Ziel erreicht hat
* [Statistische Methodik](#section_statistical-methodology): So werden Ergebnisse analysiert
* [Andere Metadaten](#section_2E8917BEFB954480A4206B9E9E917F80): Anmerkungen

## [!UICONTROL Aktivitätseinstellungen] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Im Abschnitt **[!UICONTROL Aktivitätseinstellungen]** der Seite **[!UICONTROL Ziele und Einstellungen]** können Sie die folgenden Optionen konfigurieren.

![](../../assets/goals-ab-1.png)

### Ziel {#objective}

Geben Sie ein optionales Ziel ein. Das Ziel kann jede Information sein, die Ihnen und Ihren Team-Mitgliedern dabei hilft, die Aktivität zu identifizieren.

### Priorität {#priority}

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für **[!UICONTROL Priorität]**:

* **Legacy-Prioritäten (Standard):** Wenn diese Option in **[!UICONTROL Administration]** nicht aktiviert ist (Standard), geben Sie die Priorität **[!UICONTROL Niedrig]**, **[!UICONTROL Medium]** oder **[!UICONTROL Hoch]** an.
* **Detaillierte Prioritäten:** Geben Sie einen Wert zwischen 0 und 999 an, wobei 0 = **[!UICONTROL Niedrig]** und 999 = **[!UICONTROL Hoch]**.

  Um [detaillierten Prioritäten](/help/main/administrating-target/reporting.md) zu aktivieren, greifen Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Reporting]** zu und schalten Sie dann die Option **[!UICONTROL Aktivieren detaillierter Prioritäten]** um.

Für Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden **[!UICONTROL wird]** Priorität auf 0, **[!UICONTROL Medium]** auf 5 und **[!UICONTROL Hoch]** auf 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Bevor Sie nach der Verwendung feinkörnige Prioritäten deaktivieren können, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden.

### Dauer {#duration}

Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden.

Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## [!UICONTROL Berichterstellungseinstellungen] {#section_13119392051044FBA6387D9B3B1C43CF}

Im **[!UICONTROL Reporting-]** der Seite **[!UICONTROL Ziele und Einstellungen]** können Sie die folgenden Optionen konfigurieren.

![](../../assets/goals-ab-2.png)

### Berichtsquelle {#reporting-source}

Geben Sie an, aus welcher Lösung Daten erfasst werden:

* [!DNL Adobe Target]

* [!DNL Adobe Analytics]

  +++ Mehr über Analytics als Berichtsquelle

  Informationen über die Unterschiede zwischen den Berichterstellungslösungen und deren jeweilige Vorteile finden Sie unter [Adobe Analytics als Berichterstellungsquelle für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md). Bei der Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target] wählen Sie eine [!DNL Analytics] Report Suite aus, um [!DNL Target] Aktivitätsdaten zu erhalten.

  Um eine Berichtsquelle anzugeben, wählen Sie zunächst eines der [!DNL Analytics] Unternehmen aus, mit denen Ihr Konto verknüpft ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Adobe Target] bereitgestellt wurden. Wenn die erwarteten Report Suites nicht angezeigt werden, versuchen Sie zunächst, sich abzumelden und sich wieder bei der [!DNL Adobe Experience Cloud] anzumelden, um es dann erneut zu versuchen. Wenn die Report Suite noch immer in der Liste fehlt, wenden Sie sich an die Kundenunterstützung.

  [!DNL Analytics for Target] (A4T) erfordert einen Trackingserver, um Ergebnisse korrekt zu melden. Im Feld **[!UICONTROL Tracking-Server]** wird ein standardmäßiger Tracking-Server angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie den richtigen Tracking-Server in dieses Feld einbeziehen. Weitere Informationen finden [ unter „Verwenden eines Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)Trackingservers“.
  +++

* [!DNL Adobe Customer Journey Analytics]

  +++ Weitere Informationen zu Customer Journey Analytics als Berichtsquelle

  Unter [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) finden Sie Informationen zu unterstützten Aktivitätstypen, zur Auswahl von Sandboxes und Datenansichten, zu Zielmetriken und zur Einrichtung von Berichten in [!DNL Customer Journey Analytics].
  +++

Wenn in Ihren [Kontoeinstellungen“ eine Berichtsquelle angegeben ist](/help/main/administrating-target/reporting.md) wird die angegebene Quelle verwendet, und diese Einstellung ist nicht sichtbar.

Sie können Ihre Berichtsquelle nicht ändern, nachdem die Aktivität live geschaltet wurde, um die Konsistenz der Berichte zu gewährleisten.

### Zielmetrik {#goal-metric}

>[!NOTE]
>
>Wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist, ist die einzige verfügbare Zielmetrik **[!UICONTROL Konversion]**. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden.

Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine Metrik **[!UICONTROL Konversion]** und legen Sie dann die Parameter fest, die bestimmen, wann der Erfolg erzielt wird.

Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).

Klicken Sie für weitere Optionen auf das Symbol **[!UICONTROL Mehr]** neben der Zielmetrik und dann auf **[!UICONTROL Erweiterte Einstellungen]**. Siehe [Erweiterte Einstellungen](#section_E2FE441AFB324E498793ABB025ED9974)

![](../../assets/goals-ab-3.png)

Wenn diese Option aktiviert ist **[!UICONTROL liefert der Feld „Geschätzter Wert]** Konversion“ einen Wert für Ihr Ziel, aber nicht für andere Metriken. Folgende Punkte gelten für dieses Feld:

* Der Wert ermöglicht es [!DNL Target], eine geschätzte Steigerung des Umsatzes zu berechnen.
* Das Feld ist optional. Der inkrementelle Umsatz für eine andere Metrik als Umsatz kann jedoch ohne dieses Feld nicht berechnet werden.
* Das Feld ist nicht für die Metriken **[!UICONTROL Seitenbewertung]** verfügbar.
* Für alle Umsatzmetriken (**[!UICONTROL Umsatz pro Besucher]**, **[!UICONTROL Durchschnittlicher Bestellwert]**, **[!UICONTROL Gesamtumsatz]** und **[!UICONTROL Bestellungen]**) verwendet die Schätzung **[!UICONTROL Umsatz pro Besucher]**. Der Datentyp ist eine Währung.

### Zusätzliche Metriken {#additional-metrics}

Diese Einstellung ist nicht verfügbar, wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet.

### Zielgruppen für die Berichterstellung {#audiences-for-reporting}

![](../../assets/goals-ab-4.png)

Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um Informationen nur zu bestimmten Zielgruppen anzuzeigen.

Beachten Sie, dass diese Einstellung nicht verfügbar ist, wenn Sie [!DNL Analytics] als Berichtslösung auswählen. Die für die [!DNL Analytics] Report Suite definierte Zielgruppe wird angewendet.

## Erweiterte Einstellungen {#section_E2FE441AFB324E498793ABB025ED9974}

Im **[!UICONTROL Erweiterte Einstellungen]** der Seite **[!UICONTROL Ziele und Einstellungen]** können Sie die erweiterten Optionen konfigurieren.

Um erweiterte Einstellungen festzulegen, klicken Sie auf das Symbol **[!UICONTROL Mehr]** ( ![Mehr-](/help/main/assets/icons/MoreSmallList.svg) ) im Abschnitt **[!UICONTROL Mein Primäres Ziel]** und klicken Sie dann auf **[!UICONTROL Erweiterte Einstellungen]**.

![](../../assets/goals-ab-3.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option „Erweiterte Einstellungen“ ist nicht verfügbar.

### Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird? {#dependencies}

Verwenden Sie diese Option, um zu zählen, dass eine Person die Erfolgsmetrik nur dann erreicht, wenn sie zuvor eine andere Erfolgsmetrik erreicht hat. Beispielsweise ist eine Aktivitätskonvertierung möglicherweise nur gültig, wenn der Besucher auf das Angebot klickt oder vor der Konvertierung auf eine bestimmte Seite gelangt.

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht. Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine von einer anderen abhängig machen können. Mithilfe der Option **[!UICONTROL Abhängigkeit hinzufügen]** kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf **[!UICONTROL Erweiterte Einstellungen]**.

1. Klicken Sie auf die Option **[!UICONTROL Abhängigkeit hinzufügen.]**

1. Ziehen Sie die gewünschten Metriken per Drag-and-Drop und klicken Sie dann auf **[!UICONTROL Erreicht]**, um zwischen **[!UICONTROL Erreicht]** und **[!UICONTROL Nicht erreicht]** umzuschalten.

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft? {#after-goal}

Nach Erreichen des Aktivitätsziels wird einem Besucher weiterhin der Aktivitätsinhalt angezeigt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dies unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie die Aktivität erneut sehen.

Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:

* **[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]**, um anzugeben, wie die Anzahl erhöht wird.
* **[!UICONTROL Anzahl erhöhen, Benutzer freigeben und erneuten Eintritt erlauben]** um das Erlebnis anzugeben, das Benutzende sehen, wenn sie wieder in die Aktivität eintreten.
* **[!UICONTROL Anzahl inkrementieren, Benutzer und Leiste von erneuten Eintritten freigeben]** um anzugeben, was der Benutzer anstelle des Aktivitätsinhalts sieht.

### Wie wird die Anzahl erhöht? {#count-increment}

Es gibt drei Möglichkeiten, wie die Anzahl erhöht werden kann:

* **[!UICONTROL Einmal pro Teilnehmer]**
* **[!UICONTROL Bei jeder Impression (ohne Seitenaktualisierungen)]**
* **[!UICONTROL Bei jeder Impression]**

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#overview).

## Statistische Methodik {#section_statistical-methodology}

Im **[!UICONTROL Statistische Methodik]** der Seite **[!UICONTROL Ziele und Einstellungen]** können Sie auswählen, wie die Experimentergebnisse analysiert werden sollen.

### Methodenoptionen {#methodology-options}

Diese Auswahl bestimmt das statistische Framework, die Ergebnismetriken und die Entscheidungskriterien, die für die Zielmetrik **[!UICONTROL Konversion]** dieser Aktivität verwendet werden:

* **[!UICONTROL Bayes]:** Wahrscheinlichkeitsbasierte Entscheidungsfindung, die Glaubenssätze aktualisiert, wenn Daten eingehen, und kontinuierliche Überwachung und kleinere Stichprobengrößen unterstützt. Die Ergebnisse werden als Wahrscheinlichkeit ausgedrückt, dass eine Variante besser ist als eine andere, z. B. „92%ige Wahrscheinlichkeit, dass Variante B die Kontrolle übertrifft“.
  * Am besten geeignet für kleinere Stichprobengrößen, kontinuierliche Überwachung, Stakeholder, die Wahrscheinlichkeiten bevorzugen, oder wenn Sie Vorkenntnisse aus früheren Tests haben, um sich zu bewerben.
  * Nicht ideal, wenn Sie eine strenge behördliche oder Compliance-Abnahme benötigen oder traditionelle p-Werte benötigen.
  * Berichte zeigen **[!UICONTROL Chance zur Beat-Kontrolle]** und ein glaubwürdiges Intervall anstelle der frequentistischen **[!UICONTROL Konfidenz]** Spalte.
* **[!UICONTROL Welchs t-Test (Frequentist)]:** Die bestehende, traditionelle Hypothesentestmethode. Verwendet p-Werte und erfordert eine feste Stichprobengröße. Berichte zeigen einen **[!UICONTROL Konfidenz]** Prozentsatz und ein Konfidenzintervall an.

Diese Einstellung ist nur für Aktivitäten verfügbar, deren primäre Zielmetrik &quot;**[!UICONTROL &quot;]**. Aktivitäten mit einem **[!UICONTROL Umsatz]** oder **[!UICONTROL Engagement]** primären Ziel verwenden immer **[!UICONTROL Welchs t-Test]**.

Weitere Informationen zur Berechnung und Berichterstellung der einzelnen Methoden finden Sie unter [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

### Bayes&#39;sche Konfiguration {#bayesian-configuration}

Diese Einstellung wird nur angezeigt, wenn **[!UICONTROL Bayes]** als **[!UICONTROL Statistische Methodik]** ausgewählt ist. Konfigurieren Sie die folgenden Optionen:

* **[!UICONTROL Glaubwürdiges Intervall]**: Legt den Bereich fest, in den der wahre Effekt fallen soll.
* **[!UICONTROL Entscheidungsschwellenwert]**: Legt die Mindestwahrscheinlichkeit fest, die eine Variante erreichen muss, relativ **[!UICONTROL Kontrolle]**, bevor sie zum Gewinner erklärt werden kann.
* **[!UICONTROL Vorkenntnisse aus vergangenen Tests verwenden?]**: Schalten Sie diese Option ein, um Vorkenntnisse aus vergangenen Tests bereitzustellen, die als Grundlage für die **[!UICONTROL Bayes&#39;sche]**-Berechnung dienen.

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Im Abschnitt **[!UICONTROL Sonstige Metadaten]** der Seite **[!UICONTROL Ziele und Einstellungen]** können Sie alle Informationen zu Ihrer Aktivität angeben, die Sie für sich selbst oder andere Team-Mitglieder verfügbar halten können.
