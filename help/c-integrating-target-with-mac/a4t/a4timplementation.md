---
keywords: A4T; Adobe Analytics; Analytics-basierte Aktivität; Analytics Report Suite; Report Suite; Analytics-Target-Integration; Report Suite konfigurieren
description: Führen Sie die erforderlichen Schritte aus, um Analytics for Zielgruppe (A4T) in Ihre Adobe Target- und Adobe Analytics-Lösungen zu implementieren.
title: Wie implementiere ich Analytics für die Zielgruppe (A4T)?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 260492867eb31c59637fc8dff2b8440b5d24c347
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 42%

---


# Implementieren von Analytics for Target{#analytics-for-target-implementation}

Bei der Implementierung von [!DNL Adobe Analytics] als Berichte-Quelle für [!DNL Target] (A4T) sind mehrere Schritte erforderlich.

## Implementierungsschritte {#section_73961BAD5BB4430A95E073DE5C026277}

Die folgenden Abschnitte beschreiben die Schritte, die erforderlich sind, um diese Integration auf Ihrer Site bereitzustellen.

## Schritt 1: Anfordern der Bereitstellung für Analytics und Target

Nachdem Sie [!DNL Analytics] als Berichte-Quelle für [!DNL Target] implementiert haben, müssen Sie für [!DNL Analytics] und [!DNL Target] bereitgestellt werden. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](http://www.adobe.com/go/audiences).

## Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine [!DNL Analytics]-basierte Aktivität in [!DNL Target] erstellen können. Siehe [Anforderungen an Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Service können Sie Benutzer über [!DNL Adobe Experience Cloud]-Lösungen hinweg identifizieren. Die erforderliche Version der Experience Cloud-Besucher-ID muss implementiert oder migriert werden. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Siehe [Implementieren des Experience Cloud-ID-Diensts für Zielgruppe](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) in der *Experience Cloud-Besucher-ID-Dienst*-Dokumentation.

## Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Sie müssen die erforderliche Version von appMeasurement.js implementieren oder migrieren. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Neue Implementierungen finden Sie unter [Übersicht über die JavaScript-Implementierung](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) im *Analytics-Implementierungshandbuch*.

Eine Migration finden Sie unter [Migration zu AppMeasurement for JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) im *Analytics Implementierungshandbuch*.

## Schritt 5: &quot;at.js&quot;herunterladen und aktualisieren

Sie müssen die erforderliche Version von at.js mithilfe Ihres Produktionskontos implementieren oder migrieren. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Schritt 6: &quot;at.js&quot;hosten

Wenn Sie zuvor at.js bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

## Schritt 7: Verweisen Sie auf at.js auf alle Siteseiten {#step7}

Fügen Sie at.js unter VisitorAPI.js ein, indem Sie dem Tag auf jeder Seite die folgende Codezeile hinzufügen:

Für at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

VisitorAPI.js muss unbedingt vor &quot;at.js&quot;geladen werden. Wenn Sie eine vorhandene Datei &quot;at.js&quot;oder &quot;mbox.js&quot;aktualisieren, überprüfen Sie die Ladereihenfolge.

Die vordefinierte Konfiguration der Einstellungen für [!DNL Target] und [!DNL Analytics] aus Implementierungsperspektive besteht darin, die SDID zu verwenden, die von der Seite weitergereicht wird, um die [!DNL Target]- und [!DNL Analytics]-Anforderung automatisch für Sie am Backend zu verknüpfen.

Wenn Sie jedoch mehr Kontrolle darüber haben möchten, wie und wann Analytics-Daten zu [!DNL Target] zu [!DNL Analytics] zu Berichte gesendet werden sollen und Sie nicht auf die Standardeinstellungen [!DNL Target] und [!DNL Analytics] zugreifen möchten, können Sie **analyticsLogging = client_side** über &lt;a6 festlegen/>window.targetGlobalSettings **.** Hinweis: Keine Version unter 2.1 unterstützt diesen Ansatz.

Beispiel:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Dieses Setup hat einen globalen Effekt. Das bedeutet, dass jeder Aufruf von at.js **analyticsLogging hat: &quot;client_side&quot;**, die innerhalb der [!DNL Target]-Anforderungen gesendet werden, und für jede Anforderung wird eine Analytics-Nutzlast zurückgegeben. Bei dieser Einstellung sieht das Format der zurückgegebenen Nutzlast wie folgt aus:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) an Analytics weitergeleitet werden. Beachten Sie, dass Sie für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatische Zielgruppe] auch sessionId weiterleiten müssen. Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T) Berichte](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) im Handbuch *Adobe Target SDKs*.

Wenn statt einer globalen Einstellung ein situationsbezogener Ansatz gewünscht wird, können Sie die Funktion at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)verwenden, um dies durch Übergabe von,**analyticsLogging: &quot;client_side&quot;** zu erreichen. Die Analytics-Nutzlast wird nur für diesen Aufruf zurückgegeben, und das [!DNL Target]-Backend leitet die Nutzlast nicht an [!DNL Analytics] weiter. Bei diesem Ansatz gibt jede Anforderung von at.js [!DNL Target] die Nutzlast nicht standardmäßig zurück, sondern nur, wenn sie gewünscht und angegeben wird.

Beispiel:

```javascript
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

Dieser Aufruf ruft eine Antwort auf, aus der Sie die Analyse-Nutzlast extrahieren können.

Die Antwort sieht wie folgt aus:

```javascript
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) an [!DNL Analytics] weitergeleitet werden.

## Schritt 8: Validieren der Implementierung {#step8}

Laden Sie Ihre Seiten, nachdem Sie die JavaScript-Bibliotheken aktualisiert haben, um sicherzustellen, dass die `mboxMCSDID`-Parameterwerte in [!DNL Target]-Aufrufen mit dem Parameterwert `sdid` im Aufruf [!DNL Analytics] der Ansicht übereinstimmen.

Dies ist besonders für einseitige Anwendungen (Single Page Applications, SPA) wichtig, bei denen die Reihenfolge der Aufrufe nicht immer vorhersehbar ist.

**Hinweis:** Diese Werte müssen übereinstimmen, um die korrekte Funktionsweise von A4T sicherzustellen.

## Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Wir empfehlen, dass Sie die vorherige Integration entfernen, um Ihre Implementierung zu vereinfachen und die Notwendigkeit zur Regelung von Diskrepanzen zwischen den Systemen zu beseitigen. Sie können sämtlichen Code entfernen, den Sie für die vorherige Integration von SC zu T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

## Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration > Visual Experience Composer]** und wählen Sie entweder **[!UICONTROL Pro Aktivität]** oder **[!UICONTROL Adobe Analytics]** aus, um die Optionen zu aktivieren.

* **[!UICONTROL Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen und beim Erstellen der einzelnen Aktivitäten.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.]**[!DNL Analytics]

