---
description: Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.
keywords: implementieren;implementieren;Implementierung;Adobe Launch;Launch;Race;umleiten
seo-description: Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.
seo-title: Implementieren von Target mit Adobe Launch
title: Implementieren von Target mit Adobe Launch
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Implementieren von Target mit Adobe Launch{#implement-target-using-adobe-launch}

Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.

## Implementieren von Target mit Adobe Launch {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.

In der folgenden Tabelle finden Sie verschiedene Quellen, über die Sie weitere Informationen zu Launch abrufen können:

| Ressource | Details |
|--- |--- |
| [Implementieren von Target mit dem Adobe Target Extension Tutorial](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Diese Anleitung enthält schrittweise Anweisungen zur Implementierung von Adobe Target auf einer Website mit Launch. Die Themen umfassen unter anderem das Hinzufügen der at.js-JavaScript-Bibliothek, das Auslösen der globalen Mbox, das Hinzufügen von Parametern und die Integration mit anderen Lösungen. Dieser Artikel ist Teil eines größeren Tutorials, in dem Sie erfahren, wie Sie Adobe Launch sowie die anderen Adobe Experience Cloud-Lösungen implementieren. |
| [Adobe Launch-Dokumentation](https://docs.adobelaunch.com/getting-started) | Informationen zur Implementierung und Verwaltung der Analyse-, Marketing- und Werbe-Tags, die zur Unterstützung relevanter Kundenerlebnisse erforderlich sind. |
| [Dokumentation zu Adobe Target Extension](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension) | Informationen zur Implementierung von Target mit Launch. |

## Vorteile der Implementierung von at.js mit der Target-Launch-Erweiterung {#section_48B3F938B6F8491DAF798E0DB54EF304}

Folgende Vorteile erhalten Sie nur, wenn Sie Adobe Launch für die Implementierung von at.js verwenden. Deshalb empfehlen wir dringend, dass Sie statt DTM oder der manuellen Implementierung von at.js Adobe Launch einsetzen.

* **Solves Analytics and Target Race Condition:** Da der Analytics-Aufruf vor dem Target-Aufruf ausgelöst werden konnte, wird der Target-Aufruf nicht an den Analytics-Aufruf gesendet. Dies kann zu falschen Daten führen. Ab 0.6.0 stellt die Target-Starterweiterung sicher, dass der Analytics-Beacon-Aufruf wartet, bis der Target-Aufruf abgeschlossen ist, erfolgreich oder nicht. Hierdurch sollte das Problem uneinheitlicher Daten behoben sein, das bei einigen Kunden auftrat.
* **Verhindert fehlerhafte Umleitungsangebote:** Wenn Sie über Target und Analytics auf der Seite verfügen und ein Umleitungsangebot von Target ausgeführt wird, kann es vorkommen, dass der Analytics-Tracker eine Anforderung auslöst, wenn dies nicht der Fall ist (da der Benutzer zu einer anderen URL weitergeleitet wird). Wenn Sie Target und Analytics über Launch implementieren, wird dieses Problem nicht auftreten. Mit dem Start wird Analytics angewiesen, die Analytics-Beacon-Anforderung abzubrechen.