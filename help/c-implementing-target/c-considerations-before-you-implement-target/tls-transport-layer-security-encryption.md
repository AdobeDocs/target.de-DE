---
keywords: TLS;TLS 1.0;Transport Layer Security;Verschlüsselung;TLS 1.1;TLS 1.2
description: Erfahren Sie, wie [!DNL Target] das TLS-Protokoll (Transport Layer Security) verwendet, um die höchsten Sicherheitsstandards zu erfüllen und die Sicherheit Ihrer Kundendaten zu fördern.
title: Wie stellt [!DNL Target] Mit TLS Sicherheit bereit?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: 964a642a-830a-4556-a92a-d300670cd2fa
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 53%

---

# Änderungen der TLS-Verschlüsselung (Transport Layer Security)

Informationen über Änderungen an der Verwendung von [!DNL Adobe] und [!DNL Adobe Target] TLS (Transport Layer Security) zur Aufrechterhaltung der höchsten Sicherheitsstandards und zur Förderung der Sicherheit von Kundendaten.

Transport Layer Security (TLS) ist das am weitesten verbreitete Sicherheitsprotokoll, das aktuell in Webbrowsern und anderen Anwendungen Verwendung findet, bei denen über ein Netzwerk übertragene Daten geschützt werden müssen. Um die Sicherheitsstandards von Adobe einzuhalten, muss die Unterstützung für ältere Protokolle beendet und durch TLS 1.2 als obligatorisches Sicherheitsprotokoll ersetzt werden, damit die Daten durch die neueste und sicherste Version des Protokolls geschützt sind.

>[!IMPORTANT]
>
>Ab dem 1. März 2020 bietet Adobe Target keine Unterstützung mehr für die TLS 1.1-Verschlüsselung für Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), Aktivitätsbereitstellung, APIs usw. Führen Sie vor dem 1. März 2020 ein Upgrade auf TLS 1.2 durch, um Probleme zu vermeiden.

Wir gehen davon aus, dass dies keine wesentlichen Auswirkungen auf Kundendaten oder die Berichterstattung haben wird.

## Visual Experience Composer (VEC) mit aktiviertem Enhanced Experience Composer (EEC) {#section_B374B62DEC3344C194AC7BECC2EE0AA0}

TLS 1.2 ist die Standardeinstellung ab dem 1. März 2020 und TLS 1.1 wird nicht mehr unterstützt.

Adobe führt TLS 1.2 schrittweise ein. Kunden, deren Domänen bereits mit 1.2 konform sind, müssen beim Übergang zu TLS 1.2 keine Änderungen vornehmen. Die meisten Kundendomänen unterstützen bereits TLS 1.2. Wenn Ihre Domäne TLS 1.2 jedoch nicht unterstützt, bleiben diese Domänen auf TLS 1.1 wie heute (bis März 2020).

In dieser Übergangsphase sollten keine Probleme auftreten. Wenn der VEC eine Site, die zuvor funktioniert hat, nicht mehr lädt,  [senden Sie eine Anfrage an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie den Übergang zu TLS 1.2 als mögliche Ursache an.

Wenn Sie jedoch zu den Kunden gehören, die TSL 1.1 verwenden, ohne TLS 1.2 zu unterstützen, sollten Sie den Wechsel Ihrer Domänen/Infrastruktur zu TLS 1.2 planen. Das TLS 1.1-Protokoll wird bis zum 1. März 2020 weiterhin unterstützt. Ab dem 1. März 2020 unterstützt Target das TLS 1.1-Protokoll nicht mehr, das über die Funktion Enhanced Experience Composer für VEC verwendet werden soll.

Auch wenn allen Kunden der Umstieg auf TLS 1.2 empfohlen wird – falls Sie als neuer Kunde TLS 1.2 *NICHT* unterstützen, teilen Sie dem Kundendienst mit, dass Sie TLS 1.1 für Enhanced Experience Composer verwenden müssen. Planen Sie jedoch den Wechsel zu TLS 1.2 ein, da Sie auch nach dem 1. März 2020 nicht mehr unterstützt werden.

## Aktivitätsbereitstellung {#section_46CA5943E4354B259014C2BF340AECD6}

Ab dem 1. März 2020 bieten die Target-Server keine Unterstützung für TLS 1.1 mehr. Aufgrund dieser Änderung werden Target-Server keine Anforderungen mehr von Besuchern mit älteren Geräten oder Webbrowsern ohne Unterstützung für TLS 1.2 (oder höher) akzeptieren. Daher erhalten ältere Geräte und Browser, die nur TLS 1.1 unterstützen (oder standardmäßig TLS 1.1 unterstützen), keine Aktivitätsinhalte von Adobe Target. Standardinhalte der Site werden gerendert.

Zu den betroffenen älteren Geräten und Browsern gehören:

* Google Chrome (Chrome für Android), Version 29 und früher
* Opera Browser (Opera Mobile), Versionen 12.17 und früher
* Mozilla Firefox (Firefox für Mobilgeräte), Version 26 und früher
* Android 4.3 und frühere Versionen
* Internet Explorer 8 bis 10 unter Windows 7 und frühere Versionen
* Internet Explorer 10 unter Windows Phone 8.0
* Safari 6.0.4/OS X 10.8.4 und frühere Versionen

Beachten Sie bei der Planung dieser Änderung Folgendes (beachten Sie, dass der Termin am 1. März 2020 alle diese Punkte betrifft):

* Sie müssen sicherstellen, dass Ihre Standardsite vorbereitet ist und auf kompatiblen Geräten und Browsern genutzt werden kann.
* Beachten Sie, dass die Anzahl der Besucher in Ihren Target-Berichten geringfügig zurückgehen kann.
* Möglicherweise müssen Sie Zielgruppen ändern, die speziell für ältere Geräte oder Browser erstellt wurden, die TLS 1.2 nicht unterstützen. Die Bereitstellung auf diesen Geräten und Browsern funktioniert nicht mehr.

Weitere Informationen zu unterstützten Browsern und Versionen finden Sie unter  [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## Adobe [!DNL Target] APIs {#section_88797FA5434049EC89F908853CC76903}

Ab dem 1. März 2020 bieten Target-APIs keine Unterstützung mehr für die Verschlüsselung mit TLS 1.1. Kunden, die auf die API zugreifen, sollten sicherstellen, dass sie nicht von den Auswirkungen betroffen sind.

* Für API-Clients, die Java 7 mit den Standardeinstellungen verwenden, sind Änderungen erforderlich, damit TLS 1.2 unterstützt wird. Weitere Informationen finden Sie unter „[Changing default TLS protocol version for client end points: TLS 1.0 to TLS 1.2](https://www.java.com/en/configure_crypto.html)“ auf der Java-Website.
* API-Clients, die Java 8 verwenden, sollten nicht beeinträchtigt werden, da die Standardeinstellung TLS 1.2 ist.
* Bei API-Clients, die andere Frameworks verwenden, müssen Sie die Details zur Unterstützung von TLS 1.2 beim jeweiligen Anbieter erfragen.

## Zugriff auf die Benutzeroberflächen von Experience Cloud Solutions {#section_748870ADE77B4CBEB18518DC784E64E5}

Da für die Benutzeroberfläche von Target Standard/Premium bereits ein [aktueller Webbrowser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) benötigt wird, werden keine Probleme erwartet. Wenn Sie keine Verbindung zu Target herstellen können, sollten Sie Ihren Browser auf die neueste Version aktualisieren.

## Überprüfen der TLS-Version, die Ihr Browser verwendet {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

So überprüfen Sie die TLS-Version auf Ihrer Website mit Google Chrome:

1. Öffnen Sie die betroffene Website in Chrome.
1. Klicken Sie im Chrome-Menü (den drei vertikalen Ellipsen) auf Mehr Tools > Entwicklertools .

   ![Chrome Developer Tools](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-developer-tools.png)

1. Öffnen Sie die Registerkarte Sicherheit und überprüfen Sie dann die TLS-Versionsinformationen unter Verbindung:

   ![TLS-Versionsdetails](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-tls-version.png)

>[!NOTE]
>
>Diese Anweisungen sind ab der Veröffentlichung aktuell und können sich ändern. Eine schnelle Internet-Suche sollte helfen, falls sich diese Anweisungen ändern.  Andere Browser weisen ähnliche Schritte auf.

## Erwartetes Verhalten mit Browsern, die TLS-Versionen unter 1.2 unterstützen {#section_B5DA97A34EF248EB927610A5DA71EF2F}

In diesem Abschnitt wird beschrieben, was mit Browsern zu erwarten ist, die TLS-Versionen unter 1.2 nur bei Verwendung einer at.js-Implementierung unterstützen. Zu Vergleichszwecken wird in diesem Abschnitt auch beschrieben, was mit Browsern zu erwarten ist, die TLS 1.2 unterstützen.

### Zentrale Endpunkte

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | Bei aktiviertem TLS 1.0 oder TLS 1.1:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Die „at.js“-Datei wird heruntergeladen.</li></ul> |

### Edge-Endpunkte

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| [!DNL Adobe Experience Platform Web SDK] | Bei aktiviertem TLS 1.0 oder TLS 1.1:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Der Standardinhalt wird bereitgestellt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |
| at.js | Bei aktiviertem TLS 1.0 oder TLS 1.1:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Der Standardinhalt wird bereitgestellt.</li></ul>Bei aktiviertem TLS 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |

### Aktivitäten, die auf eine Browserversion-Audience ausgerichtet sind (Internet Explorer, Versionen 6, 7 oder 8)

>[!NOTE]
>
>Zielgruppen funktionieren nicht mehr.

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| [!DNL Adobe Experience Platform Web SDK] | Das Platform SDK wird in Internet Explorer-Versionen vor Version 10 nicht unterstützt. |
| at.js | „at.js“ wird erst ab Internet Explorer 10 unterstützt. |
