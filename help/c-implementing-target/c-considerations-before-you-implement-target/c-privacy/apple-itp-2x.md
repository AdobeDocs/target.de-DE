---
keywords: apple; ITP; intelligente Tracking-Prävention; Experience Cloud ID; ecid
description: Erfahren Sie mehr über die Adobe [!DNL Target] und die Auswirkungen der ITP-Initiative (Apple Intelligent Tracking Prevention), mit der die Privatsphäre von Safari-Benutzern geschützt werden soll.
title: Wie behandelt  [!DNL Target] Apple ITP-Unterstützung?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: 05a62be5-ccfb-4d5c-b511-35023b95e567
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 52%

---

# Apple Intelligent Tracking Prevention (ITP) 2.x

Informationen zur [!DNL Adobe Target]-Unterstützung für ITP 2.x von Apple über die Experience Cloud ID-Bibliothek 4.3 (ECID).

Intelligent Tracking Prevention (ITP) ist eine Initiative von Apple zum Schutz der Privatsphäre von Safari-Benutzern. Die erste Version von ITP, die im Jahr 2017 veröffentlicht wurde, zielte auf die Verwendung von Drittanbieter-Cookies ab. Genau genommen blockierte Apple alle Drittanbieter-Cookies, was wiederum die Arbeit von Anzeigen- und Werbefirmen erschwerte, da Drittanbieter-Cookies allgemein zum Tracking von Besuchern und zur Erfassung von Besucherdaten eingesetzt werden. Jetzt ist Apple dabei, die Verwendung von Erstanbieter-Cookies in Safari zu beschränken.

Die unten angegebenen ITP-Versionen beinhalten die folgenden Einschränkungen:

| Version | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Clientseitige Cookies, die im Browser mit der `document.cookie` API gesetzt werden, laufen nach sieben Tagen ab.<br>Veröffentlicht am 21. Februar 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Der Verfall nach sieben Tagen wurde drastisch auf einen Tag reduziert.<br>Veröffentlicht am Mittwoch, 24. April 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Mehrere Problemumgehungen wurden beseitigt, z. B. die Verwendung von localStorage oder die Verwendung von JavaScript `Document.referrer property`.<br>Veröffentlicht am 23. September 2019. |

## Wie wirkt sich dies auf mich als Adobe [!DNL Target] aus? {#impact}

[!DNL Target] stellt Ihnen JavaScript-Bibliotheken bereit, die Sie auf Ihren Seiten verwenden können, sodass [!DNL Target] Ihren Besuchern Echtzeit-Personalisierung bieten kann. Es gibt drei Target-JavaScript-Bibliotheken at.js 1.x, at.js 2.x, die clientseitige [!DNL Target] -Cookies über die `document.cookie` -API auf den Browsern Ihrer Besucher platzieren. Daher sind [!DNL Target]-Cookies von ITP 2.x von Apple betroffen und laufen nach sieben Tagen (mit ITP 2.1) und nach einem Tag (mit ITP 2.2 und ITP 2.3) ab.

Apple ITP 2.x wirkt sich auf [!DNL Target] in den folgenden Bereichen aus:

| Wirkung | Details |
| --- | --- |
| Mögliche Zunahme von Unique Visitors | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) festgelegt ist, kann es zu einem Anstieg der Unique Visitors kommen, die von Safari-Browsern stammen. Wenn Ihre Besucher Ihre Domäne nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2 und ITP 2.3) erneut aufrufen, wird [!DNL Target] gezwungen, anstelle des abgelaufenen Cookies ein neues [!DNL Target]-Cookie in Ihrer Domäne zu platzieren. Das neue [!DNL Target]-Cookie wird als neuer Unique Visitor gewertet, auch wenn der Benutzer derselbe ist. |
| Verringerte Lookback-Zeiträume für [!DNL Target]-Aktivitäten | Besucherprofile für [!DNL Target]-Aktivitäten haben möglicherweise für die Entscheidungsfindung einen verringerten Lookback-Zeitraum. [!DNL Target]-Cookies werden verwendet, um einen Besucher zu erkennen und Benutzerprofilattribute zur Personalisierung zu speichern. Da [!DNL Target]-Cookies in Safari nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2 und 2.3) abgelaufen sein können, können die Benutzerprofildaten, die mit dem bereinigten [!DNL Target]-Cookie verknüpft waren, nicht für die Entscheidungsfindung verwendet werden. |
| Profil-Skripte, die auf der ID von Drittanbietern (3rdPartyID) basieren | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt ist, funktionieren [Profilskripte](/help/c-target/c-visitor-profile/profile-parameters.md), die auf dem 3rdPartyID-Cookie basieren, nach Ablauf nicht mehr. |
| QA-/Vorschau-URLs auf iOS-Geräten | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt ist, funktionieren [QA/Preview-URLs](/help/c-activities/c-activity-qa/activity-qa.md) nach Ablauf nicht mehr, da die URLs auf dem 3rdPartyID-Cookie basieren. |

## Ist meine aktuelle [!DNL Target]-Implementierung betroffen?

Navigieren Sie in einem Safari-Browser zu der Website, auf der Sie eine JavaScript -Bibliothek für [!DNL Target] haben. Wenn ein [!DNL Target]-Cookie im Kontext eines CNAME gesetzt wird, z. B. `analytics.company.com`, sind Sie von ITP 2.x nicht betroffen.

Wenn Sie die Experience Cloud ID (ECID)-Bibliothek zusätzlich zur JavaScript-Bibliothek von Target verwenden, erfährt Ihre Implementierung die in diesem Artikel aufgeführten Auswirkungen: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Wie kann ich die Auswirkungen künftiger ITP 2.x-Versionen auf Target umgehen?

Führen Sie die folgenden Aufgaben aus, um die Auswirkungen künftiger ITP 2.x-Versionen auf Target zu minimieren:

1. Implementieren Sie die Experience Cloud ID (ECID)-Bibliothek auf Ihren Seiten.

   Die ECID-Bibliothek ermöglicht das Personenidentifizierungs-Framework für die Experience Cloud Core-Lösungen. Mit der ECID-Bibliothek können Sie dieselben Site-Besucher und deren Daten in verschiedenen Experience Cloud-Lösungen identifizieren, indem Sie persistente und eindeutige IDs zuweisen. Die ECID-Bibliothek wird häufig aktualisiert, damit Sie etwaige ITP-bezogenen Änderungen umgehen können, die sich auf Ihre Implementierung auswirken.

   Für ITP 2.x muss [ECID-Bibliothek 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html?lang=de) zur Schadensminderung verwendet werden.

1. Verwenden Sie den CNAME von Adobe und melden Sie sich für das Managed Certificate Program von Adobe Analytics an.

   Nach der Installation der ECID-Bibliothek 4.3.0+ können Sie den CNAME und das Managed Certificate Program von Adobe Analytics nutzen. Mit diesem Programm können Sie kostenlos ein Erstanbieter-Zertifikat für Erstanbieter-Cookies implementieren. Die Verwendung von CNAME hilft [!DNL Target] Kunden, die Auswirkungen von ITP 2.x zu mindern.

   Wenn Sie CNAME nicht verwenden, können Sie den Prozess starten, indem Sie sich mit Ihrem Kundenbetreuer unterhalten und sich im [Adobe Managed Certificate Program](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program) anmelden.

Nach der Implementierung einer JavaScript-Bibliothek von Target in Verbindung mit der ECID-Bibliothek Version 4.3.0 + bereitgestellt und der Anmeldung beim Adobe Managed Certificate Program zur Nutzung des CNAME, haben Sie einen robusten und langfristigen Umgehungsplan für ITP-bezogene Änderungen.

Die Branche macht bei der Bereitstellung eines sicheren Webs stetig Fortschritte. Mit [!DNL Adobe Target] werden bei der Bereitstellung personalisierter Inhalte die Erwartungen der Besucher an den Datenschutz nicht nur erfüllt, sondern übertroffen. [!DNL Adobe Target] hat bereits die Unterstützung für die SameSite-Chrome-Richtlinien von  [Google ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) zusätzlich zur Unterstützung von ITP 2.x von Apple angekündigt.

Da sich diese Richtlinien zum Schutz unserer Verbraucher stetig weiterentwickeln, wird [!DNL Adobe] auch in Zukunft diese Initiativen bei [!DNL Target] unterstützen. Gleichzeitig wird unseren Kunden ermöglicht, die besten personalisierten Erlebnisse bereitzustellen.
