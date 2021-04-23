---
keywords: Sicherheitsrichtlinie für Inhalte;csp;at.js;Whitelist;Zulassungsliste;Flicker;Pre-hide;Pre-hide;Prehiding;Prehiding
description: Erfahren Sie mehr über die CSP-Richtlinien (Content Security Policy), die Sie bei Verwendung von Adobe Target hinzufügen sollten.
title: Wie behandelt [!DNL Target] Content Security-Richtlinien (CSP)?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Richtlinien zur Content Security Policy (CSP)

Wenn Sie [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre [!DNL Adobe Target]-Implementierung verwenden, sollten Sie bei Verwendung von [at.js 2.1 oder höher](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) die folgenden CSP-Anweisungen hinzufügen:

* `connect-src` mit  `*.tt.omtrdc.net` auf die Zulassungsliste gesetzt. Erforderlich, um die Netzwerkanforderung an die [!DNL Target]-Kante zu ermöglichen.
* `style-src unsafe-inline`. Erforderlich für das Prähnen und Flimmern.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein könnte.
