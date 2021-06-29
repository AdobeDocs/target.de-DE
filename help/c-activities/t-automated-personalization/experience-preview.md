---
keywords: Erlebnisvorschau;Erlebnis-URLs;URLs generieren;Erlebnis-URLs anzeigen
description: Erfahren Sie, wie Sie Erlebnisvorschau-URLs für Adobe [!DNL Target] Automated Personalization-Aktivitäten verwenden, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität live ist.
title: Wie kann ich URLs für die Erlebnisvorschau in Automated Personalization-Aktivitäten verwenden?
feature: Automated Personalization
exl-id: 9f329b8a-5f86-4cae-a3be-eed24fa0a9cd
source-git-commit: 0d24bcf335980291891e3198a13ec283d1dd325f
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 50%

---

# ![](/help/assets/premium.png) PREMIUMPreview Automated Personalization activities with experience preview URLs

Sie können Erlebnisvorschau-URLs für [!DNL Target] [!UICONTROL Automated Personalization]-Aktivitäten generieren, um Erlebnisinhalte direkt auf Ihrer Site anzuzeigen, bevor die Aktivität für Vorschau- und QA-Zwecke live ist. URLs für die Erlebnisvorschau umgehen das Targeting, um die Anzeige eines bestimmten Erlebnisses zu erzwingen.

>[!NOTE]
>
>Sie können Erlebnisvorschau-URLs für andere Typen von [!DNL Target] -Aktivitäten erstellen. Der Prozess unterscheidet sich jedoch geringfügig. Weitere Informationen finden Sie unter [Activitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md#preview).

Verwenden Sie Erlebnisvorschau-URLs, um Erlebnisse für Team-Mitglieder freizugeben und Erlebnisse über Browser und Umgebungen hinweg zu überprüfen, ohne eine separate QA-Aktivität zu erstellen. Diese Funktion ist besonders nützlich, wenn eine Site komplex ist oder Ihre Sicherheitsrichtlinien das Anzeigen der Site in einem Simulator nicht zulassen.

1. Erstellen Sie eine [automatisierte Personalisierungsaktivität](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oder klicken Sie auf die Aktivität, um sie zu öffnen.

   Diese Aktivität muss nicht live sein, um eine Vorschau eines Erlebnisses anzeigen zu können.

1. Klicken Sie auf der Aktivitätsübersichtsseite auf die drei vertikalen Punkte und klicken Sie dann auf **[!UICONTROL Erlebnis-URLs anzeigen]**.

1. Überprüfen bzw. geben Sie Ihre URLs an.

   * Wenn Sie den [!UICONTROL Visual Experience Composer] (VEC) verwenden, wird automatisch die von Ihnen für die Aktivität angegebene Standard-URL eingegeben und für jedes Erlebnis in Ihrer Aktivität wird ein Link generiert. Sie können diese URL nach Wunsch ändern oder weitere hinzufügen.
   * Wenn Sie den [!UICONTROL Form-Based Experience Composer] verwenden, wird keine Standard-URL automatisch eingegeben. Wenn Sie noch keine Erlebnisvorschau-URLs erstellt haben, klicken Sie auf **Neue URL hinzufügen**. Sie müssen alle URLs, für die Sie eine Vorschau anzeigen möchten, sowie einen Namen für jede URL angeben.

   Sie können mehrere URLs angeben, was besonders bei mehrseitigen Tests oder Vorlagentests nützlich ist, wenn Sie eine Vorschau der Aktivität auf mehr als einer Seite anzeigen möchten.

   In einem modalen Fenster werden Links zu Ihren Erlebnissen auf Ihrer Site angezeigt, um eine &quot;echte Vorschau&quot;der Erlebnisse außerhalb von [!DNL Target] VEC zu erhalten. Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Anklicken des Links und das Kopieren der resultierenden URL auf der Seite funktionieren nicht, weil die URL einen Parameter enthält, der die Seite nur dann korrekt anzeigt, wenn Sie vom Link in der Nachricht aus auf die Seite zugreifen. Kopieren Sie stattdessen den Text im modalen Fenster und senden Sie den ganzen Text per E-Mail an Ihr Team.

1. Klicken Sie auf **[!UICONTROL Alle erzeugen]** und klicken Sie auf jedes Erlebnis, dessen Vorschau Sie anzeigen möchten.

   Wenn Sie dann Änderungen am Erlebnis vornehmen, stellen Sie sicher, dass Sie neue Vorschaulinks für Ihr Team generieren, indem Sie zum modalen Fenster zurückkehren und auf **Links erneuern** klicken, um neue Links zu erhalten.

   >[!NOTE]
   >
   >Vorschau-Links werden in neuen Registerkarten geöffnet und erfordern, dass der Popup-Blocker in Ihrem Browser deaktiviert ist.

1. Klicken Sie auf den jeweiligen Erlebnisnamen, um eine Vorschau der Aktivität anzuzeigen.

   Die Seite mit der Aktivität wird geöffnet.

1. Klicken Sie auf **[!UICONTROL Fertig]**, um zur Aktivitätsübersicht zurückzukehren.

## Zu beachten {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Erstellen von Erlebnisvorschau-URLs**

* Die Erlebnisvorschau-URL wird durch die Traffic-Aufteilung zwischen Erlebnissen nicht beeinflusst.
* Die Ausrichtung auf die Zielgruppe wirkt sich nicht auf die Vorschau aus.
* Sie können höchstens 300 Erlebnis-URLs pro Aktivität automatisch generieren. Darüber hinaus müssen Sie die URLs manuell generieren.
* Je nach Anzahl der Erlebnisse kann die Generierung von URLs bis zu fünf Minuten dauern. Schließen Sie das Dialogfeld nicht oder die generierten URLs gehen verloren.
* Die generierten Vorschaulinks sind zwei Monate lang gültig. Danach müssen Sie Ihre Vorschau-URLs neu generieren.
* Sie müssen bei jeder Änderung eines Erlebnisses neu generieren.

**Freigeben von Erlebnisvorschau-URLs**

* Sie können ein Erlebnis auch dann zur Vorschau anzeigen, wenn Sie nicht zur Targeting-Zielgruppe gehören.
* Sie können Erlebnisvorschau-URLs für Kollegen freigeben, die keinen Zugriff auf [!DNL Adobe Target] haben.

**Anzeigen von Erlebnissen mit Erlebnisvorschau-URLs**

* Die Vorschau funktioniert für alle gespeicherten Aktivitäten, solange die Seite nicht verändert wird.
* Die Erlebnisvorschau-URL ist unabhängig davon verfügbar, ob die Aktivität aktiv oder inaktiv ist.
* Sie können keine Vorschau eines Erlebnisses anzeigen, das sich im Status [!UICONTROL Entwurf] befindet.
* Die Anzeige der Vorschau-URLs für Erlebnisse wirkt sich nicht auf die Berichterstellung aus.

**Fehlerbehebung für Erlebnisvorschau-URLs**

* Wenn Sie die Vorschau nicht auf der neuen Registerkarte anzeigen können (aufgrund des Browser-Caches), aktualisieren Sie die Seite zwei- oder dreimal oder kopieren Sie den Link und öffnen Sie ihn in einem neuen Browser, einer neuen Sitzung oder in einem privaten Surfmodus.
