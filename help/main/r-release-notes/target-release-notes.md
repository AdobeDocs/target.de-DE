---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: a9c4264672b44da815c721c08c735a2692b2cb33
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 34%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Mittwoch, 11. März 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.3.5 (11. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, durch das Benutzer keine Angebote im [!UICONTROL Modifications] ändern konnten. (TGT-51800)
* Es wurde ein Problem behoben, bei dem Aktionen im linken Bereich für Erlebnisse und Zielgruppen falsch angezeigt wurden, einschließlich im [!UICONTROL ClickTrack]. (TGT-51895)
* Es wurde ein Problem behoben, bei dem [!UICONTROL ClickTrack] -Selektoren nicht auf die richtige Zielgruppenseite angewendet wurden. (TGT-51871)

## [!DNL Target Standard/Premium] 25.3.4 (7. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem Zielgruppen, die nur für Aktivitäten bestimmt waren, im [!UICONTROL Audiences] nicht sichtbar waren, sodass sie nicht bearbeitet oder wiederverwendet werden konnten. (TGT-51860)
* Es wurde ein Problem behoben, das [!DNL Target Standard] Kunden daran hinderte, Aktivitäten mithilfe der Berichterstellung von [!UICONTROL Analytics for Target] (A4T) zu erstellen. (TGT-51854)
* Es wurde ein Problem behoben, durch das lokale ID-Zähler während Batch-Erstellungs- und -Bearbeitungsvorgängen von der Payload ausgeschlossen wurden. (TGT-51867)

## [!DNL Target Standard/Premium] 25.3.2 (6. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Fehlerkorrektur - Beim Kopieren einer Aktivität mit einer Zielgruppe auf Basis einer reinen Aktivität wird jetzt keine neue Aktivität mehr erstellt, sondern stattdessen die Zielgruppe der ursprünglichen Aktivität verwendet. (TGT-51855)
* Es wurde ein Problem behoben, das die Bearbeitung von [!UICONTROL Experience Targeting] (XT)-Aktivitäten mit Zielgruppen, die nur für Aktivitäten bestimmt sind, verhinderte. (TGT-51846)
* Es wurde ein Problem behoben, bei dem der [!UICONTROL Visual Experience Composer] (VEC) Änderungen an einem Erlebnis beim ersten Bearbeiten nicht korrekt anwandte. (TGT-51843)
* Es wurde ein Problem behoben, das beim Klicken auf bestimmte Elemente in VEC einen „ID“-Fehler auslöste. (TGT-51814)
* Die Fehlerbehandlung in VEC während der Aktivitätserstellung wurde aktualisiert. (TGT-51759)
* Fehlerkorrektur - Beim Speichern der Aktivität tritt jetzt kein Fehler mehr auf, wenn die Ansicht &quot;[!UICONTROL Modifications]&quot; im Bedienfeld „Ungültige Benutzereingabe“ fehlt. (TGT-51827)
* Es wurde ein Problem behoben, das die Erstellung von Recommendations-Kriterien verhinderte. (TGT-51834)
* Es wurde eine Bestätigungsnachricht vor der Weiterleitung an eine andere URL hinzugefügt. (TGT-51703)
* Es wurden Probleme mit GraphQL-Integrationstests in Angeboten und Ordnern behoben. (TGT-51839)

## [!DNL Target Standard/Premium] 25.3.1 (3. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Eine kombinierte Zielgruppe kann Untergruppen enthalten, von denen jede mehrere Zielgruppen enthält. In dieser Version wurde ein Problem behoben, das die Anzeige von Untergruppen-Zielgruppen im [!UICONTROL Rules] verhinderte. (TGT-51813)
* Es wurde ein Problem behoben, bei dem beim Öffnen älterer Aktivitäten einige Erlebnis-Zielgruppen durch [!UICONTROL All Visitors] ersetzt wurden. (TGT-51812)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten mit Audiences, die nur für Aktivitäten bestimmt sind, verhinderte. (TGT-51807)
* Es wurde ein Problem behoben, durch das die Bearbeitung von Änderungen am Seitenkopf in der aktualisierten [!DNL Target]-Benutzeroberfläche verhindert wurde. (TGT-51797)
* Es wurde ein Null-Fehler behoben, der beim Duplizieren eines Erlebnisses, beim Löschen eines anderen Erlebnisses und beim anschließenden Versuch, die Aktivität zu speichern, auftrat. (TGT-51796)
* Es wurde ein Problem behoben, das verhinderte, dass Regeln zum Ausschluss von Zielgruppen im Informationsbereich der Zielgruppe während des [!UICONTROL Targeting] Schritts zum Erstellen von Aktivitäten angezeigt wurden. (TGT-51579)
* Aktualisierte Fehlermeldungen, die auf Koreanisch lokalisiert sind. (TGT-51701 und TGT-51699)

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
