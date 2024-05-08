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

Informationen zu den Einstellungen, die Sie zum Beschreiben und Steuern einer [!UICONTROL Recommendations] Aktivität in [!DNL Adobe Target].

![Seite „Recommendations-Ziele und -Einstellungen“](/help/main/c-recommendations/t-create-recs-activity/assets/recs-settings.png)

In den folgenden Abschnitten werden die verfügbaren Einstellungen für eine [!UICONTROL Recommendations] -Aktivität.

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

Wenn Sie eine [!UICONTROL Recommendations] Aktivitätsname, der bereits für eine andere Aktivität in [!UICONTROL Recommendations Classic], wird die neue Aktivität mit einem neuen Namen erneut synchronisiert. Der neue Name ist der ursprüngliche Name, der mit einem Zeitstempel versehen wird, um ihn eindeutig zu machen. Dieser neue Name wird sowohl in [!DNL Target Standard/Premium] als auch in [!UICONTROL Recommendations Classic] angezeigt.

## Ziel

(Optional) Beschreiben Sie das Ziel der Aktivität.

## Priorität

Stellen Sie mit dem Schieberegler die Prioritätsstufe ein.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

## Dauer

Legen Sie die Dauer der Aktivität fest.

Die Aktivität kann bei Aktivierung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## Berichterstellungseinstellungen 

* **Berichtsquelle:** Geben Sie an, aus welchen Lösungsdaten erfasst werden:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  Wenn eine Berichterstellungslösung in Ihrer [Kontoeinstellungen](/help/main/administrating-target/reporting.md)festgelegt ist, wird die angegebene Lösung verwendet und diese Einstellung ist nicht sichtbar.

  Sie können Ihre Berichtsquelle nach Liveschaltung einer Aktivität nicht mehr ändern, um die Berichte konsistent zu halten.

  **[!DNL Adobe Analytics]**: Siehe [[!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) , um mehr über die Unterschiede zwischen den Berichterstellungslösungen und deren Vorteile zu erfahren.

  Bei Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T), wählen Sie eine [!DNL Analytics] Report Suite, die empfangen wird [!DNL Target] Aktivitätsdaten. Wählen Sie dazu zunächst einen der [!DNL Analytics] Unternehmen, an die Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Nur Report Suites, für die eine Verbindung hergestellt wurde [!DNL Target] stehen zur Auswahl zur Verfügung. Wenn die erwartete Report Suite nicht angezeigt wird, melden Sie sich zunächst ab und dann wieder bei der [!DNL Adobe Experience Cloud] erneut versuchen. Wenn die Report Suite weiterhin in der Liste fehlt, wenden Sie sich an [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T) erfordert einen Tracking-Server, um die Ergebnisse korrekt zu melden. Ein standardmäßiger Trackingserver wird im [!UICONTROL Tracking Server] -Feld. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie in dieses Feld den richtigen Tracking-Server einschließen. Siehe [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) für weitere Informationen.

  **[!DNL Adobe Customer Journey Analytics]**: Siehe [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) Weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target].

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
