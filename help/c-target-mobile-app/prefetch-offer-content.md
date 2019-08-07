---
description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
keywords: Angebot; Vorabruf; iOS; android; sdk; mobile; mobile SDK
seo-description: Die Vorabruffunktion von Adobe Target verwendet iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalt wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
seo-title: Vorabruf des Angebotsinhalts
solution: Target
title: Vorabruf des Angebotsinhalts
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: 95bf4b2070cc2de235ac09ac164f0f9ec48dd6cd

---


# Vorabruf des Angebotsinhalts{#prefetch-offer-content}

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Während des Prefetch-Aufrufs wird der gesamte Inhalt abgerufen und zwischengespeichert. Dieser Inhalt wird aus dem Cache für alle zukünftigen Aufrufe abgerufen, die zwischengespeicherte Inhalte für den angegebenen mbox-Namen enthalten.

Berücksichtigen Sie Folgendes, wenn Sie in der prefetch-Methode mit den ios- und Android Mobile sdks verwendet werden:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.
* Die Funktion zum Vorausholen von Funktionen in ios- und Android Mobile-sdks wird nicht für Aktivitätstypen "Auto-Targeting" ," Automatisierte Zuordnung" und "Automatisierte Personalisierung" unterstützt.

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **iOS.**[Vorzeitiger Abruf des Angebotsinhalts in iOS](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_mob_target-prefetch_ios.html) im Handbuch zu *iOS-SDK 4.x für Experience Cloud-Lösungen*.
* **Android:**[Vorzeitiger Abruf des Angebotsinhalts in Android](https://marketing.adobe.com/resources/help/en_US/mobile/android/c_mob_target-prefetch_android.html) im Handbuch zu *Android-SDK 4.x für Experience Cloud-Lösungen*.
