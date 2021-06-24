---
keywords: Übersicht und Referenz; Webkit; Cookies; Erstanbieter; Drittanbieter; Erstanbieter; Erstanbieter; Drittanbieter
description: Erfahren Sie mehr über [!DNL Target] Cookie-Verhalten (Erstanbieter-Cookie, Drittanbieter-Cookie mit Erstanbieter-Cookie oder Drittanbieter-Cookie allein).
title: Wo finde ich Informationen über [!DNL Target] Cookies?
feature: at.js
role: Developer
exl-id: 1c4e5b0b-8ae4-4526-aea0-318a33f4d247
source-git-commit: e773db20ac593108aa3e54aae1bcb2c0f713e387
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 58%

---

# Cookies in Target

Das Verhalten von Cookies ist davon abhängig, ob es sich um ein Erstanbieter-Cookie, ein Drittanbieter-Cookie mit Erstanbieter-Cookie oder nur um ein Drittanbieter-Cookie handelt.

>[!NOTE]
>
>Dieses Thema enthält Informationen zu `mboxSession` und `mboxPC`. Best Practices bei der Implementierung empfehlen, vertrauliche Informationen nicht mit den Cookie-Daten zu verknüpfen oder zu speichern: `mboxSession` oder `mboxPC`.

Siehe auch [Löschen des Target-Cookies](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md).

## Verwenden von Erstanbieter-Cookies und Drittanbieter-Cookies {#section_F71B29420C004A7FA3B1921E619B326E}

Durch Ihre Site-Einrichtung wird bestimmt, welche Cookies Sie verwenden. Es ist hilfreich zu verstehen, wie [!DNL Target] funktioniert, wenn Sie versuchen, Erst- und Drittanbieter-Cookies zu verstehen. Siehe [ [!DNL Adobe Target] Funktionsweise von ](/help/c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584) für weitere Informationen.

Es gibt drei Haupt-Nutzungsszenarien für Cookies:

1. Eine Domäne.

   Alle Ihre Tests finden innerhalb einer Top-Level-Domäne (`www.domain.com`, `store.domain.com`, `anysub.domain.com` usw.) statt.

   Ansatz: Verwenden Sie nur Erstanbieter-Cookies (Standardeinstellung).

1. Die Benutzer wechseln zwischen Domänen und Sie möchten ihr Verhalten auf allen diesen Domänen nachverfolgen und testen.

   Beispiel: Ein Benutzer besucht Ihren Onlineshop, geht aber über Yahoo Store zum Checkout. Drei Vorgehensweisen (erarbeiten Sie mit Ihrem Kundenbetreuer die beste Vorgehensweise):

   * Erstanbieter- und Drittanbieter-Cookies aktivieren.
   * Nur Drittanbieter-Cookies aktivieren (selten, doch der Vorteil ist, dass das Mbox-Cookie von Ihrer Domäne fern bleibt).
   * Nur Erstanbieter-Cookies aktivieren und den Parameter `mboxSession` beim Wechseln von Domänen weitergeben.

      Der Parameter `mboxSession` muss an eine Landingpage weitergegeben und von der JavaScript-Bibliothek (Adobe Experience Platform Web SDK oder at.js) referenziert werden. Es darf sich nicht um eine Zwischenseite als Weiterleitung handeln.

1. Sie verwenden nur AdBoxes oder Flashboxes auf einer Site eines Drittanbieters.

   Zwei Vorgehensweisen (erarbeiten Sie mit Ihrem Kundenbetreuer den besten Ansatz):

   * Erstanbieter- und Drittanbieter-Cookies aktivieren.

      Erstanbieter- und Drittanbieter-Cookies sind für Flashbox- und dynamische Kreativinhalte erforderlich.

   * Nur Drittanbieter-Cookies aktivieren.

      Diese Vorgehensweise wird nur in seltenen Fällen angewendet, in denen AdBox-Implementierungen ohne On-Site-Targeting verwendet werden.

## Verhalten von Erstanbieter-Cookies {#section_CE6313D979EA4D0897D2F661E7A8AFA7}

Das Erstanbieter-Cookie wird unter [!DNL clientdomain.com] gespeichert, wobei `clientdomain` Ihre Domäne ist.

Die JavaScript-Bibliothek generiert ein `mboxSession ID` und speichert es im [!DNL Target]-Cookie. Die erste Mbox-Antwort enthält das Angebot und das JavaScript, um die von der Anwendung erzeugte `mboxPC ID` im Mbox-Cookie zu speichern.

>[!NOTE]
>
>Das Erstanbieter-Cookie [!DNL AMCV_###@AdobeOrg] wird immer als [!DNL Experience Cloud Visitor ID] festgelegt.

## Verhalten von Drittanbieter-Cookies {#section_4C3A83990BF8415BB1806602D84AED48}

Das Drittanbieter-Cookie wird unter [!DNL clientcode.tt.omtrdc.net] und das Erstanbieter-Cookie unter [!DNL clientdomain.com] gespeichert, wobei `clientdomain` Ihre Domäne ist.

Die JavaScript-Bibliothek generiert eine `mboxSession ID`. Die erste Ortsanforderung gibt HTTP-Antwortheader zurück, die versuchen, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet.

Wenn der Browser Drittanbieter-Cookies akzeptiert, enthält die Weiterleitungsanfrage diese Cookies und das Angebot wird zurückgegeben.

Wenn der Browser Drittanbieter-Cookies ablehnt, enthält die Weiterleitungsanfrage diese Cookies nicht und es wird überall auf der Seite Standardinhalt angezeigt. Da keine Cookies eingerichtet wurden, wird bei jeder Seitenanfrage der gleiche Prozess ausgeführt.

>[!NOTE]
>
>Das [!DNL demdex.net]-Cookie wird gesetzt, wenn Drittanbieter-Cookies nicht blockiert werden.

## Verhalten von Drittanbieter- und Erstanbieter-Cookies {#section_F0C9AD8BFDF8457A999C4A07A0F7A981}

Das Drittanbieter-Cookie wird unter [!DNL clientcode.tt.omtrdc.net] und das Erstanbieter-Cookie unter [!DNL clientdomain.com] gespeichert, wobei `clientdomain` Ihre Domäne ist.

Die JavaScript-Bibliothek generiert eine `mboxSession ID`. Die erste Ortanforderung gibt HTTP-Antwortheader zurück, die versuchen, Drittanbieter-Cookies namens `mboxSession` und `mboxPC` festzulegen. Eine Weiterleitungsanfrage wird zusammen mit einem zusätzlichen Parameter (`mboxXDomainCheck=true`) zurückgesendet.

Wenn der Browser Drittanbieter-Cookies akzeptiert, enthält die Weiterleitungsanfrage diese Cookies und das Angebot wird zurückgegeben.

Einige Browser weisen Drittanbieter-Cookies ab. Wenn das Drittanbieter-Cookie blockiert wird, funktioniert das Erstanbieter-Cookie immer noch. [!DNL Target] versucht, das Drittanbieter-Cookie festzulegen. Falls dies nicht möglich ist, kann [!DNL Target] nur die spezifische Domäne des Kunden nachverfolgen. Domänenübergreifendes Tracking funktioniert nicht, wenn das Drittanbieter-Cookie blockiert ist, es sei denn, das `mboxSession` wird an den domänenüberschreitenden Link angehängt. In diesem Fall wird ein weiteres Erstanbieter-Cookie gesetzt und mit dem Erstanbieter-Cookie der vorherigen Domäne synchronisiert.

## Cookie-Einstellungen {#section_B498B8D1A34A444BBF84CC720EE9D87F}

Das Cookie verfügt über mehrere Standardeinstellungen. Sie können diese Einstellungen bei Bedarf ändern, mit Ausnahme der Cookie-Dauer. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Cookie-Einstellungen ändern möchten.

| Einstellung | Informationen |
|--- |--- |
| Cookie-Name | mbox. |
| Cookie-Domäne | Die obersten und die darunter liegenden Ebenen der Domänen, von denen der Inhalt geliefert wird. Da der Cookie von der Domäne Ihres Unternehmens bereitgestellt wird, handelt es sich um ein Erstanbieter-Cookie.<br>Beispiel: `mycompany.com`. |
| Serverdomäne | `clientcode.tt.omtrdc.net`, unter Verwendung des Kundencodes für Ihr Konto. |
| Cookie-Dauer | Das Cookie verbleibt zwei Wochen nach der letzten Anmeldung im Browser des Besuchers. Sie können die Cookie-Dauer nicht ändern. |
| P3P-Richtlinie | Das Cookie wird mit einer P3P-Richtlinie veröffentlicht, wie sie von den Standardeinstellungen in den meisten Browsern gefordert wird. Eine P3P-Richtlinie gibt einem Browser an, wer das Cookie bereitstellt und wie die Informationen verwendet werden. |

Das Cookie enthält verschiedene Werte, um zu verwalten, wie Ihre Besucher Kampagnen erleben:

| Wert | Definition |
|--- |--- |
| session ID | Eine eindeutige Kennung für eine Benutzersitzung. Standardmäßig ist diese ID 30 Minuten gültig. |
| pc ID | Eine eingeschränkt dauerhafte Kennung für den Browser eines Besuchers. Wird 14 Tage beibehalten. |
| check | Ein einfacher Testwert, mit dem bestimmt wird, ob ein Besucher Cookies unterstützt. Wird immer dann eingestellt, wenn ein Besucher eine Seite anfordert. |
| disable | Wird eingestellt, wenn die Ladezeit des Besuchers den in der JavaScript-Bibliotheksdatei konfigurierten Timeout überschreitet. Standardmäßig ist dieser Wert eine Stunde gültig. |

## Auswirkungen auf [!DNL Target] für Safari-Besucher aufgrund von Änderungen des Trackings durch Apple WebKit {#section_2A2E5730ED7D4A0985C904AFEA310AAE}

**Wie funktioniert das  [!DNL Adobe Target] Tracking?**

| Cookies | Details |
|--- |--- |
| Erstanbieter-Domänen | Die Standardimplementierung für [!DNL Target]-Kunden. Die „Mbox“-Cookies werden in der Domäne des Kunden festgelegt. |
| Drittanbieter-Tracking | Das Tracking von Drittanbietern ist für Anwendungsfälle für Werbung und Targeting in [!DNL Target] und [!DNL Adobe Audience Manager] (AAM) wichtig. Für das Drittanbieter-Tracking sind siteübergreifende Techniken zur Skripterstellung erforderlich. [!DNL Target] verwendet zwei Cookies, „mboxSession“ und „mboxPC“, die in der Domäne `clientcode.tt.omtrd.net` festgelegt sind. |
**Welchen Ansatz verfolgt Apple?**

Von Apple (übersetzter Auszug):

„Intelligent Tracking Prevention ist eine neue WebKit-Funktion, die das siteübergreifende Tracking durch die Einschränkung von Cookies und anderen Website-Daten reduziert.“

„Das nennt man siteübergreifendes Tracking und das von `example-tracker.com` verwendete Cookie wird als Drittanbieter-Cookie bezeichnet. Im Rahmen unserer Tests haben wir beliebte Webseiten gefunden, die mehr als 70 solcher Tracker verwenden, die alle insgeheim Daten der Benutzer sammeln.“

| Ansatz | Details |
|--- |--- |
| Intelligent Tracking Prevention | Weitere Informationen finden Sie unter [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/) auf der Website „WebKit Open Source Web Browser Engine“. |
| Cookies | Der Umgang mit Cookies in Safari:<ul><li>Drittanbieter-Cookies, die sich nicht auf einer Domäne befinden, auf die der Benutzer direkt zugreift, werden nie gespeichert. Dieses Verhalten ist nicht neu. Drittanbieter-Cookies werden in Safari bereits nicht unterstützt.</li><li>Drittanbieter-Cookies, die auf einer Domäne festgelegt sind, auf die der Benutzer direkt zugreift, werden nach 24 Stunden gelöscht.</li><li>Erstanbieter-Cookies werden nach 30 Tagen gelöscht, wenn die Klassifizierung der jeweiligen Erstanbieter-Domäne zeigt, dass Benutzer siteübergreifend verfolgt werden. Dies trifft möglicherweise auf große Unternehmen zu, die Benutzer online auf verschiedene Domänen weiterleiten. Apple hat nicht klargestellt, wie genau diese Domänen klassifiziert sind oder wie eine Domäne feststellen kann, ob sie als seitenübergreifendes Tracking von Benutzern klassifiziert wurden.</li></ul> |
| Maschinelles Lernen zur Identifikation von siteübergreifenden Domänen | Von Apple (übersetzter Auszug):<br>Machine Learning Classifier: Ein Modell für maschinelles Lernen wird verwendet, um zu klassifizieren, welche privat registrierten Top-Domänen den Benutzer anhand der erfassten Statistiken siteübergreifend verfolgen können. Aus den zahlreichen gesammelten Statistiken haben sich drei Vektoren hervorgehoben, die einen starken Indikator für die Classification anhand aktueller Tracking-Vorgehensweisen darstellen: „Teilressource unter Anzahl der eindeutigen Domänen“, „Subframe unter Anzahl der eindeutigen Domänen“ und „Anzahl der eindeutigen Domänen weitergeleitet an“. Die gesamte Datensammlung und Classification erfolgt auf dem Gerät.<br>Wenn der Benutzer jedoch mit  `example.com` als oberster Domäne interagiert, die häufig als Erstanbieterdomäne bezeichnet wird, betrachtet Intelligent Tracking Prevention dies als Signal, dass der Benutzer an der Website interessiert ist, und passt sein Verhalten vorübergehend an, wie in dieser Zeitleiste dargestellt: <br>Wenn der Benutzer mit  `example.com` den letzten 24 Stunden interagiert hat, sind seine Cookies verfügbar, wenn er ein Drittanbieter  `example.com` ist. Diese Vorgehensweise ermöglicht Anmeldeszenarien mit &quot;Mit meinem X-Konto bei Y anmelden&quot;.<ul><li>Domänen, die als Domäne der obersten Ebene besucht werden, sind nicht betroffen. Seiten wie beispielsweise OKTA</li><li>Domänen, bei denen es sich um Sub-Domänen oder Subframes der aktuellen Seite handelt, werden über mehrere eindeutige Domänen hinweg identifiziert.</li></ul> |

**Wie wirkt sich die Adobe aus?**

| Betroffene Funktionalität | Details |
|--- |--- |
| Abmeldeunterstützung | Wegen der durch das WebKit von Apple bewirkten Änderungen am Tracking ist die Unterstützung für Ausschlüsse hinfällig.<br>[!DNL Target] Opt-out verwendet ein Cookie in der  `clientcode.tt.omtrdc.net` Domäne. Weitere Informationen finden Sie unter [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).<br>[!DNL Target] unterstützt zwei Opt-outs:<ul><li>Einen pro Kunde (der Kunde verwaltet den Ausschluss-Link).</li><li>Eine über [!DNL Adobe] , die den Benutzer von allen [!DNL Target]-Funktionen für alle Kunden abmeldet.</li></ul>Beide Methoden verwenden den Drittanbieter-Cookie. |
| [!DNL Target] Aktivitäten | Kunden können ihre [Profillebensdauer](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) für ihre [!DNL Target]-Konten auswählen (bis zu 90 Tage). Wenn die Profillebensdauer des Kontos länger als 30 Tage ist und das Erstanbieter-Cookie gelöscht wird, weil die Domäne des Kunden als Site-übergreifendes Tracking von Benutzern markiert wurde, besteht das Problem darin, dass das Verhalten von Safari-Besuchern in den folgenden Bereichen in [!DNL Target]:<br>**[!DNL Target] Berichten **beeinträchtigt wird: Wenn ein Safari-Benutzer eine Aktivität aufruft, nach 30 Tagen zurückkehrt und dann konvertiert, zählt dieser Benutzer als zwei Besucher und eine Konversion.<br>[!DNL Analytics]Dieses Verhalten gilt auch für Aktivitäten, die als Berichtsquelle nutzen (A4T).<br>** Profil- und Aktivitätsmitgliedschaft **:<ul><li>Profildaten werden gelöscht, wenn das Erstanbieter-Cookie abläuft.</li><li>Die Aktivitätsmitgliedschaft wird gelöscht, wenn das Erstanbieter-Cookie abläuft.</li><li> [!DNL Target] funktioniert in Safari nicht bei Konten, die eine Implementation mit Drittanbieter-Cookie oder Erst- und Drittanbieter-Cookie verwenden. Dieses Verhalten ist nicht neu. Safari hat für eine Weile keine Drittanbieter-Cookies zugelassen.</li></ul><br>**Empfehlungen**: Wenn Bedenken bestehen, dass die Kundendomäne möglicherweise als eine Domäne markiert wird, die Besucher sitzungsübergreifend verfolgt, ist es am sichersten, die Profillebensdauer auf 30 Tage oder weniger in festzulegen  [!DNL Target]. Mit dieser Beschränkung wird sichergestellt, dass Benutzer in Safari und allen anderen Browsern auf ähnliche Weise verfolgt werden. |
