---
keywords: Content Security-Richtlinie;csp;at.js;Whitelist;Zulassungsliste;Flackern;Vorab-Ausblenden;Vorab-Ausblenden;Vorab-Ausblenden
description: Erfahren Sie mehr über die CSP-Anweisungen (Content Security Policy), die Sie bei Verwendung von Adobe Target hinzufügen sollten.
title: Funktionsweise [!DNL Target] Umgang mit Inhaltssicherheitsrichtlinien (Content Security Policies, CSP)?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# Richtlinien zur Content Security Policy (CSP)

Wenn Sie [Inhaltssicherheitsrichtlinie](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) für Ihre [!DNL Adobe Target] -Implementierung sollten Sie bei Verwendung von die folgenden CSP-Anweisungen hinzufügen [at.js 2.1 oder höher](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` mit `*.tt.omtrdc.net` auf die Zulassungsliste gesetzt. Erforderlich, um die Netzwerkanforderung an die [!DNL Target] -Kante.
* `style-src unsafe-inline`. Erforderlich für die Vorab-Ausblendung und die Flackerverhinderung.
* `script-src unsafe-inline`.  Erforderlich, um die Ausführung von JavaScript zu ermöglichen, die Teil eines HTML-Angebots sein kann.
