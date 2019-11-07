---
keywords: google;samesite;cookies;chrome 80;ietf
description: Informationen zu Adobe Target und dem SameSite-IETF-Standard, der mit Google Chrome Version 80 eingeführt wurde.
title: Adobe Target- und Google-Cookie-Richtlinien
subtopic: Erste Schritte
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# SameSite-Cookie-Richtlinien von Google Chrome

Google wird anfangen, neue Cookie-Richtlinien für Benutzer vorzuschreiben, die mit Chrome 80 beginnen, das voraussichtlich Anfang 2020 veröffentlicht wird. In diesem Artikel wird alles erläutert, was Sie über die neuen SameSite-Cookie-Richtlinien, die Unterstützung dieser Richtlinien und die Verwendung zur Einhaltung der neuen Google Chrome-Cookie-Richtlinien wissen müssen, [!DNL Adobe Target] [!DNL Target] und beschrieben.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies über Websites hinweg verwendet werden können. Dies ist die erste von vielen Ankündigungen, die Google zur Verbesserung der Privatsphäre und der Sicherheit im Internet machen will.

Angesichts der Tatsache, dass Facebook in Bezug auf Privatsphäre und Sicherheit auf dem heißen Stein war, haben andere wichtige Akteure wie Apple und jetzt Google schnell die Gelegenheit genutzt, neue Identitäten als Schutz- und Sicherheitsmeister zu schaffen. Apple führte das Paket durch, indem er Anfang dieses Jahres Änderungen seiner Cookie-Richtlinien durch ITP 2.1 und kürzlich ITP 2.2 ankündigte. In ITP 2.1 blockiert Apple Cookies von Drittanbietern vollständig und hält Cookies, die im Browser erstellt wurden, nur sieben Tage lang bei. In ITP 2.2 werden Cookies nur einen Tag lang aufbewahrt. Die Ankündigung von Google ist nicht annähernd so aggressiv wie die von Apple, aber sie ist der erste Schritt in Richtung auf dasselbe Endziel. Weitere Informationen zu den Richtlinien von Apple finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Was sind Cookies und wie werden sie verwendet?

Bevor wir in die Änderungen der Cookie-Richtlinien von Google eintauchen, sollten wir uns mit den Cookies und deren Verwendung befassen. Einfach ausgedrückt sind Cookies kleine Textdateien, die im Webbrowser gespeichert werden und die zum Speichern von Benutzerattributen verwendet werden.

Cookies sind wichtig, da sie die Benutzererfahrung beim Durchsuchen des Internets verbessern. Wenn Sie z. B. auf einer eCommerce-Website einkaufen und etwas zum Einkaufswagen hinzufügen, sich aber bei diesem Besuch nicht anmelden oder einkaufen, merken Cookies Ihre Artikel und halten sie für den nächsten Besuch im Warenkorb. Oder stellen Sie sich vor, Sie wären gezwungen, Ihren Benutzernamen und Ihr Passwort jedes Mal erneut einzugeben, wenn Sie Ihre bevorzugte Social Media-Website besuchen. Cookies lösen auch dieses Problem, da sie Informationen speichern, die Sites bei der Identifizierung Ihrer Person unterstützen. Solche Cookies werden Erstanbieter-Cookies genannt, da sie von der von Ihnen besuchten Website erstellt und verwendet werden.

Auch Drittanbieter-Cookies sind vorhanden. Um sie besser zu verstehen, lassen Sie uns dieses Beispiel betrachten:

Nehmen wir an, ein hypothetisches Social-Media-Unternehmen namens "Freunde"stellt eine Freigabe-Schaltfläche bereit, die andere Sites implementieren, damit Freunde den Inhalt der Site im Feed "Freunde"freigeben können. Jetzt liest ein Benutzer einen Newsartikel auf einer News-Website, der die Schaltfläche "Freigeben"verwendet, und klickt auf diesen Artikel, um automatisch auf seinem Freundeskonto zu posten.

Damit dies geschieht, ruft der Browser die Schaltfläche "Freigeben"für Freunde ab, `platform.friends.com` sobald der News-Artikel geladen wird. Innerhalb dieses Prozesses fügt der Browser die Cookies "Freunde", die die Anmeldedaten des Benutzers enthalten, an die Anforderung an die Server "Freunde"an. Auf diese Weise können Freunde den Newsartikel in ihrem Feed im Namen des Benutzers veröffentlichen, ohne dass der Benutzer sich anmelden muss.

Dies ist alles möglich, indem Drittanbieter-Cookies verwendet werden. In diesem Fall wird das Drittanbieter-Cookie im Browser gespeichert, `platform.friends.com`damit der Beitrag in der Friends-App im Auftrag des Benutzers erstellt werden `platform.friends.com` kann.

Wenn Sie sich einen Moment vorstellen, wie Sie diesen Verwendungsfall ohne Drittanbieter-Cookies erreichen können, muss der Benutzer eine Menge manueller Schritte ausführen. Zunächst muss der Benutzer den Link zum News-Artikel kopieren. Zweitens muss sich der Benutzer separat bei der Friends-App anmelden. Anschließend klickt der Benutzer auf die Schaltfläche Beitrag erstellen. Anschließend kopierte der Benutzer den Link und fügte ihn in das Textfeld ein und klickte schließlich auf "Posten". Wie Sie sehen können, helfen Drittanbieter-Cookies dem Benutzer enorm, da manuelle Schritte drastisch reduziert werden können.

Im Allgemeinen ermöglichen Drittanbieter-Cookies die Speicherung von Daten im Browser eines Benutzers, ohne dass der Benutzer explizit eine Website besuchen muss.

## Sicherheitsbedenken

Obwohl Cookies die Benutzererfahrung verbessern und die Werbung verstärken, können sie auch Sicherheitslücken wie CSRF-Angriffe (Cross-Site Request Forgery) einführen. Wenn sich ein Benutzer beispielsweise bei einer Bank-Site anmeldet, um Kreditkartenrechnungen zu bezahlen, und die Site verlässt, ohne sich abzumelden, und dann in derselben Sitzung zu einer bösartigen Site navigiert, kann es zu einem CSRF-Angriff kommen. Die böswillige Site könnte Code enthalten, der eine Anforderung an die Banksite sendet, die beim Laden der Seite ausgeführt wird. Da der Benutzer weiterhin auf der Bankseite authentifiziert ist, kann der Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten, um ein Überweisungsereignis vom Bankkonto des Benutzers zu starten. Das liegt daran, dass bei jedem Besuch einer Site alle Cookies in der HTTP-Anforderung angehängt werden. Und aufgrund dieser Sicherheitsbedenken versucht Google nun, diese zu mindern.

## Wie verwendet Target Cookies?

Lassen Sie uns bei all dem sehen, wie Cookies [!DNL Target] verwendet werden. Damit Sie [!DNL Target] die [!DNL Target] JavaScript-Bibliothek zunächst verwenden können, müssen Sie sie auf Ihrer Site installieren. Auf diese Weise können Sie ein Erstanbieter-Cookie im Browser des Benutzers platzieren, der Ihre Site besucht. Wenn Ihr Benutzer mit Ihrer Website interagiert, können Sie die Verhaltens- und Interessensdaten des Benutzers [!DNL Target] über die JavaScript-Bibliothek weiterleiten. Die [!DNL Target] JavaScript-Bibliothek verwendet Erstanbieter-Cookies, um Identifizierungsinformationen über den Benutzer zu extrahieren, die den Verhalten- und Interessensdaten des Benutzers zugeordnet werden sollen. Diese Daten werden dann verwendet, [!DNL Target] um Ihre Personalisierungsaktivitäten zu optimieren.

Target verwendet auch (manchmal) Drittanbieter-Cookies. Wenn Sie über mehrere Websites verfügen, die auf verschiedenen Domänen leben, und Sie die Benutzerreise über diese Websites hinweg verfolgen möchten, können Sie Drittanbieter-Cookies nutzen, indem Sie domänenübergreifendes Tracking nutzen. Durch Aktivierung der domänenübergreifenden Verfolgung in der [!DNL Target] JavaScript-Bibliothek verwendet Ihr Konto Cookies von Drittanbietern. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server von [!DNL Target]und dabei wird ein Drittanbieter-Cookie erstellt und im Browser des Benutzers platziert. Über das Drittanbieter-Cookie, das im Browser des Benutzers gespeichert ist, [!DNL Target] kann ein einheitliches Erlebnis für einen einzelnen Benutzer über verschiedene Domänen hinweg bereitgestellt werden.

## Das neue Cookie-Rezept von Google

Um sicherzustellen, dass Cookies über Sites hinweg gesendet werden, sodass Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens SameSite hinzuzufügen, der Webentwickler dazu verpflichtet, Cookies mit der Attributkomponente SameSite im Set-Cookie-Header zu verwalten.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domäne besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich am besten für Anwendungen, die hohe Sicherheit erfordern, wie zum Beispiel Banken. |
| Nicht streng | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Daher würde diese Option verwendet werden, wenn das Cookie von Dritten verwendet werden kann, jedoch mit einem zusätzlichen Sicherheitsvorteil, der die Benutzer vor einer Viktimisierung durch CSRF-Angriffe schützt. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

In Chrome 80 werden zwei unabhängige Einstellungen für Benutzer eingeführt: "SameSite durch Standard-Cookies"und "Cookies ohne SameSite müssen sicher sein." Diese Einstellungen werden in Chrome 80 standardmäßig aktiviert.

![Gleiche Site, Dialogfeld](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite-Standardcookies**: Bei Festlegung werden alle Cookies, die nicht das Attribut SameSite angeben, automatisch zur Verwendung gezwungen `SameSite = Lax`.
* **Cookies ohne SameSite müssen sicher** sein: Bei Festlegung müssen Cookies ohne das Attribut SameSite oder mit dem Wert Secure sein. `SameSite = None` „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. Alle Websites sollten HTTPS verwenden, um diese Anforderung zu erfüllen.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

Adobe möchte stets die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Für die Einstellung "SameSite durch Standard-Cookies", [!DNL Target] wird weiterhin Personalisierung ohne Auswirkungen und Intervention durch Sie. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Für die Option "Cookies ohne SameSite müssen sicher sein"funktionieren Erstanbieter-Cookies in weiterhin, wenn Sie sich nicht für die domänenübergreifende Verfolgungsfunktion in entscheiden, [!DNL Target]die Erstanbieter-Cookies in [!DNL Target] weiterhin.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Clientseitige Bibliotheken in [!DNL Target] verwenden automatisch das HTTPS-Protokoll und hängen die `SameSite = None` [!DNL Target] und sicheren Flags an Drittanbieter-Cookies an, um sicherzustellen, dass alle Aktivitäten weiterhin bereitgestellt werden.

## Was müssen Sie tun?

Um zu verstehen, was Sie tun müssen, damit Sie weiterhin für Google Chrome 80+-Benutzer arbeiten [!DNL Target] können, sehen Sie in der folgenden Tabelle die folgenden Spalten:

* **JavaScript-Bibliothek** in Target: Wenn Sie mbox.js verwenden, at.js 1.*x* oder at.js 2.*x* auf Ihren Sites.
* **sameSite by default cookies = Aktiviert**: Wenn Ihre Benutzer "SameSite by default cookies"aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen, damit Sie weiter arbeiten [!DNL Target] können?
* **Cookies ohne SameSite müssen sicher sein = Aktiviert**: Wenn Ihre Benutzer "Cookies ohne SameSite müssen sicher sein" aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen, damit Sie [!DNL Target] weiter arbeiten können.

| JavaScript-Bibliothek in Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, damit diese über ein sicheres Flag verfügen `SameSite = None` können. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, damit diese über ein sicheres Flag verfügen `SameSite = None` können. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was muss Target tun?

Was mussten wir also auf unserer Plattform tun, um Ihnen bei der Einhaltung der neuen Google Chrome 80+ SameSite Cookie-Richtlinien zu helfen?

| JavaScript-Bibliothek in Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | [!DNL Target] fügt dem Drittanbieter-Cookie beim Aufruf von `SameSite = None` [!DNL Target] Servern das Flag "Sicher"hinzu. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was ist der Effekt, wenn Sie nicht zum HTTPS-Protokoll übergehen?

Der einzige Anwendungsfall, der sich auf Sie auswirkt, ist der Fall, wenn Sie die domänenübergreifende Verfolgungsfunktion [!DNL Target] über "mbox.js"oder "at.js 1"verwenden.*x*. Ohne auf HTTPS umzustellen, was eine Voraussetzung für Google ist, werden Sie eine Spitze bei Unique Visitors über Ihre Domänen hinweg sehen, da das von uns verwendete Drittanbieter-Cookie von Google gelöscht wird. Da das Drittanbieter-Cookie gelöscht wird, kann [!DNL Target] dieser Benutzer keine einheitliche und personalisierte Erfahrung bieten, wenn der Benutzer von einer Domäne zur anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich zur Identifizierung eines einzelnen Benutzers verwendet, der über Domänen navigiert, die Sie besitzen.

## Schlussfolgerung 

Da die Branche Anstrengungen unternimmt, um ein sichereres Web für die Verbraucher zu schaffen, ist [!DNL Adobe] es absolut wichtig, unseren Kunden zu helfen, personalisierte Erlebnisse auf eine Weise bereitzustellen, die Sicherheit und Privatsphäre für die Endbenutzer gewährleistet. Sie müssen lediglich die oben genannten Best Practices befolgen und die neuen SameSite-Cookie-Richtlinien von Google Chrome einhalten, [!DNL Target] um diese zu erfüllen.
