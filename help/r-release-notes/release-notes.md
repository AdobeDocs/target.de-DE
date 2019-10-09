---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Erweiterungen, Fehlerbehebungen und bekannten Problemen in jeder Target Standard- und Target Premium-Version.
keywords: Versionshinweise;Neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
seo-title: 'Adobe Target-Versionshinweise (aktuell) '
solution: Target
title: Target-Versionshinweise (aktuell)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 71d94ef5d2351dc8410c0d418096088a0a900f03

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Target-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

## Target-Plattform (9. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Node.js SDK Version 1.0 | Mit dem SDK "Target Node.js"können Sie Target serverseitig bereitstellen.<br>Dieses Node.js-SDK unterstützt Sie bei der einfachen Integration von Target in andere Experience Cloud-Lösungen, z. B. den Adobe Experience Cloud-Identitätsdienst, Adobe Analytics und Adobe Audience Manager.<br>Das Node.js-SDK stellt Best Practices vor und entfernt Komplexitäten, wenn es über unsere Bereitstellungs-API mit Adobe Target integriert wird, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können. Die folgenden bemerkenswerten Funktionen werden in der neuesten Version eingeführt:<ul><li>Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen.</li><li>Unterstützung für die Leistungsoptimierung, wenn Sie eine hybride Integration von Target sowohl auf Ihren Webseiten als auch serverseitig haben. Wir führen eine Einstellung ein, die von Erlebnissen aufgefüllt wird, die über den Server abgerufen werden, sodass at.js 2.2 keinen zusätzlichen Server-Aufruf mehr vornimmt, um die Erlebnisse abzurufen. `serverState` Dieser Ansatz optimiert die Seitenladeleistung.</li><li> Unterstützung für das Abrufen von VEC-erstellten Aktivitäten über das Node.js SDK, das durch die neue API für die Auslieferung ermöglicht wird.</li><li>Open Source, damit Ihre Entwickler zum Node.js SDK beitragen können.</li></ul><br>Weitere Informationen finden Sie unter [Versionshinweise - SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)für Target Node.js. |
| Auslieferungs-API | Ein vollständig neuer API-Endpunkt (/v1/delivery) ist in der Produktion verfügbar. Die wichtigsten Funktionen sind:<ul><li>Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.</li><li>Rufen Sie VEC-erstellte Aktivitäten über die API ab.</li><li>Unterstützung für ein völlig neues Objekt namens "Ansichten", das für Einzelseitenanwendungen (SPAs) und mobile Anwendungen verwendet wird.</li></ul><br>Weitere Informationen finden Sie unter [Versionshinweise - Serverseitige Target-APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |

## Target Standard/Premium 19.9.2 (30. September 2019)

Dieser Maintenance Release enthält die folgende Verbesserung:

* Verschiedene Korrekturen von Sicherheitsfehlern, einschließlich eines Sicherheits-Updates für den Rich-Text-Editor (RTE) im Visual Experience Composer (VEC). (TGT-35383)
* Recommendations-Angebote können jetzt neben DIV auch anderen Elementen als DIV (z. B. P, UL, H1) in A/B-Test- und Erlebnis-Targeting-Aktivitäten hinzugefügt werden. (TGT-34333)
* Ereignisbenachrichtigungen (das Glockensymbol in der Target-Benutzeroberfläche) sind nicht mehr verfügbar. Die Benachrichtigungen werden demnächst neu angezeigt.

## Target Standard/Premium 19.9.1 (10. September 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) für Unternehmen | Mit der Version Target September 2019 bieten Enterprise Permissions Kunden die folgenden Zugriffssteuerungen:<UL><li>Sie können die Arbeitsbereiche auswählen, auf die die Integration angewendet werden kann.</li><li>Sie können der Adobe I/O-Integration eine Rolle zuweisen: Genehmiger, Bearbeiter oder Beobachter.</li></ul>Schrittweise Anleitungen und weitere Informationen finden Sie unter [Gewähren von Zugriff von Adobe I/O Integrationen auf Arbeitsbereiche und Zuweisen von Rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - Target-serverseitige APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu den serverseitigen APIs von Adobe Target. |
| [Versionshinweise - SDK für Target Node.js](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK Node.js. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der JavaScript-Bibliothek von Adobe Target "at.js". |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek "mbox.js"nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
