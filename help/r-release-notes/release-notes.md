---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 95fdb1dcee873f7a414a3aecdc363fca2b621c01
workflow-type: ht
source-wordcount: '692'
ht-degree: 100%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs, der [!DNL Adobe Experience Platform Web SDK] und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek „at.js“, um mögliche Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## at.js 2.6.1 (16. August 2021)

* Fehlerbehebung für „Für den Hybrid-Modus ist kein zwischengespeichertes Artefakt verfügbar“ bei Verwendung der geräteinternen Entscheidungsfindung.

## [!DNL Target] node.js SDK 2.2.0 (11. August 2021)

* Ergänzung der Datenerfassung von SDK-Telemetriedaten
* Automatisierung von API-Client „openapi-codegen“ für die Bereitstellung

Weitere Informationen zu dieser Version sowie zu vorherigen Versionen finden Sie im [Änderungsprotokoll](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md) in der [Dokumentation zur Bibliothek node.js vom Target-SDK](https://github.com/adobe/target-nodejs-sdk) auf GitHub.

## [!DNL Target Standard/Premium] 21.8.1 (10. August 2021)

Diese Wartungsversion enthält viele Backend-Verbesserungen einschließlich der folgenden kundenrelevanten Änderung:

* Es wurde ein Fehler behoben, der dazu führte, dass Berichte für Aktivitäten mit [!UICONTROL automatisierter Personalisierung], die im [!UICONTROL formularbasierten Experience Composer] erstellt wurden, in Berichten auf gelöschte Angebote verweisen. Dieses Problem führte zur Anzeige der folgenden Fehlermeldung: „Wir haben Probleme beim Abrufen der Daten für diesen Bericht. Wenden Sie sich an den Kundendienst von Adobe, wenn das Problem weiterhin besteht.“ (TGT-41028)

## [!DNL Target Delivery API] (3. August 2021)

Diese Version umfasst die folgenden Verbesserungen:

* Die Beschränkung für mBox-Parameter wurde auf 100 Parameter erhöht. Zuvor waren maximal 50 Parameter zulässig. (TNT-41717)
* Die Beschränkung für `categoryId` wurde auf 256 Zeichen erhöht. Zuvor waren maximal 128 Zeichen zulässig.
* Die folgenden Details von [!DNL Adobe Audience Manager] (AAM) wurden zur Bereitstellungs-API hinzugefügt:

   * AAM UUID: Die interne AAM-ID, die zur eindeutigen Identifizierung eines Benutzers verwendet wird.
   * dataPartnerId: Die ID für einen Datenpartner.
   * dataPartnerUserId: Die von einem Datenpartner bereitgestellte Benutzer-ID.

   Zuvor umfasste die Bereitstellungs-API nur `dcsLocationHint` und `blob`. (TNT-41644)

## at.js 2.6.0 (27. Juli 2021)

* Das Attribut „secure“ wurde zu Cookies hinzugefügt für alle Fälle, in denen die at.js-Einstellungen `secureOnly` auf `true` gesetzt sind.
* Bei Verwendung von `triggerView()` sind jetzt Antwort-Token verfügbar.
* Es wurde ein Problem im Zusammenhang mit dem Ereignis `CONTENT_RENDERING_NO_OFFERS` behoben. Jetzt wird dieses Ereignis korrekt ausgelöst, wenn kein Inhalt von [!DNL Target] zurückgegeben wird.
* Details zur Klickmetrik von [!DNL Analytics for Target] (A4T) werden bei der Verwendung von `prefetch`-Anfragen korrekt zurückgegeben.
* Die UUID-Generierung verwendet nicht mehr `Math.random()`, sondern beruht auf `window.crypto`.
* Der Ablauf des `sessionId`-Cookies wird bei jedem Netzwerkaufruf korrekt verlängert.
* Die Ansichts-Cache-Initialisierung für die [!UICONTROL Einzelseiten-Anwendung] (SPA, Single Page Application) wird jetzt korrekt verarbeitet und berücksichtigt die Einstellungen `viewsEnable`.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority-Produktaktualisierung | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
