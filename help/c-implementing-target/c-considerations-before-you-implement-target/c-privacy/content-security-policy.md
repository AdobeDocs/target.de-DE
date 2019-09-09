---
description: Informationen zu Content Security Policy-Richtlinien (CSP), die Sie bei Verwendung von Adobe Target at. js 2.1 oder höher hinzufügen sollten.
keywords: content security policy; csp; at. js; whitelist; flackern; pre-hide; pre-hide; ausblenden
seo-description: Informationen zu Content Security Policy-Richtlinien (CSP), die Sie bei Verwendung von Adobe Target at. js 2.1 oder höher hinzufügen sollten.
seo-title: Content Security Policies (CSP)
solution: Target
subtopic: Erste Schritte
title: Content Security Policy (CSP)-Anweisungen
topic: Standard
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Content Security Policy (CSP)-Anweisungen

Wenn Sie [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre Target-Implementierung verwenden, sollten Sie bei Verwendung von [at. js 2.1 oder höher die folgenden CSP-Anweisungen hinzufügen](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src``*.tt.omtrdc.net` mit der Positivliste. Erforderlich, damit die Netzwerkanforderung an [!DNL Target] die Kante gesendet werden kann.
* `style-src unsafe-inline`. Erforderlich für das Ausblenden und Flimmern.
* `script-src unsafe-inline`.  Erforderlich, um die javascript-Ausführung zu ermöglichen, die Teil eines HTML-Angebots ist.
