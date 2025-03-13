---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 729b88c3db9e88a5cd428587e34614c5d56542da
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 45%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

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

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md) | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind. |
| [Versionshinweise für vorherige Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Sehen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium an. |
| [Versionshinweise zu Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de){target=_blank} | Sehen Sie sich die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an. |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| [Vorrangiges Produkt-Update von Adobe](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
