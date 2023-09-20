---
keywords: Erlebnis-Targeting;XT;Aktivitäts-URL;URL
description: Erfahren Sie, wie Sie die [!UICONTROL Aktivitäts URL] , die die Seite bestimmt, die im Test verwendet wird und die beim Öffnen der [!UICONTROL Erlebnis-Targeting] -Aktivität wird mit [!DNL Adobe Target].
title: Was ist das [!UICONTROL Aktivitäts URL] In einer [!UICONTROL Erlebnis-Targeting] (XT) Aktivität?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 24513d8cb39d38dcfbc74bf40961d5517cc90a4b
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 48%

---

# Aktivitäts-URL [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten

Die [!UICONTROL Aktivitäts URL] bestimmt die Seite, die in einer [!DNL Adobe Target] [!UICONTROL Erlebnis-Targeting] (XT). Diese Seite wird im [!UICONTROL Visual Experience Composer] (VEC) [!UICONTROL Form-Based Experience Composer] wenn die Aktivität erstellt wurde.

1. Spezifizieren Sie die Aktivitäts-URL, wenn Sie [beim Erstellen einer XT-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.
   >
   >Standardmäßig wird der VEC oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) öffnet die Seite, die in Ihrem [Visual Experience Composer-Einstellungen](/help/main/administrating-target/visual-experience-composer-set-up.md). Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site angeben, die keine [[!DNL Target] JavaScript-Bibliothek &quot;at.js&quot;oder [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=de){target=_blank}können Sie keine Seitenelemente auswählen.

1. (Bedingt) Wenn Sie nach dem Öffnen des VEC eine andere Seite anzeigen möchten, klicken Sie auf **[!UICONTROL Konfigurieren]** auswählen **[!UICONTROL Seitenbereitstellung]** und geben Sie dann die URL in der [!UICONTROL URL] -Feld.

   ![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

1. (Abhängig von Ihrer Lizenz) Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domain
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“

   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.
