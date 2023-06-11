---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: b06cc6f4a8e7d1617dd5d3a8226e2b77474cfe77
workflow-type: ht
source-wordcount: '654'
ht-degree: 100%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 23.5.2 (31. Mai 2023)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
|--- |--- |
| Real-Time CDP-Profilattribute, die für [!DNL Target] freigegeben werden | [!UICONTROL Real-Time CDP-Profilattribute] können für [!DNL Target] zur Verwendung in HTML- und JSON-Angeboten freigegeben werden.<P>Weitere Informationen finden Sie unter [Freigeben von Real-Time CDP-Profilattributen für [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes). |

* Es wurde ein Fehler behoben, der dazu führte, dass beim Generieren eines Profil-API-Autorisierungs-Tokens eine leere Seite angezeigt wurde. (TGT-45387 und TGT-45423)
* Es wurde ein Problem behoben, das die Anzeige eines Bildes im Bedienfeld [!UICONTROL Design erstellen] verhindert hat, wenn der Bildname GB-18030-Zeichen enthält. (TGT-44614)
* Es wurde ein Problem behoben, bei dem einige GB 18030-Symbolzeichen in Text/HTML in Erlebnissen fälschlicherweise maskiert wurden. (TGT-44600)
* Es wurde ein Fehler behoben, der dazu führte, dass Berichte für Aktivitäten von [!UICONTROL Automatisierte Personalisierung] während der Analyse eingefroren sind. (TGT-44820)
* Es wurde ein Fehler behoben, der die Suche nach einer Aktivität auf der Seite [!UICONTROL Aktivität] verhinderte, wenn der Aktivitätsname eine eckige Klammer ([ oder ]) enthielt. (TGT-44777)
* Es wurde ein Fehler behoben, der die Synchronisierung einer Aktivität verhinderte, wenn das Ziel der Aktivität Sonderzeichen enthielt. (TGT-44982)
* Es wurde ein Fehler behoben, der dazu führte, dass in der [!DNL Target]-Benutzeroberfläche für den Standardarbeitsbereich bei bestimmten Kundinnen und Kunden keine Aktivitäten angezeigt wurden. (TGT-45286)
* Das Verhalten der Markierung „Duplikate nicht zulassen“ wurde aktualisiert. Die Flags für ausgeschlossene wiederholende Angebote werden aktualisiert, damit sich wiederholende Angebote möglich sind, wenn sie das Standardinhaltsangebot sind (für APIs v3 und v4). Außerdem können doppelte Optionen aktiviert werden, wenn die Optionen auf das Standardinhaltsangebot verweisen und keine Vorlagen definiert sind. (TNT-46617)
* Es wurde ein Problem behoben, bei dem ein Abfrageparameter zu einer URL hinzugefügt wurde, der verhinderte, dass die Seite im [!UICONTROL Visual Experience Composer (VEC)] geladen wurde. (TGT-44873)
* Es wurden in der gesamten [!DNL Target]-Benutzeroberfläche Lokalisierungskorrekturen vorgenommen.

## [!DNL Target] Standard/Premium 23.5.1 (23.-25. Mai 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

&#x200B;23. Mai: Europa, Naher Osten und Afrika (EMEA)
&#x200B;24. Mai: Asien-Pazifik (APAC)
&#x200B;25. Mai: Amerika

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

* Es wurde ein Problem behoben, durch das bestimmte Kunden keine Zielgruppen mit Besucherprofilen erstellen konnten, die die Operatoren „größer als“ oder „kleiner als“ verwendeten. (TGT-45271)
* Es wurden in der gesamten [!DNL Target]-Benutzeroberfläche Lokalisierungskorrekturen vorgenommen.
* Die Target-Benutzeroberfläche wurde an verschiedenen Stellen für eine bevorstehende Aktualisierung der Benutzeroberfläche aktualisiert (Änderungen befinden sich hinter einem Feature Flag, bis die Aktualisierungen veröffentlicht werden).

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

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
