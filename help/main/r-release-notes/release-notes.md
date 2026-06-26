---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: aab659046a6583aeedaf8ec34803b0751bebe3c6
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 49%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 26.6.8 (24. Juni 2026)

**Aktivitäten**

+++Details anzeigen

* **Source-Filter für API- und MCP-erstellte Ressourcen.** Es wurde ein Problem behoben, bei dem das Filtern nach [!UICONTROL Adobe Target]API oder [!UICONTROL Adobe Target MCP] bei den Listenseiten für Aktivitäten, Zielgruppen und Angebote nicht funktionierte. (TGT-55236)

* **Filterwerte der Aktivitätsquelle.** Es wurde ein Problem behoben, bei dem der Quellfilter {0]Adobe Target API] oder [!UICONTROL  Adobe Target MCP2 keine neu erstellten Zielgruppen anzeigte. [!UICONTROL (TGT-55237)

+++

**Lokalisierung**

+++Details anzeigen

* **Nicht lokalisierte Zeichenfolgen im Modal [!UICONTROL JSON-Angebot erstellen].** Es wurde ein Problem behoben, bei dem Zeichenfolgen im [!UICONTROL JSON-Angebot erstellen]-Modal, einschließlich [!UICONTROL Name] und [!UICONTROL Workspace], während der Erstellung einer Aktivität nicht lokalisiert wurden. (TGT-50084)

* **Nicht lokalisierte Popup-Nachricht in einer [!UICONTROL Recommendations]-Aktivität.** Fehlerkorrektur - Beim Hinzufügen von Recommendations in einer formularbasierten Aktivität (Recommendations) tritt jetzt keine [!UICONTROL  mehr ]. (TGT-50463)

* **Nicht lokalisierte Zeichenfolge in den [!UICONTROL Sammlungen] und [!UICONTROL Ausschlüsse] Dialogfeldern.** Es wurde ein Problem behoben, bei dem die Zeichenfolge „Element-Payload“ in den Dialogfeldern [!UICONTROL Sammlungen] und [!UICONTROL Ausschlüsse] in [!UICONTROL Recommendations] nicht lokalisiert wurde. (TGT-51542)

* **Nicht lokalisierte Zeichenfolge „Genehmigende Person“ auf der Registerkarte [!UICONTROL Zielgruppen].** Es wurde ein Problem behoben, bei dem die Zeichenfolge „Genehmigende Person“ nicht in der Spalte [!UICONTROL Workspace] auf der Seite [!UICONTROL Zielgruppenbibliothek] lokalisiert wurde. (TGT-51751)

+++

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
