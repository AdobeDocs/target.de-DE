---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: a5d2c07105b1d0fac6115fe507537be6a36799e9
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 33%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am 19. Juli 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 22.7.1 (20. Juli 2022)

Diese Version umfasst die folgenden Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Beschreibung |
| --- | --- |
| Verbesserte Genauigkeit der Zielgruppenbewertung und Latenz der Endbenutzer durch IPv6-Unterstützung | Die Geostandorte der Besucher werden jetzt nach IPv6-Adressen bestimmt, sofern verfügbar, im Gegensatz zu nur IPv4-Adressen. Bereitstellungs-APIs unterstützen auch IPv6-Eingabeparameter. Filter und Zulassungsauflistung unterstützen sowohl IPv4- als auch IPv6-Adressen. Diese IPv6-Unterstützung in dieser Version bedeutet, dass Besucher genauer in Zielgruppen eingeschlossen werden (sie qualifizieren sich also genauer für Aktivitäten oder werden in Filterkriterien aufgenommen). Außerdem wird die Datenlatenz verbessert, da IPv6-Clients die Kommunikation direkt durchführen und so den Verwaltungsaufwand für das IPv6-zu-IPv4-Gateway vermeiden. |
| Verbesserung der clientseitigen A4T-Payload-Handhabung | Bei einer serverseitigen A4T-Integration leitet Adobe Target die Payload nicht an Analytics weiter, wenn feststellt, dass eine Anforderung von einem Bot stammt, und es wird kein mod_stats -Ereignis in der Datei [!DNL Target] Protokolle. Vor dieser Version leiteten clientseitige A4T-Integrationen die Payload an [!DNL Analytics], selbst wenn sie als Bot-Traffic identifiziert worden war. Diese Inkonsistenz zwischen Server- und Client-Seite würde zu Diskrepanzen führen, da A4T-Berichte für letztere den Bot-Traffic enthielten. Außerdem wurde Bot-Traffic nicht notwendigerweise identifiziert oder gekennzeichnet, was bedeutet, dass es nicht möglich war, den Bot-Traffic vom Rest des Traffics zu trennen oder zu entfernen. Und selbst wenn ein Kunde Bot-Traffic allein berücksichtigt, würde dies nicht notwendigerweise mit dem Traffic übereinstimmen, der [!DNL Target] als Bot-Traffic identifiziert und ausgeschlossen werden, was zu Spaltdiskrepanzen oder anderen Problemen führt. Mit dieser Version wurde die clientseitige Protokollierung von A4T verbessert, sodass das Verhalten in Bezug auf die A4T-Payload dasselbe ist wie bei der serverseitigen A4T-Protokollierung: Besucher, die als Bots identifiziert werden, sind von [!DNL Target] Zählung/Berichterstellung für Server- und Client-seitige Implementierungen. |


## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
