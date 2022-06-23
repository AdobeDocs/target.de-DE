---
keywords: Browser;Bedingungen;Voraussetzungen;Internet Explorer;Chrome;Firefox;Safari;Android;Surface
description: Erfahren Sie mehr über die Adobe der Internetbrowser [!DNL Target] unterstützt für die Benutzeroberfläche und die Inhaltsbereitstellung.
title: Funktionsweise von Browsern [!DNL Target] Support?
feature: Implementation
role: Developer
exl-id: 8a366c79-d944-4d44-be5a-7c4f65385beb
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 44%

---

# Unterstützte Browser

Die Bereitstellung der [!DNL Adobe Target]-Anwendung und von Inhalten wurde für eine breite Auswahl von Browsern und Geräten geprüft.

Weitere wichtige Informationen zu TLS finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/).

## [!DNL Target] Standard/Premium-Benutzeroberfläche {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

Die [!DNL Target] -Schnittstelle unterstützt die folgenden Browser und Geräte:

| Gerätetyp | Browser-Version |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome (neueste Version, neueste Version minus 1)</li><li>Mozilla Firefox (neueste Version, neueste Version minus 1)</li></ul> |
| Mac | <ul><li>Firefox (neueste Version, neueste Version minus 1)</li><li>Chrome (neueste Version, neueste Version minus 1)</li></ul> |

## Inhaltsbereitstellung {#section_1045A946056441268D40025529918D3D}

Die Inhaltsbereitstellung wurde für folgende Browser und Geräte getestet:

| Gerätetyp | Browser-Version |
|--- |--- |
| Windows | <ul><li>Microsoft Internet Explorer 9 und 10. Im Emulationsmodus getestet.<br>**Hinweis**: Die Inhaltsbereitstellung in IE 9 wird in at.js 1.3.0 (und höher) nicht mehr unterstützt. Die Inhaltsbereitstellung in IE 10, 11 und allen älteren Versionen wird in at.js 2.5.0 (und höher) nicht mehr unterstützt.</li><li>Internet Explorer 11 <br>**Hinweis**: Die Inhaltsbereitstellung in IE 10, 11 und allen älteren Versionen wird in at.js 2.5.0 (und höher) nicht mehr unterstützt.</li><li>Microsoft Edge</li><li>Chrome (neueste Version, neueste Version minus 1)</li><li>Firefox (neueste Version, neueste Version minus 1)</li></ul> |
| Mac | <ul><li>Apple Safari (neueste Version)<br>**Hinweis**: Weitere Informationen dazu, wie Safari mit Erst- und Drittanbieter-Cookies umgeht, finden Sie unter [Target-Cookie](https://developer.adobe.com/target/before-implement/privacy/cookie-behavior/).</li><li>Firefox (neueste Version, neueste Version minus 1)</li><li>Chrome (neueste Version, neueste Version minus 1)</li></ul> |
| Mobiltelefon/Tablet | <ul><li>Apple iOS (neueste Version)</li><li>Android-Geräte und -Tablets (Android 4 und neuer)</li><li>Microsoft Surface (Windows 8.1)</li></ul> |

Beachten Sie Folgendes:

* Bei [!DNL at.js]-Implementierungen werden in [!DNL Target] in älteren Versionen von Internet Explorer sowie möglicherweise in älteren Versionen der oben aufgeführten Browser Standardinhalte angezeigt.
* Internet Explorer behandelt alle unbekannten Elemente (z. B. benutzerdefinierte Elemente) als denselben Elementtyp. Daher funktioniert der Versand nicht mit benutzerdefinierten Elementen.
* [!DNL Target]In nicht oben aufgeführten Browsern sowie in Browsern im [Quirks-Modus](https://en.wikipedia.org/wiki/Quirks_mode) zeigt Standardinhalte an. Für at.js ist ein Dokumenttyp erforderlich, der im Standardmodus dargestellt wird, beispielsweise `<!DOCTYPE html>`.
* Um die Sicherheit der Adobe-Bereitstellungsinfrastruktur zu erhöhen, werden Geräte und Browser mit TLS 1.0 nach dem 12. September 2018 nicht mehr unterstützt. Siehe [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/), um die Gesamtauswirkungen dieser Änderung zu verstehen.
