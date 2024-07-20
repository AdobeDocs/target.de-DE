---
keywords: Inhalt;Assets;Inhalt verwalten;Angebote;Assets verwalten;Auswahlmodus aufrufen;Auswahlmodus
description: Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der Angebotsbibliothek verwalten.
title: Wie verwalte ich Code- und Bildangebote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 5d14dfd700cb1cec0fa62f66da1400bc8d7fd109
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 17%

---

# Angebote

Verwenden Sie die Bibliothek [!UICONTROL Offers] in [!DNL Adobe Target], um den Code und den Inhalt Ihres Bildangebots zu verwalten.

>[!NOTE]
>
>Dieser Artikel enthält Informationen zu Aktualisierungen der [!DNL Target] -Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Das [!DNL Adobe Target]-Team ermöglicht für ausgewählte Kunden oft neue Funktionen zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen in zukünftigen [!DNL Target Standard/Premium]-Versionen für alle Kunden aktiviert und in den Versionshinweisen angekündigt.

Klicken Sie auf die Registerkarte **[!UICONTROL Offers]** oben in der Benutzeroberfläche von [!DNL Target] , um die Bibliothek [!UICONTROL Offers] anzuzeigen.

![Angebotsbibliothek in Adobe Target](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

Die Bibliothek [!UICONTROL Offers] enthält Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs eingerichtet wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

Die Angebotsbibliothek bietet einen Überblick über alle Code- und Bildangebote und ermöglicht Ihnen die Durchführung verschiedener Aktionen:

| Element | Beschreibung |
|--- |--- |
| Linke Navigationsleiste | Zwischen der Auflistung [!UICONTROL Code Offers] oder [!UICONTROL Image Offers] wechseln. |
| Symbol [!UICONTROL Show filters]<P>![Symbol &quot;Filter anzeigen&quot;](/help/main/c-activities/assets/show-filters-icon.png) | Klicken Sie auf das Symbol **[!UICONTROL Show filters]** , um Angebote nach [!UICONTROL Type], [!UICONTROL Source] und [!UICONTROL AEM Type] zu filtern.<P>Weitere Informationen finden Sie unter [Anwenden von Filtern auf die Angebotsliste](#filters) weiter unten. |
| Suchfelder | Verwenden Sie die Felder **[!UICONTROL Search in]** , um schnell ein Angebot zu finden oder die Anzahl der in der Bibliothek [!UICONTROL Offers] angezeigten Angebote zu reduzieren. Sie können nach [!UICONTROL Offer Name], [!UICONTROL AEM Paths] oder [!UICONTROL AEM Tags] suchen. |
| [!UICONTROL Create Folder] | Klicken Sie auf Ordner erstellen , um Ordner in der Bibliothek [!UICONTROL Offer] zu erstellen und Codeangebote, Bildangebote sowie andere Ordner zu speichern, um eine Unterordnerstruktur zu erstellen. Weitere Informationen finden Sie unter [Erstellen von Angebotsordnern](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Erstellen Sie ein Angebot. Weitere Informationen zur Erstellung der verschiedenen Angebotstypen finden Sie unter: <ul><li>HTML-Angebot</li><li>[JSON-Angebot](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Kontrollkästchen für Massenvorgänge | Führen Sie Massenvorgänge für alle Aktivitäten oder für ausgewählte Aktivitäten durch.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Angebotsstatus) finden Sie unten unter [Durchführen von Schnellaktionen](#quick-actions) . |
| [!UICONTROL Name] | Der Name jedes Angebots.<P>Klicken Sie auf das Symbol &quot;**[!UICONTROL Quick Info]**&quot;neben dem jeweiligen Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Pop-up-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums, an dem das Angebot zuletzt geändert wurde und von wem und mehr.<p>Klicken Sie auf das Symbol &quot;**[!UICONTROL More actions]**&quot;(die horizontalen Auslassungspunkte) neben dem jeweiligen Angebotsnamen, um ein Menü zu öffnen, über das Sie für eine Aktivität Schnellaktionen durchführen können. Die folgenden Aktionen sind verfügbar (je nach Ihren Berechtigungen und dem Angebotsstatus): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] und [!UICONTROL Move]. Weitere Informationen zu den einzelnen Aktionen finden Sie unten unter [Schnellaktionen durchführen](#quick-actions) .<P>Klicken Sie auf die Tabellenüberschrift, um die Liste alphabetisch in auf- oder absteigender Reihenfolge nach Namen zu sortieren. |
| [!UICONTROL Type] | Der Angebotstyp: HTML-Angebote, [Umleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebote](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Zeigt an, wo das Angebot erstellt wurde: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager]. |

## Anwenden von Filtern auf die Angebotsbibliothek {#filters}

Klicken Sie auf das Symbol **[!UICONTROL Show filters]** ( ![Filter anzeigen auf der Seite &quot;Angebote&quot;](/help/main/c-experiences/c-manage-content/assets/show-filters-icon.png) ), um Angebote nach [!UICONTROL Type], [!UICONTROL Source] und [!UICONTROL AEM Type] zu filtern.

![offer_filter image](assets/offers-filter-new.png)

Mit dem Symbol **[!UICONTROL Show filters]** können Sie Angebote nach folgenden Kategorien filtern:

* **Typ**: HTML-Angebot, [JSON-Angebot](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

* **Source**: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager].

* **AEM Typ**: [Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) und [Experience Fragments](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Weitere Informationen zu den verschiedenen Fragmenttypen finden Sie unter [AEM Übersicht über Experience Fragments und Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Schnellaktionen durchführen {#quick-actions}

Sie können die folgenden Schnellaktionen durchführen, indem Sie auf das entsprechende Symbol klicken:

### Schnellinformationen

Klicken Sie auf das Symbol &quot;**[!UICONTROL Quick Info]**&quot;neben dem jeweiligen Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Pop-up-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums, an dem das Angebot zuletzt geändert wurde und von wem und mehr. Die verfügbaren Optionen hängen vom Angebotstyp ab: HTML-Angebot, [JSON-Angebot](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

![](/help/main/c-experiences/c-manage-content/assets/quick-actions.png)

### Mehr Aktionen	

Die für Code-Angebote und Bildangebote verfügbaren Aktionen unterscheiden sich geringfügig. Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

#### [!UICONTROL Code Offer] Optionen

Klicken Sie auf das Symbol &quot;**[!UICONTROL More actions]**&quot;(die horizontalen Auslassungspunkte) neben dem jeweiligen Angebotsnamen, um ein Menü zu öffnen, über das Sie für eine Aktivität Schnellaktionen durchführen können. Die folgenden Aktionen sind verfügbar (je nach Ihren Berechtigungen und dem Angebotsstatus): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] und [!UICONTROL Move].

![Option &quot;Mehr Aktionen&quot;in der Target-Angebotsbibliothek](/help/main/c-experiences/c-manage-content/assets/more-actions.png)

* Bearbeiten 
* Kopieren 
* Löschen
* Verschieben (Um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf das Symbol **[!UICONTROL Move]** für das gewünschte Element, klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Drop]**.)

Je nach Ihren Berechtigungen werden möglicherweise keine Symbole für alle Optionen angezeigt. Beispielsweise verfügt ein Benutzer mit [!UICONTROL Observer] -Berechtigungen nicht über die Rechte zur Verwendung der [!UICONTROL Copy] -Option.

Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] Optionen

Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den gewünschten Ordner auf der Registerkarte [!UICONTROL Image Offers] bewegen und dann auf das gewünschte Symbol klicken.

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

So können Sie beispielsweise auf die folgende Angebotsdefinitionskarte für ein HTML-Angebot zugreifen, indem Sie den Mauszeiger über ein Angebot in der Liste [!UICONTROL Content] bewegen und auf das Informationssymbol klicken:

![offer-card-html image](assets/offer-card-html.png)

Die folgenden Informationen sind verfügbar:

* Name
* Quelle
* Typ
* Angebots-ID
* Angebotspfad
* Zuletzt geändert

Klicken Sie auf den Tab [!UICONTROL Offer Usage] , um die Aktivitäten anzuzeigen, die auf ein Codeangebot in der Popup-Karte für die Angebotsdefinition verweisen. Diese Funktionalität gilt nicht für Bildangebote. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Zu den Informationen gehören [!UICONTROL Live Activities] und [!UICONTROL Inactive Activities].

![Bild zur Nutzung der Angebotskarte](assets/offer-card-usage.png)

Die folgende Angebotsdefinitionskarte für ein Umleitungsangebot:

![offer-card-redirect image](assets/offer-card-redirect.png)

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

![offer-card-remote image](assets/offer-card-remote.png)

Die folgenden Informationen sind verfügbar:

* Name
* Quelle
* Typ
* Angebots-ID
* Angebotspfad
* Zuletzt geändert
* Umleitungs-URL-Typ
* Absolute oder relative URL

## Schulungsvideo: Symbol &quot;Content Repository ![Überblick&quot;](/help/main/assets/overview.png)

In diesem Video wird beschrieben, wie Angebote verwaltet werden.

* Zusammenhang zwischen der [Experience Cloud-Asset-Bibliothek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) und der Target-Inhaltsbibliothek
* Benutzerdefinierte HTML-Angebote
* Benutzerdefinierte HTML-Angebote im Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)
