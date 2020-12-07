---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: In diesem Abschnitt wird beschrieben, wie Sie Adobe Target-Informationen zur Aktivität mobiler Apps zur postAhoc-Segmentierung an Adobe Analytics senden.
title: Adobe Target-Aktivitäten an Adobe Analytics senden
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 34%

---


# Senden von Aktivitätsinformationen an Adobe Analytics{#send-activity-information-to-adobe-analytics}

This section describes how to send [!DNL Target] mobile app activity information to Adobe [!DNL Analytics] for post hoc segmentation.

**Voraussetzungen**

* This integration requires that [!DNL Analytics] and [!DNL Target] are implemented using the mobile SDK.
* Ensure that your report suite is enabled to receive activity information from [!DNL Target].

   This is usually done by adding the [!DNL Target] client code to the [!DNL Analytics] report suite. Dies kann bereits aktiviert sein, wenn Sie die SiteCatalyst-Test&amp;Target-Integration für Webaktivitäten verwenden. Wenden Sie sich an den Kundendienst von Adobe, wenn Sie Fragen zu diesem Schritt haben.

1. Rufen Sie die Aktivitätsinformationen ab.

   If you include a string like the following in your experience content, [!DNL Target] returns the activity information that you can send to [!DNL Analytics]:

   ```javascript
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   Ersetzen Sie den Text in Ihrem Erlebnis-JSON-Code beispielsweise durch Folgendes:

   ```javascript
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In this example, a node with the variable `tntVal` is added to obtain the activity information. Fügen Sie einen ähnlichen Code für die anderen Erlebnisse mit einem passenden Titel und einer passenden Meldung hinzu.

   Diese Zeichenfolge liefert eine Zahl (z. B. 115110:0:0) in der Antwort von [!DNL Target]. Dies zeigt die Aktivitäten-ID, Erlebnis-ID und den Traffic-Typ an. The following is a sample response from [!DNL Target]:

   ```javascript
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analysieren Sie das JSON-Objekt.

   Parse the response that came back from [!DNL Target] in the callback. You can use `NSJSONSerialization` to parse this response and store it in a dictionary or an array.

   Weitere Informationen finden Sie in der [NSJSONSerialization-Dokumentation](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) .

1. Send the data to [!DNL Analytics].

   Add the parsed activity information (such as `tntVal` in the above response) to your context data object in an [!DNL Analytics] call. This [!DNL Analytics] call containing the context data can be fired immediately or it can wait until the next [!DNL Analytics] call is fired.

   Dieser Aufruf kann beispielsweise im Callback des Aufrufs `targetLoadRequest` ausgelöst werden:

   ```javascript
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt` ist ein reservierter Ereignisschlüssel im mobilen SDK. Die Post-Klassifizierung der `tntVal`-Variable funktioniert im mobilen SDK genauso wie im Internet (JavaScript). [!DNL Analytics] After the information is processed in [!DNL Analytics], you should see activity and experience names in the [!DNL Analytics] interface.

