---
description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
keywords: Angebot; Vorabruf; iOS; android;sdk;mobile;mobile sdk
seo-description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
seo-title: Vorabruf des Angebotsinhalts
solution: Target
title: Vorabruf des Angebotsinhalts
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: ce8a890d0d662c0eec4d7fe254da371694811822

---


# Vorabruf des Angebotsinhalts{#prefetch-offer-content}

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Der gesamte Inhalt wird abgerufen und während des Aufrufs für den Vorabruf im Cache abgelegt, und dieser Inhalt wird bei allen zukünftigen Aufrufen abgerufen, die im Cache abgelegte Inhalte für den spezifizierten mbox-Namen enthalten.

Beachten Sie Folgendes, wenn mit der Vorabruf-Methode iOS- und Android-Mobile SDKs verwendet werden:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.
* Die Vorabruffunktion in iOS- und Android-Mobile-SDKs wird nicht für die Aktivitätstypen „Automatisches Targeting“, „Automatisierte Zuordnung“ und „Automatisierte Personalisierung“ unterstützt.

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **** iOS:  Angebotsinhalte [in iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) in der *Mobile Services iOS SDK-Hilfe* vorab abrufen.
* **** Android:  Angebotsinhalte [in Android](https://docs.adobe.com/content/help/en/mobile-services/android/target-android/c-mob-target-prefetch-android.html) in der Hilfe zum *Mobile Services-Android-SDK abrufen*.
