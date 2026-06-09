---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 391653c7a45a48c311c6a6cff358bd077f8c47b7
workflow-type: tm+mt
source-wordcount: 656
ht-degree: 41%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 26.6.1 (4. Juni 2026)

**Aktivitäten**

+++Details anzeigen

* **Unvollständige Aktivitäts-URL in [!UICONTROL Aktivitätsübersicht].** Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem in der &#x200B;]Aktivitätsübersicht“ nicht die vollständige URL für eine Aktivität angezeigt wurde. (TGT-54029)

* **Nicht lokalisiertes Datumsformat in Aktivitätsberichten.** Fehlerkorrektur - Das Datumsformat ist jetzt auf der Registerkarte **[!UICONTROL Berichte]** nicht lokalisiert, wenn Sie eine Option **Letzte X Tage** aus der Dropdown-Liste **[!UICONTROL Vorgegebener Datumsbereich]** auswählen. (TGT-51637)

* **Die formularbasierte Aktivität kann mit bestimmten GB2-18030 nicht in &quot;[!UICONTROL &quot; gespeichert &#x200B;].** Es wurde ein Problem behoben, bei dem Sie eine formularbasierte Aktivität nicht speichern konnten, wenn das Feld **[!UICONTROL Standort]** bestimmte GB18030-Zeichen enthielt. (TGT-46980)

+++

**[!UICONTROL Zielgruppen]**

+++Details anzeigen

* **Nicht lokalisierter Kalender im Zielgruppen-Fluss für vereinfachtes und traditionelles Chinesisch erstellen.** Es wurde ein Problem behoben, bei dem der Kalender in den **[!UICONTROL Start]** und **[!UICONTROL Ende]**-Feldern des **[!UICONTROL Zeitrahmen]**-Attributs während des Flusses Zielgruppe erstellen nicht in den Gebietsschemata Vereinfachtes Chinesisch (CHS) und Traditionelles Chinesisch (CHT) lokalisiert wurde. (TGT-50619)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Nicht lokalisierte QuickInfos im aktualisierten Activity Builder.** Es wurden Lokalisierungsprobleme behoben, bei **[!UICONTROL die QuickInfos für]** Verfeinerungen **[!UICONTROL und]** Inhalte“ im aktualisierten Activity Builder [!UICONTROL Visual Experience Composer] nicht lokalisiert wurden. (TGT-53721)

* **Nicht lokalisiert [!UICONTROL Alle Besucher] in [!UICONTROL Experience Audiences].** Es wurde ein Problem behoben **[!UICONTROL bei dem die Zeichenfolge]** Alle Besucher **[!UICONTROL in Erlebniszielgruppen]** in der linken Leiste nicht im [!UICONTROL Visual Experience Composer) &#x200B;]. (TGT-50086)

+++

**[!UICONTROL Berichte]**

+++Details anzeigen

* **Nicht lokalisiertes Datumsformat im Fenster [!UICONTROL Vorgabe erstellen].** Es wurde ein Problem behoben, bei dem das Datumsformat im Feld **[!UICONTROL Datumsbereich]** des Fensters **[!UICONTROL Vorgabe erstellen]** nicht lokalisiert wurde. (TGT-49239)

+++

**Lokalisierung**

+++Details anzeigen

* **GB18030 Zeichenanzeige in mehreren Bereichen.** Es wurden Probleme behoben, bei denen einige Zeichen im Bereich für private Verwendung fälschlicherweise als Briefe in der **[!UICONTROL Zielgruppe]**-Benutzeroberfläche, **[!UICONTROL Administration]** > **[!UICONTROL Eigenschaften]**, der Konfiguration mobiler Viewports und in Popup-Benachrichtigungen angezeigt wurden. (TGT-49622, TGT-49623, TGT-49624 UND TGT-49625)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit der [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

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
