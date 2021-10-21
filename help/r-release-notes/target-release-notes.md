---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 962464a98f2a7771525d432ba1b51c828f5a8df6
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 57%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am: 20. Oktober 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.10.4 (21. Oktober 2021)

Dieses Maintenance Release enthält die folgende Erweiterung:

| Funktion | Details |
| --- | --- |
| Warenkorb-basiertes Recommendations | Es wurde eine neue Reihe von Algorithmen hinzugefügt, um Empfehlungen basierend auf dem Inhalt des Warenkorbs des Besuchers zu senden.<br>Weitere Informationen finden Sie unter &quot;Warenkorb-basiert&quot; in [Kriterien erstellen](/help/c-recommendations/c-algorithms/create-new-algorithm.md) und &quot;Warenkorb-/Warenkorb-Ansichten/Checkout-Seiten&quot; und &quot;Bereits im Warenkorb des Besuchers befindliche Elemente ausschließen&quot; in [Recommendations planen und umsetzen](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19. Oktober 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen:

* Behobene Probleme, die das Öffnen von Kunden verhinderten [!UICONTROL A4T] Bereich in [!DNL Analysis Workspace] durch Klicken auf [!UICONTROL Ansicht in Analytics] Schaltfläche in [!DNL Target] Aktivität Berichte. (TGT-42099, TGT-42100)
* Es wurde ein Problem behoben, das [!UICONTROL Entwurf bearbeiten] Schaltfläche, die während der Bearbeitung nicht angezeigt wird [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten mit [!UICONTROL Formularbasierter Experience Composer]. (TGT-41980)
* Es wurde ein Problem behoben, durch das [!UICONTROL Kompatibel] Kontrollkästchen bei der Anzeige in der Kriterienauswahl beim Erstellen eines neuen [!UICONTROL Recommendations] Aktivität. (TGT-42053)
* Es wurde eine fehlerhafte Fehlermeldung behoben, die angezeigt wurde, wenn die Auswahl nicht möglich war [!DNL Analytics] als Berichte-Quelle (A4T) aufgrund des Fehlens von [!DNL Analytics] Berechtigungen. (TGT-41954)
* Mehrere Barrierefreiheitskorrekturen implementiert, um die Navigation über die Tastatur zu verbessern [!DNL Target] UI.

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
