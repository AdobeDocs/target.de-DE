---
description: Die Aktivitäts-URL bestimmt die Seite, die im Multivarianz-Test (MVT) verwendet wird und die beim Entwerfen des Tests in Target geöffnet wird.
keywords: Targeting
seo-description: Die Aktivitäts-URL bestimmt die Seite, die im Multivarianz-Test (MVT) verwendet wird und die beim Entwerfen des Tests in Adobe Target geöffnet wird.
seo-title: Aktivitäts-URL
solution: Target
title: Aktivitäts-URL
uuid: ddc7330c-199a-4e38-b3d4-6786e3997783
translation-type: tm+mt
source-git-commit: 0730d5f8f6aa2b72c2069c81d6e5a0183489e91c

---


# Aktivitäts-URL{#activity-url}

Die Aktivitäts-URL bestimmt die Seite, die im [!Multivariaten Test] (MVT) verwendet wird und die beim Entwerfen des Tests geöffnet wird [!DNL Adobe Target].

Geben Sie die Aktivitäts-URL an, wenn Sie während der Erstellung [](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie auf **[!UICONTROL Weiter]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `https://www.adobe.com`] und [!DNL `http://www.adobe.com`] überein.

Standardmäßig öffnet der [!UICONTROL Visual Experience Composer] (VEC) die Seite, die in Ihren [Kontovoreinstellungen angegeben](/help/administrating-target/r-target-account-preferences/target-account-preferences.md)ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

Um nach dem Öffnen des VEC eine andere Seite anzuzeigen, klicken Sie auf das Symbol **[!UICONTROL Konfigurieren]** und wählen **[!UICONTROL Sie dann Seitenauslieferung]** und geben Sie dann die URL an.

![Seitenbereitstellung, Dialogfeld](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen], um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen.**

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domäne
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter

Zusätzliche Regeln können mithilfe von „AND“ oder „OR“ an die Aktivitäts-URL angefügt werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.

Klicken Sie auf **[!UICONTROL „Speichern“], wenn Sie damit fertig sind.**

>[!NOTE]
>
>Wenn Sie eine URL für eine Site eingegeben haben, die keinen Target Standard-JavaScript-Code enthält, können Sie keine Seitenelemente auswählen.

Standardmäßig lässt VEC keine Änderungen an Elementen zu, die javascript enthalten, wie zum Beispiel sich drehende Banner. Sie können die Option **[!UICONTROL Mit JavaScript rendern]** deaktivieren, wenn Sie in der Lage sein möchten, solche Elemente mit dem [!UICONTROL Visual Experience Composer] zu ändern.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.