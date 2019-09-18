---
description: Informationen zur Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID (ECID)-Bibliothek 4.3.
keywords: Apfel;ITP;Intelligente Verfolgungsverhütung
seo-description: Informationen zur Adobe Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID (ECID)-Bibliothek 4.3.
seo-title: ITP-Unterstützung für Adobe Target und Apple
solution: Target
subtopic: Erste Schritte
title: Apple ITP 2.x
topic: Standard
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Die Initiative "Intelligent Tracking Prevention"(ITP) von Apple zum Schutz der Privatsphäre von Safari-Benutzern. Die erste Version von ITP, die 2017 veröffentlicht wurde, zielte auf die Verwendung von Drittanbieter-Cookies ab. Tatsächlich blockierte Apple Cookies von Drittanbietern vollständig, was wiederum zu ernsthaften Kopfschmerzen für Werbe- und Technologieunternehmen führte, da Drittanbieter-Cookies in der Regel zur Verfolgung von Besuchern und zur Erfassung von Besucherdaten verwendet werden. Jetzt ist Apple dabei, Beschränkungen und Beschränkungen für die Verwendung von Erstanbieter-Cookies in Safari einzuführen.

Diese ITP-Versionen umfassen die folgenden Einschränkungen:

| Version | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Clientseitige Cookies, die mithilfe der `document.cookie` API im Browser platziert werden, wurden auf einen siebentägigen Ablauf geklickt.<br>Veröffentlicht am 21. Februar 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Die siebentägige Verfallskappe wurde auf einen Tag reduziert.<br>Veröffentlicht am 24. April 2019. |

## Welchen Einfluss habe ich als Adobe Target-Kunde?

[!DNL Target] bietet JavaScript-Bibliotheken, die Sie auf Ihren Seiten bereitstellen können, um Ihren Besuchern eine Echtzeit-Personalisierung zu ermöglichen. [!DNL Target] Es gibt drei Target-JavaScript-Bibliotheken ([at.js 1).*x* und at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)und [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)), die clientseitige [!DNL Target] Cookies über die `document.cookie` API in den Browsern Ihrer Besucher platzieren. Infolgedessen werden [!DNL Target] Cookies von den ITP 2.1 und 2.2 von Apple beeinflusst und laufen nach sieben Tagen (mit ITP 2.1) und nach einem Tag (mit ITP 2.2) ab.

Auswirkungen von Apple ITP 2.1 und 2.1 [!DNL Target] in den folgenden Bereichen:

| Wirkung | Details |
| --- | --- |
| Potenzielle Steigerung der Anzahl individueller Besucher | Da das Ablauffenster auf sieben Tage (mit ITP 2.1) und einen Tag (mit ITP 2.2) eingestellt ist, kann es zu einem Anstieg der Unique Visitors kommen, die von Safari-Browsern kommen. Wenn Ihre Besucher Ihre Domäne nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2) erneut aufrufen, [!DNL Target] wird gezwungen, anstelle des abgelaufenen Cookies ein neues [!DNL Target] Cookie in Ihrer Domäne zu platzieren. Das neue [!DNL Target] Cookie wird in einen neuen Unique Visitor übersetzt, obwohl der Benutzer identisch ist. |
| Reduzierte Lookback-Zeiträume für [!DNL Target] Aktivitäten | Besucherprofile für [!DNL Target] Aktivitäten weisen möglicherweise eine verkürzte Lookback-Zeit für die Entscheidungsfindung auf. [!DNL Target] Cookies werden zur Identifizierung eines Besuchers und zur Speicherung von Benutzerprofilattributen zur Personalisierung eingesetzt. Da [!DNL Target] Cookies in Safari nach sieben Tagen (ITP 2.1) oder einem Tag (ITP 2.2) abgelaufen sein können, können die Benutzerprofildaten, die mit dem bereinigten [!DNL Target] Cookie verknüpft waren, nicht für Entscheidungen verwendet werden. |

## Ist meine derzeitige Umsetzung [!DNL Target] davon betroffen?

Navigieren Sie in einem Safari-Browser zu Ihrer Website, auf der Sie über eine [!DNL Target] JavaScript-Bibliothek verfügen. Wenn Sie ein [!DNL Target] Cookie sehen, das im Kontext eines CNAME gesetzt wurde, z. B. `analytics.company.com`, sind Sie von ITP 2.1 oder 2.2 nicht betroffen.

Wenn Sie zusätzlich zur JavaScript-Bibliothek von Target die Experience Cloud ID (ECID)-Bibliothek verwenden, wird Ihre Implementierung auf die in diesem Artikel beschriebene Weise beeinträchtigt: Auswirkungen von [Safari ITP 2.1 auf Adobe Experience Cloud- und Experience Platform-Kunden](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Wie kann ich die Auswirkungen von ITP 2.1, ITP 2.2 und zukünftigen ITP-Versionen auf [!DNL Target]eindämmen?

Führen Sie die folgenden Aufgaben aus, um die Auswirkungen von ITP 2.1, ITP 2.2 und zukünftigen ITP-Versionen zu mildern [!DNL Target]:

1. Stellen Sie die Experience Cloud ID (ECID)-Bibliothek auf Ihren Seiten bereit.

   Die ECID-Bibliothek ermöglicht die Personenerkennung für Experience Cloud-Core-Lösungen. Mit der ECID-Bibliothek können Sie dieselben Site-Besucher und ihre Daten in verschiedenen Experience Cloud-Lösungen identifizieren, indem Sie beständige und eindeutige IDs zuweisen. Die ECID-Bibliothek wird regelmäßig aktualisiert, damit Sie alle Änderungen, die mit ITP in Zusammenhang stehen und sich auf Ihre Implementierung auswirken, eindämmen können.

   Für ITP 2.1 und ITP 2.2 muss die [ECID-Bibliothek 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) zur Abschwächung des Problems genutzt werden.

1. Verwenden Sie den CNAME und die Anmeldung von Adobe Analytics im Programm für verwaltete Zertifikate.

   Nach der Installation der ECID-Bibliothek 4.3.0+ können Sie das Adobe Analytics-Programm für CNAME und verwaltete Zertifikate nutzen. Mit diesem Programm können Sie ein Erstanbieter-Zertifikat für Erstanbieter-Cookies kostenlos implementieren. Die Nutzung von CNAME hilft [!DNL Target] Kunden, die Auswirkungen von ITP 2.1 und ITP 2.2 zu mindern.

   Wenn Sie CNAME nicht verwenden, können Sie den Prozess starten, indem Sie mit Ihrem Kundenbetreuer sprechen und sich im [Adobe Managed Certificate-Programm](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program)anmelden.

Nachdem Sie eine Target-JavaScript-Bibliothek in Verbindung mit der ECID-Bibliothek v4.3.0+ bereitgestellt und sich beim Adobe Managed Certificate-Programm für die Nutzung von CNAME angemeldet haben, verfügen Sie über einen robusten und langfristigen Abmilderungsplan für Änderungen im Zusammenhang mit ITP.

As the industry makes strides to create a more secure web for consumers, [!DNL Adobe Target] is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors. [!DNL Adobe Target] hat bereits die Unterstützung für die SameSite-Chrome-Richtlinien[ von ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md)Google angekündigt, zusätzlich zur Unterstützung von ITP 2.1 und ITP 2.2 von Apple.

Da sich die Richtlinien zum Schutz unserer Verbraucher weiterentwickeln, [!DNL Adobe] werden sie diese Initiativen auch weiterhin unterstützen [!DNL Target]und unseren Kunden dabei helfen, die besten personalisierten Erlebnisse zu bieten.
