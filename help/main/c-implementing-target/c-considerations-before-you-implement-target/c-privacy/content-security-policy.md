---
keywords: Content Security Policy;csp;at.js;Whitelist;Zulassungsliste;Flimmern;Ausblenden;pre-hide;Vorab ausblenden
description: Erfahren Sie mehr über die CSP-Richtlinie (Content Security Policy), die Sie bei Verwendung von Adobe Target hinzufügen sollten.
title: Wie handhabt  [!DNL Target]  Content Security Policies (CSP)?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: db632225d21c2e061e82269bec168341b410575a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Richtlinien zur Content Security Policy (CSP)

Wenn Sie eine [Content Security Policy](https://de.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre [!DNL Adobe Target]-Implementierung verwenden, sollten Sie die folgenden CSP-Anweisungen hinzufügen, wenn Sie [at.js 2.1 oder höher](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) verwenden:

* `connect-src` mit `*.tt.omtrdc.net` auf der Zulassungsliste. Erforderlich, um die Netzwerkanfrage an das [!DNL Target]-Edge-Netzwerk zuzulassen.
* `style-src unsafe-inline`. Erforderlich, um die Flimmerregelung vorab auszublenden.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein kann.

## Häufig gestellte Fragen (FAQs)

Lesen Sie die folgenden häufig gestellten Fragen zu Sicherheitsrichtlinien:

### Stellt die Cross Origin Resource Sharing (CORS)- und Flash Cross-Domain-Richtlinien Sicherheitsprobleme dar?

Die empfohlene Methode zur Implementierung der CORS-Richtlinie besteht darin, den Zugriff nur auf vertrauenswürdige Quellen zu ermöglichen, die über eine Zulassungsliste vertrauenswürdiger Domänen erforderlich sind. Dasselbe gilt für die domänenübergreifende Richtlinie des Flashs. Einige [!DNL Adobe Target] Kunden sind besorgt über die Verwendung von Platzhalterzeichen für Domänen in [!DNL Target]. Wenn ein Benutzer bei einer Anwendung angemeldet ist und eine von der Richtlinie zugelassene Domäne besucht, besteht das Problem darin, dass schädliche Inhalte, die in dieser Domäne ausgeführt werden, potenziell sensible Inhalte aus der Anwendung abrufen und Aktionen im Sicherheitskontext des angemeldeten Benutzers ausführen können. Dies wird häufig als Cross-Site Request Forgery (CSRF) bezeichnet.

In einer [!DNL Adobe Target] Diese Maßnahmen sollten jedoch kein Sicherheitsproblem darstellen.

&quot;adobe.tt.omtrdc.net&quot;ist eine Adobe-eigene Domäne. [!DNL Adobe Target] ist ein Test- und Personalisierungstool, und es wird erwartet, dass [!DNL Target] kann Anfragen von überall empfangen und verarbeiten, ohne dass eine Authentifizierung erforderlich ist. Diese Anforderungen enthalten Schlüssel-Wert-Paare, die für A/B-Tests, Empfehlungen oder die Personalisierung von Inhalten verwendet werden.

[!DNL Adobe] speichert keine personenbezogenen oder anderen sensiblen Informationen über [!DNL Adobe Target] Edge-Server, auf die &quot;adobe.tt.omtrdc.net&quot;verweist.

Es wird erwartet, dass [!DNL Target] über JavaScript-Aufrufe von jeder Domäne aus aufgerufen werden können. Die einzige Möglichkeit, diesen Zugriff zu ermöglichen, besteht darin, &quot;Access-Control-Allow-Origin&quot;mit einem Platzhalter zu verwenden.
