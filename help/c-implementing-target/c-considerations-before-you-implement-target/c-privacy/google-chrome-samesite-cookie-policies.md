---
keywords: google;samesite;cookies;chrome 80;ietf
description: Informationen zu Adobe Target und dem SameSite-IETF-Standard, der mit Google Chrome Version 80 eingeführt wurde.
title: Adobe Target und die Cookie-Richtlinien von Google
feature: privacy and security
subtopic: Getting Started
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '2033'
ht-degree: 8%

---


# SameSite-Cookie-Richtlinien von Google Chrome

Google wird anfangen, neue Cookie-Richtlinien für Benutzer vorzuschreiben, die mit Chrome 80 beginnen, das voraussichtlich Anfang 2020 veröffentlicht wird. In diesem Artikel wird alles erläutert, was Sie über die neuen SameSite-Cookie-Richtlinien, die Unterstützung dieser Richtlinien und die Verwendung zur Einhaltung der neuen Google Chrome-Cookie-Richtlinien wissen müssen, [!DNL Adobe Target] [!DNL Target] und beschrieben.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies über Websites hinweg verwendet werden können. Dies ist die erste von vielen Ankündigungen, die Google zur Verbesserung der Privatsphäre und der Sicherheit im Internet machen will.

Given the fact that Facebook has been on the hot seat with regards to privacy and security, other major players such as Apple, and now Google, have been quick to capitalize on the opportunity to create new identities as privacy and security champions. Apple led the pack by first announcing changes to its cookie policies early this year through ITP 2.1 and recently, ITP 2.2. In ITP 2.1, Apple completely blocks third-party cookies and keeps cookies created on the browser for only seven days. In ITP 2.2, cookies are kept for only one day. Google’s announcement is nowhere near as aggressive as Apple’s, but it is the first step toward the same end goal. For more information on Apple&#39;s policies, see [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## What are cookies and how are they used?

Before we dive into Google’s changes to its cookies policies, let’s touch upon what cookies are and how they are used. Simply put, cookies are small text files stored in the web browser that are used to remember user attributes.

Cookies sind wichtig, da sie das Erlebnis des Benutzers beim Durchsuchen des Internets verbessern. For example, if you are shopping on an eCommerce website and add something to your cart but don’t sign in or purchase in that visit, cookies remember your items and keep them in your cart for your next visit. Or, imagine if you were forced to re-input your username and password every time you visit your favorite social media website. Cookies solve that problem too, because they store information that helps sites identify who you are. These kinds of cookies are called first-party cookies because they are created and used by the website you visited.

Third-party cookies also exist. Um sie besser zu verstehen, lassen Sie uns dieses Beispiel betrachten:

Nehmen wir an, eine hypothetische Social-Media-Firma mit dem Namen &quot;Friends&quot;stellt eine Freigabe-Schaltfläche bereit, die von anderen Sites implementiert wird, damit Freunde den Inhalt der Site im Feed &quot;Freunde&quot;freigeben können. Jetzt liest ein Benutzer einen Newsartikel auf einer News-Website, der die Schaltfläche &quot;Freigeben&quot;verwendet, und klickt auf diesen Artikel, um automatisch auf seinem Freundeskonto zu posten.

Damit dies geschieht, ruft der Browser die Schaltfläche &quot;Freigeben&quot;für Freunde ab, `platform.friends.com` sobald der News-Artikel geladen wird. Innerhalb dieses Prozesses fügt der Browser die Cookies &quot;Freunde&quot;, die die Anmeldedaten des Benutzers enthalten, an die Anforderung an die Server &quot;Freunde&quot;an. Auf diese Weise können Freunde den Newsartikel in ihrem Feed im Namen des Benutzers veröffentlichen, ohne dass der Benutzer sich anmelden muss.

Dies ist alles möglich, indem Drittanbieter-Cookies verwendet werden. In diesem Fall wird das Drittanbieter-Cookie im Browser gespeichert, `platform.friends.com`damit der Beitrag in der Friends-App im Auftrag des Benutzers erstellt werden `platform.friends.com` kann.

Wenn Sie sich einen Moment vorstellen, wie Sie diesen Verwendungsfall ohne Drittanbieter-Cookies erreichen können, muss der Benutzer eine Menge manueller Schritte ausführen. Zunächst muss der Benutzer den Link zum News-Artikel kopieren. Zweitens muss sich der Benutzer separat bei der Friends-App anmelden. Anschließend klickt der Benutzer auf die Schaltfläche Beitrag erstellen. Anschließend kopierte der Benutzer den Link und fügte ihn in das Textfeld ein und klickte schließlich auf &quot;Posten&quot;. Wie Sie sehen können, helfen Drittanbieter-Cookies dem Benutzer enorm, da manuelle Schritte drastisch reduziert werden können.

Im Allgemeinen ermöglichen Drittanbieter-Cookies die Speicherung von Daten im Browser eines Benutzers, ohne dass der Benutzer explizit eine Website besuchen muss.

## Sicherheitsbedenken

Obwohl Cookies die Benutzererfahrung verbessern und die Werbung verstärken, können sie auch Sicherheitslücken wie CSRF-Angriffe (Cross-Site Request Forgery) einführen. Wenn sich ein Benutzer beispielsweise bei einer Bank-Site anmeldet, um Kreditkartenrechnungen zu bezahlen, und die Site verlässt, ohne sich abzumelden, und dann in derselben Sitzung zu einer bösartigen Site navigiert, kann es zu einem CSRF-Angriff kommen. Die böswillige Site könnte Code enthalten, der eine Anforderung an die Banksite sendet, die beim Laden der Seite ausgeführt wird. Da der Benutzer immer noch auf der Bankseite authentifiziert ist, kann der Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten, um ein Ereignis zum Geldtransfer aus dem Benutzerkonto zu starten. Das liegt daran, dass bei jedem Besuch einer Site alle Cookies in der HTTP-Anforderung angehängt werden. Und aufgrund dieser Sicherheitsbedenken versucht Google nun, diese zu mindern.

## Wie verwendet Zielgruppe Cookies?

Lassen Sie uns bei all dem sehen, wie Cookies [!DNL Target] verwendet werden. Damit Sie [!DNL Target] die [!DNL Target] JavaScript-Bibliothek zunächst verwenden können, müssen Sie sie auf Ihrer Site installieren. Auf diese Weise können Sie ein Erstanbieter-Cookie im Browser des Benutzers platzieren, der Ihre Site besucht. Wenn Ihr Benutzer mit Ihrer Website interagiert, können Sie die Verhaltens- und Interessensdaten des Benutzers [!DNL Target] über die JavaScript-Bibliothek weiterleiten. Die [!DNL Target] JavaScript-Bibliothek verwendet Erstanbieter-Cookies, um Identifizierungsinformationen über den Benutzer zu extrahieren, die den Verhalten- und Interessensdaten des Benutzers zugeordnet werden sollen. Diese Daten werden dann verwendet, [!DNL Target] um Ihre Personalisierungs-Aktivitäten zu optimieren.

Zielgruppe verwendet auch (manchmal) Drittanbieter-Cookies. Wenn Sie über mehrere Websites verfügen, die auf verschiedenen Domänen leben, und Sie die Benutzerreise über diese Websites hinweg verfolgen möchten, können Sie Drittanbieter-Cookies nutzen, indem Sie domänenübergreifendes Tracking nutzen. Durch Aktivierung der domänenübergreifenden Verfolgung in der [!DNL Target] JavaScript-Bibliothek wird Ihr Konto mit Drittanbieter-Cookies Beginn. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server von [!DNL Target]und dabei wird ein Drittanbieter-Cookie erstellt und im Browser des Benutzers platziert. Über das Drittanbieter-Cookie, das im Browser des Benutzers gespeichert ist, [!DNL Target] kann ein einheitliches Erlebnis für einen einzelnen Benutzer über verschiedene Domänen hinweg bereitgestellt werden.

## Das neue Cookie-Rezept von Google

Um sicherzustellen, dass Cookies über Sites hinweg gesendet werden, sodass Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens SameSite hinzuzufügen, der Webentwickler verpflichtet, Cookies mit der Attributkomponente SameSite im Set-Cookie-Header zu verwalten.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domäne besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich am besten für Anwendungen, die hohe Sicherheit erfordern, wie zum Beispiel Banken. |
| Nicht streng | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Therefore, this option would be used if the cookie can be used by third-parties, but with an added security benefit that protects users from being victimized by CSRF attacks. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

In Chrome 80 werden zwei unabhängige Einstellungen für Benutzer eingeführt: &quot;SameSite durch Standard-Cookies&quot;und &quot;Cookies ohne SameSite müssen sicher sein.&quot; Diese Einstellungen werden in Chrome 80 standardmäßig aktiviert.

![Gleiche Site, Dialogfeld](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite-Standardcookies**: Bei Festlegung werden alle Cookies, die nicht das Attribut SameSite angeben, automatisch zur Verwendung gezwungen `SameSite = Lax`.
* **Cookies without SameSite must be secure**: When set, cookies without the SameSite attribute or with `SameSite = None` need to be Secure. „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. All websites should use HTTPS to meet this requirement.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

In der Adobe wollen wir stets die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Für die Einstellung &quot;SameSite durch Standard-Cookies&quot;, [!DNL Target] wird weiterhin Personalisierung ohne Auswirkungen und Intervention durch Sie. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Für die Option &quot;Cookies ohne SameSite müssen sicher sein&quot;funktionieren Erstanbieter-Cookies in weiterhin, wenn Sie sich nicht für die domänenübergreifende Verfolgungsfunktion in entscheiden, [!DNL Target]die Erstanbieter-Cookies in [!DNL Target] weiterhin.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Clientseitige Bibliotheken in [!DNL Target] verwenden automatisch das HTTPS-Protokoll und hängen die `SameSite = None` [!DNL Target] und sicheren Flags an Drittanbieter-Cookies an, um sicherzustellen, dass alle Aktivitäten weiterhin bereitgestellt werden.

## Was müssen Sie tun?

To understand what you need to do to have [!DNL Target] continue to work for Google Chrome 80+ users, consult the table below, of which you will see the following columns:

* **Target JavaScript Library**: If you are using mbox.js, at.js 1.*x* oder at.js 2.*x* on your sites.
* **sameSite by default cookies = Aktiviert**: Wenn Ihre Benutzer &quot;SameSite by default cookies&quot;aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen, damit Sie weiter arbeiten [!DNL Target] können?
* **Cookies without SameSite must be secure = Enabled**: If your users have &quot;Cookies without SameSite must be secure&quot; enabled, how does it impact you and is there anything you need to do to have [!DNL Target] continue to work.

| Target JavaScript Library | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js with first-party cookie only. | No impact. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js with cross-domain tracking enabled. | No impact. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, damit diese über ein sicheres Flag verfügen `SameSite = None` können. The Secure flag requires your sites must use the HTTPS protocol. |
| at.js 1.*x*  with first-party cookie. | No impact. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  with cross-domain tracking enabled. | No impact. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, damit diese über ein sicheres Flag verfügen `SameSite = None` können. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was muss die Zielgruppe tun?

Was mussten wir also auf unserer Plattform tun, um Ihnen bei der Einhaltung der neuen Google Chrome 80+ SameSite Cookie-Richtlinien zu helfen?

| JavaScript-Bibliothek der Zielgruppe | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | [!DNL Target] fügt dem Drittanbieter-Cookie das Flag &quot;Sicher&quot;hinzu, wenn `SameSite = None` [!DNL Target] Server aufgerufen werden. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was ist der Effekt, wenn Sie nicht zum HTTPS-Protokoll übergehen?

Der einzige Anwendungsfall, der sich auf Sie auswirkt, ist der Fall, wenn Sie die domänenübergreifende Verfolgungsfunktion [!DNL Target] über &quot;mbox.js&quot;oder &quot;at.js 1&quot;verwenden.*x*. Ohne die Umstellung auf HTTPS, die eine Voraussetzung von Google ist, werden Sie eine Spitze an eindeutigen Besuchern Ihrer Domänen sehen, da das von uns verwendete Drittanbieter-Cookie von Google gelöscht wird. Da das Drittanbieter-Cookie gelöscht wird, kann [!DNL Target] dieser Benutzer keine einheitliche und personalisierte Erfahrung bieten, wenn der Benutzer von einer Domäne zur anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich zur Identifizierung eines einzelnen Benutzers verwendet, der über Domänen navigiert, die Sie besitzen.

## Schlussfolgerung 

Da die Branche Anstrengungen unternimmt, um ein sichereres Web für die Verbraucher zu schaffen, ist [!DNL Adobe] es absolut wichtig, unseren Kunden zu helfen, personalisierte Erlebnisse auf eine Weise bereitzustellen, die Sicherheit und Privatsphäre für die Endbenutzer gewährleistet. Sie müssen lediglich die oben genannten Best Practices befolgen und die neuen SameSite-Cookie-Richtlinien von Google Chrome einhalten, [!DNL Target] um diese zu erfüllen.
