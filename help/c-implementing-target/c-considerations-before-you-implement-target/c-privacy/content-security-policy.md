---
keywords: Sicherheitsrichtlinie für Inhalte;csp;at.js;Whitelist;Zulassungsliste;Flicker;Pre-hide;Pre-hide;Prehiding;Prehiding
description: Erfahren Sie mehr über die CSP-Richtlinien (Content Security Policy), die Sie bei Verwendung von Adobe Target hinzufügen sollten.
title: Wie behandelt Zielgruppe Content Security-Richtlinien (CSP)?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Richtlinien zur Content Security Policy (CSP)

Wenn Sie [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre [!DNL Adobe Target]-Implementierung verwenden, sollten Sie bei Verwendung von [at.js 2.1 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) die folgenden CSP-Anweisungen hinzufügen:

* `connect-src` mit  `*.tt.omtrdc.net` auf die Zulassungsliste gesetzt. Erforderlich, um die Netzwerkanforderung an die [!DNL Target]-Kante zu ermöglichen.
* `style-src unsafe-inline`. Erforderlich für das Prähnen und Flimmern.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein könnte.
