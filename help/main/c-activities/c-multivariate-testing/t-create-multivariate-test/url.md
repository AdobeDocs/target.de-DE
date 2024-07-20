---
keywords: Multivarianz-Tests;Aktivitäts-URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die beim Test verwendet wird und beim Entwurf der [!UICONTROL Multivariate Test] -Aktivität mit  [!DNL Adobe Target] geöffnet wird.
title: Was ist die Aktivitäts-URL in einer [!UICONTROL Multivariate Test] -Aktivität (MVT)?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 7853d8c5934e40d1026e067dfa413f520ecba931
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 34%

---

# Aktivitäts-URL

Die Aktivitäts-URL legt die Seite fest, die im [!UICONTROL Multivariate Test] (MVT) verwendet wird und beim Entwurf des Tests in [!DNL Adobe Target] geöffnet wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der [Erstellung der Aktivität](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Next]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen sowohl [!DNL `https://www.adobe.com`] als auch [!DNL `http://www.adobe.com`] überein.

Standardmäßig öffnet der VEC (0) die Seite, die in Ihren [Visual Experience Composer-Einstellungen](/help/main/administrating-target/visual-experience-composer-set-up.md) angegeben ist. [!UICONTROL Visual Experience Composer] Sie können während der Erstellung der Aktivität eine andere Seite angeben.

Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf das Symbol &quot;**[!UICONTROL Configure]**&quot;, wählen Sie &quot;**[!UICONTROL Page Delivery]**&quot;und geben Sie dann die URL an.

![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Klicken Sie auf **[!UICONTROL Add Template Rule]** , um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domain
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter

Zusätzliche Regeln können mit UND oder ODER zur Aktivitäts-URL hinzugefügt werden. Alle von Ihnen hinzugefügten Regeln werden mit UND gegeneinander ausgewertet.

Klicken Sie auf **[!UICONTROL Save]** , wenn Sie fertig sind.

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die nicht den JavaScript-Code [!DNL Target] enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können **[!UICONTROL Render using JavaScript]** deaktivieren, wenn Sie diese Elemente mit dem [!UICONTROL Visual Experience Composer] ändern können möchten.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
