---
description: In diesem Abschnitt wird beschrieben, wie Sie Target Mobile App-Aktivitätsinformationen an Adobe Analytics für postAhoc-Segmentierung senden.
seo-description: In diesem Abschnitt wird beschrieben, wie Sie Target Mobile App-Aktivitätsinformationen an Adobe Analytics für postAhoc-Segmentierung senden.
seo-title: Senden von Aktivitätsinformationen an Adobe Analytics
title: Senden von Aktivitätsinformationen an Adobe Analytics
uuid: 2ca1ebfe-5008-4a73-a032-1ad81f062925
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Senden von Aktivitätsinformationen an Adobe Analytics{#send-activity-information-to-adobe-analytics}

In diesem Abschnitt wird beschrieben, wie Sie Target Mobile App-Aktivitätsinformationen an Adobe Analytics für postAhoc-Segmentierung senden.

**Voraussetzungen**

* Für diese Integration müssen Analytics und Target mit dem mobilen SDK implementiert sein.
* Stellen Sie sicher, dass Ihre Report Suite aktiviert ist, um Aktivitätsinformationen aus Target zu erhalten.

   Dies erfolgt normalerweise durch Hinzufügen des Target-Kunden-Codes zur Analytics Report Suite. Dies kann bereits aktiviert sein, wenn Sie die SiteCatalyst-Test&amp;Target-Integration für Webaktivitäten verwenden. Wenden Sie sich an den Kundendienst von Adobe, wenn Sie Fragen zu diesem Schritt haben.

1. Rufen Sie die Aktivitätsinformationen ab.

   Wenn Sie in Ihren Erlebnisinhalt eine Zeichenfolge wie die folgende einfügen, gibt Target die Kampagneninformationen zurück, die Sie an Analytics senden können:

   ```
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   Ersetzen Sie den Text in Ihrem Erlebnis-JSON-Code beispielsweise durch Folgendes:

   ```
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In diesem Beispiel wird ein Knoten mit der Variable `tntVal` hinzugefügt, um die Aktivitätsinformationen abzurufen. Fügen Sie einen ähnlichen Code für die anderen Erlebnisse mit einem passenden Titel und einer passenden Meldung hinzu.

   Diese Zeichenfolge liefert eine Zahl (z. B. 115110:0:0) in der Antwort von Target. Dies zeigt die Aktivitäts-ID, Erlebnis-ID und den Traffic-Typ an. Es folgt eine Beispielantwort von Target:

   ```
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analysieren Sie das JSON-Objekt.

   Analysieren Sie die Antwort, die von Target im Callback zurückgegeben wurde. Sie können NSJSONSerialization verwenden, um diese Antwort zu analysieren und sie in einem Dict oder Array zu speichern.

   Weitere Informationen finden Sie in der [Dokumentation](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) zu nsjsonserialization.
1. Daten an Analytics senden.

   Fügen Sie die analysierten Aktivitätsinformationen (wie `tntVal` in der obigen Antwort) Ihrem Kontextdatenobjekt in einem Analytics-Aufruf hinzu. Dieser Analytics-Aufruf mit den Kontextdaten kann sofort ausgelöst werden oder warten, bis der nächste Analytics-Aufruf ausgelöst wird.

   Dieser Aufruf kann beispielsweise im Callback des Aufrufs `targetLoadRequest` ausgelöst werden:

   ```
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt` ist ein reservierter Ereignisschlüssel im mobilen SDK. Die Post-Klassifizierung der `tntVal`-Variable in Analytics funktioniert im mobilen SDK genauso wie im Internet (JavaScript). Sobald die Informationen in Analytics verarbeitet werden, sollten Sie Aktivitäten- und Erlebnisnamen in der Benutzeroberfläche von Analytics sehen.

