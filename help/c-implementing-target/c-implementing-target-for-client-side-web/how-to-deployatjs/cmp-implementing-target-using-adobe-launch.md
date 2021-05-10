---
keywords: Implementierung;Implementierung;Implementierung;adobe-Start;Start;Rennen;Umleiten;Erlebnis-platform launch;platform launch
description: Erfahren Sie, wie Sie die Adobe [!DNL Target] at.js-Bibliothek mit Adobe Experience Platform Launch implementieren, der bevorzugten Methode zur Implementierung von Adobe [!DNL Target].
title: Wie implementiere ich [!DNL Target] mit Adobe Launch?
feature: Serverseitige Implementierung
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
translation-type: tm+mt
source-git-commit: a69737f49a52cde703627f91d4b97609c1796ee6
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 6%

---

# [!DNL Target] mithilfe von [!DNL Adobe Platform Launch] implementieren

[!DNL Adobe Experience Platform Launch] ist die Tag-Management-Plattform der nächsten Generation  [!DNL Adobe] und die bevorzugte Methode zur Implementierung  [!DNL Adobe Target]. [!DNL Platform Launch] bietet Kunden eine einfache Möglichkeit, die Analyse-, Marketing- und Werbetags bereitzustellen und zu verwalten, die zur Nutzung relevanter Kundenerlebnisse erforderlich sind.

## [!DNL Target] mithilfe von [!DNL Platform Launch] {#topic_5234DDAEB0834333BD6BA1B05892FC25} implementieren

In der folgenden Tabelle werden die verschiedenen Quellen Liste, in denen Sie weitere Informationen zu [!DNL Platform Launch] erhalten können:

| Ressource | Details |
|--- |--- |
| [ [!DNL Target] Implementieren mit dem  [!UICONTROL Adobe Target Extension Tutorial]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Dieses Lernprogramm enthält schrittweise Anweisungen zur Implementierung von [!DNL Target] in eine Website mit [!DNL Platform Launch]. Die Themen umfassen unter anderem das Hinzufügen der at.js-JavaScript-Bibliothek, das Auslösen der globalen Mbox, das Hinzufügen von Parametern und die Integration mit anderen Lösungen. Dieser Artikel ist Teil eines umfangreicheren Lernprogramms, das Ihnen zeigt, wie [!DNL Platform Launch] und andere [!DNL Adobe Experience Cloud]-Lösungen implementiert werden. |
| [[!DNL Adobe Platform Launch] Dokumentation](https://experienceleague.adobe.com/docs/launch/using/get-started/quick-start.html#get-started) | Informationen über die Bereitstellung und Verwaltung der Analyse-, Marketing- und Werbetags, die zur Nutzung relevanter Kundenerlebnisse erforderlich sind. |
| [Dokumentation zu  [!DNL Target] AdobeExtension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informationen zur Implementierung von [!DNL Target] mit [!DNL Platform Launch]. |

## Vorteile der Implementierung von at.js mit der [!DNL Target] [!DNL Platform Launch]-Erweiterung {#section_48B3F938B6F8491DAF798E0DB54EF304}

Die folgenden Vorteile gelten nur, wenn Sie [!DNL Platform Launch] verwenden, um at.js zu implementieren. [!DNL Adobe] empfiehlt daher dringend, [!DNL Platform Launch] anstelle einer manuellen Implementierung von at.js zu verwenden.

* **Löst  [!DNL Adobe Analytics] und  [!DNL Target] Racebedingung:** Da der  [!DNL Analytics] Aufruf vor dem  [!DNL Target] Aufruf ausgelöst werden konnte, wird der  [!DNL Target] Aufruf nicht dem  [!DNL Analytics] Aufruf zugeordnet. Diese Sequenzierung kann zu falschen Daten führen. Ab 0.6.0 stellt die Erweiterung [!DNL Platform Launch] sicher, dass der Beacon-Aufruf bis zum Abschluss des [!DNL Target]-Aufrufs erfolgreich oder nicht gewartet wird. [!DNL Analytics] Die Verwendung von [!DNL Platform Launch] löst die Dateninkonsistenz, die Kunden bei der manuellen Implementierung erleben können.
* **Verhindert die fehlerhafte Verarbeitung von Umleitungs-Angeboten:** Wenn Sie  [!DNL Target] auf der Seite sind  [!DNL Analytics] und ein Umleitungs-Angebot ausgeführt wird, kann es vorkommen, dass der  [!DNL Target]  [!DNL Analytics] Tracker eine Anforderung auslöst, wenn dies nicht der Fall ist (weil der Benutzer zu einer anderen URL umgeleitet wird). Wenn Sie [!DNL Target] und [!DNL Analytics] über [!DNL Platform Launch] implementieren, tritt dieses Problem nicht auf. [!DNL Platform Launch] weist [!DNL Target] [!DNL Analytics] an, die [!DNL Analytics]-Beacon-Anforderung abzubrechen.
