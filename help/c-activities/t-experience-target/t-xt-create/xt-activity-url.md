---
description: Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität verwendet wird und im Visual Experience Composer (VEC) oder in Form-Based Experience Composer geöffnet wird, wenn die Aktivität entwickelt wurde.
keywords: Targeting
seo-description: Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität verwendet wird und im Adobe Target Visual Experience Composer (VEC) oder in Form-Based Experience Composer geöffnet wird, wenn die Aktivität entwickelt wurde.
seo-title: Aktivitäts-URL
solution: Target
title: Aktivitäts-URL
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: ca9639ccca286dac182728f7bbd43fac78217209

---


# Aktivitäts-URL{#activity-url}

Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität (XT) verwendet wird und im Visual Experience Composer (VEC) oder in Form-Based Experience Composer geöffnet wird, wenn die Aktivität entwickelt wurde.

1. Geben Sie die Aktivitäts-URL an, wenn Sie [beim Erstellen einer XT-Aktivität](/help/c-activities/t-experience-target/t-xt-create/xt-create.md)dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.
   >
   >Standardmäßig öffnet der VEC oder Form-Based Experience Composer die Seite, die in Ihren [Kontovoreinstellungen angegeben](/help/administrating-target/r-target-account-preferences/target-account-preferences.md)ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site angeben, die keinen Target Standard-javascript-Code enthält, können Sie keine Seitenelemente auswählen.

1. (Bedingt) Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf **[!UICONTROL Konfigurieren]**, wählen **[!UICONTROL Sie &quot;Seitenauslieferung]**«und geben Sie die URL im Feld [!UICONTROL &quot; URL] &quot; an.

   ![Seitenbereitstellung, Dialogfeld](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

1. (Bedingt) Klicken **[!UICONTROL Sie auf Vorlagenregel]** hinzufügen, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domäne
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“
   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL „Speichern“], wenn Sie damit fertig sind.**