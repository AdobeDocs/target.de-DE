---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e130c68c838e799228956c598c583038a2f68ecf
workflow-type: ht
source-wordcount: '494'
ht-degree: 100%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Geplante Aktualisierung der Edge-Infrastruktur in [!DNL Adobe Target] {#edge}

Für die geplante Aktualisierung der Edge-Infrastruktur müssen zusätzliche IP-Adressen oder Domains auf die Zulassungsliste gesetzt werden. Überprüfen Sie NAT und IP/Domains für die Edge-Bereitstellungen 41-48 und setzen Sie sie auf die Zulassungsliste. Aktualisierungen der Infrastruktur beginnen am 9. August 2023.

Weitere Informationen finden Sie unter [Zulassungsliste für Target-Edge-Knoten](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html?lang=de){target=_blank} im *Adobe Target-Entwicklerhandbuch*.

## [!DNL Target] Standard/Premium 23.8.1 (9. August 2023)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde ein Fehler behoben, durch den manchmal Aktivitäten nicht ordnungsgemäß synchronisiert wurden, wie in der Spalte „[!UICONTROL Status]“ auf der Listenseite [!UICONTROL Aktivität] zu sehen war. (TGT-46010 und TGT-44831)
* Es wurde ein Problem behoben, durch das manchmal der Link „[!UICONTROL In Analytics anzeigen]“ auf der Seite [!UICONTROL Berichte] von Aktivitäten, die [!UICONTROL Analytics for Target] (A4T) als Berichtsquelle verwenden, nicht angezeigt wurde. (TGT-45808)
* Die Darstellung der Werte in Tabellen wurde so angepasst, dass sie anstelle von Dezimalzahlen als Prozentwerte angezeigt werden. Beispiel: 8 % anstelle von 0,08. (TGT-45548)
* Es wurde ein Problem behoben, durch das Kundinnen und Kunden für Aktivitäten von [!UICONTROL Experience Targeting] (XT) den Tastaturfokus nicht dazu verwenden konnten, auf der Seite [!UICONTROL Ziele und Einstellungen] zum nächsten Element zu gehen. (TGT-44526)
* Es wurde ein Problem behoben, durch das die Tastatur nach dem Öffnen des Dialogfelds [!UICONTROL Zielgruppen hinzufügen] den Fokus verlor, während eine Aktivität erstellt wurde. (TGT-44525)

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
