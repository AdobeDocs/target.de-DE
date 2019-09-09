---
description: Informationen zu Target und dem SameSite-IETF-Standard, der ab Google Chrome Version 76 verwendet wird.
keywords: google;samesite; Cookies; chrome 80; ietf
seo-description: Informationen zu Adobe Target und dem SameSite-IETF-Standard, der mit Google Chrome Version 80 eingeführt wurde.
seo-title: Richtlinien für Adobe Target und Google samesite-Cookies
solution: Target
subtopic: Erste Schritte
title: SameSite-Cookie-Richtlinien von Google Chrome
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# SameSite-Cookie-Richtlinien von Google Chrome

Google beginnt für Benutzer, die mit Chrome 80 beginnend mit Chrome 80 beginnen, standardmäßig neue Cookie-Richtlinien, die in Anfang 2020 veröffentlicht werden. In diesem Artikel wird alles erläutert, was Sie über die neuen Cookie-Richtlinien von samesite wissen müssen, wie [!DNL Adobe Target] diese Richtlinien unterstützt werden und wie Sie die [!DNL Target] neuen samesite-Cookie-Richtlinien von Google Chrome einhalten können.

Ab Chrome 80 müssen Webentwickler explizit angeben, welche Cookies auf Websites funktionieren können. Dies ist die erste von vielen Mitteilungen, die Google plant, um die Privatsphäre und Sicherheit im Web zu verbessern.

Angesichts der Tatsache, dass Facebook im Hinblick auf Datenschutz und Sicherheit auf der Hot Lizenz war, haben sich andere Hauptplayer wie Apple und jetzt auch Google schnell an die Gelegenheit gewöhnt, neue Identitäten als Datenschutz und Sicherheitssieger zu erstellen. Apple hat das Paket geführt, indem er zunächst Änderungen an den Cookie-Richtlinien ankündigte, die seit diesem Jahr über ITP 2.1 und kürzlich ITP 2.2 vorgenommen wurden. In ITP 2.1 blockiert Apple Cookies von Drittanbietern vollständig und hält Cookies nur für sieben Tage an. In ITP 2.2 werden Cookies nur für einen Tag aufbewahrt. Die Ankündigung von Google ist nirgendwo so aggressiv wie die Apple, aber es ist der erste Schritt in Richtung desselben Endziels. Weitere Informationen zu den Apple-Richtlinien finden Sie unter [Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Was sind Cookies und wie werden sie eingesetzt?

Bevor wir in die von Google vorgenommenen Änderungen an den Cookies wechseln, sollten wir uns darauf konzentrieren, welche Cookies und wie sie verwendet werden. Platzieren Sie einfach Cookies, die im Webbrowser gespeichert sind und zum Speichern von Benutzerattributen verwendet werden.

Cookies sind wichtig, da sie das Benutzererlebnis beim Browsen des Web verbessern. Wenn Sie z. B. auf einer E-Commerce-Website einkaufen und Ihren Einkaufswagen etwas hinzufügen, sich jedoch nicht anmelden oder bei diesem Besuch nicht kaufen, speichern Cookies Ihre Artikel und behalten Sie sie für Ihren nächsten Besuch in Ihren Einkaufswagen. Sie sollten sich auch vorstellen, dass Sie jedes Mal, wenn Sie Ihre bevorzugte Social-Media-Website besuchen, gezwungen sind, Ihren Benutzernamen und Ihr Passwort erneut einzugeben. Cookies lösen dieses Problem ebenfalls aus, da sie Informationen speichern, die Sites helfen, wer Sie sind. Diese Cookies werden Erstanbieter-Cookies genannt, da sie von der von Ihnen besuchten Website erstellt und verwendet werden.

Drittanbieter-Cookies sind ebenfalls vorhanden. Um sie besser zu verstehen, sollten wir dieses Beispiel betrachten:

Nehmen wir an, ein hypothetisches soziales Medienunternehmen namens "Freunde" stellt eine Schaltfläche für Freigeben bereit, die andere Sites implementieren, damit Freunde den Inhalt der Site auf dem Freunde-Feed freigeben können. Jetzt liest ein Benutzer einen News-Artikel auf einer News-Website, die über die Schaltfläche "Freigeben" verfügt, und klickt auf ihn, um automatisch in ihrem Freunde-Konto zu posten.

Dazu ruft der Browser die Schaltfläche Freunde freigeben ab, wenn `platform.friends.com` der News-Artikel geladen wird. In diesem Prozess hängt der Browser Freunde-Cookies an, die die angemeldeten Anmeldeinformationen des Benutzers enthalten, der Anforderung an Freunde-Server. Dadurch können Freunde den Nachrichtenartikel im Feed im Namen des Benutzers posten, ohne dass der Benutzer sich anmelden muss.

Dies ist alles möglich, wenn Sie Drittanbieter-Cookies verwenden. In diesem Fall wird das Drittanbieter-Cookie im Browser gespeichert, damit `platform.friends.com`der Beitrag `platform.friends.com` in der Freunde-App im Namen des Benutzers angezeigt werden kann.

Wenn Sie sich einen Moment lang vorstellen, wie Sie diesen Anwendungsfall ohne Drittanbieter-Cookies erreichen, muss der Benutzer viele manuelle Schritte ausführen. Zunächst muss der Benutzer den Link zum News-Artikel kopieren. Zweitens müsste sich der Benutzer separat bei der Freunde-App anmelden. Anschließend würde der Benutzer auf die Schaltfläche Beitrag erstellen klicken. Anschließend würde der Benutzer den Link in das Textfeld kopieren und einfügen und schließlich auf "Posten" klicken. Wie Sie sehen können, helfen Drittanbieter-Cookies erheblich der Benutzererfahrung, da manuelle Schritte drastisch reduziert werden können.

Im Allgemeinen ermöglichen Drittanbieter-Cookies die Speicherung von Daten im Browser eines Benutzers, ohne dass der Benutzer explizit eine Website besuchen muss.

## Sicherheitsbedenken

Obwohl Cookies Benutzererfahrungen und Stromwerbung verbessern, können sie auch Sicherheitslücken wie Cross-Site Request Forgery (CSRF)-Angriffe einführen. Wenn sich ein Benutzer beispielsweise auf einer Banksite anmeldet, um Kreditkartenrechnungen zu bezahlen und die Site zu verlassen, ohne sich abzumelden und zu einer böswilligen Site in derselben Sitzung zu wechseln, kann ein CSRF-Angriff auftreten. Die böswillige Site könnte Code enthalten, der eine Anforderung an die Banking-Site angibt, die beim Laden der Seite ausgeführt wird. Da der Benutzer weiterhin auf der Banksite authentifiziert ist, kann das Sitzungs-Cookie verwendet werden, um einen CSRF-Angriff zu starten, um ein Geldübertragungs-Ereignis aus dem Bankkonto des Benutzers zu initiieren. Dies liegt daran, dass alle Cookies bei jedem Besuch einer Site an die HTTP-Anforderung angehängt werden. Aufgrund dieser Sicherheitsbedenken versucht Google jetzt, diese abzuschwächen.

## Wie verwendet Target Cookies?

In diesem Fall sehen wir, wie Cookies [!DNL Target] verwendet werden. Damit Sie zunächst verwenden [!DNL Target] können, müssen Sie die [!DNL Target] javascript-Bibliothek auf Ihrer Site installieren. Dadurch können Sie ein Erstanbieter-Cookie im Browser des Benutzers platzieren, der Ihre Site besucht. Wenn Ihr Benutzer mit Ihrer Website interagiert, können Sie die Verhaltensdaten des Benutzers an [!DNL Target] die javascript-Bibliothek übergeben. Die [!DNL Target] javascript-Bibliothek verwendet Erstanbieter-Cookies, um Identifizierungsinformationen zu dem Benutzer zu extrahieren, um dem Verhalten und den Zinsdaten des Benutzers zuzuordnen. Diese Daten werden dann genutzt, [!DNL Target] um Ihre Personalisierungsaktivitäten zu nutzen.

Target verwendet auch Drittanbieter-Cookies. Wenn Sie mehrere Websites verwenden, die auf verschiedenen Domänen leben und die Benutzerpfade auf diesen Websites verfolgen möchten, können Sie Drittanbieter-Cookies verwenden, indem Sie domänenübergreifende Verfolgung nutzen. Durch Aktivierung der domänenübergreifenden Verfolgung in der [!DNL Target] javascript-Bibliothek beginnt Ihr Konto mit Cookies von Drittanbietern. Wenn ein Benutzer von einer Domäne zu einer anderen wechselt, kommuniziert der Browser mit dem Backend-Server und [!DNL Target]in diesem Prozess wird ein Drittanbieter-Cookie erstellt und im Browser des Benutzers platziert. Über das Drittanbieter-Cookie, das im Browser des Benutzers lebt, kann für [!DNL Target] einen einzelnen Benutzer ein konsistentes Erlebnis über verschiedene Domänen hinweg bereitgestellt werden.

## Neues Cookie-Rezept von Google

Um Sicherheitsmaßnahmen für die domänenübergreifende Übermittlung von Cookies bereitzustellen, sodass die Benutzer geschützt sind, plant Google, Unterstützung für einen IETF-Standard namens samesite hinzuzufügen, für den Webentwickler Cookies mit der samesite-Attributkomponente im Set-Cookie-Header verwalten müssen.

Es gibt drei verschiedene Werte, die an das Attribut SameSite übergeben werden können: „Streng“, „Nicht streng“ und „Keine“.

| Wert | Beschreibung |
| --- | --- |
| Streng | Auf Cookies mit dieser Einstellung kann nur zugegriffen werden, wenn die Domäne besucht wird, auf der der Cookie eingerichtet wurde. Mit anderen Worten: die Einstellung „Streng“ verhindert die websiteübergreifende Nutzung des Cookies. Diese Option eignet sich optimal für Anwendungen, die hohe Sicherheit erfordern, z. B. Banken. |
| Nicht streng | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Daher wird diese Option verwendet, wenn das Cookie von Dritten verwendet werden kann, aber mit einem zusätzlichen Sicherheitsvorteil, der Benutzer vor CSRF-Angriffen schützt. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

In Chrome 80 werden zwei unabhängige Einstellungen für Benutzer vorgestellt: " Samesite nach standardmäßigen Cookies" und "Cookies ohne samesite müssen sicher sein" . Diese Einstellungen werden standardmäßig in Chrome 80 aktiviert.

![Samesite, Dialogfeld](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **Standardcookies von samesite**: Bei Festlegung werden alle Cookies, die das Attribut samesite nicht angeben, automatisch verwendet `SameSite = Lax`.
* **Cookies ohne samesite müssen sicher** sein: Cookies ohne das Attribut samesite oder `SameSite = None` mit Secure sein. „Sicher“ bedeutet in diesem Zusammenhang, dass alle Browser-Anfragen dem HTTPS-Protokoll folgen müssen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. Alle Websites sollten HTTPS verwenden, um diese Anforderung zu erfüllen.

## Target unterstützt die bewährten Sicherheitsmethoden von Google.

Wir möchten immer die neuesten Best Practices der Branche für Sicherheit und Datenschutz unterstützen. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Für die Einstellung "samesite mit standardmäßiger Cookies [!DNL Target] «wird die Personalisierung weiterhin ohne Einfluss und Intervention bereitgestellt. [!DNL Target] verwendet Erstanbieter-Cookies und funktioniert weiterhin ordnungsgemäß, da das Flag `SameSite = Lax` von Google Chrome angewendet wird.

Wenn die Option "Cookies ohne samesite sicher sein" aktiviert ist und Sie nicht für die domänenübergreifende Tracking-Funktion angemeldet sind [!DNL Target], funktionieren die Erstanbieter-Cookies weiter [!DNL Target] .

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Clientseitige Bibliotheken verwenden [!DNL Target] automatisch das HTTPS-Protokoll und hängen die `SameSite = None` und sicheren Flags an Drittanbieter-Cookies an, um [!DNL Target] sicherzustellen, dass alle Aktivitäten weiterhin bereitgestellt werden.

## Was müssen Sie tun?

Um zu verstehen, was Sie für Google Chrome 80 + Benutzer [!DNL Target] benötigen, lesen Sie die unten stehende Tabelle, in der Sie die folgenden Spalten sehen werden:

* **Javascript-Bibliothek für Target**: Wenn Sie mbox. js verwenden, at. js 1.*x* oder at.js 2.*x* auf Ihren Sites.
* **Cooksite standardmäßig Cookies = Aktiviert**: Wenn Ihre Benutzer "samesite standardmäßig Cookies" aktiviert haben, wie wirkt sich dies auf Sie aus, und es gibt alles, was [!DNL Target] Sie tun müssen, um weiterhin zu funktionieren.
* **Cookies ohne samesite müssen sicher = Aktiviert** sein: Wenn Ihre Benutzer "Cookies ohne samesite sicher sein müssen" aktiviert haben, wie sich dies auf Sie auswirkt, können Sie darauf hindeuten, dass Sie [!DNL Target] weiterhin funktioniert.

| Javascript-Bibliothek für Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox. js nur mit Erstanbieter-Cookies. | Keine Auswirkung. | Keine Auswirkungen, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox. js mit aktivierter domänenübergreifendes Tracking. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie zur Verfolgung von Benutzern und Google erfordert Cookies von Drittanbietern, um das sichere `SameSite = None` Flag zu erhalten. Für das sichere Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 1.*x* mit Erstanbieter-Cookies. | Keine Auswirkung. | Keine Auswirkungen, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x* bei aktivierter domänenübergreifender Verfolgung aktiviert ist. | Keine Auswirkung. | Sie müssen das HTTPS-Protokoll für Ihre Site aktivieren.<br>[!DNL Target] verwendet ein Drittanbieter-Cookie zur Verfolgung von Benutzern und Google erfordert Cookies von Drittanbietern, um das sichere `SameSite = None` Flag zu erhalten. Für das sichere Flag müssen Ihre Sites das HTTPS-Protokoll verwenden. |
| at.js 2.*x* | Keine Auswirkung. | Keine Auswirkung. |

## Was muss Target tun?

Was mussten wir daher auf unserer Plattform tun, um Sie bei der Einhaltung der neuen Cookie-Richtlinien für Google Chrome 80 + samesite zu unterstützen?

| Javascript-Bibliothek für Target | Standard-SameSite-Cookies = Aktiviert | Cookies ohne SameSite müssen sicher sein = Aktiviert |
| --- | --- | --- |
| mbox. js nur mit Erstanbieter-Cookies. | Keine Auswirkung. | Keine Auswirkungen, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| mbox. js mit aktivierter domänenübergreifendes Tracking. | Keine Auswirkung. | [!DNL Target] fügt das Drittanbieter-Cookie hinzu `SameSite = None` , wenn [!DNL Target] Server aufgerufen werden. |
| at.js 1.*x* mit Erstanbieter-Cookies. | Keine Auswirkung. | Keine Auswirkungen, wenn Sie keine domänenübergreifende Verfolgung verwenden. |
| at.js 1.*x* bei aktivierter domänenübergreifender Verfolgung aktiviert ist. | Keine Auswirkung. | at.js 1.*x* bei aktivierter domänenübergreifender Verfolgung aktiviert ist. |
| at.js 2.*x* | Keine Auswirkung. | Keine Auswirkung. |

## Welche Auswirkungen haben Sie, wenn Sie nicht zur Verwendung des HTTPS-Protokolls wechseln?

Der einzige Verwendungsfall, der sich auf Sie auswirkt, ist, wenn Sie die domänenübergreifende Verfolgungsfunktion [!DNL Target] über mbox. js oder at. js 1 verwenden.*x*. Ohne die Umstellung auf HTTPS, was eine Anforderung von Google ist, sehen Sie in all Ihren Domänen eine Spitze, da das Drittanbieter-Cookie, das wir verwenden, von Google abgelegt wird. Und da das Drittanbieter-Cookie abgelegt wird, ist es nicht [!DNL Target] möglich, ein einheitliches und personalisiertes Erlebnis für diesen Benutzer bereitzustellen, wenn der Benutzer von einer Domäne zu einer anderen navigiert. Das Drittanbieter-Cookie wird hauptsächlich verwendet, um einen einzelnen Benutzer zu identifizieren, der über Domänen hinweg navigiert.

## Schlussfolgerung

Da die Branche ein sicheres Web für Verbraucher schaffen kann, ist es absolut [!DNL Adobe] sinnvoll, unseren Kunden dabei zu helfen, personalisierte Erlebnisse auf eine Weise bereitzustellen, die Sicherheit und Datenschutz für Endbenutzer gewährleistet. Sie müssen nur die erwähnten Best Practices befolgen und nutzen die [!DNL Target] neuen samesite-Cookie-Richtlinien von Google Chrome.
