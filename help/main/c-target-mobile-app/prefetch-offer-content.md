---
keywords: Angebot;Vorabruf;iOS;Android;SDK;Mobile;Mobile SDK
description: Verwenden der Adobe [!DNL Target] Vorabruffunktion in den iOS- und Android Mobile-SDKs, um so wenig Angebotsinhalte wie möglich abzurufen, indem die Serverantworten im Cache abgelegt werden.
title: Kann ich Angebotsinhalte für mobile Apps vorab abrufen?
feature: Implement Mobile
role: Developer
exl-id: 83a96a41-cf27-4ed8-8169-277f3ef3f249
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 54%

---

# Vorabruf des Angebotsinhalts

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Der gesamte Inhalt wird abgerufen und während des Aufrufs für den Vorabruf im Cache abgelegt, und dieser Inhalt wird bei allen zukünftigen Aufrufen abgerufen, die im Cache abgelegte Inhalte für den spezifizierten mbox-Namen enthalten.

Beachten Sie bei der Verwendung der Vorabruf-Methode mit den iOS- und Android Mobile-SDK die folgenden Einschränkungen:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **iOS:**  [Vorabruf für Angebotsinhalte in iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) im *Hilfe zum Mobile Services iOS SDK*.
* **Android:**  [Vorabruf für Android-Angebotsinhalte](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) im *Hilfe zum Mobile Services Android SDK*.
