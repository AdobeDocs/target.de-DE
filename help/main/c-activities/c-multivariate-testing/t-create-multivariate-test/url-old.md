---
keywords: Multivarianz-Tests;Aktivitäts-URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die im Test verwendet wird und die geöffnet wird, wenn die [!UICONTROL Multivariate Test]-Aktivität erstellt wird mit [!DNL Adobe Target].
title: Was ist die Aktivitäts-URL in einer [!UICONTROL Multivariate Test]-Aktivität (MVT)?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 34%

---

# Aktivitäts-URL

Die Aktivitäts-URL bestimmt die Seite, die im [!UICONTROL Multivariate Test] (MVT) verwendet wird und die geöffnet wird, wenn der Test in [!DNL Adobe Target] entworfen wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der [Erstellung der Aktivität](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Next]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] (VEC) die Seite, die in Ihren [Visual Experience Composer-Einstellungen“ ](/help/main/administrating-target/visual-experience-composer-set-up.md) ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

Um nach dem Öffnen von VEC eine andere Seite anzuzeigen, klicken Sie auf das **[!UICONTROL Configure]**, wählen Sie **[!UICONTROL Page Delivery]** aus und geben Sie die URL an.

![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Klicken Sie auf **[!UICONTROL Add Template Rule]** , um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domain
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter

Zusätzliche Regeln können mit UND oder ODER mit der Aktivitäts-URL verbunden werden. Alle hinzugefügten Regeln werden gegeneinander mit UND ausgewertet.

Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** .

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die nicht den [!DNL Target] JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können **[!UICONTROL Render using JavaScript]** deaktivieren, wenn Sie diese Elemente mithilfe der [!UICONTROL Visual Experience Composer] ändern möchten.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
