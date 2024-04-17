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

Verwenden Sie die [!UICONTROL Offers] Bibliothek in [!DNL Adobe Target] zur Verwaltung Ihres Code- und Bildangebots.

1. Klicks **[!UICONTROL Offers]** , um die Bibliothek zu öffnen.

   Die Bibliothek enthält die Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs erstellt wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

   Die [!UICONTROL Offers] Die Seite enthält zwei Registerkarten rechts: [!UICONTROL Code Offers] und [!UICONTROL Image Offers] die es Ihnen ermöglicht, Angebote nach Typ anzuzeigen.

   ![Angebotsseite mit den Registerkarten Code-Angebote und Bildangebote](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Optional) Klicken Sie auf die **[!UICONTROL Type]** Dropdown-Liste zum Filtern von Angeboten nach Typ (HTML-Angebot, [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md), und [Ordner](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![offer_filter-Bild](assets/offers_filter.png)

1. (Optional) Klicken Sie auf die **[!UICONTROL Source]** Dropdownliste zum Filtern von Angeboten nach Quelle (Adobe Target, Adobe Target Classic und Adobe Experience Manager).

1. (Optional) Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Angebot oder den Ordner auf der [!UICONTROL Code Offers] und klicken Sie dann auf das gewünschte Symbol.

   ![Optionen für Code-Angebote](assets/offer-picker-large.png)

   Zu den Optionen zählen:

   * Anzeigen (weitere Informationen finden Sie unter [Angebotsdefinitionen anzeigen](#section_6B059DD121434E6292CAB393507D010E) unten.)
   * Bearbeiten 
   * Kopieren 
   * Verschieben (um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf die **[!UICONTROL Move]** für das gewünschte Element klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Drop]**.
   * Löschen

   Je nach Ihren Berechtigungen werden möglicherweise keine Symbole für alle Optionen angezeigt. Beispiel: ein Benutzer mit [!UICONTROL Observer] -Berechtigungen verfügen nicht über die Rechte zur Verwendung der [!UICONTROL Copy] -Option.

   Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Optional) Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den Ordner auf der [!UICONTROL Image Offers] und klicken Sie dann auf das gewünschte Symbol.

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
   >Bildangebote sind nicht Teil der [Berechtigungen für Unternehmensbenutzer](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) -Modell.


## Angebotsdefinitionen anzeigen {#section_6B059DD121434E6292CAB393507D010E}

Sie können Details zur Angebotsdefinition auf einer Popup-Karte im [!UICONTROL Offers] -Bibliothek, ohne das Angebot zu öffnen.

Beispielsweise kann auf die folgende Angebotsdefinitionskarte für ein HTML-Angebot durch Klicken auf das Informationssymbol zugegriffen werden:

![offer-card-html image](assets/offer-card-html-new.png)

Die folgenden Informationen sind verfügbar:

* Name
* Angebots-ID
* Typ
* Zuletzt geändert

Klicken Sie auf [!UICONTROL View Full Details] -Link, um den Angebotsinhalt und die Aktivitäten anzuzeigen, die auf ein Codeangebot verweisen. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Informationen enthalten [!UICONTROL Live Activities] und [!UICONTROL Inactive Activities].

Die verfügbaren Informationen auf den einzelnen Karten variieren je nach Angebotstyp: HTML-Angebot, [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md)oder [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Die Funktion für Angebotsdetails gilt nicht für Bildangebote.

<!--

## Training video: The Content Repository ![Overview badge](/help/main/assets/overview.png)

This video includes information about managing offers.

* Connection between the [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) and the Target Content Library 
* Custom HTML Offers 
* Custom HTML Offer in the [!UICONTROL Visual Experience Composer]

>[!VIDEO](https://video.tv.adobe.com/v/17387)

-->
