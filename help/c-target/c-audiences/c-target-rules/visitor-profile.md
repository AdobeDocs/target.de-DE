---
keywords: Besucherprofil; Target-Besucherprofil
description: Erfahren Sie, wie Sie in [!DNL Adobe Target] Zielgruppen erstellen, um Besucher anzusprechen, die bestimmte Profilparameter wie neue oder wiederkehrende Besucher, Kategorieaffinität und mehr erfüllen.
title: Kann ich Besucher ansprechen, die bestimmte Profilparameter erfüllen?
feature: Zielgruppen
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 47%

---

# Besucherprofil

Erstellen Sie Zielgruppen in [!DNL Adobe Target], um Besucher anzusprechen, die bestimmte Profilparameter erfüllen.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Besucherprofil]** in den Bereich Audience Builder .

1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

   ![](assets/target_visitor_profile.png)

   Die Parameter des Besucherprofils werden über die Mbox (Profil) übergeben. Sie können neue oder zurückkehrende Besucher als Ziel auswählen oder alle Benutzer einschließen.

   * [!UICONTROL Neuer Besucher]
   * [!UICONTROL Wiederkehrender Besucher]
   * [!UICONTROL In anderen Tests]
   * [!UICONTROL Nicht in anderen Tests]
   * [!UICONTROL Erste Seite der Sitzung]
   * [!UICONTROL Nicht die erste Seite der Sitzung]
   * [!UICONTROL Kategorieaffinität]

   Für jeden Mbox-Aufruf mit neuem `mboxPC`-Wert wird ein Besucherprofil im lokalen Edge-Speicher erstellt. Nach 30 Minuten Inaktivität wird das Profil in der [!DNL Target]-Datenbank gespeichert und kann von anderen Edges aus aufgerufen werden.

   Wenn sich ein Site-Besucher mitten in einer Sitzung anmeldet und einen `3rdpartyId` erhält, sind alle zuvor geladenen Profilattribute, die mit `3rdPartyId` verknüpft sind, sofort verfügbar.

   Sie können benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Wählen Sie den Parameter aus, den Sie für das Targeting Ihrer Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Schulungsvideo: Erstellen von Zielgruppen ![Badge &quot;Überblick&quot;](/help/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
