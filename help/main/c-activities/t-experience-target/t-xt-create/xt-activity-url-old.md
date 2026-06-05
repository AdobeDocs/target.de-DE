---
keywords: Experience Targeting;XT;Aktivitäts-URL;URL
description: Erfahren Sie, wie Sie die [!UICONTROL Aktivitäts-URL] angeben, die die im Test verwendete Seite bestimmt und die geöffnet wird, wenn die [!UICONTROL Erlebnis-Targeting]-Aktivität erstellt wird [!DNL Adobe Target].
title: Was ist die [!UICONTROL Aktivitäts-URL] in einer [!UICONTROL Erlebnis-Targeting]-Aktivität (XT)?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 36%

---

# Aktivitäts-URL in [!UICONTROL Erlebnis-Targeting]-Aktivitäten (XT)

Die [!UICONTROL Aktivitäts-URL] bestimmt die Seite, die in einer [!DNL Adobe Target] (Experience [!UICONTROL ) &#x200B;]Zielgruppenbestimmungsaktivität (XT) verwendet wird. Hierbei handelt es sich um die Seite, [!UICONTROL &#x200B; beim Entwerfen der Aktivität im &#x200B;]Visual Experience Composer[!UICONTROL &#x200B; (VEC) oder &#x200B;]Form-Based Experience Composer) geöffnet wird.

1. Spezifizieren Sie die Aktivitäts-URL, wenn Sie [beim Erstellen einer XT-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.
   >
   >Standardmäßig öffnet der VEC oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) die Seite, die in Ihren Einstellungen von [Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md) angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site angeben, die keine [[!DNL Target] at.js-JavaScript-Bibliothek oder  [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank} enthält, können Sie keine Seitenelemente auswählen.

1. (Bedingt) Um nach dem Öffnen von VEC eine andere Seite anzuzeigen, klicken Sie auf **[!UICONTROL Konfigurieren]** wählen Sie **[!UICONTROL Seitenbereitstellung]** aus und geben Sie dann die URL in das Feld [!UICONTROL URL] ein.

   ![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domain
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“

   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.
