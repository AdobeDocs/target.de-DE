---
keywords: Implementieren;Implementierung;Adobe Launch;Start;Race;Umleitung;Experience Platform Launch;Platform Launch;Tags;Adobe Platform
description: Erfahren Sie, wie Sie die [!DNL Adobe Target] at.js-Bibliothek mit [!DNL Adobe Experience Platform], die bevorzugte Methode zur Implementierung [!DNL Target].
title: Wie implementiere ich  [!DNL Target]  mit  [!DNL Adobe Experience Platform]?
feature: Implement Server-side
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 96%

---

# Implementieren von [!DNL Target] mithilfe von [!DNL Adobe Experience Platform]

Tags in [!DNL Adobe Experience Platform] sind die nächste Generation von Tag-Management-Funktionen von [!DNL Adobe]. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] wurde als Suite von Datenerfassungstechnologien in [!DNL Adobe Experience Platform] umbenannt. Dies spiegelt sich in der Produktdokumentation in verschiedenen Änderungen hinsichtlich der verwendeten Begriffe wider. Eine konsolidierte Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de).

In der folgenden Tabelle finden Sie verschiedene Quellen, über die Sie weitere Informationen abrufen können:

| Ressource | Details |
|--- |--- |
| [Hinzufügen von [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html?lang=de#implement-solutions) | Diese Anleitung enthält schrittweise Anweisungen zur Implementierung von [!DNL Target] auf einer Website mit Tags in [!DNL Adobe Experience Platform]. Die Themen umfassen unter anderem das Hinzufügen der at.js-JavaScript-Bibliothek, das Auslösen der globalen Mbox, das Hinzufügen von Parametern und die Integration mit anderen Lösungen. Dieser Artikel ist Teil eines größeren Tutorials, in dem Sie erfahren, wie Sie [!DNL Adobe Experience Platform] und andere [!DNL Adobe Experience Cloud]-Lösungen implementieren. |
| [Schnellstartanleitung](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=de) | Informationen zur Implementierung und Verwaltung der Analyse-, Marketing- und Werbe-Tags, die zur Unterstützung relevanter Kundenerlebnisse erforderlich sind. |
| [Adobe  [!DNL Target] -Erweiterungen – Überblick](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=de) | Informationen zur Implementierung von [!DNL Target] mit [!DNL Adobe Experience Platform]. |

## Vorteile der Implementierung von at.js mit der [!DNL Target]-Erweiterung {#section_48B3F938B6F8491DAF798E0DB54EF304}

Folgende Vorteile erzielen Sie nur, wenn Sie Tags in [!DNL Adobe Experience Platform] für die Implementierung von at.js verwenden. Daher empfiehlt [!DNL Adobe] dringend, Tags in [!DNL Adobe Experience Platform] anstelle einer manuellen Implementierung von at.js zu verwenden.

* **Behebt [!DNL Adobe Analytics] und Wettbewerbssituationen [!DNL Target]:** Da der [!DNL Analytics]-Aufruf vor dem [!DNL Target]-Aufruf ausgelöst werden kann, ist der [!DNL Target]-Aufruf nicht an den [!DNL Analytics]-Aufruf gebunden. Dies kann zu falschen Daten führen. Die Erweiterung [!DNL Target] stellt sicher, dass der Beacon-Aufruf [!DNL Analytics] wartet, bis der Aufruf [!DNL Target] abgeschlossen wurde (egal ob erfolgreich oder nicht). Die Verwendung von Tags in [!DNL Adobe Experience Platform] ist eine Lösung bezüglich der Dateninkonsistenz, die Kunden bei der manuellen Implementierung erleben können.

   >[!NOTE]
   >
   >Verwenden Sie die Aktion [!UICONTROL Beacon senden] in der [!DNL Adobe Analytics]-Erweiterung, damit der Aufruf [!DNL Analytics] auf den Aufruf [!DNL Target] wartet. Wenn Sie `s.t()` oder `s.tl()` direkt mit benutzerdefiniertem Code aufrufen, warten [!DNL Analytics]-Aufrufe nicht, bis [!DNL Target]-Aufrufe abgeschlossen sind.

* **Verhindert fehlerhafte Verarbeitung von Umleitungsangeboten:** Wenn [!DNL Target] und [!DNL Analytics] auf einer Seite eingesetzt werden und ein Umleitungsangebot von [!DNL Target] ausgeführt wird, kann eine Situation entstehen, in der der [!DNL Analytics]-Tracker fälschlicherweise eine Anfrage auslöst (da der Benutzer an eine andere URL umgeleitet wird). Wenn Sie [!DNL Target] und [!DNL Analytics] über Tags in [!DNL Adobe Experience Platform] implementieren, tritt dieses Problem nicht auf. Mithilfe von Tags in [!DNL Adobe Experience Platform] weist [!DNL Target] [!DNL Analytics] an, die [!DNL Analytics]-Beacon-Anforderung abzubrechen.
