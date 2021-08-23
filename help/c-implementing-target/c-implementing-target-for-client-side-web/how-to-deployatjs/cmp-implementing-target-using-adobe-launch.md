---
keywords: implementieren;Implementierung;Implementierung;Adobe Launch;Start;Race;Umleitung;Erlebnis-platform launch;platform launch
description: Erfahren Sie, wie Sie die Adobe [!DNL Target] at.js-Bibliothek mit Adobe Experience Platform Launch implementieren, der bevorzugten Methode zur Implementierung von Adobe [!DNL Target].
title: Wie implementiere ich [!DNL Target] mit Adobe Launch?
feature: Serverseitig implementieren
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: fd7d3900f9e5d1a6c3d13fd2452de8528f8fd248
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 5%

---

# [!DNL Target] mithilfe von [!DNL Adobe Platform Launch] implementieren

[!DNL Adobe Experience Platform Launch] ist die Tag-Management-Plattform der nächsten Generation von  [!DNL Adobe] und ist die bevorzugte Methode zur Implementierung  [!DNL Adobe Target]. [!DNL Platform Launch] bietet Kunden eine einfache Möglichkeit, die Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind.

## [!DNL Target] mithilfe von [!DNL Platform Launch] implementieren {#topic_5234DDAEB0834333BD6BA1B05892FC25}

In der folgenden Tabelle sind die verschiedenen Quellen aufgeführt, aus denen Sie weitere Informationen zu [!DNL Platform Launch] erhalten können:

| Ressource | Details |
|--- |--- |
| [ [!DNL Target] Implementieren mit dem Tutorial zur  [!UICONTROL Adobe Target-Erweiterung]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Dieses Tutorial enthält schrittweise Anweisungen zur Implementierung von [!DNL Target] auf einer Website mit [!DNL Platform Launch]. Die Themen umfassen unter anderem das Hinzufügen der at.js-JavaScript-Bibliothek, das Auslösen der globalen Mbox, das Hinzufügen von Parametern und die Integration mit anderen Lösungen. Dieser Artikel ist Teil eines größeren Tutorials, in dem Sie erfahren, wie Sie [!DNL Platform Launch] und andere [!DNL Adobe Experience Cloud]-Lösungen implementieren. |
| [Schnellstartanleitung für Tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | Informationen zur Bereitstellung und Verwaltung der Analyse-, Marketing- und Werbe-Tags, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind. |
| [ [!DNL Target] Dokumentation zu AdobeExtension](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | Informationen zur Implementierung von [!DNL Target] mit [!DNL Platform Launch]. |

## Vorteile der Implementierung von at.js mithilfe der [!DNL Target] [!DNL Platform Launch]-Erweiterung {#section_48B3F938B6F8491DAF798E0DB54EF304}

Die folgenden Vorteile gelten nur, wenn Sie [!DNL Platform Launch] zur Implementierung von at.js verwenden. Daher empfiehlt [!DNL Adobe] dringend, [!DNL Platform Launch] anstelle einer manuellen Implementierung von at.js zu verwenden.

* **Löst  [!DNL Adobe Analytics] und  [!DNL Target] Wettlaufsituation:** Da der  [!DNL Analytics] Aufruf vor dem  [!DNL Target] Aufruf ausgelöst werden konnte, wird der  [!DNL Target] Aufruf nicht an den  [!DNL Analytics] Aufruf zugeordnet. Diese Sequenzierung kann zu falschen Daten führen. Ab 0.6.0 stellt die Erweiterung [!DNL Platform Launch] sicher, dass der Beacon-Aufruf [!DNL Analytics] wartet, bis der Aufruf [!DNL Target] erfolgreich abgeschlossen wurde oder nicht. Die Verwendung von [!DNL Platform Launch] löst die Dateninkonsistenz, die Kunden bei der manuellen Implementierung erleben können.
* **Verhindert fehlerhafte Verarbeitung von Umleitungsangeboten:** Wenn Sie über  [!DNL Target] und  [!DNL Analytics] auf der Seite verfügen und ein Umleitungsangebot von ausgeführt wird, kann  [!DNL Target]es zu einer Situation kommen, in der der  [!DNL Analytics] Tracker eine Anforderung auslöst, wenn dies nicht der Fall ist (da der Benutzer an eine andere URL umgeleitet wird). Wenn Sie [!DNL Target] und [!DNL Analytics] über [!DNL Platform Launch] implementieren, tritt dieses Problem nicht auf. Mit [!DNL Platform Launch] weist [!DNL Target] [!DNL Analytics] an, die [!DNL Analytics]-Beacon-Anfrage abzubrechen.
