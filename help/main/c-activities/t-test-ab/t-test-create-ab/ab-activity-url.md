---
keywords: Aktivitäts-URL;URL;andere URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die beim Test verwendet wird und beim Entwurf des Tests geöffnet wird, indem Sie [!DNL Adobe Target].
title: Was ist die Aktivitäts-URL in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
source-git-commit: 6bca763d24649349dbc7cdf6e5f2dbc4ac0a480d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 64%

---

# Aktivitäts-URL

Die Aktivitäts-URL legt die Seite fest, die beim Test verwendet wird und beim Entwurf des Tests mit Adobe Target geöffnet wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Erstellen]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://www.adobe.com`] überein.

## Spezifizieren einer anderen URL

Standardmäßig wird die Variable [!UICONTROL Visual Experience Composer] öffnet die Seite, die in Ihrem [Visual Experience Composer-Einstellungen](/help/main/administrating-target/visual-experience-composer-set-up.md). Sie können während der Erstellung der Aktivität eine andere Seite angeben.

1. So zeigen Sie eine andere Seite nach dem [!UICONTROL Visual Experience Composer] öffnet sich in der **[!UICONTROL Erlebnisse]** klicken Sie auf die **[!UICONTROL Konfigurieren]** Zahnradsymbol, und wählen Sie **[!UICONTROL Seitenbereitstellung]**.

1. Geben Sie die URL in der **[!UICONTROL URL]** -Feld.

   ![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

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

Wenn Sie eine URL für eine Site eingegeben haben, die keinen [!DNL Target]-Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig gestattet der [!UICONTROL Visual Experience Composer] das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können die Option **[!UICONTROL Mit JavaScript rendern]** deaktivieren, wenn Sie in der Lage sein möchten, solche Elemente mit dem [!UICONTROL Visual Experience Composer] zu ändern.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
