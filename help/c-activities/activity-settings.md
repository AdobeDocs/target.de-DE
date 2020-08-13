---
keywords: Goal &Settings;objective;priority;duration
description: Verwenden Sie zum Verwalten des Ziels, der Priorität und der Dauer Ihrer Aktivitäten die „Aktivitätseinstellungen“.
title: Aktivitätseinstellungen
feature: activities
subtopic: Multivariate Test
topic: Standard
uuid: d317e63a-ba1f-4c0e-ab90-c6181b8b45fd
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 90%

---


# Aktivitätseinstellungen{#activity-settings}

Verwenden Sie zum Verwalten des Ziels, der Priorität und der Dauer Ihrer Aktivitäten die „Aktivitätseinstellungen“.

1. Geben Sie Hinweise zum Ziel der Aktivität ein.

   Geben Sie sämtliche Informationen ein, die für Sie und Ihre Team-Mitglieder von Nutzen sind. Ziehen Sie das Feld [!UICONTROL Ziel], um seine Größe zu ändern.
1. Legen Sie die Priorität der Aktivität fest.

   Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für [!UICONTROL Prioritäten]. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

   Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

   If this option is not enabled in [!UICONTROL Administration] > [!UICONTROL Reporting] (the default), specify a priority: Low, Medium, or High.

   To enable fine-grained priorities, click [!UICONTROL Administration] > [!UICONTROL Reporting], then toggle the [!UICONTROL Enable Fine-Grained Priorities] option to the &quot;On&quot; position.

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

* [A/B-Test](../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Automatisierte Personalisierung](../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)
* [Erlebnis-Targeting](../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Multivarianz-Test](../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Recommendations](../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

## Schulungsvideo: Aktivitätseinstellungen ![Tutorialzeichen](/help/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

   >[!VIDEO](https://video.tv.adobe.com/v/17381)
