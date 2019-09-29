---
description: Informationen zu den Richtlinien für Content Security Policy (CSP), die Sie bei Verwendung von Adobe Target "at.js 2.1"oder höher hinzufügen sollten.
keywords: Sicherheitsrichtlinie für Inhalte;csp;at.js;Whitelist;Flicker;Pre-hide;Pre-hide;Prehiding
seo-description: Informationen zu den Richtlinien für Content Security Policy (CSP), die Sie bei Verwendung von Adobe Target "at.js 2.1"oder höher hinzufügen sollten.
seo-title: Content Security-Richtlinien (CSP)
solution: Target
subtopic: Erste Schritte
title: Richtlinien zur Content Security Policy (CSP)
topic: Standard
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Richtlinien zur Content Security Policy (CSP)

Wenn Sie [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre Target-Implementierung verwenden, sollten Sie die folgenden CSP-Anweisungen bei Verwendung von [at.js 2.1 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)hinzufügen:

* `connect-src` mit `*.tt.omtrdc.net` weißer Liste. Erforderlich, um die Netzwerkanforderung an der [!DNL Target] Kante zu ermöglichen.
* `style-src unsafe-inline`. Erforderlich für das Prähnen und Flimmern.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein könnte.
