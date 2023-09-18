---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6fa553c7179cd2a6d500bdc53cc77dc01ee906e7
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 79%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 23.9.3 (18. September 2023)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Der [!UICONTROL Visual Experience Composer] (VEC) zur Unterstützung von BlitzWeb-Komponenten (Light DOM). (TGT-45422)
* Es wurde ein Fehler behoben, der dazu führte, dass VEC-Aktionen in der falschen Reihenfolge angewendet wurden. In einigen Fällen führte der VEC asynchron einige Änderungen durch und das Hinzufügen zusätzlicher Änderungen an einem Element verursachte Fehler, wenn dieses Element nach einem [!UICONTROL Einfügen] Aktion. Korrekturen an der VEC-URL, die jetzt beim Klicken auf Ankerlinks aktualisiert wird. (TGT-45983)
* Es wurde ein Problem mit dem VEC behoben [!UICONTROL Überlagerung] -Funktion, die jetzt Elemente in Shadow-DOMs unterstützt. (TGT-45202 und TGT-45262)
* Es wurde ein Problem behoben, das beim Öffnen einer Seite mit Einzelseiten-Apps (SPA) im VEC und anschließendem Öffnen von [!UICONTROL Durchsuchen] -Modus dazu geführt hat, dass die Pfeile &quot;Zurück&quot;und &quot;Weiter&quot;nicht ordnungsgemäß funktionierten. (TGT-45956)
* Es wurde ein Problem behoben, das das Laden einiger Webseiten in VEC verhindert hat. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (12.–14. September 2023)

Diese Version ist gemäß dem folgenden gestaffelten Zeitplan verfügbar:

* **12. September**: Amerikanische Region
* **13. September**: Region Asien-Pazifik (APAC)
* **14. September**: Region Europa, Naher Osten und Afrika (EMEA)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Die [!DNL Analytics]-API wurde durch die neue [!DNL Analytics]-API Version 2.0 ersetzt.  (TGT-45345)
* Es wurden Probleme behoben, die sich auf Aktivitäten der [!UICONTROL Automatisierten Personalisierung] (AP) für einige Kundinnen und Kunden auswirkten, einschließlich der rechtzeitigen Synchronisierung der Aktivität im [!DNL Target]-Backend und der Bereitstellung des erwarteten Erlebnisses in Vorschau-Links.  (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (6.–11. September 2023)

Diese Version ist gemäß dem folgenden gestaffelten Zeitplan verfügbar:

* **6. September**: Amerikanische Region
* **7. September**: Region Europa, Naher Osten und Afrika (EMEA)
* **11. September**: Region Asien-Pazifik (APAC)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde ein Problem behoben, das zu inkonsistenten Berichtsdaten in der Benutzeroberfläche [!DNL Target] und der Benutzeroberfläche [!DNL Adobe Analytics] für Aktivitäten der [!UICONTROL automatischen Zuordnung] führte, die [!UICONTROL Analytics for Target] (A4T) als Berichtsquelle verwenden.  (TGT-46112)
* Der Timeout für PUT-Aufrufe an die Target-Bereitstellungs-API wurde auf 15 Sekunden erhöht, um Timeout-Fehler zu vermeiden. (TGT-46091)
* Es wurde ein Problem behoben, durch das die URL beim Durchsuchen einer Single Page Application(SPA)-Website nicht immer aktualisiert wurde. (TGT-45417)

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
