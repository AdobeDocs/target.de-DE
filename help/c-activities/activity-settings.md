---
keywords: Ziel und Einstellungen;Ziel;Priorität;Dauer
description: Erfahren Sie, wie Sie mit den Einstellungen für die Aktivität in Adobe Target das Ziel, die Priorität und die Dauer Ihrer Aktivitäten verwalten.
title: Wie gebe ich Einstellungen für die Aktivität an?
feature: Activities
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 80%

---


# Aktivitätseinstellungen

Verwenden Sie [!UICONTROL Aktivitäten-Einstellungen] in [!DNL Adobe Target], um das Ziel, die Priorität und die Dauer Ihrer Aktivitäten zu verwalten.

1. Geben Sie Hinweise zum Ziel der Aktivität ein.

   Geben Sie sämtliche Informationen ein, die für Sie und Ihre Team-Mitglieder von Nutzen sind. Ziehen Sie das Feld [!UICONTROL Ziel], um seine Größe zu ändern.
1. Legen Sie die Priorität der Aktivität fest.

   Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für [!UICONTROL Prioritäten]. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

   Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

   Wenn diese Option in [!UICONTROL Administration] > [!UICONTROL Berichte] (Standard) nicht aktiviert ist, geben Sie eine Priorität an: Niedrig, mittel oder hoch.

   Klicken Sie zum Aktivieren der Feinabstufungen auf [!UICONTROL Administration] > [!UICONTROL Berichte] und schalten Sie dann die Option [!UICONTROL Feinkörnige Prioritäten aktivieren] auf die Position &quot;Ein&quot;.

   Ist diese Option aktiviert, legen Sie einen Wert zwischen 0 und 999 fest:

   * 0 = Niedrig
   * 999 = Hoch

   Bei Aktivitäten, die in älteren Versionen von [!DNL Target Standard/Premium] erstellt wurden, wird eine niedrige Priorität in den Wert 0, eine mittlere in den Wert 5 und eine hohe in den Wert 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.

   >[!NOTE]
   >
   >Wenn Sie genauer unterteilte Prioritäten verwendet haben und die Option deaktivieren möchten, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden.

1. Legen Sie die Dauer der Aktivität fest.

   Sie können die Aktivität manuell aktivieren oder deaktivieren oder ein Datum und eine Uhrzeit festlegen, zu denen die Aktivität automatisch bereitgestellt werden soll. Das Zeitsteuerelement verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone wird auf die in Ihrem Browser konfigurierte Zeitzone eingestellt. Wenn Sie eine andere Zeitzone verwenden möchten, stellen Sie in Ihrem Browser eine andere Zeitzone ein und starten Sie ihn neu.

   >[!NOTE]
   >
   >Beim Planen einer Aktivität wird der Bereitstellungszeitrahmen der Aktivität festgelegt. Die Aktivität muss jedoch zudem eigens aktiviert werden, bevor sie in Einklang mit dem festgelegten Zeitplan bereitgestellt wird.

Auf der Seite [!UICONTROL „Ziele und Einstellungen“] befinden sich zusätzliche Einstellungen, die abhängig davon variieren, welchen Aktivitätstyp Sie erstellen. Weitere Informationen zu diesen Einstellungen erhalten Sie in den Abschnitten zum jeweiligen Aktivitätstyp:

* [A/B-Test](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)
* [Erlebnis-Targeting](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Multivarianz-Test](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Recommendations](/help/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

## Schulungsvideo: Aktivitätseinstellungen  ![Tutorialzeichen](/help/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

   >[!VIDEO](https://video.tv.adobe.com/v/17381)
