---
keywords: scene7;Dynamic Media Classic;Digital Asset Management;Assets;DAM;Inhaltsbibliothek;Bild tauschen
description: Erfahren Sie, wie Sie Adobe [!DNL Target] mit Adobe Dynamic Media Classic (früher Scene7) integrieren, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
title: Wie konfiguriere ich die Integration von Dynamic Media Classic (Scene7)?
feature: Administration und Konfiguration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
source-git-commit: be7b5478006af231aae2b78e4a8c0066e3cb4a5b
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 21%

---

# Dynamic Media Classic (früher Scene7)-Konfiguration

[!DNL Adobe Target] kann in integriert werden ( [!DNL Adobe Dynamic Media Classic] früher  [!DNL Scene7]), um Digital Asset Management (DAM) in der  [!UICONTROL Inhaltsbibliothek] bereitzustellen.

>[!NOTE]
>
>Durch die Integration von [!DNL Target] mit [!DNL Dynamic Media Classic] wird die Bereitstellung von Assets (als Teil von Aktivitäten) aktiviert, die in den Ordner [!DNL Adobe Experience Cloud] Assets hochgeladen wurden. Diese Integration ermöglicht nicht den Zugriff auf alle Assets, die in [!DNL Dynamic Media Classic] hochgeladen wurden, um sie in [!DNL Target] -Aktivitäten bereitzustellen.

Wenn Sie bereits über ein [!DNL Dynamic Media]-Konto verfügen, können Sie Ihre vorhandenen Anmeldedaten angeben. Wenn Sie kein Konto haben, können Sie ein eingeschränktes [!DNL Dynamic Media Classic]-Konto ohne zusätzliche Kosten von Ihrem [!DNL Adobe]-Support-Mitarbeiter anfordern. Dieses Konto kann nur für Zwecke verwendet werden, die nur in [!DNL Target] verwendet werden können. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Wenn diese Einstellung nicht konfiguriert ist, ist die Option [!UICONTROL Bildangebot tauschen] im Workflow zur Aktivitätserstellung nicht verfügbar. Nachdem diese Einstellung konfiguriert wurde, steht die Option zum Austauschen/Ändern von Bildangeboten in  [Visual Experience Composer (VEC) und im formularbasierten Experience Composer](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) zur Verfügung. Sie können dann Bildangebote mit Bildern nutzen, die aus [!DNL Adobe Experience Cloud] hochgeladen wurden und in [!DNL Target] -Aktivitäten verwendet werden können.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, die veröffentlichte URL eines Bildes abzurufen, das in [!DNL Experience Cloud] hochgeladen wurde, um es direkt oder außerhalb der Zielgruppen-Workflows mit [!DNL Target] zu nutzen. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass sich die Speicher-URL und die endgültigen Veröffentlichungs-URLs der Bilder von [!DNL Dynamic Media] unterscheiden und *NOT* Angebote erstellen muss, die den Speicherlink der Bilder verwenden, da die Bereitstellung in solchen Fällen nicht funktioniert. Sie müssen die Bildangebotsfunktion verwenden, wie in unserer Hilfedokumentation beschrieben.

Zur Integration mit [!DNL Dynamic Media Classic] ([!DNL Scene7]) müssen Sie die folgenden Informationen angeben.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Scene7-Konfiguration]**.

   ![Scene7-Seite](/help/administrating-target/assets/scene7.png)

1. Geben Sie die folgenden [!DNL Dynamic Media Classic]-Kontoinformationen an:

   **Region:** Die Region für Ihr  [!DNL Dynamic Media] Konto: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Speicherort für Inhalt, der außerhalb des Zielordners liegt und manuell in  [!DNL Dynamic Media]hochgeladen wird.

   **E-Mail-Adresse:** Die für die Anmeldung bei  [!DNL Dynamic Media Classic] ([!DNL Scene7]) verwendete E-Mail-Adresse.

   **Kennwort:** Das Kennwort für die Anmeldung bei  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Klicken Sie auf **[!UICONTROL Senden]**.
