---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: e458793e4d0110d97f3f5124cbe6e54520d3f0e9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 57%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 8. März 2023**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 22.15.1 (8. und 9. März 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **8. März**: Amerikanische Region
* **9. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **9. März**: Region Asien-Pazifik (APAC)

Diese Version beinhaltet die folgenden neuen Funktionen und Verbesserungen:

| Funktion | Details |
| --- | --- |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] | [!DNL Target] ermöglicht die Auswahl von Metriken basierend auf binomialen Ereignissen oder Metriken basierend auf kontinuierlichen Ereignissen bei Verwendung von [!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.<P>Beachten Sie die folgende Änderung bei den unterstützten Metriken:<ul><li>[!DNL Target] das vorherige Verhalten für bestehende Aktivitäten bis beibehalten (DATUM ZU BESTIMMEN). Nach diesem Datum werden Aktivitäten, die nicht unterstützte Metriken verwenden, eingestellt, um die vorhandene Aktivitätsmigration zum neuen Verhalten zu erzwingen.</li></ul>Weitere Informationen finden Sie unter [Unterstützte Zielmetriken](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) in *A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting*. |
| [!UICONTROL Automatische Zuordnung] using [!UICONTROL Analytics for Target] (A4T) | Neues Tutorial:<ul><li>[Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Automatische Zuordnung] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Automatisches Targeting] using [!UICONTROL Analytics for Target] (A4T) | Neues Tutorial:<ul><li>[Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Automatisches Targeting] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

## at.js-Version 2.10.2 (7. März 2023)

* Es wurde ein Fehler behoben, der dazu führte, dass die `trackEvent` -Funktion immer einen Fehler zurückgeben.

Informationen zu allen at.js-Versionen finden Sie unter [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |


## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
