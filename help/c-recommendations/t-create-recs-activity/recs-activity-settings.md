---
keywords: Recommendations;Settings;name;objective;priority;duration;reporting settings;other metadata
description: Es können verschiedene Einstellungen verwendet werden, um eine Recommendations-Aktivität in Adobe Target zu beschreiben und zu steuern.
title: Einstellungen für Recommendations-Aktivitäten in Adobe Target
feature: null
subtopic: Recommendations
uuid: 7c66d0e8-cecf-4d0d-8c62-5347a7d80a53
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 98%

---


# ![PREMIUM](/help/assets/premium.png) Recommendations Activities-Einstellungen{#recommendations-activity-settings}

Informationen über die Einstellungen, mit denen Sie eine [!UICONTROL Recommendations]-Aktivität beschreiben und steuern können.

![Seite „Recommendations-Ziele und -Einstellungen“](/help/c-recommendations/t-create-recs-activity/assets/recs-settings.png)

Die folgenden Abschnitte beschreiben die verfügbaren Einstellungen für eine [!UICONTROL Recommendations]-Aktivität.

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

Wenn Sie den Namen einer [!UICONTROL Recommendations]-Aktivität angeben, der bereits für eine andere Aktivität in [!UICONTROL Recommendations Classic] existiert, wird die neue Aktivität mit einem neuen Namen erneut synchronisiert. Der neue Name ist der ursprüngliche Name, der mit einem Zeitstempel versehen wird, um ihn eindeutig zu machen. Dieser neue Name wird sowohl in Target Standard/Premium als auch in [!UICONTROL Recommendations Classic] angezeigt.

## Ziel

(Optional) Beschreiben Sie das Ziel der Aktivität.

## Priorität

Stellen Sie mit dem Schieberegler die Prioritätsstufe ein.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

## Dauer

Legen Sie die Dauer der Aktivität fest.

Die Aktivität kann bei Aktivierung starten, oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit festlegen. Ebenso kann die Aktivität bei Deaktivierung oder zu einem festgelegten Datum und einer festgelegten Uhrzeit enden. Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

## Berichterstellungseinstellungen 

* **Berichtsquelle:** Wählen Sie die Berichtsquelle aus: Adobe Target oder [Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md). Ändern Sie die Berichtsquelle nicht mehr, nachdem die Aktivität aktiviert wurde. Eine Änderung der Berichtsquelle nach der Aktivierung einer Aktivität führt zu inkonsistenten Berichten.
* **Zielmetrik:** Wählen Sie die Erfolgsmetrik aus, die festlegt, ob eine Aktivität erfolgreich ist.
* **Zusätzliche Metriken:** Konfigurieren Sie weitere Erfolgsmetriken zur Verwendung in Ihren Berichten.
* **Zielgruppen für Berichterstellung:** Definieren Sie Zielgruppen, die beim Filtern Ihrer Berichte verwendet werden können.

## Sonstige Metadaten

Geben Sie Anmerkungen zu Ihrer Aktivität ein.

## Schulungsvideo: Aktivität Settings (3:02) ![Tutorial-Abzeichen](/help/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/17381)