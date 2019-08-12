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
source-git-commit: 2588a7c251e58193b969d57f91a7c3f640318fbf

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version.

## Mitteilungen

**31. Juli 2019**

[!UICONTROL Mit Unternehmensberechtigungen] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen. Mit der [!UICONTROL Funktion für Unternehmensberechtigungen] können optimierte Optimierungsprogramme für Teams optimiert werden. Obwohl diese Funktion in der [!DNL Target] Benutzeroberfläche verfügbar war, konnten die Admin-apis bis zum Release [!DNL Target] von Februar 2019 die entsprechende Unterstützung ablesen. Adobe hat die Admin-apis aktualisiert, damit Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. Zuvor waren Admin-apis also auf den Standardarbeitsbereich beschränkt. Das Update vom Februar 2019 ermöglichte den Zugriff auf alle Arbeitsbereiche mit [!UICONTROL dem Genehmigerzugriff.]

Ab der neuen [!DNL Target] Version September 2019 [!UICONTROL stehen Kunden die folgenden] Zugriffssteuerungsmöglichkeiten zur Verfügung:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* Sie können eine Rolle auf die Integration von Adobe I/O anwenden: [!UICONTROL Genehmigende Person], [!UICONTROL Editor]oder [!UICONTROL Beobachter].

**Erforderliche Aktion**: Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihre vorhandene Adobe I/O-Integration für alle Arbeitsbereiche mit der gewünschten Rolle bereitstellen. Vor der September-Version wurden alle Integrationen, die mit [!UICONTROL dem Genehmiger ausgeführt wurden,] unabhängig von der Rolle, die in der Dropdownliste [!UICONTROL "Produktrolle] " ausgewählt wurde, verwendet. In der kommenden Version können Sie jetzt die gewünschte Rolle auswählen.

Diese Aktion sollte im **August 2019** durchgeführt werden. Nach der Version [!DNL Target] vom September 2019 werden die Zugriffssteuerungselemente aktiviert und Sie werden nur auf den Standardarbeitsbereich zugreifen, wenn Sie aktuell eingerichtet sind. Es gibt keine negativen Auswirkungen auf die Einrichtung von Integrationsrollen im Voraus.

Schrittweise Anweisungen und weitere Informationen finden Sie unter [Gewähren von Adobe I/O-Integrationen auf Arbeitsflächen und Zuweisen von Rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Mobile VEC SDK ios 2.1.0 &amp; Android 1.1.1 (7. August 2019)

Dieses Release von Mobile VEC SDK umfasst die folgenden Erweiterungen und Fehlerbehebungen:

(Die Ausgabennummern in Klammern dienen internen Adobe-Benutzern.)

* Unterstützung für Vorschau für visuelle Aktivitäten auf Mobilgeräten hinzugefügt. (TGT-27875)
* Es wurde ein Problem behoben, durch das aufgrund `UIImagePickerController` der Verwendung eine Apple Standard-Verletzung verursacht wurde.
* Die GSON-Abhängigkeit von Android SDK wurde entfernt. (TGT-31710)
* Andere redundante Gradle-Abhängigkeiten wurden entfernt (TGT -35479)
* Es wurde ein Problem behoben, durch das das Bereitstellungsangebot zum Zeitpunkt des Authoring nicht zurückgesetzt wurde. (TGT-35270)

## Target Standard/Premium 19.7.1 (24. Juli 2019) {#tgt-19-7-1}

Dieses Release umfasst die folgenden neuen Funktionen und Erweiterungen:

(Die Ausgabennummern in Klammern dienen internen Adobe-Benutzern.)

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer für mobile Apps | In der mobilen App-VEC wird ein neues Bedienfeld "Änderungen" angezeigt, in dem die Elemente angezeigt werden, die Sie für die Klick-Tracking eingerichtet haben. (TGT -31741)<br> Siehe [Einrichten der Klick-Verfolgung in der Mobile App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md). |
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
* Es wurde ein Problem behoben, durch das `triggerView()` Angebote nicht mehr als einmal gerendert wurden. (TNT-32780)
* Es wurde ein Problem behoben, `triggerView()` durch das die Anforderung Marketing Cloud ID (MCID)-Informationen enthält. (TNT-32776)
* Es wurde ein Problem behoben, durch das `triggerView()` die Benachrichtigung auch dann ausgelöst wurde, wenn keine gespeicherten Ansichten vorhanden waren. (TNT-32614)
* Es wurde ein Fehler behoben, der aufgrund der Verwendung von decodeuricomponent zu Fehlern führte, die zu Problemen führte, wenn die URL einen falsch formatierten Abfragezeichenfolgenparameter enthielt. (TNT-32710)
* Das Beacon-Flag ist nun im Kontext der über die `Navigator.sendBeacon()` API gesendeten Versandanforderungen auf "true" gesetzt. (TNT-32683)
* Es wurde ein Problem behoben, durch das Recommendations-Angebote nicht auf Websites für einige wenige Kunden angezeigt wurden. Kunden könnten den Angebotsinhalt im Bereitstellungs-API-Aufruf sehen, das Angebot wurde jedoch nicht auf der Website angewendet. (TNT-32680)
* Es wurde ein Problem behoben, durch das die Klick-Tracking über mehrere Erlebnisse nicht wie erwartet funktionierte. (TNT-32644)
* Es wurde ein Problem behoben, durch das at. js die zweite Metrik nach dem Rendern der ersten Metrik nicht mehr anwenden konnte. (TNT-32628)
* Es wurde ein Problem behoben, das beim Weiterleiten `mboxThirdPartyId` mit der `targetPageParams` Funktion auftrat, die dazu führte, dass die Nutzlast der Anforderung weder in den Abfrageparametern noch in der Nutzlast der Anforderung vorhanden war. (TNT-32613)
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
