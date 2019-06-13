---
description: Erlebnis-URLs können für Aktivitäten zur automatisierten Personalisierung in Target generiert werden, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität für Vorschau und QA livegeschaltet wird. Erlebnis-URLs umgehen Targeting, um die Ansicht eines bestimmten Erlebnisses zu erzwingen.
keywords: Erlebnisvorschau;Erlebnis-URLs;URLs generieren;Erlebnis-URLs anzeigen
seo-description: Erlebnis-URLs können für Aktivitäten zur automatisierten Personalisierung in Target generiert werden, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität für Vorschau und QA livegeschaltet wird. Erlebnis-URLs umgehen Targeting, um die Ansicht eines bestimmten Erlebnisses zu erzwingen.
seo-title: Weitergeben von Erlebnis-URLs zur Automated Personalization-Vorschau außerhalb von Target
solution: Target
title: Weitergeben von Erlebnis-URLs zur Automated Personalization-Vorschau außerhalb von Target
title-outputclass: Premium
topic: Standard
uuid: 2ef07b6c-086d-43ac-bf02-efe217652a3a
badge: Premium
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Weitergeben von Erlebnis-URLs zur Automated Personalization-Vorschau außerhalb von Target{#share-experience-urls-to-preview-automated-personalization-outside-of-target}

Erlebnis-URLs können für Aktivitäten zur automatisierten Personalisierung in Target generiert werden, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität für Vorschau und QA livegeschaltet wird. Erlebnis-URLs umgehen Targeting, um die Ansicht eines bestimmten Erlebnisses zu erzwingen.

>[!NOTE]
>
>Im Aktivitäts-QA-Modus können Sie Aktivitäts-URLs für andere Aktivitätstypen erstellen. Weitere Informationen finden Sie unter [Activitäts-QA](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40)

.

Möchten Sie Erlebnis-URLs verwenden, müssen Sie die mit Target generierten Links freigeben, nicht die endgültige URL, auf die Sie bei Ansicht des Erlebnisses umgeleitet werden. Ändert sich der Inhalt, müssen auch neue URLs generiert werden. Sollten Sie neue URLs generieren, funktionieren ältere URLs möglicherweise nicht mehr.

Verwenden Sie Erlebnis-URLs, um Erlebnisse für Team-Mitglieder freizugeben und Erlebnisse für verschiedene Browser und Umgebungen zu prüfen, ohne hierfür eine eigene QS-Aktivität erstellen zu müssen. Diese Funktion ist besonders nützlich, wenn eine Site komplex ist oder Ihre Sicherheitsrichtlinien das Anzeigen der Site in einem Simulator nicht zulassen.

1. Erstellen Sie eine [automatisierte Personalisierungsaktivität](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder klicken Sie auf die Aktivität, um sie zu öffnen.

   Diese Aktivität muss nicht live sein, um eine Vorschau eines Erlebnisses anzeigen zu können.
1. Klicken Sie auf der Aktivitätsübersichtsseite auf die drei vertikalen Punkte und dann auf **[!UICONTROL Erlebnis-URLs anzeigen]**.
1. Überprüfen bzw. geben Sie Ihre URLs an.

   * Wenn Sie Visual Experience Composer verwenden, wird die von Ihnen für die Aktivität angegebene Standard-URL automatisch geöffnet. Zudem wird ein Link für jedes einzelne Erlebnis in Ihrer Aktivität generiert. Sie können diese URL nach Wunsch ändern oder weitere hinzufügen.
   * Sollten Sie mit dem Form-Based Experience Composer arbeiten, wird keine Standard-URL angezeigt. Klicken Sie auf **Neue URL hinzufügen**, sofern Sie zuvor nicht bereits Erlebnis-URLs erstellt haben. Sie müssen alle URLs, für die Sie eine Vorschau anzeigen möchten, sowie einen Namen für jede URL angeben.
   Sie können mehrere URLs angeben, was besonders bei mehrseitigen Tests oder Vorlagentests nützlich ist, wenn Sie eine Vorschau der Aktivität auf mehr als einer Seite anzeigen möchten.

   In einem modalen Fenster werden Links zu den Erlebnissen auf Ihrer Site angezeigt, um eine „echte Vorschau“ der Erlebnisse außerhalb des Visual Experience Composer von Target zu erhalten. Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Anklicken des Links und das Kopieren der resultierenden URL auf der Seite funktionieren nicht, weil die URL einen Parameter enthält, der die Seite nur dann korrekt anzeigt, wenn Sie vom Link in der Nachricht aus auf die Seite zugreifen. Kopieren Sie stattdessen den Text im modalen Fenster und senden Sie den ganzen Text per E-Mail an Ihr Team.
1. Klicken Sie auf **[!UICONTROL Alle erzeugen]** und klicken Sie auf jedes Erlebnis, dessen Vorschau Sie anzeigen möchten.

   Wenn Sie anschließend Änderungen an den Erlebnissen vornehmen, stellen Sie sicher, dass Sie neue Vorschaulinks für Ihr Team generieren, indem Sie zum modalen Fenster zurückkehren und auf **Alle erzeugen** klicken, um neue Links zu erhalten.

   **Hinweis:** Die Vorschau-Links werden in neuen Registerkarten geöffnet; dafür muss der Pop-up-Blocker in Ihrem Browser deaktiviert sein.

1. Klicken Sie auf den jeweiligen Erlebnisnamen, um eine Vorschau der Aktivität anzuzeigen.

   Die Seite mit der Aktivität wird geöffnet.
1. Klicken Sie auf **[!UICONTROL Fertig]**, um zur Aktivitätsübersicht zurückzukehren.

## Zu beachten {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Erstellen von Erlebnis-URLs**

* Die Erlebnis-URL wird nicht durch die Traffic-Aufteilung zwischen den Erlebnissen beeinflusst.
* Die Ausrichtung auf die Zielgruppe wirkt sich nicht auf die Vorschau aus.
* Sie können höchstens 300 Erlebnis-URLs pro Aktivität automatisch generieren. Darüber hinaus müssen Sie die URLs manuell generieren.
* Sie können höchstens 300 Erlebnis-URLs pro Aktivität automatisch generieren. Darüber hinaus müssen Sie die URLs manuell generieren.
* Je nach Anzahl der Erlebnisse kann die Generierung von URLs bis zu fünf Minuten dauern. Schließen Sie nicht den Dialog, sonst gehen die generierten URLs verloren.
* Die generierten Vorschaulinks sind zwei Monate lang gültig. Danach müssen Sie Ihre Vorschau-URLs neu generieren.
* Sie müssen bei jeder Änderung eines Erlebnisses neu generieren.

**Freigeben von Erlebnis-URLs**

* Sie können ein Erlebnis auch dann zur Vorschau anzeigen, wenn Sie nicht zur Targeting-Zielgruppe gehören.
* Sie können Erlebnis-URLs für Kollegen freigeben, die nicht auf Adobe Target zugreifen können.

**Vorschau der Erlebnisse mit Erlebnis-URLs**

* Die Vorschau funktioniert für alle gespeicherten Aktivitäten, solange die Seite nicht verändert wird.
* Die Erlebnis-URL ist verfügbar, unabhängig davon, ob die Aktivität aktiv oder inaktiv ist.
* Für ein Erlebnis mit Entwurf-Status kann keine Vorschau angezeigt werden.
* Die Vorschau von Erlebnis-URLs wirkt sich nicht auf die Berichterstellung aus.

**Fehlerbehebung für Erlebnis-URLs**

* Wenn Sie die Vorschau nicht auf der neuen Registerkarte anzeigen können (aufgrund des Browser-Caches), aktualisieren Sie die Seite zwei- oder dreimal oder kopieren Sie den Link und öffnen Sie ihn in einem neuen Browser, einer neuen Sitzung oder in einem privaten Surfmodus.
* Unabhängig davon, ob Sie Ihre eigene QS für die Aktivität durchführen oder Links an ein anderes Team weiterleiten - Sie können mühelos eine Vorschau für bestimmte Erlebnisse anzeigen, ohne separate Tests einrichten zu müssen.

