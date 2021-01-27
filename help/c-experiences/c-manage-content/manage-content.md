---
keywords: content;assets;manage content;offers;manage assets;enter selection mode;selection mode
description: Wie verwalte ich Code- und Image-Angebot?
title: Angebote
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 70547a05155aa2909b0e66a1f26b0fd2cc730dd9
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 40%

---


# Angebote

Verwenden Sie die Bibliothek [!UICONTROL Angebote] in [!DNL Adobe Target], um Ihr Code-Angebot und Ihren Image-Angebot-Inhalt zu verwalten.

1. Klicken Sie auf **[!UICONTROL Angebote]**, um die Bibliothek zu öffnen.

   Die Bibliothek enthält die Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs erstellt wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

   Die Seite [!UICONTROL Angebot] enthält zwei Registerkarten rechts: [!UICONTROL Code-Angebot] und [!UICONTROL Image-Angebot], mit denen Sie Angebot nach Typ Ansicht haben.

   ![Seite &quot;Angebote&quot;mit den Registerkarten &quot;Code-Angebote&quot;und &quot;Image-Angebot&quot;](/help/c-experiences/c-manage-content/assets/offers-page.png)

1. (Optional) Klicken Sie auf die Dropdown-Liste **[!UICONTROL Typ]**, um Angebot nach Typ zu filtern (HTML-Angebot, [Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md), [Umleitungs-Angebot](/help/c-experiences/c-manage-content/offer-redirect.md)Remote-Angebot](/help/c-experiences/c-manage-content/about-remote-offers.md), [JSON-Angebot](/help/c-experiences/c-manage-content/create-json-offer.md) und [ Ordner](/help/c-experiences/c-manage-content/create-content-folder.md)).[

   ![](assets/offers_filter.png)

1. (Optional) Klicken Sie auf die Dropdown-Liste **[!UICONTROL Quelle]**, um Angebot nach Quelle (Adobe Target, Adobe Target Classic und Adobe Experience Manager) zu filtern.

1. (Optional) Führen Sie weitere Aufgaben durch, indem Sie auf der Registerkarte [!UICONTROL Angebote] den Mauszeiger über das gewünschte Angebot bzw. den gewünschten Ordner halten und anschließend auf das gewünschte Symbol klicken.

   ![Optionen für Code-Angebote](assets/offer-picker-large.png)

   Zu den Optionen zählen:

   * Ansicht (Weitere Informationen finden Sie unter [Anzeigen von Angebot-Definitionen](#section_6B059DD121434E6292CAB393507D010E) unten.)
   * Bearbeiten 
   * Kopieren 
   * Verschieben (Um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf das Symbol **[!UICONTROL Verschieben]** für das gewünschte Element, klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Ablegen]**.)
   * Löschen

   Abhängig von Ihren Berechtigungen werden möglicherweise nicht alle Symbole für alle Optionen angezeigt. Beispielsweise hat ein Benutzer mit den Berechtigungen [!UICONTROL Beobachter] nicht die Rechte, die Option [!UICONTROL Kopieren] zu verwenden.

1. (Optional) Führen Sie weitere Aufgaben durch, indem Sie auf der Registerkarte [!UICONTROL Angebote] den Mauszeiger über das gewünschte Angebot bzw. den Ordner halten und anschließend auf das gewünschte Symbol klicken.

   ![Optionen für Bildangebote](/help/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Zu den Optionen zählen:

   * Select
   * Download 
   * Eigenschaften anzeigen
   * Bearbeiten 
   * Anmerkungen hinzufügen
   * Kopieren 

## Anzeigen von Angebot-Definitionen {#section_6B059DD121434E6292CAB393507D010E}

Sie können Angebot-Definitionsdetails auf einer Popupkarte in der [!UICONTROL Angebots]-Bibliothek Ansicht haben, ohne das Angebot zu öffnen.

Beispielsweise wird auf die folgende Angebot-Definitionskarte für ein HTML-Angebot zugegriffen, indem Sie den Mauszeiger über ein Angebot in der Liste [!UICONTROL Content] bewegen und dann auf das Informationssymbol klicken:

![](assets/offer-card-html.png)

Die folgenden Informationen sind verfügbar:

* Name
* Quelle
* Typ
* Angebots-ID
* Angebotspfad
* Zuletzt geändert

Klicken Sie auf die Registerkarte [!UICONTROL Angebotsnutzung], um die Aktivitäten anzuzeigen, die sich auf ein Codeangebot in der Pop-up-Karte der jeweiligen Angebotsdefinition beziehen. Diese Funktionalität gilt nicht für Bildangebote. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Zu den Informationen gehören [!UICONTROL Live-Aktivitäten] und [!UICONTROL Inaktive Aktivitäten].

![](assets/offer-card-usage.png)

Die folgende Angebotsdefinitionskarte für ein Umleitungsangebot:

![](assets/offer-card-redirect.png)

Die folgenden Informationen sind verfügbar:

* Name
* Quelle
* Typ
* Angebots-ID
* Angebotspfad
* Zuletzt geändert
* Umleitungs-URL
* Alle URL-Parameter einschließen (Ein oder Aus)
* Sitzungs-ID der Mbox weitergeben (Ein oder Aus)

Die folgende Angebotsdefinitionskarte für ein Remoteangebot:

![](assets/offer-card-remote.png)

Die folgenden Informationen sind verfügbar:

* Name
* Quelle
* Typ
* Angebots-ID
* Angebotspfad
* Zuletzt geändert
* Umleitungs-URL-Typ
* Absolute oder relative URL

## Schulungsvideo: Das Content-Repository  ![Übersichtskennzeichnung](/help/assets/overview.png)

In diesem Video wird beschrieben, wie Angebote verwaltet werden.

* Zusammenhang zwischen der [Experience Cloud-Asset-Bibliothek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) und der Target-Inhaltsbibliothek
* Benutzerdefinierte HTML-Angebote
* Benutzerdefinierte HTML-Angebote im Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)