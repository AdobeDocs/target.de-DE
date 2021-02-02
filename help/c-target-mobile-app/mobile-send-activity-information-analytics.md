---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: In diesem Abschnitt wird beschrieben, wie Sie Adobe Target-Informationen zur Aktivität mobiler Apps zur postAhoc-Segmentierung an Adobe Analytics senden.
title: Aktivitäten an Adobe Analytics senden
feature: Implement Mobile
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 33%

---


# Senden von Aktivitätsinformationen an Adobe Analytics{#send-activity-information-to-adobe-analytics}

In diesem Abschnitt wird beschrieben, wie Sie [!DNL Target] Informationen zur mobilen App-Aktivität zur Post-hoc-Segmentierung an Adobe [!DNL Analytics] senden.

**Voraussetzungen**

* Für diese Integration müssen [!DNL Analytics] und [!DNL Target] mit dem mobilen SDK implementiert werden.
* Stellen Sie sicher, dass Ihre Report Suite für den Empfang von Informationen zur Aktivität von [!DNL Target] aktiviert ist.

   Dies geschieht in der Regel durch Hinzufügen des [!DNL Target]-Clientcodes zur [!DNL Analytics] Report Suite. Dies kann bereits aktiviert sein, wenn Sie die SiteCatalyst-Test&amp;Target-Integration für Webaktivitäten verwenden. Wenden Sie sich an den Kundendienst von Adobe, wenn Sie Fragen zu diesem Schritt haben.

1. Rufen Sie die Aktivitätsinformationen ab.

   Wenn Sie eine Zeichenfolge wie die folgende in Ihren Erlebnisinhalt einschließen, gibt [!DNL Target] die Informationen zur Aktivität zurück, die Sie an [!DNL Analytics] senden können:

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

   In diesem Beispiel wird ein Knoten mit der Variablen `tntVal` hinzugefügt, um die Informationen zur Aktivität abzurufen. Fügen Sie einen ähnlichen Code für die anderen Erlebnisse mit einem passenden Titel und einer passenden Meldung hinzu.

   Diese Zeichenfolge liefert eine Zahl (z. B. 115110:0:0) in der Antwort von [!DNL Target]. Dies zeigt die Aktivitäten-ID, Erlebnis-ID und den Traffic-Typ an. Die folgende Tabelle zeigt eine Beispielantwort von [!DNL Target]:

   ```javascript
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analysieren Sie das JSON-Objekt.

   Analysieren Sie die Antwort, die von [!DNL Target] im Rückruf zurückgegeben wurde. Sie können `NSJSONSerialization` verwenden, um diese Antwort zu analysieren und in einem Wörterbuch oder Array zu speichern.

   Weitere Informationen finden Sie in der [NSJSONSerialization-Dokumentation](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error).

1. Senden Sie die Daten an [!DNL Analytics].

   hinzufügen Sie die Informationen zur analysierten Aktivität (z. B. `tntVal` in der obigen Antwort) in einem [!DNL Analytics]-Aufruf an Ihr Kontextdatenobjekt. Dieser [!DNL Analytics]-Aufruf, der die Kontextdaten enthält, kann sofort ausgelöst werden oder es kann gewartet werden, bis der nächste [!DNL Analytics]-Aufruf ausgelöst wird.

   Dieser Aufruf kann beispielsweise im Callback des Aufrufs `targetLoadRequest` ausgelöst werden:

   ```javascript
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt` ist ein reservierter Ereignisschlüssel im mobilen SDK. Die Post-Klassifizierung der `tntVal`-Variable funktioniert im mobilen SDK genauso wie im Internet (JavaScript). [!DNL Analytics] Nachdem die Informationen in [!DNL Analytics] verarbeitet wurden, sollten Sie die Aktivitäten- und Erlebnisnamen in der [!DNL Analytics]-Schnittstelle sehen.

