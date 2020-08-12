---
keywords: tls;tls 1.0;transport layer security;encryption;tls 1.1;tls 1.2
description: Informationen zu Änderungen in Bezug auf die Verwendung von TLS (Transport Layer Security), die durch Adobe und Target vorgenommen werden, um den höchsten Sicherheitsstandards gerecht zu werden und die Sicherheit von Kundendaten zu fördern.
title: Änderungen der TLS-Verschlüsselung (Transport Layer Security)
feature: null
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 60%

---


# Änderungen der TLS-Verschlüsselung (Transport Layer Security){#tls-transport-layer-security-encryption-changes}

Information about changes to how Adobe and Adobe Target use TLS (Transport Layer Security) to maintain the highest security standards and promote the safety of customer data.

Transport Layer Security (TLS) ist das am weitesten verbreitete Sicherheitsprotokoll, das aktuell in Webbrowsern und anderen Anwendungen Verwendung findet, bei denen über ein Netzwerk übertragene Daten geschützt werden müssen. Um die Sicherheitsstandards von Adobe einzuhalten, muss die Unterstützung für ältere Protokolle beendet und durch TLS 1.2 als obligatorisches Sicherheitsprotokoll ersetzt werden, damit die Daten durch die neueste und sicherste Version des Protokolls geschützt sind.

>[!IMPORTANT]
>
>Ab dem 1. März 2020 unterstützt Adobe Target keine TLS 1.1-Verschlüsselung mehr für Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), Aktivität Versand, APIs usw. Bitte aktualisieren Sie vor dem 1. März 2020 auf TLS 1.2, um Probleme zu vermeiden.

Wir gehen davon aus, dass dies keine wesentlichen Auswirkungen auf Kundendaten oder die Berichterstattung haben wird.

## Visual Experience Composer (VEC) mit aktiviertem Enhanced Experience Composer (EEC){#section_B374B62DEC3344C194AC7BECC2EE0AA0}

TLS 1.2 ist die Standardeinstellung ab dem 1. März 2020 und TLS 1.1 wird nicht mehr unterstützt.

Adobe führt TLS 1.2 schrittweise ein. Kunden, deren Domänen bereits mit 1.2 konform sind, müssen beim Übergang zu TLS 1.2 keine Änderungen vornehmen. Die meisten Kundendomänen unterstützen bereits TLS 1.2. Wenn Ihre Domäne TLS 1.2 nicht unterstützt, behalten wir diese Domänen wie heute (bis März 2020) bei TLS 1.1.

In dieser Übergangsphase sollten keine Probleme auftreten. Wenn der VEC eine Site, die zuvor funktioniert hat, nicht mehr lädt,  [senden Sie eine Anfrage an den Kundendienst](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie den Übergang zu TLS 1.2 als mögliche Ursache an.

Wenn Sie jedoch einer der Kunden sind, die TSL 1.1 nutzen, ohne TLS 1.2 zu unterstützen, sollten Sie den Umstieg Ihrer Domänen/Infrastruktur auf TLS 1.2 planen. Wir werden das TLS 1.1-Protokoll bis zum 1. März 2020 weiterhin unterstützen. Starting March 1, 2020, Target will not support the TLS 1.1 protocol to be used for the VEC via the Enhanced Experience Composer capability.

Auch wenn allen Kunden der Umstieg auf TLS 1.2 empfohlen wird – falls Sie als neuer Kunde TLS 1.2 *NICHT* unterstützen, teilen Sie dem Kundendienst mit, dass Sie TLS 1.1 für Enhanced Experience Composer verwenden müssen. However, please plan to move to TLS 1.2 as you will also not be supported beyond March 1, 2020.

## Activity delivery {#section_46CA5943E4354B259014C2BF340AECD6}

Ab dem 1. März 2020 wird TLS 1.1 nicht mehr von Zielgruppen-Servern unterstützt. Mit dieser Änderung akzeptieren Zielgruppen-Server keine Anfragen von Besuchern mit älteren Geräten oder Webbrowsern, die TLS 1.2 (oder höher) nicht unterstützen. Ältere Geräte und Browser, die nur TLS 1.1 unterstützen (oder standardmäßig TLS 1.1 unterstützen), erhalten daher keine Aktivitäten von Adobe Target. Standardinhalte der Site werden gerendert.

Zu den betroffenen älteren Geräten und Browsern gehören:

* Google Chrome (Chrome für Android), Versionen 29 und früher
* Opera Browser (Opera Mobile) Versionen 12.17 und früher
* Mozilla Firefox (Firefox für Mobilgeräte), Version 26 und früher
* Android 4.3 und frühere Versionen
* Internet Explorer 8 bis 10 unter Windows 7 und frühere Versionen
* Internet Explorer 10 unter Windows Phone 8.0
* Safari 6.0.4/OS X 10.8.4 und frühere Versionen

Beachten Sie bei der Planung dieser Änderung Folgendes (beachten Sie, dass die Frist vom 1. März 2020 alle diese Punkte betrifft):

* Sie müssen sicherstellen, dass Ihre Standardsite vorbereitet ist und auf kompatiblen Geräten und Browsern genutzt werden kann.
* Beachten Sie, dass die Anzahl der Besucher in Ihren Target-Berichten geringfügig zurückgehen kann.
* You might need to change audiences created specifically to target older devices or browsers that do not support TLS 1.2. Delivery to those devices and browsers will no longer work.

Weitere Informationen zu unterstützten Browsern und Versionen finden Sie unter  [Unterstützte Browser](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## Adobe Target-APIs {#section_88797FA5434049EC89F908853CC76903}

Ab dem 1. März 2020 unterstützen Zielgruppe-APIs keine TLS 1.1-Verschlüsselung mehr. Kunden, die auf die API zugreifen, sollten sicherstellen, dass sie nicht von den Auswirkungen betroffen sind.

* Für API-Clients, die Java 7 mit den Standardeinstellungen verwenden, sind Änderungen erforderlich, damit TLS 1.2 unterstützt wird. Weitere Informationen finden Sie unter „[Changing default TLS protocol version for client end points: TLS 1.0 to TLS 1.2](https://www.java.com/en/configure_crypto.html)“ auf der Java-Website.
* API-Clients, die Java 8 verwenden, sollten nicht beeinträchtigt werden, da die Standardeinstellung TLS 1.2 ist.
* Bei API-Clients, die andere Frameworks verwenden, müssen Sie die Details zur Unterstützung von TLS 1.2 beim jeweiligen Anbieter erfragen.

## Access to Experience Cloud Solutions interfaces {#section_748870ADE77B4CBEB18518DC784E64E5}

Da für die Benutzeroberfläche von Target Standard/Premium bereits ein [aktueller Webbrowser](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) benötigt wird, werden keine Probleme erwartet. Wenn Sie keine Verbindung zu Target herstellen können, sollten Sie Ihren Browser auf die neueste Version aktualisieren.

## How to check which TLS version your browser uses {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

So überprüfen Sie die TLS-Version auf Ihrer Website mit Google Chrome:

1. Öffnen Sie die betroffene Website in Chrome.
1. Klicken Sie im Chrome-Menü (die drei vertikalen Ellipsen) auf Mehr Tools > Developer Tools.

   ![Chrome Developer Tools](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-developer-tools.png)

1. Öffnen Sie die Registerkarte Sicherheit und überprüfen Sie dann die TLS-Versionsinformationen unter Verbindung:

   ![TLS-Versionsdetails](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-tls-version.png)

>[!NOTE]
>
>Diese Anweisungen sind ab der Veröffentlichung aktuell und können geändert werden. Eine schnelle Internetsuche sollte helfen, falls sich diese Anweisungen ändern.  Andere Browser haben ähnliche Schritte.

## Erwartetes Verhalten mit Browsern, die TLS-Versionen unter 1.2 unterstützen {#section_B5DA97A34EF248EB927610A5DA71EF2F}

This section describes what to expect with browsers that support TLS versions below 1.2 only when using an at.js or mbox.js implementation. For comparison purposes, this section also describes what to expect with browsers that support TLS 1.2.

### Central endpoints

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | Bei aktivierten TLS 1.0 oder TLS 1.1:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Die „at.js“-Datei wird heruntergeladen.</li></ul> |
| mbox.js | Bei aktivierten TLS 1.0 oder TLS 1.1:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Die „mbox.js“-Datei wird heruntergeladen.</li></ul> |

### Edge-Endpunkte

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | With TLS 1.0 or TLS 1.1 enabled:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Der Standardinhalt wird bereitgestellt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |
| mbox.js | With TLS 1.0 or TLS 1.1 enabled:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Der Standardinhalt wird bereitgestellt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |

### Aktivität, die auf die Audience der Browser-Version (Internet Explorer, Versionen 6, 7 oder 8) zugeschnitten ist

>[!NOTE]
>
>Zielgruppen funktionieren nicht mehr.

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | „at.js“ wird erst ab Internet Explorer 10 unterstützt. |
| mbox.js | With TLS 1.0 or TLS 1.1 enabled:<ul><li>Der Standardinhalt wird bereitgestellt.</li><li>Es werden keine Target-Anfragen gesendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |