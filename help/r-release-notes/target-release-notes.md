---
keywords: Versionshinweise;Versionen;Updates;Zukünftige Versionen;Verbesserungen;Neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: ' Versionshinweise '
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 20%

---

# Versionshinweise zu Target (Vorabversion)

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 16. April 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Ab dem 31. März 2021 wird die Bibliothek &quot;mbox.js&quot; [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;in Würde fehl und wirken sich auf Ihre Seiten aus, deren Aktivitäten [!DNL Target] ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek at.js. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

## Target Standard/Premium 21.4.1 (19. April 2021)

Diese Version enthält die folgenden neuen Funktionen und Erweiterungen. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| Unterstützung von Entscheidungen auf dem Gerät für &quot;at.js&quot; | Die geräteinterne Entscheidungsfindung ermöglicht es Marketingexperten und Entwicklern, Experimente und Personalisierungen im Browser eines Benutzers mit einer Latenz von nahezu null zu ermöglichen.<br>Weitere Informationen finden Sie unter  [Gerätebezogene Entscheidungsfindung für &quot;at.js&quot;.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)<br>(Datum der Bekanntgabe) |
| ![](/help/assets/premium.png) PremiumList-basierte Operatoren für Entitäts-Filterregeln | [!DNL Target Recommendations] unterstützt neue Liste-basierte Operatoren für Entitätsfilterregeln. (TGT-39234)<br>Neu hinzugefügte Operatoren umfassen:<br><ul><li>in Liste</li><li>ist nicht in der Liste enthalten</li><li>Liste enthält ein Element in</li><li>Liste enthält kein Element in</li><li>Liste enthält alle Elemente in</li><li>Liste enthält nicht alle Elemente in</li></ul>Weitere Informationen finden Sie unter &quot;Verfügbare Operatoren&quot;in [Dynamische und statische Inklusionsregeln verwenden](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Diese Version enthält die folgenden Fehlerbehebungen.

* Es wurde ein Fehler behoben, der dazu führte, dass eine Aktivität nach dem Ändern der Audience in [!UICONTROL Alle Besucher] nicht synchronisiert werden konnte. (TGT-40259)
* Es wurde ein Fehler behoben, der verhinderte, dass Angebot dupliziert wurden, wenn sie an verschiedenen Stellen in den [!UICONTROL Automated Personalization]-Aktivitäten verwendet wurden, obwohl die Option [!UICONTROL Duplikat nicht zulassen] aktiviert war. (TGT-39567)
* Es wurde ein Fehler behoben, der verhinderte, dass die Seite [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] ordnungsgemäß geladen wurde. (TGT-39918)
* Es wurde ein Fehler behoben, der dazu führte, dass Eigenschaften dem falschen Arbeitsbereich zugeordnet wurden. (TGT-39869)
* Es wurde ein Problem behoben, das zu unbegrenztem Laden führte, wenn die Anforderung nach dem Ändern der Umgebung beim Erstellen eines Empfehlungsausschlusses fehlschlug. (TGT-39948)

## at.js Version 2.5.0 (Datum der Bekanntgabe)

Diese Version von at.js umfasst die folgenden Erweiterungen und Änderungen:

* [Unterstützung von ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) Entscheidungen auf dem Gerät für &quot;at.js&quot;.
* [Unterstützung ](/help/c-activities/c-activity-qa/activity-qa.md) von Vorschauen für Automated Personalization-Aktivitäten

Mit dieser Version wird auch die Unterstützung für Microsoft Internet Explorer 10 und höher entfernt.

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
