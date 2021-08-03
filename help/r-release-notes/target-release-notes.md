---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Versionshinweise
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: ade66cbef912bcf4de5d43aebf5c3bc79e92a30e
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 61%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 3. August 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.8.1 (4. August 2021)

Diese Wartungsversion enthält viele Backend-Verbesserungen, einschließlich der folgenden kundenrelevanten Änderung:

* Es wurde ein Fehler behoben, der dazu führte, dass Berichte für [!UICONTROL Automatisierte Personalisierung]-Aktivitäten, die im [!UICONTROL Form-Based Experience Composer] erstellt wurden, auf gelöschte Angebote in Berichten verweisen. Diese Ausgabe führte zur Anzeige der folgenden Fehlermeldung: &quot;Wir haben Probleme beim Abrufen der Daten für diesen Bericht. Wenden Sie sich an den Kundendienst von Adobe , wenn das Problem weiterhin besteht.&quot; (TGT-41028)

## Target-Bereitstellungs-API (3. August 2021)

Diese Version enthält die folgenden Verbesserungen:

* Die Beschränkung für Mbox-Parameter wurde auf 100 Parameter erhöht. Die vorherige Begrenzung betrug 50 Parameter. (TNT-41717)
* Die Beschränkung für `categoryId` wurde auf 256 Zeichen erhöht. Die vorherige Beschränkung betrug 128 Zeichen.
* Die folgenden [!DNL Adobe Audience Manager] (AAM) Details wurden zur Bereitstellungs-API hinzugefügt:

   * AAM UUID (Adobe Audience Manager Unique User ID)
   * dataPartnerId
   * dataPartnerUserId

   Zuvor umfasste die Bereitstellungs-API nur `dcsLocationHint` und `blob`. (TNT-41644)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
