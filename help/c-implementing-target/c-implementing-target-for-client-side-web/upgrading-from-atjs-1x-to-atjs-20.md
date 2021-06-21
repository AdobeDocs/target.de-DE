---
keywords: at.js-Versionen;at.js-Releases;Einzelseiten-App;spa;domänenübergreifend;Domänen übergreifend
description: Erfahren Sie, wie Sie von Adobe [!DNL Target] at.js 1.x auf at.js 2.x aktualisieren. Untersuchen Sie Systemflussdiagramme, lernen Sie neue und veraltete Funktionen kennen und vieles mehr.
title: Wie aktualisiere ich von at.js Version 1.x auf Version 2.x?
feature: 'at.js  '
role: Developer
exl-id: f5ec6bf1-f38c-4681-a6c1-b862272ee55d
source-git-commit: a4e2d388266e318276ca38417b7d3f3c210e9ed3
workflow-type: tm+mt
source-wordcount: '2765'
ht-degree: 92%

---

# Aktualisieren von at.js 1.*x* auf at.js 2.*x*

Die neueste Version von at.js [!DNL Adobe Target] bietet umfassende Funktionen, mit denen Ihr Unternehmen mithilfe von Client-seitigen Technologien der neuesten Generation Personalisierungen ausführen kann. Diese neue Version konzentriert sich auf die Aktualisierung von at.js, um harmonische Interaktionen mit Einzelseitenanwendungen (SPAs) zu ermöglichen.

Hier einige Vorteile der Verwendung von at.js 2.*x*, die in früheren Versionen nicht verfügbar sind:

* Möglichkeit zur Zwischenspeicherung aller Angebote beim Seitenladen, um mehrere Server-Aufrufe auf einen einzelnen Server-Aufruf zu reduzieren
* Drastische Verbesserung der Erlebnisse Ihrer Endbenutzer auf Ihrer Site, da Angebote sofort über den Cache angezeigt werden, ohne dass die herkömmlichen Serveraufrufe verzögert werden.
* Einfache Einrichtung mit einmaliger, einzeiliger Codeeingabe und Entwicklerunterstützung, sodass Ihre Marketer A/B- und XT-Aktivitäten über VEC in Ihren SPAs erstellen und ausführen können

## at.js 2.*x*  - Systemdiagramme

Die folgenden Diagramme helfen Ihnen, den Arbeitsablauf von at.js 2.*x* mit View zu verstehen und wie dieser die SPA-Integration verbessert. Eine bessere Einführung in die in at.js 2.*x* verwendeten Konzepte finden Sie unter [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Ablauf mit at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

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

![Target-Ablauf at.js 2 *x* triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Aufruf | Details |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 1 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den [!DNL Target]-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

## Bereitstellen von at.js 2 *x* {#deploy-atjs-200}

1. Bereitstellen von at.js 2 *x* über die [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)-Erweiterung.

   >[!NOTE]
   >
   > Die Bereitstellung von at. js mit Adobe Launch ist die bevorzugte Methode.

   Oder

   Laden Sie at.js 2.*x* manuell über die Target-Benutzeroberfläche herunter und implementieren Sie die Version mithilfe der [Methode Ihrer Wahl](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

## Nicht mehr unterstützte Funktionen von at.js

Es gibt mehrere Funktionen, die in at.js 2.*x* nicht mehr unterstützt werden.

>[!IMPORTANT]
>
>Sind diese veralteten Funktionen weiterhin auf Ihrer Site, wenn Sie at.js 2.*x* implementieren, werden in der Konsole Warnungen angezeigt. Die empfohlene Vorgehensweise bei der Aktualisierung besteht darin, die Implementierung von at.js 2.*x* in einer Staging-Umgebung zu testen und alle in der Konsole protokollierten Warnungen sorgfältig zu prüfen und die veralteten Funktionen auf die neuen Funktionen von at.js 2.*x* zu übertragen.

Sie finden die veralteten Funktionen und das zugehörige Gegenstück unten. Eine vollständige Liste der Funktionen finden Sie unter [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

>[!NOTE]
>at.js 2.*x*  blendet mit `mboxDefault` markierte Elemente nicht mehr automatisch aus. Kunden müssen daher die Pre-Hide-Logik entweder manuell auf der Site selbst oder über einen Tag-Manager verwalten.

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

**at.js 2.*x*-Äquivalent**

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

**at.js 2.*x*-Äquivalent**:

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

## Übersicht über veraltete, neue und unterstützte Funktionen in at.js 2.*x* 

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

### Konversions-Tracking

Kunden, die `mboxCreate()` für ihr Konversions-Tracking verwenden, müssen `trackEvent()` oder `getOffer()` benutzen.

### Bereitstellung von Angeboten

Kunden, die `mboxCreate()` nicht durch `getOffer()` oder `applyOffer()` ersetzen, riskieren möglicherweise, dass Angebote nicht bereitgestellt werden.

### Kann at.js 2.*x* auf manchen Seiten verwendet werden, während at.js 1.*x* oder mbox.js auf anderen Seiten verwendet wird?

Ja, das Besucherprofil wird über verschiedene Seiten mit verschiedenen Versionen und Bibliotheken hinweg erhalten. Das Cookie-Format ist identisch.

### Neue API-Nutzung in at.js 2.*x*

at.js 2.*x*  verwendet eine neue API, die wir die Bereitstellungs-API nennen. Um beim Debugging festzustellen, ob at.js den [!DNL Target]-Edge-Server richtig aufruft, können Sie die Registerkarte „Netzwerk“ in den Entwicklerwerkzeugen Ihres Browsers nach „Bereitstellung“, „`tt.omtrdc.net`“ oder Ihrem Clientcode filtern. Sie werden außerdem feststellen, dass [!DNL Target] eine JSON-Nutzlast anstelle von Schlüssel/Wert-Paaren sendet.

### Target Global Mbox wird nicht mehr verwendet

In at.js 2.*x* sehen Sie „`target-global-mbox`“ nicht mehr in den Netzwerkaufrufen. Stattdessen haben wir die „`target-global-mbox`“-Syntax in der JSON-Nutzlast, die an die [!DNL Target]-Server gesendet wird, mit „`execute > pageLoad`“ ersetzt:

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

### Ist der Name der globalen Mbox in at.js nicht mehr wichtig?

Kunden können einen globalen Mbox-Namen über [!UICONTROL Target > Administration > Implementierung > at.js-Einstellungen bearbeiten] angeben. Diese Einstellung wird von den [!DNL Target]-Edge-Servern verwendet, um „Ausführen > Seite laden“ in den globalen Mbox-Namen zu übersetzen, der in der [!DNL Target]-Benutzeroberfläche angezeigt wird. Dadurch können Kunden mit dem globalen Mbox-Namen weiterhin Server-seitige APIs, den Form-Based Composer und Profilskripts verwenden und Zielgruppen erstellen. Wir empfehlen dringend, dass Sie auch sicherstellen, dass derselbe globale Mbox-Name auch auf der Seite [!UICONTROL Administration > Visual Experience Composer] konfiguriert ist, falls Sie noch Seiten mit at.js 1 haben.*x* oder mbox.js, benutzen, wie in den folgenden Abbildungen dargestellt.

![Dialogfeld „at.js ändern“](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

und

![Benutzerdefinierte globale Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

### Muss die Einstellung „Globale Mbox automatisch erstellen“ für at.js 2.*x* aktiviert sein?

In den meisten Fällen ja. Diese Einstellung teilt at.js 2.*x* mit, dass beim Laden der Seite eine Anfrage an die [!DNL Target]-Edge-Server gesendet wird. Da die globale Mbox als „Ausführen > Seite laden“ übersetzt wird, sollte diese Einstellung aktiviert sein, wenn Sie eine Anfrage beim Laden der Seite auslösen möchten.

### Funktionieren vorhandene VEC-Aktivitäten weiterhin, auch wenn der Zielname der globalen Mbox nicht in at.js 2.*x* angegeben ist?

Ja, weil „Ausführen > Seite laden“ auf dem [!DNL Target]-Backend wie `target-global-mbox` behandelt wird.

### Wenn meine formularbasierten Aktivitäten auf `target-global-mbox` zielen, funktionieren diese Aktivitäten weiterhin?

Ja, weil „Ausführen > Seite laden“ auf den [!DNL Target]-Edge-Servern wie `target-global-mbox` behandelt wird.

### Unterstützte und nicht unterstützte at.js 2.*x*-Einstellungen

| Einstellung | Unterstützt? |
| --- | --- |
| X-Domäne | Nein |
| Globale Mbox automatisch erstellen | Ja |
| Globaler Mbox-Name | Ja |

### Unterstützung von domänenübergreifendem Tracking in at.js 2.x {#cross-domain}

Durch domänenübergreifendes Tracking können Besucher auf verschiedenen Domänen verbunden werden. Da für jede Domäne ein neues Cookie erstellt werden muss, ist es schwierig, Besucher zu tracken, wenn sie beim Navigation von einer Domäne zu einer anderen wechseln. Um domänenübergreifendes Tracking zu ermöglichen, verwendet [!DNL Target] ein Drittanbieter-Cookie, um Besucher über verschiedene Domänen hinweg zu verfolgen. Damit können Sie eine Target-Aktivität erstellen, die sich über `siteA.com` und `siteB.com` erstreckt, während Besuchern dasselbe Erlebnis angezeigt wird, auch wenn sie die Domäne wechseln. Diese Funktionalität wird mit dem Verhalten von Target von Drittanbieter- und Erstanbieter-Cookies verknüpft.

>[!NOTE]
>
>Das domänenübergreifende Tracking wird in at.js 2 nicht nativ unterstützt.*x*. Das domänenübergreifende Tracking wird in at.js 2.*x* über die Experience Cloud ID (ECID)-Bibliothek v 4.3.0+ unterstützt.

In Target wird das Drittanbieter-Cookie in `<CLIENTCODE>.tt.omtrdc.net` gespeichert. Das Erstanbieter-Cookie wird in `clientdomain.com` gespeichert. Die erste Anfrage gibt HTTP-Antwort-Header zurück, die versuchen, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet. Wenn der Browser Drittanbieter-Cookies akzeptiert, enthält die Weiterleitungsanfrage diese Cookies und das Erlebnis wird zurückgegeben. Dieser Arbeitsablauf ist möglich, da wir die HTTP GET-Methode verwenden.

In at.js 2.*x* wird HTTP GET jedoch nicht mehr verwendet, stattdessen wird HTTP POST verwendet. HTTP POST wird jetzt über at.js 2.*x* verwendet, um JSON-Payloads an Target Edge-Server zu senden. Das bedeutet, dass die Weiterleitungsanfrage zur Überprüfung, ob ein Browser Drittanbieter-Cookies unterstützt, jetzt nicht mehr funktioniert. Dies liegt daran, dass HTTP GET-Anfragen idempotent sind, während HTTP POST nicht idempotent ist und nicht willkürlich wiederholt werden darf. Daher wird domänenübergreifendes Tracking in at.js 2.*x* nicht mehr nativ unterstützt. Nur at.js 1.*x* verfügt über native Unterstützung für domänenübergreifendes Tracking.

Wenn Sie domänenübergreifendes Tracking verwenden möchten, müssen Sie die [ECID-Bibliothek v4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html?lang=de) in Verbindung mit at.js 2 installieren.*x*. Die ECID-Bibliothek hat den Zweck, persistente IDs zu verwalten, die zur domänenübergreifenden Identifizierung eines Besuchers verwendet werden können.

>[!NOTE]
>
>Nach der Installation der ECID-Bibliothek v 4.3.0 + und at.js 2.*x* können Sie Aktivitäten erstellen, die mehrere Domänen umfassen und Benutzer tracken können. Beachten Sie, dass diese Funktion erst nach Ablauf der Sitzung funktioniert.

### Automatische Erstellung einer globalen Mbox wird unterstützt

Diese Einstellung veranlasst at.js 2.*x* beim Laden der Seite eine Anfrage an die [!DNL Target]-Edge-Server zu senden. Da die globale Mbox als „Ausführen > Seite laden“ übersetzt wird und dies von den [!DNL Target]-Edge-Servern interpretiert wird, sollten Kunden dies aktivieren, wenn sie eine Anfrage beim Laden der Seite auslösen möchten.

### Globaler Mbox-Name wird unterstützt

Kunden können einen globalen Mbox-Namen über [!UICONTROL Target > Administration > Implementierung > Bearbeiten] angeben. Diese Einstellung wird von den [!DNL Target]-Edge-Servern verwendet, um „Ausführen > Seite laden“ in den eingegebenen globalen Mbox-Namen zu übersetzen. Dadurch können Kunden weiterhin Server-seitige APIs, den formularbasierten Composer und Profilskripts verwenden und Zielgruppen erstellen, die auf die globale Mbox zielen.

### Gelten die folgenden benutzerdefinierten at.js-Ereignisse für `triggerView()` oder gilt dies nur für `applyOffer()` oder `applyOffers()`?

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

Ja, die benutzerdefinierten at.js-Ereignisse gelten auch für `triggerView()`.

### Wenn ich `triggerView()` mit &amp;lbrace;`“page” : “true”`&amp;rbrace aufrufe, wird eine Benachrichtigung an das [!DNL Target]-Backend gesendet und die Impression erhöht. Führt dies auch dazu, dass die Profilskripts ausgeführt werden?

Wenn ein Prefetch-Aufruf an das [!DNL Target]-Backend erfolgt, werden die Profilskripts ausgeführt. Anschließend werden die betroffenen Profildaten verschlüsselt und an die Client-Seite zurückgegeben. Nachdem `triggerView()` mit `{"page": "true"}` aufgerufen wurde, wird eine Benachrichtigung zusammen mit den verschlüsselten Profildaten gesendet. Dann entschlüsselt das [!DNL Target]-Backend die Profildaten und speichert sie in den Datenbanken.

### Müssen wir vor dem Aufrufen von `triggerView()` Pre-hiding-Code hinzufügen, um Flackern zu verhindern?

Nein, Sie müssen vor dem Aufrufen von `triggerView()` keinen Pre-hiding-Code hinzufügen. at.js 2.*x*  verwaltet die Pre-Hiding- und Flacker-Logik, bevor die Ansicht angezeigt und angewendet wird.

### Welches at.js 1.** xparameter zum Erstellen von Zielgruppen werden in at.js 2 nicht unterstützt.*x*? {#audience-parameters}

Die folgenden at.js 1.x-Parameter sind *NOT*, die derzeit für die Erstellung von Zielgruppen bei der Verwendung von at.js 2 unterstützt werden.*x*:

* browserHeight
* browserWidth
* browserTimeOffset
* screenHeight
* screenWidth
* screenOrientation
* colorDepth
* devicePixelRatio

## Kompatibilität von at.js

Die folgenden Tabellen erläutern die at.js. 2.*x* Kompatibilität mit verschiedenen Aktivitätstypen, Integrationen, Funktionen und at.js-Funktionen.

### Aktivitätstypen {#types}

| Typ | Unterstützt? |
| --- | --- |
| A/B-Test | Ja |
| Automatische Zuordnung | Ja |
| Automatisches Targeting | Ja |
| Erlebnis-Targeting | Ja |
| Multivarianz-Test | Ja |
| Automatisierte Personalisierung | Ja |
| Recommendations | Ja |

>[!NOTE]
>
>Aktivitäten mit automatischem Targeting werden über at.js 2.*x* und VEC unterstützt, wenn alle Änderungen auf die `Page Load Event`-Datei angewendet werden. Wenn Änderungen an bestimmten Ansichten hinzugefügt werden, werden nur die Aktivitäten A/B-Test, Automatisierte Zuordnung und Erlebnis-Targeting (XT) unterstützt.

### Integrationen {#integrations}

| Typ | Unterstützt? |
| --- | --- |
| Analytics for Target (A4T) | Ja |
| Zielgruppen | Ja |
| Kundenattribute | Ja |
| AEM-Experience Fragments | Ja |
| Adobe Launch-Erweiterung | [Ja](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) |
| Debugger | Ja |
| Auditor | Regeln wurden für at.js 2.*x* noch nicht aktualisiert. |
| Opt-in | Nein. Die Unterstützung für die Teilnahme an [DSGVO](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) wird in [at. js Version 2.1.0 unterstützt](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
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
| `?mboxOverride.browserIp` | Ja |

## Antwort-Token {#response-tokens}

at.js 2.*x* verwendet genau wie at.js 1.*x* das benutzerdefinierte Ereignis `at-request-succeeded` zu den Antworttoken. Codebeispiele, die das `at-request-succeeded` benutzerdefinierte Ereignis verwenden, finden Sie unter [Antwort-Token](/help/administrating-target/response-tokens.md).

## at.js 1.*x*  Parameter auf at.js 2.*x* Payload-Mapping {#payload-mapping}

In diesem Abschnitt werden die Zuordnungen zwischen at.js 1.*x* und at.js 2.*x*.

Beachten Sie vor dem Befassen mit der Parameterzuordnung, dass sich die Endpunkte, die diese Bibliotheksversionen verwenden, geändert haben:

* at.js 1.*x* - `http://<client code>.tt.omtrdc.net/m2/<client code>/mbox/json`
* at.js 2.*x*  - `http://<client code>.tt.omtrdc.net/rest/v1/delivery`

Ein weiterer wichtiger Unterschied besteht darin, dass:

* at.js 1.*x* - Client-Code ist Teil des Pfads
* at.js 2.*x*  - Client-Code wird als Abfragezeichenfolgenparameter gesendet, z. B.:
   `http://<client code>.tt.omtrdc.net/rest/v1/delivery?client=democlient`

Die folgenden Abschnitte listen jeden at.js 1.** xparameter, seine Beschreibung und die entsprechenden 2.** xJSON-Nutzlast (falls zutreffend):

### at_property

(at.js 1.*x*-Parameter)

Wird für [Unternehmens-Benutzerberechtigungen verwendet](/help/administrating-target/c-user-management/property-channel/property-channel.md).

```
{
  ....
  "property": {
    "token": "1213213123122313121"
  }
  ....
}
```

### mboxHost

(at.js 1.*x*-Parameter)

Die Domäne der Seite, auf der die Target-Bibliothek ausgeführt wird.

at.js 2.*x*  JSON-Payload:

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

(at.js 1.*x*-Parameter)

Die WEB-GL-Renderer-Funktionen des Browsers. Dies wird von unserem Geräteerkennungsmechanismus verwendet, um festzustellen, ob das Gerät des Besuchers ein Desktop, iPhone, Android-Gerät usw. ist.

at.js 2.*x*  JSON-Payload:

```
{
  "context": {
    "browser": {
       "webGLRenderer": "AMD Radeon Pro 560X OpenGL Engine"
    }
  }
}
```

### mboxURL

(at.js 1.*x*-Parameter)

Die Seiten-URL.

at.js 2.*x*  JSON-Payload:

```
{
  "context": {
    "address": {
       "url": "http://test.com"
    }
  }
}
```

### mboxReferrer

(at.js 1.*x*-Parameter)

Der Seitenverweis.

at.js 2.*x*  JSON-Payload:

```
{
  "context": {
    "address": {
       "referringUrl": "http://google.com"
    }
  }
}
```

### mbox (der Name) entspricht der globalen Mbox

(at.js 1.*x*-Parameter)

Die Bereitstellungs-API hat kein globales Mbox-Konzept mehr. In der JSON-Nutzlast müssen Sie `execute > pageLoad` verwenden.

at.js 2.*x*  JSON-Payload:

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

### mbox (der Name) entspricht *nicht* der globalen Mbox

(at.js 1.*x*-Parameter)

Um einen Mbox-Namen zu verwenden, übergeben Sie ihn an `execute > mboxes`. Eine Mbox erfordert einen Index und einen Namen.

at.js 2.*x*  JSON-Payload:

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

### mboxId

(at.js 1.*x*-Parameter)

Wird nicht mehr länger verwendet.

### mboxCount

(at.js 1.*x*-Parameter)

Wird nicht mehr länger verwendet.

### mboxRid

(at.js 1.*x*-Parameter)

Von Downstream-Systemen verwendete Anforderungs-ID zur Hilfe beim Debugging.

at.js 2.*x*  JSON-Payload:

```
{
  "requestId": "2412234442342"
  ....
}
```

### mboxTime

(at.js 1.*x*-Parameter)

Wird nicht mehr länger verwendet.

### mboxSession

(at.js 1.*x*-Parameter)

Sitzungs-ID wird als Abfragezeichenfolgenparameter (`sessionId`) zum Bereitstellungs-API-Endpunkt gesendet.

### mboxPC

(at.js 1.*x*-Parameter)

Die TNT-ID wird an `id > tntId` übergeben.

at.js 2.*x*  JSON-Payload:

```
{
  "id": {
    "tntId": "ca5ddd7e33504c58b70d45d0368bcc70.21_3"
  }
  ....
}
```

### mboxMCGVID

(at.js 1.*x*-Parameter)

Experience Cloud-Besucher-ID wird an `id > marketingCloudVisitorId` übergeben.

at.js 2.*x*  JSON-Payload:

```
{
  "id": {
    "marketingCloudVisitorId": "797110122341429343505"
  }
  ....
}
```

### `vst.aaaa.id` und `vst.aaaa.authState`

(at.js 1.*x* -Parameter)

Kunden-IDs sollten an `id > customerIds` übergeben werden.

at.js 2.*x*  JSON-Payload:

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

(at.js 1.*x*-Parameter)

Kunden-Drittanbieter-ID, die für die Verknüpfung verschiedener Target-IDs verwendet wird.

at.js 2.*x*  JSON-Payload:

```
{
  "id": {
    "thirdPartyId": "1232312323123"
  }
  ....
}
```

### mboxMCSDID

(at.js 1.*x*-Parameter)

SDID, auch als zusätzliche Daten-ID bekannt. Sollte an `experienceCloud > analytics > supplementalDataId` übergeben werden.

at.js 2.*x*  JSON-Payload:

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

### vst.trk

(at.js 1.*x*-Parameter)

Analytics-Tracking-Server. Sollte an `experienceCloud > analytics > trackingServer` übergeben werden.

at.js 2.*x*  JSON-Payload:

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

### vst.trks

(at.js 1.*x*-Parameter)

Sicherer Analytics-Tracking-Server. Sollte an `experienceCloud > analytics > trackingServerSecure` übergeben werden.

at.js 2.*x*  JSON-Payload:

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

(at.js 1.*x*-Parameter)

Audience Manager-Standorthinweis. Sollte an `experienceCloud > audienceManager > locationHint` übergeben werden.

at.js 2.*x*  JSON-Payload:

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

(at.js 1.*x*-Parameter)

Audience Manager-Blob. Sollte an `experienceCloud > audienceManager > blob` übergeben werden.

at.js 2.*x*  JSON-Payload:

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

### mboxVersion

(at.js 1.*x*-Parameter)

Version wird als Abfragezeichenfolgenparameter über den Versionsparameter gesendet.

## Schulungsvideo: at.js 2.** Zeichen für  ![Überblick in xarchitectural diagramm](/help/assets/overview.png)

at.js 2.*x*  verbessert die Unterstützung von Adobe Target für SPAs und kann mit anderen Experience Cloud-Lösungen integriert werden. In diesem Video wird erklärt, wie alles zusammenkommt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Siehe [So funktioniert at.js 2.** ](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) xworks für weitere Informationen.
