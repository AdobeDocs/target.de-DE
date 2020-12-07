---
keywords: A4T;Adobe Analytics;Analytics-based activity;Analytics report suite;report suite;Analytics Target integration;configure report suite
description: Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.
title: Implementieren von Analytics for Target
feature: a4t implementation
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 44%

---


# Implementieren von Analytics for Target{#analytics-for-target-implementation}

Several steps are required when implementing [!DNL Adobe Analytics] as the reporting source for [!DNL Target] (A4T).

## Implementation steps {#section_73961BAD5BB4430A95E073DE5C026277}

Die folgenden Abschnitte beschreiben die Schritte, die erforderlich sind, um diese Integration auf Ihrer Site bereitzustellen.

## Schritt 1: Anfordern der Bereitstellung für Analytics und Target

After you implement [!DNL Analytics] as the reporting source for [!DNL Target], you must be provisioned for [!DNL Analytics] and [!DNL Target]. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](http://www.adobe.com/go/audiences).

## Schritt 2: Einrichten der Benutzerberechtigungen

User account requirements must be met before you can create an [!DNL Analytics]-based activity in [!DNL Target]. See [User permission requirements](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Service können Sie Benutzer über [!DNL Adobe Experience Cloud]-Lösungen hinweg identifizieren. Die erforderliche Version der Experience Cloud-Besucher-ID muss implementiert oder migriert werden. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

See [Implement the Experience Cloud ID Service for Target](https://experienceleague.adobe.com/docs/id-service/using/implementation-guides/setup-target.html) in the *Experience Cloud Visitor ID Service* documentation.

## Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Sie müssen die erforderliche Version von appMeasurement.js implementieren oder migrieren. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Informationen zu neuen Implementierungen finden Sie unter Übersicht über die [JavaScript-Implementierung](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) im *Analytics-Implementierungshandbuch*.

Eine Migration finden Sie unter [Migration zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) im *Analytics-Implementierungshandbuch*.

## Schritt 5: &quot;at.js&quot;herunterladen und aktualisieren

Sie müssen die erforderliche Version von at.js mithilfe Ihres Produktionskontos implementieren oder migrieren. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Schritt 6: &quot;at.js&quot;hosten

Wenn Sie zuvor at.js bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

## Step 7: Reference at.js on all site pages {#step7}

Fügen Sie at.js unter VisitorAPI.js ein, indem Sie dem Tag auf jeder Seite die folgende Codezeile hinzufügen:

Für at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

VisitorAPI.js muss unbedingt vor &quot;at.js&quot;geladen werden. Wenn Sie eine vorhandene Datei &quot;at.js&quot;oder &quot;mbox.js&quot;aktualisieren, überprüfen Sie die Ladereihenfolge.

The way the out-of-the-box settings are configured for [!DNL Target] and [!DNL Analytics] integration from an implementation perspective is to use the SDID that is passed from the page to stitch the [!DNL Target] and [!DNL Analytics] request together on the backend automatically for you.

However, if you want more control on how and when to send analytics data related to [!DNL Target] to [!DNL Analytics] for reporting purposes, and you do not want to opt-in to the default settings of having [!DNL Target] and [!DNL Analytics] automatically stitch the analytics data via the SDID, then you can set **analyticsLogging = client_side** via **window.targetGlobalSettings**. Hinweis: Keine Version unter 2.1 unterstützt diesen Ansatz.

Beispiel:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

This set up has a global effect, which means that every call made by at.js will have **analyticsLogging: &quot;client_side&quot;** sent within the [!DNL Target] requests and an analytics payload will be returned for every request. Bei dieser Einstellung sieht das Format der zurückgegebenen Nutzlast wie folgt aus:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)an Analytics weitergeleitet werden. Beachten Sie, dass Sie bei [!UICONTROL Aktivitäten für die automatische Zuordnung] und [!UICONTROL automatische Zielgruppe] auch die sessionId weiterleiten müssen. Weitere Informationen finden Sie im Berichte [zu](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) Analytics for Zielgruppe (A4T) im Handbuch *Adobe Target SDKs* .

Wenn statt einer globalen Einstellung ein situationsbezogener Ansatz gewünscht wird, können Sie die Funktion at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)verwenden, um dies durch Übergabe von,**analyticsLogging: &quot;client_side&quot;** zu erreichen. The analytics payload will be returned for only this call and the [!DNL Target] backend will not forward the payload to [!DNL Analytics]. By pursuing this approach, every at.js [!DNL Target] request will not return the payload by default, but instead only when desired and specified.

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

Die Nutzlast kann dann [!DNL Analytics] über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)an weitergeleitet werden.

## Schritt 8: Validieren der Implementierung {#step8}

Load your pages after you have updated the JavaScript libraries to confirm that the `mboxMCSDID` parameter values in [!DNL Target] calls match the `sdid` parameter value in the [!DNL Analytics] page-view call.

Dies ist besonders für einseitige Anwendungen (Single Page Applications, SPA) wichtig, bei denen die Reihenfolge der Aufrufe nicht immer vorhersehbar ist.

**Hinweis:** Diese Werte müssen übereinstimmen, um die korrekte Funktionsweise von A4T sicherzustellen.

## Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Wir empfehlen, dass Sie die vorherige Integration entfernen, um Ihre Implementierung zu vereinfachen und die Notwendigkeit zur Regelung von Diskrepanzen zwischen den Systemen zu beseitigen. Sie können sämtlichen Code entfernen, den Sie für die vorherige Integration von SC zu T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

## Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

In [!DNL Target], click **[!UICONTROL Administation > Visual Experience Composer]** and choose either **[!UICONTROL Select per activity]** or **[!UICONTROL Adobe Analytics]** to enable the options.

* **[!UICONTROL Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen und beim Erstellen der einzelnen Aktivitäten.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.]**[!DNL Analytics]

