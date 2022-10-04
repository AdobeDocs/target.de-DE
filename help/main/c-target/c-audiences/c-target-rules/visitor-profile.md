---
keywords: Besucherprofil; Target-Besucherprofil
description: Erfahren Sie, wie Sie Zielgruppen erstellen in [!DNL Adobe Target] , um Besucher anzusprechen, die bestimmte Profilparameter erfüllen, wie z. B. neue oder wiederkehrende Besucher, Kategorieaffinität und mehr.
title: Kann ich Besucher ansprechen, die bestimmte Profilparameter erfüllen?
feature: Audiences
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 46%

---

# Besucherprofil

Erstellen von Zielgruppen in [!DNL Adobe Target] , um Besucher anzusprechen, die bestimmte Profilparameter erfüllen.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Drag &amp; Drop **[!UICONTROL Besucherprofil]** in den Audience Builder-Bereich.

1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

   ![target_visitor_profile image](assets/target_visitor_profile.png)

   Die Parameter des Besucherprofils werden über die Mbox (Profil) übergeben. Sie können neue oder zurückkehrende Besucher als Ziel auswählen oder alle Benutzer einschließen.

   * [!UICONTROL Neuer Besucher]
   * [!UICONTROL Wiederkehrender Besucher]
   * [!UICONTROL In anderen Tests]
   * [!UICONTROL Nicht in anderen Tests]
   * [!UICONTROL Erste Seite der Sitzung]
   * [!UICONTROL Nicht die erste Seite der Sitzung]
   * [!UICONTROL Kategorieaffinität]

   Für jeden Mbox-Aufruf mit neuem `mboxPC`-Wert wird ein Besucherprofil im lokalen Edge-Speicher erstellt. Nach 30 Minuten Inaktivität wird das Profil im [!DNL Target] Datenbank und ist von anderen Edges aus zugänglich.

   Wenn sich ein Besucher der Site mitten in einer Sitzung anmeldet und eine `3rdpartyId`, alle zuvor geladenen Profilattribute, die mit dem `3rdPartyId` sofort verfügbar sind.

   Sie können benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Wählen Sie den Parameter aus, den Sie für das Targeting Ihrer Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Schulungsvideo: Erstellen von Zielgruppen ![Übersichtszeichen](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
