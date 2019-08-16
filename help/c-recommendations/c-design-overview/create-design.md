---
description: Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden.
keywords: Empfehlungsentwurf; Entwurf erstellen; Entwurf kopieren
seo-description: Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden.
seo-title: Erstellen eines Designs
solution: Target
title: Erstellen eines Designs
title-outputclass: premium
topic: Premium
uuid: 812258e0-8d28-4ef3-b745-45ed694fcabe
badge: premium
translation-type: tm+mt
source-git-commit: 0466b6d5cf6804ec3a26716a9ade35fe5678bcb6

---


# ![PREMIUM](/help/assets/premium.png) Erstellen eines Designs{#create-a-design}

Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden.

Sie können einen [!UICONTROL Recommendations]-Entwurf erstellen, indem ein Standardentwurf oder ein benutzerdefinierter Entwurf verwendet wird. Im Bildschirm **[!UICONTROL Recommendations &gt; Entwürfe]** werden sowohl Standardentwurfskarten als auch von Ihnen erstellte Entwürfe angezeigt. Die Standardentwürfe können nicht bearbeitet oder gelöscht werden.

1. Bewegen Sie den Mauszeiger auf dem Bildschirm **[!UICONTROL Empfehlungen &gt; Entwürfe]** über die Karte für den Entwurf, den Sie erstellen möchten.

   ![](assets/Card_CopyDesign.png)

1. Um einen vorhandenen Entwurf zu kopieren und zu bearbeiten, klicken Sie auf das Symbol **[!UICONTROL Kopieren]**.

   Oder

   Möchten Sie einen benutzerdefinierten Entwurf erstellen, klicken Sie auf die Option **[!UICONTROL Entwurf erstellen]**, verfügbar im Bildschirm **Recommendations &gt; Entwurf[!UICONTROL .]**

   ![](assets/createDesign.png)

1. Fügen Sie einen **[!UICONTROL Inhaltsnamen]** hinzu.

   Verwenden Sie einen Standardentwurf, lautet dessen Name „Kopie“. Dieser Name erscheint im Feld **[!UICONTROL Inhaltsname]**. Sie können den Namen bearbeiten. 1. (Optional) Wählen Sie per Klick ein Bild aus, das auf der Entwurfskarte angezeigt werden soll.
1. Bearbeiten Sie den Entwurfs-**[!UICONTROL Code]**.

   Empfehlungsentwürfe verwenden die Open Source-Entwurfssprache Velocity. Informationen über Velocity finden Sie unter [](https://velocity.apache.org)https://velocity.apache.org.

   Der Entwurf kann ein HTML- oder ein Nicht-HTML-Entwurf sein. Standardmäßig werden HTML-Entwürfe mit einem <div> Tag umschlossen, um Clicktracking in einer Webumgebung zuzulassen. Nicht-HTML-Entwürfe eignen sich für Nicht-Webumgebungen, in denen ein Klick-Tracking nicht möglich ist.

   >[!NOTE]
   >
   >Die maximale Anzahl von Entitäten, die in einem Entwurf referenziert werden können, egal ob hardcodiert oder in Schleife, beträgt 99.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Schulungsvideo: Benutzerdefinierte Designs in Recommendations erstellen (3:20)

Dieses Video enthält die folgenden Informationen:

* Erstellen eines benutzerdefinierten Entwurfs
* Verstehen Sie, wie Sie auf Anzeigevariablen in Ihren Designs verweisen.

>[!VIDEO](https://video.tv.adobe.com/v/27687?captions=ger)
