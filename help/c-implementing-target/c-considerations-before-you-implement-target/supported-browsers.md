---
keywords: Browsers;Prerequisites;Requirements;internet explorer;chrome;firefox;safari;android;surface
description: Die Bereitstellung der Adobe Target-Anwendung und von Inhalten wurde für eine breite Auswahl von Browsern und Geräten geprüft.
title: Unterstützte Browser
feature: reference general
subtopic: Getting Started
topic: Standard
uuid: 614088da-412c-45e3-9f2d-6985391973be
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 86%

---


# Unterstützte Browser{#supported-browsers}

Die Bereitstellung der [!DNL Adobe Target]-Anwendung und von Inhalten wurde für eine breite Auswahl von Browsern und Geräten geprüft.

Weitere wichtige Informationen zu TLS finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

## [!DNL Target] Standard/Premium-Benutzeroberfläche {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

The [!DNL Target] interface supports the following browsers and devices:

| Gerätetyp | Browser-Version |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome (neueste Version, neueste Version minus 1)</li><li>Mozilla Firefox (neueste Version, neueste Version minus 1)</li></ul> |
| Mac | <ul><li>Firefox (neueste Version, neueste Version minus 1)</li><li>Chrome (neueste Version, neueste Version minus 1)</li></ul> |

## Inhaltsbereitstellung {#section_1045A946056441268D40025529918D3D}

Die Inhaltsbereitstellung wurde für folgende Browser und Geräte getestet:

| Gerätetyp | Browser-Version |
|--- |--- |
| Windows | <ul><li>Internet Explorer 9 und 10. Im Emulationsmodus getestet.<br>**Hinweis:** at.js 1.3.0 (und neuer) unterstützt nun nicht mehr die Inhaltsbereitstellung für Microsoft Internet Explorer 9.</li><li>Internet Explorer 11</li><li>Microsoft Edge</li><li>Chrome (neueste Version, neueste Version minus 1)</li><li>Firefox (neueste Version, neueste Version minus 1)</li></ul> |
| Mac | <ul><li>Apple Safari (neueste Version)<br>**Hinweis:** Weitere Informationen dazu, wie Safari mit Erst- und Drittanbieter-Cookies umgeht, finden Sie unter [Target-Cookie](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md).</li><li>Firefox (neueste Version, neueste Version minus 1)</li><li>Chrome (neueste Version, neueste Version minus 1)</li></ul> |
| Mobiltelefon/Tablet | <ul><li>Apple iOS (neueste Version)</li><li>Android-Geräte und -Tablets (Android 4 und neuer)</li><li>Microsoft Surface (Windows 8.1)</li></ul> |

Note the following:

* Bei [!DNL at.js]-Implementierungen werden in [!DNL Target] in älteren Versionen von Internet Explorer sowie möglicherweise in älteren Versionen der oben aufgeführten Browser Standardinhalte angezeigt. Bei [!DNL mbox.js]-Implementierungen versucht [!DNL Target], die Inhalte zu rendern, möglicherweise jedoch ohne Erfolg.
* Internet Explorer treats all unknown elements (such as custom elements) as the same element type. As a result, delivery will not work with custom elements.
* [!DNL Target]In nicht oben aufgeführten Browsern sowie in Browsern im [Quirks-Modus](https://en.wikipedia.org/wiki/Quirks_mode) zeigt Standardinhalte an. Für at.js ist ein Dokumenttyp erforderlich, der im Standardmodus dargestellt wird, beispielsweise `<!DOCTYPE html>`.
* Um die Sicherheit der Adobe-Bereitstellungsinfrastruktur zu erhöhen, werden Geräte und Browser mit TLS 1.0 nach dem 12. September 2018 nicht mehr unterstützt. Siehe [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451), um die Gesamtauswirkungen dieser Änderung zu verstehen.
