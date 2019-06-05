---
description: Upgrade von at. js 1. x auf at. js 2. x
keywords: at.js-Releases;at.js-Versionen;Einzelseiten-App;SPA
seo-description: Detaillierte Informationen zur Aktualisierung von Adobe Target at.js 1.x auf at.js, Version 2.0.0
seo-title: 'Aktualisierung von Adobe Target at.js, Version 1.x, auf at.js, Version 2.0.0 '
solution: Target
subtopic: Erste Schritte
title: Upgrade von at. js 1. x auf at. js 2. x
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
translation-type: tm+mt
source-git-commit: 6d3d8468dc65fc350dcf7d669039fae79015455d

---


# Upgrade von at. js 1. x auf at. js 2. x {#upgrading-from-atjs-1x-to-atjs-200}

Die neueste Version von at. js bietet [!DNL Adobe Target] umfangreiche Funktionssätze, die Ihr Unternehmen zur Durchführung der Personalisierung auf den nächsten clientseitigen Technologien bereitstellen. Diese neue Version konzentriert sich auf die Aktualisierung von at.js, um harmonische Interaktionen mit Einzelseitenanwendungen (SPAs) zu ermöglichen.

Hier einige Vorteile der Verwendung von at. js 2. x, die in früheren Versionen nicht verfügbar sind:

* Möglichkeit zur Zwischenspeicherung aller Angebote beim Seitenladen, um mehrere Server-Aufrufe auf einen einzelnen Server-Aufruf zu reduzieren
* Drastische Verbesserung der Erlebnisse Ihrer Endbenutzer auf Ihrer Site, da Angebote sofort über den Cache angezeigt werden, ohne dass durch herkömmliche Server-Aufrufe Latenz entsteht
* Einfache Einrichtung mit einmaliger, einzeiliger Codeeingabe und Entwicklerunterstützung, sodass Ihre Marketer A/B- und XT-Aktivitäten über VEC in Ihren SPAs erstellen und ausführen können

## at. js 2. x-Systemdiagramme

Die folgenden Diagramme helfen Ihnen, den Arbeitsablauf von at. js 2. x mit Ansichten zu verstehen und die Einzelseitenintegration zu verbessern. Eine bessere Einführung der in at. js 2. x verwendeten Konzepte finden Sie unter [Implementierung der Einzelseitenanwendung](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Fluss mit at. js 2. x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Aufruf | Details |
| --- | --- |
| 1 | Ein Aufruf gibt die [!DNL Experience Cloud ID] zurück, falls sich der Benutzer authentifiziert hat. Bei einem weiteren Aufruf wird die Kunden-ID synchronisiert. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>at.js kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert wird. |
| 3 | Es wird eine Seitenlade-Anfrage durchgeführt, in der alle konfigurierten Parameter (MCID, SDID und Kunden-ID) enthalten sind. |
| 4 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist. Der Speicher ruft geeignete Zielgruppen aus der Zielgruppenbibliothek ab (beispielsweise über Adobe Analytics, Zielgruppen-Management etc. bereitgestellte Zielgruppen).<br>Kundenattribute werden in einem Batch-Prozess an den Profilspeicher übermittelt. |
| 5 | Basierend auf den URL-Anfrageparametern und den Profildaten entscheidet [!DNL Target], welche Aktivitäten und Erlebnisse für die aktuelle Seite und zukünftige Ansichten an den Besucher zurückgegeben werden sollen. |
| 6 | Zielgerichteter Inhalt wird zurück an die Seite übermittelt. Dieser enthält optional Profilwerte für eine weitere Personalisierung.<br>Die zielgerichteten Inhalte auf der aktuellen Seite werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern.<br>Zielgerichtete Inhalte für Ansichten, die als Ergebnis von Benutzeraktionen in einer SPA, die im Browser zwischengespeichert wird, angezeigt werden. Die SPA kann sofort ohne zusätzlichen Serveraufruf angewendet werden, wenn die Ansichten durch `triggerView()` ausgelöst werden. |
| 7 | Analytics-Daten werden an Datenerfassungsserver übermittelt. |
| 8 | Zielgerichtete Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt.<br>Analytics-Daten können dann sowohl in Analytics als auch in Target eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs Analytics for Target (A4T). |

Egal, wo `triggerView()` in Ihrer SPA implementiert ist, werden die Ansichten und Aktionen aus dem Cache abgerufen und dem Benutzer ohne Serveraufruf gezeigt. `triggerView()` sendet außerdem eine Benachrichtigungsanfrage an das [!DNL Target]-Backend, um Impressions-Zählungen zu erhöhen und aufzuzeichnen.

![Target-Fluss at. js 2. x triggerview](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Aufruf | Details |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 3 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den [!DNL Target]-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

## at. js 2. x bereitstellen {#deploy-atjs-200}

1. Stellen Sie at. js 2. x über die [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) -Erweiterung bereit.

   >[!NOTE]
   >
   > Die Bereitstellung von at. js mit Adobe Launch ist die bevorzugte Methode.

   Oder

   Laden Sie at. js 2. x manuell über die Target-Benutzeroberfläche herunter und stellen Sie sie mithilfe der [Methode Ihrer Wahl bereit](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

## Nicht mehr unterstützte Funktionen von at.js

Es gibt mehrere Funktionen, die in at. js 2. x nicht mehr unterstützt wurden.

>[!IMPORTANT]
>
>Wenn diese veralteten Funktionen weiterhin auf Ihrer Site verwendet werden, wenn at. js 2. x bereitgestellt wird, werden Konsolenwarnungen angezeigt. Bei der Aktualisierung wird empfohlen, die Bereitstellung von at. js 2. x in einer Staging-Umgebung zu testen und die einzelnen und alle in der Konsole angemeldeten Warnmeldungen zu durchlaufen und die veralteten Funktionen in neue Funktionen zu übersetzen, die in at. js 2. x eingeführt wurden.

Sie finden die veralteten Funktionen und das zugehörige Gegenstück unten. Eine vollständige Liste der Funktionen finden Sie unter [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

>[!NOTE]
>at. js 2. x nicht mehr `mboxDefault` automatisch markierte Elemente ausblenden. Kunden müssen daher die Pre-Hide-Logik entweder manuell auf der Site selbst oder über einen Tag-Manager verwalten.

### mboxCreate(mbox,params)

**Beschreibung**:

Führt eine Anfrage aus und wendet das Angebot auf das nächste DIV mit dem `mboxDefault`-Klassennamen an.

**Beispiel**:

```
<div class="mboxDefault">
  default content to replace by offer
</div>
<script>
  mboxCreate('mboxName','param1=value1','param2=value2');
</script>
```

**&quot; at. js 2. x&quot; -Entsprechung**

Eine Alternative zu `mboxCreate(mbox, params)` sind `getOffer()` und `applyOffer()`.

**Beispiel**:

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  var el = document.currentScript.previousElementSibling;
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2"
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: el,
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      el.style.visibility = "visible";
    }
  });
</script> 
```

### „mboxDefine()“ und „mboxUpdate()“

**Beschreibung**:

Erstellt eine interne Zuordnung zwischen einem Element und einem Mbox-Namen, führt die Anforderung jedoch nicht aus. Wird zusammen mit `mboxUpdate()` verwendet, was die Anfrage ausführt und das Angebot auf das in `mboxDefine()` von der nodeId identifizierte Element anwendet. Die Funktion kann auch dazu genutzt werden, eine Mbox zu aktualisieren, die durch `mboxCreate` initiiert wurde. 

**Beispiel**:

```
<div id="someId" class="mboxDefault"></div>
<script>
 mboxDefine('someId','mboxName','param1=value1','param2=value2');
 mboxUpdate('mboxName','param3=value3','param4=value4');
</script>
```

**äquivalent zu. js 2. x**:

Eine Alternative zu `mboxDefine()` und `mboxUpdate` sind `getOffer()` und `applyOffer()`, mit Verwendung der Selektor-Option in `applyOffer()`. Mit diesem Ansatz können Sie das Angebot einem Element mit jedem CSS-Selektor zuordnen, nicht nur mit einem mit einer ID.

**Beispiel**:

```
<div id="someId" class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2",
      param3: "value3",
      param4: "value4" 
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: "#someId",
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      var el = document.getElementById("someId");
      el.style.visibility = "visible";
    }
  });
</script>
```

### adobe.target.registerExtension()

**Beschreibung**:

Stellt eine Standardart zur Registrierung bestimmter Erweiterungen dar.

Dies wird nicht mehr unterstützt und sollte nicht verwendet werden.

## Übersicht über veraltete, neue und unterstützte Funktionen in at.js 2.0

| Methode | Unterstützt? | Neu? | Nicht mehr verwendet?<br>(Standardinhalt wird angezeigt) |
| --- | --- | --- | --- |
| `getOffer()` | Ja |  |  |
| `getOffers()` |  | Ja |  |
| `applyOffer()` | Ja |  |  |
| `applyOffers()` |  | Ja |  |
| `triggerView()` |  | Ja |  |
| `trackEvent()` | Ja |  |  |
| `mboxCreate()` |  |  | Ja |
| `mboxDefine()`<br>`mboxUpdate()` |  |  | Ja |
| `targetGlobalSettings()` | Ja |  |  |
| `Data Providers` | Ja |  |  |
| `targetPageParams()` | Ja |  |  |
| `targetPageParamsAll()` | Ja |  |  |
| `registerExtension()` |  |  | Ja |
| `At.js Custom Events` | Ja |  |  |

## Einschränkungen und Legenden

Beachten Sie die folgenden Einschränkungen und Legenden:

**Konversions-Tracking**

Kunden, die `mboxCreate()` für ihr Konversions-Tracking verwenden, müssen `trackEvent()` oder `getOffer()` benutzen.

**Bereitstellung von Angeboten**

Kunden, die `mboxCreate()` nicht durch `getOffer()` oder `applyOffer()` ersetzen, riskieren möglicherweise, dass Angebote nicht bereitgestellt werden.

**Kann at. js 2. x auf einigen Seiten verwendet werden, während at. js 1 verwendet wird.*x*oder mbox.js auf anderen Seiten verwendet wird?**

Ja, das Besucherprofil wird über verschiedene Seiten mit verschiedenen Versionen und Bibliotheken hinweg erhalten. Das Cookie-Format ist identisch.

**Der Adobe Experience Cloud-Debugger wird in at. js 2. x nicht vollständig unterstützt.**

[!DNL Adobe Experience Cloud Debugger][!UICONROL Funktionen für Registerkarten] und [!UICONTROL Deaktivieren und Konsolen] werden unterstützt, aber Netzwerkanforderungen und mboxtrace werden für at. js 2. x nicht unterstützt.

Dies liegt daran, dass in at. js 2. x eine JSON-Nutzlast anstelle von Schlüssel/Wert-Paaren gesendet wird. Um [!DNL Target]-Anfragen zu untersuchen, filtern Sie die Registerkarte [!UICONTROL Netzwerk] in den Entwicklerwerkzeugen Ihres Browsers nach „Bereitstellung“, „`tt.omtrdc.net`“ oder Ihrem Clientcode. Trace-Daten können weiterhin mithilfe des Abfragezeichenfolge-Parameters und des Autorisierungstokens überprüft werden. Weitere Informationen finden Sie unter [mboxTrace](/help/c-activities/c-troubleshooting-activities/content-trouble.md).

**Neue API in at. js 2. x**

at. js 2. x verwendet eine neue API, die wir die Bereitstellungs-API aufrufen. Um beim Debugging festzustellen, ob at.js den [!DNL Target]-Edge-Server richtig aufruft, können Sie die Registerkarte „Netzwerk“ in den Entwicklerwerkzeugen Ihres Browsers nach „Bereitstellung“, „`tt.omtrdc.net`“ oder Ihrem Clientcode filtern. Sie werden außerdem feststellen, dass [!DNL Target] eine JSON-Nutzlast anstelle von Schlüssel/Wert-Paaren sendet.

**Target Global Mbox wird nicht mehr verwendet**

In at. js 2. x sehen Sie nicht mehr &quot;`target-global-mbox`sichtbar&quot; in den Netzwerkaufrufen. Stattdessen haben wir die „`target-global-mbox`“-Syntax in der JSON-Nutzlast, die an die [!DNL Target]-Server gesendet wird, mit „`execute > pageLoad`“ ersetzt:

```
{
  "id": {
    // ...
  },
  "context": {
    "channel": "web",
    // ...
  },
  "execute": {
    "pageLoad": {}
  }
}
```

Im Grunde wurde das Konzept der globalen Mbox eingeführt, um [!DNL Target] mitzuteilen, ob Angebote und Inhalt beim Laden der Seite abgerufen werden sollten. Daher haben wir dies in unserer neuesten Version deutlicher gemacht.

**Ist der Name der globalen Mbox in at.js nicht mehr wichtig?**

Kunden können einen globalen Mbox-Namen über [!UICONTROL Target &gt; Einrichtung &gt; Implementierung &gt; at.js-Einstellungen bearbeiten] angeben. Diese Einstellung wird von den [!DNL Target]-Edge-Servern verwendet, um „Ausführen &gt; Seite laden“ in den globalen Mbox-Namen zu übersetzen, der in der [!DNL Target]-Benutzeroberfläche angezeigt wird. Dadurch können Kunden mit dem globalen Mbox-Namen weiterhin Server-seitige APIs, den Form-Based Composer und Profilskripts verwenden und Zielgruppen erstellen. Wir empfehlen dringend, dass Sie auch sicherstellen, dass der gleiche globale Mbox-Name auch auf der Seite [!UICONTROL Einrichtung &gt; Voreinstellungen] konfiguriert ist, falls Sie noch Seiten haben, die at.js. 1.*x* oder mbox.js, benutzen, wie in den folgenden Abbildungen dargestellt.

![Dialogfeld „at.js ändern“](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

und

![Benutzerdefinierte globale Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

**Muss die Einstellung Globale Mbox automatisch erstellen für at. js 2. x aktiviert sein?**

In den meisten Fällen ja. Diese Einstellung gibt at. js 2. x an, dass beim Laden der Seite auf [!DNL Target] den Edge-Servern eine Anforderung ausgelöst wird. Da die globale Mbox als „Ausführen &gt; Seite laden“ übersetzt wird, sollte diese Einstellung aktiviert sein, wenn Sie eine Anfrage beim Laden der Seite auslösen möchten.

**Funktionieren vorhandene VEC-Aktivitäten weiterhin, auch wenn der globale Name der globalen Mbox nicht in at. js 2. x angegeben ist?**

Ja, weil „Ausführen &gt; Seite laden“ auf dem [!DNL Target]-Backend wie `target-global-mbox` behandelt wird.

**Wenn meine formularbasierten Aktivitäten auf`target-global-mbox`zielen, funktionieren diese Aktivitäten weiterhin?**

Ja, weil „Ausführen &gt; Seite laden“ auf den [!DNL Target]-Edge-Servern wie `target-global-mbox` behandelt wird.

**Unterstützte und nicht unterstützte at. js 2. x-Einstellungen**

| Einstellung | Unterstützt? |
| --- | --- |
| X-Domäne | Nein |
| Globale Mbox automatisch erstellen | Ja |
| Globaler Mbox-Name | Ja |

**Domänenübergreifendes Tracking wird*nicht*unterstützt**

Domänenübergreifendes Tracking ermöglicht die Anzeige von Sitzungen auf zwei verwandten Sites mit verschiedenen Domänen als einzelne Sitzung. Sie können eine [!DNL Target]-Aktivität erstellen, die sich über `siteA.com` und `siteB.com` erstreckt, während der Besucher im selben Erlebnis verbleibt, wenn er von einer Domäne in die andere wechselt. Diese Funktionalität wird mit dem Verhalten von Target von Drittanbieter- und Erstanbieter-Cookies verknüpft.

In [!DNL Target] wird das Drittanbieter-Cookie in `[CLIENTCODE].tt.omtrdc.net` gespeichert, während das Erstanbieter-Cookie in `clientdomain.com` gespeichert wird. Die erste Anfrage gibt HTTP-Antwort-Header zurück, die versuchen, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet. Wenn der Browser Drittanbieter-Cookies akzeptiert, enthält die Weiterleitungsanfrage diese Cookies und das Angebot wird zurückgegeben. Dieser Arbeitsablauf ist möglich, da wir die HTTP GET-Methode verwenden.

In at. js 2. x wird HTTP GET jedoch nicht mehr verwendet und stattdessen wird HTTP POST verwendet. HTTP POST wird jetzt über at.js verwendet, um JSON-Nutzlasten an die [!DNL Target]-Edge-Server zu senden. Das bedeutet, dass die Weiterleitungsanfrage zur Überprüfung, ob ein Browser Drittanbieter-Cookies unterstützt, jetzt nicht mehr funktioniert. Dies liegt daran, dass HTTP GET-Anfragen idempotent sind, während HTTP POST nicht idempotent ist und nicht willkürlich wiederholt werden darf. Daher wird die domänenübergreifende Verfolgung in at. js 2. x nicht mehr unterstützt.

**Automatische Erstellung einer globalen Mbox wird unterstützt**

Diese Einstellung weist at. js 2. x an, eine Anforderung an die [!DNL Target] Edge-Server beim Laden der Seite auszulösen. Da die globale Mbox als „Ausführen &gt; Seite laden“ übersetzt wird und dies von den [!DNL Target]-Edge-Servern interpretiert wird, sollten Kunden dies aktivieren, wenn sie eine Anfrage beim Laden der Seite auslösen möchten.

**Globaler Mbox-Name wird unterstützt**

Kunden können einen globalen Mbox-Namen über [!UICONTROL Target &gt; Einrichtung &gt; Implementierung &gt; at.js-Einstellungen bearbeiten] angeben. Diese Einstellung wird von den [!DNL Target]-Edge-Servern verwendet, um „Ausführen &gt; Seite laden“ in den eingegebenen globalen Mbox-Namen zu übersetzen. Dadurch können Kunden weiterhin Server-seitige APIs, den Form-Based Composer und Profilskripts verwenden und Zielgruppen erstellen, die auf die globale Mbox zielen.

**Gelten die folgenden benutzerdefinierten at.js-Ereignisse für`triggerView()`oder gilt dies nur für`applyOffer()`oder`applyOffers()`?**

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

Ja, die benutzerdefinierten at.js-Ereignisse gelten auch für `triggerView()`.

**Wenn ich`triggerView()`über`{“page” : “true”}`aufrufe, heißt es, dass es eine Benachrichtigung an das[!DNL Target]-Backend sendet und die Impression erhöht wird. Führt dies auch dazu, dass die Profilskripts ausgeführt werden?**

Wenn ein Prefetch-Aufruf an das [!DNL Target]-Backend erfolgt, werden die Profilskripts ausgeführt. Anschließend werden die betroffenen Profildaten verschlüsselt und an die Client-Seite zurückgegeben. Nachdem `triggerView()` mit `{"page": "true"}` aufgerufen wurde, wird eine Benachrichtigung zusammen mit den verschlüsselten Profildaten gesendet. Dann entschlüsselt das [!DNL Target]-Backend die Profildaten und speichert sie in den Datenbanken.

**Müssen wir vor dem Aufrufen von`triggerView()`Pre-hiding-Code hinzufügen, um Flackern zu verhindern?**

Nein, Sie müssen vor dem Aufrufen von `triggerView()` keinen Pre-hiding-Code hinzufügen. at. js 2. x verwaltet die Vor- und Flackerlogik, bevor die Ansicht angezeigt und angewendet wird.

## Kompatibilität von at.js

Die folgenden Tabellen erläutern die at.js. 2.0.0-Kompatibilität mit verschiedenen Aktivitätstypen, Integrationen, Funktionen und Funktionen von at.js.

### Aktivitätstypen {#types}

| Typ | Unterstützt? |
| --- | --- |
| A/B-Test | Ja |
| Automatische Zuordnung | Ja |
| Automatisches Targeting | Ja |
| Erlebnis-Targeting | Ja |
| Multivarianz-Test | Ja |
| Automatisierte Personalisierung | Ja |
| Recommendations  | Ja |

>[!NOTE]
>
>Aktivitäten mit automatischem Targeting werden über at. js 2. x und VEC unterstützt, wenn alle Änderungen auf `Page Load Event`die Datei angewendet werden. Wenn Änderungen an bestimmten Ansichten hinzugefügt werden, werden nur die Aktivitäten A/B-Test, Automatisierte Zuordnung und Erlebnis-Targeting (XT) unterstützt.

### Integrationen {#integrations}

| Typ | Unterstützt? |
| --- | --- |
| Analytics for Target (A4T) | Ja |
| Zielgruppen | Ja |
| Kundenattribute | Ja |
| AEM-Erlebnisfragmente | Ja |
| Adobe Launch-Erweiterung | [Ja](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) |
| Debugger | Ja |
| Auditor | Regeln wurden für at. js 2. x noch nicht aktualisiert. |
| Dynamischer Tag-Manager (DTM) | Ja |
| Opt-in | Nein. Die Unterstützung für die Teilnahme an [GDPR](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) wird in [at. js Version 2.1.0 unterstützt](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| AEM Enhanced Personalization mit Adobe Target | Nein |

### Funktionen

| Funktion | Unterstützt? |
| --- | --- |
| X-Domäne | Nein |
| Eigenschaften/Workspaces | Ja |
| QA-Links | Ja |
| Form-Based Experience Composer | Ja |
| Visual Experience Composer (VEC) | Ja |
| Benutzerspezifischer Code | Ja |
| Antwort-Token | [Ja](#response-tokens) |
| Klick-Tracking | Ja |
| Bereitstellung mehrerer Aktivitäten | Ja |
| targetGlobalSettings | Ja (jedoch nicht X-Domäne) |
| at.js-Methoden | Alles außer<br>`mboxCreate()`<br>`mboxUpdate()`<br>`mboxDefine()`<br>, was Standardinhalte anzeigt, wird unterstützt. |

### Abfragezeichenfolge-Parameter

| Parameter | Unterstützt? |
| --- | --- |
| `?mboxDisable` | Ja |
| `?mboxDisable` | Ja |
| `?mboxTrace` | Ja |
| `?mboxSession` | Nein |
| `?mboxOverride.browserIp` | Nein |

## Antwort-Token {#response-tokens}

at.js 2.*x*, genau wie at. js 1.*x*verwendet das benutzerdefinierte Ereignis `at-request-succeeded` zu den Antworttoken. Codebeispiele, die das `at-request-succeeded` benutzerdefinierte Ereignis verwenden, finden Sie unter [Antwort-Token](/help/administrating-target/response-tokens.md).

## Parameter &quot;at. js 1. x&quot; zu&quot; at. js 2. x payload-Zuordnung « {#payload-mapping}

In diesem Abschnitt werden die Zuordnungen zwischen &quot;at. js 1&quot; erläutert.*x* und at. js 2. x.

Vor der Trennung der Parameterzuordnung haben sich die Endpunkte, die diese Bibliotheksversionen verwenden, geändert:

* at.js 1.*x* - `http://<client code>.tt.omtrdc.net/m2/<client code>/mbox/json`
* at. js 2. x - `http://<client code>.tt.omtrdc.net/rest/v1/delivery`

Ein weiterer wichtiger Unterschied besteht darin, dass:

* at.js 1.*x* - Client-Code ist Teil des Pfads
* at. js 2. x - Client-Code wird als Abfragezeichenfolgenparameter gesendet, z. B.:
   `http://<client code>.tt.omtrdc.net/rest/v1/delivery?client=democlient`

Die folgenden Abschnitte führen zu jeder at. js 1-Liste.*x* -Parameter, dessen Beschreibung und die entsprechende 2.0.0 JSON-Nutzlast (falls zutreffend):

### at_ property

(at.js 1.*x* -Parameter)

Wird für [Enterprise-Benutzerberechtigungen verwendet](/help/administrating-target/c-user-management/property-channel/property-channel.md).

```
{
  ....
  "property": {
    "token": "1213213123122313121"
  }
  ....
}
```

### browserHeight

(at.js 1.*x* -Parameter)

Die Höhe des Browserfensters des Besuchers.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "window": {
       "height": 200
    }
  }
}
```

### browserWidth

(at.js 1.*x* -Parameter)

Die Breite des Browserfensters des Besuchers.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "window": {
       "width": 200
    }
  }
}
```

### Browsertimeoffset

(at.js 1.*x* -Parameter)

Der Zeitzonenoffset.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "timeOffsetInMinutes": -480
  }
}
```

### Screenheight

(at.js 1.*x* -Parameter)

Die Höhe des Besucherbildschirms.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "screen": {
       "height": 200
    }
  }
}
```

### Screenwidth

(at.js 1.*x* -Parameter)

Die Breite des Besucherbildschirms.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "screen": {
       "width": 200
    }
  }
}
```

### colorDepth

(at.js 1.*x* -Parameter)

Die Farbtiefe des Besucherbildschirms.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "screen": {
       "colorDepth": 24
    }
  }
}
```

### mboxHost

(at.js 1.*x* -Parameter)

Die Domäne der Seite, auf der die Target-Bibliothek ausgeführt wird.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "browser": {
       "host": "test.com"
    }
  }
}
```

### webGLRenderer

(at.js 1.*x* -Parameter)

Die WEB-GL-Renderer-Funktionen des Browsers. Dies wird von unserem Geräteerkennungsmechanismus verwendet, um festzustellen, ob das Gerät des Besuchers ein Desktop, iphone, Android-Gerät usw. ist.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "browser": {
       "webGLRenderer": "AMD Radeon Pro 560X OpenGL Engine"
    }
  }
}
```

### Mboxurl

(at.js 1.*x* -Parameter)

Die Seiten-URL.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "address": {
       "url": "http://test.com"
    }
  }
}
```

### Mboxreferrer

(at.js 1.*x* -Parameter)

Der Seitenverweis.

at. js 2. x JSON Nutzlast:

```
{
  "context": {
    "address": {
       "referringUrl": "http://google.com"
    }
  }
}
```

### mbox (Name) entspricht der globalen Mbox

(at.js 1.*x* -Parameter)

Die Bereitstellungs-API hat kein globales Mbox-Konzept mehr. In der JSON-Nutzlast müssen `execute > pageLoad`Sie verwenden.

at. js 2. x JSON Nutzlast:

```
{
  "execute": {
    "pageLoad": {
       "parameters": ....
       "profileParameters": ...
       .....
    }
  }
}
```

### mbox (name) entspricht *nicht* der globalen Mbox

(at.js 1.*x* -Parameter)

Um einen mbox-Namen zu verwenden, übergeben Sie ihn an `execute > mboxes`. Eine mbox erfordert einen Index und einen Namen.

at. js 2. x JSON Nutzlast:

```
{
  "execute": {
    "mboxes": [{
       "index": 0,
       "name": "some-mbox",
       "parameters": ....
       "profileParameters": ...
       .....
    }]
  }
}
```

### Mboxid

(at.js 1.*x* -Parameter)

Wird nicht mehr länger verwendet.

### Mboxcount

(at.js 1.*x* -Parameter)

Wird nicht mehr länger verwendet.

### Mboxrid

(at.js 1.*x* -Parameter)

Von Downstream-Systemen verwendete Anforderungs-ID zur Hilfe beim Debugging.

at. js 2. x JSON Nutzlast:

```
{
  "requestId": "2412234442342"
  ....
}
```

### Mboxtime

(at.js 1.*x* -Parameter)

Wird nicht mehr länger verwendet.

### mboxSession

(at.js 1.*x* -Parameter)

Sitzungs-ID wird als Abfragezeichenfolgenparameter (`sessionId`) zum Bereitstellungs-API-Endpunkt gesendet.

### „mboxPC“

(at.js 1.*x* -Parameter)

Die TNT-ID wird an `id > tntId`.

at. js 2. x JSON Nutzlast:

```
{
  "id": {
    "tntId": "ca5ddd7e33504c58b70d45d0368bcc70.21_3"
  }
  ....
}
```

### mboxMCGVID

(at.js 1.*x* -Parameter)

Marketing Cloud-Besucher-ID wird an `id > marketingCloudVisitorId`.

at. js 2. x JSON Nutzlast:

```
{
  "id": {
    "marketingCloudVisitorId": "797110122341429343505"
  }
  ....
}
```

### vst. aaaa. id und vst. aaaa. authstate

(at.js 1.*x* -Parameter)

Kunden-IDs sollten weitergegeben `id > customerIds`werden.

at. js 2. x JSON Nutzlast:

```
{
  "id": {
    "customerIds": [{
       "id": "1232131",
       "integrationCode": "aaaa",
       "authenticatedState": "....."
     }]
  }
  ....
}
```

### mbox3rdPartyId

(at.js 1.*x* -Parameter)

Drittanbieter-ID für die Verknüpfung verschiedener Target-IDs.

at. js 2. x JSON Nutzlast:

```
{
  "id": {
    "thirdPartyId": "1232312323123"
  }
  ....
}
```

### Mboxmcsdid

(at.js 1.*x* -Parameter)

SDID, auch als zusätzliche Daten-ID bekannt. Sollte weitergegeben `experienceCloud > analytics > supplementalDataId`werden.

at. js 2. x JSON Nutzlast:

```
{
  "experienceCloud": {
    "analytics": {
      "supplementalDataId": "1212321132123131"
    }
  }
  ....
}
```

### vst. trk

(at.js 1.*x* -Parameter)

Analytics-Tracking-Server. Sollte weitergegeben `experienceCloud > analytics > trackingServer`werden.

at. js 2. x JSON Nutzlast:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServer": "analytics.test.com"
    }
  }
  ....
}
```

### vst. trks

(at.js 1.*x* -Parameter)

Sicherer Analytics-Trackingserver. Sollte weitergegeben `experienceCloud > analytics > trackingServerSecure`werden.

at. js 2. x JSON Nutzlast:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServerSecure": "secure-analytics.test.com"
    }
  }
  ....
}
```

### mboxMCGLH

(at.js 1.*x* -Parameter)

Audience Manager-Standorthinweis. Sollte weitergegeben `experienceCloud > audienceManager > locationHint`werden.

at. js 2. x JSON Nutzlast:

```
{
  "experienceCloud": {
    "audienceManager": {
      "locationHint": 9
    }
  }
  ....
}
```

### mboxAAMB

(at.js 1.*x* -Parameter)

Audience Manager-Blob. Sollte weitergegeben `experienceCloud > audienceManager > blob`werden.

at. js 2. x JSON Nutzlast:

```
{
  "experienceCloud": {
    "audienceManager": {
      "blob": "2142342343242342"
    }
  }
  ....
}
```

### Mboxversion

(at.js 1.*x* -Parameter)

Version wird als Abfragezeichenfolgenparameter über den Versionsparameter gesendet.

## Schulungsvideo: &quot; at. js 2. x&quot; -Architekturdiagramm

at. js 2. x verbessert die Unterstützung von Adobe Target für spas und ist in andere Experience Cloud-Lösungen integriert. In diesem Video wird erklärt, wie alles zusammenkommt.

>[!VIDEO](https://video.tv.adobe.com/v/26250?captions=ger)

See [Understanding how at.js 2.x works](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) for more information.