---
keywords: scene7;Dynamic Media Classic;Digital Asset Management;Assets;DAM;Inhaltsbibliothek;Bild tauschen
description: Erfahren Sie, wie Sie Adobe [!DNL Target] mit Adobe Dynamic Media Classic (früher Scene7) integrieren können, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
title: Wie konfiguriere ich die Integration von Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: 'https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 78%
---
# Konfiguration von Dynamic Media Classic (früher Scene7)

[!DNL Adobe Target] kann in [!DNL Adobe Dynamic Media Classic] (früher [!DNL Scene7]) integriert werden, um Digital Asset Management (DAM) in der [!UICONTROL Inhaltsbibliothek) &#x200B;].

{{permissions-update}}

>[!NOTE]
>
>Die Integration von [!DNL Target] mit [!DNL Dynamic Media Classic] ermöglicht die Bereitstellung von Assets (als Teil von Aktivitäten), die in den Asset-Ordner von [!DNL Adobe Experience Cloud] hochgeladen wurden. Diese Integration bietet jedoch keinen Zugriff auf alle Assets, die in [!DNL Dynamic Media Classic] hochgeladen wurden, um sie in [!DNL Target]-Aktivitäten bereitzustellen.

Wenn Sie bereits über ein [!DNL Dynamic Media]-Konto verfügen, können Sie Ihre vorhandenen Anmeldedaten verwenden. Wenn Sie noch kein Konto haben, können Sie ein [!DNL Dynamic Media Classic]-Konto mit beschränkter Nutzung ohne zusätzliche Kosten bei Ihrem [!DNL Adobe]-Ansprechpartner anfordern. Dieses Konto kann für Zwecke verwendet werden, die sich ausschließlich auf [!DNL Target] beschränken. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Wenn diese Einstellung nicht konfiguriert ist, steht die Option [!UICONTROL Bild austauschen] im Workflow für die Erstellung der Aktivität nicht zur Verfügung. Nachdem diese Einstellung konfiguriert wurde, ist die Option zum Austauschen/Ändern von Bildangeboten sowohl im [Visual Experience Composer (VEC) als auch im formularbasierten Experience Composer &#x200B;](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Anschließend können Sie die Bildangebote mit Bildern nutzen, die aus [!DNL Adobe Experience Cloud] für die Verwendung in [!DNL Target]-Aktivitäten hochgeladen wurden.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, mithilfe von [!DNL Target] die veröffentlichte URL eines in [!DNL Experience Cloud] hochgeladenen Bilds abzurufen, um es direkt oder außerhalb der Zielgruppen-Workflows zu verwenden. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass sich die Speicher-URL und die endgültigen Veröffentlichungs-URLs von Bildern aus [!DNL Dynamic Media] unterscheiden. Zudem dürfen *KEINE* Angebote über den Speicher-Link der Bilder erstellt werden, da die Bereitstellung in solchen Fällen nicht funktioniert. Stattdessen muss die Bildangebotsfunktionalität verwendet werden. Erläuterungen dazu finden Sie in unserer Hilfedokumentation.

Zur Integration mit [!DNL Dynamic Media Classic] ([!DNL Scene7]) müssen Sie die folgenden Informationen angeben.

1. Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Scene7-Konfiguration]**.

1. Geben Sie folgende [!DNL Dynamic Media Classic]-Kontoinformationen an:

   **Region:** Die Region Ihres [!DNL Dynamic Media]-Kontos: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Speicherort für Inhalte, die außerhalb des Zielordners liegen und manuell in [!DNL Dynamic Media] hochgeladen werden.

   **E-Mail-Adresse:** Die für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete E-Mail-Adresse.

   **Kennwort:** Das für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete Kennwort.

1. Klicken Sie auf **[!UICONTROL Absenden]**.
