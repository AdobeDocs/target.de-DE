---
keywords: Besucherprofil; Target-Besucherprofil
description: Erfahren Sie, wie Sie Zielgruppen in erstellen [!DNL Adobe Target]  um Besuchende anzusprechen, die bestimmte Profilparameter erfüllen, z. B. neue oder wiederkehrende Besuchende, Kategorieaffinität und mehr.
title: Kann ich Besuchende ansprechen, die bestimmte Profilparameter erfüllen?
feature: Audiences
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 35%

---

# Besucherprofil

Erstellen Sie Zielgruppen in [!DNL Adobe Target] , um Besuchende anzusprechen, die bestimmte Profilparameter erfüllen.

1. Klicken Sie in der [!DNL Target] auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Visitor Profile]** per Drag-and-Drop in den Bereich Audience Builder .

1. Klicken Sie auf **[!UICONTROL Select]** und wählen Sie dann eine der folgenden Optionen aus:

   ![target_visitor_profile Bild](assets/target_visitor_profile.png)

   Die Parameter des Besucherprofils werden über die Mbox (Profil) übergeben. Sie können neue oder zurückkehrende Besucher als Ziel auswählen oder alle Benutzer einschließen.

   * [!UICONTROL New Visitor]
   * [!UICONTROL Returning Visitor]
   * [!UICONTROL In Other Tests]
   * [!UICONTROL Not In Other Tests]
   * [!UICONTROL First Page of Session]
   * [!UICONTROL Not First Page of Session]
   * [!UICONTROL Category Affinity]

   Für jeden Mbox-Aufruf mit neuem `mboxPC`-Wert wird ein Besucherprofil im lokalen Edge-Speicher erstellt. Nach 30 Minuten Inaktivität wird das Profil in der [!DNL Target]-Datenbank gespeichert und kann von anderen Edges aus aufgerufen werden.

   Wenn sich ein Site-Besucher während der Sitzung anmeldet und eine `3rdpartyId` erhält, sind alle zuvor geladenen Profilattribute, die mit der `3rdPartyId` verknüpft sind, sofort verfügbar.

   Sie können benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Wählen Sie den Parameter aus, den Sie für das Targeting Ihrer Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Done]**.

## Schulungsvideo: Erstellen von Zielgruppen ![Übersichts-Badge](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
