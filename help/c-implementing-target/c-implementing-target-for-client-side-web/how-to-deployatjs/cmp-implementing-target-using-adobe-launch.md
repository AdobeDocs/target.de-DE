---
keywords: implementieren;Implementierung;Implementierung;Adobe Launch;Start;Race;Umleitung;Erlebnis-platform launch;platform launch;Tags;Adobe-Plattform
description: Erfahren Sie, wie Sie die Bibliothek [!DNL Adobe Target] at.js mit  [!DNL Adobe Experience Platform], the preferred method to implement [!DNL Target] implementieren.
title: Wie implementiere ich [!DNL Target] mit [!DNL Adobe Experience Platform]?
feature: Implement Server-side
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 11%

---

# Implementieren von[!DNL Target]mithilfe von [!DNL Adobe Experience Platform]

Tags in [!DNL Adobe Experience Platform] sind die nächste Generation von Tag-Management-Funktionen von [!DNL Adobe]. Mit Tags können Kunden die Analyse-, Marketing- und Werbe-Tags bereitstellen und verwalten, die für relevante Kundenerlebnisse erforderlich sind.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] wurde als Suite von Datenerfassungstechnologien in [!DNL Adobe Experience Platform] umbenannt. Dies spiegelt sich in der Produktdokumentation in verschiedenen Änderungen hinsichtlich der verwendeten Begriffe wider. Eine konsolidierte Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) .

In der folgenden Tabelle sind die verschiedenen Quellen aufgeführt, aus denen Sie weitere Informationen erhalten können:

| Ressource | Details |
|--- |--- |
| [Hinzufügen von  [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Dieses Tutorial enthält schrittweise Anweisungen zur Implementierung von [!DNL Target] auf einer Website mit Tags in [!DNL Adobe Experience Platform]. Die Themen umfassen unter anderem das Hinzufügen der at.js-JavaScript-Bibliothek, das Auslösen der globalen Mbox, das Hinzufügen von Parametern und die Integration mit anderen Lösungen. Dieser Artikel ist Teil eines größeren Tutorials, in dem Sie erfahren, wie Sie [!DNL Adobe Experience Platform] und andere [!DNL Adobe Experience Cloud]-Lösungen implementieren. |
| [Schnellstartanleitung](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | Informationen zur Bereitstellung und Verwaltung der Analyse-, Marketing- und Werbe-Tags, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind. |
| [ [!DNL Target] Übersicht über die Adobe-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | Informationen zur Implementierung von [!DNL Target] mit [!DNL Adobe Experience Platform]. |

## Vorteile der Implementierung von at.js mithilfe der [!DNL Target]-Erweiterung {#section_48B3F938B6F8491DAF798E0DB54EF304}

Die folgenden Vorteile gelten nur, wenn Sie Tags in [!DNL Adobe Experience Platform] verwenden, um at.js zu implementieren. Daher empfiehlt [!DNL Adobe] dringend, Tags in [!DNL Adobe Experience Platform] anstelle einer manuellen Implementierung von at.js zu verwenden.

* **Löst  [!DNL Adobe Analytics] und  [!DNL Target] Wettlaufsituation:** Da der  [!DNL Analytics] Aufruf vor dem  [!DNL Target] Aufruf ausgelöst werden konnte, wird der  [!DNL Target] Aufruf nicht an den  [!DNL Analytics] Aufruf zugeordnet. Diese Sequenzierung kann zu falschen Daten führen. Die Erweiterung [!DNL Target] stellt sicher, dass der Beacon-Aufruf [!DNL Analytics] wartet, bis der Aufruf [!DNL Target] erfolgreich abgeschlossen wurde oder nicht. Die Verwendung von Tags in [!DNL Adobe Experience Platform] löst die Dateninkonsistenz, die Kunden bei der manuellen Implementierung erleben können.

   >[!NOTE]
   >
   >Verwenden Sie die Aktion [!UICONTROL Beacon] in der Erweiterung [!DNL Adobe Analytics] senden , damit der Aufruf [!DNL Analytics] auf den Aufruf [!DNL Target] wartet. Wenn Sie `s.t()` oder `s.tl()` direkt mit benutzerdefiniertem Code aufrufen, warten [!DNL Analytics]-Aufrufe erst nach Abschluss der Aufrufe von [!DNL Target].

* **Verhindert fehlerhafte Verarbeitung von Umleitungsangeboten:** Wenn Sie über  [!DNL Target] und  [!DNL Analytics] auf der Seite verfügen und ein Umleitungsangebot von ausgeführt wird, kann  [!DNL Target]es zu einer Situation kommen, in der der  [!DNL Analytics] Tracker eine Anforderung auslöst, wenn dies nicht der Fall ist (da der Benutzer an eine andere URL umgeleitet wird). Wenn Sie [!DNL Target] und [!DNL Analytics] über Tags in [!DNL Adobe Experience Platform] implementieren, tritt dieses Problem nicht auf. Mithilfe von Tags in [!DNL Adobe Experience Platform] weist [!DNL Target] [!DNL Analytics] an, die [!DNL Analytics]-Beacon-Anforderung abzubrechen.
