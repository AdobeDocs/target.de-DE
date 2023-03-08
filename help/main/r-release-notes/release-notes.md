---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e458793e4d0110d97f3f5124cbe6e54520d3f0e9
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 69%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 22.15.1 (8. und 9. März 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **8. März**: Amerikanische Region
* **9. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **9. März**: Region Asien-Pazifik (APAC)

Diese Version beinhaltet die folgenden neuen Funktionen und Verbesserungen:

| Funktion | Details |
| --- | --- |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] | [!DNL Target] ermöglicht die Auswahl von Metriken basierend auf binomialen Ereignissen oder Metriken basierend auf kontinuierlichen Ereignissen bei Verwendung von [!UICONTROL A4T] für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.<P>Beachten Sie die folgende zeitkritische Änderung bei unterstützten Metriken:<ul><li>[!DNL Target] das vorherige Verhalten für bestehende Aktivitäten bis zum 9. September 2023 beibehalten. Nach diesem Datum werden Aktivitäten, die nicht unterstützte Metriken verwenden, eingestellt, um die vorhandene Aktivitätsmigration zum neuen Verhalten zu erzwingen.</li></ul>Weitere Informationen finden Sie unter [Unterstützte Zielmetriken](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) in *A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting*. |
| [!UICONTROL Automatische Zuordnung] using [!UICONTROL Analytics for Target] (A4T) | Neues Tutorial:<ul><li>[Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Automatische Zuordnung] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Automatisches Targeting] using [!UICONTROL Analytics for Target] (A4T) | Neues Tutorial:<ul><li>[Einrichten von A4T-Berichten in [!DNL Analysis Workspace] für [!UICONTROL Automatisches Targeting] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

## at.js-Version 2.10.2 (7. März 2023)

* Es wurde ein Fehler behoben, der dazu führte, dass die `trackEvent` -Funktion immer einen Fehler zurückgeben.

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
