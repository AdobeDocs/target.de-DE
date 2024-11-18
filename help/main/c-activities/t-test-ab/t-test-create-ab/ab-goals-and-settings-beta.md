---
keywords: Aktivitätseinstellungen;A/B-Ziele und -Einstellungen;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie mit der Seite [!UICONTROL Goals and Settings] A/B-Aktivitätsziele definieren.
title: Wie gebe ich Ziele und Einstellungen in einer [!DNL Target] A/B-Aktivität an?
feature: A/B Tests
hide: true
hidefromtoc: true
exl-id: aeafb4d8-a486-46cf-8871-4c220bc3674e
source-git-commit: d5bd3b0d7cdf6eb06175a6365da6b8173f76800f
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 30%

---

# Ziele und Einstellungen

Auf der Seite [!UICONTROL Goals & Settings] in [!DNL Adobe Target] geben Sie Informationen zu den Zielen der Aktivität an.

Die verfügbaren Einstellungen hängen davon ab, ob Sie Target oder [Analytics als Berichtsquelle verwenden](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Im Abschnitt [!UICONTROL Activity Settings] der Seite [!UICONTROL Goals & Settings] können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Objective] | Geben Sie ein optionales Ziel ein. Das Ziel kann jede Information sein, die Ihnen und Ihren Teammitgliedern dabei hilft, die Aktivität zu identifizieren. |
| [!UICONTROL Priority] | Abhängig von Ihren Einstellungen variieren die [!DNL Target]-Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die veralteten Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder genauer unterteilte Prioritäten von 0 bis 999 aktivieren.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option in [!UICONTROL Administration] (der Standardeinstellung) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].<P>Um [ genauer unterteilte Prioritäten](/help/main/administrating-target/reporting.md) zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und stellen Sie dann die Option [!UICONTROL Enable Fine-Grained Priorities] auf die Position &quot;Ein&quot;. <P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an: 0 = [!UICONTROL Low] und 999 = [!UICONTROL High]. <P>Bei Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden, wird die Priorität [!UICONTROL Low] in 0, die Priorität [!UICONTROL Medium] in 5 und die Priorität [!UICONTROL High] in 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.<P>Hinweis: Bevor Sie diese Option deaktivieren können, nachdem Sie genauere Prioritäten verwendet haben, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden. |
| [!UICONTROL Duration] | Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

Im Abschnitt [!UICONTROL Reporting Settings] der Seite [!UICONTROL Goals & Settings] können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Reporting Source] | Geben Sie an, aus welchen Lösungsdaten erfasst werden:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Wenn in Ihren [Kontoeinstellungen](/help/main/administrating-target/reporting.md) eine Berichtsquelle angegeben ist, wird die angegebene Quelle verwendet und diese Einstellung ist nicht sichtbar.<P>Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten.<P>**Adobe Analytics**: Unter [Adobe Analytics als Reporting-Source für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) erfahren Sie mehr über die Unterschiede zwischen den Berichterstellungslösungen und deren Vorteile. Wenn Sie [!DNL Analytics] als Berichtsquelle für [!DNL Target] auswählen, wählen Sie eine [!DNL Analytics] Report Suite aus, die [!DNL Target] Aktivitätsdaten erhält.<P>Um eine Berichtsquelle anzugeben, wählen Sie zunächst eines der [!DNL Analytics] Unternehmen aus, an die Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Adobe Target] bereitgestellt wurden. Wenn die erwarteten Report Suites nicht angezeigt werden, versuchen Sie zunächst, sich abzumelden und sich wieder bei [!DNL Adobe Experience Cloud] anzumelden, um es erneut zu versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die Kundenunterstützung.<P><P>**Adobe Customer Journey Analytics**: Weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target] finden Sie unter [[!DNL Target] Berichterstellung in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) .<P>Die [!DNL Target] Berichterstellung in [!DNL Customer Journey Analytics] wird in A/B-Aktivitäten mit manueller Traffic-Aufspaltung unterstützt. [!UICONTROL Auto-Target] und [!UICONTROL Auto-Allocate] A/B-Aktivitäten können die [!DNL Target] Berichterstellung in [!DNL Customer Journey Analytics] nicht verwenden. |
| [!UICONTROL Goal Metric] | Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine Metrik vom Typ [!UICONTROL Conversion] und legen Sie dann die Parameter fest, die bestimmen, wann ein Erfolg erreicht wird. Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Hinweis: Wenn die Berichterstellungslösung auf &quot;[!DNL Analytics]&quot; eingestellt ist, ist die einzige verfügbare Zielmetrik &quot;[!UICONTROL Conversion]&quot;. [!DNL Analytics] -Metriken können nicht als Ziel ausgewählt werden. Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.<P>Wenn diese Option aktiviert ist, bietet das Feld [!UICONTROL Estimated Value of the Conversion] (nicht verfügbar für die Metriken [!UICONTROL Page Score] ) einen Wert für Ihr Ziel, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] und [!UICONTROL Orders]) verwendet die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung.<P>Nach Erreichen des Aktivitätsziels sieht ein Besucher weiterhin den Aktivitätsinhalt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dies unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie die Aktivität erneut sehen. |
| [!UICONTROL Additional Metrics] | Erstellen Sie zusätzliche Erfolgsmetriken. Diese Einstellung ist nicht verfügbar, wenn die Berichterstellungslösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet. |
| [!UICONTROL Audiences for Reporting] | Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen zu bestimmten Zielgruppen anzuzeigen. Diese Einstellung ist nicht verfügbar, wenn Sie [!DNL Analytics] als Berichterstellungslösung auswählen. Die für die Report Suite [!DNL Analytics] definierte Zielgruppe wird angewendet. |

## Erweiterte Einstellungen   {#section_E2FE441AFB324E498793ABB025ED9974}

Im Abschnitt [!UICONTROL Advanced Settings] der Seite [!UICONTROL Goals & Settings] können Sie die erweiterten Optionen konfigurieren.

Um erweiterte Einstellungen festzulegen, klicken Sie im Abschnitt [!UICONTROL My Primary Goal] auf das Symbol **[!UICONTROL More]** ( ![Mehr Symbol](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Advanced Settings]**.

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option für erweiterte Einstellungen ist nicht verfügbar.

Die folgenden Optionen sind verfügbar:

| Einstellung | Beschreibung |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | Verwenden Sie diese Option, um nur Personen zu zählen, die die Erfolgsmetrik erreicht haben, wenn sie zuvor eine andere Erfolgsmetrik erreicht haben. Eine Aktivitätskonversion kann beispielsweise nur dann gültig sein, wenn der Besucher auf das Angebot klickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt. Sie können für mehrere Metriken eine Abhängigkeit bereitstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit die Anzahl erhöht wird. Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine Abhängigkeit voneinander festlegen können. Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde. So fügen Sie eine Abhängigkeit hinzu:<ul><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf [!UICONTROL Advanced Settings].</li><li>Klicken Sie auf die Option [!UICONTROL Add Dependency] :</li><li>Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf [!UICONTROL Reached] , um die Einstellung zwischen [!UICONTROL Reached] und [!UICONTROL  Not Reached] umzuschalten.</li><li>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:<ul><li>Wählen Sie **[!UICONTROL Increment Count & Keep User in Activity]** aus, um festzulegen, wie die Anzahl erhöht wird.</li><li>Wählen Sie **[!UICONTROL Increment Count, Release User & Allow Reentry]** aus, um das Erlebnis anzugeben, das dem Benutzer angezeigt wird, wenn er die Aktivität erneut aufruft.</li><li>Wählen Sie **[!UICONTROL Increment Count, Release User & Bar from Reentry]** aus, um festzulegen, was der Benutzer anstelle des Aktivitätsinhalts sieht.</li></ul> |
| [!UICONTROL How will the count be incremented?] | Es gibt drei Möglichkeiten, wie die Anzahl erhöht werden kann:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Im Abschnitt [!UICONTROL Other Metadata] der Seite [!UICONTROL Goals & Settings] können Sie alle Informationen zu Ihrer Aktivität angeben, die für Sie oder andere Teammitglieder nützlich sind. Die Größe des Bereichs Notizen kann angepasst werden.|
