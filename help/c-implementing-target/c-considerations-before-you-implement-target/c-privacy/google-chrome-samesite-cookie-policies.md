---
description: Informationen zu Target und der Norm samesite IETF, die ab Google Chrome Version 76 verwendet werden.
keywords: google; samesite
seo-description: Informationen zu Adobe Target und der Norm "samesite IETF" , die mit Google Chrome Version 76 eingeführt wurden.
seo-title: Richtlinien für Adobe Target und samesite-Cookies
solution: Target
subtopic: Erste Schritte
title: Google Chrome-Cookie-Richtlinien
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: b6b649e31173e80fd0a79b3ce695c130052bf81a

---


# Google Chrome-Cookie-Richtlinien

Google hat kürzlich angekündigt, dass die Entwickler seit Chrome 76, die für ein Release vom 30. Juli 2019 verpackt sind, explizit angeben müssen, welche Cookies auf Websites funktionieren und welche Cookies Benutzer verfolgen können.

## Überblick über die SameSite

To provide safeguards around when cookies can be sent across sites so that users are protected, Google adds support for an IETF standard called &quot;SameSite&quot; in Google Chrome 76 (and later), which requires web developers to manage cookies with the SameSite attribute component in the `Set-Cookie` header.

Es gibt drei verschiedene Werte, die an das Attribut samesite übergeben werden können: Streng, Lax oder Keine.

| Wert | Beschreibung |
| --- | --- |
| Strikt | Cookies mit dieser Einstellung können nur aufgerufen werden, wenn Sie die Domäne besuchen, auf der sie ursprünglich festgelegt wurde. Mit anderen Worten, strikte Blockierungen blockieren das Cookie vollständig auf allen Websites. Diese Option eignet sich optimal für Anwendungen, für die hohe Sicherheit erforderlich ist, z. B. Banken. |
| Lax | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, such as `HTTP GET`. Therefore, this option should be used if the cookie can be used by third-parties, but with an added security benefit that protects users from being victimized by [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery) (Cross-Site Request Forgery) attacks. |
| Keine | Cookies mit dieser Einstellung funktionieren genauso wie Cookies heute. |

In den beiden folgenden Einstellungen werden die beiden Einstellungen Chrome 76 (und höher) vorgestellt: &quot; Samesite nach standardmäßigen Cookies&quot; und &quot;Cookies ohne samesite müssen sicher sein&quot; . Benutzer haben die Möglichkeit, entweder die Einstellung oder beide Einstellungen zu aktivieren.

| Einstellung | Beschreibung |
| --- | --- |
| Standardcookies von samesite | When set, all cookies that don&#39;t specify the SameSite attribute are automatically forced with `SameSite = Lax`. |
| Cookies ohne samesite müssen sicher sein | When set, cookies without the SameSite attribute or with `SameSite = None`, need to be Secure. In diesem Kontext müssen alle Browser-Anforderungen dem HTTPS-Protokoll entsprechen. Cookies, die diese Anforderung nicht erfüllen, werden abgelehnt. |

![Samesite-Einstellungsseite](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

## Target befolgt die bewährten Verfahren von Google

Mit Target wollen wir sicherstellen, dass Sie erfolgreich die neuesten Best Practices der Branche für die Sicherheit unterstützen. Wir freuen uns, dass Target die neuen Sicherheitseinstellungen unterstützt, die in Google Chrome 76 eingeführt wurden.

Wenn Ihre Besucher die standardeinstellung für Cookies in &quot;samesite&quot; aktiviert haben, stellt Target weiterhin Personalisierung ohne jegliche Auswirkung und ohne Eingreifen von Ihnen bereit. Target uses first-party cookies and will continue to function properly as the flag `SameSite = Lax` is applied by Google Chrome.

Wenn Besucher die &quot;Cookies ohne samesite müssen sicher sein müssen&quot; aktivieren und Sie nicht für die domänenübergreifende Tracking-Funktion von Target teilnehmen, funktionieren die Erstanbieter-Cookies von Target weiterhin. However, when you opt-in to using cross-domain tracking to leverage Target across multiple domains, Google Chrome 76 (and later) requires `SameSite = None` and `Secure` flags to be used for third-party cookies. Dies bedeutet, dass Sie sicherstellen müssen, dass Ihre Sites das HTTPS-Protokoll verwenden. Target&#39;s client-side libraries automatically use the HTTPS protocol and, in addition to that, attach the `SameSite = None` and `Secure` flags to Target’s third-party cookie to ensure all activities continue to deliver.

## Was müssen Sie tun?

Lesen Sie die folgende Tabelle, um zu verstehen, was Sie tun müssen, damit Target weiterhin für Google Chrome 76 + Benutzer funktioniert.

Die Tabelle enthält die folgenden Spalten:

* **Clientseitige Bibliothek als Ziel**: ob Sie mbox. js, at. js 1 verwenden.*x*oder at. js 2.*x* auf Ihren Sites und Einfluss von Google Chrome-Einstellungen auf die
* **Cooksite standardmäßig Cookies = Aktiviert**: Wenn Ihre Besucher auf Chrome 76 + über &quot;Skripte für standardmäßige Cookies&quot; verfügen, wie wirkt sich dies auf Sie aus und ist alles, was erforderlich ist, damit Target weiterhin funktioniert
* **Cookies ohne samesite müssen sicher = Aktiviert** sein: Wenn Ihre Besucher auf Chrome 76 + die Option &quot;Cookies ohne samesite sicher sein müssen&quot; aktiviert haben, wie wirkt sich dies auf Sie aus und es gibt alles, was Sie benötigen, damit Target weiterhin funktioniert.
* **Domänenübergreifende Verfolgung von Adobe Target = Aktiviert**: Wenn Ihre Besucher auf Chrome 76 + die &quot;Gleiche Site nach standardmäßigen Site-Cookies&quot; aktivieren und&quot; Cookies ohne samesite sicher sein müssen&quot; , und Sie Target für domänenübergreifende Verfolgung verwenden, wie wirkt sich dies auf Sie aus und ist alles, was erforderlich ist, damit Target weiterhin funktioniert

| Clientseitige Bibliothek in Target | Samesite standardmäßig Cookies = Aktiviert | Cookies ohne samesite müssen sicher = aktiviert sein | Domänenübergreifende Verfolgung von Adobe Target = Aktiviert |
| --- | --- | --- | --- |
| mbox.js | Keine Auswirkung, da mbox. js ein Erstanbieter-Cookie verwendet | Keine Auswirkungen, da Kunden keine domänenübergreifende Verfolgung verwenden | Kunden müssen das HTTPS-Protokoll für ihre Site aktivieren.<br>Target verwendet ein Drittanbieter-Cookie, um Benutzer zu verfolgen, und Google erfordert Drittanbieter-Cookies für die Verwendung `SameSite = None` und für Sites, die das HTTPS-Protokoll verwenden. |
| at.js 1.*x* | Keine Auswirkung, weil at. js 1.*x* verwendet ein Erstanbieter-Cookie | Keine Auswirkungen, da Kunden keine domänenübergreifende Verfolgung verwenden | Kunden müssen das HTTPS-Protokoll für ihre Site aktivieren.<br>Target verwendet ein Drittanbieter-Cookie zur Verfolgung von Benutzern und Google erfordert, dass Drittanbieter-Cookies vorhanden und `SameSite = None` für Sites das HTTPS-Protokoll verwendet werden. |
| at.js 2.*x* | Keine Auswirkung, weil at. js 2.*x* verwendet ein Erstanbieter-Cookie | Keine Auswirkungen, da Kunden keine domänenübergreifende Verfolgung verwenden | Domänenübergreifende Verfolgung wird in at. js 2 nicht unterstützt.*x* und daher gibt es keine Auswirkungen auf Kunden. |

## Was muss Adobe tun?

| Clientseitige Bibliothek in Target | Samesite standardmäßig Cookies = Aktiviert | Cookies ohne samesite müssen sicher = aktiviert sein | Domänenübergreifende Verfolgung von Adobe Target = Aktiviert |
| --- | --- | --- | --- |
| mbox.js | Keine Auswirkung, da mbox. js ein Erstanbieter-Cookie verwendet | Keine Auswirkungen, da Kunden keine domänenübergreifende Verfolgung verwenden | Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called. |
| at.js 1.*x* | Keine Auswirkung, weil at. js 1.*x* verwendet ein Erstanbieter-Cookie | Keine Auswirkungen, da Kunden keine domänenübergreifende Verfolgung verwenden | Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called. |
| at.js 2.*x* | Keine Auswirkung, weil at. js 2.*x* verwendet ein Erstanbieter-Cookie | Keine Auswirkungen, da Kunden keine domänenübergreifende Verfolgung verwenden | Domänenübergreifende Verfolgung wird in at. js 2 nicht unterstützt.*x* |

## Schlussfolgerung

Da die Branche ein sicheres Web für Verbraucher schaffen kann, ist Target absolut verpflichtet, personalisierte Erlebnisse während des Meetings bereitzustellen und die Datenschutzerwartungen der Besucher zu überschreiten.
