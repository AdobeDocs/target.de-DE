---
description: Target Standard kann in Adobe Dynamic Media Classic (früher Scene 7) integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
seo-description: Target Standard kann in Adobe Dynamic Media Classic (früher Scene 7) integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.
seo-title: Integration von Dynamic Media Classic
solution: Target
subtopic: Erste Schritte
title: Integration von Dynamic Media Classic
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: c6a59843c80017e6f072f65ffad822fe198ebb55

---


# Dynamic Media Classic integration{#scene-settings}

Target Standard kann in Adobe Dynamic Media Classic (früher Scene 7) integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek bereitzustellen.

>[!NOTE]
>
>Die Integration von Target mit Dynamic Media Classic ermöglicht die Bereitstellung von Assets (als Teil von Aktivitäten), die in den Adobe Experience Cloud-Asset-Ordner hochgeladen wurden. Diese Integration ermöglicht keinen Zugriff auf alle Assets, die in Dynamic Media Classic hochgeladen wurden, um die Bereitstellung in Target-Aktivitäten durchzuführen.

Wenn Sie bereits über ein Konto für dynamische Medien verfügen, können Sie Ihre vorhandenen Anmeldedaten bereitstellen. Wenn Sie kein Konto haben, können Sie ein dynamisches Media Media Classic-Konto ohne zusätzliche Gebühren von Ihrem Adobe-Vertreter abfordern. Dieses Konto kann für Zwecke verwendet werden, die sich ausschließlich auf Target beschränken. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

Wenn diese Einstellung nicht konfiguriert ist, steht die Angebotsoption „Bild austauschen“ im Workflow für die Erstellung der Aktivität nicht zur Verfügung. Nachdem diese Einstellung konfiguriert wurde, steht die Option zum Austauschen/Ändern von Bildangeboten in [Visual Experience Composer (VEC) und im formularbasierten Experience Composer](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) zur Verfügung. Anschließend können Sie die Bildangebote mit Bildern nutzen, die aus Adobe Experience Cloud für die Verwendung in Target-Aktivitäten hochgeladen wurden.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, mithilfe von Adobe Target die veröffentlichte URL eines in Experience Cloud hochgeladenen Bilds abzurufen, um es direkt oder außerhalb der Targeting-Workflows zu verwenden. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass die Speicher-URL und die endgültigen Veröffentlichungs-urls von Bildern von dynamischen Medien unterschiedlich sind und eine KEINE Angebote mithilfe des Speicherlinks von Bildern erstellt werden kann, wenn die Bereitstellung in diesen Fällen nicht funktioniert. Stattdessen muss die Bildangebotsfunktionalität verwendet werden. Erläuterungen dazu finden Sie in unserer Hilfedokumentation.

Zur Integration mit Dynamic Media Classic (Scene 7) müssen Sie einige der folgenden Informationen angeben.

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Scene7-Einstellungen]**.
1. Geben Sie die folgenden dynamischen Media Classic-Kontoinformationen an:

   **Region:** Die Region für Ihr dynamisches Medienkonto: Nordamerika, Europa oder Asien.

   **Adhoc-Ordner:** Der Speicherort für Inhalte, die sich außerhalb des Zielordners befinden und manuell in dynamische Medien hochgeladen werden.

   **E-Mail-Adresse:** Die E-Email-Adresse, die für die Anmeldung bei Dynamic Media Classic (Scene 7) verwendet wird.

   **Kennwort:** Das Kennwort für die Anmeldung bei Dynamic Media Classic (Scene 7).
1. Klicken Sie auf **[!UICONTROL Senden]**.
