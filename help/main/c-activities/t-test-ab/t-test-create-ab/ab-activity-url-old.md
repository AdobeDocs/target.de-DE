---
keywords: Aktivitäts-URL;URL;andere URL
description: Erfahren Sie, wie Sie die Aktivitäts-URL angeben, die die im Test verwendete Seite bestimmt und die geöffnet wird, wenn der Test mit [!DNL Adobe Target] entworfen wird.
title: Was ist die Aktivitäts-URL in einer A/B-Aktivität?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 55%
---
# Aktivitäts-URL

Die Aktivitäts-URL bestimmt die im Test verwendete Seite. Sie wird geöffnet, wenn der Test mit Adobe Target erstellt wird.

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Erstellen]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://www.adobe.com`] überein.

## Spezifizieren einer anderen URL

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] die Seite, die in Ihren [Visual Experience Composer-Einstellungen“ &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md) ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

1. Um nach dem Öffnen von [!UICONTROL Visual Experience Composer] eine andere Seite anzuzeigen, klicken Sie auf der Seite **[!UICONTROL Erlebnisse]** auf das **[!UICONTROL Konfigurieren]** und wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus.

1. Geben Sie die URL im Feld **[!UICONTROL URL]** an.

   ![Dialogfeld „Seitenbereitstellung“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

1. (Bedingt) Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]**, um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.

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
