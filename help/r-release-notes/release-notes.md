---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Erweiterungen, Fehlerbehebungen und bekannten Problemen in jeder Target Standard- und Target Premium-Version.
keywords: Versionshinweise; Vorabversion
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
seo-title: Versionshinweise zu Adobe Target (aktuell)
solution: Target
title: Target-Versionshinweise (aktuell)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: e1174aacc5610878c8671e88fbd20d51fedffe6c

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version.

## Mitteilungen

**31. Juli 2019**

[!UICONTROL Mit Unternehmensberechtigungen] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen. The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although this feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until the [!DNL Target] February 2019 release. Adobe hat die Admin-apis aktualisiert, damit Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. So, while earlier, Admin APIs were restricted to the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

**Erforderliche Aktion**: Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihre vorhandene Adobe I/O-Integration für alle Arbeitsbereiche mit der gewünschten Rolle bereitstellen. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of the role selected from the [!UICONTROL Product Role] drop-down list. In der kommenden Version können Sie jetzt die gewünschte Rolle auswählen.

This action should be performed during the month of **August 2019**. After the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. Es gibt keine negativen Auswirkungen auf die Einrichtung von Integrationsrollen im Voraus.

For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.7.1 (24. Juli 2019) {#tgt-19-7-1}

Dieses Release umfasst die folgenden neuen Funktionen und Erweiterungen:

(Die Ausgabennummern in Klammern dienen internen Adobe-Benutzern.)

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer für mobile Apps | In der mobilen App-VEC wird ein neues Bedienfeld "Änderungen" angezeigt, in dem die Elemente angezeigt werden, die Sie für die Klick-Tracking eingerichtet haben. (TGT-31741)<br> See [Set up click tracking in the Mobile App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md). |
| ![Premium badgerecommenüationen](/help/assets/premium.png)<br>in A/B-Test- und Erlebnis-Targeting (XT)-Aktivitäten | Der Recommendations-Angebotsstatus (Algorithmus) wird auf der Seite Überblick für A/B-Test- und XT-Aktivitäten angezeigt, die Recommendations-Angebote enthalten. Zu den Status gehören: Ergebnisse bereit, Ergebnisse nicht bereit und Feed-Fehler. (TGT-33649)<br>See [Recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md#status). |
| Unterstützung domänenübergreifender Tracking-Unterstützung für at. js 2.0 + über die Experience Cloud ID (ECID)-Bibliothek | Zuvor wurde die domänenübergreifende Verfolgung in at. js 2 nicht unterstützt.*x*. Mit dieser Version können Kunden, die at. js 2.0 oder höher verwenden, jetzt domänenübergreifende Verfolgung über die ECID-Bibliothek nutzen. Die ECID-Bibliothek muss zusammen mit at. js 2.0 oder höher auf der Seite installiert sein, damit die domänenübergreifende Verfolgung funktioniert. [Die Experience Cloud ID-Bibliothek 4.3.0 +](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) muss verwendet werden.<br>Siehe [domänenübergreifende Verfolgung in at. js 2. x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain). |
| Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID (ECID)-Bibliothek 4.3 | Target-Kunden können die Apple ITP 2.1 und ITP 2.2 heute durch Nutzung des CNAME-Zertifizierungsprogramms von Adobe abschwächen.<br>Mit dieser Version führt Target eine nahtlose Integration in die ECID-Bibliothek 4.3 ein, die ein serverseitiges Cookie nutzt, um ITP 2.1 und ITP 2.2 zu reduzieren. Es wird dringend empfohlen, Target-Kunden in Verbindung mit der javascript-Bibliothek von Target die [ECID-Bibliothek 4.3 bereitzustellen](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) , um zukünftige ITP-Versionen abzuschwächen. Die ECID-Bibliothek wird weiterhin Verbesserungen an der Entwicklung vornehmen, die eine robuste Lösung für die sich ständig ändernden Cookie-Richtlinien bereitstellen, die von Browsern eingeführt wurden.<br>Siehe [Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md). |

**Verbesserungen, Fehlerbehebungen und Änderungen**

* Es wurde ein Fehler behoben, der verhinderte, dass in Recommendations-Aktivitäten Ausschlusswerte gelöscht wurden, wenn doppelte Werte hinzugefügt wurden. (TGT-34996)
* Sie können nun einen Entwurf in einer Recommendations-Aktivität aus der Targeting-Seite entfernen (Schritt 2 des dreiteiligen geleiteten Arbeitsablaufs). Zum Entfernen eines Entwurfs müssen mehrere Entwürfe ausgewählt sein. (TGT-35118)
* Es wurde ein Problem behoben, durch das benutzerdefinierte Kriterienkarten einige Kunden nicht ordnungsgemäß in der Target-Benutzeroberfläche geladen oder bearbeitet werden konnten. (TGT-35170)

## at. js Version 2.1.1 (24. Juli 2019)

Diese Version von at. js ist ein Maintenance Release und enthält die folgenden Erweiterungen und Fehlerbehebungen:

(Die Ausgabennummern in Klammern dienen internen Adobe-Benutzern.)

* Es wurde ein Problem behoben, durch das mehrere Beacons ausgelöst wurden, wenn die Klick-Tracking-Metrik auf der Seite Ziele und Einstellungen im Visual Experience Composer (VEC) verwendet wurde. (TNT-32812)
* Fixed an issue that caused `triggerView()` to not render offers more than once. (TNT-32780)
* Fixed an issue with `triggerView()` to ensure that the request contains Marketing Cloud ID (MCID) information. (TNT-32776)
* Fixed an issue that prevented the `triggerView()` notification to fire even if there are no saved views. (TNT-32614)
* Es wurde ein Fehler behoben, der aufgrund der Verwendung von decodeuricomponent zu Fehlern führte, die zu Problemen führte, wenn die URL einen falsch formatierten Abfragezeichenfolgenparameter enthielt. (TNT-32710)
* The beacon flag is now set to "true" in the context of delivery requests sent via the `Navigator.sendBeacon()` API. (TNT-32683)
* Es wurde ein Problem behoben, durch das Recommendations-Angebote nicht auf Websites für einige wenige Kunden angezeigt wurden. Kunden könnten den Angebotsinhalt im Bereitstellungs-API-Aufruf sehen, das Angebot wurde jedoch nicht auf der Website angewendet. (TNT-32680)
* Es wurde ein Problem behoben, durch das die Klick-Tracking über mehrere Erlebnisse nicht wie erwartet funktionierte. (TNT-32644)
* Es wurde ein Problem behoben, durch das at. js die zweite Metrik nach dem Rendern der ersten Metrik nicht mehr anwenden konnte. (TNT-32628)
* Fixed an issue when passing `mboxThirdPartyId` using the `targetPageParams` function that caused the request payload to not be present in either the query parameters or in the request payload. (TNT-32613)
* Es wurde ein Problem behoben, durch das die Antworten zur Anzeige und zum Klicken auf die Benachrichtigungsbenachrichtigungen in Chromium-basierten Browsern blockiert wurden (einschließlich Google Chrome). (TNT-32290)

For information about this and previous versions of at.js, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://marketing.adobe.com/resources/help/en_US/whatsnew/). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |