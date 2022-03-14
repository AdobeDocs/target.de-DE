---
keywords: Inhalt;Assets;Inhalt verwalten;Angebote;Assets verwalten;Auswahlmodus aufrufen;Auswahlmodus
description: Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der Angebotsbibliothek in Adobe Target verwalten.
title: Wie verwalte ich Code- und Bildangebote?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 37%

---

# Angebote

Verwenden Sie die [!UICONTROL Angebote] Bibliothek in [!DNL Adobe Target] zur Verwaltung Ihres Code- und Bildangebots.

1. Klicken Sie auf **[!UICONTROL Angebote]**, um die Bibliothek zu öffnen.

   Die Bibliothek enthält die Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs erstellt wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

   Die [!UICONTROL Angebote] Die Seite enthält zwei Registerkarten rechts: [!UICONTROL Code-Angebote] und [!UICONTROL Bildangebote] die es Ihnen ermöglicht, Angebote nach Typ anzuzeigen.

   ![Angebotsseite mit den Registerkarten Code-Angebote und Bildangebote](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Optional) Klicken Sie auf die **[!UICONTROL Typ]** Dropdown-Liste zum Filtern von Angeboten nach Typ (HTML-Angebot, [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md)und [Ordner](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![](assets/offers_filter.png)

1. (Optional) Klicken Sie auf die **[!UICONTROL Quelle]** Dropdownliste zum Filtern von Angeboten nach Quelle (Adobe Target, Adobe Target Classic und Adobe Experience Manager).

1. (Optional) Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Angebot oder den Ordner auf der [!UICONTROL Code-Angebote] und klicken Sie dann auf das gewünschte Symbol.

   ![Optionen für Code-Angebote](assets/offer-picker-large.png)

   Zu den Optionen zählen:

   * Anzeigen (weitere Informationen finden Sie unter [Angebotsdefinitionen anzeigen](#section_6B059DD121434E6292CAB393507D010E) unten.)
   * Bearbeiten 
   * Kopieren 
   * Verschieben (um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf die **[!UICONTROL Verschieben]** für das gewünschte Element klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Drop]**.
   * Löschen

   Je nach Ihren Berechtigungen werden möglicherweise keine Symbole für alle Optionen angezeigt. Beispiel: ein Benutzer mit [!UICONTROL Beobachter] -Berechtigungen verfügen nicht über die Rechte zur Verwendung der [!UICONTROL Kopieren] -Option.

   Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Optional) Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den Ordner auf der [!UICONTROL Bildangebote] und klicken Sie dann auf das gewünschte Symbol.

   ![Optionen für Bildangebote](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

   Zu den Optionen zählen:

   * Select
   * Download 
   * Eigenschaften anzeigen
   * Bearbeiten 
   * Anmerkungen hinzufügen
   * Kopieren 

   Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

## Angebotsdefinitionen anzeigen {#section_6B059DD121434E6292CAB393507D010E}

Sie können Details zur Angebotsdefinition auf einer Pop-up-Karte im [!UICONTROL Angebote] -Bibliothek, ohne das Angebot zu öffnen.

Beispielsweise wird auf die folgende Angebotsdefinitionskarte für ein HTML-Angebot zugegriffen, indem Sie den Mauszeiger über ein Angebot auf der Seite [!UICONTROL Inhalt] und klicken Sie auf das Informationssymbol:

![](assets/offer-card-html.png)

Die folgenden Informationen sind verfügbar:

* Name
* Quelle
* Typ
* Angebots-ID
* Angebotspfad
* Zuletzt geändert

Klicken Sie auf die Registerkarte [!UICONTROL Angebotsnutzung], um die Aktivitäten anzuzeigen, die sich auf ein Codeangebot in der Pop-up-Karte der jeweiligen Angebotsdefinition beziehen. Diese Funktionalität gilt nicht für Bildangebote. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Informationen enthalten [!UICONTROL Live-Aktivitäten] und [!UICONTROL Inaktive Aktivitäten].

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
* Übergeben der mbox-Sitzungs-ID (ein oder aus)

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

## Schulungsvideo: Das Content-Repository ![Übersichtszeichen](/help/main/assets/overview.png)

In diesem Video wird beschrieben, wie Angebote verwaltet werden.

* Zusammenhang zwischen der [Experience Cloud-Asset-Bibliothek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) und der Target-Inhaltsbibliothek
* Benutzerdefinierte HTML-Angebote
* Benutzerdefinierte HTML-Angebote im Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)
