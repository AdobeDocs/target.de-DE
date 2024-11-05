---
keywords: Inhalt;Assets;Inhalt verwalten;Angebote;Assets verwalten;Auswahlmodus aufrufen;Auswahlmodus
description: Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der [!UICONTROL Offers] -Bibliothek effizient verwalten können.
title: Wie verwalte ich Code- und Bildangebote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 0c86e142b7d459d07af51ec0c3454611564c8e08
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 8%

---

# Angebote

Erfahren Sie, wie Sie Code- und Bildangebote effizient mit der [!UICONTROL Offers] -Bibliothek in [!DNL Adobe Target] verwalten.

>[!NOTE]
>
>Dieser Artikel enthält Informationen zu Aktualisierungen der [!DNL Target] -Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Das [!DNL Adobe Target]-Team ermöglicht für ausgewählte Kunden oft neue Funktionen zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen für alle Kunden in zukünftigen [!DNL Target]-Versionen aktiviert und in den [Versionshinweisen](/help/main/r-release-notes/release-notes.md) angekündigt.

Um die Bibliothek [!UICONTROL Offers] anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Offers]** oben in der Benutzeroberfläche von [!DNL Target].

![Angebotsseite](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

Die Bibliothek [!UICONTROL Offers] enthält Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs eingerichtet wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

Die Bibliothek [!UICONTROL Offers] bietet einen Überblick über alle Code- und Bildangebote und ermöglicht Ihnen die Durchführung verschiedener Aktionen:

| Element | Beschreibung |
|--- |--- |
| Linke Navigationsleiste | Zwischen Anzeige von [!UICONTROL Code Offers] oder [!UICONTROL Image Offers] wechseln. |
| [!UICONTROL Show Folders] / [!UICONTROL Hide Folders]<P>![Symbol Filter einblenden/Filter ausblenden](/help/main/assets/icons/RailLeft.svg) | Klicken Sie auf das Symbol **[!UICONTROL Show Folders]** oder **[!UICONTROL Hide Folders]** , um zwischen der Anzeige der Ordnerstruktur Ihrer Angebote oder der Anzeige der Ordnerstruktur umzuschalten.<P>Weitere Informationen finden Sie unter [Erstellen von Angebotsordnern](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| Symbol [!UICONTROL Show filters]<P>![Symbol &quot;Filter anzeigen&quot;](/help/main/assets/icons/Filter.svg) | Klicken Sie auf das Symbol **[!UICONTROL Show filters]** , um Angebote nach [!UICONTROL Type], [!UICONTROL Source] und [!UICONTROL AEM Type] zu filtern.<P>Weitere Informationen finden Sie unter [Anwenden von Filtern auf die Angebotsliste](#filters) weiter unten. |
| Suchfelder | Verwenden Sie die Felder **[!UICONTROL Search in]** , um schnell ein Angebot zu finden oder die Anzahl der in der Bibliothek [!UICONTROL Offers] angezeigten Angebote zu reduzieren. Sie können nach [!UICONTROL Offer Name], [!UICONTROL AEM Paths] oder [!UICONTROL AEM Tags] suchen. |
| [!UICONTROL Create Folder] | Klicken Sie auf &quot;**[!UICONTROL Create Folder]**&quot;, um Ordner in der Bibliothek &quot;[!UICONTROL Offer]&quot;zu erstellen und Codeangebote, Bildangebote sowie andere Ordner zu speichern, um eine Unterordnerstruktur zu erstellen.<P>Weitere Informationen finden Sie unter [Erstellen von Angebotsordnern](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Klicken Sie auf **[!UICONTROL Create Offer]** , um ein Angebot zu erstellen.<P>Weitere Informationen zur Erstellung der verschiedenen Angebotstypen finden Sie unter: <ul><li>HTML-Angebot</li><li>[JSON-Angebot](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Kontrollkästchen für Massenvorgänge<P>![Symbol &quot;Massenvorgänge&quot;](/help/main/assets/icons/Rectangle.svg) | Aktivieren Sie die Kontrollkästchen [!UICONTROL Bulk Operations] , um Massenvorgänge für alle Angebote oder ausgewählte Angebote durchzuführen.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Angebotsstatus) finden Sie unten unter [Durchführen von Schnellaktionen](#quick-actions) . |
| [!UICONTROL Name] | Der Name jedes Angebots.<P>Klicken Sie auf das Symbol **[!UICONTROL Quick Info]** ( ![Quick Info icon](/help/main/assets/icons/InfoOutline.svg) ) neben dem jeweiligen Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Pop-up-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums, an dem das Angebot zuletzt geändert wurde und von wem und mehr.<p>Klicken Sie neben dem jeweiligen Angebotsnamen auf das Symbol **[!UICONTROL More Actions]** ( ![Symbol Weitere Aktionen](/help/main/assets/icons/MoreSmallList.svg) ), um ein Menü zu öffnen, über das Sie schnell Aktionen für eine Aktivität durchführen können. Die folgenden Aktionen sind verfügbar (je nach Ihren Berechtigungen und dem Angebotsstatus): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] und [!UICONTROL Move]. Weitere Informationen zu den einzelnen Aktionen finden Sie unten unter [Schnellaktionen durchführen](#quick-actions) .<P>Klicken Sie auf die Tabellenüberschrift, um die Liste alphabetisch in auf- oder absteigender Reihenfolge nach Namen zu sortieren. |
| [!UICONTROL Type] | Der Angebotstyp: [!UICONTROL HTML Offers], [[!UICONTROL Redirect Offers]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offers]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [[!UICONTROL JSON Offers]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Zeigt an, wo das Angebot erstellt wurde: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager]. |
| [!UICONTROL Last updated] | Zeigt Datum und Uhrzeit der letzten Änderung des Angebots an und nach wem.<P>Klicken Sie auf die Tabellenüberschrift, um die Liste in auf- oder absteigender Reihenfolge nach Datum zu sortieren. |

## Anwenden von Filtern auf die Angebotsbibliothek {#filters}

Klicken Sie auf das Symbol **[!UICONTROL Show filters]** ( ![Filter anzeigen auf der Seite &quot;Angebote&quot;](/help/main/assets/icons/Filter.svg)), um Angebote nach [!UICONTROL Type], [!UICONTROL Source] und [!UICONTROL AEM Type] zu filtern.

Mit dem Symbol **[!UICONTROL Show filters]** können Sie Angebote nach folgenden Kategorien filtern:

* 0: [!UICONTROL HTML Offer], [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md).**[!UICONTROL Type]**

* 0: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager].**[!UICONTROL Source]**

* **AEM Typ**: [Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) und [Experience Fragments](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Weitere Informationen zu den verschiedenen Fragmenttypen finden Sie unter [AEM Übersicht über Experience Fragments und Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Schnellaktionen durchführen {#quick-actions}

Sie können die folgenden Schnellaktionen durchführen, indem Sie auf das entsprechende Symbol klicken:

### Schnellinformationen

Klicken Sie auf das Symbol **[!UICONTROL Quick Info]** ( ![Quick Info icon](/help/main/assets/icons/InfoOutline.svg) ) neben dem jeweiligen Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Pop-up-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums, an dem das Angebot zuletzt geändert wurde und von wem und mehr. Die verfügbaren Optionen hängen vom Angebotstyp ab: [!UICONTROL HTML Offer], [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

### Mehr Aktionen	

Die für [!UICONTROL Code Offers] und für [!UICONTROL Image Offers] verfügbaren Aktionen unterscheiden sich geringfügig. Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

#### [!UICONTROL Code Offer] Optionen

Klicken Sie neben dem jeweiligen Angebotsnamen auf das Symbol **[!UICONTROL More actions]** ( ![Symbol Weitere Aktionen](/help/main/assets/icons/MoreSmallList.svg) ), um ein Menü zu öffnen, über das Sie schnell Aktionen für eine Aktivität durchführen können.

Die folgenden Aktionen sind verfügbar (je nach Berechtigungen und Angebotsstatus):

* [!UICONTROL Edit]
* [!UICONTROL Copy]
* [!UICONTROL Delete]
* [!UICONTROL Move] (Um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf **[!UICONTROL Move]** neben dem gewünschten Element, klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Move]**.)

Je nach Ihren Berechtigungen werden möglicherweise keine Symbole für alle Optionen angezeigt. Beispielsweise verfügt ein Benutzer mit [!UICONTROL Observer] -Berechtigungen nicht über die Rechte zur Verwendung der [!UICONTROL Copy] -Option.

Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] Optionen

Führen Sie zusätzliche Aufgaben durch, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den gewünschten Ordner auf der Registerkarte [!UICONTROL Image Offers] bewegen und dann auf das gewünschte Symbol klicken.

Zu den Optionen zählen:

* [!UICONTROL Select]
* [!UICONTROL Download]
* [!UICONTROL View Properties]
* [!UICONTROL More Actions]
* [!UICONTROL Edit]
* [!UICONTROL Annotate]
* [!UICONTROL Copy]

Detaillierte Informationen zu den Aufgaben, die Sie für Angebote und Ordner ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Bildangebote sind nicht Teil des Modells [Berechtigungen für Unternehmensbenutzer](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

## Angebotsdefinitionen anzeigen {#section_6B059DD121434E6292CAB393507D010E}

Um Details zur Angebotsdefinition auf einer Pop-up-Karte in der Bibliothek &quot;[!UICONTROL Offers]&quot;anzuzeigen, ohne das Angebot zu öffnen, klicken Sie auf das Symbol ( ![Quick Info&quot;-Symbol](/help/main/assets/icons/InfoOutline.svg) ).

Die folgenden Informationen sind verfügbar:

* [!UICONTROL Name]
* [!UICONTROL Offer ID]
* [!UICONTROL Type]
* [!UICONTROL Last Modified]

Klicken Sie auf den Link [!UICONTROL View Full Details] , um die Attribute und Aktivitäten des Angebots anzuzeigen, die auf ein Codeangebot in der Popup-Karte für die Angebotsdefinition verweisen. Diese Funktionalität gilt nicht für Bildangebote. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Die Informationen enthalten Details für [!UICONTROL Live Activities] und [!UICONTROL Inactive Activities].
