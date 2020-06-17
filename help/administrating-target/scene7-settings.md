---
description: Target Standard kann in Adobe Dynamic Media Classic (zuvor Scene7) integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek zu ermöglichen.
title: Integration von Dynamic Media Classic Konfigurationsintegration
subtopic: Getting Started
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 85%

---


# Integration von Dynamic Media Classic{#scene-settings}

Target kann in Adobe Dynamic Media Classic (zuvor Scene7) integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek zu ermöglichen.

>[!NOTE]
>
>Die Informationen in diesem Thema wurden aktualisiert, um Ihnen einen kurzen Höhepunkt bei den UI-Änderungen zu geben, die in der Target Standard/Premium-Version 20.6.1 (Juli 2020) erscheinen. Die meisten der in diesem Thema dargestellten Informationen gelten für die aktuelle Benutzeroberfläche; Die Optionen befinden sich jedoch möglicherweise an etwas anderen Orten.

>[!NOTE]
>
>Die Integration von Target mit Dynamic Media Classic ermöglicht die Bereitstellung von Assets (als Teil von Aktivitäten), die in den Asset-Ordner von Adobe Experience Cloud hochgeladen wurden. Diese Integration gibt jedoch keinen Zugriff auf alle Assets, die in Dynamic Media Classic hochgeladen wurden, um sie in Target-Aktivitäten bereitzustellen.

Wenn Sie bereits über ein Dynamic Media-Konto verfügen, können Sie Ihre vorhandenen Anmeldedaten verwenden. Wenn Sie noch kein Konto haben, können Sie ein Dynamic Media Classic-Konto mit beschränkter Nutzung ohne zusätzliche Kosten bei einem Adobe-Support-Mitarbeiter anfordern. Dieses Konto kann für Zwecke verwendet werden, die sich ausschließlich auf Target beschränken. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

Wenn diese Einstellung nicht konfiguriert ist, steht die Angebotsoption „Bild austauschen“ im Workflow für die Erstellung der Aktivität nicht zur Verfügung. Nachdem diese Einstellung konfiguriert wurde, steht die Option zum Austauschen/Ändern von Bildangeboten in  [Visual Experience Composer (VEC) und im formularbasierten Experience Composer](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) zur Verfügung. Anschließend können Sie die Bildangebote mit Bildern nutzen, die aus Adobe Experience Cloud für die Verwendung in Target-Aktivitäten hochgeladen wurden.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, mithilfe von Adobe Target die veröffentlichte URL eines in Experience Cloud hochgeladenen Bilds abzurufen, um es direkt oder außerhalb der Targeting-Workflows zu verwenden. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass sich die Speicher-URL und die endgültigen Veröffentlichungs-URLs von Bildern aus Dynamic Media unterscheiden. Zudem dürfen KEINE Angebote über den Speicherlink der Bilder erstellt werden, da die Bereitstellung in solchen Fällen nicht funktioniert. Stattdessen muss die Bildangebotsfunktionalität verwendet werden. Erläuterungen dazu finden Sie in unserer Hilfedokumentation.

Zur Integration mit Dynamic Media Classic (Scene7) müssen Sie die folgenden Informationen angeben.

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Settings]**.

   ![Scene7-Seite](/help/administrating-target/assets/scene7.png)

1. Geben Sie die folgenden Informationen zum Dynamic Media Classic-Konto an:

   **Region:** Die Region Ihres Dynamic Media-Kontos: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Ort für Inhalt, der außerhalb des Zielordners liegt und manuell in Dynamic Media hochgeladen wird.

   **E-Mail-Adresse:** Die für die Anmeldung bei Dynamic Media Classic (Scene7) verwendete E-Mail-Adresse.

   **Passwort:** Das Passwort für die Anmeldung bei Dynamic Media Classic (Scene7).

1. Klicken Sie auf **[!UICONTROL Senden]**.
