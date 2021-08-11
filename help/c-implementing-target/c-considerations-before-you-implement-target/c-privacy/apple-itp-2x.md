---
keywords: apple; ITP; intelligente Tracking-Prävention; Experience Cloud ID; ecid; itp
description: Erfahren Sie mehr über die Adobe [!DNL Target] und die Auswirkungen der ITP-Initiative (Apple Intelligent Tracking Prevention), mit der die Privatsphäre von Safari-Benutzern geschützt werden soll.
title: Wie behandelt  [!DNL Target] Apple ITP-Unterstützung?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: 05a62be5-ccfb-4d5c-b511-35023b95e567
source-git-commit: 898a18cbd9c6f499f9e7b74078575bc149c9a292
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 38%

---

# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) ist eine Initiative von Apple zum Schutz der Privatsphäre von Safari-Benutzern. Die erste Version von ITP, die im Jahr 2017 veröffentlicht wurde, zielte auf die Verwendung von Drittanbieter-Cookies ab. Genau genommen blockierte Apple alle Drittanbieter-Cookies, was wiederum die Arbeit von Anzeigen- und Werbefirmen erschwerte, da Drittanbieter-Cookies allgemein zum Tracking von Besuchern und zur Erfassung von Besucherdaten eingesetzt werden. Jetzt ist Apple dabei, die Verwendung von Erstanbieter-Cookies in Safari zu beschränken.

Die unten angegebenen ITP-Versionen beinhalten die folgenden Einschränkungen:

| Version | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Clientseitige Cookies, die im Browser mit der `document.cookie` API gesetzt werden, laufen nach sieben Tagen ab.<br>Veröffentlicht am 21. Februar 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Der Verfall nach sieben Tagen wurde drastisch auf einen Tag reduziert.<br>Veröffentlicht am Mittwoch, 24. April 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-3-2/) | Mehrere Problemumgehungen wurden beseitigt, z. B. die Verwendung von localStorage oder die Verwendung von JavaScript `Document.referrer property`.<br>Veröffentlicht am 23. September 2019.<br>CNAME-Cloaking-Verteidigungsfunktion für ITP, die in Safari 14, macOS Big Sur, Catalina, Mojave, iOS 14 und iPadOS 14 veröffentlicht wurde. Alle Cookies, die von einer CNAME-blockierten HTTP-Antwort eines Drittanbieters erstellt werden, laufen in sieben Tagen ab.<br>Angesagt am 12. November 2020. |

## Wie wirkt sich dies auf mich als Adobe [!DNL Target] aus? {#impact}

[!DNL Target] stellt Ihnen JavaScript-Bibliotheken bereit, die Sie auf Ihren Seiten verwenden können, sodass [!DNL Target] Ihren Besuchern Echtzeit-Personalisierung bieten kann. Es gibt drei Target-JavaScript-Bibliotheken at.js 1.x, at.js 2.x, die clientseitige [!DNL Target] -Cookies über die `document.cookie` -API auf den Browsern Ihrer Besucher platzieren. Daher sind [!DNL Target]-Cookies von ITP 2.1, 2.2 und 2.3 von Apple betroffen und laufen nach sieben Tagen (mit ITP 2.1) und nach einem Tag (mit ITP 2.2 und ITP 2.3) ab.

Apple ITP 2.x wirkt sich auf [!DNL Target] in den folgenden Bereichen aus:

| Wirkung | Details |
| --- | --- |
| Mögliche Zunahme von Unique Visitors | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) festgelegt ist, kann es zu einem Anstieg der Unique Visitors kommen, die von Safari-Browsern stammen. Wenn Ihre Besucher Ihre Domäne nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2 und ITP 2.3) erneut aufrufen, wird [!DNL Target] gezwungen, anstelle des abgelaufenen Cookies ein neues [!DNL Target]-Cookie in Ihrer Domäne zu platzieren. Das neue [!DNL Target]-Cookie wird als neuer Unique Visitor gewertet, auch wenn der Benutzer derselbe ist. |
| Verringerte Lookback-Zeiträume für [!DNL Target]-Aktivitäten | Besucherprofile für [!DNL Target]-Aktivitäten haben möglicherweise für die Entscheidungsfindung einen verringerten Lookback-Zeitraum. [!DNL Target]-Cookies werden verwendet, um einen Besucher zu erkennen und Benutzerprofilattribute zur Personalisierung zu speichern. Da [!DNL Target]-Cookies in Safari nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2 und 2.3) abgelaufen sein können, können die Benutzerprofildaten, die mit dem bereinigten [!DNL Target]-Cookie verknüpft waren, nicht für die Entscheidungsfindung verwendet werden. |
| Profil-Skripte, die auf der ID von Drittanbietern (3rdPartyID) basieren | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt ist, funktionieren [Profilskripte](/help/c-target/c-visitor-profile/profile-parameters.md), die auf dem 3rdPartyID-Cookie basieren, nach Ablauf nicht mehr. |
| QA-/Vorschau-URLs auf iOS-Geräten | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2 und ITP 2.3) eingestellt ist, funktionieren [QA/Preview-URLs](/help/c-activities/c-activity-qa/activity-qa.md) nach Ablauf nicht mehr, da die URLs auf dem 3rdPartyID-Cookie basieren. |

## Ist meine aktuelle [!DNL Target]-Implementierung betroffen?

Wenn Sie die Experience Cloud-ID-Bibliothek (ECID) zusätzlich zur JavaScript-Bibliothek [!DNL Target] verwenden, wird Ihre Implementierung auf die in diesem Artikel aufgeführten Arten beeinträchtigt: [Auswirkungen von Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).
