---
keywords: implement;implementing;implementation;adobe launch;launch;race;redirect;experience platform launch
description: Adobe Experience Platform Launch ist die Tag-Management-Plattform der nächsten Generation aus der Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.
title: Implementieren von Target mit Adobe Launch
feature: Implement Server-side
translation-type: tm+mt
source-git-commit: 88f6e4c6ad168e4f9ce69aa6618d8641b466e28a
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 81%

---


# Implementieren von Target mit Adobe Launch

Adobe Experience Platform Launch ist die Tag-Management-Plattform der nächsten Generation aus der Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.

## Implementieren von Target mit Adobe Launch {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.

In der folgenden Tabelle finden Sie verschiedene Quellen, über die Sie weitere Informationen zu Launch abrufen können:

| Ressource | Details |
|--- |--- |
| [Implementierung der Zielgruppe mithilfe des Adobe Target Extension Tutorials](https://experienceleague.adobe.com/docs/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Diese Anleitung enthält schrittweise Anweisungen zur Implementierung von Adobe Target auf einer Website mit Launch. Die Themen umfassen unter anderem das Hinzufügen der at.js-JavaScript-Bibliothek, das Auslösen der globalen Mbox, das Hinzufügen von Parametern und die Integration mit anderen Lösungen. Dieser Artikel ist Teil eines größeren Tutorials, in dem Sie erfahren, wie Sie Adobe Launch sowie die anderen Adobe Experience Cloud-Lösungen implementieren. |
| [Adobe Launch-Dokumentation](https://experienceleague.adobe.com/docs/launch/using/intro/get-started/quick-start.html) | Informationen zur Implementierung und Verwaltung der Analyse-, Marketing- und Werbe-Tags, die zur Unterstützung relevanter Kundenerlebnisse erforderlich sind. |
| [Dokumentation zur Adobe Target Extension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informationen zur Implementierung von Target mit Launch. |

## Vorteile der Implementierung von at.js mit der Zielgruppe Launch Extension {#section_48B3F938B6F8491DAF798E0DB54EF304}

Folgende Vorteile erhalten Sie nur, wenn Sie Adobe Launch für die Implementierung von at.js verwenden. Deshalb empfehlen wir dringend, dass Sie statt DTM oder der manuellen Implementierung von at.js Adobe Launch einsetzen.

* **Behebt Analytics- und Target-Wettlaufsituationen:** Da der Analytics-Aufruf vor dem Target-Aufruf ausgelöst werden kann, ist der Target-Aufruf nicht an den Analytics-Aufruf gebunden. Dies kann zu falschen Daten führen. Ab 0.6.0 gewährleistet die Target-Launch-Erweiterung, dass der Analytics-Beacon-Aufruf erst ausgelöst wird, wenn der Target-Aufruf (erfolgreich) abgeschlossen wurde. Hierdurch sollte das Problem uneinheitlicher Daten behoben sein, das bei einigen Kunden auftrat.
* **Verhindert fehlerhafte Verarbeitung von Umleitungsangeboten:** Wenn Target und Analytics auf einer Seite eingesetzt werden und ein Umleitungsangebot von Target ausgeführt wird, kann eine Situation entstehen, in der der Analytics-Tracker fälschlicherweise eine Anfrage auslöst (da der Benutzer an eine andere URL umgeleitet wird). Wenn Sie Target und Analytics über Launch implementieren, tritt dieses Problem nicht auf. Target weist Analytics mithilfe von Launch an, die Analytics-Beacon-Anforderung abzubrechen.
