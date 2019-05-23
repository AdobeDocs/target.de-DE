---
description: Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.
keywords: implementieren;implementieren;Implementierung;Adobe Launch;Launch;Race;umleiten
seo-description: Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.
seo-title: Implementieren von Target mit Adobe Launch
title: Implementieren von Target mit Adobe Launch
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: 19834da75f163d6357bc9b986a23f0bc1fea6d8e

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

* **Ermöglicht asynchrone Implementierung von Target:** Weitere Informationen finden Sie unter „Adobe Target-Erweiterung mit asynchroner Implementierung“ in der [Dokumentation der Adobe Target-Erweiterung](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension).
* **Behebt Analytics- und Target-Wettlaufsituationen:** Da der Analytics-Aufruf vor dem Target-Aufruf ausgelöst werden kann, ist der Target-Aufruf nicht an den Analytics-Aufruf gebunden, was zu falschen Daten führen kann. Ab Launch 0.6.0 gewährleistet die Target-Launch-Erweiterung, dass der Analytics-Beacon-Aufruf erst ausgelöst wird, wenn der Target-Aufruf (erfolgreich) abgeschlossen wurde. Hierdurch sollte das Problem uneinheitlicher Daten behoben sein, das bei einigen Kunden auftrat.
* **Verhindert fehlerhafte Verarbeitung von Umleitungsangeboten:** Wenn sowohl Target als auch Analytics auf einer Seite eingesetzt werden und ein Umleitungsangebot von Target ausgeführt wird, kann eine Situation entstehen, in der der Analytics-Tracker fälschlicherweise eine Anfrage auslöst, da der Benutzer an eine andere URL umgeleitet wird. Wenn Sie Target und Analytics über Launch implementieren, tritt dieses Problem nicht auf, da hierdurch Target Analytics anweist, die Analytics-Beacon-Anfrage abzubrechen.

