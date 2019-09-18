---
description: 'Target kann mithilfe von Adobe Pulse Benachrichtigungen mit anderen Adobe Experience Cloud-Lösungen austauschen. Target sendet zwei Arten von Benachrichtigungen für alle Aktivitätstypen: eine bei Liveschaltung der Aktivität und eine bei ihrer Deaktivierung.'
keywords: Benachrichtigungen
seo-description: 'Target kann mithilfe von Adobe Pulse Benachrichtigungen mit anderen Adobe Experience Cloud-Lösungen austauschen. Target sendet zwei Arten von Benachrichtigungen für alle Aktivitätstypen: eine bei Liveschaltung der Aktivität und eine bei ihrer Deaktivierung.'
seo-title: Aktivitätsbenachrichtigungen
solution: Target
title: Aktivitätsbenachrichtigungen
topic: Standard
uuid: eb9b8657-1c8e-4eba-8f6d-612944f917f3
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Aktivitätsbenachrichtigungen{#activity-notifications}

Target kann mithilfe von Adobe Pulse Benachrichtigungen mit anderen Adobe Experience Cloud-Lösungen austauschen. Target sendet zwei Arten von Benachrichtigungen für alle Aktivitätstypen: eine bei Liveschaltung der Aktivität und eine bei ihrer Deaktivierung.

Benachrichtigungen von [!DNL Target] können in allen Lösungen von Benutzern gelesen werden, die in einer [!DNL Experience Cloud]-Produktumgebung mit [!DNL Target Standard/Premium] arbeiten.

For information about setting up Notifications, see [Enable notifications](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/getting-started-experience-cloud.html#concept_0105453AD71847B8BFCAF4A40915F157) in the [!DNL Adobe Experience Cloud] documentation.

Auf Benachrichtigungen in [!DNL Target] können Sie überall zugreifen, mit Ausnahme des Erstellungsarbeitsablaufs für Aktivitäten. Klicken Sie auf das Glockensymbol in der Überschrift der Seite, um das Benachrichtigungswidget ein- oder auszublenden.

![Benachrichtigungssymbol](assets/notifications-shell.png)

[!DNL Target] sendet für sämtliche Aktivitätstypen zwei Arten von Benachrichtigungen:

* Wenn eine Aktivität verfügbar wird und die Bereitstellung des Angebots beginnt

   Beispiel:

   ![](assets/notif_app.png)

* Wenn eine Aktivität deaktiviert wird und das Angebot nicht mehr verfügbar ist

   Beispiel:

   ![](assets/notif-deact.png)

Ähnliche Benachrichtigungen erscheinen auch dann, wenn eine geplante Aktivität ihr Startdatum erreicht oder beim Erreichen ihres Enddatums beendet wird.

Alle [!DNL Target]-Benachrichtigungen enthalten zur einfachen Erkennung den Namen der Aktivität, die genehmigt oder deaktiviert wurde, und die Wörter „Adobe Target“.

Wenn eine einzelne Aktivität mehrere Benachrichtigungen desselben Typs sendet, werden diese zu einer Karte zusammengefasst und die Anzahl an Benachrichtigungen darauf angezeigt. Beispiel:

![](assets/notif-multi.png)

Klicken Sie auf die Benachrichtigungskarte, um sich Einzelheiten zu den einzelnen Benachrichtigungen anzeigen zu lassen.

Wenn Sie zum Beispiel auf die Karten oben klicken, erscheinen diese drei Benachrichtigungen:

![](assets/notif-multi-open.png)

## Einschränkungen {#section_B466EB20B2554CE7B1915374B39F4322}

* Benachrichtigungen enthalten keine Informationen darüber, wer die Aktivität genehmigt, deaktiviert oder importiert hat.
* MVT-Benachrichtigungen erscheinen als „A/B-Test“, da sie in [!DNL Target Classic] als A/B-Kampagnen synchronisiert werden.

