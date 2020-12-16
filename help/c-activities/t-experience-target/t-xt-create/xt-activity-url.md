---
keywords: Targeting
description: Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität verwendet wird und im Visual Experience Composer (VEC) von Adobe Target oder im formularbasierten Experience Composer bei der Erstellung der Aktivität geöffnet wird.
title: Aktivitäts-URL
feature: xt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 92%

---


# Aktivitäts-URL{#activity-url}

Die Aktivitäts-URL bestimmt die Seite, die in der Erlebnis-Targeting-Aktivität (XT) verwendet wird und im Visual Experience Composer (VEC) oder im formularbasierten Experience Composer bei der Erstellung der Aktivität geöffnet wird.

1. Spezifizieren Sie die Aktivitäts-URL, wenn Sie [beim Erstellen einer XT-Aktivität](/help/c-activities/t-experience-target/t-xt-create/xt-create.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.
   >
   >Standardmäßig öffnet der VEC- oder Form-Based Experience Composer die Seite, die in den [Visual Experience Composer-Einstellungen](/help/administrating-target/visual-experience-composer-set-up.md) angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site eingegeben haben, die keinen Target Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

1. (Abhängig von Ihrer Lizenz) Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf **[!UICONTROL Konfigurieren]**, wählen Sie **[!UICONTROL Seitenbereitstellung]** aus und geben Sie im Feld [!UICONTROL URL] die URL an.

   ![Dialogfeld „Seitenbereitstellung“](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

1. (Abhängig von Ihrer Lizenz) Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domäne
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“

   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.