---
keywords: Target implementieren;Implementierung;at.js implementieren;Tag-Manager;On-Device Decisioning;bei Geräteentscheidungen
description: Erfahren Sie, wie Sie die Einstellungen festlegen (Kontodetails, Implementierungsmethoden usw.). zur Implementierung der Adobe [!DNL Target] "at.js"-Bibliothek ohne Verwendung eines Tag-Managers.
title: Kann ich implementieren? [!DNL Target] ohne Tag-Manager?
feature: Implement Server-side
role: Developer
exl-id: cb57f6b8-43cb-485d-a7ea-12db8170013f
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 47%

---

# Implementierung [!DNL Target] ohne Tag-Manager

Informationen zur Implementierung [!DNL Adobe Target] ohne Verwendung von Tag-Manager oder -Tags in [!DNL Adobe Experience Platform].

>[!NOTE]
>
>Tags in [Adobe Experience Platform](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} ist die bevorzugte Methode zur Implementierung von [!DNL Target] und der &quot;at.js&quot;-Bibliothek. Die folgenden Informationen gelten nicht für die Verwendung von Tags in [!DNL Adobe Experience Platform] um [!DNL Target].

So greifen Sie auf die [!UICONTROL Implementierung] Seite, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

Sie können die folgenden Einstellungen auf dieser Seite angeben:

* Kontodetails
* Implementierungsmethoden
* Profil-API
* Debugger-Tools
* Datenschutz

>[!NOTE]
>
>Sie können Einstellungen der at.js-Bibliothek überschreiben, anstatt die Einstellungen in der Oberfläche von [!DNL Target Standard/Premium] oder durch Verwendung von REST-APIs zu bearbeiten. Weitere Informationen finden Sie unter [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

## Kontodetails

Sie können die folgenden Kontodetails anzeigen. Diese Einstellungen können nicht geändert werden.

| Einstellung | Beschreibung |
| --- | --- |
| [!UICONTROL Clientcode] | Der Clientcode ist eine clientspezifische Folge von Zeichen, die oft benötigt wird, wenn die [!DNL Target]-APIs zum Einsatz kommen. |
| [!UICONTROL IMS-Organisations-ID] | Diese ID ordnet Ihre Implementierung Ihrem [!DNL Adobe Experience Cloud]-Konto zu. |
| [!UICONTROL On-Device Decisioning] | Um die Entscheidungsfindung auf dem Gerät zu aktivieren, schieben Sie den Umschalter in die Position &quot;Ein&quot;.<br>Über die geräteübergreifende Entscheidungsfindung können Sie Ihre A/B- und [!UICONTROL Erlebnis-Targeting] (XT) Kampagnen auf Ihrem Server und führen speicherinterne Entscheidungen bei nahezu null Latenz durch. Weitere Informationen finden Sie unter [Einführung in die geräteübergreifende Entscheidungsfindung](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank} im *[!DNL Adobe Target]SDKs* Handbuch. |
| [!UICONTROL Schließen Sie alle vorhandenen Entscheidungsaktivitäten auf dem Gerät in das Artefakt ein.] | (Bedingt) Diese Option wird angezeigt, wenn Sie die Entscheidungsfindung auf dem Gerät aktivieren.<br>Schalten Sie den Umschalter in die &quot;Ein&quot;-Position, wenn Sie möchten, dass alle Ihre Live-Target-Aktivitäten, die für die Entscheidungsfindung auf dem Gerät geeignet sind, automatisch in das Artefakt einbezogen werden.<br>Wenn Sie diesen Umschalter deaktivieren, müssen Sie alle Entscheidungsaktivitäten auf dem Gerät neu erstellen und aktivieren, damit sie in das generierte Regelartefakt aufgenommen werden. |

## Implementierungsmethoden

Die folgenden Einstellungen können im Bereich Implementierungsmethoden konfiguriert werden:

### Globale Einstellungen

>[!NOTE]
>
>Diese Einstellungen werden auf alle [!DNL Target] .js-Bibliotheken. Nachdem Sie Änderungen im Abschnitt &quot;Implementierungsmethoden&quot;vorgenommen haben, müssen Sie die Bibliothek herunterladen und in Ihrer Implementierung aktualisieren.

| Einstellung | Beschreibung |
| --- | --- |
| Seitenladeaktivierung (globale Mbox automatisch erstellen | Wählen Sie aus, ob der globale Mbox-Aufruf in die Datei at.js integriert werden soll, damit er automatisch bei jedem Laden der Seite aktiviert wird. |
| Globale Mbox | Wählen Sie einen Namen für die globale Mbox aus. Der Standardname lautet target-global-mbox.<br>Sonderzeichen wie das kaufmännische Und (&amp;) können mit at.js für Mbox-Namen verwendet werden. |
| Zeitüberschreitung (Sekunden) | Falls [!DNL Target] nicht innerhalb des festgelegten Zeitraums mit Inhalten antwortet, erfolgt ein Timeout für den Server-Aufruf und es werden Standardinhalte angezeigt. Während der Sitzung des Besuchers werden weiter Aufrufe durchgeführt. Der Standardwert liegt bei 5 Sekunden.<br>Die Bibliothek at.js verwendet die Timeout-Einstellung in `XMLHttpRequest`. Der Timeout beginnt, wenn die Anforderung ausgelöst wird, und endet, wenn [!DNL Target] eine Antwort von dem Server erhält. Weitere Informationen dazu finden Sie unter [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) im Mozilla Developer Network.<br>Tritt der festgelegte Timeout vor Erhalt der Antwort ein, wird dem Besucher ein Standardinhalt angezeigt, und der Besucher wird möglicherweise als Teilnehmer in einer Aktivität gezählt, da die gesamte Datenerfassung am [!DNL Target]-Edge erfolgt. Erreicht die Anforderung den [!DNL Target]-Edge, wird der Besucher gezählt.<br>Beim Konfigurieren der Timeout-Einstellung müssen Sie Folgendes beachten:<ul><li>Wenn der Wert zu niedrig ist, erhalten Besucher wahrscheinlich meist nur den Standardinhalt angezeigt, auch wenn sie möglicherweise als Teilnehmer in einer Aktivität gezählt werden.</li><li>Ist der Wert zu hoch, werden Besuchern unter Umständen leere Stellen auf Ihrer Webseite oder komplett leere Seiten angezeigt, falls Sie für längere Zeiträume Textausblendung einsetzen.</li></ul>Genaueres über Mbox-Antwortzeiten erfahren Sie auf der Registerkarte „Netzwerk“ in den Entwicklertools Ihres Browsers. Sie können auch Tools zur Überwachung der Webleistung einsetzen, die von Drittanbietern stammen, wie zum Beispiel Catchpoint.<br>**Hinweis**: Die [visitorApiTimeout](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)Die Einstellung {target=_blank} stellt sicher, dass [!DNL Target] wartet nicht zu lange auf die Antwort der Besucher-API. Diese Einstellung und die hier beschriebene Timeout-Einstellung für at.js beeinflussen sich nicht gegenseitig. |
| Profillebensdauer | Mit dieser Einstellung legen Sie fest, wie lange Besucherprofile gespeichert werden. Profile werden standardmäßig zwei Wochen lang gespeichert. Diese Einstellung kann auf 90 Tage erhöht werden.<br>Wenden Sie sich an den [Kundendienst](https://helpx.adobe.com/de/contact/enterprise-support.ec.html), wenn Sie die Profillebensdauer ändern möchten. |

### Wichtigste Implementierungsmethode

>[!IMPORTANT]
>
>Das Target-Team unterstützt beide at.js 1.*x* und at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen.

Um die gewünschte at.js-Version herunterzuladen, klicken Sie auf die entsprechende **[!UICONTROL Download]** Schaltfläche.

Um at.js-Einstellungen zu bearbeiten, klicken Sie auf **[!UICONTROL Bearbeiten]** neben der gewünschten at.js-Version.

>[!IMPORTANT]
>
>Wenden Sie sich vor dem Ändern dieser Standardeinstellungen an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md) sodass Sie sich nicht auf Ihre aktuelle Implementierung auswirken.

Zusätzlich zu den oben erläuterten Einstellungen sind auch die folgenden spezifischen at.js-Einstellungen verfügbar:

| Einstellung | Beschreibung |
|--- |--- |
| Benutzerdefinierte Bibliothekskopfzeile | Fügen Sie benutzerdefiniertes JavaScript hinzu, das oben in der Bibliothek aufgeführt wird. |
| Benutzerdefinierte Bibliotheksfußzeile | Fügen Sie benutzerdefiniertes JavaScript hinzu, das unten in der Bibliothek aufgeführt wird. |

### Implementierungsmethoden mit On-Device Decisioning

Ab Version 2.5.0 bietet at.js Entscheidungen auf Geräten. Über die Entscheidungsfindung auf dem Gerät können Sie Ihre [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) und [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) (XT) -Aktivitäten im Browser, um speicherinterne Entscheidungen ohne blockierende Netzwerkanforderung für die [!DNL Adobe Target] Edge Network.

Weitere Informationen finden Sie unter Themen:

* [Entscheidungsfindung auf dem Gerät für Client-seitige](https://developer.adobe.com/target/implement/client-side/){target=_blank}
* [Entscheidungsfindung auf dem Gerät für Server-seitig](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank}

### Profil-API

Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.

Weitere Informationen finden Sie unter [Profil-API-Einstellungen](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/profile-api-settings/).

### Debugger-Tools

Autorisierungstoken zur Verwendung erweiterter [!DNL Target] Debugging-Tools. Klicken **[!UICONTROL Neues Authentifizierungstoken generieren]**.

![Neues Authentifizierungstoken erstellen](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Datenschutz

Mit diesen Einstellungen können Sie [!DNL Target] in Übereinstimmung mit den geltenden Datenschutzgesetzen.

Wählen Sie die gewünschte Einstellung aus der Dropdownliste Besucher-IP-Adresse verschleiern aus:

* Verschleierung des letzten Oktetts
* Gesamte IP-Verschleierung
* Keine

Weitere Informationen finden Sie unter   [Datenschutz](https://developer.adobe.com/target/before-implement/privacy/privacy/).

>[!NOTE]
>
>Die Option Unterstützung älterer Browser war in at.js , Version 0.9.3 und älter verfügbar. Diese Option wurde in at.js, Version 0.9.4, entfernt. Eine Liste der von at.js unterstützten Browser finden Sie unter [Unterstützte Browser](https://developer.adobe.com/target/before-implement/supported-browsers/).<br>Bei älteren Browsern handelt es sich in der Regel um alte Versionen, die CORS (Cross Origin Resource Sharing) nicht vollständig unterstützen. Solche Browser sind zum Beispiel alle Versionen von Internet Explorer vor Version 11 oder Safari Version 6 und ältere Versionen. Wenn die Unterstützung älterer Browser deaktiviert war, stellte Target keine Inhalte bereit und zählte keine Besucher in Berichten zu diesen Browsern. Wenn diese Option aktiviert wurde, wird empfohlen, eine Qualitätssicherung für ältere Browser durchzuführen, um ein gutes Kundenerlebnis zu gewährleisten.

## „at.js“ herunterladen  {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Anleitung zum Herunterladen der Bibliothek mit dem [!DNL Target] -Benutzeroberfläche oder der Download-API.

>[!NOTE]
>
>* [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} ist die bevorzugte Methode zur Implementierung von [!DNL Target] und der &quot;at.js&quot;-Bibliothek. Die folgenden Informationen gelten nicht für die Verwendung von Tags in [!DNL Adobe Experience Platform] um [!DNL Target].
>
>* Die [!DNL Target] -Team unterstützt beide at.js 1.*x* und at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung einer der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/).


### Herunterladen von at.js mithilfe der [!DNL Target] Benutzeroberfläche {#section_1F5EE401C2314338910FC57F9592894E}

So können Sie [!DNL at.js] über die [!DNL Target]-Oberfläche herunterladen:

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Aus dem [!UICONTROL Implementierungsmethoden] klicken Sie auf die **[!UICONTROL Download]** neben der gewünschten at.js-Version.

### Herunterladen von at.js mithilfe der [!DNL Target] Download-API {#section_C0D9D2A9068144708D08526BA5CA10D0}

So laden Sie [!DNL at.js] mithilfe der API herunter.

1. So finden Sie Ihren Clientcode.

   Ihr Client-Code ist oben im **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** der [!DNL Target] -Schnittstelle.

1. So finden Sie Ihre Administratornummer.

   Laden Sie diese URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Ersetzen `client code` mit dem Clientcode aus Schritt 1.

   Das Ergebnis nach dem Laden dieser URL sollte in etwa wie im folgenden Beispiel aussehen:

   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```

   In diesem Beispiel lautet die Administratornummer „6“.

1. Download [!DNL at.js].

   Laden Sie diese URL mit der folgenden Struktur:

   ```
   https://admin<varname>admin number</varname>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code</varname>&version=<version number>
   ```

   * Ersetzen `admin number` mit Ihrer Administratornummer.
   * Ersetzen `client code` mit dem Clientcode aus Schritt 1.
   * Ersetzen `version number` mit der gewünschten at.js-Versionsnummer (z. B. 2.2).

   >[!IMPORTANT]
   >
   >Das Target-Team pflegt nur zwei Versionen von [!DNL at.js] – die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/).

   Wenn Sie diese URL laden, wird der Download Ihrer angepassten [!DNL at.js]-Datei initiiert.

## at.js-Implementierung {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js sollte im `<head>`-Element jeder Seite Ihrer Website implementiert werden.

Eine typische Implementierung von Target ohne Verwendung eines Tag-Managers, z. B. Tags in [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} sieht wie folgt aus:

```
<!doctype html> 
<html> 
<head> 
    <meta charset="utf-8"> 
    <title>Title of the Page</title> 
    <!--Preconnect and DNS-Prefetch to improve page load time--> 
    <link rel="preconnect" href="//<client code>.tt.omtrdc.net"> 
    <link rel="dns-prefetch" href="//<client code>.tt.omtrdc.net"> 
    <!--/Preconnect and DNS-Prefetch--> 
    <!--Data Layer to enable rich data collection and targeting--> 
    <script> 
        var digitalData = { 
            "page": { 
                "pageInfo": { 
                    "pageName": "Home" 
                } 
            } 
        }; 
    </script> 
    <!--/Data Layer--> 
    <!-- targetPageParams(), targetPageParamsAll(), Data Providers or targetGlobalSettings() functions to enrich the visitor profile or modify the library settings--> 
    <script> 
        targetPageParams = function() { 
            return { 
                "a": 1, 
                "b": 2, 
                "pageName": digitalData.page.pageInfo.pageName, 
                "profile": { 
                    "age": 26, 
                    "country": { 
                        "city": "San Francisco" 
                    } 
                } 
            }; 
        }; 
    </script> 
    <!--/targetPageParams()--> 
 
    <!--jQuery or other helper libraries should be implemented before at.js if you would like to use their methods in Target--> 
    <script src="jquery-3.3.1.min.js"></script> 
    <!--/jQuery--> 
    <!--Target's JavaScript SDK, at.js--> 
    <script src="at.js"></script> 
    <!--/at.js--> 
</head>
<body> 
    The default content of the page 
</body> 
</html>
```

Beachten Sie folgende wichtige Hinweise:

* Der Doctype HTML5 (z. B. `<!doctype html>`) verwendet werden. Nicht unterstützte oder ältere Doctypes können dazu führen, dass Target keine Anfragen senden kann.
* Mit den Optionen zum Vorabladen und Vorabruf können Sie die Seitenladezeiten reduzieren. Wenn Sie diese Konfigurationen verwenden, stellen Sie sicher, dass Sie `<client code>` mit Ihrem eigenen Clientcode, den Sie aus dem **[!UICONTROL Administration]** > **[!UICONTROL Implementierung] Seite.
* Wenn Sie über einen Daten-Layer verfügen, empfiehlt es sich, einen möglichst großen Teil im `<head>` Ihrer Seiten zu definieren, bevor „at.js“ geladen wird. Diese Platzierung bietet die maximale Möglichkeit, diese Informationen in Target zur Personalisierung zu verwenden.
* Spezielle Funktionen wie z. B. `targetPageParams()`, `targetPageParamsAll()`, Datenanbieter und `targetGlobalSettings()` sollten definiert werden, nachdem Sie Ihren Daten-Layer definiert haben und bevor „at.js“ geladen wird. Alternativ können diese Funktionen im [!UICONTROL Bibliothekskopfzeile] Abschnitt [!UICONTROL &quot;at.js&quot;-Einstellungen bearbeiten] und als Teil der at.js-Bibliothek selbst gespeichert. Weitere Informationen zu diesen Funktionen finden Sie unter  [„at.js“-Funktionen](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/).
* Wenn Sie JavaScript-Hilfsbibliotheken wie jQuery verwenden, schließen Sie sie vor Target ein, damit Sie beim Erstellen von Target-Erlebnissen deren Syntax und Methoden verwenden können.
* Fügen Sie „at.js“ im `<head>` Ihrer Seiten hinzu.

## Konversionen verfolgen {#task_E85D2F64FEB84201A594F2288FABF053}

Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.

>[!NOTE]
>
>Wenn Benutzer auf Ihrer Website Einkäufe tätigen, empfiehlt Adobe die Implementierung einer Auftragsbestätigungs-Mbox, selbst wenn Sie für Ihre Berichterstellung Analytics for Target (A4T) verwenden.

1. Fügen Sie auf Ihrer Bestellungsdetailseite das Mbox-Skript ein. Befolgen Sie dabei das folgende Modell:
1. Ersetzen Sie die WORTE IN GROSSBUCHSTABEN entweder durch dynamische oder statische Werte aus Ihrem Katalog.

   >[!NOTE]
   >
   >Trennen Sie mehrere Produkt-IDs mithilfe von Kommas.

   **Tipp:** Sie können Informationen auch in beliebigen anderen Mboxes senden (sie müssen nicht `orderConfirmPage` genannt werden). Darüber hinaus können Bestellinformationen auch an mehrere Mboxes innerhalb derselben Kampagne weitergegeben werden.

   ```
   <script type="text/javascript"> 
   adobe.target.trackEvent({ 
       "mbox": "orderConfirmPage", 
       "params":{  
           "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
           "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
           "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
       } 
   }); 
   </script> 
   ```

Die Mbox für die Auftragsbestätigung verwendet die folgenden Parameter:

| Parameter | Beschreibung |
|--- |--- |
| orderId | Eindeutiger Wert zur Identifizierung einer Bestellung für die Konversionszählung.<br>`orderId` muss eindeutig sein. Doppelte Bestellungen werden in Berichten ignoriert. |
| orderTotal | Geldwert des Einkaufs.<br>Das Währungssymbol wird nicht übergeben. Verwenden Sie einen Dezimalpunkt (kein Komma), um die Dezimalwerte anzugeben. |
| productPurchasedId (optional) | Kommagetrennte Liste von Produkt-IDs, die innerhalb der Bestellung gekauft wurden.<br>Diese Produkt-IDs werden im Audit-Bericht angezeigt, um die zusätzliche Berichtanalyse zu unterstützen. |
