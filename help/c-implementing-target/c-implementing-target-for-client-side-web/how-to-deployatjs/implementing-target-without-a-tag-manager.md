---
description: Informationen zur Implementierung von Adobe Target ohne einen Tag-Manager (Adobe Launch oder Dynamic Tag Management).
keywords: Bestellbestätigung;orderConfirmPage
seo-description: Informationen zur Implementierung von Adobe Target ohne einen Tag-Manager (Adobe Launch oder Dynamic Tag Management).
seo-title: Implementieren von Target ohne einen Tag-Manager
solution: Target
subtopic: Erste Schritte
title: Implementieren von Target ohne einen Tag-Manager
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: tm+mt
source-git-commit: ffa6585834b271838629d65ceb00d1770b37e80c

---


# Implementieren von Target ohne einen Tag-Manager{#implement-target-without-a-tag-manager}

Informationen zur Implementierung [!DNL Adobe Target] ohne Verwendung eines Tag-Managers (Adobe Launch oder dynamisches Tag-Management).

## Implementieren von Target ohne einen Tag-Manager {#topic_397FFA3D6918456BBE02A9FBE9537894}

Informationen zur Implementierung von Adobe Target ohne einen Tag-Manager (Adobe Launch oder Dynamic Tag Management).

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ist die bevorzugte Methode zur Implementierung von Target und der „at.js“-Bibliothek. Folgende Informationen gelten nicht, wenn Sie zur Implementierung von Target Adobe Launch verwenden.

## „at.js“-Konfigurationen{#concept_2FA0456607D04F82B0539C5BF5309812}

Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „at.js“-Einstellungsseite unterstützen.

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ist die bevorzugte Methode zur Implementierung von Target und der „at.js“-Bibliothek. Folgende Informationen gelten nicht, wenn Sie zur Implementierung von Target Adobe Launch verwenden.

>[!NOTE]
>
>Sie können Einstellungen der „at.js“-Bibliothek überschreiben, anstatt die Einstellungen in der Oberfläche von Target Standard/Premium oder durch Verwendung von REST-APIs zu bearbeiten. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

So öffnen Sie die Seite [!UICONTROL Einstellungen]:

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]**.
1. Wählen Sie **[!UICONTROL at.js]** &gt; **[!UICONTROL at.js-Einstellungen bearbeiten]** aus.

## Einstellungen zur Inhaltsbereitstellung {#section_118D290DFC444509AD8E4AE86C9D92C0}

Wenden Sie sich an ClientCare, bevor Sie Änderungen an diesen Einstellungen vornehmen. Diese Einstellungen sind für den Großteil der Implementierungen erforderlich.

| Einstellung | Beschreibung |
|--- |--- |
| Globale Mbox automatisch erstellen | Wählen Sie aus, ob der globale Mbox-Aufruf in die Datei at.js integriert werden soll, damit er automatisch bei jedem Laden der Seite aktiviert wird.<br>Eine Änderung dieser Einstellung wirkt sich sowohl auf at.js als auch auf mbox.js aus. |
| Globaler Mbox-Name | Wählen Sie einen Namen für die globale Mbox aus. Der Standardname lautet target-global-mbox.<br>Sonderzeichen wie das kaufmännische Und (&amp;) können mit at.js für Mbox-Namen verwendet werden.<br>Eine Änderung dieser Einstellung wirkt sich sowohl auf at.js als auch auf mbox.js aus. |

## Erweiterte Einstellungen {#section_33B697B77BA64A01B5939D7EC75231F2}

| Einstellung | Beschreibung |
|--- |--- |
| Clientcode | Der Clientcode ist eine clientspezifische Folge von Zeichen, die oft benötigt wird, wenn die Target-APIs zum Einsatz kommen.<br>Diese Einstellung kann nicht geändert werden. |
| IMS-Organisations-ID | Diese ID ordnet Ihre Implementierung Ihrem [!DNL Adobe Experience Cloud]-Konto zu.<br>Diese Einstellung kann nicht geändert werden. |
| Profillebensdauer | Mit dieser Einstellung legen Sie fest, wie lange Besucherprofile gespeichert werden. Profile werden standardmäßig zwei Wochen lang gespeichert. Dies kann auf bis zu 90 Tage erhöht werden.<br>Wenden Sie sich an den [Kundendienst](https://helpx.adobe.com/contact/enterprise-support.ec.html), wenn Sie die Profillebensdauer ändern möchten. |
| X-Domäne | Legt fest, ob der Browser die Cookies in Ihrer eigenen Domäne (Erstanbieter-Cookies), in der Target-Domäne oder in beiden Domänen einrichtet.<br>Eine Änderung dieser Einstellung wirkt sich sowohl auf at.js als auch auf mbox.js aus. |
| Zeitüberschreitung | Falls [!DNL Target] nicht innerhalb des festgelegten Zeitraums mit Inhalten antwortet, erfolgt ein Timeout für den Server-Aufruf und es werden Standardinhalte angezeigt. Während der Sitzung des Besuchers werden weiter Aufrufe durchgeführt. Der Standardwert liegt bei 5 Sekunden.<br>Eine Änderung dieser Einstellung wirkt sich sowohl auf at.js als auch auf mbox.js aus.<br>Die Bibliothek at.js verwendet die Timeout-Einstellung in `XMLHttpRequest`. Der Timeout beginnt, wenn die Anforderung ausgelöst wird, und endet, wenn Target eine Antwort von dem Server erhält. Weitere Informationen dazu finden Sie unter [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) im Mozilla Developer Network.<br>Tritt der festgelegte Timeout vor Erhalt der Antwort ein, wird dem Besucher ein Standardinhalt angezeigt, und der Besucher wird möglicherweise als Teilnehmer in einer Aktivität gezählt, da die gesamte Datenerfassung am [!DNL Target]-Edge erfolgt. Erreicht die Anforderung den [!DNL Target]-Edge, wird der Besucher gezählt.<br>Beim Konfigurieren der Timeout-Einstellung müssen Sie Folgendes beachten:<ul><li>Wenn der Wert zu niedrig ist, erhalten Besucher wahrscheinlich meist nur den Standardinhalt angezeigt, auch wenn sie möglicherweise als Teilnehmer in einer Aktivität gezählt werden.</li><li>Ist der Wert zu hoch, werden Besuchern unter Umständen leere Stellen auf Ihrer Webseite oder komplett leere Seiten angezeigt, falls Sie für längere Zeiträume Textausblendung einsetzen.</li></ul>Genaueres über Mbox-Antwortzeiten erfahren Sie auf der Registerkarte „Netzwerk“ in den Entwicklertools Ihres Browsers. Sie können auch Tools zur Überwachung der Webleistung einsetzen, die von Drittanbietern stammen, wie zum Beispiel Catchpoint.<br>**Hinweis:** Die Einstellung [visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) stellt sicher, dass [!DNL Target] nicht zu lange auf die Antwort der Besucher-API wartet. Diese Einstellung und die hier beschriebene Timeout-Einstellung für at.js beeinflussen sich nicht gegenseitig. |
| Unterstützung älterer Browser | **Hinweis:** Die Option „Unterstützung älterer Browser“ ist in at.js, Version 0.9.3, und älter, verfügbar. Diese Option wurde in at.js, Version 0.9.4, entfernt. Eine Liste der von at.js unterstützten Browser finden Sie unter [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>Bei älteren Browsern handelt es sich in der Regel um alte Versionen, die CORS (Cross Origin Resource Sharing) nicht vollständig unterstützen. Solche Browser sind zum Beispiel alle Versionen von Internet Explorer vor Version 11 oder Safari Version 6 und ältere Versionen. Wenn die Unterstützung älterer Browser deaktiviert ist, stellt Target keine Inhalte bereit und zählt keine Besucher für Berichte, wenn ein entsprechender Browser genutzt wird. Falls diese Option verwendet wird, ist es empfehlenswert, eine Qualitätssicherung für ältere Browser durchzuführen und so für ein gutes Kundenerlebnis zu sorgen. |

## Code-Einstellungen   {#section_D41C905D0F8149949F525C85F2CCFF7F}

| Einstellung | Beschreibung |
|--- |--- |
| Bibliotheksüberschrift | Fügen Sie benutzerdefiniertes JavaScript hinzu, das oben in der Bibliothek aufgeführt wird. |
| Bibliotheksfußzeile | Fügen Sie benutzerdefiniertes JavaScript hinzu, das unten in der Bibliothek aufgeführt wird. |

## „at.js“ herunterladen {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Anleitung zum Herunterladen der Bibliothek mithilfe der Target-Benutzeroberfläche oder der Download-API.

<!-- 

ov2/c_target-configure-atjs.xml

 -->

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ist die bevorzugte Methode zur Implementierung von Target und der „at.js“-Bibliothek. Folgende Informationen gelten nicht, wenn Sie zur Implementierung von Target Adobe Launch verwenden.

>[!IMPORTANT]
>
>Das Target-Team pflegt nur zwei Versionen von [!DNL at.js] – die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

## „at.js“ über die Target-Oberfläche herunterladen{#section_1F5EE401C2314338910FC57F9592894E}

So können Sie [!DNL at.js] über die [!DNL Target]-Oberfläche herunterladen:

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]**.
1. Wählen Sie **[!UICONTROL at.js aus]**.
1. Klicken Sie auf **[!UICONTROL „at.js“ herunterladen]**.

## at.js über die Target-Download-API herunterladen {#section_C0D9D2A9068144708D08526BA5CA10D0}

So laden Sie [!DNL at.js] mithilfe der API herunter.

1. So finden Sie Ihren Clientcode.

   Ihr Clientcode befindet sich oben auf der Seite **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]** &gt; **[!UICONTROL at.js-Einstellungen bearbeiten]** der [!DNL Target]-Benutzeroberfläche.

1. So finden Sie Ihre Administratornummer.

   Laden Sie diese URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Ersetzen Sie den ` < *`Clientcode`*>` durch den Clientcode aus Schritt 1.

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
   https://admin<varname>admin number</varname>>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code </varname>version=<version number>
   ```

   * Ersetzen Sie die ` < *`Administratornummer`*>` durch Ihre Administratornummer.
   * Ersetzen Sie den ` < *`Clientcode`*>` durch den Clientcode aus Schritt 1.
   * Ersetzen Sie die ` < *`Versionsnummer`*>` durch die gewünschte [[!DNL at.js]-Versionsnummer](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (z. B. 1.6.2).
   >[!IMPORTANT]
   >
   >Das Target-Team pflegt nur zwei Versionen von [!DNL at.js] – die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Wenn Sie diese URL laden, wird der Download Ihrer angepassten [!DNL at.js]-Datei initiiert.

## „at.js“-Implementierung{#concept_03CFA86973A147839BEB48A06FEE5E5A}

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
* Mit den Optionen zum Vorabladen und Vorabruf können Sie die Seitenladezeiten reduzieren. Stellen Sie bei der Verwendung dieser Konfigurationen sicher, dass Sie `<client code>` durch Ihren eigenen Clientcode ersetzen, den Sie über **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]** &gt; **[!UICONTROL at.js-Einstellungen bearbeiten]** abrufen können.
* Wenn Sie über einen Daten-Layer verfügen, empfiehlt es sich, einen möglichst großen Teil im `<head>` Ihrer Seiten zu definieren, bevor „at.js“ geladen wird. So können diese Informationen optimal für die Target-Personalisierung verwendet werden.
* Spezielle Funktionen wie z. B. `targetPageParams()`, , `targetPageParamsAll()`, Datenanbieter und `targetGlobalSettings()` sollten definiert werden, nachdem Sie Ihren Daten-Layer definiert haben und bevor „at.js“ geladen wird. Alternativ können Sie sie im Abschnitt [!UICONTROL Bibliothek-Header] der Seite [!UICONTROL „‚at.js‘-Einstellungen bearbeiten“] oder im Rahmen der „at.js“-Bibliothek selbst speichern. Weitere Informationen zu diesen Funktionen finden Sie unter   [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Wenn Sie unterstützende JavaScript-Bibliotheken wie jQuery verwenden, fügen Sie sie vor Target hinzu, damit Sie beim Erstellen von Target-Erlebnissen ihre Syntax und Methoden nutzen können.
* Fügen Sie „at.js“ im `<head>` Ihrer Seiten hinzu.

## Konversions-Tracking {#task_E85D2F64FEB84201A594F2288FABF053}

Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.

<!-- 

ov/t_create_orderconfirm-page-mbox-atjs.xml

 -->

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