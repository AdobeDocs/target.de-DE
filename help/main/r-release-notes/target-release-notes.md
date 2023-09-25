---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 11b5915d75b72a3891572d841de0a353f68dcbf3
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 93%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 18. September 2023**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 23.9.3 (18. September 2023)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* [!UICONTROL Visual Experience Composer] (VEC) wurde verbessert und unterstützt jetzt Lightning Web Components (Light DOM). (TGT-45422)
* Es wurde ein Fehler behoben, der dazu führte, dass VEC-Aktionen in der falschen Reihenfolge angewendet wurden. In einigen Fällen führte VEC asynchron einige Änderungen durch und das Hinzufügen zusätzlicher Änderungen an einem Element verursachte Fehler, wenn dieses Element nach einer [!UICONTROL Einfügen]-Aktion angezeigt wurde. Außerdem wird die VEC-URL jetzt beim Klicken auf Anker-Links aktualisiert. (TGT-45983)
* Es wurde ein Problem mit der [!UICONTROL Überlagerungsfunktion] von VEC behoben, die jetzt Elemente in Shadow-DOMs unterstützt. (TGT-45202 und TGT-45262)
* Es wurde ein Problem behoben, das beim Öffnen einer Seite mit Single Page Application (SPA) im VEC und anschließendem Wechsel in den Modus [!UICONTROL Durchsuchen] dazu geführt hat, dass die Pfeile „Zurück“ und „Weiter“ nicht ordnungsgemäß funktionierten. (TGT-45956)
* Es wurde ein Problem behoben, das das Laden einiger Web-Seiten in VEC verhindert hat. (TGT-45983)

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

## [!DNL Target] Standard/Premium 23.5.2 (Datum noch festzulegen)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Auswahl der Optimierungskriterien für [!DNL Adobe Analytics] Metriken.
* Die Synchronisierung externer Zielgruppen mit Sling-Aufträgen wurde aktiviert.
* Es wurde ein Problem behoben, bei dem SC Report Suites, die ein Punktzeichen im Namen enthielten, nicht unterstützt wurden.
* Neue Funktion, mit der Kunden integrierte Zielgruppen löschen und bearbeiten können.

## [!DNL Target] Standard/Premium 23.5.3 (Datum noch festzulegen)

Diese Version umfasst die folgenden Verbesserungen:

| Funktion | Details |
|--- |--- |
| [!UICONTROL QA-Modus] für Aktivitäten von [!UICONTROL Automatisierte Personalisierung] | [!DNL Adobe Target] [!UICONTROL QA-Modus] ist jetzt für Aktivitäten von [!UICONTROL Automatisierte Personalisierung] verfügbar, was die Funktionalität [!UICONTROL Links in der Vorschau anzeigen] ersetzt.<P>Weitere Informationen finden Sie unter [Aktivitäts-QA](/help/main/c-activities/c-activity-qa/activity-qa.md). |

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
