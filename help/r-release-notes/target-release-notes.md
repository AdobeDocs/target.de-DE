---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 3fb58864e265653b48e851c8dff404589bb867a6
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 51%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am: 25. Oktober 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.10.5 (28. Oktober 2021)

Dieses Maintenance Release umfasst die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Hinzugefügte Unterstützung für [Webkomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Personalisierte Erlebnisse und Angebote können mit benutzerdefinierten Elementen und Elementen in benutzerdefinierten Elementen erstellt und getestet werden.<br>Diese Version fällt mit der Veröffentlichung von at.js Version 2.7.0 zusammen. |

## [!DNL Target Standard/Premium] 21.10.4 (21. Oktober 2021)

Dieses Maintenance Release umfasst die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| Warenkorbbasierte Recommendations | Eine neue Reihe von Algorithmen wurde hinzugefügt, um Empfehlungen basierend auf dem Inhalt des Warenkorbs des Besuchers bereitzustellen.<br>Weitere Informationen finden Sie unter &quot;Warenkorb-basiert&quot;in [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) und &quot;Warenkorb fügt/Warenkorbansichten/Checkout-Seiten hinzu&quot;und &quot;Artikel, die sich bereits im Warenkorb des Besuchers befinden, ausschließen&quot;in [Planen und Implementieren von Recommendations](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19. Oktober 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen:

* Es wurden Probleme behoben, durch die Kunden die [!UICONTROL A4T] Bedienfeld in [!DNL Analysis Workspace] durch Klicken auf [!UICONTROL In Analytics anzeigen] Schaltfläche in [!DNL Target] Aktivitätsberichte. (TGT-42099, TGT-42100)
* Es wurde ein Fehler behoben, der dazu führte, dass die [!UICONTROL Design bearbeiten] Schaltfläche wird beim Bearbeiten nicht angezeigt [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten, die die [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* Es wurde ein Problem behoben, durch das die [!UICONTROL Kompatibel] bei der Erstellung eines neuen [!UICONTROL Recommendations] Aktivität. (TGT-42053)
* Fehlerkorrektur - die Fehlermeldung wird nun auch dann korrekt angezeigt, wenn die Option [!DNL Analytics] als Berichtsquelle (A4T), da [!DNL Analytics] Berechtigungen. (TGT-41954)
* Mehrere Fehlerbehebungen zur Barrierefreiheit wurden implementiert, um die Tastaturnavigation über das [!DNL Target] Benutzeroberfläche.

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
