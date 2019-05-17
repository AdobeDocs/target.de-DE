---
description: Die Aktivitäts-URL legt die Seite fest, die bei dem Test verwendet wird und die beim Entwurf des Tests geöffnet wird.
keywords: Targeting
seo-description: Die Aktivitäts-URL legt die Seite fest, die bei dem Test verwendet wird und die beim Entwurf des Tests geöffnet wird.
seo-title: Aktivitäts-URL
solution: Target
title: Aktivitäts-URL
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Aktivitäts-URL{#activity-url}

Die Aktivitäts-URL legt die Seite fest, die bei dem Test verwendet wird und die beim Entwurf des Tests geöffnet wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Aktivität erstellen]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.

Standardmäßig öffnet der Visual Experience Composer die Seite, die in Ihren Konto-Voreinstellungen angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

Damit nach dem Öffnen von Visual Experience Composer eine andere Seite angezeigt wird, klicken Sie auf **[!UICONTROL Konfigurieren]**. Wählen Sie **[!UICONTROL URL]** und geben Sie im Feld „Aktivitäts-URL“ die gewünschte URL ein.

![](assets/url-config.png)

Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen], um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.**

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domäne
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter „mbox“

Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

Klicken Sie auf **[!UICONTROL „Speichern“], wenn Sie damit fertig sind.**

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die keinen Target Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig gestattet der [!UICONTROL Visual Experience Composer] das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können die Option **[!UICONTROL Mit JavaScript rendern]** deaktivieren, wenn Sie in der Lage sein möchten, solche Elemente mit dem [!UICONTROL Visual Experience Composer] zu ändern.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
