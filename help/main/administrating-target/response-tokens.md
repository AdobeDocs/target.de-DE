---
keywords: Antwort-Token;Token;Plug-ins;Plug-ins;at.js;Antwort;Platform Web SDK;Google Analytics
description: Erfahren Sie, wie Sie Antwort-Token in [!DNL Adobe Target]  verwenden können, um ausgabespezifische Informationen zum Debugging und zur Integration mit Tools von Drittanbietern zu erhalten.
title: Was sind Antwort-Token und wie verwende ich sie?
feature: Administration & Configuration
role: Admin
exl-id: d0c1e914-3172-466d-9721-fe0690abd30b
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 22%

---

# Antwort-Token

Mit Antwort-Token können Sie automatisch Informationen ausgeben, die für die [!DNL Adobe Target] auf der Web-Seite Ihrer Marke spezifisch sind. Diese Informationen können Details zur Aktivität, zum Angebot, zum Erlebnis, zum Benutzerprofil, zu geografischen Informationen und mehr enthalten. Diese Details enthalten zusätzliche Antwortdaten, die für interne Tools oder Tools von Drittanbietern freigegeben oder zum Debugging verwendet werden können.

Mit Antwort-Token können Sie auswählen, welche Variablen (in Schlüsselwertpaaren) verwendet werden sollen, und dann aktivieren, dass sie als Teil einer [!DNL Target]-Antwort gesendet werden können. Sie aktivieren eine Variable mithilfe des Schalters und die Variable wird mit [!DNL Target] Antworten gesendet, die in Netzwerkaufrufen validiert werden können. Antwort-Token funktionieren auch im [!UICONTROL Preview].

Ein wichtiger Unterschied zwischen Plug-ins und Antwort-Token besteht darin, dass Plug-ins JavaScript an die Seite senden, die beim Versand ausgeführt wird. Antwort-Token liefern jedoch ein -Objekt, das dann mithilfe von Ereignis-Listenern gelesen und bearbeitet werden kann. Der Ansatz mit Antwort-Token ist sicherer und ermöglicht eine einfachere Entwicklung und Wartung von Drittanbieter-Integrationen.

>[!NOTE]
>
>Antwort-Token sind in at.js-Version 1.1 oder neuer verfügbar.

| Target SDK | Vorgeschlagene Aktionen |
|--- |--- |
| [Adobe Experience Platform Web-SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} | Stellen Sie sicher, dass Sie Platform Web SDK Version 2.6.0 oder höher verwenden. Informationen zum Herunterladen der neuesten Version von Platform Web SDK finden Sie unter [SDK installieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html){target=_blank} im Handbuch *Platform Web SDK - Übersicht*. Weitere Informationen zu den neuen Funktionen der einzelnen Versionen von Platform Web SDK finden Sie unter [Versionshinweise](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) im Handbuch *Platform Web SDK - Übersicht*. |
| [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank} | Stellen Sie sicher, dass Sie at.js der Version 1.1 oder neuer verwenden. Informationen zum Herunterladen der neuesten Version von at.js finden Sie unter [Herunterladen von at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=en){target=_blank}. Informationen zu neuen Funktionen in den einzelnen Versionen von at.js finden Sie unter [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.<br>Kunden, die at.js verwenden, sollten Antwort-Token nutzen und auf Plug-ins verzichten. Einige Plug-ins, die sich auf interne Methoden stützen, die in mbox.js (inzwischen nicht mehr unterstützt), aber nicht in at.js vorhanden waren, werden bereitgestellt, schlagen jedoch fehl. |

## Verwenden von Antwort-Token {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Stellen Sie sicher, dass Sie Platform Web SDK Version 2.6.0 (oder höher) oder at.js Version 1.1 (oder höher) verwenden.

   Weitere Informationen:

   * **Platform Web SDK**: Siehe [Installieren von SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) im *Platform Web SDK - Übersicht*.
   * **at.js**: Siehe &quot;[.js herunterladen](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html){target=_blank}.

1. Klicken Sie [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**.

1. Aktivieren Sie die gewünschten Antwort-Token, z. B. `activity.id` und `offer.id`.

   Die folgenden Parameter sind standardmäßig verfügbar:

   | Typ | Parameter | Hinweise |
   |--- |--- |--- |
   | Integrierte Profile | `profile.activeActivities` | Gibt eine Reihe an `activityIds` aus, für die der Besucher qualifiziert ist. Die Inkrementierung erfolgt im Zuge der Benutzerqualifizierung. Auf einer Seite mit zwei [!DNL Target]-Anfragen, die zwei verschiedene Aktivitäten liefern, enthält die zweite Anfrage beispielsweise beide Aktivitäten. |
   |  | `profile.isFirstSession` | Gibt „true“ oder „false“ zurück. |
   |  | `profile.isNewSession` | Gibt „true“ oder „false“ zurück. |
   |  | `profile.daysSinceLastVisit` | Gibt die Anzahl der Tage seit dem letzten Zugriff des Besuchers zurück. |
   |  | `profile.tntId` | Gibt die tntID des Besuchers zurück. |
   |  | `profile.marketingCloudVisitorId` | Gibt die Experience Cloud-ID des Besuchers zurück. |
   |  | `profile.thirdPartyId` | Gibt die Drittanbieter-ID des Besuchers zurück. |
   |  | `profile.categoryAffinity` | Gibt die Lieblingskategorie des Besuchers zurück. |
   |  | `profile.categoryAffinities` | Gibt eine Reihe der Top-5-Kategorien des Besuchers als Zeichenfolgen zurück. |
   | Aktivität | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`offer.name`<br>`offer.id` | Details der aktuellen Aktivität.<br> Beachten Sie, dass Werte für Angebotsparameter auf Erlebnisebene ausgewertet werden. |
   | Geo | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | Weitere Informationen zur Verwendung von Geo-Targeting in Aktivitäten finden Sie unter [Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md). |
   | Traffic-Zuordnungsmethode<br>(Gilt nur für [!UICONTROL Auto-Target] und [!UICONTROL Automated Personalization] Aktivitäten.) | `experience.trafficAllocationId` | Gibt 0 zurück, wenn ein Besucher ein Erlebnis aus Kontroll-Traffic erhalten hat, und 1, wenn ein Besucher ein Erlebnis aus der Targeting-Traffic-Verteilung erhalten hat. |
   |  | `experience.trafficAllocationType` | Gibt „Kontrolle“ oder „Targeting“ zurück. |

   Benutzerprofil- und Kundenattribute werden ebenfalls in der Liste angezeigt.

   >[!NOTE]
   >
   >Parameter mit Sonderzeichen werden in der Liste nicht angezeigt. Es werden nur alphanumerische Zeichen und Unterstriche unterstützt.

1. (Bedingt) Um einen Profilparameter als Antwort-Token zu verwenden, der Parameter jedoch nicht über eine [!DNL Target]-Anfrage weitergeleitet wurde und daher nicht in die [!DNL Target]-Benutzeroberfläche geladen wurde, können Sie die Schaltfläche [!UICONTROL Add Response Token] verwenden, um das Profil zur Benutzeroberfläche hinzuzufügen.

   Klicken Sie auf **[!UICONTROL Add Response Token]**, geben Sie den Token-Namen ein und klicken Sie dann auf **[!UICONTROL Activate]**.

1. Erstellen Sie eine Aktivität.

## Überwachen von Antworten und Lesen von Antwort-Token

Der Prozess, mit dem Sie auf [!DNL Target] Antworten und Leseantwort-Token warten, hängt davon ab, ob Sie über eine [!DNL Platform Web SDK]- oder at.js-Implementierung verfügen.

### ![Adobe Experience Platform Web SDK-Badge](/help/main/assets/platform.png) [!DNL Platform Web SDK] Verwendung der Handle-Objektklasse {#platform-web-sdk}

Verwenden Sie die Handle-Objektklasse, die über ein Metadatenobjekt und ein Datenobjekt verfügt, um auf [!DNL Target] Antworten zu warten und die Antwort-Token zu lesen.

Im folgenden Antwortbeispiel wird ein [!DNL Platform Web SDK] benutzerdefinierter Ereignishandler direkt zur HTML-Seite hinzugefügt (in der Tabelle werden die im Code verwendeten Objekte erläutert):

| Objekt | Informationen |
| --- | --- |
| Typ - Personalization.decision | Ob die Entscheidung vom [!DNL Target]- oder Offer decisioning-Anbieter getroffen wurde. |
| Entscheidungsanbieter - TGT | TGT-[!DNL Target]. [!DNL Target] stellt die Metadaten und Werte des Antwort-Tokens für die Seite bereit. |
| meta | Metadaten, die an die Seite übergeben werden. |
| Daten | Werte der an die Seite übergebenen Metadaten. |

```html
<html>

<head>
 ...
 <script src="alloy.js"></script>
 <script>
  {
   "requestId": "4d0a7cfd-952c-408c-b3b8-438edc38250a",
   "handle": [{
    "type": "personalization:decisions",
    "payload": [{
     "id": "....",
     "scope": "__view__",
     "scopeDetails": {
      "decisionProvider": "TGT",
      "activity": {
       "id": "..."
      },
      "experience": {
       "id": "...."
      }
     },
     "items": [{
      "id": "123",
      "schema": "https://ns.adobe.com/personalization/dom-action",
      "meta": {
       "activity.id": "...",
       "activity.name": "...",
       "profile.foo": "...",
       "profile.bar": "..."
      },
      "data": {
       "id": "123",
       "type": "setHtml",
       "selector": "#foo",
       "prehidingSelector": "#foo",
       "content": "<div>Hello world</div>"
      }
     }]
    }]
   }]
  }
  });
 </script>
</head>

<body>
 ...
</body>

</html>
```

### ![at.js-Badge](/help/main/assets/atjs.png) at.js mit benutzerdefinierten Ereignissen

Verwenden Sie [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-custom-events.html?lang=en){target=_blank} benutzerspezifische Ereignisse, um auf die [!DNL Target] Antwort zu warten und die Antwort-Token zu lesen.

Mit dem folgenden Code-Beispiel wird direkt ein benutzerdefinierter [!DNL at.js]-Eventhandler auf der HTML-Seite hinzugefügt:

```html
<html> 
  <head> 
    .... 
    <script src="at.js"></script> 
    <script> 
      document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
        console.log("Request succeeded", e.detail); 
      }); 
    </script> 
  <head> 
  <body> 
  ... 
  </body> 
</html>
```

## Häufig gestellte Fragen zu Antwort-Token {#section_3DD5F32C668246289CDF9B4CDE1F536D}

**Welche Rolle wird zum Aktivieren oder Deaktivieren von Antwort-Token benötigt?**

Antwort-Token können nur von Benutzenden mit der Rolle [!DNL Target]-[!UICONTROL Administrator] aktiviert oder deaktiviert werden.

**Was passiert, wenn ich [!DNL Platform Web SDK] 2.6.0 (oder früher) verwende?**

Sie haben keinen Zugriff auf Antwort-Token.

**Was passiert, wenn ich at.js 1.0 (oder früher) verwende?**

Die Antwort-Token werden angezeigt, aber at.js kann sie nicht verwenden.

**Kann ich [!DNL Target Classic] Plug-ins und Antwort-Token gleichzeitig aktivieren?**

Plug-ins und Antwort-Token sind parallel verfügbar; Plug-ins werden jedoch in Zukunft nicht mehr unterstützt.

**Werden Antwort-Token über alle [!DNL Target] Antworten oder nur über [!DNL Target] Antworten bereitgestellt, die eine Aktivität liefern?**

Antwort-Token werden nur über [!DNL Target] Antworten bereitgestellt, die eine Aktivität bereitstellen.

**Mein [!DNL Target Classic]-Plug-in enthielt JavaScript. Wie reproduziere ich diese Funktionalität mithilfe von Antwort-Token?**

Bei der Migration zu Antwort-Token muss dieser JavaScript-Typ in Ihrer Code-Basis oder Tag-Management-Lösung beibehalten werden. Sie können diesen Trigger mit [!DNL Platform Web SDK] oder [!DNL at.js] benutzerspezifischen Ereignissen erstellen und die Werte des Antwort-Tokens an Ihre JavaScript-Funktionen übergeben.

**Warum wird mein Profil-/Kundenattribut-Parameter nicht in der Liste der Antwort-Token angezeigt?**

[!DNL Target] aktualisiert Parameter normalerweise alle 15 Minuten. Diese Aktualisierung hängt von der Benutzeraktion ab. Die Daten werden nur aktualisiert, wenn die Seite mit den Antwort-Token aufgerufen wird. Wenn Ihre Parameter nicht in der Liste der Antwort-Token angezeigt werden, hat [!DNL Target] die Daten noch nicht aktualisiert.

Wenn Ihr Parameter außerdem keine nicht alphanumerischen Zeichen oder andere Symbole als Unterstriche enthält, wird der Parameter nicht in der Liste angezeigt. Momentan werden nur alphanumerische Zeichen und Unterstriche unterstützt.

**Liefert das Antwort-Token weiterhin Inhalte, wenn es ein gelöschtes Profilskript oder einen Profilparameter verwendet?**

Antwort-Token extrahieren Informationen aus Benutzerprofilen und stellen diese Informationen dann bereit. Wenn Sie ein Profilskript oder einen Profilparameter löschen, heißt das nicht, dass die Informationen aus den Benutzerprofilen entfernt wurden. Die Benutzerprofile verfügen weiterhin über Daten, die dem Profilskript entsprechen. Das Antwort-Token stellt den Inhalt weiterhin bereit. Für Benutzende, die diese Informationen nicht in ihrem Profil gespeichert haben, oder für neue Besucher wird dieses Token nicht bereitgestellt, da die Daten nicht in ihren Profilen vorhanden sind.

[!DNL Target] schaltet das Token nicht automatisch aus. Wenn Sie ein Profilskript löschen und das Token nicht mehr bereitgestellt werden soll, müssen Sie das Token selbst deaktivieren.

**Ich habe mein Profilskript umbenannt. Warum ist das Token, das dieses Skript verwendet, weiterhin mit dem alten Namen aktiv?**

Wie zuvor erwähnt, agieren Antwort-Token mit den für Benutzer gespeicherten Profilinformationen. Obwohl Sie Ihr Profilskript umbenannt haben, wird den Benutzern, die Ihre Website besucht haben, der alte Wert des Profilskripts in ihren Profilen gespeichert. Das Token nimmt weiterhin den alten Wert auf, der bereits in den Benutzerprofilen gespeichert ist. Wenn Sie den Inhalt nun für den neuen Namen bereitstellen möchten, müssen Sie das vorherige Token deaktivieren und das neue Token aktivieren.

**Wenn sich meine Attribute geändert haben, wann werden sie dann aus der Liste entfernt?**

[!DNL Target] führt in regelmäßigen Abständen eine Aktualisierung der Attribute durch. Attribute, die nicht aktiviert sind, werden bei der nächsten Aktualisierung entfernt. Wenn Sie jedoch über ein Attribut verfügen, das aktiviert wurde und entfernt wurde, wird dieses Skript erst aus der Attributliste entfernt, wenn Sie es deaktivieren. Beispielsweise haben Sie ein Profilskript entfernt, das als Token verwendet wurde. [!DNL Target] entfernt nur die ausgeschalteten Attribute aus der Liste, wenn sie gelöscht oder umbenannt werden.

## Daten an Google Analytics senden

In den folgenden Abschnitten wird beschrieben, wie Sie [!DNL Target] Daten an Google Analytics 4 senden. Daten, die über Antwort-Token gesendet werden, können auch an andere Drittanbieter-Integrationen gesendet werden.

### ![AEP-Badge](/help/main/assets/platform.png) Senden von Daten an Google Analytics über Platform Web SDK

Google Analytics-Daten können über Platform Web SDK Version 2.6.0 (oder höher) gesendet werden, indem der folgende Code auf der HTML-Seite hinzugefügt wird.

>[!NOTE]
>
>Stellen Sie sicher, dass sich das Wertpaar des Antwort-Token-Schlüssels unter dem `alloy("sendEvent"` befindet.

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>
<script type="text/javascript">
    alloy("sendEvent", {
 
 
    })
    .then(({ renderedPropositions, nonRenderedPropositions }) => {
        // concatenate all the propositions
        const propositions = [...renderedPropositions, ...nonRenderedPropositions];
        // extractResponseTokens() extract the meta from item -> meta
        const tokens = extractResponseTokens(propositions);
        const activityNames = [];
        const experienceNames = [];
        const uniqueTokens = distinct(tokens);
    
    
        uniqueTokens.forEach(token => {
            activityNames.push(token["activity.name"]);
            experienceNames.push(token["experience.name"]);
        });
 
        gtag('config', 'TAG_ID');
        gtag('event', 'action_name', {'eventCategory': 'target',
            'eventAction': experienceNames, 'eventLabel': activityNames
        });
    });
</script>
```

### ![at.js-Badge](/help/main/assets/atjs.png) Senden von Daten an Google Analytics über at.js {#section_04AA830826D94D4EBEC741B7C4F86156}

Daten können via at.js an Google Analytics gesendet werden, indem Sie auf der HTML-Seite den folgenden Code hinzufügen:

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>

<script type="text/javascript">
    document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) {
        var tokens = e.detail.responseTokens;

        if (isEmpty(tokens)) {
            return;
        }

        var activityNames = [];
        var experienceNames = [];
        var uniqueTokens = distinct(tokens);

        uniqueTokens.forEach(function(token) {
            activityNames.push(token["activity.name"]);
            experienceNames.push(token["experience.name"]);
        });

        gtag('config', 'TAG_ID');
        gtag('event', 'action_name', {'eventCategory': 'target',
            'eventAction': experienceNames, 'eventLabel': activityNames
        });
    });

    function isEmpty(val) {
        return (val === undefined || val == null || val.length <= 0) ? true : false;
    }

    function key(obj) {
        return Object.keys(obj)
        .map(function(k) { return k + "" + obj[k]; })
        .join("");
    }

    function distinct(arr) {
        var result = arr.reduce(function(acc, e) {
            acc[key(e)] = e;
            return acc;
        }, {});

        return Object.keys(result)
        .map(function(k) { return result[k]; });
    }
</script>
```

## Debugging

Die folgenden Abschnitte enthalten Informationen zum Debugging von Antwort-Token:

### ![at.js-Badge](/help/main/assets/atjs.png) Google Analytics und Debugging

Mit dem folgenden Code können Sie mit Google Analytics debuggen:

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>
  
<script type="text/javascript">
    document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) {
      var tokens = e.detail.responseTokens;
  
      if (isEmpty(tokens)) {
        return;
      }
  
      var activityNames = [];
      var experienceNames = [];
      var uniqueTokens = distinct(tokens);
  
      uniqueTokens.forEach(function(token) {
        activityNames.push(token["activity.name"]);
        experienceNames.push(token["experience.name"]);
      });
  
      gtag('config', 'TAG_ID');
      gtag('event', 'action_name', {'eventCategory': 'target',
          'eventAction': experienceNames, 'eventLabel': activityNames
      });
    });
  
    function isEmpty(val) {
      return (val === undefined || val == null || val.length <= 0) ? true : false;
    }
  
    function key(obj) {
       return Object.keys(obj)
      .map(function(k) { return k + "" + obj[k]; })
      .join("");
    }
  
    function distinct(arr) {
      var result = arr.reduce(function(acc, e) {
        acc[key(e)] = e;
        return acc;
      }, {});
  
      return Object.keys(result)
      .map(function(k) { return result[k]; });
    }
</script>
```

### Debugging mit dem Äquivalent des ttMeta-Plug-ins

Das Äquivalent des ttMeta-Plug-ins für Debugging-Zwecke kann durch Hinzufügen des folgenden Codes zu der HTML-Seite erstellt werden:

```javascript
<script type="text/javascript" > 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function (e) { 
    window.ttMETA= typeof(window.ttMETA)!="undefined" ? window.ttMETA : []; 
 
    var tokens=e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
     
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      window.ttMETA.push({ 
        'CampaignName': token["activity.name"], 
        'CampaignId' : token["activity.id"], 
        'RecipeName': token["experience.name"], 
        'RecipeId': token["experience.id"], 
        'OfferId': token["offer.id"], 
        'OfferName': token["offer.name"], 
        'MboxName': e.detail.mbox}); 
      console.log(ttMETA); 
    }); 
  }); 
 
  function isEmpty(val){ 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
</script>
```

## ![at.js](/help/main/assets/atjs.png) Schulungsvideo: Antwort-Token und benutzerdefinierte at.js-Ereignisse {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

Im folgenden Video wird erläutert, wie Sie mit Antwort-Token und benutzerdefinierten at.js-Ereignissen Profilinformationen von [!DNL Target] an Drittanbietersysteme weitergeben können.

>[!NOTE]
>
>Die Benutzeroberfläche des [!DNL Target] [!UICONTROL Administration]-Menüs (früher [!UICONTROL Setup]) wurde überarbeitet, um eine verbesserte Leistung zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu reduzieren und das Benutzererlebnis im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind korrekt, die Optionen befinden sich jedoch an etwas anderen Stellen.
>
>Im Video werden `option.name` und `option.id` erwähnt, die durch `offer.name` bzw. `offer.id` ersetzt wurden.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
