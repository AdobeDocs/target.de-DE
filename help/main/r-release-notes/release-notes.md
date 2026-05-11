---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 860dd22fc4ec261a62869cb656d72bd49f2bd91c
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 51%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.5.1 (7. Mai 2026)

**Integrationen**

+++Details anzeigen

* **[!DNL Adobe Target]in Experimentation Accelerator.** Es wurde Unterstützung für die Zuweisung [!DNL Target] Arbeitsbereiche zu Experimentation Accelerator-Sandboxes hinzugefügt, damit Teams Experimente aus [!DNL Adobe Target] in Experimentation Accelerator an einem Ort anzeigen können. [Weitere Informationen](../c-integrating-target-with-mac/experimentation-accelerator.md)

+++

**Aktivitäten**

+++Details anzeigen

* **[!UICONTROL Graph View]mit Tabelle und Download nicht synchron.** Es wurde ein Problem behoben, bei dem Aktivitätsberichte in **[!UICONTROL Graph View]** für einige Datumsbereiche fehlende oder null Metriken anzeigen konnten, obwohl **[!UICONTROL Table View]** und der heruntergeladene Bericht immer noch die richtigen Werte zeigten. (TGT-54998)

+++

**[!UICONTROL Audiences]**

+++Details anzeigen

* **Liste der Zielgruppennutzung nicht vollständig gerendert.** Es wurde ein Problem behoben, bei dem der Abschnitt **[!UICONTROL Usage]** in den Zielgruppendetails nur eine Teilmenge der zugeordneten Aktivitäten anzeigen konnte, selbst wenn zusätzliche Aktivitäten mit dieser Zielgruppe verknüpft waren. (TGT-55094)

+++

**[!UICONTROL Administration]**

+++Details anzeigen

* **Klarere Bestätigung für IP-Verschleierung des letzten Oktetts.** Wenn Sie **[!UICONTROL Obfuscate Visitor IP addresses]** in **[!UICONTROL Last octet]** auf **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** ändern, wird im Bestätigungsdialogfeld jetzt erklärt, dass [!DNL Target] das letzte Oktett der Besucher-IP-Adresse ausblendet. (TGT-44821)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Details anzeigen

* **Leere oder unvollständige Seite mit Enhanced Experience Composer (EEC).** Es wurde ein Problem behoben, bei dem der [!UICONTROL Visual Experience Composer] die Site nicht im Editor laden konnte, wenn **[!UICONTROL Enhanced Experience Composer]** aktiviert war. (TGT-54576)

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
