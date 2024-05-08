---
keywords: Aktivitätseinstellungen;A/B-Ziele und -Einstellungen;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie die [!UICONTROL Goals and Settings] Seite, um Informationen über die Ziele einer A/B-Aktivität anzugeben.
title: Wie gebe ich Ziele und Einstellungen in einer [!DNL Target] A/B-Aktivität?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: b5f508d283390c859085d4ee52c582312085addc
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 35%

---

# Ziele und Einstellungen

Die [!UICONTROL Goals & Settings] Seite in [!DNL Adobe Target] Hier geben Sie Informationen zu den Zielen der Aktivität an.

Die verfügbaren Einstellungen hängen davon ab, ob Sie Target oder [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) als Berichtsquelle.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Die [!UICONTROL Activity Settings] Abschnitt [!UICONTROL Goals & Settings] -Seite können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Objective] | Geben Sie ein optionales Ziel ein. Das Ziel kann jede Information sein, die Ihnen und Ihren Teammitgliedern dabei hilft, die Aktivität zu identifizieren. |
| [!UICONTROL Priority] | Abhängig von Ihren Einstellungen wird die [!DNL Target] Benutzeroberfläche und Optionen für [!UICONTROL Priority] variieren. Sie können die veralteten Einstellungen von [!UICONTROL Low], [!UICONTROL Medium]oder [!UICONTROL High]oder Sie können genauer unterteilte Prioritäten von 0 bis 999 festlegen.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option nicht aktiviert ist in [!UICONTROL Administration] (Standardeinstellung), geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium]oder [!UICONTROL High].<P>Aktivieren [Präzise Prioritäten](/help/main/administrating-target/reporting.md)klicken [!UICONTROL Administration] > [!UICONTROL Reporting], und schalten Sie dann die [!UICONTROL Enable Fine-Grained Priorities] auf die Position &quot;Ein&quot;. <P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an: 0 = [!UICONTROL Low] und 999 = [!UICONTROL High]. <P>Für Aktivitäten, die in früheren Versionen von [!DNL Target], [!UICONTROL Low] die Priorität in 0 umgewandelt wird, [!UICONTROL Medium] in 5 umgewandelt wird und [!UICONTROL High] wird in 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.<P>Hinweis: Bevor Sie diese Option deaktivieren können, nachdem Sie genauere Prioritäten verwendet haben, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden. |
| Dauer | Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

Die [!UICONTROL Reporting Settings] Abschnitt [!UICONTROL Goals & Settings] -Seite können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Reporting Source] | Geben Sie an, aus welchen Lösungsdaten erfasst werden:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Wenn eine Berichtsquelle in Ihrer [Kontoeinstellungen](/help/main/administrating-target/reporting.md), wird die angegebene Quelle verwendet und diese Einstellung ist nicht sichtbar.<P>Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten.<P>**Adobe Analytics**: Siehe [Adobe Analytics als Berichtsquelle für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) , um mehr über die Unterschiede zwischen den Berichterstellungslösungen und deren Vorteile zu erfahren. Bei Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target], wählen Sie eine [!DNL Analytics] Report Suite, die empfangen wird [!DNL Target] Aktivitätsdaten.<P>Um eine Berichtsquelle anzugeben, wählen Sie zunächst eine der [!DNL Analytics] Unternehmen, an die Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Nur Report Suites, für die eine Verbindung hergestellt wurde [!DNL Adobe Target] stehen zur Auswahl zur Verfügung. Wenn die erwarteten Report Suites nicht angezeigt werden, melden Sie sich zunächst ab und melden Sie sich wieder bei der [!DNL Adobe Experience Cloud] erneut versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die Kundenunterstützung.<P><P>**Adobe Customer Journey Analytics**: Siehe [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) Weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target].<P>[!DNL Target] Reporting in [!DNL Customer Journey Analytics] wird in A/B-Aktivitäten mit manueller Traffic-Aufteilung unterstützt. [!UICONTROL Auto-Target] und [!UICONTROL Auto-Allocate] A/B-Aktivitäten können nicht verwendet werden [!DNL Target] Reporting in [!DNL Customer Journey Analytics]. |
| [!UICONTROL Goal Metric] | Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Conversion] und legen Sie dann die Parameter fest, die bestimmen, wann ein Erfolg erreicht wird. Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Hinweis: Wenn die Berichterstellungslösung auf [!DNL Analytics], lautet die einzige verfügbare Zielmetrik . [!UICONTROL Conversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden. Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.<P>Wenn diese Option aktiviert ist, wird die [!UICONTROL Estimated Value of the Conversion] -Feld (nicht verfügbar für [!UICONTROL Page Score] Metriken) einen Wert für Ihr Ziel bereitstellt, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], und [!UICONTROL Orders]), verwendet die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung.<P>Nach Erreichen des Aktivitätsziels sieht ein Besucher weiterhin den Aktivitätsinhalt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dies unterscheidet sich vom Standardverhalten in [!DNL Target Classic], was Besucher als neu zählt, wenn sie die Aktivität erneut sehen. |
| [!UICONTROL Additional Metrics] | Erstellen Sie zusätzliche Erfolgsmetriken. Diese Einstellung ist nicht verfügbar, wenn die Berichterstellungslösung auf [!DNL Analytics]. In diesem Fall werden die für die [!DNL Analytics] Report Suite angewendet werden. |
| [!UICONTROL Audiences for Reporting] | Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen zu bestimmten Zielgruppen anzuzeigen. Diese Einstellung ist nicht verfügbar, wenn Sie [!DNL Analytics] als Berichterstellungslösung. Die für die [!DNL Analytics] Report Suite angewendet wird. |

## Erweiterte Einstellungen   {#section_E2FE441AFB324E498793ABB025ED9974}

Die [!UICONTROL Advanced Settings] Abschnitt [!UICONTROL Goals & Settings] -Seite können Sie die folgenden Optionen konfigurieren:

Um erweiterte Einstellungen festzulegen, klicken Sie auf das **[!UICONTROL More]** Symbol (die vertikalen Auslassungspunkte), und klicken Sie dann auf **[!UICONTROL Advanced Settings]**, wie in der folgenden Abbildung dargestellt.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option für erweiterte Einstellungen ist nicht verfügbar.

![Erweiterte Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Einstellung | Beschreibung |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | Verwenden Sie diese Option, um nur Personen zu zählen, die die Erfolgsmetrik erreicht haben, wenn sie zuvor eine andere Erfolgsmetrik erreicht haben. Eine Aktivitätskonversion kann beispielsweise nur dann gültig sein, wenn der Besucher auf das Angebot klickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt. Sie können für mehrere Metriken eine Abhängigkeit bereitstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit die Anzahl erhöht wird. Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine Abhängigkeit voneinander festlegen können. Die [!UICONTROL Add Dependency] ermöglicht es, die Erfolgsmetrik zu inkrementieren, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde. So fügen Sie eine Abhängigkeit hinzu:<ul><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf [!UICONTROL Advanced Settings].</li><li>Klicken Sie auf [!UICONTROL Add Dependency] Option:</li><li>Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf [!UICONTROL Reached] zum Umschalten der Einstellung zwischen [!UICONTROL Reached] und[!UICONTROL  Not Reached].</li><li>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:<ul><li>Auswählen [!UICONTROL Increment Count & Keep User in Activity] um anzugeben, wie die Anzahl erhöht wird.</li><li>Auswählen [!UICONTROL Increment Count, Release User & Allow Reentry] um das Erlebnis anzugeben, das dem Benutzer angezeigt wird, wenn er die Aktivität erneut aufruft.</li><li>Auswählen [!UICONTROL Increment Count, Release User & Bar from Reentry] um festzulegen, was der Benutzer anstelle des Aktivitätsinhalts sieht.</li></ul> |
| [!UICONTROL How will the count be incremented?] | Es gibt drei Möglichkeiten, wie die Anzahl erhöht werden kann:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Die [!UICONTROL Other Metadata] Abschnitt [!UICONTROL Goals & Settings] -Seite können Sie beliebige Informationen über Ihre Aktivität angeben, die für Sie oder andere Team-Mitglieder nützlich sind. Die Größe des Bereichs Notizen kann angepasst werden.|

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätseinstellungen (3:02) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

(https://video.tv.adobe.com/v/17381?captions=ger)

### Erstellen von A/B-Tests (8:36) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Aktivitätseinstellungen bei der Einrichtung einer Aktivität mit dem drei Schritte umfassenden, geleiteten Arbeitsablauf integriert werden können. Ziele und Einstellungen werden ab 5:30 erläutert.

* Erstellen einer A/B-Aktivität in Adobe Target
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
