---
keywords: aktivität URL;URL;andere URL
description: Erfahren Sie, wie Sie die Aktivitäten-URL angeben, die die  bestimmt, die im Test verwendet wird und die beim Testen mit Adobe Target geöffnet wird.
title: Wie lautet die Aktivitäten-URL in einer A/B-Aktivität?
feature: A/B Tests
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---


# Aktivitäts-URL

Die Aktivitäten-URL bestimmt die Seite, die im Test verwendet wird und die geöffnet wird, wenn der Test mit Adobe Target entworfen wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Erstellen]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://www.adobe.com`] überein.

## Spezifizieren einer anderen URL

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] die Seite, die in den [Visual Experience Composer-Einstellungen](/help/administrating-target/visual-experience-composer-set-up.md) angegeben ist.
. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

Damit nach dem Öffnen von [!UICONTROL Visual Experience Composer] eine andere Seite angezeigt wird, klicken Sie auf das Zahnradsymbol **[!UICONTROL Konfigurieren]** und wählen Sie dann **[!UICONTROL Seitenbereitstellung]**. Geben Sie die URL in das Feld „Aktivitäts-URL“ ein.

![Dialogfeld „Seitenbereitstellung“](/help/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domäne
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter „mbox“

Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die keinen [!DNL Target]-Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig gestattet der [!UICONTROL Visual Experience Composer] das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können die Option **[!UICONTROL Mit JavaScript rendern]** deaktivieren, wenn Sie in der Lage sein möchten, solche Elemente mit dem [!UICONTROL Visual Experience Composer] zu ändern.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
