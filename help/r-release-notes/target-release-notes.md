---
keywords: Versionshinweise;Versionen;Updates;Zukünftige Versionen;Verbesserungen;Neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: ' Versionshinweise '
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: a45cfbd52df935fa3138eda6cc7f1028c13ff81d
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 24%

---

# Versionshinweise zu Target (Vorabversion)

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 9. April 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Ab dem 31. März 2021 wird die Bibliothek &quot;mbox.js&quot; [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;in Würde fehl und wirken sich auf Ihre Seiten aus, deren Aktivitäten [!DNL Target] ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek at.js. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

## Target Standard/Premium 21.4.1 (19. April 2021)

Diese Version enthält die folgenden neuen Funktionen. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| Unterstützung von Entscheidungen auf dem Gerät für &quot;at.js&quot; | Die geräteinterne Entscheidungsfindung ermöglicht es Marketingexperten und Entwicklern, Experimente und Personalisierungen im Browser eines Benutzers mit einer Latenz von nahezu null zu ermöglichen. |

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen.

* Es wurde ein Fehler behoben, der dazu führte, dass eine Aktivität nach dem Ändern der Audience in [!UICONTROL Alle Besucher] nicht synchronisiert werden konnte. (TGT-40259)
* Es wurde ein Fehler behoben, der verhinderte, dass Angebot dupliziert wurden, wenn sie an verschiedenen Stellen in den [!UICONTROL Automated Personalization]-Aktivitäten verwendet wurden, obwohl die Option [!UICONTROL Duplikat nicht zulassen] aktiviert war. (TGT-39567)
* Es wurde ein Fehler behoben, der verhinderte, dass die Seite [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] ordnungsgemäß geladen wurde. (TGT-39918)
* Es wurde ein Fehler behoben, der dazu führte, dass Eigenschaften dem falschen Arbeitsbereich zugeordnet wurden. (TGT-39869)
* [!DNL Target Recommendations] unterstützt neue Liste-basierte Operatoren für Entitätsfilterregeln. (TGT-39234)

   Neu hinzugefügte Operatoren umfassen:

   * in Liste
   * ist nicht in der Liste enthalten
   * Liste enthält ein Element in
   * Liste enthält kein Element in
   * Liste enthält alle Elemente in
   * Liste enthält nicht alle Elemente in

* Es wurde ein Problem behoben, das zu unbegrenztem Laden führte, wenn die Anforderung nach dem Ändern der Umgebung beim Erstellen eines Empfehlungsausschlusses fehlschlug. (TGT-39948)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
