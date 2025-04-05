---
keywords: Versionshinweise; Auslösungen; Aktualisierungen; zukünftige Version; Verbesserungen; neue Funktionen; Behebt; Aktualisierungen; Prerelease; Frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 0618d39fc5966c64cceea8f5bcccb625fc243ebb
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 38%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Donnerstag, 2. April 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Aktualisierung der Target Berechtigungen (22. April 2025)

Dieses zukünftige Update verbessert die organisatorische Kontrolle über [!DNL Target] Instanz Konfigurationen und verhindert versehentliche Updates, die sich auf Aktivität Sendungen in verschiedenen Test- und Personalisierung Teams auswirken könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Product] [!UICONTROL Solutions] Administratoren die Einstellungen in den [!UICONTROL Administration] Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzer ohne diese Berechtigung erhalten schreibgeschützten Zugriff auf die [!UICONTROL Administration] Abschnitte.

Weitere Informationen finden Sie unter [Verwalten von Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.1 (2. April 2025)

Dieses Release umfasst die folgenden Fehlerbehebungen und Updates:

* Fest ein Problem, das dazu führte, dass Erlebnis Zielgruppen aus den Aktivitäten verschwanden. (TGT-52003)
* Fest ein Problem, das während der Sendungen zu unerwarteten Elementen führte. (TGT-52011)
* Fest ein Problem, das Kunden daran hinderte, die Zielgruppe im Targeting Diagramm auf der Ove[!UICONTROL r]Ansicht Seite und während der Aktivität Bearbeitung anzuzeigen. (TGT-52050)
* Fest ein Problem, das Kunden daran hinderte, Erlebnisse in bestellen von Priorität in [!UICONTROL Experience Targeting] (XT-)Aktivitäten neu zu bestellen. (TGT-52054)
* Fest ein Problem, das beim Rückgängigmachen von Textstiländerungen zu einer falschen Wiedergabe führte. (TGT-51876)
* Fest das Problem, dass beim Ändern einer Redirect Angebot auch alle [!UICONTROL ClickTrack] Selektoren entfernt werden, [!DNL Target] die mit dieser Angebot verknüpft sind. (TGT-51936)
* Fest ein Problem, das dazu führte [!DNL Target] , dass die Selektor beim Abbrechen falsch gespeichert wurde [!UICONTROL ClickTrack]. (TGT-51937)
* Fest ein Problem auf, das einen ungültig Namensfehler auslöste, nachdem die mbox-Auswahl auf der [!UICONTROL Goals & Settings] Seite geöffnet und geschlossen wurde, ohne Änderungen vorzunehmen. (TGT-51983)
* Fest ein Problem auf, das die Bearbeitung von Anzeige in der alten [!DNL Target] UI erstellten blockierte. (TGT-51984)
* Fest ein Problem, das die Bearbeitung von Aktivitäten blockiert hat, die Anzeige-hoc-Angebote mit benutzerdefiniertem Code enthalten. (TGT-51995)
* Fest ein Problem, das dazu führte, dass Ausschlussregeln als Einschlussregeln angezeigt wurden, wenn kombinierte Zielgruppe Definitionen bearbeitet wurden. (TGT-51999)
* Fest ein Problem, das dazu führte, dass benutzerdefinierter Code bei der Bearbeitung von Erlebnis nicht richtig angezeigt wurde. (TGT-52005)
* Fest ein Problem, das dazu führte, dass die [!UICONTROL Insert Before] Option zum Einfügen von Inhalte vor dem Navigation nicht verfügbar war. (TGT-52031)
* Fest ein Problem, das die korrekte Hervorhebung der Standard Erlebnis in Berichte verhinderte. (TGT-51716)
* Fest ein Problem, das beim Erstellen einer Aktivität eine `default message [Invalid optionLocalIds: xx]]` Meldung auslöste. (TGT-52038)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
