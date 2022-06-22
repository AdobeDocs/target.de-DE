---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7455d680d3ca9ea2fe2a613429f9895b94e79812
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 99%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 2.6.1 (gestaffelte Version: 7.-9. Juni 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **7. Juni**: Region Asien-Pazifik (APAC)
* **8. Juni**: Amerikanische Region
* **9. Juni**: Region Europa, Naher Osten und Afrika (EMEA)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde eine Verbesserung für die neue Seite [!UICONTROL Zielgruppen] bereitgestellt, um einen inkonsistenten Zustand zwischen der alten Datenbank, in der die Zielgruppen in der Vergangenheit gespeichert waren, und der neuen Architektur, die die Informationen direkt aus dem Backend abruft, zu verhindern. (TGT-43552)
* Es wurde ein Fehler behoben, der dazu führte, dass einige Kunden kombinierte Zielgruppen nicht speichern konnten, da die Target-Benutzeroberfläche „leere“ Container erstellte. (TGT-43588)

## Target-Plattform-Release (25. Mai 2022)

Dieses Release umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Unterstützung für [User Agent Client Hints](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md) wurde hinzugefügt.
* Es wurde ein Problem behoben, das zeitweise zu Timeouts beim Rendern von [!UICONTROL Angebotsentscheidungen] in [!UICONTROL Experience Targeting]-Aktivitäten (XT) führte. (TNT-44611)

## at.js-Version 2.9.0 (27. Mai 2022)

* Unterstützung für [User Agent Client Hints](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md) wurde hinzugefügt.
* Es wurde ein Fehler behoben, durch den mehrere Mbox-Anfragen auf derselben Seite unterschiedliche Impressions-IDs erhielten.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

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
