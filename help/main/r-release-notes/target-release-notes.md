---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: ad82d108adc6f5c76b2104f40fb0bb2c66e98a2b
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 33%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Donnerstag, 23. April 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.4.5 (24. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem Empfehlungen nach der Aktivierung der [!DNL Recommendations]-Aktivität nicht auf der Website des Kunden angezeigt wurden. (TGT-52164)
* `OptionLocalIDs` nicht mehr fälschlicherweise inkrementiert, wenn die Option unverändert bleibt. (TGT-52187)
* Heruntergeladene Berichtsdateien zeigen jetzt die in der Berichterstellungs-Benutzeroberfläche vorhandenen Daten korrekt an. (TGT-52068)
* Stapelvorgänge schlagen nach dem Hinzufügen von Seitenbereitstellungsregeln nicht mehr fehl. (TGT-52097)
* Es wurde ein Fehler behoben, der dazu führte, dass [!DNL Target] alle Abfrageparameter aus der URL der Website kürzte. (TGT-52100)
* Es wurde ein Konsolenfehler behoben, der Kunden daran hinderte, Aktivitäten sowohl in der alten als auch in der aktualisierten Target-Benutzeroberfläche zu erstellen. (TGT-52181)
* Es wurde ein Problem behoben, durch das Kunden keine neuen Seiten hinzufügen konnten, was zu einem Fehler bei der ungültigen Benutzereingabe führte. (TGT-52258)
* Es wurde ein Problem behoben, das dazu führte, dass Änderungen nach dem Hinzufügen zusätzlicher Seiten und dem anschließenden Zurücknavigieren zur Registerkarte [!UICONTROL Experiences] verschwanden. (TGT-52264)
* Es wurde ein Problem behoben, durch das Kundinnen und Kunden daran gehindert wurden, die Zielgruppe in einer [!UICONTROL Experience Targeting] (XT)-Aktivität zu ändern. (TGT-52191)
* Fehlerkorrektur - Die Bearbeitung einer XT-Aktivität ist jetzt möglich, da die Benutzeroberflächenregel nicht unterstützt wird. (TGT-52273)
* Es wurde ein Problem behoben, bei dem Aktivitätsänderungen nicht in der [!DNL Target]-Benutzeroberfläche angezeigt wurden, obwohl sie erfolgreich auf der Web-Seite bereitgestellt wurden. (TGT-52192)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, bei dem Breadcrumbs nicht immer unten im Editor angezeigt wurden, was bei der präzisen Auswahl von Elementen zu Problemen führte. (TGT-51169)
* Es wurde ein Problem behoben, bei dem in der Dropdown-Liste [!UICONTROL Audience] aufgrund von Paginierung nicht alle Zielgruppen angezeigt wurden. (TGT-52204)
* Fehlerkorrektur - Jetzt wird keine Meldung mehr angezeigt, dass eine ungültige Benutzereingabe erfolgt ist, wenn neue Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten hinzugefügt werden. (TGT-52210)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Analytics for Target] (A4T) fälschlicherweise als Berichtsquelle ausgewählt wurde, obwohl die Kundin bzw. der Kunde keinen Zugriff auf A4T hatte. (TGT-52226)
* Es wurde ein Problem behoben, das das Speichern einer Aktivität mit der [!UICONTROL View a Page] URL-Metrik verhinderte. (TGT-52260)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Arbeitsbereiche beim Erstellen von Angeboten innerhalb einer Aktivität auszuwählen. (TGT-52289)
* Es wurde ein Problem behoben, bei dem Änderungen von einem Erlebnis falsch angezeigt wurden, wenn zu einem anderen Erlebnis gewechselt wurde. (TGT-52184)
* Es wurde ein Problem behoben, bei dem das Standardangebot nach dem Öffnen der Aktivität nicht korrekt in der [!DNL Target]-Benutzeroberfläche angezeigt wurde. (TGT-52198)

## Aktualisierung der Target-Berechtigungen (22. April 2025)

Diese zukünftige Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Product]- und [!UICONTROL Solutions]-Administratoren die Einstellungen in den [!UICONTROL Administration] Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die [!UICONTROL Administration].

Weitere Informationen finden Sie unter [Verwaltung von Target](/help/main/administrating-target/start-target.md).

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
