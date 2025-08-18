---
keywords: Real-time Customer Data Platform;rtcdp;Personalisierung;AEP-Audiences;Adobe Experience Platform-Audiences;Profilattribute
description: Erfahren Sie, wie Sie die  [!DNL Target]/[!DNL Real-Time Customer Data Platform] -Integration (RTCDP) zur Bereitstellung umfassenderer Kundendaten und einer wirkungsvolleren Personalisierung nutzen können.
title: Wie kann ich  [!DNL Target]  mit  [!DNL Real-Time Customer Data Platform] integrieren?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 4104b6cb67347205c0143c9dea46dd483a8266ce
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 71%

---

# Integrieren mit [!DNL Real-Time Customer Data Platform]

Die auf [!DNL Adobe Experience Platform] aufbauende [!DNL Real-Time Customer Data Platform] (RTCDP) hilft Unternehmen, bekannte und anonyme Daten aus mehreren Unternehmensquellen zusammenzuführen. Mit der RTCDP können Sie Kundenprofile erstellen, mit denen Sie personalisierte Kundenerlebnisse über alle Kanäle und Geräte hinweg in Echtzeit bereitstellen können.

Weitere Informationen zu RTCDP finden Sie unter [Übersicht über Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank}.

## Wichtigste Funktionen

Zu den wichtigsten Funktionen gehören:

* Direkte [!DNL Target]-Integration mit Real-Time CDP/[!DNL Adobe Experience Platform] am Edge (beseitigt die Abhängigkeit von [!DNL Audience Core services] – AAM)
* [!UICONTROL Target Edge Destinations Card] mit Governance und Richtliniendurchsetzung
* Real-Time CDP-Segmente und freigegebene Profilattribute

## Implementierungsszenarien

Die folgenden Abschnitte zeigen, welcher Anwendungsfall für Personalisierung (nächste Sitzung oder dieselbe Seite) bei Verwendung verschiedener Implementierungsmethoden verfügbar ist:

### at.js-Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] (AAM) und [!DNL Target]</li><li>[!DNL RTCDP] (Premium oder Ultimate) und [!DNL Target]</li><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM] und [!DNL Target]</li></ul> | Personalisierung der nächsten Sitzung |

### Implementierung von [!DNL Adobe Experience Platform Web SDK] oder [!DNL Experience Platform Server-Side API]

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL RTCDP] (beliebige SKU) und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><li>Personalisierung derselben Seite über Edge</li><li>Governance bei Freigabe von Segmenten erzwungen</li></ul> |
| <ul><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM] und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>[!DNL AAM] Segmente</li><li>Drittanbietersegmente über [!DNL AAM]</li></ul><li>Personalisierung derselben Seite über Edge</li><ul><li>[!DNL RTCDP] Segmente</li><li>Governance bei Freigabe von Segmenten erzwungen</li></ul> |

### Mischung aus [!UICONTROL at.js] und [!DNL Platform Web SDK] Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL RTCDP] (beliebige SKU) und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>Für alle Seiten mit [!UICONTROL at.js]</li></ul><li>Personalisierung derselben Seite</li><ul><li>Für alle Seiten mit [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM] und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>Für alle Seiten mit [!UICONTROL at.js]</li><li>[!DNL AAM] Segmente</li><li>Drittanbietersegmente über [!DNL AAM]</li></ul> |

## Segmentbewertungszeit

Die folgende Tabelle zeigt die Segmentbewertungszeit für Ereignisse aus verschiedenen Implementierungsszenarien:

| Szenario | Edge-Segment (Millisekundenbewertung) | Streaming-Segment (Minutenbewertung) | Batch-Segmentbewertung |
| --- | --- | --- | --- |
| Ereignisse/Daten aus [!DNL Adobe Experience Platform] SDKs | Ja | Ja | K. A. |
| Ereignisse aus [!UICONTROL at.js] | Nein | Ja | K. A. |
| Ereignisse aus [!DNL Target Mobile] SDKs | Nein | Ja | K. A. |
| Ereignisse aus Batch-Upload | Nein | Nein | Ja |
| Ereignisse aus Offline-Daten (Stream) | Nein | Ja | Ja |

## Verwenden von Audiences aus [!DNL Adobe Experience Platform] {#aep}

Die Verwendung der in [!DNL Adobe Experience Platform] erstellten [Audiences](/help/main/c-target/c-audiences/audiences.md) liefert umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen. Die [Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank} (RTCDP), die auf [!DNL Adobe Experience Platform] aufbaut, hilft Unternehmen dabei, bekannte und anonyme Daten aus mehreren Unternehmensquellen zusammenzuführen. Auf diese Weise können Sie Kundenprofile erstellen, mit denen in Echtzeit personalisierte Kundenerlebnisse über alle Kanäle und Geräte hinweg bereitgestellt werden können.

Durch Verbinden von [!DNL Target] und [!DNL Real-Time Customer Data Platform] können Kundinnen und Kunden ihre Web-Personalisierung anreichern. Mit dieser Integration können Sie neue Segmente erschließen, die für [!DNL Target] möglicherweise nicht zugänglich waren, um die Echtzeit-Personalisierung in Millisekunden auf der ersten Seite des Web-Besuchs eines Kunden bzw. einer Kundin zu aktivieren. Durch die Verwendung von in [!DNL Adobe Experience Platform] erstellten Audiences und Profilattributen können Sie die verfügbaren Datenpunkte erweitern, was eine umfassendere Personalisierung ermöglicht.

Diese Integration erschließt wichtige Anwendungsfälle mit Real-Time CDP:

* Personalisierung für gleiche Seite / nächsten Treffer
* Personalisierung für erstmalige / unbekannte Benutzende

## Freigeben von Real-Time CDP-Profilattributen für [!DNL Target] {#rtcdp-profile-attributes}

Real-Time CDP-Profilattribute können für [!DNL Target] freigegeben werden, um sie in HTML- und [JSON-Angeboten](/help/main/c-experiences/c-manage-content/create-json-offer.md) zu verwenden.

### Einschränkungen und Überlegungen zu Real-Time CDP-Profilattributen {#limitations}

Beachten Sie Folgendes:

* Attribute innerhalb eines bestimmten Angebots müssen aus derselben [!UICONTROL Experience Platform]-Sandbox stammen. (Anders ausgedrückt: Ein Angebot darf keine Attribute aus verschiedenen [!UICONTROL Experience Platform]-Sandboxes enthalten.)
* Attribute innerhalb eines Angebots können aus verschiedenen Quellen stammen, nämlich aus dem [!DNL Target] und dem [!UICONTROL Experience Platform]. (Mit anderen Worten: Sie können Attribute unabhängig davon kombinieren, ob sie aus [!DNL Target] oder aus dem [!UICONTROL Experience Platform] stammen.)
* Bei der Definition eines Angebots können Sie Standardwerte für [!UICONTROL Real-Time CDP Profile Attributes] zuweisen, falls das Attribut keinen expliziten Wert hat. Wenn beispielsweise eine Einverständnis- oder Governance-Richtlinie das im Personalisierungsdienst verwendete Attribut blockiert, kann stattdessen der Standardwert verwendet werden.
* [!DNL Target] unterstützt nur den Datentyp „Zeichenfolge“ für [!DNL Adobe Experience Platform] Profilattribute, die in Angeboten verwendet werden sollen. Attribute vom Typ „Zuordnung“ und „Array“ werden noch nicht unterstützt.

### JSON-Beispielanwendungsfall

Als Fachkraft für Online-Marketing möchten Sie, dass das AEP/Unified Profile Attributwerte für [!DNL Target] freigibt, um Personalisierung in Echtzeit zu bieten. Durch die Verwendung von [!UICONTROL Real-Time CDP Profile Attributes] können Sie den Wert des Attributs [!UICONTROL Experience Platform] in einem [!DNL Target] Angebot mithilfe von Token-Ersetzung anzeigen. Sie können zum Beispiel anhand der Lieblingsfarbe von Kundinnen und Kunden personalisieren, indem Sie mithilfe der Token `${aep.loyalty.tier}` und `${aep.loyalty.points}` die `${aep.profile.favoriteColor}` oder ihre Treuestufe und ihre Treuepunkte heranziehen.

So erstellen Sie ein JSON-Angebot, um AEP-/Unified Profile-Attribute für [!DNL Target] freizugeben:

1. Wählen [ beim Erstellen eines JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md)Angebots in der **[!UICONTROL Select a source]** Liste **[!UICONTROL Adobe Experience Platform]** aus.
1. Wählen Sie in der **[!UICONTROL Select a profile sandbox name]** die gewünschte Sandbox aus.
1. Wählen Sie aus der Liste **[!UICONTROL Select a profile attribute]** die gewünschten Attribute aus.
1. (Optional) Wählen Sie aus der **[!UICONTROL Insert a default value]** die gewünschten Werte aus.
1. Klicken Sie auf **[!UICONTROL Add]**.

Die folgende Abbildung zeigt, dass zwei Profilattribute, `loyalty.tier` und `loyalty.points`, zum JSON-Angebot hinzugefügt wurden.

![Bild offer-json-aep-shared-attribute](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Links zu weiteren Informationen

Weitere Informationen finden Sie in den folgenden Themen:

* [Ziele - Versionshinweise](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de#destinations){target=_blank} in den *Versionshinweisen zu Adobe Experience Platform*
* [Konfigurieren von Personalisierungszielen für die Personalisierung der gleichen und der nächsten Seite](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html?lang=de){target=_blank} im Handbuch *Ziele - Übersicht*.
* [Adobe Target-](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html?lang=de){target=_blank} im Handbuch *Ziele - Übersicht*
* [Zuordnungsattribute](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=de#map-attributes){target=_blank} im Handbuch *Ziele - Übersicht*.
* [Aktivieren von Zielgruppen für Edge-Personalisierungsziele](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html?lang=de){target=_blank} im Handbuch *Ziele - Übersicht*.
* [Personalisierung der gleichen und der nächsten Seite über die Ziele  [!DNL Adobe Target]  und benutzerdefinierte Personalization](https://experienceleague.adobe.com/docs/experience-platform/destinations/destinations-faq.html?lang=de#same-next-page-personalization?lang=de){target=_blank} unter „Häufig gestellte Fragen“ im Handbuch *Ziele - Übersicht* .

## Videos und Blogposts {#videos-blogs}

Die folgenden Videos und Blogposts enthalten weitere Informationen zur verbesserten Personalisierung mit Target und RTCDP:

### Video: Personalisierung für den nächsten Treffer mit Real-Time CDP und [!DNL Adobe Target]{#RTCDP}

Erfahren Sie, wie Sie mit [!DNL Real-Time Customer Data Platform] und [!DNL Adobe Target] den nächsten Treffer personalisieren können. Das [!DNL Adobe Target]-Ziel in [!DNL Real-Time CDP] ermöglicht Ihnen die Verwendung von [!DNL Experience Platform]-Segmenten in [!DNL Adobe Target] für die Personalisierung derselben Seite und die Personalisierung der nächsten Seite mit Governance- und Datenschutzunterstützung.

Weitere Informationen finden Sie unter [Personalisierung für den nächsten Treffer mit Real-Time CDP und Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html?lang=de){target=_blank} im Handbuch *Platform-Tutorials*.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Video: Konfigurieren des [!DNL Adobe Target]-Ziels in [!DNL Real-Time Customer Data Platform]

Erfahren Sie, wie Sie das [!DNL Adobe Target]-Ziel in [!DNL Real-Time Customer Data Platform] konfigurieren können, um Segmente und Profilattribute von [!DNL Real-Time CDP] an [!DNL Target] zu senden.

>[!VIDEO](https://video.tv.adobe.com/v/3449802/?learn=on&captions=ger)

### Video: Aktivieren von Segmenten und Profilattributen

Erfahren Sie, wie Sie Segmente und Profilattribute von [!DNL Adobe Real-Time Customer Data Platform] für [!DNL Adobe Target] aktivieren, um in Echtzeit personalisierte Inhalte in Ihren Websites, mobilen Apps und anderen digitalen Eigenschaften anzuzeigen.

>[!VIDEO](https://video.tv.adobe.com/v/3447364/?learn=on&captions=ger)

### Video: Verwenden von [!DNL Real-Time CDP]-Segmenten in [!DNL Target]

Erfahren Sie, wie Sie [!DNL Real-Time Customer Data Platform]-Segmente in [!DNL Adobe Target] verwenden, um personalisierte Erlebnisse auf Ihrer Website und in Mobile Apps bereitzustellen.

>[!VIDEO](https://video.tv.adobe.com/v/3446836/?learn=on&captions=ger)

### Video: Verwenden von [!DNL Real-Time CDP]-Profilattribute in [!DNL Adobe Target]

Erfahren Sie, wie Sie [!DNL Adobe Real-Time Customer Data Platform]-Profilattribute in [!DNL Adobe Target] verwenden, um personalisierte Erlebnisse auf Ihrer Website und in Mobile Apps bereitzustellen.

>[!VIDEO](https://video.tv.adobe.com/v/3451902/?learn=on&captions=ger)

### [!DNL Adobe Target]-Blog und -Video: Verbesserte Personalisierung derselben Seite

[[!DNL Adobe] kündigt die optimierte Personalization für dieselbe Seite mit  [!DNL Adobe Target]  und an [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
