---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Versionshinweise
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 146395f5453093ca34b259a143ff4e4c63be949b
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 69%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 7. Juni 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.5.2 (noch festzulegender Zeitpunkt)

Diese Version beinhaltet die folgenden neuen Funktionen und Verbesserungen. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | Die folgenden Verbesserungen gelten für [!DNL Recommendations]-Popularitätsalgorithmen:<ul><li>Eine neue sechsstündige &quot;Lookback-Fenster&quot;(Datenbereich)-Option steht für alle Popularitätsalgorithmen (am häufigsten angezeigte/Topverkäufe) zur Verfügung, wenn [!DNL Target] die Verhaltensdatenquelle ist. (Dieses Lookback-Fenster ist *nicht* verfügbar, wenn [!DNL Adobe Analytics] die Verhaltensdatenquelle ist.)</li><li>Wenn diese Option aktiviert ist, werden die folgenden Algorithmen ungefähr alle drei Stunden (statt alle 12 Stunden) ausgeführt.<ul><li>Am häufigsten angezeigt</li><li>Am häufigsten gekauft</li><li>Am häufigsten angezeigt nach Kategorie</li><li>Am häufigsten gekauft nach Kategorie</li><li>Am häufigsten angezeigt durch benutzerdefiniertes Attribut (mithilfe der groupBy-Funktion)</li><li>Am häufigsten gekauft durch benutzerdefiniertes Attribut (mithilfe der groupBy-Funktion)</li></ul></ul>(TOP-1086) |

Diese Version enthält die folgenden Fehlerbehebungen.

* Der Inhalt wird hinzugefügt, sobald das Veröffentlichungsdatum näher rückt.

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
