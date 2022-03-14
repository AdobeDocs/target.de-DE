---
keywords: Multivarianz-Tests;Aktivitäts-URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die beim Test verwendet wird und beim Entwurf der Aktivität Multivarianz-Test mit Adobe Target geöffnet wird.
title: Was ist die Aktivitäts-URL in einer Multivarianz (MVT)-Aktivität?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 85%

---

# Aktivitäts-URL

Die Aktivitäts-URL legt die Seite fest, die bei dem [!UICONTROL Multivarianz-Test] (MVT) verwendet wird und bei dessen Entwurf in [!DNL Adobe Target] geöffnet wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der [Erstellung der Aktivität](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie anschließend auf **[!UICONTROL Weiter]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.

Standardmäßig öffnet [!UICONTROL Visual Experience Composer] (VEC) die Seite, die in Ihren [Voreinstellungen von Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md) angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf das Symbol **[!UICONTROL Konfigurieren]**, wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus und geben Sie die URL an.

![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domain
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter

Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die keinen Target Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können die Option **[!UICONTROL Mit JavaScript rendern]** deaktivieren, wenn Sie in der Lage sein möchten, solche Elemente mit dem [!UICONTROL Visual Experience Composer] zu ändern.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
