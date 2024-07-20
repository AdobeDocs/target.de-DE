---
keywords: Empfehlungen; Einstellungen; Name; Ziel; Priorität; Dauer; Berichterstellungseinstellungen; andere Metadaten
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, mit denen eine Recommendations-Aktivität in Adobe Target beschrieben und gesteuert wird.
title: Wie konfiguriere ich Recommendations-Aktivitätseinstellungen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 48%

---

# Einstellungen für Recommendations-Aktivitäten

Informationen zu den Einstellungen, mit denen Sie eine [!UICONTROL Recommendations] -Aktivität in [!DNL Adobe Target] beschreiben und steuern können.

![Seite „Recommendations-Ziele und -Einstellungen“](/help/main/c-recommendations/t-create-recs-activity/assets/recs-settings.png)

In den folgenden Abschnitten werden die verfügbaren Einstellungen für eine [!UICONTROL Recommendations] -Aktivität beschrieben.

## Name

Geben Sie einen beschreibenden Namen an, der Ihnen und Ihrem Team dabei hilft, die Aktivität zu identifizieren.

Folgende Zeichen sind im Aktivitätsnamen nicht zulässig:

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

Wenn Sie den Aktivitätsnamen [!UICONTROL Recommendations] angeben, der bereits für eine andere Aktivität in [!UICONTROL Recommendations Classic] vorhanden ist, wird die neue Aktivität mit einem neuen Namen erneut synchronisiert. Der neue Name ist der ursprüngliche Name, der mit einem Zeitstempel versehen wird, um ihn eindeutig zu machen. Dieser neue Name wird sowohl in [!DNL Target Standard/Premium] als auch in [!UICONTROL Recommendations Classic] angezeigt.

## Ziel

(Optional) Beschreiben Sie das Ziel der Aktivität.

## Priorität

Stellen Sie mit dem Schieberegler die Prioritätsstufe ein.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

## Dauer

Legen Sie die Dauer der Aktivität fest.

Die Aktivität kann bei Aktivierung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## Berichterstellungseinstellungen 

* **Source-Berichterstellung:** Geben Sie an, aus welchen Lösungsdaten erfasst werden:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  Wenn in Ihren [Kontoeinstellungen](/help/main/administrating-target/reporting.md) eine Berichterstellungslösung angegeben ist, wird die angegebene Lösung verwendet und diese Einstellung ist nicht sichtbar.

  Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten.

  **[!DNL Adobe Analytics]**: Siehe [[!DNL Adobe Analytics]  als Berichtsquelle für  [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) , um mehr über die Unterschiede zwischen den Berichterstellungslösungen und deren Vorteile zu erfahren.

  Wenn Sie [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) auswählen, wählen Sie eine [!DNL Analytics] Report Suite aus, die [!DNL Target] Aktivitätsdaten erhält. Wählen Sie dazu zunächst ein [!DNL Analytics] Unternehmen aus, an das Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Target] bereitgestellt wurden. Wenn die erwartete Report Suite nicht angezeigt wird, versuchen Sie zunächst, sich abzumelden und sich wieder bei [!DNL Adobe Experience Cloud] anzumelden, um es erneut zu versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  Für [!DNL Analytics for Target] (A4T) ist ein Tracking-Server erforderlich, um Ergebnisse korrekt zu melden. Im Feld [!UICONTROL Tracking Server] wird ein standardmäßiger Trackingserver angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie in dieses Feld den richtigen Tracking-Server einschließen. Weitere Informationen finden Sie unter [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) .

  **[!DNL Adobe Customer Journey Analytics]**: Weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target] finden Sie unter [[!DNL Target] Berichterstellung in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) .

* **Zielmetrik:** Wählen Sie die Erfolgsmetrik aus, die festlegt, ob eine Aktivität erfolgreich ist.
* **Zusätzliche Metriken:** Konfigurieren Sie weitere Erfolgsmetriken zur Verwendung in Ihren Berichten.
* **Zielgruppen für Berichterstellung:** Definieren Sie Zielgruppen, die beim Filtern Ihrer Berichte verwendet werden können.

## Sonstige Metadaten

Geben Sie Anmerkungen zu Ihrer Aktivität ein.

## Schulungsvideo: Aktivitätseinstellungen (3:02) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
