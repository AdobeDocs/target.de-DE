---
keywords: scene7;Dynamic Media Classic;Digital Asset Management;Assets;DAM;Inhaltsbibliothek;Bild tauschen
description: Hier erfahren Sie, wie Sie Adobe  [!DNL Target]  mit Adobe Dynamic Media Classic (früher Scene7) integrieren können, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
title: Wie konfiguriere ich die Integration von Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 85%

---

# Konfiguration von Dynamic Media Classic (früher Scene7)

[!DNL Adobe Target] kann in [!DNL Adobe Dynamic Media Classic] (früher [!DNL Scene7]) integriert werden, um Digital Asset Management (DAM) in der [!UICONTROL Content Library] bereitzustellen.

>[!NOTE]
>
>Die Integration von [!DNL Target] mit [!DNL Dynamic Media Classic] ermöglicht die Bereitstellung von Assets (als Teil von Aktivitäten), die in den Asset-Ordner von [!DNL Adobe Experience Cloud] hochgeladen wurden. Diese Integration bietet jedoch keinen Zugriff auf alle Assets, die in [!DNL Dynamic Media Classic] hochgeladen wurden, um sie in [!DNL Target]-Aktivitäten bereitzustellen.

Wenn Sie bereits über ein [!DNL Dynamic Media]-Konto verfügen, können Sie Ihre vorhandenen Anmeldedaten verwenden. Wenn Sie noch kein Konto haben, können Sie ein [!DNL Dynamic Media Classic]-Konto mit beschränkter Nutzung ohne zusätzliche Kosten bei Ihrem [!DNL Adobe]-Ansprechpartner anfordern. Dieses Konto kann für Zwecke verwendet werden, die sich ausschließlich auf [!DNL Target] beschränken. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Wenn diese Einstellung nicht konfiguriert ist, ist die Option [!UICONTROL Swap Image offer] im Workflow zur Erstellung der Aktivität nicht verfügbar. Nachdem diese Einstellung konfiguriert wurde, ist die Option zum Austauschen/Ändern von Bildangeboten sowohl im [Visual Experience Composer (VEC) als auch im formularbasierten Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) verfügbar. Anschließend können Sie die Bildangebote mit Bildern nutzen, die aus [!DNL Adobe Experience Cloud] für die Verwendung in [!DNL Target]-Aktivitäten hochgeladen wurden.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, mithilfe von [!DNL Target] die veröffentlichte URL eines in [!DNL Experience Cloud] hochgeladenen Bilds abzurufen, um es direkt oder außerhalb der Zielgruppen-Workflows zu verwenden. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass sich die Speicher-URL und die endgültigen Veröffentlichungs-URLs von Bildern aus [!DNL Dynamic Media] unterscheiden. Zudem dürfen *KEINE* Angebote über den Speicher-Link der Bilder erstellt werden, da die Bereitstellung in solchen Fällen nicht funktioniert. Stattdessen muss die Bildangebotsfunktionalität verwendet werden. Erläuterungen dazu finden Sie in unserer Hilfedokumentation.

Zur Integration mit [!DNL Dynamic Media Classic] ([!DNL Scene7]) müssen Sie die folgenden Informationen angeben.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

   ![Scene7-Seite](/help/main/administrating-target/assets/scene7.png)

1. Geben Sie folgende [!DNL Dynamic Media Classic]-Kontoinformationen an:

   **Region:** Die Region Ihres [!DNL Dynamic Media]-Kontos: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Speicherort für Inhalte, die außerhalb des Zielordners liegen und manuell in [!DNL Dynamic Media] hochgeladen werden.

   **E-Mail-Adresse:** Die für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete E-Mail-Adresse.

   **Kennwort:** Das für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete Kennwort.

1. Klicken Sie auf **[!UICONTROL Submit]**.
