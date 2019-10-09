---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder kommenden Adobe Target-Versionen enthalten.
keywords: Versionshinweise;Versionen;Aktualisierungen;Zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen
seo-description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
seo-title: Versionshinweise zu Adobe Target
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 9fa095b910b85f244b626c34cacdf9f4a13a6929

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert am: 2. Oktober 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target-Plattform

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Node.js SDK Version 1.0<br>(9. Oktober 2019) | Mit dem SDK "Target Node.js"können Sie Target serverseitig bereitstellen.<br>Dieses Node.js-SDK unterstützt Sie bei der einfachen Integration von Target in andere Experience Cloud-Lösungen, z. B. den Adobe Experience Cloud-Identitätsdienst, Adobe Analytics und Adobe Audience Manager.<br>Das Node.js-SDK stellt Best Practices vor und entfernt Komplexitäten, wenn es über unsere Bereitstellungs-API mit Adobe Target integriert wird, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können. Die folgenden bemerkenswerten Funktionen werden in der neuesten Version eingeführt:<ul><li>Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen.</li><li>Unterstützung für die Leistungsoptimierung, wenn Sie eine hybride Integration von Target sowohl auf Ihren Webseiten als auch serverseitig haben. Wir führen eine Einstellung ein, die von Erlebnissen aufgefüllt wird, die über den Server abgerufen werden, sodass at.js 2.2 keinen zusätzlichen Server-Aufruf mehr vornimmt, um die Erlebnisse abzurufen. `serverState` Dieser Ansatz optimiert die Seitenladeleistung.</li><li> Unterstützung für das Abrufen von VEC-erstellten Aktivitäten über das Node.js SDK, das durch die neue API für die Auslieferung ermöglicht wird.</li><li>Open Source, damit Ihre Entwickler zum Node.js SDK beitragen können.</li></ul>Weitere Informationen finden Sie unter [Versionshinweise - SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)für Target Node.js. |
| Auslieferungs-API<br>(9. Oktober 2019) | Ein vollständig neuer API-Endpunkt (/v1/delivery) wird in der Produktion verfügbar sein. Die wichtigsten Funktionen sind:<ul><li>Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.</li><li>Rufen Sie VEC-erstellte Aktivitäten über die API ab.</li><li>Unterstützung für ein völlig neues Objekt namens "Ansichten", das für Einzelseitenanwendungen (SPAs) und mobile Anwendungen verwendet wird.</li></ul>Weitere Informationen finden Sie unter [Versionshinweise - Serverseitige Target-APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |
| at.js Version 2.2<br><br>andat.js Version 1.8<br>(zu bestimmende Datumswerte) | Diese Versionen von at.js bieten:<ul><li>Verbesserte Leistung bei der Verwendung von Experience Cloud ID Service (ECID) Version 4.4 und at.js 2.2 oder at.js 1.8 auf Ihren Webseiten.</li><li>Zuvor führte die ECID zwei Sperraufrufe durch, bevor at.js Erlebnisse abrufen konnte. Dies wurde auf einen einzigen Aufruf reduziert, wodurch die Leistung deutlich verbessert wird.</li></ul> Um diese Leistungsverbesserungen zu nutzen, müssen Sie auf "at.js 2.2"oder "at.js 1.8"sowie auf "ECID Library v4.4"aktualisieren. |


## Target Standard/Premium 19.10.1 (22. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) Benutzerbasierte Empfehlungen | Empfiehlt Artikel basierend auf dem Browsing, der Anzeige und dem Kaufverlauf jedes Besuchers. Diese Elemente werden allgemein als "Empfohlen für Sie"bezeichnet.<br>Mithilfe dieser Kriterien können Sie personalisierte Inhalte und Erlebnisse sowohl für neue als auch für wiederkehrende Besucher bereitstellen. Die Liste der Empfehlungen wird mit der neuesten Aktivität des Besuchers gewichtet und wird während der Sitzung aktualisiert und personalisiert, wenn der Besucher Ihre Site aufsucht. |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
