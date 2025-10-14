---
keywords: Aktivitäts-URL;URL;andere URL
description: Erfahren Sie, wie Sie die [!UICONTROL Activity URL] festlegen, um Testseiten zu definieren und ein korrektes Testdesign sicherzustellen.
title: Was ist die Aktivitäts-URL in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
source-git-commit: 2f86c9ee89b4e1698180f6b3dc9df393733eb780
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 32%

---

# Aktivitäts-URL

Die Aktivitäts-URL bestimmt die im Test verwendete Seite. Sie wird geöffnet, wenn der Test mit [!DNL Adobe Target] entworfen wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://www.adobe.com`] überein.

## Spezifizieren einer anderen URL

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] die Seite, die in Ihren [Visual Experience Composer-Einstellungen“ angegeben &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md). Sie können während der Erstellung der Aktivität eine andere Seite angeben.

1. (Bedingt) Um nach dem Öffnen der [!UICONTROL Visual Experience Composer] eine andere Seite anzuzeigen, klicken Sie auf der **[!UICONTROL Experiences]** Seite oben auf der Seite auf **[!UICONTROL Configure]** und wählen Sie dann **[!UICONTROL Page Delivery]** aus.

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

   Zusätzliche Regeln können mit UND oder ODER mit der Aktivitäts-URL verbunden werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** .

   Wenn Sie eine URL für eine Site eingegeben haben, die nicht den JavaScript-Code der [!DNL Target] enthält, können Sie keine Seitenelemente auswählen.

   Standardmäßig lässt das [!UICONTROL Visual Experience Composer] keine Änderungen an Elementen zu, die JavaScript enthalten, z. B. rotierende Banner. Sie können **[!UICONTROL Render using JavaScript]** deaktivieren, wenn Sie diese Elemente mithilfe der [!UICONTROL Visual Experience Composer] ändern möchten.—>

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.
