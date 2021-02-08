---
keywords: Browser;Bedingungen;Voraussetzungen;Internet Explorer;Chrome;Firefox;Safari;Android;Surface
description: Erfahren Sie, welche Internetbrowser Adobe Target für seine Schnittstelle und für Content Versand unterstützt.
title: Welche Browser werden von Zielgruppe unterstützt?
feature: Implementation
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Unterstützte Browser

Die Bereitstellung der [!DNL Adobe Target]-Anwendung und von Inhalten wurde für eine breite Auswahl von Browsern und Geräten geprüft.

Weitere wichtige Informationen zu TLS finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

## [!DNL Target] Standard/Premium-Benutzeroberfläche {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

Die [!DNL Target]-Schnittstelle unterstützt die folgenden Browser und Geräte:

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

Beachten Sie Folgendes:

* Bei [!DNL at.js]-Implementierungen werden in [!DNL Target] in älteren Versionen von Internet Explorer sowie möglicherweise in älteren Versionen der oben aufgeführten Browser Standardinhalte angezeigt. Bei [!DNL mbox.js]-Implementierungen versucht [!DNL Target], die Inhalte zu rendern, möglicherweise jedoch ohne Erfolg.
* Internet Explorer behandelt alle unbekannten Elemente (wie z. B. benutzerdefinierte Elemente) als denselben Elementtyp. Daher funktioniert Versand nicht mit benutzerdefinierten Elementen.
* [!DNL Target]In nicht oben aufgeführten Browsern sowie in Browsern im [Quirks-Modus](https://en.wikipedia.org/wiki/Quirks_mode) zeigt Standardinhalte an. Für at.js ist ein Dokumenttyp erforderlich, der im Standardmodus dargestellt wird, beispielsweise `<!DOCTYPE html>`.
* Um die Sicherheit der Adobe-Bereitstellungsinfrastruktur zu erhöhen, werden Geräte und Browser mit TLS 1.0 nach dem 12. September 2018 nicht mehr unterstützt. Siehe [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451), um die Gesamtauswirkungen dieser Änderung zu verstehen.
