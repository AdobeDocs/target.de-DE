---
keywords: Erlebnis-Targeting;XT;Aktivitäts-URL;URL
description: Erfahren Sie, wie Sie den [!UICONTROL Activity URL] angeben, der die Seite bestimmt, die beim Test verwendet wird und beim Entwurf der [!UICONTROL Experience Targeting] -Aktivität mit  [!DNL Adobe Target] geöffnet wird.
title: Was ist der [!UICONTROL Activity URL] in einer [!UICONTROL Experience Targeting] (XT)-Aktivität?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 24513d8cb39d38dcfbc74bf40961d5517cc90a4b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 39%

---

# Aktivitäts-URL in [!UICONTROL Experience Targeting] -Aktivitäten (XT)

Der [!UICONTROL Activity URL] bestimmt die Seite, die in einer [!DNL Adobe Target] [!UICONTROL Experience Targeting] -Aktivität (XT) verwendet wird. Dies ist die Seite, die beim Entwurf der Aktivität in [!UICONTROL Visual Experience Composer] (VEC) oder [!UICONTROL Form-Based Experience Composer] geöffnet wird.

1. Spezifizieren Sie die Aktivitäts-URL, wenn Sie [beim Erstellen einer XT-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen sowohl [!DNL `https://www.adobe.com`] als auch [!DNL `http://www.adobe.com`] überein.
   >
   >Standardmäßig öffnet der VEC oder [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) die Seite, die in Ihren [Visual Experience Composer-Einstellungen](/help/main/administrating-target/visual-experience-composer-set-up.md) angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site angeben, die keine [[!DNL Target] at.js JavaScript-Bibliothek oder  [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank} enthält, können Sie keine Seitenelemente auswählen.

1. (Bedingt) Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf **[!UICONTROL Configure]**, wählen Sie **[!UICONTROL Page Delivery]** aus und geben Sie dann die URL im Feld [!UICONTROL URL] an.

   ![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Add Template Rule]** , um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domain
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“

   Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL Save]** , wenn Sie fertig sind.
