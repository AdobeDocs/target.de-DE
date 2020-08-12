---
keywords: google;samesite;cookies;chrome 80;ietf
description: Informationen zu Adobe Target und dem SameSite-IETF-Standard, der mit Google Chrome Version 80 eingeführt wurde.
title: Adobe Target und die Cookie-Richtlinien von Google
feature: null
subtopic: Getting Started
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '2033'
ht-degree: 8%

---


# SameSite-Cookie-Richtlinien von Google Chrome

Google wird anfangen, neue Cookie-Richtlinien für Benutzer vorzuschreiben, die mit Chrome 80 beginnen, das voraussichtlich Anfang 2020 veröffentlicht wird. In diesem Artikel wird alles erläutert, was Sie über die neuen SameSite-Cookie-Richtlinien, die Unterstützung dieser Richtlinien und die Verwendung zur Einhaltung der neuen Google Chrome-Cookie-Richtlinien wissen müssen, [!DNL Adobe Target] [!DNL Target] und beschrieben.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies über Websites hinweg verwendet werden können. Dies ist die erste von vielen Ankündigungen, die Google zur Verbesserung der Privatsphäre und der Sicherheit im Internet machen will.

Angesichts der Tatsache, dass Facebook in Bezug auf Privatsphäre und Sicherheit auf dem heißen Stein war, haben andere wichtige Akteure wie Apple und jetzt Google schnell die Gelegenheit genutzt, neue Identitäten als Schutz- und Sicherheitsmeister zu schaffen. Apple führte das Paket durch, indem er Anfang dieses Jahres Änderungen seiner Cookie-Richtlinien durch ITP 2.1 und kürzlich ITP 2.2 ankündigte. In ITP 2.1 blockiert Apple Cookies von Drittanbietern vollständig und hält Cookies, die im Browser erstellt wurden, nur sieben Tage lang bei. In ITP 2.2 werden Cookies nur einen Tag lang aufbewahrt. Die Ankündigung von Google ist nicht annähernd so aggressiv wie die von Apple, aber sie ist der erste Schritt in Richtung auf dasselbe Endziel. Weitere Informationen zu den Richtlinien von Apple finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Was sind Cookies und wie werden sie verwendet?

Bevor wir in die Änderungen der Cookie-Richtlinien von Google eintauchen, sollten wir uns mit den Cookies und deren Verwendung befassen. Einfach ausgedrückt sind Cookies kleine Textdateien, die im Webbrowser gespeichert werden und die zum Speichern von Benutzerattributen verwendet werden.

Cookies sind wichtig, da sie das Erlebnis des Benutzers beim Durchsuchen des Internets verbessern. Wenn Sie z. B. auf einer eCommerce-Website einkaufen und etwas zum Einkaufswagen hinzufügen, sich aber bei diesem Besuch nicht anmelden oder einkaufen, merken die Cookies Ihre Artikel und halten sie für den nächsten Besuch im Warenkorb. Oder stellen Sie sich vor, Sie wären gezwungen, Ihren Benutzernamen und Ihr Passwort jedes Mal erneut einzugeben, wenn Sie Ihre bevorzugte Social Media-Website besuchen. Cookies lösen auch dieses Problem, da sie Informationen speichern, die Sites bei der Identifizierung Ihrer Person unterstützen. Solche Cookies werden Erstanbieter-Cookies genannt, da sie von der von Ihnen besuchten Website erstellt und verwendet werden.

Auch Drittanbieter-Cookies sind vorhanden. To better understand them, let’s consider this example:

Nehmen wir an, eine hypothetische Social-Media-Firma mit dem Namen &quot;Friends&quot;stellt eine Freigabe-Schaltfläche bereit, die von anderen Sites implementiert wird, damit Freunde den Inhalt der Site im Feed &quot;Freunde&quot;freigeben können. Jetzt liest ein Benutzer einen Newsartikel auf einer News-Website, der die Schaltfläche &quot;Freigeben&quot;verwendet, und klickt auf diesen Artikel, um automatisch in seinem Freundeskonto zu posten.

Damit dies geschieht, ruft der Browser die Schaltfläche &quot;Freigeben&quot;für Freunde ab, `platform.friends.com` sobald der News-Artikel geladen wird. Innerhalb dieses Prozesses fügt der Browser die Cookies &quot;Freunde&quot;, die die Anmeldedaten des Benutzers enthalten, an die Anforderung an die Server &quot;Freunde&quot;an. Auf diese Weise können Freunde den Newsartikel in ihrem Feed im Namen des Benutzers veröffentlichen, ohne dass der Benutzer sich anmelden muss.

Dies ist alles möglich, indem Drittanbieter-Cookies verwendet werden. In diesem Fall wird das Drittanbieter-Cookie im Browser gespeichert, `platform.friends.com`damit der Beitrag in der Friends-App im Auftrag des Benutzers erstellt werden `platform.friends.com` kann.

Wenn Sie sich einen Moment vorstellen, wie Sie diesen Verwendungsfall ohne Drittanbieter-Cookies erreichen können, muss der Benutzer eine Menge manueller Schritte ausführen. Zunächst muss der Benutzer den Link zum News-Artikel kopieren. Zweitens muss sich der Benutzer separat bei der Friends-App anmelden. Then, the user would click on the Create Post button. Anschließend kopierte der Benutzer den Link und fügte ihn in das Textfeld ein und klickte schließlich auf &quot;Posten&quot;. Wie Sie sehen können, helfen Drittanbieter-Cookies dem Benutzer enorm, da manuelle Schritte drastisch reduziert werden können.

More generally, third-party cookies make it possible for data to be stored on a user’s browser without requiring that user to explicitly visit a website.

## Security concerns

Although cookies enhance user experiences and power advertising, they can also introduce security vulnerabilities like Cross-Site Request Forgery (CSRF) attacks. For example, if a user logs in to a banking site to pay credit card bills and leaves the site without logging out and then browses to a malicious site in the same session, a CSRF attack can occur. Die böswillige Site könnte Code enthalten, der eine Anforderung an die Banksite sendet, die beim Laden der Seite ausgeführt wird. Da der Benutzer immer noch auf der Bankseite authentifiziert ist, kann der Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten, um ein Ereignis zum Geldtransfer aus dem Benutzerkonto zu starten. Das liegt daran, dass bei jedem Besuch einer Site alle Cookies in der HTTP-Anforderung angehängt werden. Und aufgrund dieser Sicherheitsbedenken versucht Google nun, diese zu mindern.

## Wie verwendet Zielgruppe Cookies?

Lassen Sie uns bei all dem sehen, wie Cookies [!DNL Target] verwendet werden. In order for you to use [!DNL Target] in the first place, you need to install the [!DNL Target] JavaScript library on your site. This enables you to place a first-party cookie on the browser of the user that visits your site. As your user interacts with your website, you can pass the user’s behavioral and interest data to [!DNL Target] through the JavaScript library. The [!DNL Target] JavaScript library uses first-party cookies to extract identification information about the user to map to the user’s behavior and interest data. This data is then used by [!DNL Target] to power your personalization activities.

Target also (sometimes) uses third-party cookies. Wenn Sie über mehrere Websites verfügen, die auf verschiedenen Domänen leben, und Sie die Benutzerreise über diese Websites hinweg verfolgen möchten, können Sie Drittanbieter-Cookies nutzen, indem Sie domänenübergreifendes Tracking nutzen. By enabling cross-domain tracking in the [!DNL Target] JavaScript library, your account will start using third-party cookies. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server von [!DNL Target]und dabei wird ein Drittanbieter-Cookie erstellt und im Browser des Benutzers platziert. Through the third-party cookie that lives on the user’s browser, [!DNL Target] is able to deliver a consistent experience across different domains for a single user.

## Das neue Cookie-Rezept von Google

Um sicherzustellen, dass Cookies über Sites hinweg gesendet werden, sodass Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens SameSite hinzuzufügen, der Webentwickler verpflichtet, Cookies mit der Attributkomponente SameSite im Set-Cookie-Header zu verwalten.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domäne besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich am besten für Anwendungen, die hohe Sicherheit erfordern, wie zum Beispiel Banken. |
| Nicht streng | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Daher würde diese Option verwendet werden, wenn das Cookie von Dritten verwendet werden kann, jedoch mit einem zusätzlichen Sicherheitsvorteil, der die Benutzer vor einer Viktimisierung durch CSRF-Angriffe schützt. |
| Keine | Cookies with this setting will work the same way as cookies work today. |

In Chrome 80 werden zwei unabhängige Einstellungen für Benutzer eingeführt: &quot;SameSite durch Standard-Cookies&quot;und &quot;Cookies ohne SameSite müssen sicher sein.&quot; Diese Einstellungen werden in Chrome 80 standardmäßig aktiviert.

![SameSite dialog box](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite-Standardcookies**: Bei Festlegung werden alle Cookies, die nicht das Attribut SameSite angeben, automatisch zur Verwendung gezwungen `SameSite = Lax`.
* **Cookies ohne SameSite müssen sicher** sein: Bei Festlegung müssen Cookies ohne das Attribut SameSite oder mit dem Wert Secure sein. `SameSite = None` „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. Alle Websites sollten HTTPS verwenden, um diese Anforderung zu erfüllen.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

In der Adobe wollen wir stets die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Für die Einstellung &quot;SameSite durch Standard-Cookies&quot;, [!DNL Target] wird weiterhin Personalisierung ohne Auswirkungen und Intervention durch Sie. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Für die Option &quot;Cookies ohne SameSite müssen sicher sein&quot;funktionieren Erstanbieter-Cookies in weiterhin, wenn Sie sich nicht für die domänenübergreifende Verfolgungsfunktion in entscheiden, [!DNL Target]die Erstanbieter-Cookies in [!DNL Target] weiterhin.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Clientseitige Bibliotheken in [!DNL Target] verwenden automatisch das HTTPS-Protokoll und hängen die `SameSite = None` [!DNL Target] und sicheren Flags an Drittanbieter-Cookies an, um sicherzustellen, dass alle Aktivitäten weiterhin bereitgestellt werden.

## Was müssen Sie tun?

Um zu verstehen, was Sie tun müssen, damit Sie weiterhin für Google Chrome 80+-Benutzer arbeiten [!DNL Target] können, sehen Sie in der folgenden Tabelle die folgenden Spalten:

* **Zielgruppe JavaScript Library**: Wenn Sie mbox.js verwenden, at.js 1.*x* oder at.js 2.*x* auf Ihren Sites.
* **sameSite by default cookies = Aktiviert**: Wenn Ihre Benutzer &quot;SameSite by default cookies&quot;aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen, damit Sie weiter arbeiten [!DNL Target] können?
* **Cookies ohne SameSite müssen sicher sein = Aktiviert**: Wenn Ihre Benutzer &quot;Cookies ohne SameSite müssen sicher sein&quot; aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen, damit Sie [!DNL Target] weiter arbeiten können.

| JavaScript-Bibliothek der Zielgruppe | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, damit diese über ein sicheres Flag verfügen `SameSite = None` können. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] uses a third-party cookie to track users and Google requires third-party cookies to have `SameSite = None` and Secure flag. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was muss die Zielgruppe tun?

Was mussten wir also auf unserer Plattform tun, um Ihnen bei der Einhaltung der neuen Google Chrome 80+ SameSite Cookie-Richtlinien zu helfen?

| JavaScript-Bibliothek der Zielgruppe | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | [!DNL Target] fügt dem Drittanbieter-Cookie das Flag &quot;Sicher&quot;hinzu, wenn `SameSite = None` [!DNL Target] Server aufgerufen werden. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | No impact. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  with cross-domain tracking enabled. | No impact. | at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. |
| at.js 2.*x*  | No impact. | Keine Auswirkung. |

## Was ist der Effekt, wenn Sie nicht zum HTTPS-Protokoll übergehen?

The only use case that will impact you is if you are using the cross-domain tracking feature in [!DNL Target] through mbox.js or at.js 1.*x*. Ohne die Umstellung auf HTTPS, die eine Voraussetzung von Google ist, werden Sie eine Spitze an eindeutigen Besuchern Ihrer Domänen sehen, da das von uns verwendete Drittanbieter-Cookie von Google gelöscht wird. Da das Drittanbieter-Cookie gelöscht wird, kann [!DNL Target] dieser Benutzer keine einheitliche und personalisierte Erfahrung bieten, wenn der Benutzer von einer Domäne zur anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich zur Identifizierung eines einzelnen Benutzers verwendet, der über Domänen navigiert, die Sie besitzen.

## Schlussfolgerung 

Da die Branche Anstrengungen unternimmt, um ein sichereres Web für die Verbraucher zu schaffen, ist [!DNL Adobe] es absolut wichtig, unseren Kunden zu helfen, personalisierte Erlebnisse auf eine Weise bereitzustellen, die Sicherheit und Privatsphäre für die Endbenutzer gewährleistet. Sie müssen lediglich die oben genannten Best Practices befolgen und die neuen SameSite-Cookie-Richtlinien von Google Chrome einhalten, [!DNL Target] um diese zu erfüllen.
