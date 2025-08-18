---
keywords: Inhalt;Assets;Inhalt verwalten;Angebote;Assets verwalten;Auswahlmodus aufrufen;Auswahlmodus
description: Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der [!UICONTROL Offers] effizient verwalten können.
title: Wie verwalte ich Code- und Bildangebote?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: f034aba7fe4f54b937dee0846140af140052694c
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 8%

---

# Angebote

Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der [!UICONTROL Offers] in [!DNL Adobe Target] effizient verwalten können.

Um die [!UICONTROL Offers]-Bibliothek anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Offers]** oben in der [!DNL Target]-Benutzeroberfläche.

![Angebotsseite](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

Die [!UICONTROL Offers]-Bibliothek enthält Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs eingerichtet wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

Die [!UICONTROL Offers]-Bibliothek bietet einen Überblick über alle Code- und Bildangebote und ermöglicht die Durchführung verschiedener Aktionen:

| Element | Beschreibung |
|--- |--- |
| Linke Navigationsleiste | Wechseln zwischen Anzeige von [!UICONTROL Code Offers] oder [!UICONTROL Image Offers]. |
| [!UICONTROL Show Folders]/[!UICONTROL Hide Folders]<P>![Symbol „Filter anzeigen/Filter ausblenden“](/help/main/assets/icons/RailLeft.svg) | Klicken Sie auf das Symbol **[!UICONTROL Show Folders]** oder **[!UICONTROL Hide Folders]** , um zwischen der Anzeige der Ordnerstruktur des Angebots und der Anzeige der Ordnerstruktur umzuschalten.<P>Weitere Informationen finden Sie unter [Erstellen von ](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| Symbol [!UICONTROL Show filters]<P>![Symbol „Filter anzeigen“](/help/main/assets/icons/Filter.svg) | Klicken Sie auf das Symbol **[!UICONTROL Show filters]** , um Angebote nach [!UICONTROL Type], [!UICONTROL Source] und [!UICONTROL AEM Type] zu filtern.<P>Weitere Informationen finden Sie [Anwenden von Filtern auf die Liste der Angebote](#filters) unten. |
| Suchfelder | Verwenden Sie die **[!UICONTROL Search in]**, um schnell ein Angebot zu finden oder die Anzahl der in der [!UICONTROL Offers]-Bibliothek angezeigten Angebote zu reduzieren. Sie können nach [!UICONTROL Offer Name], [!UICONTROL AEM Paths] oder [!UICONTROL AEM Tags] suchen. Suchoptionen sind sitzungspersistent. |
| [!UICONTROL Create Folder] | Klicken Sie auf **[!UICONTROL Create Folder]** , um Ordner in der [!UICONTROL Offer]-Bibliothek zu erstellen, in denen Code-Angebote, Bildangebote und andere Ordner gespeichert werden können, um eine Unterordnerstruktur zu erstellen.<P>Weitere Informationen finden Sie unter [Erstellen von ](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Zum Erstellen eines Angebots auf **[!UICONTROL Create Offer]** klicken<P>Weitere Informationen zur Erstellung der verschiedenen Angebotstypen finden Sie unter: <ul><li>HTML-Angebot</li><li>[JSON-Angebot](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Kontrollkästchen für Massenvorgänge<P>![Symbol für Massenvorgänge](/help/main/assets/icons/Rectangle.svg) | Aktivieren Sie die Kontrollkästchen [!UICONTROL Bulk Operations] , um Massenvorgänge für alle Angebote oder für ausgewählte Angebote durchzuführen.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Angebotsstatus) finden Sie [Ausführen von Schnellaktionen](#quick-actions) unten. |
| [!UICONTROL Name] | Der Name jedes Angebots.<P>Klicken Sie auf das **[!UICONTROL Quick Info]**-Symbol ( ![Quick Info-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben jedem Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Popup-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums, an dem das Angebot zuletzt geändert wurde, und von wem und mehr.<p>Klicken Sie auf das **[!UICONTROL More Actions]** (Symbol ![Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben jedem Angebotsnamen, um ein Menü zu öffnen, in dem Sie Schnellaktionen für eine Aktivität durchführen können. Die folgenden Aktionen sind verfügbar (abhängig von Ihren Berechtigungen und dem Angebotsstatus): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] und [!UICONTROL Move]. Weitere Informationen zu den einzelnen Aktionen finden Sie [Ausführen von Schnellaktionen](#quick-actions) unten.<P>Klicken Sie auf die Tabellenkopfzeile, um die Liste alphabetisch nach Namen in auf- oder absteigender Reihenfolge zu sortieren. |
| [!UICONTROL Type] | Der Angebotstyp: [!UICONTROL HTML Offers], [[!UICONTROL Redirect Offers]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offers]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [[!UICONTROL JSON Offers]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Zeigt an, wo das Angebot erstellt wurde: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager]. |
| [!UICONTROL Last updated] | Zeigt das Datum und die Uhrzeit der letzten Änderung des Angebots an und nach wem.<P>Klicken Sie auf die Tabellenkopfzeile, um die Liste in auf- oder absteigender Reihenfolge nach Datum zu sortieren. |

## Anwenden von Filtern auf die Angebotsbibliothek {#filters}

Klicken Sie auf das **[!UICONTROL Show filters]**-Symbol ![Filtersymbol auf der Seite Angebote anzeigen](/help/main/assets/icons/Filter.svg), um Angebote nach [!UICONTROL Type], [!UICONTROL Source] und [!UICONTROL AEM Type] zu filtern.

Mit dem Symbol **[!UICONTROL Show filters]** können Sie Angebote nach den folgenden Kategorien filtern:

* **[!UICONTROL Type]**: [!UICONTROL HTML Offer], [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md).

* **[!UICONTROL Source]**: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager].

* **AEM-**: [Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) und [Experience Fragments](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Weitere Informationen zu den verschiedenen Fragmenttypen finden Sie in der Übersicht über [AEM Experience Fragments und Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

Filter sind sitzungspersistent.

## Ausführen von Schnellaktionen {#quick-actions}

Sie können die folgenden Schnellaktionen ausführen, indem Sie auf das entsprechende Symbol klicken:

### Schnellinfo

Klicken Sie auf das **[!UICONTROL Quick Info]**-Symbol ( ![Quick Info-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben jedem Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Popup-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums, an dem das Angebot zuletzt geändert wurde, und von wem und mehr. Die verfügbaren Optionen hängen vom Angebotstyp ab: [!UICONTROL HTML Offer], [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

### Mehr Aktionen	

Die für [!UICONTROL Code Offers] und für [!UICONTROL Image Offers] verfügbaren Aktionen unterscheiden sich geringfügig. Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

#### [!UICONTROL Code Offer]

Klicken Sie auf das **[!UICONTROL More actions]** (Symbol ![Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben jedem Angebotsnamen, um ein Menü zu öffnen, in dem Sie Schnellaktionen für eine Aktivität durchführen können.

Die folgenden Aktionen sind verfügbar (abhängig von Ihren Berechtigungen und dem Angebotsstatus):

* [!UICONTROL Edit]
* [!UICONTROL Copy]
* [!UICONTROL Delete]
* [!UICONTROL Move] (Um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf **[!UICONTROL Move]** neben dem gewünschten Element, dann auf den gewünschten Ordner und anschließend auf **[!UICONTROL Move]**.)

Je nach Ihren Berechtigungen werden möglicherweise nicht für alle Optionen Symbole angezeigt. Beispielsweise verfügt ein Benutzer mit [!UICONTROL Observer] Berechtigungen nicht über die Rechte zur Verwendung der Option [!UICONTROL Copy] .

Ausführliche Informationen zu den Aufgaben, die Sie mit Angeboten und Ordnern ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer]

Führen Sie zusätzliche Aufgaben aus, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den gewünschten Ordner auf der Registerkarte [!UICONTROL Image Offers] bewegen und dann auf das gewünschte Symbol klicken.

Zu den Optionen zählen:

* [!UICONTROL Select]
* [!UICONTROL Download]
* [!UICONTROL View Properties]
* [!UICONTROL More Actions]
* [!UICONTROL Edit]
* [!UICONTROL Annotate]
* [!UICONTROL Copy]

Ausführliche Informationen zu den Aufgaben, die Sie mit Angeboten und Ordnern ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Bildangebote sind nicht Teil des Modells [Enterprise-](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)&quot;.

## Anzeigen der Angebotsdefinitionen {#section_6B059DD121434E6292CAB393507D010E}

Um Details zur Angebotsdefinition auf einer Popup-Karte in der [!UICONTROL Offers]-Bibliothek anzuzeigen, ohne das Angebot zu öffnen, klicken Sie auf das Symbol ![Schnellinfo](/help/main/assets/icons/InfoOutline.svg) .

Die folgenden Informationen sind verfügbar:

* [!UICONTROL Name]
* [!UICONTROL Offer ID]
* [!UICONTROL Type]
* [!UICONTROL Last Modified]

Klicken Sie auf den Link [!UICONTROL View Full Details] , um die Attribute und Aktivitäten des Angebots anzuzeigen, die auf ein Code-Angebot in der Popup-Karte für die Definition jedes Angebots verweisen. Diese Funktionalität gilt nicht für Bildangebote. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Die Informationen enthalten Details zu [!UICONTROL Live Activities] und [!UICONTROL Inactive Activities].
