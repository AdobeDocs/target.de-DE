---
keywords: Aktivitäts-URL;URL;andere URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die im Test verwendet wird und die geöffnet wird, wenn der Test mit entworfen wird [!DNL Adobe Target].
title: Was ist die Aktivitäts-URL in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
source-git-commit: 6bca763d24649349dbc7cdf6e5f2dbc4ac0a480d
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 44%

---

# Aktivitäts-URL

Die Aktivitäts-URL bestimmt die im Test verwendete Seite. Sie wird geöffnet, wenn der Test mit Adobe Target erstellt wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://www.adobe.com`] überein.

## Spezifizieren einer anderen URL

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] die Seite, die in Ihren [Visual Experience Composer-Einstellungen“ angegeben ](/help/main/administrating-target/visual-experience-composer-set-up.md). Sie können während der Erstellung der Aktivität eine andere Seite angeben.

1. Wenn Sie nach dem Öffnen des [!UICONTROL Visual Experience Composer] eine andere Seite anzeigen möchten, klicken Sie auf der **[!UICONTROL Experiences]** auf das Zahnradsymbol **[!UICONTROL Configure]** und wählen Sie **[!UICONTROL Page Delivery]** aus.

1. Geben Sie die URL im Feld **[!UICONTROL URL]** an.

   ![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

1. (Bedingt) Klicken Sie auf **[!UICONTROL Add Template Rule]** , um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domain
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“

   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** .

Wenn Sie eine URL für eine Site eingegeben haben, die keinen [!DNL Target]-Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig lässt das [!UICONTROL Visual Experience Composer] keine Änderungen an Elementen zu, die JavaScript enthalten, z. B. rotierende Banner. Sie können **[!UICONTROL Render using JavaScript]** deaktivieren, wenn Sie diese Elemente mithilfe der [!UICONTROL Visual Experience Composer] ändern möchten.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
