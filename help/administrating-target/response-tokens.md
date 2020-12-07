---
keywords: response tokens;tokens;plugins;plug-ins;at.js;response
description: Mithilfe von Antworttoken können Sie automatisch Zielgruppen-spezifische Informationen (Details zur Aktivität, Profil des Benutzers, Geo-Informationen usw.) ausgeben, die beim Debugging oder bei der Integration mit Drittanbietersystemen (z. B. Clicktale) verwendet werden sollen
title: Antwort-Token in Adobe Target
feature: response tokens
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 77%

---


# Antwort-Token{#response-tokens}

Response tokens let you automatically output information specific to [!DNL Target] (activity details, user profile information, geo information, and so forth) to use in debugging or integrating with 3rd-party systems (such as Clicktale).

Mithilfe von Antworttoken können Sie festlegen, welche Variablen genutzt werden sollen, und dann ermöglichen, dass sie als Teil einer Zielgruppe-Antwort gesendet werden. Dazu aktivieren Sie einfach eine Variable mit dem Switch und die Variable wird mit Zielgruppe-Antworten gesendet, die in Netzwerkaufrufen validiert werden können. Response tokens work in [!UICONTROL Preview] mode as well.

Ein wesentlicher Unterschied zwischen Plug-ins und Antwort-Token besteht darin, dass Plug-ins JavaScript für die Seite bereitstellen, das bei Bereitstellung ausgeführt wird, wohingegen Antwort-Token ein Objekt bereitstellen, das anschließend gelesen und auf das mithilfe von Ereignislistenern reagiert werden kann. Weitere Informationen finden Sie unter  [Benutzerdefinierte at.js-Ereignisse](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) und in den Beispielen im späteren Verlauf dieses Artikels. Der Ansatz der Antwort-Token ist sicherer und ermöglicht eine problemlosere Bereitstellung und Wartung von Drittanbieterintegrationen.

>[!NOTE]
>
>Antwort-Token sind mit at.js 1.1 oder höher verfügbar. mbox.js unterstützt keine Antwort-Token.

| Verwendete Target-Bibliothek | Empfohlene Aktionen |
|--- |--- |
| at.js | Stellen Sie sicher, dass Sie at.js der Version 1.1 oder neuer verwenden. Weitere Informationen zum Herunterladen der neuesten Version von at.js finden Sie unter [Herunterladen von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md). Weitere Informationen zu neuen Funktionen in den einzelnen Versionen von at.js finden Sie unter [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).<br>Kunden, die at.js verwenden, sollten Antwort-Token nutzen und auf Plug-ins verzichten. Einige Plug-ins, die auf internen Methoden basieren, die in mbox.js, aber nicht in at.js vorhanden sind, werden zwar bereitgestellt, sie schlagen jedoch fehl. Weitere Informationen finden Sie unter [Einschränkungen von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md). |
| mbox.js | Bei der Verwendung von mbox.js werden Plug-ins weiterhin unterstützt und bereitgestellt.<br>Kunden, die mit mbox.js und Plug-ins arbeiten, sollten jedoch stattdessen at.js und Antwort-Token verwenden. Weitere Informationen zu den Vorteilen von at.js im Vergleich zu mbox.js finden Sie unter [Häufig gestellte Fragen zu at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md). Weitere Informationen zum Migrieren finden Sie unter [Migration von „mbox.js“ zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md).<br>Nach der Einstellung von Target Classic (November 2017) müssen Sie sich möglicherweise an den Kundendienst wenden, um vorhandene Plug-ins bearbeiten oder deaktivieren zu können. Sie sollten Ihre Plug-ins geprüft haben, bevor Target Classic veraltet war und unerwünschte Plug-ins deaktiviert wurden.<br>Sie können keine neuen Plug-ins in Target Standard/Premium erstellen. Verwenden Sie stattdessen Antwort-Token.<br>Alte SiteCatalyst-Plug-ins sollten deaktiviert und durch [Adobe Analytics als Berichtsquelle für Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) ersetzt werden. Das ttMeta-Plugin sollte deaktiviert und durch [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) ersetzt werden. |

## Verwenden von Antwort-Token {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Stellen Sie sicher, dass Sie [!DNL at.js] der Version 1.1 oder neuer verwenden.

   Weitere Informationen finden Sie unter [at.js herunterladen](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2).

1. In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**.

   ![](assets/response_tokens-new.png)

1. Aktivieren Sie die gewünschten Antwort-Token wie `activity.id`, `option.id` usw.

   Die folgenden Parameter sind standardmäßig verfügbar:

   | Typ | Parameter | Hinweise |
   |--- |--- |--- |
   | Integrierte Profile | `profile.activeActivities` | Gibt eine Reihe an `activityIds` aus, für die der Besucher qualifiziert ist. Die Inkrementierung erfolgt im Zuge der Benutzerqualifizierung. For example, on a page with two [!DNL Target] requests delivering two different activities, the second request includes both activities. |
   |  | `profile.isFirstSession` | Gibt „true“ oder „false“ zurück. |
   |  | `profile.isNewSession` | Gibt „true“ oder „false“ zurück. |
   |  | `profile.daysSinceLastVisit` | Gibt die Anzahl der Tage seit dem letzten Zugriff des Besuchers zurück. |
   |  | `profile.tntId` | Gibt die tntID des Besuchers zurück. |
   |  | `profile.marketingCloudVisitorId` | Gibt die Experience Cloud-ID des Besuchers zurück. |
   |  | `profile.thirdPartyId` | Gibt die Drittanbieter-ID des Besuchers zurück. |
   |  | `profile.categoryAffinity` | Gibt die Lieblingskategorie des Besuchers zurück. |
   |  | `profile.categoryAffinities` | Gibt eine Reihe der Top-5-Kategorien des Besuchers als Zeichenfolgen zurück. |
   | Aktivität | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`option.name`<br>`option.id` | Details der aktuellen Aktivität. Beachten Sie, dass „option“ und „offer“ gleich sind. |
   | Geo | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | Weitere Informationen zur Verwendung von Geo-Targeting in Aktivitäten finden Sie unter [Geo](/help/c-target/c-audiences/c-target-rules/geo.md). |
   | Traffic-Zuordnungsmethode<br>(gilt nur für [!UICONTROL Auto-Zielgruppe] - und [!UICONTROL Automated Personalization] -Aktivitäten.) | `experience.trafficAllocationId` | Gibt 0 zurück, wenn ein Besucher ein Erlebnis aus dem &quot;Kontroll&quot;-Traffic erhalten hat, und 1, wenn ein Besucher ein Erlebnis aus der &quot;zielgerichteten&quot; Traffic-Verteilung erhalten hat. |
   |  | `experience.trafficAllocationType` | Gibt &quot;Kontrolle&quot;oder &quot;Targeting&quot;zurück. |

   Benutzerprofil- und Kundenattribute werden ebenfalls in der Liste angezeigt.

   >[!NOTE]
   >
   >Parameter mit Sonderzeichen werden in der Liste nicht angezeigt. Es werden nur alphanumerische Zeichen und Unterstriche unterstützt.

1. (Conditional) If you want to use a profile parameter as a response token, but the parameter has not been passed through a [!DNL Target] request and, thus, has not loaded into the Target UI, you can use the [!UICONTROL Add Response Token] button to add the profile to the UI.

   Klicken Sie auf **[!UICONTROL Hinzufügen Antwort-Token]**, geben Sie den Token-Namen ein und klicken Sie dann auf **[!UICONTROL Aktivieren]**.

   ![](assets/response_token_create.png)

1. Erstellen Sie eine Aktivität.

Use [at.js custom events](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) to listen for the [!DNL Target] response and read the response tokens.

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

Die folgenden Anweisungen zeigen, wie Sie mit dem dynamischer Tag-Manager (DTM) einen benutzerdefinierten [!DNL at.js]-Eventhandler hinzufügen:

1. Anmelden in DTM.
1. Gehen Sie zur gewünschten Eigenschaft.
1. Öffnen Sie das Target-Tool.

   Da DTM keine native Unterstützung für at.js bietet, müssen Sie den Code-Editor verwenden.

1. Hängen Sie im Code-Editor den folgenden Code an [!DNL at.js] an:

   ```json
   document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
     console.log("Request succeeded", e.detail); 
   });
   ```

Sie können das folgende Snippet zur [at.js-Setupseite](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812) der Bibliotheksfußzeile hinzufügen, wenn Sie alles in einer Datei haben möchten.

```json
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
  console.log("Request succeeded", e.detail); 
});
```

## Häufig gestellte Fragen zu Antwort-Token {#section_3DD5F32C668246289CDF9B4CDE1F536D}

**Welche Rolle wird zum Aktivieren oder Deaktivieren von Antwort-Token benötigt?**

Antwort-Token können nur von Benutzern mit der Target-Admin-Rolle aktiviert oder deaktiviert werden.

**Was geschieht, wenn ich at.js 1.0 oder niedriger verwende?**

Die Antwort-Token werden zwar angezeigt, at.js kann sie jedoch nicht verwenden.

**Was geschieht, wenn ich at.js 1.1 (oder neuer) auf einigen Seiten meiner Site verwende, während ich auf anderen Seiten mbox.js nutze?**

Response tokens will be delivered to the [!DNL at.js] Target responses, but not to the [!DNL mbox.js] responses.

**Können Target Classic-Plug-ins und Antwort-Token gleichzeitig aktiv sein?**

Plug-ins und Antwort-Token sind parallel verfügbar, Plug-ins werden jedoch in der Zukunft eingestellt.

**Werden Antworttoken durch alle [!DNL Target] Antworten oder nur durch [!DNL Target] Antworten bereitgestellt, die eine Aktivität liefern?**

Response tokens are delivered only through [!DNL Target] responses delivering an activity.

**Mein Target Classic-Plug-in beinhaltet JavaScript. Wie reproduziere ich diese Funktionalität mithilfe von Antwort-Token?**

Bei der Migration zu Antwort-Token muss dieser JavaScript-Typ in Ihrer Codebase oder der Tag-Management-Lösung beibehalten werden. Sie können diesen Code mithilfe von benutzerdefinierten [!DNL at.js]-Ereignissen auslösen und die Antwort-Token-Werte an Ihre JavaScript-Funktionen übergeben.

**Warum wird mein Profil-/Kundenattribut-Parameter nicht in der Liste der Antwort-Token angezeigt?**

Target aktualisiert die Parameter normalerweise aller 15 Minuten. Diese Aktualisierung ist von der Benutzeraktion abhängig, und die Daten werden nur dann aktualisiert, wenn Sie die Antwort-Token-Seite anzeigen. Wenn Ihre Parameter nicht in der Antwort-Token-Liste angezeigt werden, kann die Ursache dafür sein, dass Target die Daten noch nicht aktualisiert hat.

Wenn Ihr Parameter etwas anderes als nicht-alphanumerische Zeichen oder andere Symbole als Unterstriche enthält, wird der Parameter nicht in der Liste angezeigt. Momentan werden nur alphanumerische Zeichen und Unterstriche unterstützt.

**Stellt der Antwort-Token weiterhin Inhalt bereit, wenn ich ein Antwort-Token mit einem Profilskript oder Profilparameter erstelle und dieses Profilskript oder diesen Parameter dann lösche?**

Antwort-Token extrahieren Informationen aus Benutzerprofilen und stellen diese Informationen dann bereit. Wenn Sie ein Profilskript oder einen Profilparameter löschen, heißt das nicht, dass die Informationen aus den Benutzerprofilen entfernt wurden. Die Benutzerprofile enthalten weiterhin Daten, die dem Profilskript entsprechen. Das Antwort-Token stellt weiterhin den Inhalt bereit. Dieses Token wird nicht für neue Besucher oder Benutzer bereitgestellt, die diese Informationen nicht in ihren Profilen gespeichert haben, weil die Daten nicht in den Profilen vorhanden sind.

Target deaktiviert das Token nicht automatisch. Wenn Sie ein Profilskript löschen und das Token nicht mehr bereitgestellt werden soll, müssen Sie das Token selbst deaktivieren.

**Ich habe mein Profilskript umbenannt. Warum ist das Token, das dieses Skript verwendet, weiterhin mit dem alten Namen aktiv?**

Wie zuvor erwähnt, agieren Antwort-Token mit den für Benutzer gespeicherten Profilinformationen. Obwohl Sie Ihr Profilskript umbenannt haben, ist für Benutzer, die Ihre Website besucht haben, der alte Profilskriptwert in deren Profilen gespeichert. Das Token ruft weiterhin den alten Wert auf, der bereits in den Benutzerprofilen gespeichert ist. Wenn Sie den Inhalt nun für den neuen Namen bereitstellen möchten, müssen Sie das vorherige Token deaktivieren und das neue Token aktivieren.

**Wann werden meine Attribute aus der Liste entfernt, wenn sie sich geändert haben?**

Target führt in regelmäßigen Abständen eine Aktualisierung der Attribute durch. Nicht aktivierte Attribute werden bei der nächsten Aktualisierung entfernt. Wenn jedoch ein Attribut vorhanden ist, das aktiviert und entfernt wurde (wenn Sie beispielsweise ein als Token verwendetes Profilskript entfernt haben), wird dieses Skript erst nach dessen Deaktivierung aus der Attributliste entfernt. Target entfernt die deaktivierten Attribute erst aus der Liste, wenn sie gelöscht oder umbenannt werden.

## Senden von Daten an Google Analytics via at.js  {#section_04AA830826D94D4EBEC741B7C4F86156}

Daten können via at.js an Google Analytics gesendet werden, indem Sie auf der HTML-Seite den folgenden Code hinzufügen:

```javascript
<script type="text/javascript"> 
  (function(i, s, o, g, r, a, m) { 
    i['GoogleAnalyticsObject'] = r; 
    i[r] = i[r] || function() { 
      (i[r].q = i[r].q || []).push(arguments) 
    }, i[r].l = 1 * new Date(); 
    a = s.createElement(o), 
      m = s.getElementsByTagName(o)[0]; 
    a.async = 1; 
    a.src = g; 
    m.parentNode.insertBefore(a, m) 
  })(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga'); 
  ga('create', 'Google Client Id', 'auto'); 
</script> 
 
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
 
    ga('send', 'event', { 
      eventCategory: "target", 
      eventAction: experienceNames, 
      eventLabel: activityNames 
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

## Debugging (ähnelt dem ttMeta-Plug-in)  {#section_DB3392B6E80749C1BFB520732EDF3BCE}

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
        'OfferId': token["option.id"], 
        'OfferName': token["option.name"], 
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

## Schulungsvideo: Antwort-Token und benutzerdefinierte at.js-Ereignisse ![Tutorialzeichen](/help/assets/tutorial.png) {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

Sehen Sie sich das folgende Video an, um zu erfahren, wie Sie Antwort-Token und benutzerspezifische at.js-Ereignisse verwenden können, um Profilinformationen aus Target an Drittanbietersysteme zu übergeben.

>[!NOTE]
>
>Die Benutzeroberfläche des [!DNL Target] Administrationsmenüs [!UICONTROL (früher] Setup ) wurde überarbeitet, um die Leistung zu verbessern, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu verkürzen und die Benutzerfreundlichkeit im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind im Allgemeinen korrekt. Die Optionen befinden sich jedoch möglicherweise an etwas anderen Orten. Aktualisierte Videos werden demnächst veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
