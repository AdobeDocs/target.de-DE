---
keywords: Aktivitätseinstellungen;A/B-Ziele und -Einstellungen;Einstellungen der Berichterstellung;Zielmetriken;Erfolgsmetriken;abhängige Erfolgsmetriken;erweiterte Einstellungen;primäres Ziel;zusätzliche Metriken;Ziel;Priorität;Dauer;Berichtslösung;Ziele;Zielgruppen für die Berichterstellung;Welche Erfolgsmetriken müssen erreicht werden, bevor diese Metrik inkrementiert wird;Was passiert, nachdem ein Benutzer auf diese Zielmetrik stößt;Hinweise
description: Erfahren Sie, wie Sie auf der [!UICONTROL Ziele und Einstellungen] Informationen zu den Zielen einer A/B-Aktivität angeben.
title: Wie gebe ich Ziele und Einstellungen in A/A [!DNL Target] B-Aktivitäten an?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 37%

---

# Ziele und Einstellungen

Auf [!UICONTROL &#x200B; Seite „Ziele &#x200B;] Einstellungen“ in [!DNL Adobe Target] geben Sie Informationen zu den Zielen der Aktivität an.

Die verfügbaren Einstellungen hängen davon ab, ob Sie Target oder [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) als Berichtsquelle verwenden.

## [!UICONTROL Aktivitätseinstellungen] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Im Abschnitt [!UICONTROL Aktivitätseinstellungen] der Seite [!UICONTROL Ziele und Einstellungen] können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Ziel] | Geben Sie ein optionales Ziel ein. Das Ziel kann jede Information sein, die Ihnen und Ihren Team-Mitgliedern dabei hilft, die Aktivität zu identifizieren. |
| [!UICONTROL Priorität] | Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priorität]. Sie können die Legacy-Einstellungen von [!UICONTROL Niedrig], [!UICONTROL Medium] oder [!UICONTROL Hoch] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option in [!UICONTROL Administration) nicht aktiviert &#x200B;], geben Sie eine Priorität an: [!UICONTROL Niedrig], [!UICONTROL Medium] oder [!UICONTROL Hoch].<P>Um [feinabgestimmte Prioritäten](/help/main/administrating-target/reporting.md) zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und schalten Sie dann die Option [!UICONTROL Aktivieren feinabgestimmter Prioritäten] auf „Ein“ um. <P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an: 0 = [!UICONTROL Niedrig] und 999 = [!UICONTROL Hoch]. <P>Für Aktivitäten, die in früheren Versionen von [!DNL Target] erstellt wurden[!UICONTROL &#x200B; wird &#x200B;] Priorität auf 0, [!UICONTROL Medium &#x200B;] auf 5 und [!UICONTROL Hoch] auf 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.<P>Hinweis: Bevor Sie diese Option nach der Verwendung von feinkörnigen Prioritäten deaktivieren können, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden. |
| Dauer | Die Aktivität kann bei Genehmigung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00 :00 Mitternacht ist. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu. |

## [!UICONTROL Berichterstellungseinstellungen] {#section_13119392051044FBA6387D9B3B1C43CF}

Im [!UICONTROL Reporting-] der Seite [!UICONTROL Ziele und Einstellungen] können Sie die folgenden Optionen konfigurieren:

| Einstellungen | Beschreibung |
|--- |--- |
| [!UICONTROL Reporting-Source] | Geben Sie an, aus welcher Lösung Daten erfasst werden:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Wenn in Ihren [Kontoeinstellungen“ eine Berichtsquelle angegeben ist](/help/main/administrating-target/reporting.md) wird die angegebene Quelle verwendet, und diese Einstellung ist nicht sichtbar.<P>Sie können Ihre Berichtsquelle nicht ändern, nachdem die Aktivität live geschaltet wurde, um die Konsistenz der Berichte zu gewährleisten.<P>**Adobe Analytics**: Unter [Adobe Analytics als Reporting-Source für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) erfahren Sie mehr über die Unterschiede zwischen den Reporting-Lösungen und deren Vorteile. Bei der Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target] wählen Sie eine [!DNL Analytics] Report Suite aus, um [!DNL Target] Aktivitätsdaten zu erhalten.<P>Um eine Berichtsquelle anzugeben, wählen Sie zunächst eines der [!DNL Analytics] Unternehmen aus, mit denen Ihr Konto verknüpft ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Adobe Target] bereitgestellt wurden. Wenn die erwarteten Report Suites nicht angezeigt werden, versuchen Sie zunächst, sich abzumelden und sich wieder bei der [!DNL Adobe Experience Cloud] anzumelden, um es dann erneut zu versuchen. Wenn die Report Suite noch immer in der Liste fehlt, wenden Sie sich an die Kundenunterstützung.<P><P>**Adobe Customer Journey Analytics**: Siehe [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) für weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target].<P>[!DNL Target] Reporting in [!DNL Customer Journey Analytics] wird in A/B-Aktivitäten mit manueller Traffic-Aufteilung unterstützt. [!UICONTROL Automatisches Targeting] und [!UICONTROL Automatische Zuordnung] A/B-Aktivitäten können [!DNL Target] Berichte nicht in [!DNL Customer Journey Analytics] verwenden. |
| [!UICONTROL Zielmetrik] | Wählen Sie die Aktion, die von einem Besucher ergriffen wird, um das Ziel zu erreichen. Wählen Sie beispielsweise eine Metrik [!UICONTROL Konversion] und legen Sie dann die Parameter fest, die bestimmen, wann der Erfolg erzielt wird. Weitere Informationen zum Festlegen von Metriken finden Sie unter [Festlegen von Metriken](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Hinweis: Wenn für die Reporting-Lösung [!DNL Analytics] festgelegt ist, ist die einzige verfügbare Zielmetrik [!UICONTROL Konversion]. [!DNL Analytics] Metriken können nicht als Ziel ausgewählt werden. Bei der Auswahl Ihrer Erfolgsmetrik wird ein Selektor angezeigt. Verwenden Sie diesen Selektor, um Einzelheiten zu dieser Erfolgsmetrik auszuwählen.<P>Wenn diese Option aktiviert ist[!UICONTROL &#x200B; liefert der Feld „Geschätzter Wert der Konversion] (für die Metriken [!UICONTROL Seitenbewertung] nicht verfügbar) einen Wert für Ihr Ziel, aber nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Umsatz pro Besucher], [!UICONTROL Durchschnittlicher Bestellwert], [!UICONTROL Gesamtumsatz] und [!UICONTROL Bestellungen]) verwendet die Schätzung [!UICONTROL Umsatz pro Besucher]. Der Datentyp ist eine Währung.<P>Nach Erreichen des Aktivitätsziels wird einem Besucher weiterhin der Aktivitätsinhalt angezeigt, es sei denn, dieser Besucher qualifiziert sich für eine Aktivität mit höherer Priorität. Wenn der Besucher das Ziel erneut erreicht, wird dies als eine weitere Konversion gezählt. Dies unterscheidet sich vom Standardverhalten in [!DNL Target Classic], das Besucher als neu zählt, wenn sie die Aktivität erneut sehen. |
| [!UICONTROL Zusätzliche Metriken] | Erstellen Sie zusätzliche Erfolgsmetriken. Diese Einstellung ist nicht verfügbar, wenn die Reporting-Lösung auf [!DNL Analytics] festgelegt ist. In diesem Fall werden die für die [!DNL Analytics] Report Suite definierten Metriken angewendet. |
| [!UICONTROL Zielgruppen für das Reporting] | Standardmäßig zeigen Berichte Ergebnisse für alle qualifizierten Besucher. Sie können Berichtszielgruppen hinzufügen, um Informationen nur zu bestimmten Zielgruppen anzuzeigen. Diese Einstellung ist nicht verfügbar, wenn Sie [!DNL Analytics] als Berichtslösung auswählen. Die für die [!DNL Analytics] Report Suite definierte Zielgruppe wird angewendet. |

## Erweiterte Einstellungen {#section_E2FE441AFB324E498793ABB025ED9974}

Im [!UICONTROL Erweiterte Einstellungen] der Seite [!UICONTROL Ziele und Einstellungen] können Sie die folgenden Optionen konfigurieren:

Um erweiterte Einstellungen festzulegen, klicken Sie auf das Symbol **[!UICONTROL Mehr]** (das vertikale Auslassungszeichen) und dann auf **[!UICONTROL Erweiterte Einstellungen]**, wie in der folgenden Abbildung dargestellt.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option „Erweiterte Einstellungen“ ist nicht verfügbar.

![Erweiterte Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Einstellung | Beschreibung |
|--- |--- |
| [!UICONTROL Welche Erfolgsmetrik muss erreicht werden, bevor diese Metrik inkrementiert wird?] | Verwenden Sie diese Option, um zu zählen, dass eine Person die Erfolgsmetrik nur dann erreicht, wenn sie zuvor eine andere Erfolgsmetrik erreicht hat. Beispielsweise ist eine Aktivitätskonvertierung möglicherweise nur gültig, wenn der Besucher auf das Angebot klickt oder vor der Konvertierung auf eine bestimmte Seite gelangt. Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht. Definieren Sie beide (oder mehrere) Erfolgsmetriken, bevor Sie eine von einer anderen abhängig machen können. Mithilfe der Option [!UICONTROL Abhängigkeit hinzufügen] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde. So fügen Sie eine Abhängigkeit hinzu:<ul><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf [!UICONTROL Erweiterte Einstellungen].</li><li>Klicken Sie auf die Option [!UICONTROL Abhängigkeit hinzufügen]:</li><li>Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf [!UICONTROL Erreicht], um zwischen [!UICONTROL Erreicht] und [!UICONTROL Nicht erreicht] umzuschalten.</li><li>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.</li></ul> |
| [!UICONTROL Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?] | Es gibt drei Möglichkeiten, nachdem ein Besucher die Zielmetrik erreicht hat:<ul><li>Wählen Sie [!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen] aus, um festzulegen, wie die Anzahl erhöht wird.</li><li>Wählen Sie [!UICONTROL Anzahl erhöhen, Benutzer freigeben und Wiedereintritt erlauben] aus, um festzulegen, welches Erlebnis dem Benutzer angezeigt wird, wenn er die Aktivität wieder aufnimmt.</li><li>Wählen Sie [!UICONTROL Anzahl erhöhen, Benutzer und Leiste aus Wiedereintritt freigeben], um anzugeben, was der Benutzer anstelle des Aktivitätsinhalts sieht.</li></ul> |
| [!UICONTROL Wie wird die Anzahl erhöht?] | Es gibt drei Möglichkeiten, wie die Anzahl erhöht werden kann:<ul><li>[!UICONTROL Einmal pro Teilnehmer]</li><li>[!UICONTROL Bei jeder Impression (ohne Seitenaktualisierungen)]</li><li>[!UICONTROL Bei jeder Impression]</li></ul> |

Weitere Informationen zu erweiterten Einstellungen finden Sie unter [Erfolgsmetriken](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

## Sonstige Metadaten {#section_2E8917BEFB954480A4206B9E9E917F80}

Im Abschnitt [!UICONTROL Sonstige Metadaten] der Seite [!UICONTROL Ziele und Einstellungen] können Sie alle Informationen zu Ihrer Aktivität angeben, die Sie für sich selbst oder andere Team-Mitglieder verfügbar halten können. Die Größe des Notizenbereichs kann geändert werden.|

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

### Erstellen von A/B-Tests (:36) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Aktivitätseinstellungen bei der Einrichtung einer Aktivität mit dem drei Schritte umfassenden, geleiteten Arbeitsablauf integriert werden können. Die Ziele und Einstellungen werden ab 5 Uhr :30.

* Erstellen einer A/B-Aktivität in Adobe Target
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
