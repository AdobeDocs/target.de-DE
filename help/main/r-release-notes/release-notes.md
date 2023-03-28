---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: a29a52c38e80781697a9925bc1dd88bf9d99ebe1
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 60%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 23.3.1 (28.-30. März 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **28. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **29. März**: Region Asien-Pazifik (APAC)
* **30. März**: Region Nord- und Südamerika

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
|--- |--- |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]<p>(Veröffentlichungsdatum: 30. März 2023) | [!DNL Target] ermöglicht die Auswahl von Metriken, die auf binomialen Ereignissen basieren, oder Metriken, die auf kontinuierlichen Ereignissen basieren, wenn [!UICONTROL A4T] für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] verwendet wird.<P>Beachten Sie die folgende Änderung bei den unterstützten Metriken:<ul><li>[!DNL Target] behält das vorherige Verhalten für bestehende Aktivitäten bis zum 9. September 2023 bei. Nach diesem Datum werden die Aktivitäten eingestellt, die nicht unterstützte Metriken verwenden, um die Migration vorhandener Aktivitäten auf das neue Verhalten zu erzwingen.</li></ul>Im Zusammenhang mit dieser Funktion wurden die folgenden Tutorials aktualisiert:<ul><li>[Einrichten von A4T-Berichten in  [!DNL Analysis Workspace]  für Aktivitäten des Typs [!UICONTROL Automatische Zuordnung]](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=de){target=_blank}</li><li>[Einrichten von A4T-Berichten in  [!DNL Analysis Workspace]  für Aktivitäten des Typs [!UICONTROL Automatisches Targeting]](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de){target=_blank}</li></ul> |

* Die Synchronisierung von Zielgruppe und Aktivität wurde verbessert, sodass in erstellte Elemente [!DNL Adobe Experience Platform] und [!DNL Adobe Audience Manager] finden Sie im Abschnitt [!DNL Target] Schnellere Benutzeroberfläche. (TGT-44568)
* Änderung vorgenommen, um Benutzern zu ermöglichen, die [!UICONTROL Standard-URL] under [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer] > [!UICONTROL Standard-URL]. Durch diese Änderung können Kunden die Standard-URL wieder in eine leere Zeichenfolge ändern, was nach der ersten Konfiguration bisher nicht möglich war. (TGT-44577)
* Es wurden Einschränkungen entfernt, die Kunden daran hinderten, vordefinierte Zielgruppen (Zielgruppen mit reservierten Namen) zu bearbeiten oder zu löschen. (TGT-44655)
* Deaktiviert die[!UICONTROL Fertig]&quot;-Option beim Laden von Spinnern im [!DNL Target] Benutzeroberfläche beim Erstellen [kombinierte Zielgruppen](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* Die [!UICONTROL Sprache] -Link unten im [!UICONTROL Zielgruppen] -Seite, damit sie korrekt mit dem[!UICONTROL Kontokommunikationseinstellungen]&quot;. (TGT-43562)
* Es wurde ein Problem behoben, durch das Kunden manchmal keine [!UICONTROL A/B-Test] Aktivitäten nach Auswahl der [!UICONTROL Adobe Analytics] Option unter [!UICONTROL Administration] > [!UICONTROL Berichterstellung] > [!UICONTROL Reporting-Experience Cloud-Lösung]. (TGT-44844)
* Es wurde ein Problem behoben, durch das Kunden das letzte Erlebnis in einer [!UICONTROL Multivarianz-Test] -Aktivität mit vielen Erlebnissen aus der [!UICONTROL Visual Experience Composer] (VEC). Die [DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) am Ende des VEC konnten Kunden manchmal das letzte Erlebnis nicht sehen. (TGT-44578)
* Es wurde ein Fehler behoben, der dazu führte, dass die Durchsuchen-URL im VEC nicht die aktuelle Seite darstellte, die in einer normalen Browsersitzung sichtbar ist, wenn die Seite autorisiert werden musste oder Umleitungen aufgerufen wurden. (TGT-44350)
* Es wurde ein Problem behoben, durch das Kunden die [!UICONTROL Inkompatible Kriterien filtern] Einstellung in [!UICONTROL Recommendations] > [!UICONTROL Einstellungen]. (TGT-44398)
* Es wurde ein Fehler behoben, der dazu führte, dass POST-Anforderungen neue [!DNL Recommendations] Feeds schlagen bei Verwendung von [!UICONTROL Analytics Classifications] mit Report Suites mit Punkten im Namen. (TGT-44598)
* Aktualisierte Links in der [!DNL Target] Benutzeroberfläche zum Verweis auf die neue [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Verbesserte Sicherheit, um serverseitige SSRF-Versuche (Request Forgery) zu verhindern [!DNL Recommendations] Feeds. (TGT-43769)
* Es wurde ein Problem behoben, durch das Kunden keine Vorschaubilder in anzeigen konnten. [!DNL Recommendations] entwirft, wenn der Bildname [GB18030-Zeichen](https://en.wikipedia.org/wiki/GB_18030){target=_blank}. (TGT-44614)
* Es wurde ein Problem behoben, das einige [GB18030-Zeichen](https://en.wikipedia.org/wiki/GB_18030){target=_blank} zu maskieren im [!UICONTROL Änderungen] Bedienfeld beim Bearbeiten [!UICONTROL Text/HTML] in einer Aktivität [!UICONTROL Erlebnisse] Seite. (TGT-44600)
* Es wurden in der gesamten [!DNL Target]-Benutzeroberfläche Lokalisierungskorrekturen vorgenommen.

## at.js-Version 2.10.2 (7. März 2023)

* Es wurde ein Fehler behoben, der dazu geführt hatte, dass die Funktion `trackEvent` immer einen Fehler zurückgab.

Informationen zu allen at.js-Versionen finden Sie unter [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md). |
