---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Versionshinweise
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: f5047484b7cb113698b9b09f699d4e6a293b0b59
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 36%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 12. Mai 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Ab dem 31. März 2021 wird die Bibliothek &quot;mbox.js&quot; [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;in Würde fehl und wirken sich auf Ihre Seiten aus, deren Aktivitäten [!DNL Target] ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek at.js. Weitere Informationen finden Sie unter [Übersicht: Target für clientseitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Adobe Experience Platform Web SDK] (17. Mai 2021)

Diese Version von [!DNL Platform Web SDK] unterstützt [!UICONTROL Analytics for Zielgruppe] (A4T) für [!DNL Target]-Umleitungen.

## [!DNL Target Standard/Premium] 21.5.1 (25. Mai 2021)

Der Inhalt wird hinzugefügt, sobald das Veröffentlichungsdatum näher rückt.

## [!DNL Target Standard/Premium] 21.5.2 (noch festzulegendes Datum)

Diese Version enthält die folgenden neuen Funktionen und Erweiterungen. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | Die folgenden Erweiterungen gelten für [!DNL Recommendations] Popularitätsalgorithmen:<ul><li>Eine neue sechsstündige Option für das &quot;Lookback-Fenster&quot;(Datenbereich) steht für Algorithmen mit allen Beliebtheitswerten (Am meisten angezeigt/Topverkäufe) zur Verfügung, wenn [!DNL Target] die verhaltensbasierte Datenquelle ist. (Dieses Lookback-Fenster ist *nicht* verfügbar, wenn [!DNL Adobe Analytics] die verhaltensbasierte Datenquelle ist.)</li><li>Wenn diese Option aktiviert ist, werden die folgenden Algorithmen etwa alle drei Stunden (statt alle 12 Stunden) ausgeführt.<ul><li>Am meisten angezeigt</li><li>Am häufigsten gekauft</li><li>Am häufigsten angezeigt nach Kategorie</li><li>Am häufigsten gekauft nach Kategorie</li><li>Am meisten nach benutzerdefiniertem Attribut angezeigt (mit der Funktion groupBy)</li><li>Am häufigsten nach benutzerdefiniertem Attribut gekauft (mit der Funktion groupBy)</li></ul></ul>(TOP-1086) |

Diese Version enthält die folgenden Fehlerbehebungen.

* Wird hinzugefügt, wenn sich das Veröffentlichungsdatum nähert.

## at.js Version 2.5.0 (Datum festzulegen)

Diese Version von at.js umfasst die folgenden Erweiterungen und Änderungen:

* [Unterstützung von ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) Entscheidungen auf dem Gerät für &quot;at.js&quot;.
* [Unterstützung ](/help/c-activities/c-activity-qa/activity-qa.md) von Vorschauen für Automated Personalization-Aktivitäten

Mit dieser Version wird auch die Unterstützung für Microsoft Internet Explorer 10 und höher entfernt.

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
