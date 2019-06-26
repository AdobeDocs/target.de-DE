---
description: Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität verwendet wird und im Visual Experience Composer (VEC) oder in Form-Based Experience Composer geöffnet wird, wenn die Aktivität entwickelt wurde.
keywords: Targeting
seo-description: Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität verwendet wird und im Adobe Target Visual Experience Composer (VEC) oder in Form-Based Experience Composer geöffnet wird, wenn die Aktivität entwickelt wurde.
seo-title: Aktivitäts-URL
solution: Target
title: Aktivitäts-URL
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Aktivitäts-URL{#activity-url}

Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität (XT) verwendet wird und im Visual Experience Composer (VEC) oder in Form-Based Experience Composer geöffnet wird, wenn die Aktivität entwickelt wurde.

1. When prompted while [creating an XT activity](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), specify the activity URL. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.
   >
   >By default, the VEC or Form-Based Experience Composer opens the page that is specified in your [Account Preferences](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site angeben, die keinen Target Standard-javascript-Code enthält, können Sie keine Seitenelemente auswählen.

1. (Conditional) To display a different page after the VEC opens, click **[!UICONTROL Configure]**, select **[!UICONTROL Page Delivery]**, and specify the URL in the [!UICONTROL URL] field.

   ![Seitenbereitstellung, Dialogfeld](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

1. (Conditional) Click **[!UICONTROL Add Template Rule]** to add more pages or sections to the activity.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domäne
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“
   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL „Speichern“], wenn Sie damit fertig sind.**