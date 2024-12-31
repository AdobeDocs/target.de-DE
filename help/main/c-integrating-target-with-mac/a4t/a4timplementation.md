---
keywords: A4T;Adobe Analytics;Analytics-basierte Aktivität;Analytics Report Suite;Report Suite;Analytics Target-Integration;Report Suite konfigurieren;at.js;atjs;Adobe Experience Platform Web SDK;aep web sdk;platform web sdk
description: Führen Sie die Schritte aus, die zur Implementierung von Analytics for  [!DNL Target]  (A4T) in Ihren Adobe-  [!DNL Target]  Adobe Analytics-Lösungen erforderlich sind.
title: Wie implementiere ich Analytics für  [!DNL Target] A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: ddfb06a17a24200b2aa4f01d370cc0e92ff5f180
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 18%

---

# Implementierung von Analytics für [!DNL Target]

Bei der Implementierung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) sind mehrere Schritte erforderlich. Der Vorgang hängt davon ab, ob Sie A4T mit der [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de) oder mit at.js implementieren.

## ![Adobe Experience Platform Web SDK Badge](/help/main/assets/platform.png) Implementierungsschritte für eine Adobe Experience Platform Web SDK-Implementierung {#platform}

In den folgenden Abschnitten werden die Schritte beschrieben, die zum Bereitstellen dieser Integration auf Ihrer Site erforderlich sind, wenn Sie die Platform Web SDK verwenden möchten:

### Schritt 1: Bereitstellung für [!DNL Analytics] und [!DNL Target] anfordern

Bevor Sie A4T implementieren, müssen Sie für [!DNL Analytics] und [!DNL Target] bereitgestellt werden. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y).

### Schritt 2: Einrichten der Benutzerberechtigungen

Die Anforderungen an Benutzerkonten müssen erfüllt sein, bevor Sie eine Aktivität erstellen können, die auf [!DNL Analytics] in [!DNL Target] basiert. Siehe [Anforderungen an Benutzerberechtigungen](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Schritt 3: Erstellen einer Edge-Konfiguration

Erstellen Sie eine Edge-Konfiguration mit [!DNL Adobe Experience Platform] mithilfe des Edge-Konfigurations-Tools. Konfigurieren Sie [Erstellen und Konfigurieren von Datenströmen](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

### Schritt 4: Installieren und Konfigurieren von Platform Web SDK

Um mit der Bereitstellung [!DNL Target] Erlebnisse zu beginnen und [!DNL Analytics] für Tracking- und Analysezwecke anzuwenden, [ Sie ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) [ Platform Web SDK auf Ihren Site](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html)Seiten.

### Schritt 5: Aktivieren der Optionen für die Verwendung von A4T

Klicken Sie in der [!DNL Target]-Benutzeroberfläche auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und wählen Sie dann entweder **[!UICONTROL Select per activity]** oder **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Select per activity]** können Sie beim Erstellen jeder Aktivität zwischen [!DNL Target] und [!DNL Analytics] wählen.
* **[!UICONTROL Adobe Analytics]** legt [!DNL Analytics] als Berichtsquelle für alle Aktivitäten fest, die Sie erstellen.

## ![at.js-Badge](/help/main/assets/atjs.png) Implementierungsschritte für eine at.js-Implementierung{#section_73961BAD5BB4430A95E073DE5C026277}

In den folgenden Abschnitten werden die Schritte beschrieben, die zum Bereitstellen dieser Integration auf Ihrer Site erforderlich sind, wenn Sie at.js verwenden möchten:

### Schritt 1: Anfordern der Bereitstellung für Analytics und Target

Nachdem Sie [!DNL Analytics] als Berichtsquelle für [!DNL Target] implementiert haben, müssen Sie für [!DNL Analytics] und [!DNL Target] bereitgestellt werden. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.

### Schritt 2: Einrichten der Benutzerberechtigungen

Die Anforderungen an Benutzerkonten müssen erfüllt sein, bevor Sie eine [!DNL Analytics] Aktivität in [!DNL Target] erstellen können. Siehe [Anforderungen an Benutzerberechtigungen](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Dienst können Sie Benutzer über [!DNL Adobe Experience Cloud] Lösungen hinweg identifizieren. Implementieren oder migrieren Sie zur erforderlichen Version der Experience Cloud-Besucher-ID. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Siehe [Implementieren des Experience Cloud-ID-Service für Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) in der Dokumentation *Experience Cloud-Besucher-ID* Service.

### Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Implementieren oder migrieren Sie zur erforderlichen Version von appMeasurement.js. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Informationen zu neuen Implementierungen finden Sie unter [Übersicht über die JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) im *Analytics-Implementierungshandbuch*.

Eine Migration finden Sie unter [Migrieren nach AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) im *Analytics-Implementierungshandbuch*.

### Schritt 5: at.js herunterladen und aktualisieren

Implementieren Sie at.js mit Ihrem Produktionskonto oder migrieren Sie dazu. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

### Schritt 6: Hosten von at.js

Wenn Sie zuvor at.js bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

### Schritt 7: Referenzieren von at.js auf allen Seiten der Site {#step7}

Fügen Sie at.js unter VisitorAPI.js ein, indem Sie die folgende Codezeile im -Tag auf jeder Seite hinzufügen:

Für at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Die Datei VisitorAPI.js muss vor der Datei „at.js“ geladen werden. Wenn Sie eine vorhandene at.js-Datei aktualisieren, stellen Sie sicher, dass Sie die Ladereihenfolge überprüfen.

Die Standardeinstellung für die Integration von [!DNL Target] und [!DNL Analytics] besteht aus Sicht der Implementierung darin, die von der Seite übergebene SDID zu verwenden, um die [!DNL Target] und [!DNL Analytics] Anfrage automatisch im Backend zusammenzufügen.

Sie können steuern, wie und wann Analysedaten zu [!DNL Target] zu Reporting-Zwecken an [!DNL Analytics] gesendet werden. Wenn Sie sich nicht für die Standardeinstellungen anmelden möchten, [!DNL Target] und [!DNL Analytics] die Analysedaten automatisch über die SDID zusammenfügen, legen Sie **analyticsLogging = client_side** über **window.targetGlobalSettings** fest. Hinweis: Keine Version unter 2.1 unterstützt diesen Ansatz.

Beispiel:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Diese Einrichtung hat globale Auswirkungen, was bedeutet, dass bei jedem Aufruf von at.js **analyticsLogging: „client_side“ innerhalb der [!DNL Target]-Anfragen gesendet** und für jede Anfrage eine Analytics-Payload zurückgegeben wird. Wenn diese Option eingerichtet ist, sieht das Format der zurückgegebenen Payload wie folgt aus:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Die Payload kann dann über die „Data Insertion API[ an Analytics weitergeleitet ](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Bei automatischen Zuordnungs - und automatischen Targeting -Aktivitäten müssen Sie auch die Sitzungs-ID weiterleiten. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} im Handbuch *Adobe Target SDKs*.

Wenn eine globale Einstellung nicht gewünscht ist und ein eher bedarfsorientierter Ansatz vorzuziehen ist, verwenden Sie die at.js-Funktion [getOffers()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffers-atjs-2.html){target=_blank}, indem Sie **analyticsLogging: „client_side“**. Die Analytics-Payload wird nur für diesen Aufruf zurückgegeben und das [!DNL Target]-Backend leitet die Payload nicht an [!DNL Analytics] weiter. Bei diesem Ansatz gibt jede at.js-[!DNL Target] standardmäßig die Payload zurück, jedoch nur, wenn sie gewünscht und angegeben wird.

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

Die Payload kann dann über die „Data Insertion [&quot; an [!DNL Analytics] weitergeleitet ](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

### Schritt 8: Validieren der Implementierung {#step8}

Laden Sie die Seiten, nachdem Sie die JavaScript-Bibliotheken aktualisiert haben, um zu bestätigen, dass die `mboxMCSDID` Parameterwerte in [!DNL Target] Aufrufen mit dem `sdid` Parameterwert im [!DNL Analytics] Seitenansichtsaufruf übereinstimmen.

Es ist besonders wichtig zu bestätigen, dass diese Werte in Single Page Applications (SPA) übereinstimmen, in denen die Reihenfolge der Aufrufe nicht immer vorhersehbar ist.

>[!NOTE]
>
>Die Übereinstimmung dieser Werte ist erforderlich, damit A4T ordnungsgemäß funktioniert.

### Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Adobe empfiehlt, die vorherige Integration zu entfernen, um Ihre Implementierung zu vereinfachen und Diskrepanzen zwischen den Systemen zu beseitigen. Sie können jeden Code entfernen, den Sie für eine frühere Integration von SC in T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

### Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration > Reporting]** und wählen Sie entweder **[!UICONTROL Select per activity]** oder **[!UICONTROL Adobe Analytics]** aus, um die Optionen zu aktivieren.

* **[!UICONTROL Select per activity]** können Sie beim Erstellen jeder Aktivität zwischen [!DNL Target] und [!DNL Analytics] wählen.
* **[!UICONTROL Adobe Analytics]** legt [!DNL Analytics] als Berichtsquelle für alle Aktivitäten fest, die Sie erstellen.


