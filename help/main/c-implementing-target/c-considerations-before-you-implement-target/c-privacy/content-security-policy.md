---
keywords: Content Security Policy;csp;at.js;Whitelist;Zulassungsliste;Flimmern;Ausblenden;pre-hide;Vorab ausblenden
description: Erfahren Sie mehr über die CSP-Richtlinie (Content Security Policy), die Sie bei Verwendung von Adobe Target hinzufügen sollten.
title: Wie handhabt  [!DNL Target]  Content Security Policies (CSP)?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 97%

---

# Richtlinien zur Content Security Policy (CSP)

Wenn Sie eine [Content Security Policy](https://de.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre [!DNL Adobe Target]-Implementierung verwenden, sollten Sie die folgenden CSP-Anweisungen hinzufügen, wenn Sie [at.js 2.1 oder höher](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) verwenden:

* `connect-src` mit `*.tt.omtrdc.net` auf der Zulassungsliste. Erforderlich, um die Netzwerkanfrage an das [!DNL Target]-Edge-Netzwerk zuzulassen.
* `style-src unsafe-inline`. Erforderlich, um die Flimmerregelung vorab auszublenden.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein kann.

## Häufig gestellte Fragen (FAQs)

Wenn Sie Näheres zu Sicherheitsrichtlinien erfahren möchten, lesen Sie die folgenden häufig gestellten Fragen:

### Stellen Cross Origin Resource Sharing- (CORS) und Flash Cross-Domain-Richtlinien Sicherheitsprobleme dar?

Die empfohlene Methode zur Implementierung der CORS-Richtlinie besteht darin, den Zugriff nur auf vertrauenswürdige Quellen zu ermöglichen, die den Zugriff über eine Zulassungsliste mit vertrauenswürdigen Domains verlangen. Dasselbe gilt für die Flash Cross-Domain-Richtlinie. Manche [!DNL Adobe Target]-Kunden sind besorgt über die Verwendung von Platzhalterzeichen für Domains in [!DNL Target]. Es wird befürchtet, dass, wenn ein Benutzer bei einer Anwendung angemeldet ist und eine von der Richtlinie zugelassene Domain besucht, schädliche Inhalte, die in dieser Domain ausgeführt werden, theoretisch sensible Inhalte aus der Anwendung abrufen und Aktionen im Sicherheitskontext des angemeldeten Benutzers ausführen können. Dies wird als Cross-Site Request Forgery (CSRF) bezeichnet.

In einer [!DNL Adobe Target]-Implementierung stellen diese Richtlinien normalerweise aber kein Sicherheitsproblem dar.

„adobe.tt.omtrdc.net“ ist eine Adobe-eigene Domain. [!DNL Adobe Target] ist ein Test- und Personalisierungs-Tool, und normalerweise kann [!DNL Target] Anfragen von überall empfangen und verarbeiten, ohne dass eine Authentifizierung erforderlich ist. Diese Anfragen enthalten Schlüssel-Wert-Paare, die für A/B-Tests, Empfehlungen oder die Personalisierung von Inhalten verwendet werden.

[!DNL Adobe] speichert keine personenbezogenen oder anderen sensiblen Informationen auf [!DNL Adobe Target]-Edge-Servern, auf die „adobe.tt.omtrdc.net“ verweist.

[!DNL Target] kann von jeder Domain über JavaScript-Aufrufe aufgerufen werden. Die einzige Möglichkeit, diesen Zugriff zu ermöglichen, besteht darin, „Access-Control-Allow-Origin“ mit einem Platzhalter zu verwenden.
