---
description: Target Standard kann in Adobe Scene7 integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek zu ermöglichen.
seo-description: Target Standard kann in Adobe Scene7 integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek zu ermöglichen.
seo-title: Scene7-Einstellungen
solution: Target
subtopic: Erste Schritte
title: Scene7-Einstellungen
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Scene7-Einstellungen{#scene-settings}

Target Standard kann in Adobe Scene7 integriert werden, um Digital Asset Management (DAM) in der Inhaltsbibliothek zu ermöglichen.

>[!NOTE]
>
>Die Integration von Target mit Scene7 ermöglicht die Bereitstellung von Assets (als Teil von Aktivitäten), die in den Asset-Ordner von Adobe Experience Cloud hochgeladen wurden. Diese Integration gibt jedoch keinen Zugriff auf alle Assets, die in Scene7 hochgeladen wurden, um sie in Target-Aktivitäten bereitzustellen.

Wenn Sie über ein Scene7-Konto verfügen, können Sie Ihre Scene7-Anmeldedaten angeben. Wenn Sie nicht über ein Scene7-Konto verfügen, sollten Sie sich an Ihren Adobe-Support-Mitarbeiter wenden, der diese Funktionalität mit einem kostenlosen Scene7-Konto konfigurieren kann, das für Ihr Target-Konto bestimmt ist. Dieses Konto kann für Zwecke verwendet werden, die sich ausschließlich auf Target beschränken. Dieser Service steht Kunden für Workflows zur Verfügung, die eine Bildtauschfunktionalität benötigen.

Wenn diese Einstellung nicht konfiguriert ist, steht die Angebotsoption „Bild austauschen“ im Workflow für die Erstellung der Aktivität nicht zur Verfügung. Nachdem diese Einstellung konfiguriert wurde, steht die Option zum Austauschen/Ändern von Bildangeboten in [Visual Experience Composer (VEC) und im formularbasierten Experience Composer](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) zur Verfügung. Anschließend können Sie die Bildangebote mit Bildern nutzen, die aus Adobe Experience Cloud für die Verwendung in Target-Aktivitäten hochgeladen wurden.

Wenn Sie während der Aktivitätserstellung direkt in einem Angebot oder in benutzerspezifischem Code auf eine URL zu einem öffentlichen Bild verweisen möchten, sollten Sie das Bild auf Ihren eigenen Webservern bereitstellen und Ihre eigene URL im Code verwenden. Es gibt keine Möglichkeit, mithilfe von Adobe Target die veröffentlichte URL eines in Experience Cloud hochgeladenen Bilds abzurufen, um es direkt oder außerhalb der Targeting-Workflows zu verwenden. Diese Funktionalität ist entsprechend dem Vertrag nicht zulässig.

Beachten Sie, dass sich die Speicher-URL und die endgültigen Scene7-Veröffentlichungs-URLs unterscheiden. Zudem dürfen KEINE Angebote über den Speicherlink der Bilder erstellt werden, da die Bereitstellung in solchen Fällen nicht funktioniert. Stattdessen muss die Bildangebotsfunktionalität verwendet werden. Erläuterungen dazu finden Sie in unserer Hilfedokumentation.

Zur Integration in Scene7 müssen Sie einige Scene7-Informationen angeben.

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Scene7-Einstellungen]**.
1. Geben Sie folgende Scene7-Kontoinformationen an:

   **Scene7-Region:** Die Region Ihres Scene7-Kontos: Nordamerika, Europa oder Asien.

   **Scene7-Adhoc-Ordner:** Der Ort für Inhalt, der außerhalb des Zielordners liegt und manuell in Scene7 hochgeladen wird.

   **Scene7-E-Mail-Adresse:** Die für die Anmeldung bei Scene7 verwendete E-Mail-Adresse.

   **Scene7-Passwort:** Das für die Anmeldung bei Scene7 verwendete Passwort.
1. Klicken Sie auf **[!UICONTROL Senden]**.
