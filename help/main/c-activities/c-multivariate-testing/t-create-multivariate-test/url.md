---
keywords: Multivarianz-Tests;Aktivitäts-URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die Seite bestimmt, die im Test verwendet wird und die geöffnet wird, wenn die Aktivität [!UICONTROL Multivarianz-Test] mit entworfen wird [!DNL Adobe Target].
title: Was ist die Aktivitäts-URL in einer Aktivität [!UICONTROL Multivariater Test] (MVT)?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
TQID: https://experienceleague.adobe.com/oQKwrlZ95XKEKSJIUiWqXXo9AJJzCb20gfS1rtwGImM
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 38%

---

# Aktivitäts-URL

Die Aktivitäts-URL bestimmt die Seite, die im [!UICONTROL Multivarianz-Test] (MVT) verwendet wird und die geöffnet wird, wenn der Test in [!DNL Adobe Target] entworfen wird.

1. Geben Sie die Aktivitäts-URL ein, wenn Sie während der [Erstellung der Aktivität](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.

   Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] (VEC) die Seite, die in Ihren [Visual Experience Composer-Einstellungen) ](/help/main/administrating-target/visual-experience-composer-set-up.md) ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

1. (Bedingt) Um nach dem Öffnen von VEC eine andere Seite anzuzeigen, klicken Sie auf das Symbol **[!UICONTROL Konfigurieren]**, wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus und geben Sie die URL an.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Regel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * [!UICONTROL  URL]
   * [!UICONTROL Domain]
   * [!UICONTROL path]
   * [!UICONTROL Hash (#)-Fragment]
   * [!UICONTROL Abfrage]
   * [!UICONTROL Benutzerspezifisch]

   Zusätzliche Regeln können mit UND oder ODER mit der Aktivitäts-URL verbunden werden. Alle hinzugefügten Regeln werden gegeneinander mit UND ausgewertet.

   Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die nicht den [!DNL Target] JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.
>
>Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können die Option **[!UICONTROL Mit JavaScript rendern]** deaktivieren, wenn Sie in der Lage sein möchten, solche Elemente mit dem [!UICONTROL Visual Experience Composer] zu ändern.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
