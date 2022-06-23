---
keywords: at.js; Funktionen; Javascript-Bibliothek
description: Zeigen Sie eine Liste der Funktionen an, die mit den Versionen 1.x und 2.x der at.js-JavaScript-Bibliothek in Adobe Target verwendet werden können.
title: Welche Funktionen kann ich mit at.js verwenden?
feature: at.js
role: Developer
exl-id: a386e478-16f4-4bf6-9771-6b1e75f2e362
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 78%

---

# „at.js“-Funktionen

Liste der Funktionen, die mit der at.js-JavaScript-Bibliothek von Adobe Target verwendet werden können. Klicken Sie in der Spalte „Funktion“ auf die Links, um weitere Informationen und Beispiele zu erhalten.

| Funktion | Details |
| --- | --- | 
| [adobe.target.getOffer(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/) | Diese Funktion löst die Anforderung eines Target-Angebots aus. Verwenden Sie sie mit `adobe.target.applyOffer()`, um die Antwort zu verarbeiten, oder verwenden Sie Ihre eigene Methode für die Verarbeitung von „success“. |
| [adobe.target.getOffers(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/)<br>(at.js 2.x) | Mit dieser Funktion können Sie mehrere Angebote abrufen, indem Sie mehrere Mboxes übergeben. Darüber hinaus können mehrere Angebote für alle Ansichten in aktiven Aktivitäten abgerufen werden.<br>**Hinweis:** Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*. |
| [adobe.target.applyOffer(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffer/) | Diese Funktion dient zur Anwendung der Antwortinhalte. |
| [adobe.target.applyOffers(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffers-atjs-2/)<br>(at.js 2.x) | Mit dieser Funktion können Sie mehr als ein Angebot, das von adobe.target.getOffers() abgerufen wurde, anwenden.<br>**Hinweis:** Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*. |
| [adobe.target.triggerView (viewName, options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-triggerview-atjs-2/)<br>(at.js 2.x) | Diese Funktion kann immer aufgerufen werden, wenn eine neue Seite geladen wird oder wenn eine Komponente auf einer Seite erneut wiedergegeben wird.<br>Diese Funktion sollte für Einzelseiten-Apps (SPAs) implementiert werden, um den Visual Experience Composer (VEC) zum Erstellen von A/B-Tests und Erlebnis-Targeting(XT)-Aktivitäten verwenden zu können. |
| [adobe.target.trackEvent(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-trackevent/) | Diese Funktion löst eine Anforderung zum Melden von Benutzeraktionen aus (wie beispielsweise Klicks und Konversionen). Sie übermittelt keine Aktivitäten in der Antwort. |
| [mboxCreate(mbox,params)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxcreate-atjs/)<br>(at.js 1.x) | Führt eine Anforderung aus und wendet das Angebot auf den nächsten DIV-Bereich mit dem Klassennamen „mboxDefault“ an.<br>**Hinweis:** Diese Funktion steht nur für at.js Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird. |
| [mboxDefine(options) und mboxUpdate(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxdefine-mboxupdate-atjs-1x/)<br>(at.js 1.x) | Mbox definieren und aktualisieren <br>**Hinweis:** Diese Funktion steht nur für at.js Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird. |
| [targetGlobalSettings(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) | Sie können Einstellungen in der at.js-Bibliothek mithilfe von `targetGlobalSettings()` überschreiben, anstatt die Einstellungen in der Benutzeroberfläche von Target Standard/Premium oder durch Verwendung von REST-APIs zu konfigurieren.<ul><li>Datenanbieter: Mit dieser Einstellung können Kunden Daten von Drittdatenanbietern sammeln, beispielsweise Demandbase, BlueKai und benutzerspezifischen Services, und die Daten an Target als Mbox-Parameter in der globalen Mbox-Anfrage weitergeben.</li></ul> |
| [targetPageParams(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/) | Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen. |
| [targetPageParamsAll(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparamsall/) | Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an alle Mboxes anfügen. |
| [registerExtension(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/registerextension-atjs-1x/)<br>(at.js 1.x) | Stellt eine Standardart zur Registrierung bestimmter Erweiterungen dar.<br>**Hinweis:** Diese Funktion steht nur für at.js Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird. |
| [Benutzerdefinierte at.js-Ereignisse](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-custom-events/) | Benutzerdefinierte at.js-Ereignisse teilen Ihnen mit, wenn eine Mbox-Anforderung oder ein Angebot erfolgreich oder fehlgeschlagen ist. |
| [adobe.target.sendNotifications(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-sendnotifications-atjs-21/)<br>(at.js 2.1.0) | Diese Funktion sendet eine Benachrichtigung an Target-Edge, wenn ein Erlebnis ohne Verwendung von `adobe.target.applyOffer()` oder `adobe.target.applyOffers()` gerendert wird.<br>**Hinweis**: Diese Funktion wurde mit at.js 2.1.0 eingeführt und steht für alle Versionen höher als 2.1.0 zur Verfügung. |
