---
keywords: Besucherprofil; Target-Besucherprofil
description: Erfahren Sie, wie Sie Audiencen in Adobe [!DNL Target] zu Zielgruppe-Besuchern erstellen, die bestimmte Profil-Parameter erfüllen, wie neue oder wiederkehrende Besucher, Kategorie-Affinität und mehr.
title: Kann ich [!DNL Target] Besucher, die bestimmte Profil-Parameter erfüllen?
feature: Zielgruppen
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 83%

---

# Besucherprofil

Erstellen Sie Zielgruppen aus Besuchern, die bestimmte Profilparameter erfüllen.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Nennen Sie die Zielgruppe.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** > **[!UICONTROL Besucherprofil]**.

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

## Schulungsvideo: Erstellen von Audiencen ![Kennzeichen ](/help/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
