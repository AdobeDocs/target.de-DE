---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Adobe Target kann in die Adobe Dynamic Media Classic integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
title: Integration der Dynamic Media Classic-Integration
feature: administration general
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 22%

---


# Scene7-Konfiguration {#scene-settings}

[!DNL Target] kann integriert werden,  [!DNL Adobe Dynamic Media Classic] um Digital Asset Management (DAM) in der  [!UICONTROL Inhaltsbibliothek] bereitzustellen.

>[!NOTE]
>
>Durch die Integration von [!DNL Target] mit [!DNL Dynamic Media Classic] wird der Versand von Assets (als Teil von Aktivitäten) aktiviert, die in den Asset-Ordner [!DNL Adobe Experience Cloud] hochgeladen wurden. Diese Integration ermöglicht nicht den Zugriff auf alle in [!DNL Dynamic Media Classic] hochgeladenen Assets für Versände in [!DNL Target]-Aktivitäten.

Wenn Sie bereits über ein [!DNL Dynamic Media]-Konto verfügen, können Sie Ihre vorhandenen Anmeldeinformationen angeben. Wenn Sie kein Konto haben, können Sie ein [!DNL Dynamic Media Classic]-Konto mit eingeschränkter Verwendung ohne zusätzliche Kosten von Ihrem [!DNL Adobe]-Kundenbetreuer anfordern. Dieses Konto kann nur für Zwecke verwendet werden, die für die Verwendung in [!DNL Target] eingeschränkt sind. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Wenn diese Einstellung nicht konfiguriert ist, ist die Option [!UICONTROL Angebot tauschen] im Arbeitsablauf zum Erstellen der Aktivität nicht verfügbar. Nachdem diese Einstellung konfiguriert wurde, steht die Option zum Austauschen/Ändern von Bildangeboten in  [Visual Experience Composer (VEC) und im formularbasierten Experience Composer](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) zur Verfügung. Sie können dann Bild-Angebote mit Bildern verwenden, die aus dem [!DNL Adobe Experience Cloud] hochgeladen wurden, um sie in [!DNL Target]-Aktivitäten zu verwenden.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, die veröffentlichte URL eines Bildes abzurufen, das in das [!DNL Experience Cloud] hochgeladen wurde, um es direkt oder außerhalb der Targeting-Workflows mit [!DNL Target] zu verwenden. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass die Datenspeicherung-URL und die endgültige Veröffentlichungs-URLs von Bildern von [!DNL Dynamic Media] unterschiedlich sind und dass *NOT* Angebote mithilfe der Datenspeicherung-Verknüpfung von Bildern erstellen muss, da Versand in solchen Fällen nicht funktioniert. Sie müssen die Image Angebots-Funktion verwenden, wie in unserer Hilfedokumentation beschrieben.

Zur Integration mit [!DNL Dynamic Media Classic] ([!DNL Scene7]) müssen Sie die folgenden Informationen angeben.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

   ![Scene7-Seite](/help/administrating-target/assets/scene7.png)

1. Geben Sie die folgenden [!DNL Dynamic Media Classic]-Kontoinformationen an:

   **Region:** Die Region für Ihr  [!DNL Dynamic Media] Konto: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Speicherort für Inhalte, die sich außerhalb des Ordners &quot;Zielgruppe&quot;befinden und manuell in diesen Ordner hochgeladen werden  [!DNL Dynamic Media].

   **E-Mail-Adresse:** Die E-Mail-Adresse, die zum Anmelden bei  [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendet wird.

   **Kennwort:** Das für die Anmeldung bei  [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete Kennwort.

1. Klicken Sie auf **[!UICONTROL Senden]**.
