---
keywords: Real-time Customer Data Platform; rtcdp; Personalisierung; aep-Zielgruppen; Adobe Experience Platform-Zielgruppen; Profilattribute
description: Erfahren Sie, wie Sie die  [!DNL Target]/[!DNL Real-Time Customer Data Platform] -Integration (RTCDP) zur Bereitstellung umfassenderer Kundendaten und einer wirkungsvolleren Personalisierung nutzen können.
title: Wie kann ich  [!DNL Target]  mit  [!DNL Real-Time Customer Data Platform] integrieren?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 08422323607f7238a7cf9bac5b863032ce734662
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 9%

---

# Integrieren mit [!DNL Real-Time Customer Data Platform]

Erstellt auf [!DNL Adobe Experience Platform], [!DNL Real-Time Customer Data Platform] (RTCDP) hilft Unternehmen, bekannte und anonyme Daten aus mehreren Unternehmensquellen zusammenzuführen. Mit der RTCDP können Sie Kundenprofile erstellen, mit denen Sie personalisierte Kundenerlebnisse über alle Kanäle und Geräte hinweg in Echtzeit bereitstellen können.

Weitere Informationen zur RTCDP finden Sie unter [Übersicht über Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank}.

## Wichtigste Funktionen

Zu den wichtigsten Funktionen gehören:

* Direkt [!DNL Target] Integration mit Real-Time CDP/[!DNL Adobe Experience Platform] am Edge (Entfernen der Abhängigkeit von [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations-Karte] mit Governance und Richtliniendurchsetzung
* Echtzeit-CDP-Segmente und freigegebene Profilattribute

## Implementierungsszenarien

Die folgenden Abschnitte zeigen, welcher Personalisierungs-Anwendungsfall (nächste Sitzung oder dieselbe Seite) bei Verwendung verschiedener Implementierungsmethoden verfügbar ist:

### at.js-Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] AAM und [!DNL Target]</li><li>[!DNL RTCDP] (Premium oder Ultimate) und [!DNL Target]</li><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM]und [!DNL Target]</li></ul> | Personalisierung der nächsten Sitzung |

### [!DNL Adobe Experience Platform Web SDK] oder [!DNL Experience Platform Server-Side API] Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL RTCDP] (beliebige SKU) und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><li>Personalisierung auf derselben Seite über Edge</li><li>Governance bei Freigabe von Segmenten erzwungen</li></ul> |
| <ul><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM]und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>[!DNL AAM] Segmente</li><li>Drittanbietersegmente über [!DNL AAM]</li></ul><li>Personalisierung auf derselben Seite über Edge</li><ul><li>[!DNL RTCDP] Segmente</li><li>Governance bei Freigabe von Segmenten erzwungen</li></ul> |

### Mischung aus [!UICONTROL at.js] und [!DNL Platform Web SDK] Implementierung

| „Lösungen“ | Anwendungsfall aktiviert |
| --- | --- |
| <ul><li>[!DNL RTCDP] (beliebige SKU) und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>Für alle Seiten mit [!UICONTROL at.js]</li></ul><li>Personalisierung auf derselben Seite</li><ul><li>Für alle Seiten mit [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (beliebige SKU), [!DNL AAM]und [!DNL Target]</li></ul> | <ul><li>Personalisierung der nächsten Sitzung</li><ul><li>Für alle Seiten mit [!UICONTROL at.js]</li><li>[!DNL AAM] Segmente</li><li>Drittanbietersegmente über [!DNL AAM]</li></ul> |

## Segmentauswertungszeit

Die folgende Tabelle zeigt die Segmentbewertungszeit für Ereignisse aus verschiedenen Implementierungsszenarien:

| Szenario | Edge-Segment (Millisekundenbewertung) | Streaming-Segment (Minutenauswertung) | Batch-Segmentbewertung |
| --- | --- | --- | --- |
| Ereignisse/Daten aus [!DNL Adobe Experience Platform] SDKs | Ja | Ja | K. A. |
| Ereignisse aus [!UICONTROL at.js] | Nein | Ja | K. A. |
| Ereignisse aus [!DNL Target Mobile] SDKs | Nein | Ja | K. A. |
| Ereignisse aus dem Batch-Upload | Nein | Nein | Ja |
| Ereignisse aus Offline-Daten (Stream) | Nein | Ja | Ja |

## Verwenden von Zielgruppen aus [!DNL Adobe Experience Platform] {#aep}

Verwenden [Zielgruppen](/help/main/c-target/c-audiences/audiences.md) erstellt in [!DNL Adobe Experience Platform] bietet umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen. Die [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank} (RTCDP), aufbauend auf [!DNL Adobe Experience Platform]unterstützt Unternehmen dabei, bekannte und anonyme Daten aus mehreren Unternehmensquellen zusammenzuführen. Auf diese Weise können Sie Kundenprofile erstellen, mit denen in Echtzeit personalisierte Kundenerlebnisse über alle Kanäle und Geräte hinweg bereitgestellt werden können.

Durch Verbinden [!DNL Target] der [!DNL Real-Time Customer Data Platform], können Kunden ihre Web-Personalisierung anreichern. Mit dieser Integration können Sie neue Segmente entsperren, auf die zuvor möglicherweise nicht zugegriffen wurde. [!DNL Target] , um die Echtzeit-Millisekunde-Personalisierung auf der ersten Seite des Webbesuchs eines Kunden zu aktivieren. Verwenden von Zielgruppen und Profilattributen, die in erstellt wurden [!DNL Adobe Experience Platform] ermöglicht Ihnen, die verfügbaren Datenpunkte für eine umfassendere Personalisierung zu erweitern.

Diese Integration entsperrt wichtige Anwendungsfälle mit Real-Time CDP:

* Personalisierung von derselben Seite/nächsten Treffern
* Personalisierung für erstmalige/unbekannte Benutzer

## Freigeben von Real-Time CDP-Profilattributen für [!DNL Target] {#rtcdp-profile-attributes}

Real-Time CDP-Profilattribute können für [!DNL Target] zur Verwendung in HTML-Angeboten und [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Einschränkungen und Überlegungen zu Real-Time CDP-Profilattributen

>[!NOTE]
>
>Die Real-Time CDP-Profilattribute-Funktion ist in der Beta-Version für das HTML von Angeboten und [JSON-Angebote](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Beachten Sie Folgendes:

* Attribute innerhalb eines Angebots müssen aus demselben stammen [!UICONTROL Experience Platform] Sandbox. (Anders ausgedrückt: Ein Angebot darf keine Attribute aus verschiedenen [!UICONTROL Experience Platform] Sandboxes.)
* Attribute innerhalb eines Angebots können aus verschiedenen Quellen stammen. nämlich die [!DNL Target] und [!UICONTROL Experience Platform] Profil. (Mit anderen Worten: Sie können Attribute unabhängig davon kombinieren, ob sie von [!DNL Target] oder von [!UICONTROL Experience Platform] profile.)
* Bei der Definition eines Angebots können Sie Standardwerte für [!UICONTROL Real-Time CDP-Profilattribute], falls das Attribut keinen expliziten Wert aufweist. Wenn beispielsweise eine Zustimmungs- oder Governance-Richtlinie das Attribut blockiert, das im Personalisierungsdienst verwendet wird, kann stattdessen der Standardwert verwendet werden.

### JSON-Beispielanwendungsfall

Als Online-Marketing-Experte möchten Sie, dass das AEP/Unified Profile Attributwerte für [!DNL Target] zur Echtzeit-Personalisierung. Durch Verwendung von [!UICONTROL Real-Time CDP-Profilattribute]können Sie den Wert der [!UICONTROL Experience Platform] -Attribut [!DNL Target] Angebot mit Token-Ersetzung. Sie können zum Beispiel anhand der Lieblingsfarbe eines Kunden personalisieren, indem Sie `${aep.profile.favoriteColor}`oder deren Loyalitäts- und Treuepunktwert mithilfe der Token `${aep.loyalty.tier}` und `${aep.loyalty.points}`.

So erstellen Sie ein JSON-Angebot, um AEP-/Unified Profile-Attribute für [!DNL Target]:

1. while [Erstellen eines JSON-Angebots](/help/main/c-experiences/c-manage-content/create-json-offer.md)aus der **[!UICONTROL Quelle auswählen]** Liste auswählen **[!UICONTROL Adobe Experience Platform]**.
1. Aus dem **[!UICONTROL Profil-Sandbox-Namen auswählen]** auswählen, wählen Sie die gewünschte Sandbox aus.
1. Aus dem **[!UICONTROL Profilattribut auswählen]** Liste die gewünschten Attribute auswählen.
1. (Optional) Wählen Sie im **[!UICONTROL Standardwert einfügen]** die gewünschten Werte aus.
1. Klicken Sie auf **[!UICONTROL Hinzufügen]**.

Die folgende Abbildung zeigt zwei Profilattribute: `loyalty.tier` und `loyalty.points` wurden zum JSON-Angebot hinzugefügt.

![offer-json-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Links zu weiteren Informationen

Weitere Informationen finden Sie in den folgenden Themen:

* [Ziele - Versionshinweise](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} im *Versionshinweise zu Adobe Experience Platform*
* [Personalisierungsziele für die Personalisierung von derselben Seite und nächsten Seiten konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} im *Ziele - Übersicht* Handbuch.
* [Adobe Target-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html?lang=de){target=_blank} im *Ziele - Übersicht* Handbuch
* [Zuordnungsattribute](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=en#map-attributes){target=_blank} im *Ziele - Übersicht* Handbuch.

## Videos und Blogbeiträge

Die folgenden Videos und Blogbeiträge enthalten weitere Informationen zur verbesserten Personalisierung mit Target und RTCDP:

### Video: Personalisierung mit Real-Time CDP als Nächstes und [!DNL Adobe Target]{#RTCDP}

Erfahren Sie, wie Sie den nächsten Treffer personalisieren können mit [!DNL Real-Time Customer Data Platform] und [!DNL Adobe Target]. Die [!DNL Adobe Target] Zielort [!DNL Real-Time CDP] ermöglicht Ihnen die Verwendung von [!DNL Experience Platform] Segmente in [!DNL Adobe Target] für die gleiche Seitenpersonalisierung und Personalisierung der nächsten Seite mit Governance und Datenschutzunterstützung.

Weitere Informationen finden Sie unter [Nächste Hit-Personalisierung mit Real-Time CDP und Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} im *Platform-Tutorials* Handbuch.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### [!DNL Adobe Target] Blog und Video: Verbesserte Personalisierung auf derselben Seite

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] und [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
