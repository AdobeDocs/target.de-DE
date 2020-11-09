---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library
description: Target Standard kann in die Adobe Dynamic Media Classic integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
title: Integration der dynamischen Media Classic-Integration
feature: administration general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 21%

---


# Scene7-Konfiguration {#scene-settings}

[!DNL Target] kann integriert werden, [!DNL Adobe Dynamic Media Classic] um Digital Asset Management (DAM) in der [!UICONTROL Inhaltsbibliothek]bereitzustellen.

>[!NOTE]
>
>Integrating [!DNL Target] with [!DNL Dynamic Media Classic] enables delivery of assets (as part of activities) uploaded to the [!DNL Adobe Experience Cloud] assets folder. This integration does not enable access to all assets uploaded in [!DNL Dynamic Media Classic] for delivery in [!DNL Target] activities.

If you already have a [!DNL Dynamic Media] account, you can supply your existing credentials. If you do not have an account, you can request a restricted-use [!DNL Dynamic Media Classic] account at no additional charge from your [!DNL Adobe] representative. This account can be used for purposes restricted for use in [!DNL Target] only. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

>[!NOTE]
>
>Ein eingeschränktes kostenloses [!DNL Dynamic Media Classic] Konto für [!DNL Adobe Target] wird nicht mehr für neue Kunden oder neue Benutzer unterstützt. Die vorhandenen Anmeldedaten funktionieren wie gewohnt.

If this setting is not configured, the [!UICONTROL Swap Image offer] option within the activity creation workflow is not available. Nachdem diese Einstellung konfiguriert wurde, steht die Option zum Austauschen/Ändern von Bildangeboten in  [Visual Experience Composer (VEC) und im formularbasierten Experience Composer](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) zur Verfügung. You can then leverage image offers with images that have been uploaded from the [!DNL Adobe Experience Cloud] for use in [!DNL Target] activities.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. There is no way to obtain the published URL of an image uploaded into the [!DNL Experience Cloud] to consume directly or outside of targeting workflows using [!DNL Target]. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Note that the storage URL and the final publish URLs of images from [!DNL Dynamic Media] are different and one must *NOT* create offers using the storage link of images as delivery will not work in such cases. Sie müssen die Image Angebots-Funktion verwenden, wie in unserer Hilfedokumentation beschrieben.

To integrate with [!DNL Dynamic Media Classic] ([!DNL Scene7]), you need to specify the following information.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Scene7-Konfiguration]**.

   ![Scene7-Seite](/help/administrating-target/assets/scene7.png)

1. Specify the following [!DNL Dynamic Media Classic] account information:

   **Region:** Die Region für Ihr [!DNL Dynamic Media] Konto: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Speicherort für Inhalte, die sich außerhalb des Ordners &quot;Zielgruppe&quot;befinden und manuell hochgeladen werden [!DNL Dynamic Media].

   **E-Mail-Adresse:** Die für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete E-Mail-Adresse.

   **Kennwort:** Das für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete Kennwort.

1. Klicken Sie auf **[!UICONTROL Senden]**.
