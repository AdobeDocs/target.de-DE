---
keywords: experience preview;experience urls;generate urls;view experience urls
description: Erlebnis-Vorschauen-URLs können für die Zielgruppe von Automated Personalization-Aktivitäten generiert werden, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität zu Vorschauen- und Qualitätszwecken live geschaltet wird. Erlebnis-Vorschauen-URLs umgehen Targeting, um die Anzeige eines bestimmten Erlebnisses zu erzwingen.
title: Vorschau von Automated Personalization-Aktivitäten mit Erlebnis-Vorschauen-URLs
feature: ap
topic: Standard
uuid: 2ef07b6c-086d-43ac-bf02-efe217652a3a
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 64%

---


# ![PREMIUM](/help/assets/premium.png) Vorschau Automated Personalization-Aktivitäten mit Erlebnis-Vorschauen-URLs{#share-experience-urls-to-preview-automated-personalization-outside-of-target}

Erlebnis-Vorschauen-URLs können für die Zielgruppe von Automated Personalization-Aktivitäten generiert werden, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität zu Vorschauen- und Qualitätszwecken live geschaltet wird. Erlebnis-Vorschauen-URLs umgehen Targeting, um die Anzeige eines bestimmten Erlebnisses zu erzwingen.

>[!NOTE]
>
>Erlebnis-Vorschauen-URLs für Automated Personalization unterscheiden sich vom Qualitätssicherungs-Modus für Aktivitäten. Im Aktivitäts-QA-Modus können Sie Aktivitäts-URLs für andere Aktivitätstypen erstellen. Weitere Informationen finden Sie unter [Activitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md).
>
>Erlebnis-Vorschauen-URLs für AP-Aktivitäten sind nur verfügbar, wenn at.js 1.x verwendet wird. Erlebnis-Vorschauen-URLs für AP-Aktivitäten werden derzeit für &quot;at.js 2.x&quot;nicht unterstützt.

Verwenden Sie Erlebnis-Vorschauen-URLs, um Erlebnisse mit Teammitgliedern auszutauschen und Erlebnisse über Browser und Umgebung hinweg zu prüfen, ohne eine separate QS-Aktivität zu erstellen. Diese Funktion ist besonders nützlich, wenn eine Site komplex ist oder Ihre Sicherheitsrichtlinien das Anzeigen der Site in einem Simulator nicht zulassen.

1. Erstellen Sie eine [automatisierte Personalisierungsaktivität](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder klicken Sie auf die Aktivität, um sie zu öffnen.

   Diese Aktivität muss nicht live sein, um eine Vorschau eines Erlebnisses anzeigen zu können.
1. Klicken Sie auf der Aktivitätsübersichtsseite auf die drei vertikalen Punkte und dann auf **[!UICONTROL Erlebnis-URLs anzeigen]**.
1. Überprüfen bzw. geben Sie Ihre URLs an.

   * Wenn Sie Visual Experience Composer verwenden, wird die von Ihnen für die Aktivität angegebene Standard-URL automatisch geöffnet. Zudem wird ein Link für jedes einzelne Erlebnis in Ihrer Aktivität generiert. Sie können diese URL nach Wunsch ändern oder weitere hinzufügen.
   * Sollten Sie mit dem Form-Based Experience Composer arbeiten, wird keine Standard-URL angezeigt. If you haven&#39;t previously created experience preview URLs, click **Add New URL**. Sie müssen alle URLs, für die Sie eine Vorschau anzeigen möchten, sowie einen Namen für jede URL angeben.

   Sie können mehrere URLs angeben, was besonders bei mehrseitigen Tests oder Vorlagentests nützlich ist, wenn Sie eine Vorschau der Aktivität auf mehr als einer Seite anzeigen möchten.

   In einem modalen Fenster werden Links zu den Erlebnissen auf Ihrer Site angezeigt, um eine „echte Vorschau“ der Erlebnisse außerhalb des Visual Experience Composer von Target zu erhalten. Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Anklicken des Links und das Kopieren der resultierenden URL auf der Seite funktionieren nicht, weil die URL einen Parameter enthält, der die Seite nur dann korrekt anzeigt, wenn Sie vom Link in der Nachricht aus auf die Seite zugreifen. Kopieren Sie stattdessen den Text im modalen Fenster und senden Sie den ganzen Text per E-Mail an Ihr Team.
1. Klicken Sie auf **[!UICONTROL Alle erzeugen]** und klicken Sie auf jedes Erlebnis, dessen Vorschau Sie anzeigen möchten.

   If you then make changes to the experience, make sure to generate new preview links for your team by returning to the modal window and clicking **Renew Links** to get new links.

   **Hinweis:** Die Vorschau-Links werden in neuen Registerkarten geöffnet; dafür muss der Pop-up-Blocker in Ihrem Browser deaktiviert sein.

1. Klicken Sie auf den jeweiligen Erlebnisnamen, um eine Vorschau der Aktivität anzuzeigen.

   Die Seite mit der Aktivität wird geöffnet.
1. Klicken Sie auf **[!UICONTROL Fertig]**, um zur Aktivitätsübersicht zurückzukehren.

## Zu beachten {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Generieren von Experience Vorschau-URLs**

* Die Erlebnis-Vorschauen-URL wird nicht durch die Traffic-Aufteilung zwischen Erlebnissen beeinflusst.
* Die Ausrichtung auf die Zielgruppe wirkt sich nicht auf die Vorschau aus.
* Sie können höchstens 300 Erlebnis-URLs pro Aktivität automatisch generieren. Darüber hinaus müssen Sie die URLs manuell generieren.
* Sie können höchstens 300 Erlebnis-URLs pro Aktivität automatisch generieren. Darüber hinaus müssen Sie die URLs manuell generieren.
* Je nach Anzahl der Erlebnisse kann die Generierung von URLs bis zu fünf Minuten dauern. Schließen Sie nicht den Dialog, sonst gehen die generierten URLs verloren.
* Die generierten Vorschaulinks sind zwei Monate lang gültig. Danach müssen Sie Ihre Vorschau-URLs neu generieren.
* Sie müssen bei jeder Änderung eines Erlebnisses neu generieren.

**Freigeben von Experience Vorschau-URLs**

* Sie können ein Erlebnis auch dann zur Vorschau anzeigen, wenn Sie nicht zur Targeting-Zielgruppe gehören.
* Sie können Erlebnis-URLs für Kollegen freigeben, die keinen Zugriff auf Adobe Target haben.

**Anzeigen von Erlebnissen mit Experience Vorschau-URLs**

* Die Vorschau funktioniert für alle gespeicherten Aktivitäten, solange die Seite nicht verändert wird.
* Die Erlebnis-Vorschauen-URL steht unabhängig davon zur Verfügung, ob die Aktivität aktiv oder inaktiv ist.
* Ein Erlebnis, das sich im Entwurfsstatus befindet, kann nicht Vorschau werden.
* Berichte wird nicht durch die Anzeige von Erlebnis-Vorschauen-URLs beeinträchtigt.

**Fehlerbehebung für Experience Vorschau-URLs**

* Wenn Sie die Vorschau nicht auf der neuen Registerkarte anzeigen können (aufgrund des Browser-Caches), aktualisieren Sie die Seite zwei- oder dreimal oder kopieren Sie den Link und öffnen Sie ihn in einem neuen Browser, einer neuen Sitzung oder in einem privaten Surfmodus.
