---
keywords: implement target;implementation;implement at.js;tag manager
description: Informationen zur Implementierung von Adobe Target ohne einen Tag-Manager (Adobe Launch oder Dynamic Tag Management).
title: Implementieren von Target ohne einen Tag-Manager
feature: implementation general
subtopic: Getting Started
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: tm+mt
source-git-commit: 12366dd29552a4073a932ddfdb04a1302e775c9e
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 66%

---


# Implementieren von Target ohne einen Tag-Manager{#implement-target-without-a-tag-manager}

Information about implementing [!DNL Adobe Target] without using a tag manager ([!DNL Adobe Launch] or [!DNL Dynamic Tag Manager]).

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ist die bevorzugte Methode zur Implementierung von Target und der „at.js“-Bibliothek. Folgende Informationen gelten nicht, wenn Sie zur Implementierung von Target Adobe Launch verwenden.

Um die Seite &quot; [!UICONTROL Implementierung] &quot;aufzurufen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

Auf dieser Seite können Sie die folgenden Einstellungen festlegen:

* Kontodetails
* Implementierungsmethoden
* Profil-API
* Debugger-Tools
* Datenschutz

>[!NOTE]
>
>Sie können Einstellungen der „at.js“-Bibliothek überschreiben, anstatt die Einstellungen in der Oberfläche von Target Standard/Premium oder durch Verwendung von REST-APIs zu bearbeiten. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Kontodetails

Die folgenden Kontodetails können Ansicht werden. Diese Einstellungen können nicht geändert werden.

| Einstellung | Beschreibung |
| --- | --- |
| Clientcode | Der Clientcode ist eine clientspezifische Folge von Zeichen, die oft benötigt wird, wenn die Target-APIs zum Einsatz kommen. |
| IMS-Organisations-ID | Diese ID ordnet Ihre Implementierung Ihrem [!DNL Adobe Experience Cloud]-Konto zu. |

## Implementierungsmethoden

Die folgenden Einstellungen können im Bereich &quot;Implementierungsmethoden&quot;konfiguriert werden:

### Globale Einstellungen

>[!NOTE]
>
>Diese Einstellungen werden auf alle [!DNL Target] .js-Bibliotheken angewendet. Nachdem Sie Änderungen im Abschnitt [!UICONTROL Implementierungsmethoden] durchgeführt haben, müssen Sie die Bibliothek herunterladen und in Ihrer Implementierung aktualisieren.

|Seitenladung aktiviert (Globale Mbox automatisch erstellen|Wählen Sie aus, ob der globale Mbox-Aufruf in die Datei &quot;at.js&quot;eingebettet werden soll, damit er bei jedem Seitenladevorgang automatisch ausgelöst wird.|
|Globale Mbox|Wählen Sie einen Namen für die globale Mbox aus. Der Standardname lautet target-global-mbox.<br>Sonderzeichen wie das kaufmännische Und (&amp;) können mit at.js für Mbox-Namen verwendet werden.|
|Timeout (seconds)|If [!DNL Target] does not respond with content within the defined period, the server call times out and default content is displayed. Während der Sitzung des Besuchers werden weiter Aufrufe durchgeführt. Der Standardwert liegt bei 5 Sekunden.<br>Die Bibliothek at.js verwendet die Timeout-Einstellung in `XMLHttpRequest`. Der Timeout beginnt, wenn die Anforderung ausgelöst wird, und endet, wenn [!DNL Target] eine Antwort von dem Server erhält. Weitere Informationen dazu finden Sie unter [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) im Mozilla Developer Network.<br>Tritt der festgelegte Timeout vor Erhalt der Antwort ein, wird dem Besucher ein Standardinhalt angezeigt, und der Besucher wird möglicherweise als Teilnehmer in einer Aktivität gezählt, da die gesamte Datenerfassung am [!DNL Target]-Edge erfolgt. Erreicht die Anforderung den [!DNL Target]-Edge, wird der Besucher gezählt.<br>Beim Konfigurieren der Timeout-Einstellung müssen Sie Folgendes beachten:<ul><li>Wenn der Wert zu niedrig ist, erhalten Besucher wahrscheinlich meist nur den Standardinhalt angezeigt, auch wenn sie möglicherweise als Teilnehmer in einer Aktivität gezählt werden.</li><li>Ist der Wert zu hoch, werden Besuchern unter Umständen leere Stellen auf Ihrer Webseite oder komplett leere Seiten angezeigt, falls Sie für längere Zeiträume Textausblendung einsetzen.</li></ul>Genaueres über Mbox-Antwortzeiten erfahren Sie auf der Registerkarte „Netzwerk“ in den Entwicklertools Ihres Browsers. Sie können auch Tools zur Überwachung der Webleistung einsetzen, die von Drittanbietern stammen, wie zum Beispiel Catchpoint.<br>**Hinweis:** Die Einstellung [visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) stellt sicher, dass [!DNL Target] nicht zu lange auf die Antwort der Besucher-API wartet. Diese Einstellung und die hier beschriebene Timeout-Einstellung für at.js beeinflussen sich nicht gegenseitig.|
|Lebensdauer des Profils|Diese Einstellung bestimmt, wie lange Profile des Besuchers gespeichert werden. Profile werden standardmäßig zwei Wochen lang gespeichert. Dies kann auf bis zu 90 Tage erhöht werden.<br>Wenden Sie sich an den [Kundendienst](https://helpx.adobe.com/de/contact/enterprise-support.ec.html), um die Einstellung für die Lebensdauer des Profils zu ändern.|

### Wichtigste Implementierungsmethode

>[!IMPORTANT]
>
>Das Zielgruppe-Team unterstützt &quot;at.js 1&quot;.*x* und at.js 2.*x*. Bitte aktualisieren Sie auf das neueste Update einer der Hauptversionen von at.js, um sicherzustellen, dass Sie eine unterstützte Version ausführen.

Um die gewünschte at.js-Version herunterzuladen, klicken Sie auf die entsprechende **[!UICONTROL Download]** -Schaltfläche.

Um at.js-Einstellungen zu bearbeiten, klicken Sie neben der gewünschten at.js-Version auf &quot; **[!UICONTROL Bearbeiten]** &quot;.

>[!IMPORTANT]
>
>Wenden Sie sich vor dem Ändern dieser Standardeinstellungen an den [Kundendienst](/help/cmp-resources-and-contact-information.md) , damit Sie Ihre aktuelle Implementierung nicht beeinträchtigen.

Zusätzlich zu den oben erläuterten Einstellungen stehen die folgenden spezifischen at.js-Einstellungen zur Verfügung:

| Einstellung | Beschreibung |
|--- |--- |
| Benutzerdefinierte Bibliothekskopfzeile | Fügen Sie benutzerdefiniertes JavaScript hinzu, das oben in der Bibliothek aufgeführt wird. |
| Benutzerdefinierte Bibliotheksfußzeile | Fügen Sie benutzerdefiniertes JavaScript hinzu, das unten in der Bibliothek aufgeführt wird. |

### Profil-API

Aktivieren oder deaktivieren Sie die Authentifizierung für Batch-Aktualisierungen via API und generieren Sie ein Token für die Profilauthentifizierung.

For more information, see [Profile API settings](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md).

### Debugger-Tools

Erstellen Sie ein Autorisierungstoken, um erweiterte [!DNL Target] Debuggingwerkzeuge zu verwenden. Click **[!UICONTROL Generate New Authentication Token]**.

![Neues Authentifizierungstoken erstellen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Datenschutz

Diese Einstellungen ermöglichen Ihnen die Verwendung unter Einhaltung [!DNL Target] der geltenden Datenschutzgesetze.

Wählen Sie die gewünschte Einstellung aus der Dropdown-Liste IP-Adresse des Besuchers verschleiern:

* Verwirrung des letzten Oktetts
* Gesamte IP-Verschleierung
* Keine

Weitere Informationen finden Sie unter  [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).

>[!NOTE]
>
>Die Option &quot;Unterstützung älterer Browser&quot;war in at.js Version 0.9.3 und früher verfügbar. Diese Option wurde in at.js, Version 0.9.4, entfernt. Eine Liste der von at.js unterstützten Browser finden Sie unter [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>Bei älteren Browsern handelt es sich in der Regel um alte Versionen, die CORS (Cross Origin Resource Sharing) nicht vollständig unterstützen. Solche Browser sind zum Beispiel alle Versionen von Internet Explorer vor Version 11 oder Safari Version 6 und ältere Versionen. Wenn die Unterstützung älterer Browser deaktiviert war, stellte Zielgruppe keine Inhalte bereit oder zählte keine Besucher in Berichten in diesen Browsern. Wenn diese Option aktiviert wurde, wird empfohlen, eine Qualitätssicherung in allen älteren Browsern durchzuführen, um eine gute Kundenerfahrung sicherzustellen.

## „at.js“ herunterladen {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructions to download the library using the [!DNL Target] interface or the Download API.

>[!NOTE]
>
>* [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ist die bevorzugte Methode zur Implementierung von Target und der „at.js“-Bibliothek. Folgende Informationen gelten nicht, wenn Sie zur Implementierung von Target Adobe Launch verwenden.
   >
   >
* Das Zielgruppe-Team unterstützt &quot;at.js 1&quot;.*x* und at.js 2.*x*. Bitte aktualisieren Sie auf das neueste Update einer der Hauptversionen von at.js, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).


### Download at.js using the Target interface {#section_1F5EE401C2314338910FC57F9592894E}

So können Sie [!DNL at.js] über die [!DNL Target]-Oberfläche herunterladen:

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Klicken Sie im Abschnitt [!UICONTROL Implementierungsmethoden] auf die Schaltfläche **[!UICONTROL Herunterladen]** neben der gewünschten at.js-Version.

### Download at.js using the Target Download API {#section_C0D9D2A9068144708D08526BA5CA10D0}

So laden Sie [!DNL at.js] mithilfe der API herunter.

1. So finden Sie Ihren Clientcode.

   Your client code is available at the top of the **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** page of the [!DNL Target] interface.

1. So finden Sie Ihre Administratornummer.

   Laden Sie diese URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Replace `client code` with the client code from Step 1.

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

   * Replace `admin number` with your admin number.
   * Replace `client code` with the client code from Step 1.
   * Replace `version number` with the desired at.js version number (for example, 2.2).

   >[!IMPORTANT]
   >
   >Das Target-Team pflegt nur zwei Versionen von [!DNL at.js] – die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Wenn Sie diese URL laden, wird der Download Ihrer angepassten [!DNL at.js]-Datei initiiert.

## at.js implementation {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js sollte im `<head>`-Element jeder Seite Ihrer Website implementiert werden.

Eine typische Implementierung von Target ohne Verwendung eines Tag-Managers wie [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) oder [Dynamic Tag Management](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96) sieht wie folgt aus:

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

* Sie sollten den HTML5-Doctype (z. B. `<!doctype html>`) verwenden. Nicht unterstützte oder ältere Doctypes können dazu führen, dass Target keine Anfragen senden kann.
* Mit den Optionen zum Vorabladen und Vorabruf können Sie die Seitenladezeiten reduzieren. If you use these configurations, ensure that you replace `<client code>` with your own client code, which you can obtain from the **[!UICONTROL Administration]** > **[!UICONTROL Implementation] page.
* Wenn Sie über einen Daten-Layer verfügen, empfiehlt es sich, einen möglichst großen Teil im `<head>` Ihrer Seiten zu definieren, bevor „at.js“ geladen wird. So können diese Informationen optimal für die Target-Personalisierung verwendet werden.
* Spezielle Funktionen wie z. B. `targetPageParams()`, `targetPageParamsAll()`, Datenanbieter und `targetGlobalSettings()` sollten definiert werden, nachdem Sie Ihren Daten-Layer definiert haben und bevor „at.js“ geladen wird. Alternativ können Sie sie im Abschnitt [!UICONTROL Bibliothek-Header] der Seite [!UICONTROL „‚at.js‘-Einstellungen bearbeiten“] oder im Rahmen der „at.js“-Bibliothek selbst speichern. Weitere Informationen zu diesen Funktionen finden Sie unter  [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Wenn Sie unterstützende JavaScript-Bibliotheken wie jQuery verwenden, fügen Sie sie vor Target hinzu, damit Sie beim Erstellen von Target-Erlebnissen ihre Syntax und Methoden nutzen können.
* Fügen Sie „at.js“ im `<head>` Ihrer Seiten hinzu.

## Track conversions {#task_E85D2F64FEB84201A594F2288FABF053}

Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.

>[!NOTE]
>
>Tätigen Benutzer auf Ihrer Website Einkäufe, empfehlen wir die Implementierung einer Auftragsbestätigungs-Mbox, selbst wenn Sie für die Berichterstellung Analytics for Target (A4T) einsetzen.

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