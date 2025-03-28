---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: bdc2f76af2a1f1554556d56a983748aa2c9caf2c
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 31%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 25.3.7 (26. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, durch das das Speichern mehrseitiger Aktivitäten blockiert wurde, wenn eine Seite nach Änderungen gelöscht wurde. (TGT-51988)
* Es wurde ein Fehler behoben, der beim Bearbeiten einer Aktivität auftrat: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* Es wurde ein Problem behoben, durch das beim Hinzufügen neuer Änderungen zu einer Aktivität vorhandene Änderungen entfernt wurden. (TGT-51981)
* Es wurde ein Problem behoben, bei dem das Ersetzen einer Zielgruppe durch &quot;[!UICONTROL All visitors]&quot; während der Erstellung oder Bearbeitung einer Aktivität den Fehler „Doppelte Zielgruppen sind nicht zulässig“ verursachte. (TGT-51978)
* Es wurde ein Problem behoben, das beim Speichern einer [!UICONTROL A/B Test]-Aktivität den Fehler „Ungültige Benutzereingabe“ verursachte. (TGT-51976)
* Es wurde ein Problem behoben, durch das berechnete Metriken auf der [!UICONTROL Goals & Settings] nicht korrekt angezeigt wurden. (TGT-51975)
* Es wurde ein Problem behoben, das verhinderte, dass in der [!DNL Analytics]-Konfiguration für die `pageviews` Metrik `companyName` und `reportSuite` vorhanden waren. (TGT-51965)
* Es wurde ein Problem behoben, durch das beim Wechsel zwischen Erlebnissen in einer Aktivität Änderungen entfernt wurden. (TGT-51945)
* Es wurde ein Problem behoben, bei dem beim Entfernen einer Seitenzielgruppe auch [!UICONTROL ClickTrack] Selektoren entfernt wurden. (TGT-51935)
* Es wurde ein Problem behoben, durch das eine Aktivität nach dem Öffnen der [!UICONTROL Overview] nicht bearbeitbar war. (TGT-51931)
* Es wurde ein Problem behoben, das während der Erstellung einer Aktivität zu einem `[Unused optionLocalIds: 0]]`-Fehler führte. (TGT-51920)
* Es wurde ein Problem behoben, bei dem einige Änderungen nach dem Entfernen von Änderungen am Textstil nicht korrekt übersetzt wurden. (TGT-51876)
* Es wurde ein Problem behoben, das verhinderte, dass Zielgruppen in der [!UICONTROL Form-Based Experience Composer] korrekt aktualisiert wurden. (TGT-51845)
* Es wurde ein Problem behoben, bei dem die URL im [!UICONTROL Visual Experience Composer] während der Aktivitätsnavigation nicht korrekt aktualisiert wurde. (TGT-51832)
* Es wurde ein Problem behoben, durch das Angebote trotz korrekter Anzeige beim Erstellen einer Aktivität und Hinzufügen von Angeboten nicht in der [!UICONTROL Offers]-Benutzeroberfläche angezeigt wurden. (TGT-51805)
* Es wurde ein Problem behoben, bei dem einigen Aktivitäten ein Fallback-Bildschirm fehlte, um Standardinhalte anzuzeigen, wenn personalisierte oder zielgerichtete Inhalte nicht bereitgestellt werden konnten. (TGT-51638)
* Es wurde ein Problem behoben, durch das Live-Angebote und bestimmte Ordner nicht korrekt in der [!UICONTROL Offers]-Benutzeroberfläche angezeigt wurden. (TGT-51628)
* Es wurde ein Problem behoben, durch das einige URL-Zeichenfolgen und goURLs nicht korrekt lokalisiert werden konnten. (TGT-35741)
* Es wurde ein Problem behoben, das verhinderte, dass Rollen ([!UICONTROL Approver], [!UICONTROL Editor] und [!UICONTROL Observer]) korrekt in der [!DNL Target]-Benutzeroberfläche lokalisiert wurden. (TGT-29925)

## [!DNL Target Standard/Premium] 25.3.6 (14. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Der Fehler „Ungültige Benutzereingabe“ in [!UICONTROL Visual Experience Composer] (VEC)-Aktivitäten mit aktiviertem [!UICONTROL Click Tracking] wurde behoben, wenn derselbe [!UICONTROL ClickTrack] mehrmals verwendet wird. (TGT-51921)
* Der Fehler „Ungültige Benutzereingabe“ in VEC-Aktivitäten mit freigegebenen Speicherorten (z. B. HEAD-Selektor) und identischen Angeboten wurde behoben. (TGT-51879)
* Es wurde ein Problem behoben, das dazu führte, dass Erlebnisänderungen für alle Zielgruppen freigegeben wurden. (TGT-51815)
* Validierungsfehler beim Erstellen von Aktivitäten aufgrund von Segment-ID-Konflikten wurden behoben. Die Fehler traten auf, als [!DNL Target] vorhandene Aktivitäten mit anonymen Segmenten erkannte. (TGT-51784)
* Es wurde ein Problem behoben, das [!DNL Target] daran hinderte, Aktivitäten mit Ausschlussregeln in einer Zielgruppe zu speichern. (TGT-51581)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Ordner ohne Zugriff auf den Standardarbeitsbereich zu erstellen, zu löschen oder zu verschieben. (TGT-51499)
* Es wurde ein Problem behoben, bei dem GET-Anfragen beim Abrufen [!DNL Analytics] Metrikliste fehlschlugen. (TGT-51106)

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
