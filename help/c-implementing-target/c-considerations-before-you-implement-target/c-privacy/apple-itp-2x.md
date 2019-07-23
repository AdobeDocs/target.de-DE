---
description: Informationen zur Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID (ECID)-Bibliothek 4.3.
keywords: apple; ITP; intelligente Tracking-Vermeidung
seo-description: Informationen über die Adobe Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID (ECID)-Bibliothek 4.3.
seo-title: Unterstützung von Adobe Target und Apple ITP
solution: Target
subtopic: Erste Schritte
title: Apple ITP 2. x
topic: Standard
translation-type: tm+mt
source-git-commit: 71419ee6053eeb86ab6595cfba2f05d8506e05b3

---


# Apple Intelligent Tracking Prevention (ITP) 2. x

Intelligent Tracking Prevention (ITP) ist die Initiative von Apple zum Schutz der Privatsphäre von Safari-Benutzern. Die erste Version von ITP, die im Jahr 2017 veröffentlicht wurde, setzte die Verwendung von Drittanbieter-Cookies ein. In der Tat hat Apple Drittanbieter-Cookies blockiert, was wiederum zu einem schwerwiegenden Headleid für Werbetechniker und Technologieunternehmen führte, da Drittanbieter-Cookies allgemein zur Verfolgung von Besuchern und zur Erfassung von Besucherdaten eingesetzt werden. Jetzt ist Apple auf dem Weg, Einschränkungen und Einschränkungen hinsichtlich der Verwendung von Erstanbieter-Cookies in Safari zu platzieren.

Zu diesen Versionen von ITP gehören die folgenden Einschränkungen:

| Version | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Capped client-side cookies that are placed on the browser using the `document.cookie` API to a seven-day expiry.<br>Veröffentlicht am 21. Februar 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Der Ablauf von sieben Tagen wurde drastisch reduziert.<br>Veröffentlicht am 24. April 2019. |

## Welchen Einfluss hat ich als Adobe Target-Kunde?

[!DNL Target] stellt javascript-Bibliotheken bereit, die Sie auf Ihren Seiten bereitstellen [!DNL Target] können, damit Ihre Besucher personalisiert werden können. There are three Target JavaScript libraries ([at.js 1.*x* und at. js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)und [mbox. js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)), die clientseitige [!DNL Target] Cookies über die `document.cookie` API auf den Browsern Ihrer Besucher platzieren. As a result, [!DNL Target] cookies are impacted by Apple’s ITP 2.1 and 2.2 and will expire after seven days (with ITP 2.1) and after one day (with ITP 2.2).

Apple ITP 2.1 and 2.1 impact [!DNL Target] in the following areas:

| Wirkung | Details |
| --- | --- |
| Potenzielles Erhöhen der Anzahl individueller Besucher | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2) festgelegt wird, wird möglicherweise eine Erhöhung der Unique Visitors aus Safari-Browsern angezeigt. If your visitors revisit your domain after seven days (ITP 2.1) or one day (ITP 2.2), [!DNL Target] is forced to place a new [!DNL Target] cookie on your domain in place of the expired cookie. The new [!DNL Target] cookie translates to a new unique visitor even though the user is the same. |
| Decreased lookback periods for [!DNL Target] activities | Visitor profiles for [!DNL Target] activities might have a decreased lookback period for decisioning. [!DNL Target] Cookies werden genutzt, um einen Besucher zu erkennen und Benutzerprofilattribute zur Personalisierung zu speichern. Given that [!DNL Target] cookies can be expired on Safari after seven days (ITP 2.1) or one day (ITP 2.2), the user profile data that was tied to the purged [!DNL Target] cookie cannot be used for decisioning. |

## Is my current implementation of [!DNL Target] impacted?

In a Safari browser, navigate to your website on which you have a [!DNL Target] JavaScript library. If you see a [!DNL Target] cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

If you are using the Experience Cloud ID (ECID) library in addition to the Target JavaScript library, your implementation will be impacted in the ways listed in this article: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## How can I mitigate the impact of ITP 2.1, ITP 2.2, and future ITP releases to [!DNL Target]?

To mitigate the impact of ITP 2.1, ITP 2.2, and future ITP releases to [!DNL Target], complete the following tasks:

1. Stellen Sie die Experience Cloud ID (ECID)-Bibliothek auf Ihren Seiten bereit.

   Die ECID-Bibliothek ermöglicht das Identifizierungs-Framework für die Experience Cloud Core-Lösungen. Mit der ECID-Bibliothek können Sie dieselben Site-Besucher und deren Daten in verschiedenen Experience Cloud-Lösungen identifizieren, indem Sie beständige und eindeutige ids zuweisen. Die ECID-Bibliothek wird häufig aktualisiert, um alle ITP-bezogenen Änderungen abzuschwächen, die sich auf Ihre Implementierung auswirken.

   For ITP 2.1 and ITP 2.2, [ECID library 4.3.0+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) must be utilized for mitigation.

1. Verwenden Sie den CNAME und die Anmeldung von Adobe im Programm für verwaltete Zertifikate von Adobe Analytics.

   Nach der Installation der ECID-Bibliothek 4.3.0 + können Sie die CNAME- und Managed Certificate-Programme von Adobe Analytics nutzen. Mit diesem Programm können Sie Erstanbieter-Zertifikate für Erstanbieter-Cookies kostenlos implementieren. Leveraging CNAME will help [!DNL Target] customers mitigate the impact of ITP 2.1 and ITP 2.2.

   If you are not leveraging CNAME, you can start the process by talking with your account representative and enrolling in the [Adobe Managed Certificate Program](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html).

Nachdem Sie eine Javascript-Bibliothek von Target in Verbindung mit der ECID-Bibliothek Version 4.3.0 + bereitgestellt und im Adobe Managed Certificate-Programm angemeldet haben, erhalten Sie einen robusten und langfristigen Bereinigungsplan für ITP-bezogene Änderungen.

As the industry makes strides to create a more secure web for consumers, [!DNL Adobe Target] is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors. [!DNL Adobe Target] unterstützt bereits die Unterstützung von [Google samesite Chrome-Richtlinien](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) , zusätzlich zur Unterstützung von Apple ITP 2.1 und ITP 2.2.

As policies continue to evolve to protect our consumers, [!DNL Adobe] will also continue to support these initiatives in [!DNL Target], while helping our customers provide the best-in-class personalized experiences.
