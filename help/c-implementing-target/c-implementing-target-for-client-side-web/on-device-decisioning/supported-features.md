---
keywords: Implementierung;JavaScript-Bibliothek;js;ATJS;on-device-Entscheidungsfindung;on-device-Entscheidungsfindung;Unterstützte Funktionen
description: Erfahren Sie, welche Funktionen für die Entscheidungsfindung auf dem Gerät unterstützt werden.
title: Welche Funktionen werden bei der Entscheidung über das Gerät unterstützt?
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
translation-type: tm+mt
source-git-commit: 62a3b387445977a1bdcd2cf45306c8ff032fca50
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 12%

---

# Unterstützte Funktionen für die Entscheidungsfindung auf dem Gerät

Das [!DNL Adobe Target] JS SDK gibt Kunden die Flexibilität, zwischen Leistung und Frische der Daten für Entscheidungen zu wählen. Mit anderen Worten: Wenn die Bereitstellung der relevantesten und interessantesten personalisierten Inhalte über maschinelles Lernen für Sie von größter Bedeutung ist, sollte ein Live-Server-Aufruf durchgeführt werden. Wenn die Leistung jedoch kritischer ist, sollte eine Entscheidung über ein Gerät und einen Speicher getroffen werden. Damit die Entscheidung für das Gerät funktioniert, lesen Sie die folgenden Abschnitte, in denen die unterstützten Funktionen Liste werden.

## Unterstützte Aktivitäten

Die folgende Tabelle zeigt an, welche [Aktivitäten vom [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) oder [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) für gerätebezogene Entscheidungen unterstützt oder nicht unterstützt werden.](/help/c-activities/target-activities-guide.md)

| Aktivitätstyp | Unterstützt? |
| --- | --- |
| [A/B-Test](/help/c-activities/t-test-ab/test-ab.md) | Ja |
| [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nein |
| [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md) ![Premium](/help/assets/premium.png) | Nein |
| [Multivarianz-Tests](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Nein |
| [](/help/c-activities/t-experience-target/experience-target.md)Erlebnis-Targeting (XT) | Ja |
| [Automatisierte ](/help/c-activities/t-automated-personalization/automated-personalization.md) ![Personalisierung Premium](/help/assets/premium.png) | Nein |
| [](/help/c-recommendations/recommendations.md) ![RecommendationsPremium](/help/assets/premium.png) | Nein |
| [Aktivitäten, die Analytics für Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md)  verwenden (A4T) | Ja |

## Audience-Targeting

Die folgende Tabelle zeigt, welche Audiencen für die Geräteentscheidung unterstützt werden oder nicht.

| Audience | Unterstützt? |
| --- | --- |
| [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Ja |
| [Netzwerk](/help/c-target/c-audiences/c-target-rules/network.md) | Nein |
| [Mobile](/help/c-target/c-audiences/c-target-rules/mobile.md) | Nein |
| [Benutzerdefinierte Parameter](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) | Ja |
| [Betriebssystem](/help/c-target/c-audiences/c-target-rules/operating-system.md) | Ja |
| [Seiten der Site](/help/c-target/c-audiences/c-target-rules/site-pages.md) | Ja |
| [Browser](/help/c-target/c-audiences/c-target-rules/browser.md) | Ja |
| [Besucherprofil](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) | Nein |
| [Traffic-Quellen](/help/c-target/c-audiences/c-target-rules/traffic-sources.md) | Nein |
| [Zeitrahmen](/help/c-target/c-audiences/c-target-rules/time-frame.md) | Ja |
| Adobe Experience Cloud-Audiencen<br>(Audiencen von [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] und [!DNL Adobe Experience Manager] | Nein |

### Geo-Targeting für Entscheidungen auf dem Gerät

Um die minimale Latenz bei Aktivitäten zur Entscheidungsfindung auf dem Gerät mit geo-basierten Audiencen zu erhalten, empfiehlt Adobe, die Geowerte selbst im Aufruf von [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) anzugeben. Legen Sie das Geo-Objekt im Kontext der Anforderung fest. Das bedeutet, dass der Browser die Position der einzelnen Besucher bestimmen kann. Beispielsweise können Sie mithilfe eines von Ihnen konfigurierten Dienstes eine IP-zu-Geo-Suche durchführen. Einige Hosting-Anbieter, wie z. B. Google Cloud, stellen diese Funktion über benutzerdefinierte Header in jedem `HttpServletRequest` bereit.

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

Wenn Sie jedoch keine IP-zu-Geo-Suchen auf Ihrem Server durchführen können, aber dennoch eine gerätebezogene Entscheidungsfindung für [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)-Anforderungen durchführen möchten, die geobasierte Audiencen enthalten, wird dies ebenfalls unterstützt. Der Nachteil dieses Ansatzes ist, dass es eine Remote-IP-zu-Geo-Suche verwendet, die jedem `getOffers`-Aufruf Latenz hinzufügt. Diese Latenz sollte geringer als ein `getOffers`-Aufruf mit serverseitiger Entscheidungsfindung sein, da er ein CDN trifft, das sich in der Nähe Ihres Servers befindet. Geben Sie im Geo-Objekt im Kontext Ihrer Anforderung an das SDK nur das Feld &quot;ipAddress&quot;ein, um den geografischen Speicherort der IP-Adresse Ihres Besuchers abzurufen. Wenn zusätzlich zu &quot;ipAddress&quot;ein anderes Feld bereitgestellt wird, ruft das SDK [!DNL Target] die Metadaten zum geografischen Standort nicht zur Auflösung ab.

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

Die folgende Tabelle zeigt, welche Zuordnungsmethoden für die geräteinterne Entscheidungsfindung unterstützt werden oder nicht.

| Zuordnungsmethode | Unterstützt? |
| --- | --- |
| Manuell | Ja |
| [Automatische Zuordnung zu bestem Erlebnis](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nein |
| [Automatische Zielgruppe für personalisierte Erlebnisse](/help/c-activities/auto-target/auto-target-to-optimize.md) | Nein |
