---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 65bc050a189b65af57b1258afeff497a0dafcfb5
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 44%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 21. August 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Die Informationen in diesem Artikel werden häufig aktualisiert, insbesondere vor Versionen.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.8.4 (28. August 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!DNL Recommendations]**

+++Details anzeigen
**Die Benutzeroberfläche wurde aktualisiert, sodass bei der erweiterten Suchfilterung in [!UICONTROL Product Catalog Search] nicht zwischen Groß- und Kleinschreibung unterschieden wird**: Die [!UICONTROL Advanced Search] Benutzeroberfläche auf der [!UICONTROL Product Catalog Search] führte zuvor eine exakte Groß-/Kleinschreibung für die zurückgegebenen Werte durch, obwohl sowohl die Backend- als auch die GraphQL-Abfrage nicht zwischen Groß-/Kleinschreibung unterschieden. Diese Inkonsistenz verursachte Verwirrung und verringerte die Suchgenauigkeit. Beim Filtern der [!UICONTROL Advanced Search] wird jetzt nicht mehr zwischen Groß- und Kleinschreibung unterschieden, sondern das Verhalten wird an das Backend angepasst und die Benutzerfreundlichkeit verbessert.

+++

**[!UICONTROL Visual Experience Composer (VEC)]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem die Umbenennung eines Speicherorts in einer [!UICONTROL Automated Personalization] (AP)- oder [!UICONTROL Multivariate Test] (MVT)-Aktivität nach der Navigation zum [!UICONTROL Targeting] Schritt und der Rückkehr nicht beibehalten wurde.** Kunden können jetzt Standortnamen erfolgreich bearbeiten und speichern, und die Änderungen bleiben während des gesamten Erstellungsprozesses der Aktivität sichtbar. (TGT-52367)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
