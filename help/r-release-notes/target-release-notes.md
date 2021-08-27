---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: afa370a38921ab76babf5e49edc1e4b23ee807b0
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 99%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 24. August 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.8.1 (10. August 2021)

Diese Wartungsversion enthält viele Backend-Verbesserungen einschließlich der folgenden kundenrelevanten Änderung:

* Es wurde ein Fehler behoben, der dazu führte, dass Berichte für Aktivitäten mit [!UICONTROL automatisierter Personalisierung], die im [!UICONTROL formularbasierten Experience Composer] erstellt wurden, in Berichten auf gelöschte Angebote verweisen. Dieses Problem führte zur Anzeige der folgenden Fehlermeldung: „Wir haben Probleme beim Abrufen der Daten für diesen Bericht. Wenden Sie sich an den Kundendienst von Adobe, wenn das Problem weiterhin besteht.“ (TGT-41028)

## Target-Bereitstellungs-API (3. August 2021)

Diese Version umfasst die folgenden Verbesserungen:

* Die Beschränkung für mBox-Parameter wurde auf 100 Parameter erhöht. Zuvor waren maximal 50 Parameter zulässig. (TNT-41717)
* Die Beschränkung für `categoryId` wurde auf 256 Zeichen erhöht. Zuvor waren maximal 128 Zeichen zulässig.
* Die folgenden Details von [!DNL Adobe Audience Manager] (AAM) wurden zur Bereitstellungs-API hinzugefügt:

   * AAM UUID: Die interne AAM-ID, die zur eindeutigen Identifizierung eines Benutzers verwendet wird.
   * dataPartnerId: Die ID für einen Datenpartner.
   * dataPartnerUserId: Die von einem Datenpartner bereitgestellte Benutzer-ID.

   Zuvor umfasste die Bereitstellungs-API nur `dcsLocationHint` und `blob`. (TNT-41644)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
