---
description: Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.
keywords: A4T; Adobe Analytics; Analytics-basierte Aktivität; Analytics Report Suite; Report Suite; Analytics-Target-Integration; Report Suite konfigurieren
seo-description: Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.
seo-title: Implementieren von Analytics for Target
solution: Target
title: Implementieren von Analytics for Target
topic: Premium
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Implementieren von Analytics for Target{#analytics-for-target-implementation}

Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.

## Implementierungsschritte {#section_73961BAD5BB4430A95E073DE5C026277}

In der folgenden Tabelle werden die Schritte beschrieben, die für die Bereitstellung dieser Integration auf Ihrer Site ausgeführt werden müssen.

## Schritt 1: Anfordern der Bereitstellung für Analytics und Target

Nach der Implementierung von Analytics als Berichtsquelle für Target sind Sie auf die Bereitstellung von Analytics und Target angewiesen. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](http://www.adobe.com/go/audiences).

## Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine Adobe Analytics-basierte Aktivität in Adobe Target erstellen können. Siehe  [Anforderungen hinsichtlich Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Service können Sie Benutzer über Experience Cloud-Lösungen hinweg identifizieren. Die erforderliche Version der Experience Cloud-Besucher-ID muss implementiert oder migriert werden. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Informationen finden Sie unter [Implementieren des Experience Cloud ID-Service mit Target](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/setup-target.html) in der Dokumentation zum Experience Cloud-Besucher-ID-Service.

## Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Sie müssen die erforderliche Version von appMeasurement.js implementieren oder migrieren. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Informationen zu neuen Implementierungen finden Sie unter Übersicht über die [JavaScript-Implementierung](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) im *Analytics-Implementierungshandbuch*.

Eine Migration finden Sie unter [Migration zu AppMeasurement für JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) im *Analytics-Implementierungshandbuch*.

## Schritt 5: Herunterladen und Aktualisieren von at.js oder mbox.js

Sie müssen die erforderliche Version von at.js oder mbox.js mithilfe des Produktionskontos migrieren oder implementieren. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Schritt 6: Hosten von at.js oder mbox.js

Wenn Sie at.js oder mbox.js zuvor bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

## Schritt 7: Verweisen auf at.js oder mbox.js auf allen Seiten der Website  {#step7}

Fügen Sie at.js oder mbox.js unterhalb von VisitorAPI.js ein, indem Sie die folgende Codezeile zum Tag auf den einzelnen Seiten hinzufügen:

Für at.js:

```
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Für mbox.js:

```
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

Es ist wichtig, dass VisitorAPI.js vor at.js oder mbox.js geladen wird. Achten Sie daher beim Aktualisieren einer vorhandenen at.js- oder mbox.js-Datei darauf, dass die richtige Ladereihenfolge festgelegt ist.

Zur Implementierung sind die nativen Einstellungen für die Target- und Analytics-Integration so konfiguriert, dass die von der Seite übermittelte SDID verwendet wird, um die Target- und Analytics-Anfrage für Sie automatisch am Backend zu verknüpfen.

Wenn Sie jedoch mehr Kontrolle darüber wünschen, wie und wann mit Target verbundene Analysedaten zur Berichterstellung an Analytics gesendet werden und Sie nicht die Standardeinstellungen für Target und Analytics zur automatischen Verknüpfung der Analysedaten über SDID aktivieren möchten, können Sie **analyticsLogging = client_side** über **window.targetGlobalSettings** einstellen. Hinweis: Keine Version unter 2.1 unterstützt diesen Ansatz.

Beispiel:

```
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Diese Konfiguration gilt global, d. h. bei jedem Aufruf von at.js wird **analyticsLogging: "client_side"** innerhalb der Target-Anfragen gesendet und bei jeder Anfrage wird eine Analytics-Nutzlast zurückgegeben. Bei dieser Einstellung sieht das Format der zurückgegebenen Nutzlast wie folgt aus:

```
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)an Analytics weitergeleitet werden.

Wenn statt einer globalen Einstellung ein situationsbezogener Ansatz gewünscht wird, können Sie die Funktion at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)verwenden, um dies durch Übergabe von,**analyticsLogging: "client_side"** zu erreichen. Die Nutzlast der Analyse wird nur für diesen Aufruf zurückgegeben und das Target-Backend leitet die Nutzlast nicht an Analytics weiter. Durch diesen Ansatz gibt eine at.js-Target-Anfrage nicht standardmäßig die Nutzlast zurück, sondern nur, wenn dies gewünscht und spezifiziert ist.

Beispiel:

```
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

```
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

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)an Analytics weitergeleitet werden.

## Schritt 8: Validieren der Implementierung {#step8}

Laden Sie Ihre Seiten nach der Aktualisierung der JavaScript-Bibliotheken, um sicherzustellen, dass die mboxMCSDID-Parameterwerte in Target-Aufrufen mit dem sdid-Parameterwert im Analytics-Seitenansichtsaufruf übereinstimmen.

Dies ist besonders für einseitige Anwendungen (Single Page Applications, SPA) wichtig, bei denen die Reihenfolge der Aufrufe nicht immer vorhersehbar ist.

**Hinweis:** Diese Werte müssen übereinstimmen, um die korrekte Funktionsweise von A4T sicherzustellen.

## Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Wir empfehlen, dass Sie die vorherige Integration entfernen, um Ihre Implementierung zu vereinfachen und die Notwendigkeit zur Regelung von Diskrepanzen zwischen den Systemen zu beseitigen. Sie können sämtlichen Code entfernen, den Sie für die vorherige Integration von SC zu T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

## Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

Klicken Sie in Target auf [!UICONTROL Setup &gt; Voreinstellungen], und wählen Sie entweder [!UICONTROL Pro Aktivität auswählen] oder [!UICONTROL Adobe Analytics] aus, um die Optionen zu aktivieren.

* Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen Target und Analytics beim Erstellen der einzelnen Aktivitäten.
* Adobe Analytics legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.

