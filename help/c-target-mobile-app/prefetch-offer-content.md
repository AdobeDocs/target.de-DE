---
keywords: angebot;prefetch;iOS;android;sdk;mobile;mobile SDK
description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
title: Vorzeitiger Abruf des Angebotsinhalts
feature: Implement Mobile
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 60%

---


# Vorabruf des Angebotsinhalts{#prefetch-offer-content}

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Der gesamte Inhalt wird abgerufen und während des Aufrufs für den Vorabruf im Cache abgelegt, und dieser Inhalt wird bei allen zukünftigen Aufrufen abgerufen, die im Cache abgelegte Inhalte für den spezifizierten mbox-Namen enthalten.

Beachten Sie bei der Verwendung der prefetch-Methode mit den iOS- und Android Mobile SDKs die folgenden Einschränkungen:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.
* Die Funktion &quot;Prefetch&quot;wird nicht unterstützt für die Traffic-Zuordnungsmethoden [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe], für die Typen [!UICONTROL Automated Personalization] oder [!UICONTROL Recommendations] oder für [Recommendations-Angebot innerhalb einer A/B- oder XT-Aktivität](/help/c-recommendations/recommendations-as-an-offer.md).

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **iOS:**  [Vorab Angebot-Inhalte in ](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) iOS in der Hilfe zum  *Mobile Services iOS SDK abrufen*.
* **Android:**  [Vorab Angebot-Inhalte in ](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) Android der  *Mobile Services Android SDK-Hilfe* abrufen.
