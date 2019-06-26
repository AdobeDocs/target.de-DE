---
description: Erstellen Sie Zielgruppen, um Besucher als Ziel auszuwählen, die bestimmte Profilparameter erfüllen.
keywords: Besucherprofil; Target-Besucherprofil
seo-description: Erstellen Sie Zielgruppen in Adobe Target, um Besucher als Ziel auszuwählen, die bestimmte Profilparameter erfüllen.
seo-title: Besucherprofil
solution: Target
title: Zielgruppen erstellen, um Besucherprofile mit Adobe Target als Ziel auszuwählen
topic: Premium
uuid: 462c80f4-bd5f-4dce-b02b-21b2c33c5bf6
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Besucherprofil{#visitor-profile}

Erstellen Sie Zielgruppen, um Besucher als Ziel auszuwählen, die bestimmte Profilparameter erfüllen.

1. Klicken Sie auf der [!DNL Target]-Benutzeroberfläche auf **[!UICONTROL Zielgruppen]** &gt; **[!UICONTROL Zielgruppe erstellen]**.
1. Nennen Sie die Zielgruppe.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** &gt; **[!UICONTROL Besucherprofil]**.

   ![](assets/target_visitor_profile.png)

1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

   Die Parameter des Besucherprofils werden über die Mbox (Profil) übergeben. Sie können neue oder zurückkehrende Besucher als Ziel auswählen oder alle Benutzer einschließen.

   * Neuer Besucher
   * Wiederkehrender Besucher
   * In anderen Tests
   * Nicht in anderen Tests
   * Erste Seite der Sitzung
   * Nicht die erste Seite der Sitzung
   * Kategorieaffinität
   Für jeden Mbox-Aufruf mit neuem `mboxPC`-Wert wird ein Besucherprofil im lokalen Edge-Speicher erstellt. Nach 30 Minuten Inaktivität wird das Profil in der Target-Datenbank gespeichert und ist für andere Edges zugänglich.

   Wenn sich ein Besucher der Site mitten in einer Sitzung anmeldet und die Kennung `3rdpartyId` erhält, sind alle vorher geladenen Profilattribute, die mit `3rdPartyId` verknüpft sind, sofort verfügbar.

   Sie können benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Wählen Sie den Parameter aus, den Sie für das Targeting Ihrer Aktivität verwenden möchten. Wird der gewünschte Parameter nicht angezeigt, wurde er nicht von einer Mbox ausgelöst.

1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und legen Sie zusätzliche Regeln für die Zielgruppe fest.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392?captions=ger)
