---
keywords: implement;at.js;javascript library
description: Informationen zur Implementierung der Adobe Target-JavaScript-Bibliothek at.js mithilfe von Adobe Launch, ohne Tag-Manager oder mithilfe des Dynamic Tag Management (DTM) von Adobe.
title: Implementieren von „at.js“
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 57%

---


# Implementieren von „at.js“{#how-to-deploy-at-js}

Informationen zur Implementierung der Adobe Target-JavaScript-Bibliothek at.js mithilfe von Adobe Launch, ohne Tag-Manager oder mithilfe des Dynamic Tag Management (DTM) von Adobe..

Sie können at.js mithilfe der folgenden Methoden bereitstellen:

* **[Implementieren von Target mithilfe von Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**: Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.
* **[Implementieren von Target ohne einen Tag-Manager](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: Sie können Target ohne Verwendung eines Tag-Managers (Adobe Launch oder Dynamic Tag Management) implementieren.
* **[Zielgruppe mithilfe des dynamischen Tag-Managements](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md)** implementieren: Sie können Zielgruppen mithilfe der Adobe Dynamisches Tag-Management (DTM), des alten Tag-Managers der Adobe, implementieren. Adobe Launch ist die bevorzugte und aktuelle Methode zur Implementierung von Target und der „at.js“-Bibliothek. Verwenden Sie für alle neuen Target-Implementierungen Launch.
* **Implementieren Sie die Zielgruppe mit einem Drittanbieter-Tag-Manager**: [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) ist die bevorzugte Methode zur Implementierung der Zielgruppe. Sie können die Zielgruppe jedoch auch mit einem Drittanbieter-Tag-Manager implementieren, z. B. Tealium, Ensighten, Google Tag usw. Eine Liste der Vorteile der Verwendung von Launch finden Sie unter [Vorteile der Implementierung von at.js mit der Zielgruppe Launch Extension](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304).

   Wenn Sie jedoch wissen, wie Zielgruppen ohne Tag-Manager implementiert werden können, können Sie diese problemlos mit einem Drittanbieter-Tag-Manager implementieren, anstatt at.js im Site-Code fest zu kodieren.

   Im Folgenden finden Sie zwei wichtige Themen, die Ihnen bei der Implementierung der Zielgruppe mit einem Drittanbieter-Tag-Manager helfen:

   * [Vor der Implementierung](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [Implementieren von Target ohne einen Tag-Manager](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   Überprüfen Sie unbedingt die Dokumentation für Ihren Tag-Manager von Drittanbietern, um weitere Informationen zu erhalten.

Informationen zur Implementierung von Target bei Verwendung von Einzelseiten-Apps (SPAs) finden Sie unter [Implementierung von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).