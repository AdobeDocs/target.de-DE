---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 1c9728b447ee1402cc133d38845a25da3038d0ca
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 49%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 28. März 2023**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 23.3.1 (28.-30. März 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **28. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **29. März**: Region Asien-Pazifik (APAC)
* **30. März**: Region Nord- und Südamerika

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
|--- |--- |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]<p>(Veröffentlichungsdatum: 30. März 2023) | [!DNL Target] ermöglicht die Auswahl von Metriken, die auf binomialen Ereignissen basieren, oder Metriken, die auf kontinuierlichen Ereignissen basieren, wenn [!UICONTROL A4T] für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] verwendet wird.<P>Beachten Sie die folgende Änderung bei den unterstützten Metriken:<ul><li>[!DNL Target] behält das vorherige Verhalten für bestehende Aktivitäten bis zum 9. September 2023 bei. Nach diesem Datum werden die Aktivitäten eingestellt, die nicht unterstützte Metriken verwenden, um die Migration vorhandener Aktivitäten auf das neue Verhalten zu erzwingen.</li></ul>Weitere Informationen finden Sie unter &quot;Unterstützte Metriken&quot;in [A4T-Unterstützung für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported).<P>Im Zusammenhang mit dieser Funktion wurden die folgenden Tutorials aktualisiert:<ul><li>[Einrichten von A4T-Berichten in  [!DNL Analysis Workspace]  für Aktivitäten des Typs [!UICONTROL Automatische Zuordnung]](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=de){target=_blank}</li><li>[Einrichten von A4T-Berichten in  [!DNL Analysis Workspace]  für Aktivitäten des Typs [!UICONTROL Automatisches Targeting]](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=de){target=_blank}</li></ul> |

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

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |


## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
