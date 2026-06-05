---
keywords: Inhalt;Assets;Inhalt verwalten;Angebote;Assets verwalten;Auswahlmodus aufrufen;Auswahlmodus
description: Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der Bibliothek [!UICONTROL Angebote] effizient verwalten können.
title: Wie verwalte ich Code- und Bildangebote?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
TQID: https://experienceleague.adobe.com/A8ZLHW-FrWHGPJR7P-mhl2pO6SPoDc--LWpFEjtQzBY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 958
ht-degree: 7%

---

# Angebote

Erfahren Sie, wie Sie Code- und Bildangebote mithilfe der Bibliothek [!UICONTROL Angebote] in [!DNL Adobe Target] effizient verwalten können.

Um die Bibliothek [!UICONTROL Angebote] anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Angebote]** oben in der [!DNL Target]-Benutzeroberfläche.

![Angebotsseite](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

Die [!UICONTROL Angebote]-Bibliothek enthält Angebote, die über [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) und APIs eingerichtet wurden. In [!DNL Target Classic] oder anderen Lösungen erstellte Angebote lassen sich in [!DNL Target Standard/Premium] bearbeiten.

Die [!UICONTROL Angebote]-Bibliothek bietet einen Überblick über alle Code- und Bildangebote und ermöglicht die Durchführung verschiedener Aktionen:

| Element | Beschreibung |
|--- |--- |
| Linke Navigationsleiste | Wechseln Sie zwischen der Anzeige [!UICONTROL Code]Angeboten oder [!UICONTROL Bildangebote]. |
| [!UICONTROL Ordner anzeigen]/[!UICONTROL Ordner ausblenden]<P>![Symbol „Filter anzeigen/Filter ausblenden“](/help/main/assets/icons/RailLeft.svg) | Klicken Sie auf das Symbol **[!UICONTROL Ordner anzeigen]** oder **[!UICONTROL Ordner ausblenden]**, um zwischen der Anzeige der Ordnerstruktur der Angebote und der Anzeige der Ordnerstruktur umzuschalten.<P>Weitere Informationen finden Sie unter [Erstellen von &#x200B;](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL Filter anzeigen] Symbol<P>![Symbol „Filter anzeigen“](/help/main/assets/icons/Filter.svg) | Klicken Sie auf **[!UICONTROL Filter anzeigen]**, um Angebote nach [!UICONTROL Typ], [!UICONTROL Source] und [!UICONTROL AEM-Typ zu &#x200B;].<P>Weitere Informationen finden Sie [Anwenden von Filtern auf die Liste der Angebote](#filters) unten. |
| Suchfelder | Verwenden Sie die Felder **[!UICONTROL Suche in]**, um schnell ein Angebot zu finden oder die Anzahl der in der Bibliothek [!UICONTROL Angebote] angezeigten Angebote zu reduzieren. Sie können nach [!UICONTROL Angebotsname], [!UICONTROL AEM-Pfaden] oder [!UICONTROL AEM-Tags] suchen. Suchoptionen sind sitzungspersistent. |
| [!UICONTROL Ordner erstellen] | Klicken Sie **[!UICONTROL Ordner erstellen]**, um Ordner in der [!UICONTROL Angebotsbibliothek] zu erstellen, um Code-Angebote, Bildangebote sowie andere Ordner zu speichern und eine Unterordnerstruktur zu erstellen.<P>Weitere Informationen finden Sie unter [Erstellen von &#x200B;](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Angebot erstellen]] | Klicken Sie **[!UICONTROL Angebot erstellen]**, um ein Angebot zu erstellen.<P>Weitere Informationen zur Erstellung der verschiedenen Angebotstypen finden Sie unter: <ul><li>HTML-Angebot</li><li>[JSON-Angebot](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Umleitungsangebot](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Remote-Angebot](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Kontrollkästchen für Massenvorgänge<P>![Symbol für Massenvorgänge](/help/main/assets/icons/Rectangle.svg) | Aktivieren Sie [!UICONTROL &#x200B; Kontrollkästchen &#x200B;]Massenvorgänge), um Massenvorgänge für alle Angebote oder für ausgewählte Angebote durchzuführen.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Angebotsstatus) finden Sie [Ausführen von Schnellaktionen](#quick-actions) unten. |
| [!UICONTROL Name] | Der Name jedes Angebots.<P>Klicken Sie auf das **[!UICONTROL Quick Info]**-Symbol ( ![Quick Info-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben jedem Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Popup-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums der letzten Änderung des Angebots und davon, von wem und mehr.<p>Klicken Sie auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben jedem Angebotsnamen, um ein Menü zu öffnen, in dem Sie Schnellaktionen für eine Aktivität durchführen können. Die folgenden Aktionen sind verfügbar (abhängig von Ihren Berechtigungen und dem Angebotsstatus): [!UICONTROL Bearbeiten], [!UICONTROL Kopieren], [!UICONTROL Löschen] und [!UICONTROL Verschieben]. Weitere Informationen zu den einzelnen Aktionen finden Sie [Ausführen von Schnellaktionen](#quick-actions) unten.<P>Klicken Sie auf die Tabellenkopfzeile, um die Liste alphabetisch nach Namen in auf- oder absteigender Reihenfolge zu sortieren. |
| [!UICONTROL Typ] | Der Angebotstyp: [!UICONTROL HTML-], [[!UICONTROL Umleitungsangebote]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote-]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [[!UICONTROL JSON-Angebote]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Zeigt an, wo das Angebot erstellt wurde: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager]. |
| [!UICONTROL Zuletzt aktualisiert] | Zeigt das Datum und die Uhrzeit der letzten Änderung des Angebots an und nach wem.<P>Klicken Sie auf die Tabellenkopfzeile, um die Liste in auf- oder absteigender Reihenfolge nach Datum zu sortieren. |

## Anwenden von Filtern auf die Angebotsbibliothek {#filters}

Klicken Sie auf das Symbol **[!UICONTROL Filter anzeigen]** (![Symbol „Filter anzeigen“ auf der Seite &quot;](/help/main/assets/icons/Filter.svg)„), um Angebote nach [!UICONTROL Typ], [!UICONTROL Source] und [!UICONTROL AEM-Typ] zu filtern.

Mit **[!UICONTROL Symbol „Filter]**&quot; können Sie Angebote nach den folgenden Kategorien filtern:

* **[!UICONTROL type]**: [!UICONTROL HTML-], [[!UICONTROL Umleitungsangebot]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote-Angebot]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) und [[!UICONTROL JSON-]](/help/main/c-experiences/c-manage-content/create-json-offer.md).

* **[!UICONTROL Source]**: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Adobe Experience Manager].

* **AEM-**: [Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) und [Experience Fragments](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Weitere Informationen zu den verschiedenen Fragmenttypen finden Sie in der Übersicht über [AEM Experience Fragments und Inhaltsfragmente](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

Filter sind sitzungspersistent.

## Ausführen von Schnellaktionen {#quick-actions}

Sie können die folgenden Schnellaktionen ausführen, indem Sie auf das entsprechende Symbol klicken:

### Schnellinfo

Klicken Sie auf das **[!UICONTROL Quick Info]**-Symbol ( ![Quick Info-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben jedem Angebotsnamen, um weitere Informationen zu diesem Angebot in einer Popup-Karte anzuzeigen, einschließlich der Angebots-ID, des Typs, des Datums der letzten Änderung des Angebots und davon, von wem und mehr. Die verfügbaren Optionen hängen vom Angebotstyp ab: [!UICONTROL HTML-], [[!UICONTROL JSON-]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Umleitungsangebot]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote-Angebot]](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

### Mehr Aktionen

Die für [!UICONTROL Code-Angebote] und für [!UICONTROL Bildangebote] verfügbaren Aktionen unterscheiden sich geringfügig. Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

#### [!UICONTROL Angebot codieren] Optionen

Klicken Sie auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben jedem Angebotsnamen, um ein Menü zu öffnen, in dem Sie schnell Aktionen für eine Aktivität durchführen können.

Die folgenden Aktionen sind verfügbar (abhängig von Ihren Berechtigungen und dem Angebotsstatus):

* [!UICONTROL Bearbeiten]
* [!UICONTROL Kopieren]
* [!UICONTROL Löschen]
* [!UICONTROL Verschieben] (um beispielsweise ein oder mehrere Elemente in einen Ordner zu verschieben, klicken Sie auf **[!UICONTROL Verschieben]** neben dem gewünschten Element, klicken Sie auf den gewünschten Ordner und dann auf **[!UICONTROL Verschieben]**.)

Je nach Ihren Berechtigungen werden möglicherweise nicht für alle Optionen Symbole angezeigt. Beispielsweise verfügt ein Benutzer mit [!UICONTROL Beobachter]-Berechtigungen nicht über die Rechte zur Verwendung der Option [!UICONTROL Kopieren].

Ausführliche Informationen zu den Aufgaben, die Sie mit Angeboten und Ordnern ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Bildangebot] Optionen

Führen Sie zusätzliche Aufgaben aus, indem Sie den Mauszeiger über das gewünschte Bildangebot oder den Ordner auf der Registerkarte [!UICONTROL Bildangebote] bewegen und dann auf das gewünschte Symbol klicken.

Zu den Optionen zählen:

* [!UICONTROL Auswählen]
* [!UICONTROL Herunterladen].
* [!UICONTROL Eigenschaften anzeigen]
* [!UICONTROL Weitere Aktionen]
* [!UICONTROL Bearbeiten]
* [!UICONTROL Anmerken]
* [!UICONTROL Kopieren]

Ausführliche Informationen zu den Aufgaben, die Sie mit Angeboten und Ordnern ausführen können, finden Sie unter [Arbeiten mit Inhalten in der Asset-Bibliothek](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Bildangebote sind nicht Teil des Modells [Enterprise-](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)&quot;.

## Anzeigen der Angebotsdefinitionen {#section_6B059DD121434E6292CAB393507D010E}

Um Details zur Angebotsdefinition auf einer Popup-Karte in der [!UICONTROL Angebotsbibliothek] anzuzeigen, ohne das Angebot zu öffnen, klicken Sie auf das Symbol ![Schnellinfo](/help/main/assets/icons/InfoOutline.svg) .

Die folgenden Informationen sind verfügbar:

* [!UICONTROL Name]
* [!UICONTROL Angebots-ID]
* [!UICONTROL Typ]
* [!UICONTROL Zuletzt geändert]

Klicken Sie auf [!UICONTROL &#x200B; Link Vollständige Details anzeigen], um die Attribute und Aktivitäten des Angebots anzuzeigen, die auf ein Code-Angebot in der Popup-Karte für die Definition jedes Angebots verweisen. Diese Funktionalität gilt nicht für Bildangebote. Auf diese Weise können Sie bei der Bearbeitung von Angeboten Auswirkungen auf andere Aktivitäten vermeiden. Die Informationen enthalten Details zu [!UICONTROL Live]Aktivitäten und [!UICONTROL inaktiven Aktivitäten].
