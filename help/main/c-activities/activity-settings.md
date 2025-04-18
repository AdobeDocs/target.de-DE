---
keywords: Ziel und Einstellungen;Ziel;Priorität;Dauer
description: Erfahren Sie, wie Sie die Aktivitätseinstellungen in Adobe [!DNL Target]  verwenden, um Ziel, Priorität und Dauer Ihrer Aktivitäten zu verwalten.
title: Wie gebe ich Aktivitätseinstellungen an?
feature: Activities
exl-id: 7f34080b-d2ed-4fe5-80ff-3aba16961223
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 74%

---

# Aktivitätseinstellungen

Verwenden Sie [!UICONTROL Activity Settings] in [!DNL Adobe Target], um das Ziel, die Priorität und die Dauer Ihrer Aktivitäten zu verwalten.

1. Geben Sie Hinweise zum Ziel der Aktivität ein.

   Geben Sie sämtliche Informationen ein, die für Sie und Ihre Team-Mitglieder von Nutzen sind. Ziehen Sie, um die Größe des [!UICONTROL Objective] zu ändern.
1. Legen Sie die Priorität der Aktivität fest.

   Je nach Ihren Einstellungen variieren die Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

   Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

   Wenn diese Option in [!UICONTROL Administration] > [!UICONTROL Reporting] (Standard) nicht aktiviert ist, geben Sie eine Priorität an: Niedrig, Medium oder Hoch.

   Um die feinabgestimmten Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und schalten Sie die Option [!UICONTROL Enable Fine-Grained Priorities] auf „Ein“.

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

Die Seite [!UICONTROL Goal & Settings] enthält zusätzliche Einstellungen, die je nach dem Typ der von Ihnen erstellten Aktivität variieren. Weitere Informationen zu diesen Einstellungen erhalten Sie in den Abschnitten zum jeweiligen Aktivitätstyp:

* [A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)
* [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Recommendations](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

## Schulungsvideo: Aktivitätseinstellungen ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video erhalten Sie Informationen zu Aktivitätseinstellungen.

* Eingeben eines Ziels für Ihre Aktivität
* Festlegen der Priorität Ihrer Aktivitäten
* Planen von Start- und Endzeitpunkt der Aktivität
* Hinzufügen von Zielgruppen für Berichterstellung und zur Erstellung von Berichtsfiltern
* Eingeben von Notizen zu Aktivitäten

  >[!VIDEO](https://video.tv.adobe.com/v/17381)
