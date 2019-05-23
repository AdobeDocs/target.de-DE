---
description: Liste der Funktionen, die für „at.js“ verwendet werden können
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Liste der Funktionen, die mit der at.js-JavaScript-Bibliothek in Adobe Target verwendet werden können.
seo-title: Adobe Target at.js-Funktionen
solution: Target
subtopic: Erste Schritte
title: „at.js“-Funktionen
topic: Standard
uuid: ec5f27a7-b22a-48c9-968c-9eb02830a2a6
translation-type: tm+mt
source-git-commit: c607b241afb535f324cd1357c8784a88fb183658

---


# „at.js“-Funktionen{#at-js-functions}

Liste der Funktionen, die mit der at.js-JavaScript-Bibliothek von Adobe Target verwendet werden können. Klicken Sie in der Spalte &quot;Funktion&quot; auf die Links, um weitere Informationen und Beispiele zu erhalten.

| Funktion | Details |
| --- | --- | 
| [adobe.target.getOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) | Diese Funktion löst die Anforderung eines Target-Angebots aus. Verwenden Sie sie mit `adobe.target.applyOffer()`, um die Antwort zu verarbeiten, oder verwenden Sie Ihre eigene Methode für die Verarbeitung von „success“.  |
| [adobe. target. getoffers (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)<br>(at. js 2. x) | Mit dieser Funktion können Sie mehrere Angebote abrufen, indem Sie mehrere Mboxes übergeben. Darüber hinaus können mehrere Angebote für alle Ansichten in aktiven Aktivitäten abgerufen werden.<br>**Hinweis:** Diese Funktion wurde mit at. js 2. x eingeführt. Diese Funktion steht für at. js Version 1 nicht zur Verfügung.*x*. |
| [adobe.target.applyOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) | Diese Funktion dient zur Anwendung der Antwortinhalte. |
| [adobe. target. applyoffer (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffers-atjs-2.md)<br>(at. js 2. x) | Mit dieser Funktion können Sie mehr als ein Angebot anwenden, das von adobe. target. getoffers () abgerufen wurde.<br>**Hinweis:** Diese Funktion wurde mit at. js 2. x eingeführt. Diese Funktion steht für at. js Version 1 nicht zur Verfügung.*x*. |
| [adobe. target. triggerview (viewname, options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)<br>(at. js 2. x) | Diese Funktion kann immer aufgerufen werden, wenn eine neue Seite geladen wird oder wenn eine Komponente auf einer Seite erneut wiedergegeben wird.<br> Diese Funktion sollte für Einzelseitenanwendungen (spas) implementiert werden, um den Visual Experience Composer (VEC) zum Erstellen von A/B-Tests und Erlebnis-Targeting (XT)-Aktivitäten zu verwenden. |
| [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) | Diese Funktion löst eine Anforderung zum Melden von Benutzeraktionen aus (wie beispielsweise Klicks und Konversionen). Sie übermittelt keine Aktivitäten in der Antwort. |
| [Mboxcreate (mbox, params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)<br>(at. js 1. x) | Führt eine Anforderung aus und wendet das Angebot auf den nächsten DIV-Bereich mit dem Klassennamen „mboxDefault“ an.<br>**Hinweis:** Diese Funktion steht für at. js-Versionen 1 zur Verfügung.*x*, zur Verfügung. Diese Funktion wurde mit der Veröffentlichung von at. js 2. x veraltet. Diese Funktion gibt Standardinhalt zurück, wenn sie mit at. js 2. x verwendet wird. |
| [Mboxdefine (options) und mboxupdate (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxdefine-mboxupdate-atjs-1x.md)<br>(at. js 1. x) | Mbox definieren und aktualisieren<br>**Hinweis:** Diese Funktion steht für at. js-Versionen 1 zur Verfügung.*x*, zur Verfügung. Diese Funktion wurde mit der Veröffentlichung von at. js 2. x veraltet. Diese Funktion gibt Standardinhalt zurück, wenn sie mit at. js 2. x verwendet wird. |
| [Targetglobalsettings (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Sie können Einstellungen in der &quot;at. js&quot; -Bibliothek überschreiben, `targetGlobalSettings()`anstatt die Einstellungen in der Benutzeroberfläche von Target Standard/Premium oder durch Verwendung von REST-apis zu konfigurieren.<ul><li>Datenanbieter: Mit dieser Einstellung können Kunden Daten von Drittanbietern von Daten erfassen, wie Demandbase, bluekai und benutzerdefinierte Dienste, und die Daten als Mbox-Parameter in der globalen Mbox-Anfrage an Target weiterleiten.</li></ul> |
| [Targetpageparams (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) | Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an die globale Mbox anfügen. |
| [Targetpageparamsall (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) | Mit dieser Methode können Sie Parameter von außerhalb des Anforderungscodes an alle Mboxes anfügen. |
| [Registerextension (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/registerextension-atjs-1x.md)<br>(at. js 1. x) | Stellt eine Standardart zur Registrierung bestimmter Erweiterungen dar.<br>**Hinweis:** Diese Funktion steht für at. js-Versionen 1 zur Verfügung.*x*, zur Verfügung. Diese Funktion wurde mit der Veröffentlichung von at. js 2. x veraltet. Diese Funktion gibt Standardinhalt zurück, wenn sie mit at. js 2. x verwendet wird. |
| [Benutzerdefinierte at.js-Ereignisse](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | benutzerdefinierte at. js-Ereignisse teilen Ihnen mit, wenn eine Mbox-Anforderung oder ein Angebot erfolgreich oder fehlgeschlagen ist. |
