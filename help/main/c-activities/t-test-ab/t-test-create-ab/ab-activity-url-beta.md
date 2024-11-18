---
keywords: Aktivitäts-URL;URL;andere URL
description: Erfahren Sie, wie Sie die [!UICONTROL Activity URL] festlegen, um Testseiten zu definieren und ein genaues Testdesign zu gewährleisten.
title: Was ist die Aktivitäts-URL in einer A/B-Aktivität?
feature: A/B Tests
hide: true
hidefromtoc: true
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
source-git-commit: d5bd3b0d7cdf6eb06175a6365da6b8173f76800f
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 40%

---

# Aktivitäts-URL

Die Aktivitäts-URL legt die Seite fest, die beim Test verwendet wird und beim Entwurf des Tests mit [!DNL Adobe Target] geöffnet wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen sowohl [!DNL `http://www.adobe.com`] als auch [!DNL `https://www.adobe.com`] überein.

## Spezifizieren einer anderen URL

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] die Seite, die in Ihren [Visual Experience Composer-Einstellungen](/help/main/administrating-target/visual-experience-composer-set-up.md) angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

1. (Bedingt) Wenn Sie nach dem Öffnen von [!UICONTROL Visual Experience Composer] eine andere Seite anzeigen möchten, klicken Sie auf der Seite **[!UICONTROL Experiences]** oben auf der Seite auf **[!UICONTROL Configure]** und wählen Sie dann **[!UICONTROL Page Delivery]** aus.

1. Geben Sie die URL im Feld **[!UICONTROL URL]** an.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Add Rule]** , um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

   Zusätzliche Regeln können auf Folgendem basieren:

   * URL
   * Domain
   * Pfad
   * Hashfragment (#)
   * Abfrage
   * Parameter „mbox“
   * Benutzerdefiniert

   Zusätzliche Regeln können mit UND oder ODER zur Aktivitäts-URL hinzugefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Klicken Sie auf **[!UICONTROL Save]** , wenn Sie fertig sind.

<!-- If you entered a URL for a site that does not include the [!DNL Target]s JavaScript code, you cannot select page elements.

By default, the [!UICONTROL Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL Visual Experience Composer].-->

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
