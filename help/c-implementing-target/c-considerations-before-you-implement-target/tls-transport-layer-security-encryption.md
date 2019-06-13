---
description: Informationen zu Änderungen in Bezug auf die Verwendung von TLS (Transport Layer Security), die durch Adobe und Target vorgenommen werden, um den höchsten Sicherheitsstandards gerecht zu werden und die Sicherheit von Kundendaten zu fördern.
keywords: TLS;TLS 1.0;Transport Layer Security;Verschlüsselung
seo-description: Informationen zu Änderungen in Bezug auf die Verwendung von TLS (Transport Layer Security), die durch Adobe und Target vorgenommen werden, um den höchsten Sicherheitsstandards gerecht zu werden und die Sicherheit von Kundendaten zu fördern.
seo-title: Änderungen der TLS-Verschlüsselung (Transport Layer Security)
solution: Target
title: Änderungen der TLS-Verschlüsselung (Transport Layer Security)
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Änderungen der TLS-Verschlüsselung (Transport Layer Security){#tls-transport-layer-security-encryption-changes}

Informationen zu Änderungen in Bezug auf die Verwendung von TLS (Transport Layer Security), die durch Adobe und Target vorgenommen werden, um den höchsten Sicherheitsstandards gerecht zu werden und die Sicherheit von Kundendaten zu fördern.

Transport Layer Security (TLS) ist das am weitesten verbreitete Sicherheitsprotokoll, das aktuell in Webbrowsern und anderen Anwendungen Verwendung findet, bei denen über ein Netzwerk übertragene Daten geschützt werden müssen. [!DNL Adobe]Um die Sicherheitsstandards von einzuhalten, muss die Unterstützung für ältere Protokolle beendet und durch TLS 1.2 als obligatorisches Sicherheitsprotokoll ersetzt werden, damit die Daten durch die neueste und sicherste Version des Protokolls geschützt sind.

>[!NOTE]
>
>Am 20. Februar 2019 wurde die Adobe Target-Infrastruktur in den Regionen EMEA, Japan und APAC aktualisiert, um keine Daten mehr von Endbenutzern mit älteren Geräten oder Webbrowsern zu erfassen, die TLS 1.1 oder höher nicht unterstützen. Dieses Upgrade ist für den nordamerikanischen Bereich für den **1. April 2019 geplant**. Die Migration zu TLS 1.2 bietet eine verbesserte Sicherheit. Für einen reibungslosen Übergang sollten Sie die Details zu diesem Thema genau durchlesen und die Änderungen mit Ihrem IT-Team entsprechend planen.

Wir gehen davon aus, dass dies keine wesentlichen Auswirkungen auf Kundendaten oder die Berichterstattung haben wird.

## Visual Experience Composer (VEC) mit aktiviertem Enhanced Experience Composer (EEC){#section_B374B62DEC3344C194AC7BECC2EE0AA0}

Bislang wurde für [Enhanced Experience Composer](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) (EEC) in Adobe Target standardmäßig TLS 1.0 verwendet. Ab der Version Target 18.4.1 (veröffentlicht am 25. April 2018) wird für Target standardmäßig TLS 1.2 verwendet.

Adobe führt TLS 1.2 schrittweise ein. Kunden, deren Domänen bereits mit 1.2 konform sind, müssen beim Übergang zu TLS 1.2 keine Änderungen vornehmen. Die meisten Kundendomänen unterstützen TLS 1.2 bereits. Wenn Ihre Domäne TLS 1.2 nicht unterstützt, können Sie TLS 1.0 wie bisher verwenden (bis Februar 2019).

In dieser Übergangsphase sollten keine Probleme auftreten. Wenn der VEC eine Site, die zuvor funktioniert hat, nicht mehr lädt, [senden Sie eine Anfrage an den Kundendienst](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie den Übergang zu TLS 1.2 als mögliche Ursache an.

Wenn Sie zu den Kunden gehören, deren Domäne/Infrastruktur nur TSL 1.0 unterstützt, nicht jedoch TLS 1.2, sollten Sie eine Umstellung auf TLS 1.2 planen. Das Protokoll TLS 1.0 wird noch bis Februar 2019 unterstützt. Ab Februar 2019 wird das Protokoll TLS 1.0 bei der Verwendung von VEC über die Funktion „Enhanced Experience Composer“ nicht mehr von Target unterstützt.

Auch wenn allen Kunden der Umstieg auf TLS 1.2 empfohlen wird – falls Sie als neuer Kunde TLS 1.2 *NICHT* unterstützen, teilen Sie dem Kundendienst mit, dass Sie TLS 1.0 für Enhanced Experience Composer verwenden müssen. Planen Sie jedoch den Übergang zu TLS 1.2 ein, da TLS 1.0 nur noch bis Februar 2019 unterstützt wird.

## Aktivitätsbereitstellung {#section_46CA5943E4354B259014C2BF340AECD6}

Ab Februar 2019 bieten die Target-Server keine Unterstützung für TLS 1.0 mehr. Aufgrund dieser Änderung akzeptieren Target-Server keine Anfragen mehr von Endbenutzern mit älteren Geräten oder Webbrowsern ohne Unterstützung für TLS 1.1 oder höher. Daher empfangen ältere Geräte und Browser, die nur (oder standardmäßig) TLS 1.0 unterstützen, keinen Aktivitätsinhalt mehr von Adobe Target. Standardinhalte der Site werden gerendert.

Zu den betroffenen älteren Geräten und Browsern gehören:

* Android 4.3 und frühere Versionen
* Internet Explorer 8 bis 10 unter Windows 7 und frühere Versionen
* Internet Explorer 10 unter Windows Phone 8.0
* Safari 6.0.4/OS X 10.8.4 und frühere Versionen

Berücksichtigen Sie Folgendes bei der Planung für diese Änderung (beachten Sie, dass der Termin ab Februar 2019 für alle Punkte gilt):

* Sie müssen sicherstellen, dass Ihre Standardsite vorbereitet ist und auf kompatiblen Geräten und Browsern genutzt werden kann.
* Beachten Sie, dass die Anzahl der Besucher in Ihren Target-Berichten geringfügig zurückgehen kann.
* Möglicherweise müssen Sie Zielgruppen, die speziell für ältere Geräte oder Browser ohne Unterstützung für TLS 1.0 erstellt wurden, ändern, da die Bereitstellung auf solchen Geräten und Browsern nicht mehr funktioniert.

Weitere Informationen zu unterstützten Browsern und Versionen finden Sie unter [Unterstützte Browser](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## Adobe Target-APIs {#section_88797FA5434049EC89F908853CC76903}

Ab Februar  2019 unterstützen Target-APIs keine Verschlüsselung mit TLS 1.0 mehr. Kunden, die auf die API zugreifen, sollten sicherstellen, dass sie nicht von den Auswirkungen betroffen sind.

* Für API-Clients, die Java 7 mit den Standardeinstellungen verwenden, sind Änderungen erforderlich, damit TLS 1.2 unterstützt wird. Weitere Informationen finden Sie unter „[Changing default TLS protocol version for client end points: TLS 1.0 to TLS 1.2](https://www.java.com/en/configure_crypto.html)“ auf der Java-Website.
* API-Clients, die Java 8 verwenden, sollten nicht beeinträchtigt werden, da die Standardeinstellung TLS 1.2 ist.
* Bei API-Clients, die andere Frameworks verwenden, müssen Sie die Details zur Unterstützung von TLS 1.2 beim jeweiligen Anbieter erfragen.

## Zugriff auf die Benutzeroberflächen von Experience Cloud-Lösungen {#section_748870ADE77B4CBEB18518DC784E64E5}

Da für die Benutzeroberfläche von Target Standard/Premium bereits ein [aktueller Webbrowser](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) benötigt wird, werden keine Probleme erwartet. Wenn Sie keine Verbindung zu Target herstellen können, sollten Sie Ihren Browser auf die neueste Version aktualisieren.

## Überprüfen der in Ihrem Browser verwendeten TLS-Version {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie in der Adresszeile des Browsers auf das Symbol **[!UICONTROL Website-Informationen anzeigen].**

   ![](assets/firefox_more_info.png)

1. Klicken Sie auf **[!UICONTROL Verbindungsdetails anzeigen]** &gt; **[!UICONTROL Weitere Informationen]**.

   ![](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![](assets/firefox_more_info_3.png)

## Erwartetes Verhalten bei Browsern, die nur TLS 1.0 unterstützen {#section_B5DA97A34EF248EB927610A5DA71EF2F}

Dieser Abschnitt beschreibt das erwartete Verhalten von Browsern, die nur TLS 1.0 unterstützen, wenn Sie eine „at.js“- oder „mbox.js“-Implementierung verwenden. Zum Vergleich beschreibt dieser Abschnitt auch das erwartete Verhalten bei Browsern, die TLS 1.1 und 1.2 unterstützen.

### Zentrale Endpunkte

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | Bei aktiviertem TLS 1.0:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li></ul>Bei aktiviertem TLS 1.1 oder 1.2:<ul><li>Die „at.js“-Datei wird heruntergeladen.</li></ul> |
| mbox.js | Bei aktiviertem TLS 1.0:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li></ul>Bei aktiviertem TLS 1.1 oder 1.2:<ul><li>Die „mbox.js“-Datei wird heruntergeladen.</li></ul> |

### Edge-Endpunkte

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | Bei aktiviertem TLS 1.0:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Der Standardinhalt wird bereitgestellt.</li></ul>Bei aktiviertem TLS 1.1 oder 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |
| mbox.js | Bei aktiviertem TLS 1.0:<ul><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li><li>Benutzer sehen die Meldung „Keine sichere Verbindung zu dieser Seite möglich“. In der Nachricht wird erläutert, dass dies möglicherweise daran liegt, dass die Site veraltete oder unsichere TLS-Sicherheitseinstellungen verwendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Der Standardinhalt wird bereitgestellt.</li></ul>Bei aktiviertem TLS 1.1 oder 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |

### Aktivitäten mit Targeting per Browserversion-Zielgruppen (Internet Explorer-Versionen 6, 7 oder 8)

>[!NOTE]
>
>Zielgruppen funktionieren nicht mehr.

| Target-JavaScript-Implementierung | Details |
|--- |--- |
| at.js | „at.js“ wird erst ab Internet Explorer 10 unterstützt. |
| mbox.js | Bei aktiviertem TLS 1.0:<ul><li>Der Standardinhalt wird bereitgestellt.</li><li>Es werden keine Target-Anfragen gesendet.</li><li>Es wird kein Konsolenfehler angezeigt.</li><li>Mit Browser-Entwicklungstools wird auf der Registerkarte „Netzwerk“ die Meldung „200 OK“ angezeigt. Das bedeutet, dass die Anfrage erfolgreich war.</li></ul>Bei aktiviertem TLS 1.1 oder 1.2:<ul><li>Der Angebotsinhalt wird bereitgestellt.</li></ul> |