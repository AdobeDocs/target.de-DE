---
keywords: Inhalt;Assets;Inhalt verwalten;Angebote;Assets verwalten;Auswahlmodus aufrufen;Auswahlmodus
description: Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der Angebotsbibliothek in Adobe Target verwalten.
title: Wie verwalte ich Code- und Bildangebote?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: f93e33e91fb7be9c0d1772a2014864b46c1dfe47
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 16%

---

# Angebote

Verwenden Sie die Bibliothek [!UICONTROL Offers] in [!DNL Adobe Target], um Ihren Code- und Bildangebotsinhalt zu verwalten.

1. Klicken Sie auf **[!UICONTROL Offers]** , um die Bibliothek zu öffnen.

   Die Bibliothek enthält die Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs erstellt wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

   Die Seite [!UICONTROL Offers] enthält zwei Registerkarten rechts: [!UICONTROL Code Offers] und [!UICONTROL Image Offers] , mit denen Sie Angebote nach Typ anzeigen können.

   ![Seite &quot;Angebote&quot;mit den Registerkarten &quot;Code-Angebote&quot;und &quot;Bildangebote&quot;](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Optional) Klicken Sie auf die Dropdownliste &quot;**[!UICONTROL Type]**&quot;, um Angebote nach Typ zu filtern (HTML-Angebot, [Erlebnisfragmente](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md) und [Ordner](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![offer_filter image](assets/offers_filter.png)

1. (Optional) Klicken Sie auf die Dropdownliste **[!UICONTROL Source]** , um Angebote nach Quelle (Adobe Target, Adobe Target Classic und Adobe Experience Manager) zu filtern.

1. (Optional) Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Angebot oder den gewünschten Ordner auf der Registerkarte [!UICONTROL Code Offers] bewegen und dann auf das gewünschte Symbol klicken.

   ![Optionen für Code-Angebote](assets/offer-picker-large.png)

   Zu den Optionen zählen:

   * Ansicht (Weitere Informationen finden Sie unten unter [Anzeigen von Angebotsdefinitionen](#section_6B059DD121434E6292CAB393507D010E).)
   * Bearbeiten 
   * Kopieren 
   * Verschieben (Um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf das Symbol **[!UICONTROL Move]** für das gewünschte Element, klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Drop]**.)
   * Löschen

   Je nach Ihren Berechtigungen werden möglicherweise keine Symbole für alle Optionen angezeigt. Beispielsweise verfügt ein Benutzer mit [!UICONTROL Observer] -Berechtigungen nicht über die Rechte zur Verwendung der [!UICONTROL Copy] -Option.

   Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Optional) Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den Ordner auf der Registerkarte [!UICONTROL Image Offers] bewegen und dann auf das gewünschte Symbol klicken.

   ![Optionen für Bildangebote](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Zu den Optionen zählen:

   * Auswählen
   * Download 
   * Eigenschaften anzeigen
   * Bearbeiten 
   * Anmerkungen hinzufügen
   * Kopieren 

   Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

   >[!NOTE]
   >
   >Bildangebote sind nicht Teil des Modells [Berechtigungen für Unternehmensbenutzer](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).


## Angebotsdefinitionen anzeigen {#section_6B059DD121434E6292CAB393507D010E}

Sie können Details zur Angebotsdefinition auf einer Pop-up-Karte in der Bibliothek [!UICONTROL Offers] anzeigen, ohne das Angebot zu öffnen.

Beispielsweise kann auf die folgende Angebotsdefinitionskarte für ein HTML-Angebot durch Klicken auf das Informationssymbol zugegriffen werden:

![offer-card-html image](assets/offer-card-html-new.png)

Die folgenden Informationen sind verfügbar:

* Name
* Angebots-ID
* Typ
* Zuletzt geändert

Klicken Sie auf den Link [!UICONTROL View Full Details] , um den Angebotsinhalt und die Aktivitäten anzuzeigen, die auf ein Codeangebot verweisen. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Zu den Informationen gehören [!UICONTROL Live Activities] und [!UICONTROL Inactive Activities].

Die verfügbaren Informationen auf jeder Karte variieren je nach Angebotstyp: HTML-Angebot, [Erlebnisfragmente](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md) oder [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Die Funktion für Angebotsdetails gilt nicht für Bildangebote.

<!--

## Training video: The Content Repository ![Overview badge](/help/main/assets/overview.png)

This video includes information about managing offers.

* Connection between the [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) and the Target Content Library 
* Custom HTML Offers 
* Custom HTML Offer in the [!UICONTROL Visual Experience Composer]

>[!VIDEO](https://video.tv.adobe.com/v/17387)

-->
