---
keywords: content security policy;csp;at.js;whitelist;allowlist;flicker;pre-hide;pre-hiding;prehiding
description: Informationen zu den Richtlinien für Content Security Policy (CSP), die Sie bei Verwendung von Adobe Target at.js 2.1 oder höher hinzufügen sollten.
title: Content Security-Richtlinien (CSP)
feature: Privacy & Security
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# Richtlinien zur Content Security Policy (CSP)

Wenn Sie [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre [!DNL Adobe Target]-Implementierung verwenden, sollten Sie bei Verwendung von [at.js 2.1 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) die folgenden CSP-Anweisungen hinzufügen:

* `connect-src` mit  `*.tt.omtrdc.net` auf die Zulassungsliste gesetzt. Erforderlich, um die Netzwerkanforderung an die [!DNL Target]-Kante zu ermöglichen.
* `style-src unsafe-inline`. Erforderlich für das Prähnen und Flimmern.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein könnte.
