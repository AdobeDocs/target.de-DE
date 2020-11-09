---
keywords: offer;prefetch;iOS;android;sdk;mobile;mobile sdk
description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
title: Vorabruf des Angebotsinhalts
feature: mobile implementation
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 63%

---


# Vorabruf des Angebotsinhalts{#prefetch-offer-content}

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Der gesamte Inhalt wird abgerufen und während des Aufrufs für den Vorabruf im Cache abgelegt, und dieser Inhalt wird bei allen zukünftigen Aufrufen abgerufen, die im Cache abgelegte Inhalte für den spezifizierten mbox-Namen enthalten.

Beachten Sie bei der Verwendung der prefetch-Methode mit den iOS- und Android Mobile SDKs die folgenden Einschränkungen:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.
* Die Funktion &quot;Prefetch&quot;wird nicht unterstützt für [!UICONTROL Traffic-Zuordnungsmethoden für die automatische Zuordnung] und [!UICONTROL automatische Zielgruppe] , für [!UICONTROL Automated Personalization] - oder [!UICONTROL Recommendations] -Aktivitäten oder für [Recommendations-Angebot in einer A/B- oder XT-Aktivität](/help/c-recommendations/recommendations-as-an-offer.md).

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **iOS:**  [Vorab Angebot-Inhalte in iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) in der *Mobile Services iOS SDK-Hilfe* abrufen.
* **Android:**  [Vorab Angebot-Inhalte in Android](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) in der *Mobile Services Android SDK-Hilfe* abrufen.
