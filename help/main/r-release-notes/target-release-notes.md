---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 1f8fa78c2b88e179f021128a8fd3dac177dfa3dd
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 37%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 15. August 2025**

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
* **Es wurde ein Problem in der Recs-Benutzeroberfläche behoben, bei dem der CSV-Download für benutzerdefinierte Kriterien einen 404-Fehler zurückgab**: Es wurde ein Problem behoben, bei dem Kunden die CSV-Datei für benutzerdefinierte Kriterien beim Erstellen der Aktivität nicht herunterladen konnten.
* **Inkonsistentes Laden von Bildern in[!UICONTROL Catalog Search]** behoben: Es wurde ein Problem behoben, bei dem Miniaturansichten und Bilder in [!UICONTROL  Catalog Search] beim Erstellen von Aktivitäten nicht konsistent geladen wurden. Bilder werden nur angezeigt, wenn die Spalte „Miniatur-URL“ sichtbar war und einige Produktbilder nach Navigations- oder Suchaktionen teilweise oder überhaupt nicht geladen wurden. (TGT-52778)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Details anzeigen
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das den Übergang zu [!UICONTROL Targeting] Schritt in AP-Aktivitäten blockierte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden in [!UICONTROL Targeting] (AP)-Aktivitäten nicht zum [!UICONTROL Automated Personalization] Schritt wechseln konnten, es sei denn, zwei Standorte wurden hinzugefügt. Dieses Verhalten unterschied sich vom vorherigen Erlebnis, bei dem ein einzelner Standort mit mehreren Angeboten ausreichend war. Die Anforderung wurde korrigiert, sodass Kundinnen und Kunden weiterhin Einzelspeicherort-Setups als Teil ihrer API-Workflows verwenden können. (TGT-53426)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
