---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8f7cdf94438763679273b3631e45b1b41899cda5
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 21%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 18. August 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Die Informationen in diesem Artikel werden häufig aktualisiert, insbesondere vor Versionen.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.8.3 (21. August 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**Recommendations**

+++Details anzeigen
* **Es wurde ein Problem in der Recs-Benutzeroberfläche behoben, bei dem der CSV-Download für benutzerdefinierte Kriterien einen 404-Fehler zurückgab**: Es wurde ein Problem behoben, bei dem Kunden die CSV-Datei für benutzerdefinierte Kriterien beim Erstellen der Aktivität nicht herunterladen konnten. (TGT-51966)
* **Inkonsistentes Laden von Bildern in[!UICONTROL Catalog Search]** behoben: Es wurde ein Problem behoben, bei dem Miniaturansichten und Bilder in [!UICONTROL &#x200B; Catalog Search] beim Erstellen von Aktivitäten nicht konsistent geladen wurden. Bilder werden nur angezeigt, wenn die Spalte „Miniatur-URL“ sichtbar war und einige Produktbilder nach Navigations- oder Suchaktionen teilweise oder überhaupt nicht geladen wurden. (TGT-52778)
* **Es wurde ein Problem behoben, durch das die Bearbeitung einer Empfehlung in einem duplizierten Erlebnis das ursprüngliche Erlebnis beeinträchtigte**: Kundinnen und Kunden berichteten, dass die Änderung einer Empfehlung in einem duplizierten Erlebnis das ursprüngliche Erlebnis unbeabsichtigt veränderte. Insbesondere nach dem Duplizieren von Erlebnis B im Prozess zur Erstellung der Aktivität und dem Bearbeiten des Designs oder der Kriterien wurden dieselben Änderungen im ursprünglichen Erlebnis B widergespiegelt, obwohl es sich um separate Entitäten handelte. (TGT-53369)
* **Es wurde ein Problem behoben, bei dem Änderungen an einem duplizierten Erlebnis das ursprüngliche Erlebnis in einer Aktivität unbeabsichtigt beeinträchtigten:** Kunden berichteten, dass beim Duplizieren eines Erlebnisses innerhalb einer Aktivität und beim Zuweisen einer neuen Zielgruppe alle Änderungen am Design oder an den Kriterien des duplizierten Erlebnisses auch im ursprünglichen Erlebnis widergespiegelt wurden. Dies trat auf, obwohl keine direkten Änderungen an der Originalversion vorgenommen wurden, was die Möglichkeit beeinträchtigte, unabhängige Varianten innerhalb derselben Aktivität zu erstellen. (TGT-53361)
* **Es wurde ein Problem behoben, bei dem der [!UICONTROL Recommendation Catalog] zeitweise nicht in der Lage war, vollständige Produktattributdaten anzuzeigen**: In der aktualisierten [!DNL Recommendations]-Benutzeroberfläche trat ein Problem auf, bei dem bestimmte Produktattribute, wie z. B. Nachricht, nicht konsistent in den Katalogsuchergebnissen angezeigt wurden, obwohl die Daten im Feed vorhanden waren. Aufgrund dieses Problems mussten Kundinnen und Kunden die Sichtbarkeit der Spalten manuell neu konfigurieren, um die fehlenden Werte abzurufen. (TGT-52769)
+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das den Übergang zu [!UICONTROL Targeting] Schritt in AP-Aktivitäten blockierte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden in [!UICONTROL Targeting] (AP)-Aktivitäten nicht zum [!UICONTROL Automated Personalization] Schritt wechseln konnten, es sei denn, zwei Standorte wurden hinzugefügt. Dieses Verhalten unterschied sich vom vorherigen Erlebnis, bei dem ein einzelner Standort mit mehreren Angeboten ausreichend war. Die Anforderung wurde korrigiert, sodass Kundinnen und Kunden weiterhin Einzelspeicherort-Setups als Teil ihrer API-Workflows verwenden können. (TGT-53426)

+++

**[!UICONTROL Workspaces]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem Kundinnen und Kunden, die auf einen einzigen Arbeitsbereich beschränkt waren, Aktivitäten aus anderen Arbeitsbereichen anzeigen konnten**: Kundinnen und Kunden mit Zugriff auf einen Arbeitsbereich konnten unerwartet Aktivitäten in allen Arbeitsbereichen anzeigen, wenn sie [!UICONTROL All Workspaces] im Prozess zur Erstellung einer Aktivität auswählten. Diese Sichtbarkeit birgt das Risiko von unbeabsichtigten Änderungen an Live-Aktivitäten in anderen Arbeitsbereichen, die sich möglicherweise auf die Website-Leistung auswirken. (TGT-53101)
* **Es wurde ein Problem behoben, bei dem eine Kundin oder ein Kunde Aktivitäten aus der [!UICONTROL Default Workspace] anzeigen konnte, ohne Zugriff zu haben:** Eine Kundin oder ein Kunde mit eingeschränktem Zugriff auf den Staging-Arbeitsbereich konnte Aktivitäten aus der [!UICONTROL Default Workspace] über den Prozess zur Erstellung einer Aktivität anzeigen. Dies trat trotz korrekter Backend-Konfiguration und Zugriffsrechten auf. (TGT-53297)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
