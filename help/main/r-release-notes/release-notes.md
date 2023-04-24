---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 97%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 23.3.1 (28. bis 30. März 2023)

Diese Version ist gemäß dem folgenden gestaffelten Zeitplan verfügbar:

* **28. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **29. März**: Region Asien-Pazifik (APAC)
* **30. März**: Region Nord- und Südamerika

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
|--- |--- |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]<p>(Veröffentlichungsdatum: 30. März 2023) | [!DNL Target] ermöglicht die Auswahl von Metriken, die auf binomialen Ereignissen basieren, oder Metriken, die auf kontinuierlichen Ereignissen basieren, wenn [!UICONTROL A4T] für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] verwendet wird.<P>Beachten Sie die folgende Änderung bei den unterstützten Metriken:<ul><li>[!DNL Target] behält das vorherige Verhalten für bestehende Aktivitäten bis zum 9. September 2023 bei. Nach diesem Datum werden die Aktivitäten eingestellt, die nicht unterstützte Metriken verwenden, um die Migration vorhandener Aktivitäten auf das neue Verhalten zu erzwingen.</li></ul>Weitere Informationen finden Sie unter „Unterstützte Zielmetriken“ in [A4T-Unterstützung für Aktivitäten der [!UICONTROL automatischen Zuordnung] und des [!UICONTROL automatischen Targetings]](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported).<br>Mit dieser Funktion wurden die folgenden Tutorials aktualisiert:<ul><li>[Einrichten von A4T-Berichten in  [!DNL Analysis Workspace]  für Aktivitäten des Typs [!UICONTROL Automatische Zuordnung]](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=de){target=_blank}</li><li>[Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für Aktivitäten des Typs [!UICONTROL Automatisches Targeting]](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de){target=_blank}</li></ul> |

* Die Synchronisierung von Zielgruppe und Aktivität wurde verbessert, sodass in [!DNL Adobe Experience Platform] und [!DNL Adobe Audience Manager] erstellte Elemente schneller in der Benutzeroberfläche von [!DNL Target] zu finden sind. (TGT-44568)
* Verbesserte Benutzeroberfläche, damit Benutzende die [!UICONTROL Standard-URL] unter [!UICONTROL Verwaltung] > [!UICONTROL Visual Experience Composer] > [!UICONTROL Standard-URL] entfernen können. Durch diese Änderung können Kundinnen und Kunden die Standard-URL wieder in eine leere Zeichenfolge ändern, was nach der Erstkonfiguration bisher nicht möglich war. (TGT-44577)
* Es wurden Einschränkungen entfernt, die Kundinnen und Kunden daran hinderten, vordefinierte Zielgruppen (Zielgruppen mit reservierten Namen) zu bearbeiten oder zu löschen. (TGT-44655)
* Die Option „[!UICONTROL Fertig]“ wurde deaktiviert, die beim Laden von Spinnern in der [!DNL Target]-Benutzeroberfläche beim Erstellen von [kombinierten Zielgruppen](/help/main/c-target/combining-multiple-audiences.md) angezeigt wurde. (TGT-44079)
* Ein Problem mit dem Link [!UICONTROL Sprache] unten auf der Seite [!UICONTROL Zielgruppen] wurde behoben, sodass er korrekt auf die Seite „[!UICONTROL Voreinstellungen für Kontomitteilungen]“ verweist. (TGT-43562)
* Es wurde ein Problem behoben, aufgrund dessen Kundinnen und Kunden nach Auswahl der Option [!UICONTROL Adobe Analytics] unter [!UICONTROL Administration] > [!UICONTROL Berichterstellung] > [!UICONTROL Reporting Cloud-Lösung] manchmal keine [!UICONTROL A/B-Test]-Aktivitäten erstellen konnten. (TGT-44844)
* Es wurde ein Problem behoben, aufgrund dessen Kundinnen und Kunden in einer Aktivität des Typs [!UICONTROL Multivariater Test] mit vielen Erlebnissen das letzte Erlebnis nicht in [!UICONTROL Visual Experience Composer] (VEC) sehen konnten. Der [DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) am Ende des VEC hinderte Kundinnen und Kunden manchmal daran, das letzte Erlebnis anzusehen. (TGT-44578)
* Es wurde ein Fehler behoben, der dazu führte, dass die Durchsuchen-URL im VEC nicht die aktuelle Seite zeigte, die in einer normalen Browser-Sitzung sichtbar wäre, wenn die Seite autorisiert werden muss oder auf andere Seiten weiterleitet. (TGT-44350)
* Es wurde ein Problem behoben, das Kundinnen und Kunden daran hinderte, die Einstellung [!UICONTROL Inkompatible Kriterien filtern] in [!UICONTROL Recommendations] > [!UICONTROL Einstellungen] zu ändern. (TGT-44398)
* Es wurde ein Fehler behoben, der dazu führte, dass POST-Anfragen zur Erstellung von [!DNL Recommendations]-Feeds fehlschlugen, wenn [!UICONTROL Analytics-Klassifizierungen] mit Report Suites mit Punkten im Namen verwendet wurden. (TGT-44598)
* Links in der [!DNL Target]-Benutzeroberfläche wurden aktualisiert, damit sie auf die neue [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) verweisen. (TGT-44459)
* Die Sicherheit wurde verbessert, um Server-seitige Request Forgery-Angriffe (SSRF) in [!DNL Recommendations]-Feeds zu verhindern. (TGT-43769)
* Es wurden in der gesamten [!DNL Target]-Benutzeroberfläche Lokalisierungskorrekturen vorgenommen.

## at.js-Version 2.10.2 (7. März 2023)

* Es wurde ein Fehler behoben, der dazu geführt hatte, dass die Funktion `trackEvent` immer einen Fehler zurückgab.

Informationen zu allen at.js-Versionen finden Sie unter [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.corp.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

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
