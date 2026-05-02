---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7976d43e43baeabdb68509373f1b0b72bbe723b3
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 49%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.4.4 (28. April 2026)

**Aktivitäten**

+++Details anzeigen

* **Fehler mit Zielgruppenfilter in Berichten.** Es wurde ein Problem behoben, bei dem eine Änderung des Zielgruppenfilters in **[!UICONTROL Goals & Settings]** einen Fehler im Abschnitt Reporting der [!DNL Target]-Benutzeroberfläche verursachte. (TGT-55006)

* **Aktivitäten nach Priorität sortieren.** Es wurde eine Sortierung nach Priorität auf der Aktivitätenliste unter Verwendung der **[!UICONTROL Priority]** Spaltenüberschrift hinzugefügt, wobei aufsteigende und absteigende Reihenfolge mit anderen sortierbaren Spalten übereinstimmen. (TGT-54948)

* **Zusätzliche Aktivitätseigenschaften werden nach dem Speichern nicht beibehalten.** Es wurde ein Problem behoben, bei dem bestimmte **[!UICONTROL Properties]** nach dem Speichern und erneuten Öffnen einer Aktivität nicht beibehalten wurden. (TGT-53889)

+++

**Lokalisierung**

+++Details anzeigen

* **Japanische Kennzeichnungen für [!UICONTROL Page Delivery] Regeloperatoren.** Fehlerkorrektur - Unlesbare oder beschädigte Zeichenfolgen für Operatorkennzeichnungen der Seitenbereitstellungsregel in der japanischen Benutzeroberfläche wurden korrigiert. (TGT-53097)

+++

**APIs**

+++Details anzeigen

* **Reporting [!DNL GraphQL] API-Unterstützung für `segmentId`.** `segmentId` zur Reporting-[!DNL GraphQL]-API hinzugefügt. (TGT-55021)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Änderungen werden im Editor am falschen Erlebnis angezeigt.** Es wurde ein Problem behoben, bei dem ein Löschen oder eine andere Änderung im falschen Erlebnis angezeigt werden konnte, nachdem zwischen Erlebnissen in der [!UICONTROL Visual Experience Composer] gewechselt wurde. (TGT-54955)

* **Änderungen beim Löschen von insert HTML entfernt.** Es wurde ein Problem behoben, bei dem durch Löschen des zusätzlichen **[!UICONTROL HTML]**-Blocks, der mit **[!UICONTROL Insert before]** oder **[!UICONTROL Insert after]** hinzugefügt wurde, auch eine verknüpfte Änderung entfernt wurde, die keinen CSS-Selektor hatte. (TGT-54530)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)




**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

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
