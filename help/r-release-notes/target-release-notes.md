---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Versionshinweise
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 14e1a71bbebbf8baec09df41e3e08f89bb64a4e0
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 28%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 25. Mai 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungszeitpunkt identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**&quot;mbox.js&quot;-Einstellung**: Ab dem 31. März 2021 wird die mbox.js -Bibliothek  [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von mbox.js korrekt fehl und wirken sich auf Seiten aus, deren Aktivitäten [!DNL Target] durch die Bereitstellung von Standardinhalten ausgeführt werden.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek. Weitere Informationen finden Sie unter [Übersicht: Target für clientseitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] badgeversion 2.5.0 (1. Juni 2021)

Diese Version von [!DNL Platform Web SDK] unterstützt Folgendes:

| Funktion | Details |
| --- | --- |
| Umleitungs-Unterstützung mit [!UICONTROL Analytics for Target] (A4T) | Das Platform Web SDK unterstützt jetzt [!DNL Target]-Umleitungen bei der Verwendung von A4T. Umleitungsangebote in [!DNL Adobe Target] führen dazu, dass ein Browser zu einer neuen Seite umleitet. |
| Antwort-Token | Das Platform Web SDK unterstützt jetzt [!DNL Target] Antwort-Token. Mithilfe von Antwort-Token können Sie [!DNL Adobe Target]-spezifische Informationen automatisch an die Webseite Ihrer Marke ausgeben. Diese Informationen können Details zur Aktivität, zum Angebot, zum Erlebnis, zum Benutzerprofil, zu geografischen Informationen und mehr enthalten. Diese Details bieten zusätzliche Antwortdaten, um sie für interne Systeme oder Drittanbietersysteme freizugeben oder für das Debugging zu verwenden. |

## [!DNL Target Standard/Premium] 21.5.1 (8. Juni 2021)

| Funktion | Details |
| --- | --- |
| ![Premium ](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL badgeCatalog ] SearchAPI | Durchsuchen Sie Ihren [!DNL Recommendations] Produkt- und Inhaltskatalog programmgesteuert per API, um Elemente zu identifizieren, die einem Suchkriterium entsprechen, und vereinfachen Sie die Verwaltung Ihres Katalogs.<br>**Einschränkungen und Hinweise**:<ul><li>Die Katalogsuche per API wird nicht für Umgebungen mit mehr als 2.000.000 Elementen unterstützt.</li><li>Katalogsuchergebnisse über API werden schneller aktualisiert als Katalogsuchergebnisse über die [!DNL Target] -Benutzeroberfläche. Die Katalogsuche in der Benutzeroberfläche [!DNL Target] kann länger dauern, bis die neuesten Ergebnisse angezeigt werden.</li></ul>Weitere Informationen finden Sie unter [Suchen nach Entitäten](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) im Handbuch *[!DNL Adobe Target][!DNL Recommendations] API* . |

## [!DNL Target Standard/Premium] 21.5.2 (noch festzulegender Zeitpunkt)

Diese Version enthält die folgenden neuen Funktionen und Erweiterungen. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | Die folgenden Verbesserungen gelten für [!DNL Recommendations]-Popularitätsalgorithmen:<ul><li>Eine neue sechsstündige &quot;Lookback-Fenster&quot;(Datenbereich)-Option steht für alle Popularitätsalgorithmen (am häufigsten angezeigte/Topverkäufe) zur Verfügung, wenn [!DNL Target] die Verhaltensdatenquelle ist. (Dieses Lookback-Fenster ist *nicht* verfügbar, wenn [!DNL Adobe Analytics] die Verhaltensdatenquelle ist.)</li><li>Wenn diese Option aktiviert ist, werden die folgenden Algorithmen ungefähr alle drei Stunden (statt alle 12 Stunden) ausgeführt.<ul><li>Am häufigsten angezeigt</li><li>Am häufigsten gekauft</li><li>Am häufigsten angezeigt nach Kategorie</li><li>Am häufigsten gekauft nach Kategorie</li><li>Am häufigsten angezeigt durch benutzerdefiniertes Attribut (mithilfe der groupBy-Funktion)</li><li>Am häufigsten gekauft durch benutzerdefiniertes Attribut (mithilfe der groupBy-Funktion)</li></ul></ul>(TOP-1086) |

Diese Version enthält die folgenden Fehlerbehebungen.

* Der Inhalt wird hinzugefügt, sobald das Veröffentlichungsdatum näher rückt.

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
