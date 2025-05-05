---
keywords: Target; Berichte; Berichtseinstellungen; Voreinstellung; Target-Vorgabe; Metrik; Zielgruppe; Datumsbereich; Einstellungen; Download; Tabellenansicht; Graphansicht; durchschnittliche Steigerung; Steigerung; Steigerungsgrenzen; Konfidenzintervall; Konfidenz; Ortseinfluss; laufender Durchschnitt; Zählmethodik
description: Erfahren Sie, wie Sie Berichteinstellungen in Adobe Target konfigurieren, einschließlich Metriken, Zielgruppen, Datumsbereiche und mehr.
title: Wie konfiguriere ich Berichteinstellungen?
feature: Reports
exl-id: 337579d1-c678-43b6-9e80-b5abe159c2d3
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '1778'
ht-degree: 48%

---

# Berichtseinstellungen

Hilfreiche Informationen zum Festlegen der Elemente, die im Bericht in [!DNL Adobe Target] angezeigt werden sollen. Berichtseinstellungen können für eine spätere Verwendung gespeichert werden.

So zeigen Sie einen Bericht an:

1. Klicken Sie auf **[!UICONTROL Activities]** und klicken Sie dann in der Liste auf die gewünschte Aktivität.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Reports]** .

   ![Benutzeroberfläche für den Bericht](/help/main/c-reports/c-report-settings/assets/report-ui-refresh.png)

## Zielvorgabe {#section_51F67341465045BEB4F1A2FB638A8EB1}

Sie können bis zu zehn verschiedene Voreinstellungen für die Berichte der einzelnen Aktivitäten speichern, nachdem Sie sie wie gewünscht konfiguriert haben (Metriken, Zielgruppen, erweiterte Einstellungen usw.). Alle [!DNL Target] Benutzer können die verschiedenen Voreinstellungen anzeigen, bearbeiten und löschen, unabhängig davon, wer sie erstellt hat.

Sie können auch einzelne Aktivitätsberichte nach Bedarf konfigurieren und als Standardeinstellung oder Favoriten speichern. So wird jedes Mal, wenn Sie den Bericht der entsprechenden Aktivität öffnen, diese Ansicht angezeigt.

### Erstellen einer Voreinstellung oder Standardvorgabe

1. Konfigurieren Sie den Bericht der Aktivität nach Bedarf.

   Die verfügbaren Einstellungen, einschließlich Metriken, Datumsbereiche, Zielgruppen, erweiterte Einstellungen usw., werden unten erläutert.

1. Klicken Sie neben **[!UICONTROL Target Preset]** auf das Symbol **[!UICONTROL More Options]** ( ![Symbol Weitere Optionen](/help/main/assets/icons/MoreSmallListVert.svg) ) > **[!UICONTROL Save as New]**.

   Das Dialogfeld [!UICONTROL Create Preset] wird angezeigt.

   ![Dialogfeld für neue Voreinstellung](/help/main/c-reports/c-report-settings/assets/report_preset_dialog-new.png)

1. Überprüfen Sie die Informationen in den **[!UICONTROL Filters]** Abschnitten, um sicherzustellen, dass der Bericht wie gewünscht konfiguriert ist, und geben Sie dann die **[!UICONTROL Preset Name]** (bis zu 50 Zeichen) an.
1. (Bedingt) Wenn Sie dies als Standard-/Lieblingsberichtsansicht verwenden möchten, schieben Sie den Umschalter **[!UICONTROL Set as default preset]** auf „Ein“.
1. Klicken Sie auf **[!UICONTROL Create]**.

### Andere Vorgabe auswählen

Wählen Sie die gewünschte Vorgabe aus der Dropdown-Liste **[!UICONTROL Target Preset]** aus.

### Bearbeiten einer Voreinstellung

1. Wählen Sie die Voreinstellung aus, die Sie bearbeiten möchten.
1. Bearbeiten Sie die Berichtskonfiguration wie gewünscht (Metriken, Datumsbereiche, Zielgruppen, erweiterte Einstellungen usw.).

   Nachdem Sie nach der Bearbeitung der Berichtskonfiguration auf [!UICONTROL Save] geklickt haben, wird nach dem Namen der Vorgabe ein Sternchen ( &#42; ) angezeigt, um anzugeben, dass die Vorgabe geändert wurde.

1. Klicken Sie auf das Symbol **[!UICONTROL More Options]** ( ![Symbol „Weitere Optionen](/help/main/assets/icons/MoreSmallListVert.svg) ) > **[!UICONTROL Save as New]** , um eine neue Vorgabe zu erstellen.

### Löschen einer Vorgabe

1. Wählen Sie die Voreinstellung aus, die Sie löschen möchten.
1. Klicken Sie auf das Symbol **[!UICONTROL More Options]** ( ![Symbol „Weitere Optionen](/help/main/assets/icons/MoreSmallListVert.svg) ) > **[!UICONTROL Delete]**.

1. Klicken Sie erneut auf **[!UICONTROL Delete]** , um das Löschen zu bestätigen (gelöschte Voreinstellungen können nicht wiederhergestellt werden).

### Behandlung von Voreinstellungsfehlern

Warnhinweise und Meldungen weisen Sie darauf hin, wenn eine Voreinstellung ungültig ist. Die Hinweise oder Meldungen enthalten Anweisungen zur Auswahl einer anderen Zielgruppe, Metrik oder Hostgruppe oder eines anderen Erlebnisses, um das Problem zu beheben.

Die folgende Liste enthält Beschreibungen zu verschiedenen Situationen, in denen Voreinstellungen ungültig sein können:

* Eine Berichtsgruppe wurde aus der Aktivität entfernt, ist jedoch noch in der Definition der Voreinstellung enthalten.
* Mindestens eine Metrik wurde gelöscht, ist jedoch noch in der Definition der Voreinstellung enthalten (wenn Sie beispielsweise eine oder mehrere Metriken aus der Aktivität löschen und anschließend neue Metriken hinzufügen).
* Mindestens eine Hostgruppe wurde gelöscht, ist jedoch noch in der Definition der Voreinstellung enthalten.
* Mindestens ein Erlebnis wurde gelöscht, ist jedoch noch in der Definition der Voreinstellung enthalten.
* Eine Voreinstellung weist eine fehlerhafte Semantik auf, da referenzierte Elemente zwar vorhanden sind, aber auf eine Weise aktualisiert wurden, die sich auf die Semantik der Einstellungsdefinition ausgewirkt hat. Gehen Sie beispielsweise von einer Voreinstellung namens „Umsätze über Chrome“ aus. Nach Erstellung der Voreinstellung ändern Sie die Aktivität, damit sie die Konversions- statt der Umsatzmetrik misst. Durch diese Aktualisierung der Aktivitätsdefinition wird die Voreinstellungsdefinition semantisch ungültig.

## [!UICONTROL Report Metric] {#section_894ABD7148244806B7CE556EBBA2AD62}

Klicken Sie auf die Dropdown-Liste **[!UICONTROL Report Metric]** , um eine andere [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) oder mehrere Metriken auszuwählen, die im Diagramm angezeigt werden sollen.

Standardmäßig wird die primäre Metrik in der Einrichtung der Erfolgsmetriken beim Erstellen der Aktivität bestimmt. Wenn Sie die Einrichtung ändern und die Aktivität erneut speichern, wird die primäre Metrik für die Berichterstattung aktualisiert.

Weitere Informationen zur Auswahl mehrerer Metriken, die in Berichten angezeigt werden sollen, finden Sie unter [Anzeigen mehrerer Metriken in einem Bericht](/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7).

## [!UICONTROL Audience] {#section_70926EB4618945D9AFF2B0564FF3717B}

Klicken Sie auf die Dropdown-Liste **[!UICONTROL Audience]** , um die angezeigte Zielgruppe für den Bericht zu ändern.

Weitere Informationen finden Sie unter [Zielgruppen](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522).

## [!UICONTROL Preset Date Range]

Klicken Sie auf die Dropdown-Liste **[!UICONTROL Preset Date Range]** , um aus voreingestellten Datumsbereichen auszuwählen.

Neue **[!UICONTROL Start]** und **[!UICONTROL End]** für den Bericht auswählen. Sie können auch die Bereiche **[!UICONTROL Start of Activity]** und **[!UICONTROL Start of activity - End of Activity]** verwenden.

Vordefinierte Datumsbereiche umfassen: Letzte 7 Tage, Letzte 15 Tage oder Letzte 30 Tage. Diese vordefinierten Datumsbereiche werden automatisch weiterverschoben. Wenn das Startdatum kleiner ist als die Anzahl der ausgewählten Tage, zeigt der Kalender den Bereich ab dem Startdatum an, meldet aber erst dann ein Rollout, wenn das Startdatum älter wird als die Anzahl der ausgewählten Tage, wenn die Aktivitätsdauer ansteigt.

Für Berichte gelten folgende Datenbeschränkungen:

* Das Startdatum des Berichts muss innerhalb der letzten beiden Jahre liegen.
* Berichte von Angebotsgruppen sind auf 99 Tage ab dem aktuellen Tag beschränkt.
* Stündliche Berichte sind auf 15 Tage beschränkt.

## Datumsbereich {#section_A410A768403C4E01891F95CB357E63ED}

Im [!UICONTROL Date Range] wird der aktuelle Datumsbereich des Berichts angezeigt. Klicken Sie auf das **[!UICONTROL Calendar]** ( ![Kalendersymbol](/help/main/assets/icons/Calendar.svg) ), um einen Kalender anzuzeigen, in dem Sie den Datumsbereich des Berichts ändern können.

## Einstellungen {#section_D99CE462107D45CABE0960F820E1E972}

So konfigurieren Sie Berichteinstellungen:

1. Klicken Sie auf das Symbol **[!UICONTROL Report Settings]** ![Berichteinstellungen](/help/main/assets/icons/Setting.svg) ) und nehmen Sie die gewünschten Änderungen vor (wie unten beschrieben).
1. Klicken Sie abschließend auf **[!UICONTROL Save]** .

Die Optionen variieren abhängig vom gewählten Aktivitätstyp:

### Zählmethodik

Wählen Sie die gewünschte Methode aus:

* Besuchern
* Besuchen
* Aktivitätsimpressionen

### Kontrolle

Auswahl des Kontrollerlebnisses, das beim Berechnen und Vergleichen der Steigerung verwendet werden soll.

### Umgebung {#environment}

Wählen Sie die Umgebung (Hostgruppe) aus, die für den Bericht verwendet werden soll. Weitere Informationen finden Sie unter [Hosts](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

>[!NOTE]
>
>Wenn Ihr Unternehmen [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de){target=_blank} (AEP) verwendet, um Metrikdaten an [!DNL Target] zu senden, sollte die Umgebung im AEP-Datenstrom mit der Umgebung in Ihren [!DNL Target] Berichteinstellungen übereinstimmen.

### Berichtsdaten zurücksetzen

Klicken Sie auf [!UICONTROL Reset Report Data]. Berichtsdaten zurücksetzen, um alte Daten zu entfernen. Aktuelle Besucher verbleiben in der Aktivität.  Diese Option ist nur für Benutzer mit [!UICONTROL Approver] Berechtigungen verfügbar.

>[!IMPORTANT]
>
>Dies ist eine dauerhafte Aktion und kann nicht rückgängig gemacht werden.

Extremwerte ausschließen

Der Umschalter [!UICONTROL Exclude Extreme Values] gilt nur für Aktivitäten mit den Metriktypen Umsatz und Interaktion . Weitere Informationen finden Sie unter [Ausschließen extremer Bestellungen](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

## Download  {#section_77E65C50BAAF4AB79242DB3A8778ADEF}

Klicken Sie auf das **[!UICONTROL Download]**-Symbol ![Download-](/help/main/assets/icons/Download.svg) ), um Berichtsdaten in einem [!DNL .csv] Format für den schnellen Import in Excel, Access oder andere Datenanalyseprogramme herunterzuladen.

Weitere Informationen finden Sie unter [Herunterladen von Daten in einer CSV-Datei](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md).

## Aktualisieren {#section_E203729F2F314DF3856D2EE67C60B370}

Klicken Sie auf das Symbol **[!UICONTROL Refresh]** ( ![Aktualisierungssymbol](/help/main/assets/icons/Refresh.svg) ), um die Tabellen- und Diagrammansicht eines Berichts zu aktualisieren, ohne die gesamte Seite, ihre Konfiguration oder ihren Datumsbereich zu aktualisieren.

## Weitere Optionen {#section_AB1B5C695D7045A0A0AC0E2698D2E7DE}

Klicken Sie auf das Symbol **[!UICONTROL More Options]** ( ![Symbol „Weitere Optionen](/help/main/assets/icons/MoreSmallListVert.svg) ), um auf die [!UICONTROL Save as New] und [!UICONTROL Delete] Optionen zuzugreifen.

## Optionen anzeigen

Je nach Aktivitätstyp können Sie den Bericht in verschiedenen Formaten anzeigen. Wählen Sie die gewünschte Option aus.

* **Tabellenansicht**: Klicken Sie auf das Symbol **[!UICONTROL Table View]** ( ![Tabellenansichtssymbol](/help/main/assets/icons/Table.svg) ), um den Bericht als Tabelle anzuzeigen.
* **Diagrammansicht**: Klicken Sie auf das **[!UICONTROL Graph View]** ( ![Diagrammansichtssymbol](/help/main/assets/icons/GraphTrend.svg) ), um den Bericht als Diagramm anzuzeigen.
* **Automatisierte Segmente**:(Nur für [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Auto-Target] (AT)-Aktivitäten verfügbar.) Klicken Sie auf das Symbol **[!UICONTROL Automated Segments] ( ![Symbol für automatisierte Segmente](/help/main/assets/icons/AutomatedSegment.svg) ), um den Bericht [Automatisierte Segmente“ ](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).
* **Wichtige Attribute**: (Nur für [!DNL Automated Personalization] (AP)- und [!UICONTROL Auto-Target] (AT)-Aktivitäten verfügbar.) Klicken Sie auf das Symbol **[!UICONTROL Important Attributes]** ( ![Wichtige Attribute](/help/main/assets/icons/ViewList.svg) ), um den Bericht [Wichtige Attribute](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) anzuzeigen.

## Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall {#section_0D87615B1D3344B3858BA494EEBC16FB}

Berichte enthalten verschiedene Datenpunkte und Visualisierungsdarstellungen, anhand derer Sie die Steigerungsgrenzen und das Konfidenzniveau nachvollziehen können, die mit Ihrer Aktivität verbunden sind. Dadurch lässt sich ein Gewinner genauer ermitteln.

Weitere Informationen finden Sie unter [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

Beachten Sie Folgendes:

* Nur verfügbar, wenn Berichte in [!UICONTROL Table View] angezeigt werden.
* Diese Funktion steht nicht für Aktivitäten zur Verfügung, die [Analytics als Berichtsquelle verwenden (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## Ortsbeschränkung  {#section_5832F126AC114AE1ABFFF4D9B904393B}

Klicken Sie auf das Symbol [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![Location Contribution](/help/main/assets/icons/LocationContribution.svg) ), um den Bericht so umzuschalten, dass der Beitrag für Aktivitäten des Typs Multivariater Test (MVT) nach Standort angezeigt wird.

## Erlebnisse {#section_3A450DE1FA7E43F0AAB73165EC3D1C34}

Nur verfügbar, wenn der Bericht in [!UICONTROL Graph View] angezeigt wird.

Wählen Sie auf der linken Seite des Diagramms Erlebnisse aus oder heben Sie die Auswahl auf, um die entsprechenden Erlebnisse in das Diagramm ein- oder aus dem Diagramm auszublenden.

## Gleitendes Mittel {#section_59066693158C4433B87D07402C2BC6CD}

Nur verfügbar, wenn der Bericht in [!UICONTROL Graph View] angezeigt wird.

„Laufender Durchschnitt“ spiegelt die kumulativen Konversionen (vom Beginn des Reporting-Fensters bis zum im Diagramm dargestellten Datum) dividiert durch die kumulativen Besucher wider.

Wählen Sie die gewünschte Grafikansicht:

* Gleitendes Mittel
* Gleitendes Mittel der Steigerung
* Täglich
* Tägliche Steigerung

Der Name dieser Dropdown-Liste variiert je nach ausgewählter Ansicht, es handelt sich jedoch um eine der oben aufgeführten Ansichten.

## Zählmethodik {#section_01B0ED5665C74AE1AE97259800190C3E}

Nur verfügbar, wenn der Bericht in [!UICONTROL Graph View] angezeigt wird.

Sie können die Zählmethodologie für Diagramme in Berichten wählen. Beachten Sie, dass dies für [!UICONTROL Automated Personalization] (AP)-Aktivitäten nicht unterstützt wird.

Um auf die Option [!UICONTROL Counting Methodology] zuzugreifen, während Sie einen Bericht im Diagrammmodus anzeigen, klicken Sie auf die Dropdown-Liste **[!UICONTROL My Primary Goal]** und wählen Sie dann die Zählmethode aus.

Die Zählmethodik entspricht der im oben beschriebenen [!UICONTROL Settings]-Dialogfeld ausgewählten.

Standardmäßig wird das Diagramm im [!UICONTROL Daily]-Modus dargestellt.

Sie können den Modus ändern, indem Sie auf die Dropdown-Liste [!UICONTROL Daily] klicken und dann eine kumulative Option auswählen.

>[!NOTE]
>
>Der Name dieser Dropdown-Liste hängt vom ausgewählten Modus ab.

Es gibt vier Modi für [!UICONTROL Auto-Target] Aktivitäten: [!UICONTROL Daily Control], [!UICONTROL Daily Targeted], [!UICONTROL Cumulative Control] und [!UICONTROL Cumulative Targeted].

Die Standardreihenfolge, in der das Diagramm gezeichnet wird, lautet wie folgt:

* **[!UICONTROL A/B Test] (einschließlich [!UICONTROL Auto-Allocate] und [!UICONTROL Automated Personalization])**: Reihenfolge der Erlebniserstellung in absteigender Reihenfolge.
* **[!UICONTROL Experience Targeting] (XT)**: Reihenfolge der Erlebnisse in der Aktivität.
* **[!UICONTROL Multivariate Test] (MVT)** Alphabetisch nach Erlebnisname.
* **[!UICONTROL Recommendations]**: Reihenfolge der Erlebniserstellung in absteigender Reihenfolge.

Beachten Sie beim Arbeiten mit den [!UICONTROL Counting Methodology] die folgenden Einschränkungen:

* Bei [[!UICONTROL Auto-Target] Aktivitäten ](/help/main/c-activities/auto-target/auto-target-to-optimize.md) es keine Option zur Auswahl von „Besuchern“ als Zählmethodik. [!UICONTROL Auto-Target] ist der einzige Aktivitätstyp, den Sie nicht nach Besuchern grafisch darstellen können.
* Bei Aktivitäten, die [Analytics als Berichtsquelle (A4T) verwenden](/help/main/c-integrating-target-with-mac/a4t/a4t.md) können Sie Besucher, Besuche oder Impressionen nicht kumulativ darstellen.

## Arbeiten mit Diagrammen, die mehr als 16 Erlebnisse in der Aktivität haben

Wenn eine Aktivität weniger als 16 Erlebnisse umfasst, wird jedes Erlebnis im Diagramm mit einer anderen Farbe gezeichnet.

Hat eine Aktivität mehr als 16 Erlebnisse, werden die farbigen Linien für die ersten 16 Erlebnisse im Diagramm angezeigt. Die restlichen Erlebnisse werden im Bereich „Erlebnisse“ auf der linken Seite ausgegraut, und im Diagramm werden keine entsprechenden Darstellungslinien angezeigt. Es können jeweils nur die Linien für 16 Erlebnisse angezeigt werden.

Wenn Sie die Maus über eines der ausgegrauten Erlebnisse bewegen, wird im Diagramm vorübergehend eine neue graue Darstellungslinie angezeigt, die dem jeweiligen Erlebnis entspricht. Wenn Sie die Darstellungslinie eines ausgegrauten Erlebnisses in einer Farbe anzeigen möchten, können Sie ein farbig angezeigtes Erlebnis deaktivieren, indem Sie zunächst auf den zugehörigen Namen klicken und dann das gewünschte ausgegraute Erlebnis auswählen, indem Sie auf den zugehörigen Namen klicken.

In dem Diagramm werden die Linien für die ersten 16 Erlebnisse angezeigt (es liegen einige Überschneidungen vor, daher sind scheinbar weniger als 16 Linien vorhanden). Der farbige Punkt im Bereich „Erlebnisse“ auf der linken Seite neben den einzelnen Erlebnisnamen gibt an, dass die Darstellungslinie des Erlebnisses in der entsprechenden Farbe angezeigt wird.

Wenn Sie im Bereich „Erlebnisse“ einen Bildlauf nach unten durchführen, werden Sie feststellen, dass die Namen für das 17. bis 26. Erlebnis ausgegraut sind, wie in der folgenden Abbildung dargestellt:

Wenn Sie die Maus über eines der ausgegrauten Erlebnisse bewegen, wird im Diagramm vorübergehend eine neue graue Darstellungslinie angezeigt, die dem jeweiligen Erlebnis entspricht.

Angenommen, Sie möchten die Darstellungslinie für Erlebnis R anzeigen, während die Line für Erlebnis P nicht angezeigt werden soll. Sie können auf den Namen von Erlebnis P klicken, um dessen Auswahl aufzuheben, und Sie können dann auf den Namen von Erlebnis R klicken, um es auszuwählen, wie unten dargestellt:
