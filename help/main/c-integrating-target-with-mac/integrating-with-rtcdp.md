---
keywords: Real-time Customer Data Platform; rtcdp; Personalisierung; aep-Zielgruppen; Adobe Experience Platform-Zielgruppen; Profilattribute
description: Erfahren Sie, wie Sie die  [!DNL Target]/[!DNL Real-time Customer Data Platform] -Integration (RTCDP) zur Bereitstellung umfassenderer Kundendaten und einer wirkungsvolleren Personalisierung nutzen können.
title: Wie kann ich  [!DNL Target]  mit  [!DNL Real-time Customer Data Platform] integrieren?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 21065da5b96413af5d93f2a158137ce3e68e2cf7
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 18%

---

# Integrieren mit [!DNL Real-time Customer Data Platform]

Die auf [!DNL Adobe Experience Platform] basierende [!DNL Real-time Customer Data Platform] (RTCDP) hilft Unternehmen dabei, bekannte und anonyme Daten aus verschiedenen Unternehmensquellen zusammenzuführen, um Kundenprofile zu erstellen, mit denen in Echtzeit personalisierte Kundenerlebnisse auf allen Kanälen und Geräten bereitgestellt werden können.

Weitere Informationen zur RTCDP finden Sie unter [Übersicht über Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank}.

## Verwenden von Zielgruppen aus [!DNL Adobe Experience Platform] {#aep}

Verwenden [Zielgruppen](/help/main/c-target/c-audiences/audiences.md) erstellt in [!DNL Adobe Experience Platform] bietet umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen. Die [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank} (RTCDP), aufbauend auf [!DNL Adobe Experience Platform]unterstützt Unternehmen dabei, bekannte und anonyme Daten aus mehreren Unternehmensquellen zusammenzuführen. Auf diese Weise können Sie Kundenprofile erstellen, mit denen in Echtzeit personalisierte Kundenerlebnisse über alle Kanäle und Geräte hinweg bereitgestellt werden können.

Durch die Verbindung von [!DNL Target] mit [!DNL Real-time Customer Data Platform] können Kunden ihre Web-Personalisierung verbessern, indem sie neue Segmente nutzen, auf die zuvor über [!DNL Target] nicht zugegriffen werden konnte. Dies ermöglicht auf der ersten Seite eines Web-Besuchs Echtzeit-Personalisierung innerhalb von Millisekunden. Verwenden von Zielgruppen und Profilattributen, die in erstellt wurden [!DNL Adobe Experience Platform] ermöglicht Ihnen, die verfügbaren Datenpunkte für eine umfassendere Personalisierung zu erweitern.

Diese Integration entsperrt wichtige Anwendungsfälle mit der Echtzeit-Kundendatenplattform:

* Personalisierung von derselben Seite/nächsten Treffern
* Personalisierung für erstmalige/unbekannte Benutzer

### Wichtigste Funktionen

Zu den wichtigsten Funktionen gehören:

* Direkt [!DNL Target] Integration mit der Echtzeit-Kundendatenplattform/[!DNL Adobe Experience Platform] am Edge (Entfernen der Abhängigkeit von [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations-Karte] mit Governance und Richtliniendurchsetzung
* Echtzeit-CDP-Segmente und freigegebene Profilattribute

### Anwendungsfälle für die Personalisierung

Die folgenden Abschnitte zeigen, welcher Personalisierungs-Anwendungsfall (nächste Sitzung oder dieselbe Seite) bei Verwendung verschiedener Implementierungsmethoden verfügbar ist:

#### at.js-Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] AAM und [!DNL Target]</li><li>[!DNL RTCDP] (Premium oder Ultimate) und [!DNL Target]</li><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM]und [!DNL Target]</li></ul> | Personalisierung der nächsten Sitzung |

#### Adobe Experience Platform Web SDK- oder AEP Server-seitige API-Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL RTCDP] (beliebige SKU) und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><li>Personalisierung auf derselben Seite über Edge</li><li>Governance bei Freigabe von Segmenten erzwungen</li></ul> |
| <ul><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM]und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>[!DNL AAM] Segmente</li><li>Drittanbietersegmente über [!DNL AAM]</li></ul><li>Personalisierung auf derselben Seite über Edge</li><ul><li>[!DNL RTCDP] Segmente</li><li>Governance bei Freigabe von Segmenten erzwungen</li></ul> |

#### Mischung aus [!UICONTROL at.js] und [!DNL Platform Web SDK] Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL RTCDP] (beliebige SKU) und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>Für alle Seiten mit [!UICONTROL at.js]</li></ul><li>Personalisierung auf derselben Seite</li><ul><li>Für alle Seiten mit [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM]und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>Für alle Seiten mit [!UICONTROL at.js]</li><li>[!DNL AAM] Segmente</li><li>Drittanbietersegmente über [!DNL AAM]</li></ul> |

### Segmentauswertungszeit

Die folgende Tabelle zeigt die Segmentbewertungszeit für Ereignisse aus verschiedenen Implementierungsszenarien:

| Szenario | Edge-Segment (Millisekundenbewertung) | Streaming-Segment (Minutenauswertung) | Batch-Segmentbewertung |
| --- | --- | --- | --- |
| Ereignisse/Daten aus [!DNL Adobe Experience Platform] SDKs | Ja | Ja | K. A. |
| Ereignisse aus [!UICONTROL at.js] | Nein | Ja | K. A. |
| Ereignisse aus [!DNL Target Mobile] SDKs | Nein | Ja | K. A. |
| Ereignisse aus dem Batch-Upload | Nein | Nein | Ja |
| Ereignisse aus Offline-Daten (Stream) | Nein | Ja | Ja |

### Links zu weiteren Informationen

Weitere Informationen finden Sie in den folgenden Themen:

* [Ziele - Versionshinweise](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} im *Versionshinweise zu Adobe Experience Platform*
* [Personalisierungsziele für die Personalisierung von derselben Seite und nächsten Seiten konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} im *Ziele - Übersicht* Handbuch.
* [Benutzerdefinierte Personalisierungsverbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} im *Ziele - Übersicht* Handbuch
* [Adobe Target-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html?lang=de){target=_blank} im *Ziele - Übersicht* Handbuch
* [Konfigurieren von Personalisierungszielen für dieselben Anwendungsfälle für die Personalisierung der Seite und der nächsten Seite](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} im *Ziele - Übersicht* Handbuch

## Freigeben von Echtzeit-Kundendatenplattform-Profilattributen für [!DNL Target] {#rtcdp-profile-attributes}

Echtzeit-Kundendatenplattform-Profilattribute können für [!DNL Target] zur Verwendung in HTML-Angeboten und [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Einschränkungen und Überlegungen zu Funktionen und Profilattributen der Echtzeit-Kundendatenplattform

>[!NOTE]
>
>Die Funktion &quot;Echtzeit-Kundendatenplattform-Profilattribute&quot;ist derzeit in der Beta-Version für das HTML von Angeboten und [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Beachten Sie Folgendes:

* Attribute innerhalb eines Angebots müssen aus derselben AEP-Sandbox stammen. (Das heißt, ein Angebot kann keine Attribute aus verschiedenen AEP-Sandboxes enthalten.)
* Attribute innerhalb eines Angebots können aus verschiedenen Quellen stammen. nämlich die [!DNL Target] Profil und das AEP-Profil. (Mit anderen Worten: Sie können Attribute unabhängig davon kombinieren, ob sie von [!DNL Target] oder aus dem AEP-Profil.)
* Beim Definieren eines Angebots können Sie Standardwerte für Echtzeit-Kundendatenplattform-Profilattribute zuweisen, falls das Attribut keinen expliziten Wert aufweist. Wenn beispielsweise eine Zustimmungs- oder Governance-Richtlinie das Attribut blockiert, das im Personalisierungsdienst verwendet wird, kann stattdessen der Standardwert verwendet werden.
* Bei Freigabe werden Echtzeit-Kundendatenplattform-Profilattribute in den Personalisierungsmodellen für künstliche Intelligenz/maschinelles Lernen für [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization] Aktivitäten.

### Anwendungsbeispiel

Als Online-Marketing-Experte möchten Sie, dass das AEP/Unified Profile Attributwerte für [!DNL Target] um eine Echtzeit-Personalisierung zu ermöglichen. Mithilfe von Echtzeit-Kundendatenplattform-Profilattributen können Sie den Wert des AEP-Attributs in einem [!DNL Target] Angebot mit Token-Ersetzung. Sie können zum Beispiel anhand der Lieblingsfarbe eines Kunden personalisieren, indem Sie `${aep.profile.favoriteColor}`oder deren Loyalitäts- und Treuepunktwert mithilfe der Token `${aep.loyalty.tier}` und `${aep.loyalty.points}`.

![offer-json-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

Beachten Sie, dass die Zuweisung von Standardwerten optional ist.

## Videos und Blogbeiträge

Die folgenden Videos und Blogbeiträge enthalten weitere Informationen zur verbesserten Personalisierung mit Target und RTCDP:

### Video: Nächste Hit-Personalisierung mit Echtzeit-Kundendatenplattform und [!DNL Adobe Target]{#RTCDP}

Erfahren Sie, wie Sie den nächsten Treffer personalisieren können mit [!DNL Real-time Customer Data Platform] und [!DNL Adobe Target]. Die [!DNL Adobe Target] Zielort [!DNL Real-time CDP] ermöglicht Ihnen die Verwendung von [!DNL Experience Platform] Segmente in [!DNL Adobe Target] für die gleiche Seitenpersonalisierung und Personalisierung der nächsten Seite mit Governance und Datenschutzunterstützung.

Weitere Informationen finden Sie unter [Nächste Hit-Personalisierung mit Echtzeit-Kundendatenplattform und Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} im *Platform-Tutorials* Handbuch.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Adobe Target-Blog und -Video: Verbesserte Personalisierung auf derselben Seite

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] und [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
