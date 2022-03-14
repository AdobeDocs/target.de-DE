---
keywords: Google;SameSite;Cookies;Chrome 80;Ietf
description: Adobe [!DNL Target] behandelt den SameSite-IETF-Standard, der mit Google Chrome Version 80 eingeführt wurde, und was Sie tun müssen, um diese Richtlinien zu erfüllen.
title: Funktionsweise [!DNL Target] Umgang mit den Samsite-Cookie-Richtlinien von Google?
feature: Privacy & Security
role: Developer
exl-id: 5abd2065-3692-4a6d-9ac9-6d416604c2d2
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1948'
ht-degree: 7%

---

# SameSite-Cookie-Richtlinien von Google Chrome

Google wird ab Chrome 80, das Anfang 2020 veröffentlicht werden soll, standardmäßig neue Cookie-Richtlinien für Benutzer durchsetzen, die mit Chrome 80 beginnen. In diesem Artikel erfahren Sie alles, was Sie über die neuen SameSite-Cookie-Richtlinien wissen müssen, und wie [!DNL Adobe Target] unterstützt diese Richtlinien und wie Sie [!DNL Target] , um die neuen SameSite-Cookie-Richtlinien von Google Chrome einzuhalten.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies websiteübergreifend verwendet werden können. Dies ist die erste von vielen Ankündigungen, die Google zur Verbesserung der Privatsphäre und der Sicherheit im Internet vorlegen will.

Angesichts der Tatsache, dass Facebook in Bezug auf Privatsphäre und Sicherheit auf dem heißen Stein war, konnten andere wichtige Akteure wie Apple und jetzt Google rasch die Möglichkeit nutzen, neue Identitäten als Datenschutz- und Sicherheitsführer zu schaffen. Apple führte das Paket an, indem es Anfang dieses Jahres erstmals Änderungen an seinen Cookie-Richtlinien über ITP 2.1 und kürzlich ITP 2.2 ankündigte. In ITP 2.1 blockiert Apple vollständig Drittanbieter-Cookies und speichert Cookies, die im Browser erstellt wurden, nur sieben Tage lang. In ITP 2.2 werden Cookies nur einen Tag lang aufbewahrt. Googles Ankündigung ist nicht annähernd so aggressiv wie die von Apple, aber sie ist der erste Schritt in Richtung desselben Endziels. Weitere Informationen zu den Apple-Richtlinien finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Was sind Cookies und wie werden sie verwendet?

Bevor wir uns mit den Änderungen an den Cookie-Richtlinien von Google befassen, sollten wir uns mit den Cookies und ihrer Verwendung befassen. Einfach ausgedrückt, sind Cookies kleine Textdateien, die im Webbrowser gespeichert werden und zum Speichern von Benutzerattributen verwendet werden.

Cookies sind wichtig, da sie das Benutzererlebnis beim Surfen im Internet verbessern. Wenn Sie z. B. auf einer eCommerce-Website einkaufen und etwas zum Warenkorb hinzufügen, sich aber bei diesem Besuch nicht anmelden oder einkaufen, speichern Cookies Ihre Artikel und behalten sie für Ihren nächsten Besuch im Warenkorb. Stellen Sie sich vor, Sie wären gezwungen, bei jedem Besuch Ihrer bevorzugten Social-Media-Website Ihren Benutzernamen und Ihr Passwort erneut einzugeben. Cookies lösen dieses Problem auch, da sie Informationen speichern, die Sites dabei helfen, die Identität zu identifizieren. Diese Arten von Cookies werden als Erstanbieter-Cookies bezeichnet, da sie von der von Ihnen besuchten Website erstellt und verwendet werden.

Es gibt auch Drittanbieter-Cookies. Sehen wir uns folgendes Beispiel an, um sie besser zu verstehen:

Nehmen wir an, ein hypothetisches Social-Media-Unternehmen namens &quot;Freunde&quot;stellt eine Freigabe-Schaltfläche bereit, die von anderen Sites implementiert wird, damit Freunde die Inhalte der Site im Feed &quot;Freunde&quot;freigeben können. Jetzt liest ein Benutzer einen News-Artikel auf einer News-Website, die die Schaltfläche Freigeben verwendet, und klickt darauf, um automatisch auf seinem Freundeskonto zu posten.

Dazu ruft der Browser die Schaltfläche Freundesfreigabe ab von `platform.friends.com` wenn der News-Artikel geladen wird. Innerhalb dieses Prozesses hängt der Browser Freunde-Cookies, die die angemeldeten Anmeldedaten des Benutzers enthalten, an die Anfrage an die Freunde-Server an. Auf diese Weise können Freunde den Newsartikel im Feed im Namen des Benutzers posten, ohne dass der Benutzer sich anmelden muss.

Dies ist alles durch die Verwendung von Drittanbieter-Cookies möglich. In diesem Fall wird das Drittanbieter-Cookie im Browser für `platform.friends.com`, sodass `platform.friends.com` kann den Beitrag in der Friends-App im Namen des Benutzers erstellen.

Wenn Sie sich einen Moment vorstellen, wie dieser Anwendungsfall ohne Drittanbieter-Cookies erreicht werden kann, müsste der Benutzer viele manuelle Schritte ausführen. Zunächst müsste der Benutzer den Link zum News-Artikel kopieren. Zweitens muss sich der Benutzer separat bei der Friends-App anmelden. Anschließend klickte der Benutzer auf die Schaltfläche Beitrag erstellen . Anschließend kopierte der Benutzer den Link, fügte ihn in das Textfeld ein und klickte schließlich auf &quot;Post&quot;. Wie Sie sehen, helfen Drittanbieter-Cookies dem Anwendererlebnis enorm, da manuelle Schritte drastisch reduziert werden können.

Allgemeiner gesagt ermöglichen Drittanbieter-Cookies die Speicherung von Daten im Browser eines Benutzers, ohne dass der Benutzer eine Website explizit aufrufen muss.

## Sicherheitsbedenken

Obwohl Cookies Benutzererlebnisse verbessern und die Werbeanzeige optimieren, können sie auch Sicherheitslücken wie CSRF-Angriffe (Cross Site Request Forgery) verursachen. Wenn sich ein Benutzer beispielsweise auf einer Bank-Website anmeldet, um Kreditkartenrechnungen zu bezahlen, und die Website verlässt, ohne sich abzumelden, und dann in derselben Sitzung zu einer böswilligen Site navigiert, kann es zu einem CSRF-Angriff kommen. Die böswillige Site kann Code enthalten, der eine Anfrage an die Bank-Site sendet, die beim Laden der Seite ausgeführt wird. Da der Benutzer weiterhin auf der Bank-Site authentifiziert ist, kann das Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten und ein Überweisungsereignis aus dem Bankkonto des Benutzers zu initiieren. Dies liegt daran, dass bei jedem Besuch einer Site alle Cookies in der HTTP-Anforderung angehängt werden. Und aufgrund dieser Sicherheitsbedenken versucht Google jetzt, sie zu mildern.

## Wie funktioniert [!DNL Target] Cookies verwenden?

Mit all dem sehen wir, wie [!DNL Target] verwendet Cookies. Damit Sie [!DNL Target] Zunächst müssen Sie die [!DNL Target] JavaScript-Bibliothek auf Ihrer Site. Dadurch können Sie ein Erstanbieter-Cookie im Browser des Benutzers platzieren, der Ihre Site besucht. Wenn Ihr Benutzer mit Ihrer Website interagiert, können Sie die Verhaltens- und Interessendaten des Benutzers an [!DNL Target] durch die JavaScript-Bibliothek. Die [!DNL Target] Die JavaScript-Bibliothek verwendet Erstanbieter-Cookies, um Identifizierungsinformationen über den Benutzer zu extrahieren und diese den Verhaltens- und Interessensdaten des Benutzers zuzuordnen. Diese Daten werden dann von [!DNL Target] , um Ihre Personalisierungsaktivitäten zu optimieren.

Target verwendet auch (manchmal) Drittanbieter-Cookies. Wenn Sie über mehrere Websites verfügen, die auf verschiedenen Domänen leben, und die Journey der Benutzer auf diesen Websites verfolgen möchten, können Sie Drittanbieter-Cookies verwenden, indem Sie domänenübergreifendes Tracking nutzen. Durch Aktivierung des domänenübergreifenden Trackings im [!DNL Target] JavaScript-Bibliothek verwenden, verwendet Ihr Konto Cookies von Drittanbietern. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server von [!DNL Target]und in diesem Prozess wird ein Drittanbieter-Cookie erstellt und im Browser des Benutzers platziert. Durch das Drittanbieter-Cookie, das im Browser des Benutzers gespeichert ist, [!DNL Target] kann für einen einzelnen Benutzer ein konsistentes Erlebnis über verschiedene Domänen hinweg bereitstellen.

## Neues Cookie-Rezept von Google

Um sicherzustellen, dass Cookies über Sites hinweg gesendet werden, sodass Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens SameSite hinzuzufügen, der Webentwickler verpflichtet, Cookies mit der SameSite-Attributkomponente im Set-Cookie-Header zu verwalten.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domain besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich am besten für Anwendungen, die hohe Sicherheit erfordern, z. B. Banken. |
| Nicht streng | Cookies mit dieser Einstellung werden nur bei Anforderungen derselben Site oder bei der Navigation auf oberster Ebene mit nicht idempotenten HTTP-Anforderungen wie `HTTP GET`. Daher würde diese Option verwendet, wenn das Cookie von Drittanbietern verwendet werden kann, jedoch mit einem zusätzlichen Sicherheitsvorteil, der Benutzer vor CSRF-Angriffen schützt. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

Unter Berücksichtigung der oben genannten Aspekte werden in Chrome 80 zwei unabhängige Einstellungen für Benutzer eingeführt: &quot;Standard-SameSite-Cookies&quot;und &quot;Cookies ohne SameSite müssen sicher sein.&quot; Diese Einstellungen sind in Chrome 80 standardmäßig aktiviert.

![SameSite-Dialogfeld](/help/main/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **Standard-SameSite-Cookies**: Wenn diese Einstellung festgelegt ist, werden alle Cookies, die das SameSite-Attribut nicht angeben, automatisch gezwungen, `SameSite = Lax`.
* **Cookies ohne SameSite müssen sicher sein**: Wenn festgelegt, Cookies ohne das SameSite-Attribut oder mit `SameSite = None` muss sicher sein. „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. Alle Websites sollten HTTPS verwenden, um diese Anforderung zu erfüllen.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

Wir möchten in der Adobe stets die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. Wir freuen uns, Ihnen mitteilen zu können, dass [!DNL Target] unterstützt die neuen Sicherheits- und Datenschutzeinstellungen von Google.

Für die Einstellung &quot;Standard-SameSite-Cookies&quot;gilt Folgendes: [!DNL Target] Sie werden weiterhin Personalisierungen bereitstellen, ohne Auswirkungen und Eingriffe durch Sie zu haben. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Für die Option &quot;Cookies ohne SameSite müssen sicher sein&quot;müssen Sie sich nicht für die domänenübergreifende Tracking-Funktion in [!DNL Target], die Erstanbieter-Cookies in [!DNL Target] wird weiterhin funktionieren.

Wenn Sie sich jedoch für die Verwendung von domänenübergreifendem Tracking entscheiden, um [!DNL Target] domänenübergreifend erfordert Chrome `SameSite = None` und sichere Flags, die für Drittanbieter-Cookies verwendet werden. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Client-seitige Bibliotheken in [!DNL Target] verwendet automatisch das HTTPS-Protokoll und hängt die `SameSite = None` und Sichere Flags für Drittanbieter-Cookies in [!DNL Target] sicherzustellen, dass alle Aktivitäten weiterhin Ergebnisse liefern.

## Was müssen Sie tun?

Um zu verstehen, was Sie tun müssen, um [!DNL Target] weiterhin für Google Chrome 80+-Benutzer arbeiten, sehen Sie sich die unten stehende Tabelle an, in der die folgenden Spalten angezeigt werden:

* **JavaScript-Bibliothek von Target**: Wenn Sie at.js 1.*x* oder at.js 2.*x* auf Ihren Sites.
* **Standard-SameSite-Cookies = Aktiviert**: Wenn für Ihre Benutzer &quot;Standard-SameSite-Cookies&quot;aktiviert sind, wie wirkt sich dies auf Sie aus und gibt es irgendetwas, was Sie tun müssen [!DNL Target] die Arbeit fortzusetzen.
* **Cookies ohne SameSite müssen sicher sein = Aktiviert**: Wenn für Ihre Benutzer &quot;Cookies ohne SameSite müssen sicher sein&quot;aktiviert ist, wie wirkt sich dies auf Sie aus und müssen Sie irgendetwas tun, was Sie tun müssen [!DNL Target] weiterhin arbeiten.

| JavaScript-Bibliothek von Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie kein domänenübergreifendes Tracking verwenden. |
| at.js 1.*x*  mit aktiviertem domänenübergreifenden Tracking. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie zur Benutzerverfolgung und Google erfordert, dass Drittanbieter-Cookies `SameSite = None` und Sichere Markierung. Für das Flag &quot;Secure&quot;müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Funktion [!DNL Target] Müssen Sie das tun?

Was mussten wir also in unserer Plattform tun, um Ihnen bei der Einhaltung der neuen Google Chrome 80+ SameSite-Cookie-Richtlinien zu helfen?

| JavaScript-Bibliothek von Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| at.js 1.*x*  mit Erstanbieter-Cookie. | Keine Auswirkung. | Keine Auswirkung, wenn Sie kein domänenübergreifendes Tracking verwenden. |
| at.js 1.*x*  mit aktiviertem domänenübergreifenden Tracking. | Keine Auswirkung. | at.js 1.*x*  mit aktiviertem domänenübergreifenden Tracking. |
| at.js 2.*x*  | Keine Auswirkung. | Keine Auswirkung. |

## Wie wirkt sich das aus, wenn Sie nicht mit dem HTTPS-Protokoll fortfahren?

Der einzige Anwendungsfall, der sich auf Sie auswirkt, ist die Verwendung der domänenübergreifenden Tracking-Funktion in [!DNL Target] durch at.js 1.*x*. Ohne den Wechsel zu HTTPS, was eine Voraussetzung von Google ist, werden Sie einen Anstieg der Unique Visitors in Ihren Domänen feststellen, da das von uns verwendete Drittanbieter-Cookie von Google gelöscht wird. Und weil das Drittanbieter-Cookie gelöscht wird, [!DNL Target] kann diesem Benutzer kein konsistentes und personalisiertes Erlebnis bieten, wenn er von einer Domäne zu einer anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich zur Identifizierung eines einzelnen Benutzers verwendet, der über Domänen navigiert, deren Inhaber Sie sind.

## Schlussfolgerung 

Da die Branche Fortschritte macht, um ein sichereres Internet für Verbraucher zu schaffen, [!DNL Adobe] ist fest entschlossen, unseren Kunden dabei zu helfen, personalisierte Erlebnisse so bereitzustellen, dass Sicherheit und Datenschutz für Endbenutzer gewährleistet sind. Sie müssen lediglich die oben genannten Best Practices befolgen und von [!DNL Target] , um die neuen SameSite-Cookie-Richtlinien von Google Chrome einzuhalten.
