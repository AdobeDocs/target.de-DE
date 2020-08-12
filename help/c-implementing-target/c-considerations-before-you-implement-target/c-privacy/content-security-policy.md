---
keywords: content security policy;csp;at.js;whitelist;allowlist;flicker;pre-hide;pre-hiding;prehiding
description: Informationen zu den Richtlinien für Content Security Policy (CSP), die Sie bei Verwendung von Adobe Target at.js 2.1 oder höher hinzufügen sollten.
title: Content Security-Richtlinien (CSP)
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Richtlinien zur Content Security Policy (CSP)

Wenn Sie [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für die Implementierung der Zielgruppe verwenden, sollten Sie die folgenden CSP-Anweisungen bei Verwendung von [at.js 2.1 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)hinzufügen:

* `connect-src` mit `*.tt.omtrdc.net` auf die Zulassungsliste gesetzt. Erforderlich, um die Netzwerkanforderung an der [!DNL Target] Kante zu ermöglichen.
* `style-src unsafe-inline`. Required for pre-hiding and flicker control.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein könnte.
