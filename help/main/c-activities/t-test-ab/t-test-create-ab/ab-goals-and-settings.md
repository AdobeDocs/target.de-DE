---
keywords: Aktivitätseinstellungen;A/B-Ziele und -Einstellungen;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie die [!UICONTROL Ziele und Einstellungen] Seite in [!DNL Adobe Target] um Informationen über die Ziele einer A/B-Aktivität anzugeben.
title: Wie gebe ich Ziele und Einstellungen in einer [!DNL Target] A/B-Aktivität?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 52%

---

# Ziele und Einstellungen

Die [!UICONTROL Ziele und Einstellungen] Seite in [!DNL Adobe Target] Hier geben Sie Informationen zu den Zielen der Aktivität an.

Die verfügbaren Einstellungen hängen davon ab, ob Sie Target oder [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) als Berichtsquelle.

## [!UICONTROL Aktivitätseinstellungen] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Die [!UICONTROL Aktivitätseinstellungen] Abschnitt [!UICONTROL Ziele und Einstellungen] -Seite können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Ziel] | Geben Sie ein optionales Ziel ein. Das Ziel kann jede Information sein, die Ihnen und Ihren Teammitgliedern dabei hilft, die Aktivität zu identifizieren. |
| [!UICONTROL Priorität] | Abhängig von Ihren Einstellungen wird die [!DNL Target] Benutzeroberfläche und Optionen für [!UICONTROL Priorität] variieren. Sie können die veralteten Einstellungen von [!UICONTROL Niedrig], [!UICONTROL Mittel]oder [!UICONTROL Hoch]oder Sie können genauer unterteilte Prioritäten von 0 bis 999 festlegen.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option nicht aktiviert ist in [!UICONTROL Administration] (Standardeinstellung), geben Sie eine Priorität an: [!UICONTROL Niedrig], [!UICONTROL Mittel]oder [!UICONTROL Hoch].<P>Aktivieren [Präzise Prioritäten](/help/main/administrating-target/reporting.md)klicken [!UICONTROL Administration] > [!UICONTROL Berichterstellung], und schalten Sie dann die [!UICONTROL Aktivieren genauer Prioritätensetzung] auf die Position &quot;Ein&quot;. <P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an: 0 = [!UICONTROL Niedrig] und 999 = [!UICONTROL Hoch]. <P>Für Aktivitäten, die in früheren Versionen von [!DNL Target], [!UICONTROL Niedrig] die Priorität in 0 umgewandelt wird, [!UICONTROL Mittel] in 5 umgewandelt wird und [!UICONTROL Hoch] wird in 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.<P>Hinweis: Haben Sie genauere Prioritäten verwendet und möchten Sie die Option deaktivieren, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden. |
| Dauer | Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu. |

## [!UICONTROL Berichterstellungseinstellungen ] {#section_13119392051044FBA6387D9B3B1C43CF}

Die [!UICONTROL Berichtseinstellungen] Abschnitt [!UICONTROL Ziele und Einstellungen] -Seite können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Berichtsquelle] | Festlegen, ob Daten erfasst werden sollen von [!DNL Adobe Target] oder von [!DNL Adobe Analytics]. Informationen über die Unterschiede zwischen den Berichterstellungslösungen und deren jeweilige Vorteile finden Sie unter [Adobe Analytics als Berichterstellungsquelle für Target. ](/help/main/c-integrating-target-with-mac/a4t/a4t.md) Bei Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target], wählen Sie eine [!DNL Analytics] Report Suite, die empfangen wird [!DNL Target] Aktivitätsdaten.<P>Um eine Berichtsquelle anzugeben, wählen Sie zunächst eine der [!DNL Analytics] Unternehmen, an die Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Nur Report Suites, für die eine Verbindung hergestellt wurde [!DNL Adobe Target] stehen zur Auswahl zur Verfügung. Wenn die erwarteten Report Suites nicht angezeigt werden, melden Sie sich zunächst ab und melden Sie sich wieder bei der [!DNL Adobe Experience Cloud] erneut versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die Kundenunterstützung.<P>Sollte in Ihren Kontoeinstellungen eine Berichterstellungsquelle angegeben sein, wird die angegebene Quelle verwendet und diese Einstellung ist nicht sichtbar.<P>Hinweis: Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten. |
| [!UICONTROL Zielmetrik] | Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Konversion] und legen Sie dann die Parameter fest, die bestimmen, wann ein Erfolg erreicht wird. Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Hinweis: Wenn die Berichterstellungslösung auf [!DNL Analytics], lautet die einzige verfügbare Zielmetrik . [!UICONTROL Konversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden. Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.<P>Wenn diese Option aktiviert ist, wird die [!UICONTROL Geschätzter Wert der Konversion] -Feld (nicht verfügbar für [!UICONTROL Seitenergebnis] Metriken) einen Wert für Ihr Ziel bereitstellt, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Umsatz pro Besucher], [!UICONTROL Durchschnittlicher Bestellwert], [!UICONTROL Gesamtverkäufe], und [!UICONTROL Bestellungen]), verwendet die Schätzung [!UICONTROL Umsatz pro Besucher]. Der Datentyp ist eine Währung.<P>Nach Erreichen des Aktivitätsziels sieht ein Besucher weiterhin den Aktivitätsinhalt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dies unterscheidet sich vom Standardverhalten in [!DNL Target Classic], was Besucher als neu zählt, wenn sie die Aktivität erneut sehen. |
| [!UICONTROL Zusätzliche Metriken] | Erstellen Sie zusätzliche Erfolgsmetriken. Diese Einstellung ist nicht verfügbar, wenn die Berichterstellungslösung auf [!DNL Analytics]. In diesem Fall werden die für die [!DNL Analytics] Report Suite angewendet werden. |
| [!UICONTROL Zielgruppen für die Berichterstellung] | Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen zu bestimmten Zielgruppen anzuzeigen. Diese Einstellung ist nicht verfügbar, wenn Sie [!DNL Analytics] als Berichterstellungslösung. Die für die [!DNL Analytics] Report Suite angewendet wird. |

## Erweiterte Einstellungen   {#section_E2FE441AFB324E498793ABB025ED9974}

Die [!UICONTROL Erweiterte Einstellungen] Abschnitt [!UICONTROL Ziele und Einstellungen] -Seite können Sie die folgenden Optionen konfigurieren:

Um erweiterte Einstellungen festzulegen, klicken Sie auf das **[!UICONTROL Mehr]** Symbol (die vertikalen Auslassungspunkte), und klicken Sie dann auf **[!UICONTROL Erweiterte Einstellungen]**, wie in der folgenden Abbildung dargestellt.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option für erweiterte Einstellungen ist nicht verfügbar.

![Erweiterte Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Einstellung | Beschreibung |
|--- |--- |
| [!UICONTROL Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird?] | Verwenden Sie diese Option, um nur Personen zu zählen, die die Erfolgsmetrik erreicht haben, wenn sie zuvor eine andere Erfolgsmetrik erreicht haben. Eine Aktivitätskonversion kann beispielsweise nur dann gültig sein, wenn der Besucher auf das Angebot klickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt. Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht. Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine Abhängigkeit voneinander festlegen können. Mithilfe der Option [!UICONTROL Abhängigkeit hinzufügen] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde. So fügen Sie eine Abhängigkeit hinzu:<ul><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf [!UICONTROL Erweiterte Einstellungen].</li><li>Klicken Sie auf die Option [!UICONTROL Abhängigkeit hinzufügen]:</li><li>Verschieben Sie die gewünschte Metrik per Drag-and-drop vom linken Bereich in den rechten Bereich. Klicken Sie dann auf [!UICONTROL Erreicht][!UICONTROL , um die Einstellung zwischen Erreicht und Nicht erreicht zu wechseln].</li><li>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.</li></ul> |
| [!UICONTROL Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?] | Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:<ul><li>Wählen Sie [!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen] aus, um festzulegen, wie die Anzahl erhöht wird.</li><li>Wählen Sie [!UICONTROL Anzahl erhöhen, Benutzer freigeben und Wiedereintritt erlauben] aus, um festzulegen, welches Erlebnis dem Benutzer angezeigt wird, wenn er die Aktivität wieder aufnimmt.</li><li>Wählen Sie [!UICONTROL Anzahl erhöhen, Benutzer freigeben und an Wiedereintritt hindern] aus, um festzulegen, was dem Benutzer statt der Aktivitätsinhalte angezeigt wird.</li></ul> |
| [!UICONTROL Wie wird die Anzahl erhöht?] | Es gibt drei Möglichkeiten, wie die Anzahl erhöht werden kann:<ul><li>[!UICONTROL Einmal pro Teilnehmer]</li><li>[!UICONTROL Bei jeder Impression (außer bei Seitenaktualisierungen)]</li><li>[!UICONTROL Bei jeder Impression]</li></ul> |

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Die [!UICONTROL Sonstige Metadaten] Abschnitt [!UICONTROL Ziele und Einstellungen] -Seite können Sie beliebige Informationen über Ihre Aktivität angeben, die für Sie oder andere Team-Mitglieder nützlich sind. Die Größe des Anmerkungen-Feldes kann geändert werden.|

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
