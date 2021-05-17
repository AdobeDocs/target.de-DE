---
keywords: A4T;Adobe Analytics;Analytics-basierte Aktivität;Analytics-Report Suite;Report Suite;Analytics-Zielgruppe-Integration;Report Suite konfigurieren;at.js;atjs;adobe experience platform web sdk;aep web sdk;platform web sdk
description: Führen Sie die erforderlichen Schritte aus, um Analytics für  [!DNL Target] (A4T) in your Adobe [!DNL Target] und Adobe Analytics-Lösungen zu implementieren.
title: Wie implementiere ich Analytics for [!DNL Target] (A4T)?
feature: 'Analytics for Target (A4T) '
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: efa796edf3cd4da718fdcb0dbfd3d6f635ebf401
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 22%

---

# Analytics für [!DNL Target]-Implementierung

Bei der Implementierung von [!DNL Adobe Analytics] als Berichte-Quelle für [!DNL Adobe Target] (A4T) sind mehrere Schritte erforderlich. Der Prozess variiert je nachdem, ob Sie A4T mit [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) oder mit at.js implementieren.

## Implementierungsschritte für eine Adobe Experience Platform Web SDK-Implementierung {#platform}

>[!NOTE]
>
>Die Unterstützung für A4T in einer [!DNL Adobe Experience Platform Web SDK]-Implementierung, die in diesem Artikel besprochen wird, ist für die [!DNL Platform Web SDK] Version 2.5.0 (24. Mai 2021) geplant.

Die folgenden Abschnitte beschreiben die Schritte, die zum Bereitstellen dieser Integration auf Ihrer Site erforderlich sind, wenn Sie das Platform Web SDK verwenden möchten:

### Schritt 1: Anforderungs-Bereitstellung für [!DNL Analytics] und [!DNL Target]

Vor der Implementierung von A4T müssen Sie für [!DNL Analytics] und [!DNL Target] bereitgestellt werden. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES).

### Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine Aktivität auf der Grundlage von [!DNL Analytics] in [!DNL Target] erstellen können. Siehe [Anforderungen an Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

### Schritt 3: Edge-Konfiguration erstellen

Erstellen Sie eine Edge-Konfiguration mit [!DNL Adobe Experience Platform Launch] mithilfe des Edge-Konfigurationstools. Konfigurieren Sie die [[!DNL Analytics] and [!DNL Target] Edge-Konfigurationseinstellungen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html).

### Schritt 4: Installieren und Konfigurieren des Platform Web SDK

Um Beginn, die [!DNL Target]-Erlebnisse bereitstellen, anzuwenden und [!DNL Analytics] für Tracking- und Analyse-Zwecke anzuwenden, [Installieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) und [konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) das Plattform-Web-SDK auf Ihren Siteseiten.

### Schritt 5: Optionen für die Verwendung von A4T aktivieren

Klicken Sie in der Benutzeroberfläche [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und wählen Sie dann entweder **[!UICONTROL Pro Aktivität]** oder **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen und beim Erstellen der einzelnen Aktivitäten.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.]**[!DNL Analytics]

## Implementierungsschritte für eine &quot;at.js&quot;-Implementierung{#section_73961BAD5BB4430A95E073DE5C026277}

Die folgenden Abschnitte beschreiben die Schritte, die für die Bereitstellung dieser Integration auf Ihrer Site erforderlich sind, wenn Sie at.js verwenden möchten:

### Schritt 1: Anfordern der Bereitstellung für Analytics und Target

Nachdem Sie [!DNL Analytics] als Berichte-Quelle für [!DNL Target] implementiert haben, müssen Sie für [!DNL Analytics] und [!DNL Target] bereitgestellt werden. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](http://www.adobe.com/go/audiences).

### Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine [!DNL Analytics]-basierte Aktivität in [!DNL Target] erstellen können. Siehe [Anforderungen an Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

### Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Service können Sie Benutzer über [!DNL Adobe Experience Cloud]-Lösungen hinweg identifizieren. Implementieren oder migrieren Sie zur erforderlichen Version der Experience Cloud-Besucher-ID. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Siehe [Implementieren des Experience Cloud-ID-Diensts für Zielgruppe](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) in der *Experience Cloud-Besucher-ID-Dienst*-Dokumentation.

### Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Implementieren oder migrieren Sie die erforderliche Version von appMeasurement.js. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Neue Implementierungen finden Sie unter [Übersicht über die JavaScript-Implementierung](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) im *Analytics-Implementierungshandbuch*.

Eine Migration finden Sie unter [Migration zu AppMeasurement for JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) im *Analytics Implementierungshandbuch*.

### Schritt 5: &quot;at.js&quot;herunterladen und aktualisieren

Implementieren oder migrieren Sie mithilfe Ihres Produktionskontos zur erforderlichen Version von at.js. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

### Schritt 6: &quot;at.js&quot;hosten

Wenn Sie zuvor at.js bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

### Schritt 7: Verweisen Sie auf &quot;at.js&quot;auf allen Siteseiten {#step7}

Fügen Sie at.js unter VisitorAPI.js ein, indem Sie dem Tag auf jeder Seite die folgende Codezeile hinzufügen:

Für at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

VisitorAPI.js muss vor &quot;at.js&quot;geladen werden. Wenn Sie eine vorhandene Datei &quot;at.js&quot;oder &quot;mbox.js&quot;aktualisieren, überprüfen Sie die Ladereihenfolge.

Die Standardeinstellung für die Integration von [!DNL Target] und [!DNL Analytics] ist aus der Sicht der Implementierung die Verwendung der SDID, die von der Seite übergeben wird, um die [!DNL Target]- und [!DNL Analytics]-Anforderung automatisch im Backend zusammenzufügen.

Sie können steuern, wie und wann Analysedaten zu [!DNL Target] zu Berichten an [!DNL Analytics] gesendet werden. Wenn Sie die Standardeinstellungen für [!DNL Target] und [!DNL Analytics] nicht automatisch mit den Analysedaten über die SDID Opt-in möchten, setzen Sie **analyticsLogging = client_side** über **window.targetGlobalSettings**. Hinweis: Keine Version unter 2.1 unterstützt diesen Ansatz.

Beispiel:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Dieses Setup hat einen globalen Effekt. Das bedeutet, dass jeder Aufruf von at.js **analyticsLogging hat: &quot;client_side&quot;** wird innerhalb der [!DNL Target]-Anforderungen gesendet und für jede Anforderung wird eine Analytics-Nutzlast zurückgegeben. Wenn diese Option eingerichtet ist, sieht das Format der zurückgegebenen Nutzlast wie folgt aus:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Die Nutzlast kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) an Analytics weitergeleitet werden. Bei Aktivitäten für die automatische Zuordnung und automatische Zielgruppe müssen Sie auch die sessionId weiterleiten. Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T) Berichte](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) im Handbuch *Adobe Target SDKs*.

Wenn eine globale Einstellung nicht gewünscht wird und ein bedarfsorientierter Ansatz vorzuziehen ist, verwenden Sie die Funktion at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md), indem Sie **analyticsLogging übergeben: &quot;client_side&quot;**. Die Analytics-Nutzlast wird nur für diesen Aufruf zurückgegeben und das [!DNL Target]-Backend leitet die Nutzlast nicht an [!DNL Analytics] weiter. Bei diesem Ansatz gibt jede at.js [!DNL Target]-Anforderung standardmäßig die Nutzlast zurück, jedoch nur, wenn gewünscht und angegeben.

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

### Schritt 8: Validieren der Implementierung {#step8}

Laden Sie Ihre Seiten, nachdem Sie die JavaScript-Bibliotheken aktualisiert haben, um sicherzustellen, dass die `mboxMCSDID`-Parameterwerte in [!DNL Target]-Aufrufen mit dem Parameterwert `sdid` im Aufruf [!DNL Analytics] der Ansicht übereinstimmen.

Es ist besonders wichtig zu bestätigen, dass diese Werte in Einzelseitenanwendungen (SPA) übereinstimmen, bei denen die Reihenfolge der Aufrufe nicht immer vorhersagbar ist.

>[!NOTE]
>
>Die Übereinstimmung dieser Werte ist erforderlich, damit A4T ordnungsgemäß funktioniert.

### Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Adobe empfiehlt, die vorherige Integration zu entfernen, um die Implementierung zu vereinfachen und Systemdiskrepanzen zu beseitigen. Sie können jeden Code entfernen, den Sie für eine vorherige Integration von SC zu T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

### Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration > Visual Experience Composer]** und wählen Sie entweder **[!UICONTROL Pro Aktivität]** oder **[!UICONTROL Adobe Analytics]** aus, um die Optionen zu aktivieren.

* **[!UICONTROL Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen und beim Erstellen der einzelnen Aktivitäten.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.]**[!DNL Analytics]


