---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5f41bcebce4e103fada006f53cd3ccd297769d0d
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 28%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 25.6.1 (Samstag, 6. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem QA-Links nicht das richtige Erlebnis für die zugehörige Aktivität lieferten. (TGT-52163 und TGT-52790)
* Fehlerkorrektur - Bei QA-Links fehlt jetzt die zugehörige Zielgruppen-ID. (TGT-52722)
* Es wurde ein Problem behoben, um sicherzustellen, dass Erlebnisse nur bereitgestellt werden, wenn die konfigurierten URL-Bedingungen für die Seitenbereitstellung korrekt erfüllt sind. (TGT-52696)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine [!DNL Recommendations] Design-Vorlage zu erstellen. Der Versuch, eine Vorlage zu erstellen, hat den Fehler ausgelöst: „Im Skript sollte mindestens eine Entitätsvariable verwendet werden.“ (TGT-52395)
* Es wurde ein Problem behoben, das das Speichern von [!DNL Recommendations]-Designs mithilfe von Velocity-Arrays verhinderte. Die Fehlermeldung „Es muss mindestens eine Entitätsvariable im Skript verwendet werden“ wurde fälschlicherweise ausgelöst. (TGT-52734)
* Es wurde ein Problem behoben, bei dem Änderungen in der [!UICONTROL Visual Experience Composer] (VEC) nicht zugänglich waren, wenn die Seite für interne Web-Seiten nicht geladen werden konnte. (TGT-52488 UND TGT-52470)
* Es wurde ein Problem behoben, bei dem das [!UICONTROL Modifications]-Bedienfeld bei kleineren Bildschirmgrößen in Visual Experience Composer nicht sichtbar war. (TGT-52470)
* Fehlerkorrektur - Im aktualisierten VEC tritt jetzt kein Fehler mehr auf, bei dem der Wechsel vom [!UICONTROL Browse]- in den [!UICONTROL Design]-Modus zu einem Konsolenfehler führte und weitere Interaktionen verhinderte. (TGT-52532)
* Es wurde ein Problem in Visual Experience Composer behoben, bei dem durch Klicken auf bestimmte Elemente unbeabsichtigt deren Größe erweitert wurde. (TGT-52497)
* Es wurde ein Problem behoben, bei dem bestimmte Seitenelemente nicht geladen oder in Visual Experience Composer nicht erkannt werden konnten, wodurch Interaktionen wie das Auswählen von Schaltflächen oder Bannern verhindert und die genaue Ereignisverfolgung in -Aktivitäten unterbrochen wurde. (TGT-52663)
* Es wurde ein Problem behoben, das verhinderte, dass Kundinnen und Kunden Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten löschen oder entfernen konnten. (TGT-52690)
* Es wurde ein Problem behoben, das zu einem inkonsistenten Verhalten bei der Aktivitätsqualifizierung in mehrseitigen Aktivitäten führte. (TGT-52694)
* Es wurde ein Fehler behoben, der dazu führte, dass auf der Seite [!UICONTROL Overview] der Aktivität eine ungültige URL für die [!UICONTROL Activity Location] angezeigt wurde. (TGT-52695)
* Ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche wurde behoben, das dazu führte, dass für Aktivitätsspeicherorte doppelte Einträge angezeigt wurden. (TGT-52693)
* Es wurde ein Problem behoben, das einen `getAudiencesV3` auslöste und Kunden daran hinderte, Aktivitäten zu bearbeiten oder zu kopieren. (TGT-52709)
* Fehlerkorrektur - Beim Hinzufügen von [!UICONTROL Experience Fragments]- oder HTML-Angeboten zu einer Aktivität tritt jetzt kein Fehler mehr wegen ungültiger Payload auf. (TGT-52779 und TGT-52773)
* Fehlerkorrektur - In der aktualisierten [!DNL Target]-Benutzeroberfläche wird E[!UICONTROL xperience Fragments] aufgrund eines ungültigen Eingabefehlers nicht mehr korrekt angezeigt. (TGT-52701)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Aktivitäten im [!UICONTROL Form-based Experience Composer] aufgrund eines ungültigen Benutzerfehlers zu bearbeiten. (TGT-52470)
* Es wurde ein Lokalisierungsproblem in der koreanischen Sprache behoben, bei dem bei früheren Übersetzungen Zeichen außerhalb der mehrsprachigen Basisebene verwendet wurden. Die aktualisierte Übersetzung verwendet geeignete Zeichen, die die beabsichtigte Bedeutung genau vermitteln. (TGT-52508 und TGT-52509)
* Fehlerkorrektur - Bei der Lokalisierung in Koreanisch tritt bei der Auswahl des Start- und Enddatums für eine Aktivität kein Übersetzungsproblem mehr auf, wenn die Übersetzung für „Datum“ inkonsistent ist. (TGT-52510)

## Einstellen der Target-Benutzeroberflächenversion (23. Mai 2025) {#toggle}

Der Rollout der neuen [!DNL Target]-Benutzeroberfläche wird bis zum 27. **2025**. Ab diesem Zeitpunkt haben alle Kunden Zugriff auf die neueste Version der Benutzeroberfläche.

Ab **22. Juni** wird der Umschalter für die Benutzeroberflächenversion entfernt. Alle Benutzer wechseln dauerhaft zur neuen Benutzeroberfläche, ohne die Möglichkeit, zur vorherigen Version zurückzukehren.

### Wichtige Informationen zum Umschalten der Benutzeroberflächenversion

Wir bieten eine temporäre Funktion, mit der Sie mithilfe einer Umschaltfläche zwischen der aktualisierten [!DNL Target]-Benutzeroberfläche und der Legacy-Version wechseln können. Diese Option ist nur während der letzten Phase des Rollouts der Benutzeroberfläche verfügbar.

![Umschalter für Target-Benutzeroberflächenversion](/help/main/r-release-notes/assets/toggle.png)

Sobald der Rollout abgeschlossen ist, wird der Umschalter entfernt und alle Benutzenden werden am (22. **2025) dauerhaft zur aktualisierten Benutzeroberfläche**. Adobe empfiehlt, vorauszuplanen, da diese Funktion bald auslaufen wird.

### Einschränkungen des Umschalt-Verhaltens der Benutzeroberfläche

* **Sichtbarkeit neuer Aktivitäten**: Aktivitäten, die in der aktualisierten Benutzeroberfläche erstellt wurden, werden nicht angezeigt, wenn Sie zur alten Benutzeroberfläche zurückkehren.
* **Bearbeiten vorhandener Aktivitäten**: Änderungen an vorhandenen Aktivitäten (die ursprünglich in der veralteten Benutzeroberfläche erstellt wurden), während die aktualisierte Benutzeroberfläche verwendet wird, werden auf Ihrer Website veröffentlicht. Diese Aktualisierungen werden jedoch nicht in der alten Benutzeroberfläche angezeigt, wenn Sie zurückwechseln. Nur die letzten Aktualisierungen, die von der alten Benutzeroberfläche vorgenommen wurden, werden dort angezeigt.
* **Konsistenz der Aktivitätsdetails**: Die neuesten Änderungen werden unabhängig von der verwendeten Benutzeroberfläche auf Ihrer Live-Website angezeigt. In der veralteten Benutzeroberfläche werden jedoch nur die neuesten Änderungen angezeigt, die in dieser Version vorgenommen wurden. Dies kann verwirrend sein, wenn die in der aktualisierten Benutzeroberfläche bearbeiteten Aktivitäten anders aussehen als die in der alten Benutzeroberfläche.

### Weitere Informationen zur aktualisierten Benutzeroberfläche

* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für [!UICONTROL Activities], [!UICONTROL Recommendations] und den [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für die [!UICONTROL Offers Library].

* [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md): Bietet einen kurzen Überblick, der Ihnen hilft, sich mit [!DNL Target] vertraut zu machen, und enthält Links für detailliertere Informationen und schrittweise Anweisungen.

* [[!UICONTROL Visual Experience Composer] Änderungen](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der alten und der aktualisierten Version des VEC erläutert.

* [[!UICONTROL Visual Experience Composer] Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): In diesem Artikel werden die aktualisierte VEC-Benutzeroberfläche und ihre Optionen erläutert.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

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
| [Adobe Priority-Produktaktualisierung](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
