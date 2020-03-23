---
keywords: apple;ITP;intelligent tracking prevention
description: Informationen über Adobe Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID-Bibliothek 4.3 (ECID)
title: Unterstützung von Adobe Target und Apple ITP
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 0fad08727233566dae6e948e53cda4f7acb64f6f

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) ist eine Initiative von Apple zum Schutz der Privatsphäre von Safari-Benutzern. Die erste Version von ITP, die im Jahr 2017 veröffentlicht wurde, zielte auf die Verwendung von Drittanbieter-Cookies ab. Genau genommen blockierte Apple alle Drittanbieter-Cookies, was wiederum die Arbeit von Anzeigen- und Werbefirmen erschwerte, da Drittanbieter-Cookies allgemein zum Tracking von Besuchern und zur Erfassung von Besucherdaten eingesetzt werden. Jetzt ist Apple dabei, die Verwendung von Erstanbieter-Cookies in Safari zu beschränken.

Die unten angegebenen ITP-Versionen beinhalten die folgenden Einschränkungen:

| Version | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Clientseitige Cookies, die im Browser mit der `document.cookie` API gesetzt werden, laufen nach sieben Tagen ab.<br>Veröffentlicht am 21. Februar 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Der Verfall nach sieben Tagen wurde drastisch auf einen Tag reduziert.<br>Veröffentlicht am Mittwoch, 24. April 2019. |

## Welchen Einfluss hat dies auf mich als Adobe Target-Kunde? {#impact}

[!DNL Target] stellt Ihnen JavaScript-Bibliotheken bereit, die Sie auf Ihren Seiten verwenden können, sodass [!DNL Target] Ihren Besuchern Echtzeit-Personalisierung bieten kann. Es gibt drei Target-JavaScript-Bibliotheken ([at. js 1,x and at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md), and [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) that place client-side [!DNL Target] cookies on your visitors&#39; browsers via the `document.cookie` API. Daher haben ITP 2.1 und 2.2 von Apple eine Auswirkung auf [!DNL Target]-Cookies, die nach 7 Tagen (bei ITP 2.1) und nach einem Tag (bei ITP 2.2) ablaufen.

Apple ITP 2.1 und 2.2 haben in den folgendne Bereichen Einfluss auf [!DNL Target]:

| Wirkung | Details |
| --- | --- |
| Mögliche Zunahme von Unique Visitors | Da der Verfall der Gültigkeit auf sieben Tage (bei ITP 2.1) und einen Tag (bei ITP 2.2) festgelegt ist, wird möglicherweise eine Steigerung der Unique Visitors auf Safari-Browsern angezeigt. Wenn Ihre Besucher nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2) erneut Ihre Domäne aufrufen, muss [!DNL Target] anstelle des abgelaufenen Cookies ein neues [!DNL Target]-Cookie in Ihrer Domäne setzen. Das neue [!DNL Target]-Cookie wird als neuer Unique Visitor gewertet, auch wenn der Benutzer derselbe ist. |
| Verringerte Lookback-Zeiträume für [!DNL Target]-Aktivitäten | Besucherprofile für [!DNL Target]-Aktivitäten haben möglicherweise für die Entscheidungsfindung einen verringerten Lookback-Zeitraum. [!DNL Target]-Cookies werden verwendet, um einen Besucher zu erkennen und Benutzerprofilattribute zur Personalisierung zu speichern. Da [!DNL Target]-Cookies in Safari nach 7 Tagen (ITP 2.1) oder einem Tag (ITP 2.2) abgelaufen sein können, können die mit dem entfernten [!DNL Target]-Cookie verknüpften Benutzerprofildaten nicht für die Entscheidungsfindung verwendet werden. |
| Profil-Skripten basierend auf 3rdPartyID | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2) eingestellt wird, funktionieren [Profil-Skripte](/help/c-target/c-visitor-profile/profile-parameters.md) , die auf dem Cookie &quot;3rdPartyID&quot;basieren, nach Ablauf nicht mehr. |
| QS-/Vorschauen-URLs auf iOS-Geräten | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2) eingestellt wird, funktionieren die [QS/Vorschauen-URLs](/help/c-activities/c-activity-qa/activity-qa.md) nach Ablauf nicht mehr, da die URLs auf dem Cookie &quot;3rdPartyID&quot;basieren. |

## Ist meine aktuelle [!DNL Target]-Implementierung betroffen?

Navigieren Sie in einem Safari-Browser zu der Website, auf der Sie eine JavaScript -Bibliothek für [!DNL Target] haben. Wenn Sie dort ein [!DNL Target]-Cookie sehen, das im Kontext eines CNAME gesetzt wurde, wie z. B. `analytics.company.com`, haben ITP 2.1 oder 2.2 keine Auswirkung auf Sie.

Wenn Sie die Experience Cloud ID (ECID)-Bibliothek zusätzlich zur JavaScript-Bibliothek von Target verwenden, erfährt Ihre Implementierung die in diesem Artikel aufgeführten Auswirkungen: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Wie kann ich die Auswirkungen von ITP 2.1, ITP 2.2 und zukünftiger Versionen auf [!DNL Target] umgehen?

Führen Sie die folgenden Aufgaben aus, um die Auswirkungen von ITP 2.1, ITP 2.2 und zukünftiger ITP-Versionen auf [!DNL Target] zu vermindern:

1. Implementieren Sie die Experience Cloud ID (ECID)-Bibliothek auf Ihren Seiten.

   Die ECID-Bibliothek ermöglicht das Personenidentifizierungs-Framework für die Experience Cloud Core-Lösungen. Mit der ECID-Bibliothek können Sie dieselben Site-Besucher und deren Daten in verschiedenen Experience Cloud-Lösungen identifizieren, indem Sie persistente und eindeutige IDs zuweisen. Die ECID-Bibliothek wird häufig aktualisiert, damit Sie etwaige ITP-bezogenen Änderungen umgehen können, die sich auf Ihre Implementierung auswirken.

   Für ITP 2.1 und ITP 2.2 muss die [ECID-Bibliothek 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) zur Abschwächung des Problems genutzt werden.

1. Verwenden Sie den CNAME von Adobe und melden Sie sich für das Managed Certificate Program von Adobe Analytics an.

   Nach der Installation der ECID-Bibliothek 4.3.0+ können Sie den CNAME und das Managed Certificate Program von Adobe Analytics nutzen. Mit diesem Programm können Sie kostenlos ein Erstanbieter-Zertifikat für Erstanbieter-Cookies implementieren. Mit CNAME können [!DNL Target]-Kunden die Auswirkungen von ITP 2.1 und ITP 2.2 verringern.

   If you are not leveraging CNAME, you can start the process by talking with your account representative and enrolling in the [Adobe Managed Certificate Program](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Nach der Implementierung einer JavaScript-Bibliothek von Target in Verbindung mit der ECID-Bibliothek Version 4.3.0 + bereitgestellt und der Anmeldung beim Adobe Managed Certificate Program zur Nutzung des CNAME, haben Sie einen robusten und langfristigen Umgehungsplan für ITP-bezogene Änderungen.

Die Branche macht bei der Bereitstellung eines sicheren Webs stetig Fortschritte. Mit [!DNL Adobe Target] werden bei der Bereitstellung personalisierter Inhalte die Erwartungen der Besucher an den Datenschutz nicht nur erfüllt, sondern übertroffen. [!DNL Adobe Target] hat bereits die Unterstützung für die [SameSite Chrome-Richtlinien von Google](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) zusätzlich zur Unterstützung von ITP 2.1 und ITP 2.2 von Apple angekündigt.

Da sich diese Richtlinien zum Schutz unserer Verbraucher stetig weiterentwickeln, wird [!DNL Adobe] auch in Zukunft diese Initiativen bei [!DNL Target] unterstützen. Gleichzeitig wird unseren Kunden ermöglicht, die besten personalisierten Erlebnisse bereitzustellen.
