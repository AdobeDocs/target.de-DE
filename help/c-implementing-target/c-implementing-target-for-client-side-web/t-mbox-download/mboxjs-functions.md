---
description: Liste der mbox.js-Funktionen, die bei der Implementierung von mbox.js verwendet werden können.
keywords: mbox-Funktionen
seo-description: Liste der mbox.js-Funktionen, die bei der Implementierung von mbox.js verwendet werden können.
seo-title: „mbox.js“-Funktionen
solution: Target
title: „mbox.js“-Funktionen
uuid: f503bc44-a664-4d09-82dc-80a1198ad9d0
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# „mbox.js“-Funktionen{#mbox-js-functions}

Liste der mbox.js-Funktionen, die bei der Implementierung von mbox.js verwendet werden können.

>[!NOTE]
>
>Sollten Sie [!DNL at.js] verwenden, sind sie nicht für Sie relevant.

| Methode | Hinweise |
|--- |--- |
| `mbox.getName()` |
| `mbox.getURL()` |
| `mbox.getDiv()` | Gibt die mit der mbox verknüpfte Umleitung zurück (Standardinhalt oder ein Angebot) |
| `mbox.getParameters()` | Ein Array von Parametern mit zwei Feldern, Name und Wert |
| `mbox.setOnError()` | Beispiel:<br>`mbox.setOnError(function() { alert(this.getName() +" had error"});` |
| `mbox.setMessage(message)` | Es wird eine Meldung im Debug-Fenster angezeigt. |
| `mboxCurrent.activate()` |
| `mboxCurrent.cancelTimeout()` |
| `mboxCurrent.finalize()` |
| `mboxCurrent.getDefaultDiv()` |
| `mboxCurrent.getDiv()` | Gibt die mit der mbox verknüpfte Umleitung zurück (Standardinhalt oder ein Angebot) |
| `mboxCurrent.getEventTimes()` |
| `mboxCurrent.getFetcher()` |
| `mboxCurrent.getId()` |
| `mboxCurrent.getImportName()` |
| `mboxCurrent.getName()` |
| `mboxCurrent.getOffer()` |
| `mboxCurrent.getParameters()` | Ein Array von Parametern mit zwei Feldern, Name und Wert. |
| `mboxCurrent.getURL()` |
| `mboxCurrent.getURLBuilder()` |
| `mboxCurrent.hide()` |
| `mboxCurrent.isActivated`() |
| `mboxCurrent.load()` |
| `mboxCurrent.loaded()` |
| `mboxCurrent.setEventTime()` |
| `mboxCurrent.setFetcher()` |
| `mboxCurrent.setMessage()` |
| `mboxCurrent.setMessage(message)` | Zeigt eine Meldung im Debug-Fenster an. |
| `mboxCurrent.setOffer()` |
| `mboxCurrent.setOnError()` | Beispiel:<br>`mboxCurrent.setOnError(function(){ alert(this.getName() +" had error"});` |
| `mboxCurrent.setOnLoad()` | Beispiel:<br>`mboxCurrent.setOnLoad(function(){alert(this.getName()+" loaded")});` |
| `mboxCurrent.show()` |
| `mboxCurrent.showContent()` |
| `mboxFactoryDefault.addOnLoad(action)` | Aktion wird aufgerufen, wenn die Seite lädt. |
| `mboxFactoryDefault.getMboxes().each()` | Beispiel:<br>`mboxFactoryDefault.getMboxes().each(function() { alert(mbox.getName()) };` |
| `mboxFactoryDefault.getMboxes().length()` |
| `mboxFactoryDefault.getPageId()` |
| `mboxFactoryDefault.getPCId().getId()` |
| `mboxFactoryDefault.getSessionId().getId()` |
| `mboxFactories.get('default').getSessionId()​.forceId("1276011116668");` |
| `mboxFactories.get('default').getPCId()​.forceId("1276011116668");` |
| `mboxFactoryDefault.create()` |
| `mboxFactoryDefault.disable()` |
| `mboxFactoryDefault.enable()` |
| `mboxFactoryDefault.get()` |
| `mboxFactoryDefault.getCookieManager()` |
| `mboxFactoryDefault.getDisableReason()` |
| `mboxFactoryDefault.getEllapsedTime()` |
| `mboxFactoryDefault.getEllapsedTimeUntil()` |
| `mboxFactoryDefault.getMboxes()` | Gibt eine `mboxList` zurück. |
| `mboxFactoryDefault.getSignaler()` |
| `mboxFactoryDefault.getURLBuilder()` |
| `mboxFactoryDefault.isAdmin()` |
| `mboxFactoryDefault.isDomLoaded()` |
| `mboxFactoryDefault.isEnabled()` |
| `mboxFactoryDefault.isSupported()` |
| `mboxFactoryDefault.limitTraffic()` |
| `mboxFactoryDefault.update()` |
| `mboxFactoryDefault.getCookieManager()​.getCookie("name")//!= null) {` |
| `mboxFactoryDefault.getCookieManager()​.setCookie(_name,_value, _duration);` |