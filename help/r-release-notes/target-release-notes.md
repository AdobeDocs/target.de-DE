---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 7336522ab5fbe96b887b990437de105a579d9fd8
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 86%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 6. Januar 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 22.1.1 (6. Januar 2022)

Diese Version enthält die folgende neue Funktion:

| Funktion | Details |
| --- | --- |
| Angebotsentscheidungen in [!DNL Target] activities | Sie können jetzt [!DNL Adobe Journey Optimizer] Angebotsentscheidungen in [!DNL Target] [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten, um das nächste beste Angebot für Ihre Besucher im Web und auf Mobilgeräten zu ermitteln und bereitzustellen.<br>Weitere Informationen finden Sie unter [Angebotsentscheidungen verwenden](/help/c-integrating-target-with-mac/ajo/offer-decision.md).<br>**Hinweis**: Diese Funktion steht für [!DNL Target] Kunden, die auch Zugriff auf Offer decisioning haben und über eine [!DNL Target] Implementierung basierend auf dem Adobe Experience Platform Web SDK. |

## at.js-Version 2.7.0 (28. Oktober 2021)

Diese Version enthält die folgende Verbesserung:

* Hinzugefügte Unterstützung für [Web-Komponenten](https://developer.mozilla.org/de/docs/Web/Web_Components). Diese Version von at.js ist erforderlich, um personalisierte Erlebnisse und Angebote für benutzerdefinierte Elemente und Elemente innerhalb von benutzerdefinierten Elementen zu erstellen und zu testen. Diese Funktion ist in der Version 21.10.5 von [!DNL Target Standard/Premium] enthalten.

## [!DNL Target Standard/Premium] 21.10.5 (28. Oktober 2021)

Diese Wartungsversion enthält die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Hinzugefügte Unterstützung für [Web-Komponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Personalisierte Erlebnisse und Angebote können mit benutzerdefinierten Elementen und Elementen innerhalb von benutzerdefinierten Elementen erstellt und getestet werden.<br>Weitere Informationen finden Sie unter [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

## [!DNL Target Standard/Premium] 21.10.4 (21. Oktober 2021)

Diese Wartungsversion enthält die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| Warenkorbbasierte Empfehlungen | Eine neue Reihe von Algorithmen wurde hinzugefügt, um Empfehlungen basierend auf dem Inhalt des Warenkorbs des Besuchers bereitzustellen.<br>Weitere Informationen finden Sie unter „Warenkorbbasiert“ in [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) und unter „Warenkorbhinzufügungen/Warenkorbansichten/Checkout-Seiten“ und „Artikel ausschließen, die sich bereits im Warenkorb des Besuchers befinden“ in [Planen und Implementieren von Empfehlungen](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19. Oktober 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen:

* Es wurden Probleme behoben, die Kunden daran hinderten, das [!UICONTROL A4T]-Bedienfeld in [!DNL Analysis Workspace] zu öffnen, indem sie auf die Schaltfläche [!UICONTROL In Analytics anzeigen] in der [!DNL Target]-Aktivitätsberichterstattung klickten. (TGT-42099, TGT-42100)
* Es wurde ein Problem behoben, das dazu führte, dass die Schaltfläche [!UICONTROL Entwurf bearbeiten] beim Bearbeiten von [!UICONTROL A/B-Test]- und [!UICONTROL Experience Targeting] (XT)-Aktivitäten mit dem [!UICONTROL formularbasierten Experience Composer] nicht angezeigt wurde. (TGT-41980)
* Es wurde ein Problem behoben, das verhinderte, dass das Kontrollkästchen [!UICONTROL Kompatibel] in der Kriterienauswahl beim Erstellen einer neuen [!UICONTROL Recommendations]-Aktivität angezeigt wurde. (TGT-42053)
* Es wurde eine falsche Fehlermeldung behoben, die angezeigt wurde, wenn [!DNL Analytics] als Berichtsquelle (A4T) aufgrund fehlender [!DNL Analytics]-Berechtigungen nicht ausgewählt werden konnte. (TGT-41954)
* Es wurden mehrere Korrekturen zur Verbesserung der Tastaturnavigation auf der gesamten [!DNL Target]-Benutzeroberfläche vorgenommen.

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
