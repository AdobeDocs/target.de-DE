---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 362fac25f04028dff0fb0233d418ef9ce88e53d6
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 56%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 4. September 2023**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 23.9.1 (6. bis 11. September 2023)

Diese Version ist gemäß dem folgenden gestaffelten Zeitplan verfügbar:

* **6. September**: Amerikanische Region
* **7. September**: Region Europa, Naher Osten und Afrika (EMEA)
* **11. September**: Region Asien-Pazifik (APAC)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde ein Problem behoben, das zu inkonsistenten Berichtsdaten in der [!DNL Target] Benutzeroberfläche und [!DNL Adobe Analytics] Benutzeroberfläche für [!UICONTROL Automatische Zuordnung] Aktivitäten, die [!UICONTROL Analytics for Target] (A4T) als Berichtsquelle verwenden. (TGT-46112)
* Der Timeout für PUT-Aufrufe an die Target-Bereitstellungs-API wurde auf 15 Sekunden erhöht, um Timeout-Fehler zu vermeiden. (TGT-46091)
* Fehlerkorrektur - Beim Wechsel zwischen den [!UICONTROL Tabellenansicht] und [!UICONTROL Automatisierte Segmente] und [!UICONTROL Wichtige Attribute] Berichte. (TGT-46040)
* Der [!UICONTROL Visual Experience Composer] (VEC) zur Unterstützung von BlitzDOM (Webkomponenten). (TGT-45422)
* Es wurde ein Fehler behoben, der dazu führte, dass VEC-Aktionen in der falschen Reihenfolge angewendet wurden. In einigen Fällen führte der VEC asynchron einige Änderungen durch und das Hinzufügen zusätzlicher Änderungen an einem Element verursachte Fehler, wenn dieses Element nach einem [!UICONTROL Einfügen] Aktion. (TGT-45983)
* Es wurde die Möglichkeit hinzugefügt, einen CSS-Selektor im VEC anzugeben. (TGT-45958 und TGT-46017)
* Es wurde ein Fehler behoben, der dazu führte, dass beim Öffnen einer Einzelseiten-App (SPA)-Seite im VEC und anschließendem Wechseln in den Durchsuchen-Modus die Pfeile &quot;Zurück&quot;und &quot;Weiter&quot;nicht ordnungsgemäß funktionierten. (TGT-45956)
* Es wurde ein Problem behoben, das verhindert hat, dass die URL beim Durchsuchen einer SPA Website (Single Page Application) durchgängig aktualisiert wurde. (TGT-45417)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
