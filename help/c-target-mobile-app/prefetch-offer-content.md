---
keywords: Angebot;prefetch;iOS;android;sdk;mobile;mobile SDK
description: Verwenden Sie die Funktion "Adobe [!DNL Target] prefetch"in den iOS- und Android Mobile-SDKs, um Angebot-Inhalte so oft wie möglich abzurufen, indem Sie die Serverantworten zwischenspeichern.
title: Kann ich Angebot-Inhalte für mobile Apps im Voraus abrufen?
feature: Mobile implementieren
role: Developer
exl-id: 83a96a41-cf27-4ed8-8169-277f3ef3f249
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 47%

---

# Vorabruf des Angebotsinhalts

Die [!DNL Target] Vorabruffunktion verwendet die iOS- und Android Mobile-SDKs, um so wenige Angebotsinhalte wie möglich abzurufen, indem sie die Serverantworten zwischenspeichert.

Dieser Prozess reduziert die Ladezeit, verhindert multiple Netzwerkaufrufe und ermöglicht es [!DNL Target], darüber benachrichtigt zu werden, welche Mbox vom Benutzer der mobilen Anwendung besucht wurde. Der gesamte Inhalt wird abgerufen und während des Aufrufs für den Vorabruf im Cache abgelegt, und dieser Inhalt wird bei allen zukünftigen Aufrufen abgerufen, die im Cache abgelegte Inhalte für den spezifizierten mbox-Namen enthalten.

Beachten Sie bei der Verwendung der prefetch-Methode mit den iOS- und Android Mobile SDKs die folgenden Einschränkungen:

* Vorabgerufene Inhalte werden nicht über Starts hinweg behalten. Der Inhalt des vorherigen Artikels wird zwischengespeichert, solange die Anwendung aktiv ist oder bis die `clearPrefetchCache()` Methode aufgerufen wird.
* Die Funktion &quot;Prefetch&quot;wird nicht unterstützt für die Traffic-Zuordnungsmethoden [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe], für die Typen [!UICONTROL Automated Personalization] oder [!UICONTROL Recommendations] oder für [Recommendations-Angebot innerhalb einer A/B- oder XT-Aktivität](/help/c-recommendations/recommendations-as-an-offer.md).

Weitere Informationen einschließlich Vorabruf-Methoden, öffentliche Klassen und Code-Beispiele finden Sie unter:

* **iOS:**  [Vorab Angebot-Inhalte in ](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) iOS in der Hilfe zum  *Mobile Services iOS SDK abrufen*.
* **Android:**  [Vorab Angebot-Inhalte in ](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) Android der  *Mobile Services Android SDK-Hilfe* abrufen.
