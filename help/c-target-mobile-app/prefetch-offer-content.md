---
keywords: offer;prefetch;iOS;android;sdk;mobile;mobile sdk
description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
title: Vorabruf des Angebotsinhalts
feature: mobile implementation
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 62%

---


# Vorabruf des Angebotsinhalts{#prefetch-offer-content}

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Der gesamte Inhalt wird abgerufen und während des Aufrufs für den Vorabruf im Cache abgelegt, und dieser Inhalt wird bei allen zukünftigen Aufrufen abgerufen, die im Cache abgelegte Inhalte für den spezifizierten mbox-Namen enthalten.

Consider the following limitations when using the prefetch method with the iOS and Android Mobile SDKs:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.
* Prefetch functionality is not supported for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] traffic allocation methods, for [!UICONTROL Automated Personalization] or [!UICONTROL Recommendations] activity types, or for [recommendations offers within an A/B or XT activity](/help/c-recommendations/recommendations-as-an-offer.md).

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **iOS:**  [Prefetch offer content in iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) in the *Mobile Services iOS SDK Help*.
* **Android:**  [Prefetch offer content in Android](https://docs.adobe.com/content/help/en/mobile-services/android/target-android/c-mob-target-prefetch-android.html) in the *Mobile Services Android SDK Help*.
