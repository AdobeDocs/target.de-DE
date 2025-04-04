---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: ca14a94365e75704622e76ac13aab324fc836e09
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 43%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Donnerstag, 2. April 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.4.1 (2. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der dazu führte, dass Erlebnis-Zielgruppen aus -Aktivitäten verschwanden. (TGT-52003)
* Fehlerkorrektur - Beim Versand treten jetzt keine unerwarteten Elemente mehr auf. (TGT-52011)
* Es wurde ein Problem behoben, durch das Kunden die Anzeige der Zielgruppe im Targeting-Diagramm auf der [!UICONTROL r]-Seite und während der Aktivitätsbearbeitung nicht sehen konnten. (TGT-52050)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Erlebnisse in [!UICONTROL Experience Targeting] (XT)-Aktivitäten nach Priorität neu anzuordnen. (TGT-52054)
* Es wurde ein Problem behoben, das beim Rückgängigmachen von Textstil-Änderungen zu falschem Rendering führte. (TGT-51876)
* Es wurde ein Problem behoben, durch das [!DNL Target] beim Ändern eines Umleitungsangebots auch alle [!UICONTROL ClickTrack] entfernt, die mit diesem Angebot verknüpft sind. (TGT-51936)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Target] beim Abbrechen von [!UICONTROL ClickTrack] die Auswahl fälschlicherweise speicherte. (TGT-51937)
* Es wurde ein Problem behoben, das nach dem Öffnen und Schließen der Mbox-Auswahl auf der [!UICONTROL Goals & Settings] ohne Änderungen zu einem Fehler wegen ungültigem Namen führte. (TGT-51983)
* Es wurde ein Problem behoben, das die Bearbeitung von Ad-hoc-Angeboten blockierte, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. (TGT-51984)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten blockierte, die Ad-hoc-Angebote mit benutzerdefiniertem Code enthielten. (TGT-51995)
* Es wurde ein Problem behoben, das dazu führte, dass Ausschlussregeln beim Bearbeiten kombinierter Zielgruppendefinitionen als Einschlussregeln angezeigt wurden. (TGT-51999)
* Ein Problem wurde behoben, das dazu führte, dass benutzerdefinierter Code während der Erlebnisbearbeitung nicht korrekt angezeigt wurde. (TGT-52005)
* Es wurde ein Problem behoben, durch das die [!UICONTROL Insert Before]-Option zum Einfügen von Inhalten vor der Navigationsleiste nicht mehr verfügbar war. (TGT-52031)
* Fehlerkorrektur - Das Standarderlebnis in Berichten wird jetzt korrekt hervorgehoben. (TGT-51716)
* Es wurde ein Problem behoben, das beim Erstellen einer Aktivität eine `default message [Invalid optionLocalIds: xx]]` auslöste. (TGT-52038)

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
