---
keywords: Erlebnis-Targeting;XT;Aktivitäts-URL;URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die beim Test verwendet wird und beim Entwurf der Erlebnis-Targeting-Aktivität mit Adobe Target geöffnet wird.
title: Was ist die Aktivitäts-URL in einer Erlebnis-Targeting (XT)-Aktivität?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 63%

---

# Aktivitäts-URL in Erlebnis-Targeting-Aktivitäten (XT)

Die [!UICONTROL Aktivitäts-URL] bestimmt die Seite, die in der Variablen [!DNL Adobe Target] [!UICONTROL Erlebnis-Targeting] (XT) und die in der [!UICONTROL Visual Experience Composer] (VEC) oder [!UICONTROL Form-Based Experience Composer] wenn die Aktivität erstellt wurde.

1. Spezifizieren Sie die Aktivitäts-URL, wenn Sie [beim Erstellen einer XT-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.
   >
   >Standardmäßig öffnet der VEC oder formularbasierte Experience Composer die Seite, die in Ihrer [Visual Experience Composer-Einstellungen](/help/main/administrating-target/visual-experience-composer-set-up.md). Sie können während der Erstellung der Aktivität eine andere Seite angeben.
   >
   >Wenn Sie eine URL für eine Site eingegeben haben, die keinen Target Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

1. (Abhängig von Ihrer Lizenz) Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf **[!UICONTROL Konfigurieren]**, wählen Sie **[!UICONTROL Seitenbereitstellung]** aus und geben Sie im Feld [!UICONTROL URL] die URL an.

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
