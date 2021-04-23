---
keywords: Aktivitätseinstellungen;A/B-Ziele und -Einstellungen;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie auf der Seite "Ziele und Einstellungen"in Adobe [!DNL Target] Informationen über die Ziele einer A/B-Aktivität angeben können.
title: Wie gebe ich Ziele und Einstellungen in einer [!DNL Target] A/B-Aktivität an?
feature: A/B-Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 92%

---

# Ziele und Einstellungen

Auf der Seite &quot;Ziele und Einstellungen&quot;in [!DNL Adobe Target] geben Sie Informationen zu den Zielen des Tests ein.

Welche Einstellungen verfügbar sind, hängt davon ab, ob Sie als Datenquelle Target oder [Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md) verwenden.

![Dialogfeld „Aktivitätseinstellungen“](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

## Aktivitätseinstellungen {#section_DCBDC354261F420EBD4B43EA34947BAC}

| Einstellungen | Beschreibung |
|--- |--- |
| Ziel | Geben Sie ein optionales Ziel ein. Beim Ziel kann es sich um beliebige Informationen handeln, die Ihnen und Ihren Team-Mitgliedern beim Identifizieren der Kampagne helfen. |
| Priorität | Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.<br>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<br>Wenn diese Option in  [!UICONTROL Administration]  nicht aktiviert ist (Standard), geben Sie eine Priorität an: Niedrig, mittel oder hoch. <br>Klicken Sie zum Aktivieren der Feinabstufungen auf   [!UICONTROL Administration]  >  [!UICONTROL Berichte] und aktivieren Sie dann die Option Feinkörnige Prioritäten aktivieren auf die Position &quot;Ein&quot;. <br>Ist diese Option aktiviert, legen Sie einen Wert zwischen 0 und 999 fest: 0 = Niedrig und 999 = Hoch. <br>Bei Aktivitäten, die in älteren Versionen von Target Standard/Premium erstellt wurden, wird eine niedrige Priorität in den Wert 0, eine mittlere in den Wert 5 und eine hohe in den Wert 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.<br>Hinweis: Haben Sie genauere Prioritäten verwendet und möchten Sie die Option deaktivieren, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden. |
| Dauer | Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu. |

## Berichterstellungseinstellungen   {#section_13119392051044FBA6387D9B3B1C43CF}

| Einstellungen | Beschreibung |
|--- |--- |
| Berichtsquelle | Geben Sie an, ob die Daten von Adobe Target oder Adobe Analytics erfasst werden. Informationen über die Unterschiede zwischen den Berichterstellungslösungen und deren jeweilige Vorteile finden Sie unter [Adobe Analytics als Berichterstellungsquelle für Target.  ](/help/c-integrating-target-with-mac/a4t/a4t.md)  Wenn Sie Analytics als Berichtsquelle für Target auswählen, wählen Sie eine Analytics-Report Suite, um Target-Aktivitätsdaten zu empfangen.<br>Wählen Sie dazu zunächst ein Analytics-Unternehmen aus, an das ihr Konto gebunden ist, und wählen Sie anschließend die der Aktivität entsprechende Report Suite aus. Es stehen nur Report Suites, die für die Verbindung mit Adobe Target bereitgestellt werden, zur Auswahl zur Verfügung. Wenn nicht die erwarteten Report Suites angezeigt werden, versuchen Sie, sich bei Adobe Experience Cloud ab- und dann wieder anzumelden, und wiederholen Sie den Vorgang. Wenn die Report Suite weiterhin nicht in der Liste zu finden ist, wenden Sie sich an den Kundendienst.<br>Sollte in Ihren Kontoeinstellungen eine Berichterstellungsquelle angegeben sein, wird die angegebene Quelle verwendet und diese Einstellung ist nicht sichtbar.<br>Hinweis: Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, da die Berichte sonst nicht mehr konsistent wären. |
| Ziel | Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie zum Beispiel eine Konversionsmetrik und stellen Sie dann die Parameter ein, anhand derer festgestellt wird, dass ein Erfolg erreicht wurde.  Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<br>Hinweis: Wenn bei Berichterstellungslösung Analytics eingestellt ist, lautet die einzige verfügbare Zielmetrik „Konversion“. Es ist nicht möglich, Analytics-Metriken als Ziel auszuwählen.   Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.<br>Bei Aktivierung bietet der geschätzte Wert des Konversionsfeldes (nicht verfügbar für Seitenergebnis-Metriken) einen Wert für Ihr Ziel, jedoch nicht für andere Metriken. Mit diesem Wert kann Target die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Die Schätzung verwendet für alle Umsatzmetriken (Umsatz pro Besucher, durchschnittlicher Bestellwert, Gesamtverkäufe und Bestellungen) die Metrik „Umsatz pro Besucher“. Der Datentyp ist eine Währung.<br>Nach Erreichen des Aktivitätsziels sieht ein Besucher weiterhin den Aktivitätsinhalt, es sei denn, dieser Besucher ist qualifiziert für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Beachten Sie, dass sich dieses Verhalten vom Standardverhalten in Target Classic unterscheidet, da Besucher dort als neu gezählt werden, wenn Sie den Test erneut sehen. |
| Zusätzliche Metriken | Erstellen Sie zusätzliche Erfolgsmetriken.  Diese Einstellung ist nicht verfügbar, wenn Analytics als Berichterstellungslösung eingestellt ist. In diesem Fall werden die für die Analytics-Berichtssuite definierten Metriken angewendet. |
| Zielgruppen für die Berichterstellung | Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um nur Informationen über bestimmte Zielgruppen zu zeigen.  Diese Einstellung ist nicht verfügbar, wenn Sie Analytics als Berichterstellungslösung wählen. Die für die Analytics Report Suite definierten Zielgruppen werden angewendet. |

## Erweiterte Einstellungen {#section_E2FE441AFB324E498793ABB025ED9974}

Erweiterte Einstellungen sind für A/B-Test-Zielmetriken verfügbar.

![Menü „Erweiterte Einstellungen“](/help/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Wenn Sie Adobe Analytics als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom Analytics-Server verwaltet. Die Option für erweiterte Einstellungen steht nicht zur Verfügung.

![Erweiterte Einstellungen](/help/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Einstellung | Beschreibung |
|--- |--- |
| Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik erhöht wird? | Verwenden Sie diese Option, um die Erfolgsmetrik nur dann als erreicht zu werten, wenn jemand vorher bereits eine andere Erfolgsmetrik erreicht hat. So kann eine Testkonversion nur dann gültig sein, wenn der Besucher das Angebot anklickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.  Sie können für mehrere Metriken eine Abhängigkeit bereitstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.  Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.  Mithilfe der Option Abhängigkeit hinzufügen kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.  So fügen Sie eine Abhängigkeit hinzu:<ul><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf Erweiterte Einstellungen.</li><li>Klicken Sie auf die Option Abhängigkeit hinzufügen:</li><li>Verschieben Sie die gewünschte Metrik per Drag-and-drop vom linken Bereich in den rechten Bereich. Klicken Sie dann auf Erreicht, um die Einstellung zwischen Erreicht und Nicht erreicht zu wechseln.</li><li>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.</li></ul> |
| Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft? | Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:<ul><li>Wählen Sie „Anzahl erhöhen und Benutzer in Aktivität belassen“ aus, um festzulegen, wie die Anzahl erhöht wird.</li><li>Wählen Sie „Anzahl erhöhen, Benutzer freigeben und Wiedereintritt erlauben“ aus, um festzulegen, welches Erlebnis dem Benutzer angezeigt wird, wenn er die Aktivität wieder aufnimmt.</li><li>Wählen Sie „Anzahl erhöhen, Benutzer freigeben und an Wiedereintritt hindern“ aus, um festzulegen, was dem Benutzer statt der Aktivitätsinhalte angezeigt wird.</li></ul> |
| Wie wird die Anzahl erhöht? | Es gibt drei Möglichkeiten, wie die Anzahl erhöht werden kann:<ul><li>Einmal pro Teilnehmer</li><li>Bei jeder Impression (außer bei Seitenaktualisierungen)</li><li>Bei jeder Impression</li></ul> |

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

| Einstellungen | Beschreibung |
|---|---|
| Hinweise | Geben Sie sämtliche Informationen ein, die für Sie und Ihre Team-Mitglieder von Nutzen sind. Die Größe des Anmerkungen-Feldes kann geändert werden. |

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivität Settings (3:02) ![Tutorial badge](/help/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

(https://video.tv.adobe.com/v/17381?captions=ger)

### Erstellen von A/B-Tests (8:36) ![Tutorialzeichen](/help/assets/tutorial.png)

In diesem Video wird gezeigt, wie Aktivitätseinstellungen bei der Einrichtung einer Aktivität mit dem drei Schritte umfassenden, geleiteten Arbeitsablauf integriert werden können. Ziele und Einstellungen werden ab 5:30 erläutert.

* Erstellen einer A/B-Aktivität in Adobe Target
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
