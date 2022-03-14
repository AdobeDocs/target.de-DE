---
keywords: at.js; Funktionen; Javascript-Bibliothek
description: Zeigen Sie eine Liste der Funktionen an, die mit den Versionen 1.x und 2.x der at.js-JavaScript-Bibliothek in Adobe Target verwendet werden können.
title: Welche Funktionen kann ich mit at.js verwenden?
feature: at.js
role: Developer
exl-id: a386e478-16f4-4bf6-9771-6b1e75f2e362
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 94%

---

# „at.js“-Funktionen

Liste der Funktionen, die mit der at.js-JavaScript-Bibliothek von Adobe Target verwendet werden können. Klicken Sie in der Spalte „Funktion“ auf die Links, um weitere Informationen und Beispiele zu erhalten.

| Funktion | Details |
| --- | --- | 
| [adobe.target.getOffer(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) | Diese Funktion löst die Anforderung eines Target-Angebots aus. Verwenden Sie sie mit `adobe.target.applyOffer()`, um die Antwort zu verarbeiten, oder verwenden Sie Ihre eigene Methode für die Verarbeitung von „success“. |
| [adobe.target.getOffers(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)<br>(at.js 2.x) | Mit dieser Funktion können Sie mehrere Angebote abrufen, indem Sie mehrere Mboxes übergeben. Darüber hinaus können mehrere Angebote für alle Ansichten in aktiven Aktivitäten abgerufen werden.<br>**Hinweis:** Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*. |
| [adobe.target.applyOffer(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) | Diese Funktion dient zur Anwendung der Antwortinhalte. |
| [adobe.target.applyOffers(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffers-atjs-2.md)<br>(at.js 2.x) | Mit dieser Funktion können Sie mehr als ein Angebot, das von adobe.target.getOffers() abgerufen wurde, anwenden.<br>**Hinweis:** Diese Funktion wurde mit at.js 2.x eingeführt. Diese Funktion steht für at.js Version 1 nicht zur Verfügung.*x*. |
| [adobe.target.triggerView (viewName, options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)<br>(at.js 2.x) | Diese Funktion kann immer aufgerufen werden, wenn eine neue Seite geladen wird oder wenn eine Komponente auf einer Seite erneut wiedergegeben wird.<br>Diese Funktion sollte für Einzelseiten-Apps (SPAs) implementiert werden, um den Visual Experience Composer (VEC) zum Erstellen von A/B-Tests und Erlebnis-Targeting(XT)-Aktivitäten verwenden zu können. |
| [adobe.target.trackEvent(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) | Diese Funktion löst eine Anforderung zum Melden von Benutzeraktionen aus (wie beispielsweise Klicks und Konversionen). Sie übermittelt keine Aktivitäten in der Antwort. |
| [mboxCreate(mbox,params)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)<br>(at.js 1.x) | Führt eine Anforderung aus und wendet das Angebot auf den nächsten DIV-Bereich mit dem Klassennamen „mboxDefault“ an.<br>**Hinweis:** Diese Funktion steht nur für at.js Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird. |
| [mboxDefine(options) und mboxUpdate(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/mboxdefine-mboxupdate-atjs-1x.md)<br>(at.js 1.x) | Mbox definieren und aktualisieren <br>**Hinweis:** Diese Funktion steht nur für at.js Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird. |
| [targetGlobalSettings(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Sie können Einstellungen in der at.js-Bibliothek mithilfe von `targetGlobalSettings()` überschreiben, anstatt die Einstellungen in der Benutzeroberfläche von Target Standard/Premium oder durch Verwendung von REST-APIs zu konfigurieren.<ul><li>Datenanbieter: Mit dieser Einstellung können Kunden Daten von Drittdatenanbietern sammeln, beispielsweise Demandbase, BlueKai und benutzerspezifischen Services, und die Daten an Target als Mbox-Parameter in der globalen Mbox-Anfrage weitergeben.</li></ul> |
| [targetPageParams(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) | Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen. |
| [targetPageParamsAll(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) | Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an alle Mboxes anfügen. |
| [registerExtension(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/registerextension-atjs-1x.md)<br>(at.js 1.x) | Stellt eine Standardart zur Registrierung bestimmter Erweiterungen dar.<br>**Hinweis:** Diese Funktion steht nur für at.js Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird. |
| [Benutzerdefinierte at.js-Ereignisse](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | Benutzerdefinierte at.js-Ereignisse teilen Ihnen mit, wenn eine Mbox-Anforderung oder ein Angebot erfolgreich oder fehlgeschlagen ist. |
| [adobe.target.sendNotifications(options)](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)<br>(at.js 2.1.0) | Diese Funktion sendet eine Benachrichtigung an Target-Edge, wenn ein Erlebnis ohne Verwendung von `adobe.target.applyOffer()` oder `adobe.target.applyOffers()` gerendert wird.<br>**Hinweis**: Diese Funktion wurde mit at.js 2.1.0 eingeführt und steht für alle Versionen höher als 2.1.0 zur Verfügung. |