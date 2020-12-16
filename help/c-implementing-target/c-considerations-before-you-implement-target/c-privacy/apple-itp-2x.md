---
keywords: apple;ITP;intelligent tracking prevention
description: Informationen zur Adobe Target-Unterstützung für ITP 2.x von Apple über die Experience Cloud-ID (ECID)-Bibliothek 4.3.
title: Unterstützung von Adobe Target und Apple ITP
feature: privacy and security
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 54%

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) ist eine Initiative von Apple zum Schutz der Privatsphäre von Safari-Benutzern. Die erste Version von ITP, die im Jahr 2017 veröffentlicht wurde, zielte auf die Verwendung von Drittanbieter-Cookies ab. Genau genommen blockierte Apple alle Drittanbieter-Cookies, was wiederum die Arbeit von Anzeigen- und Werbefirmen erschwerte, da Drittanbieter-Cookies allgemein zum Tracking von Besuchern und zur Erfassung von Besucherdaten eingesetzt werden. Jetzt ist Apple dabei, die Verwendung von Erstanbieter-Cookies in Safari zu beschränken.

Die unten angegebenen ITP-Versionen beinhalten die folgenden Einschränkungen:

| Version | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Clientseitige Cookies, die im Browser mit der `document.cookie` API gesetzt werden, laufen nach sieben Tagen ab.<br>Veröffentlicht am 21. Februar 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Der Verfall nach sieben Tagen wurde drastisch auf einen Tag reduziert.<br>Veröffentlicht am Mittwoch, 24. April 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Es wurden mehrere Workarounds entfernt, z. B. die Verwendung von localStorage oder die Verwendung von JavaScript `Document.referrer property`.<br>Veröffentlicht am 23. September 2019. |

## Welchen Einfluss hat dies auf mich als Adobe Target-Kunde? {#impact}

[!DNL Target] stellt Ihnen JavaScript-Bibliotheken bereit, die Sie auf Ihren Seiten verwenden können, sodass [!DNL Target] Ihren Besuchern Echtzeit-Personalisierung bieten kann. Es gibt drei Target-JavaScript-Bibliotheken ([at. js 1,x, at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) und [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)), die clientseitige [!DNL Target]-Cookies über die `document.cookie`-API in den Browsern Ihrer Besucher platzieren. Infolgedessen werden die [!DNL Target]-Cookies von Apple ITP 2.x beeinflusst und nach sieben Tagen (mit ITP 2.1) und nach einem Tag (mit ITP 2.2 und ITP 2.3) ablaufen.

Apple ITP 2.x wirkt sich auf [!DNL Target] in den folgenden Bereichen aus:

| Wirkung | Details |
| --- | --- |
| Mögliche Zunahme von Unique Visitors | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt ist, kann es zu einer Zunahme der individuellen Besucher kommen, die von Safari-Browsern kommen. Wenn Ihre Besucher Ihre Domäne nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2 und ITP 2.3) erneut aufrufen, ist [!DNL Target] gezwungen, anstelle des abgelaufenen Cookies ein neues [!DNL Target]-Cookie in Ihrer Domäne zu platzieren. Das neue [!DNL Target]-Cookie wird als neuer Unique Visitor gewertet, auch wenn der Benutzer derselbe ist. |
| Verringerte Lookback-Zeiträume für [!DNL Target]-Aktivitäten | Besucherprofile für [!DNL Target]-Aktivitäten haben möglicherweise für die Entscheidungsfindung einen verringerten Lookback-Zeitraum. [!DNL Target]-Cookies werden verwendet, um einen Besucher zu erkennen und Benutzerprofilattribute zur Personalisierung zu speichern. Da [!DNL Target]-Cookies in Safari nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2 und 2.3) abgelaufen sein können, können die Benutzerdaten, die mit dem bereinigten [!DNL Target]-Cookie verknüpft waren, nicht für die Entscheidungsfindung verwendet werden. |
| Profil-Skripten basierend auf 3rdPartyID | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt ist, funktionieren [Profil-Skripte](/help/c-target/c-visitor-profile/profile-parameters.md) basierend auf dem Drittanbieter-ID-Cookie nach Ablauf nicht mehr. |
| QS-/Vorschauen-URLs auf iOS-Geräten | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt wird, funktionieren [QA/Vorschau-URLs](/help/c-activities/c-activity-qa/activity-qa.md) nach Ablauf nicht mehr, da die URLs auf dem Cookie &quot;3rdPartyID&quot;basieren. |

## Ist meine aktuelle [!DNL Target]-Implementierung betroffen?

Navigieren Sie in einem Safari-Browser zu der Website, auf der Sie eine JavaScript -Bibliothek für [!DNL Target] haben. Wenn ein [!DNL Target]-Cookie im Kontext eines CNAME gesetzt wird, z. B. `analytics.company.com`, werden Sie nicht von ITP 2.x beeinflusst.

Wenn Sie die Experience Cloud ID (ECID)-Bibliothek zusätzlich zur JavaScript-Bibliothek von Target verwenden, erfährt Ihre Implementierung die in diesem Artikel aufgeführten Auswirkungen: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Wie kann ich die Auswirkungen künftiger ITP 2.x-Versionen auf die Zielgruppe mildern?

Um die Auswirkungen künftiger ITP 2.x-Versionen auf die Zielgruppe zu mildern, führen Sie die folgenden Aufgaben aus:

1. Implementieren Sie die Experience Cloud ID (ECID)-Bibliothek auf Ihren Seiten.

   Die ECID-Bibliothek ermöglicht das Personenidentifizierungs-Framework für die Experience Cloud Core-Lösungen. Mit der ECID-Bibliothek können Sie dieselben Site-Besucher und deren Daten in verschiedenen Experience Cloud-Lösungen identifizieren, indem Sie persistente und eindeutige IDs zuweisen. Die ECID-Bibliothek wird häufig aktualisiert, damit Sie etwaige ITP-bezogenen Änderungen umgehen können, die sich auf Ihre Implementierung auswirken.

   Für ITP 2.x muss [ECID-Bibliothek 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) zur Abschwächung verwendet werden.

1. Verwenden Sie den CNAME von Adobe und melden Sie sich für das Managed Certificate Program von Adobe Analytics an.

   Nach der Installation der ECID-Bibliothek 4.3.0+ können Sie den CNAME und das Managed Certificate Program von Adobe Analytics nutzen. Mit diesem Programm können Sie kostenlos ein Erstanbieter-Zertifikat für Erstanbieter-Cookies implementieren. Durch die Verwendung von CNAME können [!DNL Target]-Kunden die Auswirkungen von ITP 2.x mildern.

   Wenn Sie CNAME nicht verwenden, können Sie den Beginn des Vorgangs durch einen Kundenbetreuer durchführen und sich im [Adobe Managed Certificate-Programm](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program) registrieren.

Nach der Implementierung einer JavaScript-Bibliothek von Target in Verbindung mit der ECID-Bibliothek Version 4.3.0 + bereitgestellt und der Anmeldung beim Adobe Managed Certificate Program zur Nutzung des CNAME, haben Sie einen robusten und langfristigen Umgehungsplan für ITP-bezogene Änderungen.

Die Branche macht bei der Bereitstellung eines sicheren Webs stetig Fortschritte. Mit [!DNL Adobe Target] werden bei der Bereitstellung personalisierter Inhalte die Erwartungen der Besucher an den Datenschutz nicht nur erfüllt, sondern übertroffen. [!DNL Adobe Target] hat bereits die Unterstützung für die SameSite-Chrome- [Richtlinien von ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Google angekündigt, zusätzlich zur Unterstützung von Apple ITP 2.x.

Da sich diese Richtlinien zum Schutz unserer Verbraucher stetig weiterentwickeln, wird [!DNL Adobe] auch in Zukunft diese Initiativen bei [!DNL Target] unterstützen. Gleichzeitig wird unseren Kunden ermöglicht, die besten personalisierten Erlebnisse bereitzustellen.
