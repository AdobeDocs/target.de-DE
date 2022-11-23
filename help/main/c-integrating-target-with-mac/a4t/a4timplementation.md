---
keywords: A4T; Adobe Analytics; Analytics-basierte Aktivität; Analytics Report Suite; Report Suite; Analytics Target-Integration; Report Suite konfigurieren; at.js; at.js; Adobe Experience Platform Platform Web SDK; aep Web SDK; Platform Web SDK
description: Führen Sie die erforderlichen Schritte aus, um Analytics für [!DNL Target] (A4T) in Ihrer Adobe [!DNL Target] und Adobe Analytics-Lösungen.
title: Implementieren von Analytics für [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: f19d7de5b248ab1a55e7aad47d2e445eadf69717
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 22%

---

# Analytics zur [!DNL Target] Implementierung

Bei der Implementierung sind mehrere Schritte erforderlich [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T). Der Prozess variiert je nachdem, ob Sie A4T mit der [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de) oder mit at.js.

## ![Adobe Experience Platform Web SDK-Badge](/help/main/assets/platform.png) Implementierungsschritte für eine Adobe Experience Platform Web SDK-Implementierung {#platform}

In den folgenden Abschnitten werden die Schritte beschrieben, die zum Bereitstellen dieser Integration auf Ihrer Site erforderlich sind, wenn Sie das Platform Web SDK verwenden möchten:

### Schritt 1: Anfordern der Bereitstellung für [!DNL Analytics] und [!DNL Target]

Vor der Implementierung von A4T müssen Sie für [!DNL Analytics] und [!DNL Target]. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y).

### Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine Aktivität erstellen können, die auf [!DNL Analytics] in [!DNL Target]. Siehe [Anforderungen an Benutzerberechtigungen](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Schritt 3: Erstellen einer Edge-Konfiguration

Erstellen Sie eine Edge-Konfiguration mit [!DNL Adobe Experience Platform] mit dem Edge-Konfigurationstool. Konfigurieren Sie die [[!DNL Analytics] and [!DNL Target] Edge-Konfigurationseinstellungen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html).

### Schritt 4: Installieren und Konfigurieren des Platform Web SDK

Zu Beginn des Versands [!DNL Target] Erlebnisse und zur Anwendung [!DNL Analytics] zu Tracking- und Analysezwecken, [Installieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) und [konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) das Platform Web SDK auf den Seiten Ihrer Site.

### Schritt 5: Aktivieren der Optionen für die Verwendung von A4T

Im [!DNL Target] Benutzeroberfläche, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**, wählen Sie entweder **[!UICONTROL Pro Aktivität auswählen]** oder **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen und beim Erstellen der einzelnen Aktivitäten.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.]**[!DNL Analytics]

## ![at.js-Badge](/help/main/assets/atjs.png) Implementierungsschritte für eine at.js-Implementierung{#section_73961BAD5BB4430A95E073DE5C026277}

In den folgenden Abschnitten werden die Schritte beschrieben, die zum Bereitstellen dieser Integration auf Ihrer Site erforderlich sind, wenn Sie at.js verwenden möchten:

### Schritt 1: Anfordern der Bereitstellung für Analytics und Target

Nach der Implementierung [!DNL Analytics] als Berichtsquelle für [!DNL Target], müssen Sie für [!DNL Analytics] und [!DNL Target]. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.

### Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine [!DNL Analytics]-basierte Aktivität in [!DNL Target]. Siehe [Anforderungen an Benutzerberechtigungen](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Service können Sie Benutzer über [!DNL Adobe Experience Cloud]-Lösungen hinweg identifizieren. Implementieren oder migrieren Sie die erforderliche Version der Experience Cloud-Besucher-ID. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Siehe [Implementieren des Experience Cloud-ID-Diensts für Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) im *Experience Cloud-Besucher-ID-Service* Dokumentation.

### Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Implementieren oder migrieren Sie die erforderliche Version von appMeasurement.js. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Weitere Informationen zu neuen Implementierungen finden Sie unter [Übersicht über die JavaScript-Implementierung](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) im *Implementierungshandbuch für Analytics*.

Informationen zur Migration finden Sie unter [Migration zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) im *Implementierungshandbuch für Analytics*.

### Schritt 5: Herunterladen und Aktualisieren von at.js

Implementieren oder migrieren Sie mithilfe Ihres Produktionskontos zur erforderlichen Version von at.js. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

### Schritt 6: &quot;at.js&quot;hosten

Wenn Sie at.js bereits bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

### Schritt 7: Verweisen auf at.js auf allen Seiten der Site {#step7}

Fügen Sie at.js unterhalb von VisitorAPI.js ein, indem Sie dem Tag auf jeder Seite die folgende Codezeile hinzufügen:

Für at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Die Datei VisitorAPI.js muss vor at.js geladen werden. Wenn Sie eine vorhandene at.js-Datei aktualisieren, überprüfen Sie die Ladereihenfolge.

Die Standardeinstellung für [!DNL Target] und [!DNL Analytics] Aus Implementierungsperspektive besteht darin, die von der Seite übergebene SDID zu verwenden, um die [!DNL Target] und [!DNL Analytics] -Anfrage automatisch zusammen im Backend ausführen.

Sie können steuern, wie und wann Analysedaten im Zusammenhang mit [!DNL Target] nach [!DNL Analytics] für Berichtszwecke. Wenn Sie sich nicht für die Standardeinstellungen von [!DNL Target] und [!DNL Analytics] die Analysedaten automatisch über die SDID zuordnen, **analyticsLogging = client_side** via **window.targetGlobalSettings**. Hinweis: Keine Version unter 2.1 unterstützt diesen Ansatz.

Beispiel:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Diese Einrichtung hat globale Auswirkungen, d. h. jeder Aufruf von at.js hat folgende Auswirkungen: **analyticsLogging: &quot;client_side&quot;** innerhalb der [!DNL Target] -Anfragen und eine Analytics-Payload werden für jede Anfrage zurückgegeben. Wenn diese Option eingerichtet ist, sieht das Format der zurückgegebenen Payload wie folgt aus:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Die Payload kann dann über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Bei Aktivitäten mit automatischer Zuordnung und automatischem Targeting müssen Sie auch die sessionId weiterleiten. Weitere Informationen finden Sie unter [Berichterstellung von Analytics for Target (A4T)](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/){target=_blank} im *Adobe Target SDKs* Handbuch.

Wenn keine globale Einstellung gewünscht wird und ein bedarfsorientierter Ansatz vorzuziehen ist, verwenden Sie die Funktion at.js . [getOffers()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/){target=_blank} durch Übergabe **analyticsLogging: &quot;client_side&quot;**. Die Analytics-Payload wird nur für diesen Aufruf und die [!DNL Target] Backend leitet die Payload nicht an [!DNL Analytics]. Durch diesen Ansatz wird jeder at.js-Dienst [!DNL Target] -Anfrage gibt die Payload standardmäßig zurück, jedoch nur, wenn gewünscht und angegeben.

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

Die Payload kann dann an weitergeleitet werden [!DNL Analytics] über die [Dateneinfüge-API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

### Schritt 8: Validieren der Implementierung {#step8}

Laden Sie Ihre Seiten, nachdem Sie die JavaScript-Bibliotheken aktualisiert haben, um zu bestätigen, dass die Variable `mboxMCSDID` Parameterwerte in [!DNL Target] -Aufrufe entsprechen `sdid` Parameterwert in der [!DNL Analytics] Seitenansichtsaufruf.

Es ist besonders wichtig zu bestätigen, dass diese Werte in Einzelseiten-Apps (SPA) übereinstimmen, bei denen die Reihenfolge der Aufrufe nicht immer vorhersehbar ist.

>[!NOTE]
>
>Die Übereinstimmung dieser Werte ist erforderlich, damit A4T ordnungsgemäß funktioniert.

### Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Adobe empfiehlt, die vorherige Integration zu entfernen, um Ihre Implementierung zu vereinfachen und die Notwendigkeit zur Beseitigung von Systemdiskrepanzen zu beseitigen. Sie können sämtlichen Code entfernen, den Sie für eine vorherige Integration von SC zu T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

### Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

In [!DNL Target]klicken **[!UICONTROL Administration > Berichterstellung]** und wählen Sie entweder **[!UICONTROL Pro Aktivität auswählen]** oder **[!UICONTROL Adobe Analytics]** um die Optionen zu aktivieren.

* **[!UICONTROL Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen und beim Erstellen der einzelnen Aktivitäten.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.]**[!DNL Analytics]


