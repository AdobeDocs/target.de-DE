---
keywords: Implementierung;JavaScript-Bibliothek;js;at.js;On-Device Decisioning;bei Geräteentscheidungen;unterstützte Funktionen
description: Erfahren Sie, welche Funktionen für die Entscheidungsfindung auf dem Gerät unterstützt werden.
title: Welche Funktionen werden bei der On-Device-Entscheidungsfindung unterstützt?
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 13%

---

# Unterstützte Funktionen für die geräteinterne Entscheidungsfindung

Die [!DNL Adobe Target] Das JS-SDK bietet Kunden die Möglichkeit, für Entscheidungen zwischen Leistung und Aktualisierung von Daten zu wählen. Sollte Ihnen also die Bereitstellung der relevantesten und ansprechendsten personalisierten Inhalte über maschinelles Lernen am wichtigsten sein, sollte ein Live-Server-Aufruf durchgeführt werden. Wenn die Leistung jedoch kritischer ist, sollte eine Entscheidung auf dem Gerät und im Speicher getroffen werden. Die Entscheidungsfindung auf dem Gerät funktioniert in den folgenden Abschnitten, in denen die unterstützten Funktionen aufgelistet sind.

## Unterstützte Aktivitätstypen

Die folgende Tabelle zeigt, [Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) erstellt von [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) oder [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) werden für die Entscheidungsfindung auf dem Gerät unterstützt oder nicht unterstützt.

| Aktivitätstyp | Unterstützt? |
| --- | --- |
| [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nein |
| [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) ![Premium](/help/main/assets/premium.png) | Nein |
| [Multivariate Tests](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Nein |
| [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) (XT) | Ja |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) ![Premium](/help/main/assets/premium.png) | Nein |
| [Recommendations](/help/main/c-recommendations/recommendations.md) ![Premium](/help/main/assets/premium.png) | Nein |
| [Aktivitäten mit Analytics für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Ja |

## Zielgruppen-Targeting

Die folgende Tabelle zeigt, welche Zielgruppenregeln für die Entscheidungsfindung auf dem Gerät unterstützt oder nicht unterstützt werden.

| Zielgruppenregel | Unterstützt? |
| --- | --- |
| [Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md) | Ja |
| [Netzwerk](/help/main/c-target/c-audiences/c-target-rules/network.md) | Nein |
| [Mobile](/help/main/c-target/c-audiences/c-target-rules/mobile.md) | Nein |
| [Benutzerdefinierte Parameter](/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md) | Ja |
| [Betriebssystem](/help/main/c-target/c-audiences/c-target-rules/operating-system.md) | Ja |
| [Seiten der Site](/help/main/c-target/c-audiences/c-target-rules/site-pages.md) | Ja |
| [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) | Ja |
| [Besucherprofil](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) | Nein |
| [Traffic-Quellen](/help/main/c-target/c-audiences/c-target-rules/traffic-sources.md) | Nein |
| [Zeitrahmen](/help/main/c-target/c-audiences/c-target-rules/time-frame.md) | Ja |
| Adobe Experience Cloud-Zielgruppen<br>(Zielgruppen aus [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]und [!DNL Adobe Experience Manager] | Nein |

### Geotargeting für Entscheidungen auf Geräten

Um eine minimale Latenz für Entscheidungsaktivitäten auf dem Gerät mit geobasierten Zielgruppen zu erhalten, empfiehlt Adobe, die Geowerte selbst im Aufruf von anzugeben. [getOffers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md). Legen Sie das Geo-Objekt im Kontext der Anforderung fest. Das bedeutet, dass der Browser die Position jedes Besuchers ermitteln kann. Sie können beispielsweise mithilfe eines von Ihnen konfigurierten Dienstes eine IP-zu-Geo-Suche durchführen. Einige Hosting-Provider, wie z. B. Google Cloud, bieten diese Funktionalität über benutzerdefinierte Header in jedem `HttpServletRequest`.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				city: "SAN FRANCISCO", 
				countryCode: "US", 
				stateCode: "CA", 
				latitude: 37.75, 
				longitude: -122.4 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

Wenn Sie jedoch keine IP-zu-Geo-Suchen auf Ihrem Server durchführen können, aber dennoch eine geräteübergreifende Entscheidungsfindung für [getOffers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) Anforderungen, die geobasierte Zielgruppen enthalten, wird dies ebenfalls unterstützt. Der Nachteil dieses Ansatzes besteht darin, dass eine Remote-IP-zu-Geo-Suche verwendet wird, wodurch Latenzzeiten zu jedem `getOffers` aufrufen. Diese Latenz sollte kleiner sein als `getOffers` mit serverseitiger Entscheidungsfindung aufrufen, da es ein CDN trifft, das sich in der Nähe Ihres Servers befindet. Geben Sie nur das Feld &quot;ipAddress&quot;im Geo-Objekt im Kontext Ihrer SDK-Anfrage an, um den geografischen Standort der IP-Adresse Ihres Besuchers abzurufen. Wenn ein anderes Feld zusätzlich zur &quot;ipAddress&quot;angegeben wird, wird die [!DNL Target] Das SDK ruft die Metadaten für den geografischen Standort nicht zur Auflösung ab.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				ipAddress: "127.0.0.1" 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

### Zuordnungsmethode

Die folgende Tabelle zeigt, welche Zuordnungsmethoden für die Entscheidungsfindung auf dem Gerät unterstützt oder nicht unterstützt werden.

| Zuordnungsmethode | Unterstützt? |
| --- | --- |
| Manuell | Ja |
| [Automatisch dem besten Erlebnis zuordnen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nein |
| [Automatisches Targeting für personalisierte Erlebnisse](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nein |
