---
keywords: at.js;2.0;1.x;Cookies
description: Details zum Umgang mit Cookies in Adobe [!DNL Target] at.js 2.x und at.js 1.x
title: at.js-Cookies
feature: 'at.js '
role: Developer
exl-id: 101be093-72fa-4f66-95bd-4b60e584a059
translation-type: tm+mt
source-git-commit: 7bcc560c56dab8cf8fc69ff9f8b0f087061c258b
workflow-type: tm+mt
source-wordcount: '1827'
ht-degree: 96%

---

# „at.js“-Cookies

Informationen zum Cookie-Verhalten von at.js 2.x und at.js 1.*x*.

## Cookie-Verhalten von at.js 2.x

Für at.js, Version 2.0.0, werden *nur Erstanbieter-Cookies unterstützt*. Genau wie in at.js 1.*x* wird das Erstanbieter-Cookie, „mbox“, unter `clientdomain.com` gespeichert, wobei `clientdomain` Ihre Domäne ist.

at.js erzeugt eine Sitzungs-ID und speichert sie im Cookie. Die erste Antwort enthält alle Aktivitätsinformationen sowie die `TNT` oder `PC ID`, die von den [!DNL Target]-Servern generiert wurde. at.js fügt dann die `TNT/PC ID` zum Cookie hinzu.

Das `AMCV_###@AdobeOrg`-Erstanbieter-Cookie wird immer vom [!DNL Experience Cloud ID Service] festgelegt, obwohl die `ECID` in [!DNL Target]-Anfragen übergeben wird.

### Drittanbieter-Cookies und domänenübergreifendes Tracking werden nicht unterstützt

Domänenübergreifendes Tracking ermöglicht die Anzeige von Sitzungen auf zwei verwandten Sites mit verschiedenen Domänen als einzelne Sitzung. Sie können eine [!DNL Target]-Aktivität erstellen, die sich über `siteA.com` und `siteB.com` erstreckt, während der Besucher im selben Erlebnis verbleibt, wenn er von einer Domäne in die andere wechselt. Diese Funktionalität hängt mit at.js 1.*x* zusammen und damit, wie Erst- und Drittanbieter-Cookies behandelt werden.

In at.js 1.*x* wurde das Drittanbieter-Cookie in der `[CLIENTCODE].tt.omtrdc.net`-Domäne gespeichert, während das Erstanbieter-Cookie in `clientdomain.com` gespeichert wurde. Die erste Anfrage gab HTTP-Antwort-Header zurück, die versuchten, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet. Wenn der Browser Drittanbieter-Cookies akzeptierte, enthält die Weiterleitungsanfrage diese Cookies und das Angebot wurde zurückgegeben. Dieser Arbeitsablauf war möglich, da at.js 1.*x* die HTTP GET-Methode verwendete.

In at.js 2.x wird HTTP GET jedoch nicht mehr verwendet, stattdessen wird HTTP POST verwendet. HTTP POST wird jetzt über at.js verwendet, um JSON-Nutzlasten anstelle von Schlüssel-Wert-Parametern an die [!DNL Target]-Edge-Server zu senden. Das bedeutet, dass die Weiterleitungsanfrage zur Überprüfung, ob ein Browser Drittanbieter-Cookies unterstützt, jetzt nicht mehr funktioniert. Dies liegt daran, dass HTTP GET-Anfragen idempotent sind, während HTTP POST nicht idempotent ist und nicht willkürlich wiederholt werden darf.

Deshalb werden in at.js 2.0.0 weder Drittanbieter-Cookies noch domänenübergreifendes Tracking unterstützt.

## at.js 1.*x* {#at-js-1x-cookie-behavior}

Für at.js 1.*x* ist das Verhalten von Cookies davon abhängig, ob es sich um ein Erstanbieter-Cookie, ein Drittanbieter-Cookie mit Erstanbieter-Cookie oder nur um ein Drittanbieter-Cookie handelt.

### Verwenden von Erstanbieter-Cookies und Drittanbieter-Cookies

Durch Ihre Site-Einrichtung wird bestimmt, welche Cookies Sie verwenden. Das Verständnis der Funktionsweise von Target hilft, den Unterschied zwischen Erstanbieter-Cookies und Drittanbieter-Cookies zu verstehen. Weitere Informationen finden Sie unter [Funktionsweise von Adobe Target](/help/c-intro/how-target-works.md).

Es gibt drei Haupt-Nutzungsszenarien für Cookies:

1. Eine Domäne.

   Sämtliche Tests finden innerhalb einer Top-Level-Domain statt (z. B. `www.domain.com`, `store.domain.com`, `anysub.domain.com`).

   Verwenden Sie nur Erstanbieter-Cookies. Dies ist die Standardvorgehensweise.

1. Die Benutzer wechseln zwischen Domänen und Sie möchten ihr Verhalten auf allen diesen Domänen nachverfolgen und testen.

   Beispiel: Ein Benutzer besucht Ihren Onlineshop, geht aber über Yahoo Store zum Checkout. Drei Vorgehensweisen (erarbeiten Sie mit Ihrem Kundenbetreuer die beste Vorgehensweise):

   * Erstanbieter- und Drittanbieter-Cookies aktivieren.
   * Nur Drittanbieter-Cookies aktivieren (sehr selten, doch der Vorteil ist, dass das at.js-Cookie von Ihrer Domäne fern bleibt).
   * Nur Erstanbieter-Cookies aktivieren und den Parameter `mboxSession` beim Wechseln von Domänen weitergeben.

      Der Parameter `mboxSession` muss an eine Landingpage mit Verweis auf at.js übergeben werden. Es darf sich nicht um eine Zwischenseite als Weiterleitung handeln.

1. Sie verwenden nur AdBoxes oder Flashboxes auf einer Site eines Drittanbieters.

   Zwei Vorgehensweisen (erarbeiten Sie mit Ihrem Kundendienst-Ansprechpartner die beste Vorgehensweise):

   * Erst- und Drittanbieter-Cookies aktivieren.

      Erst- und Drittanbieter-Cookies sind für Flashbox- und dynamische Kreativinhalte erforderlich.

   * Nur Drittanbieter-Cookies aktivieren.

      Diese Vorgehensweise wird nur in seltenen Fällen angewendet, in denen AdBox-Implementierungen ohne On-Site-Targeting verwendet werden.

### Verhalten von Erstanbieter-Cookies

Das Erstanbieter-Cookie wird unter `clientdomain.com` gespeichert, wobei `clientdomain` Ihre Domäne ist.

at.js generiert eine `mboxSession ID` und speichert sie im Cookie. Die erste Antwort enthält das Angebot sowie das JavaScript, um die von der Anwendung erzeugte `mboxPC ID`-Kennung im Mbox-Cookie zu speichern.

>[!NOTE]
>
>Das Erstanbieter-Cookie `AMCV_###@AdobeOrg` wird immer als [!DNL Experience Cloud Visitor ID] festgelegt.

### Verhalten von Drittanbieter-Cookies

Das Drittanbieter-Cookie wird unter `clientcode.tt.omtrdc.net` und das Erstanbieter-Cookie unter `clientdomain.com` gespeichert, wobei `clientdomain` Ihre Domäne ist.

at.js generiert eine `mboxSession ID`. Die erste Ortsanforderung gibt HTTP-Antwortheader zurück, die versuchen, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet.

Wenn der Browser Drittanbieter-Cookies akzeptiert, enthält die Weiterleitungsanfrage diese Cookies und das Angebot wird zurückgegeben.

Wenn der Browser Drittanbieter-Cookies ablehnt, enthält die Weiterleitungsanfrage diese Cookies nicht und es wird überall auf der Seite Standardinhalt angezeigt. Da keine Cookies eingerichtet wurden, wird bei jeder Seitenanfrage der gleiche Prozess ausgeführt.

### Verhalten von Drittanbieter- und Erstanbieter-Cookies

Das Drittanbieter-Cookie wird unter `clientcode.tt.omtrdc.net` und das Erstanbieter-Cookie unter `clientdomain.com` gespeichert, wobei `clientdomain` Ihre Domäne ist.

at.js generiert eine `mboxSession ID`. Die erste Ortanforderung gibt HTTP-Antwortheader zurück, die versuchen, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet.

Wenn der Browser Drittanbieter-Cookies akzeptiert, enthält die Weiterleitungsanfrage diese Cookies und das Angebot wird zurückgegeben.

Einige Browser weisen Drittanbieter-Cookies ab. Wenn das Drittanbieter-Cookie blockiert wird, funktioniert das Erstanbieter-Cookie immer noch. [!DNL Target] versucht, das Drittanbieter-Cookie festzulegen. Falls dies nicht möglich ist, kann [!DNL Target] nur die spezifische Domäne des Kunden nachverfolgen. Eine domänenübergreifende Nachverfolgung funktioniert nicht, wenn der Drittanbieter blockiert ist, es sei denn, die `mboxSession` ist an den domänenüberschreitenden Link angehängt. In diesem Fall wird ein weiteres Erstanbieter-Cookie gesetzt und mit dem Erstanbieter-Cookie der vorherigen Domäne synchronisiert.

## Cookie-Einstellungen

Das Cookie verfügt über mehrere Standardeinstellungen. Sie können diese Einstellungen bei Bedarf ändern, außer die Cookie-Dauer. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Cookie-Einstellungen ändern möchten.

| Einstellung | Informationen |
|--- |--- |
| Cookie-Name | mbox. |
| Cookie-Domäne | Die obersten und die darunter liegenden Ebenen der Domänen, von denen der Inhalt geliefert wird. Da die Belieferung von der Domäne Ihres Unternehmens stattfindet, handelt es sich um ein Erstanbieter-Cookie. Beispiel: `mycompany.com`. |
| Serverdomäne | `clientcode.tt.omtrdc.net`, unter Verwendung des Kundencodes für Ihr Konto. |
| Cookie-Dauer | Das Cookie bleibt zwei Jahre nach seiner letzten Anmeldung im Browser des Besuchers.<br>Die  `deviceIdLifetime` Einstellung kann in  [at.js Version 2.3.1 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) überschrieben werden. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). |
| P3P-Richtlinie | Das Cookie wird mit einer P3P-Richtlinie veröffentlicht, wie sie von den Standardeinstellungen in den meisten Browsern gefordert wird. Durch eine P3P-Richtlinie wird einem Browser angezeigt, wer das Cookie bereitstellt und wie die Informationen verwendet werden. |

Das Cookie enthält verschiedene Werte, mit denen verwaltet werden kann, wie die Besucher die Kampagnen erleben:

| Wert | Definition |
|--- |--- |
| session ID | Eine eindeutige Kennung für eine Benutzersitzung. Standardmäßig ist diese 30 Minuten gültig. |
| pc ID | Eine eingeschränkt dauerhafte Kennung für den Browser eines Besuchers. Wird 14 Tage beibehalten. |
| check | Ein einfacher Testwert, mit dem bestimmt wird, ob ein Besucher Cookies unterstützt. Wird immer dann eingestellt, wenn ein Besucher eine Seite anfordert. |
| disable | Wird eingestellt, wenn die Ladezeit des Besuchers den in der Datei mbox.js konfigurierten Timeout überschreitet. Standardmäßig ist dieser Wert eine Stunde gültig. |

## Auswirkungen auf &lt; a0/> für Safari-Besucher aufgrund von Apple WebKit-Verfolgungsänderungen[!DNL Target]

Berücksichtigen Sie Folgendes:

### Wie funktioniert die Adobe [!DNL Target] Verfolgung?

| Cookies | Details |
|--- |--- |
| Erstanbieter-Domänen | Dies ist die standardmäßige Implementierung für Target-Kunden.  Die „Mbox“-Cookies werden in der Domäne des Kunden festgelegt. |
| Drittanbieter-Tracking | Das Drittanbieter-Tracking stellt für Anwendungsfälle im Werbe- und Targeting-Bereich in Target und in Adobe Audience Manager (AAM) eine wichtige Komponente dar.  Für das Drittanbieter-Tracking sind siteübergreifende Techniken zur Skripterstellung erforderlich.  Target verwendet zwei Cookies, „mboxSession“ und „mboxPC“, die in der Domäne `clientcode.tt.omtrd.net` festgelegt sind. |

### Welchen Ansatz verfolgt Apple?

Von Apple (übersetzter Auszug):

„Intelligent Tracking Prevention ist eine neue WebKit-Funktion, die das siteübergreifende Tracking durch die Einschränkung von Cookies und anderen Website-Daten reduziert.“

„Das nennt man siteübergreifendes Tracking und das von `example-tracker.com` verwendete Cookie wird als Drittanbieter-Cookie bezeichnet. Im Rahmen unserer Tests haben wir beliebte Webseiten gefunden, die mehr als 70 solcher Tracker verwenden, die alle insgeheim Daten der Benutzer sammeln.“

| Ansatz | Details |
|--- |--- |
| Intelligent Tracking Prevention | Weitere Informationen finden Sie unter [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/) auf der Website „WebKit Open Source Web Browser Engine“. |
| Cookies | Der Umgang mit Cookies in Safari:<ul><li>Drittanbieter-Cookies, die sich nicht auf einer Domäne befinden, auf die der Benutzer direkt zugreift, werden nie gespeichert. Dieses Verhalten ist nicht neu. Drittanbieter-Cookies werden in Safari bereits nicht unterstützt.</li><li>Drittanbieter-Cookies, die auf einer Domäne festgelegt sind, auf die der Benutzer direkt zugreift, werden nach 24 Stunden gelöscht.</li><li>Erstanbieter-Cookies werden nach 30 Tagen gelöscht, wenn die Klassifizierung der jeweiligen Erstanbieter-Domäne zeigt, dass Benutzer siteübergreifend verfolgt werden. Dies trifft möglicherweise auf große Unternehmen zu, die Benutzer online auf verschiedene Domänen weiterleiten. Apple hat sich bislang nicht dazu geäußert, wie genau solche Domänen klassifiziert werden oder wie eine Domäne bestimmen kann, ob sie laut ihrer Klassifizierung Benutzer siteübergreifend verfolgt.</li></ul> |
| Maschinelles Lernen zur Identifikation von siteübergreifenden Domänen | Von Apple (übersetzter Auszug):<br>Machine Learning Classifier: Basierend auf den gesammelten Statistiken wird anhand eines maschinell lernenden Modells klassifiziert, welche privat registrierten Top-Level-Domains die Fähigkeit haben, Benutzer siteübergreifend zu verfolgen. Aus den zahlreichen gesammelten Statistiken haben sich drei Vektoren hervorgehoben, die einen starken Indikator für die Classification anhand aktueller Tracking-Vorgehensweisen darstellen: „Teilressource unter Anzahl der eindeutigen Domänen“, „Subframe unter Anzahl der eindeutigen Domänen“ und „Anzahl der eindeutigen Domänen weitergeleitet an“. Die gesamte Datensammlung und Classification erfolgt auf dem Gerät.<br>Wenn der Benutzer jedoch mit example.com als Top-Domäne (häufig als Erstanbieter-Domäne bezeichnet) interagiert, wird dies von Intelligent Tracking Prevention als Signal angesehen, dass der Benutzer an der Website interessiert ist. Das Verhalten von Intelligent Tracking Prevention wird vorübergehend wie in dieser Timeline dargestellt angepasst:<br>Wenn der Benutzer innerhalb der letzten 24 Stunden mit example.com interagiert hat, stehen die Cookies zur Verfügung, wenn es sich bei `example.com` um einen Drittanbieter handelt. Dies ermöglicht Anmeldeszenarien nach dem Schema „Mit meinem X-Konto bei Y anmelden“.<ul><li>Domänen, die als Top-Level-Domäne besucht werden, sind nicht betroffen. Seiten wie beispielsweise OKTA</li><li>Domänen, bei denen es sich um Sub-Domänen oder Subframes der aktuellen Seite handelt, werden über mehrere eindeutige Domänen hinweg identifiziert.</li></ul> |

### Wie wirkt sich das auf Adobe aus?

| Betroffene Funktionalität | Details |
|--- |--- |
| Abmeldeunterstützung | Wegen der durch das WebKit von Apple bewirkten Änderungen am Tracking ist die Unterstützung für Ausschlüsse hinfällig.<br>Der Target-Ausschluss verwendet ein Cookie in der `clientcode.tt.omtrdc.net`-Domäne. Weitere Informationen finden Sie unter [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).<br>Target unterstützt zwei Arten von Ausschlüssen:<ul><li>Einen pro Kunde (der Kunde verwaltet den Ausschluss-Link).</li><li>Einen über Adobe, der den Benutzer für alle Target-Funktionalität für alle Benutzer ausschließt.</li></ul>Beide Methoden verwenden den Drittanbieter-Cookie. |
| Target-Aktivitäten | Kunden können die  [Profillebensdauer](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) für ihre Target-Konten auf bis zu 90 Tage festlegen. Das Problem ist, dass wenn die Profillebensdauer des Kontos länger als 30 Tage ist und das Erstanbieter-Cookie gelöscht wird, da die Domäne des Kunden als Tracking-Benutzer über mehrere Sites hinweg gekennzeichnet wurde, das Verhalten für Safari-Besucher in Target wie folgt beeinflusst wird:<br>**Target-Berichte:** Wenn ein Safari-Benutzer eine Aktivität beginnt, nach 30 Tagen zurückkehrt und dann konvertiert, zählt dieser Benutzer als zwei Besucher und eine Konversion.<br>Dieses Verhalten gilt auch für Aktivitäten, die Analytics als Berichtsquelle nutzen (A4T).<br>**Profil und Aktivitätsmitgliedschaft**:<ul><li>Profildaten werden gelöscht, wenn das Erstanbieter-Cookie abläuft.</li><li>Die Aktivitätsmitgliedschaft wird gelöscht, wenn das Erstanbieter-Cookie abläuft.</li><li> Target funktioniert in Safari nicht bei Konten, die eine Implementation mit Drittanbieter-Cookie oder Erst- und Drittanbieter-Cookie verwenden. Beachten Sie, dass es sich dabei nicht um ein neues Verhalten handelt. Safari erlaubt schon seit einer Weile keine Drittanbieter-Cookies.</li></ul><br>**Vorschläge:** Wenn Sie befürchten, dass die Domäne des Kunden möglicherweise als Domäne markiert wird, die Besucher sitzungsübergreifend verfolgt, ist es am sichersten, die Profillebensdauer in Target auf 30 Tage oder weniger festzulegen. So wird sichergestellt, dass Benutzer in Safari und allen anderen Browsern auf ähnliche Weise verfolgt werden. |
