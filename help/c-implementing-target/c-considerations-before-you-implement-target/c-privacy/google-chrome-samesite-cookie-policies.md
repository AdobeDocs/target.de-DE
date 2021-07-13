---
keywords: Google;SameSite;Cookies;Chrome 80;Ietf
description: Erfahren Sie, wie Adobe [!DNL Target] den mit Google Chrome Version 80 eingeführten SameSite-IETF-Standard verarbeitet und was Sie tun müssen, um diese Richtlinien zu erfüllen.
title: Wie behandelt [!DNL Target] die Samesite-Cookie-Richtlinien von Google?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: 5abd2065-3692-4a6d-9ac9-6d416604c2d2
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '1950'
ht-degree: 7%

---

# SameSite-Cookie-Richtlinien von Google Chrome

Google wird ab Chrome 80, das Anfang 2020 veröffentlicht werden soll, standardmäßig neue Cookie-Richtlinien für Benutzer durchsetzen, die mit Chrome 80 beginnen. In diesem Artikel erfahren Sie alles, was Sie über die neuen SameSite-Cookie-Richtlinien wissen müssen, wie [!DNL Adobe Target] diese Richtlinien unterstützt und wie Sie [!DNL Target] verwenden können, um die neuen SameSite-Cookie-Richtlinien von Google Chrome einzuhalten.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies websiteübergreifend verwendet werden können. Dies ist die erste von vielen Ankündigungen, die Google plant, um die Privatsphäre und Sicherheit im Internet zu verbessern.

Angesichts der Tatsache, dass Facebook in Bezug auf Privatsphäre und Sicherheit auf dem heißen Stein war, haben andere wichtige Akteure wie Apple und nun Google die Möglichkeit, neue Identitäten als Datenschutz- und Sicherheitsführer zu schaffen, rasch genutzt. Apple führte das Paket an, indem es Anfang dieses Jahres erstmals Änderungen an seinen Cookie-Richtlinien über ITP 2.1 und kürzlich ITP 2.2 ankündigte. In ITP 2.1 blockiert Apple vollständig Drittanbieter-Cookies und speichert Cookies, die im Browser erstellt wurden, nur sieben Tage lang. In ITP 2.2 werden Cookies nur einen Tag lang aufbewahrt. Die Ankündigung von Google ist nicht annähernd so aggressiv wie die von Apple, aber sie ist der erste Schritt in Richtung des gleichen Endziels. Weitere Informationen zu den Richtlinien von Apple finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Was sind Cookies und wie werden sie verwendet?

Bevor wir uns mit den Änderungen an den Cookie-Richtlinien von Google befassen, sollten wir uns kurz mit den Cookies und ihrer Verwendung befassen. Einfach ausgedrückt, sind Cookies kleine Textdateien, die im Webbrowser gespeichert werden und zum Speichern von Benutzerattributen verwendet werden.

Cookies sind wichtig, da sie das Benutzererlebnis beim Surfen im Internet verbessern. Wenn Sie z. B. auf einer eCommerce-Website einkaufen und etwas zum Warenkorb hinzufügen, sich aber bei diesem Besuch nicht anmelden oder einkaufen, speichern Cookies Ihre Artikel und behalten sie für Ihren nächsten Besuch im Warenkorb. Stellen Sie sich vor, Sie wären gezwungen, bei jedem Besuch Ihrer bevorzugten Social-Media-Website Ihren Benutzernamen und Ihr Passwort erneut einzugeben. Cookies lösen dieses Problem auch, da sie Informationen speichern, die Sites dabei helfen, die Identität zu identifizieren. Diese Arten von Cookies werden als Erstanbieter-Cookies bezeichnet, da sie von der von Ihnen besuchten Website erstellt und verwendet werden.

Es gibt auch Drittanbieter-Cookies. Sehen wir uns folgendes Beispiel an, um sie besser zu verstehen:

Nehmen wir an, ein hypothetisches Social-Media-Unternehmen namens &quot;Freunde&quot;stellt eine Freigabe-Schaltfläche bereit, die von anderen Sites implementiert wird, damit Freunde die Inhalte der Site im Feed &quot;Freunde&quot;freigeben können. Jetzt liest ein Benutzer einen News-Artikel auf einer News-Website, die die Schaltfläche Freigeben verwendet, und klickt darauf, um automatisch auf seinem Freundeskonto zu posten.

Dazu ruft der Browser die Schaltfläche Freundesfreigabe von `platform.friends.com` ab, wenn der News-Artikel geladen wird. Innerhalb dieses Prozesses hängt der Browser Freunde-Cookies, die die angemeldeten Anmeldedaten des Benutzers enthalten, an die Anfrage an die Freunde-Server an. Auf diese Weise können Freunde den Newsartikel im Feed im Namen des Benutzers posten, ohne dass der Benutzer sich anmelden muss.

Dies ist alles durch die Verwendung von Drittanbieter-Cookies möglich. In diesem Fall wird das Drittanbieter-Cookie im Browser für `platform.friends.com` gespeichert, sodass `platform.friends.com` den Beitrag in der Friends-App im Namen des Benutzers erstellen kann.

Wenn Sie sich einen Moment vorstellen, wie dieser Anwendungsfall ohne Drittanbieter-Cookies erreicht werden kann, müsste der Benutzer viele manuelle Schritte ausführen. Zunächst müsste der Benutzer den Link zum News-Artikel kopieren. Zweitens muss sich der Benutzer separat bei der Friends-App anmelden. Anschließend klickte der Benutzer auf die Schaltfläche Beitrag erstellen . Anschließend kopierte der Benutzer den Link, fügte ihn in das Textfeld ein und klickte schließlich auf &quot;Post&quot;. Wie Sie sehen, helfen Drittanbieter-Cookies dem Anwendererlebnis enorm, da manuelle Schritte drastisch reduziert werden können.

Allgemeiner gesagt ermöglichen Drittanbieter-Cookies die Speicherung von Daten im Browser eines Benutzers, ohne dass der Benutzer eine Website explizit aufrufen muss.

## Sicherheitsbedenken

Obwohl Cookies Benutzererlebnisse verbessern und die Werbeanzeige optimieren, können sie auch Sicherheitslücken wie CSRF-Angriffe (Cross Site Request Forgery) verursachen. Wenn sich ein Benutzer beispielsweise auf einer Bank-Website anmeldet, um Kreditkartenrechnungen zu bezahlen, und die Website verlässt, ohne sich abzumelden, und dann in derselben Sitzung zu einer böswilligen Site navigiert, kann es zu einem CSRF-Angriff kommen. Die böswillige Site kann Code enthalten, der eine Anfrage an die Bank-Site sendet, die beim Laden der Seite ausgeführt wird. Da der Benutzer weiterhin auf der Bank-Site authentifiziert ist, kann das Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten und ein Überweisungsereignis aus dem Bankkonto des Benutzers zu initiieren. Dies liegt daran, dass bei jedem Besuch einer Site alle Cookies in der HTTP-Anforderung angehängt werden. Und aufgrund dieser Sicherheitsbedenken versucht Google nun, diese zu mindern.

## Wie verwendet [!DNL Target] Cookies?

Mit all dem sehen wir, wie [!DNL Target] Cookies verwendet. Damit Sie [!DNL Target] überhaupt verwenden können, müssen Sie die JavaScript-Bibliothek [!DNL Target] auf Ihrer Site installieren. Dadurch können Sie ein Erstanbieter-Cookie im Browser des Benutzers platzieren, der Ihre Site besucht. Wenn Ihr Benutzer mit Ihrer Website interagiert, können Sie die Verhaltens- und Interessendaten des Benutzers über die JavaScript-Bibliothek an [!DNL Target] übergeben. Die JavaScript-Bibliothek [!DNL Target] verwendet Erstanbieter-Cookies, um Identifizierungsinformationen über den Benutzer zu extrahieren und sie dem Verhalten und den Interessensdaten des Benutzers zuzuordnen. Diese Daten werden dann von [!DNL Target] verwendet, um Ihre Personalisierungsaktivitäten zu unterstützen.

Target verwendet auch (manchmal) Drittanbieter-Cookies. Wenn Sie über mehrere Websites verfügen, die auf verschiedenen Domänen leben, und die Journey der Benutzer auf diesen Websites verfolgen möchten, können Sie Drittanbieter-Cookies verwenden, indem Sie domänenübergreifendes Tracking nutzen. Durch Aktivierung des domänenübergreifenden Trackings in der JavaScript-Bibliothek [!DNL Target] verwendet Ihr Konto Cookies von Drittanbietern. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server von [!DNL Target]. Dabei wird ein Drittanbieter-Cookie erstellt und im Browser des Benutzers platziert. Über das Drittanbieter-Cookie, das im Browser des Benutzers gespeichert ist, kann [!DNL Target] für einen einzelnen Benutzer ein konsistentes domänenübergreifendes Erlebnis bereitstellen.

## Das neue Cookie-Rezept von Google

Um sicherzustellen, dass Cookies über Sites hinweg gesendet werden, sodass Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens SameSite hinzuzufügen, der von Webentwicklern verlangt, Cookies mit der SameSite-Attributkomponente im Set-Cookie-Header zu verwalten.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domäne besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich am besten für Anwendungen, die hohe Sicherheit erfordern, z. B. Banken. |
| Nicht streng | Cookies mit dieser Einstellung werden nur bei Anforderungen derselben Site oder bei der Navigation auf oberster Ebene mit nicht idempotenten HTTP-Anforderungen wie `HTTP GET` gesendet. Daher würde diese Option verwendet, wenn das Cookie von Drittanbietern verwendet werden kann, jedoch mit einem zusätzlichen Sicherheitsvorteil, der Benutzer vor CSRF-Angriffen schützt. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

Unter Berücksichtigung der oben genannten Aspekte werden in Chrome 80 zwei unabhängige Einstellungen für Benutzer eingeführt: &quot;Standard-SameSite-Cookies&quot;und &quot;Cookies ohne SameSite müssen sicher sein.&quot; Diese Einstellungen sind in Chrome 80 standardmäßig aktiviert.

![SameSite-Dialogfeld](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **Standard-SameSite-Cookies**: Wenn festgelegt, werden alle Cookies, die das Attribut SameSite nicht angeben, automatisch zur Verwendung gezwungen  `SameSite = Lax`.
* **Cookies ohne SameSite müssen sicher** sein: Wenn festgelegt,  `SameSite = None` müssen Cookies ohne das SameSite-Attribut oder mit sicher sein. „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. Alle Websites sollten HTTPS verwenden, um diese Anforderung zu erfüllen.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

Wir möchten in der Adobe stets die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. Wir freuen uns, Ihnen mitteilen zu können, dass [!DNL Target] die neuen Sicherheits- und Datenschutzeinstellungen von Google unterstützt.

Für die Einstellung &quot;Standard-SameSite-Cookies&quot;liefert [!DNL Target] weiterhin Personalisierungen ohne Auswirkungen und Eingriffe durch Sie. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Bei der Option &quot;Cookies ohne SameSite müssen sicher sein&quot;funktionieren die Erstanbieter-Cookies in [!DNL Target] weiterhin, wenn Sie sich nicht für die domänenübergreifende Tracking-Funktion in [!DNL Target] entscheiden.

Wenn Sie sich jedoch für die Verwendung des domänenübergreifenden Trackings entscheiden, um [!DNL Target] domänenübergreifend zu nutzen, erfordert Chrome die Verwendung der Flags `SameSite = None` und Sicher für Drittanbieter-Cookies. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Client-seitige Bibliotheken in [!DNL Target] verwenden automatisch das HTTPS-Protokoll und hängen die Flags `SameSite = None` und Sicher an Drittanbieter-Cookies in [!DNL Target] an, um sicherzustellen, dass alle Aktivitäten weiterhin bereitgestellt werden.

## Was müssen Sie tun?

Um zu verstehen, was Sie tun müssen, damit [!DNL Target] weiterhin für Google Chrome 80+-Benutzer funktioniert, konsultieren Sie die unten stehende Tabelle, von der Ihnen die folgenden Spalten angezeigt werden:

* **JavaScript-Bibliothek** von Target: Wenn Sie at.js 1.** xor at.js 2.** auf Ihren Sites.
* **Standard-SameSite-Cookies = Aktiviert**: Wenn für Ihre Benutzer &quot;Standard-SameSite-Cookies&quot;aktiviert sind, wie wirkt sich dies auf Sie aus und müssen Sie irgendetwas tun,  [!DNL Target] damit Sie weiterhin arbeiten können.
* **Cookies ohne SameSite müssen sicher sein = Aktiviert**: Wenn Ihre Benutzer &quot;Cookies ohne SameSite müssen sicher sein&quot;aktiviert haben, wie wirkt sich dies auf Sie aus und gibt es etwas, das Sie tun müssen, damit Sie  [!DNL Target] weiterhin funktionieren.

| JavaScript-Bibliothek von Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie kein domänenübergreifendes Tracking verwenden. |
| at.js 1.*x*  mit aktiviertem domänenübergreifenden Tracking. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie zur Verfolgung von Benutzern und Google erfordert die Kennzeichnung von Drittanbieter-Cookies  `SameSite = None` und Secure. Für das Flag &quot;Secure&quot;müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Was muss [!DNL Target] tun?

Was mussten wir also in unserer Plattform tun, um Ihnen bei der Einhaltung der neuen Google Chrome 80+ SameSite-Cookie-Richtlinien zu helfen?

| JavaScript-Bibliothek von Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie kein domänenübergreifendes Tracking verwenden. |
| at.js 1.*x*  mit aktiviertem domänenübergreifenden Tracking. | Keine Auswirkung. | at.js 1.*x*  mit aktiviertem domänenübergreifenden Tracking. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Wie wirkt sich das aus, wenn Sie nicht mit dem HTTPS-Protokoll fortfahren?

Der einzige Anwendungsfall, der sich auf Sie auswirkt, ist die Verwendung der domänenübergreifenden Tracking-Funktion in [!DNL Target] bis at.js 1.*x*. Ohne den Wechsel zu HTTPS, was eine Voraussetzung von Google ist, werden Sie einen Anstieg der Unique Visitors in Ihren Domänen feststellen, da das von uns verwendete Drittanbieter-Cookie von Google gelöscht wird. Da das Drittanbieter-Cookie gelöscht wird, kann [!DNL Target] für diesen Benutzer kein konsistentes und personalisiertes Erlebnis bieten, wenn der Benutzer von einer Domäne zu einer anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich zur Identifizierung eines einzelnen Benutzers verwendet, der über Domänen navigiert, deren Inhaber Sie sind.

## Schlussfolgerung 

Da die Branche Fortschritte bei der Schaffung eines sicheren Webs für Verbraucher macht, ist [!DNL Adobe] fest entschlossen, unseren Kunden zu helfen, personalisierte Erlebnisse auf eine Weise bereitzustellen, die Sicherheit und Privatsphäre für Endbenutzer gewährleistet. Sie müssen lediglich die oben genannten Best Practices befolgen und [!DNL Target] nutzen, um die neuen SameSite-Cookie-Richtlinien von Google Chrome einzuhalten.
