---
keywords: google;samesite;cookies;chrome 80;ietf
description: Informationen zu Adobe Target und dem SameSite-IETF-Standard, der mit Google Chrome Version 80 eingeführt wurde.
title: Adobe Target und die Cookie-Richtlinien von Google
feature: privacy and security
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '2033'
ht-degree: 8%

---


# SameSite-Cookie-Richtlinien von Google Chrome

Google wird anfangen, neue Cookie-Richtlinien für Benutzer vorzuschreiben, die mit Chrome 80 beginnen, das voraussichtlich Anfang 2020 veröffentlicht wird. In diesem Artikel wird alles erklärt, was Sie über die neuen SameSite-Cookie-Richtlinien wissen müssen, wie [!DNL Adobe Target] diese Richtlinien unterstützt und wie Sie [!DNL Target] verwenden können, um die neuen SameSite-Cookie-Richtlinien von Google Chrome einzuhalten.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies über Websites hinweg verwendet werden können. Dies ist die erste von vielen Ankündigungen, die Google zur Verbesserung der Privatsphäre und der Sicherheit im Internet machen will.

Angesichts der Tatsache, dass Facebook in Bezug auf Privatsphäre und Sicherheit auf dem heißen Stein war, haben andere wichtige Akteure wie Apple und jetzt Google schnell die Gelegenheit genutzt, neue Identitäten als Schutz- und Sicherheitsmeister zu schaffen. Apple führte das Paket durch, indem er Anfang dieses Jahres Änderungen seiner Cookie-Richtlinien durch ITP 2.1 und kürzlich ITP 2.2 ankündigte. In ITP 2.1 blockiert Apple Cookies von Drittanbietern vollständig und hält Cookies, die im Browser erstellt wurden, nur sieben Tage lang bei. In ITP 2.2 werden Cookies nur einen Tag lang aufbewahrt. Die Ankündigung von Google ist nicht annähernd so aggressiv wie die von Apple, aber sie ist der erste Schritt in Richtung auf dasselbe Endziel. Weitere Informationen zu den Richtlinien von Apple finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Was sind Cookies und wie werden sie verwendet?

Bevor wir in die Änderungen der Cookie-Richtlinien von Google eintauchen, sollten wir uns mit den Cookies und deren Verwendung befassen. Einfach ausgedrückt sind Cookies kleine Textdateien, die im Webbrowser gespeichert werden und die zum Speichern von Benutzerattributen verwendet werden.

Cookies sind wichtig, da sie das Erlebnis des Benutzers beim Durchsuchen des Internets verbessern. Wenn Sie z. B. auf einer eCommerce-Website einkaufen und etwas zum Einkaufswagen hinzufügen, sich aber bei diesem Besuch nicht anmelden oder einkaufen, merken die Cookies Ihre Artikel und halten sie für den nächsten Besuch im Warenkorb. Oder stellen Sie sich vor, Sie wären gezwungen, Ihren Benutzernamen und Ihr Passwort jedes Mal erneut einzugeben, wenn Sie Ihre bevorzugte Social Media-Website besuchen. Cookies lösen auch dieses Problem, da sie Informationen speichern, die Sites dabei helfen, herauszufinden, wer Sie sind. Solche Cookies werden Erstanbieter-Cookies genannt, da sie von der von Ihnen besuchten Website erstellt und verwendet werden.

Auch Drittanbieter-Cookies sind vorhanden. Um sie besser zu verstehen, lassen Sie uns dieses Beispiel betrachten:

Nehmen wir an, eine hypothetische Social-Media-Firma mit dem Namen &quot;Friends&quot;stellt eine Freigabe-Schaltfläche bereit, die von anderen Sites implementiert wird, damit Freunde den Inhalt der Site im Feed &quot;Freunde&quot;freigeben können. Jetzt liest ein Benutzer einen Newsartikel auf einer News-Website, der die Schaltfläche &quot;Freigeben&quot;verwendet, und klickt auf diesen Artikel, um automatisch in seinem Freundeskonto zu posten.

Damit dies geschieht, ruft der Browser die Schaltfläche &quot;Freigeben&quot;von `platform.friends.com` ab, wenn der News-Artikel geladen wird. Innerhalb dieses Prozesses fügt der Browser die Cookies &quot;Freunde&quot;, die die Anmeldedaten des Benutzers enthalten, an die Anforderung an die Server &quot;Freunde&quot;an. Auf diese Weise können Freunde den Newsartikel in ihrem Feed im Namen des Benutzers veröffentlichen, ohne dass der Benutzer sich anmelden muss.

Dies ist alles möglich, indem Drittanbieter-Cookies verwendet werden. In diesem Fall wird das Drittanbieter-Cookie im Browser für `platform.friends.com` gespeichert, sodass `platform.friends.com` den Beitrag in der Friends-App im Auftrag des Benutzers erstellen kann.

Wenn Sie sich einen Moment vorstellen, wie Sie diesen Verwendungsfall ohne Drittanbieter-Cookies erreichen können, muss der Benutzer eine Menge manueller Schritte ausführen. Zunächst muss der Benutzer den Link zum News-Artikel kopieren. Zweitens muss sich der Benutzer separat bei der Friends-App anmelden. Anschließend klickt der Benutzer auf die Schaltfläche Beitrag erstellen. Anschließend kopierte der Benutzer den Link und fügte ihn in das Textfeld ein und klickte schließlich auf &quot;Posten&quot;. Wie Sie sehen können, helfen Drittanbieter-Cookies dem Benutzer enorm, da manuelle Schritte drastisch reduziert werden können.

Im Allgemeinen ermöglichen Drittanbieter-Cookies die Speicherung von Daten im Browser eines Benutzers, ohne dass der Benutzer explizit eine Website besuchen muss.

## Sicherheitsbedenken

Obwohl Cookies die Benutzererfahrung verbessern und die Werbung verstärken, können sie auch Sicherheitslücken wie CSRF-Angriffe (Cross-Site Request Forgery) einführen. Wenn sich ein Benutzer beispielsweise bei einer Bank-Site anmeldet, um Kreditkartenrechnungen zu bezahlen, und die Site verlässt, ohne sich abzumelden, und dann in derselben Sitzung zu einer bösartigen Site navigiert, kann es zu einem CSRF-Angriff kommen. Die böswillige Site könnte Code enthalten, der eine Anforderung an die Banksite sendet, die beim Laden der Seite ausgeführt wird. Da der Benutzer immer noch auf der Bankseite authentifiziert ist, kann der Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten, um ein Ereignis zum Geldtransfer aus dem Benutzerkonto zu starten. Das liegt daran, dass bei jedem Besuch einer Site alle Cookies in der HTTP-Anforderung angehängt werden. Und aufgrund dieser Sicherheitsbedenken versucht Google nun, diese zu mindern.

## Wie verwendet Zielgruppe Cookies?

Lassen Sie uns mit all dem sehen, wie [!DNL Target] Cookies verwendet. Damit Sie [!DNL Target] zunächst verwenden können, müssen Sie die [!DNL Target] JavaScript-Bibliothek auf Ihrer Site installieren. Auf diese Weise können Sie ein Erstanbieter-Cookie im Browser des Benutzers platzieren, der Ihre Site besucht. Wenn Ihr Benutzer mit Ihrer Website interagiert, können Sie die Verhaltens- und Interessensdaten des Benutzers über die JavaScript-Bibliothek an [!DNL Target] weitergeben. Die JavaScript-Bibliothek [!DNL Target] verwendet Erstanbieter-Cookies, um Identifizierungsinformationen über den Benutzer zu extrahieren, die den Verhalten- und Interessensdaten des Benutzers zugeordnet werden sollen. Diese Daten werden dann von [!DNL Target] verwendet, um Ihre Personalisierungs-Aktivitäten zu optimieren.

Zielgruppe verwendet auch (manchmal) Drittanbieter-Cookies. Wenn Sie über mehrere Websites verfügen, die auf verschiedenen Domänen leben, und Sie die Benutzerreise über diese Websites hinweg verfolgen möchten, können Sie Drittanbieter-Cookies nutzen, indem Sie domänenübergreifendes Tracking nutzen. Durch Aktivierung der domänenübergreifenden Verfolgung in der JavaScript-Bibliothek [!DNL Target] wird Ihr Konto mit Drittanbieter-Cookies Beginn. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server von [!DNL Target]. Dabei wird ein Drittanbieter-Cookie erstellt und in den Browser des Benutzers eingefügt. Durch das Drittanbieter-Cookie, das im Browser des Benutzers gespeichert ist, kann [!DNL Target] ein konsistentes Erlebnis über verschiedene Domänen hinweg für einen einzelnen Benutzer bereitstellen.

## Das neue Cookie-Rezept von Google

Um sicherzustellen, dass Cookies über Sites hinweg gesendet werden, sodass Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens SameSite hinzuzufügen, der Webentwickler verpflichtet, Cookies mit der Attributkomponente &quot;SameSite&quot;im Set-Cookie-Header zu verwalten.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domäne besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich am besten für Anwendungen, die hohe Sicherheit erfordern, wie zum Beispiel Banken. |
| Nicht streng | Cookies mit dieser Einstellung werden nur auf Anforderungen derselben Site oder auf der obersten Navigationsebene mit nicht-idempotenten HTTP-Anforderungen wie `HTTP GET` gesendet. Daher würde diese Option verwendet werden, wenn das Cookie von Dritten verwendet werden kann, jedoch mit einem zusätzlichen Sicherheitsvorteil, der die Benutzer vor einer Viktimisierung durch CSRF-Angriffe schützt. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

In Chrome 80 werden zwei unabhängige Einstellungen für Benutzer eingeführt: &quot;SameSite durch Standard-Cookies&quot;und &quot;Cookies ohne SameSite müssen sicher sein.&quot; Diese Einstellungen werden in Chrome 80 standardmäßig aktiviert.

![Gleiche Site, Dialogfeld](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite-Standardcookies**: Bei Festlegung werden alle Cookies, die nicht das Attribut SameSite angeben, automatisch zur Verwendung gezwungen  `SameSite = Lax`.
* **Cookies ohne SameSite müssen sicher** sein: Bei Festlegung müssen Cookies ohne das Attribut SameSite oder mit dem Wert Secure sein.  `SameSite = None` „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. Alle Websites sollten HTTPS verwenden, um diese Anforderung zu erfüllen.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

In der Adobe wollen wir stets die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. Wir freuen uns, Ihnen mitteilen zu können, dass [!DNL Target] die neuen Sicherheits- und Datenschutzeinstellungen von Google unterstützt.

Für die Einstellung &quot;SameSite by default cookies&quot; liefert [!DNL Target] weiterhin Personalisierung ohne Auswirkungen und Eingriffe durch Sie. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Wenn Sie sich nicht für die domänenübergreifende Verfolgungsfunktion in [!DNL Target] entscheiden, funktionieren die Erstanbieter-Cookies in [!DNL Target] für die Option &quot;Cookies ohne SameSite müssen sicher sein&quot;weiterhin.

Wenn Sie sich jedoch für die domänenübergreifende Verfolgung entscheiden, um [!DNL Target] über mehrere Domänen hinweg zu nutzen, müssen für Chrome `SameSite = None`- und Secure-Flags für Drittanbieter-Cookies verwendet werden. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Clientseitige Bibliotheken in [!DNL Target] verwenden automatisch das HTTPS-Protokoll und hängen die `SameSite = None`- und Secure-Flags an Drittanbieter-Cookies in [!DNL Target] an, um sicherzustellen, dass alle Aktivitäten weiterhin bereitgestellt werden.

## Was müssen Sie tun?

Um zu verstehen, was Sie tun müssen, damit [!DNL Target] weiterhin für Google Chrome 80+-Benutzer funktioniert, sehen Sie in der folgenden Tabelle nach, in der die folgenden Spalten angezeigt werden:

* **Zielgruppe JavaScript Library**: Wenn Sie mbox.js verwenden, at.js 1.*x* oder at.js 2.*xon* Ihre Sites.
* **sameSite by default cookies = Aktiviert**: Wenn Ihre Benutzer &quot;SameSite by default cookies&quot;aktiviert haben, wie wirkt sich dies auf Sie aus und müssen Sie irgendetwas tun, um weiterhin  [!DNL Target] zu funktionieren?
* **Cookies ohne SameSite müssen sicher sein = Aktiviert**: Wenn Ihre Benutzer &quot;Cookies ohne SameSite müssen sicher sein&quot; aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen, damit Sie  [!DNL Target] weiterhin funktionieren.

| JavaScript-Bibliothek der Zielgruppe | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, um  `SameSite = None` und Secure-Flag zu haben. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies, um  `SameSite = None` und Secure-Flag zu haben. Für das Secure-Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was muss die Zielgruppe tun?

Was mussten wir also auf unserer Plattform tun, um Ihnen bei der Einhaltung der neuen Google Chrome 80+ SameSite Cookie-Richtlinien zu helfen?

| JavaScript-Bibliothek der Zielgruppe | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox.js nur mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox.js mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | [!DNL Target] fügt dem Drittanbieter-Cookie beim Aufruf von  `SameSite = None` Servern das Flag  [!DNL Target] und Sicher hinzu. |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. | Keine Auswirkung. | at.js 1.*x*  mit aktivierter domänenübergreifender Verfolgung. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was ist der Effekt, wenn Sie nicht zum HTTPS-Protokoll übergehen?

Der einzige Anwendungsfall, der sich auf Sie auswirkt, ist der Fall, wenn Sie die domänenübergreifende Verfolgungsfunktion in [!DNL Target] über mbox.js oder at.js 1 verwenden.*x*. Ohne die Umstellung auf HTTPS, die eine Voraussetzung von Google ist, werden Sie eine Spitze an eindeutigen Besuchern Ihrer Domänen sehen, da das von uns verwendete Drittanbieter-Cookie von Google gelöscht wird. Da das Drittanbieter-Cookie gelöscht wird, kann [!DNL Target] für diesen Benutzer kein einheitliches und personalisiertes Erlebnis bereitstellen, wenn der Benutzer von einer Domäne zu einer anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich zur Identifizierung eines einzelnen Benutzers verwendet, der über Domänen navigiert, die Sie besitzen.

## Schlussfolgerung 

Da die Branche Anstrengungen unternimmt, um ein sichereres Web für Verbraucher zu schaffen, ist [!DNL Adobe] absolut entschlossen, unseren Kunden zu helfen, personalisierte Erlebnisse auf eine Weise bereitzustellen, die Sicherheit und Privatsphäre für Endbenutzer gewährleistet. Sie müssen lediglich die oben genannten Best Practices befolgen und [!DNL Target] nutzen, um die neuen Google Chrome-Cookie-Richtlinien einzuhalten.
